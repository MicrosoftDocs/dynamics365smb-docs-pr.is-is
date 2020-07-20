---
title: Nota Business Central í Power BI-skýrslum | Microsoft Docs
description: Notandi getur gert gögnin sín aðgengileg sem gagnaveitu í Power BI og byggt upp öflugar skýrslur um stöðu síns reksturs.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: b42437f0759ecb6d977797b31222bfa2b88cdb13
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/01/2020
ms.locfileid: "3528463"
---
# <a name="using-prodlong-as-power-bi-data-source-for-building-reports"></a>Notkun [!INCLUDE[prodlong](includes/prodlong.md)] sem Power BI gagnagjafa fyrir skýrslugerð

Notandi getur gert [!INCLUDE[prodlong](includes/prodlong.md)]-gögnin sín aðgengileg sem gagnaveitu í Power BI og byggt upp öflugar skýrslur um stöðu síns reksturs.  

Notandi verður að vera með gildan reikning hjá [!INCLUDE[prodshort](includes/prodshort.md)] og hjá Power BI. Einnig þarf að sækja [Power BI Desktop](https://powerbi.microsoft.com/desktop/). Frekari upplýsingar er að finna í [Stutt leiðbeining: Tengjast við gögn í Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).  

## <a name="to-add-prodshort-as-a-data-source-in-power-bi-desktop"></a>Til að bæta [!INCLUDE[prodshort](includes/prodshort.md)] við sem gagnaveitu í Power BI Desktop

1. Í Power BI Desktop, á vinstra yfirlitssvæðinu, skal velja **Sækja gögn**.
2. Á síðunni **Ná í gögn** skal velja **Þjónusta á netinu**, velja **Microsoft Dynamics 365 Business Central** og síðan velja hnappinn **Tengjast**.
3. Power BI birtir leiðsagnarforrit sem leiðbeinir þér gegnum tengingarferlið, þ.á.m. innskráningu í [!INCLUDE[prodshort](includes/prodshort.md)]. Velja skal **Innskráning** og síðan viðeigandi reikning. Notaðu sama reikning og þú skráir þig inn í [!INCLUDE[prodshort](includes/prodshort.md)] með.
4. Veldu hnappinn **Tengjast** til að halda áfram. Power BI leiðsagnarforritið sýnir lista yfir Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)] umhverfi, fyrirtæki og gagnaveitur. Þessar gagnaveitur tákna allar vefþjónustur sem notandi hefur birt úr [!INCLUDE[prodshort](includes/prodshort.md)].

    Einnig er hægt að búa til vefslóð vefþjónustu í [!INCLUDE[prodshort](includes/prodshort.md)] í staðinn. Veljið eina af eftirfarandi leiðum:

      - Nota aðgerðina **Búa til gagnasafn** á síðunni **Vefþjónusta**
      - Nota uppsetningarleiðbeiningar **Setja upp skýrslugerð** með hjálp
      - Velja aðgerðina **Breyta í Excel** í hvaða lista sem er

5. Tilgreinið gögnin sem notandi vill bæta við gagnalíkanið þitt og veljið svo hnappinn **Hlaða**.
6. Endurtaktu fyrri skref til að bæta við viðbótar [!INCLUDE[prodshort](includes/prodshort.md)] eða öðrum gögnum í Power BI gagnalíkanið þitt.

> [!NOTE]  
> Þegar notandi hefur tengst [!INCLUDE[prodshort](includes/prodshort.md)] verður hann ekki beðinn aftur um skrá sig inn.

Þegar gögnum hefur verið hlaðið er hægt að sjá þau á hægra yfirlitssvæði síðunnar. Notanda tókst að tengjast gögnum sínum í [!INCLUDE[prodshort](includes/prodshort.md)] og getur byrjað að byggja upp Power BI-skýrsluna sína.  

Áður en þú býrð til skýrsluna mælum við með að þú flytjir inn [!INCLUDE[prodshort](includes/prodshort.md)] þemaskrána.  Þemaskráin mun búa til litaspjald þannig að þú getir búið til skýrslur í sama litastíl og [!INCLUDE[prodshort](includes/prodshort.md)] forrit án þess að þurfa að skilgreina sérsniðna liti fyrir hvert myndefni.

Frekari upplýsingar er að finna í [Power BI skráning](/power-bi/consumer/).

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig

[Gera viðskiptagögn þín virk fyrir Power BI](admin-powerbi.md)  
[Viðskiptaupplýsingar](bi.md)  
[Hafist handa](product-get-started.md)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Fjármál](finance.md)  
[Stutt leiðbeining: Tengjast við gögn í Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
