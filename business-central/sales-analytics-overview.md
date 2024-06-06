---
title: Greiningar á sölu
description: 'Business Central inniheldur margar aðgerðir til að hjálpa þér að safna saman, greina og deila verðmætum sölugögnum fyrir viðskiptaupplýsingar og ákvarðanatöku innan sölufyrirtækisins.'
author: kennienp
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '516, 9300, 5119, 9301, 9305'
ms.date: 04/28/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="sales-analytics"></a>Greiningar á sölu

Fyrirtæki safna fjölda gagna við daglegar aðgerðir sem styðja viðskiptaupplýsingar (BI) fyrir sölustjóra:

- Tækifæri
- Sölutilboð
- Sölupantanir
- Sölureikningar

[!INCLUDE[prod_short](includes/prod_short.md)] veitir eiginleika sem hjálpa til við söfnun, greiningu og samnýtingu sölugagna fyrirtækisins:

- Ad-hoc greining á listum
- Tilfallandi greining á gögnum í Excel (með Opið í Excel)
- Innbyggð sölugreiningarverkfæri
- Innbyggðar söluskýrslur

Hver þessara eiginleika hefur sína kosti og galla, allt eftir tegund greiningar á gögnum og hlutverki notandans. Til að [fræðast meira er yfirlit yfir Analytics, viðskiptagreind og skýrslugerðaryfirlit](reports-bi-reporting.md).

Þessi grein kynnir hvernig hægt er að nota þessar greiningaraðgerðir til að fá innsýn í sölu.

## <a name="analytics-needs-in-sales"></a>Greiningarþarfir í sölu

Þegar hugsað er um greiningarþarfir í sölustjórnun getur það hjálpað til við að nota einstaklingsbundið líkan sem lýsir mismunandi greiningarþörfum á háu stigi.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Útskýring ólíkra einstaklinga við greiningar" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Starfsfólk í mismunandi hlutverkum hefur mismunandi þarfir þegar kemur að gögnum og notar gögnin á mismunandi hátt. Til dæmis getur starfsfólk í eignastjórnun og fjármagnað samskipti við gögn á annan hátt en fólk í sölu.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Útskýring á því hvernig mismunandi einstaklingar hafa mismunandi greiningarþarfir." lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Hlutverk              | Uppsöfnun gagna  | Dæmigerðar leiðir til að nota gögn                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|CCO / CFO / forstjóri    | Gögn um afköst  | Afkastavísar (KPI) <br> Mælaborð <br> Fjárhagsskýrslur           |
|Sölustjóri      | Þróun, samantektir | Innbyggðar stjórnunarskýrslur <br> Tilfalengd greining      | 
|Aðalbókari / Sölumaður | Sundurliðuð gögn     | Innbyggðar rekstrarskýrslur <br> Gögn um verk á skjá |

<!-- 
## <a name="sales-kpis"></a>Sales KPIs

A key performance indicator (KPI) is a measurable value that shows how effectively you’re meeting your goals. In sales management, people often use the following KPIs to monitor their organization's sales performance:

- TODO  
-->

## <a name="use-financial-reporting-to-produce-financial-statements-and-kpis-related-to-sales"></a>Nota fjárhagsskýrslugerð til að búa til ársreikninga og afkastatengda sölu

Eiginleikinn **Ársskýrslur** veitir innsýn í fjárhagsgögnin sem birtast í bókhaldslyklinum (COA). Hægt er að setja upp fjárhagsskýrslur til að greina tölur á fjárhagsreikningum og bera saman fjárhagsfærslur og áætlunarfærslur. Sérstaklega fyrir sölustjórnun er hægt að setja upp fjárhagsskýrslur á fjárhagsreikningum sem notaðir eru til að rekja sölubókanir.

Víddir gegna mikilvægu hlutverki í viðskiptagreind. Vídd eru gögn sem bætt er við færslu sem færibreytu. Í víddum er hægt að flokka færslur með svipaða eiginleika, t.d. viðskiptamenn, svæði, vörur og sölumann. Meðal annars má nota víddir þegar greiningaryfirlit eru skilgreind og fjárhagsskýrslur stofnaðar. Frekari upplýsingar eru í [Vinna með víddir](finance-dimensions.md).

