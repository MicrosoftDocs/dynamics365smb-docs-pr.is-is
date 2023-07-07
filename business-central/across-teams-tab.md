---
title: Bæta við flipa Business Central í Microsoft Teams
description: Kynntu þér hvernig á að bæta við flipum í Teams sem sýna síður Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 11/04/2022
ms.custom: bap-template
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, share records, tab'
---

# <a name="add-business-central-tab-in-microsoft-teams"></a>Bæta við flipa Business Central í Microsoft Teams

[!INCLUDE [online_only](includes/online_only.md)]

Í Teams birtast flipar efst í rásum og spjalli, sem veitir þátttakendum fljótlegt aðgengi að viðeigandi upplýsingum. Þessi grein útskýrir mismunandi leiðir til að bæta við flipa sem sýnir [!INCLUDE [prod_short](includes/prod_short.md)] gögn.

![Flipar í Teams](media/teams-tabs-border.png)

## <a name="about-business-central-tabs"></a>Um Business Central-flipa

[!INCLUDE [prod_short](includes/prod_short.md)] flipi gefur ítarlegt yfirlit yfir síður [!INCLUDE [prod_short](includes/prod_short.md)] lista og spjalda. Flipinn sýnir ekki allan [!INCLUDE [prod_short](includes/prod_short.md)] vefbiðlarann. Engin vafragluggi, [!INCLUDE [prod_short](includes/prod_short.md)] borði (til dæmis með viðmótsleit, leit, hjálp) eða yfirlitsvalmynd efst&mdash;aðeins efni síðu og aðgerðir hennar. Efnið er gagnvirkt sem þýðir að hægt er að velja aðgerðir og tengla, breyta gögnum og fleira. Þú takmarkast við það sem þú sérð og getur gert með sömu heimildinni og er úthlutað á reikninginn þinn í [!INCLUDE [prod_short](includes/prod_short.md)].

