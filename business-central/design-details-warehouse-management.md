---
title: Umsjón með vöruhúsaaðgerðum
description: Auk innhreyfinga og sendinga styður Viðskiptamiðröð innri vöruhúsaaðgerðir.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 12/05/2022
ms.custom: bap-template
---

# Yfirlit yfir vöruhúsastjórnun

Það er tvennt sem skiptir öllu máli fyrir öll fyrirtæki sem flytja vörur inn og út úr vöruhúsi sínu:

* Þær hafa yfirlit yfir birgðastig og staðsetningu vöru í vöruhúsinu.
* Þau geta fljótt og nákvæmlega tekið á móti, sótt og sent vörur.

Til að hjálpa fyrirtækjum að ná þeim hlutum er vöruhúsaaðgerðum  [!INCLUDE[prod_short](includes/prod_short.md)]  bætt eftirfarandi eiginleikum við birgðastjórnun:

* Hólf
* Afhendingar vöruhúss
* Birgðatínslur
* Vinnublað hreyfinga

Útfæra þessar aðgerðir í mismunandi samsetningum til að sníða vöruhúsaferlana fyrir fyrirtækið. Heimilið fyrir að auka margbreytileika eftir því sem fyrirtækið þitt stækkar og ferlar þínir breytast.

## Yfirlit yfir mismunandi skilgreiningarvalkosti

Hægt er að skilgreina vöruhúsaaðgerðir á ýmsa vegu. Það skiptir miklu máli að Valkostir þú velur að bæta ferla þína án þess að valda rekstrarkostnaði. Eftirfarandi tafla gefur yfirlit yfir dæmigerðar skilgreiningar sem eru notaðar þegar verið er að fást við efnislegar vörur.

|Flækjustig|Description|Stillingar|Hólfkóti|Dæmi um innflæði|Dæmi um flæði á útleið|Dæmi um innra rennsli|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Engin sérstök vöruhúsaaðgerð.|Bókun úr pöntunum og færslubókum.||Valfrjálst. Hólfakóta er skylda  **að**  skipta út.|Innkaupapöntun|Sölupöntun| Framl. pöntunar-> notkunarbók|  
|Grunnatriði|Sameinuð Móttaka/bókun skipa fyrir margar pantanir.|**Krefjast kvittunar**<br>**Krefjast skips**.|Valfrjálst. Hólfakóta sem stjórnað er er skylda að skipta|Innkaupapantanir-> vöruhúsamóttaka|Sölupöntun-> vöruhúsaafhending|Sama og fyrir ofan.|
|Grunnatriði|Pöntun-eftir pöntun.|Krafist frágangs eða krafist tínslu. </br><br/> **Til athugunar** : þrátt fyrir að stillingarnar kalli  **á tiltekt**  og  **frágangssendingar** er samt hægt að bóka móttökur og afhendingar beint úr upprunaskjölunum á birgðageymslum þar sem gátreitirnir eru valdir.|Valfrjálst. Hólfakóta er skylda  **að**  skipta út.|Innkaupapöntun-> Birgðafrágangur|Sölupöntun-> Birgðatínsla|Framleiðslupöntun-> Birgðatínsla|
|Ítarlegt|Sameinuð Móttaka/bókun skipa fyrir margar pantanir.<br /><br />Sameinuð tínsla-/frágangsverkþættir fyrir mörg upprunaskjöl.|Krefjast innhreyfinga + Krefjast frágangs,</br> Krefjast skips + krefjast tínslu|Valfrjálst. Hólfakóta sem stjórnað er er skylda að skipta|Innkaupapantanir-> vöruhúsamóttaka-> vöruhúsafrágangur|Sölupantanir-> vöruhúsaafhendingar-> vinnublað-> Vöruhúsatiltekt| Framleiðslupöntunin-> tínsluvinnublað-> Vöruhúsatiltekt-> notkunarbók|
|Ítarlegt|Sama og fyrir ofan + beinar frágangs/frágang frágangsverkþátta|Beinar Tínslugerð og frágangingar (háðir víxlar verða virkjaðir sjálfkrafa)|Áskilið|Sama og fyrir ofan.|Sama og fyrir ofan.| Framleiðslupöntunin-> vinnublað-> Vöruhúsatínslubók vöruhúss|

Flækjustvið eykst með stærð fyrirtækisins og hversu margar deildir og fólk er að ræða. Ferli getur verið einfalt, til dæmis þegar sami einstaklingur stofnar og bókar söluskjal. Ferlar geta líka verið flóknir, og falið í sér nokkur skref og fólk. Eftirfarandi skref eru dæmi um flóknara ferli:

