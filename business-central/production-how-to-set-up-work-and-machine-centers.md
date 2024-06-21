---
title: Setja upp vinnustöðvar og vélastöðvar
description: Vinnustöðvarspjald skipuleggur föst gildi og þarfir viðkomandi framleiðsluforða og stjórnar þannig afköstum framleiðslu þeirrar vinnustöðvar.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '99000754, 99000755, 99000756, 99000758, 99000760, 99000761, 99000762'
ms.date: 06/13/2024
ms.service: dynamics-365-business-central
---
# <a name="set-up-work-centers-and-machine-centers"></a>Setja upp vinnustöðvar og vélastöðvar

[!INCLUDE [prod_short](includes/prod_short.md)] greinir á milli þriggja tegunda afkastagetu sem er raðað í stigveldi þar sem hvert stig inniheldur undirstig.  

Efsta stigið er vinnustöðvarflokkurinn. Vinnustöðvum er úthlutað á vinnustöðvarhópa. Hver vinnustöð getur aðeins tilheyrt einum vinnustöðvarflokki.

Hægt er að úthluta ýmsum vélastöðvum á vinnustöðvar. Vélastöð getur aðeins tilheyrt einni vinnustöð.  

Áætluð afkastageta vinnustöðvar samanstendur af tiltækum vélastöðvum og áætluðum ráðstöfunarmagni vinnustöðvarinnar. Áætlaður tiltækileiki vinnustöðvarflokksins er því samtala alls samsvarandi tiltækileika véla- og vinnustöðva. Til ráðstöfunar er geymt í dagatalsfærslum.  

> [!IMPORTANT]
> Áður en þú setur upp vinnu- eða vélastöðvar, þarftu að setja upp dagatal verkstæðis. Nánari upplýsingar eru í [Búa til dagatal verkstæðis](production-how-to-create-work-center-calendars.md).

## <a name="to-set-up-a-work-center"></a>Vinnustöð sett upp

Eftirfarandi skref útskýra hvernig setja á upp vinnustöð. Skrefin sem setja á upp dagatal vélastöðvar eru svipuð nema á flýtiflipanum **Leiðargrunnur** .  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnustöðvar** og velja síðan viðkomandi tengil.  
2. Valið er aðgerðin **Nýtt**.  
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Í reitnum **Kóti** vinnustöðvarhóps skal velja efra-stigs forðaflokkunina sem vinnustöðin er flokkuð undir, ef það á við. Valið er **Nýtt** aðgerðin í felllilistanum.  
5. Í reitnum **Önnur vinnustöð** skal velja vinnustöðina sem á að nota ef vinnustöðin er ekki í boði eða þegar eftirspurn er umfram getu. Önnur vinnustöð er aðeins til upplýsinga og er ekki sjálfkrafa höfð með í áætlunarferlum.
6. Veljið reitinn **Lokaður** til að koma í veg fyrir að vinnustöðin verði notuð í vinnslu. Þetta þýðir að ekki er hægt að bóka frálag fyrir vöru sem er framleidd í vinnustöðinni. Frekari upplýsingar eru í [Bóka framleiðslufrálag](production-how-to-post-output-quantity.md).
7. Í reitinn **Innk.verð** er færður inn kostnaður við að framleiða eina mælieiningu í þessari vinnustöð, án annarra kostnaðarliða. Þessi kostnaður er oft kallaður *beinn vinnutaxti*.  
8. Í reitinn **Óbein kostnaðar %** er færður inn almennur aðgerðakostnaður við notkun vinnustöðvarinnar sem hlutfall af Innkaupsverði. Þessari hlutfallslegu upphæð er bætt við beinan kostnað í útreikningum á kostnaðarverði.  
9. Í reitinn **Hlutfall** sameiginlegs kostnaðar er færður inn óvinnufærður kostnaður, til dæmis viðhaldskostnaður vinnustöðvarinnar sem alger upphæð.  

    Reiturinn **Kostn.verð** inniheldur reiknað kostnaðarverð einnar mælieiningar, með öllum kostnaðarliðum, í þessari vinnustöð, sem hér segir:  

    Kostnaðarverð = Innkaupsverð + (Innkaupsverð x Óbein kostnaðar%) + Hlutfall sameiginlegs kostnaðar.  

