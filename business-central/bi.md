---
title: Fjárhagsgreiningar
description: 'Business Central hjálpar þér að safna saman, greina og deila gögnum fyrirtækisins um viðskiptaupplýsingar.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '103, 108, 198, 490'
ms.date: 03/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="financial-analytics"></a>Fjárhagsgreiningar

Fyrirtæki safna saman gríðarlegu magni gagna við daglegar aðgerðir sem styðja verðmætar viðskiptagreindar (BI) fyrir þá sem taka ákvarðanir:

- Sölutölur
- Innkaup
- Rekstrarkostnaður
- Laun starfsmanna
- Áætlun

[!INCLUDE[prod_short](includes/prod_short.md)] í henni eru margar aðgerðir til að hjálpa þér að safna saman, greina og deila fjárhagsgögnum fyrirtækisins:

- Ársskýrslugerð (fyrir ársreikninga og afkastalreikninga)
- Ad-hoc greining á listum
- Tilfallandi greining á gögnum í Excel (með opnum í Excel)
- Innbyggðar fjárhagsskýrslur

Hver þessara eiginleika hefur sína eigin kosti og galla, allt eftir tegund greiningar á gögnum og hlutverki notandans. Til að [fræðast meira er yfirlit yfir Analytics, viðskiptagreind og skýrslugerðaryfirlit](reports-bi-reporting.md).

Þessi grein kynnir þú getur notað þessar greiningaraðgerðir til að veita fjárhagslega innsýn.

## <a name="analytics-needs-in-finance"></a>Greiningarþarfir í fjármálum

Þegar hugsað er um greiningarþarfir í fjármálum getur það hjálpað til við að nota andlegt líkan byggt á einstaklingum sem lýst er á hástigi og mismunandi greiningarþarfir þeirra.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Útskýring ólíkra einstaklinga við greiningar" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Starfsfólk í mismunandi hlutverkum hefur mismunandi þarfir þegar kemur að gögnum og notar gögnin á mismunandi hátt. Til dæmis starfa starfsmenn í fjármálum við gögn á mismunandi hátt en einstaklingar í sölu.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Útskýring á því hvernig mismunandi einstaklingar hafa mismunandi greiningarþarfir." lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Hlutverk              | Uppsöfnun gagna  | Dæmigerðar leiðir til að nota gögn                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|Forstjóri / forstjóri          | Gögn um afköst  | Afkastavísar (KPI) <br> Mælaborð <br> Fjárhagsskýrslur           |
|Fjármálastjórnun | Þróun, samantektir | Innbyggðar stjórnunarskýrslur <br> Tilfalengd greining      | 
|Bókari         | Sundurliðuð gögn     | Innbyggðar rekstrarskýrslur <br> Gögn um verk á skjá |

## <a name="finance-kpis"></a>Afkastalsvinnsla fjármála

Lykilafkastavísir (afkastavísir) er mælanleg gildi sem sýnir hversu skilvirkt notandi uppfyllir markmiðin. Í fjármálum notar fólk oft eftirfarandi KPI til að fylgjast með fjárhagsheilsu fyrirtækisins:

- Brúttóframlegð
- Framlegð nettóframlegðar
- Stofnfé í vinnu
- Núverandi/fljótlegt hlutfall
- Fjármálaleg skuldsetning, einnig þekkt sem Margföldun hlutafjár
- Skuldir á eigin fé hlutfall
- Velta heildareignar
- Arðsemi eigin fjár
- Skil á eignum

<!-- Not ready to publish yet
For more information, see [Financial KPIs in Business Central](bi-finance-kpis.md) 
-->

## <a name="using-financial-reporting-to-produce-financial-statements-and-kpis"></a>Notkun fjárhagsskýrslna til að framleiða ársreikninga og afkastalsreikninga

Eiginleikinn **Ársskýrslur** veitir innsýn í fjárhagsgögnin sem birtast í bókhaldslyklinum (COA). Hægt er að setja upp fjárhagsskýrslur til að greina tölur á fjárhagsreikningum og bera saman fjárhagsfærslur og áætlunarfærslur. Niðurstöðurnar birtast í myndritum og skýrslum á heimasíðunni, svo sem sjóðstreymisritinu og rekstrarreikningi og efnahagsskýrslum.

