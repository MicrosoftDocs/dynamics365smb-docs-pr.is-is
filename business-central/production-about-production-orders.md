---
title: Um framleiðslupantanir
description: Fræðast um framleiðslupantanir og hvernig þær eru notaðar til að sjá um umbreytingu keypts efnis yfir í framleiddar vörur.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '99000813, 99000814, 99000815, 99000816, 99000829, 99000830, 99000831, 99000832, 99000833, 99000838, 99000839, 99000867, 99000868, 99000882, 99000897, 99000898, 99000900, 99000912, 99000913, 99000914, 99000917'
ms.date: 08/09/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Um framleiðslupantanir

Framleiðslupantanir eru notaðar til að sjá um umbreytingu keypts efnis yfir í framleiddar vörur. Framleiðslupantanir leiða verk í gegnum ýmsar vinnu- eða vélastöðvar í vinnusalnum.  

Áður en þeir vinna með framleiðslu framkvæmir flest fyrirtæki framboðsáætlun, yfirleitt einu sinni í viku, til að reikna út hversu margar framleiðslupantanir og innkaupapantanir ættu að framkvæma til að uppfylla sölueftirspurn þeirrar viku. Innkaupapantanir uppfylla íhlutina sem eru nauðsynlegir samkvæmt framleiðsluuppskriftinni til að framleiða endanlegar vörur.

Framleiðslupantanir eru miðlægir íhlutir framleiðsluaðgerða og þær innihalda eftirfarandi upplýsingar:  

- Vörur sem áætlað er að framleiða  
- Efni sem nauðsynlegt er fyrir áætlaðar framleiðslupantanir.  
- Vörur sem búið er að framleiða  
- Efni sem þegar er búið að velja  
- Vörur sem voru framleiddar áður  
- Efni sem var notað í fyrri framleiðsluaðgerðum  

Framleiðslupantanir eru upphafspunktar fyrir:  

- Áætlun framleiðslu í framtíðinni  
- Stjórnun núverandi framleiðslu  
- Rakningu tilbúinnar framleiðslu  

## Stofnun framleiðslupöntunar  

Hægt er að búa til framleiðslupantanir á grundvellinum pöntun-fyrir-pöntun handvirkt á síðunni **Framleiðslupöntun** eða búa þær til af síðunum **Sölupöntun áætlun** eða **Pantanaáætlun** . Einnig er hægt að stofna margar pantanir eru stofnaðar af síðunni **Áætlunarvinnublað** .  

Framleiðslupantanir eru stofnaðar með upplýsingum úr:  

- Vörur  
- Framl.uppskriftir
- Leiðir  
- Vélastöðvum  
- Vinnustöðvum  

## Takmarkanir á stofnun framleiðslupantana  

Framleiðslupantanir eru sjálfkrafa teknar frá og raktar aftur til uppruna síns þegar:  

- Stofnað út frá [áætlunarvinnublaðinu](production-how-to-run-mps-and-mrp.md)  
- Stofnað af síðunni [Áætlun](production-how-to-create-production-orders-from-sales-orders.md) sölupöntunar  
- Stofnað af síðunni [Pantanaáætlun](production-how-to-plan-for-new-demand.md)   
- Aðgerðin [Enduráætla](production-how-to-replan-refresh-production-orders.md) á framleiðslupantanir notuð  

Frekari upplýsingar eru í [Rekja tengsl á milli framboðs og eftirspurnar](production-how-track-demand-supply.md).

Framleiðslupantanir sem stofnaðar eru með öðrum leiðum eru ekki sjálfkrafa teknar frá og raktar.

## Staða framleiðslupöntunar  

Staða framleiðslupöntunar stýrir því hvernig framleiðslupöntunin hagar sér innan forritsins. Staða pöntunarinnar segir til um form og innihald framleiðslunnar. Framleiðslupantanirnar eru birtar á ólíkum síðum eftir því hver staða þeirra er. Ekki er hægt að breyta stöðu framleiðslupöntunar handvirkt. Nota verður aðgerðina **Breyta stöðu** í einstakri framleiðslupöntun eða á síðunni **Breyta stöðu** framl.pöntunar.  

### Hermd framleiðslupöntun  

Hermd framleiðslupöntun er einstök, byggð á eftirfarandi eiginleikum:  

