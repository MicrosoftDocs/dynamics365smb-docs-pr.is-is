---
title: Hönnunarupplýsingar - áætlunarfæribreyta
description: Þetta efnisatriði lýsir mismunandi áætlunarfæribreytum sem þú getur notað og hvernig þær hafa áhrif á áætlanakerfið.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: planning, design
ms.date: 07/21/2021
ms.author: edupont
ms.openlocfilehash: d6598583ad118961fc15c7257e5207c3024e20e7
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2022
ms.locfileid: "8131978"
---
# <a name="design-details-planning-parameters"></a>Hönnunarupplýsingar: áætlunarfæribreyta
Þetta efni lýsir mismunandi áætlunarfæribreytum sem þú getur notað í [!INCLUDE[prod_short](includes/prod_short.md)]  

Áætlunarkerfið stjórnar vöruframboði ákvarðast af ýmsum stillingum á birgðaspjaldinu eða birgðahaldseiningunni og stillingum í uppsetningu framleiðslu. Eftirfarandi tafla sýnir hvernig þessar færibreytur eru notaðar fyrir áætlanagerð.  

|Tilgangur|Mæliþáttur|  
|-------------|---------------|  
|Skilgreina ef varan á að vera áætluð|Endurpöntunarstefna = auð|  
|Skilgreina hvenær á að endurpanta|Tímarammi<br /><br /> Endurpöntunarmark<br /><br /> Öryggisforskot|  
|Skilgreina hve mikið á að endurpanta|Magn í öryggisbirgðum<br /><br /> Endurpöntunarstefna:<br /><br /> -   Fast endurpöntunarmagn plús endurpöntunarmagn.<br />-   Hámarksmagn plús Hámarksbirgðir<br />-   pöntunina þína inn.<br />-   Lota-fyrir-Lotu|  
|Fínstilling hvenær og hversu mikið aá endurpanta|Enduráætlunartímabil<br /><br /> Lotusöfnunartímabil<br /><br /> Hömlutímabil|  
|Breyta framboðspöntununum|Lágmarksmagn pöntunar<br /><br /> Hámarksmagn pöntunar<br /><br /> Fjöldapanta|  
|Afmarka áætluðu vöruna|Framleiðslustefna:<br /><br /> -   Á lager<br />-   Eftir pöntun|  

## <a name="define-if-the-item-will-be-planned"></a>Skilgreina ef varan á að vera áætluð  
Til að fela vöru/ birgðahaldseining í áætlanagerð, verður það að hafa endurpöntunarstefnu, annars verður að skipuleggja handvirkt, til dæmis, með pantanaáætlun.  

## <a name="define-when-to-reorder"></a>Skilgreina hvenær á að endurpanta  
Endurpöntunartillögur eru almennt gefin út aðeins þegar spáð tiltækt magn hefur farið niður fyrir tiltekið magn. Þetta magn er skilgreint með endurpöntunarmark. Annars er það núll. Núll má leiðrétta með því að færa inn öryggisbirgðamagn. Ef notandi hefur skilgreint öryggisafhendingartíma veldur það því að tillagan verður afhent á tímabilinu á undan gjalddaganum sem krafist er.  

Reiturinn **Tímarammi** er notaður í endurpöntunarstefnum (**Fast endurpöntunarmagn** og **Hámarksmagn**), þar sem birgðastig er athugað eftir hvern tímaramma. Fyrsti tímaramminn hefst á upphafsdegi áætlunar.  

> [!NOTE]  
>  Þegar tímarammi er reiknaður út hunsar áætlanakerfið öll vinnudagatöl sem eru skilgreind í **Grunndagatalskóði** reitnum á síðunum **Fyrirtækjaupplýsingar** og **Birgðageymslukort**.  

Sjálfgefna öryggisforskotið á síðunni **Uppsetning framleiðslu** ætti að vera stillt á að minnsta kosti einn dag. Lokadagur eftirspurnar er vitað, en ekki lokatími. Áætlunargerðin er gerð afturvirkt til að mæta mikilli eftirspurn og, ef einginn afhendingartími er skilgreindur í öryggisskyni, gætu vörurnar komið of seint og ekki mætt eftirspurn.  

