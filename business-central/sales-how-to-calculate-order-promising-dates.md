---
title: Reikna út dagsetningar pöntunarlofgreiðslu
description: Pöntunarloforðsaðgerðin nýtist til að reikna fyrstu hugsanlegu dagsetningu fyrir sendingu eða afhendingu á vöru.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 03/05/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="calculate-order-promising-dates"></a>Reikna út dagsetningar pöntunarlofgreiðslu

Fyrirtæki verður að geta upplýst viðskiptamenn sína um afhendingardagsetningar pöntunar. Síðan **Línur pöntunarloforðs** gerir kleift að framkvæma þetta í sölupöntun.  

[!INCLUDE[prod_short](includes/prod_short.md)] reiknar út sendingar og afhendingardaga út frá þekktum og væntanlegum lausum dagsetingum sem þú getur lofað viðskiptamönnum.  

Ef tilgreindur er afgreiðsludagsetning á sölupöntunarlínunni notar forritið þessa dagsetningu sem upphafspunkt fyrir eftirfarandi útreikninga  

- Umbeðin afgreiðsludagsetning – Flutningstími = Áætluð afhendingardagsetning  
- sfhendingardagsetning + afgr.tími vara á útl. úr vöruh. = afh.dags.  

Ef varan er tiltæk til tínslu á afhendingardagsetningu þá getur söluferlið haldið áfram. Ef varan er ekki tiltæk til tínslu á afhendingardegi þá birtist viðvörun um útsendingu á birgðum.  

Ef ekki er tilgreind umbeðin afgreiðsludagsetning á sölupöntunarlínu eða ef ekki er hægt að uppfylla umbeðna afgreiðsludagsetningu er fyrsta dagsetningin þegar vörurnar eru tiltækar reiknaðar. Sú dagsetning er síðan færð í reitinn **Afh.dags** í línunni og dagsetningin þegar ætlunin er að senda vörurnar og dagsetninguna þegar afhentar verða viðskiptamanni eru reiknaðar með eftirfarandi útreikningum:  

- Afhendingardagsetning + afgr.tími vara á útl. úr vöruh. = Áætluð afhendingardagsetning  
- áætluð afhendingardagsetning + flutningstími = áætluð afgreiðsludagsetning  

## <a name="about-order-promising"></a>Um pöntunarlofun

Aðgerðin Pöntunarloforð gerir kleift að lofa því að pöntun verði send eða afhent á tilteknum degi. Kerfið reiknar út hvenær vara er tiltæk eða hægt að lofa henni og það býr til pöntunarlínur fyrir þær dagsetningar sem samþykktar eru. Pöntunarloforðsaðgerðin reiknar fyrstu hugsanlegu dagsetningu fyrir sendingu eða afhendingu á vöru. Einnig eru búnar til innkaupabeiðnilínur, ef fyrst skyldi þurfa að kaupa inn eða framleiða vörurnar, fyrir dagsetningarnar sem eru samþykktar.

[!INCLUDE[prod_short](includes/prod_short.md)] notar tvö grundvallarhugtök:  

- Tiltækt að lofa (ATP)  
- Hægt að lofa (CTP)  

### <a name="available-to-promise"></a>Tiltækt til að lofa

Tiltæk til að lofa (ATP) reiknar út dagsetningar á grundvelli frátekningarkerfisins. Hún framkvæmir athugun á ófráteknu magni í birgðum vegna áætlaðrar framleiðslu, innkaupa, millifærslu og vöruskila sölu. Á grundvelli þessarar upplýsinga, reiknar [!INCLUDE[prod_short](includes/prod_short.md)] afhendingardagsetningu fyrir pöntun viðskiptamanns þar sem vörurnar eru tiltækar, annaðhvort í birgðum eða í áætluðum móttökum.  

### <a name="capable-to-promise"></a>Ekki hægt að lofa

Hægt að lofa (CTP) gerir ráð fyrir "hvað ef" dæmi, sem á aðeins við um vörumagn sem er ekki í birgðum eða á tímasettum pöntunum. Reiknar út fyrsta daginn sem varan getur verið tiltæk ef framleiða á [!INCLUDE[prod_short](includes/prod_short.md)]  hana, kaupa eða flytja hana.

#### <a name="example"></a>Dæmi

Ef pöntun er fyrir 10 stykki og 6 stykki eru tiltæk í birgðum eða á tímasettum pöntunum er hægt að lofa útreikningum á 4 stykkjum.

### <a name="calculations"></a>Útreikningar

Þegar [!INCLUDE[prod_short](includes/prod_short.md)] reiknar afhendingardagsetningu viðskiptamanns framkvæmir það tvo verkhluta:  

