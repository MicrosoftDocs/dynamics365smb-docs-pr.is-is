---
title: Stjórna vöruhúsastarfsemi
description: Auk kvittana og sendinga styður Business Central röð af innri vöruhúsastarfsemi.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 12/13/2023
ms.custom: bap-template
---

# <a name="warehouse-management-overview"></a>Yfirlit yfir vöruhússtjórnun

Það eru tveir hlutir sem eru mikilvægir fyrir öll fyrirtæki sem flytja vörur líkamlega inn og út úr vöruhúsi sínu:

* Þeir hafa yfirsýn yfir birgðastig og vörustaðsetningu í vöruhúsinu.
* Þeir geta fljótt og örugglega tekið á móti, valið og sent vörur.

Til að hjálpa fyrirtækjum að ná þessum hlutum bæta vöruhúseiginleikar í [!INCLUDE[prod_short](includes/prod_short.md)]  eftirfarandi getu við birgðastjórnun:

* Hólf
* Vöruhúsasendingar
* Birgðaval
* Verkefnablað fyrir hreyfingu

Innleiða þessa eiginleika í mismunandi samsetningum til að sérsníða vöruhúsaferli fyrir fyrirtæki þitt. Gerðu kleift að auka flókið eftir því sem fyrirtækið þitt stækkar og ferlar þínir breytast.

## <a name="overview-of-different-configuration-options"></a>Yfirlit yfir mismunandi stillingarvalkosti

Þú getur stillt vöruhúseiginleika á ýmsa vegu. Það er mikilvægt að velja valkosti sem bæta ferla þína án þess að valda kostnaði. Eftirfarandi tafla gefur yfirlit yfir dæmigerðar stillingar til að takast á við efnislegar vörur.

|Flækjustig|Heimildasamstæða|Stillingar|Hólfkóði|Dæmi um innstreymi|Dæmi um útstreymi|Dæmi um innra flæði|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Engin sérstök vöruhúsaaðgerð.|Bókun úr pöntunum og dagbókum.||Valfrjálst. Stjórnað af **Bin Code er skylda** rofi.|Innkaupapöntun|Sölupöntun| Framleiðslupöntun -> Neysludagbók|  
|Grunnatriði|Samþætt móttöku/sendingabókun fyrir margar pantanir.|**Krefjast kvittunar**<br>**Krefjast skips**.|Valfrjálst. Stjórnað af Bin Code er skyldubundinn rofi|Innkaupapantanir -> Vöruhússkvittun|Sölupöntun -> Vöruhúsasending|Sama og fyrir ofan.|
|Grunnatriði|Röð eftir pöntun.|Krefjast frágangs eða Krefjast vals. </br><br/> **ATHUGIÐ**: Þótt stillingarnar séu kallaðar **Require Pick** og **Require Set-away**, þú getur samt bókað kvittanir og sendingar beint úr upprunaskjölunum á stöðum þar sem þú velur þessa gátreit.|Valfrjálst. Stjórnað af **Bin Code er skylda** rofi.|Innkaupapöntun -> Birgðasetning|Sölupöntun -> Birgðaval|Framleiðslupöntun -> Birgðaval|
|Ítarlegt|Samþætt móttöku/sendingabókun fyrir margar pantanir.<br /><br />Samþætt tínsla/frálát starfsemi fyrir mörg frumskjöl.|Krefjast kvittunar + Krefjast frágangs,</br> Krefjast sendingar + Krefjast vals|Valfrjálst. Stjórnað af Bin Code er skyldubundinn rofi|Innkaupapantanir -> Vöruhússkvittun -> Vöruhús frágangur|Sölupantanir -> Vöruhúsasendingar -> Velja vinnublað -> Vöruhúsaval| Framleiðslupöntun -> Velja vinnublað -> Vöruhúsval -> Neysludagbók|
|Ítarlegt|Sama og hér að ofan + Stýrð tínsla/frágangur|Stýrt val og frágang (háðir rofar eru virkjaðir sjálfkrafa)|Áskilið|Sama og fyrir ofan.|Sama og fyrir ofan.| Framleiðslupöntun -> Velja vinnublað -> Neysludagbók vöruhúsvals|

