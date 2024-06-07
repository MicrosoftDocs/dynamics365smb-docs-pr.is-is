---
title: Birgðaskráning íhluta eftir frálagi aðgerðar
description: Þessi grein lýsir því hvernig á að birgðaskrá íhluti samkvæmt frálagi aðgerðar og öðrum birgðaskráningaraðferðum sem tengjast.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 12/13/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# Birgðaskráning íhluta eftir frálagi aðgerðar
Hægt er að skilgreina mismunandi losunarleiðir til að gera skráningu á notkun íhluta sjálfvirka. 

Þessi aðgerð er gagnleg af eftirfarandi ástæðum:  

- **Verðmat birgða**

    Virðisfærslur fyrir frálag og notkun eru stofnaðar samhliða framleiðslupöntun í vinnslu. Án leiðartengilskóta hækkar birgðavirðið eftir því sem frálag er bókað og minnkar svo síðar þegar virði íhlutanotkunar er bókað ásamt afgreiddu framleiðslupöntuninni.  
- **Birgðir til ráðstöfunar**

    Með stöðugri notkunarbókun er betur uppfært hvort íhlutir eru til ráðstöfunar, sem er mikilvægt til að viðhalda innra jafnvægi á milli eftirspurnar og framboðs. Án leiðartengilskóta gæti önnur eftirspurn eftir íhlutnum trúað því að hann sé tiltækur svo lengi sem beðið er eftir seinkun á notkunarbókun.  
- **Rétt í tíma**

    Þegar hægt er að sérsníða vörur að beiðnum viðskiptamanna er hægt að lágmarka sóun með því að ganga úr skugga um að vinna og kerfisbreytingar eigi sér aðeins stað þegar þörf krefur.  

- **Draga úr gagnaskráningu**

    Þegar hægt er að birgðaskrá aðgerð sjálfvirkt er hægt að gera allt ferli skráningar notkunar og frálags sjálfvirkt. Ókosturinn við að nota sjálfvirka birgðaskráningu er að hugsanlega er ekki verið að skrá úrkastið rétt eða jafnvel meðvitað um úrkast.

## Sjálfvirk bókun notkunar (birgðaskráning)  

- Framvirk birgðaskráning allrar pöntunarinnar  
- Framvirk birgðaskráning eftir aðgerð  
- Bakskráning eftir aðgerð  
- Bakskráning allrar pöntunarinnar  

### Sjálfvirk skýrslugerð - Framvirk birgðaskráning allrar pöntunarinnar  
Ef framleiðslupöntunin er birgðaskráð framvirkt í upphafi verks er hegðun forritsins svipuð handvirkri notkun. Meginmunurinn er sá að notkunin gerist sjálfvirkt.  

- Allt innihald framleiðsluuppskriftarinnar er notað og dregið af birgðaskrá á þeirri stundu sem útgefna framleiðslupöntunin er endurnýjuð.  
- Notkunarmagnið er magnið fyrir hverja samsetningu sem kemur fram á framleiðsluuppskriftinni, margfaldað með fjölda þeirra yfirvara sem verið er að byggja.  
- Ekki þarf að skrá neinar upplýsingar í notkunarbókina ef birgðaskrá á allar vörurnar.  
- Þegar vörur eru notaðar úr birgðum skiptir ekki máli hvenær færslur eru færðar inn í frálagsbókina því frálagsbókin hefur engin áhrif á þennan máta notkunarbókunar.  
- Ekki er hægt að stilla neina leiðartengilskóta.  

Framvirk birgðaskráning heillar pöntunar hentar fyrir framleiðsluumhverfi með:  

-   Lítinn fjölda af göllum  
-   Lítinn fjölda af aðgerðum  
-   Mikla notkun íhluta í fyrstu aðgerðum  

### Sjálfvirk skýrslugerð - Framvirk birgðaskráning eftir aðgerð  
Birgðaskráning eftir aðgerð gerir það mögulegt að draga frá birgðum á meðan á tiltekinni aðgerð í leið yfirvörunnar stendur. Efni er tengt leiðinni með leiðartengilskótum sem samsvara þeim leiðartengilskótum sem eru notaðir fyrir íhluti í framleiðsluuppskriftinni.  

Birgðaskráningin á sér stað þegar aðgerðin sem hefur sama leiðartengilskóta er hafin. Hafin þýðir að einhver virkni er skráð í frálagsbókina fyrir þá aðgerð. Og sú virkni gæti verið einfaldlega það að uppsetningartími er færður inn.  

Magnið í birgðaskráningunni stendur fyrir magnið fyrir hverja samsetningu sem kemur fram á framleiðsluuppskriftinni margfaldað með fjölda þeirra yfirvara sem verið er að byggja (magn sem búist er við).  

Best er að beita þessari tækni þegar margar aðgerðir eru fyrir hendi og ekki er þörf á ákveðnum íhlutum fyrr en seint í samsetningarröðinni. Raunar gæti verið að Tímanleg (JIT) uppsetning sé ekki einu sinni með vörurnar tiltækar þegar ferlið er hafið.  

