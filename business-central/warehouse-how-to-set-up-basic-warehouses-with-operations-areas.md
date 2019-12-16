---
title: 'Hvernig á að: Setja upp einfaldar vöruhúsaaðgerðir með aðgerðasvæðum | Microsoft Docs'
description: Ef innri starfsemi, svo sem framleiðsla eða samsetning, er notuð í einfaldri vöruhúsagrunnstillingu þar sem birgðageymslur nota uppsetningarreitinn **Hólf áskilið** og mögulega uppsetningarreitina **Krefjast tínslu** og **Þarf að ganga frá** er hægt að nota þrjú grunvöruhúsaskjöl til að skrá vöruhúsaaðgerðir fyrir innri starfsemi.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 4ba00aab6c929975b806e6a69c89b36da937f4ca
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/03/2019
ms.locfileid: "2881617"
---
# <a name="set-up-basic-warehouses-with-operations-areas"></a>Setja upp einfaldar vöruhúsaaðgerðir með aðgerðasvæði
Ef innri starfsemi, svo sem framleiðsla eða samsetning, er notuð í einfaldri vöruhúsagrunnstillingu þar sem birgðageymslur nota uppsetningarreitinn **Hólf áskilið** og mögulega uppsetningarreitina **Krefjast tínslu** og **Þarf að ganga frá** er hægt að nota eftirfarandi vöruhúsaskjöl til að skrá vöruhúsaaðgerðir fyrir innri starfsemi:  

- **Birgðahreyfing** síðan.  
- **Birgðatínsla** síðan.  
- **Birgðafrágangur** síðan.

> [!NOTE]
> Jafnvel þótt stillingarnar séu kallaðar **Krefjast tínslu** og **Krefjast frágangs**, geturðu samt sem áður bókað móttöku og afhendingu beint frá uppruna viðskiptaskjala í birgðageymslum þar sem þú velur þessa gátreiti.  

Til að nota þessar síður með innri aðgerðum, til dæmis til að tína og færa íhluti í framleiðslu, þarf að framkvæma sum eða öll af eftirfarandi uppsetningarþrepum eftir því hversu mikla stjórn þarf að hafa:  

- Virkja birgðatínslu-, færslu- og frágangsskjöl.  
- Skilgreina skipulag sjálfgefins hólfs fyrir íhluti og endanlegar vörur sem flæða til og frá aðgerðaforða.  
- Gera skal á- og frá-hólf sem eru sérnýtt fyrir forða sérstakra aðgerða til að koma í veg fyrir að þær séu tíndar fyrir skjöl á útleið.

