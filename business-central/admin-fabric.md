---
title: Kynning á Microsoft Fabric og Business Central
description: 'Fáðu yfirlit yfir notkun Microsoft Fabric til að fá innsýn, viðskiptaupplýsingar og afkastastærðir úr Business Central gögnunum þínum.'
author: kennienp
ms.topic: overview
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.search.form: '6316, 6317'
ms.reviewer: bholtorf
ms.date: 04/24/2024
ms.author: kepontop
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="introduction-to-microsoft-fabric-and-business-central"></a>Kynning á Microsoft Fabric og Business Central

[!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] er greiningarlausn með fullri þjónustugetu, þ.m.t. hreyfingu gagna, vötnum gagna, gagnaverkfræði, gagnasamþættingu, gagnavísindum, rauntímagreiningum og viðskiptagreindum sem allt er bakað með sameiginlegum vettvangi sem veitir öflugt&mdash; gagnaöryggi, stjórnunarhætti og samræmi. Fyrirtækið þarf ekki lengur að sauma saman einstakar greiningarþjónustur frá mörgum lánardrottnum. Þess í stað skal nota straumlínulagaða lausn sem auðvelt er að tengja, um borð og starfa.

> [!NOTE]
> Sjá Microsoft Fabric  [aka.ms/FabricRoadmap](https://aka.ms/FabricRoadmap)
> 
> Regluleg birting vegamyndarinnar mun hjálpa þér að vera upplýstur um það hvernig [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] mun takast á við þarfir þínar.

## <a name="where-does--fit-into-includeprod_short-analytics"></a>[!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] Hvar passar inn í [!INCLUDE[prod_short](includes/prod_short.md)] greiningar

[!INCLUDE[prod_short](includes/prod_short.md)] Margar skýrslur og greiningargetu gagna eins og fjárhagsskýrslugerð, opnar í Excel og greiningarstillingu á listum og fyrirspurnum. Ofan á þetta er auðvelt að skilgreina Power BI skýrslur sem lesa gögn frá stöðluðum og sérsniðnum API, skilgreina Power BI mælikvarða árangursmat og setja öll þessi beint inn í biðlarann [!INCLUDE[prod_short](includes/prod_short.md)] . En fyrir viðskiptamenn með ítarlegri gagnavísindi eða viðskiptagreind sem krefjast ríkari gagnaverkfræði eða samþættingar gagna gæti [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)]  verið góður valkostur. 

## <a name="onelake"></a>OneLake

Lykilatriði í tilboðum [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] er OneLake. OneLake er eitt, sameinað, rökrétt gagnavatn fyrir allt fyrirtækið. Hægt er að hugsa OneLake sem OneDrive fyrir gögn. Það veitir þér gagnavötn sem þjónustu án þess að þurfa að byggja það sjálfur. OneLake kemur sjálfkrafa með hverjum [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] leigjanda án innviða til að stjórna. Öll gögn, sem lenda í OneLake, taka sjálfkrafa þátt í eftirliti með gögnum úr kassanum, svo sem gagnalínu, gagnavernd, vottun og samþættingu vörulista. Það sundurliðar gögn kísilversins með því að gera ólíkum hlutum fyrirtækisins kleift að vinna sjálfstætt á meðan það stuðlar enn að sama gagnavatninu.

[!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] vörur geyma gögnin í OneLake á opnu skrársniði. Fyrir skipulögð dálkagögn er *þetta snið delta parket*. Delta parket snið gerir öllum greiningarvélum [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] kleift að fá aðgang að gögnum frá öðrum greiningarvélum. Þannig býður það upp á sveigjanleika fyrir gagnabanka að nota verkfærin að eigin vali.


## <a name="see-also"></a>Sjá einnig .
[Nota Power BI með Business Central](admin-powerbi.md)   

[!INCLUDE[footer-include](includes/footer-banner.md)]
