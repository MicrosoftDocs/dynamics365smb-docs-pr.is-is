---
title: Setja upp vinnu- og vélastöðvar
description: Vinnustöðvarspjald skipuleggur föst gildi og þarfir viðkomandi framleiðsluforða og stjórnar þannig afköstum framleiðslu þeirrar vinnustöðvar.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '99000754, 99000755, 99000756, 99000758, 99000760, 99000761, 99000762'
ms.date: 04/01/2021
ms.author: edupont
---
# Setja upp vinnu- og vélastöðvar

Forritið greinir á milli þrennskonar afkastagetu. Henni er raðað eftir stigveldi: Á hverju stigi eru undirstig.  

Efsta stigið er vinnustöðvarflokkurinn. Vinnustöðvum er úthlutað á vinnustöðvaflokkana. Hver vinnustöð getur aðeins tilheyrt einum vinnustöðvarflokki.

Hægt er að úthluta ýmsum vélastöðvum á hverja vinnustöð. Aðeins ein vélastöð getur tilheyrt hverri vinnustöð.  

Áætluð afkastageta vinnustöðvarinnar samanstendur af tiltækileika samsvarandi vélastöðva og áætlaðrar aukaafkastagetu vinnustöðvarinnar. Áætlaður tiltækileiki vinnustöðvarflokksins er því samtala alls samsvarandi tiltækileika véla- og vinnustöðva.  

Það sem er til ráðstöfunar er geymt í dagatalsfærslum.  

> [!IMPORTANT]
> Áður en þú setur upp vinnu- eða vélastöðvar, þarftu að setja upp dagatal verkstæðis. Nánari upplýsingar eru í [Búa til dagatal verkstæðis](production-how-to-create-work-center-calendars.md).

## Vinnustöð sett upp

Eftirfarandi lýsir fyrst og fremst því hvernig vinnustöð er sett upp. Skrefin í uppsetningu dagatals vélastöðva eru svipuð, fyrir utan flýtiflipann **Uppsetning leiða**.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnustöðvar** og velja síðan viðkomandi tengil.  
2. Valið er **Nýtt** aðgerð.  
3. Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Í reitnum **Vinnustöðvarhópur** skal velja efra-stigs forðaflokkun sem vinnustöðin er flokkuð undir, ef það á við. Valið er **Nýtt** aðgerðin í felllilistanum.  
5. Í reitnum **Önnur vinnustöð** skal velja vinnustöðina sem á að nota ef vinnustöðin er ekki í boði eða þegar eftirspurn er umfram getu. Önnur vinnustöð er aðeins til upplýsinga og er ekki sjálfkrafa höfð með í áætlunarferlum.
6. Veljið reitinn **Lokaður** til að koma í veg fyrir að vinnustöðin verði notuð í vinnslu. Þetta þýðir að frálag er ekki hægt að bóka fyrir vörur sem er framleidd í vinnustöðinni. Frekari upplýsingar eru í [Bóka framleiðslufrálag](production-how-to-post-output-quantity.md).
7. Í reitinn **Innk.verð** er færður inn kostnaður við að framleiða eina mælieiningu í þessari vinnustöð, án annarra kostnaðarliða. Þessi kostnaður er oft kallaður *beinn vinnutaxti*.  
8. Í reitinn **Óbein kostnaðar %** er færður inn almennur aðgerðakostnaður við notkun vinnustöðvarinnar sem hlutfall af Innkaupsverði. Þessari hlutfallslegu upphæð er bætt við beinan kostnað í útreikningum á kostnaðarverði.  
9. Í reitinn **Hlutf. sameiginl. kostn.** er færður inn kostnaður vegna vinnustöðvar sem ekki kemur aðgerðum beint við, s.s. viðhaldskostnað, sem algilda tölu.  

    Reiturinn **Kostn.verð** inniheldur reiknað kostnaðarverð einnar mælieiningar, með öllum kostnaðarliðum, í þessari vinnustöð, sem hér segir:  

    Kostnaðarverð = Innkaupsverð + (Innkaupsverð x Óbein kostnaðar %) + Hlutfall sameiginlegs kostnaðar.  

