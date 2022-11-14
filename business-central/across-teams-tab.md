---
title: Bæta við miðlægu flipa Business í Microsoft Teams
description: Lærðu að bæta við flipum í teymum sem birta vefsíður fyrirtækja.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 11/04/2022
ms.custom: bap-template
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, share records, tab
ms.openlocfilehash: cff1392b0e4ae622819fa50d4eaf69b98a9a1a52
ms.sourcegitcommit: bef166d75d656f4cc516f5f9a85227e540630344
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/07/2022
ms.locfileid: "9748402"
---
# <a name="add-business-central-tab-in-microsoft-teams"></a>Bæta við miðlægu flipa Business í Microsoft Teams

[!INCLUDE [online_only](includes/online_only.md)]

Í teymum birtast flipar efst í rásum og spjalli og gefa þátttakendum skjótan aðgang að persónupplýsingum. Í greininni er útskýrt mismunandi leiðir til að bæta við flipa sem birtir [!INCLUDE [prod_short](includes/prod_short.md)] gögn.

![Flipar í teymum](media/teams-tabs-border.png)

## <a name="about-business-central-tabs"></a>Um flipa Viðskiptamiðis

Á [!INCLUDE [prod_short](includes/prod_short.md)] flipa fæst einblöðungur Yfirlit [!INCLUDE [prod_short](includes/prod_short.md)] yfir lista og kortasíður. Flipinn birtist ekki í heilvefbiðlaranum [!INCLUDE [prod_short](includes/prod_short.md)]. Það er ekki vafrandi rammi, [!INCLUDE [prod_short](includes/prod_short.md)] Banner (til dæmis með segja mér, leit, hjálp) eða Top Navigation valmynd &mdash; bara síðu efni og aðgerðir. Efnið er gagnvirkt, sem þýðir að hægt er að velja aðgerðir og tengla, breyta gögnum og fleira. Þú takmarkast við það sem þú sérð og getur gert með sömu heimildum og þú hefur úthlutað reikningnum þínum í [!INCLUDE [prod_short](includes/prod_short.md)].

