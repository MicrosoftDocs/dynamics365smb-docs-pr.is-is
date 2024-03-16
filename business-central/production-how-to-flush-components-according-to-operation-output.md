---
title: Skolið íhluti í samræmi við vinnsluúttak
description: Þessi grein lýsir því hvernig á að skola íhluti í samræmi við rekstrarúttak og aðrar skolunaraðferðir sem taka þátt.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 12/13/2023
ms.author: bholtorf
---

# <a name="flush-components-according-to-operation-output"></a>Skolið íhluti í samræmi við vinnsluúttak
Hægt er að skilgreina mismunandi losunarleiðir til að gera skráningu á notkun íhluta sjálfvirka. 

Þessi aðgerð er gagnleg af eftirfarandi ástæðum:  

- **Verðmat birgða**

    Virðisfærslur fyrir frálag og notkun eru stofnaðar samhliða framleiðslupöntun í vinnslu. Án leiðartenglakóða eykst birgðagildið þegar framleiðsla er bókuð og lækkar síðan síðar þegar verðmæti íhlutanotkunar er bókað ásamt fullunninni framleiðslupöntun.  
- **Birgðir til ráðstöfunar**

    Með stöðugri notkunarbókun er betur uppfært hvort íhlutir eru til ráðstöfunar, sem er mikilvægt til að viðhalda innra jafnvægi á milli eftirspurnar og framboðs. Án leiðartengilkóða gætu aðrar kröfur um íhlutinn trúað því að hann sé tiltækur svo framarlega sem hann bíður seinkaðrar notkunarfærslu.  
- **Rétt í tíma**

    Með getu til að sérsníða vörur að beiðni viðskiptavina geturðu lágmarkað sóun með því að ganga úr skugga um að vinnu- og kerfisbreytingar eigi sér aðeins stað þegar þess er þörf.  

- **Draga úr gagnaskráningu**

    Með getu til að skola aðgerð sjálfkrafa er hægt að gera allt neyslu- og framleiðsluferlið sjálfvirkt. Ókosturinn við að nota sjálfvirka skolun er að þú gætir ekki verið að taka upp nákvæmlega, eða jafnvel meðvituð um, rusl.

## <a name="automatic-consumption-posting-flushing-methods"></a>Sjálfvirk neyslubókun (Róun) aðferðir

- Framvirk birgðaskráning allrar pöntunarinnar  
- Framvirk birgðaskráning eftir aðgerð  
- Bakskráning eftir aðgerð  
- Bakskráning allrar pöntunarinnar  

### <a name="automatic-reporting---forward-flush-the-entire-order"></a>Sjálfvirk skýrsla - Áfram skolaðu alla pöntunina
Ef þú tæmir framleiðslupöntunina áfram við upphaf verksins er hegðun beitingar svipað og handvirk neysla. Meginmunurinn er sá að notkunin gerist sjálfvirkt.  

- Allt innihald framleiðsluuppskriftarinnar er notað og dregið af birgðaskrá á þeirri stundu sem útgefna framleiðslupöntunin er endurnýjuð.  
- Neyslumagnið er magnið á hverja samsetningu sem tilgreint er á framleiðsluuppskriftinni, margfaldað með fjölda yfirvara sem þú ert að smíða.  
- Það er engin þörf á að skrá neinar upplýsingar í neysludagbók ef skola á alla hlutina.  
- Við neyslu á vörum úr birgðum skiptir ekki máli hvenær úttaksbókunarfærslur eru gerðar, því úttaksbókin hefur engin áhrif á þessa notkunarbókun.  
- Ekki er hægt að stilla neina leiðartengilskóta.  

Framvirk birgðaskráning heillar pöntunar hentar fyrir framleiðsluumhverfi með:  

-   Lítinn fjölda af göllum  
-   Lítinn fjölda af aðgerðum  
-   Mikla notkun íhluta í fyrstu aðgerðum  

### <a name="automatic-reporting---forward-flushing-by-operation"></a>Sjálfvirk tilkynning - Áframskolun með aðgerð
Birgðaskráning eftir aðgerð gerir það mögulegt að draga frá birgðum á meðan á tiltekinni aðgerð í leið yfirvörunnar stendur. Efni er tengt leiðinni með leiðartengilskótum sem samsvara þeim leiðartengilskótum sem eru notaðir fyrir íhluti í framleiðsluuppskriftinni.  

Birgðaskráningin á sér stað þegar aðgerðin sem hefur sama leiðartengilskóta er hafin. Hafin þýðir að einhver virkni er skráð í frálagsbókina fyrir þá aðgerð. Og sú virkni gæti verið einfaldlega það að uppsetningartími er færður inn.  

