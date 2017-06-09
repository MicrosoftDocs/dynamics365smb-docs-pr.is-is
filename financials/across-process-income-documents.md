---
title: "Vinnsla skjala á innleið| Microsoft Docs"
description: "Vinnsla skjala á innleið"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 05/12/2016
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 93a3ba01e479ba8256f4a3628aae2b7838d8e5ad
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="processing-incoming-documents"></a>Vinnsla skjala á innleið
Til að skrá ytra skjal í [!INCLUDE[d365fin](includes/d365fin_md.md)] verður fyrst að stofna eða ljúka við færslu fyrir skjal á innleið. Þú getur gert þetta með handvirkt, eða þú getur tekið mynd af ytra skjal og síðan að búa til skjal á innleið með myndaskrá í viðhengi.

Úr PDF-skjölum eða myndaskrám sem standa fyrir skjöl á innleið er hægt að láta ytri OCR-þjónustu (sjónræn stafakennsl) stofna rafræn skjöl sem hægt er að umbreyta í skráarfærslur í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Til dæmis Þegar reikningur berst frá lánardrottni á PDF-sniði er til dæmis hægt að senda hann til OCR-þjónustu úr glugganum **Skjöl á innleið**. Einnig getur þú sent skrána í OCR þjónustu með tölvupósti. Þá, þegar þú færð rafræna skjal aftur, er tengd færsla fyrir skjal á innleið búin til sjálfkrafa. Eftir nokkrar sekúndur berst skráin aftur sem rafrænn reikningur sem hægt er að breyta í innkaupareikning fyrir lánardrottin.

| Til | Sjá |
| --- | --- |
| Búa til færslur fyrir skjöl á innleið handvirkt eða sjálfvirkt með því að taka mynd af pappírskvittun, til dæmis. |[Hvernig á að: Stofna færslur skjala á innleið](across-how-create-income-document-records.md) |
| Notið OCR-þjónustu til að breyta PDF eða myndaskrár í rafræn skjöl sem hægt er að breyta í innkaupareikninga í [!INCLUDE[d365fin](includes/d365fin_md.md)], til dæmis. Þjálfa OCR-þjónustu til að forðast villur næst þegar það vinnur álíka gögn. |[Hvernig á að: Nota OCR til að breyta PDF og myndaskrám í rafræn skjöl](across-how-use-ocr-pdf-images-files.md) |
| Tengja eða fjarlægja færslur fyrir skjal á innleið við óbókuð sölu- eða innkaupaskjöl og við viðskiptamaður, lánardrottin eða fjárhagsfærsla úr skjali eða færslu. |[Hvernig á að: Tengja og aftengja færslur skjals á innleið úr Skjölum og færslum](across-how-connect-disconnect-income-document-records.md) |
| Úr gluggunum **Bókhaldslyklar** og **Fjárhagsfærslur**, nota leitaraðgerð til að finna fjárhagsfærslur fyrir bókuð skjöl sem hafa ekki færslur fyrir skjöl á innleið og tengjast miðlægt við fyrirliggjandi færslur eða stofna nýjar með viðhengdum skrám. |[Hvernig á að: Finna bókuð fylgiskjöl án færslu skjals á innleið](across-how-find-posted-documents-without-income-document-records.md) |
| Fá betri yfirsýn með því að stilla færslur fyrir skjal á innleið sem unnið, til að fjarlægja þá úr sjálfgefna yfirlitinu. |[Hvernig á að: Vinna með margar færslur skjala á innleið](across-how-manage-many-income-document-records.md) |

## <a name="see-also"></a>Sjá einnig
[Skjöl á innleið](across-income-documents.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

