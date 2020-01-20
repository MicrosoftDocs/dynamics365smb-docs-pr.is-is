---
title: Flytja bankasjóði| Microsoft Docs
description: Þú getur millifært upphæðir frá einum bankareikningi til annars, meðal annars í ólíkum gjaldmiðlum, með því að bóka millifærsluna í færslubókina.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 12/13/2019
ms.author: sgroespe
ms.openlocfilehash: 3618ad87377ebc47f183292207d2f25dc6c3ed34
ms.sourcegitcommit: 3d128a00358668b3fdd105ebf4604ca4e2b6743c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2910421"
---
# <a name="transfer-bank-funds"></a>Flytja bankainnstæður
Stundum þarf að millifæra upphæð af einum bankareikningi í [!INCLUDE[d365fin](includes/d365fin_md.md)] yfir á annan. Til að gera þetta verður að bóka færsluna á síðunni **Færslubók**. Verkið er misjafnt eftir því hvort bankareikningarnir nota sama gjaldmiðil eða mismunandi gjaldmiðla.

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a>Millifærslur af einum bankareikningi á annan með sama gjaldmiðilskóða
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Færslubók** og veldu síðan tengda tengilinn.
2. Reitirnir **Bókunardagsetning** og **Númer fylgiskjals** eru fylltir út í færslubókarlínu.
3. Í reitnum **Tegund reiknings** er valinn **Bankareikningur**.
4. Í reitnum **Reikningur númer** skal velja bankann sem flytja á bankainnistæðuna frá.
5. Heildarupphæðin sem á að úthluta í reitinn  **Upphæð** er færð inn.
6. Veljið aðgerðina **Sýna fleiri dálka** til að skoða alla tiltæka reiti.
7. Í reitnum **Tegund mótreiknings** er **Bankareikningur** valinn.
8. Í reitnum **Mótreikningur númer** skal velja bankareikninginn sem flytja á bankainnistæðuna til.
9. Bóka skal færslubókina.

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a>Færslur milli bankareikninga bókaðar með gjaldmiðilskótum
Til að færa fjármuni milli bankareikninga sem nota mismunandi gjaldmiðla, verður að bóka tvær færslubókarlínur.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Færslubók** og veldu síðan tengda tengilinn.
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
    > Ef gengið sem notað er í færslunni er annað en gengið á síðunni **Gengi gjaldmiðils** þarf að bæta inn þriðju línunni fyrir gengishagnað eða -tap. Færið inn **Fjárhagsreikning** í reitnum **Tegund reiknings**. Færið inn fjárhagsreikningsnúmer fyrir gengishagnað eða -tap í reitinn **Reikningur nr.**. Færa inn gengishagnað eða -tap í reitinn **Upphæð** með eða án neikvæðs formerkis, eftir því hvort um er að ræða kreditupphæð eða debetupphæð.
13. Bóka skal færslubókina.

## <a name="see-also"></a>Sjá einnig
[Afstemming bankareikninga](bank-manage-bank-accounts.md)  
[Uppsetning bankaþjónustu](bank-setup-banking.md)  
[Vinna í færslubókum](ui-work-general-journals.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
