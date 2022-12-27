---
title: Setja upp vinnuskýrslur og samþykktarferli þeirra
description: Þú setur upp vinnuskýrslu til að mæla tíma sem notaður er í verk og og verkefni, sem auðveldar þér verkefnastjórnun, mönnun og afkastaveitu
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource, time sheet
ms.search.form: 977, 462, 76, 77
ms.date: 12/13/2021
ms.author: edupont
ms.openlocfilehash: 7d019f9003ccd3ca0b2da7157d2d30f98d118e63
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/19/2022
ms.locfileid: "9532026"
---
# <a name="set-up-time-sheets"></a>Setja upp vinnuskýrslur

Vinnuskjöl í [!INCLUDE[prod_short](includes/prod_short.md)] meðhöndla tímaskráningu í vikulegum stigum sjö daga. Hægt er að nota þær til að mæla tímann sem fer í verkefni og til að skrá einfalda forðatímaskráningu. Áður en hægt er að nota vinnuskýrslur þarf að tilgreina hvaða notendur munu senda inn vinnuskýrslur og hvernig á að grunnstilla þær.  

> [!TIP]
> Í [!INCLUDE [prod_short](includes/prod_short.md)] eru notendur vinnuskýrslna *forðar*. Þannig er til dæmis hægt að nota vinnuskýrslur til að fylgjast með vinnu annarra en starfsmanna. Til að fylgjast með vinnu eigin starfsmanna eða nota vinnuskýrslur til að fylgjast með fjarvist starfsmanna verður þú að tengja *starfsmenn* við *forða* í uppsetningarleiðbeiningunum.  

Einnig er hægt að tilgreina hvort og hvernig vinnuskýrslur eru samþykktar. Allt eftir þörfum fyrirtækisins er hægt að tilgreina:

* Einn eða fleiri notendur sem vinnuskýrslustjóra og sem samþykkja allar vinnuskýrslur.
* Vinnuskýrslusamþykkjandi fyrir hvern forða.

Þegar búið er að setja upp vinnuskýrslur er hægt að búa til vinnuskýrslur fyrir forða og forðarnir geta bókað vinnuskýrslulínur. Einnig er hægt að úthluta vinnuskýrslum á verkáætlunarlínur. Frekari upplýsingar eru í [Nota vinnuskýrslur](projects-how-use-time-sheets.md).  

## <a name="set-up-time-sheets-with-the-assisted-setup-guide"></a>Setja upp vinnuskýrslur með leiðbeiningum um uppsetningu

[!INCLUDE [2021_releasewave2](includes/2021_releasewave2.md)]

Frá og með 2021 útgáfutímabili 2 getur þú notað leiðbeiningar um uppsetningu til að hjálpa þér að setja upp vinnuskýrslur.  

