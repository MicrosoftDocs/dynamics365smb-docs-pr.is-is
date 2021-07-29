---
title: Deila Business Central Records í Microsoft Teams
description: Fá upplýsingar um notkun Business Central fyrir Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, share records
ms.date: 05/19/2021
ms.author: jswymer
ms.openlocfilehash: fb134ce04cb6b53f2432f0f371d7ca82411f0cee
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/08/2021
ms.locfileid: "6444019"
---
# <a name="sharing-business-central-records-in-microsoft-teams"></a>Deila Business Central Records í Microsoft Teams

[!INCLUDE [online_only](includes/online_only.md)]

[!INCLUDE [prod_short](includes/prod_short.md)] býður upp á forrit sem tengir Microsoft Teams við viðskiptagögn í [!INCLUDE [prod_short](includes/prod_short.md)] þannig að hægt sé að deila upplýsingum á fjótlegan hátt á meðal teymismeðlima og svara fyrirspurnum með skjótari hætti. Í þessari grein koma fram upplýsingar um hvernig á að nota forritið til að deila [!INCLUDE [prod_short](includes/prod_short.md)] færslum, á borð við viðskiptavini, sölupöntunum, eða reikningum með samstarfsfólki í samtali í Teams.

## <a name="overview"></a>Yfirlit

[!INCLUDE [prod_short](includes/prod_short.md)]-forritið gerir kleift að:

- Afrita tengil í hvaða færslu Business Central sem er og líma hann í spjall á Teams til að deila honum með samstarfsfólki. Forritið stækkar svo tengilinn í gagnvirkt spjald sem birtir upplýsingar um færsluna.
- Þegar á samtalinu stendur getur þú og samstarfsfólk þitt skoðað frekari upplýsingar um færsluna, breytt gögnum og gripið til aðgerða &mdash; án þess að fara úr Teams.

