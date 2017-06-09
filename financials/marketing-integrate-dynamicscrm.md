---
title: "Stjórna viðskiptasamböndum þínum með Dynamics 365 for Financials innan úr Dynamics 365 for Financials | Microsoft Docs"
description: "Ef þú notar Dynamics 365 til sölu fyrir viðskiptavinaþátttöku geturðu notað Dynamics 365 til fjármála fyrir vinnslu og fjármál og hefur óaðfinnanlegur samþætting í leiðslu til reiðufé"
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map
ms.date: 03/05/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: c0291cc316b49e1f1f4f2196745914daca158f61
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017

---
# <a name="managing-your-customer-relationships-using-dynamics-365-for-sales-from-inside-dynamics-365-for-financials"></a>Stjórna viðskiptasamböndum þínum með því að nota Dynamics 365 til sölu innan Dynamics 365 for Financials
Ef þú notar Dynamics 365 til sölu til að taka þátt í viðskiptum, getur þú notað [!INCLUDE[d365fin](includes/d365fin_md.md)] til þess að panta vinnslu og fjármál og hafa óaðfinnanlegur samþættingu í framhaldi af peningum.

Þegar umsóknin þín er sett upp til að samþætta við Dynamics 365 til sölu, hefur þú aðgang að söluupplýsingum frá [!INCLUDE[d365fin](includes/d365fin_md.md)] og öfugt í sumum tilfellum. Þessi samþætting gerir þér kleift að vinna með og samstilla gagnategundir sem eru algengar fyrir bæði þjónustu, svo sem viðskiptavini, tengiliði og söluupplýsingar og halda gögnunum uppfærðar á báðum stöðum.  

