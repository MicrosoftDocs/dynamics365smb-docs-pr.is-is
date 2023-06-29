---
title: Hönnunarupplýsingar - áætlunarfæribreyta
description: Þessi grein lýsir mismunandi áætlunarfæribreytum sem hægt er að nota og hvernig þær hafa áhrif á áætlanakerfið.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 04/26/2023
ms.custom: bap-template
---
# <a name="design-details-planning-parameters"></a><a name="design-details-planning-parameters"></a>Hönnunarupplýsingar: áætlunarfæribreyta

Þessi grein lýsir áætlunarfæribreytum sem hægt er að nota í [!INCLUDE[prod_short](includes/prod_short.md)].  

Hvernig áætlanakerfið stýrir vöruframboði ræðst af mismunandi stillingum **á síðunum Birgðaspjald,** **SKUog** **Uppsetning** framleiðslu. Eftirfarandi tafla útskýrir hvernig áætlanagerð notar þessar stillingar.  

|Tilgangur|Stillingar|
|-------------|---------------|
|Skilgreina hvort varan sé áætluð|Endurpöntunarstefna = auð|
|Skilgreina hvenær á að endurpanta|Tímarammi<br /><br /> Endurpöntunarmark<br /><br /> Öryggisforskot|
|Skilgreina hve mikið á að endurpanta|Magn í öryggisbirgðum<br /><br /> Endurpöntunarstefna:<br /><br /> -   Fast endurpöntunarmagn plús endurpöntunarmagn.<br />-   Hámarksmagn plús Hámarksbirgðir<br />-   pöntunina þína inn.<br />-   Lota-fyrir-Lotu|
|Fínstilling hvenær og hversu mikið aá endurpanta|Enduráætlunartímabil<br /><br /> Lotusöfnunartímabil<br /><br /> Hömlutímabil|
|Breyta framboðspöntununum|Lágmarksmagn pöntunar<br /><br /> Hámarksmagn pöntunar<br /><br /> Fjöldapanta|
|Afmarka áætluðu vöruna|Framleiðslustefna:<br /><br /> - Gera á lager<br />- Gera eftir pöntun|

## <a name="define-whether-the-item-is-planned"></a><a name="define-whether-the-item-is-planned"></a>Skilgreina hvort varan sé áætluð

Til að hafa vöru eða birgðahaldseiningu með í áætlunarferlinu þarf að úthluta henni endurpöntunarstefnu. Annars verður að áætla handvirkt, til dæmis með því að nota eiginleikann Pöntunaráætlun.  

## <a name="define-when-to-reorder"></a><a name="define-when-to-reorder"></a>Skilgreina hvenær á að endurpanta

Endurpöntunartillögur eru almennt gefin út aðeins þegar spáð tiltækt magn hefur farið niður fyrir tiltekið magn. Endurpöntunarmarkið skilgreinir magnið. Annars er það núll. Núll má leiðrétta með því að færa inn öryggisbirgðamagn. Ef þú skilgreinir afhendingartíma í öryggisskyni verður tillagan afhent á tímabilinu fyrir tilskilinn gjalddaga.  

Reiturinn **Tímarammi** er notaður af reglum um endurpöntunarmark (**Fast endurpöntunarmagn.**  og **Hámarks magn).** Birgðastaðan er athuguð eftir hverja tímaramma. Fyrsta tímaramminn hefst á upphafsdegi áætlunar.  

> [!NOTE]  
> Þegar tímarammi er reiknaður hunsar áætlanakerfið vinnudagatöl sem eru skilgreind í reitnum Grunndagatalskóði **á** síðunum **Fyrirtækjaupplýsingar** og **birgðageymsluspjald.**   

 **Á síðunni Uppsetning** framleiðslu ætti að stilla sjálfgefinn afhendingartíma öryggis á að minnsta kosti einn dag. Gjalddagi eftirspurnarinnar gæti verið þekktur, en ekki gjalddagi. Áætlunaráætlanir aftur á bak til að mæta brúttó eftirspurn. Ef þú skilgreinir ekki afhendingartíma öryggis gætu vörurnar komið of seint til að mæta eftirspurninni.  