- Eins og nafnið gefur tilefni til er hægt að nota eftir tilboðum og kostnaði. Til dæmis þegar rannsóknar- og þróunardeildin vill fá kostnaðaráætlun fyrir vöru sem lögð er til. Hermd framleiðslupöntun er notuð sem dæmi um framleiðslupöntun.  
- Þau hafa ekki áhrif á skipulagningu pantana. Áætlun (MPS og MRP) hefur ekki áhrif á hermdar framleiðslupantanir. Einnig er ekki hægt að nota hermda framleiðslupöntun sem sniðmát vegna þess að hún hverfur þegar stöðu hennar er breytt.  

### Áætluð framleiðslupöntun  

Áætluð framleiðslupöntun er einstök vegna eftirfarandi eiginleika:  

- Hægt er að gera áætlaða framleiðslupöntun sjálfvirkt eftir sölupöntun.  
- Áætlaðar framleiðslupantanir eru eins og útgefnar framleiðslupantanir og veita ílag til áætlunar afkastaþarfa með því að birta afkastaþarfirnar í heild sinni eftir vinnustöð eða vélastöð.  
- Áætluð framleiðslupöntun er besta mat á framtíðarálagi fyrir álag vinnustöðvarinnar eða vélastöðvarinnar á grundvelli upplýsinga sem eru fyrir hendi. Yfirleitt eru þær myndaðar úr áætlun en einnig er hægt að stofna þær handvirkt. Þar sem þeim er eytt í næstu stofnun áætlunar er ekki hentugt að stofna handvirka stofnun.  
- Stofnun þeirra í áætlananiðurstöðum í tillagðri "áætlaðri útgáfu pantana" sem felur í sér magn, útgáfudagsetningu og skiladagsetningu. Grunnur áætlunarkerfisins er byggður á endurnýjunarkerfinu, endurpöntunarstefnunni, og pöntunarbreytum sem hann finnur í áætlunarferli nettóþarfa.  
- Skoða má álagið fyrir hverja vinnustöð eða vélastöð á leið áætluðu framleiðslupöntunarinnar til að skoða áhrif þeirra.  

### Fastáætluð framleiðslupöntun  

Fastáætluð framleiðslupöntun er einstök vegna eftirfarandi eiginleika:  

- Hægt er að stofna fastáætlaða framleiðslupöntun sjálfvirkt eftir sölupöntun.  
- Fastáætluð framleiðslupöntun er föst í áætlunaráætlun fyrir verkefni sem gefið er út í framtíðinni.  
- Fastáætlaða framleiðslupöntun er hægt að mynda úr áætlun eða stofna handvirkt eða úr sölupöntunum. Þær eru ekki strokaðar út í áætlunum sem á eftir kemur.  
- Stonfun þeirra í áætlananiðurstöðum í tillagðri "áætlaðri útgáfu pantana" sem felur í sér magn, útgáfudagsetningu og skiladagsetningu. Grunnur áætlunarkerfisins er byggður á endurnýjunarkerfinu, endurpöntunarstefnunni, og pöntunarbreytum sem hann finnur í áætlunarferli nettóþarfa.  
- Skoða má álagið fyrir hverja vinnustöð eða vélastöð á leið fastáætluðu framleiðslupöntunarinnar til að skoða áhrif þeirra.  

### Útgefin framleiðslupöntun  

Útgefna framleiðslupöntunin er einstök samkvæmt eftirfarandi eiginleikum:  

- Hægt er að gera útgefna framleiðslupöntun sjálfvirkt eftir sölupöntun.  
- Þegar framleiðslupöntun er gefin út þýðir það ekki endilega að efni sé tínt eða efnislega fært í fyrstu vinnsluaðgerðina.  
- Í umhverfi sem býr til eftir pöntun (MTO) er ekki óvanalegt að stofna útgefna framleiðslupöntun strax eftir færslu sölupöntunarinnar.  
- Raunveruleg efnisnotkun og vöruílag er hægt að færa handvirkt inn með útgefinni framleiðslupöntun. Þar að auki er sjálfvirk birgðaskráning notkunar og vöru aðeins notuð fyrir útgefnar framleiðslupantanir.  

### Afgreidd framleiðslupöntun  

Fullunnin framleiðslupöntun er einstök samkvæmt eftirfarandi eiginleikum:  

- Fullunnin framleiðslupöntun er gjarnan framleidd.  
- Það er mikilvægur þáttur í að ljúka kostnaðarferli þeirrar vöru sem verið er að framleiða að fullvinna framleiðslupöntunina. Þegar framleiðslupöntun hefur verið lokið er hægt að stilla og stemma af kostnað.  
- Fullunnar framleiðslupantanir eru notaðar til tölfræðilegrar skýrslugerðar og til að styðja þann eiginleika að geta rakið aftur til annarra pantana (sölu-, framleiðslu- og innkaupa- til dæmis). Það að geta rakið aftur til fullunninnar framleiðslupöntunar gerir það mögulegt að sjá söguna í heild sinni.  
- Aldrei er hægt að breyta afgreiddum framleiðslupöntunum.  

