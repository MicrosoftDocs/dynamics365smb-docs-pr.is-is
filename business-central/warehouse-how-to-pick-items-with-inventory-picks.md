---
title: Hvernig á að tína vörur með birgðatínslu
description: Fræðast um notkun birgðatínslu til að skrá og bóka tínslu- og afhendingarupplýsingar fyrir upprunaskjöl.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.forms: '931, 7377'
---
# <a name="pick-items-with-inventory-picks"></a>Vörur tíndar með birgðatínslu

Vörur [!INCLUDE[prod_short](includes/prod_short.md)] eru tíndar og afhentar með einni af fjórum aðferðum, eins og lýst er í eftirfarandi töflu.

|Aðferð|Útleiðarferli|Krefjast tínslu|Krefjast afhendingar|Flóknarastig (Fræðast meira um [vöruhúsakerfisyfirlit](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Bóka tínsluna og afhendinguna úr pöntunarlínunni|||Engin sérstök vöruhúsaaðgerð.|  
|Á|Bóka tínslu og afhendingu úr birgðatínsluskjali|Kveikt||Grunnur: Pöntun-fyrir-pöntun.|  
|U|Bóka tínslu og afhendingu úr vöruhúsaafhendingarskjali||Kveikt|Grunnur: Bókuð móttaka/sending í mörgum pöntunum.|  
|D|Tínslan er bókuð úr vöruhúsatínsluskjali og afhendingin bókuð úr vöruhúsaafhendingarskjali|Kveikt|Kveikt|Ítarlegt|  

Nánari upplýsingar í Vöruhúsaflæði á [útleið](design-details-outbound-warehouse-flow.md).

Þessi grein vísar til aðferðar B í töflunni.

Þegar birgðageymslan er sett upp til að krefjast tínsluvinnslu en ekki afhendingarvinnslu skal nota **síðuna Birgðatínsla** til að skrá og bóka tínslu og afhendingu upplýsinga fyrir upprunaskjölin. Upprunaskjöl á útleið geta verið sölupantanir, innkaupavöruskilapantanir og millifærslupantanir á útleið.

> [!NOTE]
> Íhlutaþarfir framleiðslu- og samsetningarpöntunar tákna einnig upprunaskjöl á útleið. Fræðast meira um meðhöndlun framleiðslu- og samsetningarpantana fyrir innanhússvinnslur í [Hönnunarupplýsingar: Vöruhúsaflæði innanhúss](design-details-internal-warehouse-flows.md).
>
> Þó þjónustupantanir séu einnig upprunaskjöl á útleið styðja þær ekki grunnstig flókinna pantana fyrir pöntun.
>
> Við tínslu og afhendingu sölulínumagns sem sett er saman í pöntunina eru reglur sem fylgja þarf þegar birgðatínslulínur eru stofnaðar. Fræðast meira um [samsetningarvörur í pöntun með birgðatínslu](#handling-assemble-to-order-items-with-inventory-picks).  

Hægt er að stofna birgðatínslu á þrjá vegu:

* Birgðatínslan er stofnuð beint úr upprunaskjalinu.  
* Stofna birgðatínslu fyrir mörg upprunaskjöl samtímis með keyrslu.
* Tínslan er beðin um í tveim þrepum með því að gefa upprunaskjalið fyrst út sem merki til vöruhússins um að upprunaskjalið sé tilbúið tínslu.

Síðan er hægt að stofna birgðatínslu á síðunni **Birgðatínsla** á grundvelli upprunaskjalsins.  

## <a name="to-create-an-inventory-pick-from-the-source-document"></a>Birgðatínsla stofnuð í upprunaskjali:

1. Í upprunaskjalinu, sem getur verið sölupöntun, innkaupavöruskilapöntun eða millifærslupöntun á útleið, skal velja aðgerðina **Stofna birgðafrágang/tínslu** .
2. Velja skal reitinn **Stofna birgðafrávik Tínslureiturinn** .  
3. Velja hnappinn **Í lagi**. Ný birgðatínsla verður stofnuð.

## <a name="to-create-multiple-inventory-picks-with-a-batch-job"></a>Fleiri en ein birgðatínsla stofnuð með keyrslu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teikn, færa inn **Stofna birgðafrágang/tínslu/hreyfingu** og velja síðan viðeigandi tengil.  
2. Á flýtiflipanum **Vöruhúsabeiðni** skal nota **Upprunaskjal og** Upprunanúmer **.** til að afmarka eftir tilteknum tegundum fylgiskjala eða sviðum fylgiskjalsnúmera. Til dæmis er hægt að stofna tínslu einungis fyrir sölupantanir.  
3. Á flýtiflipanum **Valkostir** er reiturinn Stofna birgðafrávik **valinn. Tínslureiturinn** .
4. Velja hnappinn **Í lagi**.

## <a name="to-create-the-pick-in-two-steps"></a>Tínslan stofnuð í tveimur þrepum

### <a name="to-request-an-inventory-pick-by-releasing-the-source-document"></a>Til að biðja um birgðatínslu með því að gefa út upprunaskjalið

Fyrir sölupantanir, innkaupaskilapantanir og millifærslupantanir á útleið er vöruhússbeiðnin stofnuð með því að gefa út pöntunina. Ef pöntunin er gerð út gera vörurnar tiltækar til tínslu.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.
2. Valinn er sölupöntun sem á að gefa út og velja síðan aðgerðina **Gefa út**.

### <a name="to-create-an-inventory-pick-based-on-the-source-document"></a>Birgðatínsla stofnaður á grundvelli upprunaskjals

Þegar pöntun hefur verið gefin út getur starfsmaður vöruhússins stofnað birgðatínslu.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, farðu í **Birgðatínsla** og veldu síðan viðkomandi tengil.  
2. Valið er aðgerðin **Nýtt**.  
3. Í reitnum **Upprunaskjal** er valin tegund fylgiskjalsins sem verið er að tína fyrir.  
4. Í reitnum **Forðanr.** er forðaskjal valið.  
5. Einnig er hægt að velja aðgerðina **Sækja upprunaskjal** til að stofna lista yfir öll upprunaskjöl á útleið sem eru tilbúin til tínslu í birgðageymslunni.  
6. Hnappurinn **Í lagi** er valinn til að fylla út tínslulínurnar eftir völdum upprunaskjölum.  

## <a name="to-record-inventory-picks"></a>Til að skrá birgðatínslur

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, farðu í **Birgðatínsla** og veldu síðan viðkomandi tengil.  
2. í reitnum **Hólfakóði** í tínslulínunum, hólfið sem vörurnar þurfa að vera tíndar úr er tillaga á sjálfgefið hólf vörunnar. Hægt er að skipta um hólf á þessari síðu ef með þarf.  
3. Tínslan er framkvæmd og magnið sem fært er inn í reitinn **Magn til afgreiðslu er fært** inn.

    Ef tína þarf vörur fyrir línu úr fleiri en einu hólfi, til dæmis vegna þess að allt magnið er ekki í hólfinu, skal nota aðgerðina **Skipta línu** á flýtiflipanum **Línur** . Aðgerðin stofnar línu fyrir eftirstandandi magn sem á að meðhöndla.

4. Valið er **Bóka** aðgerðin.  

    * Bóka afhendingu upprunaskjalslínanna sem voru tíndar.
    * Ef hólf eru notuð í birgðageymslunni stofnar bókun einnig vöruhúsafærslur til að bóka breytingar á magni í hólfum.  

    [!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

## <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Meðhöndlun á vörum sem eru settar saman eftir pöntunum og birgðatínslum

Einnig er hægt að nota síðuna **Birgðatínsla** til að tína og senda fyrir sölu þar sem setja þarf saman vörur áður en hægt er að afhenda þær. Nánari upplýsingar um sölu á [vörum sem settar eru saman í pöntun](assembly-how-to-sell-items-assembled-to-order.md).

Samsetningarvörur í pöntun eru ekki efnislega í hólfi fyrr en þær eru settar saman og bókaðar sem frálag í hólf. Tínsla á vörum sem eru settar saman í pöntun úr hólfi fyrir afhendingar fylgir sérstakt flæði.

1. Starfsmenn í vöruhúsi færa samsetningaríhluti úr hólfi á afhendingarsvæði og bóka síðan birgðatínsluna.
2. Bókaða birgðatínslan bókar samsetningarfrálagið, íhlutanotkunina og söluafhendinguna.

Hægt er að setja upp [!INCLUDE[prod_short](includes/prod_short.md)] í búa til birgðahreyfingu sjálfkrafa þegar birgðatínsla fyrir samsetningarvöru er stofnuð. Reiturinn **Stofna hreyfingar sjálfvirkt** á síðunni **Samsetningargrunnur** er valinn. Nánari upplýsingar um [Uppsetning grunnvöruhúsa með aðgerðasvæðum](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md).

Birgðatínslulínur fyrir söluvörur eru stofnaðar með mismunandi hætti eftir því hvort ekkert, sumt eða allt magn sölulínunnar er sett saman í pöntun. Í dæmum þar sem sumt af magninu er sett saman og sumt er tekið úr birgðum eru stofnaðar minnst tvær tínslulínur.

Fyrir sölu þar sem allt magnið í sölupöntunarlínunni er sett saman í pöntun er ein birgðatínslulína stofnuð fyrir magnið. Gildið í reitnum **Magn til samsetningar** er það sama og gildið í reitnum **Magn til afhendingar** . **Setja saman í pöntun** reiturinn er valið í línunni.

Ef samsetningarfrálagsflæði er sett upp fyrir birgðageymsluna **inniheldur reiturinn Hólfkóti** á birgðatínslulínunni gildið úr eftirfarandi reitum í eftirfarandi röð.

* ***Hólfkóti afhendingarpöntunar til pöntunar** <!-- not applicable for inv pick-->
* **Kóti frá-samsetningarhólfs**

Ef hólfkóti er ekki tilgreindur á sölupöntunarlínunni og ekkert samsetningarfrálagsflæði er sett upp fyrir birgðageymsluna **er reiturinn Hólfkóti** á birgðatínslulínunni auður. Starfsmaður í vöruhúsi verður að opna síðuna **Hólfainnihald** og velja hólfið þar sem samsetningarvörurnar eru settar saman.

Í dæmum þar sem hluti magnsins er settur saman og aðra þarf að tína þarf að lágmarki tvær tínslulínur.

* Ein tínslulína fyrir magnið saman til pöntunar. [!INCLUDE [prod_short](includes/prod_short.md)] notar eftirfarandi reiti, í þessari röð, til að ákvarða hólfakótann: **Hólfakóti,Kóti** **afhendingarpöntunar** og síðan **Frá-samsetningarhólfskóti**. Ef þessir reitir eru auðir verður starfsmaður vöruhússins **að opna síðuna Innihald hólfs** og velja hólfið þar sem vörurnar eru settar saman.  
* Hin tínslulínan ræðst af því hvaða hólf geta uppfyllt eftirstandandi magn. Ef varan er geymd í mörgum hólfum verða margar línur stofnaðar. Taka-línan byggist á magninu í reitnum **Magn til afhendingar** .

> [!NOTE]  
> Ef vörur eru settar saman í pöntun er birgðatínslan fyrir tengdu sölupöntunina þar til stofnuð er birgðahreyfing fyrir alla samsetningaríhlutina.  

## <a name="see-also"></a>Sjá einnig .

[Yfirlit yfir vöruhúsakerfi](design-details-warehouse-management.md)
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Samsetningardeild](assembly-assemble-items.md)  
[Kynning: Tínsla og Afhending í Einfaldar grunngerð vöruhúss](walkthrough-picking-and-shipping-in-basic-warehousing.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
