---
title: "Flytja gögn viðskiptamanna | Microsoft Docs"
description: "Hægt er að flytja núverandi gögn viðskiptamanna úr fyrirliggjandi ERP-kerfi yfir í Business Central með því að nota RapidStart Services. Hægt er að nota Excel. xlsx skrár til að flytja gögnin. Einnig er hægt að færa gögn handvirkt með því að opna þau beint í fyrirtækinu."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/07/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: ce50ff8213e85a8343a93eb80bbbc381eaa8e350
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="migrate-customer-data"></a>Flytja gögn viðskiptamanna
Hægt er að flytja núverandi gögn um viðskiptavini úr fyrirliggjandi ERP-kerfi yfir í [!INCLUDE[d365fin](includes/d365fin_md.md)] með því að nota gagnaflutningstæki RapidStart Services. Hægt er að nota Excel-skrár til að flytja gögnin. Einnig er hægt að færa gögn handvirkt með því að slá þau beint inn í fyrirtækið.

Gluggarnir **Flutningsyfirlit** og **Grunnstilling vinnublaðs** veita aðgang að aðgerðum og yfirlitum til að framkvæma öll verk sem snúa að gagnaflutningi. Mælt er með að ein tafla sé flutt í einu, til að meðhöndla tengsl í gögnunum. Við flutning er einnig unnið með aðalgagnatöflur, sem innihalda upplýsingar um viðskiptavini, lánardrottna, vörur, tengiliði og fjárhag.  

## <a name="to-import-configuration-packages"></a>Að flytja inn grunnstillingarpakka
Þegar nýtt fyrirtæki er stofnað er hægt að flytja inn fyrirtækjastillingar fyrir nýja fyrirtækið. Stillingarnar úr .rapidstart skrá eru fluttar inn, sem afhendir innihald pakkans á samþjöppuðu formi. Samsvarandi safn sjálfgefinna gagnaflutningstaflna eru flutt inn. Gagnasamstæðan inniheldur aðalgagnatöflur og uppsetningargagnatöflur. Fyrsta verkið í gagnaflutningi er að meta hvort sjálfgefin flutningsuppsetning sé í samræmi við þarfir nýja fyrirtækisins.

> [!NOTE]  
>  Ekki er hægt að endurnefna skrá sem ekki er þegar skilgreiningarpakki RapidStart Services sem .rapidstart skilgreiningarpakkaskrá og svo reyna að flytja hana inn. Ef það er reynt, munu koma upp villuboð.  

Áður en hafist er handa þarf að ganga úr skugga um að notandi sé á Mitt hlutverk RapidStart Services innleiðara.

> [!IMPORTANT]  
>  Við inn- og útflutning stillingapakka milli gagnagrunna tveggja fyrirtækja ættu gagnagrunnarnir að hafa sama skema til að ganga úr skugga um að öll gögn séu flutt rétt. Þetta merkir að gagnagrunnar ættu að hafa sama skipulag í töflum og reitum, þar sem töflur hafa sömu aðallykla og reitir hafa sama kenni og gagnagerðir.  
>   
>  Hægt er að flytja inn skilgreiningapakka sem hefur verið fluttur út úr gagnagrunni sem hefur annað skemma en markgagnagrunnur. Allar töflur eða reitir sem eru í skilgreiningapakkanum en ekki í markgagnagrunninum verða hins vegar ekki fluttir inn.
>   
> Töflur með öðrum aðallyklum og reitum sem hafa aðrar gagnagerðir verða heldur ekki fluttir inn. Sem dæmi má nefna að gögn munu ekki flytjast yfir ef skilgreiningapakki inniheldur töfluna **50000 Customer** sem hefur aðallykilinn **Code20** og gagnagrunnurinn sem flutt er inn í inniheldur töfluna **50000 Customer Bank Account** sem hefur aðallykilinn **Code20 + Code 20**.  

