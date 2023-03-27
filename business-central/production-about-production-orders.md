---
title: Um framleiðslupantanir
description: Kynntu þér hvernig framleiðslupantanir virka og hvernig þær eru notaðar til að sjá um umbreytingu keypts efnis yfir í framleiddar vörur.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '99000813, 99000814, 99000815, 99000816, 99000829, 99000830, 99000831, 99000832, 99000833, 99000838, 99000839, 99000867, 99000868, 99000882, 99000897, 99000898, 99000900, 99000912, 99000913, 99000914, 99000917'
ms.date: 06/22/2021
ms.author: edupont
---
# Um framleiðslupantanir

Framleiðslupantanir eru notaðar til að sjá um umbreytingu keypts efnis yfir í framleiddar vörur. Framleiðslupantanir leiða verk í gegnum ýmsar vinnu- eða vélastöðvar í vinnusalnum.  

Áður en haldið er áfram með framleiðslu framkvæma flesti fyrirtæki framboðsáætlun, vanalega einu sinni í viku, til að reikna út hversu margar framleiðslupantanir og innkaupapantanir eigi að framkvæma til að uppfylla sölueftirspurn þeirrar viku. Innkaupapantanir uppfylla íhlutina sem eru nauðsynlegir samkvæmt framleiðsluuppskriftinni til að framleiða endanlegar vörur.

Framleiðslupantanir eru lykilhlutar framleiðsluvirkni forritsins og þær innihalda eftirfarandi upplýsingar:  

- Vörur sem áætlað er að framleiða  
- Efni sem nauðsynlegt er fyrir áætlaðar framleiðslupantanir.  
- Vörur sem búið er að framleiða  
- Efni sem er þegar búið að velja  
- Vörur sem hafa verið framleiddar í gegnum tíðina  
- Efni sem var notað í fyrri framleiðsluaðgerðum  

Framleiðslupantanir eru upphafspunktar fyrir:  

- Áætlun framleiðslu í framtíðinni  
- Stjórnun núverandi framleiðslu  
- Rakningu tilbúinnar framleiðslu  

## Stofnun framleiðslupantana  
Hægt er að stofna framleiðslupantanir á grundvellinum pöntun-fyrir-pöntun handvirkt á síðunni **Framleiðslupöntun** eða mynda þær í gluggunum **Sölupöntun Áætlun** eða **Pöntunaráætlun**. Síðan **Áætlunarblað** er notuð til að gera margar pantanir.  

Framleiðslupantanir eru stofnaðar eftir upplýsingum frá:  

- Birgðir  
- Framl.uppskriftir
- Leið  
- Vélastöðvum  
- Vinnustöðvum  

## Takmarkanir á stofnun Framleiðslupantana  
Framleiðslupantanir eru sjálfkrafa teknar frá og raktar aftur til uppruna síns þegar:  

- Þær eru stofnaðar á **[Áætlunarvinnublaðinu](production-how-to-run-mps-and-mrp.md)**.  
- Stofnaðar á síðunni **[Áætlun sölupöntunar](production-how-to-create-production-orders-from-sales-orders.md)**  
- Stofnaðar á síðunni **[Pantanaáætlun](production-how-to-plan-for-new-demand.md)**  
- Nota aðgerðina **[Enduráætla](production-how-to-replan-refresh-production-orders.md)** á framleiðslupantanir  

Frekari upplýsingar eru í [Rekja tengsl á milli framboðs og eftirspurnar](production-how-track-demand-supply.md).

Framleiðslupantanir sem eru stofnaðar eftir öðrum leiðum eru ekki sjálfkrafa teknar frá og raktar.   

## Staða framleiðslupöntunar  
Staða framleiðslupöntunar stýrir því hvernig framleiðslupöntunin hagar sér innan forritsins. Form og innihald framleiðslunnar ráðast af stöðu pöntunarinnar. Framleiðslupantanirnar eru birtar á ólíkum síðum eftir því hver staða þeirra er. Ekki er hægt að breyta stöðu framleiðslupöntunar handvirkt; nota þarf aðgerðina **Breyta stöðu** í einstaka framleiðslupöntunum eða í glugganum **Breyta stöðu framleiðslupöntunar**.  

### Hermd framleiðslupöntun  
Hermda framleiðslupöntunin er einstök hvað varðar eftirfarandi eiginleika:  