10. Í reitnum **Útreikningur kostn.verðs** er tilgreint hvort útreikningurinn hér að ofan sé byggður á tímafjölda:  **Tími**; eða fjölda framleiddra eininga:  **Einingar**.  
11. Veljið reitinn **Tiltekinn einingarkostnaður** ef á að skilgreina einingarkostnað vinnustöðvar í leiðarlínunni þar sem hann er notaður. Slíkt kann að eiga við aðgerðir með verulegan mismun í kostnaði afkastagetu miðað við það sem er venjulega unnið í vinnustöðinni.  
12. Í reitnum **Birgðaskráningaraðferð** er valið hvort reikna á og bóka frálagsbókun á þessari vinnustöð handvirkt eða sjálfvirkt með annarri hvorri eftirfarandi aðferð.

    |Valkostur|Description|
    |------|-----------|
    |**Handvirkt**| Notaður tími, úttak og rýrnun eru bókuð handvirkt í úttaksbók eða framleiðslubók.|
    |**Framvirk**|Úttak er bókað sjálfkrafa þegar framleiðslupöntun er gefin út.|
    |**Afturvirkt**|Úttak er bókað sjálfkrafa þegar framleiðslupöntun er lokið.|

    > [!NOTE]
    > Ef nauðsyn krefur er hægt að hunsa losunaraðferðina hér fyrir einstakar aðgerðir með því að breyta stillingunni í leiðarlínum

13. Í reitinn **Mælieiningarkóði** er færð inn tímaeiningin þar sem þessi kostnaðarútreikningur og afkastagetuáætlun vinnustöðvar eru gerð.
    Til að geta fylgst stöðugt með notkun verður fyrst að setja upp mæliaðferð. Einingarnar sem eru færðar inn eru grunneiningar. Vinnslutíminn er til dæmis mældur í klukkustundum og mínútum.

    > [!NOTE]  
    > Ef valið er að nota Dagar Skal hafa það í huga að 1 dagur = 24 klukkustundir - en ekki 8 (vinnustundir).

14. Í reitnum **Geta** er tilgreint hvort vinnustöð er með fleiri en einn einstakling við vinnu og eina vél í vinnslu á sama tíma. Ef uppsetning [!INCLUDE[prod_short](includes/prod_short.md)] inniheldur ekki Vélastöðvaraðgerð verður gildið í þessum reit að vera **1**.  
15. Í reitinn **Skilvirkni** er fært inn hlutfall áætlaðra staðlaðra afkasta sem þessi vinnustöð afkastar í raun. Ef fært er inn **100** þýðir það að raunveruleg afköst vinnustöðvarinnar eru þau sömu og staðlaða afkastagetan.  
16. Velja skal **Sameinað dagatal** gátreitinn ef þú ert líka að nota vélstöðvar. Þetta tryggir að dagatalsfærslur verði settar saman frá vélastöðva dagatölum.  
17. Í reitnum **Dagatalskóti verkstæðis** veljið dagatal verkstæðis. Nánari upplýsingar eru í [Búa til dagatal verkstæðis](production-how-to-create-work-center-calendars.md).  
18. Í reitnum **Biðraðartími** er tilgreindur fastur tími sem þarf að líða áður en úthlutað verk er hafið á þessari vinnustöð. 

> [!NOTE]
> Nota skal biðtíma til að veita smá tíma á milli þess þegar íhluturinn kemur á vél eða vinnustöð og þegar aðgerðin hefst í raun. Ef til dæmis hlutur er afhentur vélastöð klukkan 10:00 en það tekur klukkustund að festa hann við vél hefst aðgerðin ekki fyrr en 11:00. Biðtíminn yrði þá ein klukkustund. Gildið úr reitnum **Biðraðartími** á véla- eða Vinnustöðvarspjaldi plús samtala gildanna í reitunum **Uppsetningartími**, **Keyrslutími**, **Biðtími** og **Flutningstími** í vöruleiðarlínunni gefa afgreiðslutímann í framleiðslu vörunnar. Þetta hjálpar til við að gefa upp nákvæman framleiðslutíma alls.  