Reitirnir **Enduráætlunartímabil,** lotusöfnunartímabil og **dempunartímabil** **·**  gegna einnig hlutverki við að skilgreina hvenær á að endurpanta. Nánari upplýsingar er að finna [Bjartsýni Hvenær og Hvernig Mikill að Endurraða](design-details-planning-parameters.md#optimize-when-and-how-much-to-reorder).  

## <a name="define-how-much-to-reorder"></a><a name="define-how-much-to-reorder"></a>Skilgreina hve mikið á að endurpanta

Ef áætlanakerfið greinir þörfina á að endurpanta ákvarðar endurpöntunarstefnan hvenær og hversu mikið á að panta.  

Óháð endurpöntunarstefnu, notar áætlanakerfið yfirleitt þessum reglum:  

1. Reiknið magn pöntunartillögunnar til að uppfylla lágmarksbirgðastig vörunnar, yfirleitt öryggisbirgðamagnið. Ef ekkert er tilgreint er lágmarksbirgðastig núll.  
2. Ef áætlaðar tiltækar birgðir eru undir öryggisbirgðamagninu er afturvirkt dagsett birgðapöntun lögð til. Pöntunarmagnið mun hið minnsta fylla á öryggisbirgðir og það má auka við mjög mikla eftirspurn innan tímarammans, með endurpöntunarstefnu og með breytingum á pöntunum.  
3. Ef áætlaðar birgðir eru undir endurpöntunarmarkinu (reiknað út frá uppsöfnuðum breytingum innan tímarammans) og yfir öryggisbirgðamagninu er framvirkt áætluð frávikspöntun lögð til. Bæði brúttó eftirspurn að vera uppfyllt og endurpöntunarstefna mun ákvarða pöntunarmagn. Pöntunarmagnið þarf að lágmarki að uppfylla endurpöntunina.  
4. Ef það er meiri brúttóeftirspurn á gjalddaga fyrir lokadagsetningu framvirkrar áætlaðrar pöntunartillögu og þessi eftirspurn færir núverandi áætlaðar tiltækar birgðir undir öryggisbirgðamagnið, er pöntunarmagnið aukið til að bæta upp hallann. Ráðlögð birgðapöntun er því næst áætluð aftur á bak frá skiladegi vergrar eftirspurnar sem hefði farið út fyrir magn öryggisbirgða.  
5. Ef reiturinn **Tímarammi** er ekki fylltur út er aðeins brúttóeftirspurn á sama gjalddaga bætt við.  

### <a name="reordering-policies"></a><a name="reordering-policies"></a>Endurpöntunarstefnur

Eftirfarandi endurpöntunarstefnur hafa áhrif á magnið sem er endurpantað. Frekari upplýsingar um endurpöntunarstefnur er að finna í [Hönnunarupplýsingar: Meðhöndlun endurpöntunarstefna](design-details-handling-reordering-policies.md).  

|Endurpöntunarstefna|Heimildasamstæða|  
|-----------------------|---------------------------------------|  
|**Fast endurpöntunarmagn**|Pöntunarmagnið þarf minnst að vera jafnt og endurpöntunarmagnið. Hægt er að auka magnið til að mæta eftirspurn eða æskilegu birgðastigi. Þessi endurpöntunarstefna er yfirleitt notað með endurpöntunarmark.|  
|**Hámarksmagn**|Pöntunarmagnið er reiknað til að uppfylla hámarksbirgðir. Ef magnbreytur eru notaðar er hægt að brjóta gegn hámarksbirgðum. Við mælum ekki með að þú notir tímaramma ásamt hámarks magni. Tímarammanum er vanalega hnekkt. Þessi endurpöntunarstefna er yfirleitt notað með endurpöntunarmark.|  
|**Röð**|Pöntunarmagnið verður reiknað út þannig að það svari öllu eftirspurnartilvikum og framboð-eftirspurn gögn verða áfram tengd þar til kemur að framkvæmd. Engar áætlunarfæribreytur eru teknar til greina.|  
|**Lotu-fyrir-lotu**|Magnið er reiknað út þannig að það samsvari samtölu eftirspurnarinnar sem verður gjaldfallin í tímarammanum.|  

## <a name="optimize-when-and-how-much-to-reorder"></a><a name="optimize-when-and-how-much-to-reorder"></a>Fínstilling hvenær og hversu mikið aá endurpanta

Skipuleggjandi getur fínstillt áætlunarfæribreytur til að takmarka enduráætlunartillögur, safna eftirspurn (kvikt endurpöntunarmagn) eða til að forðast óverulegar áætlunaraðgerðir. Eftirfarandi reitir hjálpa til við að fínstilla hvenær og hversu mikið á að endurpanta.  

|Svæði|Heimildasamstæða|  
|---------------------------------|---------------------------------------|  
|**Enduráætlunartímabil**|Þessi reitur ákvarðar hvort aðgerðaboðin eigi að enduráætla fyrirliggjandi pöntun eða hætta við hana og stofna nýja pöntun. Fyrirliggjandi pöntun verður enduráætluð innan eins enduráætlunartímabils fyrir núgildandi framboð og fram að einu enduráætlunartímabili eftir núgildandi framboð.<br><br>**Athugaðu:** Þessi færibreyta virkar aðeins með endurpöntunarstefnu **lota fyrir lotu** .|  
|**Lotusöfnunartímabil**|Með endurpöntunarstefnunni Runu-fyrir-runu er þessi reitur notaður til að safna saman margfeldi birgðaþarfa í eina birgðapöntun. Frá dagsetningu fyrstu eftirspurnar safnast öll eftirspurn í eftirfarandi lotusöfnunartímabili saman í eina afhendingarpöntun sem skráð er á dagsetningu fyrstu eftirspurnar. Eftirspurn sem er utan lotusöfnunartímabilsins fellur ekki undir framboðið.|  
|**Hömlutímabil**|Þessi reitur er notaður til að forðast smávægilegar enduráætlanir núverandi birgða fram í tímann. Breytingar frá birgðadegi þar til eitt hömlutímabil frá birgðadegi mun ekki mynda nein aðgerð skilaboð.<br /><br /> Hömlutímabil tilgreinir tímabil þar sem ekki á að áætlanakerfið leggi til að fyrirliggjandi birgðapantanir verði enduráætlaðar. Þetta takmarkar fjölda óverulegra enduráætlana á núverandi framboðs við seinni dagsetningu, ef nýja áætlaða dagsetningin er innan hömlunartímabilsins.<br /><br /> Niðurstaðan er að jákvætt delta á milli áætlaðrar nýrrar framboðsdagsetningar og upphaflegrar framboðsdagsetningar verður alltaf stærra en hömlunartímabilið.|  

> [!NOTE]
> Með endurpöntunarstefnunni lotu-fyrir-lotu verður gildið í reitnum **Lotusöfnunartímabil** að vera jafnt eða stærra en gildið í reitnum **Hömlutímabil** . Að öðrum kosti er demparatímabilið stytt meðan á skipulagningu stendur til að passa við lotusöfnunartímabilið.  

Tímasetning enduráætlunartímabils, hömlutímabils og lotusöfnunartímabils byggir á birgðadegi. Tímaramminn byggir á upphafsdagsetningu áætlanagerðar eins og sést á eftirfarandi skýringarmynd.  

:::image type="content" source="media/supply_planning_5_time_bucket_elements.png" alt-text="Tímarammaeiningar.":::

Í eftirfarandi dæmum, svarta örvar tákna núverandi framboð (upp) og eftirspurn (niður). Rauðar, grænar og appelsínuguldar örvar eru áætlunartillögur.  

**Dæmi 1**: Breytta dagsetningin er utan enduráætlunartímabilsins sem veldur því að hætt er við núverandi framboð. Nýtt framboð er lagt til til að ná yfir eftirspurn í lotusöfnunartímabilinu.  

:::image type="content" source="media/supply_planning_5_recheduling_period_lot_accumulation_period.png" alt-text="Enduráætlunar- og lotusöfnunartímabil.":::

**Dæmi 2**: Breytta dagsetningin er á enduráætlunartímabilinu, sem veldur því að núverandi framboð er enduráætlað. Nýtt framboð er lagt til til að ná yfir eftirspurn utan lotusöfnunartímabilsins.  

:::image type="content" source="media/supply_planning_5_recheduling_period_lot_accum_period_reschedule.png" alt-text="Enduráætlunartímabil, lotusöfnunartímabil og enduráætlun.":::

**Dæmi 3**: Það er eftirspurn á hömlutímabilinu og framboðsmagnið á uppsöfnunartímabili lotunnar passar við framboðsmagnið. Næsta eftirspurn er óvarin og stungið er upp á nýrri eftirspurn.  

:::image type="content" source="media/supply_planning_5_dampener_period_lot_accumulation_period.png" alt-text="Dampener tímabil og lotusöfnunartímabil.":::

**Dæmi 4**: Það er eftirspurn á demparatímabilinu og framboðið helst á sama degi. Hins vegar nær núverandi framboðsmagn ekki yfir eftirspurn á uppsöfnunartímabili lotunnar. Tillaga er gerð um breytingu á magni fyrirliggjandi birgðapöntunar.  

:::image type="content" source="media/supply_planning_5_dampener_period_lot_accum_period_change_qty.png" alt-text="Deyfitímabil, lotusöfnunartímabil og breyting á magni.":::

**Sjálfgefin gildi:** Sjálfgefin gildi reitarins **Tímarammi** og þriggja endurpantanatímabilsreita eru auð. Fyrir alla reiti nema reitinn **Hömlutímabil** þetta merkir 0D núll dagar. Ef reiturinn **Hömlutímabil** er auður verður altæka gildið í reitnum **Sjálfgefið hömlutímabil** á síðunni **Uppsetning framleiðslu** notað.  

## <a name="modify-the-supply-orders"></a><a name="modify-the-supply-orders"></a>Breyta framboðspöntununum

Þegar magn pöntunartillögu hefur verið reiknað út er hægt að lempa hana með einum eða fleiri breytum. Til dæmis er hámarkspöntunarmagn stærra eða jafnstórt og lágmarkspöntunarmagn, sem er stærra en eða jafnt og fjöldapöntunin.  

Magnið er minnkað ef það fer fyrir hámarks pöntunarmagn. Þá er það aukið ef það er fyrir neðan lágmarkspöntunarmagni. Að lokum er talan sléttuð upp svo hún passi við tilgreinda fjöldapöntun. Allt eftirstandandi magn notar sömu leiðréttingu þar til heildareftirspurn hefur verið umbreytt í pöntunartillögur.  

## <a name="delimit-the-item"></a><a name="delimit-the-item"></a>Afmarka hlutinn

Reiturinn Framleiðslustefna **á** síðunni Vöruspjald **skilgreinir hvaða aðrar pantanir MRP útreikningurinn** leggur til.  

Ef valkosturinn **Búa til birgðir** er notaður eiga pantanirnar aðeins við um vöruna.  

Ef valkosturinn **Gera pöntun er notaður greinir áætlanakerfið framleiðsluuppskrift vörunnar og stofnar tengdar pöntunartillögur fyrir þær vörur á neðri stigum sem eru einnig skilgreindar sem gera-eftir-pöntun** . Þetta heldur áfram eins lengi og það eru vörur til að framleiða eftir pöntun í lækkandi uppskriftarstrúktúr.

## <a name="use-low-level-codes-to-manage-derived-demand"></a><a name="use-low-level-codes-to-manage-derived-demand"></a>Nota kóða á lágu stigi til að stjórna afleiddri eftirspurn

Nota lágstigs kóða til að afleidd eftirspurn eftir íhlutum þróist yfir á neðri stig uppskriftarinnar. Til að læra meira um lágstigs kóða, farðu í [Item Priority / Low-Level Code](design-details-central-concepts-of-the-planning-system.md#item-priority--low-level-code).

Hægt er að tengja lágstigskóta hverjum hlut í vöru sem gerð er úr mörgum hlutum eða inndreginni uppskrift. Efsta samsetningarstigið telst vera stig 0 - fullunna varan. Því hærra sem númer lágstigskóta er því aftar er varan í röðinni. Endanleg vara hefur til dæmis lágstigskótann 0, og þeir hlutar hennar sem fara í samsetningu á henni eru með lágstigskótana 1, 2, 3 og svo framvegis. Niðurstaðan er áætlun íhluta sem eru samstilltir þörfum allra framar raðaðra stiga. Þegar áætlun er reiknuð er uppskriftin opnuð í áætlunar-vinnublaðinu og brúttóþörfum fyrir 0-stigið er raðað niður áætlunarstigin sem brúttóþarfir næsta áætlunarstigs.

 **Á síðunni Uppsetning** framleiðslu skal nota víxlhnappinn **Kvikur lágstigs kóði** til að tilgreina hvort eigi að úthluta og reikna út kóða á lágu stigi strax fyrir hvern þátt í uppbyggingu afurðarinnar. Þessi aðgerð getur haft neikvæð áhrif á afköst kerfisins ef um mikið af gögnum er að ræða, til dæmis í  sjálfvirkri kostnaðarleiðréttingu. Hafa ber í huga að þessi aðgerð er ekki afturvirk og því rétt að íhuga notkun eiginleikans fyrirfram.

Í stað þess að nota sjálfvirkan útreikning sem er gerður þegar reiturinn er valinn er hægt að nota keyrsluna **Reikna lágstigskóða** í **framleiðsluvalmyndinni** með því að smella á **vöruhönnun**, **Reikna lágstigskóða**.

> [!IMPORTANT]
> Ef ekki er kveikt á  **dynamic lágstigskóta**  skipta þarf að keyra  **keyrsluna Reikna lágstigskóta**  áður en framboðsáætlun (  **keyrslan Reikna áætlun**) er reiknuð út.  

> [!NOTE]
>  **Þó að reiturinn kvika lágstigs kóti**  sé valinn er lágstigs-Kótarnir í íhlutavörum ekki breyttir breytilegt ef yfiruppskrift er eytt eða stillt á að vera ekki vottuð. Þetta tilfelli gæti gert það erfitt að bæta nýjum vörum við lok vöruskipulagsins því það gæti farið eftir hámarksfjölda lágra tölukóða. Þess vegna er hægt að keyra  **keyrsluna Reikna lágmark stigs kóða til að viðhalda stórum virkjunarkóðum**  sem ná til skipulags á lágmörkum vöru.  

## <a name="see-also"></a><a name="see-also"></a>Sjá einnig .

[Hönnunarupplýsingar: Meðhöndlun endurpöntunarstefnur](design-details-handling-reordering-policies.md)  
[Hönnunarupplýsingar: Jöfnun eftirspurn og framboð](design-details-balancing-demand-and-supply.md)  
[Hönnunarupplýsingar: Miðlægar hugmyndir áætlanakerfis](design-details-central-concepts-of-the-planning-system.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
