---
title: Skrá neyslu eða notkun á tilföngum og hlutum verks
description: Í greininni er fjallað um hvernig skrá skuli notkun eða notkun vara eða fjármuna fyrir störf í verkefnastjórnun.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 03/08/2023
ms.custom: bap-template
---
# Skrá neyslu eða notkun fyrir verk

 **Á síðunni vinnsluspjald**  er hægt að opna  **síðuna verkáætlunarlínur**  til að skoða og skrá notkun á ýmsum hlutum vinnslunnar. Þessar upplýsingar eru sjálfkrafa uppfærðar þegar verið er að breyta og flytja upplýsingar milli verka og verkbóka eða verkreikninga. Þetta krefst þess að kveikt sé á  **tengilinn nota notkun eftir sjálfgefna**  víxlun á  **síðu verkuppsetningar** . Frekari upplýsingar í  [Setja upp störf](projects-how-setup-jobs.md).  

Fyrir áætlunarlínur af gerðinni  **áætlun** er til dæmis hægt að færa inn magn forða og tilgreina síðan magnið sem á að flytja í verkbókina. Ef gerð áætlunarlínunnar er  **innheimt** er hægt að færa inn magn forðarinnar og tilgreina síðan magnið sem á að millifæra á reikning. Til að fræðast meira um reikningsfærslu á viðskiptamanninum er farið í  [Reikningsvinnslur](projects-how-invoice-jobs.md). Með því að bera saman upprunalegt magn, eftirstöðvar magns eða bókað magn er fljótlegt að skoða upplýsingar um notkun. Til að fræðast nánar um hvernig á að áætla áætlað virði við áætlanagerð er farið í til að  [stjórna verkáætlunum](projects-how-manage-budgets.md).  

Eftirfarandi ferli lýsa hvernig á að skrá raunverulegt (áætlað) magn og kostnað með verkbók. Einnig er hægt að nota innkaupaskjöl til að skrá innkaup fyrir verk. Frekari upplýsingar fást hjá  [Verkbirgðum](projects-how-manage-project-supplies.md).

## Til að skrá notkun fyrir verkáætlunarlínu af gerðinni Áætlun

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verk** og velja síðan viðkomandi tengil.  
2. Velja vinnsluna og velja  **síðan aðgerðina áætlunarlínur** . 
3. Veljið verkáætlunarlínu af gerðinni **Áætlun** eða **Bæði fjárhagsáætlun og reikningshæft** sem á að skrá notkun fyrir.   

    > [!NOTE]
    > Þú getur einnig skráð notkun fyrir verkáætlunarlínu af gerðinni **Reikningshæf**. Yfirleitt eru þessar línur notaðar til að stofna reikninga en einnig er hægt að flytja upplýsingarnar í færslubók. Frekari upplýsingar um  [Reikningsstörf](projects-how-invoice-jobs.md) 

4. Í reitnum  **Magn. Ef flytja á í Færslubókarreit**  er fært inn magnið sem á að flytja. Sjálfgefna gildið er sama magn og það sem er í reitnum **Magn**.

    Reiturinn magn  **sem eftir er**  sýnir magnið sem á eftir að ljúka vinnslunni og flytja í færslubókina.
5. Velja skal aðgerðina **Stofna verkbókarlínur**.

    > [!TIP]
    > Ef ætlunin er að bæta við fleiri verkáætlunarlínum fyrir þetta verk skal bíða með þetta skref þar til öllum verkáætlunarlínum hefur verið bætt við.
6. Á síðunni **Verk - Flytja verkáætlunarlínu** skal fylla reiti út eftir þörfum og velja síðan hnappinn **Í lagi**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Velja skal aðgerðina **Opna verkbók**.  
8. Á síðunni **Verkbók** skal velja viðeigandi línu og svo aðgerðina **Bóka**.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

9. Á síðunni **Verkáætlunarlínur** skal fara yfir skráða notkun með því að athuga reitina **Magn**, **Eftirstöðvar (magn)** og **Magn til flutnings í færslubók**.  
10. Endurtakið skref 3 til 8 til að skrá frekari notkun.  

## Til að búa til verkbókarlínur handvirkt

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verkbækur** og velja síðan viðkomandi tengil.  
2. Í reitnum **Heiti keyrslu** skal velja viðeigandi verkbókarkeyrslu.  
3. Sláið inn skjalanúmer, verknúmer, verkhlutanúmer, tegund og magn tegundarinnar sem verið er að nota í nýja línu.  
4. Þegar verkbókarlínurnar eru tilbúnar skal velja aðgerðina **Bóka**.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## Til að skoða áætlanir um verknotkun og bóka uppfærslur

Skoða má verknotkun allt að lokum verkefnis í einu skrefi. Til þess er notuð keyrslan **Verk - Reikna eftirstandandi notkun** fyrir alla verkhluta allt að og með lokum verks.  

