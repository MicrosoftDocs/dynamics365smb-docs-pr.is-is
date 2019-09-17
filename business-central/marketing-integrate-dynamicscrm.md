---
title: Stjórna viðskiptavinum með Dynamics 365 for Sales| Microsoft Docs
description: Hægt er að nota Dynamics 365 for Sales innan Business Central til að varpa gögnum og hafa óaðfinnanlega samþættingu og samstillingu í heildarferlinu.
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map, Sales
ms.date: 06/13/2019
ms.author: bholtorf
ms.openlocfilehash: d0f1dfd88b30a4ec2e3a9bfd3366005a93d97f82
ms.sourcegitcommit: 6ef7d2fae52feff786f2e15e2863d7f5aaa762be
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/22/2019
ms.locfileid: "1917369"
---
# <a name="using-dynamics-365-for-sales-from-business-central"></a>Að nota Dynamics 365 for Sales úr Business Central
Ef þú notar Dynamics 365 for Sales til að taka þátt í viðskiptum, getur þú notað óaðfinnanlega samþættingu í heildarferlinu með því að nota [!INCLUDE[d365fin](includes/d365fin_md.md)] fyrir bakvinnsluaðgerðir á borð við úrvinnslu pantana, birgðastjórnun og fjármálagerð.

Áður en hægt er að nota möguleika samþættingar þarf fyrst að setja upp tenginguna og skilgreina notendur í [!INCLUDE[crm_md](includes/crm_md.md)]. Frekari upplýsingar er að finna í [Samþætting við Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).

