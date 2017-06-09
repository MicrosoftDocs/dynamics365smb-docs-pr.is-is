---
title: "Hvernig á að: Flytja bankasjóði | Microsoft Docs"
description: "Hvernig á að: Flytja bankainnistæður"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 03/32/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: e2e3642d08428367fac1dd5845013e14627fe6ed
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-transfer-bank-funds"></a>Hvernig á að: Flytja bankainnistæður
Stundum þarf að bóka millifærslu á upphæðum af einum bankareikningi yfir á annan. Til að gera þetta verður að bóka á færslu í færslubók. Verkið er misjafnt eftir því hvort bankareikningarnir nota sama gjaldmiðil eða mismunandi gjaldmiðla.

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a>Millifærslur af einum bankareikningi á annan með sama gjaldmiðilskóða
1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Færslubók**, og velja síðan viðeigandi tengil.
2. **Bókunardagsetning** og **Númer fylgiskjals** eru fylltir út í færslubókarlínu. Reitir
3. Í reitnum **Tegund reiknings** er valinn **Bankareikningur**.
4. Í svæðinu **Bankareikningsnúmer**,  veljið bankann sem flytja á bankainnistæðuna frá.
5. Heildarupphæðin sem á að úthluta í reitinn  **Upphæð** er færð inn.
6. Í reitnum **Tegund mótreiknings** er **Bankareikningur** valinn.
7. Í svæðinu **Númer mótreiknings**,  veljið bankareikninginn sem flytja á bankainnistæðuna til.
8. Bóka skal færslubókina.

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a>Færslur milli bankareikninga bókaðar með gjaldmiðilskótum
Til að færa fjármuni milli bankareikninga sem nota mismunandi gjaldmiðla, verður að bóka tvær færslubókarlínur.

1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Færslubók**, og velja síðan viðeigandi tengil.
2. Búið til tvær færslubókarlínur og fyllið út reitina **Bókunardagsetning** og **Númer fylgiskjals**. Reitir
3. Í fyrstu færslubókarlínunni skal færa inn **Bankareikningur** í reitnum **Tegund reiknings**.
4. Í svæðinu **Bankareikningsnúmer**,  veljið bankareikninginn sem flytja á bankainnistæðuna frá.
5. Í reitnum **Upphæð** er rituð upphæðin sem er í gjaldmiðli bankareiknings. Færið inn kreditáætlunarupphæð með neikvæðu formerki. Færið inn debetáætlunarupphæð með neikvæðu formerki.
6. Í reitnum **Tegund mótreiknings** er **Bankareikningur** valinn.
7. Í svæðinu **Númer mótreiknings**,  veljið bankareikninginn sem flytja á bankainnistæðuna til.
8. Í seinni færslubókarlínunni skal færa inn **Bankareikningur** í reitnum **Tegund reiknings**.
9. Í svæðinu **Bankareikningsnúmer**,  veljið bankareikninginn sem flytja á bankainnistæðuna til.
10. Í reitnum **Upphæð** er rituð upphæðin sem er í gjaldmiðli bankareiknings. Færið inn kreditáætlunarupphæð með neikvæðu formerki. Færið inn debetáætlunarupphæð með neikvæðu formerki.
11. Í reitnum **Tegund mótreiknings** er **Bankareikningur** valinn.  
12. Í svæðinu **Númer mótreiknings**,  veljið bankareikninginn sem flytja á bankainnistæðuna frá.

    **Athugið**: Ef gengið sem notað er í færslunni er annað en gengið í glugganum **Gengi gjaldmiðils** þarf að bæta inn þriðju línunni fyrir gengishagnað eða -tap. Færið inn **Fjárhagsreikning** í reitnum **Tegund reiknings**. Færið inn fjárhagsreikningsnúmer fyrir gengishagnað eða -tap í reitinn **Reikningur nr.**. . Færa inn gengishagnað eða -tap í reitinn **Upphæð** með eða án neikvæðs formerkis, eftir því hvort um er að ræða kreditupphæð eða debetupphæð.
13. Bóka skal færslubókina.

## <a name="see-also"></a>Sjá einnig
[Stjórna bankareikningum](bank-manage-bank-accounts.md)  
[Uppsetning bankaþjónustu](bank-setup-banking.md)  
[Vinna í færslubókum](ui-work-general-journals.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

