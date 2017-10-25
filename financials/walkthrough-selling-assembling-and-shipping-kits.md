---
title: Kynning - Selja, setja saman og afhenda sett | Microsoft Docs
description: "Til að styðja tímanlegar birgðir og getuna til að sérsníða vörur eftir þörfum viðskiptavina er hægt að búa til og tengja samsetningarpantanir sjálfkrafa um leið og sölupöntunarlínan er búin til. Tengingin milli sölueftirspurnarinnar og framboðssamsetningar gerir sölupantanagjörvum mögulegt að sérsníða samsetningaríhlutinn og lofar afhendingardagsetningum samkvæmt framboði íhluta. Auk þess bókast samsetningarfrálag og -notkun sjálfkrafa með afhendingu tengdu pöntunarinnar."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: d87aa7fe44b183a823457be4448c84631cd75db6
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="walkthrough-selling-assembling-and-shipping-kits"></a>Kynning: Selja, setja saman og afhenda sett
Til að styðja tímanlegar birgðir og getuna til að sérsníða vörur eftir þörfum viðskiptavina er hægt að búa til og tengja samsetningarpantanir sjálfkrafa um leið og sölupöntunarlínan er búin til. Tengingin milli sölueftirspurnarinnar og framboðssamsetningar gerir sölupantanagjörvum mögulegt að sérsníða samsetningaríhlutinn og lofar afhendingardagsetningum samkvæmt framboði íhluta. Auk þess bókast samsetningarfrálag og -notkun sjálfkrafa með afhendingu tengdu pöntunarinnar.  

Sérstök virkni er til staðar til að stýra sendingu sameiningarpöntunarmagns, bæði í venjulegri og ítarlegri vöruhúsagrunnstillingu. Þegar starfsmenn sem bera ábyrgð á samsetningu ljúka við að setja saman magnið sem setja á saman í pöntun að hluta til eða í heild skrá þeir það í reitinn **Magn til afhendingar** í vöruhúsasendingarlínunni, í ítarskilgreiningum, og velja svo **Bóka afhend.** Niðurstaðan er að samsvarandi samsetningarfrálag er bókað, að meðtalinni tengdri íhlutanotkun, og söluafhending fyrir magnið er bókuð fyrir tengdu sölupöntunina. Þessi kynning skýrir ítarlega vöruhúsaferlið.  

Í einfaldri vöruhúsagrunnstillingu, þegar magn samsetningarpöntunar er tilbúið til afhendingar, bókar starfsmaður í vöruhúsi birgðatínslu fyrir sölupöntunarlínuna. Þetta stofnar birgðahreyfingu fyrir íhlutina, bókar samsetningarfrálagið og sölupöntunarsendinguna. Nánari upplýsingar eru í hlutanum „Meðhöndlun íhluta pantanasamsetninga við birgðatínslu” í Birgðatínsla.  

## <a name="about-this-walkthrough"></a>Um kynninguna  
Þessi kynning fjallar um eftirfarandi verk:  

### <a name="setting-up-assembly-items"></a>Uppsetning Samsetningaríhlutir.  
Einkennandi fyrir samsetningarvörur er áfyllingarkerfi þeirra og samsetningaruppskriftin. Samsetningarstefna vörunnar getur annaðhvort verið samsetning-til-pöntunar (ATO) eða samsetning-í-birgðir (ATS). Í þessum hluta er fjallað um eftirfarandi verkhluta:  

-   Uppsetning viðeigandi áfyllingarkerfis og samsetningarreglu á nýja samsetningarvöruspjaldinu.  
-   Stofnun samsetningaruppskriftar sem skráir samsetningaríhlutina og forðann sem fara í samsetningarvöruna.  

### <a name="selling-customized-assembly-items"></a>Sala sérsniðinna samsetningaríhluta  
[!INCLUDE[d365fin](includes/d365fin_md.md)] veitir þann sveigjanleika að geta fært inn bæði magn birgða og magn samsetningarpöntunar í eina sölupöntunarlínu. Í þessum hluta er fjallað um eftirfarandi verkhluta:  

-   Stofnun á hreinni ATO sölupöntunarlínu þar sem ekki er allt magn tiltækt og verður að setja saman fyrir afhendingu.  
-   Sérstilling á ATO vörum.  
-   Endurreiknar einingarverð sérsniðinnar samsetningarvöru.  
-   Stofnun blandaðrar sölupöntunarlínu þar sem hlutar af sölumagninu koma úr birgðum og það sem eftir stendur verður að setja saman fyrir afhendingu.  
-   Að skilja ATO-ráðstöfunarviðvaranir.  

### <a name="planning-for-assembly-items"></a>Áætlun fyrir samsetningaríhluti  
Samsetningareftirspurn og -framboð eru meðhöndluð með áætlunarkerfinu, rétt eins og fyrir innkaup, flutning og framleiðslu. Í þessum hluta er fjallað um eftirfarandi verkhluta:  