10. Í reitnum **Útreikningur kostn.verðs** er tilgreint hvort útreikningur kostnaðarverðs skuli byggður á tímafjölda eða fjölda framleiddra eininga.  
11. Reiturinn **Sérstakt kostnaðarverð** er valinn ef skilgreina á kostnaðarverð vinnustöðvarinnar á leiðarlínunni þar sem það er notað. Þessi stilling getur átt við aðgerðir með afkastagetukostnað sem er öðruvísi en það sem venjulega er unnið í þeirri vinnustöð.  
12. Í reitnum **Birgðaskráningaraðferð** er valið hvort reikna og bóka afköst sjálfvirkt í þessari vinnustöð með því að nota eina af eftirfarandi aðferðum.

    |Valkostur|Heimildasamstæða|
    |------|-----------|
    |**Handvirkt**| Bóka handvirkt notaðan tíma, frálag og úrkast í frálagsbók eða framleiðslubók.|
    |**Framvirk**|Bóka frálag sjálfkrafa þegar framleiðslupöntunin er gefin út.|
    |**Afturvirkt**|Bóka frálag sjálfkrafa þegar framleiðslupöntuninni er lokið.|

    > [!NOTE]
    > Ef nauðsyn krefur er hægt að breyta birgðaskráningaraðferðinni sem hér er valin fyrir einstakar aðgerðir með því að breyta stillingum á leiðarlínum

13. Í reitinn **Mælieiningarkóði** er færð inn tímaeiningin þar sem þessi kostnaðarútreikningur og afkastagetuáætlun vinnustöðvar eru gerð.
    Til að geta fylgst stöðugt með notkun þarf fyrst að setja upp mæliaðferð. Einingarnar sem eru færðar inn eru grunneiningar. Vinnslutíminn er til dæmis mældur í klukkustundum og mínútum.

    > [!NOTE]  
    > Ef notaðir eru Dagar skal muna að einn dagur er 24 klukkustundir en ekki átta klukkustunda vinnudagur.

14. Í reitnum **Geta** er tilgreint hvort vinnustöð er með fleiri en einn einstakling við vinnu og eina vél í vinnslu á sama tíma.  [!INCLUDE[prod_short](includes/prod_short.md)] Ef vélastöðin er ekki með verður gildið í þessum reit að vera **1**.  
15. Í reitinn **Skilvirkni** er fært inn hlutfall áætlaðra staðlaðra afkasta sem þessi vinnustöð afkastar í raun. Ef fært er inn **100** þýðir það að raunveruleg afköst vinnustöðvarinnar eru þau sömu og staðlaða afkastagetan.  
16. Kveikja á vísbendingu um **samsteypudagatal** ef einnig eru notaðar vélastöðvar. Þessi stilling tryggir að dagatalsfærslur séu samanteknar úr dagatölum vélastöðvar.  
17. Í reitnum **Dagatalskóti verkstæðis** veljið dagatal verkstæðis. Nánari upplýsingar eru í [Búa til dagatal verkstæðis](production-how-to-create-work-center-calendars.md).  
18. Í reitnum **Biðraðartími** er tilgreindur fastur tími sem þarf að líða áður en úthlutað verk er hafið á þessari vinnustöð. 

> [!NOTE]
> Nota skal biðtíma til að veita smá tíma á milli þess þegar íhluturinn kemur á vél eða vinnustöð og þegar aðgerðin hefst í raun. Ef til dæmis hlutur er afhentur vélastöð klukkan 10:00 en það tekur klukkustund að festa hann við vél hefst aðgerðin ekki fyrr en 11:00. Biðtíminn yrði þá ein klukkustund. Gildið úr reitnum **Biðraðartími** á véla- eða Vinnustöðvarspjaldi plús samtala gildanna í reitunum **Uppsetningartími**, **Keyrslutími**, **Biðtími** og **Flutningstími** í vöruleiðarlínunni gefa afgreiðslutímann í framleiðslu vörunnar. Þetta hjálpar til við að gefa upp nákvæman framleiðslutíma alls.  

## <a name="considerations-about-capacity"></a>Hvað skal hafa í huga varðandi afkastagetu

