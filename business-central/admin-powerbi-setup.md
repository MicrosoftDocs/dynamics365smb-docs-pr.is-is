---
title: Virkjun Power BI samþættingar við Business Central
description: Kynntu þér hvernig á að setja upp Power BI. Með Power BI skýrslum geturðu öðlast innsýn, viðskiptaupplýsingar og afkastavísa (KPI) úr Business Central gögnum.
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Power BI, setup, analysis, reporting, financial report, business intelligence, KPI
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: b3eb777c7a495c5b4b73ace26151e53403f81f00
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8521203"
---
# <a name="enabling-power-bi-integration-with-prod_short"></a>Virkjun Power BI samþættingar við [!INCLUDE[prod_short](includes/prod_short.md)]

Þessi grein lýsir því hvernig hægt er að undirbúa [!INCLUDE[prod_short](includes/prod_short.md)] til samþættingar við Power BI. [!INCLUDE[prod_short](includes/prod_short.md)] á netinu er þegar virkt fyrir samþættingu, þó þú kunnir að vilja lesa einhverjar upplýsingar um leyfi. Fyrir [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum er búið að setja upp umhverfi til að tengjast við Power BI áður en notendur geta unnið með það.

## <a name="power-bi-licensing"></a><a name="license"></a>Power BI Leyfisveiting

Með [!INCLUDE[prod_short](includes/prod_short.md)] fá notendur ókeypis Power BI leyfi sem veitir aðgang að algengustu aðgerðunum í [!INCLUDE[prod_short](includes/prod_short.md)] og Power BI. Einnig er hægt að kaupa Power BI Pro-leyfi sem veitir aðgang að viðbótareiginleikum. Eftirfarandi tafla sýnir yfirlit yfir tiltæka eiginleika með hverju leyfi.

|Power-leyfi|Skoða skýrslur|Stofna skýrslur|Deila skýrslum|Uppfæra skýrslur| [!INCLUDE[prod_short](includes/prod_short.md)] Forrit|
|-------------|--------||
|Power BI laus|![hak.](media/check.png)|![annað hak](media/check.png)|(takmarkað)|(takmarkað)||
|Power BI Pro|![enn eitt hakið.](media/check.png)|![þetta er hak](media/check.png)|![aftur hak](media/check.png)|(ítarlegt)|![síðasta hakið](media/check.png)|

Frekari upplýsingar er að finna í [Leyfi fyrir Power BI þjónustunni fyrir notendur í fyrirtækinu](/power-bi/admin/service-admin-licensing-organization) eða [Skráning á þjónustunni Power BI sem einstaklingur](/power-bi/fundamentals/service-self-service-signup-for-power-bi).

## <a name="expose-data-through-api-pages-or-odata-web-services"></a><a name="exposedata"></a>Birta gögn í gegnum API-síður eða OData-vefþjónustur

Business Central býður upp á tvær leiðir til að birta gögn sem Power BI skýrslur geta notað: API-síður og OData-vefþjónustur.

### <a name="api-pages"></a>API-síður

> **GILDIR UM:** Eingöngu Business Central á netinu 

API-síða er sérstök tegund af síðu sem er búin til í AL-kóða sem veitir aðgang að gagnagrunnstöflum í gegnum REST-þjónustu, virkjuð með OData v4, sem byggir á stuðningi veftengingar. Ekki er hægt að birta slíka síðu í notandaviðmótinu, en er ætlað til að setja á stofn áreiðanlegar samþættingarþjónustur.

Business Central á netinu er í boði með safni af innbyggðu API sem hægt er að nota til að sækja gögn fyrir algengustu viðskiptaeiningarnar, eins og viðskiptavini, vörur, sölupantanir og margt fleira. Engin viðbótarvinna eða uppsetning er nauðsynleg til að nota þessi API sem gagnagjafa fyrir Power BI skýrslur. Frekari upplýsingar um þessi API er að finna í [Business Central API V2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/).

Business Central á netinu styður einnig sérsniðin API. Þróunaraðilar Business Central-lausna geta búið til sínar eigin API-síður og pakkað þeim í viðbætur. Þú setur síðan viðaukunum á framfæri við leigjanda. Þegar upp er komin notar þú síður API fyrir Power BI skýrslurnar, eins og þú myndir gera við innbyggðan APIs (v 2.0). Frekari upplýsingar um hvernig á að búa til API-síður er að finna í [Þróun á sérsniðnu API](/dynamics365/business-central/dev-itpro/developer/devenv-develop-custom-api).

> [!IMPORTANT]
> Sem hefst í febrúar 2022, Power BI skýrslur vegna [!INCLUDE[prod_short](includes/prod_short.md)] netverslunar eru úr aukaföllum, lesnir gagnagrunnseftirmynd af sýningarástæðum. Þar af leiðandi ætti AL verktaki að forðast að hanna síður API sem gerir breytingar á gagnagrunni meðan síðurnar eru að opna eða hlaða færslum. Sérstaklega þarf að huga að kóðanum á AL-kveikjum: Onopen, OnOpenPage, Onfindmet, OnNextRecord, OnAfterGetRecord og OnAfterGetCurrRecord. Þessar gagnagrunnsbreytingar geta í sumum tilvikum valdið afkastavandamálum og komið í veg fyrir að skýrslan endurhressigögn. Frekari upplýsingar er að finna [í afkastamikunum greinum í þróunarhjálp fyrir forritara](/dynamics365/business-central/dev-itpro/performance/performance-developer?branch=main#writing-efficient-web-services) í bransanum.
>
> Í einstaka tilfellum orsakar hegðunin villu þegar notandi reynir að fá gögn af API síðu fyrir skýrslu í Power BI Desktop. Ef hins vegar breytingar á gagnagrunni eru nauðsynlegar á síðunni Power BI Desktop sérsniðin API geta notendur þvingað hegðunina. Frekari upplýsingar er að finna [í byggingarskýrslum Power BI til að birta aðalgögn](across-how-use-financials-data-source-powerbi.md#fixing-problems) fyrirtækja.

### <a name="odata-web-services"></a>OData-vefþjónustur

Þú getur birt hugbúnaðarhluti Business Central, eins og kóðaeiningar, síðu og fyrirspurnir, sem [OData-vefþjónustur](/dynamics365/business-central/dev-itpro/webservices/odata-web-services). Með Business Central á netinu eru margar vefþjónustur birtar sjálfkrafa. Auðveld leið til að finna vefþjónustu er að leita að *vefþjónustu* í [!INCLUDE[prod_short](includes/prod_short.md)]. Á síðunni **Vefþjónusta** skal ganga úr skugga um að reiturinn **Birta** sé valinn fyrir vefþjónustuna sem finna má að ofan. Frekari upplýsingar um birtingu vefþjónustu er að finna á [Birta vefþjónustu](across-how-publish-web-service.md).

Til að fræðast um hvað hægt er að gera til að tryggja bestu frammistöðu vefþjónustunnar, eins og hún birtist úr Business Central Server (endastöð) og frá neytanda (viðskiptavini), skal lesa [Skrifa gagnalega vefþjónustu](/dynamics365/business-central/dev-itpro/performance/performance-developer#writing-efficient-web-services).

### <a name="choosing-whether-to-use-api-pages-or-odata-web-services"></a>Velja hvort eigi að nota API-síður eða OData-vefþjónustur

Við hvert tækifæri er mælt með að nota API-síður í stað OData-vefþjónustu. API-síður eru almennt hraðari að hlaða inn gögnum í Power BI skýrslur en OData-vefþjónustur. Auk þess eru þær sveigjanlegri vegna þess að þær gera þér kleift að sækja gögn úr töflureitum sem eru ekki skilgreindir í síðuhlut.

## <a name="set-up-prod_short-on-premises-for-power-bi-integration"></a><a name="setup"></a>Setja upp [!INCLUDE[prod_short](includes/prod_short.md)] innanhúss fyrir Power BI samþættingu

Þessi hluti útskýrir kröfur fyrir [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum til að samþætta við Power BI.

1. Skilgreinið annaðhvort NavUserPassword eða Azure Active Directory-sannvottun fyrir uppsetninguna.

    Power BI samþætting styður ekki Windows-sannvottun.  

2. Virkja OData-vefþjónustu og ODataV4 endastöð .

    OData-vefþjónusta verður að vera virk á [!INCLUDE[server](includes/server.md)], og OData-tengið opnað í eldvegg. Frekari upplýsingar er að finna í [Skilgreining Business Central Server - OData vefþjónustur](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#ODataServices).

    Staðbundni þjónninn verður að vera aðgengilegur á internetinu.

3. Gefa [!INCLUDE[prod_short](includes/prod_short.md)] notendareikninga aðgangslykil vefþjónustu.

    Aðgangslykill vefþjónustu er aðeins nauðsynlegur til að skoða [!INCLUDE[prod_short](includes/prod_short.md)] gögn í Power BI. Hægt er að úthluta aðgangslykli vefþjónustunnar á hvern notendareikning. Eða þess í stað skaltu stofna tiltekinn reikning með aðgangslykli vefþjónustu til notkunar fyrir alla notendur. Frekari upplýsingar eru í [Sannvottun vefþjónustu](/dynamics365/business-central/dev-itpro/webservices/web-services-authentication#generate-a-web-service-access-key).

    <!--
    > [!IMPORTANT]
    > With [!INCLUDE[prod_short](../developer/includes/prod_short.md)] online, the use of access keys (Basic Auth) for web service authentication is [deprecated](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#accesskeys). We recommend that you use OAuth2 instead. For more information, see [Use OAuth to Authorize Business Central Web Services](/dynamics365/business-central/dev-itpro/webservices/authenticate-web-services-using-oauth).-->

4. Búið til forritsskráningu fyrir [!INCLUDE[prod_short](includes/prod_short.md)] í Microsoft Azure.

    Til að skoða Power BI skýrslur sem eru innfelldar á [!INCLUDE[prod_short](includes/prod_short.md)] síður verður forrit að vera skráð fyrir [!INCLUDE[prod_short](includes/prod_short.md)] í Microsoft Azure. Skráð forrit þarf að hafa leyfi fyrir Power BI þjónustunni. Frekari upplýsingar er að finna á [Skráning [!INCLUDE[prod_short](includes/prod_short.md)] innanhúss í Azure AD fyrir samþættingu við aðrar þjónustur](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

    > [!NOTE]
    > Ef virkjun notar NavUserPassword-sannvottun, tengist [!INCLUDE[prod_short](includes/prod_short.md)] sömu Power BI þjónustunni fyrir alla notendur. Þessi þjónustureikningur er tilgreindur sem hluti af skráningu á forritinu. Með Azure AD sannvottun er [!INCLUDE[prod_short](includes/prod_short.md)] tengt við Power BI-þjónustuna sem tengist einstökum notendareikningum.

    <!-- Windows authentication can also be used but you can't get data from BC in Power BI -->
5. Gerið upphaflega tengingu frá Business Central til Power BI.

    Áður en notendur geta notað Power BI í [!INCLUDE[prod_short](includes/prod_short.md)] verður stjórnandi Azure-forrits að veita samþykki fyrir Power BI-þjónustunni.

    Til að koma á fyrstu tengingunni skal opna [!INCLUDE[prod_short](includes/prod_short.md)] og keyra **Hefjast handa með Power BI** úr hlutverkamiðstöðinni. Þessi aðgerð mun leiða þig í gegnum samþykktarferlið og fara yfir Power BI-leyfið þitt. Þegar beðið er um innskráningu skal nota innskráningu með Azure-stjórnendareikningi. Frekari upplýsingar er að finna í [Tengjast við Power BI - aðeins einu sinni](across-working-with-powerbi.md#connect).


## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/Configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig

[Business Central og Power BI](admin-powerbi.md)  
[Power BI Samþættingaríhlutur og hönnunaryfirlit fyrir [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)  
[Power BI fyrir neytendur](/power-bi/consumer/end-user-consumer)  
[„Nýtt útlit“ Power BI þjónustunnar](/power-bi/service-new-look)  
[Stutt leiðbeining: Tengjast við gögn í Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Power BI fylgiskjöl](/power-bi/)  
[Viðskiptaupplýsingar](bi.md)  
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Uppsetning [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Nota [!INCLUDE[prod_short](includes/prod_short.md)] sem Power BI gagnagjafa](across-how-use-financials-data-source-powerbi.md)  
[Nota [!INCLUDE[prod_short](includes/prod_short.md)] sem Power Apps gagnagjafa](across-how-use-financials-data-source-powerapps.md)  
[Notkunar [!INCLUDE[prod_short](includes/prod_short.md)] í Power Automate](across-how-use-financials-data-source-flow.md)  




[!INCLUDE[footer-include](includes/footer-banner.md)]