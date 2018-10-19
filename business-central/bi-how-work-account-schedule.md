---
title: "Búa til fjárhagsskýrslur með fjárhagsskemum"
description: "Lýsir því hvernig skal nota fjárhagsskemu til að búa til ýmis konar yfirlit og skýrslur fyrir greiningar á afkastagögnum fjárhags."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 8e63e507411f41c67caa94834f4d99861bd1ae77
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="prepare-financial-reporting-with-account-schedules-and-account-categories"></a>Undirbúa fjárhagsskýrslugerð með fjárhagsskemu og lyklategundum
Notaðu reikningsáætlanir til að fá innsýn í fjárhagsupplýsingar sem eru geymdar í bókhaldslyklum. Fjárhagsskemu eru notuð til að greina upphæðir í fjárhagsreikningi og bera saman fjárhagsfærslur og færslur í fjárhagsáætlunarskýrslu. Niðurstöðurnar birtast í myndritum í Mínu hlutverki, eins og myndrit sjóðstreymis, og í skýrslum á borð við tekjuyfirlit og skýrslum efnahagsreiknings.

Þú opnar þessar tvær skýrslur til dæmis með aðgerðinni **Fjárhagsyfirlit** í Mínu hlutverki viðskiptastjórnanda og endurskoðanda.   

[!INCLUDE[d365fin](includes/d365fin_md.md)] veitir nokkrar sýnishornareikninga sem hægt er að nota strax eða þú getur sett upp eigin línur og dálka til að tilgreina tölurnar sem þú vilt bera saman. Notendur getur þú búið til fjárhagskema til að reikna út framlegð fyrir víddir eins og deildir eða hópa viðskiptamanna. Hægt er að búa til eins margar sérsniðnar fjárhagsskýrslur og óskað er.  

Uppsetning fjárhagsskema krefst skilnings á fjárhagsgögnum í bókhaldslyklinum. Hægt er til dæmis að skoða fjárhagsfærslur sem prósentuhlutfall af áætlunarfærslum. Þetta krefst þess að fjárhagsáætlanir séu búnar til. Frekari upplýsingar eru í [Stofna fjárhagsáætlun](finance-how-create-budgets.md).

## <a name="account-categories-and-account-schedules"></a>Lykiltegundir og fjárhagsskemu
Hægt er að nota lykiltegundir til að breyta sniði fjárhagsskýrslna. Þegar lykiltegundir hafa verið settar upp í glugganum **Flokkar fjárhagsreikninga** og aðgerðin **Mynda fjárhagsskemu** er valin, eru undirliggjandi fjárhagsskemu fyrir kjarnaviðskiptaskýrslur uppfærð. Í næsta skipti sem ein af þessum skýrslum er keyrð, t.d. skýrsla stöðuyfirlits, er nýjum samtölum og undirfærslum bætt við sem byggjast á breytingunum. Frekari upplýsingar er að finna í kaflanum „Lykilltegundir“ í [Skilja fjárhag og bókhaldslykil](finance-general-ledger.md).  

## <a name="to-create-new-account-schedules"></a>Nýtt fjárhagsskema búið til:  
 Fjárhagsskemu eru notuð til að greina upphæðir í fjárhagsreikningi eða bera saman fjárhagsfærslur og fjárhagsáætlunarfærslur. Hægt er til dæmis að skoða fjárhagsfærslur sem prósentuhlutfall af áætlunarfærslum.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **fjárhagsskema** og veldu síðan tengda tengilinn.  
2. Í glugganum **Heiti fjárhagsskema** skal velja aðgerðina **Nýtt** til að búa til nýtt heiti á fjárhagsskema.
3. Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Veljið aðgerðina **Breyta fjárhagsskema**.
5. Í glugganum **Fjárhagsskema** skal fylla reitina út eftir þörfum.  

    Þegar nýtt fjárhagsskema hefur verið stofnað og línurnar hafa verið settar upp, þarf að setja upp dálka. Annaðhvort er hægt að setja þær upp handvirkt eða úthluta forskilgreindri dálkauppsetningu á viðkomandi fjárhagsskema.
6. Veljið aðgerðina **Breyta uppsetningu dálkaútlits**.
7. Í glugganum **Dálkaútlit** skal fylla reitina út eftir þörfum.

