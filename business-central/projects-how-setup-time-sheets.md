---
title: Setja upp vinnuskýrslur og samþykktarferli þeirra
description: 'Þú setur upp vinnuskýrslu til að mæla tíma sem notaður er í verk og og verkefni, sem auðveldar þér verkefnastjórnun, mönnun og afkastaveitu'
ms.reviewer: jswymer
author: brentholtorf
ms.author: bholtorf
mw.reviewer: ivkoleti
ms.topic: conceptual
ms.search.keywords: 'project management, capacity, staff, resource, time sheet'
ms.search.form: '977, 462, 76, 77, 462'
ms.date: 07/27/2023
ms.service: dynamics365-business-central
ms.custom: bap-template
---
# <a name="set-up-time-sheets"></a>Setja upp vinnuskýrslur

Vinnuskjöl í [!INCLUDE[prod_short](includes/prod_short.md)] meðhöndla tímaskráningu í vikulegum stigum sjö daga. Hægt er að nota þær til að mæla tímann sem fer í verkefni og til að skrá einfalda forðatímaskráningu. Áður en hægt er að nota vinnuskýrslur þarf að tilgreina hvaða notendur munu senda inn vinnuskýrslur og hvernig á að grunnstilla þær.  

> [!TIP]
> Þeir sem nota vinnuskýrslur eru  *fjármagn*. Til dæmis sem gerir þér kleift að nota vinnuskýrslur til að fylgjast með starfi sem ekki eru starfsmenn. Til að rekja vinnu starfsmanna, eða til að nota vinnuskýrslur til að rekja fjarvistir starfsmanna, verður að tengja starfsmenn við tilföng. Það er leiðarvísir fyrir aðstoðarforrit sem geta hjálpað þér að gera það. Til að fræðast um leiðbeiningarnar er farið í að  [Setja upp vinnuskýrslur með leiðbeiningum um uppsetningu á hjálpartæki](#set-up-time-sheets-with-the-assisted-setup-guide).  

Einnig er tilgreint hvort og hvernig, vinnuskýrslur eru samþykktar. Allt eftir þörfum fyrirtækisins er hægt að tilgreina:

* Einn eða fleiri notendur sem vinnuskýrslustjóra og sem samþykkja allar vinnuskýrslur.
* Vinnuskýrslusamþykkjandi fyrir hvern forða.

Þegar búið er að setja upp vinnuskýrslur er hægt að búa til vinnuskýrslur fyrir forða og forðarnir geta bókað vinnuskýrslulínur. Einnig er hægt að úthluta vinnuskýrslum á verkáætlunarlínur. Til að fá frekari upplýsingar er farið í að  [nota vinnuskýrslur](projects-how-use-time-sheets.md).  

## <a name="set-up-time-sheets-with-the-assisted-setup-guide"></a>Setja upp vinnuskýrslur með leiðbeiningum um uppsetningu

Leiðbeiningar fyrir uppsetningu hjálpartækja geta hjálpað við að setja upp vinnuskýrslur.  

> [!TIP]
> Sé útgáfa fyrr en 2023 út bylgju 1 (v22) verður að virkja  **uppfærsluaðgerðina: ný reynsla**  á vinnublaði er á  [síðunni Feature Management](https://businesscentral.dynamics.com/?page=2610)  til að nota þennan möguleika.
>
> Þessi stilling leyfir þér einnig að nota vinnuskýrslur í farsímabúnaði.

Opnaðu uppsetningarleiðbeininguna **Setja upp vinnuskýrslur** af síðunni [Uppsetning með hjálp](https://businesscentral.dynamics.com/?page=1801).

Leiðbeining um uppsetningu fer með þig í gegnum eftirfarandi skref:

1. Setja upp þátttakendur í vinnublaðaferlunum.

    Fyrsta síðan í leiðbeiningunum sýnir þér fjölda notenda í [!INCLUDE [prod_short](includes/prod_short.md)]. Hún sýnir einnig aðrar nauðsynlegar og valfrjálsar upplýsingar.  
2. Tilgreinið fyrsta dag vinnuviku í viðkomandi stofnun.

    Fyrsti dagur vinnuviku verður sjálfgefinn fyrsti dagur fyrir allar vinnuskýrslur.
3. Tilgreina þann sem stjórna vinnuskýrslum.

    Þessi einstaklingur getur breytt og eytt öllum vinnuskýrslum. Auk þess er valfrjálst að bæta sama hlutverkinu við aðra einstaklinga á síðunni **Uppsetning notanda**.
4. Setja upp tilföng sem munu nota vinnuskýrslur og fólkið sem samþykkir vinnuskýrslur.

Í lok uppsetningarleiðbeiningar getur þú valið að leyfa [!INCLUDE [prod_short](includes/prod_short.md)] að búa til vinnuskýrslur út frá stillingunum þínum. Skoðaðu nýju vinnuskýrslurnar á síðunni **Vinnuskýrslur** sem þú getur opnað [hér](https://businesscentral.dynamics.com/?page=951). Annars skal keyra uppsetningarleiðbeininguna aftur eða ljúka uppsetningunni handvirkt.

> [!IMPORTANT]
> Ef þú ert að nota 2023 út bylgju 1 (v22) eða síðar, til að tryggja að þú getir stjórnað vinnuskýrslum um farsíma, verður þú að kveikja handvirkt á  **notkun nýs**  valkosts í tímauppsetningu eins og lýst er í næstu aðferð.

## <a name="set-up-time-sheets-manually"></a>Setja upp vinnuskýrslur handvirkt

Í eftirfarandi köflum er lýst hvernig setja á upp vinnuskýrslur ef ekki eru notaðar leiðbeiningar um  **uppsetningu vinnublaða** .  

### <a name="to-set-up-general-information-for-time-sheets-manually"></a>Að setja upp almennar upplýsingar fyrir vinnuskýrslur handvirkt

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning tilfanga** og velja síðan viðkomandi tengil.  
1. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!IMPORTANT]
   > Ef þú ert að nota 2023 útgáfu Wave 1 (v22) eða seinna, til að tryggja að þú getir stjórnað vinnuskýrslum um farsíma, skaltu kveikja á  **valkostinum nota nýjar vinnuskýrslur** .
1. Í reitnum **Vinnuskýrslur eftir samþykkt verks** skal velja einn af eftirfarandi valkostum.

| Valkostur | Lýsing |
| --- | --- |
| **Aldrei** |Notandinn í reitnum **Notandakenni samþykktaraðila vinnuskýrslu** á forðaspjaldinu samþykkir vinnuskýrsluna. |
| **Alltaf** |Notandinn í reitnum **Ábyrgðaraðili** á verkspjaldinu samþykkir vinnuskýrsluna. |
| **Aðeins véla** |Ef vinnuskýrsla vélar er tengd við verk er það notandinn í reitnum **Ábyrgðaraðili** á verkspjaldinu sem samþykkir vinnuskýrsluna. Ef vinnuskýrsla vélar er tengd við forða er það notandinn í reitnum **Notandakenni samþykktaraðila vinnuskýrslu** á forðaspjaldinu sem samþykkir vinnuskýrsluna. |

### <a name="to-assign-a-time-sheet-administrator-manually"></a>Að úthluta stjórnanda vinnuskýrslu handvirkt

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning notanda** og velja síðan viðkomandi tengil.  
3. Velja skal notandann sem verður kerfisstjóri tímablaðsins og velja  **síðan admin Time.** gátreit.  

> [!TIP]  
> Mælt er með því að aðeins einn notandi sé tilnefndur sem vinnublaðstjórinn fyrir fyrirtæki. Í eftirfarandi ferli eru eigandi og samþykkjandi vinnuskýrslu settir upp þar sem samþykkjandi er tilgreindur fyrir hvern forða.  

### <a name="to-assign-a-time-sheets-owner-and-approver-manually"></a>Að úthluta eiganda og samþykktaraðila vinnuskýrslna handvirkt

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Tilföng** og velja síðan viðkomandi tengil.
2. Velja skal tilfang sem setja á upp möguleika á að nota vinnuskýrslur fyrir og velja  **síðan gátreitinn Nota vinnublað** .  
3. Í reitinn **Notandakenni eiganda vinnuskýrslu** skal slá inn notandakenni eiganda vinnuskýrslunnar. Eigandinn getur fært inn tímanotkun á vinnuskýrslu og sent hana til samþykktar. Þegar forði er einstaklingur er einstaklingurinn yfirleitt einnig eigandi.  
4. Í reitinn **Notandakenni samþykkjanda vinnuskýrslu** skal slá inn notandakenni samþykkjanda vinnuskýrslunnar. Samþykkjandi getur samþykkt, hafnað eða enduropnað vinnuskýrslu.  

> [!NOTE]  
> Ekki er hægt að breyta AUÐKENNI samþykkjanda vinnuskjals ef til eru vinnuskýrslur sem hafa ekki verið unnar og hafa stöðuna  **send**  eða  **opin**.

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