- Reiknar út fyrsta afgreiðsludag þegar viðskiptamaðurinn hefur ekki beðið um tiltekna afgreiðsludagsetningu.  
- Vottar hvort afhendingardagsetningin sem viðskiptavinurinn biður um eða er lofað er raunsæ.  

Ef viðskiptamaðurinn óskar ekki eftir tiltekinni afgreiðsludagsetningu er afhendingardagsetningin stillt á vinnudagsetninguna og það sem er til ráðstöfunar er byggt á þeirri dagsetningu. Ef varan er í birgðum reiknar [!INCLUDE[prod_short](includes/prod_short.md)] fram í tíma til að ákvarða hvenær afhenda megi pöntunina. Þetta næst með eftirfarandi formúlum:  

- Afhendingardagsetning + afgr.tími vara á útl. úr vöruh. = Áætluð afhendingardagsetning  
- Áætluð afhendingardagsetning – Flutningstími = Áætluð afgreiðsludagsetning  

[!INCLUDE[prod_short](includes/prod_short.md)] síðan er sannreynt hvort útreiknuð afhendingardagsetning er raunhæf með því að reikna aftur í tímann til að ákvarða hvenær varan verður að vera tiltæk til að standast setta dagsetningu. Þetta næst með eftirfarandi formúlum:  

- Áætluð afhendingardagsetning – Flutningstími = Áætluð afgreiðsludagsetning  
- Áætluð afhendingardagsetning - Afgreiðslutími út úr vöruhúsi + Afh.dags.  

Afhendingardagsetning er notuð til að gera til ráðstöfunarathugunina. Ef varan er tiltæk á þeim degi staðfestir [!INCLUDE[prod_short](includes/prod_short.md)] að umbeðin/lofuð afhending standist með því að stilla áætlaða afhendingardagsetningu á umbeðna/lofaða dagsetningu. Ef varan er ekki tiltæk er auðri dagsetningu skilað og þá getur pöntunarvinnslan notað CTP-virkni.  

Byggt á nýjum dagsetningum og tímum, allar tengdar dagsetningar eru reiknaðar samkvæmt reiknireglum sem lýst var fyrr í þessum kafla. CTP-útreikningurinn tekur lengri tíma en gefur nákvæmari dagsetningu þess hvenær viðskiptavinurinn gefur vænst þess að fá vöruna afhenta. Dagsetningarnar sem eru reiknaðar með CTP eru sýndar í **Áætluð afhendingardagsetning** og **Fyrsti mögulegi afhendingardagur** svæðunum á síðunni **Pöntun lofað línur**.  

Pantanavinnsla lýkur CTP-ferlinu með því að samþykkja dagsetningarnar. Þetta þýðir að áætlunarlína og frátekningarfærslan hafa verið stofnaðar fyrir vöruna fyrir reiknaðar dagsetningar til að tryggja að pöntunin sé uppfyllt.  

Auk ytri pantanaloforða sem hægt er að framkvæma á síðunni **Línur pöntunarloforða** er einnig hægt að lofa innri eða ytri afhendingardagsetningu fyrir uppskriftavörur. Frekari upplýsingar, sjá [Skoða tiltækileika vöru](inventory-how-availability-overview.md).

## <a name="to-set-up-order-promising"></a>Uppsetning pöntunarloforðs

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning pöntunarloforðs** og velja síðan viðkomandi tengil.  
2. Númer og tímaeiningarkóti er fært inn í reitinn **Mótfært (Tími)**. Einn af eftirfarandi kótum er valinn:  

    |Kóti|Lýsing|  
    |----------|-----------------|  
    |**d**|Almanaksdagur|  
    |**v**|Vika|  
    |**m**|Mánuður|  
    |**f**|Fjórðungur|  
    |**á**|Ár|  

    Til dæmis merkir “3v” að mótfærður tími eða frestur er þriggja vikna. Til að gefa til kynna gildandi tímabil, setjið forlið fyrir alla þessa kóta með bókstafnum “ c “. Eigi til dæmis mótfærður tími að vera yfirstandandi mánuður er fært inn **cm**.  
3. Númeraröð er færð inn í reitinn **Pöntunarloforð nr.** með því að velja línu af listanum á síðunni **Nr. röð**.  
4. Sniðmát pöntunarloforða er fært inn í reitinn **Sniðmát pöntunarloforða** með því að velja línu af listanum á síðunni **Listi yfir innkaupatillögusniðmát** .  
5. Innkaupatillögusniðmát er fært inn í reitinn **Pöntunarloforð Innkaupatillaga** með því að velja línu af listanum á síðunni **Listi yfir innkaupatillögusniðmát** .