Þrír viðbótar endurpöntunartímabilsreitir gegna einnig hlutverki í því að skilgreina hversu mikið þarf að endurpanta: **Enduráætlunartímabil**, **Lotusöfnunartímabil** og **Hömlutímabil**. Nánari upplýsingar er að finna [Bjartsýni Hvenær og Hvernig Mikill að Endurraða](design-details-planning-parameters.md#optimize-when-and-how-much-to-reorder).  

## <a name="define-how-much-to-reorder"></a>Skilgreina hve mikið á að endurpanta  
Ef áætlanakerfið greinir þörfina á að endurpanta er valin endurpöntunarstefna notuð til að ákvarða hvenær og hversu mikið á að panta.  

Óháð endurpöntunarstefnu, notar áætlanakerfið yfirleitt þessum reglum:  

1. Magn pöntunartillögu er reiknað út til að mæta tilgreindu lágmarksbirgðastigi vörunnar, oftast magni öryggisbirgða. Ef ekkert er tilgreint er lágmarksbirgðastig núll.  
2. Ef áætlaðar tiltækar birgðir eru undir öryggisbirgðamagninu er afturvirkt dagsett birgðapöntun lögð til. Pöntunarmagnið mun hið minnsta fylla á öryggisbirgðir og það má auka við mjög mikla eftirspurn innan tímarammans, með endurpöntunarstefnu og með breytingum á pöntunum.  
3. Ef áætlaðar birgðir eru undir endurpöntunarmarkinu (reiknað út frá uppsöfnuðum breytingum innan tímarammans) og yfir öryggisbirgðamagninu er framvirkt áætluð frávikspöntun lögð til. Bæði brúttó eftirspurn að vera uppfyllt og endurpöntunarstefna mun ákvarða pöntunarmagn. Pöntunarmagnið þarf að lágmarki að uppfylla endurpöntunina.  
4. Ef það er meiri brúttóeftirspurn til afhendingar fyrir lokadagsetningu framvirkt áætluðu pöntunartillögunnar og þessi eftirspurn færir núverandi áætlaðar tiltækar birgðir niður fyrir öryggisbirgðamagnið er pöntunarmagnið aukið til að bæta upp fyrir hallann. Ráðlögð birgðapöntun er því næst áætluð aftur á bak frá skiladegi vergrar eftirspurnar sem hefði farið út fyrir magn öryggisbirgða.  
5. Ef ekki er fyllt út í reitinn **Tímarammi** verður eingöngu brúttóeftirspurn á sama gjalddaga bætt við.  

     Eftirfarandi endurpöntunartímabilsreitir gegna einnig hlutverki í því að skilgreina hversu mikið þarf að endurpanta: **Enduráætlunartímabil**, **Lotusöfnunartímabil** og **Hömlutímabil**. Nánari upplýsingar er að finna [Bjartsýni Hvenær og Hvernig Mikill að Endurraða](design-details-planning-parameters.md#optimize-when-and-how-much-to-reorder).  

### <a name="reordering-policies"></a>Endurpöntunarstefnur  
Eftirfarandi endurpöntunarstefnur stjórna því hversu mikið er endurpantað.  

|Endurpöntunarstefna|Lýsing|  
|-----------------------|---------------------------------------|  
|**Fast endurpöntunarmagn**|Pöntunarmagnið þarf minnst að vera jafnt og endurpöntunarmagnið. Það er hægt að auka til að mæta eftirspurn eða viðeigandi birgðastigi. Þessi endurpöntunarstefna er yfirleitt notað með endurpöntunarmark.|  
|**Hámarksmagn**|Pöntunarmagnið verður reiknað út þannig að það svari hámarksbirgðum. Ef magnbreytur eru notaðar er hægt að brjóta gegn hámarksbirgðum. Við mælum ekki með að þú notir tímaramma ásamt hámarks magni. Tímarammanum er vanalega hnekkt. Þessi endurpöntunarstefna er yfirleitt notað með endurpöntunarmark.|  
|**Röð**|Pöntunarmagnið verður reiknað út þannig að það svari öllu eftirspurnartilvikum og framboð-eftirspurn gögn verða áfram tengd þar til kemur að framkvæmd. Engar áætlunarfæribreytur eru teknar til greina.|  
|**Lotu-fyrir-lotu**|Magnið er reiknað út þannig að það samsvari samtölu eftirspurnarinnar sem verður gjaldfallin í tímarammanum.|  

##  <a name="optimize-when-and-how-much-to-reorder"></a>Fínstilling hvenær og hversu mikið aá endurpanta  
Til að fá skynsamlegar framboðsáætlun, skipuleggjandi mun fínstilla áætlanarfæribreytur til að takmarka enduráætlunartillögur, safnast eftirspurn (kvikt pöntunarmark magn), eða til að forðast óverulegar áætlanagerðaraðgeðrir. Eftirfarandi endurpöntunartímabilsreitir hjálpa til við að fínstilla hvenær og hversu mikið á að endurpanta.  

|Svæði|Lýsing|  
|---------------------------------|---------------------------------------|  
|**Enduráætlunartímabil**|Þessi reitur er notaður til að ákvarða hvort aðgerðaboðin ættu að enduráætla fyrirliggjandi pöntun eða hætta við hana og stofna nýja. Fyrirliggjandi pöntun verður enduráætluð innan eins enduráætlunartímabils fyrir núgildandi framboð og fram að einu enduráætlunartímabili eftir núgildandi framboð.|  
|**Lotusöfnunartímabil**|Með endurpöntunarstefnunni Runu-fyrir-runu er þessi reitur notaður til að safna saman margfeldi birgðaþarfa í eina birgðapöntun. Frá dagsetningu fyrstu eftirspurnar safnast öll eftirspurn í eftirfarandi lotusöfnunartímabili saman í eina afhendingarpöntun sem skráð er á dagsetningu fyrstu eftirspurnar. Eftirspurn sem er utan lotusöfnunartímabilsins fellur ekki undir framboðið.|  
|**Hömlutímabil**|Þessi reitur er notaður til að forðast smávægilegar enduráætlanir núverandi birgða fram í tímann. Breytingar frá birgðadegi þar til eitt hömlutímabil frá birgðadegi mun ekki mynda nein aðgerð skilaboð.<br /><br /> Hömlutímabilið tilgreinir tímabil þar sem áætlunarkerfið á ekki að stinga upp á að núverandi birgðapantanir verði færðar fram á við. Þetta takmarkar fjölda óverulegra enduráætlana á núverandi framboðs við seinni dagsetningu, ef nýja áætlaða dagsetningin er innan hömlunartímabilsins.<br /><br /> Niðurstaðan er að jákvætt delta á milli áætlaðrar nýrrar framboðsdagsetningar og upphaflegrar framboðsdagsetningar verður alltaf stærra en hömlunartímabilið.|  
> [!NOTE]
> Með endurpöntunarstefnunni lotu-fyrir-lotu verður gildið í reitnum **Lotusöfnunartímabil** að vera jafnt eða stærra en gildið í reitnum **Hömlutímabil** . Að öðrum kosti verður hömlutímabilið stytt sjálfkrafa í áætlunarrútínunni til að stemma við lotusöfnunartímabilið.  

Tímasetning enduráætlunartímabils, hömlutímabils og lotusöfnunartímabils byggir á birgðadegi. Tímaramminn byggir á upphafsdagsetningu áætlanagerðar eins og sést á eftirfarandi skýringarmynd.  

![Einingar tímaramma.](media/supply_planning_5_time_bucket_elements.png "Einingar tímaramma")  

Í eftirfarandi dæmum, svarta örvar tákna núverandi framboð (upp) og eftirspurn (niður). Rauðar, grænar og appelsínuguldar örvar eru áætlunartillögur.  

**Dæmi 1**: Breytta dagsetningin er utan enduráætlunartímabilsins sem veldur því að hætt er við núverandi framboð. Nýtt framboð er lagt til til að ná yfir eftirspurn í lotusöfnunartímabilinu.  

![Enduráætlunar- og lotusöfnunartímabil.](media/supply_planning_5_recheduling_period_lot_accumulation_period.png "Enduráætlunar- og lotusöfnunartímabil")  

**Dæmi 2**: Breytta dagsetningin er á enduráætlunartímabilinu, sem veldur því að núverandi framboð er enduráætlað. Nýtt framboð er lagt til til að ná yfir eftirspurn utan lotusöfnunartímabilsins.  

![Enduráætlunartímabil, lotusöfnunartímabil og enduráætlun.](media/supply_planning_5_recheduling_period_lot_accum_period_reschedule.png "Enduráætlunartímabil, lotusöfnunartímabil og enduráætlun")  

**Dæmi 3**: Eftirspurn er á hömlutímabilinu og framboðsmagnið á lotusöfnunartímabilinu stemmir við framboðsmagnið. Næsta eftirspurn er óvarin og stungið er upp á nýrri eftirspurn.  

![Hömlu- og lotusöfnunartímabil.](media/supply_planning_5_dampener_period_lot_accumulation_period.png "Hömlu- og lotusöfnunartímabil")  

**Dæmi 4**: Eftirspurn er á hömlutímabilinu og framboðið er áfram á sömu dagsetningu. Hins vegar er núverandi framboðsmagn ekki nóg til að svara eftirspurn á lotusöfnunartímabilinu, svo lögð er til breytingaraðgerð á magni fyrir núverandi birgðir.  

![Hömlutímabil, lotusöfnunartímabil og breyting á magni.](media/supply_planning_5_dampener_period_lot_accum_period_change_qty.png "Hömlutímabil, lotusöfnunartímabil og breyting á magni")  

**Sjálfgefin gildi:** Sjálfgefin gildi reitarins **Tímarammi** og þriggja endurpantanatímabilsreita eru auð. Fyrir alla reiti nema reitinn **Hömlutímabil** þetta merkir 0D núll dagar. Ef reiturinn **Hömlutímabil** er auður verður altæka gildið í reitnum **Sjálfgefið hömlutímabil** á síðunni **Uppsetning framleiðslu** notað.  

## <a name="modify-the-supply-orders"></a>Breyta framboðspöntununum  
Þegar magn pöntunartillögu hefur verið reiknað út er hægt að lempa hana með einum eða fleiri breytum. Til dæmis er hámarkspöntunarmagn stærra eða jafnstórt og lágmarkspöntunarmagn, sem er stærra en eða jafnt og fjöldapöntunin.  

Magnið er minnkað ef það fer fyrir hámarks pöntunarmagn. Þá er það aukið ef það er fyrir neðan lágmarkspöntunarmagni. Að lokum er talan sléttuð upp svo hún passi við tilgreinda fjöldapöntun. Allt eftirstandandi magn notar sömu leiðréttingu þar til heildareftirspurn hefur verið umbreytt í pöntunartillögur.  

## <a name="delimit-the-item"></a>Afmarka vöruna  
Valkosturinn **Framleiðslustefna** skilgreinir hvaða viðbótarpantanir lánstímaálagsútreikningar munu leggja til.  

Ef valkosturinn **Framleiða-á-lager** er notaður varða pantanirnar eingöngu vöruna sem um ræðir.  

Ef valkosturinn **Framleiða-eftir-pöntun** er notaður greinir áætlanakerfið framleiðsluuppskrift vörunnar og býr til tengdar viðbótarpöntunartillögur fyrir vörur á neðri stigum sem einnig eru skilgreindar sem framleiða-eftir-pöntun. Þetta heldur áfram eins lengi og það eru vörur til að framleiða eftir pöntun í lækkandi uppskriftarstrúktúr.

## <a name="use-low-level-codes-to-manage-derived-demand"></a>Nota lágstigskóða til að stjórna afleiddri eftirspurn

Notaðu lágstigskóða til að gera afleidda eftirspurn eftir framvindu íhluta í gegnum lægri stig uppskriftarinnar. Til að fá ítarlegri útskýringu á þessu skaltu skoða [Vöruforgangur / lágstigskóði](design-details-central-concepts-of-the-planning-system.md#item-priority--low-level-code).

Hægt er að tengja lágstigskóða hverjum hlut í vöru sem gerð er úr mörgum hlutum eða inndreginni uppskrift. Efsta samsetningarstigið telst vera stig 0 - fullunna varan. Því hærra sem númer lágstigskóða er því aftar er varan í röðinni. Endanleg vara hefur til dæmis lágstigskóðann 0, og þeir hlutar hennar sem fara í samsetningu á henni eru með lágstigskóðana 1, 2, 3 og svo framvegis. Niðurstaðan er áætlun íhluta sem eru samstilltir þörfum allra framar raðaðra stiga. Þegar áætlun er reiknuð er uppskriftin opnuð í áætlunar-vinnublaðinu og brúttóþörfum fyrir 0-stigið er raðað niður áætlunarstigin sem brúttóþarfir næsta áætlunarstigs.

Veldu reitinn **Gagnvirkur lágstigskóði** til að tilgreina hvort samstundis eigi að úthluta og reikna lágstigskóða fyrir hvern íhlut í afurðarskipulaginu. Þessi aðgerð getur haft neikvæð áhrif á afköst kerfisins ef um mikið af gögnum er að ræða, til dæmis í  sjálfvirkri kostnaðarleiðréttingu. Hafa ber í huga að þessi aðgerð er ekki afturvirk og því rétt að íhuga notkun eiginleikans fyrirfram.

Í stað þess að nota sjálfvirkan útreikning sem er gerður þegar reiturinn er valinn er hægt að nota keyrsluna **Reikna lágstigskóða** í **framleiðsluvalmyndinni** með því að smella á **vöruhönnun**, **Reikna lágstigskóða**.

> [!IMPORTANT]
> Ef reiturinn **Gagnvirkur lágstigskóði** er ekki valinn þarf að keyra keyrsluna **Reikna lágstigskóða** áður en framboðsáætlun er reiknuð (runuvinnslan **Reikna áætlun**).  

> [!NOTE]
> Jafnvel þegar reiturinn **Gagnvirkur lágstigskóði** er valinn breytast lágstigskóðar íhlutavara ekki á gagnvirkan hátt ef yfiruppskrift er eytt eða stillt sem óvottuð. Þetta getur gerst vegna vandamála við að bæta nýjum vörum við lok vörusamsetningar þar sem farið gæti verið yfir hámarksfjölda lágstigskóða. Þess vegna er best að nota runuvinnsluna **Reikna lágstigskóða** oft þegar unnið er með stórar vörusamsetningar til að halda samsetningunni.  

### <a name="optimize-low-level-code-calculation"></a>Fínstilla útreikning fyrir lágstigskóða

Veldu reitinn **Fínstilla útreikning fyrir lágstigskóða** til að tilgreina að þú viljir nota nýja hraðvirkari aðferð við útreikning á lágstigskóða. Athugaðu að nýi útreikningurinn er gerður á annan hátt og hann gæti haft neikvæð áhrif á viðbætur sem reiða sig á núverandi aðferð. Nýja útreikningsaðferðin kemur í stað núverandi aðferðar í framtíðarútgáfu.

## <a name="see-also"></a>Sjá einnig  
[Hönnunarupplýsingar: Meðhöndlun endurpöntunarstefna](design-details-handling-reordering-policies.md)   
[Hönnunarupplýsingar: Jöfnun eftirspurnar og framboðs](design-details-balancing-demand-and-supply.md)   
[Hönnunarupplýsingar: Miðlægar hugmyndir áætlanakerfisins](design-details-central-concepts-of-the-planning-system.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]