---
title: Hvernig á að úthýsa framleiðslu til undirverktaka | Microsoft Docs
description: Þegar innkaupapöntunin hefur verið stofnuð í Vinnublaði undirverktaka er hægt að bóka hana.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: e3d72eecf3f0d4e92b0255dffdece8dcb795cf96
ms.sourcegitcommit: 319023e53627dbe8e68643908aacc6fd594a4957
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/04/2019
ms.locfileid: "2553795"
---
# <a name="subcontract-manufacturing"></a>Úthýsa framleiðslu til undirverktaka
Úthýsing á völdum aðgerðum til lánardrottna er algeng í mörgum framleiðslufyrirtækjum. Undirverktakastarfsemi getur verið sjaldgæf hending eða mikill þáttur í öllum framleiðsluferlum.

[!INCLUDE[d365fin](includes/d365fin_md.md)] býður upp á nokkur verkfæri til að sjá um starfsemi undirverktaka:  

- Vinnustöðvar með úthlutaðan lánardrottin: Þessi aðgerð gerir það mögulegt að setja upp vinnustöð sem er tengd lánardrottni (undirverktaka). Þetta heitir vinnustöð undirverktaka. Hægt er að tiltaka vinnustöð undirverktaka í leiðaraðgerð, sem gerir það mögulegt að meðhöndla undirverktakastarfsemina auðveldlega. Þar að auki er hægt að ákvarða kostnað aðgerðarinnar á leiðar- eða vinnustöðvarstiginu.  
- Kostnaður vinnustöðvar byggt á einingum eða tíma: Þessi aðgerð gerir það mögulegt að taka fram hvort kostnaður tengdur vinnustöðinni er byggður á framleiðslutímanum eða flatt gjald fyrir hverja einingu. Þó svo að undirverktakar noti yfirleitt flatt gjald fyrir hverja einingu til að fá borgað fyrir þjónustu sína getur forritið ráðið við báða valkosti (framleiðslutíma og flatt gjald fyrir hverja einingu).  
- Vinnublað undirverktakasamnings: Þessi aðgerð gerir það mögulegt að finna framleiðslupantanir með efni sem er tilbúið til sendingar til undirverktaka og að búa sjálfkrafa til innkaupapantanir fyrir aðgerðir undirverktaka frá leiðum framleiðslupöntunar. Þá bókar forritið sjálfkrafa gjöldin fyrir innkaupapöntunina á framleiðslupöntunina á meðan á bókun innkaupapöntunarinnar stendur. Aðeins er hægt að fá aðgang að og nota framleiðslupantanir sem hafa stöðuna útgefin á vinnublaði undirverktaka.  

## <a name="subcontract-work-centers"></a>Vinnustöðvar undirverktaka  
Vinnustöðvar undirverktaka eru  settar upp eins og venjulegar vinnustöðvar með viðbótarupplýsingar. Þeim er úthlutað á leiðir á sama hátt og aðrar vinnustöðvar.  

### <a name="subcontract-work-center-fields"></a>Reitir vinnustöðva undirverktaka  
Þessi reitur,  **Undirverktakanr.**, táknar vinnustöðina sem vinnustöð undirverktaka. Hægt er að rita númer undirverktaka sem sér um vinnustöðina. Hægt er að nota þennan reit til að sjá um vinnustöðvar sem ekki eru á staðnum en eru í vinnslu samkvæmt verksamningi.  

Ef gerður er undirverktakasamningur við lánardrottininn um mismunandi taxta fyrir hvert ferli þá er hægt að velja reitinn **Tiltekið kostnaðarverð**. Þetta gerir það mögulegt að setja upp kostnað á hverja leiðarlínu og sparar þann tíma sem færi í að slá aftur inn hverja innkaupapöntun. Kostnaðurinn í leiðarlínunni er notaður í vinnslu frekar en kostnaðurinn í kostnaðarreitum vinnustöðvarinnar. Með því að velja **Tiltekið kostnaðarverð** reitinn er reiknaður út kostnaður fyrir lánardrottininn með leiðaraðgerðinni.  

