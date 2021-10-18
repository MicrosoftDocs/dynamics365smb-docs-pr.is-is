---
title: Notkun Business Central með Outlook| Microsoft Docs
description: Þessi þjónusta er rækilega samþætt Microsoft 365, sem gerir þér kleift að stjórna öllum fyrirtækja- og tölvupóstsamskiptum við viðskiptamenn og lánardrottna í Outlook.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Microsoft 365
ms.date: 08/13/2021
ms.author: jswymer
ms.openlocfilehash: 5de1ae4dc96419d848103a8b4ea9e11113793242
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2021
ms.locfileid: "7589436"
---
# <a name="using-business-central-as-your-business-inbox-in-outlook"></a>Notkun Business Central sem fyrirtækjainnhólf í Outlook

[!INCLUDE[prod_short](includes/prod_short.md)] kynnir innbót sem gerir þér kleift að stjórna samskiptum innan fyrirtækisins við viðskiptamenn og lánardrottna beint í Microsoft Outlook. Með [!INCLUDE[prod_short](includes/prod_short.md)] innbótinni fyrir Outlook er hægt að skoða fjárhagsleg gögn sem tengjast viðskiptamönnum og lánardrottnum og búið til og sent fjárhagsleg skjöl, svo sem tilboð og reikninga.

[!INCLUDE[prod_short](includes/prod_short.md)] innbót samanstendur af tveimur aðskildum innbótum sem bjóða upp á eftirfarandi möguleika:

- Talnagögn tengiliða

   Þessi innbót gerir þér kleift að fletta upp á [!INCLUDE[prod_short](includes/prod_short.md)] viðskiptamanna- eða lánardrottnaupplýsingum í tölvupóstum og dagatalsfundum Outlook. Hún gerir þér einnig kleift að búa til og senda [!INCLUDE[prod_short](includes/prod_short.md)] viðskiptaskjöl, svo sem sölutilboð eða reikning til tengiliðar.