Frekari upplýsingar um fjárhagsskýrslur er farið [í Undirbúning fjárhagsskýrslna með fjárhagsgögnum og reikningsflokkum](bi-how-work-account-schedule.md).

## <a name="finance-reporting-across-business-units-or-legal-entities-related-to-sales"></a>Fjármálaskýrsla þvert á fyrirtækiseiningar eða lögaðila sem tengjast sölu

Sum fyrirtæki nota [!INCLUDE [prod_short](includes/prod_short.md)] í mörgum fyrirtækiseiningum eða lögaðilum. Aðrir nota [!INCLUDE [prod_short](includes/prod_short.md)] í dótturfélögum sem gefa skýrslu til móðurfyrirtækja. [!INCLUDE [prod_short](includes/prod_short.md)] gefur endurskoðendum verkfæri sem hjálpa þeim að flytja fjárhagsfærslur frá tveimur eða fleiri fyrirtækjum (dótturfyrirtækjum) í samsteypufyrirtæki. Sérstaklega fyrir sölustjórnun gæti þurft að sameina fjárhagsfærslur fyrir sölureikninga til að geta rakið söluafkastagetu í fyrirtækiseiningum eða lögaðilum.

Nánari upplýsingar eru í [Sameiningu fyrirtækis](finance-consolidated-company-reporting.md).

## <a name="ad-hoc-analysis-of-sales-data"></a>Tilfalalengd greining á sölugögnum

Stundum þarf bara að athuga hvort tölurnar eru rétt settar upp eða staðfesta tölu á fljótlegan hátt. Eftirfarandi eiginleikar eru frábærir fyrir tilfalengdar greiningar:

- Gagnagreining á fjárhagslistasíðum
- Opna í Excel

Eiginleikinn Gagnagreining gerir kleift að opna næstum hvaða listasíðu sem er, svo sem **Fjárhagsfærslur**, **Viðskm.færslur**, **Birgðafærslur** eða **Bókaðir** reikningar, færa inn greiningarham og síðan flokka, afmarka og velta gögnum eftir hentugleika.

:::image type="content" source="media/data-analysis-customer-ledger-entries.png" alt-text="Dæmi um gagnagreiningu á síðunni Viðskm.færslur." lightbox="media/data-analysis-customer-ledger-entries.png":::

Á svipaðan hátt er hægt að nota aðgerðina **Opna í Excel** til að opna listasíðu, afmarka listann við undirmengi gagna og nota Excel svo til að vinna með gögnin. Til dæmis með því að nota aðgerðir eins og Greiningargögn, Hvað-Ef greining eða Spárblað.

:::image type="content" source="media/open-in-excel-customer-ledger-entries.png" alt-text="Dæmi um hvernig á að gera gagnagreiningu á gögnum viðskiptamannafærslna með Excel." lightbox="media/open-in-excel-customer-ledger-entries.png":::

> [!TIP]
> Ef grunnstillt OneDrive er fyrir kerfisaðgerðir opnast Excel-vinnubókin í vafranum.

Nánari upplýsingar um hvernig á að gera tilfallanda greiningu á sölugögnum er farið í [Tilfallandsgreiningu á sölugögnum](ad-hoc-analysis-sales.md). 

## <a name="built-in-reports-for-sales"></a>Innbyggðar skýrslur fyrir sölu

[!INCLUDE [prod_short](includes/prod_short.md)] inniheldur nokkrar innbyggðar skýrslur, rakningaraðgerðir og verkfæri til að hjálpa sölufyrirtækjum að gefa skýrslu um gögn sín.

Til að fá yfirlit yfir tiltækar skýrslur skal velja **Allar skýrslur** á efsta svæði heimasíðunnar. Þessi aðgerð opnar Hlutverkavafrann sem er afmarkaður við aðgerðirnar í valkostinum **Skýrsla & Greining** . Nánari upplýsingar eru í [Finna skýrslur með hlutverkavafranum](ui-role-explorer.md). 

:::image type="content" source="media/report-explorer-sales.png" alt-text="Dæmi um skýrslur í söluhlutverkamiðstöðinni." lightbox="media/report-explorer-sales.png":::

Innbyggðar skýrslur koma í tveimur bragðtegundum:

- Hannað fyrir prentun (pdf).
- Hannað til greiningar í Excel.

Til að [fá nánari upplýsingar um skýrslur sem tengjast sölu er farið í Innbyggðar söluskýrslur](sales-reports.md).

