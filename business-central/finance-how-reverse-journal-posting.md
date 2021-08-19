---
title: Afturkalla bókun með bókun bakfærslu
description: Ef þú hefur framkvæmt ranga bókun í færslubók, geturðu notað bakfærsluaðgerðina til að afturkalla bókunina með réttri endurskoðunarslóð.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 07/22/2021
ms.author: edupont
ms.openlocfilehash: c23dcaed561997b5c0f38b4cd5ad5631b8519706
ms.sourcegitcommit: e904da8dc45e41cdd1434111c15e2a9d9edd3fa2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/23/2021
ms.locfileid: "6660157"
---
# <a name="reverse-journal-postings-and-undo-receiptsshipments"></a>Bakfæra bókun Færslubókar og afturkalla kvittanir/sendingar
Að bakfæra bókanir færslubókar er ekki aðeins notað til að leiðrétta villur heldur er einnig hægt að nota það til að hreinsa út gamlar færslur uppsöfnunar áður en ný er færð inn sem dæmi. Þú velur færsluna og býrð til bakfærslu (færsla sem er alveg eins og upphaflega færslan en með andstæðu tákni í reitnum fyrir upphæð) með sama skjalanúmeri og bókunardagsetningu og upphaflega færslan. Þegar færsla hefur verið bakfærð þarf að búa til rétta færslu.

Aðeins er hægt að bakfæra færslu sem er bókuð frá færslubókarlínu. Færslu er einungis hægt að bakfæra einu sinni.

Til að afturkalla móttöku-eða sendingarbókun, áður en hún er bókuð sem reikningsfærð er hægt að nota aðgerðina **afturkalla** á bókaða skjalinu. Hægt er að afturkalla magn af gerðinni **Vara** og **Tilfang**.

Ef magn hefur verið ranglega neikvætt bókað, t.d. ef innkaupapöntun hefur verið gerð með röngum stykkjafjölda og síðan bókað sem móttekið en ekki reikningsfært, er hægt að ógilda bókunina.

Ef magn hefur verið ranglega jákvætt bókað, t.d. ef söluafhending eða innkaupaskilasending hefur verið gerð með röngum stykkjafjölda og síðan bókað sem afgreitt en ekki reikningsfært, er hægt að ógilda bókunina.   

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a>Að bakfæra færslubókarbókun fjárhagsfærslu
Hægt er að bakfæra færslur af öllum síðum **Fjárhagsfærslur**. Eftirfarandi ferli byggist á **Fjárhagsfærslur** síðunni.
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, farðu í **Fjárhagsfærslur** og veldu síðan tengda tengilinn.
2. Veljið færsluna sem á að bakfæra og veljið síðna aðgerðina **Bakfæra færslu**. Athugið að þetta verður að koma úr bókun færslubókar.
3. Á síðunni **Bakfærðar viðskiptafærslur** skal velja aðgerðina **Bakfæra**.
4. Velja hnappinn **Já** á staðfestingarskilaboðunum.

> [!NOTE]
> Ekki er hægt að bakfæra færslur sem hafa verið bókaðar með upplýsingum úr verki, eða sem hafa innleystan hagnað og tap innan sömu færslu.

## <a name="to-post-a-negative-entry"></a>Að bóka neikvæða færslu  
Hægt er að nota reitinn **Leiðrétting** til að bóka neikvæða debetfærslu í stað kreditfærslu, eða til að bóka neikvæða kreditfærslu í stað debetfærslu á reikningi. Til að uppfylla lagaskilyrði er þetta svæði sýnilegt að sjálfgefnu í öllum færslubókum. Reitirnir **Debetupphæð** og **Kreditupphæð** innihalda bæði upphaflegu færsluna og leiðréttu færsluna. Þessir reitir hafa engin áhrif á reikningsstöðuna.  

1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Færslubækur** og velja síðan viðkomandi tengil  
2.  Í reitnum **Heiti keyrslu** skal velja viðeigandi heiti keyrslu.  
3.  Færið inn upplýsingar í viðkomandi reiti.  
4.  Í færslubókarlínu sem á að virkja fyrir neikvæðar færslur skal velja gátreitinn **Leiðrétting**.  
5.  Til að bóka færslubókina skal velja aðgerðina **Bóka** og síðan smella á hnappinn **Já**.

## <a name="to-undo-a-quantity-posting-on-a-posted-purchase-receipt"></a>Að afturkalla magnbókun í bókuðum innkaupamóttökum  
Eftirfarandi lýsir því hvernig á að hætta við bókaða kvittun á vörum eða tilföngum. Skrefin eru svipuð fyrir bókaðar sendingar.

1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") tákn, fara í **Bókaðar innkaupamóttökur** og velja síðan viðkomandi tengil.  
2.  Opna bókuðu móttökuna sem á að afturkalla.  
3.  Velja skal línuna eða línurnar sem þú vilt afturkalla.  
4.  Veldu **Afturkalla móttöku** aðgerðina.

Leiðréttingarlína er sett inn undir völdu móttökulínuna. Ef magnið var móttekið í vöruhúsamóttöku er leiðréttingarlínan sett inn í bókuðu vöruhúsamóttökuna.  

Reitirnir **Móttekið magn** og **Móttekið magn, óreikningsfært** svæði í tengdri innkaupapöntun eru stilltir á núll.

## <a name="to-undo-and-then-redo-a-quantity-posting-on-a-posted-return-shipment"></a>Hvernig skal afturkalla og endurgera magnbókun á bókaða skilaafhendingu.
Eftirfarandi lýsir því hvernig á að afturkalla bókaða skilasendingu á vörum eða tilföngum og endurbóka síðan innkaupaskilin með nýju magni. Skrefin eru svipuð fyrir bókaðar vöruskilamóttökur.

1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") tákn, fara í **Bókaðar skilaafhendingar** og velja síðan viðkomandi tengil.  
2.  Opna bókuðu skilaafhendinguna sem á að afturkalla.
3. Velja skal línuna eða línurnar sem þú vilt afturkalla.  

4.  Velja skal aðgerðina **Afturkalla vöruskilaafhendingu**.  

    Leiðréttingarlína er sett í bókaða fylgiskjalið og reitirnir **Skilamagn afhent** og **Skilaupph. afhent óreikningsf.** í innkaupabeiðninni eru settir á núll.  

    Farið nú aftur í innkaupaskilapöntunina til að endurtaka bókunina.  

5.  Á síðunni **Bókuð skilaafhending** takið mið af tölunni á svæðinu **Skilapöntun nr**. .  
6.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Skilapantanir innkaupa** og velja síðan viðkomandi tengil.  
7.  Opna skilapöntunina sem um ræðir og velja síðan **Enduropna** aðgerðina.  
8.  Leiðrétta færsluna í **Magn** reitnum og bóka skilapöntun innkaupa aftur.  

## <a name="see-also"></a>Sjá einnig
[Afturkalla samsetningarbókun](assembly-how-to-undo-assembly-posting.md)  
[Bóka færslu beint í Fjárhag](finance-how-post-transactions-directly.md)  
[Vinna í færslubókum](ui-work-general-journals.md)  
[Fjármál](finance.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]