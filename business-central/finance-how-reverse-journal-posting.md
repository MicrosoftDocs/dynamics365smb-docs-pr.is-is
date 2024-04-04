---
title: Afturkalla bókun með bókun bakfærslu
description: Ef mistök finnast í bókaðri almennri færslubók er hægt að nota aðgerðina Bakfæra færslu til að afturkalla bókunina með réttri slóð endurskoðunar.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 03/28/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="reverse-journal-postings-and-undo-receiptsshipments"></a>Bakfæra bókun Færslubókar og afturkalla kvittanir/sendingar

Að bakfæra bókanir færslubókar eru gagnlegar sem dæmi til að leiðrétta villur og hreinsa út gamlar uppsöfnunarfærslur áður en ný er færð inn. Bakfærsla er sú sama og upphaflega færslan en hefur öfugt formerki í reitnum **Upphæð**. Bakfærslan verður að vera með sama fylgiskjalsnúmer og bókunardagsetningu og upphaflega færslan. Þegar færsla hefur verið bakfærð þarf að stofna rétta færslu.

Aðeins er hægt að bakfæra færslu sem er bókuð frá færslubókarlínu. Færslu er einungis hægt að bakfæra einu sinni.

Til að afturkalla móttöku-eða sendingarbókun, áður en hún er bókuð sem reikningsfærð er hægt að nota aðgerðina **afturkalla** á bókaða skjalinu. Hægt er að afturkalla magn af gerðinni **Vara** og **Tilfang**.

Ef þú hefur bókað rangt neikvætt magn, t.d. innkaupapöntun með röngum vörufjölda, sem móttekið en ekki reikningsfært, er hægt að afturkalla bókunina.

Ef þú hefur bókað rangt jákvætt magn, t.d. söluafhendingu eða innkaupaskilaafhendingu með röngum vörufjölda, sem afgreitt en ekki reikningsfært, er hægt að afturkalla bókunina.

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

Reiturinn **Leiðrétting** er notaður til að bóka neikvæða debetfærslu í stað kreditfærslu, eða til að bóka neikvæða kreditfærslu í stað debetfærslu á reikningi. Reiturinn er sjálfgefið í boði í öllum færslubókum. Reitirnir **Debetupphæð** og **Kreditupphæð** innihalda bæði upphaflegu færsluna og leiðréttu færsluna. Þessir reitir hafa engin áhrif á reikningsstöðuna.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Færslubækur** og velja síðan viðkomandi tengil  
2. Í reitnum **Heiti keyrslu** skal velja viðeigandi heiti keyrslu.  
3. Færið inn upplýsingar í viðkomandi reiti.  
4. Í færslubókarlínu sem á að virkja fyrir neikvæðar færslur skal velja gátreitinn **Leiðrétting**.  
5. Til að bóka færslubókina skal velja aðgerðina **Bóka** og síðan smella á hnappinn **Já**.

## <a name="to-undo-a-quantity-on-a-posted-purchase-receipt"></a>Að afturkalla magn í bókaðri innkaupakvittun

Eftirfarandi skref lýsir því hvernig á að hætta við bókaða kvittun á vörum eða tilföngum. Skrefin eru svipuð fyrir bókaðar sendingar.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") tákn, fara í **Bókaðar innkaupamóttökur** og velja síðan viðkomandi tengil.  
2. Opna bókuðu móttökuna sem á að afturkalla.  
3. Velja skal línuna eða línurnar sem þú vilt afturkalla.  
4. Veldu **Afturkalla móttöku** aðgerðina.

Leiðréttingarlínu er bætt við undir völdu móttökulínuna. Ef magnið var móttekið í vöruhúsamóttöku er leiðréttingarlínan bætt við bókuðu vöruhúsamóttökuna.  

Reitirnir **Móttekið magn** og **Móttekið magn, óreikningsfært** svæði í tengdri innkaupapöntun eru stilltir á núll.

## <a name="to-undo-and-then-redo-a-quantity-posting-on-a-posted-return-shipment"></a>Hvernig skal afturkalla og endurgera magnbókun á bókaða skilaafhendingu.

Eftirfarandi skref útskýra hvernig á að:

* Afturkallaðu bókaða skilasendingu á vörum eða tilföngum.
* Bókaðu aftur innkaupaskil með nýju magni.

Skrefin eru svipuð fyrir bókaðar vöruskilamóttökur.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") tákn, fara í **Bókaðar skilaafhendingar** og velja síðan viðkomandi tengil.  
2. Opnaðu skráðu skilasendinguna til að afturkalla.
3. Veldu línuna eða línurnar sem á að afturkalla.  

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
[Vinna í færslubókum](ui-work-general-journals.md)  
[Fjármál](finance.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
