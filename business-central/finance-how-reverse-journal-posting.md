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
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: f2767fca96e1f3689fc4806d878381d02622f261
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1243734"
---
# <a name="reverse-postings"></a>Bakfæra bókanir
Til að afturkalla ranga bókun færslubókar skal velja færsluna og búa til bakfærslu (færsla sem er alveg eins og upphaflega færslan en með andstæðu tákni í reitnum fyrir upphæð) með sama skjalanúmeri og bókunardagsetningu og upphaflega færslan. Þegar færsla hefur verið bakfærð þarf að búa til rétta færslu.

Aðeins er hægt að bakfæra færslu sem er bókuð frá færslubókarlínu. Færslu er einungis hægt að bakfæra einu sinni.

Frekari upplýsingar um bókun frá færslubók, sjá [Bóka færslur beint í fjárhag](finance-how-post-transactions-directly.md).

Ef magn hefur verið ranglega neikvætt bókað, t.d. ef innkaupapöntun hefur verið gerð með röngum stykkjafjölda og síðan bókað sem móttekið en ekki reikningsfært, er hægt að ógilda bókunina.

Ef magn hefur verið ranglega jákvætt bókað, t.d. ef innkaupaskilapöntun hefur verið gerð með röngum stykkjafjölda og síðan bókað sem afgreitt en ekki reikningsfært, er hægt að ógilda bókunina.   

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a>Að bakfæra færslubókarbókun fjárhagsfærslu
Hægt er að bakfæra færslur af öllum síðum **Fjárhagsfærslur**. Eftirfarandi ferli byggist á **Fjárhagsfærslur** síðunni.
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **fjárhagsfærslur** og veldu síðan tengda tengilinn.
2. Veljið færsluna sem á að bakfæra og veljið síðna aðgerðina **Bakfæra færslu**. Athugið að þetta verður að koma úr bókun færslubókar.
3. Á síðunni **Bakfærðar viðskiptafærslur** skal velja viðeigandi línu og svo aðgerðina **Bakfæra**.
4. Velja hnappinn **Já** á staðfestingarskilaboðunum.

## <a name="to-undo-a-quantity-posting-on-a-posted-purchase-receipt"></a>Að afturkalla magnbókun í bókuðum innkaupamóttökum  

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **bókaðar innkaupakvittanir** og veldu síðan tengda tengilinn.  
2.  Opna bókuðu móttökuna sem á að afturkalla.  
3.  Velja skal línuna eða línurnar sem þú vilt afturkalla.  
4.  Veldu **Afturkalla móttöku** aðgerðina.

    Leiðréttingarlína er sett inn undir völdu móttökulínuna.  

    Ef magnið móttekið í vöruhúsamóttöku er leiðréttingarlínan sett inn í bókuðu vöruhúsamóttökuna.  

    Reitirnir **Móttekið magn** og **Móttekið magn, óreikningsfært** svæði í tengdri innkaupapöntun eru stilltir á núll.

## <a name="to-undo-and-then-redo-a-quantity-posting-on-a-posted-return-shipment"></a>Hvernig skal afturkalla og endurgera magnbókun á bókaða skilaafhendingu.

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Bókaðar skilaafhendingar** og veldu síðan tengda hlekkinn.  
2.  Opna bókuðu skilaafhendinguna sem á að afturkalla.
3. Velja skal línuna eða línurnar sem þú vilt afturkalla.  

4.  Velja skal aðgerðina **Afturkalla vöruskilaafhendingu**.  

    Leiðréttingarlína er sett í bókaða fylgiskjalið og reitirnir **Skilamagn afhent** og **Skilaupph. afhent óreikningsf.** í innkaupabeiðninni eru settir á núll.  

    Farið nú aftur í innkaupaskilapöntunina til að endurtaka bókunina.  

5.  Á síðunni **Bókuð skilaafhending** takið mið af tölunni á svæðinu **Skilapöntun nr**. .  
6.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vöruskilapöntun innkaupa** og veldu síðan tengda tengilinn.  
7.  Opna skilapöntunina sem um ræðir og velja síðan **Enduropna** aðgerðina.  
8.  Leiðrétta færsluna í **Magn** reitnum og bóka skilapöntun innkaupa aftur.  

## <a name="to-post-a-negative-entry"></a>Að bóka neikvæða færslu  
Hægt er að nota reitinn **Leiðrétting** til að bóka neikvæða debetfærslu í stað kreditfærslu, eða til að bóka neikvæða kreditfærslu í stað debetfærslu á reikningi. Til að uppfylla lagaskilyrði er þetta svæði sýnilegt að sjálfgefnu í öllum færslubókum. Reitirnir **Debetupphæð** og **Kreditupphæð** innihalda bæði upphaflegu færsluna og leiðréttu færsluna. Þessir reitir hafa engin áhrif á reikningsstöðuna.  

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **færslubækur** og veldu síðan tengda tengilinn  
2.  Í reitnum **Heiti keyrslu** skal velja viðeigandi heiti keyrslu.  
3.  Færið inn upplýsingar í viðkomandi reiti.  
4.  Í færslubókarlínu sem á að virkja fyrir neikvæðar færslur skal velja gátreitinn **Leiðrétting**.  
5.  Til að bóka færslubókina skal velja aðgerðina **Bóka** og síðan smella á hnappinn **Já**.

## <a name="see-also"></a>Sjá einnig
[Bóka færslu beint í Fjárhag](finance-how-post-transactions-directly.md)  
[Vinna í færslubókum](ui-work-general-journals.md)  
[Fjármál](finance.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