## Hvað skal hafa í huga varðandi afkastagetu

Afkastageta og skilvirkni sem eru tilgreindar fyrir vinnu- og vélastöð hefur ekki aðeins áhrif á tiltæka afkastagetu. Þær hafa einnig áhrif á heildarframleiðslutímann sem samanstendur af uppsetningartíma og keyrslutíma, sem báðir eru skilgreindir í leiðarlínunni.  

Þegar tiltekinni leiðarlínu er úthlutað á vinnu- eða vélastöð reiknar kerfið út hversu mikla afkastagetu þarf og hversu lengi það tekur að ljúka aðgerðinni.  

### Keyrslutími

Til að reikna keyrslutíma úthlutar kerfið nákvæmlega þeim tíma sem skilgreindur er í reitnum **Keyrslutími** fyrir leiðarlínuna. Hvorki skilvirkni né afkastageta hafa áhrif á úthlutaðan tíma. Ef keyrslutíminn er til dæmis skilgreindur sem 2 klukkustundir mun úthlutaður tími vera 2 klukkustundir burtséð frá gildum í reitum skilvirkni og afkastagetu í vinnustöðinni.  

> [!NOTE]
> Afkastagetan sem er notuð í útreikningunum er skilgreind sem lágmarksgildið milli afkastagetu sem er skilgrein í vinnu- eða vélastöðinni og samhliða afkastagetunni sem er skilgreind fyrir leiðarlínuna. Ef vinnustöð er með afkastagetu 100, en samhliða afkastageta fyrir leiðarlínu er 2, mun *2* verða notað í útreikningunum.

*Tímalengd* aðgerðar tekur aftur á móti bæði skilvirkni og afkastagetu til greina. Tímalengd er reiknuð sem *Keyrslutími / Skilvirkni / Afkastageta*. Eftirfarandi listi sýnir nokkur dæmi um útreikning tímalengdar fyrir sama keyrslutímann sem er skilgreindur sem 2 klukkustundir fyrir leiðarlínuna:

- Skilvirkni 80% þýðir að þú þarft 2,5 klst. í stað tveggja klst.  
- Skilvirkni 200% þýðir að þú getur lokið verkinu á einni klukkustund - þú getur grafið holuna tvisvar sinnum hraðar ef þú ert með gröfu sem er tvöfalt stærri en sú minni  

    Þú getur náð sömu niðurstöðu ef þú notar tvær minni gröfur í stað stórrar – notaðu *2* sem afkastagetu og *100%* sem skilvirkni  

Afkastageta með aukastöfum er flókin og við fjöllum um hana síðar. 

### Uppsetningartími

Úthlutun tíma fyrir uppsetningartímann fer eftir afkastagetu og er reiknaður sem *Uppsetningartími * afkastageta*. Ef afkastagetan er til dæmis stillt á *2* verður úthlutaður uppsetningartími tvöfaldaður vegna þess að þú verður að setja upp tvær vélar fyrir aðgerðina.  

*Tímalengd* uppsetningartíma fer eftir skilvirkni og er reiknuð út sem *Uppsetningartími / skilvirkni*. 

- Skilvirkni 80% þýðir að þú þarft 2,5 klst í stað tveggja klukkustunda til að setja upp  
- Skilvirkni 200% þýðir að þú getur lokið uppsetningunni á 1 klst. í stað 2 klst. eins og skilgreint er í leiðarlínunni  

Ekki er auðvelt að halda utan um afkastagetu með aukastöfum og er hún notuð í mjög sérstökum tilfellum.

### Vinnustöð sem vinnur úr mörgum pöntunum samtímis

Notum sprautunarklefa sem dæmi. Hann er með sömu uppsetningu og keyrslutíma fyrir hverja lotu. En hver lota getur innihaldið margar stakar pantanir sem eru sprautaðar samtímis.  

Í þessu tilfelli er tíma og kostnaði sem er úthlutað á pantanir stjórnað af uppsetningartíma og samhliða afkastagetu. Ekki er mælt með að nota keyrslutíma og leiðarlínur.  

