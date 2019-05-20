---
title: Sérstillingarsíður | Microsoft Docs
description: Lærðu hvernig á að sérstilla notendaviðmótið til að henta því hvernig þú vinnur í Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 16f334548d9831507970a1b74ba5fa1716611380
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1253724"
---
# <a name="personalizing-your-workspace"></a>Sérstillingar verksvæðis

Þú getur sérstillt eða *sérsniðið* vinnusvæðið þitt til að henta vinnu þinni og óskum með því að breyta síðum þannig að þær birti einungis upplýsingarnar sem þú þarfnast þegar þú þarfnast þeirra. Breytingar á sérstillingum sem þú gerir mun aðeins hafa áhrif á það sem þú sérð, ekki hvað aðrir notendur sjá.

Hægt er að gera ýmsa hluti, háð því hvernig gerð af síðu þetta er og hvað hún inniheldur, t.d. færa til og fela reiti, dálka og aðgerðir, færa til og fela heilu partana og meira.
<!--
-   Add, move, and remove fields.
-   Add, move, and remove columns in a list.
-   Change the freeze pane of columns in a list. The freeze pane locks one or more columns to the left side of a list so that are always present, even when you scroll horizontally.
-   Adjust the width of columns in a list.
-   Move and remove Cues (tiles).
-   Move and remove parts. Parts are subdivisions or areas on a page that contain things like multiple fields, another page, a chart, or tiles.

-->
> [!NOTE]
> Til viðbótar við það sem notendur geta sérsniðið, geta stjórnendur og stórnotendur hnekkt sérstillingum notenda og skilgreint hvaða aðgerðir eru aðgengilegar í öllum eða tilteknum fyrirtækjum. Frekari upplýsingar eru í [Sérstilling Business Central](ui-customizing-overview.md).

## <a name="to-personalize-a-page"></a>Til að sérsníða síðu

1. Í efra hægra horninu skaltu velja táknið ![Stillingar](media/ui-experience/settings_icon_small.png "Stillingartákn fyrir Mitt hlutverk") og velja síðan **Sérstilla**.

    Borðinn **Sérstillir** birtist efst til að tákna að hægt sé að byrja að gera breytingar.

    ![Sérstillingar](media/ui_personalize_mode_small.png "Sérstillingar")

2. Fara á síðu sem þú vilt að sérsníða.

    Ef þú sérð ![Sérstilla lás](media/personalization-lock-icon.png "Sérstilla lás") eða ![Sérstilling útilokuð](media/personalization-blocked-icon.png "Sérstilling útilokuð") í borðanum, geturðu ekki sérstillt síðuna. Frekari upplýsingar er að finna í [Af hverju get ég ekki sérsniðið síðuna](ui-personalization-locked.md).

