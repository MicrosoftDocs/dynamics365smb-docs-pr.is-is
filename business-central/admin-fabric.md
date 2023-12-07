---
title: Kynning á efni frá Microsoft og Viðskiptabönkum
description: 'Fá yfirlit yfir notkun á Microsoft efni til að fá innsýn, viðskiptagreind og afkastavísa úr aðalgögnum fyrirtækisins.'
author: kennienp
ms.topic: overview
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.search.form: '6316, 6317'
ms.reviewer: jswymer
ms.date: 10/10/2023
ms.author: kepontop
ms.custom: bap-template
---
# <a name="introduction-to-microsoft-fabric-and-business-central"></a>Kynning á efni frá Microsoft og Viðskiptabönkum

[!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] er enda í greiningarlausn með fulla þjónustugetu þar með talið gagnahreyfingu, gagnagátt, gagnaverkfræði, samþættingu gagna, gagnagátt, gagnafræði, rauntíma Analytics og viðskiptagreind &mdash; öll öryggisafrit af sameiginlegum palli veita öfluga gagnaöryggi, stjórnhæfni og samræmi. Fyrirtækið þitt þarf ekki lengur að sauma saman einstaka greiningarþjónustu frá mörgum lánardrottnum. Í staðinn skaltu nota straumlínulögun lausn sem auðvelt er að tengja, um borð og starfa.

> [!NOTE]
> [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] er nú í forskoðun. Nánari upplýsingar um losunaráætlun fyrir Microsoft-efni er að finna hér [aka.ms/FabricRoadmap](https://aka.ms/FabricRoadmap)
> 
> Með reglulegri birtingu þessa vegakorta verður þér hjálpað að vera upplýstur um hvernig  [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)]  mun takast að sinna þínum þörfum.

## <a name="where-does--fit-into-includeprod_short-analytics"></a>[!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] Hvar passar inn í  [!INCLUDE[prod_short](includes/prod_short.md)]  Analytics

[!INCLUDE[prod_short](includes/prod_short.md)] kemur með mörgum út-á-Box skýrslum og getu gagnagreiningar eins og fjárhagslegum skýrslugerð, opnum í Excel og greiningarstillingu á listum og fyrirspurnum. Hér að ofan er því auðvelt að skilgreina  Power BI  skýrslur sem lesa gögn úr stöðluðum og sérsniðnum API, skilgreina  Power BI  árangursmat og ívefja allt þetta beint í  [!INCLUDE[prod_short](includes/prod_short.md)]  biðlaranum. En fyrir viðskiptavini með ítarlegri gagnafræði eða viðskiptagreindaratburðarás sem krefjast ríkari gagnaverkfræði eða gagnasamþættingar  [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)]  gæti verið góður kostur. 

## <a name="onelake"></a>OneLake

Lykilþáttur í að  [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)]  bjóða upp á er OneLake. OneLake er stakt, einhæft og rökrétt gagnastöðuvatn fyrir skipulagið í heild sinni. Þú getur hugsað um OneLake sem fyrir gögnin eru OneDrive . Það veitir þér gagnvökur sem þjónustu án þess að þurfa að byggja það sjálfur. OneLake kemur sjálfkrafa með hverjum  [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)]  leigjanda án þess að hafa innviði til að stjórna. Öll gögnin, sem lenda í OneLake, taka sjálfkrafa þátt í út-kassa gögnum stjórnsýslu, svo sem gagnafókus, gagnavernd, vottun og Samþætting vörulista. Það brýtur niður gögn Silos með því að gera ólíkum hlutum skipulagsins kleift að vinna sjálfstætt meðan enn er verið að leggja sömu gögn vötnum.

[!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] vörur geyma gögnin þín í OneLake í opnu skráarsniði. Fyrir skipulögð tabular gögn er  *þetta snið Delta parket*. Delta parket sniðið leyfir hverja Analytics vél í  [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)]  til að nálgast gögnin frá öðrum Analytics vélum. Með þessum hætti getur það gert sveigjanleika fyrir gagnaðila að nota þau verkfæri sem að eigin vali eru notuð.

> [!NOTE]
> Við gerum ráð fyrir að með einni af okkar síðari útgáfum  [!INCLUDE[prod_short](includes/prod_short.md)]  verði gögn einnig gerð aðgengileg í OneLake fyrir viðskiptavinina sem nota bæði  [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)]  og  [!INCLUDE[prod_short](includes/prod_short.md)]  og hafa einstaka kröfur á þeim sviðum sem það  [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)]  styður. Tímalína veltur á tímalínu almenns framboðs  [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)]  og íhluta sem þarf til að gera þessa reynslu virka. Við ætlum að uppfæra þessa grein með nákvæmari tímalínu, einu sinni vitum við meira.

## <a name="see-also"></a>Sjá einnig .
[Nota Power BI með Business Central](admin-powerbi.md)   

[!INCLUDE[footer-include](includes/footer-banner.md)]
