---
title: Notkun Business Central Apps í Power BI| Microsoft docs
description: Það er auðvelt að fá innsýn, viðskiptaupplýsingar og afkastavísi (KPI) í Business Central gögnum með Business Central forritunum fyrir Power BI.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: b4430118eb8075ceded16bdc375479e61a132f96
ms.sourcegitcommit: aeaa0dc64e54432a70c4b0e1faf325cd17d01389
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/17/2020
ms.locfileid: "3697769"
---
# <a name="using-the-prodshort-apps-in-power-bi"></a>Með [!INCLUDE [prodshort](includes/prodshort.md)]-forritunum í Power BI

> **Á VIÐ:** [!INCLUDE [prodlong](includes/prodlong.md)] á netinu 

[!INCLUDE [prodlong](includes/prodlong.md)] gefur út eftirfarandi Power BI-forrit, sem bjóða upp á ítarleg mælaborð til að skoða gögn:

- [!INCLUDE [prodlong](includes/prodlong.md)] - CRM  
- [!INCLUDE [prodlong](includes/prodlong.md)] - Finance  
- [!INCLUDE [prodlong](includes/prodlong.md)] - Sales

## <a name="overview"></a>Yfirlit

Í hverju forriti eru nokkrar skýrslur sem hægt er að skoða nánar, þar á meðal eftirfarandi eiginleika:

- Velja hvaða sjónræna hlutinn á yfirlitinu til að kalla fram einn af sjö undirliggjandi skýrslum.  
- Síða skýrsluna eða bæta við reitum sem eiga að fylgjast með.  
- Festu þetta sérsniðna yfirlit á yfirlitið til að halda áfram rakningu.  
  Hægt er uppfæra gögn handvirkt og þú getur sett upp uppfærsluáætlun. Frekari upplýsingar eru í [Grunnstilla uppfærsluáætlun](/power-bi/refresh-scheduled-refresh).  

Forritin eru hönnuð til að vinna með gögn frá hvaða fyrirtæki sem er í [!INCLUDE[prodshort](includes/prodshort.md)]. Þegar þú setur upp Power BI-forritið tilgreinir þú eina eða fleiri færibreytur til að tengja við [!INCLUDE [prodshort](includes/prodshort.md)].  

> [!NOTE]
> Einnig er hægt að búa til eigin skýrslur og yfirlit í Power BI á grundvelli þinna [!INCLUDE[prodshort](includes/prodshort.md)] gagna. Nánari upplýsingar eru í [Tengja viðskiptagögn þín við Power BI](across-how-use-financials-data-source-powerbi.md), . 

## <a name="prerequisites"></a>Frumskilyrði

Power BI forrit þarfnast heimildar í töflur þaðan sem gögn eru sótt úr og vefþjónustuna sem er notuð til að sækja gögnin. Eftirfarandi tafla sýnir vefþjónustuna sem er áskilin fyrir hvert Power BI-forrit:
    
|Forrit | Vefþjónustur|
|----|-------------|
|[!INCLUDE[prodshort](includes/prodshort.md)] - TENGSLASTJÓRNUN| <ul><li>Sölutækifæri</li><li>Upplýsingar um fyrirtæki í yfirliti Excel-sniðmáts</li><li>Power BI Skýrslumerki</li></ul>|
|[!INCLUDE[prodshort](includes/prodshort.md)] – Finance| <ul><li>PowerBIFinance</li><li>Upplýsingar um fyrirtæki í yfirliti Excel-sniðmáts</li><li>Power BI Skýrslumerki</li></ul>|
|[!INCLUDE[prodshort](includes/prodshort.md)] – Sales| <ul><li>Sala vöru eftir viðskiptamönnum</li><li>Stjórnborð sölu</li><li>Upplýsingar um fyrirtæki í yfirliti Excel-sniðmáts</li><li>Power BI Skýrslumerki</li></ul>|

> [!TIP]
> Auðveld leið til að finna vefþjónustu er að leita að *vefþjónustu* í [!INCLUDE[prodshort](includes/prodshort.md)]. Á síðunni **Vefþjónusta** skal ganga úr skugga um að reiturinn **Birta** sé valinn fyrir vefþjónustuna sem finna má að ofan. Frekari upplýsingar er að finna í [Birta vefþjónustu](across-how-publish-web-service.md).