Víddir gegna mikilvægu hlutverki í viðskiptagreind. Vídd er gögn sem þú getur bætt við færslu sem færibreytu. Víddir gera kleift að flokka færslur með svipaða eiginleika svo auðveldara sé að greina þær. Til dæmis viðskiptamenn, svæði, vörur og sölumenn. Meðal annars má nota víddir þegar greiningaryfirlit eru skilgreind og fjárhagsskýrslur stofnaðar. Frekari upplýsingar eru í [Vinna með víddir](finance-dimensions.md).

> [!TIP]
> Hægt er að greina færslugögn á skjótan hátt með því að afmarka samtölur á bókhaldslyklum og öllum færslum á síðunni **Færslur** eftir víddum. Leitaðu að aðgerðinni **Stilla víddarafmörkun**.  

Eftirfarandi tafla lýsir röð verka í fjárhagsskýrslugerð, með tenglum á greinarnar sem lýsa þeim.  

| Til | Sjá |
| --- | --- |
| Búðu til nýjar fjárhagsskýrslur til að skilgreina fjárhagsskýrslur fyrir skýrslugerð eða til að sýna sem gröf.| [Undirbúa fjárhagsskýrslur með fjárhagsgögnum og reikningsflokkum](bi-how-work-account-schedule.md)|
| Nota tölfræðilega reikninga til viðbótarupplýsinga í fjárhagsskýrslum. Með tölfræðilegum reikningum er hægt að bæta við mælikvörðum sem byggðar eru á gögnum sem ekki eru virk. Hægt er að bæta við gögnum sem ekki eru til staðar sem einingafjölda sem byggjast á tölum eins og höfuðstól starfsmanns, fermetrafjölda eða fjölda viðskiptamanna með reikninga sem komnir eru fram yfir gjalddaga. | [Greina gögn með tölfræðilegum lyklum](bi-use-statistical-accounts.md) |
| Fræðast um hvernig á að setja upp nýja fjárhagsskýrslu með dæmum. | [Kynning: Nota fjárhagsskýrslur til að gera sjóðstreymisspá](walkthrough-making-cash-flow-forecasts-by-using-account-schedules.md) |
| Greindu fjárhagslega frammistöðu þína með því að setja upp afkastamælikvarða (KPI) sem byggja á fjárhagsskýrslum sem þú gefur svo út sem vefþjónustur. Hægt er að skoða útgefið KPI fyrir fjárhagsskýrslur á vefsvæði eða flytja inn í Microsoft Excel með OData-vefþjónustum. |[Setja upp og gefa út KPI-vefþjónustu sem byggir á fjárhagsskýrslum](bi-how-to-set-up-and-publish-kpi-web-services-based-on-account-schedules.md) |
| Settu upp yfirlit til að greina gögn með víddum.|[Greina gögn eftir víddum](bi-how-analyze-data-dimension.md)|
| Búa til ný greiningaryfirlit fyrir sölu, innkaup og birgðir og búa til greiningarsniðmát. |[Stofna greiningarskýrslur](bi-how-create-analysis-views-reports.md)|

## <a name="finance-reporting-across-business-units-or-legal-entities"></a>Fjármálaskýrslur þvert á fyrirtækiseiningar eða lögaðila

Sum fyrirtæki nota [!INCLUDE [prod_short](includes/prod_short.md)] í mörgum fyrirtækiseiningum eða lögaðilum. Önnur nota [!INCLUDE [prod_short](includes/prod_short.md)] í dótturfélögum sem þarf að tilkynna um í móðurfyrirtækjum. [!INCLUDE [prod_short](includes/prod_short.md)] gefur endurskoðendum verkfæri sem hjálpa þeim að flytja fjárhagsfærslur frá tveimur eða fleiri fyrirtækjum (dótturfyrirtækjum) í samsteypufyrirtæki.  

Nánari upplýsingar eru í [Sameiningu fyrirtækis](finance-consolidated-company-reporting.md).

## <a name="ad-hoc-analysis-of-finance-data"></a>Tilfallandi greining á fjárhagsgögnum

Stundum þarf bara að athuga hvort tölurnar eru rétt settar upp eða staðfesta tölu á fljótlegan hátt. Eftirfarandi eiginleikar eru frábærir fyrir tilfalengdar greiningar:

- Gagnagreining á fjárhagslistasíðum
- Opna í Excel

Eiginleikinn Gagnagreining gerir kleift að opna næstum listasíðu, svo sem Fjárhagsfærslur, Eignafærslur, Tékkafærslur eða Bankareikningsfærslur, færa inn greiningarham og síðan flokka, afmarka og velta gögnum eftir hentugleikum.

