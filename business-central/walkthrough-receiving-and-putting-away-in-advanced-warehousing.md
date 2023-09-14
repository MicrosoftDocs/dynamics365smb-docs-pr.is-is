---
title: Móttaka og frágangur í ítarlegri vöruhúsavinnu
description: 'Hægt að framkvæma ferli innleiðar til að taka við og ganga frá á fjóra vegu, með því að nota mismunandi eiginleika, allt eftir flækjustigi vöruhússins.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/24/2021
ms.author: bholtorf
---
# Kynning: Móttaka og Frágangur í ítarlegri grunngerð vöruhúss

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

Í, Móttaka og frágangur á  [!INCLUDE[prod_short](includes/prod_short.md)] sér stað með einni af fjórum aðferðum, eins og lýst er í eftirfarandi töflu.

|Aðferð|Ferli á innleið|Krefjast kvittana|Krefjandi frágangur|Flókið stig (frekari upplýsingar um  [Vöruhúsakerfi-Yfirlit](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Bóka móttöku og frágang frá pöntunarlínunni|||Engin sérstök vöruhúsaaðgerð.|  
|Á|Bóka móttöku og frágang frá birgðafrágangsskjali||Kveikt|Grunnur: pöntun-eftir pöntun.|  
|U|Bóka móttöku og frágang frá vöruhúsamóttökuskjali|Kveikt||Grunnur: Samstæða móttöku/skipa bóka fyrir margar pantanir.|  
|D|Bóka móttöku frá vöruhúsamóttökuskjali og bóka frágang frá vöruhúsafrágangsskjali|Kveikt|Kveikt|Ítarlegt|  

Frekari upplýsingar um vöruflæði á  [innleið](design-details-inbound-warehouse-flow.md).

Eftirfarandi kynning sýnir aðferð D í fyrri töflu.  

## Um kynninguna

Í vöruhúsi ítarlegrar grunngerðar þar sem birgðageymsla er sett upp þannig að krafist sé móttökuvinnslu til viðbótar frágangsvinnslu skal nota síðuna **Vöruhús móttaka** til að skrá og bóka móttöku og afhendingarupplýsingar fyrir upprunaskjöl á innleið. Þegar vöruhúsamóttakan er bókuð verður eitt eða fleiri frágangsskjöl vöruhúss búin til til að skipa starfsmönnum vöruhússins að flytja mótteknar vörur á uppgefnar staðsetningar samkvæmt hólfauppsetningu eða í önnur hólf. Tiltekin staðsetning varanna er skráð þegar frágangur vöruhúss er skráður. Upprunaskjalið á innleið getur verið innkaupapöntun, söluvöruskilapöntun, millifærslupöntun á innleið eða framleiðslupöntun þar sem úttakið er tilbúið til frágangs. Ef móttakan er búin til úr pöntun á innleið fást fleiri en eitt upprunaskjal á innleið fyrir móttökuna. Með þessari aðferð hægt er að skrá margar vörur frá mismunandi pöntunum á innleið með einni móttöku.  

Þessi kynning fjallar um eftirfarandi verk:  

-   HVÍT birgðageymsla sett upp fyrir móttöku og frágang.  
-   Stofnun og útgáfa tveggja innkaupapantana til að hámarka afgreiðslutíma á vörum í vöruhúsi.  
-   Stofnaðu og bókaðu vöruhúsamóttökuskjal fyrir margar innkaupapantanalínur frá tilteknum lánardrottnum.  
-   Skráning á vöruhúsafrágangi fyrir mótteknar vörur.  

## Hlutverk

Þessi kynning sýnir þau verk sem framkvæmd eru með eftirfarandi hlutverkum notenda:  

-   Yfirmaður vöruhúss  
-   Innkaupaaðili  
-   Starfsmenn í móttöku  
-   Starfsmaður í vöruhúsi  

## Frumskilyrði

Til að ljúka þessari kynningu þarf:  

-   CRONUS uppsett.  
-   Notandi verður að starfsmanni vöruhúss í hvítri birgðageymslu á eftirfarandi hátt:  

1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Starfsmenn vöruhúss** og velja síðan viðkomandi tengil.  
2.  Velja reitinn **Notandakenni** og velja síðan eigin notandareikning notanda á síðunni **Notendur**.  
3.  Í reitnum **Birgðageymslu kóti** færið inn HVÍTT.  
4.  Veljið reitinn **Sjálfgefið**.  

## Ferill

Ellen, stjórnandi vöruhúss í CRONUS stofnar tvær innkaupapantanir fyrir fylgihlutavörur frá lánardrottnum 10000 og 20000 sem afhenda á til WHITE vöruhúss. Þegar vörur eru afhentar í vöruhúsið notar Sammy, sem ber ábyrgð á móttöku vara frá lánardrottnum 10000 og 20000, afmörkun til að stofna móttökulínur fyrir innkaupapantanir sem koma frá tveimur lánardrottnum. Sammi skráir vörurnar sem mótteknar í einni vöruhúsamóttöku og gerir þær tiltækar til sölu eða annarrar ráðstöfunar. Jón í vöruhúsinu tekur hlutina úr móttökuhólfinu og gengur frá þeim. John setur allar einingarnar upp í sjálfgefnu hólfin sín, nema 40 af 100 sem eru á mótteknum einingum er gengið frá í samsetningardeildinni með því að skipta frágangslínunni. Þegar John skráir fráganginn er hólfainnihald uppfært og vörurnar gerðar tiltækar til tínslu úr vöruhúsinu.  

## Farið yfir HVÍTU birgðageymsluuppsetninguna

Uppsetning síðunnar **Birgðageymsluspjald** skilgreinir vöruhúsaflæði fyrirtækisins.  

### Til að fara yfir uppsetningu birgðageymslunnar  

1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Staðsetningar** og velja síðan viðkomandi tengil.  
2.  HVÍTT-staðsetningarspjaldið er opnað.  
3.  Athugasemd á flýtiflipanum **Vöruhús** um að gátmerkið **Beinn frágangur og tínsla** hafi verið valið.  

    Þetta þýðir að birgðageymslan er sett upp fyrir hæsta flækjustig, eins og sést á því að allir gátreitir fyrir vöruhúsaafgreiðslu eru valdir.  

4.  Athugasemd á flýtiflipanum **Hólf** um að hólf séu tilgreind í reitunum **Hólfkóti móttöku** og **Hólfkóti afhendingar**.  

Þetta þýðir að þegar vöruhúsamóttaka er stofnuð er þessi hólfkóti sjálfgefið afritaður í haus vöruhúsamóttökuskjalsins og í línur vöruhúsafrágangsins sem verður til.  

## Stofna innkaupapantanirnar

Innkaupapantanir eru algengustu tegundir af upprunaskjölum á innleið.  

### Innkaupapantanir stofnaðar  

1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupapantanir** og velja síðan viðkomandi tengil.  
2.  Valið er **Nýtt** aðgerð.  
3.  Stofna innkaupapöntun fyrir lánardrottinn 10000 á vinnudeginum (23. Janúar) með eftirfarandi innkaupapöntunarlínum.  

    |Vara|Staðsetningarkóði|Magn|  
    |----------|-------------------|--------------|  
    |70200|HVÍTT|100 STYKKI|  
    |70201|HVÍTT|50 STYKKI|  

    Tilkynnið svo vöruhúsinu að innkaupapöntunin sé tilbúin til afgreiðslu í vöruhúsi þegar sendingin berst.  

4.  Valið er **Losa** aðgerð. Staðan breytist úr Opin í Losuð.

    Búðu nú til aðra innkaupapöntunina.  

5.  Valið er aðgerðin **Nýtt**.  
6.  Stofna innkaupapöntun fyrir lánardrottinn 20000 á vinnudeginum (23. Janúar) með eftirfarandi innkaupapöntunarlínum.  

    |Vara|Staðsetningarkóði|Magn|  
    |----------|-------------------|--------------|  
    |70100|HVÍTT|10 dósir|  
    |70101|HVÍTT|12 dósir|  

    Valið er **Losa** aðgerð. Staðan breytist úr Opin í Losuð.

    Vörur frá lánardrottnum 10000 og 20000 hafa verið afhentar í hvíta vöruhúsið og Sammy byrjar að vinna úr innkaupamóttökum.  

## Vörurnar mótteknar

Á síðunni **Vöruhús móttaka** er hægt að meðhöndla margar pantanir á innleið fyrir upprunaskjöl, til dæmis innkaupapantanir.  

### Vörurnar mótteknar  
1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vöruhúsamóttökur** og velja síðan viðkomandi tengil.  
2.  Valið er aðgerðin **Nýtt**.  
3.  Í reitnum **Birgðageymslu kóði** færið inn HVÍTT.  
4.  Veldu **Aðgerðir**, síðan **Virkni**, veldu síðan aðgerðina **Nota afmarkanir til að sækja uppr.skjöl**.  
5.  Í reitnum **Kóti** skal færa inn **AUKABÚNAÐUR**.  
6.  Í reitnum **Lýsing** eru slegnir inn **Lánardrottnar 10000 og 20000**.  
7.  Velja aðgerðina **Breyta**.  
8.  Í flýtiflipanum **Innkaup** í reitinn **Kaupa-frá lánardrottinn nr. Afmörkun** er fært inn **10000&#124;20000**.  
9. Velja skal aðgerðina **Keyra**. Fyllt er út í vöruhúsamóttöku með fjórum línum sem standa fyrir innkaupapantanalínur þeirra lánardrottna sem hafa verið tilgreindir. Reiturin **Magn til móttöku** er fylltur vegna þess að þú valdir ekki gátreitinn **Ekki fylla magn til afgreiðslu** á síðunni **Afmarkanir til að sækja upprunaskjöl**.  
10. Ef ætlunin er að nota síu eins og lýst var fyrr í þessum hluta skal velja **Sækja upprunaskjal** aðgerðina og velja svo innkaupapantanir frá viðkomandi lánardrottnum.  
11. Veldu aðgerðina **Bóka**, síðan aðgerðina **Bóka móttöku** og síðan hnappinn **Já**.  

    Jákvæðar birgðafærslur eru stofnaðar og sýna bókaðar innkaupamóttökur fylgihluta frá lánardrottnum 10000 og 20000 og vörurnar eru tilbúnar til frágangs í móttökuhólfi vöruhússins.  

## Vörufrágangur

Á síðunni **Frágangur vöruhúss** er hægt að vinna með frágang fyrir tiltekið vöruhúsamóttökuskjal sem nær til margra upprunaskjala. Eins og í öllum vöruhúsaaðgerðaskjölum eru Taka- og Setja-línur fyrir hverja vöru í frágangi vöruhúss. Í eftirfarandi aðgerð er hólfkótinn í Taka-línunum sjálfgefna móttökuhólfið í HVÍTU staðsetningunni W-08-0001.  


### Til að ganga frá vörunum  
1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Frágangur** og velja síðan viðkomandi tengil.  
2.  Veldu eina frágangsskjal vöruhúss á listanum og veldu svo aðgerðina **Breyta**.  

    Vöruhúsafrágangsskjölin opnast með átta Taka- eða Setja-línum fyrir innkaupapöntunarlínurnar fjórar.

    Starfsmaður í vöruhúsi er sagt að það þurfi 40 hjarir í samsetningardeildinni og í kjölfarið skiptir hann einni staðsetningarlínu til að tilgreina aðra staðsetningarlínu fyrir hólf W-02-0001 í samsetningardeildinni þar sem starfsmaður vöruhússins setur þann hluta á mótteknum hjörum.  

3.  Veldu aðra línuna í **Frágangur vöruhúss** síðunni, Setja-línuna fyrir vöru 70200.  
4.  Breyttu gildinu úr 100 í 60 í **Magn til afgreiðslu** reitnum.  
5.  Á flýtiflipanum **Línur** skal velja **Aðgerðir** og síðan **Skipta línu**. Ný lína er sett inn fyrir vöru 70200 með 40 í **Magn til afgreiðslu** reitnum.  
6.  Í reitinn **Hólfkóti** skal færa inn W-02-0001. Sjálfkrafa er fyllt út í reitinn **Kóti þjónustusvæðis**.  

    Sjálfgefið er að **Svæðiskóði** í sölulínunni sé falinn og því þarf að kalla hann fram. Til að gera þetta þarftu að sérstilla síðuna. Frekari upplýsingar eru í [Hefja sérstillingu á síðu með borðanum Sérstilla](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

    Næst skal skrá fráganginn.  

7.  Veljið aðgerðina **Skrá frágang** og svo hnappinn **Já**.  

    Mótteknir fylgihlutir eru nú frágengnir í sjálfgefnum hólfum varanna og 40 lamir eru í samsetningardeildinni. Nú er hægt að tína mótteknar vörur fyrir innri eftirspurn, svo sem samsetningarpantanir, eða ytri eftirspurn, svo sem söluafhendingar.  

## Sjá einnig  
 [Ganga frá vörum með vöruhúsafrágangi](warehouse-how-to-put-items-away-with-warehouse-put-aways.md)   
 [Færa vörur með ítarlegum vöruhúsaaðgerðum](warehouse-how-to-move-items-in-advanced-warehousing.md)   
 [Hönnunarupplýsingar: vöruhúsaflæði inn](design-details-inbound-warehouse-flow.md)   
 <!-- [Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations](walkthrough-receiving-and-putting-away-in-basic-warehousing.md)    -->
 [Kynningar á viðskiptaferli](walkthrough-business-process-walkthroughs.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