-   Að keyra endurgerðaráætlun fyrir vörur sem hafa sölueftirspurn fyrir samsett framboð.  
-   Myndar samsetningarpöntun til að uppfylla magn í sölulínu fyrir áskilda afhendingardagsetningu.  

### <a name="assembling-items"></a>Samsetning á vörum  
Samsetningarpantanir virka á svipaðan hátt og framleiðslupantanir, nema að notkun og frálag eru skráð og bókuð beint úr pöntuninni. Þegar vörurnar eru settar saman í birgðir, hefur samsetningarstarfsmaðurinn fullan aðgang að öllum haus- og línureitum. Þegar vörurnar eru settar saman í pöntun þar sem magni og röðunardagsetningum er lofað til viðskiptavinar er ekki hægt að breyta ákveðnum reitum í samsetningarpöntuninni. Í því tilfelli er samsetning bókuð úr vöruhúsaafhendingu tengdrar sölupöntunar. Í þessum hluta er fjallað um eftirfarandi verkhluta.  

-   Skráningu og bókun samsetningarnotkunar og -frálags í birgðir.  
-   Farið í vöruhúsaafhendingarlínuna úr ATO-samsetningarpöntun til að skrá samsetningarvinnu.  
-   Farið í ATO-samsetningarpöntun úr vöruhúsaafhendingarlínu til að endurskoða sjálfvirkt innfærð gögn.  

### <a name="shipping-assembly-items-from-stock-and-assembled-to-order"></a>Afhenda Samsetningarvörur úr Birgðir og Sett saman í pöntun  
Sérstakar virkni er til staðar til að stýra sendingu af sameiningarpantanamagni. Í þessum hluta er fjallað um eftirfarandi verkhluta:  

-   Stofnun vöruhúsatínslu fyrir samsetningarvörur í birgðum og fyrir samsetningaríhluti sem á að setja saman fyrir afhendingu.  
-   Skráning vöruhúsatínslu fyrir samsetningaríhluti og síðan fyrir samsetningarvörur.  
-   Farið í samsetningarpöntun úr vöruhúsaafhendingu til að endurskoða tínda eða notaða íhluti.  
-   Afhenda samsetningarpöntunarmagn.  
-   Afhending birgðasamsetningarvörur.  

## <a name="roles"></a>Hlutverk  
Þessi kynning sýnir þau verk sem framkvæmd eru með eftirfarandi hlutverkum notenda:  

-   Sölupöntunarvinnsla  
-   Áætlun  
-   Samsetningarstarfsmaður  
-   Tínslumaður  
-   Afhending Ábyrgðaraðili  

## <a name="prerequisites"></a>Frumskilyrði  
Áður en hægt er að framkvæma verk hér í kynningunni þarf að gera eftirfarandi:  

-   Setja upp [!INCLUDE[d365fin](includes/d365fin_md.md)].  
-   Gera notanda að starfsmanni vöruhúss í hvítri birgðageymslu á eftirfarandi hátt:  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **starfsmenn vöruhúss** og velja svo viðeigandi tengil.  
2.  Velja reitinn **Notandakenni** og velja síðan eigin notandareikning notanda í glugganum **Notendur**.  
3.  Í reitnum **Birgðageymslu kóti** færið inn HVÍTT.  
4.  Veljið reitinn **Sjálfgefið**.  

Birgðageymslan HVÍTT er undirbúin fyrir samsetningu í eftirfarandi skrefum:  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Staðsetningar** og velja svo viðeigandi tengil.  
2.  Opna birgðageymsluspjaldið fyrir hvíta birgðageymslu.  
3.  Á flýtiflipanum **Hólf** færið inn **W-10-0001** í reitinn **Í samsetningu hólfakóði**.  

    Með því að færa inn þennan hólfkóta sem ekki er til tínslu, eru allar samsetningarpöntunarlínurnar tilbúnar til móttöku íhluta þeirra í hólfinu.  

4.  Í reitinn **Úr samsetningu hólfakóði** er fært inn **W-01-0001**.  

    Með því að færa inn þennan tínsluhólfkóta, verður loknar samsetningarvörur keyrðar út úr hólfinu.  

Fjarlægja skal sjálfgefinn afhendingartíma fyrir innri ferli á eftirfarandi hátt:  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Framleiðsluuppsetning** og velja svo viðeigandi tengil.  
2.  Í glugganum **Framleiðsluuppsetning** á flýtiflipanum **Áætlun** er gildið fjarlægt í reitnum **Sjálfgefið öryggisforskot**.  

Stofna birgðir fyrir samsetningaríhluti með því að fara eftir hlutanum "Undirbúa sýnigögn" í þessari leiðsögn.  