> [!TIP]
> Þú verður að virkja eiginleikann **Eiginleikauppfærsla: Ný upplifun fyrir vinnuskýrslu** á síðu [Eiginleikastjórnunar](https://businesscentral.dynamics.com/?page=2610) til að nota þennan möguleika.
>
> Sami eiginleiki auðveldar þér einnig að stjórna vinnuskýrslum í fartæki.

Opnaðu uppsetningarleiðbeininguna **Setja upp vinnuskýrslur** af síðunni [Uppsetning með hjálp](https://businesscentral.dynamics.com/?page=1801).

Leiðbeining um uppsetningu fer með þig í gegnum eftirfarandi skref:

1. Setja upp þátttakendur í vinnuskýrsluferli

    Fyrsta síðan í leiðbeiningunum sýnir þér fjölda notenda í [!INCLUDE [prod_short](includes/prod_short.md)]. Hún sýnir einnig aðrar nauðsynlegar og valfrjálsar upplýsingar.  
2. Tilgreina fyrsta dag vinnuviku í þessu fyrirtæki

    Fyrsti dagur vinnuviku verður sjálfgefinn fyrsti dagur fyrir allar vinnuskýrslur.
3. Tilgreina einstaklinginn sem stjórnar vinnuskýrslum

    Þessi einstaklingur getur breytt og eytt öllum vinnuskýrslum. Auk þess er valfrjálst að bæta sama hlutverkinu við aðra einstaklinga á síðunni **Uppsetning notanda**.
4. Setja upp tilföngin sem munu nota vinnuskýrslur og einstaklingana sem munu samþykkja vinnuskýrslur

Í lok uppsetningarleiðbeiningar getur þú valið að leyfa [!INCLUDE [prod_short](includes/prod_short.md)] að búa til vinnuskýrslur út frá stillingunum þínum. Skoðaðu nýju vinnuskýrslurnar á síðunni **Vinnuskýrslur** sem þú getur opnað [hér](https://businesscentral.dynamics.com/?page=951). Annars skal keyra uppsetningarleiðbeininguna aftur eða ljúka uppsetningunni handvirkt.  

## <a name="set-up-time-sheets-manually"></a>Setja upp vinnuskýrslur handvirkt

Eftirfarandi hlutar lýsa því hvernig á að setja upp vinnuskýrslur ef þú notar ekki uppsetningarleiðbeininguna **Setja upp vinnuskýrslur**.  

### <a name="to-set-up-general-information-for-time-sheets-manually"></a>Að setja upp almennar upplýsingar fyrir vinnuskýrslur handvirkt

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning tilfanga** og velja síðan viðkomandi tengil.  
2. Fyllið inn í svæðin eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Í reitnum **Vinnuskýrslur eftir samþykkt verks** skal velja einn af eftirfarandi valkostum.

| Valkostur | Lýsing |
| --- | --- |
| **Aldrei** |Notandinn í reitnum **Notandakenni samþykktaraðila vinnuskýrslu** á forðaspjaldinu samþykkir vinnuskýrsluna. |
| **Alltaf** |Notandinn í reitnum **Ábyrgðaraðili** á verkspjaldinu samþykkir vinnuskýrsluna. |
| **Aðeins véla** |Ef vinnuskýrsla vélar er tengd við verk er það notandinn í reitnum **Ábyrgðaraðili** á verkspjaldinu sem samþykkir vinnuskýrsluna. Ef vinnuskýrsla vélar er tengd við forða er það notandinn í reitnum **Notandakenni samþykktaraðila vinnuskýrslu** á forðaspjaldinu sem samþykkir vinnuskýrsluna. |

### <a name="to-assign-a-time-sheet-administrator-manually"></a>Að úthluta stjórnanda vinnuskýrslu handvirkt

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning notanda** og velja síðan viðkomandi tengil.  
2. Bæta við nýjum notanda ef notandalistinn inniheldur ekki einstaklinginn sem notandinn vill að sé vinnuskýrslustjórnandi. Frekari upplýsingar eru í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md).
3. Velja skal notanda sem á að vera vinnuskýrslustjóri og svo skal velja gátreitinn **Stjórnandi vinnuskýrslu**  

> [!TIP]  
> Mælt er með að aðeins einn notandi sé tilgreindur sem vinnuskýrslustjóri fyrir fyrirtæki. Í eftirfarandi ferli eru eigandi og samþykkjandi vinnuskýrslu settir upp þar sem samþykkjandi er tilgreindur fyrir hvern forða.  

### <a name="to-assign-a-time-sheets-owner-and-approver-manually"></a>Að úthluta eiganda og samþykktaraðila vinnuskýrslna handvirkt

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Tilföng** og velja síðan viðkomandi tengil.
2. Veljið forðann sem á að geta notað vinnuskýrslur og veljið svo gátreitinn **Nota vinnuskýrslu**.  
3. Í reitinn **Notandakenni eiganda vinnuskýrslu** skal slá inn notandakenni eiganda vinnuskýrslunnar. Eigandinn getur fært inn tímanotkun á vinnuskýrslu og sent hana til samþykktar. Þegar forði er einstaklingur er einstaklingurinn yfirleitt einnig eigandi.  
4. Í reitinn **Notandakenni samþykkjanda vinnuskýrslu** skal slá inn notandakenni samþykkjanda vinnuskýrslunnar. Samþykkjandi getur samþykkt, hafnað eða enduropnað vinnuskýrslu.  

> [!NOTE]  
> Ekki er hægt að auðkenni samþykkjanda vinnuskýrslu ef tíma fyrir eru tímaskýrslur sem ekki hefur verið unnið með og sem hafa stöðuna **Sent** eða **Opið**.

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft þjálfun](/training/paths/set-up-jobs-resources/)

## <a name="see-also"></a>Sjá einnig .

[Nota vinnuskýrslur fyrir verkefni](projects-how-use-time-sheets.md)  
[Hvernig á að stofna vinnuskýrslur](projects-how-use-time-sheets.md#to-create-time-sheets)  
[Skrá neyslu eða notkun fyrir verk](projects-how-record-job-usage.md)  
[Setja upp verkefnastjórnun](projects-setup-projects.md)  
[Verkefnastjórnun](projects-manage-projects.md)  
[Fjármál](finance.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Sala](sales-manage-sales.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
