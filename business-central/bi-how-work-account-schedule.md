---
title: Búa til fjárhagsskýrslur með fjárhagsgögnum og reikningsflokkum
description: Lýsir því hvernig skal nota fjárhagsskýrslur til að búa til ýmis konar yfirlit og skýrslur fyrir greiningar á gögnum fyrir fjárhagslega frammistöðu.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 03/27/2024
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, account schedule, financial report'
ms.search.form: '103, 104, 108, 195, 196, 197, 198, 489, 490, 764, 765, 766'
ms.service: dynamics-365-business-central
---
# <a name="prepare-financial-reporting-with-financial-data-and-account-categories"></a>Undirbúa fjárhagsskýrslugerð með fjárhagsgögnum og lykilflokkum

Eiginleikinn **Ársskýrslur** veitir innsýn í fjárhagsgögnin sem birtast í bókhaldslyklinum (COA). Hægt er að setja upp fjárhagsskýrslur til að greina tölur á fjárhagsreikningum og bera saman fjárhagsfærslur og áætlunarfærslur. Niðurstöðurnar birtast í myndritum og skýrslum í Hlutverkamiðstöðinni, t.d. sjóðstreymisritinu og rekstrarreikningi og efnahagsskýrslum. Þessar tvær skýrslur eru opnaðar, til dæmis með aðgerðinni **Ársreikningar** á heimasíðum viðskiptastjóra og endurskoðanda.  

[!INCLUDE[prod_short](includes/prod_short.md)] veitir sýnishorn fjárhagsskýrslna sem hægt er að nota strax sem sniðmát. Einnig er hægt að setja upp eigin skýrslur til að tilgreina tölurnar sem á að bera saman. Til dæmis er hægt að stofna fjárhagsskýrslur til að reikna út hagnaðarhlutfall með því að nota víddir eins og deildir eða viðskiptavinaflokka. Fjöldi fjárhagsskýrslna sem hægt er að búa til er ótakmarkaður og þarfnast ekki þátttöku forritara.  

## <a name="prerequisites-for-financial-reporting"></a>Skilyrði fyrir fjárhagsskýrslugerð

Uppsetning fjárhagsskýrslna krefst skilnings á skipulagi bókhaldslykilsins. Það eru þrjú lykilhugtök sem líklega þarf að vekja athygli á áður en fjárhagsskýrslurnar eru hannaðar:

- Varpa fjárhagsbókunarreikningum í fjárhagsreikningsflokka.
- Hanna hvernig víddir eru notaðar.
- Setja upp fjárhagsáætlanir.