Ef gerður er undirverktakasamningur um einn taxta fyrir hvern birgja skal reiturinn **Tiltekið kostnaðarverð** látinn vera auður. Kostnaðurinn er settur upp með því að fylla í reitina **Innkaupaverð** , **Óbein kostnaðar %** og **Hlutfall sameiginlegs kostnaðar**.  

### <a name="routings-that-use-subcontract-work-centers"></a>Leiðir sem nota Vinnustöðvar undirverktaka  
Hægt er að nota Vinnustöðvar verktaka fyrir aðgerðir á leiðum á  sama hátt og venjulegar vinnustöðvar.  

Hægt er að setja upp leið sem notar utanaðkomandi vinnustöð sem staðlað aðgerðarskref. Hægt er líka að breyta leiðinni fyrir tiltekna framleiðslupöntun til að hún nái yfir utanaðkomandi aðgerð. Þetta gæti verið nauðsynlegt í neyðartilfellum eins og þegar þjónn bilar eða á afmörkuðu tímabili hærri eftirspurnar þegar senda þarf verk sem er yfirleitt unnið innanhúss til undirverktaka.  

Nánari upplýsingar eru í [Stofna leiðir](production-how-to-create-routings.md).  

## <a name="calculate-subcontracting-worksheets-and-create-subcontract-purchase-orders"></a>Reikna vinnublöð undirverktakasamninga og stofna innkaupapantanir fyrir undirverktaka  
Þegar búið er að reikna út Vinnublað undirverktaka er viðeigandi skjal, í þessu tilfelli innkaupapöntun, stofnuð.  

Síðan **Vinnublað undirverktakasamninga** virkar eins og **Áætlunarvinnublað** með því að reikna út framboð sem þarf, í þessu tilfelli innkaupapantanir, sem er endurskoðað í vinnublaðinu og síðan stofnað með aðgerðinni **Framkvæma aðgerðarboð**.  

> [!NOTE]  
>  Aðeins er hægt að fá aðgang að og nota framleiðslupantanir sem hafa stöðuna **Útgefin** á vinnublaði undirverktaka.  

### <a name="to-calculate-the-subcontracting-worksheet"></a>Útreikningur Vinnublaðs undirverktakasamnings  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **vinnublað undirverktakasamninga** og veldu síðan tengda tengilinn.  
2.  Til að reikna út vinnublaðið er smellt á aðgerðina **Útreikningur verktakasamninga**.  
3.  Á síðunni **Reikna út undirverktaka** er hægt að stilla afmarkanir fyrir aðgerðir undirverktaka eða vinnustöðvar þar sem þær eru framkvæmdar til að reikna aðeins viðeigandi framleiðslupantanir.  
4.  Velja hnappinn **Í lagi**.  

    Fara yfir línurnar á síðunni **Vinnublað undirverktakasamninga**. Upplýsingarnar á þessu vinnublaði koma frá framleiðslupöntuninni og leiðarlínum framleiðslupöntunarinnar og flæðir til innkaupapöntunarinnar þegar það skjal er búið til. Hægt er að eyða röð úr vinnublaðinu án þess að hafa áhrif á upphaflegu upplýsingarinnar, líkt og gert er við önnur vinnublöð. Upplýsingarnar birtast aftur í næsta skipti sem aðgerðin **Reikna undirverktakasamninga** er keyrð.  

### <a name="to-create-the-subcontract-purchase-order"></a>Að búa til Framleiðslupöntun undirverktakans  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **vinnublað undirverktakasamninga** og veldu síðan tengda tengilinn.  
2.  Veljið aðgerðina **Framkvæma aðgerðaboð**.  
3.  Hakað er í reitinn **Prenta pantanir** til að prenta innkaupapöntunina þegar hún er stofnuð.  
4.  Velja hnappinn **Í lagi**.  