:::image type="content" source="media/data-analysis-gl-entries.png" alt-text="Dæmi um gagnagreiningu á fjárhagsfærslusíðunni." lightbox="media/data-analysis-gl-entries.png":::

Á svipaðan hátt er hægt að nota aðgerðina **Opna í Excel** til að opna listasíðu fyrir færslur, afmarka listann við hlutmengi gagna og nota Excel svo til að vinna með gögnin. Til dæmis með því að nota aðgerðir eins og Greiningargögn, Hvað-Ef greining eða Spárblað.

:::image type="content" source="media/open-in-excel-gl-entries.png" alt-text="Dæmi um hvernig eigi að gera greiningu á gögnum um fjárhagsfærslur með Excel." lightbox="media/open-in-excel-gl-entries.png":::

> [!TIP]
> Ef grunnstillt OneDrive er fyrir kerfisaðgerðir opnast Excel-vinnubókin í vafranum með því að nota Excel fyrir vefinn. 


Nánari upplýsingar um hvernig á að gera tilfallandi greiningu á fjárhag eru [í Tilfallandi greining á fjárhagsgögnum](ad-hoc-analysis-finance.md). 

## <a name="built-in-reports-for-finance"></a>Innbyggðar skýrslur um fjármál

[!INCLUDE [prod_short](includes/prod_short.md)] þar á meðal eru nokkrar innbyggðar skýrslur, rakningaraðgerðir og verkfæri til að hjálpa endurskoðendum eða ráðamönnum sem bera ábyrgð á skýrslugerð til fjármáladeildarinnar.

Til að fá yfirlit yfir tiltækar skýrslur er hægt að velja **Allar skýrslur** efst á heimasíðunni. Þessi aðgerð opnar Hlutverkavafrann sem er afmarkaður við aðgerðirnar í valkostinum **Skýrsla & Greining** . Nánari upplýsingar eru í [Finna skýrslur með hlutverkavafranum](ui-role-explorer.md).

:::image type="content" source="media/report-explorer-finance.png" alt-text="Dæmi um skýrslur í fjármálahlutverkamiðstöðinni." lightbox="media/report-explorer-finance.png":::

Innbyggðar skýrslur koma í tveimur bragðtegundum:

- Hannað fyrir prentun (pdf).
- Hannað til greiningar í Excel.

Nánari upplýsingar eru í þessum yfirlitum um skýrslur sem varða fjármál.

- [Innbyggðar fjárhagsskýrslur í Excel](finance-analyze-excel.md)
- [Innbyggðar lykilfjárhagsskýrslur](finance-reports.md)
- [Innbyggðar eignaskýrslur](fa-reports.md)
- [Innbyggðar skýrslur viðskiptakrafna](receivables-reports.md)
- [Innbyggðar skýrslur viðskiptaskulda](payables-reports.md)

<!-- TODO: add when we have these articles
* [Built-in Cost Accounting reports](cost-accounting-reports.md) 
* [Built-in Cash Management reports](cost-accounting-reports.md) 
* [Built-in Tax and VAT reports](tax-and-vat-reports.md) 
-->

## <a name="on-screen-finance-task-pages"></a>Síður fjármálaverka á skjánum

[!INCLUDE [prod_short](includes/prod_short.md)] á nokkrum síðum sem gefa fjárhagsyfirlit og verkhluta.

### <a name="show-general-ledger-entries-and-balances-from-the-chart-of-accounts-page"></a>Sýna fjárhagsfærslur og stöður af síðunni Bókhaldslykill

Síðan Bókhaldslykill sýnir alla fjárhagsreikninga með samanlögðu númeri sem bókuð eru í fjárhaginn. Á þessari síðu er hægt að gera hluti eins og:  

- Skoða skýrslur sem sýna aðalbókaratriði og jafnvægi.  
- Skoða lista yfir bókunarflokka fyrir þann reikning.
- Skoða debet- og kreditstöður fyrir einstakan fjárhagsreikning

:::image type="content" source="media/chart-of-accounts-page.png" alt-text="Dæmi um hvernig síðan Bókhaldslykill sýnir fjárhagsinnsýni" lightbox="media/chart-of-accounts-page.png":::

