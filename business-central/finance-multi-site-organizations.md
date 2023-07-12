---
title: Business Central fyrir fyrirtæki á mörgum stöðum og alþjóðlegar stofnanir | Microsoft Docs
description: Business Central býður upp á möguleika sem styðja „hub-and-spoke“ viðskiptalíkan.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'hub-and-spoke, multi-site, headquarter, sites'
ms.date: 10/01/2020
ms.author: bholtorf
---

# Business Central fyrir fyrirtæki á mörgum stöðum og alþjóðlegar stofnanir
Stofnanir á mörgum svæðum nota oft „hub-and-spoke“ viðskiptalíkan þegar móðurfyrirtæki, eða höfuðstöðvar, stjórna heildarrekstri fyrirtækisins en þar sem hvert svæði starfar sem ein, sjálfstæð eining. Svæði eru oft dreifð landfræðilega og hafa mismunandi þörf fyrir deilingu upplýsinga með höfuðstöðvum fyrirtækisins. Auk þess hafa svæði yfirleitt ekki sömu þarfir og oft skortir úrræði til að viðhalda stóru kerfi.

[!INCLUDE[prod_short](includes/prod_short.md)] gefur litlum og meðalstórum fyrirtækjum viðskiptalausn sem auðvelt er að nota og með lágum rekstrarkostnaði.

Í þessari grein eru útlistaðar nokkrar leiðir sem [!INCLUDE[prod_short](includes/prod_short.md)] styður við „hub-and-spoke“ viðskiptalíkan.

## Samþætting höfuðstöðvarfyrirtækisins og svæða

[!INCLUDE[prod_short](includes/prod_short.md)] er hægt að samþætta við bókhaldskerfi höfuðstöðvanna og uppfylla mismunandi þarfir mismunandi svæða, óháð stærð, staðsetningu eða gerð fyrirtækja.

Eftirfarandi skýringarmynd er dæmi um mismunandi svæði sem eru samþætt höfuðstöðvum fyrirtækis.

![Lýsing skýringarmyndar sjálfkrafa búin til.](media/multisite-headquarter-sites.png)

## Uppfylla þarfir innlendra og alþjóðlegra vefsvæða

Viðskiptaþörf á svæðum er oft mismunandi eftir iðnaði, viðskiptaaðferðum eða tengslum við höfuðstöðvar fyrirtækisins. [!INCLUDE[prod_short](includes/prod_short.md)] það er auðvelt að aðlaga og stækka fyrir ýmis konar fyrirtæki og staði. Microsoft AppSource býður upp á fjölmörg forrit frá Microsoft og samstarfsaðilum þess, og samstarfsaðilar geta nota [!INCLUDE[prod_short](includes/prod_short.md)] á stuttum tíma og með lágmarkstruflunum fyrir daglegan rekstur.

Fyrir fjölþjóðlegar stofnanir styður [!INCLUDE[prod_short](includes/prod_short.md)] lagalegar kröfur og viðskiptahætti á staðnum.

* Fyrir netútgáfur eru fleiri en  [40 staðbundnar útgáfur](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json)  af lands-/svæðum sem hægt er að setja upp sem viðbætur frá Microsoft AppSource.  
* Fyrir útgáfur  [innanhúss eru útgáfur lands-/svæðisútgáfa](/azure/architecture/solution-ideas/articles/business-central)  tiltækar annaðhvort sem Microsoft-staðfærðar útgáfur eða Partner-LED-viðbætur.

Yfir 4.000 samstarfsaðilar Microsoft um allan heim veita staðbundna sérþekkingu.

