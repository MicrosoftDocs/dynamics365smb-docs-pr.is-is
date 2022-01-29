---
title: Setja upp vinnuskýrslur og samþykktarferli þeirra
description: Hægt er að setja upp vinnuskýrslur til að rekja tímann sem er notaður á verk og verk, sem hjálpa til við verkefnastjórnun, staffing og afkastagetu
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource, time sheet
ms.search.form: 977, 462, 76, 77
ms.date: 12/13/2021
ms.author: edupont
ms.openlocfilehash: 21993ad4ee675384f7ffebfc77e0999d5dec05a6
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/14/2022
ms.locfileid: "7972227"
---
# <a name="set-up-time-sheets"></a>Setja upp vinnuskýrslur

Vinnuskjöl í [!INCLUDE[prod_short](includes/prod_short.md)] meðhöndla tímaskráningu í vikulegum stigum sjö daga. Hægt er að nota þá til að rekja tímann sem notaður er á verkum og þá má nota til að skrá einfalda skráningu á forðatíma. Áður en hægt er að nota vinnuskýrslur verður að tilgreina hvaða notendur leggja fram vinnuskýrslur og hvernig á að samskipa vinnuskýrslur.  

> [!TIP]
> Í [!INCLUDE [prod_short](includes/prod_short.md)], notendur vinnublaða eru *fjármagn*. Þannig er hægt að nota vinnuskýrslur til að fylgjast með starfi sem ekki eru starfsmenn, td. Til að rekja vinnu eigin starfsmanna eða til að nota vinnuskýrslur til að rekja fjarvistir starfsmanna þarf að tengja *starfsmenn* við *tilföng* í uppsetningarhandbókinni.  

Einnig er tilgreint hvort og hvernig vinnuskýrslur eru samþykktar. Allt eftir þörfum fyrirtækisins er hægt að tilgreina:

* Einn eða fleiri notendur sem vinnuskýrslustjóra og sem samþykkja allar vinnuskýrslur.
* Vinnuskýrslusamþykkjandi fyrir hvern forða.

Þegar vinnuskýrslur hafa verið settar upp er hægt að stofna vinnuskýrslur fyrir tilföng og hægt er að bóka tímablaðslínur. Einnig er að tilgreina vinnuskýrslur í verkáætlunarlínum. Frekari upplýsingar eru í [Nota vinnuskýrslur](projects-how-use-time-sheets.md).  

## <a name="set-up-time-sheets-with-the-assisted-setup-guide"></a>Setja upp vinnuskýrslur með leiðbeiningum um uppsetningu

[!INCLUDE [2021_releasewave2](includes/2021_releasewave2.md)]

Frá og með 2021 útgáfutímabili 2 getur þú notað leiðbeiningar um uppsetningu til að hjálpa þér að setja upp vinnuskýrslur.  

> [!TIP]
> Þú verður að virkja eiginleikann **Eiginleikauppfærsla: Ný upplifun fyrir vinnuskýrslu** á síðu [Eiginleikastjórnunar](https://businesscentral.dynamics.com/?page=2610) til að nota þennan möguleika.
>
> Sami eiginleiki auðveldar þér einnig að stjórna vinnuskýrslum í fartæki.

Opna **uppsetningu vinnublaða með** aðstoð uppsetningarleiðbeininganna frá [síðunni aðstoð aðstoðar](https://businesscentral.dynamics.com/?page=1801).

Leiðbeining um uppsetningu fer með þig í gegnum eftirfarandi skref:

1. Setja upp þátttakendur í vinnuskýrsluferli

    Fyrsta síðan í leiðarvísinum sýnir þú fjölda notenda í þínum [!INCLUDE [prod_short](includes/prod_short.md)]. Þar koma einnig fram aðrar nauðsynlegar og valfrjálsar upplýsingar.  
2. Tilgreina fyrsta dag vinnuviku í þessu fyrirtæki

    Fyrsti dagur vinnuviku verður sjálfgefinn fyrsti dagur fyrir allar vinnuskýrslur.
3. Tilgreina einstaklinginn sem stjórnar vinnuskýrslum

    Þessi einstaklingur getur breytt og eytt öllum vinnuskýrslum. Auk þess er valfrjálst að bæta sama hlutverkinu við aðra einstaklinga á síðunni **Uppsetning notanda**.
4. Setja upp tilföngin sem munu nota vinnuskýrslur og einstaklingana sem munu samþykkja vinnuskýrslur

Í lok uppsetningarleiðbeiningar getur þú valið að leyfa [!INCLUDE [prod_short](includes/prod_short.md)] að búa til vinnuskýrslur út frá stillingunum þínum. Skoða nýju vinnublöðin á **síðunni tímablöð** sem opna má [hér](https://businesscentral.dynamics.com/?page=951). Annars skal keyra uppsetningarleiðbeininguna aftur eða ljúka uppsetningunni handvirkt.  

## <a name="set-up-time-sheets-manually"></a>Setja upp vinnuskýrslur handvirkt

Í eftirfarandi köflum er lýst hvernig á að setja upp vinnuskýrslur ef **leiðbeiningar um uppsetningu vinnublaða eru ekki notaðar**.  

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

## <a name="see-also"></a>Sjá einnig

[Nota vinnuskýrslur fyrir verk](projects-how-use-time-sheets.md)  
[Til að stofna vinnuskýrslur](projects-how-use-time-sheets.md#to-create-time-sheets)  
[Skrá notkun eða notkun verka](projects-how-record-job-usage.md)  
[Setja upp verkefnastjórnun](projects-setup-projects.md)  
[Verkefnastjórnun](projects-manage-projects.md)  
[Fjármál](finance.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Sala](sales-manage-sales.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]