1. Opna skal nýja fyrirtækið.  
2. Velja skal táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslutákni"), slá inn **Grunnstillingarpakkar** og velja svo viðeigandi tengil.  
3. Velja skal aðgerðina **Flytja inn pakka**. Farið er í .rapidstart pakkaskrána sem á að flytja inn og svo er valin aðgerðin **Opna**. Á meðan innflutningi stendur, er innihald pakkans afþjappað og pakkafærslan stofnuð.  

    Að innflutningi loknum er hægt að sjá fjölda grunnstillingartaflna sem hafa ferð fluttar inn í reitnum **Fjöldi taflna**.  
4. Til að fara yfir lista grunnstillingartafla er valin aðgerðin **Skoða**.  
5. Til að nota pakkann skal velja aðgerðina **Nota pakka**.  

    > [!NOTE]  
    >  Gagnaflutningsupplýsingar byggjast á skilgreiningarsniðmátum, ef slíkt er tilgreint. Uppfæra þarf sniðmátið fyrst til að breyta lista reita.  

6.  Til að fara yfir reitaval skal velja töflu og því næst á flipanum **Línur** skal velja aðgerðina **Reitir**. Bera saman og skoða fjölda reita sem eru tiltækir þeim fjölda reita hverra gögn hafa verið jöfnuð.  

Ef val á töflum uppfyllir ekki þarfir fyrirtækisins er hægt að stofna eina eða fleiri nýjar gagnaflutningsskrár. Ef skrárnar eru fullnægjandi er hægt að halda áfram með gagnaflutninginn með því að nota Excel- eða XML-skrár.

## <a name="to-create-a-data-migration-file"></a>Til að búa til gagnaflutningsskrá
Hægt er að stofna nýjar gagnaflutningaskrár og sérsníða þær til stuðnings fyrirtækisins. Athugið að aðeins er hægt að nota skrá til að flytja reit sem er með eiginleikann **FieldClass** stilltan á **Venjulegt**.  

1. Velja skal táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslutákni"), slá inn **Grunnstillingarpakki** og velja svo viðeigandi tengil.  
2. Veljið og opnið pakkann sem á að nota til að flytja gögn og veljið svo aðgerðina **Ná í töflur**. Glugginn **Sækja pakkatöflu** opnast.  
3. Í reitnum **TableID** færið inn töflunúmer eða veljið töflu af listanum, til dæmis töflu 18, **Viðskiptamaður**. Reiturinn **Heiti töflu** útfyllist sjálfkrafa.  
4. Veljið nýja flutningstöflu og síðan á flipanum **Töflur** skal velja aðgerðina **Reitir**. Glugginn **Flutningsreitir** opnast.  
5. Hreinsið gátreitinn **Reitur hafður með** fyrir alla reiti sem ekki á að flytja inn og veljið síðan aðgerðina **Safn haft með** eða **Hreinsa það sem haft er með**.  

> [!IMPORTANT]  
>  Ef gátreiturinn **Innifela svæði** er sjálfgefið valinn er hann hluti af aðallyklinum. Ekki ætti að hreinsa valið, annars koma inn villur og ekki er hægt að flytja færsluna út.  
>
>  Þegar reitur sem tengist annarri töflu er hafður með er gátreiturinn **Staðfesta svæði** sjálfkrafa valinn. Villuleit getur leitt til uppfærslu á öðrum reitum í þessari töflu og öðrum og er framkvæmd í þeirri röð sem reitsnúmerið segir til um.  

Ný innflutningstafla er stofnuð.  

## <a name="to-export-data-migration-files"></a>Til að flytja út nauðsynlegar gagnaflutningsskrár.
Eftir að hafa ákvarðað töflurnar sem á að millifæra gögn um viðskiptavini á, skal flytja skrárnar út.  

1. Velja skal táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslutákni"), slá inn **Grunnstillingarpakkar** og velja svo viðeigandi tengil.  
2. Veljið og opnið pakkann sem á að nota til útflutnings.
3. Veljið töfluna eða töflurnar sem á að flytja út og veljið svo aðgerðina **Flytja út Flytja út í Excel**.
4. Vista skal Excel-skrána sem flutt var út.  
5. Þetta ferli er endurtekið fyrir allar viðeigandi gagnaflutningstöflur. Ef margar töflur eru valdar í einu verða gögn þeirra fluttar í eina sameiginlega vinnubók.  

