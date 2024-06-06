---
title: Hönnunarupplýsingar - áætlunarfæribreyta
description: Þessi grein lýsir mismunandi áætlunarfæribreytum sem hægt er að nota og hvernig þær hafa áhrif á áætlunarkerfið.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 04/26/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Hönnunarupplýsingar: áætlunarfæribreyta

Þessi grein lýsir áætlunarfæribreytunum sem hægt er að nota í [!INCLUDE[prod_short](includes/prod_short.md)].  

Hvernig áætlunarkerfið stýrir birgðaframboði ræðst af ýmsum stillingum á síðunum **Birgðaspjald,** Birgðahaldseining **og** **Uppsetning** framleiðslu. Eftirfarandi tafla útskýrir hvernig áætlanir nota þessar stillingar.  

|Tilgangur|Stillingar|
|-------------|---------------|
|Skilgreina hvort varan er áætluð|Endurpöntunarstefna = auð|
|Skilgreina hvenær á að endurpanta|Tímarammi<br /><br /> Endurpöntunarmark<br /><br /> Öryggisforskot|
|Skilgreina hve mikið á að endurpanta|Magn í öryggisbirgðum<br /><br /> Endurpöntunarstefna:<br /><br /> -   Fast endurpöntunarmagn plús endurpöntunarmagn.<br />-   Hámarksmagn plús Hámarksbirgðir<br />-   pöntunina þína inn.<br />-   Lota-fyrir-Lotu|
|Fínstilling hvenær og hversu mikið aá endurpanta|Enduráætlunartímabil<br /><br /> Lotusöfnunartímabil<br /><br /> Hömlutímabil|
|Breyta framboðspöntununum|Lágmarksmagn pöntunar<br /><br /> Hámarksmagn pöntunar<br /><br /> Fjöldapanta|
|Afmarka áætluðu vöruna|Framleiðslustefna:<br /><br /> - Til-til-lager<br />- Eftir pöntun|

## Skilgreina hvort varan er áætluð  

Ef taka á vöru eða birgðahaldseiningu með í áætlunarferlinu verður að úthluta henni endurpöntunarstefnu. Annars þarf að áætla hana handvirkt, til dæmis með aðgerðinni Pantanaáætlun.  

## Skilgreina hvenær á að endurpanta  

Endurpöntunartillögur eru almennt gefin út aðeins þegar spáð tiltækt magn hefur farið niður fyrir tiltekið magn. Endurpöntunarmarkið skilgreinir magnið. Annars er það núll. Núll má leiðrétta með því að færa inn öryggisbirgðamagn. Ef öryggisforskot er skilgreint verður tillagan afhent á tímabilinu á undan tilskildum skiladegi.  

Reiturinn **Tímarammi** er notaður í endurpöntunarmarksstefnu (**Fast endurpöntunarmagn.** og **Hámarksmagn**). Birgðastigið er athugað eftir hverja tímafyrirferð. Fyrsti tími fötunnar hefst á upphafsdagsetningu áætlunarinnar.  

> [!NOTE]  
> Þegar tímaramlar eru reiknaðir hunsar áætlunarkerfið vinnudagatöl sem skilgreind eru í reitnum **Kóti** grunndagatals á síðunum **Stofngögn** og **Birgðageymsluspjald** .  

Á síðunni **Uppsetning** framleiðslu ætti að stilla sjálfgefinn öryggisforskot á að minnsta kosti einn dag. Skiladagur eftirspurnarinnar gæti verið þekktur en ekki gjalddaginn. Áætlunin áætlar afturábak til að mæta brúttóeftirspurn. Ef öryggisforskot eru ekki skilgreind gætu vörurnar komið of seint til að uppfylla eftirspurnina.  

