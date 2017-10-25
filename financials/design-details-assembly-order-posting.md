---
title: "Hönnunarupplýsingar - Bókun samsetningarpöntunar | Microsoft Docs"
description: "Bókun samsetningarpöntunar er byggð á sömu forsendum og bókun svipaðra aðgerða sölupantana og notkun/frálag framleiðslu. Hins vegar eru reglur sameinaðar að því leyti að samsetningarpantanir eru með eigið bókunarviðmót eins og fyrir sölupantanir á meðan raunveruleg bókun færslna fer fram í bakgrunninum sem beinar vöru- og forðabókarbókanir, eins og fyrir framleiðslunotkun, framleiðslu og afkastagetu."
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
ms.openlocfilehash: 66590eb8ce7749658bad1fc3c9e54c1dff538abd
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-assembly-order-posting"></a>Hönnunarupplýsingar: Bókun samsetningarpöntunar
Bókun samsetningarpöntunar byggir á sömu meginreglum og þegar bókun tengist sambærilegum aðgerðum á borð við sölupantanir og notkun/frálag framleiðslu. Hins vegar eru reglur sameinaðar að því leyti að samsetningarpantanir eru með eigið bókunarviðmót eins og fyrir sölupantanir á meðan raunveruleg bókun færslna fer fram í bakgrunninum sem beinar vöru- og forðabókarbókanir, eins og fyrir framleiðslunotkun, framleiðslu og afkastagetu.  

Svipað bókun framleiðslupöntunar er notuðum íhlutum og notuðum tilföngum umreiknað og skilað sem samsetningarvara þegar samsetningarpöntunin er bókuð. Frekari upplýsingar eru í [Hönnunarupplýsingar: staða framleiðslupöntunar](design-details-production-order-posting.md). Hins vegar er kostnaðarrennsli fyrir samsetningarpantanir síður flókið, sérstaklega vegna þess að bókun samsetningarkostnaðar á sér aðeins stað einu sinni og myndar því ekki birgðir með verkum í vinnslu.  

Eftirfarandi bókarfærslur komu til við bókun samsetningarpöntunar:  

-   Birgðabókin bókar jákvæðar birgðafærslur sem sýna framleiðslu samsetningarvörunnar úr samsetningarpöntunarlínunum.  
-   Birgðabókin bókar neikvæðar birgðafærslur sem sýna notkun samsetningaríhluta úr samsetningarpöntunarlínunum.  
-   Notkun forðabókarfærslna á samsetningartilföngum (tímaeiningum) af samsetningarpöntunarlínum.  
-   Afkastagetubók bókar gildifærslur í tengslum við tilfanganotkun, frá samsetningarpöntunarlínum.  

Eftirfarandi skýringarmynd sýnir uppbyggingu vöru og fjárhagsfærslur tilfanga vegna bókum samsetningarpöntunar.  

![Kostnaður við tilföng og afkastaveitu](media/design_details_assembly_posting_1.png "design_details_assembly_posting_1")  

> [!NOTE]  
>  Vinnuvél og vinnustöðvar eru teknar með til að sýna að afkastahöfuðbókarfærslur eru stofnaðar úr bæði framleiðslu og samsetningu.  

Eftirfarandi skýringarmynd sýnir hvernig samsetningargögn flæða fjárhagsfærslur við bókun:  

![Gagnaflæði á meðan á bókun stendur](media/design_details_assembly_posting_2.png "design_details_assembly_posting_2")  

## <a name="posting-sequence"></a>Bókunarröð  
Til að bókun samsetningarpöntunar á sér stað í þessari röð:  

1.  Samsetningarpöntunarlínurnar eru bókaðar.  
2.  Samsetningarpöntunarhausinn er bókaður.  

Eftirfarandi tafla sýnir röð aðgerða.  