Ef taflan er auð mun gagnaflutningsskráin innihalda auð hólf fyrir þá reiti sem valdir voru þegar flutningstöflur voru valdar eða stofnaðar fyrir nýja fyrirtækið. Ef valin gagnaflutningstafla inniheldur gögn verða þau flutt út.  

## <a name="to-map-values-to-be-used-during-import"></a>Að varpa gildum sem á að nota við innflutning
Þegar þú jafnar gögn sem þú hefur flutt inn úr Excel eða RapidStart-pakka notar og höndlar [!INCLUDE[d365fin](includes/d365fin_md.md)] vörpunina byggt á töflutengslum:  

- Ef þú skilgreinir vörpun beint fyrir reit í töflu notar [!INCLUDE[d365fin](includes/d365fin_md.md)] hann.  

- Ef reiturinn er með tengsl í aðra töflu leitar [!INCLUDE[d365fin](includes/d365fin_md.md)] að vörpuninni sem er skilgreind fyrir reit aðallykilsins í tengdu töflunni. Tengda taflan verður hins vegar að vera hluti af grunnstillingapakkanum.  

- Ef vörpun upplýsinga er skilgreind á báðum stöðum, bæði beint fyrir reitinn og fyrir aðallykilinn í tengdu töflunni þá mun [!INCLUDE[d365fin](includes/d365fin_md.md)] leita að vörpuninni á báðum stöðum.  

- Ef sömu varpanir eru skilgreindar beint fyrir reit og í tengdu töflunni, en mismunandi gildi eru til staðar, þá mun vörpunin sem er skilgreind beint fyrir reitinn vera notuð yfir vörpunina sem er skilgreind fyrir töfluna sem reiturinn vísar í.  

Í ferlunum sem fylgja ætti að athuga fyrirfram hvaða gildum á að halda við flutningsferlið. Til að framkvæma eftirfarandi ferli þarf að gagnaflutningsskrár (.xlsx) sem hafa verið fluttar úr [!INCLUDE[d365fin](includes/d365fin_md.md)]. Nánari upplýsingar eru í kaflanum „Að flytja út nauðsynlegar gagnaflutningsskrár.“

1. Velja skal táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslutákni"), slá inn **Grunnstillingarpakkar** og velja svo viðeigandi tengil.
2. Opna skal pakkann fyrir fyrirtækið sem um ræðir.  
3. Veljið töfluna sem á að varpa gildum fyrir og síðan á flipanum **Töflur** skal velja aðgerðina **Töflur**.  
4. Fyrir hvern reit sem á að varpa skal velja aðgerðina **Vörpun**.  
5. Í reitinn **Gamalt gildi** skal færa inn gildið sem á að breyta. Í reitinn **Nýtt gildi** skal færa inn nýtt gildi í stað gamla gildisins. Velja hnappinn **Í lagi**.  
6. Innflutningur gagna viðskiptamanns Nánari upplýsingar eru í kaflanum „Að flytja inn gögn viðskiptamanns.“
7. Í reitnum **Fjölda pakkavillna** skal athuga hvort einhverjar villur eru tilkynntar. Ef það er, skaltu fara niður til að sjá villurnar. Glugginn **Stilla pakkafærslur** opnast.
8. Veljið aðgerðina **Sýna villur**. Þú færð eftirfarandi villu: **<option> er ekki gildur valkostur. Gildir valkostir eru <valid option list>**. Velja hnappinn **Í lagi**.  
9. Til að nota vörpunina sem sett var upp skal velja aðgerðina **Nota gögn**.  

### <a name="mapping-example"></a>Dæmi vörpunar  
Eftirfarandi dæmi sýnir hvernig [!INCLUDE[d365fin](includes/d365fin_md.md)] innleiðir vörpunarskilgreiningar.  

