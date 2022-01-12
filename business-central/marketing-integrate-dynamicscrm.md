---
title: Stjórna viðskiptavinum með notkun Dynamics 365 Sala (inniheldur Video) | Microsoft docs
description: Hægt er að nota Dynamics 365 Sales innan Business Central til að varpa gögnum og hafa óaðfinnanlegur samþætting og samstillingu í heildarferlinu.
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map, Sales
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 67d9915e4f60b20d0e871810dfc3d66450103a5a
ms.sourcegitcommit: 4c97f38fc53c1c1ec534054a4a100d8cfb73175b
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2021
ms.locfileid: "7940452"
---
# <a name="using-dynamics-365-sales-from-business-central"></a>Nota Dynamics 365 Sales úr Business Central
Ef þú notar Dynamics 365 Sales til að taka þátt í viðskiptum, getur þú notað óaðfinnanlega samþættingu í heildarferlinu með því að nota [!INCLUDE[prod_short](includes/prod_short.md)] fyrir bakvinnsluaðgerðir á borð við úrvinnslu pantana, birgðastjórnun og fjármálagerð.

Áður en hægt er að nota möguleika samþættingar þarf kerfisstjórinn fyrst að setja upp tenginguna og skilgreina notendur í [!INCLUDE[crm_md](includes/crm_md.md)]. Frekari upplýsingar er að finna í [Samþætting við Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).