## Framkvæmd framleiðslupöntunar  

Þegar búið er að stofna og tímasetja framleiðslupöntun verður að gefa hana út í vinnusalinn til að framkvæma hana. Á meðan á framkvæmd pöntunarinnar stendur er fært inn:  

- Efnið sem var tínt eða notað  
- Hversu miklum tíma var varið í vinnslu pöntunarinnar  
- Magn vörunnar yfireining framleiddra vara  

Hægt er að skrá þessar upplýsingar handvirkt eða með sjálfvirkri skýrslugerð. Aðferðin fer eftir uppsetningunni í reitnum Birgðaskráningaraðferð á vörunni og vinnustöðinni.  

### Efnisnotkun  

[!INCLUDE [prod_short](includes/prod_short.md)] býður upp á ýmsa valkosti til að skrá efnisnotkun. Til dæmis er hægt að skrá efnisnotkun handvirkt, sem gæti hentað ef til eru tíðar skiptingar á íhlutum eða hærri en búist var við.  

Hægt er að vinna efnisnotkun í [gegnum notkunarbókina](production-how-to-post-consumption.md), en einnig er hægt að skrá hana sjálfvirkt með [!INCLUDE [prod_short](includes/prod_short.md)] því að kallast sjálfvirk skýrslugerð (birgðaskráning). Skýrslugerðaraðferðirnar Handvirk, Framvirk og Afturvirk eru tiltækar.

Handvirk notkunarskýrsla notar Notkunarbókina til að tilgreina efnisval.  

Framvirk notkunarskýrsla gerir ráð fyrir því að búið sé að nota sjálfkrafa væntanlegt magn alls efnisins í allri pöntuninni við útgáfu framleiðslupöntunarinnar, nema leiðartengilskótar séu notaðir. Þegar leiðar-tengja kótar eru notaðir er efnið sem notað er eftir upphaf aðgerðarskrefsins skráð í frálagsbókina. Til að birgðaskrá alla framleiðslupöntunina framvirkt þarf að gera tvennt:  

- Velja þarf framvirka birgðaskráningu á birgðaspjaldi hverrar vöru í uppskrift efsta stigs framleiðslu.  
- Fjarlægja þarf alla leiðartengilskóta úr framleiðsluuppskriftinni.  

Afturvirk notkunarskýrsla skráir raunverulegt magn alls efnis sem er valið eða notað þegar stöðu framleiðslupöntunar er breytt í *Lokið* nema leiðartengilskótar séu notaðir. Þegar leiðar-tengja kótar eru notaðir er efnið notað eftir að magn vörunnar yfireining er skráð fyrir aðgerðarskrefið í frálagsbókinni.  

Þegar Framleiðslupöntunin er endurnýjuð er birgðaskráningaraðferðin afrituð af birgðaspjaldinu. Þar sem birgðaskráningaraðferðin fyrir hvern íhlut framleiðslupöntunar stýrir því hvernig og hvenær notkunin er skráð er mikilvægt að hafa í huga að hægt er að breyta birgðaskráningaraðferð fyrir tilteknar vörur beint á framleiðslupöntuninni. Nánari upplýsingar eru í [Birgðaskrá íhluti samkvæmt frálagi aðgerða](production-how-to-flush-components-according-to-operation-output.md).

### Framleiðslufrálag  

[!INCLUDE [prod_short](includes/prod_short.md)] gefur möguleika á að rekja það hversu miklum tíma er eytt í að vinna með framleiðslupöntun, auk þess að skrá það magn sem er framleitt. Þessar upplýsingar geta hjálpað þér við að meta á nákvæmari hátt kostnað framleiðslunnar. Framleiðendur sem nota staðlað kerfi kostnaðarútreiknings gætu líka viljað skrá raunverulegar upplýsingar til að auðvelda þeim að þróa betri staðla.  

Hægt er að vinna frálag í [gegnum frálagsbókina](production-how-to-post-output-quantity.md) en einnig er hægt að skrá það sjálfvirkt. [!INCLUDE [prod_short](includes/prod_short.md)] afritar birgðaskráningaraðferðina af véla- eða vinnustöðvarspjaldinu yfir á framleiðslupöntunarleiðina þegar hún er endurnýjuð. Eins og með efnisnotkun eru það Handvirk, Framvirk og Afturvirk skýrslugerð fyrir frálag.

