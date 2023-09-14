---
title: 'Uppsetning bestu venjur: Áætla færibreytur'
description: Þetta efnisatriði útskýrir bestu starfsvenjur um hvernig eigi að setja upp valda reiti fyrir færibreytu áætlanagerðar með flýtiflipa áætlanagerðar á birgðakortinu.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: bholtorf
---
# Uppsetning bestu venjur: Áætla færibreytur

Flýtiflipinn **Áætlun** á birgðaspjaldinu er þungamiðja birgðakeðju fyrirtækis. Uppsetning réttra áætlunarfæribreyta er mjög mikilvæg fyrir hagkvæma birgðastjórnun og gæði þjónustu við viðskiptamenn.  

 Eftirfarandi tafla gefur upp bestu venjur um uppsetningu valinna áætlunarfæribreytareita. Nánari upplýsingar um reit fást með því að velja tengilinn í dálkinum **Uppsetningarreitur**.  

|Uppsetning reits|Bestu starfsvenjur|Athugasemd|  
|-----------------|-------------------|-------------|  
|Endurpöntunarstefna||Nánari upplýsingar er að finna í [Uppsetning bestu venjur: Endurpöntunarstefnur](setup-best-practices-reordering-policies.md).|  
|Taka frá|Veljið **Aldrei** þegar varan er áætluð með endurpöntunarmarki.<br /><br /> Við framleiðslu skal velja **Aldrei** til að leyfa áætlunarkerfinu til að ná yfir alla eftirspurn.<br /><br /> Veljið **Valfrjálst** fyrir vörur sem hægt er að taka frá fyrir viðskiptamenn með mestan forgang.<br /><br /> Veljið **Alltaf** fyrir einstakar vörur (vörur sem ekki eru venjulegar), svo sem ýmsar vörur sem eru á innleið fyrir tiltekna þörf.|Frátekningar hafa yfirleitt andstæðan tilgang en áætlanir, sem koma jafnvægi á eftirspurn og framboð. Því ætti almennt ekki að taka frá vörur sem uppsettar eru fyrir áætlun.<br /><br /> Ef notandinn tekur frá birgðamagn fyrir eftirspurn í framtíðinni mun það trufla forsendur áætlunarinnar og þá gæti endurpöntunarmark virkað illa. Jafnvel þótt áætlað birgðastig sé leyfilegt með tilliti til endurpöntunarmarks, má magnið ekki vera til staðar vegna frátekningarinnar.|  
|Hömlutímabil|Uppsetning með tilliti til sveigjanleika birgisins.<br /><br /> Styttri tímabil gerir þér kleift að draga úr veltufé með því að forðast of mikið af hlutabréfum, en það mun einnig valda fleiri enduráætlunaraðgerðum.|Ef birgir samþykkir breytingar á pöntunum á síðustu stundu má nota lengra tímabil, búðu þig undir frekari endurskipulagningu. Ef birgirinn krefst fastari áætlana skal stytta tímabilið eins og hægt er.<br /><br /> Nánari upplýsingar um reitinn **Hömlutímabil** eru að finna í [Hönnunarupplýsingar: Áætlunarfæribreytur](design-details-planning-parameters.md).|  
|Taka með birgðir|Velja alltaf við notkun lotu-fyrir lotu endurpöntunarstefnu|Ekki velja einungis í einstökum tilvikum, eins og þegar birgðir eru ekki söluhæfar.|  
|Öryggisforskot|Stilla á milli 1D og 6D.<br /><br /> Setja öryggisforskot í að minnsta kosti einn dag til að tryggja að birgðir séu tiltækar deginum áður en þeirra er þörf.<br /><br /> Ef nýr birgir er notaður skal skilgreina lengri tíma þar til afhendingarframmistaða hans er þekkt.<br /><br /> Við framleiðslu skal skilgreina lengri afgreiðslutíma fyrir mikilvæga íhluti.|Aðföng sem áætluð eru af kerfinu til að forðast uppseld berast á sama dag og uppseld á sér stað. Þetta getur verið nokkrum klukkutímum of seint, til dæmis ef eftirspurnina þarf að morgni og framboðið kemur síðdegis. **Athugið:** Svæðið **Öryggisforskot** notar grunndagatal. Því eru 14D ekki endilega tvær vikur.|  
|Magn í öryggisbirgðum|Notist fyrir vörur sem þar sem mikil sveifla er í eftirspurn.<br /><br /> Við framleiðslu skal nota þetta fyrir mikilvæga íhluti.<br /><br /> Notist fyrir vörur sem falla undir þjónustusamninga.|Ef reiturinn **Endurpöntunarmark** er fylltur út virka öryggisbirgðir einnig sem endurpöntunarmark.|  
|Lotusöfnunartímabil|Ef aðeins þarf nokkrar stórar pantanir og í lagi er að safna upp birgðum skal stilla langt lotusöfnunartímabil.<br /><br /> Ef nota á margar litlar pantanir og lágmarksbirgðir skal stilla stutt lotusöfnunartímabil.|Lotusöfnunartímabilið er almennt séð lengsta tímabilið sem birgðir munu verða haldnar.|  
|Endurpöntunarmark|Byggja endurpöntunarmark á eftirspurnarforstillingu vörunnar.|Ef fyrirliggjandi gögn sýna að meðaleftirspurn vörunnar sé 100 einingar með sjö daga afhendingartíma er hægt að stilla lágmark endurpöntunarmarks á 100.<br /><br /> Það þýðir að þegar birgðastig fer niður fyrir 100 einingar mun áætlunarkerfið leggja til áfyllingu þar sem það tekur sjö daga að ná í vöruna og nóg þarf að vera til að uppfylla eftirspurnina innan þessara sjö daga.|  
|Tímarammi|Haft autt, þannig að birgðastig er athugað á hverjum degi.|Að kanna birgðastig daglega tryggir bestu endurpöntunarmarksáætlun. **Athugið:** Tímaramminn 1V þýðir að birgðastig getur verið undir endurpöntunarmarkinu í eina viku áður en stungið er upp á framboðspöntun.|  
|Sléttunarnákvæmni|Stillið á 0,00001 ef framleiðslan er dýr.|Mikið sléttað magn af úrkasti eða efnisnotkun getur valdið mjög háum birgðakostnaði. Það kann því að vera viðeigandi að stilla minnstu sléttunarnákvæmni með það að markmiði að lágmarka þennan hugsanlega kostnað.|  

> [!NOTE]  
> Bestu venjur fyrir áætlunarfæribreytur í birgðaspjöldum eiga einnig við um sömu svæðin á í birgðahaldseiningaspjöldum.  
>
> Ef fyrirtæki áætla eftirspurn fyrir mismunandi birgðageymslur er eindregið mælt með því að skilgreina birgðahaldseiningar fyrir hverja birgðageymslu og búa alla eftirspurn til með því að nota gildi úr reitnum **Kóti birgðageymslu**. Frekari upplýsingar hjá  [Hönnunarmiðstöð: áætlunarferðir með eða án birgðageymslna](production-planning-with-without-locations.md).  

## Sjá einnig  
[Uppsetning bestu venja: Framboðsáætlun](setup-best-practices-supply-planning.md)  
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)  
[Setja upp flókin notkunarsviðum með því að nota bestu venjur](set-up-complex-application-areas-using-best-practices.md)  
[Hönnunarupplýsingar: áætlun með eða án staðsetningar](production-planning-with-without-locations.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
