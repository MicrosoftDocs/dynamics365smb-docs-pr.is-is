---
title: Stjórnun Microsoft Teams samþættingar við Business Central | Microsoft docs
description: Stjórna samþættingu Business Central við Microsoft Teams.
author: jswymer
ms.topic: overview
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork'
ms.date: 02/03/2023
ms.author: jswymer
ms.reviewer: jswymer
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="managing-microsoft-teams-integration-with-"></a>Að stjórna Microsoft Teams samþættingu við [!INCLUDE [prod_short](includes/prod_short.md)]

[!INCLUDE [online_only](includes/online_only.md)]

Í þessari grein er að finna yfirlit yfir það sem hægt er að gera sem stjórnandi til að stýra Microsoft Teams samþættingu við [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="in-microsoft-teams"></a>Eftir Microsoft Teams

### <a name="minimum-requirements"></a>Lágmarkskröfur

Í þessum hluta er lýst lágmarkskröfum til að eiginleikar [!INCLUDE [prod_short](includes/prod_short.md)]-forritsins virki í Teams.

- Nauðsynleg leyfi

    Forritið [!INCLUDE[prod_short](includes/prod_short.md)] krefst Teams-leyfis í gegnum Microsoft 365 fyrirtækja- eða enterprise-áskrift. Sjálfstæðar Teams-áskriftir eins og Microsoft Teams (ókeypis) eða Microsoft Teams grunnþættir eru ekki studdar.

    Flestir eiginleikar [!INCLUDE[prod_short](includes/prod_short.md)] forritsins fyrir Teams þurfa einnig [!INCLUDE [prod_short](includes/prod_short.md)] leyfi eins og sýnt er í eftirfarandi töflu.

    |Hvað|[!INCLUDE [prod_short](includes/prod_short.md)] leyfi|
    |----|---|
    |Leita að [!INCLUDE [prod_short](includes/prod_short.md)] tengiliðum.|![gátmerki](media/check.png "ávísun")|
    |Límið tengil við [!INCLUDE [prod_short](includes/prod_short.md)]-færslu í samtal og sendið hann sem spjald.|![gátmerki](media/check.png "ávísun")|
    |Deildu tengli frá síðu í [!INCLUDE [prod_short](includes/prod_short.md)] með samtali í Teams.|![gátmerki](media/check.png "ávísun")|
    |Skoðið spjald [!INCLUDE [prod_short](includes/prod_short.md)]-færslu í samtali.||
    |Skoðið frekari upplýsingar um spjald fyrir [!INCLUDE [prod_short](includes/prod_short.md)]-færslu í samtali.|![gátmerki](media/check.png "ávísun")|
    |Opnaðu tengil á síðu í [!INCLUDE [prod_short](includes/prod_short.md)] úr samtali.|![gátmerki](media/check.png "ávísun")|

- Leyfa forskoðanir vefslóða

    Það verður að vera kveikt á reglustillingunni **Leyfa forskoðanir vefslóða**. Annars verður ekki hægt að búa til spjald fyrir [!INCLUDE [prod_short](includes/prod_short.md)]-tengla sem límdir eru í samtal í Teams. Frekari upplýsingar um þessa stillingur er að finna í [Stjórna skilaboðareglum í Teams](/microsoftteams/messaging-policies-in-teams).

### <a name="managing-the--app-optional"></a>Að stjórna [!INCLUDE [prod_short](includes/prod_short.md)]-forritinu (valfrjálst)

Sem stjórnandi í Teams er hægt að stjórna öllum forritum fyrir fyrirtækið, þ.m.t. [!INCLUDE [prod_short](includes/prod_short.md)]-forritinu. Hægt er að samþykkja eða setja upp [!INCLUDE [prod_short](includes/prod_short.md)]-forritið fyrir fyrirtækið þitt, útiloka notanda frá því að setja upp forritið og fleira.

Frekari upplýsingar er að finna í eftirfarandi greinum í fylgiskjölum Microsoft Teams:

- [Stjórna forritunum í Microsoft Teams stjórnendamiðstöðinni](/MicrosoftTeams/manage-apps)
- [Stjórna uppsetningarreglum forrits í Microsoft Teams](/microsoftteams/teams-app-setup-policies)

## <a name="in-"></a>Eftir [!INCLUDE [prod_short](includes/prod_short.md)]

### <a name="minimum-requirements-1"></a>Lágmarkskröfur

- útgáfa [!INCLUDE [prod_short](includes/prod_short.md)]:

    [!INCLUDE [prod_short](includes/prod_short.md)] 2021 útgáfutímabil 1 eða nýrra. Samþætting Teams er aðeins studd fyrir [!INCLUDE [prod_short](includes/prod_short.md)] á netinu; ekki á staðnum.

- Codeunit: **2718 Þjónustuaðili síðusamantektar** er gefin út sem vefþjónusta:

    Þetta codeunit er gefið út sem vefþjónusta að sjálfgefnu. Codeunit er hluti af kerfisforriti [!INCLUDE [prod_short](includes/prod_short.md)]. Það er notað til að sækja reitargögn fyrir [!INCLUDE [prod_short](includes/prod_short.md)]-síðu sem er bætt við samtal í Teams. Upplýsingar um birtingu vefþjónustu er að finna í [Birta vefþjónustu](across-how-publish-web-service.md).

- <a name="permissions"></a>Aðgangsheimildir notanda:

    Að mestu leyti eru leitarsíður tengiliða og gögn sem notendur geta skoðað og breytt í samtali í Teams stjórnað af heimildum þeirra í [!INCLUDE [prod_short](includes/prod_short.md)].

    - Til að leita að tengiliðum verða notendur að hafa að minnsta kosti lesheimild fyrir **Tengiliðir** töfluna. 
    - Til að líma [!INCLUDE [prod_short](includes/prod_short.md)]-tengil í samtal í Teams og fá hann til að stækka í spjald, verða notendur að minnsta kosti að hafa lesheimild á síðunni og gögnum hennar.
    - Þegar spjald er sent inn í samtal, getur hvaða notandi sem er í því samtali skoðað spjaldið án leyfis frá [!INCLUDE [prod_short](includes/prod_short.md)].
    - Til að skoða frekari upplýsingar um spjald eða opna færsluna í [!INCLUDE [prod_short](includes/prod_short.md)], verða notendur að hafa lesheimild á síðunni og gögnum hennar.
    - Til að breyta gögnum þarf notandi að breyta heimildum.
    
    Frekari upplýsingar um heimildir er að finna í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md).

