---
title: Senda skjöl og tölvupósta
description: Þú getur skilgreint innihald til að setja inn í meginmál tölvupóstskeytis, til dæmis PayPal tengil. Þú getur líka sett skjöl í viðhengi tölvupóstskeyta.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.workload: na
ms.search.keywords: SMTP, mail, Microsoft 365, cover, body, PayPal, layout
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 3322199feee09c656b01c7723a8c95396015cde4
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2021
ms.locfileid: "7588452"
---
# <a name="send-documents-and-emails"></a>Senda skjöl og tölvupósta

Auðvelt er að miðla upplýsingum og skjölum, svo sem sölu- og innkaupapöntunum og reikningum, með tölvupósti beint frá [!INCLUDE[prod_short](includes/prod_short.md)], án þess að þurfa að opna tölvupóstforrit.  

Hægt er að senda næstum allar tegundir skjala sem PDF-viðhengi. Að öðrum kosti er hægt að setja upp skýrsluútlit sem inniheldur upplýsingar úr skjalinu texta tölvupóstsins ásamt texta sem gerir tölvupóstinn vinalegri, t.d. hefðbundna kveðju. Frekari upplýsingar, sjá [Stjórna útliti skýrslna og skjala](ui-manage-report-layouts.md). <!--this topic does not mention how to set up a layout for email. Need to investigate.-->

Þegar reikningar eru sendir er hægt að auðvelda viðskiptamönnum að greiða í gegnum greiðsluþjónustu, svo sem PayPal, með því að bæta sjálfkrafa við upplýsingum og tengli við þjónustuna í tölvupóstinum. Nánari upplýsingar eru í [Virkja greiðslur viðskiptamanns í gegnum greiðsluþjónustur](sales-how-enable-payment-service-extensions.md).

Til að virkja tölvupósta innan [!INCLUDE[prod_short](includes/prod_short.md)] skal ræsa hjálparuppsetninguna **Setja upp tölvupóst**. Frekari upplýsingar eru í [Setja upp tölvupóst](admin-how-setup-email.md).

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] styður aðeins tölvupóstsamskipti á útleið. Ekki er hægt að taka einnig við svörum innan forritsins.

## <a name="to-send-documents-by-email"></a>Að senda fylgiskjöl með tölvupósti

Þetta ferli lýsir því hvernig hengja á bókaðan sölureikning við tölvupóst sem PDF-skjal og með texta um skjalið í tölvupóstinum. <!--update this-->

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bókaðir sölureikningar** og velja síðan viðkomandi tengil.
2. Velja skal reikninginn og síðan velja aðgerðina **Prenta/senda** og því næst **Senda**.
3. Í reitnum **Tölvupóstur** skal velja **Já (biðja um stillingar)**. Frekari upplýsingar er að finna á [Setja upp sendisnið skjala](sales-how-setup-document-send-profiles.md).
    
    Ef reiturinn **Tölvupóstur** á síðunni **Senda skjal til** er stilltur á **Já (Biðja um Stillingar)**, mun síðan **Senda tölvupóst** opnast með tengiliðinn fyrirfram skráðan í reitnum **Til:** og skjalið hengt við sem PDF-skrá. Í reitnum **Meginmál** er annað hvort hægt að færa textann inn handvirkt eða hafa reitinn fylltur út með fyrirfram uppsettum meginmálslínum sem eru sértækar fyrir skjalið.

4. Velja hnappinn **Í lagi**.
5. Í reitnum **Til:** er fært inn gilt netfang. Sjálfgefna gildið°er netfang viðskiptamannsins.
6. Lýsandi texti er færður inn í reitinn **Efni**. Sjálfgefna gildið er nafn og reikningsnúmer viðskiptamannsins.
7. Í reitnum **Viðhengi** er myndaður reikningur sjálfgefið hengdur við sem PDF-skrá.
8. Í reitinn **Meginmál** skal slá inn stutt skilaboð til viðtakanda.

    Ef texti tölvupósts sértækur fyrir skjal er settur upp á síðunni **Skýrsluval - Sala** er reiturinn **Meginmálslínur** útfylltur sjálfkrafa. Frekari upplýsingar eru í [Setja upp endurnýtanlega texta og útlit tölvupósts fyrir sölu- og innkaupaskjöl](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents).
