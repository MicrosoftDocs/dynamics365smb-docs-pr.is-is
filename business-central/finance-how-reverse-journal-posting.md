---
title: Afturkalla bókun með bókun bakfærslu
description: Ef þú hefur framkvæmt ranga bókun í færslubók, geturðu notað bakfærsluaðgerðina til að afturkalla bókunina með réttri endurskoðunarslóð.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.search.form: 20, 25, 29, 38, 202, 5912,
ms.date: 07/22/2021
ms.author: bholtorf
ms.openlocfilehash: d00f8b355e25e15a6aa610dd3392bfc63b7bfad3
ms.sourcegitcommit: 5bb13966e9ba8d7a3c2f00dd32f167acccf90b82
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728681"
---
# <a name="reverse-journal-postings-and-undo-receiptsshipments"></a>Bakfæra bókun Færslubókar og afturkalla kvittanir/sendingar

Bakfærslubókanir eru gagnlegar til dæmis, til að leiðrétta villur og til að hreinsa út gamlar uppsöfnunar færslur áður en nýtt er fært inn. Bakfærsla er sú sama og upprunalega færslan en er með gagnstæðan kladda í **upphæðarreitnum**. Bakfærslan verður að hafa sama fylgiskjalsnúmer og bókunardagsetninguna og upphaflega færslan. Eftir að færsla hefur verið bakfærð verður að gera rétta færslu.

Aðeins er hægt að bakfæra færslu sem er bókuð frá færslubókarlínu. Aðeins er hægt að bakfæra skráningu í eitt skipti.

Til að afturkalla móttöku-eða sendingarbókun áður en bókað er sem reikningsfært er hægt að nota **ógilda** aðgerðina á bókaða skjalinu. Hægt er að afturkalla magn af gerðinni **Vara** og **Tilfang**.

Ef bókað hefur verið rangt neikvætt magn, til dæmis innkaupapöntun með rangan vörumagn, sem móttekinn en ekki reikningsfært, er hægt að afturkalla bókunina.

Ef bókað hefur verið rangt jákvætt magn, til dæmis söluafhending eða innkaupaskilasending með röngum fjölda vara, sem afhendar en ekki reikningsfærðar, er hægt að afturkalla bókunina.

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a>Að bakfæra færslubókarbókun fjárhagsfærslu

Hægt er að bakfæra færslur af öllum síðum **Fjárhagsfærslur**. Eftirfarandi ferli byggist á **Fjárhagsfærslur** síðunni.

> [!NOTE]
> Færslan verður að koma úr bókun færslubókar.
>
> Einnig er ekki hægt að bakfæra færslur sem hafa verið bókaðar með upplýsingum úr vinnslu eða sem hafa innleystan hagnað og tap innan sömu færslu.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, farðu í **Fjárhagsfærslur** og veldu síðan tengda tengilinn.
2. Veljið færsluna sem á að bakfæra og veljið síðna aðgerðina **Bakfæra færslu**.
3. Á síðunni **Bakfærðar viðskiptafærslur** skal velja aðgerðina **Bakfæra**.
4. Veldu **Já** til að staðfesta bakfærsluna.

## <a name="to-post-a-negative-entry"></a>Að bóka neikvæða færslu  

**Notaðu reitinn leiðrétting** til að bóka neikvæða debetfærslu í stað kreditfærslu eða til að bóka neikvæða inneign í staðinn fyrir debet á reikning. Sjálfgefið er að svæðið sé tiltækt í öllum færslubókum. Reitirnir **Debetupphæð** og **Kreditupphæð** innihalda bæði upphaflegu færsluna og leiðréttu færsluna. Þessir reitir hafa engin áhrif á reikningsstöðuna.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Færslubækur** og velja síðan viðkomandi tengil  
2. Í reitnum **Heiti keyrslu** skal velja viðeigandi heiti keyrslu.  
3. Færið inn upplýsingar í viðkomandi reiti.  
4. Í færslubókarlínu sem á að virkja fyrir neikvæðar færslur skal velja gátreitinn **Leiðrétting**.  
5. Til að bóka færslubókina skal velja aðgerðina **Bóka** og síðan smella á hnappinn **Já**.

## <a name="to-undo-a-quantity-on-a-posted-purchase-receipt"></a>Magn á bókaða innkaupamóttöku afturkallað  

Eftirfarandi skref lýsa því hvernig á að afturkalla bókaða móttöku vara eða forða. Skrefin eru svipuð fyrir bókaðar sendingar.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") tákn, fara í **Bókaðar innkaupamóttökur** og velja síðan viðkomandi tengil.  
2. Opna bókuðu móttökuna sem á að afturkalla.  
3. Velja skal línuna eða línurnar sem þú vilt afturkalla.  
4. Veldu **Afturkalla móttöku** aðgerðina.

Leiðréttingarlínu er bætt við valda móttökulínu. Ef magn var móttekið í vöruhúsamóttöku er leiðréttingarlínu bætt við bókaða vöruhúsamóttöku.  

Reitirnir **Móttekið magn** og **Móttekið magn, óreikningsfært** svæði í tengdri innkaupapöntun eru stilltir á núll.

## <a name="to-undo-and-then-redo-a-quantity-posting-on-a-posted-return-shipment"></a>Hvernig skal afturkalla og endurgera magnbókun á bókaða skilaafhendingu.

Eftirfarandi liðir lýsa því hvernig á að:

* Afturkalla bókaða vöruskilaafhendingu á vörum eða forða.
* Endurbókið innkaupin aftur með nýju magni.

Skrefin eru svipuð fyrir bókaðar vöruskilamóttökur.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") tákn, fara í **Bókaðar skilaafhendingar** og velja síðan viðkomandi tengil.  
2. Opna bókaða vöruskilaafhendinguna sem á að afturkalla.
3. Línan eða línurnar eru valdar til að afturkalla.  

4. Velja skal aðgerðina **Afturkalla vöruskilaafhendingu**.  

    Leiðréttingarlína er sett í bókaða fylgiskjalið og reitirnir **Skilamagn afhent** og **Skilaupph. afhent óreikningsf.** í innkaupabeiðninni eru settir á núll.  

    Farið nú aftur í innkaupaskilapöntunina til að endurtaka bókunina.  

5. Á síðunni **Bókuð skilaafhending** takið mið af tölunni á svæðinu **Skilapöntun nr**. .  
6. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Skilapantanir innkaupa** og velja síðan viðkomandi tengil.  
7. Opna skilapöntunina sem um ræðir og velja síðan **Enduropna** aðgerðina.  
8. Leiðrétta færsluna í **Magn** reitnum og bóka skilapöntun innkaupa aftur.  

[!INCLUDE [rev-general-journal](includes/rev-general-journal.md)]

## <a name="see-also"></a>Sjá einnig

[Afturkalla samsetningarbókun](assembly-how-to-undo-assembly-posting.md)  
[Bóka færslu beint í Fjárhag](finance-how-post-transactions-directly.md)  
[Vinna við Almennar færslubækur](ui-work-general-journals.md)  
[Fjármál](finance.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]