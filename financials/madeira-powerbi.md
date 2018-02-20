---
title: Efnispakkar Finance and Operations, Business Edition og Power BI| Microsoft Docs
description: "Það er auðvelt að fá innsýn, viðskiptagreind og afkastavísi (KPI) í Finance and Operations, Business Edition gögnum með Power BI og Finance and Operations, Business Edition efnispökkunum."
author: edupont04
ms.service: dynamics365-financials
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 09/05/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 61d339e584107d48e22bd4c250085e9468271d7e
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---
# <a name="enabling-your-business-data-for-power-bi"></a>Virkja viðskiptagögnin þín fyrir Power BI
Það er auðvelt að fá innsýn í [!INCLUDE[d365fin](includes/d365fin_md.md)] gögnin þín með Power BI og [!INCLUDE[d365fin](includes/d365fin_md.md)] efnispökkum. Power BI sækir gögn þín og býr svo til út-fyrir-kassann yfirlit og skýrslur sem byggist á þeim gögnum.  

Microsoft hefur gefið út eftirfarandi efnispakka:

| Forrit | Description |
| --- | --- |
| Microsoft Finance and Operations, Business Edition | Býður upp á yfirlit með fjárhagslegum lykilupplýsingum yfir tíma, eins og t.d. tekjur á móti útgjöldum, rekstrarframlegð og ferill bundins reiðufés.|
| Microsoft Finance and Operations, Business Edition - CRM | Býður upp á yfirlit með lykilupplýsingum um sölutækifæri og tengiliði.  |
| Microsoft Finance and Operations, Business edition - Sales | Býður upp á yfirlit með lykilupplýsingum um sölutækifæri og tengiliði. |

## <a name="using-the-dashboards"></a>Nota Yfirlitið
Hver efnispakki býður upp á skýrslur sem þú getur nýtt þér:

* Velja hvaða sjónræna hlutinn á yfirlitinu til að kalla fram einn af sjö undirliggjandi skýrslum.  
* Síða skýrsluna eða bæta við reitum sem eiga að fylgjast með.  
* Festu þetta sérsniðna yfirlit á yfirlitið til að halda áfram rakning á.  
  Hægt er uppfæra gögn handvirkt og þú getur sett upp uppfærsluáætlun. Frekari upplýsingar eru í [Grunnstilla uppfærsluáætlun](https://powerbi.microsoft.com/en-us/documentation/powerbi-refresh-scheduled-refresh/).  

Efnispakkinn er forstilltur til að vinna með sölugögnum og fjárhagsgögnum úr sýnifyrirtæki sem þú færð þegar þú nýskráir þig fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)]. Þegar þú hleður inn forritunum í Power BI og tengist eigin gögnum, er mögulegt að sumar skýrslur virki ekki því þær styðjast við gögn sem fyrirtækið þitt hefur ekki. Í þeim tilfellum geturðu einfaldlega fjarlægt skýrsluna úr yfirlitinu.  

> [!NOTE]  
>   Einnig er hægt að búa til eigin skýrslur og yfirlit í Power BI á grundvelli þinna [!INCLUDE[d365fin](includes/d365fin_md.md)] gagna. Nánari upplýsingar eru í [Tengja viðskiptagögn þín við Power BI](across-how-use-financials-data-source-powerbi.md), .  

## <a name="accessing-included365finincludesd365finmdmd-in-power-bi"></a>Aðgangur að [!INCLUDE[d365fin](includes/d365fin_md.md)] í Power BI
Til að skoða þitt [!INCLUDE[d365fin](includes/d365fin_md.md)] gögn í Power BI, verður þú að hafa eftirfarandi:  