Hólfakótar sem eru settir upp á birgðageymsluspjöldum skilgreina sjálfgefið vöruhúsaflæði fyrir tiltekna verkþætti, svo sem íhluti í samsetningardeild. Viðbótaraðgerðir eru til sem tryggja að þegar vörur eru settar í tiltekið hólf er ekki hægt að færa þær eða tína fyrir aðrar aðgerðir. Nánari upplýsingar má nálgast í [Að stofna þar til gerð íhlutahólf](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md#to-create-dedicated-component-bins).

Eftirfarandi ferli eru byggð á uppsetningu einfaldra vöruhúsaðgerða í kringum framleiðslusvæði. Skrefin eru svipuð fyrir önnur aðgerðasvið, svo sem samsetningu, þjónustustýringu og verk.  

> [!NOTE]  
>  Í eftirfarandi aðgerð er uppsettningarreiturinn **Hólf áskilið** á birgðageymsluspjaldi valinn sem forskilyrði, þar sem litið er á það sem grundvöll fyrir öll stig vöruhúsastjórnunar.  

## <a name="to-enable-inventory-documents-for-internal-operation-activities"></a>Til að virkja birgðaskjöl fyrir innri aðgerðir  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Staðsetningar** og veldu síðan tengda tengilinn.
2. Opna birgðageymsluspjaldið sem á að setja upp.  
3.  Á flýtiflipanum **Vöruhús** skal velja gátreitinn **Þarf að ganga frá** til að gefa til kynna að þegar inn- eða innra upprunaskjal með hólfakóða er gefið út, er hægt að stofna birgðafrágang eða birgðahreyfingu.  
4.  Veljið gátreitinn **Krefjast tínslu** til að gefa til kynna að þegar útleiðarskjal eða innra upprunaskjal með hólfakóta er stofnað skuli einnig stofna birgðatínslu- eða birgðahreyfingarskjal.  

## <a name="to-define-a-default-bin-structure-in-the-production-area"></a>Til að skilgreina sjálfgefna hólfaskipan í framleiðslusvæðinu  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Staðsetningar** og veldu síðan tengda tengilinn.
2. Opna birgðageymsluna sem setja á upp.  
3.  Á flýtiflipanum **Hólf** í reitnum **Hólfkóti opins vinnslusalar** er færður inn kóti hólfsins á framleiðslusvæðinu með fjölda íhluta sem starfsmaður á vél getur notað án þess að biðja þurfi um vöruhúsaaðgerð til að færa þá í hólfið. Vörur sem eru settar í þetta hólf eru venjulega settar upp fyrir sjálfvirka bókun eða söfnun. Þetta þýðir að reiturinn **Birgðaskráningaraðferð** inniheldir **Áfram** eða **Afturábak**.  
4. Í **Hólfkóti framleiðslu á innleið** færið inn kóta hólfsins á framleiðslusvæðinu sem íhlutir sem tíndir eru fyrir framleiðslu í þessari birgðageymslu eru sjálfgefið settir á áður en þeir eru notaðir. Vörur sem eru settar í þetta hólf eru venjulega settar upp fyrir handvirka notkunarbókun. Þetta þýðir að reiturinn **Birgðaskráningaraðferð** inniheldur **Handvirkt** eða **Tína + Áfram** eða **Tína + afturábak** fyrir vöruhúsatínslur og birgðahreyfingar.  

    > [!NOTE]  
    >  Þegar birgðatínsla er notuð skilgreinir reiturinn **Hólfkóti** á íhlutalínu framleiðslupöntunar hólfið *taka* hvaðan íhlutir eru minnkaðir þegar notkun er bókuð. Þegar birgðahreyfingar eru notaðar, skilgreinir reiturinn **Hólfkóti** í framleiðslupöntunaríhlutalínum hólfið *setja* í aðgerðasvæðinu þar sem starfsmaður í vöruhúsi verður setja íhlutina.  

5. Á flýtiflipanum **Hólf** í reitnum **Hólfkóti frá framleiðslu** er færður inn kóti hólfsins á framleiðslusvæðinu þar sem endanlegar vörur eru teknar úr sjálfkrafa þegar í ferlinu felst vöruhúsaðgerð. Í einfaldri vöruhúsastillingu er virkni skráð sem birgðafrágangur eða birgðahreyfing.  

Núna krefjast íhlutalínur framleiðslupöntunar með sjálfgefinn hólfakóta þess að framvirkir íhlutir séu settir þar. Þar til íhlutir úr því hólfi hafa verið notaðir getur önnur íhlutaeftirspurn ollið tínslu eða notkun úr hólfinu vegna þess að íhlutirnir teljast enn vera tiltækt innihald hólfsins. Til að tryggja að hólfainnihald sé aðeins tiltækt fyrir íhlutseftirspurnina sem notar þann hólfkóða framleiðslu á innleið, þarf að velja reitinn **Sérstakt** í línunni fyrir þann hólfakóða á síðunni **Hólf** sem opnaður er í birgðageymsluspjaldinu.

Þetta flæðirit sýnir hvernig reiturinn **Hólfkóði** í framleiðslupöntunaríhlutalínum er útfylltur samkvæmt uppsetningunni.  

![Flæðirit hólfa](media/binflow.png "BinFlow")    

## <a name="to-define-a-default-bin-structure-in-the-assembly-area"></a>Til að skilgreina sjálfgefna hólfaskipan í samsetningarsvæðinu
Íhluti fyrir samsetningarpöntun er ekki hægt að tína eða bóka með birgðatínslum. Nota skal síðuna **Birgðahreyfing** í staðinn. Frekari upplýsingar eru í [Færa íhluti á aðgerðasvæði með einföldum vöruhúsaaðgerðum](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

Ef magn sölulínu tínslu og afhendingar er sett saman í pöntunina skal fylgja nokkrum reglum við stofnun birgðatínslulína. Nánari upplýsingar eru í hlutanum „Meðhöndlun íhluta pantanasamsetninga við birgðatínslu” í [Tína vörur með Birgðatínslu](warehouse-how-to-pick-items-with-inventory-picks.md).

Nánari upplýsingar, sjá [Samsetningarstjórnun](assembly-assemble-items.md).

### <a name="to-set-up-that-an-inventory-movement-is-automatically-created-when-the-inventory-pick-for-the-assembly-item-is-created"></a>Til að setja það upp að birgðahreyfing sé sjálfkrafa búin til þegar birgðatínsla fyrir samsetningarvöru er stofnuð.
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning samsetningar** og veldu síðan tengda tengilinn.
2. Veljið gátreitinn **Stofna hreyfingar sjálfkrafa**.

### <a name="to-set-up-the-bin-in-the-assembly-area-where-components-are-placed-by-default-before-they-can-be-consumed-in-assembly"></a>Til að setja upp hólfið á samsetningarsvæðinu sem íhlutir eru sjálfgefið settir á áður en nota má þá við samsetningu.
Gildið í þessum reit er sjálfkrafa sett inn í reitinn **Hólfkóði** á samsetningarpantanalínum þegar þessi staðsetning er sett í **Staðsetningarkóði** reitinn á samsetningarpöntunarlínunni.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Staðsetningar** og veldu síðan tengda tengilinn.
2. Opna birgðageymsluna sem setja á upp.
3. Færið inn **Í samsetningu hólfakóði** reitinn.

### <a name="to-set-up-the-bin-in-the-assembly-area-where-finished-assembly-items-are-posted-to-when-they-are-assembled-to-stock"></a>Til að setja upp hólfið á samsetningarsvæðinu þar sem fullunnir samsetningaríhlutir eru bókaðir þegar þeir eru settir saman á lager.
Gildið í þessum reit er sjálfkrafa sett inn í reitinn **Hólfkóði** á samsetningarpantanahausum þegar þessi staðsetningarkóði er settur í reitinn **Staðsetningarkóði** á samsetningarpöntunarhausnum.

Hólfakótar sem eru settir upp á birgðageymsluspjöldum skilgreina sjálfgefið vöruhúsaflæði fyrir tiltekna vöruhúsaaðgerðir, svo sem notkun á íhlutum á samsetningarsvæði. Viðbótaraðgerðir eru til sem tryggja að þegar vörur eru settar í sjálfgefið hólf er ekki hægt að færa þær eða tína fyrir aðrar aðgerðir.

> [!NOTE]
> Þessi uppsetning er aðeins möguleg fyrir staðsetningar þar sem reiturinn Hólf nauðsynlegt er valinn.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Staðsetningar** og veldu síðan tengda tengilinn.
2. Opna birgðageymsluna sem setja á upp.
3. Færið inn **Frá-samsetning hólfkóða** reitinn.

### <a name="to-set-up-the-bin-where-finished-assembly-items-are-posted-to-when-they-are-assembled-to-a-linked-sales-order"></a>Til að setja upp hólfið sem fullunnir samsetningaríhlutir eru bókaðir þegar þeir eru settir saman í tengda sölupöntun.
Úr þessu hólfi eru samsetningaríhlutir afhentir strax með birgðatínslu til að uppfylla sölupöntunina.

> [!NOTE]
> Ekki er hægt að nota þennan reit ef birgðageymslan er sett upp þannig að hún noti beina tínslu og frágang.

Hólfakótinn er afritaður úr sölupöntunarlínu í haus samsetningarpöntunar til að hafa samskipti við samsetningarstarfsmenn um það hvar eigi að setja frálagið svo það sé tilbúið til afhendingar. Það er líka afritað í birgðatínslulínuna til að hafa samskipti við starfsmenn vöruhúss um hvaðan á að taka það til að senda það.

> [!NOTE]
> Afhendingarhólf fyrir Setja-saman-í-pöntun er alltaf tómt. Þegar sölulína samsetningar í pöntun er bókuð er innihald hólfsins fyrst leiðrétt jákvætt með samsetningarfrálaginu. Það er lækkað strax á eftir í samræmi við afhent magn.

Gildið í þessum reit er sjálfkrafa sett inn í reitinn  í sölupantanalínum sem innihalda magn í reitnum **Magn til samsetningar til pöntunar** reitinn eða ef varan er seld sem **Sameina í pöntun** í reitnum **Áfyllingarkerfi**.

Ef **Setja saman í pöntun hólfakóði** er auður þá er **Frá-samsetning hólfkóða** reiturinn notaður. Ef báðir uppsetningarreitirnir eru auðir verður síðasta notaða hólfið sem hefur innihald notað í reitnum **Hólfkóði** í sölupöntunarlínum.

Sami hólfakóði er svo afritaður í reitinn **Hólfkóði** í birgðatínslulínunni sem stjórnar afhendingu á magninu sem sameina á í pöntun. Nánari upplýsingar eru í hlutanum „Meðhöndlun íhluta pantanasamsetninga við birgðatínslu” í [Tína vörur með Birgðatínslu](warehouse-how-to-pick-items-with-inventory-picks.md).

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Staðsetningar** og veldu síðan tengda tengilinn.
2. Opna birgðageymsluna sem setja á upp.
3. Færið inn **Setja saman í pöntun hólfakóði** reitinn.

## <a name="to-create-dedicated-component-bins"></a>Til að stofna sérnýtt íhlutahólf
Hægt er að tilgreina að magn í hólfi sé varið fyrir tínslu fyrir aðra eftirspurn vegna núverandi tilgangs.

Enn er hægt að taka frá magn í sérstökum hólfum. Í samræmi við það er magnið í sérnýttum hólfum tekið með í reitnum **Heildarmagn tiltækt** á síðunni **Frátekning**.

Sem dæmi er vinnustöð sett upp með hólfakóðanum í reitnum **Hólfakóði framleiðslu á innleið**. Íhlutalínur framleiðslupöntunar með þann hólfakóta krefjast þess að framvirkir íhlutir séu settir þar. Þar til íhlutir úr því hólfi hafa verið notaðir getur önnur íhlutaeftirspurn ollið tínslu eða notkun úr hólfinu vegna þess að íhlutirnir teljast enn vera tiltækt innihald hólfsins. Til að tryggja að hólfainnihald sé aðeins tiltækt fyrir íhlutseftirspurnina sem notar þann hólfkóða framleiðslu á innleið, þarf að velja reitinn **Sérstakt** í línunni fyrir þann hólfakóða á síðunni **Hólf** sem opnaður er í birgðageymsluspjaldinu.

Að hólf sé gert sérstakt veitir svipaða aðgerð og að nota hólfategundir, sem er eingöngu hægt í ítarlegum vöruhúsaaðgerðum. Frekari upplýsingar eru í [Setja upp hólfategundir](warehouse-how-to-set-up-bin-types.md).

> [!Caution]
> Vörur í sérstökum hólfum eru ekki varðar þegar þær eru tíndar eða notaðar sem framleiðsluíhlutir með síðunni Birgðatínsla.

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Staðsetningar** og veldu síðan tengda tengilinn. Velja birgðageymsluna sem á að uppfæra.  
2.  Veldu aðgerðina **Hólf**.  
3.  Veljið reitinn **Sérstakt** fyrir hvert hólf sem á aðeins að nota fyrir tiltekna innri starfsemi og þegar taka á magn frá fyrir þá starfsemi eftir að það hefur verið sett þangað.  

> [!NOTE]  
>  Hólfið verður að vera tómt áður en hægt er að velja eða hreinsa svæðið **Sérnýtt**.

## <a name="see-also"></a>Sjá einnig  
[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
[Samsetningardeild](assembly-assemble-items.md)    
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