Ef senda á allar undirverktakaaðgerðir til birgðageymslu sama birgja þá er aðeins ein innkaupapöntun gerð.  

Vinnublaðslínunni sem var breytt í innkaupapöntun er eytt af vinnublaðinu. Þegar innkaupapöntun er stofnuð, mun hún ekki birtast á vinnublaðinu aftur.  

## <a name="posting-subcontract-purchase-orders"></a>Bókun innkaupapantana undirverktaka  
Þegar Innkaupapantanir undirverktaka hafa verið stofnaðar er hægt að bóka þær. Við móttöku pöntunarinnar bókast Afkastagetufærsla á framleiðslupöntunina og þegar reikningur er gerður bókast beinn kostnaður af innkaupapöntuninni á framleiðslupöntunina.  

Forritið bókar sjálfkrafa færslu frálagsbókarlínu fyrir framleiðslupöntunina þegar tekið er á móti innkaupapöntuninni. Þetta á aðeins við ef undirverktakakaaðgerðin er síðasta aðgerðin á leið framleiðslupöntuninni.  

> [!CAUTION]  
>  Bókar frálag sjálfkrafa fyrir framleiðslupöntun sem er í gangi, þegar úthýstar vörur sem mótteknar eru, eru óæskilegar. Ástæðan fyrir þessu gæti verið að afkastamagnið sem bókað er gæti verið annað en raunverulega magnið og að bókunardagsetningin á sjálfvirka frálaginu sé villandi.  
>   
>  Til að forðast að áætlað frálag framleiðslupöntunar sé bókað þegar innkaup undirverktaka eru móttekin, sjáið til þess að undirverktakakaaðgerðin sé ekki sú síðasta. Að öðrum kosti er færð inn ný lokaaðgerð fyrir loka frálagsmagnið.

## <a name="to-post-a-subcontract-purchase-order"></a>Til að bóka innkaupapöntun undirverktaka  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innkaupapantanir** og veldu síðan tengda tengilinn.  
2.  Opna innkaupapöntun sem er stofnaður frá undirverktakasamningi.  

    Á innkaupapöntunarlínunum má sjá sömu upplýsingar og þær sem voru í vinnublaðinu. Reitirnir **Framl.pöntun nr.**, **Framl.pöntunarlínunr.**, **Aðgerðarnr.** og **Vinnustöðvarnr.** eru fylltir út með upplýsingunum úr upprunaframleiðslupöntun.  

3.  Valið er **Bóka** aðgerðin.  

Forritið bókar sjálfkrafa færslu frálagsbókarlínu fyrir framleiðslupöntunina þegar tekið er á móti innkaupapöntuninni. Þetta á aðeins við ef undirverktakakaaðgerðin er síðasta aðgerðin á leið framleiðslupöntuninni.  

> [!CAUTION]  
>  Bókar frálag sjálfkrafa fyrir framleiðslupöntun sem er í gangi, þegar úthýstar vörur sem mótteknar eru, eru óæskilegar. Ástæðan fyrir þessu gæti verið að afkastamagnið sem bókað er gæti verið annað en raunverulega magnið og að bókunardagsetningin á sjálfvirka frálaginu sé villandi.  
>   
>  Til að forðast að áætlað frálag framleiðslupöntunar sé bókað þegar innkaup undirverktaka eru móttekin, sjáið til þess að undirverktakakaaðgerðin sé ekki sú síðasta. Að öðrum kosti er færð inn ný lokaaðgerð fyrir loka frálagsmagnið.  

Beinn kostnaður innkaupapöntunarinnar er bókaður í framleiðslupöntunina þegar innkaupapöntunin er reikningsfærð.  

## <a name="see-also"></a>Sjá einnig  
[Framleiðsla](production-manage-manufacturing.md)    
[Uppsetning framleiðslu](production-configure-production-processes.md)  
[Áætlun](production-planning.md)      
[Birgðir](inventory-manage-inventory.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
