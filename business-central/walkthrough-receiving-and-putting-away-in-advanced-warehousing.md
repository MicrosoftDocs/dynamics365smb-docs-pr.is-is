---
title: Móttaka og frágangur í ítarlegum vöruhúsaaðgerðum | Microsoft Docs
description: Í Business Central er hægt að framkvæma innleiðarferlið til að taka við og ganga frá á fjóra vegu, með því að nota mismunandi eiginleika, allt eftir flækjustigi vöruhússins.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f7badb1b8e43e98b8d2088ab8d963f46a5fc3f48
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/09/2021
ms.locfileid: "6214629"
---
# <a name="walkthrough-receiving-and-putting-away-in-advanced-warehouse-configurations"></a>Kynning: Móttaka og Frágangur í ítarlegri grunngerð vöruhúss

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

Í [!INCLUDE[prod_short](includes/prod_short.md)], er hægt að framkvæma innleiðarferlið til að taka við og ganga frá á fjóra vegu, með því að nota mismunandi eiginleika, allt eftir flækjustigi vöruhússins.  

|Aðferð|Ferli á innleið|Hólf|Móttökur|Frágangur|Flækjustig (Sjá [Hönnunarupplýsingar: uppsetning vöruhúss](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Bóka móttöku og frágang frá pöntunarlínunni|X|||2|  
|Á|Bóka móttöku og frágang frá birgðafrágangsskjali|||X|3|  
|C|Bóka móttöku og frágang frá vöruhúsamóttökuskjali||X||4/5/6|  
|D|Bóka móttöku frá vöruhúsamóttökuskjali og bóka frágang frá vöruhúsafrágangsskjali||X|X|4/5/6|  

Nánari upplýsingar er að finna í [Hönnunarupplýsingar: vöruhúsaflæði inn](design-details-inbound-warehouse-flow.md).  

Eftirfarandi kynning sýnir aðferð D í fyrri töflu.  

## <a name="about-this-walkthrough"></a>Um kynninguna  
Í vöruhúsi ítarlegrar grunngerðar þar sem birgðageymsla er sett upp þannig að krafist sé móttökuvinnslu til viðbótar frágangsvinnslu skal nota síðuna **Vöruhús móttaka** til að skrá og bóka móttöku og afhendingarupplýsingar fyrir upprunaskjöl á innleið. Þegar vöruhúsamóttaka er bókuð eru eitt eða fleiri vöruhúsafrágangsskjöl stofnuð til að gefa starfsmönnum í vöruhúsi fyrirmæli um að færa mótteknar vörur á tiltekna staði í samræmi við hólfauppsetningu eða í önnur hólf. Nákvæm staðsetning varanna skráist við skráningu frágangs í vöruhúsi. Upprunaskjalið á innleið getur verið innkaupapöntun, söluvöruskilapöntun, millifærslupöntun á innleið eða framleiðslupöntun þar sem úttakið er tilbúið til frágangs. Ef móttakan er búin til úr pöntun á innleið fást fleiri en eitt upprunaskjal á innleið fyrir móttökuna. Með þessari aðferð hægt er að skrá margar vörur frá mismunandi pöntunum á innleið með einni móttöku.  

Þessi kynning fjallar um eftirfarandi verk.  

-   HVÍT birgðageymsla sett upp fyrir móttöku og frágang.  
-   Stofnun og útgáfa tveggja innkaupapantana til að hámarka afgreiðslutíma á vörum í vöruhúsi.  
-   Stofnaðu og bókaðu vöruhúsamóttökuskjal fyrir margar innkaupapantanalínur frá tilteknum lánardrottnum.  
-   Skráning á vöruhúsafrágangi fyrir mótteknar vörur.  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]
## <a name="roles"></a>Hlutverk  
Þessi kynning sýnir þau verk sem framkvæmd eru með eftirfarandi hlutverkum notenda:  

-   Yfirmaður vöruhúss  
-   Innkaupaaðili  
-   Starfsmenn í móttöku  
-   Starfsmaður í vöruhúsi  

## <a name="prerequisites"></a>Frumskilyrði  
Til að ljúka þessari kynningu þarf:  

-   CRONUS International Ltd. er uppsett.  
-   Notandi verður að starfsmanni vöruhúss í hvítri birgðageymslu á eftirfarandi hátt:  

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vöruhúsastarfsmenn** og veldu síðan tengda tengilinn.  
2.  Velja reitinn **Notandakenni** og velja síðan eigin notandareikning notanda á síðunni **Notendur**.  
3.  Í reitnum **Birgðageymslu kóti** færið inn HVÍTT.  
4.  Veljið reitinn **Sjálfgefið**.  

## <a name="story"></a>Ferill  
Ellen, stjórnandi vöruhúss í CRONUS International Ltd. stofnar tvær innkaupapantanir fyrir fylgihlutavörur frá lánardrottnum 10000 og 20000 sem afhenda á til WHITE vöruhúss. Þegar vörur eru afhentar í vöruhúsið notar Sammy, sem ber ábyrgð á móttöku vara frá lánardrottnum 10000 og 20000, afmörkun til að stofna móttökulínur fyrir innkaupapantanir sem koma frá tveimur lánardrottnum. Sammi skráir vörurnar sem mótteknar í einni vöruhúsamóttöku og gerir þær tiltækar til sölu eða annarrar ráðstöfunar. Jón í vöruhúsinu tekur hlutina úr móttökuhólfinu og gengur frá þeim. Hann setur allar einingarnar í sjálfgefið hólf, nema 40 af 100 mótteknum lömum sem hann flytur í samsetningardeildina með því að skipta frágangslínunni. Þegar John skráir fráganginn er hólfainnihald uppfært og vörurnar gerðar tiltækar til tínslu úr vöruhúsinu.  

## <a name="reviewing-the-white-location-setup"></a>Farið yfir HVÍTU birgðageymsluuppsetninguna  
Uppsetning síðunnar **Birgðageymsluspjald** skilgreinir vöruhúsaflæði fyrirtækisins.  

### <a name="to-review-the-location-setup"></a>Til að fara yfir uppsetningu birgðageymslunnar  

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Staðsetningar** og veldu síðan tengda tengilinn.  
2.  HVÍTT-staðsetningarspjaldið er opnað.  
3.  Athugasemd á flýtiflipanum **Vöruhús** um að gátmerkið **Beinn frágangur og tínsla** hafi verið valið.  

    Þetta þýðir að birgðageymslan er sett upp fyrir hæsta flækjustig, eins og sést á því að allir gátreitir fyrir vöruhúsaafgreiðslu eru valdir.  

4.  Athugasemd á flýtiflipanum **Hólf** um að hólf séu tilgreind í reitunum **Hólfkóti móttöku** og **Hólfkóti afhendingar**.  

Þetta þýðir að þegar vöruhúsamóttaka er stofnuð er þessi hólfkóti sjálfgefið afritaður í haus vöruhúsamóttökuskjalsins og í línur vöruhúsafrágangsins sem verður til.  

## <a name="creating-the-purchase-orders"></a>Stofna innkaupapantanirnar  
Innkaupapantanir eru algengustu tegundir af upprunaskjölum á innleið.  

### <a name="to-create-the-purchase-orders"></a>Innkaupapantanir stofnaðar  

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innkaupapantanir** og veldu síðan tengda tengilinn.  
2.  Valið er **Nýtt** aðgerð.  
3.  Stofna innkaupapöntun fyrir lánardrottinn 10000 á vinnudeginum (23. Janúar) með eftirfarandi innkaupapöntunarlínum.  

    |Vara|Staðsetningarkóði|Magn|  
    |----------|-------------------|--------------|  
    |70200|HVÍTT|100 STYKKI|  
    |70201|HVÍTT|50 STYKKI|  

    Tilkynnið svo vöruhúsinu að innkaupapöntunin sé tilbúin til afgreiðslu í vöruhúsi þegar sendingin berst.  

4.  Valið er **Losa** aðgerð.  

    Búðu nú til aðra innkaupapöntunina.  

5.  Valið er **Nýtt** aðgerð.  
6.  Stofna innkaupapöntun fyrir lánardrottinn 20000 á vinnudeginum með eftirfarandi innkaupapöntunarlínum.  

    |Vara|Staðsetningarkóði|Magn|  
    |----------|-------------------|--------------|  
    |70100|HVÍTT|10 dósir|  
    |70101|HVÍTT|12 dósir|  

    Valið er **Losa** aðgerð.  

    Vörur frá lánardrottnum 10000 og 20000 hafa verið afhentar í hvíta vöruhúsið og Sammy byrjar að vinna úr innkaupamóttökum.  

## <a name="receiving-the-items"></a>Vörurnar mótteknar  
Á síðunni **Vöruhús móttaka** er hægt að meðhöndla margar pantanir á innleið fyrir upprunaskjöl, til dæmis innkaupapantanir.  

### <a name="to-receive-the-items"></a>Vörurnar mótteknar  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vöruhúsamóttökur** og veldu síðan tengda tengilinn.  
2.  Valið er **Nýtt** aðgerð.  
3.  Í reitnum **Birgðageymslu kóti** færið inn HVÍTT.  
4.  Velja skal **Nota afmarkanir til að sækja uppr.skjöl.** aðgerðina.  
5.  Í reitnum **Kóti** skal færa inn **AUKABÚNAÐUR**.  
6.  Í reitnum **Lýsing** eru slegnir inn **Lánardrottnar 10000 og 20000**.  
7.  Velja aðgerðina **Breyta**.  
8.  Í flýtiflipanum **Innkaup** í reitinn **Kaupa-frá lánardrottinn nr. Afmörkun** er fært inn **10000&#124;20000**.  
9. Velja skal aðgerðina **Keyra**. Fyllt er út í vöruhúsamóttöku með fjórum línum sem standa fyrir innkaupapantanalínur þeirra lánardrottna sem hafa verið tilgreindir. Reiturin **Magn til móttöku** er fylltur vegna þess að þú valdir ekki gátreitinn **Ekki fylla magn til afgreiðslu** á síðunni **Afmarkanir til að sækja upprunaskjöl**.  
10. Ef ætlunin er að nota síu eins og lýst var fyrr í þessum hluta skal velja **Sækja upprunaskjal** aðgerðina og velja svo innkaupapantanir frá viðkomandi lánardrottnum.  
11. Veljið **Bóka móttöku** og svo hnappinn **Já**.  

    Jákvæðar birgðafærslur eru stofnaðar og sýna bókaðar innkaupamóttökur fylgihluta frá lánardrottnum 10000 og 20000 og vörurnar eru tilbúnar til frágangs í móttökuhólfi vöruhússins.  

## <a name="putting-the-items-away"></a>Vörufrágangur  
Á síðunni **Frágangur vöruhúss** er hægt að vinna með frágang fyrir tiltekið vöruhúsamóttökuskjal sem nær til margra upprunaskjala. Eins og í öllum vöruhúsaaðgerðaskjölum eru Taka- og Setja-línur fyrir hverja vöru í frágangi vöruhúss. Í eftirfarandi aðgerð er hólfkótinn í Taka-línunum sjálfgefna móttökuhólfið í HVÍTU staðsetningunni W-08-0001.  

### <a name="to-put-the-items-away"></a>Til að ganga frá vörunum  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Frágangur** og veldu síðan tengda tengilinn.  
2.  Veldu eina frágangsskjal vöruhúss á listanum og veldu svo aðgerðina **Breyta**.  

    Vöruhúsafrágangsskjölin opnast með átta Taka- eða Setja-línum fyrir innkaupapöntunarlínurnar fjórar.

    Starfsmanni í vöruhúsi er sagt að 40 lamir þurfi í samsetningardeild. Hann byrjar á því að skipta Setja-línunni upp til að geta tilgreint aðra Setja-línu fyrir hólf W-02-0001 í samsetningardeild, þar sem hann setur hluta hinna mótteknu lama.  

3.  Veldu aðra línuna í **Frágangur vöruhúss** síðunni, Setja-línuna fyrir vöru 70200.  
4.  Breyttu gildinu úr 100 í 60 í **Magn til afgreiðslu** reitnum.  
5.  Á flýtiflipanum **Línur** skal velja **Aðgerðir** og síðan **Skipta línu**. Ný lína er sett inn fyrir vöru 70200 með 40 í **Magn til afgreiðslu** reitnum.  
6.  Í reitinn **Hólfkóti** skal færa inn W-02-0001. Sjálfkrafa er fyllt út í reitinn **Kóti þjónustusvæðis**.  

    Næst skal skrá fráganginn.  

7.  Veljið aðgerðina **Skrá frágang** og svo hnappinn **Já**.  

    Mótteknir fylgihlutir eru nú frágengnir í sjálfgefnum hólfum varanna og 40 lamir eru í samsetningardeildinni. Nú er hægt að tína mótteknar vörur fyrir innri eftirspurn, svo sem samsetningarpantanir, eða ytri eftirspurn, svo sem söluafhendingar.  

## <a name="see-also"></a>Sjá einnig  
 [Ganga frá vörum með vöruhúsafrágangi](warehouse-how-to-put-items-away-with-warehouse-put-aways.md)   
 [Færa vörur með ítarlegum vöruhúsaaðgerðum](warehouse-how-to-move-items-in-advanced-warehousing.md)   
 [Hönnunarupplýsingar: vöruhúsaflæði inn](design-details-inbound-warehouse-flow.md)   
 <!-- [Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations](walkthrough-receiving-and-putting-away-in-basic-warehousing.md)    -->
 [Kynningar á viðskiptaferli](walkthrough-business-process-walkthroughs.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]