Úthlutaður uppsetningartími fyrir hverja einstaka pöntun verður í öfugri röð við fjölda pantana (magns) sem er framkvæmd samtímis. Hér eru fleiri dæmi um útreikning uppsetningartíma þegar hann er skilgreindur sem tvær klukkustundir fyrir leiðarlínuna:

- Ef það eru tvær pantanir ætti samhliða afkastageta í leiðarlínunni að vera stillt á 0,5.

    Fyrir vikið verður úthlutuð afkastageta fyrir hvora pöntun að vera ein klukkustund en tímalengd hverrar pöntunar verður áfram tvær klukkustundir.
- Ef það eru tvær pantanir með einn og fjórir í magn, þá verður samhliða afkastageta fyrir leiðarlínu fyrri pöntunar 0,2 og 0,8 fyrir þá seinni.  

    Fyrir vikið verður úthlutuð afkastageta fyrir fyrri pöntunina 24 mín og 96 mín fyrir þá seinni. Tímalengd beggja pantana er áfram tvær klukkustundir.  

Í báðum tilfellum er heildartími úthlutunar fyrir allar pantanir tvær klukkustundir.


### Skilvirkt tilfang getur úthlutað aðeins hluta af vinnudagsetningu þeirra í framleiðsluvinnu

> [!NOTE]
> Ekki er mælt með þessum aðstæðum. Mælt er með því að nota skilvirkni í staðinn. 

Ein af vinnustöðvunum þínum stendur fyrir reynslumikinn starfsmann sem vinnur verk með 100% skilvirkni. En hann getur aðeins helgað 50% af vinnutímanum í verk því hinn hluta tímans sinnir hann stjórnunarverkum. Þótt þessi starfsmaður geti lokið tveggja klukkustunda verki á nákvæmlega tveimur klukkustundum þarf samt að meðaltali að bíða aðrar tvær klukkustundir á meðan einstaklingurinn sinnir öðrum verkefnum.  

Úthlutaður keyrslutími er tvær klukkustundir og tímalengdin er fjórar klukkustundir.  

Ekki nota uppsetningartíma fyrir slíkar aðstæður þar sem kerfið mun aðeins úthluta 50% af tímanum. Ef uppsetningartíminn er stilltur á *2* er úthlutaður uppsetningartími ein klukkustund og tímalengdin tvær klukkustundir.

### Sameinað dagtal

Þegar reiturinn **Sameinað dagtal** er valið hefur vinnustöðin ekki sína eigin afkastagetu. Í staðinn jafngildir afkastagetan allri afkastagetu allra vélastöðva sem úthlutaðar eru vinnustöðinni.  

> [!NOTE]
>  Skilvirkni vélastöðvarinnar er breytt í afkastagetu vinnustöðvarinnar.

Ef þú ert til dæmis með vélastöðvar með 80 og 70 í skilvirkni verður færsla sameinaðs dagatals með skilvirknina 100, afkastagetuna 1,5 og heildarafkastagetu sem 12 klukkustundir (átta klukkustunda vakt * 1,5 afkastageta). 

> [!NOTE]
>  Notaðu reitinn **Sameinað dagtal** þegar leiðir eru skipulagðar með tímasettum framleiðsluaðgerðum á stigi vélastöðvar, ekki stigi vinnustöðvar. Þegar dagatalið er sameinað verða síðan **Álag á vinnustöð** og skýrslur að yfirliti yfir samtals vinnuálag í öllum vélastöðvum sem úthlutaðar eru á vinnustöðina.

### Dæmi - Mismunandi vélastöðvum úthlutað á vinnustöð

Mikilvægt er að áætla nauðsynlega heildarafkastagetu við uppsetningu véla- og vinnustöðva.

Ef mismunandi vélastöðvum (t.d. 210 Pökkunarborð 1, 310 Málningarklefi) er úthlutað á vinnustöð þarf að taka með í reikninginn afkastagetu vélastöðvanna þar sem bilun í einni vinnustöð getur tafið allan ferilinn. Hægt er að færa inn vélarhópana samkvæmt getu þeirra en ekki má taka tillit til þeirra í áætluninni. Með því að gera reitinn **Sameinað dagatal** óvirkan er afkastagetu vinnustöðvarinnar en ekki vélastöðvarinnar úthlutað í áætluninni.

