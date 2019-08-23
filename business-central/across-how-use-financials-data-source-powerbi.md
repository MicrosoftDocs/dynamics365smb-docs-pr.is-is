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
ms.date: 07/08/2019
ms.author: edupont
ms.openlocfilehash: c86f1c3c40f80ec993d0a3a89154047ddf9e8126
ms.sourcegitcommit: 519623f9a5134c9ffa97eeaed0841ae59835f453
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/16/2019
ms.locfileid: "1755242"
---
# <a name="using-include-prodlongincludesprodlongmd-as-power-bi-data-source-for-building-reports"></a>Notkun [!INCLUDE [prodlong](includes/prodlong.md)] sem Power BI gagnagjafa fyrir skýrslugerð

Notandi getur gert [!INCLUDE[prodlong](includes/prodlong.md)]-gögnin sín aðgengileg sem gagnaveitu í Power BI og byggt upp öflugar skýrslur um stöðu síns reksturs.  

Notandi verður að vera með gildan reikning hjá [!INCLUDE[prodshort](includes/prodshort.md)] og hjá Power BI. Einnig þarf að sækja [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/). Frekari upplýsingar er að finna í [Stutt leiðbeining: Tengjast við gögn í Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).  

## <a name="to-add-includeprodshortincludesprodshortmd-as-a-data-source-in-power-bi-desktop"></a>Til að bæta [!INCLUDE[prodshort](includes/prodshort.md)] við sem gagnaveitu í Power BI Desktop

1. Í Power BI Desktop, á vinstra yfirlitssvæðinu, skal velja **Sækja gögn**.
2. Á síðunni **Ná í gögn** skal velja **Þjónusta á netinu**, velja **Microsoft Dynamics 365 Business Central** og síðan velja hnappinn **Tengjast**.
3. Power BI birtir leiðsagnarforrit sem leiðbeinir þér gegnum tengingarferlið. Þú verður beðin/n um að skrá þig inn í [!INCLUDE [prodshort](includes/prodshort.md)]. Veljið **Skrá inn** og svo reikninginn sem ætlunin er að skrá sig inn á. Þetta ætti að vera sami reikningur og við innskráningu á [!INCLUDE [prodshort](includes/prodshort.md)].
4. Veldu hnappinn **Tengjast** til að halda áfram. Leiðsagnarforrit Power BI sýnir lista yfir Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)] fyrirtæki og gagnaveitur. Þessar gagnaveitur tákna allar vefþjónustur sem notandi hefur birt úr hverju fyrirtæki í [!INCLUDE [prodshort](includes/prodshort.md)].

  ![powerbi_webservices.png](media/across-how-use-financials-data-source-powerbi/powerbi_webservices.png)

5. Einnig er hægt að stofna nýja vefslóð vefþjónustu í [!INCLUDE [prodshort](includes/prodshort.md)] með því að nota aðgerðina **Stofna gagnamengi** á síðunni **Vefþjónustur** með því að nota Uppsetningu með hjálp fyrir **Setja upp skýrslugerð** eða með því að velja aðgerðina **Breyta í Excel** í hvaða lista sem er.
6. Tilgreinið gögnin sem notandi vill bæta við gagnalíkanið þitt og veljið svo hnappinn **Hlaða**.
7. Endurtaktu fyrri skref til að bæta við viðbótar [!INCLUDE [prodshort](includes/prodshort.md)] eða öðrum gögnum í Power BI gagnalíkanið þitt.

> [!NOTE]  
> Þegar notandi hefur tengst [!INCLUDE [prodshort](includes/prodshort.md)] verður hann ekki beðinn aftur um skrá sig inn.

Þegar gögnum hefur verið hlaðið birtast þau á hægra yfirlitssvæði síðunnar. Nú hefur notanda tekist að tengjast gögnum sínum í [!INCLUDE [prodshort](includes/prodshort.md)] og getur byrjað að byggja upp Power BI-skýrsluna sína.  

Áður en þú býrð til skýrsluna mælum við með að þú flytjir inn [!INCLUDE [prodshort](includes/prodshort.md)] þemaskrána.  Þemaskráin mun búa til litaspjald þannig að þú getir búið til skýrslur í sama litastíl og [!INCLUDE [prodshort](includes/prodshort.md)] forrit án þess að þurfa að skilgreina sérsniðna liti fyrir hvert myndefni.

Frekari upplýsingar er að finna í [Power BI skráning](/power-bi/consumer/power-bi-consumer-landing/).

## <a name="see-also"></a>Sjá einnig

[Gera viðskiptagögn þín virk fyrir Power BI](admin-powerbi.md)  
[Viðskiptaupplýsingar](bi.md)  
[Hafist handa](product-get-started.md)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Fjármál](finance.md)  
[Stutt leiðbeining: Tengjast við gögn í Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