1. Pöntunarörgjörvi stofnar sölupöntun.
1. Vöruhúsastjórnandi stofnar tínsluleiðbeiningar.
1. Starfsmaður í vöruhúsi lýkur við flæðið með því að bóka vöruhúsaafhendinguna.

Einnig hafa áhrif á flækjustig verið í þeim tegundum skjala sem notuð eru í vöruhúsaaðgerðum. Til dæmis er hægt að nota skjöl um vöruhúsamóttöku og vöruhúsafrágang fyrir innflæðið en nota birgðatínsluskjöl fyrir útstreymissengi.

Annar þáttur sem hefur áhrif á flókið er hvernig efnislegt vöruhús er táknað í [!INCLUDE[prod_short](includes/prod_short.md)].  [Frekari upplýsingar um hvernig á að líkana efnislegt vöruhús](#modeling-the-physical-warehouse).

## Líkan að efnislegu vöruhúsi

Nokkrir valkostir eru í uppsetningu til að tákna raunheimsuppsetningu vöruhúss í [!INCLUDE[prod_short](includes/prod_short.md)]. Valið ræður því hvernig unnið er með vöruhúsaaðgerðir.

Staðsetningin á vörunum getur verið hillur, birgðageymslur eða hólf og það eru kostir og gallar við hvern valkost.

### Staðsetningar og hólfa

Til að afgreiða efnislegar varnir þarf að hafa a.m.k. eina staðsetningu. Hægt er að nota marga staði eða nota hólf til að líkta vöruhúsinu og stjórnskipulagi.

Yfirleitt eru staðsetningar ákjósanlegri leið til að skipuleggja aðgerðir sem eru dreifðar yfir landsvæði. Í sumum tilfellum gæti þó verið æskilegt að búa til nokkra staði sem eru staðsettir á sama stað. Notkun staðsetningar hefur eftirtalda kosti:

* Veita aðgang með því að nota síður starfsmanna  **-og**  ábyrgðarstöðvar  **á**  vöruhúsi.
* Skilgreinið dagatöl, leiðir og afgreiðslutíma á innleið og útleið fyrir dagsetningarútreikninga og áætlanagerð. [Um Skipulagsaðgerðir](production-about-planning-functionality.md).
* Tilgreina sjálfgefnar víddir og nota mismunandi uppsetningar birgðabókar.
* Setja upp færibreytur áætlunar. Frekari upplýsingar eru í  [færibreytum](production-about-planning-functionality.md#planning-parameters) skipulagsheilingar.  
* Nota mismunandi vöruhúsaaðgerðir fyrir hverja birgðageymslu.

### Hillur og hólf

Ef vara er alltaf notuð á sama stað er hægt að  **nota hillu nr.** á  **birgðaspjaldinu**  eða  **síðum Birgðahaldseiningin** . Í þessum reit má grunna handvirka geymslukerfi í umhverfi án hólfa. Gildi svæðisins er afritað af birgðaspjaldinu í Fylgiskjalslínur og skýrslur en það er aðeins upplýst. Gildið er ekki notað í vöruhúsaaðgerðum eða útreikningum á framboði.

Hólar standa að uppbyggingu grunnvöruhúsa og eru nýttir til að gera tillögur um staðsetningu á vörum:

* Eitt eða fleiri föst hólf fyrir vöru.
* Hólf fyrir tilteknar aðgerðir, til dæmis sendingarhólf eða Afkastað hólf framleiðslu.
* Takmarkanir á afkastagetu og þyngd hólfs (eingöngu fyrir beinan frágang og tínslu).
* Hólfaeinkunn (eingöngu fyrir beinan frágang og tínslu).

## Dæmigert verkflæði vöruhúss

Eftirfarandi tafla lýsir röð verkefna með tenglum í greinar þar sem þeim er lýst.

|**Til að**|**Sjá**|  
|------------|-------------|  
|Í grunnstreymi á grundvelli pöntunar er notaður Birgðafrágangur til að skrá innhreyfingar vara í birgðageymslur, þar með talið yfir innhreyfingar. Ef þú ert að sameina margar pantanir í móttökunni skaltu nota vöruhúsamóttöku.|[Innstreymis](design-details-inbound-warehouse-flow.md)|
|Skrá afhendinguna á vörum frá birgðageymslum vöruhúss. Á grundvelli pöntunar er Birgðatínsla notuð. Eða ef margar pantanir eru samstæður í sendingunni skal nota vöruhúsaafhendingu.|[Flæði út](design-details-outbound-warehouse-flow.md)|
|Afgreiða vörur innan vöruhúsastaðarins. Til dæmis þegar íhlutir eru flutt í framleiðslu eða raunbirgðatalninguna.|[Innra rennsli](design-details-internal-warehouse-flows.md)|

Setja upp vöruhúsaferla sem eru rétt fyrir fyrirtækið. Frekari upplýsingar um  [uppsetningu vöruhúsastjórnunar](warehouse-setup-warehouse.md).

## Hugtök sem tengjast vöruhúsastjórnun

### Flækjustig

Við notum hugtökin "Grunnur" og "Advanced" til að aðgreina á milli stiga flókið. Þessi einfalda aðgreining nær yfir nokkur stig sem eru flókin í uppsetningar staðsetningarinnar sem er studd af mismunandi vöruhúsaskjölum. Háþróaðasta stigagið í vöruhúsnæði er nefnt "beinn frágangur og tínsla." Ef nota á beinan frágang og tínslu fyrir staðsetningu er kveikt  **á síðunni beinn frágangur og tínsla**  á  **síðu staðsetningarkorts** .

### Vöruhús flæðir

* Innflæði-flytja vörur inn í vöruhúsastaðinn og gera þær aðgengilegar, eins og innkaup og flutningar á innleið.
* Flæði út-taka og senda vörur til viðskiptavina eða aðra staði.
* Innra flæði-afgreiðsla atriða innan staðsetningar. Til dæmis, færa íhluti í framleiðslu eða telja efnislegar birgðir.

### Grunnskjöl  

Eftirfarandi skjöl eru notuð í grunnvöruflæðinu.

* Birgðafrágangur
* Birgðatínsla
* Birgðahreyfing
* Færslubók atriðis
* Endurflokkunarbók vöru

### Ítarleg skjöl  

Eftirfarandi skjöl eru notuð í ítarlegum vöruhúsaflæði.

* Móttaka vöruhúss
* Vinnublað frágangs
* Vöruhús - Frágangur
* Vinnublað tínslu
* Vöruhús - Tína
* Hreyfingavinnublað
* Vöruhúsahreyfing
* Innri Vöruhúsatiltekt
* Innri vöruhúsafrágangur
* Vinnublað hólfastofnunar
* Vinnublað f. stofnun hólfainnihalds
* Birgðabók vöruhúss
* Endurflokkunarbók vöruhúss vöru

### Síður og stillingar

Í þessum hluta er lýst hugmyndavinnu á bak við helstu síður og stillingar fyrir vöruhúsnæði.

#### Hólf og hólf að innihaldi

Hólf er geymslutæki sem hannað fyrir geymslu tiltekinna hluta. Það er Minnsti gámaeiningin í [!INCLUDE[prod_short](includes/prod_short.md)]. Vörumagn í hólfum er nefnt  *hólfainnihald*. Uppfletting í reitnum **Vara** eða reitnum **Hólfakóði** á vöruhúsatengdri skjalalínu sýnir reiknað framboð vöru í hólfi.  

Innihald hólfs getur verið  **Fast**,  **tileinkað** eða  **Sjálfgefið**  til að skilgreina hvernig eigi að nota innihald hólfsins. Hólf með enga af þessum eiginleikum nefnast  *fljótandi*  hólf.  

Fast hólf geymir vörur sem eru tengdar hólfakótanum. Eiginleikinn föst hólf tryggir að þó að hólfið sé tæmt hverfur hólfainnihaldið ekki. Hægt er að velja hólfið aftur um leið og fylla á innihald þess.  

Sérvalið hólf inniheldur hólfainnihald sem aðeins er hægt að tína fyrir tileinkaða forðinn sem notar hólfið. Til dæmis vélarstöð. Annað efni sem ekki er valið, til dæmis magn á útleið í sendingarbókun, má nota úr sérframleiddu hólfi. Aðeins innihald hólfs sem notað er í reiknireglunni **Stofna tínslu** er varið í sérstöku hólfi.  

[!INCLUDE [prod_short](includes/prod_short.md)]  **notar sjálfgefna**  hólfeiginleika til að stinga upp á hólfum fyrir vöruhúsaaðgerðir. Í birgðageymslum sem nota beinan frágang og tínslu er sjálfgefinn hólfeiginleiki ekki notaður. Á birgðageymslum þar sem hólfum er krafist Tilgreinir eiginleiki hvar eigi að setja vörur í innflæði. Í streymi á útleið Tilgreinir eiginleikinn hvaðan á að taka vörur.  

> [!NOTE]  
> Ef vörur á útleið eru settar í nokkur hólf eru vörur teknar úr fyrst en ekki sjálfgefið hólf til að tæma innihald hólfs og vörurnar sem eftir eru eru teknar úr sjálfgefnu hólfi.  

Hægt er að hafa eitt sjálfgefið hólf fyrir hverja vöru á staðnum.  

#### Tegund hólfs

Staðsetningar sem nota beinan frágang og tínslu geta notað hólfagerðir. Hólfagerðir stjórna verkþáttum sem eru leyfðir fyrir hólf. Eftirtaldar gerðir hólfa eru tiltækar:  

|Tegund hólfs|Description|  
|------------------|---------------------------------------|  
|MÓTTAKA|Vörur sem eru mótteknar en eru ekki frágangs.|  
|SHIP|Vörur sem eru tíndar fyrir afhendingarlínur vöruhúss en eru ekki bókaðar sem afhentar.|  
|PUT AWAY|Yfirleitt eru vörur til að geyma á stórum mælieiningum en ekki er óskað eftir aðgangi að tiltektartilgangi. Þessi hólf eru ekki notuð við tiltekt, annað hvort fyrir framleiðslupantanir eða afhendingar, þannig að notkun þeirra gæti verið takmörkuð. Þessi tegund af hólfi hentar vel þegar keypt er inn mikið magn af vörum. Hólfin eiga alltaf að vera með lágri hólfaflokkun þannig að aðeins sé gengið frá vörum með hærra flokkuð PUTPICK-hólf. Reglulega fylla þessi tegund hólfa þannig að vörur þeirra séu til í PUTPICK-eða PICK-hólfum.|  
|TÍNA|Vörur sem aðeins eru notaðar í tínslu. Aðeins er hægt að nota hreyfingar við áfyllingu þessara hólfa, ekki frágangur.|  
|PUTPICK|Hlutir í hólfum sem eru lagðir fyrir bæði frágang og tínslu. Hólf af þessari tegund eru líklega með mismunandi hólfaflokkun. Setjið upp fjölhólfa geymsluhólf með neðra hólfi en venjuleg tínsluhólf eða hólf í tínt tiltektarsvæði.|  
|QC|Þetta hólf er notað fyrir birgðaleiðréttingar ef þetta hólf er tilgreind á birgðageymsluspjaldinu í reitnum **Leiðréttingahólfskóði**. Einnig er hægt að setja upp hólf af þessari tegund fyrir gallaðar vörur og vörur sem teknar eru til skoðunar. Hægt er að flytja vörur í hólf af þessari tegund ef þær eiga ekki að vera tiltækar í venjulegu vöruflæði. **Til**   athugunar:  **Ólíkt öllum öðrum hólfstegundum hefur QC**  -hólfagerðin engin af vörumeðhöndlunargátunum sem sjálfgefnar eru. Efni sem sett er í QC-hólfið er útilokað frá vöruflæði.|  

Með undantekningunum TÍNSLU, PUTPICK og PUTAWAY hólfum skilgreinir hólfagerðin verkþátt leyfinnar fyrir hólf. Til dæmis er aðeins hægt að nota hólfategund til að taka á móti vörum eða taka vörur frá.  

> [!NOTE]  
> Nota verður hreyfingar til að færa atriði til MÓTTÖKU og QC-hólfa. nota hreyfingar til að flytja vörur frá SENDIST-og QC-hólfum.  

#### Hólfaflokkun

Í háþróaðri vöruhúsun er hægt að gera og hagræða hvernig á að safna atriðum í frágangs-og tínsluvinnublöðum með því að flokksetja hólf. Vörur eru lagðar fyrir tínslur og frágang út frá hólfröðum.

Frágangsferlar eru bjartir samkvæmt hólfaflokkun með því að leggja hærra flokkuð hólf fyrir lægra flokkuð hólf. Tínsluferli leggja til vörur með hæstu hólfaflokkun úr hólfi fyrst. Hólfaáfylling bendir til lægri flokkahólfa en hærra flokkuð hólf.  

Hólfaflokkun og innihald hólfs eru Grunneiginleikar sem leiðbeina starfsmönnum vöruhúss í vöruhúsinu.  

#### Uppsetning hólfs

Í háþróaðri vöruhúsagildinu er hægt að tilgreina eftirfarandi afkastagetgildi til að stjórna því hvernig hólf eru geymt:

* Magn
* Alger rúmmál
* Þyngd  

Hægt er að tengja grunnmælieiningu (UOM) við vörur. Grunnuom gæti verið stykki, bretti, lítrar, grömm eða kassar. Einnig er hægt að búa til stærri Úmur miðað við grunnan UOM. Ef stykkið er til dæmis á grunni þess gæti bretti verið jafngilt 16 stykkjum.  

Ef vara hefur fleiri en einn UOM skal stilla Hámarksmagn fyrir hvert UOM á birgðaspjaldinu. Ef þú ræður við vöru í stykkjum og brettum er Hámarksmagn  **í**  . Reiturinn á  **Hólfainnihaldssíðu**  fyrir þá vöru verður einnig að vera í stykkjum og brettum. Annars er leyft magn fyrir það hólf er ekki reiknað rétt.  

Áður en afkastatakmarkanir á afkastagetu fyrir innihald hólfs eru stilltar skal ganga úr skugga um að UOM og víddir vörunnar séu settar upp á vörunni.  

> [!NOTE]  
> Aðeins er hægt að nota marga UOMs á staðsetningum sem nota beinan frágang og tínslu. Í öllum öðrum afbrigðum er aðeins hægt að nota innihald hólfs í reitnum grunnuom. Í færslum með UOM sem er stærri en grunnflötur vörunnar er magninu umbreytt í stofn UOM.  

#### Svæði

Í háleita vöruhúsnæði er hægt að flokka hólf í svæði til að stjórna því hvernig verkflæði vöruhúsaaðgerða er beint að birgðageymslum.  

Svæði gæti verið móttökusvæði eða geymslusvæði og hvert svæði getur verið samsett úr einu eða fleiri hólfum.  

Flestum eiginleikum sem úthlutað er á svæði er úthlutað til hólfanna sem eru stofnuð fyrir svæðið.  

#### Vöruhúsaflokkur

Í háþróaðri vöruhússkrá er hægt að úthluta vöruhúsaflokkskóta á eftirtaldar einingar: 

* Vörur
* Hólf
* Svæði

Vöruhúsaklasar stjórna hvar á að geyma vörur. Hægt er að deila svæði upp í nokkra vöruhúsaflokka. Til dæmis gæti verið hægt að geyma vörur á viðtökusvæði sem frosið, hættulítil eða aðra klasa.

Þegar unnið er með vöruhúsaklasa og sjálfgefið móttöku-/afhendingarhólf þarf að velja viðeigandi hólf í vöruhúsamóttöku-og afhendingarlínum vöruhúss.  

Í flæði á innleið er flokkakóði aðeins auðkenndur á innleiðarlínum þar sem vöruflokkakóðinn passar ekki við sjálfgefið móttökuhólf. Ef réttum sjálfgefnum hólfum er ekki úthlutað er ekki hægt að taka við magninu.  

#### Birgðageymsla

Staðsetning er efnislegt skipulag eða staður þar sem birgðir eru mótteknar, geymdar og afhentar. Staðsetning getur verið vöruhús, þjónustubíll, Sýningarrými, álveri eða svæði í álveri. Birgðum er oft raðað í hólf og svæði.

#### Fyrst útrunnið fyrst út

Ef valið er velja  **samkvæmt FEFO**  gátreitnum á  **flipanum Afhendingarskilmálar**  á  **síðunni Birgðageymsluspjald**  eru atriði sem eru rakin í vörunni valin á þeim stað samkvæmt gildistíma þeirra. Vörur með elstu lokadagsetningar eru tíndar fyrst.  

Vöruhúsaaðgerðum í öllum tínslu-og hreyfingarskjölum er raðað samkvæmt FEFO, nema vörunum séu tengdar rað-eða lotunúmerum. Ef sumu, en ekki öllu, magninu í línunni eru með raðnúmerum eða lotunúmerum er eftirstandandi magni raðað samkvæmt FEFO.  

Þegar tekið er af FEFO verða vörur sem renna fyrst saman í tímabundinn vörurakningarlista byggða á lokadagsetningu. Ef tvær vörur hafa sama gildistíma er varan með lægsta lotu eða raðnúmer tekin fyrst. Ef lotu-eða raðnúmer eru þau sömu er varan sem var skráð fyrst valin fyrst. Staðlaðar afmarkanir til að velja vörur í tínsluhólfum, svo sem flokkun hólfs og Break-magn, eru jöfnuð við listann tímabundin FEFO-Vörurakning.  

#### Frágangssniðmát

Sniðmát frágangs tilgreina safn forgangsreglna sem eiga við þegar frágangur er stofnaður. Til dæmis getur frágangssniðmát krafist þess að vörur séu settar í hólf með hólfainnihaldi sem hefur sama UOM. Ef ekki finnst nægilegt hólf fyrir sams konar afkastagetu verður að setja vöruna í tómt hólf. Sniðmáti er úthlutað til frágangs á vöru og staðsetningu.  

## Sjá tengda [Microsoft þjálfun](/training/modules/get-started-warehouse-management/)

## Sjá einnig .

[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]