Hægt er að nota efni á meðan á aðgerðum stendur með því að nota leiðartengilskóta. Suma íhluti er ekki hægt að nota fyrr en í lokasamsetningaraðgerðum og ekki ætti að taka þá úr birgðum fyrr en á þeim tíma.  

### Sjálfvirk skýrslugerð - Bakskráning eftir aðgerð  
Bakskráning eftir aðgerð skráir notkun eftir að aðgerðin er bókuð í frálagsbókina.  

Kosturinn við þessa aðferð er að fjöldi þeirra aðalhluta sem búið er að nota í aðgerðinni er þekktur.  

Efni í framleiðsluuppskriftinni er tengt við leiðarfærslurnar með leiðartengilskótum. Bakskráningin á sér stað þegar aðgerð með tiltekinn leiðartengilskóti er bókaður með afgreiddu magni.  

Magnið í birgðaskráningunni stendur fyrir magnið fyrir hverja samsetningu sem kemur fram á framleiðsluuppskriftinni margfaldað með fjölda þeirra yfirvara sem voru bókaðar sem frálagsmagn í þeirri aðgerð. Þetta gæti verið frábrugðið því magni sem búist var við.  

### Sjálfvirk skýrslugerð - Bakskráning allrar pöntunarinnar  
Þessi skýrslugerðaraðferð tekur ekki tillit til leiðartengilskóta.  

Engir íhlutir eru valdir þar til stöðu útgefnu framleiðslupöntunarinnar er breytt í *Lokið*. Magnið í birgðaskráningunni er það magn fyrir hverja samsetningu sem kemur fram á framleiðsluuppskriftinni margfaldað með þeim fjölda yfirvara sem voru fullunnar og settar í birgðir.  

Afturvirk birgðaskráning á allri framleiðslupöntuninni krefst sömu uppsetningar og fyrir framvirka söfnun: Skýrslugerðaraðferðin þarf að vera stillt á afturvirkt á hverju birgðaspjaldi til þess að allar vörur innan yfiruppskriftarinnar verði skráðar. Þar að auki þarf að fjarlægja alla leiðartengilskóta úr framleiðsluuppskriftinni. 



Til dæmis ef framleiðslupöntun um að framleiða 800 metra krefst 8 kg af íhlut, og ef 200 metrar eru bókaðir sem frálag, bókast 2 kg sjálfkrafa sem notkun. Þessu er hægt að ná með því að sameina afturvirka losunaraðferð og kóða leiðartengla þannig að magnið sem er losað fyrir hverja aðgerð er í hlutfalli við raunverulegt frálag lokinnar aðgerðar. Fyrir vörur sem hafa verið settar upp með afturvirkri birgðaskráningu er sjálfgefin virkni að reikna út og bóka notkun íhluta þegar stöðu útgefinnar framleiðslupöntunar er breytt í **Lokið**. Ef einnig eru skilgreindir leiðartengilskótar, þá gerist útreikningur og bókun þegar hverri aðgerð er lokið og magnið sem var notað í aðgerðinni er bókað. Nánari upplýsingar eru í [Stofna leiðir](production-how-to-create-routings.md).  

## Til að birgðaskrá íhluti samkvæmt frálagi aðgerðar

1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur** og velja síðan viðkomandi tengil.  
2.  Veldu aðgerðina **Breyta**.  
3.  Á flýtiflipanum **Áfylling**, í reitnum **Birgðaskráningaraðferð**, skal velja **Afturvirkt**.  

    > [!NOTE]  
    >  Veljið **Tínsla + Bakka** ef íhluturinn er notaður í birgðageymslu sem er sett upp fyrir beinan frágang og tínslu.  

4.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Leiðir** og velja síðan viðkomandi tengil.  
5.  Skilgreina leiðartengilskóða fyrir hverja aðgerð sem notar íhlutinn. Nánari upplýsingar eru í [Stofna leiðir ](production-how-to-create-routings.md).  
    > [!IMPORTANT]  
    > Ekki skal nota sama leiðartengil fyrir mismunandi aðgerðir í leiðinni, þar sem það mun leiða til skráningar á notkun íhluta fyrir hverja tengda aðgerð.  
6.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Framleiðsluuppskrift** og velja síðan viðkomandi tengil.  
7.  Skilgreina leiðartengilskóta úr hverju íhlutstilviki við aðgerðina þar sem hann er notaður.

Notkunin bókast sjálfkrafa þegar frálag er skráð. Frekari upplýsingar, sjá [Fjöldabóka frálag og keyrslutíma](production-how-to-post-output-quantity.md)

## Flæðiaðferðir

Eftirfarandi tafla lýsir tiltækri losunaraðferð sem hægt er að tilgreina í spjaldinu **Vara** og spjaldinu **Birgðahaldseining**.

