---
title: Hvernig á að tína vörur með birgðatínslu
description: Lærðu að nota birgðatínslu til að skrá og bóka tiltekt og sendingarupplýsingar fyrir upprunaskjöl.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.forms: '931, 7377'
---
# Vörur tíndar með birgðatínslu

Í  [!INCLUDE[prod_short](includes/prod_short.md)] eru tínsla og sendingarvara notuð með einni af fjórum aðferðum eins og lýst er í eftirfarandi töflu.

|Aðferð|Útleiðarferli|Krefjast tínslu|Krefjast afhendingar|Flókið stig (frekari upplýsingar um  [Vöruhúsakerfi-Yfirlit](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Bóka tínslu og sendingu úr pöntunarlínu|||Engin sérstök vöruhúsaaðgerð.|  
|B|Bóka tínslu og afhendingu úr birgðatínsluskjali|Kveikt||Grunnur: pöntun-eftir pöntun.|  
|N|Bóka tínslu og sendingu úr vöruhúsaafhendingarskjali||Kveikt|Grunnur: Samstæða móttöku/skipa bóka fyrir margar pantanir.|  
|D|Bókið tínsluna úr vöruhúsatínsluskjali og bókið sendinguna úr afhendingarskjali vöruhúss|Kveikt|Kveikt|Ítarlegt|  

Frekari upplýsingar um flæði vöruhúss á  [útleið](design-details-outbound-warehouse-flow.md).

Í þessari grein er átt við aðferð B í töflunni.

Þegar birgðageymslan er sett upp þannig að krafist sé tínsluvinnslu en ekki afhendingarvinnslu skal nota  **síðuna Birgðatínsla**  til að skrá og bóka tiltektar-og sendingarupplýsingar fyrir upprunaskjölin. Upprunaskjöl á útleið geta verið sölupantanir, innkaupaskilapantanir og flutningspantanir á útleið.

> [!NOTE]
> Þarfir framleiðslu-og samsetningarþarfa eru einnig til fyrir upprunaskjöl á útleið. Frekari upplýsingar um meðhöndlun framleiðslu og samsetningar pantana fyrir innri vinnslur í  [Design nánar: innanhúss-vöruhús flæða](design-details-internal-warehouse-flows.md).
>
> Þrátt fyrir að þjónustupantanir séu einnig upprunaskjöl á útleið styðja þær ekki grunnstig, röð eftir stigum er flókin.
>
> Þegar magn tiltektar og sölulínu sem eru sett saman við pöntunina, eru reglur þarf að fylgja þegar stofnaðar eru birgðatínslulínur. Frekari upplýsingar á  [afgreiðslunum setja saman við vörur með birgðatínslu](#handling-assemble-to-order-items-with-inventory-picks).  

Hægt er að stofna birgðatínslu í á þrjá vegu:

* Stofna birgðatínsluna beint úr upprunaskjalinu.  
* Stofna Birgðatínslur fyrir mörg upprunaskjöl á sama tíma með því að nota runuvinnslu.
* Beiðnina um tínsluna í tveimur skrefum með því að gefa fyrst út upprunaskjalið sem virkar sem merki í vöruhúsið sem upprunaskjalið er reiðubúið að tína til.

Síðan er hægt að stofna birgðatínsluna úr  **síðunni Birgðatínsla**  sem byggist á upprunaskjalinu.  

## Birgðatínsla stofnuð í upprunaskjali:

1. Í upprunaskjalinu, sem getur verið sölupöntun, Innkaupavöruskilapöntun eða flutningspöntun á útleið, skal velja  **aðgerðina stofna birgðafrágang/tínslu** .
2.  **Veljið stofna Ívt. Velja**  gátreitinn.  
3. Velja hnappinn **Í lagi**. Ný birgðatínsla verður stofnuð.

## Fleiri en ein birgðatínsla stofnuð með keyrslu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn  **stofna birgðafrágang/tínslu/hreyfingar** og velja síðan tengda tengilinn.  
2. Á flýtiflipanum **Vöruhúsabeiðni** eru reitirnir **Upprunaskjal** og **Upprunanúmer** notaðir til að afmarka eftir tilteknum gerðum fylgiskjala eða sviðum fylgiskjalanúmera. Til dæmis er hægt að stofna tínslu einungis fyrir sölupantanir.  
3.  **Á flipanum Valkostir**  er gátreiturinn Stofna ívt valinn  **. Velja**  gátreitinn.
4. Velja hnappinn **Í lagi**.

## Tínslan stofnuð í tveimur skrefum

### Til að biðja um birgðatínslu með því að gefa út upprunaskjalið

Fyrir sölupantanir, innkaupaskilapantanir og millifærslupantanir á útleið er vöruhússbeiðnin stofnuð með því að gefa út pöntunina. Ef pöntunin er tiltæk er hægt að velja vörur sem eru tiltækar.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.
2. Valinn er sölupöntun sem á að gefa út og velja síðan aðgerðina **Gefa út**.

### Birgðatínsla stofnaður á grundvelli upprunaskjals

Eftir að pöntun hefur verið gerð getur starfsmaður vöruhúss stofnað birgðatínslu.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, farðu í **Birgðatínsla** og veldu síðan viðkomandi tengil.  
2. Valið er aðgerðin **Nýtt**.  
3.  **Í reitnum upprunaskjal**  er valin gerð skjalsins sem verið er að tína til.  
4. Í reitnum **Forðanr.** er forðaskjal valið.  
5. Einnig er hægt að velja  **aðgerðina Sækja upprunaskjal**  til að stofna lista yfir öll upprunaskjöl á útleið sem eru tilbúin til tínslu á staðnum.  
6. Veldu í  **lagi**  hnappinn til að fylla tínslulínurnar samkvæmt völdum upprunaskjölum.  

## Birgðatínsla skráð

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, farðu í **Birgðatínsla** og veldu síðan viðkomandi tengil.  
2. í reitnum **Hólfakóði** í tínslulínunum, hólfið sem vörurnar þurfa að vera tíndar úr er tillaga á sjálfgefið hólf vörunnar. Hægt er að skipta um hólf á þessari síðu ef með þarf.  
3. Tínslan er framkvæmd og magnið fært inn í  **reitinn Magn til afgreiðslu** .

    Ef taka verður vörurnar fyrir í línu úr fleiri en einu hólfi, til dæmis vegna þess að heildarmagn er ekki í hólfinu, skal nota  **aðgerðina skipta línu**  á  **fastflipanum línur** . Aðgerðin býr til línu fyrir eftirstandandi magn sem á að afgreiða.

4. Valið er **Bóka** aðgerðin.  

    * Bóka sendinguna í upprunaskjalslínurnar sem voru tilteknar.
    * Ef birgðageymslan notar hólf mun bókun einnig stofna vöruhúsafærslur til að bóka breytingar á hólfmagninu.  

## Meðhöndlun á saman vörum í birgðum með birgðatínslu

Einnig er hægt að nota  **síðuna Birgðatínsla**  til að velja og senda til sölu þar sem senda þarf vörur inn áður en hægt er að afhenda þær. Læra meira at  [selja vörur saman til að panta](assembly-how-to-sell-items-assembled-to-order.md).

Samsettar vörur eru ekki efnislega í hólfi fyrr en þær eru settar saman og bókaðar sem framleiðsla í hólf. Með því að taka saman vörur í hólfi fyrir sendingar fylgir sérstakt flæði.

1. Starfsmenn í vöruhúsi færa samsetningaríhluti úr hólfi á afhendingarsvæði og bóka síðan birgðatínsluna.
2. Bókaða birgðatínslan bókar samsetningarúttakið, íhlutanotkun og söluafhendinguna.

Hægt er að setja upp [!INCLUDE[prod_short](includes/prod_short.md)] í búa til birgðahreyfingu sjálfkrafa þegar birgðatínsla fyrir samsetningarvöru er stofnuð.  **Veljið svæðið Stofna hreyfingar sjálfkrafa**  á  **síðunni samsetningaruppsetning** . Frekari upplýsingar um  [uppsetningu grunnvöruhúsa með Aðgerðarsvæðum](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md).

Línur birgðatínslu fyrir söluvörur eru stofnaðar á mismunandi hátt, eftir því hvort enginn, eða öll magn sölulínanna, eru sett saman til pöntunar. Í áætlunum þar sem eitthvað magn er sett saman og sumt er tekið úr birgðum eru stofnaðar að lágmarki tvær tínslulínur.

Fyrir sölu þar sem heildarmagn í sölupöntunarlínu er sett saman við pöntun er ein birgðatínslulína stofnuð fyrir magnið. Gildið í  **reitnum Magn til að setja saman**  við er það sama og gildið í  **svæðinu Magn til sendingar** . **Setja saman í pöntun** reiturinn er valið í línunni.

Ef frálagsflæði samsetningar er sett upp fyrir birgðageymsluna  **inniheldur reiturinn Kóti**  hólfs í birgðatínslulínunni gildið í eftirfarandi röð.

* ***Asm.-í-röð Skpt. bin Kóði** <!-- not applicable for inv pick-->
* **Kóti-Hólfakóða samsetningar**

Ef Hólfakóti er ekki tilgreint í sölupöntunarlínu og frálagsflæði samsetningar er ekki sett upp fyrir birgðageymsluna  **er reiturinn Kóti hólfs**  í birgðatínslulínunni auður. Starfsmaður í vöruhúsi verður að opna síðuna **Hólfainnihald** og velja hólfið þar sem samsetningarvörurnar eru settar saman.

Í áætlunum þar sem hluti af magninu er settur saman og annað verður að taka til, eru stofnaðar að lágmarki tvær tínslulínur.

* Eina tínslulínu fyrir magnið sem er í samsetningum. [!INCLUDE [prod_short](includes/prod_short.md)] notar eftirfarandi svæði í þessari röð til að ákvarða hólfakótann:  **hólfakóta**,  **asm.-pöntunar-kóti til-. bin-kóta** og svo  **hólfkóta** úr-samsetningu. Ef þessir reitir eru auðir þarf starfsmaður vöruhúss að opna  **innihald**  hólfs og velja hólfið þar sem vörurnar eru settar saman.  
* Önnur tínslulínan fer eftir því hvaða hólf geta uppfyllt eftirstandandi magn. Ef vörunni er haldið í mörgum hólfum verða margar línur stofnaðar. Línan taka miðast við magnið í  **reitnum Magn til sendingar** .

> [!NOTE]  
> Ef vörur eru settar saman til pöntunar velur birgðatínslan tengda sölupöntunina til að stofna birgðastöðu fyrir alla samsetningaríhluti.  

## Sjá tengda [Microsoft þjálfun](/training/paths/pick-ship-items-business-central/)

## Sjá einnig .

[Yfirlit](design-details-warehouse-management.md)
[vöruhúsakerstjórnunar birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Samsetningardeild](assembly-assemble-items.md)  
[Kynning: Tínsla og Afhending í Einfaldar grunngerð vöruhúss](walkthrough-picking-and-shipping-in-basic-warehousing.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