* Aðgang að [!INCLUDE[d365fin](includes/d365fin_md.md)]. Nánari upplýsingar eru í [Finance and Operations, Business Edition](http://go.microsoft.com/fwlink/?LinkID=759714).  
* Aðgang að Power BI Nánari upplýsingar eru í [Power BI](https://powerbi.microsoft.com), .

Á vefsvæði Power BI má finna viðbótarupplýsingar um [að tengjast þjónustu með efnispakka fyrir Power BI](http://go.microsoft.com/fwlink/?LinkID=760850).  

Til að fá aðgang að [!INCLUDE[d365fin](includes/d365fin_md.md)] gögnum þínum í Power BI, á tengisíðunni, verður þú að tilgreina eftirfarandi upplýsingar:

| Svæði | Lýsing |
| --- | --- |
| **OData streymisvefslóð** |OData vefslóð svo Power BI geti fengið aðgang að gögnum úr fyrirtæki þínu, eins og https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('My%2Business'). |
| **Sannvottunaraðferð** |Velja **Grunn**. |
| **Notandanafn** |Nafn notanda eins og það birtist fyrir reikningnum þínum í [!INCLUDE[d365fin](includes/d365fin_md.md)], eins og *Jón Jónsson*. |
| **Aðgangsorð** |Þetta er aðgangslykill vefþjónustu fyrir notandareikningur þinn í [!INCLUDE[d365fin](includes/d365fin_md.md)]. |

Þetta þýðir að þú þarft að fá 2 stykki af upplýsingar úr [!INCLUDE[d365fin](includes/d365fin_md.md)]: *OData vefslóðin* og *aðgangslykill vefþjónustu* fyrir notandareikning þinn.  

### <a name="getting-the-url"></a>Veffangið sótt
Þegar [!INCLUDE[d365fin](includes/d365fin_md.md)] er bætt við Power BI verður þú að tilgreina vefslóð þannig að Power Bi geti fá aðgang að gögnum fyrirtækisins. Á tengisíðunni er vísað til vefslóðar sem **OData streymisvefslóð**, og hún verður að vera á eftirfarandi sniði:

         https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')  
Í þessu dæmi er *mittfyrirtæki* heiti [!INCLUDE[d365fin](includes/d365fin_md.md)] þjónustu, og *CRONUS U.S.* er heiti sýndarfyrirtækinu með *%20* sem táknar bil í heitinu.   
Til að fá vefslóð, í [!INCLUDE[d365fin](includes/d365fin_md.md)], leita að og opna gluggann **vefþjónustur**. Í þessum glugga er listi yfir vefþjónustur sem eru nú tiltækar og hægt er að afrita tengillinn úr reitnum **OData vefslóð** fyrir eina af sjálfgefnu OData vefþjónustunum.  

### <a name="getting-the-user-name-and-the-web-service-access-key"></a>Sækja notandanafninu og vefþjónustu aðgang lykilinn
Til að nota gögn úr [!INCLUDE[d365fin](includes/d365fin_md.md)] í Power BI í **tengjast Financials** glugganum, verður þú að tilgreina notandanafn og aðgangsorð. Notandanafninu er nafnið þitt eins og það birtast á reikning í [!INCLUDE[d365fin](includes/d365fin_md.md)] svo að Power BI geti skrá sig inn í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Aðgangsorðið er aðgangslykill vefþjónustu sem er sett upp fyrir notandareikning þinn í verkefni [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Til að finna þessar upplýsingar í [!INCLUDE[d365fin](includes/d365fin_md.md)], leitaðu að **Notendur** glugganum, og síðan opna spjaldið fyrir notandareikning þinn. Á **Almenna** Flýtiflipanum, afritaðu efnið af **Notandanafn** reitnum, og á **Aðgangur vefþjónustu** Flýtiflipanum, afritaðu efni **Aðgangslykill vefþjónustu** reitsins. Ef reiturinn **Aðgangslykill vefþjónustu** er auður skaltu velja í borðanum **Breyta aðgangslykill vefþjónustu**, velja **Lykill rennur aldrei u** reitinn og velja svo Í lagi hnappinn. Síðan er hægt að afrita lykill  

## <a name="getting-data-from-included365finincludesd365finmdmd"></a>Sækja gögnum frá [!INCLUDE[d365fin](includes/d365fin_md.md)]
[!INCLUDE[d365fin](includes/d365fin_md.md)] yfirlitið sýnir flestar dæmigerðum skýrslur sem þú munt vilja nota til að fylgjast með fyrirtækið þitt. Gögnin eru fengin úr þínu [!INCLUDE[d365fin](includes/d365fin_md.md)] fyrirtæki með því að nota vefþjónustur til að lesa lifandi gögn. Í [!INCLUDE[d365fin](includes/d365fin_md.md)], sýnir **vefþjónustur** glugginn þær vefþjónustur sem hafa verið settar upp fyrir þig.

> [!NOTE]  
>   Ef þú breytir heiti einhverra þessara vefþjónusta munu gögnin ekki birtast í Power BI.  
Ef þú vilt bæta við nota önnur gögn í Power BI, verður þú að finna töflurnar í [!INCLUDE[d365fin](includes/d365fin_md.md)], sýna þær sem vefþjónustur og síðan bæta þeim við efnispakkann. Þetta eru aðstæður fyrir lengra komna, og við mælum með að þú byrjar með gögn sem er nú þegar í boði í Power BI.  

## <a name="troubleshooting"></a>Úrræðaleit
Power BI yfirlitið byggir á birtum vefþjónustum sem eru hér að ofan skráðar, og það mun sýna gögn sýnifyrirtæki eða eigin fyrirtæki þitt ef þú flytja inn gögn úr núverandi fjárhagslausnum þínum. Hins vegar, ef eitthvað fer úrskeiðis, þessi kafli gefur lausn fyrir dæmigerður vandamál.  

**„Sannprófun færibreyta tókst ekki, vinsamlegast vertu viss um að allar færibreytur séu gildar“**  
Ef þú sérð þessa villumeldingu eftir að þú færir inn þína [!INCLUDE[d365fin](includes/d365fin_md.md)] vefslóð, skaltu tryggja að eftirfarandi skilyrði séu uppfyllt:  

* Veffangið fylgir nákvæmlega þessum mynstri:

    https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')  
* Eyða öllum texti á eftir heiti fyrirtækis í svigum  
* Ganga þarf úr skugga um að engin skaástrik komi í kjölfar vefslóðar  
* tryggja skal að um sé að ræða öruggra tengingu eins og tilgreint af Veffangið sem byrjar á *https*.  

**„Innskráning mistókst“**  
Ef þú færð „innskráning mistókst“ villu þegar þú skráir þig inn í yfirlitið, með því að nota þínar [!INCLUDE[d365fin](includes/d365fin_md.md)] innskráningarupplýsingar, þá getur eitt af eftirfarandi vandamálum valdið þessu:

* Reikningur sem verið er að nota er ekki með heimildir til að lesa [!INCLUDE[d365fin](includes/d365fin_md.md)] gögnin úr reikninginn þinn.

    Staðfesta notandareikning í [!INCLUDE[d365fin](includes/d365fin_md.md)], og ganga úr skugga um að notaðar hafa verið rétt aðgangslykill vefþjónustu sem aðgangsorð og reyndu síðan aftur.  
* [!INCLUDE[d365fin](includes/d365fin_md.md)] Tilvikið sem verið er að reyna að tengjast er ekki með gilt SLL vottorð. Í þessu tilviki sérðu nákvæmari villuboð ("ekki er hægt að stofna traust SSL samband").

    > [!NOTE]  
>   Sjálfárituð vottorð eru ekki studd.  

**"Úps"**  
Ef þú sérð "Úps" villuglugga þegar þú ert kominn framhjá sannvottunarglugganum, er þetta oftast vegna vandamáls við að tengjast gögnum fyrir efnispakkann.

* Sannprófa að vefslóð er samkvæmt mynstri sem var tilgreint áður.

    `https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')`  
* Algeng mistök eru að tilgreina fulla vefslóð fyrir tiltekna vefþjónustu.

    `https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')/powerbifinance`
* Eða þú gætir hafa gleymt að tilgreina heiti fyrirtækis.

    `https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/`

## <a name="see-also"></a>Sjá einnig
[Viðskiptaupplýsingar](bi.md)  
[Velkomin(n) í [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Yfirfæra viðskiptagögn úr öðrum fjárhagskerfum](upload-data.md)  
[Nota [!INCLUDE[d365fin](includes/d365fin_md.md)] sem Power BI gagnaveitu](across-how-use-financials-data-source-powerbi.md)  
[Nota [!INCLUDE[d365fin](includes/d365fin_md.md)] sem PowerApps gagnaveitu](across-how-use-financials-data-source-powerapps.md)  
[Nota [!INCLUDE[d365fin](includes/d365fin_md.md)] í Microsoft Flow](across-how-use-financials-data-source-flow.md)   

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