## <a name="installing-the-business-central-app-by-using-centralized-deployment"></a>Setja upp Business Central-forritið með miðlægri innleiðingu

Í Microsoft Teams stjórnendamiðstöðinni eru uppsetningarreglur Teams skilgreindar fyrir fyrirtækið. Í stjórnendamiðstöð Teams getur þú notað eiginleika miðlægrar innleiðingar til að setja sjálfkrafa upp Business Central-forritið í Teams fyrir alla notendur í fyrirtækinu, tilteknum hópum eða einstaka notendum.

> [!NOTE]
> Til að setja upp miðlæga innleiðingu verður Teams-reikningurinn þinn að vera með hlutverkið **Stjórnandi Teams Service** eða **Altækur stjórnandi**.

1. Í Business Central skal velja ![Stækkunargler sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") fara í **Miðlæg innleiðing Teams** og velja síðan viðkomandi tengil. Einnig er hægt að velja [hér](https://businesscentral.dynamics.com/?page=1833) til að opna síðuna beint.
2. Lestu upplýsingarnar í **Setja upp Business Central-forritið fyrir Teams**, veldu síðan **Næsta**.
3. Opnaðu [Stjórnendamiðstöð Teams](https://go.microsoft.com/fwlink/?linkid=2163970) og ljúktu eftirfarandi skrefum.
    1. Farðu í **Forrit Teams** > **Reglur uppsetningar**.
    2. Búðu til nýja reglu eða veldu regluna sem á að nota til að setja upp forrit Business Central, veldu síðan **Bæta við forritum**.
    3. Á síðunni **Bæta við uppsettum forritum** skal leita að og velja **Business Central**.
    4. Veljið **Bæta við**.

       Business Central ætti nú að birtast undir **Uppsett forrit** fyrir regluna.
    5. Grunnstilla fleiri stillingar eftir þörfum og velja **svo Vista**.

    Frekari upplýsingar um reglur uppsetningar í Teams er að finna í [Stjórna uppsetningarreglum forrits í Microsoft Teams](/MicrosoftTeams/teams-app-setup-policies) í fylgigögnum Teams.
4. Farðu aftur í **Teams App Centralized Deployment** í Business Central og veldu **Done**.

> [!IMPORTANT]
> Það getur tekið allt að sólarhring að setja upp reglu uppsetningar fyrir forritið og innleiða forritið hjá notendum.

## <a name="managing-privacy-and-compliance"></a>Umsjón með persónuvernd og reglufylgni

Microsoft Teams býður upp á víðtæka stjórnun fyrir reglufylgni og umsjón með viðkvæmum eða persónugreinanlegum gögnum&mdash;þar á meðal gögnum sem bætt er við spjall og rásir af [!INCLUDE [prod_short](includes/prod_short.md)]-forritinu.

### <a name="understanding-where--cards-are-stored"></a>Að skilja hvar [!INCLUDE [prod_short](includes/prod_short.md)]-spjöld eru geymd

Eftir að kort hefur verið sent á spjall er kortið og reitirnir á kortinu afritaðir í Teams. Þessar upplýsingar heyra undir reglur Teams fyrir fyrirtækið þitt, svo sem reglur um gagnavarðveislu. Þegar upplýsingar spjalds birtast eru engin gögn í uppplýsingaglugganum geymd í Teams. Gögnin eru áfram geymd í [!INCLUDE [prod_short](includes/prod_short.md)] og verða aðeins sótt af Teams þegar notandinn velur að skoða upplýsingarnar. 

- Frekari upplýsingar um hvar Teams geymir þessi gögn er að finna í [Staðsetning gagna í Microsoft Teams](/microsoftteams/location-of-data-in-teams).
- Frekari upplýsingar um varðveislureglur í Teams er að finna í [Varðveislureglur í Microsoft Teams](/microsoftteams/retention-policies).

### <a name="restricting-sharing-of-cards"></a>Takmörkun á deilingu spjalda

Þú kemur í veg fyrir að ákveðnir notendur eða hópar sendi spjöld á spjall eða rásir með því að setja upp reglu um skilaboð sem slekkur á stillingunni **Forskoðun vefslóða**. Frekari upplýsingar um þessa stillingur er að finna í [Stjórna skilaboðareglum í Teams](/microsoftteams/messaging-policies-in-teams). 

Einnig er hægt að nota upplýsingatálma til að koma í veg fyrir að einstaklingar eða hópar séu í samskiptum. Frekari upplýsingar er að finna í [Upplýsingatálmar í Microsoft Teams](/microsoftteams/information-barriers-in-teams).

Eiginleika gagnatapsvarnar í öryggis- og reglufylgnimiðstöð Microsoft 365 er ekki hægt að nota sérstaklega fyrir spjöld. En hægt er að nota þau í spjallskilaboðunum sem innihalda kortin. <!-- To track upcoming advanced features that include enabling DLP for cards, see [https://www.microsoft.com/en-us/microsoft-365/roadmap?featureid=67093](https://www.microsoft.com/en-us/microsoft-365/roadmap?featureid=67093).-->

### <a name="responding-to-data-requests"></a>Bregðast við gagnabeiðnum

Hægt er að leyfa teymismeðlimum og eigendum hópa að eyða skilaboðum sem innihalda viðkvæm spjöld með því að setja upp skilaboðareglur eins og: **Eigendur geta eytt sendum skilaboðum** og **Notendur geta eytt sendum skilaboð**. Frekari upplýsingar er að finna í [Stjórna skilaboðareglum í Teams](/microsoftteams/messaging-policies-in-teams).

Eftirlitseiginleika efnisleitar og eDiscovery í öryggis- og reglufylgnimiðstöð Microsoft 365 er einnig hægt að nota á spjöld.

Þar sem gögn spjalds í Teams er afrit af gögnum í [!INCLUDE [prod_short](includes/prod_short.md)] er einnig hægt að nota [!INCLUDE [prod_short](includes/prod_short.md)]-eiginleika til að flytja út gögn viðskiptamanna ef þess er óskað. Frekari upplýsingar um persónuvernd í [!INCLUDE [prod_short](includes/prod_short.md)] er að finna í [Algengar spurningar um persónuvernd fyrir viðskiptamenn Business Central](/dynamics365/business-central/dev-itpro/security/privacyfaq).

## <a name="show-or-hide-record-data-on-cards"></a>Sýna eða fela færslugögn á spjöldum

Þegar færslu er deilt með öðrum á teymisspjalli eða rás birtist spjald með reitum sem innihalda gögn um færsluna. Allir viðtakendur geta sjálfgefið skoðað þessi gögn (eða færsluyfirlit) óháð leyfi þeirra eða heimildum í Business Central. Ef þú ert stjórnandi getur þú notað leiðsagnarforritið **Card Settings** með hjálp til að fela færsluyfirlitið frá því að birtast á spjöldum í Teymum. Ef færsluyfirlitið er falið fjarlægir það alla reiti og myndir en birtir hnappinn **Upplýsingar og aðrar upplýsingar sem ekki eru skráðar** á spjaldið.

|Færsluyfirlit á|Færsluyfirlit óvirkt|
|-|-|
|![Mynd sem sýnir spjald í Teams þegar kveikt er á færslunni í sumar.](media/card-settings-example-on.png)|![Mynd sem sýnir spjald í Teams þegar slökkt er á færslunni í sumar.](media/card-settings-example-off.png)|

Stillingin er stillt á hvert umhverfi. Þegar færsluyfirlitið er kveikt eða slökkt hefur það áhrif á öll fyrirtæki í umhverfinu.

1. Í Business Central er umhverfið opnað sem á að breyta.

   > [!TIP]
   > Til að skipta um umhverfi er Ctrl <kbd>O</kbd>+<kbd>valið</kbd>.
2.  ![Veldu Stækkunarglerið sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **spjaldstillingar** og velja síðan viðeigandi tengil. <!--Or, select [here](https://businesscentral.dynamics.com/?page=1833) to open the page directly.-->
3. Upplýsingarnar um **spjaldstillingarnar** eru lesnar og Næst **valið þegar það er** tilbúið.
4. Á síðunni **Gagnasýni** skal kveikja á rofanum **Sýna færsluyfirlit** til að birta gögn á spjöldunum eða slökkva á þeim til að fela gögnin.
5. Valið er **Áfram** og leiðbeiningum fylgt til að ljúka leiðsagnarforritinu um uppsetningu.

## <a name="see-also"></a>Sjá einnig

[[!INCLUDE [prod_short](includes/prod_short.md)] og Microsoft Teams samþættingaryfirlit](across-teams-overview.md)  
[Setja upp [!INCLUDE [prod_short](includes/prod_short.md)]-forritið fyrir Microsoft Teams](across-install-app-for-teams.md)  
[Teams - Algengar spurningar](teams-faq.md)  
[Úrræðaleit Teams](admin-teams-troubleshooting.md)  
[Þróun fyrir samþættingu Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