3. Bentu á svæði sem þú vilt sérstilla, svo sem reit eða dálkfyrirsögn í lista. Allt sem hægt er að sérstilla er auðkennt umsvifalaust með örvaroddi eða ramma. Sjáðu [næsti hluti](#What) fyrir upplýsingar um hvað þú getur gert.

4. Þú getur haldið áfram að gera breytingar á sömu síðu eða opnað aðra síðu. Breytingarnar þínar eru sjálfkrafa vistaðar þegar þú gerir þær. Þegar þú hefur lokið við allt skaltu, í **Sérstilling** borðanum velja **Lokið**.

## <a name="What"></a>Hvað er hægt að sérstilla

|Hvað viltu gera|Hvernig á að gera það|Athugasemdir|
|----|------------|-------|
|Færðu eitthvað, eins og reit, dálk í lista, reit aðgerð eða hluta|Bentu hvar sem er á það sem þú vilt færa og dragðu það á nýja staðinn. Staðsetningin er auðkennd annaðhvort með þykkari láréttri eða lóðréttri línu.<br /><br />![Get ekki fært hingað tákn](media/personalization-cannot-move-here.png "Sérstillingarsnið - Get ekki fært hingað tákn") gefur til kynna að þú getir ekki fært eininguna yfir á valda staðsetningu.|Hlutar eru undirdeildir eða svæði á síðu sem innihalda hluti eins og marga reiti, aðra síðu, graf eða reiti.<br /><br />Frekari upplýsingar um sérstillingaraðgerð er að finna í [næsti hluti](ui-personalization-user.md#Actions). |
|Feldu eitthvað, eins og reit, dálk í lista, reit eða hluta.|Veldu örvaroddinn og <b>Fela</b>.|Ef reiturinn sem þú felur er einnig sýndur í haus flýtiflipa þegar flýtiflipinn er dreginn saman, mun reiturinn ekki birtast þar lengur.|
|Bæta við reit eða dálki.|Í <b>Sérstilla</b> borðanum velurðu <b>Meira</b> og svo <b>Reitur</b>.<br /></br><b>Bæta reit á síðu</b> svæðið opnast til hægri. Það birtir reitina sem hægt er að bæta við síðuna.<br /><br />Til að bæta við reit skaltu draga hann af svæðinu þangað sem þú vilt. Staðsetningin er auðkennd annaðhvort með þykkari láréttri eða lóðréttri línu.|Hver síða inniheldur fyrirfram skilgreint safn reita sem hægt er að birta. Notaðu þetta ferli til að bæta við reitum eða dálkum sem hafa ekki verið sýndir áður eða til að sýna reiti sem þú hefur falið.|
|Sýndu reit í haus flýtiflipa þegar flýtiflipinn er minnkaður.|Veldu örvaroddinn og <b>Sýna þegar dregið saman</b>. <br /> <br />Ef þú sérð ekki þennan valkost þá er hann þegar settur. Í þessu tilfelli, til að hætta að sýna reitinn í haus flýtiflipans, skal velja <b>Sýna alltaf</b>.|*Flýtiflipi* er hugtakið sem er notað um flokk af reitum sem birtast undir sameiginlegri fyrirsögn. Notaðu valkostinn <b>Sýna þegar dregið saman</b> til að birta mikilvægustu reitina. Ef þú velur reit í hausnum, mun flýtiflipinn opnast og setja áhersluna á valinn reit.<br /><br />Þessi valkostur gildir aðeins ef síða er með fleiri en einn flýtiflipa. Ef aðeins er einn flýtiflipi er ekki hægt að minnka hann, þannig að valkosturinn <b>Sýna þegar dregið saman</b> er ekki fyrir hendi.|
|Aðeins birta reit þegar þú velur **Sýna meira**.|Veldu örvaroddinn og <b>Sýna undir „Sýna meira“</b>. <br /> <br />Ef þú sérð ekki valkostinn <b>Sýna undir „Sýna meira“</b> er hann þegar settur. Í þessu tilviki, til að láta reit alltaf sjást, ekki bara þegar þú velur **Sýna meira** skaltu velja <b>Sýna alltaf</b>.||
|Breyta föstum svæði í lista í annan dálk. |Veldu örina í dálknum sem þú vilt nota sem síðasta dálk í festu svæði og veldu síðan <b>Stilla Fast svæði</b>.<br /><br/>Ef þú vilt stilla föstu svæðinu aftur á upphaflega staðsetningu skaltu velja örina fyrir fasta dálkinn og velja <b>Hreinsa Fast svæði</b>. Athugaðu: Ekki er hægt að fjarlægja þetta fasta svæði.|Fast svæði tilgreinir dálkana sem birtast alltaf til vinstri, jafnvel þótt þú skrunir lárétt.|  
|Breyta breidd á dálki.|Í töfluhausalínu skal draga hægri mörk dálks. <br /><br />Til að hámarka dálkbreiddina svo hún passi lengstu línu textans í dálknum skal tvísmella á hægri mörk hans.||
|Hoppa yfir reit þegar ýtt er á Enter.|Veldu örvaroddinn við hliðina á reitnum, eða dálkahaus í lista, og veldu **Útiloka frá flýtifærslu**. <br /><br /> Ef þú sérð ekki þennan valkost þá er reiturinn þegar stilltur þannig að honum verði sleppt. Í þessu tilfelli, til að hætta að sleppa reitnum, skal velja **Hafa með í flýtifærslu**. |Sjá [Hraða gagnaskráningu með flýtifærslu](ui-enter-data.md#QuickEntry)|

## <a name="Actions"></a>Sérstilling aðgerða

Þú getur sérsniðið aðgerðarstikuna sem er staðsett efst á síðunni, eins og gefið er í skyn af auðkennda svæðinu í eftirfarandi skýringarmynd.

![Sérsníða aðgerðarstiku](media/personalize-action-bar.png "Sérsníða aðgerðarstiku")

Sérstilling gerir þér kleift að ákveða hvaða aðgerðir eigi að sýna á aðgerðarstikunni og hvar eigi að sýna þær. Þú getur sýnt, falið eða fært stakar aðgerðir eða hóp aðgerða. Sérstilling aðgerðarstikunnar er einfaldlega gerð á sama hátt og aðrar einingar vinnusvæðisins. Það sem þú hins vegar getur gert við aðgerð eða hóp aðgerða fer eftir því hvar aðgerðin eða hópur aðgerða er staðsettur í aðgerðarstikunni. Besta leiðin til að finna út úr þessu er með því að reyna hluti og leyfa skjánum að leiðbeina þér. Í eftirfarandi köflum verða sum þessara blæbrigða við sérstillingu aðgerðarstiku útskýrð.

### <a name="action-bar-overview"></a>Yfirlit aðgerðarstiku

Það eru nokkur hugtök sem þú ættir að kynna þér til að skilja betur sérstillingaraðgerðina: *aðgerðahópur* og *uppfærður flokkur*.  

*Aðgerðahópur* er atriði sem víkkar út til að birta aðrar aðgerðir eða flokka. Til dæmis, í eftirfarandi skýringarmynd, **Bókun** er aðgerðahópur.

*Uppfærður flokkur* er aðgerðahópur sem birtist milli lóðréttu línanna tveggja `|` í aðgerðarstikunni. Flokkarnir innihalda yfirleitt algengustu aðgerðirnar sem eru notaðar, svo þú getir fundið þær fljótt. Til dæmis í eftirfarandi skýringarmynd, **Útgefið**, **Bókun**, **Reikningur** og **Fletting** eru uppfærðir flokkar.

![Sérsníða aðgerðarstikuhóp](media/personalize-action-bar-group-clip.png "Sérsníða aðgerðarstikuhóp ")

### <a name="to-remove-hide-and-show-actions-and-groups"></a>Til að fjarlægja, fela og sýna aðgerðir og flokka

Til að sýna eða fela aðgerð eða aðgerðahóp skaltu velja hann og síðan velja úr einum af eftirfarandi valkostum:

|Valkostur|Það sem hann gerir|
|------|------------
|**Fjarlægja**|Þessi valkostur birtist ef valin aðgerð er einnig sýnd einhvers staðar annars staðar í aðgerðarstikunni. Ef þessi valkostur er valinn eyðist aðgerðin úr valdri staðsetningu svo hún birtist ekki lengur. Aðgerðin eða aðgerðahópurinn verður áfram í hinni staðsetningunni. |
|**Fela**|Þessi valkostur birtist ef aðgerðin eða aðgerðahópurinn er ekki staðsettur á neinum öðrum stað í aðgerðarstikunni. Eins og **Fjarlægja**, að velja þennan valkost gerir að verkum að aðgerðin eða aðgerðahópurinn hverfur úr aðgerðarstikunni. Hins vegar í sérstillingarsniðinu, verður aðgerðin eða aðgerðahópurinn enn sýndur í núverandi staðsetningu, fyrir utan að hann er skyggður.|
|**Sýna**|Þessi valkostur birtist ef aðgerðin eða aðgerðahópurinn hefur verið falinn áður (skyggður). Að velja þennan valkost gerir að verkum að aðgerðin eða aðgerðahópurinn birtist í aðgerðarstikunni.|

### <a name="to-move-actions-and-action-groups"></a>Til að færa aðgerðir og aðgerðahópa

Til að færa aðgerð eða aðgerðahóp skaltu draga og sleppa honum á viðeigandi stað, rétt eins og með reiti og dálka.

Þar sem þú getur sleppt aðgerðum eða aðgerðahópum er gefið í skyn með láréttri línu milli aðgerðanna eða rammans utan um aðgerðahóp.

- Þú getur fært einstaka aðgerðir í uppfærða flokka, en þú getur ekki endurraðað röðuninni á aðgerðum í flokknum.
- Þú getur ekki fært aðgerðahóp í uppfærðan flokk.
- Til að færa aðgerð eða aðgerðahóp í annan aðgerðahóp sem er tómur, dragðu aðgerðina eða aðgerðahópinn í nýja hópinn og slepptu honum í boxið **Sleppa aðgerð hér**.

## <a name="additional-points-of-interest"></a>Aðrar áhugaverðar upplýsingar

Til að hjálpa þér að skilja sérstillingar eru hér nokkrar ábendingar.

- Þegar þú gerir breytingar á kortasíðu sem þú opnar af lista munu breytingarnar taka gildi á öllum færslum sem þú opnar af þeim lista. Segjum til dæmis að þú opnir tiltekinn viðskiptavin af listasíðunni Viðskiptavinir og sértillir svo síðuna með því að bæta við reit. Þegar þú opnar aðra viðskiptavini af listanum birtist einnig reiturinn sem þú bættir við.
- Breytingar sem þú gerir munu taka gildi í öllum Mitt hlutverk. Ef þú til dæmis gerir breytingu á listanum Viðskiptavinir þegar Mitt hlutverk er stillt á Viðskiptastjórnandi, munt þú einnig sjá breytinguna á Viðskiptavinalistanum þegar Mitt hlutverk er stillt á Sölupöntunarvinnsla.
- Breytingar á síðu í svæði taka gildi á síðunni þar sem þær birtast.  
- Aðeins er hægt að bæta við reitum og dálkum úr fyrirfram skilgreindum lista sem byggir á síðunni. Ekki er hægt að stofna nýja grunnstillingapakka.

## <a name="to-clear-personalization"></a>Að hreinsa sérstillingu

Á einhverjum tímapunkti gætir þig langað til að afturkalla sumar eða allar breytingar sérstillinga sem þú gerðir á síðu í gegnum tíðina. Til að gera þetta, í borðanum **Sérstilling**, skaltu velja **Meira**, **Hreinsa sérstillingar** og því næst velja einn af eftirfarandi valkostum. Hafðu í huga að ekki er hægt að afturkalla hreinsun á sérstillingum.

|Valkostur|Það sem hann gerir|
|------|------------
|Aðeins aðgerðir|Hreinsar allar breytingar sérstillinga sem þú hefur gert á aðgerðarstiku síðunnar.|
|Allar nema aðgerðir|Hreinsar allar breytingar sérstillinga sem þú hefur gert á síðunni nema þær sem voru gerðar á aðgerðarstikunni. Þetta felur í sér breytingar á reitum, dálkum og pörtum. |
|Allt|Hreinsa allar breytingar sérstillinga sem hafa verið gerðar á síðunni þannig að síðan líti út eins og hún gerði í upphafi. Þetta felur í sér breytingar á aðgerðarstiku, reitum, dálkum og hlutum.|

## <a name="see-also"></a>Sjá einnig

[Sérstillingum stjórnað](ui-personalization-manage.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Breyta grundvallarstillingum](ui-change-basic-settings.md)  
[Breyting á hvaða eiginleikar eru sýndir](ui-experiences.md)  
