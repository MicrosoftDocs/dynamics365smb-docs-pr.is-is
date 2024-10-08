---
title: ESB-innkaupafærslur þriðja aðila
description: Þessi grein útskýrir hvernig á að setja upp og nota innkaup þriðja aðila í Evrópusambandinu (ESB).
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.form: '50, 51, 52, 187, 317'
ms.search.keywords: 'EU3P, EU 3-P, EU 3-Party'
ms.date: 08/12/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="eu-third-party-purchase-transactions"></a>ESB-innkaupafærslur þriðja aðila

Viðskipti þriðja aðila í Evrópusambandinu (ESB) eiga sér stað þegar tekið er á móti innkaupareikningi frá viðskiptavini í einu ESB-landi/svæði og vörurnar eru sendar til annars lands/svæðis innan Evrópusambandsins án þess að koma inn í búsetulandið. Hægt er að auðkenna færsluupphæðina og tilkynna hana sérstaklega til samræmis við virðisaukaskattsskýrslu sumra ESB-landa/svæða og kröfur UM VSK-upplýsingaskiptakerfi (VIES). Microsoft Dynamics 365 Business Central gerir kleift að setja innkaupafærslur upp sem viðskipti þriðja aðila í ESB. Bókaðar ESB-viðskipti þriðja aðila má afmarka í VSK-yfirlitum og án upphæðar í dálknum **Sala til viðskiptamanns** í skýrslunni **VSK-VIES - Skýrsla** .

Jafnvel þótt eiginleikinn sé foruppsettur sem viðauki er hann ekki sjálfgefið virkjaður. Fylgið þessum skrefum til að virkja eiginleikann.

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, fara á **vinnusvæðið Eiginleikastjórnun** og velja síðan viðeigandi tengja.
2. Í listanum skal finna og velja **Eiginleikauppfærslu: Skipta út fyrirliggjandi ESB-þríhyrningsinnkaupavirkni með nýju viðaukanum Innkaup ESB þríhyrnings**.
3. Í dálknum **Virkt fyrir** dálkinn skal velja **Allir notendur**.

> [!NOTE]
> Ef þýska eða ítalska staðfæringin er notuð verður ekki hægt að virkja forritið vegna þess að það er ekki samhæft ákveðnum VSK-aðgerðum í þessum staðfæringum.  

## <a name="enable-eu-third-party-trade-functionality-for-a-purchase"></a>Gera viðskiptaaðgerðir ESB þriðja aðila virkar fyrir innkaup

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **VSK-grunn** og velja síðan tengda tengja.
2. Á síðunni **VSK-uppsetning** er merkt í reitinn **Gera ESB þríhyrn.innkaup** virkan.

## <a name="use-eu-third-party-trade-functionality"></a>Nota viðskiptaaðgerðir ESB þriðja aðila

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **Innkaupareikninga** (eða annað innkaupaskjal) og velja síðan viðeigandi tengja.
2. Velja skal fyrirliggjandi innkaupareikning eða velja **Nýr** til að stofna nýjan.
3. Á flýtiflipanum **Sundurl. reikningur** skal velja gátreitinn **ESB-þríhyrn.viðsk** ..
4. Valið er **Í lagi**.

## <a name="include-or-exclude-eu-third-party-trade-records-on-the-vat-statement"></a>Taka með eða undanskilja ESB-viðskiptafærslur þriðja aðila á VSK-yfirlitinu

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **VSK-yfirlit** og velja síðan tengda tengja.
2. Á síðunni **VSK-yfirlit** er valinn einn af eftirfarandi kostum til að sýna viðskiptafærslur ESB-þriðja aðila með því að nota **reitinn ESB-þríhyrningsviðskiptaafmörkun** .

    | Valkostur | Heimildasamstæða |
    |--------|-------------|
    | Allt | Sýna allar færslur óháð því hvort **merkt var við reitinn ESB-þríhyrn.viðsk.skjöl** . |
    | ESB3 | Sýna aðeins færslur þar sem reiturinn **ESB-þríhyrn.viðsk.skjöl** var merktur. |
    | Ekki-ES3 | Sýna aðeins færslur þar sem reiturinn **ESB-þríhyrn.viðsk** . í fylgiskjölum var ekki merktur. |

## <a name="see-also"></a>Sjá einnig .
[Fjármálastjórnun](finance.md)    
[Vinna með Business Central](ui-work-product.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
