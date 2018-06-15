---
title: Business Central og Power BI | Microsoft Docs
description: "Það er auðvelt að fá innsýn, viðskiptaupplýsingar og afkastavísi (KPI) í Business Central gögnum með Power BI og  Business Central efnispökkunum."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 04/12/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: c7359c5246ebbc588673409740fdfbad01685308
ms.contentlocale: is-is
ms.lasthandoff: 05/17/2018

---
# <a name="enabling-your-business-data-for-power-bi"></a>Virkja viðskiptagögnin þín fyrir Power BI
Það er auðvelt að fá innsýn í [!INCLUDE[d365fin](includes/d365fin_md.md)] gögnin þín með Power BI og [!INCLUDE[d365fin](includes/d365fin_md.md)] efnispökkum. Power BI sækir gögn þín og býr svo til út-fyrir-kassann yfirlit og skýrslur sem byggist á þeim gögnum.  

Notandi verður að vera með gildan reikning hjá Dynamics 365 og hjá Power BI. Einnig verður að hlaða niður [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) ef þú vilt búa til þínar eigin Power BI skýrslur. Power BI efnispakki þarfnast heimildar í töflur þaðan sem gögn eru sótt úr. Frekari upplýsingar um kröfur er að finna hér að neðan.  

Microsoft hefur gefið út eftirfarandi efnispakka:

| Forrit | Description |
| --- | --- |
| Microsoft Business Central | Býður upp á yfirlit með fjárhagslegum lykilupplýsingum yfir tíma, eins og t.d. tekjur á móti útgjöldum, rekstrarframlegð og ferill bundins reiðufés.|
| Microsoft Business Central - CRM | Býður upp á yfirlit með lykilupplýsingum um sölutækifæri og tengiliði.  |
| Microsoft Business Central - Sales | Býður upp á yfirlit með lykilupplýsingum um sölutækifæri og tengiliði. |

## <a name="using-the-dashboards"></a>Nota Yfirlitið
Hver efnispakki býður upp á skýrslur sem þú getur nýtt þér:

* Velja hvaða sjónræna hlutinn á yfirlitinu til að kalla fram einn af sjö undirliggjandi skýrslum.  
* Síða skýrsluna eða bæta við reitum sem eiga að fylgjast með.  
* Festu þetta sérsniðna yfirlit á yfirlitið til að halda áfram rakning á.  
  Hægt er uppfæra gögn handvirkt og þú getur sett upp uppfærsluáætlun. Frekari upplýsingar eru í [Grunnstilla uppfærsluáætlun](https://powerbi.microsoft.com/en-us/documentation/powerbi-refresh-scheduled-refresh/).  

Efnispakkinn er forstilltur til að vinna með sölugögnum og fjárhagsgögnum úr sýnifyrirtæki sem þú færð þegar þú nýskráir þig fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)]. Þegar þú hleður inn forritunum í Power BI og tengist eigin gögnum, er mögulegt að sumar skýrslur virki ekki því þær styðjast við gögn sem fyrirtækið þitt hefur ekki. Í þeim tilfellum geturðu einfaldlega fjarlægt skýrsluna úr yfirlitinu.  

> [!NOTE]  
>   Einnig er hægt að búa til eigin skýrslur og yfirlit í Power BI á grundvelli þinna [!INCLUDE[d365fin](includes/d365fin_md.md)] gagna. Nánari upplýsingar eru í [Tengja viðskiptagögn þín við Power BI](across-how-use-financials-data-source-powerbi.md), .  

## <a name="how-to-connect"></a>Hvernig á að tengjast
1. Velja skal **Sækja gögn** neðst til vinstri á yfirlitssvæðinu.  
![Flett um til að sækja gögn](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)