|Aðgerð|Description|  
|------------|-----------------|  
|Frumstilla bókun|1.  Framkvæmið forskoðanir.<br />2.  Bætið við bókunarnúmeri og breytið samsetningarpöntunarhausnum.<br />3.  Losa samsetningarpöntun.|  
|Færsla|<ol><li>Stofna bókaðan samsetningarpöntunarhaus.</li><li>Afrita athugasemdarlínur.</li><li>Bóka samsetningarpöntunarlínur (notkun):<br /><br /> <ol><li>Stofna stöðuglugga til að reikna notkun við samsetningu.</li><li>Fá eftirstandandi magn sem birgðabókarlínan verður byggð á.</li><li>(Núllstilla notað magn og eftirstandandi magn.</li><li>Fyrir samsetningarpöntunarlínur af gerðinni Vara:<br /><br /> <ol><li>Fylla út reitina birgðabókarlínunni.</li><li>Millifærslufrátekningar í birgðabókarlínu</li><li>Bóka birgðahöfuðbókarlínuna til að stofna birgðafærslurnar.</li><li>Stofna vöruhúsabókarlínur og bóka þær.</li></ol></li><li>Fyrir samsetningarpöntunarlínur af gerðinni Forði:<br /><br /> <ol><li>Fylla út reitina birgðabókarlínunni.</li><li>Bókið birgðabókarlínuna. Þetta stofnar afkastagetufærslur.</li><li>Stofna og bóka forðabókarlínu.</li></ol></li><li>Reitargildi millifærslu frá samsetningarpöntunarlínu í nýstofnaða bókaða samsetningarpöntunarlínu.</li></ol></li><li>Bóka samsetningarpöntunarhaus (frálag):<br /><br /> <ol><li>Fylla út reitina birgðabókarlínunni.</li><li>Millifærslufrátekningar í birgðabókarlínu</li><li>Bóka birgðahöfuðbókarlínuna til að stofna birgðafærslurnar.</li><li>Stofna vöruhúsabókarlínur og bóka þær.</li><li>Núllstilla samsetningarmagn og eftirstandandi magn.</li></ol></li></ol>|  

> [!IMPORTANT]  
>  Ólíkt framleiðslufrálagi, sem bókað er á áætluðum kostnaði, er samsetningarfrálag bókað  á raunkostnaði.  

## <a name="cost-adjustment"></a>Leiðrétta kostnað  
 Þegar samsetningarpöntun hefur verið bókuð, allir íhlutir (efni) og forði eru samsett í nýrri vöru, ætti að vera hægt að ákvarða raunverulegan kostnað samsetningarvöru og raunverulegan birgðakostnað viðkomandi íhluta. Þessu er náð fram með því að framsenda kostnað frá bókuðum færslum uppruna (íhluta og tilfanga) í bókaðar færslur endastaðar (samsetningarvöru). Framsending kostnaðar er framkvæmd með útreikningi og myndun nýrra færslna sem kallast leiðréttingarfærslur sem munu viðtökufærslunum.  

 Samsetningarkostnaður sem á framsenda greindist með greiningarbúnaði fyrir pöntunarstig. Upplýsingar um aðrar leiðir til leiðréttingargreiningar eru í [Hönnunarupplýsingar: Kostnaðarleiðrétting](design-details-cost-adjustment.md).  

### <a name="detecting-the-adjustment"></a>Borin kennsl á leiðréttingu  
Greiningaraðgerðin á pantanastigi er notuð í umbreytingaraðstæðum, framleiðslu og samsetningu. Aðgerðin virkar á eftirfarandi hátt:  

-   Kostnaðarleiðrétting er merkt með því að merkja pöntunina þegar efni/tilfang er bókaður sem neytt/notað.  
-   Kostnaðarframsending á sér stað með því að beita kostnaðinum úr efninu/forða á frálagsfærslur sem tengjast pöntuninni.  

Eftirfarandi mynd sýnir leiðréttingarfærsluuppbyggingu og hvernig samsetningarkostnaður er leiðréttur.  

![Bygging leiðréttingarfærslu](media/design_details_assembly_posting_3.png "design_details_assembly_posting_3")  

### <a name="performing-the-adjustment"></a>Leiðrétting  
Dreifing greindra breytinga á efni og tilfangakostnaði í samsetningarúttaksfærslum er framkvæmd í runuvinnslunni **Leiðr. kostnað – Birgðafærslur**. Það inniheldur aðgerðina gera margstiga jöfnun, sem samanstendur af eftirfarandi tveimur þáttum:  

-   Leiðrétta samsetningarpöntun – framsendir kostnað vegna efnis og forða í samsetningfrálagsfærslu. Línur 5 og 6 í reiknireglunni hér að neðan eru ábyrgar fyrir því.  
-   Leiðréttingar á einu stigi – framsendir kostnað fyrir stakar vörur með viðkomandi aðferð kostnaðarútreiknings. Línur 9 og 10 í reikniriti hér á eftir eru ábyrgar fyrir því.  

![Reiknirit fyrir samsetningarleiðréttingu](media/design_details_assembly_posting_4.jpg "design_details_assembly_posting_4")  

> [!NOTE]  
>  Einingin Gera VÍV-leiðréttingu, í línum 7 og 8, er ábyrg fyrir að framsenda framleiðsluefni og notkukn á afkastagetu í frálag ólokinna framleiðslupantana. Þetta er ekki notað þegar kostnaði samsetningarpöntunar er breytt þar sem VÍV gildir ekki um samsetningu.  

Upplýsingar um hvernig kostnaður frá samsetningu og framleiðslu eru bókaðar í fjárhagur, sjá [Hönnunarupplýsingar: birgðabókun](design-details-inventory-posting.md).  

## <a name="assembly-costs-are-always-actual"></a>Samsetningarkostnaður er alltaf raunverulegur  
 Hugmyndin um verk í vinnslu (VÍV) gildir ekki í bókun samsetningarpöntunar. Samsetningarkostnaður er aðeins bókaður sem raunverulegur kostnaður, aldrei áætlaður kostnaður. Frekari upplýsingar, sjá [Hönnunarupplýsingar: Væntanleg kostnaðarfærsla](design-details-expected-cost-posting.md).  

Þetta næst með eftirfarandi gagnastrúktúr.  

-   Í **Tegund** reitnum á birgðabókarlínum, í töflunum **Afkastabókarfærsla** og **Virðisfærsla**, *Forði* er notað til að auðkenna samsetningarforðafærslur.  
-   Í reitnum  **færslugerð birgðabókar** á birgðabókarlínum í töflunum **Afkastabókarfærsla** og **Virðisfærsla** er *Samsetningarfrálag* og *Samsetningarnotkun* eru notuð til að bera kennsl á vörufærslur úttakssamsetningar og notaða samsetningaríhlutarfærslur.  

Að auki, bókunarflokkur reitir á samsetningarpöntunarhaus og samsetningarpöntunarlína er fyllt út sjálgefið svona:  

|Lögaðili|Tegund|VSK-vörubókunarfl.|Alm. vörubókunarflokkur|  
|------------|----------|-------------------|------------------------------|  
|Samsetningarpöntunarhaus|Vara|Birgðabókunarflokkur|Alm. vörubókunarflokkur|  
|Samsetningarpöntunarlína|Vara|Birgðabókunarflokkur|Alm. vörubókunarflokkur|  
|Samsetningarpöntunarlína|Forði||Alm. vörubókunarflokkur|  

Í samræmi er eingöngu raunverulegur kostnaður bókara í fjárhag og engir bráðabirgðareikningar eru útfylltir úr bókun samsetningarpöntunar. Frekari upplýsingar, sjá [Hönnunarupplýsingar: reikningar í fjárhagur](design-details-accounts-in-the-general-ledger.md)  

## <a name="assemble-to-order"></a>Samsetning til pöntunar  
Birgðafærslan sem myndast við bókun á sölu fyrir samsetningu-til-pöntunar er fastjöfnuð við tengda birgðafærslu fyrir samsetningarfrálagið. Í samræmi við það, er kostnaður við samsetningarpöntunarsölu fenginn úr samsetningarpöntun sem hún var tengd við.  

Birgðahöfuðbókarfærslur af gerðinni Sala, sem leiða af bókun magns sem er sett saman í pöntun, eru merktar með **Já** í reitnum **Setja saman í pöntun**.  

Bókun sölupantanalína þar sem einn hluti er birgðamagn og annar er magn samsetningarpöntunar býr til aðskildar birgðabókarfærslur; eina fyrir birgðamagn og aðra fyrir magn samsetningarpöntunar.  

## <a name="see-also"></a>Sjá einnig  
 [Hönnunarupplýsingar: Birgðakostnaður](design-details-inventory-costing.md)   
 [Hönnunarupplýsingar: staða framleiðslupöntunar](design-details-production-order-posting.md)   
 [Hönnunarupplýsingar: Aðferð kostn.útreiknings](design-details-costing-methods.md)  
 [Birgðakostnaði stjórnað](finance-manage-inventory-costs.md)  
 [Fjármál](finance.md)  
 [Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