> [!NOTE]
> Þessi skref lýsa ferlinu við samþættingu á vefútgáfum af [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[d365fin](includes/d365fin_md.md)]. Frekari upplýsingar um grunnstillingu á staðnum er að finna í [Undirbúningur Dynamics 365 for Sales fyrir samþættingu á staðnum](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

Samþætting forritanna gerir þér kleift að fá aðgang að gögnum í Sals úr [!INCLUDE[d365fin](includes/d365fin_md.md)], og í sumum tilfellum í hina áttina líka. Hægt er að vinna með og samstilla gögn sem báðar þjónustur eru með sameiginleg, t.d. viðskiptamenn, tengiliðir og söluupplýsingar og halda gögnum uppfærðum í báðum forritum.  

Til dæmis getur sölumaður í Sales notað verðlista frá [!INCLUDE[d365fin](includes/d365fin_md.md)] þegar sölupöntun er búin til. Þegar vörunni er bætt við sölupöntunarlínu í Sales er hægt að sjá birgðastöðuna (framboð) fyrir vöruna úr [!INCLUDE[d365fin](includes/d365fin_md.md)].

Á móti geta pantanavinnslur í [!INCLUDE[d365fin](includes/d365fin_md.md)] meðhöndlað sölupantanir sem eru fluttar sjálfkrafa eða handvirkt úr Sales. Til dæmis geta þær stofnað og bókað sölupöntunarlínur fyrir vörur eða tilföng sem voru færð inn í Sales sem innskriftarafurðir. Nánari upplýsingar er að finna í [Meðhöndlun á gögnum sölupöntunar](marketing-integrate-dynamicscrm.md#handling-sales-order-data).

> [!IMPORTANT]  
> [!INCLUDE[d365fin](includes/d365fin_md.md)] samlagast aðeins við Dynamics 365 for Sales. Önnur Dynamics 365 forrit sem breyta stöðluðu verkflæði eða gagnalíkani í Sales, til dæmis Project Service Automation, geta að rofið samþættinguna milli [!INCLUDE[d365fin](includes/d365fin_md.md)] og Sales.

### <a name="coupling-records"></a>Tengja skrár
Uppsetningarleiðbeiningar með hjálp leyfir þér að velja gögnin til að samstilla. Seinna er einnig hægt að setja upp samstillingu fyrir tilteknar færslur. Þetta er kallað *tenging*. Til dæmis getur þú tengt tiltekinn reikning í Sales við tiltekinn viðskiptamann í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Þessi kafli lýsir því sem á að taka tillit til þegar þú tengir færslur.

Til dæmis, ef þú vilt sjá Sales reikninga sem viðskiptamenn í [!INCLUDE[d365fin](includes/d365fin_md.md)], verður þú að tengja tvær gerðir af færslum. Til að gera það skal á listasíðunni **Viðskiptamenn** í [!INCLUDE[d365fin](includes/d365fin_md.md)] nota aðgerðina **Setja upp tengingu**. Svo tilgreinir þú hvaða [!INCLUDE[d365fin](includes/d365fin_md.md)] viðskiptamenn passa við hvaða reikninga í Sales.

Þú getur einnig búið til (og tengt) reikning í Sales á grundvelli til dæmis viðskiptamannafærslu í [!INCLUDE[d365fin](includes/d365fin_md.md)] með því að nota **Stofna reikning í Dynamics 365 for Sales** eða öfugt, notað **Stofna viðskiptamann í [!INCLUDE[d365fin](includes/d365fin_md.md)]**.

Þegar þú setur upp tengingu milli tveggja færslna getur þú einnig óskað handvirkt eftir að skrifað verði strax yfir núverandi færslu, t.d. viðskiptamann, af gögnum reiknings úr Sales (eða úr [!INCLUDE[d365fin](includes/d365fin_md.md)]) með því að nota aðgerðina **Samstilla núna**. Aðgerðin **Samstilla núna** sem spyr hvort skrifa eigi yfir gagnafærslur Sales eða [!INCLUDE[d365fin](includes/d365fin_md.md)].

Í sumum tilfellum verður þú að tengja ákveðin gagnasöfn á undan öðrum gagnasöfnum, eins og sýnt er í eftirfarandi töflu.

|Gögn|Hvað skal tengja fyrst|
|-----|----|
|Viðskiptavinir og reikningar|Tengja sölumenn við Sales notendur|
|Vörur og forði|Tengja mælieiningar við einingahópa Sales|
|Vörur og forðaverð|Tengja verðflokka viðskiptamanna við Sales verð|

> [!NOTE]  
> Ef verðin þín eða viðskiptamanna eru í erlendum gjaldmiðlum, skal ganga úr skugga um að gjaldmiðlar séu tengdir við gjaldmiðlafærslur Sales.

Í Sales velta sölupantanir á upplýsingum eins og viðskiptamönnum, mælieiningum, gjaldmiðlum, verðflokkum viðskiptamanna, vörum og/eða tilföngum. Til að samþættingin með sölupöntunum gangi eftir verður þú að tengja viðskiptamenn, mælieiningar, gjaldmiðla, verðflokka viðskiptamanna, vörur og/eða tilföng.

### <a name="fully-synchronizing-records"></a>Færslur fyrir fulla samstillingu
Í lok aðstoðaruppsetningarleiðbeiningarinnar geturðu valið aðgerðina **Keyra fulla samstillingu** til að byrja að samstilla allar [!INCLUDE[d365fin](includes/d365fin_md.md)] færslur við allar tengdar færslur í Sales. Á síðunni **Dynamics 365 for Sales Yfirferð á fullri samstillingu** skaltu velja **Ræsa** aðgerðina. Full samstilling getur tekið einhvern tíma að ljúka, en þú getur haldið áfram að vinna í [!INCLUDE[d365fin](includes/d365fin_md.md)] á meðan hún keyrir í bakgrunninum.

Til að athuga framvindu á einstökum verkum í fullri samstillingu skal á síðunni **Dynamics 365 for Sales Yfirfara fulla samstillingu** velja færslu til að skoða upplýsingar um. Til að uppfæra stöðuna við samstillingu, endurnýjaðu síðuna.

Frá síðunni **Uppsetning á tengingu Microsoft Dynamics 365** er hægt að fá upplýsingar um fulla samstillingu hvenær sem er. Héðan er einnig hægt að opna síðuna **Vörpun samþættingartöflu** til að sjá upplýsingar um töflurnar í [!INCLUDE[d365fin](includes/d365fin_md.md)] og Sales sem þarf að samstilla.

## <a name="handling-sales-order-data"></a>Meðhöndlun gagna sölupöntunar
Sölupantanir sem einstaklingar senda inn í [!INCLUDE[crm_md](includes/crm_md.md)] verða sjálfkrafa færðar til [!INCLUDE[d365fin](includes/d365fin_md.md)] ef valinn er gátreiturinn **Stofna sölupantanir sjálfvirkt** á síðunni **Microsoft Dynamics 365 Uppsetning tengingar**.
Einnig er hægt að umbreyta handvirkt innsendum sölupöntunum úr [!INCLUDE[crm_md](includes/crm_md.md)] með því að nota aðgerðina **Stofna í [!INCLUDE[d365fin](includes/d365fin_md.md)]** sem er tiltæk á síðunni **Sölupantanir - Dynamics 365 for Sales**.
Á slíkum sölupöntunum er reiturinn **Heiti** í upprunalegu pöntuninni fluttur og honum varpað í reitinn **Utanaðkomandi fylgiskjalsnúmer** á sölupöntuninni í [!INCLUDE[d365fin](includes/d365fin_md.md)].

Þetta getur líka virkað ef upprunalega sölupöntunin inniheldur innskriftarvörur, þ.e.a.s. vörur eða forða sem er skráður í hvorugu forritinu. Í því tilviki verður þú að fylla út reitina **Gerð innskriftarvöru** og **Nr. innskriftarvöru** reitirnir á síðunni **Sölugrunnur**, til þess að slíkri óskráðri vörusölu sé varpað í tiltekið vöru-/forðanúmer fyrir fjárhagsgreiningu.

Ef lýsingin á vörunni í upprunalegu sölupöntuninni er löng er stofnuð ný sölupöntunarlína af gerðinni **Athugasemd** til þess að rúma allan texta sölupöntunarinnar í [!INCLUDE[d365fin](includes/d365fin_md.md)].

Uppfærslur á reitum sölupöntunarhauss, t.d. síðasta sendingardagsetning eða umbeðinn afhendingardagur, sem er varpað í SÖLUPÖNTUN-PÖNTUN **Vörpun samþættingartöflu** eru samstilltar reglubundið í [!INCLUDE[crm_md](includes/crm_md.md)]. Ferli eins og losun á sölupöntun og afhendingu eða reikningsfærslu á sölupöntun eru bókuð á tímalínu sölupöntunar í [!INCLUDE[crm_md](includes/crm_md.md)]. Frekari upplýsingar er að finna í [Kynning á aðgerðastraumum](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/developer/introduction-activity-feeds).

> [!NOTE]  
> Reglubundin samstilling byggð á **Vörpun samþættingartöflu** SÖLUPÖNTUNAR-PÖNTUNAR virkar aðeins þegar samþætting sölupöntunar er virkjuð. Frekari upplýsingar er að finna í [Tengt við Dynamics 365 for Sales](admin-how-to-set-up-a-dynamics-crm-connection.md). Aðeins sölupantanir búnar til úr innsendum sölupöntunum í [!INCLUDE[crm_md](includes/crm_md.md)] eru samstilltar. Frekari upplýsingar er að finna í [Virkja sölupöntunarferli samþættingar](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration).

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098170]

## <a name="handling-sales-quotes-data"></a>Meðhöndlun á gögnum sölutilboða
Sölutilboð sem eru virkjuð í [!INCLUDE[crm_md](includes/crm_md.md)] verða flutt til [!INCLUDE[d365fin](includes/d365fin_md.md)] ef gátreiturinn **Vinna sjálfvirkt úr sölutilboðum** er valinn á síðunni **Microsoft Dynamics 365 Uppsetning tengingar**.
Einnig er hægt að umbreyta handvirkt virkjuðum sölutilboðum úr [!INCLUDE[crm_md](includes/crm_md.md)] með því að nota aðgerðina **Vinna úr í [!INCLUDE[d365fin](includes/d365fin_md.md)]** á síðunni **Sölutilboð - Dynamics 365 for Sales**.
Á slíkum sölutilboðum er reiturinn **Heiti** í upprunalega tilboðinu fluttur og honum varpað í reitinn **Utanaðkomandi fylgiskjalsnúmer** á sölupöntuninni í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Einnig er reiturinn **Virkt til** í tilboði fluttur og varpað í reitinn **Tilboð gildir til** í sölutilboði í [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Sölutilboð fara í gegnum margar útgáfur áður en þau eru fullkláruð. Bæði handvirk og sjálfvirk úrvinnsla á sölutilboðum í [!INCLUDE[d365fin](includes/d365fin_md.md)] tryggir að fyrri útgáfur af sölutilboðum eru safnvistaðar áður en unnið er úr nýjum útgáfum sölutilboða úr [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="handling-posted-sales-invoices-customer-payments-and-statistics"></a>Meðhöndlun bókaðra sölureikninga, greiðslna viðskiptamanna og talnaupplýsinga
Þegar sölupöntun hefur verið uppfyllt verða reikningar fyrir hana búnir til. Þegar sölupöntun er reikningsfærð er hægt að flytja bókaðan sölureikning til [!INCLUDE[crm_md](includes/crm_md.md)] ef gátreiturinn **Búa til reikning í [!INCLUDE[crm_md](includes/crm_md.md)]** er valinn á síðunni **Bókaður sölureikningur**. Bókaðir reikningar eru fluttir til [!INCLUDE[crm_md](includes/crm_md.md)] með stöðuna **Greiddir**.

Þegar greiðsla viðskiptamanns er móttekin fyrir sölureikninginn í [!INCLUDE[d365fin](includes/d365fin_md.md)] verður stöðu sölureiknings breytt í **Greiddur** með reitinn **Ástæða stöðu** stilltan á **Að hluta til** ef greiddur að hluta til eða **Að fullu** ef greiddur að fullu þegar aðgerðin **Uppfæra talnagögn reiknings** er valinn á síðu viðskiptamanns í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Virknin **Uppfæra talnagögn reiknings** uppfærir einnig gildi í reitum á borð við **Jafnvægi** og **Heildarsala** í upplýsingareitnum **[!INCLUDE[d365fin](includes/d365fin_md.md)] Talnagögn reiknings** í [!INCLUDE[crm_md](includes/crm_md.md)]. Að öðrum kosti er hægt láta áætluðu verkin Talnagögn um viðskiptavin og POSTEDSALESINV-INV keyra sjálfkrafa bæði þessi ferli í bakgrunninum.

## <a name="see-also"></a>Sjá einnig
[Samþætting við Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Umsjón með venslum](marketing-relationship-management.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md)  
[Vinna með notendur og heimildir](ui-how-users-permissions.md)    
[Nýliðaþjálfun fyrir fyrirtækið og notendur til Dynamics 365 (online)](/dynamics365/customer-engagement/admin/onboard-your-organization-and-users-to-dynamics-365-online)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