## <a name="story"></a>Ferill  
Þann 23. janúar, tekur Súsanna, sem sér um úrvinnslu sölupantanna, við pöntun frá Verkstæðinu fyrir þrjár einingar af Setti B, sem er ATO-vara. Allar þrjár einingarnar eru sérsniðnar og verða að innihalda öflug skjákort og auka RAM-einingu. Diskadrifin eru uppfærð í DWD, vegna þess að CD drif eru ekki tiltæk. Súsanna veit að hægt er að setja einingarnar saman strax, þannig að hún lætur ráðlagða sendingardagsetningu vera 23. janúar  

Á sama tíma pantar viðskiptamaðurinn fimmtán einingar af setti A með sérstakri beiðni um að fimm einingar verði sérstilltar þannig að þær innihaldi öflugt skjákort. Þótt sett A sé yfirleitt birgðasamsetningarvara, sameinar pantanavinnslan sölulínumagnið til að selja tíu einingar úr birgðum og sameina fimm sérsniðnar einingar svo hægt sé að vinna pöntunina. Tíu einingar af setti A eru ekki tiltækar og þurfa að berast í birgðir fyrst í gegnum samsetningarpöntun samkvæmt samsetningarstefnu vörunnar. Súsanna fær að vita frá samsetningardeild að ekki sé hægt að ljúka við einingar úr samstæðu A í núverandi viku. Hún stillir afhendingardagsetningu seinni sölupöntunarlínunnar, fyrir blandað ATO og birgðamagn, á 27. janúar og upplýsir viðskiptamann um að 15 einingar af setti A verði afhentar fjórum dögum síðar en einingarnar þrjár úr setti B. Til að gefa sendingardeild merki um að þessi sölupöntun krefjist samsetningar, stofnar Susan vöruhúsaafhendingarfylgiskjal úr sölupöntuninni.  

Erla, stjórnandinn, keyrir áætlunarvinnublaðið og myndar samsetninarpöntun fyrir tíu staðaleiningar af setti A með innri gjalddaga 27. janúar.  

Sammy, sem ber ábyrgð á afhendingu, fær þrjár vöruhúsaafhendingarlínur fyrir sölupöntunina: Eina línu fyrir þrjár hreinar ATO-einingar, eina fyrir ATO-einingarnar fimm í blönduðu sölupöntunarlínunni og eina fyrir ATS-einingarnar tíu í blönduðu sölupöntunarlínunni. Hann stofnar vöruhúsatínsluskjal fyrir alla samsetningaríhluti sem þarf fyrir samsetningu allt að átta ATO-eininga í vöruhúsaafhendingarskjalinu.  

John, tínslumaðurinn, sækir íhluti fyrir allt ATO-magn á vöruhúsaafhendingarskjalinu og kemur því á samsetningarsvæðið. Hann færir inn magn til afgreiðslu og skráir vöruhúsatínslu.  

Linda setur saman þrjár ATO einingar af Setti B. Íhlutirnir eru þegar tíndir og hún skráir ekki frálag og notkun magns eða bókar pöntunina vegna þess að báðar af þessum aðgerðum eru gerðar sjálfkrafa gegnum tengdar vöruhúsaafhendingarlínur.  

Sammy skráir samsett magn í birgðaafhendingarlínuna og bókar afhendingu þriggja eininga af setti B. Fyrsta lína sölupöntunarinnar uppfærist sem afhent. Tengda samsetningarpöntunin er opin þar til sölupöntunin er reikningsfærð að fullu. Vöruhúsaafhendingarlínurnar tvær, ein ATO og ein ATS, fyrir sett A með skiladagsetningar 27. janúar, eru áfram opnar.  

Þann 27. janúar meðhöndlar Linda tvær samsetningarpantanir fyrir Sett A. Fyrri pöntunin er ATO-pöntun upp á fimm einingar sem hún meðhöndlar á annan hátt en ATO-pöntunin fyrir Sett B sem hún meðhöndlaði 23. janúar. Í þeirri pöntun hefur hún sjálf heimild til að fá aðgang að vöruhúsaafhendingarlínunni að skrásetja lokinni samsetningarvinnu. Tilskildir íhlutir eru tilbúnir í samsetningardeild, þar sem þeir voru tíndir til ásamt íhlutunum fyrir sett B.  

Seinni samsetningarpöntunin er ATS pöntun fyrir tíu einingar sem stofnaðar voru af áætlunarkerfinu. Í þessari ATS pöntun, framkvæmir Linda allar aðgerðir sem tengjast samsetningarpöntuninni. Hún stofnar vöruhússtínsluskjal fyrir samsetningaríhlutina sem þörf er á til að setja saman einingarnar tíu. Þegar tölvurnar eru settar saman bókar Linda samsetningarpöntunina og gefur þannig til kynna að vörurnar séu tiltækar í birgðum og hægt sé að tína þær fyrir afhendingu.  