Fjárhagsreikningsflokkar einfalda skilgreiningar fjárhagsskýrslunnar og gera þær breytilegri í uppbyggingu bókhaldslykils. Fá nánari upplýsingar í [Nota fjárhagsreikningsflokka til að breyta útliti ársreikninga](bi-row-definitions.md#use-gl-account-categories-to-change-the-layout-of-your-financial-statements).

Með uppsetningu vídda er hægt að sneiða og teninga fjárhagsgögnin á þann hátt sem fyrirtæki notanda skiptir máli. Frekari upplýsingar eru í [Vinna með víddir](finance-dimensions.md). 

Ef skoða á fjárhagsfærslur sem prósentuhlutfall af áætlunarfærslum þarf að búa til fjárhagsáætlanir. Frekari upplýsingar eru á [Stofna fjárhagsáætluanir](finance-how-create-budgets.md).

## <a name="financial-reports"></a>Fjárhagsskýrslur

Fjárhagsskýrslur raða reikningum úr bókhaldslyklum þínum á þann hátt sem auðveldar framsetningu gagna. Hægt er að setja upp margvísleg útlit til að skilgreina upplýsingarnar á að finna í bókhaldslyklinum. Fjárhagsskýrslur koma einnig fram staður fyrir útreikninga sem ekki er hægt að gera beint í bókhaldslyklinum. Til dæmis er hægt að búa til millisamtölur fyrir reikningsflokka og setja þær inn í aðrar samtölur Annað dæmi er að reikna út hagnaðarhlutfall á víddum eins og deildum eða viðskiptavinaflokkum. Þar að auki getur þú síað fjárhagsfærslur og fjárhagsáætlanafærslur, t.d. eftir nettóbreytingum eða debetupphæð.

> [!NOTE] 
> Í stærðfræði er fjárhagsskýrsla skilgreind eins og hún er skilgreind:
>
> - Vektor línuskilgreininga sem skilgreina hvað þarf að reikna.
> - Vektor dálkskilgreininga sem skilgreinir gögnin fyrir útreikninginn.
>
> Fjárhagsskýrslan er síðan ytri vara þessara tveggja vektora, þar sem hvert reitsgildi er reiknað samkvæmt reiknireglunni í línunni sem notuð er fyrir skilgreiningu gagna úr dálknum.

:::image type="content" source="media/financial-report-definition.svg" alt-text="Sýnir hvernig fjárhagsskýrsla er sett upp úr línuskilgreiningu og dálkskilgreiningu." lightbox="media/financial-report-definition.svg":::

Síðan **Ársskýrslur** sýnir hvernig öllum fjárhagsskýrslum fylgir mynstur sem samanstendur af eftirfarandi eigindum:

- Heiti (kóti)
- Heimildasamstæða
- Línuskilgreining
- Dálkskilgreining

:::image type="content" source="media/financial-reports.png" alt-text="Sýnir hvernig allar fjárhagsskýrslur eru settar upp úr línuskilgreiningu og dálkskilgreiningu." lightbox="media/financial-reports.png":::

> [!NOTE]
> Sýnishornaskýrslurnar í [!INCLUDE[prod_short](includes/prod_short.md)] eru ekki tilbúnar til notkunar úr kassanum. Eftir því hvernig fjárhagsreikningar, víddir, fjárhagsreikningaflokkar og áætlanir eru settir upp þarf að leiðrétta sýnilínu- og dálkskilgreiningar og fjárhagsskýrslurnar sem þeir eru notaðir í til að uppfylla uppsetninguna.

Einnig er hægt að nota reiknireglur til að bera saman tvær eða fleiri fjárhagsskýrslur og dálkskilgreiningar. Samanburður gerir kleift að gera eftirfarandi hluti:

- Búa til sérsniðnar viðskiptaskýrslur.
- Búa til eins mörg fjárhagsskýrslur og þú þarft, hver með einkvæmt heiti.
- Búa til uppsetningu skýrslu og prenta út skýrslurnar með núverandi tölum.

## <a name="learning-path-create-financial-reports-in-microsoft-dynamics-365-business-central"></a>Námsslóð: Búa til fjárhagsskýrslur í Microsoft Dynamics 365 Business Central

Viltu læra hvernig á að stofna áætlanir og nota síðan fjárhagsskýrslur, víddir og línu- og dálkaskilgreiningar til að búa til fjárhagsskýrslur sem fyrirtæki þurfa yfirleitt?

Byrja á eftirfarandi námsleið [Búa til fjárhagsskýrslur í Microsoft Dynamics 365 Business Central](/training/paths/create-financial-reports-dynamics-365-business-central).

## <a name="create-a-new-financial-report"></a>Stofna nýja fjárhagsskýrslu

Fjárhagsskýrslur eru notaðar til að greina fjárhagsreikninga eða bera saman fjárhagfærslur og fjárhagsáætlunarfærslur. Hægt er til dæmis að skoða fjárhagsfærslur sem prósentuhlutfall af áætlunarfærslum.

Fjárhagsskýrslurnar í stöðluðu útgáfunni [!INCLUDE[prod_short](includes/prod_short.md)] henta hugsanlega ekki viðskiptaþörfum. Til að búa til eigin fjárhagsskýrslur á fljótlegan hátt skal byrja á því að afrita eldri skýrslur, eins og lýst er í skrefi 3 hér á eftir.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") veldu táknið, sláðu inn **Fjárhagsskýrslur** og veldu síðan viðkomandi tengil.  
1. Á síðunni **Fjárhagsskýrslur** skal velja aðgerðina **Nýtt** til að búa til nýtt heiti fjárhagsskýrslu. Einnig er hægt að nota aftur stillingar úr fyrirliggjandi fjárhagsskýrslu með því að velja aðgerðina **Afrita fjárhagsskýrslu** .
1. Fært er inn stutt heiti skýrslunnar (ekki er hægt að breyta heitinu síðar) og lýsingu.
1. Velja línuskilgreiningu og dálkaskilgreiningu.
1. Valfrjálst er að velja greiningaryfirlit fyrir línu- og dálkaskilgreiningar.
1. Veljið aðgerðina **Breyta fjárhagsskýrslu** til að fá aðgang að fleiri eiginleikum fjárhagsskýrslunnar.
1. Á flýtiflipanum **Valkostir** er hægt að breyta skýrslulýsingunni, breyta línu- og dálkaskilgreiningum og skilgreina hvernig eigi að sýna dagsetningar. Dagsetningar geta verið dag- og viku-/mánaðar-/ársfjórðungsstigveldi eða notað reikningstímabil. Nánari upplýsingar eru notaðar í Samanburður á reikningstímabilum með því að [nota reiknireglur tímabila](bi-column-definitions.md#comparing-accounting-periods-using-period-formulas).
1. Á flýtiflipanum **Víddir** er hægt að skilgreina víddarafmarkanir fyrir skýrsluna.
1. Hægt er að forskoða skýrsluna á svæðinu fyrir neðan **flýtiflipann Víddir** .

> [!TIP]
> Þegar búið er að stofna fjárhagsskýrslu er hægt að nota síðuna **Fjárhagsskýrsla** til að forskoða og staðfesta hana. Til að opna síðuna skal velja aðgerðina **Skoða fjárhagsskýrslu** .  

> [!NOTE]
> Þegar fjárhagsskýrsla er opnuð í Skoða eða Breyta stillingu er afmörkunarsvæðið tiltækt. Ekki nota afmörkunarsvæðið til að setja afmarkanir á gögnin í skýrslunni. Slíkar afmarkanir geta valdið villum eða hugsanlega afmarka gögnin ekki í raun. Þess í stað eru reitirnir á flýtiflipunum **Valkostir** og **Víddir notaðir** til að setja upp afmarkanir fyrir skýrsluna.

### <a name="create-or-edit-a-row-definition"></a>Stofna eða breyta línuskilgreiningu

Línuskilgreiningar í fjárhagsskýrslum eru staður fyrir útreikninga sem ekki er hægt að gera beint í bókhaldslyklinum. Til dæmis er hægt að búa til millisamtölur fyrir reikningsflokka og setja þær inn í aðrar samtölur Einnig er hægt að reikna milliskref sem ekki eru sýnd í lokaskýrslunni.

Nánari upplýsingar eru notaðar í [Línuskilgreiningar í fjárhagsskýrslugerð](bi-row-definitions.md).

### <a name="create-or-edit-a-column-definition"></a>Stofna eða breyta dálkaskilgreiningu

Nota dálkaskilgreiningar til að tilgreina dálkana sem á að hafa með í skýrslunni. Til dæmis er hægt að hanna skýrsluuppsetningu til að bera saman breytingu og stöðu fyrir sama tímabil á þessu ári og síðasta ári. Hægt er að hafa allt að 15 dálka í dálkskilgreiningu. Til dæmis eru margir dálkar gagnlegir til að birta áætlanir í 12 mánuði með dálki sem sýnir samtöluna.

Nánari upplýsingar eru í [Dálkaskilgreiningar í fjárhagsskýrslugerð](bi-column-definitions.md).

## <a name="using-dimensions-in-financial-reports"></a>Notkun vídda í fjárhagsskýrslum

Í fjárhagsgreiningu er vídd tiltekin gögn sem má bæta við færslu sem einskonar merki. Þessi gögn eru notuð til að flokka saman færslur með svipuð einkenni, eins og viðskiptamenn, svæði, vörur og sölumenn og sækja þessa hópa á auðveldan hátt til greiningar. Hægt er að nota víddir í færslum í færslubókum, fylgiskjölum og áætlunum.

Hver vídd lýsir áherslu greiningar. Tvívíð greining gæti því til dæmis verið sala eftir svæðum. Með því að nota fleiri en tvær víddir þegar færsla er stofnuð er hægt að framkvæma flóknari greiningar. Dæmi um flókna greiningu er að kanna sölu á hverja söluherferð fyrir hvern viðskiptamannaflokk á hvert svæði. Það veitir meiri innsýn í reksturinn, svo sem hversu vel fyrirtækið þitt starfar, hvar það er eða ekki þrífst ekki og hvar þú ættir að ráðstafa meiri fjármunum. Innsýnin hjálpar þér að taka upplýstar viðskiptaákvarðanir. Hægt er að fá nánari upplýsingar með því að fara í [Vinna með víddir](finance-dimensions.md).

## <a name="set-up-financial-reports-with-overviews"></a>Setja upp fjárhagsskýrslur með yfirlitum

Hægt er að nota fjárhagsskýrslu til að búa til yfirlit sem ber fjárhagstölur saman við áætlunartölur.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 3.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") veldu táknið, sláðu inn **Fjárhagsskýrslur** og veldu síðan viðkomandi tengil.
1. Á síðunni **Fjárhagsskýrslur** skal velja Fjármálaskýrsla.  
1. Veldu aðgerðina **Breyta línuskilgreiningu**  
1. Á síðunni **Línuskilgreining** í reitnum **Heiti** skal velja sjálfgefið heiti fjárhagsskýrslu.
1. Veldu aðgerðina **Setja inn fjárhagsreikninga**.  
1. Reikningarnir sem eiga að vera í yfirlitinu eru valdir og smellt á **Í lagi**.

    Reikningarnir eru settir inn í fjárhagsskýrsluna. Einnig er hægt að breyta dálkaskilgreiningunni ef þess er óskað.  
1. Veldu aðgerðina **Breyta fjárhagsskýrslu**.  
1. Á síðunni **Fjárhagsskýrsla** á flýtiflipanum **Víddir** stillir þú á fjárhagsáætlunarsíuna á það nafn á síunni sem þú vilt nota.  
1. Velja **Í lagi**.  

Nú er hægt að afrita áætlunaryfirlitið og líma það inn í töflureikni.  

## <a name="print-and-save-financial-reports"></a>Prenta og vista fjárhagsskýrslur

Þú getur prentað fjárhagsskýrslur með því að nota prentþjónustu tækisins þíns. [!INCLUDE[prod_short](includes/prod_short.md)] Býður einnig upp á valkosti til að vista skýrslur sem Excel-vinnubækur, Word skjöl, PDF og XML-skrár.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 4.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") veldu táknið, sláðu inn **Fjárhagsskýrslur** og veldu síðan viðkomandi tengil.
1. Á síðunni **Fjárhagsskýrslur** velurðu skýrsluna sem á að prenta og velur svo aðgerðina **Prenta**.
1. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
1. Í reitnum **Prentari** er valið tækið sem skýrslan er send til.
    1. Valkosturinn **(Meðhöndlað af vafra)** gefur til kynna að enginn prentari sé valinn fyrir skýrsluna. Í þessu tilviki sér vafrinn um útprentun og birtir stöðluðu prentskrefin þar sem hægt er að velja staðbundinn prentara sem tengdur er tækinu. **(Meðhöndlaður af vafranum)** er ekki tiltækt í farsímaforritinu [!INCLUDE[prod_short](includes/prod_short.md)] eða forritinu fyrir teymi.
1. Velja aðgerðina **Prenta**.

### <a name="schedule-a-financial-report-or-save-as-a-pdf-word-or-excel-document"></a>Tímasetja fjárhagsskýrslu eða vista sem PDF-, Word- eða Excel-skjal

Hægt er að vista fjárhagsskýrslu á skráarsniði eins og PDF, XML, Word eða Excel. [!INCLUDE[prod_short](includes/prod_short.md)] einnig er hægt að búa til ítrekunarfjármálaskýrslur.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 4.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") veldu táknið, sláðu inn **Fjárhagsskýrslur** og veldu síðan viðkomandi tengil.
1. Á síðunni **Fjárhagsskýrslur** skal velja aðgerðina **Prenta**.
1. Stilltu skýrsluna í samræmi við það og veldu svo aðgerðina **Senda til**.
1. Veljið skráarsnið eða aðgerðina **Tímasetja** og veljið **Í lagi**.
1. Fylltu út reitina til að búa til tímasetta eða endurtekna fjárhagsskýrslu. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].<br><br>Þegar um endurteknar fjárhagsskýrslur er að ræða skal stilla reitina **Fyrsti upphafsdagur/tími** og **Lokadagsetning/tími** með fyrstu og síðustu dagsetningunni til að búa til fjárhagsskýrsluna. Veldu einnig á hvaða dögum skýrslan er mynduð með því að stilla reitinn fyrir **Fyrsti upphafsdagur/tími** með því að fylgja sniðinu sem útskýrt er í hlutanum [Nota dagsetningarformúlur](ui-enter-date-ranges.md#use-date-formulas).

## <a name="best-practices-for-working-with-financial-report-definitions"></a>Bestu starfsvenjur til að vinna með skilgreiningar fjárhagsskýrslu

Skilgreiningar á fjárhagsskýrslum eru ekki útgáfaðar. Þegar skýrsluskilgreiningu er breytt er gömlu útgáfunni skipt út þegar breytingin er vistuð í gagnagrunninum. Eftirfarandi listi hefur að geyma bestu starfsvenjur til að vinna með skilgreiningar á fjárhagsskýrslum:

- Ef skýrsluskilgreiningar eru bætt við er valinn góður kóti og lýsingarreiturinn fylltur út með mikilvægum texta á meðan notandi veit enn hvað skýrslan er notuð fyrir. Þessar upplýsingar auðvelda samstarfsfólki þínu (og framtíðar sjálfum þér) að vinna með skýrsluna og breyta skýrsluskilgreiningunni.
- Áður en skýrsluskilgreiningu er breytt skal íhuga að taka afrit af henni sem öryggisafrit, ef breytingin virkar ekki eins og búist er við. Annaðhvort er hægt að afrita skilgreininguna (gefa henni gott heiti) eða flytja hana út. Nánari upplýsingar eru í [Flytja inn eða út fjárhagsskýrsluskilgreiningar](#import-or-export-financial-report-definitions).
- Ef þörf er á fersku eintaki af skilgreiningu sem [!INCLUDE[prod_short](includes/prod_short.md)] útvegar er auðvelt að fá það til að stofna nýtt fyrirtæki sem inniheldur aðeins uppsetningargögn. Síðan skal flytja skilgreininguna út og flytja hana inn í fyrirtækinu þar sem skilgreiningin þarfnast endurnýjunar.

## <a name="import-or-export-financial-report-definitions"></a>Skilgreiningar á fjárhagsskýrslum eða innflutningi

Hægt er að flytja inn og út fjárhagsskýrsluskilgreiningar sem RapidStart grunnstillingarpakka. Til dæmis eru grunnstillingarpakkar gagnlegir til að deila upplýsingum með öðrum fyrirtækjum. Pakkinn er búinn til í .rapidstart-skrá, sem þjappar innihaldinu saman.

> [!NOTE]
> Þegar skilgreiningar fjárhagsskýrslu eru fluttar inn koma fyrirliggjandi færslur með sömu heitum og þær sem verið er að flytja inn með nýju skilgreiningunum. Skilgreiningarpakkinn fyrir skýrsluskilgreiningu skrifar ekki yfir fyrirliggjandi línu- eða dálkskilgreiningar sem eru notaðar í skýrsluskilgreiningunni.

Til að flytja inn eða út fjárhagsskýrsluskilgreiningar skal fylgja eftirfarandi skrefum:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 4.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") veldu táknið, sláðu inn **Fjárhagsskýrslur** og veldu síðan viðkomandi tengil.
1. Veldu fjárhagsskýrsluna og veldu svo aðgerðina **Flytja inn fjárhagsskýrslu** eða **Flytja út fjárhagsskýrslu**, eftir því hvað á að gera.

Farið er í eftirfarandi greinar til að fá nánari upplýsingar um hvernig á að flytja inn eða út fjárhagsskýrslulínur eða dálkaskilgreiningar: 

- [Línuskilgreiningar fyrir inn- eða útflutning fjárhagsskýrslugerðar](bi-row-definitions.md#import-or-export-financial-reporting-row-definitions), eða
- [Skilgreiningar fjárhagsskýrsludálka fyrir inn- eða útflutning](bi-column-definitions.md#import-or-export-financial-report-column-definitions)

## <a name="see-also"></a>Sjá einnig .

[Línuskilgreiningar í fjárhagsskýrslugerð](bi-row-definitions.md)  
[Dálkaskilgreiningar í fjárhagsskýrslugerð](bi-column-definitions.md)  
[Skoða og prenta skýrslur](ui-work-report.md)  
[Viðskiptagreind fjármála](bi.md)  
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Fjárhagur og bókhaldslyklar](finance-general-ledger.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