- Skjalayfirlit

   Þegar viðskiptaskjal er sent í tölvupósti veitir innbótin beinan tengil frá tölvupósti til raunverulegs viðskiptaskjals í [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="get-started"></a>Hefjast handa

1. Það fyrsta sem þarf að gera er að fá [!INCLUDE[prod_short](includes/prod_short.md)] innbótina uppsetta í Outlook. Kerfisstjórinn þinn gæti þegar hafa sett upp innbótina fyrir þig. Kannaðu því málið hjá kerfisstjóra ef þú ert ekki viss eða sjáðu næsta skref til að staðfesta hvort hún sé uppsett.

    Ef innbótin hefur ekki verið sett upp fyrir þig skaltu skoða [Setja upp innbótina til eigin nota](admin-outlook.md#install). 

2. Með innbótina uppsetta er hægt að opna **[!INCLUDE[prod_short](includes/prod_short.md)]** innbótina úr nýjum eða fyrirliggjandi tölvupóstskilaboðum eða dagatalsfundi í Outlook.

    Byrjaðu á því að skrá þig inn í Outlook og opnaðu tölvupóstskeyti. Ef þú notar Outlook-forritið skaltu því næst fara í borðann og leita að **[!INCLUDE[prod_short](includes/prod_short.md)]**.  Eða ef þú ert að nota Outlook á vefnum skaltu efst eða neðst í tölvupóstskilaboðum leita að ![Tákn fyrir innbót Business Central í Outlook.](media/outlook-business-central-icon.png) eða fara í fleiri aðgerðir ![Sýna fleiri aðgerðir fyrir tölvupóst í Outlook.](media/outlook-more-actions-button.png) hnappur.

    ![Opna innbætur Business Central í Outlook.](media/outlook-business-central-addin.png)

   Ef þú hefur sett innbótina upp á eigin spýtur og valdir að fá sýnishorn af tölvupósti skaltu finna kynningartölvupóstinn í innhólfinu. Þessi tölvupóstur inniheldur upplýsingar sem hjálpa þér að koma þér af stað.

Það gæti verið beðið um innskráningu í [!INCLUDE[prod_short](includes/prod_short.md)] innbótasvæðinu ef þetta er fyrsta skiptið sem þú notar innbótina. Ef svo er skaltu velja **Skrá inn núna** og fylgja leiðbeiningunum á skjánum til að skrá þig inn í Business Central með reikningnum þínum.

> [!TIP]
> Ef þú notar nýtt Outlook á vefnum geturðu fest **[!INCLUDE[prod_short](includes/prod_short.md)]** þannig að það sé alltaf sýnilegt í stað þess að þurfa að fara í hnappinn Fleiri aðgerðir, sem auðveldar þér að skoða innsýn tengiliða á meðan þú flettir gegnum mismunandi tölvupósta.

Frekari upplýsingar eru í [Notkun innbóta í Outlook á vefnum](https://support.office.com/article/using-add-ins-in-outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?ns=OLWAO365B&version=16)  

## <a name="work-with-contacts-and-documents-using-the-contact-insights-add-in"></a>Nýttu þér tengiliði og skjöl með því að nota innbót tengiliðainnsýnar

Segjum að þú fáir tölvupóst frá viðskiptavini sem vill fá tilboð í sumum hlutum. Beint í Outlook, getur þú opnað [!INCLUDE[prod_short](includes/prod_short.md)] viðbótina, sem viðurkennir sendanda sem viðskiptavin, og opnar viðskiptavinakortið fyrir fyrirtæki hans. Í þessu stjórnborði má sjá yfirlit yfir upplýsingar um viðskiptamann og þú getur kafað niður til að sjá nánari upplýsingar um tiltekin skjöl. Einnig má fá frekari upplýsingar um söluferil viðskiptamannsins. Ef það er nýr tengiliður getur þú búið hann til sem nýjan viðskiptamann í [!INCLUDE[prod_short](includes/prod_short.md)] án þess að yfirgefa Outlook.  

Í innbótinni er hægt að stofna sölutilboð og senda það aftur til þessa viðskiptamanns án þess að fara úr Outlook. Allar upplýsingar sem þarf að senda sölutilboðið eru tiltækar í viðskiptainnhólfinu í Outlook. Þegar búið er að færa inn gögnin er hægt að bóka tilboðið og senda í tölvupósti. [!INCLUDE[prod_short](includes/prod_short.md)] býr til PDF-skrá með sölutilboðinu og tengir það við tölvupóstskilaboðin sem notandi býr til í innbótinni.  

Á sama hátt, ef þú færð tölvupóst frá seljanda geturðu notað viðbótina til að vinna með söluaðilum og kaupa reikninga.  

Stundum viltu sjá fleiri reiti en þú sérð í viðbótinni, svo sem þegar þú vilt fylla út línur í reikningi. Til að fá aðeins meira vinnurými er hægt að setja innbótina í aðskilda síðu. Hún er enn hluti af Outlook en vinnuýmið er meira. Þegar gögn eru færð inn í skjalið í aðskilda glugganum eru breytingarnar vistaðar sjálfkrafa. Eftirfarandi hlutar leiða þig í gegnum nokkur grunnverk svo þú öðlist almennan skilning á notkun þess.

> [!TIP]
> Verkin útskýra hvernig á að nota innbótina úr tölvupósti. En það sama er hægt að gera í dagatalsfundi í Outlook.

### <a name="look-up-a-business-contact-when-composing-an-email"></a>Fletta upp á viðskiptatengilið þegar tölvupóstur er skrifaður

1. Búa til nýtt tölvupóstskeyti.
2. Í borðanum skal fara í **[!INCLUDE[prod_short](includes/prod_short.md)]** og velja **Talnagögn tengiliðar**. Eða ef þú ert að nota Outlook á vefnum skaltu neðst í tölvupóstskilaboðum velja ![Tákn fyrir innbót Business Central í Outlook.](media/outlook-business-central-icon.png) > **Talnagögn tengiliða**.
3. Í innbótasvæðinu **[!INCLUDE[prod_short](includes/prod_short.md)]** sem opnast skal skanna eftir og velja tengiliðinn sem leitað er að.

    Yfirlit yfir tengiliðinn birtist í glugganum og tengiliðnum er bætt við í línuna **Til** í tölvupóstinum.

### <a name="view-and-change-the-contact-details-or-switch-company"></a>Skoða og breyta samskiptaupplýsingum eða skipta um fyrirtæki

Aðgerðastikan efst í [!INCLUDE[prod_short](includes/prod_short.md)] innbótasvæðinu inniheldur ýmsar aðgerðir sem gera þér kleift að kafa dýpra ofan í upplýsingar um tengiliðinn og gera breytingar.

![Aðgerðastika innbótar Business Central í Outlook.](media/outlook-addin-action-bar.png)

Þú getur til dæmis opnað tengiliðaupplýsingarnar í heild sinni eins og þú myndir sjá þær í [!INCLUDE[prod_short](includes/prod_short.md)]. Ef þú vinnur með fleiri en eitt [!INCLUDE[prod_short](includes/prod_short.md)] fyrirtæki geturðu auðveldlega skipt á milli fyrirtækja.

### <a name="track-incoming-documents"></a>Fylgjast með skjölum á innleið 

Kannski notar þú listann **Skjöl á innleið** í [!INCLUDE[prod_short](includes/prod_short.md)] til að fylgjast með skjölum til úrvinnslu sem lánardrottnar senda þér, t.d. innkaupareikning sem þarf að greiða. Ef þú gerir það getur þú auðveldlega búið til færslur skjala á innleið í Outlook-innbótinni og látið tölvupóstviðhengin fylgja með.

1. Þegar þú færð tölvupóst frá lánardrottni sem er með viðhengi velur þú ![Tákn fyrir innbót Business Central í Outlook.](media/outlook-business-central-icon.png) **[!INCLUDE[prod_short](includes/prod_short.md)]**  > **Talnagögn tengiliða**. 

2. Á aðgerðastiku innbótarinnar skal velja **Sýna fleiri aðgerðir**, síðan velja **Senda í „Skjöl á innleið“**. 

### <a name="create-and-send-new-document-to-a-contact"></a>Búa til og senda nýtt skjal til tengiliðar

1. Í borðanum eða neðst í tölvupóstinum velur þú ![Tákn fyrir innbót Business Central í Outlook.](media/outlook-business-central-icon.png) **[!INCLUDE[prod_short](includes/prod_short.md)]** > **Nýtt**, veldu síðan hvers konar skjal á að búa til, t.d. **Sölutilboð**.
2. Gerðu breytingar á skjalinu í **[!INCLUDE[prod_short](includes/prod_short.md)]** innbótasvæðinu.
3. Þegar skjalið er tilbúið til að vera sent á tengilið skal á aðgerðarstikunni velja **Sýna fleiri aðgerðir**, síðan velja aðgerðina **Senda með tölvupósti**.

## <a name="view-a-document-from-an-email-using-the-document-view-add-in"></a>Skoða skjal úr tölvupósti með því að nota innbót skjalaskoðunar

Hvort sem það er tölvupóstur sem þú sendir eða fékkst, geturðu nálgast hvaða [!INCLUDE[prod_short](includes/prod_short.md)] skjal sem er, líka sölutilboð, beint úr Outlook. Þaðan er hægt að gera breytingar og fara í tengdar upplýsingar&mdash;alveg eins og þú myndir gera í [!INCLUDE[prod_short](includes/prod_short.md)].

Ef þú notar Outlook-forritið skaltu einfaldlega velja **Tengill á skjal** efst í tölvupóstinum. Fyrir Outlook á vefnum skaltu leita að tengli í tilvísun skjals í tölvupóstinum. Texti tilvísunartengilsins mun innihalda skjalanúmerið sem byggir á númeraröð sem notuð er í [!INCLUDE[prod_short](includes/prod_short.md)]. Til dæmis væri tengill fyrir sölutilboð vera eitthvað álíka og **Sölutilboð S-QUO1000**.

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/alternative-interfaces-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig

[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Sækja Business Central í fartækið mitt](install-mobile-app.md)  
[Senda skjöl í tölvupósti](ui-how-send-documents-email.md)  
[Fjármál](finance.md)  
[Sala](sales-manage-sales.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Lágmarkskröfur fyrir Outlook](product-requirements.md#outlook)  
[Notkun innbóta í Outlook á vefnum](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]