Sammy stofnar vöruhúsatínsluskjal fyrir eftirstandandi magn áður en birgðaafhending er bókun. Tínsluskjal er stofnap fyrir tíu einingar af setti A sem var að ljúka. Íhlutirnir sem þarf til að setja saman fimm einingar af Samsetningu A til pöntunar, voru tíndir til 23. janúar.  

John kemur með tíu einingar af setti A úr vöruhúsinu á tilgreint afhendingarsvæði, skráir magnið til afgreiðslu og skráir síðan tínsluna.  

Sammy pakkar tíu ATS-einingar með ATO-einingunum fimm sem Linda setti saman fyrr sama dag. Hann færir magn til afhendingar inn í báðar línur og bókar síðan fyrir síðustu afhendingu fyrir Tækjabúðina. Tengdar samsetningarpantanir fyrir fimm einingar af setti A eru sjálfkrafa bókaðar. Seinni línan í sölupöntuninni er uppfærð sem afhent. Tvær tengdar samsetningarpantanir haldast opnar þar til sölupöntunin er reikningsfærð og henni lokað.  

Þegar sölupöntunin er bókuð síðar sem fullkomlega reikningsfærð eru sölupöntunin og tengdu samsetningarpantanirnar fjarlægðar.  

## <a name="setting-up-the-sample-data"></a>Uppsetning sýnigagna  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Birgðabækur vöruhúss** og velja svo viðeigandi tengil.  
2.  Velja reitinn **Heiti keyrslu** og velja síðan sjálfgefnu færslubókina.  
3.  Stofna jákvæðar breytingar á birgðum í hvítri birgðageymslu á vinnudagsetningunni, 23. janúar, með því að færa inn eftirfarandi upplýsingar.  

    |**Vörunr.**|**Svæðiskóti**|**Hólfkóti**|**Magn**|  
    |-----------------------------------|---------------------------------------|--------------------------------------|------------------------------------|  
    |80001|TÍNA|W-01-0001|2.0|  
    |80005|TÍNA|W-01-0001|2.0|  
    |80011|TÍNA|W-01-0001|20|  
    |80014|PICK|V-01-0001|20|  
    |80203|PICK|V-01-0001|20|  
    |80209|PICK|V-01-0001|20|  

4.  Á flipanum **Heim**, í flokknum **Skráir**, skal velja **Skrá** og velja svo hnappinn **Já**.  

    Næst skal samstilla nýja vöruhúsafærslur með birgðum.  

5.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Birgðafærslubækur** og velja svo viðeigandi tengil. Glugginn **Birgðabók** opnast.  
6.  Í flipanum **Aðgerðir** í flokknum **Eiginleikar** veljið **Reikna vöruhúsaleiðréttingu**.  
7.  Í glugganum **Reikna vöruhúsaleiðréttingu** skal velja hnappinn **Í lagi**.  
8.  Í glugganum **Birgðabók** á flipanum **Aðgerðir** í flokknum **Aðgerðir** skal velja**Bóka** og velja því næst hnappinn **Já**.  

### <a name="creating-the-assembly-items"></a>Stofnun samsetningarvöru  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Vörur** og velja svo viðeigandi tengil.  
2.  Á flipanum **Heim** í flokknum **Stjórna** veljið **Nýtt**.  
3.  Stofna fyrsta samsetningaríhlutinn sem byggður er á eftirfarandi upplýsingar.  

    |Svæði|Gildi:|  
    |---------------------------------|-----------|  
    |**Lýsing**|Sett A – Grunn-PC|  
    |**Grunnmælieining**|PCH|  
    |**Vöruflokkskóði**|Ýmislegt|  
    |**Áfyllingarkerfið**|Samsetning|  
    |**Samsetningarstefna**|Samsetning í birgðir|  
    |**Endurpöntunarstefna**|Lotu-fyrir-lotu|  

    > [!NOTE]  
    >  Sett A er yfirleitt úr samsetningu í birgðir og hefur því endurpöntunarstefnu til að gera það hluta af almennri framboðsáætlun.  

4.  Á flipanum **Færsluleit**, í flokknum **Samsetning/framleiðsla**, skal velja **Samsetning** og síðan **Samsetningaruppskrift**.  
5.  Skilgreina samsetningaruppskrift fyrir sett A með eftirfarandi upplýsingum.  

    |**Tegund**|**Fj.**|**Magn á**|  
    |-------------------------------|------------------------------|---------------------------------------|  
    |Atriði|80001|0|  
    |Atriði|80011|0|  
    |Atriði|80209|0|  
    |Forði|Eva|0|  

