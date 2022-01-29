---
title: Tímasetja verk til að keyrast sjálfvirkt
description: Tímasettum verkum er stjórnað af verkröðinni. Þessi verk keyra skýrslur og kóðaeiningar. Stilla má verk svo þau keyri einu sinni eða endurtekið.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 672, 673, 674, 671
ms.date: 10/01/2021
ms.author: edupont
ms.openlocfilehash: 46759304a312e0376e8b309b29d5e0491b34a69f
ms.sourcegitcommit: 8464b37c4f1e5819aed81d9cfdc382fc3d0762fc
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/19/2022
ms.locfileid: "8012236"
---
# <a name="use-job-queues-to-schedule-tasks"></a>Nota verkraðir til að tímaraða verkhlutum

Verkraðir í [!INCLUDE[prod_short](includes/prod_short.md)] gera notendum kleift að tímasetja og keyra tilteknar skýrslur og kótasöfn. Stilla má verk svo þau keyri einu sinni eða endurtekið. Til dæmis kann notandi að vilja keyra skýrslu yfir **Sölutölur sölumanns** vikulega, að rekja sölu sölumanns í hverri viku eða keyra kóðaeininguna **Framselja samþykktarbeiðnir** daglega, til að tryggja að skjöl safnist saman eða stífli verkflæðið á annan hátt.

Síðan **Verkraðarfærslur** birtir öll núverandi verk. Ef bætt er inn nýrri verkraðarfærslu sem á að tímasetja, er nauðsynlegt að tiltaka upplýsingar um tegund hlutarins sem þú vilt keyra, eins og t.d. skýrsla eða kóðasafn, og heiti og hlutkenni hlutarins sem keyra á. Einnig er hægt að bæta færibreytum við til að tilgreina virkni verkraðarfærslu. Til dæmis er hægt að bæta við færibreytu til að sent einungis bókaðar sölupantanir. Notandi verður að hafa heimild til að keyra skýrsluna eða kótasafnið; annars kemur upp villa þegar verkröðin er keyrð.  
> [!IMPORTANT]  
> Ef notað er SUPER-heimildasafnið sem fylgir með [!INCLUDE[prod_short](includes/prod_short.md)] hafa bæði þú og þínir notendur heimild til að keyra alla hluti innan leyfisins. Það er enn ekki nóg fyrir úthlutaðan stjórnanda eða notendur með tækjaleyfi, sem geta ekki stofnað verkraðafærslur.

Verkröðin getur haft margar færslur sem eru þau verk sem biðröð stjórnar og keyrir. Upplýsingar í færslunni tilgreina hvaða kótaeining eða skýrsla er keyrð, hvenær og hve oft færslan er keyrð, í hvaða flokki verkið er keyrt og hvernig það er keyrt.  

Eftir að verkraðir eru settar upp og í keyrslu getur staðan breyst eins og fylgir hér á eftir innan hvers endurtekins tímabils:

* **Bið**  
* **Tilbúið**  
* **Í vinnslu**  
* **Villa**  
* **Lokið**  

Þegar verki lýkur er það fjarlægt af lista yfir færslur verkraðar nema það sé endurtekið verk. Ef um endurtekið verk er að ræða er reiturinn **Fyrsti upphafstími** stilltur til að sýna næsta áætlaða keyrslutíma verksins.  

## <a name="monitor-status-or-errors-in-the-job-queue"></a>Fylgjast með stöðu eða villum í verkröð

Gögn sem verða til þegar verkröð er keyrð eru geymd í gagnagrunninum svo hægt sé að úrræðaleita villur verkraðar.  

Fyrir hverja verkraðarfærslu er hægt að skoða og breyta stöðunni. Við stofnun verkraðarfærslu er staða hennar stillt á **Bið**. T.d. er hægt að setja stöðuna á **Tilbúið** og svo aftur í **Í bið**. Annars eru stöðuupplýsingar uppfærðar sjálfkrafa.

Eftirfarandi tafla lýsir gildum reitsins **Staða**.

| Staða | Description |
|--|--|
| Tilbúið | Gefur til kynna að verkraðarfærslan er tilbúin til keyrslu. |
| Í vinnslu | Gefur til kynna að verkraðarfærslan er í vinnslu. Þessi reitur er uppfærður meðan verkröðin er í gangi. |
| Bið | Sjálfgildi. Tilgreinir stöðu verkraðarfærslu þegar hún er stofnuð. Veljið aðgerðina **Stilla stöðu í tilbúið** til að breyta stöðunni í **Tilbúið**. Veljið aðgerðina **Setja í bið** eða **Fresta** til að breyta stöðunni aftur í **Í bið**. |
| Villa | Gefur til kynna að villa hafi komið upp. Velja **Sýna villuboð** til að sjá villuboðin. |
| Lokið | Gefur til kynna að verkraðarfærslunni er lokið. |

### <a name="to-view-status-for-any-job"></a>Til að skoða stöðu fyrir hvaða verk sem er

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verkraðarfærslur** og velja síðan viðkomandi tengil.
2. Á síðunni **Verkraðarfærslur** skal velja færslu verkraðar og síðan velja aðgerðina **Skráarfærslur**.  

> [!TIP]
> Einnig er hægt að skoða stöðu verkraðarfærslna með því að nota Application Insights í Microsoft Azure fyrir dýpri greiningu sem byggir á fjarmælingum. Frekari upplýsingar er að finna í [Fylgjast með og greina fjarmælingar](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) og [Greining á líftíma fjarmælingarrakningar verkraðar](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace) í [!INCLUDE [prod_short](includes/prod_short.md)] þróunar- og stjórnunarefni.

