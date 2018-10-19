---
title: "Uppsetning skýrslugerðar fyrir Business Central í Power BI | Microsoft Docs"
description: "Notandi getur gert gögnin sín aðgengileg sem gagnaveitu í Power BI og byggt upp öflugar skýrslur um stöðu síns reksturs."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 0e0ac36bb83709b766d234e34297c2b721daabad
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="using-included365finlongmdincludesd365finlongmdmd-as-power-bi-data-source-for-building-reports"></a>Notkun [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] Power BI gagnagjafi fyrir skýrslugerð
Notandi getur gert [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-gögnin sín aðgengileg sem gagnaveitu í Power BI og byggt upp öflugar skýrslur um stöðu síns reksturs.  

Notandi verður að vera með gildan reikning hjá [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] og hjá Power BI. Einnig þarf að sækja [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).  

## <a name="to-add-included365finlongmdincludesd365finlongmdmd-as-a-data-source-in-power-bi-desktop"></a>Til að bæta [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] við sem gagnaveitu í Power BI Desktop
1. Í Power BI Desktop, á vinstra yfirlitssvæðinu, skal velja **Sækja gögn**.
2. Í glugganum **Ná í gögn** skal velja **Þjónusta á netinu**, velja **Microsoft Dynamics 365 Business Central** og síðan velja hnappinn **Tengjast**.
3. Power BI birtir leiðsagnarforrit sem leiðbeinir þér gegnum [tengingarferlið](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md). Þú verður beðin/n um að skrá þig inn í þjónustuna. Veljið **Skrá inn** og svo reikninginn sem ætlunin er að skrá sig inn á. Þetta ætti að vera sami reikningur og við innskráningu á [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].
4. Veldu hnappinn **Tengjast** til að halda áfram. Leiðsagnarforrit Power BI sýnir lista yfir Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)] fyrirtæki og gagnaveitur. Þessar gagnaveitur tákna allar vefþjónustur sem þú hefur birt frá hverju fyrirtæki í Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].
5. Einnig er hægt að stofna nýja vefslóð vefþjónustu í [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] með því að nota aðgerðina **Stofna gagnamengi** á glugganum **Vefþjónustur** með því að nota Uppsetningu með hjálp fyrir **Setja upp skýrslugerð** eða með því að velja aðgerðina **Breyta í Excel** í hvaða lista sem er.
6. Tilgreinið gögnin sem notandi vill bæta við gagnalíkanið þitt og veljið svo hnappinn **Hlaða**.
7. Endurtaktu fyrri skref til að bæta við viðbótar Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] eða öðrum gögnum í Power BI gagnalíkanið þitt.

> [!NOTE]  
> Þegar þú hefur náð að tengjast Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] verður þú ekki beðin/n um að skrá þig inn aftur.

Þegar gögnum hefur verið hlaðið birtast þau á hægra yfirlitssvæði síðunnar. Á þessum tímapunkti hefur þú náð að tengjast Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] gögnunum þínum og ert tilbúin/n til að byrja að búa til Power BI skýrsluna þína. 

Áður en þú býrð til skýrsluna mælum við með að þú flytjir inn Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] þemaskrána.  Þemaskráin mun búa til litaspjald þannig að þú getir búið til skýrslur í sama litastíl og Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] efnispakkinn án þess að þurfa að skilgreina sérsniðna liti fyrir hvert myndefni.

Frekari upplýsingar eru í [Power BI skjöl](https://powerbi.microsoft.com/documentation/powerbi-landing-page/).

## <a name="see-also"></a>Sjá einnig
[Viðskiptaupplýsingar](bi.md)  
[Hafist handa](product-get-started.md)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)   
[Fjármál](finance.md)  
[Tenging Power BI við [!INCLUDE[d365fin](includes/d365fin_md.md)]](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md)  