> [!NOTE]  
> Ef ekki var tilgreint sjálfgefið dálkaútlit fyrir fjárhagsskemað verður að setja dálkana upp handvirkt.

### <a name="to-copy-an-existing-account-schedule"></a>Til að afrita fyrirliggjandi fjárhagsskema
Fjárhagsskemu í stöðluðu útgáfunni af [!INCLUDE[d365fin](includes/d365fin_md.md)] eru grunnurinn að stöðluðu fjárhagsskýrslunum sem mögulega passa ekki þörfum reksturs þíns. Til að búa til þínar eigin fjárhagsskýrslur á fljótlegan hátt geturðu byrjað á því að afrita fyrirliggjandi fjárhagsskema.
1. Í glugganum **Fjárhagsskema** skal velja fjárhagsskema og síðan velja aðgerðina **Afrita fjárhagsskema**.
2. Í glugganum **Afrita fjárhagsskema** skal fylla út reitina eftir þörfum og velja síðan hnappinn **Í lagi**.

### <a name="to-create-a-column-that-calculates-percentages"></a>Stofnun dálks sem reiknar prósentur:  
Stundum getur verið þörf á dálkum í fjárhagsskema til að reikna prósentur heilda. Til dæmis, ef nokkrar línur skipta sölu eftir vídd kann að vera þörf á dálki sem birtir prósentu heildarsölu sem hver lína stendur fyrir.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **fjárhagsskema** og veldu síðan tengda tengilinn.
2. Í glugganum **Heiti fjárhagsskema** veljið fjárhagsskema.  
3. Veljið aðgerðina **Breyta fjárhagsskema** til að setja upp fjárhagsskemalínu til að reikna heildina sem prósenturnar munu byggjast á.  
4. Setjið inn línu beint fyrir ofan fyrstu línuna sem birta á prósentur fyrir.  
5. Fyllið inn í reitina í línunni sem hér segir: Í **Tegund samantektar** reitnum er færður inn **Valinn stofn fyrir prósentur**. Í reitnum **Samantekt** er færð inn reikniregla fyrir heildina sem prósentan verður byggð á. T. d. ef lína 11 inniheldur heildarsölu, skal færa inn **11**.  
6. Veljið aðgerðina **Breyta uppsetningu dálkaútlits** til að setja upp dálk.  
7. Fyllið inn í reitina í línunni sem hér segir: Í **Tegund dálks** reitnum er færður inn **Formúla**. Í reitnum **Reikniregla** er færð inn reikniregla fyrir upphæðina sem reikna á prósentur fyrir, með % fyrir aftan. Til dæmis ef dálkur N inniheldur hreyfingu, er fært inn **N%**.  
8. Skref 4 til 7 eru endurtekin fyrir hvern flokk línu sem skipta á niður eftir prósentum.

## <a name="to-set-up-account-schedules-with-overviews"></a>Uppsetning fjárhagsskema með yfirlitum  
Hægt er að nota fjárhagsskema til að búa til reikning sem ber saman upphæðir fjárhagsreiknings og fjárhagsáætlunar.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **fjárhagsskema** og veldu síðan tengda tengilinn.
2. Í glugganum **Heiti fjárhagsskema** veljið fjárhagsskema.  
3. Veljið aðgerðina **Breyta fjárhagsskema**.  
4. Í glugganum **Fjárhagsskema** skal velja heiti sjálfgefins fjárhagsskema í reitnum **Heiti**.
5. Veljið aðgerðina **Setja inn reikning**.  
6. Reikningarnir sem eiga að vera í yfirlitinu eru valdir og smellt á **Í lagi**.

    Reikningarnir eru ekki settir inn í fjárhagsskemað. Einnig er hægt að breyta dálkauppsetningunni.  
7. Veljið aðgerðina **Yfirlit**.  
8. Í flýtiflipanum **Víddarafmarkanir** skal stilla afmörkunarheitið sem á að nota á áætlunarafmörkun.  
9. Velja hnappinn **Í lagi**.  

Nú er hægt að afrita áætlunaryfirlitið og líma það inn í töflureikni.  