1. Búið til grunnstillingartöflu sem er með töfluna **Sölumaður/innkaupaaðili**. Skilgreina vörpun fyrir reitinn **Kóði**.  
2. Bætið við viðbótartöflum við pakkann, t.d. **Viðskiptavinur** og **Lánardrottinn**. Töflurnar vísuðu báðar í töfluna **Sölumaður/innkaupaaðili** í gegnum reitina **Kóði sölumanns** og **Innkaupakóði** í þeirri röð.  
3. Þegar þú jafnar gögn mun vörpunin sem þú gafst upp fyrir reitinn **Kóði** í töflunni **Sölumaður/innkaupaaðili** einnig verða tekin með við vinnslu á reitunum **Kóði sölumanns** og **Kóði innkaupaaðila**.

## <a name="to-add-additional-values-to-included365finincludesd365finmdmd"></a>Til að bæta viðbótargildum við [!INCLUDE[d365fin](includes/d365fin_md.md)]  
1. Velja skal táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslutákni"), slá inn **Grunnstillingarpakkar** og velja svo viðeigandi tengil.  
2. Veljið töfluna sem á að bæta við fleiri gildum fyrir og síðan á flipanum **Töflur** skal velja aðgerðina **Reitir**.  
3. Fyrir reitina þar sem [!INCLUDE[d365fin](includes/d365fin_md.md)] á að heimila viðbótargildi við flutning skal velja gátreitinn **Stofna kóða sem vantar**.  
4. Innflutningur gagna viðskiptamanns Nánari upplýsingar eru í kaflanum „Að flytja inn gögn viðskiptamanns.“

## <a name="to-clean-up-and-process-data-before-applying-data"></a>Til að hreinsa upp og meðhöndla gögn fyrir jöfnun gagna
Í sumum tilfellum kanntu að vilja hreinsa upp gögn viðskiptamanns áður en þau eru sett í gagnagrunninn. Til að gera það er hægt að nota runuvinnsluna **Grunnstilling pakka - Ferli** til að laga vandamál á borð við:  

- Umbreytir dagsetningum og tugastöfum á það snið sem eru nauðsynlegt í svæðisstillingum í tölvu notandans.  
- Fjarlægðu bil eða sérstafi.  

Eftir að runuvinnslan hefur verið keyrð skal nota eftirfarandi ferli til að meðhöndla gögnin.  

1. Opna skal grunnstillingapakka fyrir fyrirtækið.  
2. Veljið aðgerðina **Vinna gögn**.  
3. Til að nota vörpunina sem sett var upp skal velja aðgerðina **Nota gögn**.

## <a name="to-migrate-customer-data"></a>Að flytja gögn viðskiptamanna
Þegar innflutningstafla hefur verið flutt út, er næsta skrefið að færa inn gömul gögn viðskiptamanns. Til að einfalda verk er hægt að nýta XML-meðhöndlunarverkfærin sem byggð eru inn í Excel. Einnig er hægt að nota Excel innbyggðar aðgerðir til aðstoða við gagnsnið og að setja gögn í réttan flokk.

Til að fá aðstoð með XML skal virkja flipann **Forritari** á Excel-borðanum og velja svo aðgerðina **Uppruni** til að sjá XML-skema flutningstöflunnar eins og hún kemur fyrir í Excel.

Eftirfarandi ferli er byggt á Excel-vinnublaði sem hefur verið stofnað fyrir yfirfærslu. Nánari upplýsingar eru í Hvernig skal: Flytja út flutningstöflur.

