---
title: "Hönnunarupplýsingar - áætlunarfæribreyta | Microsoft Docs"
description: "Þetta efni lýsir mismunandi áætlunarfæribreytum sem þú getur notað í Business Central."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: planning, design
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 72b22b1370fcd5d2a92b9ed3c6c645d279ee72f3
ms.contentlocale: is-is
ms.lasthandoff: 11/26/2018

---
# <a name="design-details-planning-parameters"></a>Hönnunarupplýsingar: áætlunarfæribreyta
Þetta efni lýsir mismunandi áætlunarfæribreytum sem þú getur notað í [!INCLUDE[d365fin](includes/d365fin_md.md)]  

Áætlunarkerfið stjórnar vöruframboði ákvarðast af ýmsum stillingum á birgðaspjaldinu eða birgðahaldseiningunni og stillingum í uppsetningu framleiðslu. Eftirfarandi tafla sýnir hvernig þessar færibreytur eru notaðar fyrir áætlanagerð.  

|Tilgangur|Mæliþáttur|  
|-------------|---------------|  
|Skilgreina ef varan á að vera áætluð|Endurpöntunarstefna = auð|  
|Skilgreina hvenær á að endurpanta|Tímarammi<br /><br /> Endurpöntunarmark<br /><br /> Öryggisforskot|  
|Skilgreina hve mikið á að endurpanta|Magn í öryggisbirgðum<br /><br /> Endurpöntunarstefna:<br /><br /> -   Fast endurpöntunarmagn plús endurpöntunarmagn.<br />-   Hámarksmagn plús Hámarksbirgðir<br />-   pöntunina þína inn.<br />-   Lota-fyrir-Lotu|  
|Fínstilling hvenær og hversu mikið aá endurpanta|Enduráætlunartímabil<br /><br /> Lotusöfnunartímabil<br /><br /> Hömlutímabil|  
|Breyta framboðspöntununum|Lágmarksmagn pöntunar<br /><br /> Hámarksmagn pöntunar<br /><br /> Fjöldapanta|  
|Afmarka áætluðu vöruna|Framleiðslustefna:<br /><br /> -   Framleiða á lager<br />-   Framleiða eftir pöntun|  

## <a name="define-if-the-item-will-be-planned"></a>Skilgreina ef varan á að vera áætluð  
Til að fela vöru/ birgðahaldseining í áætlanagerð, verður það að hafa endurpöntunarstefnu, annars verður að skipuleggja handvirkt, til dæmis, með pantanaáætlun.  

## <a name="define-when-to-reorder"></a>Skilgreina hvenær á að endurpanta  
Endurpöntunartillögur eru almennt gefin út aðeins þegar spáð tiltækt magn hefur farið niður fyrir tiltekið magn. Þetta magn er skilgreint með endurpöntunarmark. Annars er það núll. Núll má leiðrétta með því að færa inn öryggisbirgðamagn. Ef notandi hefur skilgreint öryggisafhendingartíma veldur það því að tillagan verður afhent á tímabilinu á undan gjalddaganum sem krafist er.  

Reiturinn **Tímarammi** er notaður í endurpöntunarstefnum (**Fast endurpöntunarmagn** og **Hámarksmagn**), þar sem birgðastig er athugað eftir hvern tímaramma. Fyrsti tímaramminn hefst á upphafsdegi áætlunar.  

> [!NOTE]  
>  Þegar tímarammi er reiknaður út hunsar áætlanakerfið öll vinnudagatöl sem eru skilgreind í **Grunndagatalskóði** reitnum á síðunum **Fyrirtækjaupplýsingar** og **Birgðageymslukort**.  

Sjálfgefna öryggisforskotið á síðunni **Uppsetning framleiðslu** ætti að vera stillt á að minnsta kosti einn dag. Lokadagur eftirspurnar er vitað, en ekki lokatími. Áætlunargerðin er gerð afturvirkt til að mæta mikilli eftirspurn og, ef einginn afhendingartími er skilgreindur í öryggisskyni, gætu vörurnar komið of seint og ekki mætt eftirspurn.  

