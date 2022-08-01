---
title: Tímasetja verk til að keyrast sjálfvirkt
description: Tímasettum verkum er stjórnað af verkröðinni. Þessi verk keyra skýrslur og kóðaeiningar. Stilla má verk svo þau keyri einu sinni eða endurtekið.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 672, 673, 674, 671
ms.date: 10/01/2021
ms.author: edupont
ms.openlocfilehash: 9ed56b0724b19d971b8dc98ea79807423403fd83
ms.sourcegitcommit: f1e272485a0e675d337a694aba3e35a5daf43920
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/09/2022
ms.locfileid: "9129766"
---
# <a name="use-job-queues-to-schedule-tasks"></a>Nota verkraðir til að tímaraða verkhlutum

Starfbiðraðir gera notendum kleift að raða og keyra tilteknar skýrslur og kódeseiningar. Stilla má verk svo þau keyri einu sinni eða endurtekið. Til dæmis er hægt að keyra **sölumannskýrsluna Sölumaður * Söluupplýsingar** vikulega til að fylgjast með sölu eftir sölumönnum í hverri viku eða keyra samþykkiseiningin biður **um** samþykki á kótaeiningu daglega til að koma í veg fyrir að skjöl gangi upp.

Síðan **Verkraðarfærslur** birtir öll núverandi verk. Ef bætt er við nýrri verkraðarafærslu sem á að raða upp verður að gefa upp einhverjar upplýsingar. Dæmi:
* Gerð hlutarins sem á að keyra, til dæmis skýrslu eða Codeunit. Þú verður að hafa heimild til að keyra viðkomandi skýrslu eða Codeunit.
* Nafn og HLUTARKENNI hlutarins. 
* Færibreytur til að tilgreina hegðun verkraðarafærslu. Til dæmis er hægt að bæta við færibreytu til að sent einungis bókaðar sölupantanir. 
* Þegar, og hversu oft, keyrir verkraðarafærsla.

> [!IMPORTANT]  
> Ef notað er SUPER-heimildasafnið sem fylgir með [!INCLUDE[prod_short](includes/prod_short.md)] hafa bæði þú og þínir notendur heimild til að keyra alla hluti innan leyfisins. Það er enn ekki nóg fyrir úthlutaðan stjórnanda eða notendur með tækjaleyfi, sem geta ekki stofnað verkraðafærslur.

Eftir að verkraðir eru settar upp og í keyrslu getur staðan breyst eins og fylgir hér á eftir innan hvers endurtekins tímabils:

* **Bið**  
* **Tilbúið**  
* **Í vinnslu**  
* **Villa**  
* **Lokið**  

Eftir að verki lýkur með góðum árangri er horfið frá listanum yfir verkraðarafærslur, nema að um endurtekin verk sé að ræða. Fyrir endurteknar vinnslur **er reiturinn fyrsti Upphafstími** leiðréttur til að sýna næst þegar vinnslan er áætluð í keyrslu.  

## <a name="monitor-status-or-errors-in-the-job-queue"></a>Fylgjast með stöðu eða villum í verkröð

Gögn sem vinnsluröðin myndar er geymd í gagnagrunninum, svo hægt sé að leita að villum í vinnslubiðröð.  

Fyrir hverja verkraðarfærslu er hægt að skoða og breyta stöðunni. Við stofnun verkraðarfærslu er staða hennar stillt á **Bið**. T.d. er hægt að setja stöðuna á **Tilbúið** og svo aftur í **Í bið**. Annars eru stöðuupplýsingar uppfærðar sjálfkrafa.

Eftirfarandi tafla lýsir gildum reitsins **Staða**.

| Staða | Lýsing |
|--|--|
| Tilbúið | Verkraðarafærsla er tilbúin til keyrslu. |
| Í vinnslu | Vinnsla raðarafærslu er í vinnslu. Þessi reitur uppfærist á meðan vinnsluröðin er í gangi. |
| Í bið | Sjálfgefin staða verkraðarafærslu þegar hún er stofnuð. Veljið aðgerðina **Stilla stöðu í tilbúið** til að breyta stöðunni í **Tilbúið**. **Veldu settið í halda** aðgerð til að snúa stöðunni í **biðstöðu**. |
| Villa | Eitthvað fór úrskeiðis. Velja **skal sýna villu** til að sýna villuskilaboð. |
| Klárað | Vinnsla raðarfærslu er lokið. |

> [!Tip]  
> Færslur í vinnslubiðröð hætta keyrslu þegar villa kemur upp. Þetta getur til dæmis verið vandamál þegar færsla tengist utanríkisþjónustu, t.d. bankastraumi. Ef þjónustan er tímabundið ekki tiltæk og færslan í vinnslu getur ekki tengst, sýnir færslan villu og hættir keyrslu. Þú verður að endurræsa verkraðarafærslu handvirkt. Hins vegar er **hámark nr. Tilraunir** og endurkeyra (sek.) **svæði geta hjálpað til** við að forðast þetta ástand. **Hámark nr. af Tilraunaborði** er tilgreint hversu oft færslu í vinnslubiðröð getur mistekist áður en hætt er að reyna keyrslu. **Í reitnum endurkeyra (sek.)** er hægt að tilgreina tímafjölda, í sekúndum, á milli tilrauna. Samsetning þessara tveggja reita gæti haldið þeirri færslu í vinnslu áfram þar til utanríkisþjónustan verður tiltæk.

### <a name="to-view-status-for-any-job"></a>Til að skoða stöðu fyrir hvaða verk sem er

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verkraðarfærslur** og velja síðan viðkomandi tengil.
2. Á síðunni **Verkraðarfærslur** skal velja færslu verkraðar og síðan velja aðgerðina **Skráarfærslur**.  

