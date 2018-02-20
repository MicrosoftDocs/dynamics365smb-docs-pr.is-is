---
title: "Hönnunarupplýsingar - Bókun framleiðslupöntunar | Microsoft Docs"
description: "Svipað bókun samsetningarpöntununar er notuðum íhlutum og notuðum vélartíma umreiknað og skilað sem framleiddri vöru þegar framleiðslupöntuninni er lokið."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: bd25ed0204ee0e96e258974dc03d29aea44b67e6
ms.contentlocale: is-is
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-production-order-posting"></a>Hönnunarupplýsingar: staða framleiðslupöntunar
Svipað bókun samsetningarpöntununar er notuðum íhlutum og notuðum vélartíma umreiknað og skilað sem framleiddri vöru þegar framleiðslupöntuninni er lokið. Frekari upplýsingar, sjá [Hönnunarupplýsingar: bókun samsetningarpöntunar](design-details-assembly-order-posting.md). Hins vegar er kostnaðarrennsli fyrir samsetningarpantanir síður flókið, sérstaklega vegna þess að bókun samsetningarkostnaðar á sér aðeins stað einu sinni og myndar því ekki birgðir með verkum í vinnslu.


Færslur sem eiga sér stað á meðan á framleiðsluferlinu má rekja í gegnum eftirfarandi stig:  

1.  Efniskaup og annað framleiðsluinntak.  
2.  Umreikningur í verk í vinnslu  
3.  Umreikningur í birgðir fullunninar vöru.  
4.  Sala á fullunnar vörum.  

Því, fyrir utan venjulega birgðarreikninga, þarf framleiðslufyrirtæki að stofna þrjá mismunandi birgðarreikninga til að skrá færslur á mismunandi framleiðslustigum.  

|Reikningur birgða|Description|  
|-----------------------|---------------------------------------|  
|**Hráefnisreikningur**|Felur í sér kostnað við hráefni sem eru keypt en ekki enn flutt til framleiðslu. Staða hráefnareiknings gefur til kynna kostnað hráefna á lager.<br /><br /> Þegar hráefni færast inn á framleiðslusviðið er kostnaður hráefnis fluttur af hráefnisreikningi yfir í VÍV-reikningur.|  
|**Verk í vinnslu (VÍV) reikningur**|Safnar saman kostnaði sem fellur til við framleiðslu á reikningstímabilinu. VÍV-reikningurinn er debetfærður fyrir kostnað hráefna sem eru flutt úr vöruhúsi hráefna, kostnað við vinnu og rekstrarkostnað við framleiðslu sem stofnað hefur verið til.<br /><br /> VÍV-reikningur er kreditfærður fyrir öllum framleiðslukostnaði eininga sem er lokið í verksmiðju og fluttar í vöruhús fullbúinna vara.|  
|**Fullunnar vörur**|Þessir reikningar innihalda heildar framleiðslukostnað eininga sem hefur verið lokið en hafa ekki verið seldar. Á þeim tíma sem sala, kostnaður við einingar seldar er flutt úr fullunnar vörur í kostnaður seldra vara.|  

Verðmæti birgða er reiknað út með því að rekja kostnað við alla hækkun og minnkun eins og hún birtist í eftirafaandi jöfnu:  

* birgðavirði = uppjafsjöfnun birgða + virði allra hækkana - virði allra lækkun  

Það fer eftir tegund af birgðum, hækkun og lækkun veltja á mismunandi færslum.  

||Aukist|Minnkar|  
|-|---------------|---------------|  
|**Hráefnisbirgðir**|-   Nettóinnkaup á efni<br />-   Frálag undirsamsetninga<br />-   Neikvæð notkun|Efnisnotkun|  
|**VÍV-birgðir**|-   Efnisnotkun<br />-   Afkastaveita<br />-   Sameiginl. kostn. framleiðslu|Frálag lokavara (kostnaður framleiddra vara)|  
|**Fullunnar vörur í birgðum**|Frálag lokavara (kostnaður framleiddra vara)|-   Sala (Kostnaður seldra vara)<br />-   Framleiðsluslaki|  
|**Hráefnisbirgðir**|-   Nettóinnkaup á efni<br />-   Frálag undirsamsetninga<br />-   Neikvæð notkun|Efnisnotkun|  

Gildi aukningar og minnkunar eru skráð í mismunandi gerðum framleiddra birgða á sama hátt og fyrir keyptar birgðir. Í hverst sinn sem færsla með birgðaaukningu eða birgðaminnkun fer fram er búin til birgðafærsla og samsvarandi fjárhagsfærsla fyrir upphæðina. Nánari upplýsingar, sjá [Upplýsingar um hönnun: Birgðabókun](design-details-inventory-posting.md)  

Þótt virði færslna sem eru tengdar keyptum vörum séu bókuð aðeins sem birgðahöfuðbókarfærslur með tengdum virðisfærslum eru færslur sem eru tengdar framleiddum vörum bókaðar sem afkastahöfuðbókarfærslur með tengdum virðisfærslum, með birgðarhöfuðbókarfærslunum.  

## <a name="posting-structure"></a>Bókunaruppbygging  
Bókun framleiðslupantana í VÍV-birgðir samanstendur af frálagi, notkun og afkastaveitu.  

Eftirfarandi skýringarmynd sýnir bókunarvenjur í kóðaeiningu 22.  

![Vanalegar bókanir birgðapantana](media/design_details_inventory_costing_14_production_posting_1.png "hönnunarupplýsingar_birgðakostnaður_14_bókun_1")  

