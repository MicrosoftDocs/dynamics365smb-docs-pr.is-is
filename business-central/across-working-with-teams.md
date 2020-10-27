---
title: Unnið með Business Central Data í Microsoft Teams| Microsoft docs
description: Fá upplýsingar um notkun Business Central fyrir Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork
ms.date: 10/08/2020
ms.author: jswymer
ms.openlocfilehash: fbe024f724f018aae6d3aeb5251281bf4c3bfbde
ms.sourcegitcommit: 4bca699d2a5ce182eb5572d72fac4fb478c4f293
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989423"
---
# <a name="working-with-business-central-data-in-microsoft-teams"></a>Unnið með Business Central Data í Microsoft Teams

[!INCLUDE [teams_preview.md](includes/teams_preview.md)]

[!INCLUDE [prodshort](includes/prodshort.md)] býður upp á forrit sem tengir Microsoft Teams við viðskiptagögn í [!INCLUDE [prodshort](includes/prodshort.md)] þannig að hægt sé að deila upplýsingum á fjótlegan hátt á meðal teymismeðlima og svara fyrirspurnum með skjótari hætti. Í þessari grein koma fram upplýsingar um hvernig á að nota forritið til að deila [!INCLUDE [prodshort](includes/prodshort.md)]-gögnum með samstarfsfólki í samtali í Teams.

## <a name="overview"></a>Yfirlit

[!INCLUDE [prodshort](includes/prodshort.md)]-forritið gerir kleift að:

- Afrita tengil í hvaða færslu Business Central sem er og líma hann í spjall á Teams til að deila honum með samstarfsfólki. Tengillinn stækkar og verður að þéttu, gagnvirku spjaldi sem birtir upplýsingar um færsluna.
- Þegar á samtalinu stendur getur þú og samstarfsfólk þitt skoðað frekari upplýsingar um færsluna, breytt gögnum og gripið til aðgerða - án þess að fara úr Teams.

[![Samþætting Teams við Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)

## <a name="prerequisites"></a>Frumskilyrði

- Þú hefur aðgang að Microsoft Teams.
- Þú hefur sett upp [!INCLUDE [prodshort](includes/prodshort.md)]-forritið  í Teams. Frekari upplýsingar er að finna í [Setja upp [!INCLUDE [prodshort](includes/prodshort.md)]-forritið fyrir Microsoft Teams](across-install-app-for-teams.md)

> [!NOTE]
> Allir þátttakendur í Teams-spjalli geta skoðað spjöld fyrir færslur Business Central sem þú sendir inn á spjallið. En til að skoða frekari upplýsingar um færslur með því að nota hnappana **Upplýsingar** eða **Sprettigluggi** á spjaldi, þurfa þeir að fá aðgang að [!INCLUDE [prodshort](includes/prodshort.md)]. Nánari upplýsingar er að finna í [Stjórnun Microsoft Teams samþættingar](admin-teams-integration.md#minimum-requirements-1).
<!--
- People You and your coworkers have the following permissions in [!INCLUDE [prodshort](includes/prodshort.md)]
  - To paste a [!INCLUDE [prodshort](includes/prodshort.md)] link into a Teams conversation and have it expand into a card, you have to have at least permission to view the page and its data.
  - Once a card is submitted into a conversation, any user in that conversation can view that card without having permission to Business Central.
  - For other users to view more details from card, they must also have view permission, as a minimum, to the page and its data. If they want to change data, they'll need modify permissions.

  Setting up permissions is typically done by an administrator. For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md).-->

## <a name="include-a-business-central-card-in-a-teams-conversation"></a>Hafa með Business Central-spjald í samtali í Teams

1. Skráðu þig inn í [!INCLUDE [prodshort](includes/prodshort.md)] með vafranum.
2. Opnið færsluna sem á að deila.

    Forritið er hannað til að birta síðu kortagerðar úr [!INCLUDE [prodshort](includes/prodshort.md)]. Opnið því síðu sem sýnir eina færslu, eins og vöru, viðskiptavin eða sölupöntun. Ekki er hægt að nota hana fyrir hlutverkamiðstöðvar eða síður sem birta nokkrar færslur í lista.

3. Afritið alla vefslóðina úr veffangastiku vafrans.

   ![Afrita vefslóð Business Central úr vafranum](media/teams-url.png)
4. Farið í Teams og hefjið samtal sem getur verið spjall við einstakling, hóp eða teymisrás.

    <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. Límið vefslóðina í reitinn þar sem þú bætir við skilaboðum.

   ![Líma vefslóð Business Central í Teams](media/teams-paste-url.png)
6. Fyrsta skiptið sem tengill er límdur í samtal, verður beðið um innskráningu í [!INCLUDE [prodshort](includes/prodshort.md)] og að veita samþykki fyrir forritinu til að sækja gögn. Fylgið einfaldlega leiðbeiningunum á skjánum.

    > [!NOTE]
    > Aðeins þarf að gera þetta skref einu sinni.

7. Bíðið augnablik á meðan spjald er búið til í skilaboðaglugganum.

8. Þegar spjaldið birtist skal leita vel og vandlega í innihald þess eftir viðkvæmum upplýsingum áður en skilaboðin eru send. Þetta skref er mikilvægt vegna þess að þegar skilaboðin eru send geta allir í samtalinu séð spjaldið.

9. Ef spjaldið lítur vel út skal velja **Senda** til að senda það í samtalið.

    > [!TIP]
    > Eftir að kortið birtist og áður en **Senda** er valið er hægt að eyða límdri vefslóð ef þú vilt.

10. Til að skoða frekari upplýsingar eða gera breytingar á færslunni skal velja **Upplýsingar** .

    Upplýsingasíðan svipar til þess sem þú sérð í [!INCLUDE [prodshort](includes/prodshort.md)]. En það er örlítið aðlagað að Teams. Þegar skoðun er lokið og breytingar hafa verið gerðar skal loka glugganum til að fara aftur í samtalið í Teams.

    > [!NOTE]
    > Allar breytingar sem eru gerðar endurspeglast ekki í spjaldinu fyrr en næst þegar tengill þess er límdur í samtal.

## <a name="see-also"></a>Sjá einnig

[Business Central og Microsoft Teams samþættingaryfirlit](across-teams-overview.md)  
[Setja upp [!INCLUDE [prodshort](includes/prodshort.md)]-forritið fyrir Microsoft Teams](across-install-app-for-teams.md)  
[Þróun fyrir samþættingu Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  
[Hafist handa](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