6.  Stofna annan samsetningaríhlut sem byggður er á eftirfarandi upplýsingar.  

    |Svæði|Gildi:|  
    |---------------------------------|-----------|  
    |**Lýsing**|Sett B – Pro PC|  
    |**Grunnmælieining**|PCH|  
    |**Vöruflokkskóði**|Ýmislegt|  
    |**Áfyllingarkerfið**|Samsetning|  
    |**Samsetningarstefna**|Samsetning til pöntunar|  

    > [!NOTE]  
    >  Sett B er yfirleitt úr samsetningu eftir pöntun og því ekki með endurpöntunarstefnu, þar sem það ætti ekki að vera hluti af almennri framboðsáætlun.  

7.  Á flipanum **Færsluleit**, í flokknum **Samsetning/framleiðsla**, skal velja **Samsetning** og síðan **Samsetningaruppskrift**.  
8.  Skilgreina samsetningaruppskrift fyrir sett B með eftirfarandi upplýsingum.  

    |**Tegund**|**Fj.**|**Magn á**|  
    |-------------------------------|------------------------------|---------------------------------------|  
    |Atriði|80005|0|  
    |Atriði|80014|0|  
    |Atriði|80210|0|  
    |Forði|Eva|0|  

### <a name="selling-the-assembly-items"></a>Sala samsetningaríhluta  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Sölupantanir** og velja svo viðeigandi tengil.  
2.  Á flipanum **Heim** í flokknum **Stjórna** veljið **Nýtt**.  
3.  Stofna tvær sölupöntunarlínur fyrir viðskiptamann 62000, The Device Shop, á vinnudagsetningunni með eftirfarandi upplýsingum.  

    |**Tegund**|**Lýsing**|**Magn**|Magn til samsetningar til pöntunar|Afh.dags|  
    |--------------|---------------------|------------------|-------------------------------|-------------------|  
    |Vara|Sett B – Pro PC|3|3|23. janúar|  
    |Vara|Sett A – Grunn-PC|15|5|27. janúar|  

    > [!NOTE]  
    >  Eftirfarandi ráðstöfunarvandamál eru til fyrir sölupöntunarlínuna fyrir sett B:  
    >   
    >  -   Samsetningaríhlutur 80210 er ekki tiltækur. Þetta þýðir að ekki er hægt að setja saman tilgreindu einingarnar þrjár af setti B, eins og gefið er til kynna með **0** í reitnum **Hægt að setja saman** í glugganum **Samsetningarráðstöfun**.  
    >   
    >  Eftirfarandi ráðstöfunarvandamál eru til fyrir sölupöntunarlínuna fyrir sett A:  
    >   
    >  -   Tíu einingar af setti A eru ekki í boði. Þetta gefur áætlunarkerfinu til kynna að magnið þarfnist samsetningar í birgðir.  

    Næsta skal sérstillt sölupöntun.  

4.  Veljið sölupöntunarlínuna fyrir þrjár einingar af setti B.  
5.  Á flýtiflipanum skal velja **Línur**, velja **Lína**, velja **Samsetning til pöntunar** og síðan **Setja saman í pöntunarlínur**.  
6.  Í glugganum **Setja saman í pöntun línur** á samsetningarpöntunarlínu fyrir vöru 80014, færið inn **2** í reitinn **Magn per**.  
7.  Í samsetningarpöntunarlínu fyrir vöru 80210, veljið reitinn **Nr.**  og veljið síðan vara 80209 í staðinn.  
8.  Stofna nýja samsetningarpöntunarlínu með eftirfarandi upplýsingum:  

    |Gerð|Númer|Magn á|  
    |----------|---------|------------------|  
    |Atriði|80203|0|  

9. Loka glugganum **Setja saman í pöntunarlínur**.  

    Næsta skal uppfæra einingarverð á setti B, samkvæmt sérsniði sem verið var að framkvæma. Athugið gildandi virði í reitnum **Ein. verð án Vsk -**.  

10. Á flýtiflipanum **Línur** skal velja **Lína**, velja **Samsetning til pöntunar** og síðan **Leggja saman verð**.  
11. Velja hnappinn **Já**. Athugið aukið virði í reitnum **Ein. verð án Vsk -**.  
12. Veljið sölupöntunarlínuna fyrir 15 einingar af setti A.  
13. Á flýtiflipanum skal velja **Línur**, velja **Lína**, velja **Samsetning til pöntunar** og síðan **Setja saman í pöntunarlínur**.  
14. Í glugganum **Setja saman í pöntun línur** er stofnuð ný samsetningarpöntunarlína með eftirfarandi upplýsingum.  

    |Tegund|Fj.|Magn á|  
    |----------|---------|------------------|  
    |Vara|80203|1|  

     Næst skal breyta afhendingardagsetningu síðari sölupöntunarlínu, samkvæmt samsetningaráætlun.  

