---
title: Fara yfir fjárhagsreikninga
description: Hægt er að rekja framvindu þegar upphæðir í fjárhagslykli eru yfirfara.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.date: 02/28/2023
ms.custom: bap-template
ms.search.form: '22207,'
---

# <a name="review-amounts-in-general-ledger-accounts"></a>Fara yfir upphæðir í fjárhagslykli

Þú gætir átt almenna fjárhagslykla sem þú átt oft að fylgjast með. Eða ætla mætti að flýta endurskoðunarferlinu í lok mánaðarins. Til að auðvelda þér að fylgjast með því sem þú hefur gert, og til að flýta fyrir dómum, skaltu nota  **aðgerðina yfirfara færslur**  á  **bókhaldslykli**  eða  **síðu fjárhagsreikningsins**  fyrir hvern lykil. 

## <a name="set-up-accounts-for-reviews"></a>Setja upp lykla fyrir Umsagnir

 **Á kortasíðu**  fjárhagsreikningsins fyrir hvern reikning er tilgreint hvernig eigi að leyfa Umsagnir í  **reitnum endurskoðunarstefna** .

|Fara yfir reglu  |Description  |
|---------|---------|
|Engin     | Ekki er hægt að merkja færslur fyrir lykilinn sem yfirfarnar. Til dæmis er þessi valkostur notaður fyrir lykla, svo sem skuldir, útistandandi og bankareikninga þar sem aðrar leiðir eru til að endurskoða upphæðir þeirra.        |
|Leyfa yfirferð     | Ekki þarf að taka með færslur í yfirferð og upphæðir í debet-og kreditfærslum þurfa ekki að vera í jafnvægi. Þú fjarlægir umsögn, t.d. ef þú hefur gert mistök.        |
|Leyfa yfirferð og að jafna stöðu     | Heildarupphæð debet-og kreditfærslna í endurskoðunni verður að samsvara.  **Debet**  -og  **kreditreitir**  Sýna þær upphæðir og  **reiturinn Staða**  sýnir heildina. Þessi stilling lætur einnig fjarlægja umsögn. Þegar endurskoðun er fjarlægð úr einni eða fleiri færslum verða debet-og kreditfærslur samt að vera jafnaðar.        |

## <a name="mark-entries-as-reviewed"></a>Merkja færslur sem yfirfarnar

Færslurnar sem þú skoðar eru valdar og Notaðu  **svo aðgerðina sem valin er sem yfirfara**  aðgerð. Í hvert sinn sem ein eða fleiri færslur eru merkt sem yfirfarið færslurnar er sama númerið í  **dálknum yfirfara kenni** . Umsögn auðkennis er handhæg leið til að halda utan um þær færslur sem skoðaðar voru á sama tíma. [!INCLUDE [prod_short](includes/prod_short.md)] skráir einnig notandann hver sá um skoðunin og hvenær þeir gerðu það.

Ef þú merkir færslur sem skoðaðar en sérð eftir því að nota  **valið sem ekki er yfirfarið** .

* Ef endurskoðun leyfilega stefnu er úthlutuð reikningnum Endurstillir aðgerðin Endurskoðunin auðkenni á 0 og fjarlægir einstaklinginn og dagsetningu og tíma endurskoðunarinnar. 
* Ef endurskoðun heimiluð og samsvörun stöðu er úthlutuð, þarf kredit-og debet að vera enn í jafnvægi. Til dæmis, ef ein færslan í endurskoðun er mistök er hægt að velja aðra færslu með réttu gildi. Skiptifærslan þarf ekki að hafa sama yfirfarið auðkenni.

> [!TIP]
> Fljótleg leið til að velja margar færslur er að halda niðri CTRL eða Shift á meðan þú velur færslurnar. CTRL leyfir að velja sérstakar færslur og Shift velur allar færslur á milli fyrstu og síðustu færslna sem valdar eru.

## <a name="review-accounts-that-have-old-entries"></a>Fara yfir reikninga sem eru með gamlar færslur

Þú gætir verið með færslur frá fyrri tímabilum sem þú hefur þegar yfirfarið eða þarft bara ekki að skoða. Þú vilt bara byrja að skoða færslur frá t.d. byrjun árs eða bókhaldstímabili. Hægt er að skilja færslurnar eftir eins og er. Hins vegar ef ætlunin er að greina gögn í Excel eða með því að nota greiningarham skal merkja færslurnar sem endurskoðaðar. Ef fræðast á um greiningu færslna er farið í  [greina færslur](#analyze-entries). Ef merkja á færslurnar sem yfirfarnar skal bæta við síu á síurúðunni til að birta aðeins þær færslur og velja  **síðan valið Mark færslur sem yfirfara**  aðgerðina.

## <a name="filter-entries"></a>Sía færslur

Til að fá skýrari mynd eru nokkrar leiðir til að afmarka færslur á  **síðunni yfirfara**  fjárhagsfærslur.

*  **Nota sýninguna Sýna endurskoðaðar færslur**  og  **hylja endurskoðaðar færslur**  til að sýna aðeins færslurnar sem þú ert með eða hafa ekki yfirfarið. Til að hreinsa afmarkanirnar er aðgerðin Sýna allar færslur  **notaðar** .
* Nota síurúðuna. Til dæmis er hægt að sía eftir lykilnúmeri eða eldri færslur og merkja þær allar sem endurskoðaðar, af bókunardagsetningu.

## <a name="analyze-entries"></a>Greina færslur

Nokkrar leiðir eru til að greina þær fjárhagsfærslur sem þú gagnrýnir.

* Kveikja skal greiningarham, til dæmis, til að flokka færslur eftir endurskoðandi auðkenni sínu. Til að fræðast meira um greiningarham er farið í að  [greina gögn listasíðunnar sem nota greiningarham](analysis-mode.md).
* Flytja færslurnar út í Excel.

## <a name="see-also"></a>Sjá einnig

[Skilningur á fjárhag og bókhaldslyklum](finance-general-ledger.md)  
[Setja upp eða breyta bókhaldslyklum](finance-setup-chart-accounts.md)  