Þrír viðbótar endurpöntunartímabilsreitir gegna einnig hlutverki í því að skilgreina hversu mikið þarf að endurpanta: **Enduráætlunartímabil**, **Lotusöfnunartímabil** og **Hömlutímabil**. Nánari upplýsingar er að finna „Fínstilla Hvenær og Hve mikið skal endurpanta“ hlutanum.  

## <a name="define-how-much-to-reorder"></a>Skilgreina hve mikið á að endurpanta  
Ef áætlanakerfið greinir þörfina á að endurpanta er valin endurpöntunarstefna notuð til að ákvarða hvenær og hversu mikið á að panta.  

Óháð endurpöntunarstefnu, notar áætlanakerfið yfirleitt þessum reglum:  

1. Magn pöntunartillögu er reiknað út til að mæta tilgreindu lágmarksbirgðastigi vörunnar, oftast magni öryggisbirgða. Ef ekkert er tilgreint er lágmarksbirgðastig núll.  
2. Ef áætlaðar tiltækar birgðir eru undir öryggisbirgðamagninu er afturvirkt dagsett birgðapöntun lögð til. Pöntunarmagnið mun hið minnsta fylla á öryggisbirgðir og það má auka við mjög mikla eftirspurn innan tímarammans, með endurpöntunarstefnu og með breytingum á pöntunum.  
3. Ef áætlaðar birgðir eru undir endurpöntunarmarkinu (reiknað út frá uppsöfnuðum breytingum innan tímarammans) og yfir öryggisbirgðamagninu er framvirkt áætluð frávikspöntun lögð til. Bæði brúttó eftirspurn að vera uppfyllt og endurpöntunarstefna mun ákvarða pöntunarmagn. Pöntunarmagnið þarf að lágmarki að uppfylla endurpöntunina.  
4. Ef það er meiri brúttóeftirspurn til afhendingar fyrir lokadagsetningu framvirkt áætluðu pöntunartillögunnar og þessi eftirspurn færir núverandi áætlaðar tiltækar birgðir niður fyrir öryggisbirgðamagnið er pöntunarmagnið aukið til að bæta upp fyrir hallann. Ráðlögð birgðapöntun er því næst áætluð aftur á bak frá skiladegi vergrar eftirspurnar sem hefði farið út fyrir magn öryggisbirgða.  
5. Ef ekki er fyllt út í reitinn **Tímarammi** verður eingöngu brúttóeftirspurn á sama gjalddaga bætt við.  

     Eftirfarandi endurpöntunartímabilsreitir gegna einnig hlutverki í því að skilgreina hversu mikið þarf að endurpanta: **Enduráætlunartímabil**, **Lotusöfnunartímabil** og **Hömlutímabil**. Nánari upplýsingar er að finna „Fínstilla Hvenær og Hve mikið skal endurpanta“ hlutanum.  

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

Tímasetning enduráætlunartímabils, hömlutímabils og lotusöfnunartímabils byggir á birgðadegi. Tímaramminn byggir á upphafsdagsetningu áætlanagerðar eins og sést á eftirfarandi skýringarmynd.  

![Tímarammaeiningar](media/supply_planning_5_time_bucket_elements.png "Tímarammaeiningar")  

Í eftirfarandi dæmum, svarta örvar tákna núverandi framboð (upp) og eftirspurn (niður). Rauðar, grænar og appelsínuguldar örvar eru áætlunartillögur.  

**Dæmi 1**: Breytta dagsetningin er utan enduráætlunartímabilsins sem veldur því að hætt er við núverandi framboð. Nýtt framboð er lagt til til að ná yfir eftirspurn í lotusöfnunartímabilinu.  

![Enduráætlunar- og lotusöfnunartímabil](media/supply_planning_5_recheduling_period_lot_accumulation_period.png "Enduráætlunar- og lotusöfnunartímabil")  

