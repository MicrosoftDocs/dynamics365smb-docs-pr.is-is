---
title: "Sérstilling síðna í Financials | Microsoft Docs"
description: "Lærðu hvernig á að aðlaga notendaviðmótið til að henta því hvernig þú vinnur."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 07/26/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: daf2a1349cc3e12e634324082d4e6507c5b312be
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="personalizing-your-workspace"></a>Sérstillingar verksvæðis
<!--NAV in the Web client-->
Þú getur sérstillt eða *sérsniðið* vinnusvæðið þitt til að henta vinnu þinni og óskum með því að breyta síðum þannig að þær birti einungis upplýsingarnar sem þú þarfnast þegar þú þarfnast þeirra. Breytingar á sérstillingum sem þú gerir mun aðeins hafa áhrif á það sem þú sérð, ekki hvað aðrir notendur sjá.

Eftir tegund síðunnar og hvað hún inniheldur, þú getur:

-   Bæta við, færa og fjarlægja reiti.
-   Bæta við, færa og fjarlægja dálka í lista.
-   Breyta föstum svæðum dálka í lista. Föstu svæðin læsa einum eða fleiri dálkum vinstra megin á listanum þannig að þeir eru alltaf til staðar, jafnvel þegar þú flettir lárétt.
-   Bæta við og færa og fjarlægja bunka (reiti).
-   Bæta við og fjarlægja hluta. Hlutar eru undirdeildir eða svæði á síðu sem innihalda hluti eins og marga reiti, aðra síðu, graf eða reiti.  

## <a name="to-personalize-a-page"></a>Til að sérsníða síðu

1. Í efra hægra horninu skaltu velja ![Stillingar](media/ui-experience/settings_icon_small.png "Stillingar tákn fyrir hlutverkamiðstöð") og velja síðan **Sérstilla**.

    Borðinn **Sérstillir** birtist efst til að tákna að hægt sé að byrja að gera breytingar.

    ![Sérstillingar](media/ui_personalize_mode_small.png "Sérstillingar")

2. Fara á síðu sem þú vilt að sérsníða.

   Ef þú sérð lástáknið í borðanum, sjá [Af hverju er síðan læst](ui-personalization-locked.md) til að fá frekari upplýsingar.

3. Bentu á svæði sem þú vilt sérstilla, svo sem reit eða dálkfyrirsögn í lista. Allt sem hægt er að sérstilla er auðkennt umsvifalaust með ör eða ramma.
   <!--
   -  If a component can be personalized, an arrow head (![Personalization indicator arrow left](media/ui_personalize_arrow_left.png "Personalization indicator arrow left") or ![Personalization indicator arrow down](media/ui_personalize_arrow_down.png "Personalization indicator arrow down")) appears.
   -   If the component is a part, the extent of the part is indicated by a border.
   -   The freeze pane in a list is indicated by a vertical line along the entire right-side of the last column of the freeze pane.
   -->

4. Notaðu þessa töflu til að hálpa til við að gera breytingar:     <table>
       <tr><th>Hvað viltu gera</td><th>Hvernig á að gera það</th></tr>
       <tr><td>Færðu eitthvað, eins og reit, dálk í lista, reit eða hluta</td><td> Bentu hvar sem er á það sem þú vilt færa og dragðu það á nýja staðinn. Staðsetningin er auðkennd annaðhvort með þykkari láréttri eða lóðréttri línu.</td></tr>
       <tr><td>Fjarlægja eitthvað</td><td>Veldu örina og <b>Fjarlægja</b>. </td></tr>
       <tr><td>Bæta við reit eða dálki</td><td>Í <b>Sérstilla</b> borðanum velurðu <b>Meira</b> og svo <b>Reitur</b>.<br /></br><b>Bæta reit á síðu</b> svæðið opnast til hægri. Það birtir reitina sem hægt er að bæta við síðuna. Reitir merktir sem <b>Staðsett</b> eru þegar á síðunni. Reitir merktir sem <b>Tilbúið</b> eru ekki á síðunni.<br /></br>Til að bæta við reit skaltu draga hann af svæðinu þangað sem þú vilt. Staðsetningin er auðkennd annaðhvort með þykkari láréttri eða lóðréttri línu.</td></tr>
       <tr><td>Breyta föstum svæði í lista í annan dálk</td><td>Veldu örina í dálknum sem þú vilt nota sem síðasta dálk í festu svæði og veldu síðan <b>Stilla Fast svæði</b>.<br /><br/>Ef þú vilt stilla föstu svæðinu aftur á upphaflega staðsetningu skaltu velja örina fyrir fasta dálkinn og velja <b>Hreinsa Fast svæði</b>. Athugaðu: Ekki er hægt að fjarlægja þetta fasta svæði.</td></tr>
     </table>

   > [!IMPORTANT]  
   >   Ekki er hægt að breyta lista ef listinn er sýndur sem reitur. Fyrst verður að skipta yfir í lista með því að velja ![Sýna sem lista](media/ui_show_as_list_icon.png "Sýna sem lista ör vinstri") tákn.

5. Þú getur haldið áfram að gera breytingar á sömu síðu eða fara á aðra síðu. Breytingarnar þínar eru sjálfkrafa vistaðar þegar þú gerir þær. Þegar þú hefur lokið við allt skaltu, í **Sérstilling** borðanum velja **Lokið**.

## <a name="clear-personalization-to-change-a-page-back-to-its-original-layout"></a>Hreinsa sérstillingar til að breyta síðu aftur í upphaflegt útlit
Á einhverjum tíma kanntu að vilja hreinsa allar sérstillingar sem hafa verið gerðar á síðu þannig að síðan líti út eins og hún gerði í upphafi. Til að gera þetta, í **Sérstilling** borðanu, velurðu **Meira** og svo **Hreinsa sérstillingar**.

## <a name="personalization-in-detail"></a>Yfirlit sérstillinga
Til að hjálpa þér að skilja sérstillingar eru hér nokkrar ábendingar.  
-   Þegar þú gerir breytingar á kortasíðu sem þú opnar af lista munu breytingarnar taka gildi á öllum færslum sem þú opnar af þeim lista. Segjum til dæmis að þú opnir tiltekinn viðskiptavin af listasíðunni Viðskiptavinir og sértillir svo síðuna með því að bæta við reit. Þegar þú opnar aðra viðskiptavini af listanum birtist einnig reiturinn sem þú bættir við.
-   Breytingar sem þú gerir munu taka gildi í öllum Mitt hlutverk. Ef þú til dæmis gerir breytingu á listanum Viðskiptavinir þegar Mitt hlutverk er stillt á Viðskiptastjórnandi, munt þú einnig sjá breytinguna á Viðskiptavinalistanum þegar Mitt hlutverk er stillt á Sölupöntunarvinnsla.
-   Breytingar á síðu í svæði taka gildi á síðunni þar sem þær birtast.  
-   Aðeins er hægt að bæta við reitum og dálkum úr fyrirfram skilgreindum lista sem byggir á síðunni. Ekki er hægt að stofna nýja grunnstillingapakka.

## <a name="see-also"></a>Sjá einnig
[Sérstillingum stjórnað](ui-personalization-manage.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Breyta grundvallarstillingum](ui-change-basic-settings.md)  
[Sérstillir þína [!INCLUDE[d365fin](includes/d365fin_md.md)] upplifun](ui-experiences.md)  