> [!IMPORTANT]  
> Ekki breyta dálkum í Excel-vinnublöðunum. Ef gögnin eru færð, þeim breytt eða þeim eytt er ekki hægt að flytja vinnublaðið inn í [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Opnið útfluttu gagnaskrána í Excel. Til er vinnublað með heiti töflunnar.
2. Endurnefna skal vinnublaðið Sheet1 gefa til kynna að það verði notað til að umbreyta gögnunum. Afrita haus línu án sniðs hennar úr útfluttu töflunni í nýja vinnublaðið.
3. Á þriðja vinnublaði, afritið öll gögn um viðskiptavini. Endurnefnið blöðin svo þau fá heiti eins og „Eldri gögn.“
4. Gera Excel reiknireglu til að varpa gögnum í umbreytingarvinnublað á milli reitanna í útflutta vinnublaðinu og eldri gögnum um viðskiptavin.
5. Þegar búið er að varpa öllum gögnum, skal afrita afmörkun gagnanna á töflu á vinnublaðinu.
6. Vistið skrána og gætið þess að breyta ekki skrárgerðinni.

Nú er hægt að flytja inn gagnaflutningskrár sem innihalda eldri gögn um viðskiptavin inn í [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="to-import-customer-data"></a>Til að flytja inn viðskiptamannagögn
Þegar gögn um viðskiptavini eru færður inn í gagnaflutningsskrárnar í Excel, eru skrárnar fluttar inn í [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Opnið gluggann **Grunnstilling pakkaspjalds**.
2. Veljið töfluna þar sem á að flytja inn gögn og síðan á flipanum **Töflur** skal velja aðgerðina **Flytja inn úr Excel**.
3. Finna og opna skrána þaðan sem á að flytja gögn inn í [!INCLUDE[d365fin](includes/d365fin_md.md)].

Gögn úr skránni eru flutt inn í töflu grunnstillingarsendingar. Í reitnum **Númer færslupakka** er hægt að sjá fjölda færslna sem hafa verið innfluttar. Auk þess sést fjöldi innflutningsvillna.

## <a name="to-validate-customer-data"></a>Til að staðfesta gögn viðskiptamanna
Viðskiptamannagögn verður að sannprófa áður en færslurnar eru settar í gagnagrunninn [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!NOTE]  
>  Ógild gögn eru yfirleitt ekki búin til í gagnagrunninum. Hins vegar gæti lokast á forritið einstaka sinnum ef innflutt flutningstafla inniheldur villur.  

1. Í glugganum **Flutningsyfirlit** er farið yfir reitinn **Fjöldi flutningsvilla** til að sjá hvort einhverjar villur komu upp í innflutningi.  
2. Ef villur eru til staðar skal velja flutningstöfluna og svo í flipanum **Töflur** skal velja aðgerðina **Villur**. **Ógilt** gátreiturinn er valinn fyrir hverja færslu sem villa er í.  
3. Til að fara yfir villur skal velja línu og síðan velja aðgerðina **Sýna villu**.  

    **Villutexti** svæðið hefur að geyma ástæðuna fyrir villunni. **Yfirskrift reits** svæðið hefur að geyma yfirskrift svæðisins þar sem villuna er að finna.  
4.  Til að leiðrétta villu eða uppfæra á annan hátt í glugganum **Flutningsyfirlit** skal velja aðgerðina **Flutningsfærsla** og svo í glugganum **Flutningsfærsla** skal lagfæra færsluna sem er með villuna.  

Þegar leiðrétting er gerð, er færslan fjarlægð af lista yfir færslur í glugganum **Flutningsgagnavillur**.  

Nú er hægt að nota gögn viðskiptavinar í gagnagrunninum.  

## <a name="to-apply-customer-data"></a>Til að nota gögn viðskiptamanna
Þegar allar innfluttar gagnaflutningsfærslur sem eru gildar og villulausar eru komnar er hægt að nota færslurnar á [!INCLUDE[d365fin](includes/d365fin_md.md)] gagnagrunninn.  

1. Opna gluggann **Skilgreiningarpakkar**.  
2. Veljið töfluna fyrir gagnaflutningsskrána sem á að nota og veljið síðan aðgerðina **Nota gögn**.

Hægt er að sjá fjölda gagnagrunnsfærslna sem stofnaðar hafa verið í reitnum **Fjöldi gagnagrunnsfærslna**. Hægt er að staðfesta að réttar færslur hafi verið búnar til með því að velja tengilinn í reitnum **Fj. gagnagrunnsfærslna**.  

Gagnagrunnur fyrirtækis viðskiptavinar er nú uppsettur og grunngögn eru flutt inn. Næstu skref í innleiðingarferlinu eru að þjálfa notendur, skilgreina ferli, útbúa frekari gögn, sérsníða skýrslur o.s.frv.

## <a name="see-also"></a>Sjá einnig  
[Uppsetning fyrirtækis með RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Stjórnun](admin-setup-and-administration.md)