Nánari upplýsingar eru í [Skilja bókhaldslykilinn](finance-general-ledger.md#the-chart-of-accounts).

### <a name="view-actual-amounts-compared-to-budgeted-amounts-for-all-accounts-and-for-several-periods"></a>Skoða raunverulegar upphæðir í samanburði við áætlaðar upphæðir allra reikninga og nokkurra tímabila

Þegar safnað er saman, greint og deilt gögnum fyrirtækisins gæti verið gott að skoða raunverulegar upphæðir í samanburði við áætlaðar upphæðir allra reikninga og nokkurra tímabila. Hægt er að gera þennan samanburð á síðunni **Bókhaldslykill** með því að velja aðgerðina **Fjárhagur - Staða/Áætlun** .

Nánari upplýsingar eru notaðar til að greina [raunverulegar upphæðir samanborið við áætlaðar upphæðir](bi-how-analyze-actual-versus-budget.md).

### <a name="analyze-data-by-dimensions"></a>Greining gagna eftir víddum

Víddir eru gildi sem flokka færslur svo þú getir fylgst með og greint þær í skjölum, t.d. sölupöntunum. Víddir geta til dæmis gefið í skyn verkið eða deildina sem færsla koma frá.  

Í stað þess að setja upp sérstaka fjárhagsreikninga fyrir hverja deild og verkefni er hægt að nota víddir sem grunn að greiningu og komast hjá því að búa til flókið bókhaldslykilsuppbyggingu.

Í fjárhagsgreiningu er vídd gögnum sem bætt er við fjárhagsfærslu sem nokkurs konar merki. Þessi gögn eru notuð til að flokka fjárhagsfærslur með svipaða eiginleika, t.d. viðskiptamenn, svæði, vörur og sölumenn, og sækja þessa flokka auðveldlega til greiningar. Hægt er að nota víddir í færslum í færslubókum, fylgiskjölum og áætlunum. Nánari upplýsingar [eru í Greina gögn eftir víddum](bi-how-analyze-data-dimension.md)

### <a name="analyzing-cash-flow"></a>Greining sjóðstreymis

Á heimasíðu endurskoðanda eru **í Fjármálaafköstum**, Sjóðsferli, Sjóðsstreymi og Tekjur og Útgjaldaliðir leiðir til að greina sjóðstreymi:

- Skoða tölur fyrir tímabil með því að nota tímalínusleðann.
- Síaðu töfluna með því að velja upprunan í uppsprettunni.
- Breyta lengd tímabilsins eða fara í fyrra eða næsta tímabil með því að velja valkosti í fellilistanum Vaxtaafköst.

:::image type="content" source="media/cashflow-accountant-rolecentre.png" alt-text="Dæmi um hvernig sjóðsstreymissjónarmið líta út á hlutverki endurskoðanda" lightbox="media/cashflow-accountant-rolecentre.png":::

Til að skoða spána, auk spárfærslna, er einnig hægt að skoða sjóðstreymisvinnublaðið. Til dæmis er hægt að sjá hvernig spá:

- Meðhöndlar staðfest sölu og innkaup
- Dregur frá viðskiptaskuldir og bætir við viðskiptakröfum
- Sleppur við tvíteknar sölupantanir og innkaupapantanir.

Nánari upplýsingar eru notaðar til að [greina sjóðstreymi í fyrirtækinu](finance-analyze-cash-flow.md).

## <a name="see-also"></a>Sjá einnig .

[Meðhöndla fjárhagsskýrslur yfir rekstrareiningar eða lögaðila](finance-consolidated-company-reporting.md)  
<!-- [Financial KPIs in Business Central](bi-finance-kpis.md)    -->
[Undirbúa fjárhagsskýrslur með fjárhagsgögnum og reikningsflokkum](bi-how-work-account-schedule.md)  
[Tilfallandi greining á fjárhagsgögnum](ad-hoc-analysis-finance.md)   
[Skilja bókhaldslykilinn](finance-general-ledger.md#the-chart-of-accounts)  
[Innbyggðar fjárhagsskýrslur í Excel](finance-analyze-excel.md)  
[Innbyggðar lykilfjárhagsskýrslur](finance-reports.md)  
[Innbyggðar eignaskýrslur](fa-reports.md)  
[Innbyggðar skýrslur viðskiptakrafna](receivables-reports.md)  
[Innbyggðar skýrslur viðskiptaskulda](payables-reports.md)  
[Yfirlit yfir Fjármál](finance.md)  
[Yfirlit yfir greiningar, viðskiptagreind og skýrslur](reports-bi-reporting.md)   
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