**Dæmi 2**: Breytta dagsetningin er á enduráætlunartímabilinu, sem veldur því að núverandi framboð er enduráætlað. Nýtt framboð er lagt til til að ná yfir eftirspurn utan lotusöfnunartímabilsins.  

![Enduráætlunartímabil, lotusöfnunartímabil og enduráætlun](media/supply_planning_5_recheduling_period_lot_accum_period_reschedule.png "Enduráætlunartímabil, lotusöfnunartímabil og enduráætlun")  

**Dæmi 3**: Eftirspurn er á hömlutímabilinu og framboðsmagnið á lotusöfnunartímabilinu stemmir við framboðsmagnið. Næsta eftirspurn er óvarin og stungið er upp á nýrri eftirspurn.  

![Hömlu- og lotusöfnunartímabil](media/supply_planning_5_dampener_period_lot_accumulation_period.png "Hömlu- og lotusöfnunartímabil")  

**Dæmi 4**: Eftirspurn er á hömlutímabilinu og framboðið er áfram á sömu dagsetningu. Hins vegar er núverandi framboðsmagn ekki nóg til að svara eftirspurn á lotusöfnunartímabilinu, svo lögð er til breytingaraðgerð á magni fyrir núverandi birgðir.  

![Hömlutímabil, lotusöfnunartímabil og magnbreyting](media/supply_planning_5_dampener_period_lot_accum_period_change_qty.png "Hömlutímabil, lotusöfnunartímabil og magnbreyting")  

**Sjálfgefin gildi:** Sjálfgefin gildi reitarins **Tímarammi** og þriggja endurpantanatímabilsreita eru auð. Fyrir alla reiti nema reitinn **Hömlutímabil** þetta merkir 0D núll dagar. Ef reiturinn **Hömlutímabil** er auður verður altæka gildið í reitnum **Sjálfgefið hömlutímabil** á síðunni **Uppsetning framleiðslu** notað.  

## <a name="modify-the-supply-orders"></a>Breyta framboðspöntununum  
Þegar magn pöntunartillögu hefur verið reiknað út er hægt að lempa hana með einum eða fleiri breytum. Til dæmis er hámarkspöntunarmagn stærra eða jafnstórt og lágmarkspöntunarmagn, sem er stærra en eða jafnt og fjöldapöntunin.  

Magnið er minnkað ef það fer fyrir hámarks pöntunarmagn. Þá er það aukið ef það er fyrir neðan lágmarkspöntunarmagni. Að lokum er talan sléttuð upp svo hún passi við tilgreinda fjöldapöntun. Allt eftirstandandi magn notar sömu leiðréttingu þar til heildareftirspurn hefur verið umbreytt í pöntunartillögur.  

## <a name="delimit-the-item"></a>Afmarka vöruna  
Valkosturinn **Framleiðslustefna** skilgreinir hvaða viðbótarpantanir lánstímaálagsútreikningar munu leggja til.  

Ef valkosturinn **Framleiða-á-lager** er notaður varða pantanirnar eingöngu vöruna sem um ræðir.  

Ef valkosturinn **Framleiða-eftir-pöntun** er notaður greinir áætlanakerfið framleiðsluuppskrift vörunnar og býr til tengdar viðbótarpöntunartillögur fyrir vörur á neðri stigum sem einnig eru skilgreindar sem framleiða-eftir-pöntun. Þetta heldur áfram eins lengi og það eru vörur til að framleiða eftir pöntun í lækkandi uppskriftarstrúktúr.  

## <a name="see-also"></a>Sjá einnig  
[Hönnunarupplýsingar: Meðhöndlun endurpöntunarstefna](design-details-handling-reordering-policies.md)   
[Hönnunarupplýsingar: Jöfnun eftirspurnar og framboðs](design-details-balancing-demand-and-supply.md)   
[Hönnunarupplýsingar: Miðlægar hugmyndir áætlanakerfis](design-details-central-concepts-of-the-planning-system.md)

