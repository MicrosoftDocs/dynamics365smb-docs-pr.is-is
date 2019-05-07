---
title: Setja upp tölvupóst með innihald sértækt fyrir skjöl | Microsoft Docs
description: Þú getur skilgreint innihald til að setja inn í meginmál tölvupóstskeytis, til dæmis PayPal tengil. Þú getur líka sett skjöl í viðhengi tölvupóstskeyta.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Office 365, cover, body, PayPal, layout
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: fcae17577b448b4271adee299874cf5cad9da79f
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/16/2019
ms.locfileid: "938204"
---
# <a name="send-documents-by-email"></a>Senda skjöl í tölvupósti
Hægt er að nota aðgerðina Uppsetning skýrslu til að miðla efni fyrir sértæk viðskiptaskjöl sem fer sjálfkrafa inn í tölvupóst til að gefa upplýsingar um innihald viðskiptaskjala hratt og vel til viðskiptafélaga þinna. Frekari upplýsingar, sjá [Stjórna útliti skýrslna og skjala](ui-manage-report-layouts.md).

Til að virkja tölvupósta innan [!INCLUDE[d365fin](includes/d365fin_md.md)], skal ræsa hjálparuppsetninguna **Setja upp tölvupóst** í Mitt hlutverk.

Hægt er að senda nær allar skjalategundir sem viðhengi í tölvupóstskilaboðum beint af síðunni sem sýnir skjalið. Auk viðhengis er hægt að setja upp tölvupóstskilaboð sem eru sértæk fyrir ákveðin skjöl með kjarnaupplýsingum úr viðkomandi skjali, þar sem stöðluð kveðja og kynning á skjalinu kemur á undan þeim upplýsingum. Til að hægt sé að bjóða viðskiptamönnum til að greiða rafrænt fyrir sölur með rafrænni greiðsluþjónustu, t.d. PayPal, er einnig hægt að láta PayPal upplýsingar og tengla í meginmáli tölvupóstsins.

Úr öllum studdum skjölum er tölvupóstur virkjaður með því að velja aðgerðina **Senda** í bókuðum skjölum, eða aðgerðina **Bóka og senda** í skjölum sem eftir á að bóka.

Ef reiturinn **Tölvupóstur** á síðunni **Senda skjal til** er stilltur á **Já (Biðja um Stillingar)**, mun síðan **Senda tölvupóst** opnast með tengiliðinn fyrirfram skráðan í reitnum **Til:** og skjalið hengt við sem PDF-skrá. Í reitnum **Meginmál** er annað hvort hægt að færa textann inn handvirkt eða hafa reitinn fylltur út með fyrirfram uppsettum meginmálslínum sem eru sértækar fyrir skjalið.

Eftirfarandi ferli sýnir hvernig á að setja skýrsluna **Sala - Reikningur** upp til að nota fyrir meginmálslínur tölvupósts sem eru sértækar fyrir skjalið þegar bókaðir sölureikningar eru sendir í tölvupósti.

## <a name="to-set-up-a-document-specific-email-body-for-sales-invoices"></a>Að setja upp meginmálslínur tölvupósts sem eru sértækar fyrir sölureikninga.
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Skýrsluval - sala** og veldu síðan tengda tengilinn.
2. Á síðunni **Skýrsluval - Sala** í reitnum **Notkun** skal velja **Reikningur**.
3. Í nýrri línu í reitnum **Skýrslukenni** skal velja t.d. staðlaða skýrslu 1306.
4. Veljið gátreitinn **Nota fyrir meginmál tölvupósts**.
5. Veljið reitinn **Útlitsauðkenni meginmáls tölvupósts** og veljið síðan útlit úr fellilistanum.

    Skýrsluútlit skilgreinir bæði stílsnið og innihald meginmáls tölvupósts, þar á meðal staðlaðan texta sem fer á undan skjalaupplýsingum í meginmáli tölvupóstsins. Þú sérð allar tiltækar skýrsluútlit ef valið er **Velja úr tæmandi listi** hnappurinn á fellilistanum.