Frekari upplýsingar um hverjir geta skoðað efnið í [!INCLUDE [prod_short](includes/prod_short.md)] flipa er að finna í [Hver getur séð efni í flipa?](/dynamics365/business-central/teams-faq?tabs=tabs#who-can-view).

> [!TIP]
> Ert þú þróunaraðili? Einnig er hægt að forrita inn nýja flipa með Microsoft Graph API. Frekari upplýsingar er að finna í [Bæta við Business Central-flipum í Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams-tabs).  

## <a name="prerequisites"></a>Frumskilyrði

Til að bæta við [!INCLUDE [prod_short](includes/prod_short.md)] flipa þarf að uppfylla eftirfarandi kröfur:

- Þú hefur aðgang að Microsoft Teams.
- Þú ert með [!INCLUDE [prod_short](includes/prod_short.md)] leyfi.
- Þú hefur sett upp [!INCLUDE [prod_short](includes/prod_short.md)]-forritið  í Teams. Frekari upplýsingar er að finna í [Setja upp [!INCLUDE [prod_short](includes/prod_short.md)]-forritið fyrir Microsoft Teams](across-install-app-for-teams.md).

Til að skoða [!INCLUDE [prod_short](includes/prod_short.md)] flipa sem bætt var við af öðrum þátttakanda í rásinni eða spjallinu þarf að uppfylla eftirfarandi kröfur:

- Þú hefur aðgang að Microsoft Teams.
- Þú ert með [!INCLUDE [prod_short](includes/prod_short.md)] leyfi eða takmarkaðan aðgang að Business Central með eingöngu Microsoft 365 leyfi. Frekari upplýsingar er að finna í [Aðgangur að Business Central með Microsoft 365 leyfum](admin-access-with-m365-license.md).
- Þú hefur sett upp [!INCLUDE [prod_short](includes/prod_short.md)]-forritið  í Teams.

## <a name="add-tab-using-recommended-content"></a>Bæta við flipa með því að nota ráðlagt efni

Notaðu þessi skref til að bæta við flipa með því að velja hvað á að birta frá tiltækum lista yfir ráðlagt efni sem byggir á hlutverkamiðstöðinni&mdash;án þess að fara úr Teams. Frekari upplýsingar um efnið sem hægt er að velja úr er að finna í [Hvaðan kemur það efni sem mælt er með?](/dynamics365/business-central/teams-faq?tabs=tabs#where-does-the-recommended-content-come-from).

1. Efst á rás eða í spjalli í Teams skal velja **+ Bæta við flipa**.
2. Í reitnum **Leit** skal slá inn *business central*, velja síðan **[!INCLUDE [prod_short](includes/prod_short.md)]** táknið og bíða eftir að grunnstillingargluggi [!INCLUDE [prod_short](includes/prod_short.md)] flipans birtist.

   ![Sýnir grunnstillingarglugga Business Central-flipans í Teams](media/teams-bc-tab-config-window.png)

3. Valkosturinn **Velja úr efni sem mælt er með fyrir** sýnir fyrirtækið í [!INCLUDE [prod_short](includes/prod_short.md)] sem verið er að vinna með. Ef sýna á efni frá öðru fyrirtæki skal velja núverandi fyrirtæki og nota síðan valkostina **Umhverfi** og **Fyrirtæki** til að tilgreina fyrirtæki sem á að vinna með.
4. Veljið niðurör í valkostinum **Efni flipa** og veljið efnið sem á að birta.

   <!-- The list shows all pages that are bookmarked on your role center in [!INCLUDE [prod_short](includes/prod_short.md)]. To learn more about the content that you can choose from, see [Where does the recommended content come from?](teams-faq.md#recommended-content).-->
5. Sumar síður geta innihaldið mismunandi yfirlit, sem eru afbrigði af síðunni sem er síuð til að sýna tiltekin gögn. Til að breyta yfirlitinu fyrir efnið skal velja niðurörina fyrir valkostinn **Æskilegt yfirlit** og velja yfirlitið af listanum.

   Frekari upplýsingar um yfirlitin er að finna í [Vista og sérsníða yfirlit](ui-views.md).
6. Veljið **Birta í rásinni um þennan flipa** til að birta sjálfkrafa tilkynningu í Teams-rás eða spjalli til að láta þátttakendur vita að búið sé að bæta við þessum flipa.
7. Veljið **Vista**.

## <a name="add-tab-using-a-page-link"></a>Bæta við flipa með tengil á síðu

Önnur leið til að bæta við flipa er að nota tengil (vefslóð) á síðuna sem á að sýna. Þessi leið er gagnleg þegar á að birta tiltekna [!INCLUDE [prod_short](includes/prod_short.md)] færslu eða listasíðu sem ekki er bókamerkt í hlutverkamiðstöðinni.

1. Efst á rás eða í spjalli í Teams skal velja **+ Bæta við flipa**.
2. Í reitnum **Leit** skal slá inn *business central*, velja síðan **[!INCLUDE [prod_short](includes/prod_short.md)]** táknið.
3. Bíðið eftir því að grunnstillingargluggi [!INCLUDE [prod_short](includes/prod_short.md)] flipans birtist, veljið síðan valkostinn **Líma [!INCLUDE [prod_short](includes/prod_short.md)] tengil í staðinn**.

   ![Sýnir grunnstillingarglugga Business Central-flipans í Teams og auðkennir valkost tengils](media/teams-bc-tab-config-window-page-link.png)
4. Opnið [!INCLUDE [prod_short](includes/prod_short.md)] og opnið síðuna sem á að birta á flipanum.
5. Afritaðu tengilinn á síðuna.

   Hægt er að afrita tengilinn á tvo vegu. Auðveldasta og æskilegasta leiðin er að velja **Deila** ![Deila tákni í Business Central](media/share-icon.png) > **Afrita tengil**. Hin leiðin er að afrita alla vefslóðina úr veffangastiku vafrans. Frekari upplýsingar um þetta skref er að finna í [Deila færslum Business Central og síðutenglum](across-working-with-teams.md).

6. Farið aftur í Teams og límið tengilinn í reitinn **Vefslóð**.
7. Í reitinn **Heiti flipa** skal færa inn heiti sem birtist á flipanum.
8. Veljið **Birta í rásinni um þennan flipa** til að birta sjálfkrafa tilkynningu í Teams-rás eða spjalli til að láta þátttakendur vita að búið sé að bæta við þessum flipa.
9. Veljið **Vista**.

## <a name="add-tab-by-pinning-card-details"></a>Bæta við flipa með því að festa spjaldaupplýsingar

Notið þessi skref til að bæta við flipa fyrir færslu sem var deilt eða límd í Teams-rás eða spjall. Frekari upplýsingar um hvernig á að deila færslum og síðutenglum í Teams er að finna í [Deila færslum og síðutenglum í Teams](across-working-with-teams.md).

1. Í Teams skal velja hnappinn **Upplýsingar** á spjaldinu.
2. Efst í hægra horninu á upplýsingum spjalds skal velja **Festa efst á spjalli** ![ Festa tákn til að bæta Teams-flipa í Business Central](media/pin-teams.png) tákn.

## <a name="change-a-tab-and-its-content"></a>Breyta flipa og efni hans

Eftir að flipa hefur verið bætt við er hægt að gera ákveðnar breytingar á flipanum. Til dæmis er hægt að endurnefna flipann, færa hann og fjarlægja. Þessar aðgerðir er að finna í valkostum flipans sem eru í boði með því að velja niðurörina á flipanum.

![Sýnir grunnstillingarglugga Business Central-flipans í Teams og valmynd flipavalkosta](media/teams-bc-tab-config-window-options.png)

Hvað varðar efni flipa, þá er hægt að breyta gögnunum ef leyfi er til staðar. Ef gögnunum er breytt sjá aðrir ekki breytingarnar fyrr en þeir hafa farið úr flipanum og inn í hann aftur. Það sama á við um þig ef einhver annar gerir breytingar á gögnum. Ekki er hægt að breyta síðunni sem birtist á flipanum, fjarlægið því flipann og bætið við öðrum sem passar við.

Einnig er hægt að breyta yfirliti síðunnar og gögnum hennar, eins og röðun og skiptingu á útliti á milli lista- og reitayfirlita. Þegar slíkar breytingar eru gerðar hafa þær ekki áhrif á hvað aðrir sjá. Þeir sjá hvað þú birtir upprunalega þar til þeir gera svipaðar breytingar.

## <a name="see-also"></a>Sjá einnig .

[Business Central og Microsoft Teams samþættingaryfirlit](across-teams-overview.md)  
[Setja upp [!INCLUDE [prod_short](includes/prod_short.md)]-forritið fyrir Microsoft Teams](across-install-app-for-teams.md)  
[Deila færslum Business Central og síðutenglum í Microsoft Teams](across-working-with-teams.md)
[Teams - Algengar spurningar](teams-faq.md)  
[Leitar að viðskiptavinum, lánardrottnum og öðrum tengiliðum úr Microsoft Teams](across-search-contacts-teams.md)  
[Breyta fyrirtæki og aðrar stillingar í Teams](across-teams-settings.md)  
[Úrræðaleit Teams](admin-teams-troubleshooting.md)  
[Þróun fyrir samþættingu Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