Reitirnir **Endurtímasetningartímabil**, **Lotusöfnunartímabil** og **Hömlunartímabil** gegna einnig hlutverki þegar endurpanta á. Nánari upplýsingar er að finna [Bjartsýni Hvenær og Hvernig Mikill að Endurraða](design-details-planning-parameters.md#optimize-when-and-how-much-to-reorder).  

## Skilgreina hve mikið á að endurpanta

Ef áætlunarkerfið finnur að þörf er á endurpöntun ákvarðar endurpöntunarstefnan hvenær og hversu mikið, í pöntun.  

Óháð endurpöntunarstefnu, notar áætlanakerfið yfirleitt þessum reglum:  

1. Reikna út magn pöntunartillögunnar til að uppfylla lágmarksbirgðastig vörunnar, yfirleitt magn í öryggisbirgðum. Ef ekkert er tilgreint er lágmarksbirgðastig núll.  
2. Ef áætlaðar tiltækar birgðir eru undir öryggisbirgðamagninu er afturvirkt dagsett birgðapöntun lögð til. Pöntunarmagnið mun hið minnsta fylla á öryggisbirgðir og það má auka við mjög mikla eftirspurn innan tímarammans, með endurpöntunarstefnu og með breytingum á pöntunum.  
3. Ef áætlaðar birgðir eru undir endurpöntunarmarkinu (reiknað út frá uppsöfnuðum breytingum innan tímarammans) og yfir öryggisbirgðamagninu er framvirkt áætluð frávikspöntun lögð til. Bæði brúttó eftirspurn að vera uppfyllt og endurpöntunarstefna mun ákvarða pöntunarmagn. Pöntunarmagnið þarf að lágmarki að uppfylla endurpöntunina.  
4. Ef meiri brúttóeftirspurn er komin á gjalddaga fyrir lokadagsetningu pöntunartillögunnar sem er tímasett framvirkt og þessi eftirspurn færir áætlaðar birgðir sem nú eru áætlaðar fyrir neðan öryggisbirgðamagnið er pöntunarmagnið aukið til að lækka lækkunina. Ráðlögð birgðapöntun er því næst áætluð aftur á bak frá skiladegi vergrar eftirspurnar sem hefði farið út fyrir magn öryggisbirgða.  
5. Ef reiturinn **Tímarauður** er ekki fylltur út er aðeins brúttóeftirspurn á sama gjalddaga bætt við.  

### Endurpöntunarstefnur  

Eftirfarandi endurpöntunarstefnur hafa áhrif á magnið sem er endurpantað. Nánari upplýsingar um endurpöntunarstefnur fást [í Hönnunarupplýsingar: Meðhöndlun endurpöntunarstefnu](design-details-handling-reordering-policies.md).  

|Endurpöntunarstefna|Heimildasamstæða|  
|-----------------------|---------------------------------------|  
|**Fast endurpöntunarmagn**|Pöntunarmagnið þarf minnst að vera jafnt og endurpöntunarmagnið. Hægt er að auka magnið til að mæta eftirspurninni eða birgðastiginu sem óskað er eftir. Þessi endurpöntunarstefna er yfirleitt notað með endurpöntunarmark.|  
|**Hámarksmagn**|Pöntunarmagnið er reiknað til að uppfylla hámarksbirgðir. Ef magnbreytur eru notaðar er hægt að brjóta gegn hámarksbirgðum. Við mælum ekki með að þú notir tímaramma ásamt hámarks magni. Tímarammanum er vanalega hnekkt. Þessi endurpöntunarstefna er yfirleitt notað með endurpöntunarmark.|  
|**Röð**|Pöntunarmagnið verður reiknað út þannig að það svari öllu eftirspurnartilvikum og framboð-eftirspurn gögn verða áfram tengd þar til kemur að framkvæmd. Engar áætlunarfæribreytur eru teknar til greina.|  
|**Lotu-fyrir-lotu**|Magnið er reiknað út þannig að það samsvari samtölu eftirspurnarinnar sem verður gjaldfallin í tímarammanum.|  

## Fínstilling hvenær og hversu mikið aá endurpanta  

Skipuleggjandi getur fínstillt áætlunarfæribreytur til að takmarka endurtímasetningartillögur, safnað saman eftirspurn (kvikt endurpöntunarmagn) eða til að forðast óverulegar áætlunaraðgerðir. Eftirfarandi reitir hjálpa til við að fínstilla hvenær og hversu mikið á að endurpanta.  

|Svæði|Heimildasamstæða|  
|---------------------------------|---------------------------------------|  
|**Enduráætlunartímabil**|Þessi reitur ákvarðar hvort aðgerðarboðin skuli endurtímasetja pöntun eða hætta við hana og stofna nýja pöntun. Fyrirliggjandi pöntun verður enduráætluð innan eins enduráætlunartímabils fyrir núgildandi framboð og fram að einu enduráætlunartímabili eftir núgildandi framboð.<br><br>**Til athugunar:** Þessi færibreyta vinnur aðeins með endurpöntunarstefnunni **Lota fyrir lotu** .|  
|**Lotusöfnunartímabil**|Með endurpöntunarstefnunni Runu-fyrir-runu er þessi reitur notaður til að safna saman margfeldi birgðaþarfa í eina birgðapöntun. Frá dagsetningu fyrstu eftirspurnar safnast öll eftirspurn í eftirfarandi lotusöfnunartímabili saman í eina afhendingarpöntun sem skráð er á dagsetningu fyrstu eftirspurnar. Eftirspurn sem er utan lotusöfnunartímabilsins fellur ekki undir framboðið.|  
|**Hömlutímabil**|Þessi reitur er notaður til að forðast smávægilegar enduráætlanir núverandi birgða fram í tímann. Breytingar frá birgðadegi þar til eitt hömlutímabil frá birgðadegi mun ekki mynda nein aðgerð skilaboð.<br /><br /> Hömlutímabilið tilgreinir tímabil þar sem áætlunarkerfið á ekki að leggja til að endurtímasetja fyrirliggjandi framboðspantanir. Þetta takmarkar fjölda óverulegra enduráætlana á núverandi framboðs við seinni dagsetningu, ef nýja áætlaða dagsetningin er innan hömlunartímabilsins.<br /><br /> Niðurstaðan er að jákvætt delta á milli áætlaðrar nýrrar framboðsdagsetningar og upphaflegrar framboðsdagsetningar verður alltaf stærra en hömlunartímabilið.|  

> [!NOTE]
> Með endurpöntunarstefnunni lotu-fyrir-lotu verður gildið í reitnum **Lotusöfnunartímabil** að vera jafnt eða stærra en gildið í reitnum **Hömlutímabil** . Annars styttist hömlutímabilið meðan á áætlunarrútínunni stendur til samræmis við lotusöfnunartímabilið.  

Tímasetning enduráætlunartímabils, hömlutímabils og lotusöfnunartímabils byggir á birgðadegi. Tímaramminn byggir á upphafsdagsetningu áætlanagerðar eins og sést á eftirfarandi skýringarmynd.  

:::image type="content" source="media/supply_planning_5_time_bucket_elements.png" alt-text="Einingar tímaramma.":::

Í eftirfarandi dæmum, svarta örvar tákna núverandi framboð (upp) og eftirspurn (niður). Rauðar, grænar og appelsínuguldar örvar eru áætlunartillögur.  

**Dæmi 1**: Breytta dagsetningin er utan enduráætlunartímabilsins sem veldur því að hætt er við núverandi framboð. Nýtt framboð er lagt til til að ná yfir eftirspurn í lotusöfnunartímabilinu.  

:::image type="content" source="media/supply_planning_5_recheduling_period_lot_accumulation_period.png" alt-text="Endurtímasetning og lotusöfnunartímabil.":::

**Dæmi 2**: Breytta dagsetningin er á enduráætlunartímabilinu, sem veldur því að núverandi framboð er enduráætlað. Nýtt framboð er lagt til til að ná yfir eftirspurn utan lotusöfnunartímabilsins.  

:::image type="content" source="media/supply_planning_5_recheduling_period_lot_accum_period_reschedule.png" alt-text="Endurtímasetningartímabil, lotusöfnunartímabil og endurtímasetning.":::

**Dæmi 3**: Eftirspurn er í hömlunartímabilinu og framboðsmagnið í lotusöfnunartímabilinu passar við framboðsmagnið. Næsta eftirspurn er óvarin og stungið er upp á nýrri eftirspurn.  

:::image type="content" source="media/supply_planning_5_dampener_period_lot_accumulation_period.png" alt-text="Hömlutímabil og lotusöfnunartímabil.":::

**Dæmi 4**: Eftirspurn er í hömlunartímabilinu og framboðið helst á sama degi. Hins vegar nær núverandi framboðsmagn ekki til eftirspurnar í lotusafnunartímabilinu. Lagt er til breytingar á magnaðgerð fyrir fyrirliggjandi framboðspöntun.  

:::image type="content" source="media/supply_planning_5_dampener_period_lot_accum_period_change_qty.png" alt-text="Hömlunartímabil, lotusöfnunartímabil og breyta magni.":::

**Sjálfgefin gildi:** Sjálfgefin gildi reitarins **Tímarammi** og þriggja endurpantanatímabilsreita eru auð. Fyrir alla reiti nema reitinn **Hömlutímabil** þetta merkir 0D núll dagar. Ef reiturinn **Hömlutímabil** er auður verður altæka gildið í reitnum **Sjálfgefið hömlutímabil** á síðunni **Uppsetning framleiðslu** notað.  

## Breyta framboðspöntununum  

Þegar magn pöntunartillögu hefur verið reiknað út er hægt að lempa hana með einum eða fleiri breytum. Til dæmis er hámarkspöntunarmagn stærra eða jafnstórt og lágmarkspöntunarmagn, sem er stærra en eða jafnt og fjöldapöntunin.  

Magnið er minnkað ef það fer fyrir hámarks pöntunarmagn. Þá er það aukið ef það er fyrir neðan lágmarkspöntunarmagni. Að lokum er talan sléttuð upp svo hún passi við tilgreinda fjöldapöntun. Allt eftirstandandi magn notar sömu leiðréttingu þar til heildareftirspurn hefur verið umbreytt í pöntunartillögur.  

## Afmarka vöruna  

Reiturinn **Framleiðslustefna** á **birgðaspjaldssíðunni** skilgreinir hvaða aðrar pantanir útreikningur MRP leggur til.  

Ef valkosturinn **Eftir lager** er notaður varðar pantanirnar aðeins vöruna.  

Ef valkosturinn **Eftir pöntun** er notaður greinir áætlunarkerfið framleiðsluuppskrift vörunnar og stofnar tengdar pöntunartillögur fyrir þær lægri stigs vörur sem einnig eru skilgreindar sem eftir pöntun. Þetta heldur áfram eins lengi og það eru vörur til að framleiða eftir pöntun í lækkandi uppskriftarstrúktúr.

## Nota lágstigskóta til að stjórna afleiddri eftirspurn

Nota lágstigskóta til að búa til afleidda eftirspurn eftir íhlutum í gegnum til lægri stiga uppskriftarinnar. Nánari upplýsingar um lágstigskóta eru í [Forgangur vöru / Lágstigskóti](design-details-central-concepts-of-the-planning-system.md#item-priority--low-level-code).

Hægt er að tengja lágstigskóta hverjum hlut í vöru sem gerð er úr mörgum hlutum eða inndreginni uppskrift. Efsta samsetningarstigið telst vera stig 0 - fullunna varan. Því hærra sem númer lágstigskóta er því aftar er varan í röðinni. Endanleg vara hefur til dæmis lágstigskótann 0, og þeir hlutar hennar sem fara í samsetningu á henni eru með lágstigskótana 1, 2, 3 og svo framvegis. Niðurstaðan er áætlun íhluta sem eru samstilltir þörfum allra framar raðaðra stiga. Þegar áætlun er reiknuð er uppskriftin opnuð í áætlunar-vinnublaðinu og brúttóþörfum fyrir 0-stigið er raðað niður áætlunarstigin sem brúttóþarfir næsta áætlunarstigs.

Á síðunni **Uppsetning** framleiðslu skal nota **vífæra kvikan lágstigskóta** til að tilgreina hvort strax eigi að úthluta og reikna lágstigskóta fyrir hvern íhlut í samsetningu framleiðslunnar. Þessi aðgerð getur haft neikvæð áhrif á afköst kerfisins ef um mikið af gögnum er að ræða, til dæmis í  sjálfvirkri kostnaðarleiðréttingu. Hafa ber í huga að þessi aðgerð er ekki afturvirk og því rétt að íhuga notkun eiginleikans fyrirfram.

Í stað þess að nota sjálfvirkan útreikning sem er gerður þegar reiturinn er valinn er hægt að nota keyrsluna **Reikna lágstigskóða** í **framleiðsluvalmyndinni** með því að smella á **vöruhönnun**, **Reikna lágstigskóða**.

> [!IMPORTANT]
> Ef ekki er kveikt á vísbendingu um **kvikan lágstigskóta** verður að keyra **keyrsluna Reikna lágstigskóta** áður en birgðaáætlun er reiknuð (**keyrslan Reikna áætlun**).  

> [!NOTE]
> Þótt kveikt sé á reitnum **Kvikur lágstigskóti** er valinn breytast lágstigskótar íhlutavara ekki kvikar ef yfiruppskrift er eytt eða stillt á óvottuð. Í þessu tilviki gæti verið erfitt að bæta nýjum vörum við lok samsetningar framleiðslunnar þar sem farið gæti verið yfir hámarksfjölda lágstigskóta. Þess vegna er hægt að keyra **keyrsluna Reikna lágstigskóta** oft til að viðhalda uppbyggingunni fyrir stórar vörusamsetningar sem ná hámarkskóta.  

## Sjá einnig .  

[Hönnunarupplýsingar: Meðhöndlun endurpöntunarstefnur](design-details-handling-reordering-policies.md)  
[Hönnunarupplýsingar: Jöfnun eftirspurn og framboð](design-details-balancing-demand-and-supply.md)  
[Hönnunarupplýsingar: Miðlægar hugmyndir áætlanakerfis](design-details-central-concepts-of-the-planning-system.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]