15. Á sölupöntunarlínunni fyrir 15 einingar af setti A, skal færa **01-27-2014** inn í reitinn **Afhendingardagsetning**.  
16. Á flipanum **Aðgerðir** í flokknum **Afhending** veljið **Afhending**.  
17. Á flipanum **Aðgerðir** í flokknum **Vöruhús** veljið **Stofnið vöruhúsaafhendingu**.  
18. Loka sölupöntuninni.  

### <a name="planning-for-the-unavailable-ats-items"></a>Áætlanir fyrir ótiltækar ATS-vörur  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Áætlunarvinnublað** og velja svo viðeigandi tengil.  
2.  Á flipanum **Aðgerð** í flokknum **Aðgerðir** veljið **Reikna endurgerðaráætlun**.  
3.  Í glugganum **Reikna áætlun** stillið eftirfarandi afmarkanir.  

    |Upphafsdagsetning|Lokadagsetning|Fj.|  
    |-------------------|-----------------|---------|  
    |01-23-2014|01-27-2014|Sett A – Grunn-PC|  

4.  Velja hnappinn **Í lagi**.  

    Ný áætlunarlína er stofnuð fyrir samsetningarpöntun sem þörf er á með tíu einingar, sem skila á 27. janúar. Engin þörf er á breytingum og því er hægt að stofna pöntunina núna.  

5.  Í flipanum **Aðgerðir** í flokknum **Eiginleikar** veljið **Framkvæma aðgerðarboð**.  
6.  Í glugganum **Framkvæma aðgerðarboð** veljið reitinn **Samsetningarpöntun** veljið síðan **Búa til samsetningarpantanir**.  
7.  Velja hnappinn **Í lagi**.  

### <a name="assembling-and-shipping-the-first-ato-quantity"></a>Samsetning og afhending fyrsta ATO magns  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Afhending vöruhúss** og velja svo viðeigandi tengil.  

    > [!NOTE]  
    >  Í þessum hluta er einstaklingurinn sem er ábyrgur fyrir afhendingu sér um að skrá ATO-samsetningarvinnu, sem lokið hefur verið við, í vöruhúsaafhendingarlínuna. Þetta verkflæði getur gerst í umhverfi þar sem samsetningarvinnan er framkvæmd af einstaklingnum sem er ábyrgur fyrir afhendingu eða samsetningarstarfsmönnum á afhendingarsvæðinu.  
    >   
    >  Í þessum hluta eru aðgerðir í samsetningarpöntuninni eru framkvæmdar óbeint úr vöruhúsaafhendingarlínunni. Nánari upplýsingar um beina úrvinnslu samsetningarpöntunar eru í hlutanum „Sameina vörur í birgðir” í þessari leiðsögn.  

2.  Opna nýjustu vöruhúsaafhendingu sem er stofnuð í hvítri birgðageymslu.  

    Athugið þrjár vöruhúsaafhendingarlínur: Ein lína fyrir ATO magnið úr setti B, sem skila á 23. janúar. Ein lína fyrir ATO magnið úr setti A, sem skila á 27. janúar. Ein lína fyrir birgðamagn úr setti A, sem skila á 27. janúar.  

    **Setja saman í pöntun** Reiturinn tilgreinir samsetningaraðferðina.

    Næst skal stofna tínsluskjal fyrir alla ATO samsetningaríhluti sem þörf er fyrir á vöruhúsaafhendingunni.  

3.  Í flipanum **Aðgerðir** í flokknum **Eiginleikar** veljið **Stofna tínslu** og veljið svo hnappinn **Í lagi**.  

    Næst skal framkvæma verk tínslumannsins.  

4.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Tínsla** og velja svo viðeigandi tengil.  
5.  Opnar vöruhúsatínsluskjal sem stofnuð var í skrefi 3 í þessum hluta.  

    Athugið gildið í reitnum **Upprunaskjal** og að allar tínslulínurnar eru fyrir samsetningaríhluti.  

    Næst skal skrá tínsluna án þess að breyta sjálfgefnum upplýsingum.  

6.  Í flipanum **Aðgerðir** í flokknum **Eiginleikar** veljið **Færa magn sjálfkrafa til afgreiðaslu**.  
7.  Á flipanum **Heim**, í flokknum **Skráning**, skal velja **Skrá tínslu**.  

    Fara skal aftur í afhendingar.  

8.  Glugginn **Vöruhúsaafhending** er opnaður aftur.  

    Takið eftir að reiturinn **Magn tínt** er enn auður í öllum línum. Það er vegna þess að vörurnar sem á að afhenda hafa enn ekki verið tíndar, heldur aðeins íhlutina sem setja á saman í magnið sem setja á saman í pöntun.  

    Haldið er áfram til að fara yfir tengda samsetningarpöntun.  