Á þennan hátt má rekja og bera saman upprunalega áætlun við raunverulegar niðurstöður og gera breytingar eða bæta við færslum eftir þörfum. Taka má dæmi af notanda sem hefur áætlað að verk taki 10 klukkustundir en það hefur þegar tekið 15 klukkustundir. Hann getur bætt klukkustundunum fimm við færslubókarlínu sem fyrir er eða búið til nýja færslubókarlínu til að skilgreina þessa fimm tíma sem yfirvinnu, sem er önnur tegund vinnu. Raunkostnaður og verð eru reiknuð út, sem svo er hægt að bóka í færslubókina.  

> [!NOTE]  
> Birgðafærslur stofna færslur í birgðahöfuðbók og minnka birgðamagn. Keyrslan **Bóka birgðabreytingar** færir kostnaðinn úr birgðum í fjárhag. Forðafærslur stofna forðafærslur.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verkbækur** og velja síðan viðkomandi tengil.  
2. Veljið viðeigandi verkbók og veljið svo aðgerðina **Reikna eftirstandandi notkun**.  
3. Á síðunni **Verk - Reikna eftirstandandi notkun** skal slá inn númer skjalsins og bókunardagsetninguna sem færa skal í bókina og velja svo hnappinn **Í lagi**.  
4. Uppfærið bókina með þeim breytingum sem kann að vera þörf á.  
5. Veljið **Bókun**.

## Stofna tínsluskjöl birgða og vöruhúss fyrir verk

Til að búa til tínsluskjöl birgða og vöruhúss fyrir verk verður stjórnandinn að virkja **Uppfærsla eiginleika: Virkja birgða- og vöruhúsatínslu úr verkum** á síðunni **Eiginleikastjórnun**.

Eiginleikinn bætir aðgerðunum **Stofna birgðatínslu** og **Stofna vöruhúsatínslu** í **Verkspjaldinu**. Til að búa til eða skrá tínsluskjal skal nota aðgerðina **Frágangur/tínslulínur/hreyfingarlínur** eða **Skráðar tínslulínur**.  [Frekari upplýsingar um streymi fyrir framleiðslu, samsetningu og vinnslur](design-details-internal-warehouse-flows.md).

Hægt er að nota aðgerðirnar við eftirfarandi skilyrði:

* **Staða** verksins er **Opin**.
* **Línugerð** verkáætlunarlínunnar er **Fjárhagsáætlun** eða **Bæði fjárhagsáætlun og reikningshæft**.
* **Tegund** verkáætlunarlínunnar er **Vara**.
* **Krefjast tínslu** er virkjuð fyrir tengda birgðageymslu.
* **Stýrð tínsla og frágangur** er gerð óvirk.

> [!NOTE] 
> Þótt stillingin kallist **Krefjast tínslu** er enn hægt að bóka notkun beint úr verkbókarlínunni fyrir birgðageymsluna. Ef birgðageymslan er sett upp til að krefjast tínsluvinnslu en ekki afhendingarvinnslu notarðu síðuna **Birgðatínsla** til að skipuleggja og prenta tínsluupplýsingar. Þú notar einnig síðuna til að færa inn og bóka niðurstöður tínslunnar, sem í staðinn bókar notkun á vörunum. 
> 
> Ef birgðageymslan er sett upp til að þurfa bæði tínslu- og afhendingarvinnslu, þ.e. báðir reitirnir **Krefjast tínslu** og **Krefjast afhendingar** hafa verið valdir á síðunni **Birgðageymsluspjald**, skal nota síðuna **Vöruhúsatínsla** til að afgreiða tínsluna. Vöruhúsatínslur eru svipaðar og birgðatínslur. Munurinn er sá að í stað þess að bóka tínsluupplýsingarnar skráirðu tínsluna. Þessi skráning bókar ekki notkun, hún gerir bara vörurnar tiltækar fyrir bókun. Sem stjórnandi vöruhúss, geturðu notað tínsluvinnublað til að flokka tínsluupplýsingar áður en þú stofnar einstakar tínsluleiðbeiningar vöruhússins

## Til að fara yfir áætlunarlínur verkfærslu

Þegar verkbókarlínur hafa verið bókaðar er hægt að sjá þær áætlunarlínur sem tengjast þeim verkbókarfærslum sem hafa verið bókaðar.

> [!NOTE]  
> Þetta krefst þess að gátreiturinn **Nota notkunartengil** sé valinn fyrir verkið. Frekari upplýsingar eru í [Setja upp verk](projects-how-setup-jobs.md).  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verkbækur** og velja síðan viðkomandi tengil.  
2. Veljið viðeigandi verkbók og veljið svo aðgerðina **Færslur**.  
3. Á síðunni **Verkfærslur** er aðgerðin **Sýna áætlunarlínur verks** valin.

## Sjá tengda [Microsoft þjálfun](/training/paths/post-job-usage-sales/)

## Sjá einnig .

[Verkefnastjórnun](projects-manage-projects.md)  
[Fjármál](finance.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Sala](sales-manage-sales.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
