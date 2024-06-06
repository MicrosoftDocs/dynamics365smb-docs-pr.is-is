---
title: Skrá notkun eða notkun verkforða og vara
description: Í þessari grein er því lýst hvernig skrá skal notkun eða notkun á vörum eða forða í verkefnum í verkefnastjórnun.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 02/22/2024
ms.custom: bap-template
---
# <a name="record-consumption-or-usage-for-projects"></a>Skrá notkun eða notkun fyrir verk

Á síðunni **Verkspjald** er hægt að opna **síðuna Áætlunarlínur** verkefnis til að fara yfir og skrá notkun á ýmsum hlutum verkefnisins. Þessar upplýsingar eru uppfærðar sjálfkrafa þegar upplýsingum er breytt og þær fluttar milli verka og verkbóka eða verkreikninga. Þetta krefst þess að kveikt sé á beita **notkunartenglinum sjálfgefið** á síðunni **Verkuppsetning** . Nánari upplýsingar um [Uppsetning verkefna](projects-how-setup-jobs.md).  

Til dæmis er hægt að færa inn magn forða fyrir áætlunarlínur af tegundinni **Áætlun** og tilgreina síðan magnið sem á að flytja í verkbókina. Ef tegund áætlunarlínunnar er **Reikningshæft** er hægt að færa inn magn forðans og tilgreina síðan magnið sem á að flytja á reikning. Nánari upplýsingar um reikningsfærslu viðskiptavinarins eru í [Reikningsfæra](projects-how-invoice-jobs.md) verkefni. Með því að bera saman upphaflegt magn, eftirstöðvar eða bókað magn er fljótlegt að fara yfir notkunarupplýsingar. Nánari upplýsingar um hvernig á að meta áætluð gildi við áætlun er farið í [Vinna með verkáætlanir](projects-how-manage-budgets.md).  

Eftirfarandi leiðbeiningar lýsa því hvernig á að skrá raunverulegt (áætlað) magn og kostnað í verkbók. Einnig er hægt að nota innkaupaskjöl til að skrá innkaup fyrir verkefni. Fræðast meira um [verkbirgðir](projects-how-manage-project-supplies.md).

## <a name="to-record-usage-for-a-project-planning-line-of-type-budget"></a>Til að skrá notkun fyrir verkáætlunarlínu af gerðinni Áætlun

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Verkefni** og velja síðan viðeigandi tengil.  
2. Veljið verkið og veljið svo aðgerðina **Áætlunarlínur verks** . 
3. Velja skal verkáætlunarlínu af gerðinni **Áætlun** eða **Bæði áætlun og reikningshæft** sem skrá á notkun fyrir.   

    > [!NOTE]
    > Einnig er hægt að skrá notkun fyrir verkáætlunarlínu af gerðinni **Reikningshæft**. Þessar línur eru yfirleitt notaðar til að stofna reikninga en einnig er hægt að flytja upplýsingarnar í færslubók. Fræðast meira um [reikningsverkefni](projects-how-invoice-jobs.md) 

4. Í reitnum **Magn Til að flytja í færslubók** er magnið sem á að millifæra fært inn. Sjálfgefna gildið er sama magn og það sem er í reitnum **Magn**.

    Reiturinn **Eftirstöðvar (magn**) sýnir það magn sem eftir er til að ljúka verkefninu og flytja í færslubókina.
5. Veljið aðgerðina **Stofna verkbókarlínur** .

    > [!TIP]
    > Ef bæta á við fleiri verkáætlunarlínum fyrir þetta verkefni skal bíða með þetta skref þar til öllum verkáætlunarlínum hefur verið bætt við.