9. Veljið afhendingarlínuna fyrir þrjár einingar af setti B.  
10. Á flýtiflipanum **Línur** skal velja **Lína** og síðan **Samsetning til pöntunar**. Glugganum **Samsetningarpöntun** opnast.  

    Athugið að nokkrir reitir í samsetningarpöntuninni eru ekki tiltækir þar sem pöntunin tengist sölupöntun.  

    Takið eftir að í samsetningarpöntunarlínunum er reiturinn **Magn tínt** útfylltur. Þetta er vegna tínslu sem skráð var í skrefi 7 í þessum hluta.  

11. Í reitnum **Magn til samsetningar** skal prófa að færa inn gildi lægra en **3**.  

    Villuboðin innihalda útskýringu á því hvers egna aðeins er hægt að fylla út í þennan reit í gegnum reitinn **Magn til afhendingar** í tengdri afhendingu.  

    Hægt er að breyta **Magn til samsetningar** svæðinu til að styðja aðstæður þar sem á að senda hluta birgðamagns í stað þess að setja saman fleiri einingar til pöntunar. Nánari upplýsingar eru í hlutanum „Samsetningaraðstæður“ [Skilja hvernig skal setja saman í pöntun eða setja saman í birgðir](assembly-assemble-to-order-or-assemble-to-stock.md).  

12. Loka glugganum **Samsetningarpöntun** til að fara aftur í gluggann **Vöruhúsaafhending**.  
13. Á afhendingarlínunni fyrir þrjár einingar af setti B, í reitinn **Magn til afhendingar** skal færa inn **3**.  
14. Á flipanum **Aðgerðir** í flokknum **Bókun** veljið **Bóka afhendingu** og veljið svo **Afhenda**.  

    Ásamt þessari vöruhúsafhendingarbókun er full notkun og frálag magns tengdrar samsetningarpöntunar bókuð og reiturinn **Eftirstöðvar** er auður. Sölupöntunarlínan fyrir Sett B uppfærist til að sýna að einingarnar 3 eru afhentar.  

    Vöruhúsaaðgerðum til að uppfylla fyrstu sölupöntunarlínuna fyrir 23. janúar er lokið. Næst skal útfylla sölupöntunarlínur þar sem afhending er 27. janúar  

### <a name="assembling-and-recording-the-second-ato-quantity"></a>Samsetning og skráning seinna ATO magns  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Samsetningarpöntun** og velja svo viðeigandi tengil.  

    Takið eftir að ATO pöntunin fyrir sendar einingar af setti B eru enn í listanum, jafnvel þó **Eftirstöðvar** sé autt. Það er vegna þess að tengda sölupöntunin er enn ekki reikningsfærð að fullu.  

    > [!NOTE]  
    >  Í þessum hluta er samsetningarstarfsmaður ábyrgur fyrir að skrá ATO-samsetningarvinnu, sem lokið hefur verið við, í vöruhúsaafhendingarlínuna. Þetta verkflæði getur gerst í umhverfi þar sem samsetningarvinnan fer fram í aðskilinni samsetningardeild og samsetningarstarfsmenn hafa leyfi til að breyta afhendingarlínu vöruhússins.  

2.  Opna ATO samsetningarpöntun fyrir fimm einingar af setti A.  

    Takið eftir að reitirnir **Magn til samsetningar** og **Magn til notkunar** eru auðir þar sem engin vinna hefur enn verið skráð.  

    Takið eftir að í samsetningarpöntunarlínunum er reiturinn **Magn tínt** útfylltur. Þetta er vegna tínslunnar sem var skráð 23. janúar.  

    Næst skal skrá að samsetningarpöntunni sé lokið.  

3.  Á flipanum **Færsluleit**, í flokknum **Vöruhús**, skal velja **Setja saman í p. vöruh. send. lína**.  
4.  Í glugganum **Setja saman í pön. vöruh. send. lína** í reitnum **Magn til afhendingar**, færið inn **5** og síðan er glugganum lokað.  

    Takið eftir að í glugganum **Samsetningarpöntun** að svæðin **Magn til samsetningar** og **Magn til notkunar** eru nú fyllt út með frálags og notkunarmagni sem verður bókað með í sendingunni.  

5.  Glugganum **Samsetningarpöntun** er lokað.  

### <a name="assembling-the-ats-quantity"></a>Samsetning ATS magns  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Samsetningarpöntun** og velja svo viðeigandi tengil.  
2.  Opna samsetningarpöntunina fyrir tíu einingar af setti A.  

    Takið eftir að reiturinn **Magn til samsetningar** er fylltur út með því magni sem búist var við.  

    Næst skal stofna tínsluskjal til að sækja íhlutina sem þörf er á.  

3.  Á flipanum **Aðgerðir** í flokknum **Afhending** veljið **Afhending**.  
4.  Á flipanum **Aðgerðir** í flokknum **Vörhús** veljið **Stofna vöruhúsatínslu** og veljið svo hnappinn **Í lagi**.  

    Næst skal framkvæma verk tínslumannsins.  

