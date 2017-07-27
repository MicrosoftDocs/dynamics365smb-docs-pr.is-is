---
title: "Vinna með skjöl á innleið| Microsoft Docs"
description: "Hægt er að stjórna ytri viðskiptaskjölum á innleið, eins og greiðslukvittunum og PDF skrám, stjórna OCR verkum, og umbreyta skrám yfir í rafræn skjöl og færslur í Financials."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 8c15fded4b70ee0fce8ad43f90b915a33523fc77
ms.contentlocale: is-is
ms.lasthandoff: 07/07/2017


---
# <a name="incoming-documents"></a>Skjöl á innleið
Sumar viðskiptafærslur eru ekki skráðar í [!INCLUDE[d365fin](includes/d365fin_md.md)] upphaflega. Þess í stað ytri viðskipti skjal kemur í þitt fyrirtæki sem viðhengi eða pappír eintak sem þú grannskoða til skrá. Þetta er dæmigert við innkaup, þar sem slíkar skrár standa fyrir reikninga frá lánardrottnum eða greiðslukvittanir fyrir kostnað eða smáinnkaup.

Úr PDF-skjölum eða myndaskrám sem standa fyrir skjöl á innleið er hægt að láta ytri OCR-þjónustu (sjónræn stafakennsl) stofna rafræn skjöl sem hægt er að umbreyta í skráarfærslur innan [!INCLUDE[d365fin](includes/d365fin_md.md)].

Í glugganum **Skjöl á innleið** er hægt að nota ólíkar aðgerðir til að yfirfara kostnaðarkvittanir, sýsla með OCR-verk og breyta skjölum á innleið, handvirkt eða sjálfvirkt, yfir í viðkomandi skjöl eða færslubókarlínur í. Ytri skrárnar er hægt að hengja við tengd skjöl á öllum stigum úrvinnslunnar, þ.m.t. við bókuð skjöl og við færslur lánardrottins, viðskiptamanns eða fjárhags sem verða til.

Ferlið vegna skjal á innleið getur samanstaðið af eftirfarandi aðgerðir:

* Skrá ytri skjöl innan [!INCLUDE[d365fin](includes/d365fin_md.md)] með því að stofna línur í glugganum **skjöl á innleið** með öðrum hvorum eftirfarandi hætti:
  * Handvirkt, með því að nota einfaldar aðgerðir, annaðhvort frá tölvu eða farsíma, í einn af eftirfarandi leiðum:
    * Notaðu hnappinn **Stofna úr skrá** og fylla svo út í viðeigandi reiti í **skjal á innleið** glugganum. Skráin er hengd við sjálfkrafa.  
    * Notaðu **nýtt** hnapp og fylla svo út í viðeigandi reiti í **skjal á innleið** glugganum og hengja handvirkt tengda skrá við.
    * Úr spjaldtölvu eða síma, nota hnappinn **Stofna úr myndavél** til að stofna nýja færslu fyrir skjal á innleið og senda svo myndina í OCR-þjónustu, t.d.
  * Sjálfkrafa, með því að taka á móti skjal frá OCR þjónustu sem rafrænu skjali eftir að hafa sent tengda PDF eða myndaskrá til OCR þjónustuna með tölvupósti. Flýtiflipinn**Fjárhagsupplýsingar** er fylltur út sjálfkrafa í glugganum **skjal á innleið**.
* Nota OCR-þjónustu til að breyta PDF eða myndaskrár í rafræn skjöl sem hægt er að breyta í færslur fyrir skjöl í [!INCLUDE[d365fin](includes/d365fin_md.md)].
* Stofnið ný skjöl eða almenn færslubókarlínur fyrir færslur fyrir skjöl á innleið með því að slá inn upplýsingar um leið og þú lest þær úr skrám fyrir skjöl á innleið.
* Festið skjöl á innleið við innkaupa og söluskjöl með hvaða stöðu sem er, þar með talinn færslur fyrir lánardrottins, viðskiptamaður eða fjárhagsfærslur sem koma úr bókun.
* Skoða skjal á innleið og viðhengi þeirra úr hvaða innkaupa eða söluskjali eða færslu eða finna allar fjárhagsfærslur án færslna fyrir skjöl á innleið úr glugganum **bókhaldslykill**

| Til | Sjá |
| --- | --- |
| Setja upp valkostinn fyrir skjal á innleið og setja upp OCR-þjónustu. |[Hvernig á að: Setja upp skjöl á innleið](across-how-setup-income-documents.md) |
| Stofna færslur fyrir skjöl á innleið, festa skrár sem viðhengi, nota OCR til að breyta PDF í rafræn skjöl, breyta rafræn skjöl í færslur fyrir skjöl, endurskoða bókaðar sölur og innkaupaskjöl í færslum skjala á innleið. |[Vinnsla skjala á innleið](across-process-income-documents.md) |

## <a name="see-also"></a>Sjá einnig
[Innkaup](purchasing-manage-purchasing.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