> [!NOTE]
> Þessi skref lýsa ferlinu við samþættingu á vefútgáfum af [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar um grunnstillingu á staðnum er að finna í [Undirbúningur Dynamics 365 Sales fyrir samþættingu á staðnum](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

Samþætting forritanna gerir þér kleift að fá aðgang að gögnum í Sals úr [!INCLUDE[prod_short](includes/prod_short.md)], og í sumum tilfellum í hina áttina líka. Hægt er að vinna með og samstilla gögn sem báðar þjónustur eru með sameiginleg, t.d. viðskiptamenn, tengiliðir og söluupplýsingar og halda gögnum uppfærðum í báðum forritum.  

Til dæmis getur sölumaður í [!INCLUDE[crm_md](includes/crm_md.md)] notað verðlista frá [!INCLUDE[prod_short](includes/prod_short.md)] þegar sölupöntun er búin til. Þegar vörunni er bætt við sölupöntunarlínu í [!INCLUDE[crm_md](includes/crm_md.md)] er hægt að sjá birgðastöðuna (framboð) fyrir vöruna úr [!INCLUDE[prod_short](includes/prod_short.md)].

Á móti geta pantanavinnslur í [!INCLUDE[prod_short](includes/prod_short.md)] meðhöndlað sölupantanir sem eru fluttar sjálfkrafa eða handvirkt úr [!INCLUDE[crm_md](includes/crm_md.md)]. Til dæmis geta þær stofnað og bókað sölupöntunarlínur fyrir vörur eða tilföng sem voru færð inn í [!INCLUDE[crm_md](includes/crm_md.md)] sem innskriftarafurðir. Nánari upplýsingar er að finna í [Meðhöndlun á gögnum sölupöntunar](marketing-integrate-dynamicscrm.md#handling-sales-order-data).

> [!IMPORTANT]  
> [!INCLUDE[prod_short](includes/prod_short.md)] samlagast aðeins við [!INCLUDE[crm_md](includes/crm_md.md)]. Önnur Dynamics 365 forrit sem breyta stöðluðu verkflæði eða gagnalíkani í [!INCLUDE[crm_md](includes/crm_md.md)], til dæmis Project Service Automation, geta að rofið samþættinguna milli [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="coupling-records"></a>Tengja skrár
Uppsetningarleiðbeiningar með hjálp leyfir þér að velja gögnin til að samstilla. Seinna er einnig hægt að setja upp samstillingu fyrir tilteknar færslur. Þetta er kallað *tenging*. Til dæmis getur þú tengt tiltekinn reikning í [!INCLUDE[crm_md](includes/crm_md.md)] við tiltekinn viðskiptamann í [!INCLUDE[prod_short](includes/prod_short.md)]. Þessi kafli lýsir því sem á að taka tillit til þegar þú tengir færslur.

Til dæmis, ef þú vilt sjá [!INCLUDE[crm_md](includes/crm_md.md)] reikninga sem viðskiptamenn í [!INCLUDE[prod_short](includes/prod_short.md)], verður þú að tengja tvær gerðir af færslum. Til að gera það skal á listasíðunni **Viðskiptamenn** í [!INCLUDE[prod_short](includes/prod_short.md)] nota aðgerðina **Setja upp tengingu**. Svo tilgreinir þú hvaða [!INCLUDE[prod_short](includes/prod_short.md)] viðskiptamenn passa við hvaða reikninga í [!INCLUDE[crm_md](includes/crm_md.md)].

Þú getur einnig búið til (og tengt) reikning í [!INCLUDE[crm_md](includes/crm_md.md)] á grundvelli til dæmis viðskiptamannafærslu í [!INCLUDE[prod_short](includes/prod_short.md)] með því að nota **Stofna reikning í Dynamics 365 Sales** eða öfugt, notað **Stofna viðskiptamann í [!INCLUDE[prod_short](includes/prod_short.md)]**.

Þegar þú setur upp tengingu milli tveggja færslna getur þú einnig óskað handvirkt eftir að skrifað verði strax yfir núverandi færslu, t.d. viðskiptamann, af gögnum reiknings úr Sales (eða úr [!INCLUDE[prod_short](includes/prod_short.md)]) með því að nota aðgerðina **Samstilla núna**. Aðgerðin **Samstilla núna** sem spyr hvort skrifa eigi yfir gagnafærslur Sales eða [!INCLUDE[prod_short](includes/prod_short.md)].

Í sumum tilfellum verður þú að tengja ákveðin gagnasöfn á undan öðrum gagnasöfnum, eins og sýnt er í eftirfarandi töflu.

|Gögn|Hvað skal tengja fyrst|
|-----|----|
|Viðskiptavinir og reikningar|Tengja sölumenn við [!INCLUDE[crm_md](includes/crm_md.md)] notendur|
|Vörur og forði|Tengja mælieiningar við einingahópa [!INCLUDE[crm_md](includes/crm_md.md)]|
|Vörur og forðaverð|Tengja verðflokka viðskiptamanna við [!INCLUDE[crm_md](includes/crm_md.md)] verð|

> [!NOTE]  
> Ef verðin þín eða viðskiptamanna eru í erlendum gjaldmiðlum, skal ganga úr skugga um að gjaldmiðlar séu tengdir við gjaldmiðlafærslur Sales.

Í [!INCLUDE[crm_md](includes/crm_md.md)] velta sölupantanir á upplýsingum eins og viðskiptamönnum, mælieiningum, gjaldmiðlum, verðflokkum viðskiptamanna, vörum og/eða tilföngum. Til að samþættingin með sölupöntunum gangi eftir verður þú að tengja viðskiptamenn, mælieiningar, gjaldmiðla, verðflokka viðskiptamanna, vörur og/eða tilföng.

## <a name="fully-synchronizing-records"></a>Færslur fyrir fulla samstillingu
Í lok aðstoðaruppsetningarleiðbeiningarinnar geturðu valið aðgerðina **Keyra fulla samstillingu** til að byrja að samstilla allar [!INCLUDE[prod_short](includes/prod_short.md)] færslur við allar tengdar færslur í [!INCLUDE[crm_md](includes/crm_md.md)]. Á síðunni **Yfirferð á fullri samstillingu Dynamics 365 Sales** skaltu velja **Ræsa** aðgerðina. Full samstilling getur tekið einhvern tíma að ljúka, en þú getur haldið áfram að vinna í [!INCLUDE[prod_short](includes/prod_short.md)] á meðan hún keyrir í bakgrunninum.

Til að athuga framvindu á einstökum verkum í fullri samstillingu skal á síðunni **Yfirfara fulla samstillingu Dynamics 365 Sales** velja færslu til að skoða upplýsingar um. Til að uppfæra stöðuna við samstillingu, endurnýjaðu síðuna.

Frá síðunni **Uppsetning tengingar Microsoft Dynamics 365** er hægt að fá upplýsingar um fulla samstillingu hvenær sem er. Héðan er einnig hægt að opna síðuna **Vörpun samþættingartöflu** til að sjá upplýsingar um töflurnar í [!INCLUDE[prod_short](includes/prod_short.md)] og Sales sem þarf að samstilla.

## <a name="handling-sales-order-data"></a>Meðhöndlun gagna sölupöntunar
Sölupantanir sem einstaklingar senda inn í [!INCLUDE[crm_md](includes/crm_md.md)] verða sjálfkrafa færðar til [!INCLUDE[prod_short](includes/prod_short.md)] ef valinn er gátreiturinn **Stofna sölupantanir sjálfvirkt** á síðunni **Microsoft Dynamics 365 Uppsetning tengingar**.
Einnig er hægt að umbreyta handvirkt innsendum sölupöntunum úr [!INCLUDE[crm_md](includes/crm_md.md)] með því að nota aðgerðina **Stofna í [!INCLUDE[prod_short](includes/prod_short.md)]** sem er tiltæk á síðunni **Sölupantanir - Dynamics 365 for Sales**.
Á slíkum sölupöntunum er reiturinn **Heiti** í upprunalegu pöntuninni fluttur og honum varpað í reitinn **Utanaðkomandi fylgiskjalsnúmer** á sölupöntuninni í [!INCLUDE[prod_short](includes/prod_short.md)].

Þetta getur líka virkað ef upprunalega sölupöntunin inniheldur innskriftarvörur, þ.e.a.s. vörur eða forða sem er skráður í hvorugu forritinu. Í því tilviki verður þú að fylla út reitina **Gerð innskriftarvöru** og **Nr. innskriftarvöru** reitirnir á síðunni **Sölugrunnur**, til þess að sölur á óskráðum afurðum séu varpað á tiltekið vöru- og tilfanganúmer.

> [!NOTE]
> Ekki er hægt að varpa innskrift til vöru eða tilfangs í [!INCLUDE[prod_short](includes/prod_short.md)] sem er tengd við afurð í [!INCLUDE[crm_md](includes/crm_md.md)]. Til að leyfa innskriftir, mælum við með því að þú stofnir vöru eða tilfang sérstaklega í þeim tilgangi og tengir þær ekki við afurð í [!INCLUDE[crm_md](includes/crm_md.md)]. 

Ef lýsingin á vörunni í upprunalegu sölupöntuninni er löng er stofnuð ný sölupöntunarlína af gerðinni **Athugasemd** til þess að rúma allan texta sölupöntunarinnar í [!INCLUDE[prod_short](includes/prod_short.md)].

Uppfærslur á reitum sölupöntunarhausa, t.d. reitiri fyrir síðustu sendingardagsetningu eða umbeðinn afhendingardag, sem er varpað í **SÖLUPÖNTUN-PÖNTUN** vörpun samþættingartöflu eru samstilltar reglubundið í [!INCLUDE[crm_md](includes/crm_md.md)]. Ferli eins og losun á sölupöntun og afhendingu eða reikningsfærslu á sölupöntun eru bókuð á tímalínu sölupöntunar í [!INCLUDE[crm_md](includes/crm_md.md)]. Frekari upplýsingar er að finna í [Kynning á aðgerðastraumum](/dynamics365/sales-enterprise/manage-activities). <!--The /dynamics365/sales-enterprise/developer/introduction-activity-feeds link was broken. Should this actually point to /dynamics365/sales-enterprise/manage-activities-->

> [!NOTE]  
> Reglubundin samstilling sem byggir á **SALESORDER-ORDER** samþættingartaflavörpun virkar aðeins þegar samþætting sölupöntunar er virkjuð. Frekari upplýsingar er að finna í [Tengistillingar á uppsetningarsíðu Sales-tengingar](admin-prepare-dynamics-365-for-sales-for-integration.md). Aðeins sölupantanir búnar til úr innsendum sölupöntunum í [!INCLUDE[crm_md](includes/crm_md.md)] eru samstilltar. Frekari upplýsingar er að finna í [Virkja sölupöntunarferli samþættingar](/dynamics365/sales-enterprise/developer/enable-sales-order-processing-integration).

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098170]

## <a name="handling-sales-quotes-data"></a>Meðhöndlun á gögnum sölutilboða
Sölutilboð sem eru virkjuð í [!INCLUDE[crm_md](includes/crm_md.md)] verða flutt til [!INCLUDE[prod_short](includes/prod_short.md)] ef gátreiturinn **Vinna sjálfvirkt úr sölutilboðum** er valinn á síðunni **Microsoft Dynamics 365 Uppsetning tengingar**.
Einnig er hægt að umbreyta handvirkt virkjuðum sölutilboðum úr [!INCLUDE[crm_md](includes/crm_md.md)] með því að nota aðgerðina **Vinna úr í [!INCLUDE[prod_short](includes/prod_short.md)]** á síðunni **Sölutilboð - Dynamics 365 Sales**.
Á slíkum sölutilboðum er reiturinn **Heiti** í upprunalega tilboðinu fluttur og honum varpað í reitinn **Utanaðkomandi fylgiskjalsnúmer** á sölupöntuninni í [!INCLUDE[prod_short](includes/prod_short.md)]. Einnig er reiturinn **Virkt til** í tilboði fluttur og varpað í reitinn **Tilboð gildir til** í sölutilboði í [!INCLUDE[prod_short](includes/prod_short.md)].  

Sölutilboð fara í gegnum margar útgáfur áður en þau eru fullkláruð. Bæði handvirk og sjálfvirk úrvinnsla á sölutilboðum í [!INCLUDE[prod_short](includes/prod_short.md)] tryggir að fyrri útgáfur af sölutilboðum eru safnvistaðar áður en unnið er úr nýjum útgáfum sölutilboða úr [!INCLUDE[crm_md](includes/crm_md.md)].

Þegar valið er **Ferli** í [!INCLUDE[prod_short](includes/prod_short.md)] fyrir tilboð sem er í stöðu **Unnið** er sölupöntun stofnuð í [!INCLUDE[prod_short](includes/prod_short.md)] aðeins ef samsvarandi sölupöntun er send í [!INCLUDE[crm_md](includes/crm_md.md)]. Annars er tilboðið aðeins gefið út í [!INCLUDE[prod_short](includes/prod_short.md)]. Ef samsvarandi sölupöntun er send í [!INCLUDE[crm_md](includes/crm_md.md)] síðar og sölupöntun er stofnuð úr henni verður **Tilboðsnr.** uppfært í sölupöntuninni og tilboðið er safnvistað.

## <a name="handling-posted-sales-invoices-customer-payments-and-statistics"></a>Meðhöndlun bókaðra sölureikninga, greiðslna viðskiptamanna og talnaupplýsinga
Þegar sölupöntun hefur verið uppfyllt verða reikningar fyrir hana búnir til. Þegar sölupöntun er reikningsfærð er hægt að flytja bókaðan sölureikning til [!INCLUDE[crm_md](includes/crm_md.md)] ef gátreiturinn **Búa til reikning í [!INCLUDE[crm_md](includes/crm_md.md)]** er valinn á síðunni **Bókaður sölureikningur**. Bókaðir reikningar eru fluttir til [!INCLUDE[crm_md](includes/crm_md.md)] með stöðuna **Greiddir**.

Þegar greiðsla viðskiptamanns er móttekin fyrir sölureikninginn í [!INCLUDE[prod_short](includes/prod_short.md)] verður stöðu sölureiknings breytt í **Greiddur** með reitinn **Ástæða stöðu** stilltan á **Að hluta til** ef greiddur að hluta til eða **Að fullu** ef greiddur að fullu þegar aðgerðin **Uppfæra talnagögn reiknings** er valinn á síðu viðskiptamanns í [!INCLUDE[prod_short](includes/prod_short.md)]. Virknin **Uppfæra talnagögn reiknings** uppfærir einnig gildi í reitum á borð við **Jafnvægi** og **Heildarsala** í upplýsingareitnum **[!INCLUDE[prod_short](includes/prod_short.md)] Talnagögn reiknings** í [!INCLUDE[crm_md](includes/crm_md.md)]. Að öðrum kosti er hægt láta áætluðu verkin Talnagögn um viðskiptavin og POSTEDSALESINV-INV keyra sjálfkrafa bæði þessi ferli í bakgrunninum. 

## <a name="handling-sales-prices"></a>Umsjón með söluverðum
> [!NOTE]
> Á útgáfutímabili 2 árið 2020 gáfum við út einfaldaðri ferla til að setja upp og hafa umsjón með verðum og afsláttum. Ef þú ert nýr viðskiptamaður sem ert að nota þessa útgáfu þá ertu að nota nýju upplifunina. Ef þú ert núverandi viðskiptamaður, hvort þú ert að nota nýju upplifunina fer eftir því hvort stjórnandinn þinn hafi virkjað eiginleikauppfærsluna **Upplifun nýrrar verðlagningar** í **Eiginleikastjórnun**. Frekari upplýsingar er að finna [Virkjun væntanlegra eiginleika fyrir tíma](/dynamics365/business-central/dev-itpro/administration/feature-management).

Skrefin til að ljúka þessu ferli eru mismunandi eftir því hvort stjórnandinn hefur virkjað nýju verðupplifunina eða ekki. 

> [!NOTE]
> Ef stöðluð verðsamræming virkar ekki fyrir þig mælum við með því að þú notir sérsniðna samþættingu. Frekari upplýsingar eru í [Sérstilling samþættingar með Microsoft Dataverse](/dynamics365/business-central/dev-itpro/administration/administration-custom-cds-integration).

#### <a name="current-experience"></a>[Núverandi reynsla](#tab/current-experience/)
Í núverandi verðupplifun samstillir [!INCLUDE[prod_short](includes/prod_short.md)] söluverð sem: 

* Gildir fyrir alla viðskiptavini. Sjálfgefnir söluverðslistar eru búnir til út frá verðinu í reitnum **Einingarverð** á síðunni **Birgðaspjald** fyrir hlutina.
* Nota fyrir tiltekinn verðflokk viðskiptamanns. Til dæmis söluverð fyrir smásölu- eða heildsöluviðskiptavini þína. Gerið eftirfarandi til að samræma verð miðað við verðhóp viðskiptavinar:

    1. Tengdu atriði sem ákvarða verð í verðflokki viðskiptavinarins.
    2. Á síðunni **Verðflokkar viðskiptamanna** er tengt verðflokknum með því að velja **Tengt**, **Dynamics 365 Sales**, **Tenging** og **Setja svo upp tengingu**. Tengingin mun búa til virkan verðlista í [!INCLUDE[prod_short](includes/prod_short.md)] við sama heiti og verðflokkur viðskiptavinar í [!INCLUDE[crm_md](includes/crm_md.md)] og samstilla sjálfkrafa alla hluti sem verðflokkur viðskiptamanns notar til að skilgreina verðið.

:::image type="content" source="media/customer-price-group.png" alt-text="Verðflokkssíða viðskiptavinar.":::

#### <a name="new-experience"></a>[Ný reynsla](#tab/new-experience/)  

Nýja verðupplifunin samstillir verðlista sem uppfylla eftirfarandi skilyrði:

* Slökkt er á **Leyfa uppfærslu sjálfgilda**.
* Verðgerðin er Sala.
* Gerð upphæðar er Verð.
* Vörutegundin í línunum verður að vera Vara eða Forði. 
* Lágmarksmagn er ekki tilgreint.

[!INCLUDE[prod_short](includes/prod_short.md)] samstillir söluverð sem eiga við um alla viðskiptavini. Sjálfgefnir söluverðslistar eru búnir til út frá verðinu í reitnum **Einingarverð** á síðunni **Birgðaspjald** fyrir hlutina.

Til að samræma verðlista velurðu síðuna **Söluverðslisti**, **Tengt**, **Dynamics 365 Sales**, **Tenging** og síðan **Setja upp tengingu**. 

:::image type="content" source="media/sales-price-list.png" alt-text="Söluverðslistasíða.":::

---


## <a name="see-also"></a>Sjá einnig
[Samþætting við Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Umsjón með venslum](marketing-relationship-management.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md)  
[Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md)    
[Yfirlit yfir Sales og sölumiðstöð](/dynamics365/customer-engagement/sales-enterprise/overview)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]