Afkastageta og skilvirkni vinnu- og vélastöðva hafa áhrif á meira en bara tiltæka afkastagetu. Gildin hafa einnig áhrif á heildarframleiðslutímann sem samanstendur af uppsetningartímanum og keyrslutímanum sem eru bæði skilgreindir á leiðarlínunni.  

Þegar leiðarlínu er úthlutað á vinnu- eða vélastöð er [!INCLUDE [prod_short](includes/prod_short.md)]  reiknað:

- Hversu mikla afkastagetu er þörf.
- Hve langan tíma tekur að ljúka aðgerðinni.  

### <a name="run-time"></a>Keyrslutími

Til að reikna keyrslutíma úthlutar kerfið nákvæmlega þeim tíma sem skilgreindur er í reitnum **Keyrslutími** fyrir leiðarlínuna. Skilvirkni og afkastageta hafa ekki áhrif á úthlutaðan tíma. Ef keyrslutíminn er til dæmis skilgreindur sem 2 klukkustundir er úthlutaður tími 2 klst. óháð gildum í skilvirkni- og afkastagetureitum vinnustöðvarinnar.  

> [!NOTE]
> Afkastagetan sem er notuð í útreikningunum er skilgreind sem lágmarksgildið milli afkastagetu sem er skilgrein í vinnu- eða vélastöðinni og samhliða afkastagetunni sem er skilgreind fyrir leiðarlínuna. Ef vinnustöð er með afkastagetu 100, en samhliða afkastageta fyrir leiðarlínu er 2, mun *2* verða notað í útreikningunum.

*Tímalengd* aðgerðar tekur aftur á móti bæði skilvirkni og afkastagetu til greina. Tímalengd er reiknuð sem *Keyrslutími / Skilvirkni / Afkastageta*. Eftirfarandi listi sýnir nokkur dæmi um útreikning tímalengdar fyrir sama keyrslutímann sem er skilgreindur sem 2 klukkustundir fyrir leiðarlínuna:

- Skilvirkni 80% þýðir að þörf er á 2,5 klst. í stað tveggja tíma  
- Skilvirkni 200% þýðir að hægt er að ljúka verkinu á einni klukkustund. Hægt er að grafa gatið tvöfalt hratt ef um er að ræða uppgröftur sem er tvöfalt stærri en sá minni  

    Þú getur fengið sömu niðurstöður ef þú notar tvo smærri gröf í stað stórs. Nota *2* sem afkastagetu og *100%*  sem skilvirkni  

Brotin afkastageta er erfið. Við munum ræða það síðar í þessari grein. 

### <a name="setup-time"></a>Uppsetningartími

Úthlutun tíma fyrir uppsetningartímann fer eftir afkastagetu og er reiknaður sem *Uppsetningartími * afkastageta*. Ef afkastagetan er til dæmis stillt á *2* tvístrast úthlutaður uppsetningartími vegna þess að setja þarf upp tvær vélar fyrir aðgerðina.  

*Tímalengd* uppsetningartíma fer eftir skilvirkni og er reiknuð út sem *Uppsetningartími / skilvirkni*. 

- Skilvirkni 80% þýðir að þörf er á 2,5 klukkustundum í stað tveggja tíma til að setja upp.  
- Skilvirkni 200% merkir að hægt er að ljúka uppsetningu á 1 klukkustund í stað 2 klst. sem skilgreindar eru í leiðarlínunni.  

Brotastarfsemin er aðeins notuð í sérstökum tilvikum.

### <a name="work-center-processing-multiple-orders-simultaneously"></a>Vinnustöð sem vinnur úr mörgum pöntunum samtímis

Notum sprautunarklefa sem dæmi. Hún hefur sömu uppsetningu og keyrslutíma fyrir hverja unna lotu. En hver lota getur innihaldið margar stakar pantanir sem eru sprautaðar samtímis.  

Í þessu tilviki stjórnar uppsetningartíminn og samþ.g. afkastagetan kostnaðinum sem úthlutað er á pantanir. Mælt er með því að keyrslutími sé ekki notaður í leiðarlínum.  

Úthlutaður uppsetningartími fyrir hverja einstaka pöntun verður í öfugri röð við fjölda pantana (magns) sem er framkvæmd samtímis. Hér eru fleiri dæmi um útreikning uppsetningartíma þegar hann er skilgreindur sem tvær klukkustundir fyrir leiðarlínuna:

- Ef það eru tvær pantanir ætti samhliða afkastageta í leiðarlínunni að vera stillt á 0,5.

    Því er úthlutað afkastageta hverrar klukkustundar en lengd hverrar pöntunar helst í tvær klukkustundir.
- Ef það eru tvær pantanir með einn og fjórir í magn, þá verður samhliða afkastageta fyrir leiðarlínu fyrri pöntunar 0,2 og 0,8 fyrir þá seinni.  

    Þar af leiðandi er úthlutað afkastageta fyrstu pöntunarinnar 24 mín og 96 fyrir þá seinni. Lengd beggja pantana er áfram tveir tímar.  

Í báðum tilfellum er heildartími úthlutunar fyrir allar pantanir tvær klukkustundir.


### <a name="efficient-resource-can-dedicate-only-part-of-their-work-date-to-productive-work"></a>Skilvirkt tilfang getur úthlutað aðeins hluta af vinnudagsetningu þeirra í framleiðsluvinnu

> [!NOTE]
> Ekki er mælt með þessum aðstæðum. Mælt er með því að nota skilvirkni í staðinn. 

Ein af vinnustöðvunum þínum stendur fyrir reynslumikinn starfsmann sem vinnur verk með 100% skilvirkni. En hann getur aðeins helgað 50% af vinnutímanum í verk því hinn hluta tímans sinnir hann stjórnunarverkum. Þótt þessi starfsmaður geti lokið tveggja klukkustunda verki á nákvæmlega tveimur klukkustundum þarf samt að meðaltali að bíða aðrar tvær klukkustundir á meðan einstaklingurinn sinnir öðrum verkefnum.  

Úthlutaður keyrslutími er tvær klukkustundir og tímalengdin er fjórar klukkustundir.  

Ekki skal nota uppsetningartíma í slíkum tilfellum því [!INCLUDE [prod_short](includes/prod_short.md)] aðeins er úthlutað 50% af tímanum. Ef uppsetningartíminn er stilltur á *2* er úthlutaður uppsetningartími ein klukkustund og lengdin er tvær klukkustundir.

### <a name="consolidated-calendar"></a>Sameinað dagtal

Þegar reiturinn **Sameinað dagtal** er valið hefur vinnustöðin ekki sína eigin afkastagetu. Í staðinn jafngildir afkastagetan allri afkastagetu allra vélastöðva sem úthlutaðar eru vinnustöðinni.  

> [!NOTE]
> Skilvirkni vélastöðvarinnar er breytt í afkastagetu vinnustöðvarinnar.

Ef til dæmis tvær vélastöðvar eru með skilvirkni upp á 80 og 70 er skilvirkni í samstæðudagatalsfærslunni:

- Skilvirkni upp á 100
- Afkastageta 1,5
- Heildarafkastageta 12 klukkustundir (átta tíma vakt * 1.5 afkastageta).

> [!NOTE]
> Notaðu reitinn **Sameinað dagtal** þegar leiðir eru skipulagðar með tímasettum framleiðsluaðgerðum á stigi vélastöðvar, ekki stigi vinnustöðvar. Þegar dagatalið er sameinað verða síðan **Álag á vinnustöð** og skýrslur að yfirliti yfir samtals vinnuálag í öllum vélastöðvum sem úthlutaðar eru á vinnustöðina.

### <a name="example---different-machine-centers-assigned-to-a-work-center"></a>Dæmi - Mismunandi vélastöðvar sem úthlutað er á vinnustöð

Mikilvægt er að áætla hvaða afkastageta samanstendur af heildarafkastageta þegar vélastöðvar og vinnustöðvar eru sett upp.

Ef mismunandi vélastöðvum (t.d. 210 Pökkunarborð 1, 310 Málningarklefi...) er úthlutað á vinnustöð er mikilvægt að hafa einn afkastagetu vélastöðvanna verulega þar sem bilun í einni vélastöð getur truflað allt ferlið. Hægt er að færa inn vélarhópana eftir getu þeirra en eru ekki teknir með í áætlun. Ef slökkt er á **vífæringu samsteypudagatals** er aðeins afkastagetu vinnustöðvarinnar úthlutað í áætluninni. Afkastageta vélastöðvarinnar er undanskilin.

