---
title: Setja upp óinnleystan virðisaukaskatt
description: Ef þú ert að nota bókhaldsreikning getur þú tilgreint hvernig á að meðhöndla óinnleyst virðisaukaskatt vegna sölu og kaupa.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'cash, VAT, unrealized, cash-based'
ms.search.form: '118, 472, 473'
ms.date: 04/01/2021
ms.author: bholtorf
---

# <a name="set-up-unrealized-vat-for-cash-based-accounting"></a><a name="set-up-unrealized-vat-for-cash-based-accounting"></a><a name="set-up-unrealized-vat-for-cash-based-accounting"></a>Uppsetning óinnleyst virðisaukaskatts fyrir reiðufé

Ef þú ert að nota reikningsskilaaðferðir í reiðufé, getur þú sett upp [!INCLUDE[prod_short](includes/prod_short.md)] til að takast á við óinnleystan virðisaukaskatt.

## <a name="to-use-general-ledger-accounts-for-unrealized-vat"></a><a name="to-use-general-ledger-accounts-for-unrealized-vat"></a><a name="to-use-general-ledger-accounts-for-unrealized-vat"></a>Nota fjárhagsreikninga fyrir óinnleystan virðisaukaskatt

Hægt er að velja að VSK-upphæðir verði reiknaðar og bókaðar á bráðabirgðafjárhagsreikning þegar reikningur er bókaður, og síðan bókaður á rétta fjárhagsreikninginn og settur í VSK-yfirlitin þegar endanlega greiðsluupphæð reikningsins er bókuð. Áður en þetta er hægt þarf að ljúka við [VSK-bókunargrunninn](finance-setup-vat.md).

Til að nota reikninga fyrir óinnleyst virðisaukaskatt skaltu fylgja þessum skrefum:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið og fara í **Uppsetning fjárhags**.
2. Á síðunni **Uppsetning fjárhags** skal velja gátreitinn Óinnleystur VSK á flýtiflipanum **Almennt**.
3. Veldu **Leita að síðu eða Tilkynna** táknið ![Ljósaperuna sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") og sláðu inn **VSK-bókunargrunnur**.
4. Á síðunni **VSK-bókunargrunnur** velurðu VSK-bókunarflokk og síðan velurðu aðgerðina **Breyta**.
5. Í reitnum **Tegund áætlaðs VSK**, veldu valkost til að tilgreina hvernig á að úthluta greiðslum til reikningsupphæð (án virðisaukaskatts) og virðisaukaskatts sjálfs og hvernig á að flytja virðisfjárhæðir úr óreynduðu virðisaukaskatti á reikninginn. Eftirfarandi tafla lýsir valkostunum.

| Valkostur | Lýsing |
| --- | --- |
| Autt | Veldu þennan valkost ef þú vilt ekki nota óinnleystur virðisaukaskatt. |
| prósentu | Greiðslur nær bæði virðisaukaskatti og reikningsupphæðinni í hlutfalli við hlutfall greiðslunnar af því sem eftir er af reikningnum. Greiddur virðisaukaskattur er fluttur frá óinnleyst VSK reikningi til áttaðs VSK reikning. |
| Fyrsta | Greiðslur ná fyrst yfir virðisaukaskatt og síðan reikningsupphæðir. Þegar svo vill til verður upphæð sem flutt er af reikningi áætlaðs VSK á VSK-reikning jöfn upphæð greiðslu uns VSK er greiddur að fullu. |
| Síðasta | Greiðslur taka fyrst til reikningsupphæðar og síðan VSK. Í þessu tilviki verður engin upphæð flutt úr óreiknuðu virðisaukaskatti til VSK reiknings þar til heildarfjárhæð reikningsins, án virðisaukaskatts, hefur verið greiddur. |
| Fyrst (fullgreitt) | Greiðslur munu ná til virðisaukaskatts fyrstu (eins og valkosturinn _Fyrst_) en engin upphæð verður flutt á VSK reikning fyrr en heildarupphæð virðisaukaskatts hefur verið greidd. |
| Síðast (fullgreitt) | Greiðslur verða fyrst og fremst gjaldfærð (eins og valkosturinn _Síðasti_) en engin upphæð verður flutt á VSK reikning fyrr en heildarupphæð virðisaukaskatts hefur verið greidd. |

6. Í **Reikn. áætlaðs útskatts**, veldu reikning fyrir óinnleyst söluskatt.

    > [!NOTE]  
    > VSK upphæðin verður bókuð á þennan reikning, og verður þar til greiðslu viðskiptavinarins er bókuð. Fjárhæðin er síðan flutt á reikninginn vegna söluverðs.
7. Í reitinn **Reikn. áætlaðs innskatts** er færður áætlaður innskattur á fjárhagsreikninginn.

> [!NOTE]  
> VSK upphæðin verður bókuð á þennan reikning, og verður þar til greiðslu viðskiptavinarins er bókuð. Fjárhæðin er síðan flutt á reikninginn fyrir innskatt.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Sjá einnig
[Uppsetning fyrir útreikning og bókunaraðferðir virðisaukaskatts](finance-setup-vat.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