- Eins og nafnið gefur til kynna er hún hermir og megintilgangur hennar hefur með tilboð og kostnað að gera - eins og þegar rannsóknar- og þróunardeildin vill fá kostnaðaráætlun fyrir vöru sem er lögð til. Hermd framleiðslupöntun er notuð sem dæmi um framleiðslupöntun.  
- Hún hefur ekki áhrif á áætlanir með pantanir. Áætlun (MPS og MRP) tekur ekki tillit til hermdra framleiðslupantana og verður ekki fyrir áhrifum af þeim. Einnig er ekki hægt að nota hermda framleiðslupöntun sem sniðmát af því að hún hverfur þegar stöðu hennar er breytt.  

### Áætluð framleiðslupöntun  
Áætlaða framleiðslupöntunin er einstök út af eftirfarandi eiginleikum:  

- Hægt er að gera áætlaða framleiðslupöntun sjálfvirkt eftir sölupöntun.  
- Áætlaðar framleiðslupantanir eru eins og útgefnar framleiðslupantanir og veita ílag til áætlunar afkastaþarfa með því að birta afkastaþarfirnar í heild sinni eftir vinnustöð eða vélastöð.  
- Áætluð framleiðslupöntun er besta mat á framtíðarálagi fyrir álag vinnustöðvarinnar eða vélastöðvarinnar á grundvelli upplýsinga sem eru fyrir hendi. Yfirleitt eru þær myndaðar úr áætlun en líka er hægt að stofna þær handvirkt. Ekki er hentugt að stofna þær handvirkt af því að þeim er eytt í næstu stofnun áætlana.  
- Stofnun þeirra í áætlananiðurstöðum í tillagðri "áætlaðri útgáfu pantana" sem felur í sér magn, útgáfudagsetningu og skiladagsetningu. Grunnur áætlunarkerfisins er byggður á endurnýjunarkerfinu, endurpöntunarstefnunni, og pöntunarbreytum sem hann finnur í áætlunarferli nettóþarfa.  
- Skoða ber álagið fyrir hverja vinnustöð eða vélastöð á leið áætluðu framleiðslupöntunarinnar til að skoða áhrif þeirra.  

### Fastáætluð framleiðslupöntun  
Fastáætlaða framleiðslupöntunin er einstök út af eftirfarandi eiginleikum:  

- Hægt er að stofna fastáætlaða framleiðslupöntun sjálfvirkt eftir sölupöntun.  
- Fastáætluð framleiðslupöntun þjónar sem leppur áætlun fyrir verk sem verður gefið út í framtíðinni.  
- Fastáætlaða framleiðslupöntun er hægt að mynda úr áætlun eða stofna handvirkt eða úr sölupöntunum. Þær eru ekki strokaðar út í áætlunum sem koma á eftir.  
- Stonfun þeirra í áætlananiðurstöðum í tillagðri "áætlaðri útgáfu pantana" sem felur í sér magn, útgáfudagsetningu og skiladagsetningu. Grunnur áætlunarkerfisins er byggður á endurnýjunarkerfinu, endurpöntunarstefnunni, og pöntunarbreytum sem hann finnur í áætlunarferli nettóþarfa.  
- Skoða ber álagið fyrir hverja vinnustöð eða vélastöð á leið fastáætluðu framleiðslupöntunarinnar til að skoða áhrif þeirra.  

### Útgefin framleiðslupöntun  
Útgefna framleiðslupöntunin er einstök hvað varðar eftirfarandi eiginleika:  

- Hægt er að gera útgefna framleiðslupöntun sjálfvirkt eftir sölupöntun.  
- Þegar búið er að gefa út framleiðslupöntun þýðir það ekki endilega að búið sé að velja efnið eða að verkið hafi verið í raun fært til fyrstu aðgerðar sinnar.  
- Í MTO (gert eftir pöntun)-umhverfi er ekki óvanalegt að útgefin framleiðslupöntun sé stofnuð beint eftir að sölupöntunin hefur verið færð inn.  
- Raunveruleg efnisnotkun og vöruílag er hægt að færa handvirkt inn með útgefinni framleiðslupöntun. Þar að auki er sjálfvirk birgðaskráning notkunar og vöru aðeins notuð fyrir útgefnar framleiðslupantanir.  

### Fullunnin framleiðslupöntun  
Fullunna framleiðslupöntunin er einstök hvað varðar eftirfarandi eiginleika:  

- Fullunnin framleiðslupöntun er yfirleitt pöntun sem er búið að framleiða.  
- Það er mikilvægur þáttur í að ljúka kostnaðarferli þeirrar vöru sem verið er að framleiða að fullvinna framleiðslupöntunina. Með því að fullvinna framleiðslupöntun er hægt að leiðrétta kostnað og stemma hann af.  
- Fullunnar framleiðslupantanir eru notaðar til tölfræðilegrar skýrslugerðar og til að styðja þann eiginleika að geta rakið aftur til annarra pantana (sölu-, framleiðslu- og innkaupa- til dæmis). Það að geta rakið aftur til fullunninnar framleiðslupöntunar gerir það mögulegt að sjá söguna í heild sinni.  
- Aldrei er hægt að breyta afgreiddum framleiðslupöntunum.  