Þú gætir líka komið þér af stað inn í Dynamics 365 Business Edition. Frá hlutverkamiðstöðinni skal fletta að **Skýrsluval** í hluta Power BI hlutverkamiðstöðvar. Veldu annað hvort **Þjónusta** eða **Mitt fyrirtæki** frá borðanum. Þegar önnur hvor þessara aðgerða er valin verður þér vísað annað hvort á fyrirtækisgalleríð í Power BI eða þjónustusafnið í Power BI, sem einnig verður síað til að aðeins birta efnispakka sem tengjast [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].

2. Í **Þjónusta** reitnum er valið **Sækja**. Þá er gluggi opnaður með **AppSource** og **Forrit fyrir Power BI forrit**.  
![Velja efnispakka frá netþjónustum](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)
3. Veldu **Forrit** af flipanum **Forrit fyrir Power BI forrit**, veldu efnispakkann **Microsoft Dynamics 365 Business Central** sem þú vilt nota og veldu síðan **Fá hann núna**.  
![Velja Dynamics 365 Business Central og velja Fá núna](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)
4. Þegar kvaðning birtist skal slá inn heiti *fyrirtækisins* í [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]. Þetta er ekki birtingarnafnið. Heiti fyrirtækis er hægt að finna á síðunni „Fyrirtæki“ innan þíns [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] tilviks.  
![Velja Dynamics 365 Business Central og velja Fá núna](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)
5. Þegar tengingu hefur verið komið á er yfirliti, skýrslu og gagnamengi sjálfkrafa hlaðið í Power BI vinnusvæðið. Þegar því lýkur munu reitirnir uppfærast með gögnum úr [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] fyrirtækinu.
![Velja Dynamics 365 Business Central og velja Fá núna](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

## <a name="what-now"></a>Hvað núna?

- Prófaðu [að slá inn spurningu í reitinn Spurningar og svör](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) efst á yfirlitinu.
- [Breyta reitum](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) á yfirlitinu.  
- [Velja reit](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) til opna undirliggjandi skýrslu.  
- Gagnamengið verður stillt á að uppfærast daglega en hægt er að breyta uppfærsluáætluninni eða uppfæra það hvenær sem er í **Uppfæra núna**.

## <a name="system-requirements"></a>Kerfiskröfur
Til að flytja [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] gögn í Power BI þarf notandi að hafa heimidlir á vefþjónustunni til að sækja gögnin. Vefþjónusta sem er áskilin fyrir hvern efnispakka inniheldur:

## <a name="role-center-reports"></a>Skýrslur hlutverkamiðstöðvar

**Microsoft Dynamics 365 Business Central – CRM**
- Sölutækifæri
- Skoða fyrirtæki í Excel-sniðmáti
- Power BI-skýrslumerkimiðar

**Microsoft Dynamics 365 Business Central – Finance**
- PowerBIFinance
- Skoða fyrirtæki í Excel-sniðmáti
- Power BI-skýrslumerkimiðar

**Microsoft Dynamics 365 Business Central – Jobs**
- Verklisti
- Áætlunarlínur verks
- Verkhlutalínur verks
- Power BI-skýrslumerkimiðar
- Skoða fyrirtæki í Excel-sniðmáti

**Microsoft Dynamics 365 Business Central - Sales**
- Stjórnborð sölu
- Skoða fyrirtæki í Excel-sniðmáti
- Power BI-skýrslumerkimiðar

## <a name="list-page-reports"></a>Listasíða skýrslna

**Microsoft Dynamics 365 Business Central – Customers List**
- Sala vöru eftir viðskiptamönnum
- Power BI-vöruinnkaupalisti
- Listi yfir vörusölu í Power BI
- Stjórnborð sölu
- Power BI-viðskiptamannalisti
- ExcelTemplateViewCompany
- Power BI-skýrslumerkimiðar

**Microsoft Dynamics 365 Business Central - General Ledger Entries List**
- Listi yfir upphæð fjárhags í Power BI
- Upphæð fjárhagsáætlunar í Power BI
- ExcelTemplateViewCompany
- Power BI-skýrslumerkimiðar

**Microsoft Dynamics 365 Business Central – Items List**
- Sala vöru eftir viðskiptamönnum
- Power BI-vöruinnkaupalisti
- Listi yfir vörusölu í Power BI
- Stjórnborð sölu
- ExcelTemplateViewCompany
- Power BI-skýrslumerkimiðar

**Microsoft Dynamics 365 Business Central – Jobs List**
- Listi yfir verk í Power BI
- ExcelTemplateViewCompany
- Power BI-skýrslumerkimiðar

**Microsoft Dynamics 365 Business Central – Purchase Invoices List**
- Listi yfir innkaup í Power BI
- ExcelTemplateViewCompany
- Power BI-skýrslumerkimiðar

**Microsoft Dynamics 365 Business Central – Sales Orders List**
- Listi yfir sölu í Power BI
- ExcelTemplateViewCompany
- Power BI-skýrslumerkimiðar


**Microsoft Dynamics 365 Business Central – Vendors List**
- Power BI-vöruinnkaupalisti
- Listi yfir vörusölu í Power BI
- Power BI-lánardrottnalisti
- ExcelTemplateViewCompany
- Power BI-skýrslumerkimiðar

## <a name="web-services"></a>Vefþjónusta
Auðveld leið til að finna vefþjónustu er að leita að vefþjónustu í [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]. Í listanum skal ganga úr skugga um að reiturinn Birta sé valinn fyrir vefþjónustuna sem finna má að ofan.

## <a name="troubleshooting"></a>Úrræðaleit
Power BI yfirlitið byggir á birtum vefþjónustum sem eru hér að ofan skráðar, og það mun sýna gögn sýnifyrirtæki eða eigin fyrirtæki þitt ef þú flytja inn gögn úr núverandi fjárhagslausnum þínum. Hins vegar, ef eitthvað fer úrskeiðis, þessi kafli gefur lausn fyrir dæmigerður vandamál.

### <a name="incorrect-company-name"></a>Rangt fyrirtækjaheiti  
Algeng mistök eru að slá inn birtingarnafn fyrirtækis í stað nafn fyrirtækis. Til að finna nafn fyrirtækisins skal leita að **Fyrirtæki**. Svo skal nota reitinn **Nafn** þegar nafn fyrirtækisins er slegið inn.

### <a name="incorrect-user-name-and-password"></a>Rangt notandanafn og aðgangsorð  
Notandanafn og aðgangsorð sem er notað til að tengjast verður það sama og er notað í Microsoft Office 365 reikningnum.  

Efnispakkinn krefst þess einnig að Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] reikningur sé til staðar. Þegar upplýsingarnar hafa verið skráðar inn verða sjálfkrafa borin kennsl á alla Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] leigjendur sem notandinn hefur aðgang að. Ef notandinn hefur ekki leyfi eða prufuútgáfu að Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] reikningi munu villuboð birtast.

### <a name="the-key-didnt-match-any-rows-in-the-table"></a>Lykillinn passaði ekki við neinar línur í töflunni
Ef þú slærð inn ógilt heiti fyrirtækis meðan á tengingarferlinu stendur geturðu fengið villuskilaboðin „Lykillinn passaði ekki við neinar línur í töflunni“. Gefðu upp rétt nafn fyrirtækis og reyndu að tengjast aftur.

## <a name="see-also"></a>Sjá einnig
[Hafist handa með Power BI](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
[Power BI - Grunnhugtök](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)  
[Viðskiptaupplýsingar](bi.md)  
[Hafist handa](product-get-started.md)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Nota [!INCLUDE[d365fin](includes/d365fin_md.md)] sem Power BI gagnaveitu](across-how-use-financials-data-source-powerbi.md)  
[Nota [!INCLUDE[d365fin](includes/d365fin_md.md)] sem PowerApps gagnaveitu](across-how-use-financials-data-source-powerapps.md)  
[Nota [!INCLUDE[d365fin](includes/d365fin_md.md)] í Microsoft Flow](across-how-use-financials-data-source-flow.md)   

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