**Athugaðu**: Í núverandi útgáfu af [!INCLUDE[d365fin](includes/d365fin_md.md)], er vísað til Dynamics 365 for Sales sem Dynamics CRM. Til einföldunar, afgangur þessarar greinar mun nota hugtökin sem notuð eru í [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Til dæmis getur sölumaðurinn í Dynamics CRM notað verðlista frá [!INCLUDE[d365fin](includes/d365fin_md.md)] því að þeir búa til sölufyrirmæli. Þegar þeir bæta hlutnum við sölulínuna í Dynamics CRM, geta þeir einnig séð birgðahæð (framboð) hlutarins frá [!INCLUDE[d365fin](includes/d365fin_md.md)]. Þessar upplýsingar eru gefin út sem hluti af hjálpargögnum um uppsetningu, **Uppsetning Dynamics CRM-tengingar**.  

**Athugið**: Þessi virkni krefst að upplifun þín er stilltur á **Pakki**. Nánari upplýsingar, sjá [Sérstilli þína [!INCLUDE[d365fin](includes/d365fin_md.md)]upplifun](ui-experiences.md).  

## <a name="setting-up-the-connection"></a>Uppsetning tengingarinnar
Frá Heimili geturðu nálgast uppsetningarleiðbeiningar um **Uppsetning Dynamics CRM-tengingar** sem hjálpar þér að setja upp tengingu. Þegar það er gert verður þú að hafa óaðfinnanlega tengingu við Dynamics CRM færslur með [!INCLUDE[d365fin](includes/d365fin_md.md)] skrám.  

**Athugaðu**: Eftirfarandi skýrir frá aðstoðarsamsetningu, en þú getur framkvæmt sömu verkefni handvirkt í glugganum **Uppsetning CRM-tengingar**.

Í aðstoðarsamskipunarleiðbeiningunni geturðu valið hvaða gögn eru samstillt á milli tveggja þjónustunnar. Þú getur einnig tilgreint að þú viljir flytja inn núverandi Dynamics CRM lausnina þína. Í því tilviki verður þú að tilgreina stjórnsýslu notendareikning.

### <a name="setting-up-the-user-account-for-importing-the-solution"></a>Setja upp notandareikninginn til að flytja inn lausnina
Til að flytja inn núverandi Dynamics CRM lausn, notar uppsetningarleiðarvísir stjórnunarreikning. Þessi reikningur verður að vera gilt notandi í Dynamics CRM með eftirfarandi öryggishlutverki:

* Kerfisstjóri  
* Lausnastilling  

Nánari upplýsingar er að finna í [Búa til notendur og úthluta öryggishlutverkum Microsoft Dynamics 365](https://technet.microsoft.com/library/jj191623.aspx) á techNet og [Hvernig á að: Stjórna notendum og heimildum](ui-how-users-permissions.md).  

Þessi reikningur er aðeins notaður meðan á uppsetningu stendur. Þegar lausnin er flutt inn í [!INCLUDE[d365fin](includes/d365fin_md.md)] er reikningurinn ekki lengur þörf.

### <a name="setting-up-the-user-account-for-synchronization"></a>Setja upp notandareikning fyrir samstillingu
Samþættingin byggist á sameiginlegum notendareikningi. Svo í Office 365 áskriftinni þinni verður þú að búa til hollur notandi sem verður notaður til samstillingar á milli tveggja þjónustunnar. Þessi reikningur verður þegar að vera giltur notandi í Dynamics CRM, en þú þarft ekki að úthluta öryggishlutverkum til reikningsins vegna þess að uppsetningarleiðarvísirinn muni gera það fyrir þig. Þú verður að tilgreina þennan notandareikning einn eða fleiri sinnum í uppsetningarhandbókinni, háð því hversu mikið samstilling þú vilt virkja. Nánari upplýsingar er að finna í [Búa til notendur og úthluta öryggishlutverkum Microsoft Dynamics 365 (online)](https://technet.microsoft.com/library/jj191623.aspx) á techNet.

Ef þú velur að virkja *hlutafyrirkomulag*, verður aðgangur að notendareikningurinn að vera með aðgangstakkann fyrir vefþjónustu. Þetta er tvíþætt hlutur á [!INCLUDE[d365fin](includes/d365fin_md.md)] síðunni fyrir þennan notandareikning. Þú verður að velja **Breyta aðgangslykill vefþjónustu** Og í uppsetningarleiðbeiningar CRM-tengingarinnar verður þú að tilgreina þann notanda sem notanda OData vefþjónustunnar.

Ef þú velur að gera kleift að virkja *sölupöntunarsamþætting*, verður þú að tilgreina notanda sem getur séð þessa samstillingu - samþætting notandans eða annan notandareikning.

### <a name="coupling-records"></a>Tengja skrár
Í aðstoðarsamskipunarleiðbeiningunni geturðu valið að samstilla á milli tveggja þjónustunnar. En síðar getur þú einnig sett upp samstillingu tiltekinna gerða gagna. Þetta er kallað *tenging* og í þessum kafla er að finna tillögur um það sem þú verður að taka tillit til.

Til dæmis, ef þú vilt sjá Dynamics CRM reikninga sem viðskiptavini í [!INCLUDE[d365fin](includes/d365fin_md.md)], verður þú að tengja tvær tegundir af skrám. Það er ekki mjög flókið - þú opnar lista **Viðskiptavinalista** í [!INCLUDE[d365fin](includes/d365fin_md.md)], og það er aðgerð í borði til að tengja þessar upplýsingar við Dynamics CRM. Þá tilgreinir þú hvaða [!INCLUDE[d365fin](includes/d365fin_md.md)] viðskiptavinir passa við hvaða reikninga í Dynamics CRM.

Á ákveðnum sviðum byggir virknin á að þú tengir ákveðnar gagnasettir fyrir aðrar gagnasettir eins og sýnt er í eftirfarandi lista:

* Viðskiptavinir og reikningar  
  * Tengdu fyrst sölumenn við Dynamics CRM notendur  
* Vörur og forði  
  * Einingarmeð Dynamics CRM-einingahópar  
* Vörur og forðaverð  
  * Einföld verðlag viðskiptavina með Dynamics CRM verð fyrst  

**Athugaðu**: Ef þú ert að nota verð í erlendum gjaldmiðlum skaltu ganga úr skugga um að þú tengir gjaldmiðla við Dynamics CRM viðskipta gjaldmiðla.

Dynamics CRM sölutilboð veltur á viðbótarupplýsingum eins og viðskiptavinum, mælieiningum, gjaldmiðlum, viðskiptavinahópum, hlutum og / eða auðlindum. Í því skyni að Dynamics CRM sölufyrirmæli virka óaðfinnanlega verður þú að tengja viðskiptavini, mælieiningar, gjaldmiðla, verðlagshópa viðskiptavina, atriði og / eða auðlindir fyrst.

### <a name="synchronizing-records-fully"></a>Samstilla skrár að fullu
Í lok aðstoðaruppsetningarleiðbeiningarinnar geturðu valið aðgerðina **Keyra fulla samstillingu** til að byrja að samstilla allar [!INCLUDE[d365fin](includes/d365fin_md.md)] færslur með öllum tengdum skrám í tengdu Dynamics CRM lausninni. Í **Yfirferð á fullri samstillingu tengslastjórnunar** gluggann, veldu **Ræsa** aðgerðina. Samstillingin byrjar síðan að framkvæma störf í samræmi við ósjálfstæði. Til dæmis eru gjaldeyrisskrár samstilltar fyrir viðskiptavinaskrár. Fullur samstilling getur tekið langan tíma og mun því birtast í bakgrunni þannig að þú getir haldið áfram að vinna í [!INCLUDE[d365fin](includes/d365fin_md.md)].

Til að kanna framvindu einstakra starfa í fullri samstillingu, skal fara á **Staða verkraðarfærslu**, **Í innri vinnslustöðu töflu**, eða **Úr innri vinnslustöðu töflu** í glugganum **Yfirferð á fullri samstillingu tengslastjórnunar**.

Frá gluggann í **Uppsetning CRM-tengingar** er hægt að fá upplýsingar um fulla samstillingu hvenær sem er. Héðan er einnig hægt að opna gluggann **Vörpun samþættingartöflu** til að sjá upplýsingar um töflurnar í fjármálum og í Dynamics CRM lausninni sem þarf að samstilla.

## <a name="see-also"></a>Sjá einnig
[Tengslastjórnun](marketing-relationship-management.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Sérsníða [!INCLUDE[d365fin](includes/d365fin_md.md)] reynslu þína] (ui-experiences.md)  
[Hvernig á að: Vinna með notendur og heimildir](ui-how-users-permissions.md)    
[Um borð stofnunina þína og notendur til Dynamics 365 (á netinu)](https://www.microsoft.com/en-US/Dynamics/crm-customer-center/onboard-your-organization-and-users-to-dynamics-365-online.aspx)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
