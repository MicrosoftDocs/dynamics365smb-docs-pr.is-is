---
title: Afturkalla bókun með bókun bakfærslu| Microsoft Docs
description: Ef þú hefur framkvæmt ranga bókun í færslubók, geturðu notað bakfærsluaðgerðina til að afturkalla bókunina með réttri endurskoðunarslóð.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c5e14b19b2e8be97a683dfbb9fb7a46e2c825b4e
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750806"
---
# <a name="reverse-journal-postings-and-undo-receiptsshipments"></a>Bakfæra bókun Færslubókar og afturkalla kvittanir/sendingar
Til að afturkalla ranga bókun færslubókar skal velja færsluna og búa til bakfærslu (færsla sem er alveg eins og upphaflega færslan en með andstæðu tákni í reitnum fyrir upphæð) með sama skjalanúmeri og bókunardagsetningu og upphaflega færslan. Þegar færsla hefur verið bakfærð þarf að búa til rétta færslu.

Aðeins er hægt að bakfæra færslu sem er bókuð frá færslubókarlínu. Færslu er einungis hægt að bakfæra einu sinni.

Til að afturkalla móttöku-eða sendingarbókun, áður en hún er bókuð sem reikningsfærð er hægt að nota aðgerðina **afturkalla** á bókaða skjalinu. Hægt er að afturkalla magn af gerðinni **Vara** og **Tilfang**.

Ef magn hefur verið ranglega neikvætt bókað, t.d. ef innkaupapöntun hefur verið gerð með röngum stykkjafjölda og síðan bókað sem móttekið en ekki reikningsfært, er hægt að ógilda bókunina.

Ef magn hefur verið ranglega jákvætt bókað, t.d. ef söluafhending eða innkaupaskilasending hefur verið gerð með röngum stykkjafjölda og síðan bókað sem afgreitt en ekki reikningsfært, er hægt að ógilda bókunina.   

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a>Að bakfæra færslubókarbókun fjárhagsfærslu
Hægt er að bakfæra færslur af öllum síðum **Fjárhagsfærslur**. Eftirfarandi ferli byggist á **Fjárhagsfærslur** síðunni.
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Fjárhagsfærslur** og veldu síðan tengda tengilinn.
2. Veljið færsluna sem á að bakfæra og veljið síðna aðgerðina **Bakfæra færslu**. Athugið að þetta verður að koma úr bókun færslubókar.
3. Á síðunni **Bakfærðar viðskiptafærslur** skal velja aðgerðina **Bakfæra**.
4. Velja hnappinn **Já** á staðfestingarskilaboðunum.

> [!NOTE]
> Ekki er hægt að bakfæra færslur sem hafa verið bókaðar með upplýsingum úr verki, eða sem hafa innleystan hagnað og tap innan sömu færslu.

## <a name="to-post-a-negative-entry"></a>Að bóka neikvæða færslu  
Hægt er að nota reitinn **Leiðrétting** til að bóka neikvæða debetfærslu í stað kreditfærslu, eða til að bóka neikvæða kreditfærslu í stað debetfærslu á reikningi. Til að uppfylla lagaskilyrði er þetta svæði sýnilegt að sjálfgefnu í öllum færslubókum. Reitirnir **Debetupphæð** og **Kreditupphæð** innihalda bæði upphaflegu færsluna og leiðréttu færsluna. Þessir reitir hafa engin áhrif á reikningsstöðuna.  

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Færslubækur** og veldu síðan tengda tengilinn  
2.  Í reitnum **Heiti keyrslu** skal velja viðeigandi heiti keyrslu.  
3.  Færið inn upplýsingar í viðkomandi reiti.  
4.  Í færslubókarlínu sem á að virkja fyrir neikvæðar færslur skal velja gátreitinn **Leiðrétting**.  
5.  Til að bóka færslubókina skal velja aðgerðina **Bóka** og síðan smella á hnappinn **Já**.

## <a name="to-undo-a-quantity-posting-on-a-posted-purchase-receipt"></a>Að afturkalla magnbókun í bókuðum innkaupamóttökum  
Eftirfarandi lýsir því hvernig á að hætta við bókaða kvittun á vörum eða tilföngum. Skrefin eru svipuð fyrir bókaðar sendingar.

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Bókaðar innkaupamóttökur** og veldu síðan tengda tengilinn.  
2.  Opna bókuðu móttökuna sem á að afturkalla.  
3.  Velja skal línuna eða línurnar sem þú vilt afturkalla.  
4.  Veldu **Afturkalla móttöku** aðgerðina.

Leiðréttingarlína er sett inn undir völdu móttökulínuna. Ef magnið var móttekið í vöruhúsamóttöku er leiðréttingarlínan sett inn í bókuðu vöruhúsamóttökuna.  

Reitirnir **Móttekið magn** og **Móttekið magn, óreikningsfært** svæði í tengdri innkaupapöntun eru stilltir á núll.

## <a name="to-undo-and-then-redo-a-quantity-posting-on-a-posted-return-shipment"></a>Hvernig skal afturkalla og endurgera magnbókun á bókaða skilaafhendingu.
Eftirfarandi lýsir því hvernig á að afturkalla bókaða skilasendingu á vörum eða tilföngum og endurbóka síðan innkaupaskilin með nýju magni. Skrefin eru svipuð fyrir bókaðar vöruskilamóttökur.

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Bókaðar skilaafhendingar** og veldu síðan tengda tengilinn.  
2.  Opna bókuðu skilaafhendinguna sem á að afturkalla.
3. Velja skal línuna eða línurnar sem þú vilt afturkalla.  

4.  Velja skal aðgerðina **Afturkalla vöruskilaafhendingu**.  

    Leiðréttingarlína er sett í bókaða fylgiskjalið og reitirnir **Skilamagn afhent** og **Skilaupph. afhent óreikningsf.** í innkaupabeiðninni eru settir á núll.  

    Farið nú aftur í innkaupaskilapöntunina til að endurtaka bókunina.  

5.  Á síðunni **Bókuð skilaafhending** takið mið af tölunni á svæðinu **Skilapöntun nr**. .  
6.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vöruskilapantanir innkaupa** og veldu síðan tengda tengilinn.  
7.  Opna skilapöntunina sem um ræðir og velja síðan **Enduropna** aðgerðina.  
8.  Leiðrétta færsluna í **Magn** reitnum og bóka skilapöntun innkaupa aftur.  

## <a name="see-also"></a>Sjá einnig
[Afturkalla samsetningarbókun](assembly-how-to-undo-assembly-posting.md)  
[Bóka færslu beint í Fjárhag](finance-how-post-transactions-directly.md)  
[Vinna í færslubókum](ui-work-general-journals.md)  
[Fjármál](finance.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]