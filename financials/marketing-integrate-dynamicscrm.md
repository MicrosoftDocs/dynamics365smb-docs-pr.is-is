---
title: "Vinna með viðskiptamenn með því nota Dynamics 365 for Sales| Microsoft Docs"
description: "Hægt er að nota Dynamics 365 for Sales innan Dynamics 365 for Financials til að varpa gögnum og hafa óaðfinnanlegur samþætting og samstillingu í heildarferlinu."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map
ms.date: 06/06/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: bc0b9c8141c6c2eac78abc9cd3f5c89af3c89fbb
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="managing-your-customer-relationships-using-dynamics-365-for-sales-from-inside-dynamics-365-for-financials"></a>Stjórna viðskiptasamböndum þínum með því að nota Dynamics 365 for Sales innan Dynamics 365 for Financials
Ef þú notar Dynamics 365 for Sales til að taka þátt í viðskiptum, getur þú notað [!INCLUDE[d365fin](includes/d365fin_md.md)] til þess að panta vinnslu og fjármál og hafa óaðfinnanlegur samþættingu í framhaldi af peningum.

Þegar umsóknin þín er sett upp til að samþætta við Dynamics 365 for Sales, hefur þú aðgang að söluupplýsingum frá [!INCLUDE[d365fin](includes/d365fin_md.md)] og öfugt í sumum tilfellum. Þessi samþætting gerir þér kleift að vinna með og samstilla gagnategundir sem eru algengar fyrir bæði þjónustu, svo sem viðskiptavini, tengiliði og söluupplýsingar og halda gögnunum uppfærðar á báðum stöðum.  

Til dæmis getur sölumaðurinn í Dynamics 365 for Sales notað verðlista frá [!INCLUDE[d365fin](includes/d365fin_md.md)] þegar þeir búa til sölufyrirmæli. Þegar þeir bæta hlutnum við sölulínuna í Dynamics 365 for Sales, geta þeir einnig séð birgðahæð (framboð) hlutarins frá [!INCLUDE[d365fin](includes/d365fin_md.md)]. Þessar upplýsingar eru gefin út sem hluti af hjálpargögnum um uppsetningu, **Uppsetning Dynamics 365-tengingar**.  

> [!NOTE]  
>   Þessi virkni krefst þess að upplifun þín sé stillt á **Suite**. Nánari upplýsingar, sjá [Sérstilla þína [!INCLUDE[d365fin](includes/d365fin_md.md)] upplifun](ui-experiences.md).  

## <a name="setting-up-the-connection"></a>Uppsetning tengingarinnar
Frá Heimili geturðu nálgast uppsetningarleiðbeiningar um **Uppsetning Dynamics 365-tengingar** sem hjálpar þér að setja upp tengingu. Þegar það er gert verður þú að hafa óaðfinnanlega tengingu við Dynamics 365 for Sales færslur með [!INCLUDE[d365fin](includes/d365fin_md.md)] skrám.  

> [!NOTE]  
>   Eftirfarandi útskýrir uppsetningu með aðstoð, en þú getur framkvæmt sömu verkhluta handvirkt í glugganum **Uppsetning Dynamics 365-tengingar**.

Í aðstoðarsamskipunarleiðbeiningunni geturðu valið hvaða gögn eru samstillt á milli tveggja þjónustunnar. Þú getur einnig tilgreint að þú viljir flytja inn núverandi Dynamics 365 for Sales lausnina þína. Í því tilviki verður þú að tilgreina stjórnsýslu notendareikning.

### <a name="setting-up-the-user-account-for-importing-the-solution"></a>Setja upp notandareikninginn til að flytja inn lausnina
Til að flytja inn núverandi Dynamics 365 for Sales lausn, notar uppsetningarleiðarvísir stjórnunarreikning. Þessi reikningur verður að vera gilt notandi í Dynamics 365 for Sales með eftirfarandi öryggishlutverki:

* Kerfisstjóri  
* Lausnastilling  