| **Fyrirtækjakröfur** | **Hvernig Business Central styður það** | **Frekari upplýsingar** |
|-------------------------|-------------------------|-------------------------|
| Sérsniðið kerfið til að það passi fyrir fyrirtækið. | Njóttu kerfis sem var hannað frá grunni fyrir meðalstór fyrirtæki. | [Yfirlit](https://dynamics.microsoft.com/business-central/overview/) |
| Skoða regluverk og staðbundnar venjur. | Fylgið staðbundnum lagaskilyrðum og viðskiptaháttum. | [Staðbundin virkni](about-localization.md) |
| Aðgangur að mörgum fyrirtækjum á einni síðu. | Fá flýtiaðgang að hvaða Business Central fyrirtæki sem er í stofnuninni. | [Fyrirtækjamiðstöð](ui-extensions-company-hub.md) |
| Sjá um mörg tungumál og gjaldmiðla. | Stuðningur við mörg tungumál og gjaldmiðla hjálpar við að uppfylla staðbundnar þarfir. | [Möguleikar á mörgum tungumálum](about-locale-language.md)<br></br>[Eiginleikar margra gjaldmiðla](finance-how-setup-additional-currencies.md) |


## Sameina fjárhagsgögn

Kjarninn í „hub-and-spoke“ viðskiptalíkani er geta höfuðstöðvanna og svæða til að skiptast á fjárhagslegum gögnum, jafnvel þegar höfuðstöðvarfyrirtækið og svæðin nota mismunandi kerfi, bókhaldsskipulag, tungumál og gjaldmiðla.

| **Fyrirtækjakröfur** | **Hvernig Business Central styður það** | **Frekari upplýsingar** |
|-------------------------|-------------------------|-------------------------|
| Sameina fjárhagsgögn frá svæðum. | Sameina fjárhagsskýrslu fyrir svæði, óháð því hvort þau nota Business Central eða annað forrit, í eina rekstrareiningu (fyrirtæki). | [Steypa saman fjárhagsgögnum frá mörgum fyrirtækjum](finance-consolidated-company-reporting.md) |
| Samþætta bókhaldsskipulag. | Flytja samstæðugögn frá mismunandi bókhaldsskipulagi yfir í þitt eigið. Innbyggt skráarsnið fyrir F&O (fáanlegt með bylgju 2, 2020) | [Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)<br></br>[Undirbúa fjárhagslykla fyrir sameiningu](finance-consolidated-company-reporting-setup.md#glacc) |
| Færslur í mörgum gjaldmiðlum. | Hjálpa til við að tryggja að fjárhagsskýrslur í ólíkum gjaldmiðlum séu réttar og nota rétt gengi. | [Uppfæra gengi](finance-how-update-currencies.md) |

## Deildu viðskiptainnsýn með samþættri greiningu

Tryggðu að fyrirtækið starfi í samræmi við viðskiptamarkmiðin með því að veita sameiginlegan skilning á núverandi stöðu. Samþættar greiningar geta hjálpað fólki að byggja ákvarðanir sínar á sömu staðreyndum.

| **Fyrirtækjakröfur** | **Hvernig Business Central styður það** | **Frekari upplýsingar** |
|-------------------------|-------------------------|-------------------------|
| Deila innsýn með síðum án víðtækrar tækniaðstoðar. | Búðu til KPI og stjórnborð viðskiptagreindar í Power BI byggt á gögnum þínum. | [Vinna með Business Central Data í Power BI](across-working-with-business-central-in-powerbi.md) |
| Búa til sérsniðnar fjárhagsskýrslur. | Búa til fjárhagsskýrslur byggðar á breytum. | [Viðskiptaupplýsingar](bi.md) |
| Í samræmi við staðreyndir. | Búa til, skoða og deila skýrslum með innri og ytri hagsmunaaðilum. | [Fjárhagsskýrslur](finance-reports.md) |
| Greindu gögnin í Excel. | Gátun, úrræðaleit og tilfallandi greiningar í Microsoft Excel. | [Greina fjárhagsskýrslur í Excel](finance-analyze-excel.md) |


## Gagnaskipti með API og XMLports

API og XMLports einfalda ferlið við að tengja tilvik [!INCLUDE[prod_short](includes/prod_short.md)], þar á meðal þau sem hafa verið sérstillt fyrir hvert vefsvæði.

| **Fyrirtækjakröfur** | **Hvernig Business Central styður það** | **Frekari upplýsingar** |
|-------------------------|-------------------------|-------------------------|
| Tengja sérsniðnar útgáfur meðal svæða og höfuðstöðva fyrirtækisins. | API síður geta afhjúpað hvaða birtingu sem er á einingu, þ.m.t. sérsniði hennar. | [Virkja API fyrir Business Central](/dynamics-nav/enabling-apis-for-dynamics-nav) |
| Útgáfustjórnun og öryggi. | API notar ODataV4, með útgáfum, veftengingu og breytingarakningu. | [Öryggi og vörn](/dynamics365/business-central/dev-itpro/security/security-and-protection) |
| Birta og flytja inn XML-skjöl. | Nota má kóðaeiningur sem óbundnar aðgerðir til að styðja við birtingu og inntöku á XML-skjölum. Til að vinna úr XML-skjölum er hægt að nota XMLports. Óbundnar aðgerðir geta einnig búið til XML eða JSON skjal. | [XMLport Hlutir](/dynamics365/business-central/dev-itpro/developer/devenv-xmlport-object) |
| Auðvelda viðhald með rafrænum gagnaskiptum. | Hægt er að bæta við rafrænni gagnaskiptilausn til að nota sem samþættingarlag milli höfuðstöðvarfyrirtækisins og svæða. | [Gagnaskiptarammi](across-about-the-data-exchange-framework.md) |
| Skipting gagna á milli mismunandi kerfa. | Notaðu XMLports til að búa til XML-skjöl sem síðan er hægt að skipta á milli höfuðstöðvarfyrirtækis sem notar eitt kerfi og svæða sem nota Business Central. | [XMLport Yfirlit](/dynamics365/business-central/dev-itpro/developer/devenv-xmlport-overview) |
| Skipuleggja flókin gagnaskipti. | Notaðu samsetningu XMLports með Business Central og Microsoft BizTalk Server til að fullnægja einstökum þörfum á svæðunum þínum.</br>Notaðu rafræna gagnaskiptilausn sem byggir á BizTalk Server and Commerce Gateway í Business Central ásamt XMLports fyrir flóknari kröfur. | [Vinna með skýrslur, runuvinnslur og XMLports](ui-work-report.md) |
| Tengjast lausnum og þjónustu þriðja aðila<sup></sup>. | API setur punktatengingu milli Business Central og lausna og þjónustu<sup></sup> þriðju aðila. | [API v2.0](/dynamics-nav/api-reference/v2.0/) |


## Kynna skilvirka framboðskeðju samstæðu

Vefsvæði þurfa oft aðgang að birgðakeðjunni og möguleika á að stýra tilteknum þáttum hennar. Til dæmis gætu svæði notað sama lánardrottinn en stjórnað eignum sínum og staðsetningum sérstaklega.

| **Fyrirtækjakröfur** | **Hvernig Business Central styður það** | **Frekari upplýsingar** |
|-------------------------|-------------------------|-------------------------|
| Meðhöndla færslur milli deilda sem eðlilegar sölu- og innkaupafærslur. | Nota færslur milli fyrirtækja til að búa til sölu- og innkaupaskjöl og færslur í fjárhag fyrir allt vinnuflæðið og fyrir fleiri en eitt fyrirtæki í einu til að útiloka tvöfalda gagnafærslu. | [Vinna með millifyrirtækjafærslur](intercompany-manage.md) |
| Nota pappírslaus ferli. | Forðastu kostnað við sendingu, móttöku og prentun skjala. | [Skjöl á innleið](across-income-documents.md)<br><br> [Stjórna viðhengjum, tenglum og athugasemdum á spjöldum og fylgiskjölum](ui-how-add-link-to-record.md) |

## Bregðast hratt við nýjum viðskiptaaðstæðum

Höfuðstöðvar verða að geta brugðist skjótt við breytingum á rekstri á hverjum stað. Samhliða Power Automate getur [!INCLUDE[prod_short](includes/prod_short.md)] getur þjónað sem viðvörunarkerfi.

![Skjámynd af færslu á samfélagsmiðlum: Lýsing sjálfkrafa búin til.](media/multisite-apps.png)

| **Fyrirtækjakröfur** | **Hvernig Business Central styður það** | **Frekari upplýsingar** |
|-------------------------|-------------------------|-------------------------|
| Búa sjálfkrafa til póstviðvaranir. | Setja upp viðvaranir í Power Automate sem mynda tölvupósta til að upplýsa þig um mikilvæg viðskiptaskilyrði á síðum eða samstarfsaðilum birgðakeðjunnar. | [Business Central og Power BI](admin-powerbi.md) |
| Nota hefðbundnar eða sérsniðnar viðvaranir. | Nota 12 mismunandi sniðmát fyrir Business Central eða setja upp eigin viðvaranir sem henta fyrirtækinu. | [Nota Business Central í sjálfvirku verkflæði](across-how-use-financials-data-source-flow.md) |

## Sjá einnig
[Stjórnun á Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
