---
title: Búa til framleiðsluuppskriftir
description: 'Kynntu þér hvernig þú býrð til framleiðsluuppskriftir, nýjar útgáfur af framleiðsluuppskrift og hvernig á að nota formúlu fyrir útreikning á magni.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'production bom, bills of material,'
ms.search.form: '911, 912, 917, 9287, 99000786, 99000787, 99000788, 99000789, 99000795, 99000797, 99000800, 99000809, 99000811, 99000812, 99000818'
ms.date: 06/22/2021
ms.author: bholtorf
---
# Búa til framleiðsluuppskriftir

Framleiðsluuppskrift geymir aðalgögn sem lýsa íhlutum og millivörum sem notuð er í framleiðslu yfirvörunnar. Þegar framleiðslupöntun er búin til fyrir yfirvörunni stjórnar framleiðsluuppskriftin útreikningum á efniþörf, eins og sýnt er á síðunni **Íhlutir framl.pöntunar**.

[!INCLUDE[prod_short](includes/prod_short.md)] styður einnig samsetningaruppskriftir. Samsetningarpantanir eru notaðar til að gera lokaafurð úr íhlutum með einföldu ferli sem hægt er að vinna með einu eða fleiri tilföngum, sem ekki eru vélar eða vinnustöðvar, eða án nokkurra tilfanga. Til dæmis gæti samsetningarferli falið í sér að velja tvær vínflöskur og einn kaffipoka og pakka þeim sem gjafavöru. Frekari upplýsingar er að finna í [Samsetningaruppskriftir eða framleiðsluuppskriftir](inventory-how-work-boms.md#assembly-boms-or-production-boms).  

> [!TIP]
> Forritið **Sýnigögn Contoso Coffee** innihalda sýnivörur fyrir ýmsar aðstæður framleiðsluuppskriftar sem hægt er að nota í prófunarumhverfi, þ.m.t. í prufuútgáfu. Kynntu þér hvernig á að setja upp göng Contoso Coffee og finna kynningar fyrir mismunandi aðstæður í [Kynning á sýnigögnum Contoso Coffee](contoso-coffee/contoso-coffee-intro.md).

Áður en þú getur sett upp leið verður eftirfarandi að vera á réttum stað:  

- Birgðaspjöld er búin til fyrir yfirvörur sem taka þátt í framleiðslu. Nánari upplýsingar eru í [Skrá nýjar vörur](inventory-how-register-new-items.md).
- Framleiðsluforði eru uppsettur. Frekari upplýsingar eru í [Setja upp vinnustöðvar og vélastöðvar](production-how-to-set-up-work-and-machine-centers.md).

## Búa til framleiðsluuppskrift

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Framleiðsluuppskriftir**, velja síðan viðkomandi tengil.  
2. Valið er aðgerðin **Nýtt**.  
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Til að hægt sé að breyta uppskriftinni verður reiturinn **Staða** að vera stilltur á **Ný** eða **Í þróun**. Til að ræsa hana þarf að stilla **Staða** á **Vottað**.  

    Haldið áfram til að fylla út í framleiðsluuppskriftarlínurnar
5. Í reitnum **Tegund** er valið hvort vara á þessari uppskriftarlínu er venjuleg vara eða framleiðsluuppskrift. Ef varan á línunni er framleiðsluuppskrift þá verður hún þegar að vera til staðar sem vottuð framleiðsluuppskrift.  
6. Í reitnum **númer** er umræddri vöru eða framleiðsluuppskrift flett upp og hún valin eða hún slegin handvirkt í reitinn.  
7. Í reitnum **Magn á** er fært inn hversu margar einingar vörunnar fara í yfirvöruna, t.d. 4 dekk á 1 bifreið.  
8. Í reitnum **Úrkast %** er hægt að slá inn fast hlutfall íhluta sem er fleygt meðan á framleiðslu stendur. Þegar íhlutirnir eru tilbúnir til notkunar í útgefinni framleiðslupöntun er hlutfallinu bætt við áætlað magn (í reitnum  **Notkunarmagn**) í framleiðslubók. Frekari upplýsingar eru í [Skrá Notkun og frálag](production-how-to-register-consumption-and-output.md).  

    > [!NOTE]  
    >  Þetta úrkastshlutfall stendur fyrir íhluti sem er fleygt á meðan á framleiðslu stendur (þegar tekið er úr birgðum) á meðan úrkastshlutfall á leiðarlínum stendur fyrir frálagi sem er fleygt (áður en það verður birgðir).  

9. Í reitnum **Leiðartengilskóti** er hægt að slá inn kóta til að tengja íhlut við ákveðna aðgerð. Frekari upplýsingar er að finna í [Að stofna leiðartengla](production-how-to-create-routings.md#to-create-routing-links).
10. Framleiðsluuppskriftarlínur eru afritaðar með því að smella á **Afrita uppskr.** aðgerðina til að velja línur sem eru til.  
11. Framleiðsluuppskriftin vottuð  
12. Nú er hægt að hengja nýju framleiðsluuppskriftina við spjald viðkomandi yfirvöru. Nánari upplýsingar eru í [Skrá nýjar vörur](inventory-how-register-new-items.md).  

> [!NOTE]  
> [!INCLUDE [bom-standard-cost](includes/bom-standard-cost.md)] Til að endurreikna staðlað kostnaðarverð vörunnar úr birgðaspjaldinu skal velja **Framleiðsla** og síðan smellt á **Reikna staðlað kostn.verð** aðgerðina.  

## Gerð nýrra útgáfa af framleiðsluuppskriftum

Nýjar útgáfur af framl.uppskriftum eru t.d. notaðar þegar vöru er skipt út með annarri vöru, eða þegar viðskiptamaður krefst sérstakrar útgáfu af vörunni. Útgáfureglan gerir kleift að stjórna ólíkum útgáfum af framleiðsluuppskrift. Uppbygging framleiðsluuppskriftarútgáfunnar samsvarar uppbyggingu framleiðsluuppskriftanna. Grundvallarmunurinn er gildistími á útgáfunum. Gildistíminn er skilgreindur af upphafsdagsetningu.  

Upphafsdagsetningin sýnir upphaf tímabilsins sem útgáfan er í gildi. Upphafsdagsetningin er alltaf afmörkunarviðmiðun fyrir útreikninga og mat. Uppskriftarútgáfan er gild þar til næsta útgáfa tekur gildi samkvæmt upphafsdagsetningu hennar.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Framleiðsluuppskriftir**, velja síðan viðkomandi tengil.  
2. Veldu framleiðsluuppskriftina sem á að afrita, veldu síðan aðgerðina **Útgáfur**.  
3. Valið er aðgerðin **Nýtt**.  
4. Fyllið inn reitina eftir þörfum.
5. Einstakt auðkenni útgáfunnar er fært inn í reitinn **Útgáfukóti**. Hvaða samsetning af tölum og bókstöfum er leyfileg.  

    Nýja útgáfan sem búin var til fær sjálfkrafa stöðuna **Ný.**
6. Þegar uppskriftarútgáfunni er lokið, setja **Staða** reitinn á **Vottað**.  

Gildistími útgáfunnar er tilgreindur í reitnum **Upphafsdagsetning**.  

> [!NOTE]  
> Veljið valkostinn **Vara** í reitnum **Tegund** til að nota vöru úr aðalvörugögnum í framleiðsluuppskriftinni. Ef vörunni fylgir einnig framleiðsluuppskrift þar sem reiturinn **Nr. framleiðsluuppskriftar** er fylltur út á birgðaspjaldinu er einnig tekið tillit til hennar.  
>
> Velja skal valkostinn **Framl.uppskr.** ef nota á annan skuggaframleiðsluuppskrift í línunni.  
>
> Skuggauppskriftir eru notaðar til að skipuleggja vörur./ Þessi fram.uppskriftartegund leiðir aldrei af sér fullunna vöru, en er notuð sérstaklega til að ákvarða háða eftirspurn. Skuggauppskriftir hafa ekki eigin aðalgögn.

## Magnreikniformúla á framleiðsluuppskriftir

Magnið er reiknað samkvæmt mismunandi víddum sem einnig eru færðar í framleiðsluuppskriftarlínurnar línurnar. Víddirnar vísa til pöntunareiningar á viðkomandi vöru. Hægt er að færa inn lengd, breidd, dýpt og þyngd sem víddir.  

Dálkarnir Tegund útreiknings, Lengd, Breidd, Dýpt og Þyngd  birtast ekki þar sem aðeins fáeinir notendur nota þá. Ef notandi vill nota magnreikninga þarf fyrst að birta þessa dálka.  

Tengsl ólíkra íhluta eru skilgreind af reiknireglunni. Hægt er að nota eftirfarandi valkosti sem reiknireglu:  

- **Tómt** - Víddir ekki teknar með. (Magn = Magn á.)  
- **Lengd** - Magn = Magn á * Lengd  
- **Lengd x Breidd** - Magn = Magn á * Lengd x Breidd  
- **Lengd x Breidd x Dýpt** - Magn = Magn á Lengd x Breidd x Dýpt  
- **Þyngd** -Magn = Magn á x Þyngd  
- **Fast magn** - Magn = Magn á

> [!NOTE]
> Reikniformúlan **Fast magn** tryggir að notkun íhluts sé sú sama óháð því hvert magn rýrnunar eða úttaks er. Fyrir íhluti framleiðslupöntunar, þegar reiturinn **Reikniformúla** er stilltur á **Fast magn**, er gildið í reitnum **Væntanlegt magn** alltaf jafnt og magnið í reitnum **Magn á**. Rýrnunarprósentan sem er skilgreind í sömu línunni er hunsuð. Fast magn er virt af skýrslunni **Framboð eftir uppskrift**. Skýrslan sýnir vöruna sem flöskuháls ef tiltækt magn er minna en magnið í reitnum **Magn á yfireiningu**. Reitirnir **Get gert yfireiningu** og **Get gert aðalvöru** eru alltaf auðir óháð því hvert tiltækt magn er. Fast magn er einnig innifalið í útreikningum fyrir staðalkostnað. Lotustærðin fyrir framleidda vöru hefur áhrif á kostnaðinn sem eru úthlutað fyrir eina vöru.

### Dæmi

Framleiðsluuppskrift þarf 70 málmhluta með lengd = 0,20 m og breidd = 0,15 m. Gildin eru færð inn á eftirfarandi hátt: Reikniregla = Lengd x Breidd, Lengd = 20, Breidd = 15, Magn á = 70. Magnið fæst með Magn á x Lengd * Breidd, þ.e., Magn = 70 x 0.20 m x 0.15 m = 2.1 m2.  

## Sjá einnig .

[Stofna leiðir](production-how-to-create-routings.md)  
[Stjórna afurðarafbrigðum](inventory-item-variants.md)  
[Walkthrough: afbrigði](contoso-coffee/manufacturing/variants.md)  
[Uppsetning framleiðslu](production-configure-production-processes.md)  
[Framleiðsla](production-manage-manufacturing.md)  
[Áætlun](production-planning.md)  
[Vinna með uppskriftir](inventory-how-work-BOMs.md)  
[Vinna með samsetningaruppskriftir](assembly-how-work-assembly-boms.md)  
[Birgðir](inventory-manage-inventory.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