Nánari upplýsingar er að finna í [Búa til notendur og úthluta öryggishlutverkum Microsoft Dynamics 365](https://technet.microsoft.com/library/jj191623.aspx) á techNet og [Hvernig á að: Stjórna notendum og heimildum](ui-how-users-permissions.md).  

Þessi reikningur er aðeins notaður meðan á uppsetningu stendur. Þegar lausnin er flutt inn í [!INCLUDE[d365fin](includes/d365fin_md.md)] er reikningurinn ekki lengur þörf.

### <a name="setting-up-the-user-account-for-synchronization"></a>Setja upp notandareikning fyrir samstillingu
Samþættingin byggist á sameiginlegum notendareikningi. Svo í Office 365 áskriftinni þinni verður þú að búa til hollur notandi sem verður notaður til samstillingar á milli tveggja þjónustunnar. Þessi reikningur verður þegar að vera giltur notandi í Dynamics 365 for Sales, en þú þarft ekki að úthluta öryggishlutverkum til reikningsins vegna þess að uppsetningarleiðarvísirinn muni gera það fyrir þig. Þú verður að tilgreina þennan notandareikning einn eða fleiri sinnum í uppsetningarhandbókinni, háð því hversu mikið samstilling þú vilt virkja. Nánari upplýsingar er að finna í [Búa til notendur og úthluta öryggishlutverkum Microsoft Dynamics 365 (online)](https://technet.microsoft.com/library/jj191623.aspx) á techNet.

Ef þú velur að virkja *hlutafyrirkomulag*, verður aðgangur að notendareikningurinn að vera með aðgangstakkann fyrir vefþjónustu. Þetta er tvíþætt hlutur á [!INCLUDE[d365fin](includes/d365fin_md.md)] síðunni fyrir þennan notandareikning. Þú verður að velja **Breyta aðgangslykill vefþjónustu** Og í uppsetningarleiðbeiningar Dynamics 365-tengingarinnar verður þú að tilgreina þann notanda sem notanda OData vefþjónustunnar.

Ef þú velur að gera kleift að virkja *sölupöntunarsamþætting*, verður þú að tilgreina notanda sem getur séð þessa samstillingu - samþætting notandans eða annan notandareikning.

### <a name="coupling-records"></a>Tengja skrár
Í aðstoðarsamskipunarleiðbeiningunni geturðu valið að samstilla á milli tveggja þjónustunnar. En síðar getur þú einnig sett upp samstillingu tiltekinna gerða gagna. Þetta er kallað *tenging* og í þessum kafla er að finna tillögur um það sem þú verður að taka tillit til.

Til dæmis, ef þú vilt sjá Dynamics 365 for Sales reikninga sem viðskiptavini í [!INCLUDE[d365fin](includes/d365fin_md.md)], verður þú að tengja tvær tegundir af skrám. Það er ekki mjög flókið - þú opnar lista **Viðskiptavinalista** í [!INCLUDE[d365fin](includes/d365fin_md.md)], og það er aðgerð í borði til að tengja þessar upplýsingar við Dynamics 365 for Sales. Þá tilgreinir þú hvaða [!INCLUDE[d365fin](includes/d365fin_md.md)] viðskiptavinir passa við hvaða reikninga í Dynamics 365 for Sales.

Á ákveðnum sviðum byggir virknin á að þú tengir ákveðnar gagnasettir fyrir aðrar gagnasettir eins og sýnt er í eftirfarandi lista:

* Viðskiptavinir og reikningar  
  * Tengdu fyrst sölumenn við Dynamics 365 for Sales notendur  
* Vörur og forði  
  * Tengja mælieiningar með Dynamics 365 for Sales við einingahópa fyrst  
* Vörur og forðaverð  
  * Tengja verðlagshópa viðskiptavina með Dynamics 365 for Sales við verð fyrst  

> [!NOTE]  
>   Ef þú ert að nota verð í erlendum gjaldmiðlum skaltu ganga úr skugga um að þú tengir gjaldmiðla við Dynamics 365 for Sales viðskipta gjaldmiðla.

Dynamics 365 for Sales sölutilboð veltur á viðbótarupplýsingum eins og viðskiptavinum, mælieiningum, gjaldmiðlum, verðlagshópum viðskiptavina , vörum og / eða tilföngum. Í því skyni að láta Dynamics 365 for Sales sölufyrirmæli virka óaðfinnanlega verður þú að tengja viðskiptavini, mælieiningar, gjaldmiðla, verðlagshópa viðskiptavina, vörur og / eða tilföng fyrst.

### <a name="synchronizing-records-fully"></a>Samstilla skrár að fullu
Í lok aðstoðar uppsetningarleiðbeiningarinnar geturðu valið aðgerðina **Keyra fulla samstillingu** til að byrja að samstilla allar [!INCLUDE[d365fin](includes/d365fin_md.md)] færslur með öllum tengdum skrám í tengdu Dynamics 365 for Sales lausninni. Í **Yfirferð á fullri samstillingu tengslastjórnunar** gluggann, veldu **Ræsa** aðgerðina. Samstillingin byrjar síðan að framkvæma störf í samræmi við ósjálfstæði. Til dæmis eru gjaldeyrisskrár samstilltar fyrir viðskiptavinaskrár. Fullur samstilling getur tekið langan tíma og mun því birtast í bakgrunni þannig að þú getir haldið áfram að vinna í [!INCLUDE[d365fin](includes/d365fin_md.md)].

Til að kanna framvindu einstakra starfa í fullri samstillingu, skal fara á **Staða verkraðarfærslu**, **Í innri vinnslustöðu töflu**, eða **Úr innri vinnslustöðu töflu** í glugganum **Yfirferð á fullri samstillingu tengslastjórnunar**.

Frá gluggann í **Uppsetning Dynamics 365 for Sales-tengingar** er hægt að fá upplýsingar um fulla samstillingu hvenær sem er. Héðan er einnig hægt að opna gluggann **Vörpun samþættingartöflu** til að sjá upplýsingar um töflurnar í Financials og í Dynamics 365 for Sales lausninni sem þarf að samstilla.

## <a name="see-also"></a>Sjá einnig
[Umsjón með venslum](marketing-relationship-management.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Sérstillir þína [!INCLUDE[d365fin](includes/d365fin_md.md)] upplifun](ui-experiences.md).  
[Hvernig á að: Vinna með notendur og heimildir](ui-how-users-permissions.md)    
[Um borð stofnunina þína og notendur til Dynamics 365 (á netinu)](https://www.microsoft.com/en-US/Dynamics/crm-customer-center/onboard-your-organization-and-users-to-dynamics-365-online.aspx)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