Til að fræðast um hverjir geta skoðað efnið í [!INCLUDE [prod_short](includes/prod_short.md)] flipa Sérðu [hver getur séð innihald flipa?](/dynamics365/business-central/teams-faq?tabs=tabs#who-can-view).

> [!TIP]
> Ertu verktaki? Einnig er hægt að bæta við flipa forritað með Microsoft graph API. Frekari upplýsingar er að finna [í bæta við Þjónustuflipa í teymum](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams-tabs).  

## <a name="prerequisites"></a>Frumskilyrði

Ef bæta á [!INCLUDE [prod_short](includes/prod_short.md)] við flipa verða eftirtaldar kröfur að vera uppfylltar:

- Þú hefur aðgang að Microsoft Teams.
- Þú ert [!INCLUDE [prod_short](includes/prod_short.md)] með leyfi.
- Þú hefur sett upp [!INCLUDE [prod_short](includes/prod_short.md)]-forritið  í Teams. Frekari upplýsingar er að finna [í setja upp [!INCLUDE [prod_short](includes/prod_short.md)] App fyrir Microsoft Teams](across-install-app-for-teams.md).

Ef skoða [!INCLUDE [prod_short](includes/prod_short.md)] á flipa sem var bættur af öðrum þátttakanda í rásinni eða spjalli verða eftirfarandi kröfur að vera uppfylltar:

- Þú hefur aðgang að Microsoft Teams.
- [!INCLUDE [prod_short](includes/prod_short.md)] Leyfishafa er heimilt eða takmarkaður aðgangur að starfsemi miðsvæðis með Microsoft 365 leyfi eingöngu. Nánari upplýsingar er að finna [á miðlægu aðgengi með Microsoft 365 leyfum](admin-access-with-m365-license.md).
- Þú hefur sett upp [!INCLUDE [prod_short](includes/prod_short.md)]-forritið  í Teams.

## <a name="add-tab-using-recommended-content"></a>Bæta flipa við ráðlagt efni

Notið þessar leiðbeiningar til að bæta við flipa með því að velja það sem á að birta af tiltækan lista yfir Ráðlögð efni sem byggja hlutverkamiðstöð &mdash; þína án þess að fara frá teymi. Til að fræðast nánar um efnið sem hægt er að velja um má sjá [Hvaðan kemur mælt efni úr?](/dynamics365/business-central/teams-faq?tabs=tabs#where-does-the-recommended-content-come-from).

1. Efst í rás eða spjallað í teymum þarf að velja **+ Bæta við flipa**.
2. **Í leitarglugganum** er *Business Central* valið og síðan er **[!INCLUDE [prod_short](includes/prod_short.md)]** teiknið og beðið [!INCLUDE [prod_short](includes/prod_short.md)] eftir skilgreiningarglugga flipans að birtast.

   ![Sýnir gluggann Skilgreining miðlægu flipans í teymum](media/teams-bc-tab-config-window.png)

3. **Valið úr efni sem mælt er með fyrir** valkost sýnir fyrirtækið í [!INCLUDE [prod_short](includes/prod_short.md)] sem unnið er með. Ef þú vilt Sýna efni frá öðru fyrirtæki, Veldu þá fyrirtæki, Notaðu **svo umhverfi** og **fyrirtæki** valkosti til að tilgreina fyrirtæki sem þú vilt vinna með.
4. Velja skal niður ör í **valkostinum flipi** og velja það efni sem á að sýna.

   <!-- The list shows all pages that are bookmarked on your role center in [!INCLUDE [prod_short](includes/prod_short.md)]. To learn more about the content that you can choose from, see [Where does the recommended content come from?](teams-faq.md#recommended-content).-->
5. Sumar síður geta innihaldið mismunandi yfirlit sem eru afbrigði síðunnar sem er afmarkað til að sýna tiltekin gögn. Ef breyta á yfirliti fyrir efni er ör valin niður fyrir **valkostinn æskilegur** valkostur og yfirlitið valið úr listanum.

   Frekari upplýsingar um Yfirlit er að finna [í Vista og sérsníða yfirlit](ui-views.md).
6. Veljið **Bóka á rásinni um þennan flipa** til að bóka sjálfkrafa tilkynningu í teymum rás eða spjall til að láta þátttakendur vita að bætt hafi verið við þennan flipa.
7. Veljið **Vista**.

## <a name="add-tab-using-a-page-link"></a>Bæta flipa við með síðutengli

Önnur leið til að bæta við flipa með því að nota tengil (URL) á síðuna sem sýna á. Þessi leið er gagnleg þegar óskað er eftir að birta tiltekna [!INCLUDE [prod_short](includes/prod_short.md)] færslu eða listasíðu sem er ekki bókmerkt í hlutverkamiðstöðinni þinni.

1. Efst í rás eða spjallað í teymum þarf að velja **+ Bæta við flipa**.
2. **Í leitargluggann** er ritað *viðskiptamiðborg* og síðan er **[!INCLUDE [prod_short](includes/prod_short.md)]** táknið valið.
3. [!INCLUDE [prod_short](includes/prod_short.md)] Bíða skal eftir að glugginn samskipun birtist, og velja **síðan líma [!INCLUDE [prod_short](includes/prod_short.md)] tengil í staðinn**.

   ![Sýnir gluggann Skilgreining miðlægu flipans í teymum og auðkennir valkostinn tengill](media/teams-bc-tab-config-window-page-link.png)
4. [!INCLUDE [prod_short](includes/prod_short.md)] Farið er í og Opnið síðuna sem á að birta á flipanum.
5. Afritaðu tengilinn á síðuna.

   Það eru tvær leiðir til að afrita hlekkinn. Auðveldasta og ákjósanlegri leiðin er að **velja**![tákn með samnýta hluti í hlekknum aðalafritun. ](media/share-icon.png) > **·** Hin leiðin er að afrita alla SLÓÐINA af veffangsrein vafrans. Frekari upplýsingar um þetta skref [fást með því að samnýta miðlægu Viðskiptamiðfærslur og Síðutengla](across-working-with-teams.md).

6. Farðu aftur í teyma og límdu tengilinn í **reitinn URL**.
7. **Í reitnum flipaheiti** er fært inn heiti sem birtist á flipanum.
8. Veljið **Bóka á rásinni um þennan flipa** til að bóka sjálfkrafa tilkynningu í teymum rás eða spjall til að láta þátttakendur vita að bætt hafi verið við þennan flipa.
9. Veljið **Vista**.

## <a name="add-tab-by-pinning-card-details"></a>Bæta flipa við upplýsingar um skipreika kort

Notið þessar leiðbeiningar til að bæta við flipa fyrir færslu sem var samnýtt eða líma á Teymdir rás eða spjall. Til að fræðast um hvernig á að samnýta færslur og síðutengla í teymum er [Samnýting færslna og síðutengla í teymum](across-working-with-teams.md).

1. Í teymum skal velja **hnappinn upplýsingar** á spjaldinu.
2. Í efra hægra horninu á spjaldinu upplýsingar skal velja **PIN efst á spjallborði**![fyrir hópa sem bæta á við teymi á aðaltákni ](media/pin-teams.png) Business.

## <a name="change-a-tab-and-its-content"></a>Breyta flipa og innihaldi hans

Þegar flipa hefur verið bætt við er hægt að gera tilteknar breytingar á flipanum. Til dæmis er hægt að endurnefna flipann, færa hann og fjarlægja. Þessar aðgerðir eru í valkostum flipans sem eru tiltækir með því að velja niðurörina á flipanum.

![Sýnir gluggann Skilgreining miðlægu flipans í teymum og valmyndarvalkostunum Valkostir](media/teams-bc-tab-config-window-options.png)

Eins og um innihald flipa er að ræða er hægt að breyta gögnunum, ef heimildar er getið. Ef þú breytir gögnunum, aðrir sjá ekki breytingarnar fyrr en þeir yfirgefa flipann og koma aftur. Það sama gildir fyrir þig ef einhver annar gerir breytingar á gögnum. Þú getur ekki breytt síðunni sem birtist á flipanum, svo bara fjarlægt flipann og bætt öðru eins við jakkanum.

Einnig er hægt að breyta yfirliti síðunnar og gögnum þess, eins og að raða og skipta útliti á milli lista og tilflettingar. Þegar gerðar eru slíkar breytingar hafa þær ekki áhrif á það sem aðrir sjá. Þeir sjá það sem upphaflega var bókað, þangað til að þeir gera svipaðar breytingar sjálfir.

## <a name="see-also"></a>Sjá einnig .

[Business Central og Microsoft Teams samþættingaryfirlit](across-teams-overview.md)  
[Setja upp [!INCLUDE [prod_short](includes/prod_short.md)]-forritið fyrir Microsoft Teams](across-install-app-for-teams.md)  
[Hlutdeild fyrirtækja miðlæg færslur og Blaðsíðutenglar í Microsoft Teams](across-working-with-teams.md).
[Teams - Algengar spurningar](teams-faq.md)  
[Leitar að viðskiptavinum, lánardrottnum og öðrum tengiliðum úr Microsoft Teams](across-search-contacts-teams.md)  
[Breyta fyrirtæki og aðrar stillingar í Teams](across-teams-settings.md)  
[Úrræðaleit Teams](admin-teams-troubleshooting.md)  
[Þróun fyrir samþættingu Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
