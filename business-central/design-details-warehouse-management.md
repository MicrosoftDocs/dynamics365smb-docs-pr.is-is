---
title: Vinna með vöruhúsaaðgerðir
description: Auk móttöku og afhendinga styður Business Central raðir af vöruhúsaaðgerðum innanhúss.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 12/13/2023
ms.custom: bap-template
---

# <a name="warehouse-management-overview"></a>Yfirlit yfir vöruhúsakerfi

Það er tvennt sem skiptir máli fyrir öll fyrirtæki sem flytja vörur líkamlega inn og út úr vöruhúsi þeirra:

* Hann hefur yfirlit yfir birgðastig og staðsetningu vöru í vöruhúsinu.
* Þeir geta á fljótlegan og nákvæman hátt tekið á móti, tínt og sent vörur.

Til að hjálpa fyrirtækjum að ná þessum hlutum eru vöruhúsaaðgerðir til [!INCLUDE[prod_short](includes/prod_short.md)] að bæta eftirfarandi möguleikum við birgðastjórnun:

* Hólf
* Vöruhúsaafhendingar
* Birgðatínslur
* Hreyfingavinnublað

Innleiða þessar aðgerðir í mismunandi samsetningum til að sníða vöruhúsaferli fyrirtækisins. Gera kleift að auka flækjustig eftir því sem fyrirtækið vex og ferli breytist.

## <a name="overview-of-different-configuration-options"></a>Yfirlit yfir mismunandi skilgreiningarvalkosti

Hægt er að grunnstilla vöruhúsaaðgerðir á ýmsa vegu. Mikilvægt er að velja valkosti sem bæta ferla án þess að valda sameiginlegum kostnaði. Eftirfarandi tafla gefur yfirlit yfir dæmigerðar grunnstillingar til að takast á við efnislegar vörur.

|Flækjustig|Heimildasamstæða|Stillingar|Hólfkóði|Dæmi um innleiðarflæði|Dæmi um flæði á útleið|Dæmi um innra flæði|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Engin sérstök vöruhúsaaðgerð.|Bókun úr pöntunum og færslubókum.||Valfrjáls. Hólfakótanum er stýrt **áskilin** .|Innkaupapöntun|Sölupöntun| Framleiðslupöntun -> Notkunarbók|  
|Grunnatriði|Samsteypumóttaka/sending í mörgum pöntunum.|**Krefjast móttöku**<br>**Krefjast afhendingar**.|Valfrjáls. Hólfakótanum er stýrt áskilin vífæra|Innkaupapantanir -> vöruhúsamóttaka|Sölupöntun - > vöruhúsaafhending|Eins og hér að ofan.|
|Grunnatriði|Pöntun fyrir hverja pöntun.|Krefjast frágangs eða Krefjast tínslu. </br><br/> **ATHUGIÐ**: Þótt stillingarnar séu kallaðar **Krefjast tínslu** og **Krefjast frágangs** er samt hægt að bóka móttökur og afhendingar beint úr upprunaskjölunum í birgðageymslum þar sem þessir gátreitir eru valdir.|Valfrjáls. Hólfakótanum er stýrt **áskilin** .|Innkaupapöntun -> Birgðafrágangur|Sölupöntun -> Birgðatínsla|Framleiðslupöntun -> Birgðatínsla|
|Ítarlegt|Samsteypumóttaka/sending í mörgum pöntunum.<br /><br />Sameinaðar tínslu-/frágangsaðgerðir fyrir mörg upprunaskjöl.|Krefjast móttöku + Krefjast frágangs,</br> Krefjast sendingar + Krefjast tínslu|Valfrjáls. Hólfakótanum er stýrt áskilin vífæra|Innkaupapantanir -> vöruhúsamóttaka -> vöruhúsafrágangi|Sölupantanir -> vöruhúsaafhendingar -> tínsluvinnublað -> vöruhúsatínslur| Framleiðslupöntun -> Tínsluvinnublað -> Vöruhúsatínslur -> Notkunarbók|
|Ítarlegt|Sama og að ofan + Beinar tínslu-/frágangsaðgerðir|Bein tínsla og frágangur (ósjálfstæð vígblöð eru gerð virk sjálfvirkt)|Áskilið|Eins og hér að ofan.|Eins og hér að ofan.| Framleiðslupöntun -> Vinnublað tínslu -> Vöruhús - Tínslubók tínslu|