Handvirk aðferð notar frálagsbókina til að tilgreina tímanotkun og magn sem er framleitt.  

Framvirka aðferðin skráir frálagið (og tímann) sem búist er við, sem er skráð sjálfvirkt við útgáfu framleiðslupöntunar. Leiðar- tengja kótar eru ekki þáttur í framvirkri birgðaskráningu frálagsins.  

Afturvirk aðferð skráir frálagið (og tímann) sem búist er við, sem er skráð sjálfvirkt við lok framleiðslupöntunar. Leiðar-tengja kótar eru ekki þáttur í afturvirkri birgðaskráningu frálagsins.  

### Bókun notkunar og frálags  

Hægt er að nota hvaða samblöndu sem er af sjálfvirkri birgðaskráningu og handvirkt skráðum upplýsingum fyrir bæði notkun og frálag. Til dæmis gæti þurft að birgðaskrá íhluti framvirkt sjálfvirkt en nota samt notkunarbók til að skrá úrkast. Á svipaðan hátt gæti þurft að skrá frálag sjálfvirkt en nota frálagsbók til að skrá úrkast yfireining vörunnar eða aukatíma sem eytt er í pöntunina.  

Að lokum þarf að ákvarða í hvaða röð ætlunin er að skrá þessar upplýsingar ef notkun og frálag er fært inn handvirkt. Hægt er að skrá notkun fyrst og nota svo flýtiaðferð til að færa inn upplýsingarnar, sem eru byggðar á áætluðu frálagsmagni. Eða þá að frálag er fært inn fyrst með aðgerðinni **opna leið**. Notkun yrði þá skráð á grundvelli raunverulegs frálagsmagns.  

### Framleiðslubók  

Framleiðslubókin [sameinar](production-how-to-register-consumption-and-output.md) aðgerðir notkunarbókar og frálagsbókar í eina færslubók sem er opnuð beint frá útgefnu framleiðslupöntuninni.  

Tilgangur framleiðslubókar er að bjóða upp á eitt viðmót til að skrá notkun og frálag úr framleiðslupöntun.  

Framleiðslubækur hafa einfalt yfirlit og veita möguleika á að:  

- Skrá frálag og notkun sem tengist framleiðslupöntun auðveldlega  
- Tengja íhlutina við aðgerðir  
- Tengja raunveruleg aðgerðagögn við staðlaðar áætlanir um leið framleiðslupöntunar og íhlutalínur  
- Bóka og prenta út yfirlit yfir skráð aðgerðagögn vegna framleiðslupöntunar  

Framleiðslubókin gerir margar af sömu aðgerðum og notkunar- og frálagsbækurnar. Víddir, vörurakning og hólfainnihald eru meðhöndluð á sama hátt.  

Hins vegar eru framleiðslubækur frábrugðnar notkunar- og frálagsbókum að eftirfarandi hætti:  

- Það er kallað beint úr útgefinni framleiðslupöntunarlínu og forstillt með viðeigandi gögnum.  
- Það gerir það mögulegt að skilgreina hvaða tegundir af íhlutum á að meðhöndla á grundvelli afmörkunar birgðaskráningaraðferðar í bókinni.  
- Magn og tími sem þegar er búið að bóka fyrir pöntunina eru birt neðst í bókinni sem raunverulegar færslur.  
- Reitir þar sem gagnafærsla á ekki við eru auðir og óafturkallanlegir.  
- Notandinn getur stillt hvernig frálagsmagn er forstillt í færslubókinni &#8211 - til dæmis að síðasta aðgerðin verði að hafa Frálagsmagnið núll.  
- Ef notandinn skyldi hætta í færslubókinni án þess að bóka breytingarnar birtast skilaboð sem gera notandanum kleift að vera áfram í færslubókinni.  
- Hún birtir aðgerðir og íhluti saman í rökrænu skipulagi sem veitir yfirlit yfir framleiðsluferlið:  

Í Framleiðslubókinni er Notkunarmagn bókað sem neikvæðar Færslur í birgðafærslum, Frálagsmagn er bókað sem jákvæðar birgðafærslur og tími sem varið er er bókaður sem afkastagetufærslur.  

## Sjá einnig .

[Framleiðsla](production-manage-manufacturing.md)
[Uppsetning framleiðslu](production-configure-production-processes.md)  
[Áætlun](production-planning.md)  
[Birgðir](inventory-manage-inventory.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