## <a name="on-screen-sales-analytics"></a>Sölugreiningar á skjá

[!INCLUDE [prod_short](includes/prod_short.md)] á nokkrum síðum sem gefa söluyfirlitum og verkhlutum kleift að gera. Hér eru nokkur dæmi til að koma þér í gang:

- [Listinn Sölutilboð er **opnaður**](https://businesscentral.dynamics.com/?page=9300)
- [Listinn Sölupantanir er **opnaður**](https://businesscentral.dynamics.com/?page=9305)
- [Listinn **Bókaðir sölureikningar er** opnaður](https://businesscentral.dynamics.com/?page=143)
- [Listinn Vöruskilapantanir **sölu er opnaður**](https://businesscentral.dynamics.com/?page=9304)
- [Reikna dagsetningar pöntunarloforða](sales-how-to-calculate-order-promising-dates.md)
- [Reikna út afhendingardagsetningar fyrir sölupantanir](sales-date-calculation-for-sales.md)
- [Finna sendingar](sales-how-track-packages.md)
- [Skoða tiltækileika vöru](inventory-how-availability-overview.md)
- [Staða standandi sölupöntunar](sales-how-to-create-blanket-sales-orders.md#to-view-the-status-of-a-blanket-sales-order)
- [Skoða óbókaðar og bókaðar línur standandi sölupöntunar](sales-how-to-create-blanket-sales-orders.md#to-view-unposted-and-posted-blanket-sales-order-lines)


### <a name="show-sales-related-general-ledger-entries-and-balances-from-the-chart-of-accounts-page"></a>Sýna sölutengdar fjárhagsfærslur og stöður af síðunni Bókhaldslykill

Síðan Bókhaldslykill sýnir alla fjárhagsreikninga með samanlögðu númeri sem bókuð eru í fjárhaginn. Á þessari síðu er hægt að gera hluti eins og:  

- Skoða skýrslur sem sýna aðalbókaratriði og jafnvægi.  
- Skoða lista yfir bókunarflokka fyrir þann reikning.
- Skoða debet- og kreditstöður fyrir einstakan fjárhagsreikning

Sérstaklega fyrir sölu er hægt að búa til yfirlit á síðunni Bókhaldslykill sem sýnir aðeins reikningana sem notaðir eru til að bóka sölufærslur.

:::image type="content" source="media/chart-of-accounts-page.png" alt-text="Dæmi um hvernig síðan Bókhaldslykill sýnir fjárhagsinnsýni" lightbox="media/chart-of-accounts-page.png":::

Nánari upplýsingar eru í [Skilja bókhaldslykilinn](finance-general-ledger.md#the-chart-of-accounts).

### <a name="analyze-data-by-dimensions-related-to-sales"></a>Greining gagna eftir víddum (tengd sölu)

Víddir eru gildi sem flokka færslur svo þú getir fylgst með og greint þær í skjölum, t.d. sölupöntunum. Víddir geta til dæmis gefið í skyn verkið eða deildina sem færsla koma frá.  

Í stað þess að setja upp sérstaka fjárhagsreikninga fyrir hverja deild eða staðsetningu er hægt að nota víddir sem grunn að greiningu og komast hjá því að búa til flókið bókhaldslykilsuppbyggingu.

Nánari upplýsingar eru notaðar til að greina [gögn eftir víddum](bi-how-analyze-data-dimension.md).

## <a name="see-also"></a>Sjá einnig .

[Samsteypufyrirtæki](finance-consolidated-company-reporting.md)   
[Undirbúa fjárhagsskýrslur með fjárhagsgögnum og reikningsflokkum](bi-how-work-account-schedule.md)  
[Meðhöndla fjárhagsskýrslur yfir rekstrareiningar eða lögaðila](finance-consolidated-company-reporting.md)  
[Tilfallugreining á sölugögnum](ad-hoc-analysis-sales.md)   
[Innbyggðar söluskýrslur](sales-reports.md)   
[Skilja bókhaldslykilinn](finance-general-ledger.md#the-chart-of-accounts)  
[Greina gögn eftir víddum](bi-how-analyze-data-dimension.md)  
[Yfirlit yfir greiningar, viðskiptagreind og skýrslur](reports-bi-reporting.md)   
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
