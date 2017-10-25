---
title: "Flytja bankasjóði| Microsoft Docs"
description: "Þú getur millifært upphæðir frá einum bankareikningi til annars, meðal annars í ólíkum gjaldmiðlum, með því að bóka millifærsluna í færslubókina."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 20661cce60bc9007adb9767388bf5af6f9c3acb9
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-transfer-bank-funds"></a>Hvernig á að: Flytja bankainnistæður
Stundum þarf að bóka millifærslu á upphæðum af einum bankareikningi yfir á annan. Til að gera þetta verður að bóka á færslu í færslubók. Verkið er misjafnt eftir því hvort bankareikningarnir nota sama gjaldmiðil eða mismunandi gjaldmiðla.

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a>Millifærslur af einum bankareikningi á annan með sama gjaldmiðilskóða
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **færslubók** og velja svo viðeigandi tengil.
2. Reitirnir **Bókunardagsetning** og **Númer fylgiskjals** eru fylltir út í færslubókarlínu.
3. Í reitnum **Tegund reiknings** er valinn **Bankareikningur**.
4. Í reitnum **Reikningur númer** skal velja bankann sem flytja á bankainnistæðuna frá.
5. Heildarupphæðin sem á að úthluta í reitinn  **Upphæð** er færð inn.
6. Í reitnum **Tegund mótreiknings** er **Bankareikningur** valinn.
7. Í reitnum **Mótreikningur númer** skal velja bankareikninginn sem flytja á bankainnistæðuna til.
8. Bóka skal færslubókina.

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a>Færslur milli bankareikninga bókaðar með gjaldmiðilskótum
Til að færa fjármuni milli bankareikninga sem nota mismunandi gjaldmiðla, verður að bóka tvær færslubókarlínur.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **færslubók** og velja svo viðeigandi tengil.
2. Búið til tvær færslubókarlínur og fyllið út reitina **Bókunardagsetning** og **Númer fylgiskjals**.
3. Í fyrstu færslubókarlínunni skal færa inn **Bankareikningur** í reitnum **Tegund reiknings**.
4. Í reitnum **Reikningur númer** skal velja bankann sem flytja á bankainnistæðuna frá.
5. Í reitnum **Upphæð** er rituð upphæðin sem er í gjaldmiðli bankareiknings. Færið inn kreditáætlunarupphæð með neikvæðu formerki. Færið inn debetáætlunarupphæð með neikvæðu formerki.
6. Í reitnum **Tegund mótreiknings** er **Bankareikningur** valinn.
7. Í reitnum **Mótreikningur númer** skal velja bankareikninginn sem flytja á bankainnistæðuna til.
8. Í seinni færslubókarlínunni skal færa inn **Bankareikningur** í reitnum **Tegund reiknings**.
9. Í reitnum **Reikningur númer** skal velja bankareikninginn sem flytja á bankainnistæðuna til.
10. Í reitnum **Upphæð** er rituð upphæðin sem er í gjaldmiðli bankareiknings. Færið inn kreditáætlunarupphæð með neikvæðu formerki. Færið inn debetáætlunarupphæð með neikvæðu formerki.
11. Í reitnum **Tegund mótreiknings** er **Bankareikningur** valinn.  
12. Í reitnum **Mótreikningur númer** skal velja bankareikninginn sem flytja á bankainnistæðuna frá.

    > [!NOTE]  
>   Ef gengið sem notað er í færslunni er annað en gengið í glugganum **Gengi gjaldmiðils** þarf að bæta inn þriðju línunni fyrir gengishagnað eða -tap. Færið inn **Fjárhagsreikning** í reitnum **Tegund reiknings**. Færið inn fjárhagsreikningsnúmer fyrir gengishagnað eða -tap í reitinn **Reikningur nr.**. Færa inn gengishagnað eða -tap í reitinn **Upphæð** með eða án neikvæðs formerkis, eftir því hvort um er að ræða kreditupphæð eða debetupphæð.
13. Bóka skal færslubókina.

## <a name="see-also"></a>Sjá einnig
[Stjórna bankareikningum](bank-manage-bank-accounts.md)  
[Uppsetning bankaþjónustu](bank-setup-banking.md)  
[Vinna í færslubókum](ui-work-general-journals.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

