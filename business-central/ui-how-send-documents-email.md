---
title: Setja upp tölvupóst með innihald sértækt fyrir skjöl | Microsoft Docs
description: Þú getur skilgreint innihald til að setja inn í meginmál tölvupóstskeytis, til dæmis PayPal tengil. Þú getur líka sett skjöl í viðhengi tölvupóstskeyta.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.workload: na
ms.search.keywords: SMTP, mail, Microsoft 365, cover, body, PayPal, layout
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 8e22efc92cba6d9a59cc06c66422387d5b35f227
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5389625"
---
# <a name="send-documents-and-emails"></a>Senda skjöl og tölvupósta
Auðvelt er að miðla upplýsingum og skjölum, svo sem sölu- og innkaupapöntunum og reikningum, með tölvupósti beint frá [!INCLUDE[prod_short](includes/prod_short.md)]], án þess að þurfa að opna tölvupóstforrit. 

Hægt er að senda næstum allar tegundir skjala sem PDF-viðhengi. Að öðrum kosti er hægt að setja upp skýrsluútlit sem inniheldur upplýsingar úr skjalinu texta tölvupóstsins ásamt texta sem gerir tölvupóstinn vinalegri, t.d. hefðbundna kveðju. Frekari upplýsingar, sjá [Stjórna útliti skýrslna og skjala](ui-manage-report-layouts.md). <!--this topic does not mention how to set up a layout for email. Need to investigate.-->

Þegar reikningar eru sendir er hægt að auðvelda viðskiptamönnum að greiða í gegnum greiðsluþjónustu, svo sem PayPal, með því að bæta sjálfkrafa við upplýsingum og tengli við þjónustuna í tölvupóstinum. Nánari upplýsingar eru í [Virkja greiðslur viðskiptamanns í gegnum greiðsluþjónustur](sales-how-enable-payment-service-extensions.md).

Til að virkja tölvupósta innan [!INCLUDE[prod_short](includes/prod_short.md)] skal ræsa hjálparuppsetninguna **Setja upp tölvupóst**. Frekari upplýsingar eru í [Setja upp tölvupóst](admin-how-setup-email.md).

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)]] styður aðeins tölvupóstsamskipti á útleið. Ekki er hægt að taka einnig við svörum innan forritsins.

## <a name="to-send-documents-by-email"></a>Að senda fylgiskjöl með tölvupósti
Þetta ferli lýsir því hvernig hengja á bókaðan sölureikning við tölvupóst sem PDF-skjal og með texta um skjalið í tölvupóstinum. <!--update this-->

1. Veldu táknið ![Ljósapera sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera"), sláðu inn **Bókaðir sölureikningar** og veldu síðan tengda tengilinn.
2. Velja skal reikninginn og síðan velja aðgerðina **Prenta/senda**.
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
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Tölvupóstsreikningar** og veldu síðan tengda tengilinn.
2. Veljið reikninginn sem senda á tölvupóstinn frá og veljið síðan aðgerðina **Skrifa tölvupóst**.

## <a name="documents-marked-as-printed-when-they-are-sent"></a>Skjöl sem eru merkt sem prentuð þegar þau eru send
Sum skjöl í [!INCLUDE[prod_short](includes/prod_short.md)] eru með reit sem tilgreinir hversu oft skjalið hefur verið prentað. Talan í þeim reit <!--"that field?" need a name...--> er einnig uppfærð ef skjalið er sent með tölvupósti vegna þess að PDF-skjal er búið til fyrir hann. Talan er uppfærð þótt ekki sé sendur tölvupóstur. <!--guessing this is because emails are technically reports, so the counter bumps up whenever someone creates an email. Need to verify.-->

## <a name="sent-emails-and-your-email-outbox"></a>Sendir tölvupóstar og úthólf tölvupóstsins
[!INCLUDE[prod_short](includes/prod_short.md)]] geymir tölvupóstana sem þú sendir á **Sendur póstur**. Það er til að leyfa þér að endursenda tölvupóst eða áframsenda þá til einhvers annars. Ef ekki er hægt að finna tölvupóst í sendum pósti skal leita að honum á síðunni **Úthólf tölvupósts**. 

> [!NOTE]
> Það fer eftir því hvaða viðbót fyrirtækið þitt notar fyrir tölvupóst hvernig stjórnendur geta séð lista yfir skilaboð sem allir hafa sent, en ekki innihald skilaboðanna

Í **Úthólf tölvupósts** finnurðu tölvupóstana sem þú vistaðir sem drög og tölvupósta sem ekki tókst að senda, sem dæmi, ef netfangið var ógilt. Fyrir skilaboð sem ekki tókst að senda er hægt að velja **Sýna villu** eða **Rannsaka villu** til að úrræðaleita vandann.

## <a name="see-also"></a>Sjá einnig
[Stjórna útliti skýrslna og skjala](ui-manage-report-layouts.md)  
[Setja upp tölvupóst](admin-how-setup-email.md)  
[Reikningsfæra sölur](sales-how-invoice-sales.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]