Flækjustigið eykst með stærð fyrirtækisins og hversu margar deildir og fólk á í hlut. Ferli getur til dæmis verið einfalt þegar sami aðili stofnar og bókar söluskjal. Ferlar geta einnig verið flóknari og tekið þátt í nokkrum skrefum og einstaklingum. Eftirfarandi skref eru dæmi um flóknari ferli:

1. Pantanavinnsla stofnar sölupöntun.
1. Yfirmaður vöruhúss stofnar tínsluleiðbeiningar.
1. Starfsmaður í vöruhúsi lýkur flæðinu með því að bóka vöruhúsaafhendinguna.

Flókna stigið hefur einnig áhrif á tegundir fylgiskjala sem notuð eru í vöruhúsaaðgerðum. Til dæmis er hægt að nota vöruhúsamóttöku- og vöruhúsafrágangsskjöl fyrir innflæði en nota birgðatínsluskjöl fyrir útleiðarflæðið.

Annar þáttur sem hefur margbreytileika er hvernig raunvöruhúsið er táknað í [!INCLUDE[prod_short](includes/prod_short.md)]. Fræðast meira um [líkan í raunvöruhúsinu](#modeling-the-physical-warehouse).

## <a name="modeling-the-physical-warehouse"></a>Líkan raunvöruhúss

Í boði eru nokkrir valkostir til að tákna uppsetningu vöruhússins í raunheimum [!INCLUDE[prod_short](includes/prod_short.md)]. Valið ákvarðar hvernig unnið er með vöruhúsaaðgerðir.

Staðsetning vara getur verið hillur, birgðageymsla eða hólf og kostir og gallar eru fyrir hvern valkost.

### <a name="locations-and-bins"></a>Birgðageymslur og hólf

Ef meðhöndla á líkamlegar vörur verður að vera að minnsta kosti ein birgðageymsla. Hægt er að nota margar birgðageymslur eða nota hólf til að líkana vöruhúsið og skipulagið.

Gjarnan eru staðsetningar æskilegra leiða til að skipuleggja aðgerðir sem dreifast um landsvæði. Í sumum tilfellum gæti þó þurft að stofna nokkrar birgðageymslur sem eru staðsettar á sama stað. Notkun birgðageymslna hefur eftirfarandi kosti:

* Veita aðgang með því að nota síðurnar **Vöruhúsastarfsmaður** og **Ábyrgðarstöðvar** .
* Skilgreina dagatöl, leiðir og afgreiðslutíma á innleið og útleið fyrir útreikning dagsetninga og áætlunar. Nánari upplýsingar um [áætlunaraðgerðir](production-about-planning-functionality.md).
* Tilgreina sjálfgefnar víddir og nota mismunandi birgðabókunargrunna.
* Setja upp áætlunarfæribreytur. Fræðast meira um [áætlunarfæribreytur](production-about-planning-functionality.md#planning-parameters).  
* Nota mismunandi vöruhúsaaðgerðir fyrir hverja birgðageymslu.

### <a name="shelves-and-bins"></a>Hillur og hólf

Ef vara er alltaf geymd á sama stað er hægt að nota reitinn Hillunúmer **.** á **birgðaspjaldinu** eða **Birgðahaldseiningarspjaldssíðunum** . Þessi reitur getur verið grunnbundið geymslukerfi í umhverfi án hólfa. Gildi reitsins er afritað af birgðaspjaldinu í fylgiskjalslínur og skýrslur, en það er aðeins upplýsingar. Gildið er ekki notað í vöruhúsaaðgerðum eða útreikningum á ráðstöfunarmagni.

Hólf tákna grunnvöruhúsaskipulagið og eru notuð til að gera tillögur um staðsetningu vöru:

* Eitt eða fleiri föst hólf fyrir vöru.
* Hólf fyrir tilteknar aðgerðir, t.d. afhendingarhólf eða framleiðslufrálagshólf.
* Hólfageta og þyngdartakmarkanir (aðeins fyrir beinan frágang og tínslu).
* Hólfaeinkunn (aðeins fyrir beinan frágang og tínslu).

## <a name="typical-warehouse-workflow"></a>Dæmigerðt vöruhúsaverkflæði

Eftirfarandi tafla lýsir röð verkefna með tenglum í greinar þar sem þeim er lýst.

|**Til að**|**Sjá**|  
|------------|-------------|  
|Í grunnflæði á grundvellinum pöntun-fyrir-pöntun er notaður birgðafrágangur til að skrá móttöku á vörum í birgðageymslum, þar á meðal yfirmóttöku. Einnig er hægt að nota vöruhúsamóttöku ef verið er að sameina margar pantanir í móttökunni.|[Flæði á innleið](design-details-inbound-warehouse-flow.md)|
|Skrá afhendingu vara úr vöruhúsastaðsetningum. Birgðatínsla er notuð á grundvelli pöntunar fyrir hverja pöntun. Einnig er hægt að nota vöruhúsaafhendingu ef verið er að sameina margar pantanir í afhendingunni.|[Flæði á útleið](design-details-outbound-warehouse-flow.md)|
|Meðhöndla vörur innan vöruhússstaðsetningarinnar. Til dæmis þegar íhlutir eru fluttir í framleiðslu eða talning raunbirgða gerð.|[Innra flæði](design-details-internal-warehouse-flows.md)|

Setja upp vöruhúsaferlin sem henta fyrirtækinu. Nánari upplýsingar um [uppsetningu vöruhúsastjórnunar](warehouse-setup-warehouse.md).

## <a name="terminology-related-to-warehouse-management"></a>Hugtakafræði sem tengist vöruhúsakerfi

### <a name="complexity-levels"></a>Flóknari stig

Við notum hugtökin "grunn" og "ítarleg" til að greina á milli flækjustiga. Þessi einfaldi aðgreining nær yfir nokkur flókin stig í uppsetning birgðageymslu, hvert fyrir sig sem studd er af mismunandi vöruhúsaskjölum. Þróaðasta stigið í birgðahaldi er kallað "Beinn frágangur og tínsla." Til að nota beinan frágang og tínslu í birgðageymslu skal kveikja á beinum **frágangi og tínsluspjöldum** á síðunni **Birgðageymsluspjald** .

### <a name="warehouse-flows"></a>Vöruhúsaflæði

* Flæði á innleið - Færa vörur inn í vöruhúsið og gera þær tiltækar, t.d. innkaup og millifærslur á innleið.
* Útleiðarflæði - Tínsla og afhenda vörur til viðskiptamanna eða annarra birgðageymslna.
* Innra flæði - Meðhöndla vörur innan birgðageymslu. Til dæmis má færa íhluti í framleiðslu eða telja raunbirgðir.

### <a name="basic-documents"></a>Grunnskjöl

Eftirfarandi skjöl eru notuð í einfaldum vöruhúsaflæðum.

* Birgðafrágangur
* Birgðatínsla
* Birgðahreyfing
* Færslubók atriðis
* Endurflokkunarbók vöru

### <a name="advanced-documents"></a>Ítarleg skjöl

Eftirfarandi skjöl eru notuð í ítarlegum vöruhúsaflæðum.

* Vöruhúsamóttaka
* Vinnublað frágangs
* Frágangur vöruhúss
* Vinnublað tínslu
* Vöruhúsatínsla
* Hreyfingavinnublað
* Vöruhúsatínsla
* Innanhússtínsla vöruhúss
* Innanhússfrágangur
* Vinnublað hólfastofnunar
* Vinnublað f. stofnun hólfainnihalds
* Birgðabók vöruhúss
* Endurflokkunarbók vöruhúss

### <a name="pages-and-settings"></a>Síður og stillingar

Í þessum hluta er lýst hugtökunum á bak við lykilsíður og stillingar vöruhúsa.

#### <a name="bins-and-bin-content"></a>Hólf og innihald hólfa

Hólf er geymslutæki sem hannað fyrir geymslu tiltekinna hluta. Minnsta gámaeiningin er í [!INCLUDE[prod_short](includes/prod_short.md)]. Vörumagn í hólfum er kallað *hólfainnihald*. Uppfletting í reitnum **Vara** eða reitnum **Hólfakóði** á vöruhúsatengdri skjalalínu sýnir reiknað framboð vöru í hólfi.  

Innihald hólfs getur verið **Fast**, **Sérþekkt** eða **Sjálfgefið** til að skilgreina hvernig á að nota hólfainnihaldið. Hólf með enga eiginleika eru kallað *fljótandi* hólf.  

Fast hólf geymir vörur sem úthlutað er á hólfakótann. Fasta hólfaeiginleikinn tryggir að jafnvel þótt hólfið sé tæmt hverfur hólfainnihaldið ekki. Hægt er að velja hólfið aftur um leið og það er fyllt á.  

Sérþekkt hólf inniheldur hólfainnihald sem aðeins er hægt að tína fyrir tiltekinn forða sem notar hólfið. Til dæmis vélastöð. Annað efni sem ekki er tínt, svo sem magn á útleið í afhendingarbókun, er hægt að nota úr sérstöku hólfi. Aðeins innihald hólfs sem notað er í reiknireglunni **Stofna tínslu** er varið í sérstöku hólfi.  

[!INCLUDE [prod_short](includes/prod_short.md)] notar eiginleikann **Sjálfgefið** hólf til að leggja til hólf fyrir vöruhúsaaðgerðir. Sjálfgefni hólfaeiginleikinn er ekki notaður í birgðageymslum sem nota beinan frágang og tínslu. Í birgðageymslum þar sem hólfa er krafist tilgreinir eiginleikinn hvar setja á vörur í flæði á innleið. Í flæði á útleið tilgreinir eiginleikinn hvaðan taka á vörur.  

> [!NOTE]  
> Ef vörur á útleið eru settar í nokkur hólf eru vörur teknar úr sjálfgefnu hólfunum fyrst, til að tæma það hólfainnihald og vörurnar sem eftir eru eru teknar úr sjálfgefna hólfinu.  

Hægt er að hafa eitt sjálfgefið hólf fyrir hverja vöru fyrir hverja birgðageymslu.  

#### <a name="bin-type"></a>Hólfategund

Birgðageymslur sem nota beinan frágang og tínslu geta notað hólfategundir. Hólfategundir stjórna aðgerðunum sem leyfðar eru fyrir hólf. 

Eftirfarandi tegundir hólfa eru tiltækar:  

|Tegund hólfs|Heimildasamstæða|  
|------------------|---------------------------------------|  
|MÓTTAKA|Vörur sem mótteknar eru en eru ekki frágengnar.|  
|SHIP|Vörur sem eru tíndar fyrir vöruhúsaafhendingarlínur en eru ekki bókaðar sem afhentar.|  
|FRÁGANGUR|Yfirleitt eru vörur til að geyma í stórum mælieiningum en ekki er óskað eftir aðgangi að til tínslu. Þessi hólf eru ekki notuð til tínslu, annaðhvort í framleiðslupöntunum eða afhendingum, svo notkun þeirra gæti verið takmörkuð. Þessi tegund hólfs er gagnleg þegar keypt er inn mikið af vörum. Hólfin ættu alltaf að hafa lága hólfaflokkun þannig að fyrst sé gengið frá vörum með PUTPICK-hólf með hærra flokkuð PUTPICK-hólf. Fylla reglulega á þessa tegund af hólfi þannig að vörur þeirra séu tiltækar í PUTPICK- eða PICK-hólfum.|  
|TAKA TIL|Vörur sem aðeins eru notaðar í tínslu. Aðeins er hægt að nota hreyfingar til að fylla á þessi hólf, ekki frágang.|  
|PUTPICK|Vörur í hólfum sem lagðar eru til bæði fyrir frágang og tínslur. Hólf af þessari tegund eru líklega með mismunandi hólfaflokkun. Setja upp magngeymsluhólf með lægri hólfaflokkun en venjuleg tínsluhólf eða hólf á framtíðartínslusvæðinu.|  
|QC|Þetta hólf er notað fyrir birgðaleiðréttingar ef þetta hólf er tilgreind á birgðageymsluspjaldinu í reitnum **Leiðréttingahólfskóði**. Einnig er hægt að setja upp hólf af þessari tegund fyrir gallaðar vörur og vörur sem teknar eru til skoðunar. Hægt er að flytja vörur í hólf af þessari tegund ef þær eiga ekki að vera tiltækar í venjulegu vöruflæði. **Til athugunar:**  Ólíkt öllum öðrum hólfategundum **er** sjálfgefið að hólfategundin fyrir vörustjórnun sé valin. Innihaldið sem sett er í hólf fyrir QC er undanskilið vöruflæði.|  

Hægt er að reka vöruhúsið með öllum átta hólfategundunum sem mögulegar eru, eða nota aðeins hólfategundirnar RECEIVE, PUTPICK, SHIP og QC. Þessar fjórar hólfategundir gera kleift að gera tillögur um vöruflæði og gera notandanum kleift að skrá misræmi í birgðum.
Að undanskildum tegundunum PICK, PUTPICK og PUTAWAY hólfategundin tilgreinir hólfategundin aðgerðina sem leyfð er fyrir hólf. Til dæmis er aðeins hægt að nota MÓTTÖKUtegund hólfs til að taka á móti vörum eða tína vörur úr.  

> [!NOTE]  
> Nota verður hreyfingar til að færa vörur í MÓTTAKA og QC-hólf. Á sama hátt eru hreyfingar notaðar til að færa vörur úr SHIP og QC-hólfum.  

#### <a name="bin-ranking"></a>Hólfaflokkun

Í ítarlegri birgðahaldsvinnublaði er hægt að gera sjálfvirkar og bestar hvernig á að safna vörum í frágangs- og tínsluvinnublöð með því að flokka hólf. Vörur eru lagðar til fyrir tínslur og frágang samkvæmt hólfaflokkunum.

Frágangsferli eru bjartsýni samkvæmt hólfaflokkun með því að leggja til hærra flokkuð hólf fyrir lægra flokkuð hólf. Tínsluferli leggja til vörur með hæstu hólfaflokkun úr hólfainnihaldi fyrst. Áfylling hólfa leggur til lægri flokkuð hólf fyrir hærri flokkuð hólf.  

Hólfaflokkun og innihald hólfa eru grunneiginleikar sem leiðbeina vöruhúsastarfsmönnum í vöruhúsinu.  

#### <a name="bin-setup"></a>Uppsetning hólfs

Í ítarlegri vörugeymslu er hægt að tilgreina eftirfarandi gildi afkastagetu til að stjórna því hvernig og í hvaða hólf eru geymdar vörur:

* Magn
* Rúmföt í heild
* Þyngd  

Hægt er að úthluta vörum grunnmælieiningu (UOM). Grunnviðmið geta verið stykki, bretti, lítrar, grömm eða kassar. Einnig er hægt að búa til stærri UOM sem byggjast á grunnviðmótinu. Ef stykki eru grunnviðmið gæti bretti verið jafnt 16 stykkjum.  

Ef vara er með meira en eitt UOM skal stilla hámarksmagn fyrir hvert UOM á birgðaspjaldinu. Ef vara er meðhöndluð í stykkjum og brettum er hámarksmagnið í reitnum **Hám.magn.** á síðunni **Innihald** hólfs fyrir vöruna verður einnig að vera í stykkjum og brettum. Annars er leyfilegt magn þess hólfs ekki reiknað rétt.  

Áður en takmarkanir á afkastagetu eru settar upp fyrir innihald hólfs á hólfi þarf að ganga úr skugga um að UOM og víddir vörunnar séu settar upp á vörunni.  

> [!NOTE]  
> Aðeins er hægt að nota mörg birgðageymslur sem nota beinan frágang og tínslu. Í öllum öðrum grunnstillingum er aðeins hægt að nota hólfainnihald í grunnfrávikinu. Í færslum með UOM sem er stærra en grunnmælieining vörunnar er magninu breytt í grunnmælieininguna.  

#### <a name="zone"></a>Svæði

Í ítarlegri vöruhúsaaðgerð er hægt að flokka hólf á svæðum til að stjórna því hvernig verkflæði vöruhúsaaðgerða er stýrt fyrir birgðageymslur.  

Svæði getur verið móttökusvæði eða birgðasvæði og hvert svæði getur samanstaðið af einu eða fleiri hólfum.  

Flestum eiginleikum sem úthlutað er á svæði er úthlutað á hólfin sem stofnuð eru fyrir svæðið.  

#### <a name="warehouse-class"></a>Vöruhúsaflokkur

Í ítarlegri vöruhúsaaðgerð er hægt að úthluta vöruhúsaflokkskótum á eftirfarandi einingar: 

* Vörur
* Hólf
* Svæði

Vöruhúsaflokkar stjórna hvar geyma á vörur. Hægt er að deila svæði upp í nokkra vöruhúsaflokka. Til dæmis er hægt að geyma vörur á móttökusvæðinu sem frystar, hættulegar eða aðra flokka.

Þegar unnið er með vöruhúsaflokka og sjálfgefið móttöku-/afhendingarhólf þarf að velja handvirkt viðeigandi hólf í vöruhúsamóttöku- og afhendingarlínunum.  

Í flæði á innleið er flokkskótinn aðeins auðkenndir í línum á innleið þar sem vöruflokkskótinn passar ekki við sjálfgefið móttökuhólf. Ef ekki er hægt að úthluta réttum sjálfgefnum hólfum er ekki hægt að taka á móti magninu.  

#### <a name="location"></a>Staðsetningu

Birgðageymsla er efnisleg skipulag eða staður þar sem tekið er á móti birgðum, geymdar og afhentar. Staðsetning getur verið vöruhús, þjónustubíll, sýningarsalur, verksmiðja eða svæði í verksmiðju. Birgðum er oft raðað í hólfum og svæðum.

#### <a name="first-expired-first-out"></a>Fyrst runnið út fyrst út

Ef gátreiturinn **Tína eftir FEFO** er valinn á flýtiflipanum **Hólfareglur** á **síðunni Birgðageymsluspjald** eru vöruraktar vörur tíndar í birgðageymslunni samkvæmt fyrningardagsetningu þeirra. Vörur með fyrstu fyrningardagsetningar eru tíndar fyrst.  

Vöruhúsaaðgerðum í öllum tínslu- og hreyfingaskjölum er raðað eftir FEFO, nema vörunum hafi verið úthlutað rað- eða lotunúmerum. Ef sumu, en ekki öllu, hefur magnið í línunni úthlutað rað- eða lotunúmerum er eftirstöðvunum raðað eftirstöðvar samkvæmt FEFO.  

Við tínslu samkvæmt FEFO er vörum sem renna út fyrst safnað saman í bráðabirgða vörurakningarlista samkvæmt fyrningardagsetningunni. Ef tvær vörur hafa sömu fyrningardagsetningu er varan með lægsta lotu- eða raðnúmerið tínd fyrst. Ef lotu- eða raðnúmerin eru eins er varan sem skráð var fyrst valin fyrst. Staðlaðar viðmiðanir um val á vörum í tínsluhólfum, svo sem Hólfaflokkun og Einingaskipti, eru notaðar á bráðabirgða FEFO vörurakningarlistann.  

#### <a name="put-away-template"></a>Frágangssniðmát

Frágangssniðmát tilgreina safn forgangsreglna sem eiga við þegar frágangur er stofnaður. Til dæmis getur frágangssniðmát krafist þess að vörur séu settar í hólf með hólfainnihaldi sem er með sama UOM. Ef svipað hólf með nægilega marga afkastagetu finnst ekki verður að setja vöruna í autt hólf. Vöru og birgðageymslu er úthlutað frágangssniðmáti.  

## <a name="see-also"></a>Sjá einnig .

[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
