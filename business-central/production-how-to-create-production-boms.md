---
title: Búa til framleiðsluuppskriftir
description: Kynntu þér hvernig þú býrð til framleiðsluuppskriftir, nýjar útgáfur af framleiðsluuppskrift og hvernig á að nota formúlu fyrir útreikning á magni.
author: bholtorf
ms.topic: conceptual
ms.search.keywords: production bom, bills of material,
ms.search.form: 911, 912, 917, 9287, 99000786, 99000787, 99000788, 99000789, 99000795, 99000797, 99000800, 99000809, 99000811, 99000812, 99000818
ms.date: 06/22/2021
ms.author: edupont
ms.openlocfilehash: ec8d20ac3f6e6e02471a9f86f35aee8c551df801
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9607824"
---
# <a name="create-production-boms"></a>Búa til framleiðsluuppskriftir

Framleiðsluuppskrift geymir aðalgögn sem lýsa íhlutum og millivörum sem notuð er í framleiðslu yfirvörunnar. Þegar framleiðslupöntun er búin til fyrir yfirvörunni stjórnar framleiðsluuppskriftin útreikningum á efniþörf, eins og sýnt er á síðunni **Íhlutir framl.pöntunar**.

[!INCLUDE[prod_short](includes/prod_short.md)] styður einnig samsetningaruppskriftir. Samsetningarpantanir eru notaðar til að gera lokaafurð úr íhlutum með einföldu ferli sem hægt er að vinna með einu eða fleiri tilföngum, sem ekki eru vélar eða vinnustöðvar, eða án nokkurra tilfanga. Til dæmis gæti samsetningarferli falið í sér að velja tvær vínflöskur og einn kaffipoka og pakka þeim sem gjafavöru. Frekari upplýsingar er að finna í [Samsetningaruppskriftir eða framleiðsluuppskriftir](inventory-how-work-boms.md#assembly-boms-or-production-boms).  

> [!TIP]
> **Contoso kaffi sýniforritið Data** App inniheldur sýnivörur fyrir margvíslegar AÐSTÆÐUR framleiðsluuppskrifta sem hægt er að nota á prófunarumhverfi, þar á meðal á meðan á rannsókn stendur. Lærðu að setja upp contoso Coffee gögnin og finna gönguleið fyrir mismunandi aðstæður við [inngang að contoso Coffee sýnigögnum](/contoso-coffee/contoso-coffee-intro.md).

Áður en þú getur sett upp leið verður eftirfarandi að vera á réttum stað:  

- Birgðaspjöld er búin til fyrir yfirvörur sem taka þátt í framleiðslu. Nánari upplýsingar eru í [Skrá nýjar vörur](inventory-how-register-new-items.md).
- Framleiðsluforði eru uppsettur. Frekari upplýsingar eru í [Setja upp vinnustöðvar og vélastöðvar](production-how-to-set-up-work-and-machine-centers.md).

## <a name="to-create-a-production-bom"></a>Búa til framleiðsluuppskrift

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **framl. uppskriftir** og veljið síðan tengda tengilinn.  
2. Valið er aðgerðin **Nýtt**.  
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Til að hægt sé að breyta uppskriftinni verður reiturinn **Staða** að vera stilltur á **Ný** eða **Í þróun**. Til að ræsa hana þarf að stilla **Staða** á **Vottað**.  

    Haldið áfram til að fylla út í framleiðsluuppskriftarlínurnar
5. Í reitnum **Tegund** er valið hvort vara á þessari uppskriftarlínu er venjuleg vara eða framleiðsluuppskrift. Ef varan á línunni er framleiðsluuppskrift þá verður hún þegar að vera til staðar sem vottuð framleiðsluuppskrift.  
6. Í reitnum **númer** er umræddri vöru eða framleiðsluuppskrift flett upp og hún valin eða hún slegin handvirkt í reitinn.  
7. **Í reitinn Magn á hvert** svæði skal slá inn hversu margar einingar af vörunni fara í yfirvöruna, t.d. 4 hjól fyrir 1 bíl.  
8. **Í reitnum Úrkast%** er hægt að færa inn fast hlutfall íhluta sem hafa rýrnað við framleiðslu. Þegar íhlutirnir eru tilbúnir til notkunar í útgefinni framleiðslupöntun er hlutfallinu bætt við áætlað magn (í reitnum  **Notkunarmagn**) í framleiðslubók. Frekari upplýsingar eru í [Skrá Notkun og frálag](production-how-to-register-consumption-and-output.md).  

    > [!NOTE]  
    >  Þetta úrkastshlutfall stendur fyrir íhluti sem er fleygt á meðan á framleiðslu stendur (þegar tekið er úr birgðum) á meðan úrkastshlutfall á leiðarlínum stendur fyrir frálagi sem er fleygt (áður en það verður birgðir).  

9. Í reitnum **Leiðartengilskóti** er hægt að slá inn kóta til að tengja íhlut við ákveðna aðgerð. Frekari upplýsingar er að finna í [Að stofna leiðartengla](production-how-to-create-routings.md#to-create-routing-links).
10. Framleiðsluuppskriftarlínur eru afritaðar með því að smella á **Afrita uppskr.** aðgerðina til að velja línur sem eru til.  
11. Framleiðsluuppskriftin vottuð  
12. Nú er hægt að hengja nýju framleiðsluuppskriftina við spjald viðkomandi yfirvöru. Nánari upplýsingar eru í [Skrá nýjar vörur](inventory-how-register-new-items.md).  

> [!NOTE]  
> [!INCLUDE [bom-standard-cost](includes/bom-standard-cost.md)] Til að endurreikna staðalkostnað vörunnar á birgðaspjaldinu skal velja **aðgerðina framleiðsla** og velja **síðan aðgerðina Calc. staðlað kostnaðarverð**.  

## <a name="to-create-a-new-version-of-a-production-bom"></a>Ný útgáfa af FRAMLEIÐSLUUPPSKRIFT búin til

Nýjar útgáfur af framl.uppskriftum eru t.d. notaðar þegar vöru er skipt út með annarri vöru, eða þegar viðskiptamaður krefst sérstakrar útgáfu af vörunni. Útgáfureglan gerir kleift að stjórna ólíkum útgáfum af framleiðsluuppskrift. Uppbygging framleiðsluuppskriftarútgáfunnar samsvarar uppbyggingu framleiðsluuppskriftanna. Grundvallarmunurinn er gildistími á útgáfunum. Gildistíminn er skilgreindur af upphafsdagsetningu.  

Upphafsdagsetningin sýnir upphaf tímabilsins sem útgáfan er í gildi. Upphafsdagsetningin er alltaf afmörkunarviðmiðun fyrir útreikninga og mat. Uppskriftarútgáfan er gild þar til næsta útgáfa tekur gildi samkvæmt upphafsdagsetningu hennar.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **framl. uppskriftir** og veljið síðan tengda tengilinn.  
2. Velja FRAMLEIÐSLUUPPSKRIFTINA sem á að afrita og velja **síðan útgáfuaðgerðina**.  
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
> Skuggauppskriftir eru notaðar til að skipuleggja vörur./ Þessi gerð FRAMLEIÐSLUUPPSKRIFTAR leiðir aldrei til fullunninnar afurðar en er eingöngu notuð til að ákvarða háða eftirspurn. Skuggauppskriftir hafa ekki eigin aðalgögn.

## <a name="quantity-calculation-formula-on-production-boms"></a>Formúla magnútreiknings í framleiðsluuppskriftum

Magnið er reiknað með að taka tillit til mismunandi vídda sem einnig eru færðar inn í framl. uppskriftarlínurnar. Víddirnar vísa til pöntunareiningar á viðkomandi vöru. Hægt er að færa inn lengd, breidd, dýpt og þyngd inn sem víddir.  

Dálkarnir útreikningsformúla, lengd, breidd, dýpt og þyngd birtast ekki þar sem þeir eru aðeins notaðir af sumum notendum. Ef notandi vill nota magnreikninga þarf fyrst að birta þessa dálka.  

Tengsl ólíkra íhluta eru skilgreind af reiknireglunni. Hægt er að nota eftirfarandi valkosti sem reiknireglu:  

- **Tómt** - Víddir ekki teknar með. (Magn = Magn á.)  
- **Lengd** - Magn = Magn á * Lengd  
- **Lengd x Breidd** - Magn = Magn á * Lengd x Breidd  
- **Lengd x Breidd x Dýpt** - Magn = Magn á Lengd x Breidd x Dýpt  
- **Þyngd** -Magn = Magn á x Þyngd  
- **Fast magn** -Magn = Magn á

> [!NOTE]
> Formúla fyrir útreikning á **magni** tryggir að notkunarhluti íhlutarins sé sá sami án tillits til úrkomu eða frálagsmagns. Fyrir íhluti framleiðslupöntunar þegar **reiturinn útreikningsformúla** er stilltur á **Fast magn** **er gildið Væntanlegt magnsvæði** alltaf jafnt **magninu á hverju** svæði. Úrkastsprósentan sem er skilgreind í sömu línu er hunsuð. Fast magn er virt með **tiltækinu eftir uppskriftarskýrslu**. Skýrslan sýnir vöruna sem flöskuhálsinn ef tiltækt magn er minna en magnið í **yfirsvæðinu** Magn á eftir. Það **að geta Yfirgert** **efsta vörusvæði** er alltaf autt, óháð því magni sem er í boði. Fast magn er einnig innifalið í útreikningi fyrir staðlaðan kostnað. Lotustærðin fyrir framleiddu vöruna hefur áhrif á kostnaðinn sem er úthlutað fyrir eina vöru.

### <a name="example"></a>Dæmi

Í FRAMLEIÐSLUUPPSKRIFT eru 70 málmhlutir með lengd = 0,20 m og breidd = 0,15 m. Gildin eru færð inn á eftirfarandi hátt: Reikniregla = Lengd x Breidd, Lengd = 20, Breidd = 15, Magn á = 70. Magnið fæst með Magn á x Lengd * Breidd, þ.e., Magn = 70 x 0.20 m x 0.15 m = 2.1 m2.  

## <a name="see-also"></a>Sjá einnig .

[Stofna leiðir](production-how-to-create-routings.md)  
[Stjórna afurðarafbrigðum](inventory-item-variants.md)  
[Walkthrough: afbrigði](/contoso-coffee/variants.md)  
[Uppsetning framleiðslu](production-configure-production-processes.md)  
[Framleiðsla](production-manage-manufacturing.md)  
[Áætlun](production-planning.md)  
[Vinna með uppskriftir](inventory-how-work-BOMs.md)  
[Vinna með Samsetningaruppskriftir](assembly-how-work-assembly-boms.md)  
[Birgðir](inventory-manage-inventory.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