> [!TIP]
> Einnig er hægt að skoða stöðu verkraðarfærslna með því að nota Application Insights í Microsoft Azure fyrir dýpri greiningu sem byggir á fjarmælingum. Frekari upplýsingar er að finna í [Fylgjast með og greina fjarmælingar](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) og [Greining á líftíma fjarmælingarrakningar verkraðar](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace) í [!INCLUDE [prod_short](includes/prod_short.md)] þróunar- og stjórnunarefni.

## <a name="view-scheduled-tasks"></a>Skoða áætluð verk

Síðan **Áætluð verk** í [!INCLUDE [prod_short](includes/prod_short.md)] sýnir hvaða verk eru tilbúin fyrir keyrslu í verkröðinni. Á síðunni má einnig sjá upplýsingar um fyrirtækið sem hvert verk er sett upp til að keyra í. Hins vegar er aðeins hægt að keyra verk sem merkt eru að tilheyri núverandi umhverfi.  

Til dæmis eru allar áætlaðar framkvæmdir stöðvaðar ef fyrirtækið er í umhverfi sem er afrit af öðru umhverfi. Notaðu síðuna **Áætluð verk** til að stilla verk sem tilbúin til keyrslu í verkröðinni.  

> [!NOTE]
> Innri stjórnendur og notendur geta áætlað keyrslu á verkum. Úthlutaðir stjórnendur geta það ekki.

## <a name="the-my-job-queue-part"></a>Hlutinn fyrir Mína verkröð

Í **hlutanum vinnslan Biðtími** í hlutverkamiðstöðinni eru sýndar þær biðraðarfærslur sem byrjað var á en eru ekki tilbúnar. Sjálfgefið er að hlutinn sé ekki birtur en hægt er að bæta honum við hlutverkamiðstöðina. Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md).  

Hlutinn sýnir eftirfarandi upplýsingar:

* Hvaða skjöl með KENNI þínu í **reitnum úthlutað NOTANDAKENNI** eru í vinnslu eða eru í biðröð, þar á meðal skjöl sem eru bókuð í bakgrunni. 
* Hvort Villa hafi verið þegar fylgiskjal var bókað eða í verkraðarafærslu. 

Hluti vinnslubiðraðar leyfir einnig að hætta við bókun skjals.

### <a name="to-view-an-error-from-the-my-job-queue-part"></a>Til að skoða villu ú hlutanum Mín verkröð

1. Í færslu með stöðuna **Villa** skal velja aðgerðina **Sýna villu**.
2. Fara skal yfir villuboðin og leysa vandann.

## <a name="examples-of-what-can-be-scheduled-using-job-queue"></a>Dæmi um það sem hægt er að áætla með því að nota verkröð

### <a name="schedule-reports"></a>Áætla skýrslur

Hægt er að tímasetja skýrslu eða runuvinnslu þannig að hún keyri á tilteknum degi og tíma. Tímasettar skýrslur og runuvinnslur eru færðar inn í verkröð og unnar á áætluðum tíma, eins og önnur verk. Veldu valkostinn **Áætlun** eftir að hafa valið aðgerðina **Senda til** og færðu svo inn upplýsingar á borð við prentara, og tíma og dagsetningu, endurtekningu.  

Frekari upplýsingar eru í [Tímasetja keyrslu skýrslu](ui-work-report.md#ScheduleReport)

### <a name="schedule-synchronization-between-prod_short-and-prod_short"></a>Tímastilla samstillingu á milli [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)]

Ef samþætt [!INCLUDE[prod_short](includes/prod_short.md)][!INCLUDE[prod_short](includes/cds_long_md.md)] hefur verið, gerir vinnsluröðin áætlun þegar samstilla á gögn. Eftir því sem við á um stefnu og reglur sem skilgreindar hafa verið getur verkraðarafærsla stofnað færslur í einu forriti til að stemma af færslur í hinni. Gott dæmi er þegar notandi skráir tengilið inn [!INCLUDE[crm_md](includes/crm_md.md)], hægt er að setja upp verkraðarafærslu sem hefur samband við þig í [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar eru í [Áætla samstillingu milli Business Central og Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md).

### <a name="schedule-the-posting-of-sales-and-purchase-orders"></a>Áætla bókun sölu- og innkaupapantana

Hægt er að nota verkraðarafærslur til að áætla viðskiptaferli sem á að keyra í bakgrunni. Til dæmis eru bakgrunnsverk gagnleg þegar margir notendur bóka sölupantanir á sama tíma, en aðeins er hægt að vinna eina pöntun í einu. Frekari upplýsingar eru í [Að setja upp bókun í bakgrunni með verkraðir](ui-batch-posting.md#to-set-up-background-posting-with-job-queues)

## <a name="monitor-the-job-queue-with-telemetry"></a>Fylgjast með verkröðinni með fjarmælingu

Sem stjórnandi getur þú notað [Application Insights](/azure/azure-monitor/app/app-insights-overview) til að safna saman og greina fjarmælingar sem þú getur notað til að greina vandamál. Frekari upplýsingar er að finna í [Fylgjast með og greina fjarmælingar](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) í þróunar- og stjórnunarefni.  

## <a name="see-also"></a>Sjá einnig

[Stjórnun](admin-setup-and-administration.md)  
[Uppsetning Business Central](setup.md)  
[Grunnstillingum breytt](ui-change-basic-settings.md)  
[Greining á líftíma fjarmælingarrakningar verkraðar](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace)  


[!INCLUDE[footer-include](includes/footer-banner.md)]