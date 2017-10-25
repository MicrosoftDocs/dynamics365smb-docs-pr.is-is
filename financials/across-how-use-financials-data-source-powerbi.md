---
title: "Búa til Power BI gagnaveitu með Financials | Microsoft Docs"
description: "Notandi getur gert Financials-gögnin sín aðgengileg sem gagnaveitu í Power BI og byggt upp öflugar skýrslur um stöðu síns reksturs."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 06/06/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 3f98a08415a896c37868bf0ed5efd9314d5ab07a
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="using-included365finincludesd365finmdmd-as-a-power-bi-data-source"></a>Nota [!INCLUDE[d365fin](includes/d365fin_md.md)] sem Power BI gagnaveitu
Notandi getur gert [!INCLUDE[d365fin](includes/d365fin_md.md)]-gögnin sín aðgengileg sem gagnaveitu í Power BI og byggt upp öflugar skýrslur um stöðu síns reksturs.  

> [!NOTE]  
>   Notandi verður að vera með gildan reikning hjá [!INCLUDE[d365fin](includes/d365fin_md.md)] og hjá Power BI. Einnig þarf að sækja [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-power-bi-desktop"></a>Til að bæta [!INCLUDE[d365fin](includes/d365fin_md.md)] við sem gagnaveitu í Power BI Desktop
1. Í Power BI Desktop, á vinstra yfirlitssvæðinu, skal velja **Sækja gögn**.
2. Í reitnum **Sækja gögn** skal velja **Netþjónustu**, velja **Dynamics 365 for Financials**, og velja svo hnappinn **Tengja**.

   Power BI birtir leiðsagnarforrit sem leiðbeinir þér gegnum tengingarferlið. Fyrsta skref er notanda er að færa inn OData-vefslóð og heiti fyrirtækis sem tengist [!INCLUDE[d365fin](includes/d365fin_md.md)]-reikningnum hans.  

   Til að finna *OData vefslóð* getur notandi afritað OData V4 vefslóð fyrir hverja þeirra vefþjónusta sem taldar eru upp á síðunni **Vefþjónustur** í [!INCLUDE[d365fin](includes/d365fin_md.md)], svo sem `https://mycompany.financials.dynamics.com:7048/MS/ODataV4/`.  

   Fyrir *Fyrirtækisheiti* skal nota heitið sem birtist í reitnum **Heiti** í glugganum **Stofngögn** í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ef [!INCLUDE[d365fin](includes/d365fin_md.md)] notanda inniheldur mörg fyrirtæki skal velja viðeigandi heiti fyrirtækis af listanum í glugganum **Fyrirtæki**. Í báðum tilvikum skal ganga úr skugga um að heiti sem tilgreind eru í leiðsagnarforriti fyrir Power BI samsvari nákvæmlega textanum í [!INCLUDE[d365fin](includes/d365fin_md.md)], svo sem `My Company`.
3. Þegar búið er að færa inn upplýsingarnar er valinn hnappurinn Í lagi. Næsta skrefið í leiðsagnarforritinu verður að færa inn notandanafn og aðgangsorð.

   > [!NOTE]  
>    Ef aðrir sannvottunarkostir eru í boði á vinstra yfirlitssvæði skal velja *Grunnur*.
4. Slá inn notendanafn og aðgangsorð. Þessar upplýsingar má finna í glugganum **Notendur** í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Notið **Aðgangslykil fyrir vefþjónustu** sem aðgangsorðið þitt.

   Til dæmis, notandanafnið þitt er *ADMIN*, og aðgangslykill vefþjónustu sem virkar sem aðgangsorð er *EgzeUFQ9Uv0o5O0lUMyqCzo1ueUW9yRF3SsLU=*.
5. Veldu hnappinn **Tenging** til að halda áfram. Leiðsagnarforritið fyrir Power BI birtir lista yfir [!INCLUDE[d365fin](includes/d365fin_md.md)]-gagnaveitur. Þessar gagnaveitur tákna allar vefþjónustur sem notandi hefur birt úr [!INCLUDE[d365fin](includes/d365fin_md.md)].

   Einnig er hægt að stofna nýja vefslóð vefþjónustu í [!INCLUDE[d365fin](includes/d365fin_md.md)] með því að nota aðgerðina **Stofna gagnamengi** á síðunni **Vefþjónustur** með því að nota Uppsetningu með hjálp fyrir **Setja upp skýrslugerð** eða með því að velja aðgerðina **Breyta í Excel** í hvaða lista sem er.

6. Tilgreinið gögnin sem notandi vill bæta við gagnalíkanið þitt og veljið svo hnappinn **Hlaða**.
7. Endurtaktu fyrri skref til að bæta fleiri [!INCLUDE[d365fin](includes/d365fin_md.md)]-gögnum við Power Bi-gagnalíkanið þitt.

   > [!NOTE]  
>    Þegar notanda hefur tekist að tengjast [!INCLUDE[d365fin](includes/d365fin_md.md)] verður hann ekki beðinn aftur um OData-vefslóð, notandanafn eða aðgangsorð.

Þegar gögnum hefur verið hlaðið birtast þau á hægra yfirlitssvæði síðunnar. Nú hefur notanda tekist að tengjast gögnum sínum í Dynamics 365 og getur byrjað að byggja upp Power BI-skýrsluna sína. Frekari upplýsingar eru í [Power BI skjöl](https://powerbi.microsoft.com/documentation/powerbi-landing-page/).

## <a name="see-also"></a>Sjá einnig
[Viðskiptaupplýsingar](bi.md)  
[Velkomin(n) í [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](upload-data.md)  
[Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Fjármál](finance.md)  

