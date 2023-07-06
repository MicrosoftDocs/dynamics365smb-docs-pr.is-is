---
title: Stuttur leiðarvísir um fjárhagsupplýsingar
description: Búðu fyrirtækið þitt undir viðskipti með því að setja upp fjárhagsupplýsingarnar í Business Central.
author: rubenseishima
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: quickstart
ms.search.form: null
ms.date: 08/25/2022
ms.author: a-reishima
---

# <a name="financial-information-quick-start"></a><a name="financial-information-quick-start"></a><a name="financial-information-quick-start"></a>Stuttur leiðarvísir um fjárhagsupplýsingar

Eftir að hafa slegið inn grunnupplýsingar fyrirtækisins í [!INCLUDE[prod_short](includes/prod_short.md)] er eitt af næstu skrefum að ljúka við fjármálahlutann. Þetta er ekki bara gert til að taka á móti eða senda greiðslu heldur líka til að stjórna og gefa upp númer fyrirtækisins á viðeigandi hátt.

## <a name="the-chart-of-accounts"></a><a name="the-chart-of-accounts"></a><a name="the-chart-of-accounts"></a>Bókhaldslykillinn

Bókhaldslykillinn býður upp á yfirlit yfir fjármál fyrirtækisins, sýnir lista yfir reikninga í skipulögðum flokkum eins og eignum, skuldum, tekjum, kostnaði seldra vara og útgjöldum. [!INCLUDE[prod_short](includes/prod_short.md)] inniheldur staðlaðan bókhaldslykil sem hægt er að sérsníða að bókhaldsvenjum fyrirtækisins.

## <a name="set-up-the-chart-of-accounts"></a><a name="set-up-the-chart-of-accounts"></a><a name="set-up-the-chart-of-accounts"></a>Uppsetning bókhaldslykla

Eftirfarandi myndband sýnir hvernig á að setja upp bókhaldslykilinn í [!INCLUDE[prod_short](includes/prod_short.md)].

<br /><br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]

### <a name="add-an-account-to-the-chart-of-accounts"></a><a name="add-an-account-to-the-chart-of-accounts"></a><a name="add-an-account-to-the-chart-of-accounts"></a>Bæta reikningi við bókhaldslykilinn

Til að bæta við reikningi sem er ekki sjálfgefið innifalinn í [!INCLUDE[prod_short](includes/prod_short.md)], t.d. garðyrkjuþjónusta, skal fylgja þessum skrefum:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bókhaldslykill**, velja síðan viðkomandi tengil.
2. Veldu aðgerðina **Nýr** til að opna síðuna **Fjárhagsspjald**.
3. Færðu inn eftirfarandi gögn í samsvarandi reiti í flýtiflipanum **Almennt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   | Svæði | Gögn |
   | --- | --- |
   | **Nr.** | 61250 |
   | **Heiti** | Garðyrkjuþjónusta |
   | **Rekstur/efnahagur** | Rekstrarreikningur |
   | **Reikningsflokkur** | Útgjöld |
   | **Undirflokkur reiknings** | Viðgerða- og viðhaldskostnaður |
   | **Debet/Kredit** | Bæði |
   | **Tegund reiknings** | Bóka |

4. Í flýtiflipanum **Bókun** skal færa inn eftirfarandi gögn:

   | Svæði | Gögn |
   | --- | --- |
   | **Alm. bókunartegund** | Innkaup |
   | **Alm. viðsk.bókunarflokkur** | Innanlands |
   | **Alm. vörubókunarflokkur** | Þjónusta |

5. Fylltu út eftirstandandi reiti á síðunni **Fjárhagsspjald** eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="get-an-overview-of-the-chart-of-accounts"></a><a name="get-an-overview-of-the-chart-of-accounts"></a><a name="get-an-overview-of-the-chart-of-accounts"></a>Fá yfirlit yfir bókhaldslykilinn

Ef þú þarft þéttara yfirlit yfir bókhaldslykil, án dálka fyrir bókunarflokka, bókunargerð eða kostnaðargerð sem dæmi, sýnir **Yfirlit bókhaldslykils** meginupplýsingar fyrir hvern reikning í smærri töflu. Þar að auki er hægt að draga saman eða stækka hópa til að fela aðgangana inni í þeim.

Til að birta yfirlitið skaltu velja aðgerðina **Yfirlit bókhaldslykils** á síðunni **Bókhaldslykill** eða leita að eiginleika með ![Ljósapera sem opna eiginleika viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera").

Frekari upplýsingar um bókhaldslykilinn og fjárhaginn er að finna í [Að skilja fjárhaginn og bókhaldslykilinn](finance-general-ledger.md).

## <a name="set-up-bank-accounts"></a><a name="set-up-bank-accounts"></a><a name="set-up-bank-accounts"></a>Bankareikningar settir upp

Bankareikningar í [!INCLUDE[prod_short](includes/prod_short.md)] skrá bankafærslur og tengjast færslum í bókhaldslyklinum. Eftirfarandi myndband sýnir hvernig á að setja upp bankareikninga.

<br /><br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Vhpl?rel=0]

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bankareikningar**, velja síðan viðkomandi tengil.
2. Á síðunni **bankareikningar** skal velja aðgerðina **Nýtt**.
3. Í reitnum **númer** reitur, auðkenni eins og *B010* verður slegið inn sjálfkrafa ef númeraraðalisti er valinn fyrir bankareikninga. Ef ekki skal færa inn einkvæma samsetningu.

   Reiturinn er annar en í reitnum **Bankareikningsnr.** sem einnig er í boði í flýtiflipanum **Almennt**.
4. Fylla skal út í reitina á síðunni **Bankareikningsspjald** eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-related-training-at-microsoft-learn"></a><a name="see-related-training-at-microsoft-learn"></a><a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/paths/set-up-financial-management-dynamics-365-business-central/).

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Sjá einnig .

[Uppsetning bókhaldslykla](finance-setup-chart-accounts.md)  
[Bankareikningar settir upp](bank-how-setup-bank-accounts.md)  
[Keyra og prenta skýrslur](ui-work-report.md)  
[Stuttir leiðarvísar Business Central](quick-start-business-central.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