## Framkvæmd framleiðslupantana  
Þegar búið er að stofna framleiðslupöntun og tímasetja hana þarf að gefa hana út í vinnusalinn til að láta framkvæma hana. Á meðan á framkvæmd pöntunarinnar stendur er fært inn:  

- Efni sem hefur verið valið eða notað  
- Hversu miklum tíma var varið í vinnslu pöntunarinnar  
- Magn yfirvörunnar sem var framleidd  

Hægt er að færa þessar upplýsingar handvirkt inn eða í gegnum sjálfvirka skýrslugerð, samkvæmt vörunum sem uppsettar eru í reitnum Birgðaskráningaaðferð í vöru og vinnustöð.  

### Efnisnotkun  
Forritið býður framleiðslufyrirtæki upp á marga valkosti til að færa inn efnisnotkun. Til dæmis er hægt að skrá efnisnotkun handvirkt, sem gæti hentað ef stöðugt er verið að skipta um íhluti eða ef meira er af úrtaki en búist var við.  

Hægt er að vinna efnisnotkun í gegnum [notkunarbókina](production-how-to-post-consumption.md) en einnig er hægt að skrá hana sjálfvirkt í forritinu, það heitir sjálfvirk skýrslugerð (losun). Skýrslugerðaraðferðirnar eru:  

- Handvirk  
- Framvirk  
- Afturvirkt  

Handvirk notkunarskýrsla notar Notkunarbókina til að tilgreina efnisval.  

Framvirk notkunarskýrsla gerir ráð fyrir því að búið sé að nota sjálfkrafa væntanlegt magn alls efnisins í allri pöntuninni við útgáfu framleiðslupöntunarinnar, nema leiðartengilskótar séu notaðir. Þegar leiðartengilskótar eru notaðir er efnið sem notað er eftir að upphaf aðgerðarskrefsins skráð í frálagsbókina. Til að birgðaskrá alla framleiðslupöntunina framvirkt þarf að gera tvennt:  

- Velja þarf framvirka birgðaskráningu á birgðaspjaldi hverrar vöru í uppskrift efsta stigs framleiðslu.  
- Fjarlægja þarf alla leiðartengilskóta úr framleiðsluuppskriftinni.  

Afturvirk notkunarskýrsla skráir raunverulegt magn alls efnis sem er valið eða notað þegar stöðu framleiðslupöntunar er breytt í *Lokið* nema leiðartengilskótar séu notaðir. Þegar leiðartengilskótar eru notaðir er efnið notað eftir að magn yfirvörunnar er skráð fyrir aðgerðarskrefið í Frálagsbókinni.  

Þegar Framleiðslupöntunin er endurnýjuð er birgðaskráningaraðferðin afrituð af birgðaspjaldinu. Þar sem birgðaskráningaraðferðin fyrir hvern íhlut framleiðslupöntunar stýrir því hvernig og hvenær notkunin er færð inn er mikilvægt að athuga að hægt er að breyta birgðaskráningaraðferð fyrir tilteknar vörur beint á Framleiðslupöntuninni. 

Nánari upplýsingar eru í [Birgðaskrá íhluti samkvæmt frálagi aðgerða](production-how-to-flush-components-according-to-operation-output.md)

### Framleiðslufrálag  
Forritið veitir þann möguleika að rekja það hversu miklum tíma er eytt í að vinna með framleiðslupöntun, og að skrá magn þess sem er framleitt. Þessar upplýsingar geta hjálpað þér við að meta á nákvæmari hátt kostnað framleiðslunnar. Framleiðendur sem nota staðlað kerfi við útreikning kostnaðar gætu líka viljað skrá raunverulegar upplýsingar til að gera sér kleift að þróa betri staðla.  

Hægt er að vinna frálag í gegnum [frálagsbókina](production-how-to-post-output-quantity.md) en forritið getur líka skráð það sjálfvirkt. Forritið afritar birgðaskráningaraðferðina frá spjaldi Vélastöðvarinnar eða Vinnustöðvarinnar yfir á Framleiðslupöntunarleiðina þegar það endurnýjar. Eins og með efnisnotkun eru þrjár skýrslugerðaraðferðir fyrir frálag:  

