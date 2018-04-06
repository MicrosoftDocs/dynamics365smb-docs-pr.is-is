---
title: "Hvernig á að Tengja Power BI við Business Central | Microsoft Docs"
description: "Það er auðvelt að fá innsýn, viðskiptaupplýsingar og afkastavísi (KPI) í Business Central gögnum með Power BI og  Business Central efnispökkunum."
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 03/16/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 315d4b188cdd834e82676a0c5ef77272ad873eb7
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="connecting-power-bi-to-business-central-content-packs"></a>Tengir Power BI við efnispakka Business Central
Það er auðvelt að fá innsýn í Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] gögnin þín með Power BI og Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] efnispökkunum. Power BI sækir gögn þín og býr svo til út-fyrir-kassann yfirlit og skýrslur sem byggist á þeim gögnum.

> [!NOTE]  
>  Notandi verður að vera með gildan reikning hjá [!INCLUDE[d365fin](includes/d365fin_md.md)] og hjá Power BI. Einnig þarf að sækja [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).  
>  Power BI efnispakki þarfnast heimildar í töflur þaðan sem gögn eru sótt úr. Frekari upplýsingar um kröfur er að finna hér að neðan.  

## <a name="how-to-connect"></a>Hvernig á að tengjast
1. Velja skal **Sækja gögn** neðst til vinstri á yfirlitssvæðinu.  
![Flett um til að sækja gögn](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)
2. Í **Þjónusta** reitnum er valið **Sækja**. Þá er gluggi opnaður með **AppSource** og **Forrit fyrir Power BI forrit**.  
![Velja efnispakka frá netþjónustum](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)
3. Velja skal **Forrit** í **Forrit fyrir Power BI forrit** flipanum og velja svo **Microsoft Dynamics 365 Business Central** efnispakkann sem á að nota og svo **Sækja núna**.  
![Velja Dynamics 365 Business Central og velja Fá núna](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)
4. Þegar kvaðning birtist skal slá inn heiti *fyrirtækisins* í [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]. Þetta er ekki birtingarnafnið.  
![Velja Dynamics 365 Business Central og velja Fá núna](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)
5. Þegar tengingu hefur verið komið á er yfirliti, skýrslu og gagnamengi sjálfkrafa hlaðið í Power BI vinnusvæðið. Þegar þessu er lokið uppfærast reitirnir með gögnum af reikningnum þínum.
![Velja Dynamics 365 Business Central og velja Fá núna](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

## <a name="what-now"></a>Hvað núna?

- [Breyta reitum](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) á yfirlitinu.  
- [Velja reit](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) til opna undirliggjandi skýrslu.  
- Gagnamengið verður stillt á að uppfærast daglega en hægt er að breyta uppfærsluáætluninni eða uppfæra það hvenær sem er í **Uppfæra núna**.

## <a name="system-requirements"></a>Kerfiskröfur
Til að flytja [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] gögn í Power BI þarf notandi að hafa heimidlir á vefþjónustunni til að sækja gögnin. Vefþjónusta sem er áskilin fyrir hvern efnispakka inniheldur:

**Microsoft Dynamics 365 Business Central – CRM**
- SalesOpportunities
- ExcelTemplateViewCompany

**Microsoft Dynamics 365 Business Central – Sales**
- ItemSalesbyCustomer
- SalesDashboard
- ExcelTemplateViewCompany

**Microsoft Dynamics 365 Business Central – Finance**
- PowerBIFinance
- ExcelTemplateViewCompany

**Microsoft Dynamics 365 Business Central – Jobs**
- Verklisti
- Áætlunarlínur verks
- Verkhlutalínur verks

**Microsoft Dynamics 365 Business Central - Viðskiptamannalisti**
- ItemSalesbyCustomer
- Power_BI_Item_Purchase_List
- Power_BI_Item_Sales_List
- SalesDashboard
- Power_BI_Customer_List
- ExcelTemplateViewCompany

**Microsoft Dynamics 365 Business Central - Vörulisti**
- ItemSalesbyCustomer
- Power_BI_Item_Purchase_List
- Power_BI_Item_Sales_List
- Birgðir
- SalesDashboard
- ExcelTemplateViewCompany

**Microsoft Dynamics 365 Business Central – lánardrottnar**
- ItemSalesbyCustomer
- Power_BI_Item_Purchase_List
- Power_BI_Item_Sales_List
- Birgðir
- SalesDashboard
- Power_BI_Customer_List
- ItemSalesbyCustomer
- Power_BI_Vendor_List
- ExcelTemplateViewCompany

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
Ef þú slærð inn ógilt nafn fyrirtækis meðan á tengingarferlinu stendur geturðu fengið villuboðið "Lykillinn passaði ekki við neinar raðir í töflunni". Gefðu upp rétt nafn fyrirtækis og reyndu að tengjast aftur.

## <a name="see-also"></a>Sjá einnig
[Hafist handa með Power BI](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
[Power BI - Grunnatriði](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)
[Viðskiptagreind](bi.md)  
[Velkomin(n) í [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](upload-data.md)  
[Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Fjármál](finance.md)  
[Uppsetning skýrslugerðar fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] í Power BI](across-how-use-financials-data-source-powerbi.md)  

