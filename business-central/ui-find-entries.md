---
title: Leita að færslum | Microsoft Docs
description: Þessi grein lýsir því hvernig á að finna skjöl og færslur sem tengjast
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: c2c5dbf6dc94980e579de8b2a9bbecaca7cfeb16
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/08/2021
ms.locfileid: "6435020"
---
# <a name="finding-related-entries-for-posted-documents"></a>Leita að tengdum færslum fyrir bókuð skjöl 

Í þessari grein er að finna upplýsingar um skjöl og færslur sem tengjast innbyrðis samkvæmt sameiginlegum upplýsingum á borð við:

- Skjalanúmer eða bókunardagsetning
- Gerð viðskiptatengsla, númer eða ytra skjalanúmer
- Raðnúmer eða lotunúmer vöru

Þessi eiginleiki er gagnlegur til að hafa upp á fjárhagsfærslum sem urðu til vegna ákveðinna viðskipta. Þegar leitað er eftir skjalanúmeri, er hægt að prenta samantektina úr skýrslu skjalafærslna.

## <a name="get-started"></a>Hefjast handa

Eiginleiki færsluleitar er aðgengilegur á flestum síðum sem sýna bókuð skjöl eða bókaðar skjalafærslur - fyrir bæði lista og spjöld. Þannig að fyrsta skrefið er að opna eina af þessum síðum. Síðan skal annaðhvort velja aðgerðina **Leita að færslum** eða ýta á Alt+G.

Síðan **Leita að færslum** inniheldur öll tengd skjöl og færslur samkvæmt skjalanúmerinu og bókunardagsetningunni. Síðan skiptist í þrjá hluta:

- Efsti hlutinn sýnir reiti og aðgerðir sem eru notuð til að sía leitina.
- Miðhlutinn sýnir tengd skjöl samkvæmt leitinni.
- Neðsti hlutinn sýnir upplýsingar um upprunaskjalið sem fannst með leit.


<!--
 There are two ways to open this page:

- Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Find Entries**, and then choose the related link.

    With this way, the **Find Entries** page might be empty, and you'll have to start searching for entries from scratch.
    
- Open a page that displays posted documents or posted documents entries, either a list or a card. Then, locate and select the **Find Entries** action.

    With this way, the **Find Entries**, page will include all related documents and entries based on the document no. and posting date.


    > [!TIP]
    > If you are on a page that has the **Find Entries** action, press crtl+G to open the **Find Entries** page directly. 
-->

## <a name="search-for-entries"></a>Leita að færslum

Hægt er að leita að færslum út frá upplýsingum um annaðhvort skjalið, viðskiptatengilið eða vörutilvísun. Til að breyta leitinni skal velja **Aðgerðir**, **Leita eftir** og síðan eina af eftirfarandi aðgerðum:

|Aðgerð|Description|
|------|-----------|
|Leita eftir fylgiskjali|Skoðið færslur út frá tilteknu skjalanúmeri eða bókunardagsetningu.|
|Viðskiptatengiliður |Skoðið færslur út frá tiltekinni gerð tengiliðar, númeri tengiliðar og/eða ytra skjalanúmeri. Hægt er að færa inn upplýsingar um skjal sem lánardrottin eða viðskiptamaður úthlutaði. Notið tiltæka reiti til að leita að skjölum lánardrottins með því að nota númerin sem lánardrottinn hefur úthlutað skjölunum.|
|Vörutilvísun|Skoðið færslur út frá raðnúmeri eða lotunúmeri. Hægt er að færa inn lotunúmer eða raðnúmer, eða sía fyrir lotunúmerinu eða raðnúmerinu sem leita á að. Þessi aðgerð er gagnleg til að sjá hvar tiltekið vörurakningarnúmer var notað, frá hvaða lánardrottni það kom eða hvaða viðskiptamanni það var selt.|

Þegar búið er að velja skal færa inn viðeigandi leitarupplýsingar í reitina efst uppi. Notið ábendingarnar í reitunum til að fá hjálp. Þegar þessu er lokið skal velja **Leita** til að hefja leitina. Ef einhverjum síunum er breytt þarf að velja **Leita** aftur.

> [!TIP]
> Til að fá nokkur dæmi um notkun á **Leita að færslum** skal skoða [Rekja vöruraktar vörur](inventory-how-to-trace-item-tracked-items.md) <!--and [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md). -->

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/user-interface-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig

[Unnið með Business Central](ui-work-product.md)  
[Bæta Síðuaðgerð við hlutverkamiðstöð](ui-bookmarks.md)  
[Rekja vöruraktar vörur](inventory-how-to-trace-item-tracked-items.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
