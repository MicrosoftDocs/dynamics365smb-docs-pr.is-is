---
title: "Afturkalla bókun með bókun bakfærslu| Microsoft Docs"
description: "Ef þú hefur framkvæmt ranga bókun í færslubók, geturðu notað bakfærsluaðgerðina til að afturkalla bókunina með réttri endurskoðunarslóð."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 08/03/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 92c0bca970250b8f160ecfc15b086963c8693885
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---
# <a name="reverse-postings"></a>Bakfæra bókanir
Til að afturkalla ranga bókun færslubókar skal velja færsluna og búa til bakfærslu (færsla sem er alveg eins og upphaflega færslan en með andstæðu tákni í reitnum fyrir upphæð) með sama skjalanúmeri og bókunardagsetningu og upphaflega færslan. Þegar færsla hefur verið bakfærð þarf að búa til rétta færslu.

Aðeins er hægt að bakfæra færslu sem er bókuð frá færslubókarlínu. Færslu er einungis hægt að bakfæra einu sinni.

Frekari upplýsingar um bókun frá færslubók, sjá [Bóka færslur beint í fjárhag](finance-how-post-transactions-directly.md).

Ef magn hefur verið ranglega neikvætt bókað, t.d. ef innkaupapöntun hefur verið gerð með röngum stykkjafjölda og síðan bókað sem móttekið en ekki reikningsfært, er hægt að ógilda bókunina.

Ef magn hefur verið ranglega jákvætt bókað, t.d. ef innkaupaskilapöntun hefur verið gerð með röngum stykkjafjölda og síðan bókað sem afgreitt en ekki reikningsfært, er hægt að ógilda bókunina.   

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a>Að bakfæra færslubókarbókun fjárhagsfærslu
Hægt er að bakfæra færslur úr öllum **Fjárhagsfærslur** gluggum. Eftirfarandi ferli byggist á **Fjárhagsfærslur** glugganum.
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Fjárhagsfærslur** og velja svo viðeigandi tengil.
2. Veljið færsluna sem á að bakfæra og veljið síðna aðgerðina **Bakfæra færslu**. Athugið að þetta verður að koma úr bókun færslubókar.
3. Í glugganum **Bakfærðar viðskiptafærslur** skal velja viðeigandi línu og svo aðgerðina **Bakfæra**.
4. Velja hnappinn **Já** á staðfestingarskilaboðunum.

## <a name="to-undo-a-quantity-posting-on-a-posted-purchase-receipt"></a>Að afturkalla magnbókun í bókuðum innkaupamóttökum  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **bókað innkaupamóttaka** og velja svo viðeigandi tengil.  
2.  Opna bókuðu móttökuna sem á að afturkalla.  
3.  Velja skal línuna eða línurnar sem þú vilt afturkalla.  
4.  Veldu **Afturkalla móttöku** aðgerðina.

    Leiðréttingarlína er sett inn undir völdu móttökulínuna.  

    Ef magnið móttekið í vöruhúsamóttöku er leiðréttingarlínan sett inn í bókuðu vöruhúsamóttökuna.  

    Reitirnir **Móttekið magn** og **Móttekið magn, óreikningsfært** svæði í tengdri innkaupapöntun eru stilltir á núll.

## <a name="to-undo-and-then-redo-a-quantity-posting-on-a-posted-return-shipment"></a>Hvernig skal afturkalla og endurgera magnbókun á bókaða skilaafhendingu.

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **bókað skilaafhending** og velja svo viðeigandi tengil.  
2.  Opna bókuðu skilaafhendinguna sem á að afturkalla.
3. Velja skal línuna eða línurnar sem þú vilt afturkalla.  

4.  Velja skal aðgerðina **Afturkalla vöruskilaafhendingu**.  

    Leiðréttingarlína er sett í bókaða fylgiskjalið og reitirnir **Skilamagn afhent** og **Skilaupph. afhent óreikningsf.** í innkaupabeiðninni eru settir á núll.  

    Farið nú aftur í innkaupaskilapöntunina til að endurtaka bókunina.  

5.  Í glugganum **Bókuð skilaafhending** takið mið af tölunni á svæðinu **Skilapöntun nr**. .  
6.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Skilapöntun innkaupa** og velja svo viðeigandi tengil.  
7.  Opna skilapöntunina sem um ræðir og velja síðan **Enduropna** aðgerðina.  
8.  Leiðrétta færsluna í **Magn** reitnum og bóka skilapöntun innkaupa aftur.  

## <a name="see-also"></a>Sjá einnig
[Bóka færslu beint í Fjárhag](finance-how-post-transactions-directly.md)  
[Vinna í færslubókum](ui-work-general-journals.md)  
[Fjármál](finance.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