## <a name="get-ready"></a>Vertu með allt á tæru

Skráðu þig fyrir nýju Power BI þjónustuna. Ef þú hefur ekki þegar skráð þig skaltu fara á [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Þegar þú skráir þig skaltu nota vinnunetfang og aðgangsorð.

## <a name="install-a-prodshort-app-in-power-bi"></a>Setja upp [!INCLUDE[prodshort](includes/prodshort.md)]-forrit í Power BI

1. Opnaðu vafrann þinn, farðu á [https://powerbi.microsoft.com](https://powerbi.microsoft.com) og skráðu þig inn á reikninginn þinn.
2. Velja skal **Sækja gögn** neðst til vinstri á yfirlitssvæðinu.  

    ![Flett um til að sækja gögn](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)

    Einnig er hægt að hefjast handa úr [!INCLUDE [prodshort](includes/prodshort.md)]. Frá heimasíðunni skaltu fara í **Skýrsluval** í hlutanum Power BI. Veldu annað hvort **Þjónusta** eða **Mitt fyrirtæki** frá borðanum. Annaðhvort opnast Fyrirtækjagalleríið í Power BI eða Microsoft AppSource, afmarkað til að sýna aðeins forrit sem tengjast [!INCLUDE[prodshort](includes/prodshort.md)].

3. Í **Þjónusta** reitnum er valið **Sækja**.

    Í þessu skrefi opnast **Power BI Forrit** Page, sem gerir þér kleift að fletta upp Power BI forriti sem er í boði í **AppSource .**  

4. Í kassanum **Leit** skal færa inn **Dynamics 365 Business Central**.
5. Veldu forrit sem þú vilt nota, veldu **Sækja það núna** og svo **Setja upp**.  

    Þegar því er lokið verður forritið í boði af yfirlitsvalmyndinni **Forrit** í Power BI.

## <a name="connect-the-prodshort-app-to-your-data"></a>Tengdu [!INCLUDE[prodshort](includes/prodshort.md)]-forritið við gögnin þín

1. Í **Forrit** skal velja Business Central-forritið og síðan **Tengja**.
2. Þegar beðið er um það skal fylla út **Heiti fyrirtækis** og **Umhverfi** með upplýsingum um [!INCLUDE[prodshort](includes/prodshort.md)] tilvik sem á að tengjast við.

    - Fyrir **Heiti fyrirtækis** skal nota fullt heiti, ekki birtingarheiti. Þú getur fundið heiti fyrirtækisins á síðunni **Fyrirtæki** í [!INCLUDE[prodshort](includes/prodshort.md)]. 
    - Fyrir **Umhverfi**, ef þú hefur ekki búið til mörg umhverfi, skaltu færa inn **Framleiðsla**.

3. Veldu **Áfram**.
4. Veldu **Innskráning**.
5. Þegar beðið er um það skal færa inn notandanafn og aðgangsorð fyrir innskráningu í [!INCLUDE[prodshort](includes/prodshort.md)].
6. Þegar tenging hefur náðst er yfirliti og skýrslum bætt við Power BI-vinnusvæðið þitt. Þegar þessu er lokið sýna reitirnir gögn af [!INCLUDE[prodshort](includes/prodshort.md)] fyrirtækinu þínu.

    ![Veldu Dynamics 365 Business Central og Fá núna](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

## <a name="fixing-problems"></a>Vandamál lagfærð

Power BI yfirlitið reiðir sig á birtar vefþjónustur sem eru í listanum hér að ofan. Hún sýnir gögn sýnifyrirtækis eða eigin fyrirtækis ef þú flytur inn gögn úr núverandi fjárhagslausnum þínum. Hins vegar, ef eitthvað fer úrskeiðis, þessi kafli gefur lausn fyrir dæmigerður vandamál.  

### <a name="you-dont-have-a-power-bi-account"></a>Þú ert ekki með Power BI reikning

Power BI-Reikningur hefur ekki verið settur upp. Þú verður að hafa leyfi til að fá gildan Power BI-reikning. Einnig þarftu að hafa skráð þig inn áður á Power BI til að stofna Power BI vinnusvæði.  

### <a name="message-there-are-no-enabled-reports-choose-select-report-to-see-a-list-of-reports-that-you-can-display"></a>Skilaboð: Engar skýrslur eru virkar. Veljið Velja skýrslu til að sjá hvaða skýrslur er hægt að birta.

Þessi skilaboð birtast ef ekki tókst að virkja sjálfgefna skýrslu á Power BI vinnusvæði. Eða að skýrslan var virkjuð en ekki tókst að uppfæra hana. Ef þetta vandamál kemur upp skal fara í skýrsluna á Power BI vinnusvæðinu, velja **Gagnasafn**, **Stillingar** og uppfæra svo skilríkin handvirkt. Þegar gagnasafnið hefur verið endurnýjað er farið aftur í [!INCLUDE[prodshort](includes/prodshort.md)] og valið skýrslu handvirkt af **Velja skýrslur** síðunni.

### <a name="you-need-a-power-bi-pro-license-to-install-the-prodshort-app-in-power-bi"></a>Þú þarft Power BI-leyfi fagmanns til að setja upp [!INCLUDE[prodshort](includes/prodshort.md)]-forritið í Power BI

Þú þarft [Power BI Pro leyfi](/power-bi/service-features-license-type) til að deila efninu þínu og einnig fólkið sem þú deilir því með. Efnið verður að vera á vinnusvæði með [Premium réttindi](/power-bi/service-premium-what-is). Nánari upplýsingar eru í [Aðferðir við að deila vinnu þinn í Power BI](/power-bi/service-how-to-collaborate-distribute-dashboards-reports).  

### <a name="parameter-validation-failed-please-make-sure-all-parameters-are-valid"></a>„Sannprófun færibreyta tókst ekki, vinsamlegast vertu viss um að allar færibreytur séu gildar“

Þessi villa gefur til kynna að ein færibreyta til viðbótar sé ekki gild.

- Tilgreind umhverfisfæribreyta samsvarar ekki neinu fyrirliggjandi [!INCLUDE[prodshort](includes/prodshort.md)] -framleiðslu eða sandkassaumhverfi.
- Tilgreind færibreyta fyrirtækis passar ekki við önnur [!INCLUDE[prodshort](includes/prodshort.md)]-fyrirtæki. Staðfestu heiti fyrirtækis á síðunni **Fyrirtæki** í [!INCLUDE[prodshort](includes/prodshort.md)].
- Ef tengst er við [!INCLUDE[prodshort](includes/prodshort.md)] á staðnum var ógild vefslóð slegin inn. Þú getur staðfest vefslóðina á síðunni **Vefþjónusta** í [!INCLUDE[prodshort](includes/prodshort.md)]  
- Tengi er ekki opið til að leyfa beiðni í gegnum eldvegginn.

### <a name="cant-sign-in"></a>Innskráning tókst ekki

Ef þú færð „innskráning mistókst“ þegar þú skráir þig inn með [!INCLUDE[prodshort](includes/prodshort.md)] notandaskilríkjum er það líklega út af einu af eftirfarandi vandamálum:

- Reikningur sem verið er að nota er ekki með heimild til að sækja [!INCLUDE[prodshort](includes/prodshort.md)] gögnin af reikningnum þínum. Staðfestu að þú sért með heimildir fyrir nauðsynlegum gögnum í [!INCLUDE[prodshort](includes/prodshort.md)] og reyndu aftur.
- Þú hefur valið aðra sannvottunargerð en grunngerðina ef tengst er við [!INCLUDE[prodshort](includes/prodshort.md)] á staðnum.
- Þú hefur ekki slegið inn gilt notandanafn eða aðgangsorð.

### <a name="message-your-data-source-cant-be-refreshed-because-the-credentials-are-invalid-please-update-your-credentials-and-try-again"></a>Skilaboð: ekki er hægt að endurnýja gagnagjafa vegna þess að skilríkin eru ógild. Uppfærðu heimildirnar þínar og reyndu aftur

Fyrir [!INCLUDE[prodshort](includes/prodshort.md)] á staðnum kann vandamálið að vera vegna þess að vefslóðin að OData hafi aðeins orðið til á staðbundnu neti.

### <a name="incorrect-company-name"></a>Rangt fyrirtækjaheiti

Algeng mistök eru að slá inn birtingarnafn fyrirtækis í stað nafn fyrirtækis. Til að finna nafn fyrirtækisins skal leita að **Fyrirtæki**. Svo skal nota reitinn **Nafn** þegar nafn fyrirtækisins er slegið inn.

### <a name="the-key-didnt-match-any-rows-in-the-table"></a>Lykillinn passaði ekki við neinar línur í töflunni

Ef þú slærð inn ógilt heiti fyrirtækis meðan á tengingarferlinu stendur geturðu fengið villuskilaboðin „Lykillinn passaði ekki við neinar línur í töflunni“. Gefðu upp rétt nafn fyrirtækis og reyndu að tengjast aftur.

### <a name="historical-data-appears-to-be-missing"></a>Eldri gögn virðist vanta

Þegar Power BI-forritið er uppsett og gögnin birtast í Power BI er hugsanlegt að þú sjáir ekki öll gögnin þín. Gagnasöfnin eru síuð til að skila eingöngu gögnum fyrir síðastliðna 365 daga. Þessi sjálfgefna stilling er til staðar til að hraða skýrslunum.  

### <a name="i-only-see-data-for-a-single-company"></a>Ég sé bara gögn fyrir eitt fyrirtæki

Power BI-forritið sýnir aðeins gögn úr [!INCLUDE[prodshort](includes/prodshort.md)] fyrirtækinu sem var skilgreint þegar Power BI-forritið var sett upp. Hægt er að bæta gögnum frá viðbótarfyrirtækjum við skýrslurnar með því að bæta við nýjum fyrirspurnum sem nota mismunandi fyrirtæki sem gagnaveitu.  

### <a name="what-now"></a>Hvað núna?

- Prófaðu [að slá inn spurningu í reitinn Spurningar og svör](/power-bi/service-q-and-a-tips) efst á yfirlitinu.
- [Breyta reitum](/power-bi/service-dashboard-edit-tile) á yfirlitinu.  
- [Velja reit](/power-bi/service-dashboard-tiles) til opna undirliggjandi skýrslu.  
- Sjálfgefið er að gagnasafnið sé ekki áætlað til endurnýjunar. Hægt er að breyta uppfærsluáætluninni eða uppfæra hana hvenær sem er í **Uppfæra núna**. Frekari upplýsingar eru í [Grunnstilla uppfærsluáætlun](/power-bi/refresh-scheduled-refresh).

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig

[Business Central og Power BI](admin-powerbi.md)  
[Power BI Samþættingaríhlutur og hönnunaryfirlit fyrir [!INCLUDE[prodshort](includes/prodshort.md)]](admin-powerbi-overview.md)  
[Unnið með [!INCLUDE [prodshort](includes/prodshort.md)] gögn í Power BI](across-working-with-business-central-in-powerbi.md)  
[Búa til Power BI skýrslur til að birta [!INCLUDE [prodlong](includes/prodlong.md)]-gögn](across-how-use-financials-data-source-powerbi.md)  
[Power BI fyrir neytendur](/power-bi/consumer/end-user-consumer)  
[„Nýtt útlit“ Power BI þjónustunnar](/power-bi/service-new-look)  
[Stutt leiðbeining: Tengjast við gögn í Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Power BI fylgiskjöl](/power-bi/)  
[Viðskiptaupplýsingar](bi.md)  
[Hafist handa](product-get-started.md)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Nota [!INCLUDE[d365fin](includes/d365fin_md.md)] sem Power BI gagnaveitu](across-how-use-financials-data-source-powerbi.md)  
[Nota [!INCLUDE[d365fin](includes/d365fin_md.md)] sem Power Apps gagnaveitu](across-how-use-financials-data-source-powerapps.md)  
[Nota [!INCLUDE[d365fin](includes/d365fin_md.md)] í Power Automate](across-how-use-financials-data-source-flow.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  