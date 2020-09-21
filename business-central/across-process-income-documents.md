---
title: Vinnsla skjala á innleið | Microsoft Docs
description: Til að skrá ytra skjal, eins og t.d. PDF, í Business Central, verður fyrst að stofna eða ljúka við færslu skjals á innleið.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 9e6ce88485fcceeba9b35d8a309e9c7d73b40dae
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2020
ms.locfileid: "3778885"
---
# <a name="processing-incoming-documents"></a>Vinnsla skjala á innleið
Til að skrá ytra skjal í [!INCLUDE[d365fin](includes/d365fin_md.md)] verður fyrst að stofna eða ljúka við færslu fyrir skjal á innleið. Þú getur gert þetta með handvirkt, eða þú getur tekið mynd af ytra skjal og síðan að búa til skjal á innleið með myndaskrá í viðhengi.

Úr PDF-skjölum eða myndaskrám sem standa fyrir skjöl á innleið er hægt að láta ytri OCR-þjónustu (sjónræn stafakennsl) stofna rafræn skjöl sem hægt er að umbreyta í skráarfærslur í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Þegar reikningur berst frá lánardrottni á PDF-sniði er til dæmis hægt að senda hann til OCR-þjónustu af síðunni **Skjöl á innleið**. Einnig getur þú sent skrána í OCR þjónustu með tölvupósti. Þá, þegar þú færð rafræna skjal aftur, er tengd færsla fyrir skjal á innleið búin til sjálfkrafa. Eftir nokkrar sekúndur berst skráin aftur sem rafrænn reikningur sem hægt er að breyta í innkaupareikning fyrir lánardrottin.

| Til | Sjá |
| --- | --- |
| Búa til færslur fyrir skjöl á innleið handvirkt eða sjálfvirkt með því að taka mynd af pappírskvittun, til dæmis. |[Stofna færslur skjala á innleið](across-how-create-income-document-records.md) |
| Notið OCR-þjónustu til að breyta PDF eða myndaskrár í rafræn skjöl sem hægt er að breyta í innkaupareikninga í [!INCLUDE[d365fin](includes/d365fin_md.md)], til dæmis. Þjálfa OCR-þjónustu til að forðast villur næst þegar það vinnur álíka gögn. |[Nota OCR til að breyta PDF og myndaskrám í rafræn skjöl](across-how-use-ocr-pdf-images-files.md) |
| Tengja eða fjarlægja færslur fyrir skjal á innleið við óbókuð sölu- eða innkaupaskjöl og við viðskiptamaður, lánardrottin eða fjárhagsfærsla úr skjali eða færslu. |[Stofna færslur yfir Skjöl á innleið, beint úr Skjöl og Færslur](across-how-connect-disconnect-income-document-records.md) |
| Af síðunum **Bókhaldslyklar** og **Fjárhagsfærslur** er hægt að nota leitaraðgerð til að finna fjárhagsfærslur fyrir bókuð skjöl sem hafa ekki færslur fyrir skjöl á innleið og tengjast miðlægt við fyrirliggjandi færslur eða stofna nýjar með viðhengdum skrám. |[Finna bókuð fylgiskjöl án færslu skjals á innleið](across-how-find-posted-documents-without-income-document-records.md) |
| Fá betri yfirsýn með því að stilla færslur fyrir skjal á innleið sem unnið, til að fjarlægja þá úr sjálfgefna yfirlitinu. |[Vinna með margar færslur skjala á innleið](across-how-manage-many-income-document-records.md) |

## <a name="see-also"></a>Sjá einnig
[Skjöl á innleið](across-income-documents.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