6. Á síðunni **Verkflutningur verkáætlunarlína** skal fylla út reitina eins og þörf krefur og velja svo hnappinn **Í lagi** . [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Veljið aðgerðina **Opna verkbók** .  
8. Á síðunni **Verkbók** skal velja viðeigandi línu og velja svo aðgerðina **Bóka** .

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

9. Á síðunni **Áætlunarlínur** verkefnis skal fara yfir skráða notkun með því að **fylgjast með Magn**, **Eftirstöðvar (magn**) og **Magn. Til að flytja í færslubókarreiti** .  
10. Endurtakið skref 3 til 8 til að skrá frekari notkun.  

## <a name="to-create-project-journal-lines-manually"></a>Til að stofna verkbókarlínur handvirkt

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **verkbækur** og velja síðan viðeigandi tengil.  
2. Í reitnum **Heiti** keyrslu skal velja viðeigandi verkbókarkeyrslu.  
3. Í nýja línu skal færa inn fylgiskjalsnúmer, verknúmer, verkhlutanúmer, gerð og magn tegundarinnar sem verið er að nota.  
4. Þegar verkbókarlínurnar eru tilbúnar skal velja aðgerðina **Bóka** .  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## <a name="to-view-project-usage-estimates-and-post-updates"></a>Til að skoða áætlanir um notkun verks og bóka uppfærslur

Hægt er að skoða verknotkun allt að lokum verks í einu þrepi. Til þess er keyrslan Reikna eftirstandandi notkun **verks notuð** fyrir alla verkhluta allt að og með lokum verks.  

Á þennan hátt má rekja og bera saman upprunalega áætlun við raunverulegar niðurstöður og gera breytingar eða bæta við færslum eftir þörfum. Til dæmis gæti verið búið að áætla að verk þarf 10 klukkustundir og það hafi tekið 15 klukkustundir. Hann getur bætt klukkustundunum fimm við færslubókarlínu sem fyrir er eða búið til nýja færslubókarlínu til að skilgreina þessa fimm tíma sem yfirvinnu, sem er önnur tegund vinnu. Raunkostnaður og verð eru reiknuð út, sem svo er hægt að bóka í færslubókina.  

> [!NOTE]  
> Birgðafærslur stofna færslur í birgðahöfuðbók og minnka birgðamagn. Keyrslan **Bóka birgðabreytingar** færir kostnaðinn úr birgðum í fjárhag. Forðafærslur stofna forðafærslur.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **verkbækur** og velja síðan viðeigandi tengil.  
2. Veljið viðeigandi verkbók og veljið svo aðgerðina **Reikna eftirstandandi notkun** .  
3. Á síðunni **Reiknaðar eftirstöðvar notkunar** verks skal færa inn númer fylgiskjalsins og bókunardagsetninguna sem setja á inn í færslubókina og velja svo hnappinn **Í lagi** .  
4. Uppfærið bókina með þeim breytingum sem kann að vera þörf á.  
5. Veljið **Bókun**.

## <a name="create-inventory-and-warehouse-pick-documents-for-a-project"></a>Stofna birgða- og vöruhúsatínsluskjöl fyrir verk

Nota aðgerðirnar Stofna birgðatínslu **og** **Stofna vöruhúsatínslu** á síðunni **Verkspjald** . Til að búa til eða skrá tínsluskjal skal nota aðgerðina **Frágangur/tínslulínur/hreyfingarlínur** eða **Skráðar tínslulínur**. Nánari upplýsingar um [Flæði fyrir framleiðslu, samsetningu og verkefni](design-details-internal-warehouse-flows.md).

Hægt er að nota aðgerðirnar við eftirfarandi skilyrði:

*  **Staða** verksins er **Opin**.
* Línugerð **verkáætlunarlínunnar er** Áætlun **eða** Bæði áætlun og Reikningshæft **.**
*  **Gerð** verkáætlunarlínunnar er **Vara**.
* **Krefjast tínslu** er virkjuð fyrir tengda birgðageymslu.
* **Stýrð tínsla og frágangur** er gerð óvirk.

> [!NOTE] 
> Þó svo að stillingin sé kölluð **Krefjast tínslu** er samt hægt að bóka notkun beint úr verkbókarlínunni fyrir birgðageymsluna. Ef birgðageymslan er sett upp til að krefjast tínsluvinnslu en ekki afhendingarvinnslu notarðu síðuna **Birgðatínsla** til að skipuleggja og prenta tínsluupplýsingar. Þú notar einnig síðuna til að færa inn og bóka niðurstöður tínslunnar, sem í staðinn bókar notkun á vörunum. 
> 
> Ef birgðageymslan er sett upp til að þurfa bæði tínslu- og afhendingarvinnslu, þ.e. báðir reitirnir **Krefjast tínslu** og **Krefjast afhendingar** hafa verið valdir á síðunni **Birgðageymsluspjald**, skal nota síðuna **Vöruhúsatínsla** til að afgreiða tínsluna. Vöruhúsatínslur eru svipaðar og birgðatínslur. Munurinn er sá að í stað þess að bóka tínsluupplýsingarnar skráirðu tínsluna. Þessi skráning bókar ekki notkun, hún gerir bara vörurnar tiltækar fyrir bókun. Sem stjórnandi vöruhúss, geturðu notað tínsluvinnublað til að flokka tínsluupplýsingar áður en þú stofnar einstakar tínsluleiðbeiningar vöruhússins

## <a name="to-review-planning-lines-for-a-project-ledger-entry"></a>Til að fara yfir áætlunarlínur fyrir verkfærslu

Þegar verkbókarlínur hafa verið bókaðar er hægt að sjá áætlunarlínurnar sem tengjast verkbókarfærslunum sem hafa verið bókaðar.

> [!NOTE]  
> Þetta krefst þess að gátreiturinn **Beita notkunartengli** hafi verið valinn fyrir verkið. Nánari upplýsingar eru í [Setja upp verkefni](projects-how-setup-jobs.md).  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **verkbækur** og velja síðan viðeigandi tengil.  
2. Veljið viðeigandi verkbók og veljið **svo Fjárhagsfærslur** .  
3. Á síðunni **Verkfærslur** skal velja **Sýna tengdar áætlunarlínur** .

## <a name="see-also"></a>Sjá einnig .

[Verkefnastjórnun](projects-manage-projects.md)  
[Fjármál](finance.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Sala](sales-manage-sales.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