9. Veldu hnappinn **Í lagi** til að senda tölvupóstinn.

> [!NOTE]  
> Ef þú vilt ekki tilgreina stillingar tölvupósts í hvert sinn sem skjal er sent í tölvupósti er hægt að velja **Já (nota sjálfgefnar stillingar)** valkostinn í **Tölvupóstur** reitnum á síðunni **Senda skjal til**. Í því tilfelli mun síðan **Senda tölvupóst** ekki opnast. Sjá skref 4. Frekari upplýsingar er að finna á [Setja upp sendisnið skjala](sales-how-setup-document-send-profiles.md).  

## <a name="to-compose-and-send-an-email"></a>Að setja saman og senda tölvupóst
Hægt er að búa til tölvupósta fyrir tengiliði, viðskiptamenn, lánardrottna, sölufólk/innkaupendur og bankareikninga á fljótlegan hátt beint af síðunum fyrir þessar einingar. Veldu einfaldlega **Vinna úr** og síðan **Senda tölvupóst** til að opna ritil tölvupóstsins. Fyrir bankareikninga er aðgerðin **Senda tölvupóst** undir **Aðgerðir**.

> [!TIP]
> Ef þú sendir oft svipaða tölvupósta eða vilt senda á marga í einu, t.d. til að auglýsa markaðsherferð, getur Word-sniðmát með tölvupósti hraðað ferlinu. Þú getur búið til sniðmát fyrir aðila á borð við viðskiptamenn, lánardrottna og tengiliði sem býr til efni tölvupóstskilaboða fyrir þig og meira að segja aðlagar efnið að viðtakandanum út frá upplýsingum í [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar er að finna í [Word-sniðmát notuð fyrir mörg samskipti í einu](ui-mail-merge.md).  

## <a name="documents-marked-as-printed-when-they-are-sent"></a>Skjöl sem eru merkt sem prentuð þegar þau eru send

Sum skjöl í [!INCLUDE[prod_short](includes/prod_short.md)] eru með reit sem tilgreinir hversu oft skjalið hefur verið prentað. Talan í þeim reit <!--"that field?" need a name...--> er einnig uppfærð ef skjalið er sent með tölvupósti vegna þess að PDF-skjal er búið til fyrir hann. Talan er uppfærð þótt ekki sé sendur tölvupóstur. <!--guessing this is because emails are technically reports, so the counter bumps up whenever someone creates an email. Need to verify.-->

## <a name="sent-emails-and-your-email-outbox"></a>Sendir tölvupóstar og úthólf tölvupóstsins

[!INCLUDE[prod_short](includes/prod_short.md)] geymir tölvupóstana sem þú sendir á **Sendur póstur**. Það er til að leyfa þér að endursenda tölvupóst eða áframsenda þá til einhvers annars. Ef ekki er hægt að finna tölvupóst í sendum pósti skal leita að honum á síðunni **Úthólf tölvupósts**. 

> [!NOTE]
> Það fer eftir því hvaða viðbót fyrirtækið þitt notar fyrir tölvupóst hvernig stjórnendur geta séð lista yfir skilaboð sem allir hafa sent, en ekki innihald skilaboðanna

Í **Úthólf tölvupósts** finnurðu tölvupóstana sem þú vistaðir sem drög og tölvupósta sem ekki tókst að senda, sem dæmi, ef netfangið var ógilt. Fyrir skilaboð sem ekki tókst að senda er hægt að velja **Sýna villu** eða **Rannsaka villu** til að úrræðaleita vandann.  

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/set-up-email/)

## <a name="see-also"></a>Sjá einnig

[Stjórna útliti skýrslna og skjala](ui-manage-report-layouts.md)  
[Setja upp tölvupóst](admin-how-setup-email.md)  
[Reikningsfæra sölur](sales-how-invoice-sales.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
