---
title: Vinna með skjöl á innleið| Microsoft Docs
description: Hægt er að stjórna ytri viðskiptaskjölum á innleið, eins og greiðslukvittunum og PDF skrám, stjórna OCR verkum, og umbreyta skrám yfir í rafræn skjöl og færslur.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 938a86f316e494c0b64e5f2853ee64b9fb5064d8
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5379224"
---
# <a name="incoming-documents"></a>Skjöl á innleið

Sumar viðskiptafærslur eru ekki skráðar í [!INCLUDE[prod_short](includes/prod_short.md)] upphaflega. Þess í stað ytri viðskipti skjal kemur í þitt fyrirtæki sem viðhengi eða pappír eintak sem þú grannskoða til skrá. Þetta er dæmigert við innkaup, þar sem slíkar skrár standa fyrir reikninga frá lánardrottnum eða greiðslukvittanir fyrir kostnað eða smáinnkaup.

Úr PDF-skjölum eða myndaskrám sem standa fyrir skjöl á innleið er hægt að láta ytri OCR-þjónustu (sjónræn stafakennsl) stofna rafræn skjöl sem hægt er að umbreyta í skráarfærslur innan [!INCLUDE[prod_short](includes/prod_short.md)]. Veljið uppfærslupakka sem er viðeigandi fyrir fyrirtækið og/eða landið/svæðið. Að öðrum kosti er hægt að stofna færslur handvirkt til að tákna ytri skjölin.  

Á síðunni **Skjöl á innleið** er hægt að nota ólíkar aðgerðir til að yfirfara kostnaðarkvittanir, sýsla með OCR-verk og breyta skjölum á innleið, handvirkt eða sjálfvirkt, yfir í viðkomandi skjöl eða færslubókarlínur í. Ytri skrárnar er hægt að hengja við tengd skjöl á öllum stigum úrvinnslunnar, þ.m.t. við bókuð skjöl og við færslur lánardrottins, viðskiptamanns eða fjárhags sem verða til.

Ferlið vegna skjal á innleið getur samanstaðið af eftirfarandi aðgerðir:

* Skrá ytri skjöl innan [!INCLUDE[prod_short](includes/prod_short.md)] með því að stofna línur á síðunni **skjöl á innleið** með öðrum hvorum eftirfarandi hætti:
  * Handvirkt, með því að nota einfaldar aðgerðir, annaðhvort frá tölvu eða farsíma, í einn af eftirfarandi leiðum:
    * Notaðu hnappinn **Stofna úr skrá** og fylla svo út í viðeigandi reiti á síðunni **skjal á innleið**. Skráin er hengd við sjálfkrafa.  
    * Notaðu hnappinn **Nýtt** og fylltu svo út í viðeigandi reiti á síðunni **Skjal á innleið** og hengdu handvirkt tengda skrá við.
    * Úr spjaldtölvu eða síma, nota hnappinn **Stofna úr myndavél** til að stofna nýja færslu fyrir skjal á innleið og senda svo myndina í OCR-þjónustu, t.d.
  * Sjálfkrafa, með því að taka á móti skjal frá OCR þjónustu sem rafrænu skjali eftir að hafa sent tengda PDF eða myndaskrá til OCR þjónustuna með tölvupósti. Flýtiflipinn **Fjárhagsupplýsingar** er fylltur út sjálfkrafa á síðunni **skjal á innleið**.
* Nota OCR-þjónustu til að breyta PDF eða myndaskrár í rafræn skjöl sem hægt er að breyta í færslur fyrir skjöl í [!INCLUDE[prod_short](includes/prod_short.md)].
* Stofnið ný skjöl eða almenn færslubókarlínur fyrir færslur fyrir skjöl á innleið með því að slá inn upplýsingar um leið og þú lest þær úr skrám fyrir skjöl á innleið.
* Festið skjöl á innleið við innkaupa og söluskjöl með hvaða stöðu sem er, þar með talinn færslur fyrir lánardrottins, viðskiptamaður eða fjárhagsfærslur sem koma úr bókun.
* Skoða skjal á innleið og viðhengi þeirra úr hvaða innkaupa eða söluskjali eða færslu eða finna allar fjárhagsfærslur án færslna fyrir skjöl á innleið af síðunni **bókhaldslykill**.

| Til | Sjá |
| --- | --- |
| Setja upp valkostinn fyrir skjal á innleið og setja upp OCR-þjónustu. |[Setja upp skjöl á innleið](across-how-setup-income-documents.md) |
| Stofna færslur fyrir skjöl á innleið, festa skrár sem viðhengi, nota OCR til að breyta PDF í rafræn skjöl, breyta rafræn skjöl í færslur fyrir skjöl, endurskoða bókaðar sölur og innkaupaskjöl í færslum skjala á innleið. |[Vinnsla skjala á innleið](across-process-income-documents.md) |

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/incoming-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig

[Innkaup](purchasing-manage-purchasing.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]