Magnið í birgðaskráningunni stendur fyrir magnið fyrir hverja samsetningu sem kemur fram á framleiðsluuppskriftinni margfaldað með fjölda þeirra yfirvara sem verið er að byggja (magn sem búist er við).  

Þessi tækni er best notuð þegar það eru margar aðgerðir og ekki er þörf á tilteknum íhlutum fyrr en seint í samsetningarröðinni. Raunar gæti verið að Tímanleg (JIT) uppsetning sé ekki einu sinni með vörurnar tiltækar þegar ferlið er hafið.  

Hægt er að nota efni á meðan á aðgerðum stendur með því að nota leiðartengilskóta. Suma íhluti má ekki nota fyrr en í lokasamsetningu og ætti ekki að taka þær af lager fyrr en á þeim tíma.  

### <a name="automatic-reporting---back-flushing-by-operation"></a>Sjálfvirk tilkynning - Bakskolun með aðgerð
Bakskráning eftir aðgerð skráir notkun eftir að aðgerðin er bókuð í frálagsbókina.  

Kosturinn við þessa aðferð er að fjöldi þeirra aðalhluta sem búið er að nota í aðgerðinni er þekktur.  

Efni í framleiðsluuppskriftinni er tengt við leiðarfærslurnar með leiðartengilskótum. Bakskráningin á sér stað þegar aðgerð með tiltekinn leiðartengilskóti er bókaður með afgreiddu magni.  

Magnið í birgðaskráningunni stendur fyrir magnið fyrir hverja samsetningu sem kemur fram á framleiðsluuppskriftinni margfaldað með fjölda þeirra yfirvara sem voru bókaðar sem frálagsmagn í þeirri aðgerð. Þetta gæti verið frábrugðið því magni sem búist var við.  

### <a name="automatic-reporting---back-flushing-the-entire-order"></a>Sjálfvirk skýrsla - Skolar alla pöntunina til baka
Þessi skýrsluaðferð tekur ekki til greina að beina tengikóðum.  

Engir íhlutir eru valdir þar til stöðu útgefnu framleiðslupöntunarinnar er breytt í *Lokið*. Magnið í birgðaskráningunni er það magn fyrir hverja samsetningu sem kemur fram á framleiðsluuppskriftinni margfaldað með þeim fjölda yfirvara sem voru fullunnar og settar í birgðir.  

Afturvirk birgðaskráning á allri framleiðslupöntuninni krefst sömu uppsetningar og fyrir framvirka söfnun: Skýrslugerðaraðferðin þarf að vera stillt á afturvirkt á hverju birgðaspjaldi til þess að allar vörur innan yfiruppskriftarinnar verði skráðar. Þar að auki þarf að fjarlægja alla leiðartengilskóta úr framleiðsluuppskriftinni. 



Til dæmis ef framleiðslupöntun um að framleiða 800 metra krefst 8 kg af íhlut, og ef 200 metrar eru bókaðir sem frálag, bókast 2 kg sjálfkrafa sem notkun. Þessu er hægt að ná með því að sameina afturvirka losunaraðferð og kóða leiðartengla þannig að magnið sem er losað fyrir hverja aðgerð er í hlutfalli við raunverulegt frálag lokinnar aðgerðar. Fyrir vörur sem hafa verið settar upp með afturvirkri birgðaskráningu er sjálfgefin virkni að reikna út og bóka notkun íhluta þegar stöðu útgefinnar framleiðslupöntunar er breytt í **Lokið**. Ef þú skilgreinir einnig leiðartenglakóða, þá á sér stað útreikningur og bókun þegar hverri aðgerð er lokið og magnið sem var notað í aðgerðinni er bókað. Nánari upplýsingar eru í [Stofna leiðir](production-how-to-create-routings.md).  

## <a name="to-flush-components-according-to-operation-output"></a>Til að birgðaskrá íhluti samkvæmt frálagi aðgerðar

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

Eyðslan er bókuð sjálfkrafa þegar þú skráir úttak. Frekari upplýsingar, sjá [Fjöldabóka frálag og keyrslutíma](production-how-to-post-output-quantity.md)

## <a name="flushing-methods"></a>Flæðiaðferðir

Eftirfarandi tafla lýsir tiltækri losunaraðferð sem hægt er að tilgreina í spjaldinu **Vara** og spjaldinu **Birgðahaldseining**.