- Handvirk  
- Framvirk  
- Afturvirk  

Handvirk aðferð notar Frálagsbókina til að tilgreina þann tíma sem er notaður og það magn sem er framleitt.  

Framvirk aðferð skráir frálagið (og tímann) sem búist er við, sem er skráð sjálfvirkt við útgáfu Framleiðslupöntunar. Leiðartengilskótar eru ekki þáttur í framvirkri birgðaskráningu frálagsins.  

Afturvirkt aðferð skráir áætlaða frálagið (og tímann) sem er skráð sjálfvirkt við lok gerðar Framleiðslupöntunar. Leiðartengilskótar eru ekki þáttur í afturvirkri birgðaskráningu frálagsins.  

### Notkun og Frálag bókuð  
Hægt er að nota hvaða samblöndu sem er af sjálfvirkri birgðaskráningu og handvirkt skráðum upplýsingum fyrir bæði notkun og frálag. Til dæmis gæti verið óskað þess að birgðaskrá íhluti framvirkt sjálfkrafa en nota samt Notkunarbókina til að skrá úrkast. Á svipaðan hátt gæti þess verið óskað að skrá frálag sjálfvirkt en nota Frálagsbókina til að skrá úrkast yfirvörunnar eða aukatíma sem eytt er í pöntunina.  

Að lokum þarf að ákvarða þá röð sem skrá á upplýsingarnar í ef notkun og frálag er fært inn handvirkt. Hægt er að skrá notkun fyrst og nota svo flýtiaðferð til að færa inn upplýsingarnar, sem eru byggðar á áætluðu frálagsmagni. Eða þá að frálag er fært inn fyrst með aðgerðinni **opna leið**. Notkun yrði þá skráð á grundvelli raunverulegs frálagsmagns.  

### Framleiðslubók  
[Framleiðslubókin](production-how-to-register-consumption-and-output.md) sameinar aðgerðir Notkunarbókarinnar og Frálagsbókarinnar inn í eina bók sem farið er í beint úr útgefnu framleiðslupöntuninni.  

Tilgangurinn með Framleiðslubókinni er að útvega eitt viðmót til að skrá notkun og frálag frá Framleiðslupöntun.  

Notkunarbókin er með einfalt útlit og veitir möguleika á að:  

- Skrá frálag og notkun tengda Framleiðslupöntun á einfaldan hátt  
- Tengja íhlutina við aðgerðir  
- Tengja raunveruleg aðgerðagögn við stöðluðu áætlanirnar um framleiðslupöntunarleiðina og íhlutalínurnar  
- Bóka og prenta út lýsingu á skráðum aðgerðagögnum fyrir framleiðslupöntunina  

Framleiðslubókin framkvæmir margar af sömu aðgerðum og Notkunar- og frálagsbækurnar. Víddir, Vörurakning og Innihald hólfs eru meðhöndlaðar á sama hátt og í Notkunar- og Frálagsbókunum.  

Hins vegar er Framleiðslubókin frábrugðin Notkunar- og Frálagsbókunum að eftirfarandi leyti:  

- Hún er framkölluð beint frá línu útgefinnar framleiðslupöntunar og forstillt með viðeigandi gögnum.  
- Það gerir það mögulegt að skilgreina hvaða tegundir af íhlutum á að meðhöndla á grundvelli afmörkunar birgðaskráningaraðferðar í bókinni.  
- Magn og tími sem þegar er búið að bóka fyrir pöntunina eru birt neðst í bókinni sem raunverulegar færslur.  
- Reitir þar sem gagnafærsla skiptir ekki máli eru auðir og óbreytanlegir.  
- Notandinn getur stillt hvernig frálagsmagn er forstillt í færslubókinni &amp;#8211 - til dæmis að síðasta aðgerðin verði að hafa Frálagsmagnið núll.  
- Ef notandinn skyldi hætta í færslubókinni án þess að bóka breytingarnar birtast skilaboð sem gera notandanum kleift að vera áfram í færslubókinni.  
- Hún birtir aðgerðir og íhluti saman í rökrænu skipulagi sem veitir yfirlit yfir framleiðsluferlið:  

Í Framleiðslubókinni er Notkunarmagn bókað sem neikvæðar Færslur í birgðafærslum, Frálagsmagn er bókað sem jákvæðar birgðafærslur og tími sem varið er er bókaður sem afkastagetufærslur.  

## Sjá einnig
[Framleiðsla](production-manage-manufacturing.md)
[Uppsetning framleiðslu](production-configure-production-processes.md)  
[Áætlun](production-planning.md)  
[Birgðir](inventory-manage-inventory.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