6. Til að skoða eða breyta útlitinu sem meginmál tölvupósts er byggt á, veldu útlit á síðunni **Sérsniðið skýrsluútlit** og veldu síðan **Breyta útliti** aðgerðina.
7. Til að hægt sé að bjóða viðskiptamönnum að greiða rafrænt fyrir sölur er hægt að setja upp tengda rafræna greiðsluþjónustu, til dæmis PayPal, og láta PayPal upplýsingar og tengla í meginmál tölvupóstsins. Nánari upplýsingar eru í [Virkja greiðslur viðskiptamanns gegnum PayPal](sales-how-enable-payment-service-extensions.md).
8. Velja hnappinn **Í lagi**.

Nú þegar t.d. er valið aðgerðin **Senda** á síðunni **Bókaður sölureikningur** munu meginmálslínur tölvupósts innihalda upplýsingar fylgiskjals skýrslu 1306 og á eftir fylgir sérsniðinn staðlaður texti í samræmi við skýrsluútlitið sem valið var í 5. þrepi.

Eftirfarandi ferli sýnir hvernig eigi að senda bókaðan sölureikning sem tölvupóst með fylgiskjalið í viðhengi sem PDF-skrá og með meginmál tölvupósts sem á sérstaklega við skjalið.

## <a name="to-send-documents-by-email"></a>Að senda fylgiskjöl með tölvupósti
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Bókaðir sölureikningar** og veldu síðan tengda tengilinn.
2. Veljið viðeigandi bókaðan sölureikning og veljið síðan aðgerðina **Senda**. Síðan **Senda skjal til** opnast.
3. Í reitnum **Tölvupóstur** skal velja **Já (biðja um stillingar)**. Frekari upplýsingar er að finna á [Setja upp sendisnið skjala](sales-how-setup-document-send-profiles.md).
4. Velja hnappinn **Í lagi**. Síðan **Senda tölvupóst** opnast.
5. Í reitnum **Til:** er fært inn gilt netfang. Sjálfgefna gildið°er netfang viðskiptamannsins.
6. Lýsandi texti er færður inn í reitinn **Efni**. Sjálfgefna gildið er nafn og reikningsnúmer viðskiptamannsins.
7. Í reitnum **Viðhengi** er myndaður reikningur sjálfgefið hengdur við sem PDF-skrá. Veljið uppflettingarhnappinn til að opna skrána eða til að tengja aðra skrá.
8. Í reitinn **Meginmál** skal slá inn stutt skilaboð til viðtakanda.

    Ef meginmál tölvupósts sértækt fyrir skjal er sett upp á síðunni **Skýrsluval - Sala** er reiturinn **Meginmálslínur** útfylltur sjálfkrafa. Frekari upplýsingar er að finna í [Að setja upp meginmálslínur tölvupósts sem eru sértækar fyrir sölureikninga](ui-how-send-documents-email.md#to-set-up-a-document-specific-email-body-for-sales-invoices).
9. Veldu hnappinn **Í lagi** til að senda tölvupóstinn.

> [!NOTE]  
>   Ef þú vilt ekki tilgreina stillingar tölvupósts í hvert sinn sem skjal er sent í tölvupósti er hægt að velja **Já (nota sjálfgefnar stillingar)** valkostinn í **Tölvupóstur** reitnum á síðunni **Senda skjal til**. Í því tilfelli mun síðan **Senda tölvupóst** ekki opnast. Sjá skref 4. Frekari upplýsingar er að finna á [Setja upp sendisnið skjala](sales-how-setup-document-send-profiles.md).

## <a name="see-also"></a>Sjá einnig
[Stjórna útliti skýrslna og skjala](ui-manage-report-layouts.md)  
[Setja upp tölvupóst](admin-how-setup-email.md)  
[Reikningsfæra sölur](sales-how-invoice-sales.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