|Valkostur|Description|
|------------|-------------|  
|Handvirk|Krefst þess að notkun sé handskráð og bókuð í notkunarbók.|
|Framvirk|Bókar sjálfvirkt notkun samkvæmt íhlutalínum framleiðslupöntunar. <br><br>Sjálfgefið er að útreikningur og bókun íhlutanotkunar eigi sér stað þegar stöðu útgefinnar framleiðslupöntunar er breytt í **Útgefin**. Ef reiturinn **Leiðartengilskóði** er notaður í íhlutalínum framleiðslupöntunar verður bókað fyrir hverja aðgerð þegar aðgerðir hefjast. Frekari upplýsingar, sjá [Hvernig skal: Stofna leiðartengla](production-how-to-create-routings.md#to-create-routing-links). <br><br> **Ábending**<br>Fyrir framvirka birgðaskráningu, byggist bókunin fyrir tiltekið verk sem notandinn fær með leiðartengilskóða á magni sem er skilgreint í íhlutalínunni. Sjá lýsingu á **Afturábak** í þessari grein fyrir upplýsingar um notkunarsértæka skolun sem byggist á raunverulegri framleiðslu.<br><br>Ef birgðageymslan eða forði þar sem þessi íhlutur er notaður eru sett upp með sjálfgefnu hólfaskipulagi verður varan notuð úr **Opna hólfkóða vinnslusalar**. Frekari upplýsingar, sjá [Hvernig á að: setja upp einfaldar vöruhúsaaðgerðir með aðgerðasvæði](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md). <br><br> **Mikilvægt** <br>Framvirk birgðaskráning á sér einnig stað þegar valið er **Endurnýja** í útgefinni framleiðslupöntun sem var búin til frá grunni. Á þessum beint stofnuðu útgefnu framleiðslupantunum er ekki hægt að breyta hólfupplýsingum vegna þess að framleiðslupöntunaríhlutalínur eru búnar til þegar þú endurnýjar pöntunina, sem á sama tíma tæmir íhlutina áfram. Ef óskað er að breyta hólfaupplýsingum í framleiðslupöntunaríhlutalínum áður en framvirk birgðaskráning á sér stað þarf því að búa þá pöntun til með stöðuna *Áætlað* eða *Fastáætlað*.|
|Afturvirkt|Reiknar og bókar sjálfvirkt notkun samkvæmt íhlutalínum framleiðslupöntunar.<br><br> Sjálfgefið er að útreikningur og bókun íhlutanotkunar eigi sér stað þegar stöðu útgefinnar framleiðslupöntunar er breytt í **Lokið**. Ef reiturinn **Leiðartengilskóði** er notaður í íhlutalínum framleiðslupöntunar verður reiknað og bókað eftir hverja aðgerð.<br><br> **Ábending** <br>Kóðar afturvirkrar birgðaskráningar og leiðartengils er hægt að sameina þannig að magnið sem er birgðaskráð fyrir hverja aðgerð sé í hlutfalli við raunverulegt frálag þeirrar aðgerða. Nánari upplýsingar eru í [Hvernig á að birgðaskrá íhluti samkvæmt frálagi aðgerða](#to-flush-components-according-to-operation-output).<br><br> Ef birgðageymslan eða forði þar sem þessi íhlutur er notaður eru sett upp með sjálfgefnu hólfaskipulagi verður varan notuð úr **Opna hólfkóða vinnslusalar**.|
|Tínsla + Áfram|Sama og fyrir áframskolunaraðferðina, nema hún virkar aðeins fyrir staðsetningar sem nota annað hvort háþróaða vöruhúsastillingu eða grunnstillingar vöruhúsa með lögboðnum hólfum.<br><br> Notkun er reiknuð og bókuð úr hólfinu sem skilgreint er í reitnum **Hólfkóði til framleiðslu** á birgðageymslu eða vélastöð eftir að íhluturinn hefur verið tíndur úr vöruhúsinu.<br><br> **Ábending** <br>Ef íhlutur er settur upp með Pick + Forward skolunaraðferðinni, þá getur hann ekki haft leiðartengilkóða við aðgerð sem er sett upp með áframskolunaraðferðinni. Íhluturinn yrði þá sjálfkrafa skráður þegar aðgerð hefst, sem gerir kerfinu ókleift til að biðja um tínsluaðgerð.|
|Tínsla + Aftur á bak|Sama og fyrir afturábak skolunaraðferð, nema að hún virkar aðeins fyrir staðsetningar sem nota annaðhvort háþróaða vöruhúsastillingu eða grunnstillingar vöruhúsa með lögboðnum hólfum.<br><br> Notkun er reiknuð og bókuð úr hólfinu sem skilgreint er í reitnum **Hólfkóði til framleiðslu** á birgðageymslu eða vélastöð eftir að íhluturinn hefur verið tíndur úr vöruhúsinu.|

## <a name="see-also"></a>Sjá einnig .

[Búa til framleiðsluuppskriftir](production-how-to-create-production-boms.md)  
[Uppsetning framleiðslu](production-configure-production-processes.md)  
[Framleiðsla](production-manage-manufacturing.md)  
[Áætlun](production-planning.md)  
[Birgðir](inventory-manage-inventory.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
