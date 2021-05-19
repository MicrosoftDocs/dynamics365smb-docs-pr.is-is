---
title: Flytja bankainnstæður
description: Þú getur millifært upphæðir frá einum bankareikningi til annars, meðal annars í ólíkum gjaldmiðlum, með því að bóka millifærsluna í færslubókina.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 04/29/2021
ms.author: edupont
ms.openlocfilehash: da9c8711751040cecb267a3b2209bad2534b618b
ms.sourcegitcommit: 08ca5798cf3f04fc3ea38fff40c1860196a70adf
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/06/2021
ms.locfileid: "5985388"
---
# <a name="transfer-bank-funds"></a>Flytja bankainnstæður

Stundum þarf að millifæra upphæð af einum bankareikningi í [!INCLUDE[prod_short](includes/prod_short.md)] yfir á annan. Til að gera þetta verður að bóka færsluna á síðunni **Færslubók**. Verkið er misjafnt eftir því hvort bankareikningarnir nota sama gjaldmiðil eða mismunandi gjaldmiðla.

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a>Millifærslur af einum bankareikningi á annan með sama gjaldmiðilskóða

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Færslubók** og veldu síðan tengda tengilinn.
2. Reitirnir **Bókunardagsetning** og **Númer fylgiskjals** eru fylltir út í færslubókarlínu.
3. Í reitnum **Tegund reiknings** er valinn **Bankareikningur**.
4. Í reitnum **Reikningur númer** skal velja bankann sem flytja á bankainnistæðuna frá.
5. Heildarupphæðin sem á að úthluta í reitinn  **Upphæð** er færð inn.

    Næst þarf að tilgreina mótreikninginn. Ef þú sérð ekki viðkomandi svæði skaltu velja aðgerðina **Sýna fleiri dálka** til að skoða öll tiltæk svæði.
6. Í reitnum **Tegund mótreiknings** er **Bankareikningur** valinn.
7. Í reitnum **Mótreikningur númer** skal velja bankareikninginn sem flytja á bankainnistæðuna til.
8. Bóka skal færslubókina.

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a>Færslur milli bankareikninga bókaðar með gjaldmiðilskótum

Til að færa fjármuni milli bankareikninga sem nota mismunandi gjaldmiðla, verður að bóka tvær færslubókarlínur.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Færslubók** og veldu síðan tengda tengilinn.
2. Búið til tvær færslubókarlínur og fyllið út reitina **Bókunardagsetning** og **Númer fylgiskjals**.
3. Í fyrstu færslubókarlínunni skal færa inn **Bankareikningur** í reitnum **Tegund reiknings**.
4. Í reitnum **Reikningur númer** skal velja bankann sem flytja á bankainnistæðuna frá.
5. Upphæðin er færð í reitinn **Upphæð** í gjaldmiðli bankareikningsins með eða án mínusmerkis.

    > [!TIP]
    > Upphæð með engu merki er debet og upphæð með mínusmerki er kreditupphæð.

    > [!NOTE]
    > Sum fyrirtæki kjósa frekar að færa milli reikninga til að aðskilja færslubókarlínur. Önnur fyrirtæki kjósa að bóka allt á einni færslubókarlínu með því að nota mótreikning. Hafðu samband við sérfræðing á staðnum ef þú ert ekki viss um hvað á að gera.
    >
    > Ef fyrirtækið þitt kýs að nota mótreikning skaltu stilla reitinn **Tegund mótreiknings** á **Bankareikningur** og stilla **Númer mótreiknings** á bankareikninginn sem færa á fjármunina yfir á. Haltu síðan áfram í skref 9 eða 10.
    >
    > Ef fyrirtækið þitt kýs að nota aðskilda færslubókarlínu skaltu fara í næsta skref.
6. Í seinni færslubókarlínunni skal færa inn **Bankareikningur** í reitnum **Tegund reiknings**.
7. Í reitnum **Reikningur númer** skal velja bankareikninginn sem flytja á bankainnistæðuna til.
8. Upphæðin er færð í reitinn **Upphæð** í gjaldmiðli bankareikningsins með eða án mínusmerkis.

    > [!TIP]
    > Upphæð með engu merki er debet og upphæð með mínusmerki er kreditupphæð.
9. Ef gengið sem notað er í færslunni er annað en gengið á síðunni **Gengi gjaldmiðils** þarf að bæta inn nýrri færslubókarlínu fyrir gengishagnað eða -tap.  

    1. Færið inn **Fjárhagsreikning** í reitnum **Tegund reiknings**.  

    2. Færið inn fjárhagsreikningsnúmer fyrir gengishagnað eða -tap í reitinn **Reikningur nr.**.  

    3. Færið inn gengishagnað eða -tap í reitinn **Upphæð** með eða án mínusmerkis.

    > [!TIP]
    > Upphæð með engu merki er debet og upphæð með mínusmerki er kreditupphæð.
10. Bóka skal færslubókina.

## <a name="see-also"></a>Sjá einnig

[Afstemming bankareikninga](bank-manage-bank-accounts.md)  
[Uppsetning bankaþjónustu](bank-setup-banking.md)  
[Vinna í færslubókum](ui-work-general-journals.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]