5.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Tínsla** og velja svo viðeigandi tengil.  
6.  Opnar vöruhúsatínsluskjal sem stofnuð var í skrefi 4 í þessum hluta.  

     Haldið er áfram til að skrá tínsluna án þess að breyta sjálfgefnum upplýsingum.  

7.  Í flipanum **Aðgerðir** í flokknum **Eiginleikar** veljið **Færa magn sjálfkrafa til afgreiðaslu**.  
8.  Á flipanum **Heim**, í flokknum **Skráning**, skal velja **Skrá tínslu**.  

    Fara skal aftur í samsetningarpöntun til að framkvæma síðustu samsetningarverk.  

9. Í glugganum **Samsetningarpöntun** á flipanum **Aðgerðir** í flokknum **Bókun** veljið **Bóka** og velja því næst hnappinn **Já**.  

    Takið eftir að samsetningarpöntunin er fjarlægð af lista yfir opnar pantanir.  

### <a name="shipping-the-remaining-items-partly-from-stock-and-partly-assembled-to-the-order"></a>Afhenda Eftirstandandi vörur, að hluta til úr birgðir og að hluta til úr sett saman í pöntun  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Afhending vöruhúss** og velja svo viðeigandi tengil.  
2.  Opna nýjustu vöruhúsaafhendingu sem er stofnuð í hvítri birgðageymslu.  

    Takið eftir að í línunni fyrir tíu einingar af setti A að svæðin **Magn til afhendingar** og **Tínt magn** eru auð.  

    Næsta skal velja vörur sem eftir standa.  

3.  Í flipanum **Aðgerðir** í flokknum **Eiginleikar** veljið **Stofna tínslu** og veljið svo hnappinn **Í lagi**.  

    Næst skal framkvæma síðasta verk tínslumannsins fyrir þessa vöruhúsaafhendingu.  

4.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Tínsla** og velja svo viðeigandi tengil.  
5.  Opnar vöruhúsatínsluskjal sem stofnuð var í skrefi 3 í þessum hluta.  

    Athugið að þetta tínsluskjal er fyrir samsetningarvöru, ekki fyrir samsetningaríhluti.  

    Næst skal skrá tínsluna án þess að breyta sjálfgefnum upplýsingum.  

6.  Í flipanum **Aðgerðir** í flokknum **Eiginleikar** veljið **Færa magn sjálfkrafa til afgreiðaslu**.  
7.  Á flipanum **Heim**, í flokknum **Skráir**, skal velja **Skrá tínslu** og velja svo hnappinn **Já**.  

    Fara skal aftur í vöruhúsaafhendingu til að framkvæma síðasta verk.  

8.  Glugginn **Vöruhúsaafhending** er opnaður aftur.  

    Í glugganum **Vöruhúsaafhending** á línunni fyrir tíu einingar af setti A, athugið að í reitunum **Magn til afhendingar** og **Magn tínt** innihalda nú **10**.  

9. Á flipanum **Aðgerðir** í flokknum **Bókun** veljið **Bóka afhendingu** og veljið svo **Afhenda**.  

    Afhendingarskjal vöruhússins er fjarlægt, sem gefur til kynna að vöruhúsaaðgerðunum sem málinu tengjast sé lokið. Næst skal ganga úr skugga um að sölupöntunin hafi verið skráð.  

10. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Sölupantanir** og velja svo viðeigandi tengil.  
11. Opna sölupöntun fyrir Tækjabúðina.  

    Takið eftir að reiturinn **Magn afhent** inniheldur allt magnið í báðum línum.  

    Þegar Tækjabúðin greiðir fyrir móttöku á tölvunum 18 úr CRONUS, eru sölupantanirnar og tengdar samsetningarpantanir fjarlægðar.  

## <a name="see-also"></a>Sjá einnig  
 [Skilja hvernig skal setja saman í pöntun eða setja saman í birgðir](assembly-assemble-to-order-or-assemble-to-stock.md)   
 [Hvernig á að sameina vörur](assembly-how-to-assemble-items.md)   
 [Hvernig á að tína vörur fyrir vöruhúsaafhendingu](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
 [Hvernig á að selja sem eru settar saman í pöntun](assembly-how-to-sell-items-assembled-to-order.md)   
 [Hvernig á að sameina vörur](assembly-how-to-assemble-items.md)   
 [Hönnunarupplýsingar: Bókun samsetningarpöntunar](design-details-assembly-order-posting.md)   
 [Hönnunarupplýsingar: Innra vöruhúsaflæði](design-details-internal-warehouse-flows.md)   
 [Hönnunarupplýsingar: vöruhúsaflæði á innleið](design-details-outbound-warehouse-flow.md)   
 [Kynning: Sjálfvirk áætlun birgða](walkthrough-planning-supplies-automatically.md)