## <a name="view-scheduled-tasks"></a>Skoða áætluð verk

Síðan **Áætluð verk** í [!INCLUDE [prod_short](includes/prod_short.md)] sýnir hvaða verk eru tilbúin fyrir keyrslu í verkröðinni. Á síðunni má einnig sjá upplýsingar um fyrirtækið sem hvert verk er sett upp til að keyra í. Hins vegar er aðeins hægt að keyra verk sem merkt eru að tilheyri núverandi umhverfi.  

Ef núverandi fyrirtæki er til að mynda í umhverfi sem er afrit af öðru umhverfi verða öll tímasett verk sjálfkrafa stöðvuð. Notaðu síðuna **Áætluð verk** til að stilla verk sem tilbúin til keyrslu í verkröðinni.  

> [!NOTE]
> Innri stjórnendur og notendur geta áætlað keyrslu á verkum. Úthlutaðir stjórnendur geta það ekki.

## <a name="the-my-job-queue-part"></a>Hlutinn fyrir Mína verkröð

Hlutinn **Mín verkröð** í hlutverkamiðstöðinni þinni sýnir færslur verkraða sem þú hefur byrjað á, en er enn ekki lokið. Að sjálfgefnu er hlutinn ekki sjáanlegur, þannig að þú veður að bæta honum inn í Hlutverkamiðstöðina þína. Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md).  

Sá hluti sýnir hvaða skjöl með auðkenni þitt í reitnum **Úthlutuð notandakenni** er verið að vinna úr eða eru í röð, þ.á.m. þau sem tengjast bakgrunnsbókun. Hlutinn gefur til kynna á svipstundu hvort um villu hafi verið að ræða við bókun skjals eða hvort það hafi verið villur í verkraðarfærslu. Hlutinn býður einnig upp á að hætta við bókun skjals ef hún er ekki í gangi.

### <a name="to-view-an-error-from-the-my-job-queue-part"></a>Til að skoða villu ú hlutanum Mín verkröð

1. Í færslu með stöðuna **Villa** skal velja aðgerðina **Sýna villu**.
2. Fara skal yfir villuboðin og leysa vandann.

## <a name="examples-of-what-can-be-scheduled-using-job-queue"></a>Dæmi um það sem hægt er að áætla með því að nota verkröð

### <a name="schedule-reports"></a>Áætla skýrslur

Hægt er að tímasetja skýrslu eða runuvinnslu þannig að hún keyri á tilteknum degi og tíma. Tímasettar skýrslur og runuvinnslur eru færðar inn í verkröð og unnar á áætluðum tíma, eins og önnur verk. Veldu valkostinn **Áætlun** eftir að hafa valið aðgerðina **Senda til** og færðu svo inn upplýsingar á borð við prentara, og tíma og dagsetningu, endurtekningu.  

Frekari upplýsingar eru í [Tímasetja keyrslu skýrslu](ui-work-report.md#ScheduleReport)

### <a name="schedule-synchronization-between-prod_short-and-prod_short"></a>Tímastilla samstillingu á milli [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)]

Ef þú hefur samþætt [!INCLUDE[prod_short](includes/prod_short.md)] við [!INCLUDE[prod_short](includes/cds_long_md.md)] geturðu notað verkröðina til að tímasetja hvenær þú vilt samstilla gögn fyrir færslurnar sem þú ert með í viðskiptaforritunum tveimur. Samstillingarvinnslur geta einnig búið til nýjar færslur í áfangaforritinu til að passa við þær sem eru í upprunanum, allt eftir stefnu og reglum sem þú hefur skilgreint fyrir samþættingu. Ef Sölumaður stofnar til dæmis nýjan tengilið í [!INCLUDE[crm_md](includes/crm_md.md)] getur samstillingarvinnslan búið til þann tengilið fyrir tengdan sölumann í [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar eru í [Áætla samstillingu milli Business Central og Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md).

### <a name="schedule-the-posting-of-sales-and-purchase-orders"></a>Áætla bókun sölu- og innkaupapantana

Verkraðir eru áhrifaríkt verkfæri til að raða keyrslu viðskiptaferla í bakgrunni, t.d. þegar margir notendur reyna að bóka sölupantanir, en aðeins er hægt að vinna úr einni pöntun í einu.  

Frekari upplýsingar eru í [Að setja upp bókun í bakgrunni með verkraðir](ui-batch-posting.md#to-set-up-background-posting-with-job-queues)

## <a name="monitor-the-job-queue-with-telemetry"></a>Fylgjast með verkröðinni með fjarmælingu

Sem stjórnandi getur þú notað [Application Insights](/azure/azure-monitor/app/app-insights-overview) til að safna saman og greina fjarmælingar sem þú getur notað til að greina vandamál. Frekari upplýsingar er að finna í [Fylgjast með og greina fjarmælingar](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) í þróunar- og stjórnunarefni.  

## <a name="see-also"></a>Sjá einnig

[Stjórnun](admin-setup-and-administration.md)  
[Uppsetning Business Central](setup.md)  
[Grunnstillingum breytt](ui-change-basic-settings.md)  
[Greining á líftíma fjarmælingarrakningar verkraðar](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace)  


[!INCLUDE[footer-include](includes/footer-banner.md)]