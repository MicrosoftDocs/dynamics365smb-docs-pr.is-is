---
title: Setja upp afsláttarflokka viðskiptamanna
description: Lærðu að setja upp afsláttarflokka viðskiptamanna og stofna sölulínuafslátt fyrir þessa flokka.
author: rubenseishima
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 06/08/2022
ms.author: a-reishima
ms.openlocfilehash: fc2e5af5792a4c212c56b2e8a8a28b3b48ecff33
ms.sourcegitcommit: 7b6d70798b4da283d1d3e38a05151df2209c2b72
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/12/2022
ms.locfileid: "8950585"
---
# <a name="set-up-customer-discount-groups"></a>Setja upp afsláttarflokka viðskiptamanna

Hægt er að skilgreina sölulínuafslætti fyrir flokk viðskiptamanna í stað þess að sækja um þá sérstaklega.

**Afsláttarflokkar** viðskiptamanna vinna álíka mikið í [verðflokkum](sales-how-to-set-up-customer-price-groups.md) viðskiptamanna en hægt er að sameina við vöruafsláttarflokka til að stilla línuafslátt á einfaldan hátt á margar vörur fyrir valda viðskiptamenn.

## <a name="create-sales-line-discounts-for-a-customer-group"></a>Stofna sölulínuafslátt fyrir viðskiptavinaflokk

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **diskóklashópa** viðskiptavina og velja síðan tengda tengilinn.
2. **Á síðunni afsl. Flokkar** viðskiptamanna skal velja **nýtt** til að stofna nýjan afsláttarflokk og gefa honum heiti undir **kótanum** og bæta við lýsingu.
3. **Veljið færsluaðgerðina** aðgerð og veljið **sölulínuafslátt**.
4. **Reiturinn Kóti sölukóta** er fylltur út með afsláttarflokki sem stofnaður er á fyrri síðu.
5. Reitirnir í línunum eru fylltir út með **tegundinni** (vara-eða Vöruafsláttarflokkur), **kóti**, **Mælieiningarkóti** og **línuafsláttar%**.
6. Ef Viðskiptavinaflokkur þarf að kaupa inn lágmarksmagn til þess að fá afsláttinn er reiturinn Lágmarksmagn **fylltur út**.
7. Færa inn **upphafs** -og **lokadagsetningu** afsláttarflokksins ef þörf krefur.
8. Ef við á, er einnig hægt að **Tilgreina gjaldmiðilskóða** eða **afbrigðiskóta** eftir [að búið er að sérsníða dálkana](ui-personalization-user.md).

Endurtakið skref 4 til 8 fyrir hvern vöru eða vöruafsláttarflokk sem á að stofna sölulínuafslátt fyrir.

## <a name="assign-a-customer-to-a-discount-group"></a>Úthluta afsláttarflokki viðskiptavinar

Eftir að afsláttarflokkar viðskiptamanna hafa verið settir upp er hægt að færa inn afsláttarflokkskóta viðskiptamanns á viðskiptamannaspjöldum.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptavinir** og velja síðan viðkomandi tengil.
2. **Opnið viðskiptamannaspjald** viðskiptavinar sem óskað er eftir að verði hluti af afsláttarflokki viðskiptamanns.
3. **Á flipanum Reikningsfæra** í **reitnum Afsl. flokkur** viðskiptavina er valinn flokkskóti.

## <a name="see-also"></a>Sjá einnig .

[Sala](sales-manage-sales.md)  
[Uppsetning sölu](sales-setup-sales.md)  
[Taka upp sérstakt söluverð og afslætti](sales-how-record-sales-price-discount-payment-agreements.md)  
[Uppsetning verðflokka viðskiptamanna](sales-how-to-set-up-customer-price-groups.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