Ef hins vegar eru sams konar vélastöðvar (eins og 210 Pökkunarborð 1 og 220 Pökkunarborð 2) í vinnustöð má líta á vinnustöðina sem samtölu úthlutaðra vélastöðva. Þess vegna er vinnustöðin skráð með núll afkastagetu. Ef kveikt er á **vífærslum samsteypudagatals** er sameiginlegri afkastagetu úthlutað á vinnustöðina.

Ef ekki á að auka afkastagetu vinnustöðva í heildarafkastagetunni þarf að tilgreina **0** í reitnum **Skilvirkni** .

## <a name="to-set-up-a-capacity-constrained-machine-or-work-center"></a>Vinnu- eða vélastöð með takmarkaða afkastagetu sett upp

Setja þarf upp framleiðsluforða sem talinn er mikilvægur og merkja hann þannig að hann samþykki takmarkað álag í staðinn fyrir sjálfgefið, ótakmarkað álag sem annar framleiðsluforði samþykkir. Forði með takmarkaða afkastagetu getur verið vinnustöð eða vélastöð sem er flöskuháls og stofna þarf takmarkað, takmarkað álag fyrir.

[!INCLUDE[prod_short](includes/prod_short.md)] styður ekki nákvæma vinnusalarstjórnun. Hún áætlar hagkvæma nýtingu forða með því að útvega grófa áætlun, en býr ekki sjálfkrafa til og viðheldur nákvæmum áætlunum út frá forgangsröðun eða reglur um hagræðingu.

Á síðunni **Forði** sem er takmarkaður afkastageta er hægt að stofna uppsetningu til að koma í veg fyrir að forði verði ofálagður. Uppsetningin getur einnig tryggt að afkastageta sé ekki skilin eftir óúthlutað ef hún gæti aukið við tíma framleiðslupöntunar. Í reitnum **Hömlur (% af heildar afkastagetu)** má bæta við hömlutíma á tilföng til að draga úr skiptingu aðgerðar. Þessi stilling gerir kerfinu kleift að tímasetja álag á síðasta mögulega degi með því að fara örlítið yfir álagsprósentuna. Ef álagsprósentan er hærri getur það dregið úr fjölda aðgerða sem er skipt.

Þegar áætlanir [!INCLUDE [prod_short](includes/prod_short.md)]  eru gerðar með forða með skorðuðum afkastagetu tryggir að forðinn sé ekki hlaðinn yfir afkastagetu (bundinn álag). Hún úthlutar hverri aðgerð næstu tímarauf. Ef tímaröðin er ekki nógu stór til að ljúka allri aðgerðinni er aðgerðinni skipt í tvo eða fleiri hluta í næstu tímaraufum.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Tilföng takmarkaðrar afkastagetu** og velja síðan viðkomandi tengil.
2. Valið er aðgerðin **Nýtt**.
3. Fyllið inn í reitina eftir þörfum.

> [!NOTE]
> Aðgerðir á vinnustöðvum eða vélastöðvum sem eru settar upp sem takmarkaður forði eru alltaf áætlaðar í rað. Þessi áætlun merkir að ef takmarkaður forði hefur marga afkastagetu verður að áætla getuna í röðinni. Ekki er hægt að áætla þær samhliða eins og þær væru ef vinnu- eða vélastöðin væri ekki sett upp sem skorinn forði. Ef forðinn er takmarkaður **er reiturinn Geta** í vinnu- eða vélastöðinni meiri en **1**.

> Ef vinnsluaðgerðum er skipt er uppsetningartíma aðeins úthlutað einu sinni vegna þess að gert er ráð fyrir að einhver handvirk leiðrétting sé gerð til að fínstilla áætlunina.

## <a name="see-also"></a>Sjá einnig .

[Stofna dagatal verkstæðis](production-how-to-create-work-center-calendars.md)  
[Uppsetning framleiðslu](production-configure-production-processes.md)  
[Framleiðsla](production-manage-manufacturing.md)  
[Áætlun](production-planning.md)  
[Birgðir](inventory-manage-inventory.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