Ef hins vegar sams konar vélastöðvar (t.d. 210 Pökkunarborð 1 og 220 Pökkunarborð 2) eru sameinaðar í eina vinnustöð er það vinnustöðin sem samtala úthlutaðra vélastöðva sem skiptir höfuðmáli. Því yrði vinnustöðin skráð með enga getu. Með því að virkja reitinn **Sameinað dagatal** er sameiginlegri afkastagetu úthlutað á vinnustöðina.

Ef ekki á að taka með afkastagetu vinnustöðva í heildarafkastagetunni má stilla skilvirkni = 0.

## Vinnu- eða vélastöð með takmarkaða afkastagetu sett upp

Setja þarf upp framleiðsluforða sem talinn er mikilvægur og merkja hann þannig að hann samþykki takmarkað álag í staðinn fyrir sjálfgefið, ótakmarkað álag sem annar framleiðsluforði samþykkir. Tilfang með takmarkaða afkastagetu getur verið vinnu- eða vélastöð sem þú hefur greint sem flöskuháls og vilt setja takmarkað álag á.

[!INCLUDE[prod_short](includes/prod_short.md)] styður ekki sundurliðaða vinnusalsstýringu. Hún áætlar gerlega nýtingu tilfanga með því að leggja fram grófa áætlun en stofnar ekki og viðheldur sjálfkrafa ítarlegum áætlunum, byggðum á reglum um forgangsröðun eða bestun.

Á síðunni **Tilföng með takmarkaða afkastagetu**, geturðu búið til uppsetning sem forðast yfirálag á tilgreind tilföng og tryggir að engin afkastageta sé án úthlutunar ef úthlutun á henni gæti aukið viðdvalartíma framleiðslupöntunar. Í reitnum **Hömlur (% af heildar afkastagetu)** má bæta við hömlutíma á tilföng til að draga úr skiptingu aðgerðar. Þetta gerir kerfinu kleift að áætla hleðslu á síðasta mögulega dag með því auka álagsprósentuna lítillega ef það er hægt að minnka fjölda virkni sem er skipt.

Við áætlum á tilföngum með takmarkaða getu tryggir kerfið að engin tilföng séu hlaðin yfir skilgreina getu (hættumörk) Þetta er gert með því að úthluta hverri virkni á næsta tiltekna tímabil. Ef tímabilið er ekki nógu langt til að hægt sé að ljúka allri aðgerðinni verður aðgerðinni skipt í tvo eða fleiri hluta á næstu tiltæku tímabilum.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Tilföng takmarkaðrar afkastagetu** og velja síðan viðkomandi tengil.
2. Valið er aðgerðin **Nýtt**.
3. Fyllið inn í reitina eftir þörfum.

> [!NOTE]
> Aðgerðir á vinnustöðvum eða vélastöðvum sem settar eru upp sem takmarkaður forði verða alltaf áætlaðar í röð. Það þýðir að jafnvel ef takmarkaður forði er með margar afkastagetur þá eru aðgerðir sem þessar getur framkvæma aðeins áætlaðar í röð, ekki samhliða, eins og yrði gert ef vélastöðin var ekki sett upp sem takmarkaður forði. Reiturinn Geta í vinnu- eða vélastöð er hærri en 1 fyrir takmarkaðan forða

> Í tilviki uppskiptingar starfssemi er uppsetningartíma aðeins  úthlutað einu sinni vegna þess að það er gert ráð fyrir að sumir handvirk jöfnun sé gerð til að hámarka áætlun.

## Sjá einnig

[Stofna dagatal verkstæðis](production-how-to-create-work-center-calendars.md)  
[Uppsetning framleiðslu](production-configure-production-processes.md)  
[Framleiðsla](production-manage-manufacturing.md)  
[Áætlun](production-planning.md)  
[Birgðir](inventory-manage-inventory.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
