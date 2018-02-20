---
title: "Uppsetning skýrslugerðar fyrir Finance and Operations, Business Edition í Power BI | Microsoft Docs"
description: "Notandi getur gert Financials-gögnin sín aðgengileg sem gagnaveitu í Power BI og byggt upp öflugar skýrslur um stöðu síns reksturs."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 12/21/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 056761b398737bd052b68488756198051f0cdb9a
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---
# <a name="using-included365finincludesd365finmdmd-as-power-bi-data-source-for-building-reports"></a>Notkun [!INCLUDE[d365fin](includes/d365fin_md.md)] Power BI gagnagjafi fyrir skýrslugerð
Notandi getur gert [!INCLUDE[d365fin](includes/d365fin_md.md)]-gögnin sín aðgengileg sem gagnaveitu í Power BI og byggt upp öflugar skýrslur um stöðu síns reksturs.  

> [!NOTE]  
> Notandi verður að vera með gildan reikning hjá [!INCLUDE[d365fin](includes/d365fin_md.md)] og hjá Power BI. Einnig þarf að sækja [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-power-bi-desktop"></a>Til að bæta [!INCLUDE[d365fin](includes/d365fin_md.md)] við sem gagnaveitu í Power BI Desktop
1. Í Power BI Desktop, á vinstra yfirlitssvæðinu, skal velja **Sækja gögn**.
2. Í reitnum **Sækja gögn** skal velja **Netþjónustu**, velja **Dynamics 365 for Finance and Operations, Business Edition**, og velja svo hnappinn **Tengja**.
3. Power BI birtir leiðsagnarforrit sem leiðbeinir þér gegnum [tengingarferlið](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md). Fyrsta skrefið er að skrá sig inn í þjónustuna. Veljið **Skrá inn** og svo reikninginn sem ætlunin er að skrá sig inn á. Þetta ætti að vera sami reikningur og við innskráningu á [!INCLUDE[d365fin](includes/d365fin_md.md)].
4. Veldu hnappinn **Tengjast** til að halda áfram. Leiðsagnarforritið fyrir Power BI birtir lista yfir [!INCLUDE[d365fin](includes/d365fin_md.md)]-fyrirtæki og gagnaveitur. Þessar gagnaveitur tákna allar vefþjónustur sem notandi hefur birt úr hverju fyrirtæki í [!INCLUDE[d365fin](includes/d365fin_md.md)].
5. Einnig er hægt að stofna nýja vefslóð vefþjónustu í [!INCLUDE[d365fin](includes/d365fin_md.md)] með því að nota aðgerðina **Stofna gagnamengi** á síðunni **Vefþjónustur** með því að nota Uppsetningu með hjálp fyrir **Setja upp skýrslugerð** eða með því að velja aðgerðina **Breyta í Excel** í hvaða lista sem er.
6. Tilgreinið gögnin sem notandi vill bæta við gagnalíkanið þitt og veljið svo hnappinn **Hlaða**.
7. Endurtaktu fyrri skref til að bæta fleiri [!INCLUDE[d365fin](includes/d365fin_md.md)]-gögnum við Power Bi-gagnalíkanið þitt.

> [!NOTE]  
> Þegar notandi hefur tengst [!INCLUDE[d365fin](includes/d365fin_md.md)] verður hann ekki beðinn aftur um skrá sig inn.

Þegar gögnum hefur verið hlaðið birtast þau á hægra yfirlitssvæði síðunnar. Nú hefur notanda tekist að tengjast gögnum sínum í Finance and Operations, Business Edition og getur byrjað að byggja upp Power BI-skýrsluna sína. Frekari upplýsingar eru í [Power BI skjöl](https://powerbi.microsoft.com/documentation/powerbi-landing-page/).

## <a name="see-also"></a>Sjá einnig
[Viðskiptaupplýsingar](bi.md)  
[Velkomin(n) í [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](upload-data.md)  
[Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)   
[Fjármál](finance.md)  
[Tenging Power BI við [!INCLUDE[d365fin](includes/d365fin_md.md)]](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md)  