Flækjustig eykst með stærð fyrirtækis þíns og hversu margar deildir og fólk tekur þátt. Ferli getur verið einfalt, til dæmis þegar sami aðili býr til og bókar söluskjal. Ferlar geta líka verið flóknari og tekið til nokkurra þrepa og fólks. Eftirfarandi skref eru dæmi um flóknara ferli:

1. Pöntunaraðili býr til sölupöntun.
1. Vöruhússtjóri býr til tínsluleiðbeiningar.
1. Starfsmaður vöruhúss klárar flæðið með því að bóka vöruhúsasendinguna.

Flækjustigið hefur einnig áhrif á gerðir skjala sem þú notar í vöruhúsastarfsemi þinni. Til dæmis er hægt að nota vöruhússkvittun og vöruhúsaflátsskjöl fyrir innstreymi þitt, en notaðu birgðatínsluskjöl fyrir útstreymi.

Annar þáttur sem hefur áhrif á flókið er hvernig efnislegt vöruhús þitt er táknað í [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar er að finna á [Módelun á líkamlegu vöruhúsi](#modeling-the-physical-warehouse).

## <a name="modeling-the-physical-warehouse"></a>Líkan á líkamlegu vöruhúsi

Þú hefur nokkra möguleika til að tákna raunverulega uppsetningu vöruhússins þíns í [!INCLUDE[prod_short](includes/prod_short.md)]. Val þitt ákvarðar hvernig þú vinnur með vöruhúseiginleika.

Staðsetning hluta getur verið hillur, staðsetningar eða bakkar og það eru kostir og gallar fyrir hvern valkost.

### <a name="locations-and-bins"></a>Staðsetningar og ruslar

Til að meðhöndla líkamlegar vörur verður þú að hafa að minnsta kosti einn stað. Þú getur notað margar staðsetningar eða notað hólf til að móta vöruhús þitt og skipulag.

Venjulega eru staðsetningar ákjósanlegasta leiðin til að skipuleggja starfsemi sem er dreift yfir landfræðileg svæði. Í sumum tilfellum gætirðu þó viljað búa til nokkrar staðsetningar sem eru staðsettar á sama stað. Notkun staðsetningar hefur eftirfarandi kosti:

* Veittu aðgang með því að nota **Vöruhússtarfsmanna** og **ábyrgðarmiðstöðvar** síðurnar.
* Skilgreindu dagatöl, leiðir og afgreiðslutíma á heimleið og útleið fyrir dagsetningarútreikning og áætlanagerð. Lærðu meira á [Um skipulagsvirkni](production-about-planning-functionality.md).
* Tilgreindu sjálfgefnar víddir og notaðu mismunandi birgðabókunaruppsetningar.
* Settu upp skipulagsbreytur. Frekari upplýsingar eru á [Skipulagsbreytur](production-about-planning-functionality.md#planning-parameters).  
* Notaðu mismunandi vöruhúseiginleika fyrir hverja staðsetningu.

### <a name="shelves-and-bins"></a>Hillur og bakkar

Ef þú geymir hlut alltaf á sama stað geturðu notað **hillu nr.** Reitinn á **vörukorti** eða **birgðahaldskorti** síðunum. Þessi reitur getur verið undirstöðu handvirkt geymslukerfi í umhverfi án rusla. Gildi reitsins er afritað af vöruspjaldinu í skjallínur og skýrslur, en það er aðeins til upplýsinga. Gildið er ekki notað í vöruhúsastarfsemi eða útreikningum á framboði.

Bakkar tákna grunnbyggingu vöruhússins og eru notuð til að koma með tillögur um staðsetningu vara:

* Ein eða fleiri fastar bakkar fyrir vöru.
* Hólf fyrir sérstakar aðgerðir, svo sem sendingarhólf eða framleiðsluúttakshólf.
* Afkastagetu og þyngdartakmarkanir (aðeins fyrir beint frágang og tínslu).
* Einkunn fyrir ruslakörfu (aðeins fyrir beint frágang og val).

## <a name="typical-warehouse-workflow"></a>Dæmigert verkflæði vöruhúsa

Eftirfarandi tafla lýsir röð verkefna með tenglum í greinar þar sem þeim er lýst.

|**Til að**|**Sjá**|  
|------------|-------------|  
|Í grunnflæði eftir pöntun, notaðu birgðafrágang til að skrá móttöku vara á stöðum, þar með talið allar ofmóttökur. Eða, ef þú ert að sameina margar pantanir í kvittuninni, notaðu vöruhússkvittun.|[Innstreymi](design-details-inbound-warehouse-flow.md)|
|Skráðu sendinguna á hlutum frá vöruhúsastöðum. Notaðu birgðatínslu fyrir hverja pöntun. Eða, ef þú ert að sameina margar pantanir í sendingunni, notaðu vöruhúsasendingu.|[Útstreymi](design-details-outbound-warehouse-flow.md)|
|Meðhöndla hluti innan vöruhússins. Til dæmis, þegar þú færir íhluti í framleiðslu eða gerir efnislega birgðatalningu.|[Innra flæði](design-details-internal-warehouse-flows.md)|

Settu upp vöruhúsaferli sem henta fyrirtækinu þínu. Frekari upplýsingar á [Uppsetning vöruhúsastjórnunar](warehouse-setup-warehouse.md).

## <a name="terminology-related-to-warehouse-management"></a>Hugtök sem tengjast vöruhúsastjórnun

### <a name="complexity-levels"></a>Flækjustig

Við notum hugtökin „grunn“ og „háþróað“ til að greina á milli flækjustigs. Þessi einfalda aðgreining nær yfir nokkur flækjustig í staðsetningaruppsetningum, hvert um sig studd af mismunandi vöruhúsaskjölum. Fullkomnasta stig vörugeymsla er vísað til sem "Bein frágangur og tínsla." Til að nota beint frágang og velja staðsetningu skaltu kveikja á **beint frágangi og vali**  kveikja á **Staðsetningarkort**  síðu.

### <a name="warehouse-flows"></a>Vöruhús flæðir

* Innstreymi - Færa vörur inn á vöruhúsastaðsetningu og gera þær aðgengilegar, svo sem innkaup og millifærslur á innleið.
* Útstreymi - Veldu og sendu hluti til viðskiptavina eða annarra staða.
* Innra flæði - Meðhöndla hluti innan staðsetningar. Til dæmis, færa íhluti til framleiðslu eða telja efnislegar birgðir.

### <a name="basic-documents"></a>Grunnskjöl

Eftirfarandi skjöl eru notuð í grunnflæði vöruhúsa.

* Birgðafrágangur
* Birgðatínsla
* Birgðahreyfing
* Færslubók atriðis
* Endurflokkunarbók vöru

### <a name="advanced-documents"></a>Ítarleg skjöl

Eftirfarandi skjöl eru notuð í háþróuðum vöruhúsaflæði.

* Vöruhúsamóttaka
* Vinnublað frágangs
* Frágangur vöruhúss
* Vinnublað tínslu
* Vöruhúsatínsla
* Hreyfingavinnublað
* Vöruhúsatínsla
* Innra vöruhúsval
* Innri vöruhús frágangur
* Vinnublað hólfastofnunar
* Vinnublað f. stofnun hólfainnihalds
* Birgðabók vöruhúss
* Dagbók um endurflokkun vöruhúss

### <a name="pages-and-settings"></a>Síður og stillingar

Þessi hluti lýsir hugtökum á bak við lykilsíður og stillingar fyrir vörugeymsla.

#### <a name="bins-and-bin-content"></a>Bakkar og innihald rusla

Hólf er geymslutæki sem hannað fyrir geymslu tiltekinna hluta. Það er minnsta gámaeiningin í [!INCLUDE[prod_short](includes/prod_short.md)]. Vörumagn í tunnunum er vísað til sem *innhald hólfa*. Uppfletting í reitnum **Vara** eða reitnum **Hólfakóði** á vöruhúsatengdri skjalalínu sýnir reiknað framboð vöru í hólfi.  

Innihald hólfa getur verið **fast**, **hollt** eða **Sjálfgefið** til að skilgreina hvernig á að nota hólfainnihaldið. Bakkar með engan af þessum eiginleikum eru nefndar *fljótandi* bakkar.  

Föst hólf geymir hluti sem eru úthlutað hólfkóða. Fasta hólfaeiginleikinn tryggir að jafnvel þótt tunnan sé tæmd hverfur innihald tunnunnar ekki. Þú getur valið tunnuna aftur um leið og innihald hennar hefur verið fyllt á.  

Sérstakt hólf geymir hólfaefni sem aðeins er hægt að velja fyrir sérstaka auðlindina sem notar hólfið. Til dæmis vélamiðstöð. Annað efni sem ekki er valið, eins og magn á útleið á sendingarbókun, er hægt að neyta úr sérstakri tunnu. Aðeins innihald hólfs sem notað er í reiknireglunni **Stofna tínslu** er varið í sérstöku hólfi.  

[!INCLUDE [prod_short](includes/prod_short.md)] notar **Sjálfgefin** bin eign til að stinga upp á hólfum fyrir vöruhúsastarfsemi. Á stöðum sem nota beint frágang og tínslu er sjálfgefna hólfaeiginleikinn ekki notaður. Á stöðum þar sem hólfa er krafist, tilgreinir eignin hvar á að staðsetja hluti í innstreymi. Í útstreymi tilgreinir eignin hvaðan á að taka hluti.  

> [!NOTE]  
> Ef vörur á útleið eru settar í mörg hólf eru vörur fyrst teknar úr hólfum sem ekki eru sjálfgefnar til að tæma það hólfsinnihald og eftirstöðvarnar eru teknar úr sjálfgefna hólfinu.  

Þú getur haft eina sjálfgefna rusla fyrir hverja vöru á hverja staðsetningu.  

#### <a name="bin-type"></a>Tegund bakkar

Staðsetningar sem nota beint frágang og tínslu geta notað ruslategundir. Bakkaragerðir stjórna starfseminni sem þú leyfir fyrir ruslakörfu. Eftirfarandi gerðir af bakka eru fáanlegar:  

|Tegund hólfs|Heimildasamstæða|  
|------------------|---------------------------------------|  
|MÓTTAKA|Hlutir sem berast en eru ekki lagðir í burtu.|  
|SHIP|Vörur sem eru teknar fyrir vöruhúsasendingarlínur en eru ekki bókaðar sem sendar.|  
|FRÁGANGUR|Venjulega eru hlutir til að geyma í stórum mælieiningum, en sem þú vilt ekki fá aðgang að í tínsluskyni. Þessar bakkar eru ekki notaðar til tínslu, hvorki fyrir framleiðslupantanir eða sendingar, svo notkun þeirra gæti verið takmörkuð. Þessi tegund af tunnu er gagnleg þegar þú kaupir mikið magn af hlutum. Bakkarnir ættu alltaf að vera með lága röðun í ruslakörfu þannig að hlutir með hærra setta PUTPICK bakka eru settir fyrst. Fylltu reglulega á þessa tegund af hólfum svo að hlutir þeirra séu fáanlegir í PUTPICK eða PICK tegund hólfa.|  
|TAKA TIL|Vörur sem aðeins eru notaðar í tínslu. Þú getur aðeins notað hreyfingar til að fylla á þessar tunnur, ekki til að setja í burtu.|  
|PUTPICK|Hlutir í ruslakörfum sem mælt er með fyrir bæði frágang og tínslu. Hólf af þessari tegund eru líklega með mismunandi hólfaflokkun. Settu upp geymslutunnurnar þínar með lægri tunnuröðun en venjuleg tínslutunnur eða tunnur á framtínslusvæðinu þínu.|  
|QC|Þetta hólf er notað fyrir birgðaleiðréttingar ef þetta hólf er tilgreind á birgðageymsluspjaldinu í reitnum **Leiðréttingahólfskóði**. Einnig er hægt að setja upp hólf af þessari tegund fyrir gallaðar vörur og vörur sem teknar eru til skoðunar. Hægt er að flytja vörur í hólf af þessari tegund ef þær eiga ekki að vera tiltækar í venjulegu vöruflæði. **Athugið:**  Ólíkt öllum öðrum hólfategundum, hefur  **QC** hólf tegundin enginn af gátreitunum meðhöndlun vöru valinn sjálfgefið. Efni sem þú setur í QC rusla er útilokað frá vöruflæði.|  

Að undanskildum tegundunum PICK, PUTPICK og PUTAWAY af hólfum, skilgreinir hólfagerðin þá virkni sem leyfð er fyrir hólf. Til dæmis er aðeins hægt að nota RECEIVE tegund af hólfi til að taka á móti vörum eða velja vörur úr.  

> [!NOTE]  
> Þú verður að nota hreyfingar til að færa hluti í RECEIVE og QC bakkar. notaðu hreyfingar til að flytja hluti úr SHIP- og QC-tunnum.  

#### <a name="bin-ranking"></a>Hólfaflokkun

Í háþróaðri vörugeymslu er hægt að gera sjálfvirkan og fínstilla hvernig á að safna vörum í frágangs- og tína vinnublöð með því að raða hólfum. Stungið er upp á hlutum fyrir val og frágang á grundvelli tunnuröðanna.

Frágangsferlar eru fínstilltir í samræmi við röðun hólfa með því að stinga upp á hærra hólfum fyrir lægri hólfa. Velja ferli stinga upp á hlutum með hæstu hólfaröðun úr hólfainnihaldi fyrst. Áfylling á ruslakörfu bendir til baka í lægri röð á undan hærra hólfum.  

Röðun hólfa og innihald hólfa eru grunneiginleikar sem leiðbeina starfsmönnum vöruhúsa í vöruhúsinu.  

#### <a name="bin-setup"></a>Uppsetning tunnu

Í háþróaðri vörugeymslu er hægt að tilgreina eftirfarandi afkastagetugildi til að stjórna því hvernig og í hvaða hólfum þú geymir vörur:

* Magn
* Heildar teningur
* Þyngd  

Þú getur úthlutað grunnmælieiningu (UOM) á hluti. Grunn UOM gæti verið stykki, bretti, lítrar, grömm eða kassar. Þú getur líka búið til stærri UOM byggt á grunnUOM þínum. Til dæmis, ef stykki eru grunn UOM þín, gæti bretti jafngilt 16 stykki.  

Ef hlutur hefur fleiri en einn UOM, stilltu hámarksmagn fyrir hverja UOM á vöruspjaldinu. Ef þú meðhöndlar hlut í stykkjatali og brettum er **Hámark. Magn** reiturinn á **Hassainnihaldi** síðunni fyrir þann hlut verður einnig að vera í hlutum og brettum. Annars er leyfilegt magn fyrir þá hólf ekki reiknað rétt.  

Áður en þú setur takmarkanir á afkastagetu fyrir innihald hólfs á hólfi skaltu ganga úr skugga um að UOM og stærðir vörunnar séu settar upp á vörunni.  

> [!NOTE]  
> Þú getur aðeins notað margar UOMs á stöðum sem nota beint frágang og tínslu. Í öllum öðrum stillingum er aðeins hægt að nota hólf innihald í grunn UOM. Í færslum með UOM sem er stærri en grunn UOM vörunnar er magninu umreiknað í grunn UOM.  

#### <a name="zone"></a>Svæði

Í háþróaðri vörugeymslu er hægt að flokka hólf í svæði til að stjórna því hvernig verkflæði vöruhúsastarfsemi er beint fyrir staðsetningar.  

Svæði gæti verið móttökusvæði eða birgðasvæði og hvert svæði getur samanstandað af einni eða fleiri tunnum.  

Flestum eiginleikum sem úthlutað er á svæði er úthlutað á hólf sem eru búin til fyrir svæðið.  

#### <a name="warehouse-class"></a>Vöruhúsaflokkur

Í háþróaðri vörugeymslu er hægt að úthluta vöruhúsaflokkakóðum til eftirfarandi aðila: 

* Vörur
* Hólf
* Svæði

Vöruhúsaflokkar stjórna hvar á að geyma hluti. Hægt er að deila svæði upp í nokkra vöruhúsaflokka. Til dæmis gætirðu geymt hluti á móttökusvæðinu sem frosna, hættulega eða annan flokk.

Þegar unnið er með vöruhúsaflokka og sjálfgefna móttöku-/afgreiðsluhólf verður að velja handvirkt viðeigandi hólf í innhreyfingar- og sendingarlínum vöruhúss.  

Í flæði á innleið er flokkskóðinn aðeins auðkenndur á innleiðarlínum þar sem flokkakóðinn vöru passar ekki við sjálfgefna móttökuhólfið. Ef réttum sjálfgefnum hólfum er ekki úthlutað er ekki hægt að taka á móti magninu.  

#### <a name="location"></a>Staðsetningu

Staðsetning er efnisleg uppbygging eða staður þar sem birgðir eru mótteknar, geymdar og sendar. Staðsetning getur verið vöruhús, þjónustubíll, sýningarsalur, verksmiðja eða svæði í verksmiðju. Birgðir eru oft skipulagðar í tunnur og svæði.

#### <a name="first-expired-first-out"></a>Fyrst rann út fyrst út

Ef þú velur **Velja samkvæmt FEFO**  gátreitinn á **Reglur um ruslakörfu**  Flýtiflipi á **Staðsetningarkort**  síðu eru vörur raktar vörur valdir á staðsetningu í samræmi við gildistíma þeirra. Hlutir með elstu fyrningardagsetningar eru valdir fyrst.  

Vöruhúsastarfsemi í öllum tínslu- og flutningsskjölum er flokkuð samkvæmt FEFO, nema hlutunum sé úthlutað rað- eða lotunúmerum. Ef eitthvað, en ekki allt, magnsins á línunni hefur úthlutað rað- eða lotunúmerum, er eftirstandandi magnið flokkað samkvæmt FEFO.  

Við tínslu með FEFO er vörum sem renna fyrst saman í tímabundinn vörurakningarlista miðað við fyrningardagsetningu. Ef tveir hlutir hafa sömu fyrningardagsetningu er hluturinn með lægsta lotuna eða raðnúmerið valinn fyrst. Ef hlut- eða raðnúmerin eru þau sömu er fyrst valinn hlutur sem var skráður fyrst. Stöðluð viðmið fyrir val á hlutum í tiltektarhólfum, eins og hólfunaröðun og lausafjölda, eru notuð á tímabundna FEFO vörurakningarlistann.  

#### <a name="put-away-template"></a>Sniðmát til að setja burt

Frágangssniðmát tilgreina sett af forgangsreglum sem gilda þegar þú býrð til frágangs. Til dæmis getur frágangssniðmát krafist þess að þú setjir hluti í hólk með innihaldi hólfa sem hefur sömu UOM. Ef sambærileg tunna með nægilega miklu afkastagetu finnst ekki verður að setja vöruna í tóma tunnu. Þú úthlutar frágangssniðmáti á hlut og staðsetningu.  

## <a name="see-also"></a>Sjá einnig .

[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