## <a name="comparing-accounting-periods-using-period-formulas"></a>Samanburður á reikningstímabilum með reiknireglum tímabils
Fjárhagsskemað þitt getur borið saman niðurstöður mismunandi reikningstímabila, svo sem þessum mánuði miðað við sama mánuð í fyrra. Til að gera það bætir þú við dálki með reitnum **Reikniregla samanburðartímabils** og stillir síðan þennan reit á reiknireglu fyrir tímabil.  

Reikningstímabil þarf ekki að vera háð almanakinu, en þó verður að vera sami fjöldi reikningstímabila á öllum fjárhagsárum, þótt tímabilin geti verið mislöng.   

[!INCLUDE[d365fin](includes/d365fin_md.md)] nýtir reikniregluna fyrir tímabil til að reikna út upphæð frá samanburðartímabili miðað við tímabilið sem fæst við dagsetningarafmörkun á skýrslubeiðninni. Samanburðartímabilið byggir á upphafsdagsetningu dagsetningarsíunnar. Skammstafanirnar sem eiga við eru eftirfarandi:


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Skammstöfun</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>T</p></td>
<td><p>Tímabil</p></td>
</tr>
<tr class="even">
<td><p>ST</p></td>
<td><p>Síðasta tímabil reikningsárs, hálfs árs eða ársfjórðungs.</p></td>
</tr>
<tr class="odd">
<td><p>CP</p></td>
<td><p>Gildandi tímabil reikningsárs, hálfs árs eða ársfjórðungs.</p></td>
</tr>
<tr class="even">
<td><p>RÁ</p></td>
<td><p>Reikningsár. Til dæmis á RÁ[1..3] við um fyrsta fjórðung yfirstandandi reikningsárs.</p></td>
</tr>
</tbody>
</table>

Dæmi um reiknireglur:


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Reikniregla</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>&lt;Autt&gt;</p></td>
<td><p>Yfirstandandi tímabil</p></td>
</tr>
<tr class="even">
<td><p>-1T</p></td>
<td><p>Fyrra tímabil</p></td>
</tr>
<tr class="odd">
<td><p>-1RÁ[..ST]</p></td>
<td><p>Allt fyrra reikningsár</p></td>
</tr>
<tr class="even">
<td><p>-1RÁ</p></td>
<td><p>Yfirstandandi tímabil á fyrra reikningsári</p></td>
</tr>
<tr class="odd">
<td><p>-1RÁ[1..3]</p></td>
<td><p>Fyrsti fjórðung fyrra reikningsárs</p></td>
</tr>
<tr class="even">
<td><p>-1RÁ[..YT]</p></td>
<td><p>Frá upphafi fyrra reikningsárs til yfirstandandi tímabils og með því</p></td>
</tr>
<tr class="odd">
<td><p>-1RÁ[YT..ST]</p></td>
<td><p>Frá yfirstandandi tímabili á fyrra reikningsári til síðasta tímabils fyrra reikningsárs og með því</p></td>
</tr>
</tbody>
</table>

Ef þú vilt reikna eftir venjulegum tímabilum þarf í staðinn að slá inn reiknireglu í reitinn **Reikniregla samanburðartímabils**.

> [!NOTE]
> Það er ekki alltaf augljóst hvaða tímabil þú ert að bera saman vegna þess að þú getur stillt afmörkunardagsetningu í skýrslu sem nær yfir aðrar dagsetningar en reikningstímabilin sem endurspeglast í gögnum bókhaldslykilsins. Til dæmis stofnar þú fjárhagsskema þar sem þú vilt bera þetta tímabil saman við sama tímabil í fyrra, þannig að þú stillir reitinn **Afmörkunartímabil samanburðardagsetningar** á *-1FY*. Síðan keyrir þú skýrsluna 28. febrúar og setur afmörkunardagsetninguna á janúar og febrúar. Fyrir vikið ber fjárhagsskemað saman janúar og febrúar á þessu ári við janúar á síðasta ári, sem er eina reikningstímabilið sem hefur verið lokið á þessum tveimur árum.  


## <a name="see-also"></a>Sjá einnig
[Viðskiptaupplýsingar](bi.md)  
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Fjárhagur og bókhaldslyklar](finance-general-ledger.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

