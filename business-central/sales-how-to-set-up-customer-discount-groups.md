---
title: Setja upp afsláttarflokka viðskiptamanns
description: Kynntu þér hvernig á að setja upp afsláttarflokka viðskiptamanna og búðu til sölulínuafslætti fyrir þessa flokka.
author: rubenseishima
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 06/08/2022
ms.author: a-reishima
---
# <a name="set-up-customer-discount-groups" />Setja upp afsláttarflokka viðskiptamanns

Þú getur skilgreint sölulínuafslætti fyrir hóp viðskiptamanna í stað þess að nota hann fyrir hvern og einn.

**Afsláttarflokkar viðskiptamanna** virka svipað og [verðflokkar viðskiptamanns](sales-how-to-set-up-customer-price-groups.md) en hægt er að sameina við vöruafsláttarflokka til að setja á línuafslætti á fljótlegan hátt á margar vörur fyrir valda viðskiptamenn.

## <a name="create-sales-line-discounts-for-a-customer-group" />Stofna sölulínuafslátt fyrir viðskiptamann

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") tákn, fara í **Afsláttarflokkar viðskiptamanna** og velja síðan viðkomandi tengil.
2. Á síðunni **Afsláttarflokkar viðskiptamanna** skal velja **Nýr** til að búa til nýjan afsláttarflokk og gefa honum heiti undir dálknum **Kóði** og bæta við lýsingu.
3. Veldu aðgerðina **Skoða** og veldu **Sölulínuafslættir**.
4. Fylltu út dálkinn **Sölukóði** með afsláttarflokknum sem var búinn til á fyrri síðu.
5. Fylltu út reitina í línunum með **Tegund** (vara eða vöruafsláttarflokkur), **Kóði**, **Mælieiningarkóði** og **Línuafsláttur %**.
6. Ef viðskiptamannsflokkurinn þarf að kaupa lágmarksmagn til að fá afsláttinn skal fylla út reitinn **Lágmarksmagn**.
7. Ef nauðsyn krefur skal færa inn **Upphafsdagsetning** og **Lokadagsetning** fyrir afsláttarflokkinn.
8. Ef það á við getur þú einnig tilgreint **Gjaldmiðilskóðann** eða **Afbrigðiskóðann** eftir [sérstillingu dálkanna](ui-personalization-user.md).

Endurtaktu skref 4 til 8 fyrir hverja vöru eða vöruafsláttarflokk sem á að búa til sölulínuafslátt fyrir.

## <a name="assign-a-customer-to-a-discount-group" />Úthluta viðskiptavini á afsláttarhóp

Þegar búið er að setja upp afsláttarflokka viðskiptamanna er hægt að setja kóða afsláttarflokkanna á viðskiptamannaspjöldin.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptavinir** og velja síðan viðkomandi tengil.
2. Opnaðu **Viðskiptamannaspjaldið** fyrir viðskiptamann sem á að vera hlut af afsláttarflokki viðskiptamanna.
3. Í flýtiflipanum **Reikningsfærsla**, í reitnum **Afsláttarflokkur viðskiptamanna** skal velja kóða flokksins.

## <a name="see-also" />Sjá einnig .

[Sala](sales-manage-sales.md)  
[Uppsetning sölu](sales-setup-sales.md)  
[Skrá sérstök söluverð og afslætti](sales-how-record-sales-price-discount-payment-agreements.md)  
[Uppsetning verðflokka viðskiptamanna](sales-how-to-set-up-customer-price-groups.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