|Valkostur|Description|
|------------|-------------|  
|Handvirk|Krefst þess að notkun sé handskráð og bókuð í notkunarbók.|
|Framvirk|Bókar sjálfvirkt notkun samkvæmt íhlutalínum framleiðslupöntunar. <br><br>Sjálfgefið er að útreikningur og bókun íhlutanotkunar eigi sér stað þegar stöðu útgefinnar framleiðslupöntunar er breytt í **Útgefin**. Ef reiturinn **Leiðartengilskóði** er notaður í íhlutalínum framleiðslupöntunar verður bókað fyrir hverja aðgerð þegar aðgerðir hefjast. Frekari upplýsingar, sjá [Hvernig skal: Stofna leiðartengla](production-how-to-create-routings.md#to-create-routing-links). <br><br> **Ábending**<br>Fyrir framvirka birgðaskráningu, byggist bókunin fyrir tiltekið verk sem notandinn fær með leiðartengilskóða á magni sem er skilgreint í íhlutalínunni. Upplýsingar um birgðaskráningu sem er sértæk fyrir aðgerð byggða á raunverulegu frálagi eru í lýsingunni **Afturvirk** í þessari grein.<br><br>Ef birgðageymslan eða forði þar sem þessi íhlutur er notaður eru sett upp með sjálfgefnu hólfaskipulagi verður varan notuð úr **Opna hólfkóða vinnslusalar**. Frekari upplýsingar, sjá [Hvernig á að: setja upp einfaldar vöruhúsaaðgerðir með aðgerðasvæði](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md). <br><br> **Mikilvægt** <br>Framvirk birgðaskráning á sér einnig stað þegar valið er **Endurnýja** í útgefinni framleiðslupöntun sem var búin til frá grunni. Í þessum beint útgefnu framleiðslupöntunum er ekki hægt að breyta hólfaupplýsingum vegna þess að íhlutalínur framleiðslupöntunarinnar eru myndaðar þegar pöntunin er endurnýjuð, sem söfnuð er framvirkt íhlutunum framvirkt. Ef óskað er að breyta hólfaupplýsingum í framleiðslupöntunaríhlutalínum áður en framvirk birgðaskráning á sér stað þarf því að búa þá pöntun til með stöðuna *Áætlað* eða *Fastáætlað*.|
|Afturvirkt|Reiknar og bókar sjálfvirkt notkun samkvæmt íhlutalínum framleiðslupöntunar.<br><br> Sjálfgefið er að útreikningur og bókun íhlutanotkunar eigi sér stað þegar stöðu útgefinnar framleiðslupöntunar er breytt í **Lokið**. Ef reiturinn **Leiðartengilskóði** er notaður í íhlutalínum framleiðslupöntunar verður reiknað og bókað eftir hverja aðgerð.<br><br> **Ábending** <br>Kóðar afturvirkrar birgðaskráningar og leiðartengils er hægt að sameina þannig að magnið sem er birgðaskráð fyrir hverja aðgerð sé í hlutfalli við raunverulegt frálag þeirrar aðgerða. Nánari upplýsingar eru í [Hvernig á að birgðaskrá íhluti samkvæmt frálagi aðgerða](#to-flush-components-according-to-operation-output).<br><br> Ef birgðageymslan eða forði þar sem þessi íhlutur er notaður eru sett upp með sjálfgefnu hólfaskipulagi verður varan notuð úr **Opna hólfkóða vinnslusalar**.|
|Tínsla + Áfram|Sama og framvirk söfnunaraðferð, nema hún virkar aðeins fyrir birgðageymslur sem nota annaðhvort ítarlega vöruhúsagrunnstillingu eða grunnstillingu vöruhúss með áskilin hólf.<br><br> Notkun er reiknuð og bókuð úr hólfinu sem skilgreint er í reitnum **Hólfkóði til framleiðslu** á birgðageymslu eða vélastöð eftir að íhluturinn hefur verið tíndur úr vöruhúsinu.<br><br> **Ábending** <br>Ef íhlutur er settur upp með Tínslu + Framvirk birgðaskráningaraðferð getur hann ekki haft leiðartengilskóta við aðgerð sem er sett upp með framvirkri birgðaskráningaraðferð. Íhluturinn yrði þá sjálfkrafa skráður þegar aðgerð hefst, sem gerir kerfinu ókleift til að biðja um tínsluaðgerð.|
|Tínsla + Aftur á bak|Sama og fyrir afturvirka söfnunaraðferð, nema hún virkar aðeins fyrir birgðageymslur nota annaðhvort ítarlega vöruhúsagrunnstillingu eða grunnstillingu vöruhúss með áskilin hólf.<br><br> Notkun er reiknuð og bókuð úr hólfinu sem skilgreint er í reitnum **Hólfkóði til framleiðslu** á birgðageymslu eða vélastöð eftir að íhluturinn hefur verið tíndur úr vöruhúsinu.|

## Sjá einnig .

[Búa til framleiðsluuppskriftir](production-how-to-create-production-boms.md)  
[Uppsetning framleiðslu](production-configure-production-processes.md)  
[Framleiðsla](production-manage-manufacturing.md)  
[Áætlun](production-planning.md)  
[Birgðir](inventory-manage-inventory.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