Eftirfarandi skýringarmynd sýnir tengsl milli leiðir afleiddra færsla og kostnaðarhluta.  

![Flæði framleiðslufærslna](media/design_details_inventory_costing_14_production_posting_2.png "hönnunarupplýsingar_birgðakostnaður_14_framleiðsla_bókun_2")  

Afkastagetufærsla lýsir getuneyslu hvað varðar tímaeiningar, en tengdar gildifærsla lýsir verðmæti tilteknum getuneyslu.  

Birgðafærslan lýsir efnislegri notkun eða framleiðslu að því er varðar magn, en tengd virðisfærsla lýsir virði þessarar tilteknu notkunar á efni eða framleiðslu.  

Virðisfærsla sem lýsir VÍV-birgðavirði er hægt að tengaj við eina af eftirfarandi samsetningum kostnaðarhluta:  

-   Framleiðslupöntunarlína, vinnu- eða vélastöð og afkastahöfuðbókarfærsla.  
-   Framleiðslupöntunarlína, vara og birgðafærsla.  
-   Aðeins framleiðslupöntunarlína  

Upplýsingar um hvernig kostnaður frá samsetningu og framleiðslu eru bókaðar í fjárhag, sjá [Hönnunarupplýsingar: birgðabókun](design-details-inventory-posting.md).  

## <a name="capacity-posting"></a>Afkastagetubókun  
Bókun frálags úr leiðarlínu síðustu framleiðslupöntunar skilar afkastahöfuðbókarfærslu fyrir lokavöru, auk birgðaaukningar.  

 Afkastahöfuðbókfærsla er skrá yfir þann tíma sem var varið til að framleiða vöruna. Tengda virðisfærslan lýsir hækkun á VÍV-virði birgða, sem er virði umbreytingakostnaðar. Frekari upplýsingar, sjá „Frá afkastahöfuðbók í [Hönnunarupplýsingar: reikningar í fjárhagur](design-details-accounts-in-the-general-ledger.md)  

## <a name="production-order-costing"></a>Kostnaður framleiðslupöntunar  
 Til að stjórna birgða -og framleiðslukostnaði, framleiðsla fyrirtæki verða að meta kostnað við að framleiðslupantanir, vegna þess að fyrirfram ákveðna staðlaða kostnaður við hvert framleitt hlut er eignfærður í efnahagsreikningi. Upplýsingar um hvers vegna framleiddar vörur notar staðalaðferð kostnaðarútreiknings eru í [Hönnunarupplýsingar: Kostnaðaraðferðir](design-details-costing-methods.md).  

> [!NOTE]  
>  Í umhverfi sem ekki notar staðlaða kostnaðarútreikning er  raun- frekar en staðalkostnaður við framleidda vörur eignfærður í efnahagsreikningi.  

Raunkostnaður framleiðslupöntunar samanstendur af eftirfarandi kostnaðarþáttum:  

-   Raunkostnaður var  
-   Raunverulegur afkastaveitukostnaður eða kostnaður vegna undirverktaka  
-   Sameiginl. kostn. framleiðslu  

Raunkostnaður er bókaður á framleiðslupöntunina og borinn saman við staðalkostnað til að reikna frávik. Frávik eru reiknuð fyrir hvern vörukostnaðaríhlut: hráefni, afköst, undirverktaka, sameiginlegan kostnað afkastaveitu og framleiðslukostnað. Hægt er að greina frávik til að ákvarða vandamál, t.d. of miklum úrgangi við framleiðslu.  

Í staðalkostnaðarumhverfi er kostnaður framleiðslupöntunar byggt á eftirfarandi kerfi:  

1.  Þegar síðasta leiðaraðgerð er bókuð er framleiðslupöntunarkostnaðurinn bókaður í birgðahöfuðbók og stilltur á áætlaður kostnaður.  

    Kostnaðurinn er jafn og magn á útleið sem er bókað í frálagsbók margfaldað með staðalkostnaðinum sem er afritaður af birgðaspjaldinu. Kostnaðurinn er meðhöndlaður sem áætlaður kostnaður þar til framleiðslupöntun er lokið. Frekari upplýsingar, sjá [Hönnunarupplýsingar: Væntanleg kostnaðarfærsla](design-details-expected-cost-posting.md).  

    > [!NOTE]  
    >  Þetta er frábrugðið færslum samsetningarpöntunar, þar sem raunkostnaður er alltaf bókaður. Frekari upplýsingar, sjá [Hönnunarupplýsingar: bókun samsetningarpöntunar](design-details-assembly-order-posting.md).  
2.  Þegar framleiðslupöntun er stillt á **fullunninn** er hún reikningsfærð með því að keyra runuvinnsluna **Leiðr. kostnað-Birgðafærslur**. Niðurstaðan er sú að heildarkostnaður pöntunar er reiknaður samkvæmt stöðluðum kostnaði notaðra efna og afkasta. Frávik frá reiknuðum staðalkostnaði og raunverulegum framleiðslukostnaði eru reiknuð og bókuð.  

## <a name="see-also"></a>Sjá einnig  
 [Hönnunarupplýsingar: Birgðakostnaður](design-details-inventory-costing.md)   
 [Hönnunarupplýsingar: Bókun samsetningarpöntunar](design-details-assembly-order-posting.md)  
 [Birgðakostnaði stjórnað](finance-manage-inventory-costs.md) [Fjármál](finance.md)  
 [Unnið með Financials](ui-work-product.md)