### <a name="inbound-and-outbound-warehouse-handling-times-in-order-promising"></a>Afgreiðslutímar á afgreiðslutíma á vörum inn og út í vöruhús til þess að því er efnislegt

Ef afgreiðslutími vöruhúss þegar reiknað er út hvenær á að lofa pöntun í innkaupalínunni skal tilgreina á síðunni **Birgðauppsetning** sjálfgefinn afgreiðslutíma til að nota í sölu- og innkaupaskjölum. Einnig er hægt að færa inn ákveðna tíma fyrir hverja staðsetningu á síðunni **Birgðageymsluspjald**. 

#### <a name="to-enter-default-inbound-and-outbound-warehouse-handling-times-for-sales-and-purchase-documents"></a>Til að færa inn afgreiðslutíma vöruhús á inn- og útleið fyrir sölu- og innkaupaskjöl

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning birgða** og velja síðan viðkomandi tengil.  
2. Í flýtiflipanum **Almennt**, í reitnum **Afgr.tími vara á innl. í vöruh.** og **Afgr.tími vara á útl. úr vöruh** skal færa inn dagafjöldann sem á taka með í útreikningi á því hvenær pöntunum er lofað.  

#### <a name="to-enter-inbound-and-outbound-warehouse-handling-times-on-locations"></a>Að færa inn afgreiðslutíma vöruhúss fyrir inn- og útleið í birgðageymslum

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Staðsetningu** og velja síðan viðkomandi tengil.  
2.  Opna skal viðeigandi birgðageymsluspjald.  
3.  Í flýtiflipanum **Vöruhús**, í reitina **Afgr.t. vara á innl. í vöruh** og **Afgr.tími vara á útl. úr vöruh** skal færa inn dagafjöldann sem á að taka með í útreikningi á hvenær pöntunum er lofað.  

> [!NOTE]  
>  Þegar innkaupapöntun er stofnuð, ef þú velur **Birgðageymslu** í reitnum **Senda til** í flýtiflipanum **Afhending og greiðsla** og velur síðan birgðageymslu í reitnum **Kóði birgðageymslu** munu reitirnir **Afgr.tími vara á útl. úr vöruh** og **Afgr.t. vara á innl. í vöruh** nota afgreiðslutímann sem tilgreindur er fyrir birgðageymsluna. Fyrir sölupantanir gildir það sama ef þú velur birgðageymslu í reitnum **Kóði birgðageymslu**. Ef enginn afgreiðslutími er tilgreindur fyrir birgðageymsluna verða reitirnir **Afgr.tími vara á útl. úr vöruh** og **Afgr.t. vara á innl. í vöruh** auðir. Ef reiturinn **Kóði birgðageymslu** er skilinn eftir auður í sölu- og innkaupaskjölum notar útreikningurinn afgreiðslutíma sem tilgreindur er á síðunni **Birgðauppsetning**.

## <a name="to-make-an-item-critical"></a>Varan bundin:

Áður en vara er sett inn í útreikning pöntun lofað, verður að merkja hana sem mikilvægt. Þessi uppsetning tryggir að vörur sem ekki eru mikilvægar valda ekki útreikningum á lofun pöntunar ekki óviðkomandi útreikningum á lofun pöntunar.   
1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur** og velja síðan viðkomandi tengil.  
2.  Viðeigandi birgðaspjald er opnað.  
3.  Á flýtiflipanum **Áætlun** skal velja svæðið **Bundið**.  

## <a name="to-calculate-an-order-promising-date"></a>Dagsetning pöntunarloforðs reiknuð:

1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sölupöntun** og velja síðan viðkomandi tengil.  
2.  Glugginn sölupöntun er opnaður og sölupöntunarlínurnar sem forritið á að reikna valdar.  
3.  Veldu aðgerðina **Pöntun lofað** og veldu svo aðgerðina **Pöntun lofað línur**.  
4.  Veldu línu og síðan einn af eftirfarandi valmöguleikum:  

    - Velja skal  **Tiltæki** ef kerfið á að reikna út hvaða dag varan verður fyrst tiltæk að teknu tilliti til birgða, áætlaðrar móttöku og brúttóþarfa.  
    - Velja skal  **Óhætt að lofa** ef vitað er að varan er ekki til í birgðahaldi og ef kerfið á að reikna út hvenær varan verður fyrst tiltæki með því að gefa út tillögur um endurnýjun.  
5.  Velja hnappinn **Samþykkja** til að samþykkja fyrstu tiltæku sendingardagsetningu.  

## <a name="see-also"></a>Sjá einnig .

[Sala](sales-manage-sales.md)  
[Dagsetning útreiknings fyrir kaup](purchasing-date-calculation-for-purchases.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