[![Samþætting Teams við Business Central.](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)

## <a name="prerequisites"></a>Frumskilyrði

- Þú hefur aðgang að Microsoft Teams.
- Þú hefur sett upp [!INCLUDE [prod_short](includes/prod_short.md)]-forritið  í Teams. Frekari upplýsingar er að finna í [Setja upp [!INCLUDE [prod_short](includes/prod_short.md)]-forritið fyrir Microsoft Teams](across-install-app-for-teams.md)

> [!NOTE]
> Allir þátttakendur í Teams-spjalli geta skoðað spjöld fyrir færslur Business Central sem þú sendir inn á spjallið. En til að skoða frekari upplýsingar um færslur með því að nota hnappana **Upplýsingar** eða **Sprettigluggi** á spjaldi, þurfa þeir að fá aðgang að [!INCLUDE [prod_short](includes/prod_short.md)]. Nánari upplýsingar er að finna í [Stjórnun Microsoft Teams samþættingar](admin-teams-integration.md#minimum-requirements-1).

## <a name="include-a-business-central-card-in-a-teams-conversation"></a>Hafa með Business Central-spjald í samtali í Teams

1. Skráðu þig inn í [!INCLUDE [prod_short](includes/prod_short.md)] með vafranum.
2. Opnið færsluna sem á að deila.

    Forritið er hannað til að birta síðu kortagerðar úr [!INCLUDE [prod_short](includes/prod_short.md)]. Opnið því síðu sem sýnir eina færslu, eins og vöru, viðskiptavin eða sölupöntun. Ekki er hægt að nota hana fyrir hlutverkamiðstöðvar eða síður sem birta nokkrar færslur í lista.

3. Afritið alla vefslóðina úr veffangastiku vafrans.

   ![Afritið vefslóð Business Central úr vafra.](media/teams-url-v2.png)
4. Farið í Teams og hefjið samtal sem getur verið spjall við einstakling, hóp eða teymisrás.

    <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. Límið vefslóðina í skilaboðagluggann þar sem skrifuð eru skilaboð..

   ![Límið vefslóð Business Central í Teams.](media/teams-paste-url-v2.png)
6. Fyrsta skiptið sem tengill er límdur í samtal, verður beðið um innskráningu í [!INCLUDE [prod_short](includes/prod_short.md)] og að veita samþykki fyrir forritinu til að sækja gögn. Fylgið einfaldlega leiðbeiningunum á skjánum.

    > [!NOTE]
    > Aðeins þarf að gera þetta skref einu sinni.

7. Bíðið augnablik á meðan spjald er búið til í skilaboðaglugganum.

8. Þegar spjaldið birtist skal leita vel og vandlega í innihald þess eftir viðkvæmum upplýsingum áður en skilaboðin eru send. Þetta skref er mikilvægt vegna þess að þegar skilaboðin eru send geta allir í samtalinu séð spjaldið.

9. Ef spjaldið lítur vel út skal velja **Senda** til að senda það í samtalið.

    > [!TIP]
    > Eftir að kortið birtist og áður en **Senda** er valið er hægt að eyða límdri vefslóð ef þú vilt.

10. Til að fá frekari upplýsingar eða gera breytingar á færslunni sem birtist í spjaldinu skal velja **Upplýsingar**. Nánari upplýsingar er að finna í næsta hluta.

## <a name="view-card-details"></a>Skoða upplýsingar spjalds

Þegar búið er að senda spjald á samtal, geta allir þátttakendur með [viðeigandi heimildir](admin-teams-integration.md#permissions) valið **Upplýsingar** til að opna glugga sem sýnir frekari upplýsingar um færsluna&mdash;og hugsanlega geta gert breytingar á henni. Það skiptir ekki máli hvort það sért þú sem sendir spjaldið eða sá sem fær spjaldið. Eiginleikinn **Upplýsingar** er sérstaklega gagnlegur viðtakendum af því að hann veitir þeim samanteknar, hnitmiðaðar upplýsingar um færsluna á fljótlegan hátt í stað þess að þurfa að renna yfir alla færsluna.

Upplýsingasíðan svipar til þess sem þú sérð í færslunni [!INCLUDE [prod_short](includes/prod_short.md)]. En það er örlítið aðlagað að Teams. Þegar skoðun er lokið og breytingar hafa verið gerðar skal loka glugganum til að fara aftur í samtalið í Teams.

Hér eru nokkur atriði sem vert er að hafa í huga þegar unnið er með upplýsingar spjalds:

- Til að opna upplýsingar spjalds verða notendur að vera með heimild á síðunni og gögnum þess í [!INCLUDE [prod_short](includes/prod_short.md)].
- Spjöld í Teams-spjalli uppfærast ekki sjálfkrafa þegar gerðar eru breytingar. Allar breytingar sem eru vistaðar í færslu í upplýsingaglugganum eru vistaðar í [!INCLUDE [prod_short](includes/prod_short.md)]. En spjaldið í Teams sýnir ekki breytingarnar í samtalinu fyrr en tengillinn er límdur inn aftur.

Frekari upplýsingar um hvernig nota á spjöld og upplýsingar spjalds er að finna í [Teams - Algengar spurningar](teams-faq.md).

## <a name="see-also"></a>Sjá einnig

[Business Central og Microsoft Teams samþættingaryfirlit](across-teams-overview.md)  
[Setja upp [!INCLUDE [prod_short](includes/prod_short.md)]-forritið fyrir Microsoft Teams](across-install-app-for-teams.md)  
[Teams - Algengar spurningar](teams-faq.md)  
[Leitar að viðskiptavinum, lánardrottnum og öðrum tengiliðum úr Microsoft Teams](across-search-contacts-teams.md)  
[Breyta fyrirtæki og aðrar stillingar í Teams](across-teams-settings.md)  
[Úrræðaleit Teams](admin-teams-troubleshooting.md)  
[Þróun fyrir samþættingu Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]