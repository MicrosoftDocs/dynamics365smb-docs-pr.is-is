---
title: Gera viðskiptagögn þín virk fyrir Power BI| Microsoft Docs
description: Það er auðvelt að fá innsýn, viðskiptaupplýsingar og afkastavísi (KPI) í Business Central gögnum með Business Central forritunum fyrir Power BI.
author: bmeier90
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 01/13/2020
ms.author: bmeier
ms.openlocfilehash: 1450db26598da2f2735df1979cfacc16034fcf3a
ms.sourcegitcommit: ead69ebe5b29927876a4fb23afb6c066f8854591
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/14/2020
ms.locfileid: "2952988"
---
# <a name="enabling-your-business-data-for-power-bi"></a>Gera viðskiptagögn þín virk fyrir Power BI

Það er auðvelt að fá innsýn í [!INCLUDE[prodshort](includes/prodshort.md)] gögnin þín með [!INCLUDE[prodshort](includes/prodshort.md)] forritum fyrir Power BI. Power BI sækir gögn þín og býr svo til út-fyrir-kassann yfirlit og skýrslur sem byggist á þeim gögnum.  

Notandi verður að vera með gildan reikning hjá [!INCLUDE[prodshort](includes/prodshort.md)] og hjá Power BI. Einnig verður þú að hlaða niður [Power BI Desktop](https://powerbi.microsoft.com/desktop/) ef þú vilt búa til þínar eigin Power BI skýrslur. Power BI forrit þarfnast heimildar í töflur þaðan sem gögn eru sótt úr. Frekari upplýsingar um kröfur er að finna hér að neðan.  

> [!IMPORTANT]
> Power BI forrit sem lýst er í þessari grein eru hannaðir til að nota Azure Active Directory sem sannvottunaraðferð nema annað sé tilgreint. Til að setja upp Power BI-forrit þarftu einnig að hafa Power BI-leyfi fagmanns.  Þegar Power BI-forritið er uppsett er hægt að deila því með öðrum notendum sem eru með hvaða leyfisgerð sem er.

[!INCLUDE [prodlong](includes/prodlong.md)] hefur gefið út eftirfarandi forrit fyrir Power BI:

- [!INCLUDE [prodlong](includes/prodlong.md)] - CRM  
- [!INCLUDE [prodlong](includes/prodlong.md)] - Finance  
- [!INCLUDE [prodlong](includes/prodlong.md)] - Sales  
- [!INCLUDE [prodlong](includes/prodlong.md)](á staðnum) - CRM  
- [!INCLUDE [prodlong](includes/prodlong.md)](á staðnum) - Finance  
- [!INCLUDE [prodlong](includes/prodlong.md)](á staðnum) - Sales  

## <a name="using-the-include-prodshortincludesprodshortmd-dashboards-in-power-bi"></a>Notkun [!INCLUDE [prodshort](includes/prodshort.md)]-yfirlita í Power BI

Hvert forrit býður upp á skýrslur sem þú getur nýtt þér:

- Velja hvaða sjónræna hlutinn á yfirlitinu til að kalla fram einn af sjö undirliggjandi skýrslum.  
- Síða skýrsluna eða bæta við reitum sem eiga að fylgjast með.  
- Festu þetta sérsniðna yfirlit á yfirlitið til að halda áfram rakning á.  
  Hægt er uppfæra gögn handvirkt og þú getur sett upp uppfærsluáætlun. Frekari upplýsingar eru í [Grunnstilla uppfærsluáætlun](/power-bi/refresh-scheduled-refresh).  

Forritin eru hönnuð til að vinna með gögn frá hvaða fyrirtæki sem er sem þú ert með í [!INCLUDE[prodshort](includes/prodshort.md)]. Þegar þú setur upp Power BI-forritið tilgreinir þú eina eða fleiri færibreytur til að tengja við [!INCLUDE [prodshort](includes/prodshort.md)].  

> [!NOTE]
> Einnig er hægt að búa til eigin skýrslur og yfirlit í Power BI á grundvelli þinna [!INCLUDE[d365fin](includes/d365fin_md.md)] gagna. Nánari upplýsingar eru í [Tengja viðskiptagögn þín við Power BI](across-how-use-financials-data-source-powerbi.md), .  

### <a name="to-connect-your-data-in-power-bi"></a>Til að tengja gögnin þín í Power BI

1. Opnaðu vafrann þinn, farðu á https://powerbi.microsoft.com og skráðu þig inn á reikninginn þinn.
2. Velja skal **Sækja gögn** neðst til vinstri á yfirlitssvæðinu.  

    ![Flett um til að sækja gögn](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)

    Einnig er hægt að hefjast handa úr [!INCLUDE [prodshort](includes/prodshort.md)]. Frá heimasíðunni skaltu fara í **Skýrsluval** í hlutanum Power BI. Veldu annað hvort **Þjónusta** eða **Mitt fyrirtæki** frá borðanum. Þegar önnur hvor þessara aðgerða er valin verður farið með þig í annaðhvort gallerí fyrirtækisins í Power BI eða í Microsoft AppSource, sem verður einnig síað til að sýna aðeins forrit sem tengjast [!INCLUDE[prodshort](includes/prodshort.md)].

3. Í **Þjónusta** reitnum er valið **Sækja**. Þetta opnar síðu sem sýnir **AppSource** og **Forrit fyrir Power BI**.  

<!--    ![Choose apps from online services that you use.](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)-->
4. Velja skal **Forrit** í flipanum **Forrit fyrir Power BI** og velja forritið **Microsoft Dynamics 365 Business Central** sem á að nota og svo velja **Sækja núna**.  
<!--    ![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packspowerbi-dynamics365-for-financials-get-it-now.png)/-->
5. Þegar óskað er eftir því skal færa inn heiti fyrirtækisins í [!INCLUDE[prodshort](includes/prodshort.md)] forritið sem þú vilt tengjast við. Ef ekki hafa verið búin til mörg umhverfi skal slá inn **Framleiðsla**. Fyrir færibreytu fyrirtækisins skal ganga úr skugga um að verið sé að slá inn heitið og ekki birtingarnafnið. Þú getur fundið heiti fyrirtækisins á síðunni **Fyrirtæki** í [!INCLUDE[prodshort](includes/prodshort.md)]-tilvikinu þínu.  

    > [!NOTE]
    > Ef þú tengist [!INCLUDE [prodshort](includes/prodshort.md)] á staðnum, verður þú að tilgreina færibreytuna *Vefslóð þjónustu.*. Finndu þetta á síðunni **Vefþjónusta** í [!INCLUDE [prodshort](includes/prodshort.md)]. Skilgreina verður [!INCLUDE [server](includes/server.md)]-tilvikið þitt fyrir grunnvottun og gefa verður upp notanda og vefaðgangslykil hans sem er aðgangsorðið hans. Í eftirfarandi dæmi skaltu skipta út *myserver:7048* fyrir [!INCLUDE [server](includes/server.md)]-heitið þitt og *CRONUS%20US* fyrir heiti fyrirtækisins þíns.  
    > ```https://myserver:7048/BC140/ODataV4/Company('CRONUS%20US')/```

6. Þegar tenging hefur náðst er yfirliti og skýrslum bætt við Power BI-vinnusvæðið þitt. Þegar þessu er lokið sýna reitirnir gögn af [!INCLUDE[prodshort](includes/prodshort.md)] fyrirtækinu þínu.

    ![Veldu Dynamics 365 Business Central og Fá núna](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

### <a name="what-now"></a>Hvað núna?

- Prófaðu [að slá inn spurningu í reitinn Spurningar og svör](/power-bi/service-q-and-a-tips) efst á yfirlitinu.
- [Breyta reitum](/power-bi/service-dashboard-edit-tile) á yfirlitinu.  
- [Velja reit](/power-bi/service-dashboard-tiles) til opna undirliggjandi skýrslu.  
- Sjálfgefið er að gagnasafnið þitt uppfærist ekki sjálfkrafa. Hægt er að breyta uppfærsluáætluninni eða uppfæra hana hvenær sem er í            **Uppfæra núna**. Frekari upplýsingar eru í [Grunnstilla uppfærsluáætlun](/power-bi/refresh-scheduled-refresh).

## <a name="power-bi-in-include-prodshortincludesprodshortmd"></a>Power BI í [!INCLUDE [prodshort](includes/prodshort.md)]

Heimasíðan þín á [!INCLUDE [prodshort](includes/prodshort.md)] getur innihaldið Power BI stjórnunareiningu sem hægt er að grunnstilla svo Power BI-skýrslur birtist á heimasíðunni þinni.

> [!IMPORTANT]
> Notandi verður að vera með gildan reikning hjá [!INCLUDE [prodshort](includes/prodshort.md)] og hjá Power BI. Einnig, ef þú vilt breyta einhverri skýrslu, verður þú að sækja Power BI Desktop. Frekari upplýsingar eru í [Notkun Business Central sem Power BI Gagnagjafi](across-how-use-financials-data-source-powerbi.md).  

### <a name="on-first-login"></a>Við fyrstu innskráningu

Fyrsta skiptið sem þú skráir þig inn á [!INCLUDE [prodshort](includes/prodshort.md)] tekurðu eftir tómum Power BI hluta á heimasíðunni þinni. Til þess að skoða skýrslurnar verðurðu fyrst að tengjast við Power BI með því að velja tengilinn *Hefjast handa með Power BI*.

[!INCLUDE [prodshort](includes/prodshort.md)] hefur síðan samskipti við Power BI-þjónustuna til að komast að því hvort þú sért með gildan Power BI-reikning. Þegar leyfið þitt hefur verið staðfest birtast sjálfgefnu Power BI-skýrslurnar á heimasíðunni þinni.

### <a name="selecting-power-bi-reports"></a>Velja Power BI skýrslur

Stýringin Power BI á heimasíðunni getur birt hvaða Power BI-skýrslu sem er. Til að skoða fyrirliggjandi skýrslu skaltu velja aðgerðina **Velja skýrslu** úr Power BI-fellilistanum yfir skipanir.  

Síða skýrsluvals sýnir lista yfir allar Power BI-skýrslur sem þú hefur aðgang að. Þessi listi er sóttur úr Power BI-vinnusvæðinu þínu. Virkjaðu allar þær skýrslur sem þú vilt birta á heimasíðunni og veldu síðan „Í lagi“. Þú ferð aftur á heimasíðuna og síðasta skýrslan sem þú virkjaðir mun birtast. Í fellilistanum með skipunum skaltu nota skipanirnar „fyrri“ og „næsta“ til að fletta á milli skýrslan.  

### <a name="get-reports"></a>Fá skýrslur

Ef þú sérð engar skýrslur á síðu skýrsluvals eða sérð ekki skýrsluna sem þú hefur áhuga á. Þú getur valið að fá skýrslur frá *Fyrirtækið mitt* eða frá *Þjónustum*.
Veldu *Fyrirtækið mitt* til að fara í Power BI-þjónustuna, en þar þú getur skoðað skýrslurnar innan fyrirtækisins þar sem þú hefur réttindi til skoða þær og bæta þeim við vinnusvæðið þitt. Veldu *Þjónustur* til að fara í Microsoft AppSource þar sem þú getur sett upp Power BI-forrit.  

Einnig er hægt að velja að búa til nýjar Power BI skýrslur. Þegar þessar skýrslur eru gefna út á Power BI-vinnusvæðið þitt, birtast þær á þessari síðu.  

### <a name="managing-reports"></a>Skýrslustjórnun

Í hlutanum Power BI á heimasíðunni þinni geturðu valið aðgerðina **Stjórna skýrslu** úr fellilista yfir skipanir svo að þú getir breytt skýrslunni sem var í skoðun í Mitt hlutverk.  

Hægt er að gera breytingar á skýrslunni og þær vistaðar.  Allar breytingar sem gerðar eru á skýrslunni ná yfir alla notendur sem skýrslunni hefur verið deilt á vegna þess að þú ert að breyta skýrslunni sem vistuð er í Power BI-þjónustunni.  

Þegar þú hefur lokið við breytingarnar skaltu velja Vista. Ef þetta er samnýtt skýrsla viltu mögulega velja Vista sem til að koma í veg fyrir að gera þessa breytingu fyrir alla notendur.
Farðu aftur í Mitt hlutverk og uppfærða skýrslan mun birtast þar. Ef þú notaðir skipunina „Vista sem“ verður þú að opna síðu skýrsluvals og virkja nýju skýrsluna.

### <a name="uploading-reports"></a>Hleður upp skýrslum

Þú getur hlaðið upp nýju Power BI-skýrslunum og deilt þeim með öllum notendum í [!INCLUDE [prodshort](includes/prodshort.md)] þínu. Skýrslunum er deilt innan hvers fyrirtækis í [!INCLUDE [prodshort](includes/prodshort.md)].  

Til að hlaða upp skýrslu skaltu velja aðgerðina **Hlaða upp skýrslu** úr fellilistanum yfir skipanir. Síðan geturðu hlaðið upp .pbix-skrá sem skilgreinir skýrsluna sem þú vilt deila. Þá er hægt að breyta sjálfgefnu skráarinnar.  

Þegar skýrslunni hefur verið hlaðið upp á Power BI-vinnusvæðið þitt hleðst hún sjálfkrafa upp á Power BI-vinnusvæði allra annarra notenda í því fyrirtæki við næstu innskráningu á [!INCLUDE [prodshort](includes/prodshort.md)].

## <a name="system-requirements"></a>Kerfiskröfur

Til að flytja [!INCLUDE[prodshort](includes/prodshort.md)] gögn í Power BI þarf notandi að hafa heimildir á vefþjónustunni til að sækja gögnin. Vefþjónusta sem er áskilin fyrir hvert Power BI-forrit felur í sér:

### <a name="microsoft-dynamics-365-business-central--crm"></a>Microsoft Dynamics 365 Business Central – CRM

- Sölutækifæri
- Upplýsingar um fyrirtæki í yfirliti Excel-sniðmáts
- Power BI Skýrslumerki

### <a name="microsoft-dynamics-365-business-central--finance"></a>Microsoft Dynamics 365 Business Central – Finance

- PowerBIFinance
- Upplýsingar um fyrirtæki í yfirliti Excel-sniðmáts
- Power BI Skýrslumerki

### <a name="microsoft-dynamics-365-business-central---sales"></a>Microsoft Dynamics 365 Business Central - Sales

- Sala vöru eftir viðskiptamönnum
- Stjórnborð sölu
- Skoða fyrirtæki í Excel-sniðmáti
- Power BI Skýrslumerki

> [!NOTE]
> [!INCLUDE [prodshort](includes/prodshort.md)] á staðnum notar sömu endastöðvar vefþjónustu og [!INCLUDE [prodshort](includes/prodshort.md)] á netinu.

## <a name="web-services"></a>Vefþjónusta

Auðveld leið til að finna vefþjónustu er að leita að *vefþjónustu* í [!INCLUDE[prodshort](includes/prodshort.md)]. Á síðunni **Vefþjónusta** skal ganga úr skugga um að reiturinn **Birta** sé valinn fyrir vefþjónustuna sem finna má að ofan.

## <a name="troubleshooting"></a>Úrræðaleit

Power BI yfirlitið byggir á birtum vefþjónustum sem eru hér að ofan skráðar, og það mun sýna gögn sýnifyrirtæki eða eigin fyrirtæki þitt ef þú flytja inn gögn úr núverandi fjárhagslausnum þínum. Hins vegar, ef eitthvað fer úrskeiðis, þessi kafli gefur lausn fyrir dæmigerður vandamál.  

### <a name="you-do-not-have-a-power-bi-account"></a>Þú hefur ekki Power BI reikning.

Power BI reikningur hefur ekki verið settur upp. Til þess að hafa gildan Power BI-reikning verður þú að vera með leyfi og að hafa skráð þig inn í Power BI svo hægt sé að búa til Power BI-vinnusvæðið þitt.  

### <a name="message-there-are-no-enabled-reports-choose-select-report-to-see-a-list-of-reports-that-you-can-display"></a>Skilaboð: Engar skýrslur eru virkar. Veljið Velja skýrslu til að sjá hvaða skýrslur er hægt að birta.

Þessi skilaboð birtast ef sjálfgefna skýrslan tókst ekki að virkja Power BI vinnusvæði þitt eða skýrslan virkjaði en mistókst að uppfæra. Ef þetta gerist skal fara í skýrsluna á Power BI vinnusvæðinu, velja **gagnamengi**, **stillingar** og uppfæra svo skilríkin handvirkt. Þegar gagnamengið hefur verið endurnýjað er farið aftur í Business Central og valið handvirkt skýrsla úr **velja skýrslur** síðunni.

### <a name="you-need-a-power-bi-pro-license-to-install-the-include-prodshortincludesprodshortmd-app-in-power-bi"></a>Þú þarft Power BI-leyfi fagmanns til að setja upp [!INCLUDE [prodshort](includes/prodshort.md)]-forritið í Power BI

Aðeins er hægt að setja upp Power BI-forritin að hálfu notenda sem eru með Power BI-leyfi fagmanns. Þegar Power BI-forritið hefur verið uppsett geturðu deilt því með notendum sem eru ekki með Power BI-leyfi fagmanns.  

### <a name="parameter-validation-failed-please-make-sure-all-parameters-are-valid"></a>„Sannprófun færibreyta tókst ekki, vinsamlegast vertu viss um að allar færibreytur séu gildar“

Þessi villa gefur til kynna að ein eða fleiri færibreytur séu ekki gildar.

- Tilgreind umhverfisfæribreyta samsvarar ekki neinni fyrirliggjandi [!INCLUDE [prodshort](includes/prodshort.md)] -framleiðslu eða sandkassaumhverfi.
- Tilgreind færibreyta fyrirtækis passar ekki við önnur [!INCLUDE [prodshort](includes/prodshort.md)]-fyrirtæki. Staðfestu heiti fyrirtækis á síðunni **Fyrirtæki** í [!INCLUDE [prodshort](includes/prodshort.md)].
- Ef tengst er [!INCLUDE [prodshort](includes/prodshort.md)] á staðnum. þú hefur slegið inn vefslóð sem er ekki gild. Þú getur staðfest vefslóðina á síðunni **Vefþjónusta** í [!INCLUDE [prodshort](includes/prodshort.md)]  
- Gátt er ekki opin til að leyfa beiðni að fara í gegnum eldvegginn.

### <a name="login-failed"></a>Innskráning mistókst

Ef þú færð „innskráning mistókst“ þegar þú skráir þig inn með innskráningarupplýsingum [!INCLUDE [prodshort](includes/prodshort.md)] er það líklega út af einu af eftirfarandi vandamálum:

- Reikningur sem verið er að nota er ekki með heimildir til að sækja [!INCLUDE [prodshort](includes/prodshort.md)] gögnin úr reikningnum þínum. Staðfestu að þú sért með heimildir fyrir nauðsynlegum gögnum í [!INCLUDE [prodshort](includes/prodshort.md)] og reyndu aftur.
- Þú hefur valið aðra sannvottunargerð en grunngerðina ef tengst er við [!INCLUDE [prodshort](includes/prodshort.md)] á staðnum.
- Þú hefur ekki slegið inn gilt notandanafn eða aðgangsorð.

### <a name="incorrect-company-name"></a>Rangt fyrirtækjaheiti

Algeng mistök eru að slá inn birtingarnafn fyrirtækis í stað nafn fyrirtækis. Til að finna nafn fyrirtækisins skal leita að **Fyrirtæki**. Svo skal nota reitinn **Nafn** þegar nafn fyrirtækisins er slegið inn.

### <a name="the-key-didnt-match-any-rows-in-the-table"></a>Lykillinn passaði ekki við neinar línur í töflunni

Ef þú slærð inn ógilt heiti fyrirtækis meðan á tengingarferlinu stendur geturðu fengið villuskilaboðin „Lykillinn passaði ekki við neinar línur í töflunni“. Gefðu upp rétt nafn fyrirtækis og reyndu að tengjast aftur.

### <a name="historical-data-appears-to-be-missing"></a>Eldri gögn virðist vanta

Þegar Power BI-forritið er uppsett og gögnin birtast í Power BI er hugsanlegt að þú sjáir ekki öll gögnin þín. Gagnasöfnin eru síuð til að skila eingöngu gögnum fyrir síðastliðna 365 daga. Þessi sjálfgefna stilling er til staðar til að hraða skýrslunum.  

### <a name="i-only-see-data-for-a-single-company"></a>Ég sé bara gögn fyrir eitt fyrirtæki

Power BI-forritið sýnir aðeins gögn úr [!INCLUDE [prodshort](includes/prodshort.md)] fyrirtækinu sem var skilgreint þegar Power BI-forritið var sett upp. Hægt er að bæta gögnum frá viðbótarfyrirtækjum við skýrslurnar með því að bæta við nýjum fyrirspurnum sem nota mismunandi fyrirtæki sem gagnaveitu.  

## <a name="see-related-training-at-microsoft-learnlearnmodulesconfigure-powerbi-excel-dynamics-365-business-centralindex"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig

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
