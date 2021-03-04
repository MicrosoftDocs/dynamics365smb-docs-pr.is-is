---
title: Úrræðaleit Microsoft Teams samþættingar
description: Frekari upplýsingar um hvað hægt er að gera sem stjórnandi til að stjórna Microsoft Teams-samþættingu.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, troubleshooting, errors
ms.date: 01/20/2021
ms.author: jswymer
ms.openlocfilehash: 10612a3e5e257969b2daf0839ea0826316a956ee
ms.sourcegitcommit: 36a32c997b201ff32ed8c1cff8179b36e2468c47
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/22/2021
ms.locfileid: "5046533"
---
# <a name="troubleshooting-microsoft-teams-integration-with-prod_short"></a>Úrræðaleit Microsoft Teams-samþættingar við [!INCLUDE [prod_short](includes/prod_short.md)]

[!INCLUDE [online_only](includes/online_only.md)]

Í þessari grein er að finna upplýsingar um hvernig á að finna og lagfæra vandamál sem geta komið upp þegar Microsoft Teams er notað með [!INCLUDE [prod_short](includes/prod_short.md)], sem dæmigerður notandi eða stjórnandi.

## <a name="none-of-my-links-expand-into-a-card"></a>Enginn af tenglunum mínum stækkar í spjald 

Ef þetta vandamál kemur upp, þá eru nokkrir hlutir hér sem þú getur prófað:

1. Fyrst skal ganga úr skugga um að [!INCLUDE [prod_short](includes/prod_short.md)] forritið fyrir Teams sé uppsett.

    Til að athuga það skal skrá sig inn í Teams-skjáborðsforritið eða Teams í vafranum. Síðan skal velja vinstra megin **Forrit** og leita að **[!INCLUDE [prod_short](includes/prod_short.md)]**. Þegar **[!INCLUDE [prod_short](includes/prod_short.md)]** forrritið finnst skal velja það til að opna upplýsingasíðu forritsins. Ef hnappurinn **Bæta við fyrir mig** birtist, þá er [!INCLUDE [prod_short](includes/prod_short.md)]-forritið ekki uppsett. Frekari upplýsingar um uppsetningu forritsins er að finna í [Setja upp [!INCLUDE [prod_short](includes/prod_short.md)]-forritið fyrir Microsoft Teams](across-install-app-for-teams.md).

    > [!NOTE]
    > Gestanotendur geta ekki strax sett upp forrit. Frekari upplýsingar um gestanotendur er að finna í algengum spurningum um samvinnu við gesti. 

2. Næst skaltu athuga hvort þú hafir skráð þig inn með réttum innskráningarupplýsingum.

    Í Teams skal fara í hvaða spjall sem er og undir skrifglugga skilaboða skal velja táknið [!INCLUDE [prod_short](includes/prod_short.md)]. Þegar glugginn birtist skaltu athuga hvort notandinn sem stendur að sé tengdur sé sá sami og þú notar til að tengjast við [!INCLUDE [prod_short](includes/prod_short.md)].

3. Gangið úr skugga um að codeunit: **2718 Þjónustuaðili síðusamantektar** sé gefin út sem vefþjónusta.

    Teams tengist við [!INCLUDE [prod_short](includes/prod_short.md)] með endastöð að þessari Codeunit í [!INCLUDE [prod_short](includes/prod_short.md)]-þjónustunni. Upplýsingar um birtingu vefþjónustu er að finna í [Birta vefþjónustu](across-how-publish-web-service.md).

4. Fyrirtækið kann einnig að koma í veg fyrir að þú getir límt tengla sem verða að spjöldum. Hafa skal samband við stjórnanda til að skilja fyrirtækisreglur Teams sem kunna að eiga við.

## <a name="my-link-sometimes-doesnt-expand-into-a-card"></a>Tengillinn minn víkkar stundum ekki í spjald 

Tengill verður ekki víkkaður í spjald við eftirfarandi aðstæður:

- Tengillinn vísar í síðu af gerð sem stendur ekki fyrir færslu. Til dæmis gæti það verið tengill á hlutverkamiðstöð [!INCLUDE [prod_short](includes/prod_short.md)]. Hægt er að skoða gerð síðunnar með því að nota síðueftirlitssvæðið í vefbiðlaranum í [!INCLUDE [prod_short](includes/prod_short.md)]. Frekari upplýsingar um síðueftirlit er að finna í [Síður skoðaðar](across-inspect-page.md).
- Tengillinn vísar í síðu sem (á tæknilegu stigi) tengist ekki upprunatöflu í [!INCLUDE [prod_short](includes/prod_short.md)]. Hægt er að skoða hvort síða sé með upprunatöflu með því að nota síðueftirlitssvæðið í vefbiðlaranum í [!INCLUDE [prod_short](includes/prod_short.md)]. Frekari upplýsingar um síðueftirlit er að finna í [Síður skoðaðar](across-inspect-page.md). 
- Teams styður ekki forskoðun tengla í sumum eiginleikum. Til dæmis þegar spjall er opnað í sérglugga, þegar þú ert á fundi eða þú ert gestur í öðru fyrirtæki.
- Teams hættir að reyna að sýna spjaldið eftir 15 sekúndur, t.d. vegna netvandamála.
- Teams víkkar hugsanlega ekki tengilinn ef búið að líma tengil í sama skrifglugga skilaboða og eyða spjaldinu.

Tengillinn þarf einnig að innihalda allar nauðsynlegar upplýsingar til að finna færsluna og birta samsvarandi spjald. Þessar upplýsingar fela í sér:

- Umhverfisheiti, með því að taka það með í vefslóð. Ef heiti umhverfis er ekki tilgreint gerir Teams ráð fyrir því að þú sért að reyna að ná í umhverfi sem heitir „Framleiðsla“.
- Nafn fyrirtækis með því að nota *company=* færibreytuna
- Auðkenni síðu með því að nota *page=* færibreytuna
- Bókamerkið í færslunni með því að nota *bookmark=* færibreytuna

Dæmi:

`https://businesscentral.dynamics.com/?environmentname=Production&company=CRONUS%20USA%2C%20Inc.&page=21&dc=0&bookmark=21%3bEgAAAAJ7BTEAMAAwADAAMA%3d%3d`

Tæknilegar upplýsingar um [!INCLUDE [prod_short](includes/prod_short.md)]-vefslóðir er að finna í [Vefslóð vefbiðlara](/dynamics365/business-central/dev-itpro/developer/devenv-web-client-urls) í [!INCLUDE [prod_short](includes/prod_short.md)]-þróunaraðila og IT Pro hjálp.

## <a name="the-card-is-displayed-in-the-message-compose-box-but-selecting-the-details-button-does-nothing"></a>Spjaldið er birt í skrifglugga skilaboða, en að velja upplýsingahnappinn gerir ekkert 

Þegar tengill víkkar í spjald í skrifglugga skilaboða þarf að senda skilaboðin í spjallinu áður en hægt er að nota hnappinn **Upplýsingar**.

## <a name="the-details-window-opens-but-shows-an-error-before-details-are-shown"></a>Upplýsingaglugginn opnast en sýnir villu áður en upplýsingar eru sýndar

Tvær ástæður geta verið fyrir þessu vandamáli: ekki nægar heimildir í [!INCLUDE [prod_short](includes/prod_short.md)] eða vafrastillingar (þegar Teams er notað í vafranum).

1. Staðfestu heimildir þínar í [!INCLUDE [prod_short](includes/prod_short.md)].

    Til að skoða upplýsingar um kort, athugar [!INCLUDE [prod_short](includes/prod_short.md)] leyfið þitt og heimildirnar til að skoða þessa ákveðnu færslu og síðu í tilteknu fyrirtæki og umhverfi. Ef þú hefur ekki heimild fyrir einhverjum þessara þátta, þá birtast stöðluð [!INCLUDE [prod_short](includes/prod_short.md)] villuboð um heimildir í upplýsingaglugganum. 

    Nánari upplýsingar um heimildir má finna í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md)

2. Athugaðu vafrastillingarnar ef Teams er notað í vafranum.

    - Annaðhvort verður að vera slökkt á sprettigluggavörn vafrans eða stillt þannig að leyfa sprettiglugga frá lénum *businesscentral.dynamics.com* eða *bc.dynamics.com*. Upplýsingar um hvernig á að leyfa sprettiglugga fyrir [!INCLUDE [prod_short](includes/prod_short.md)] er að finna í [Vafrinn settur upp](across-browser-settings.md#popup).
    - Vafrinn verður að hafa aðgang að staðbundinni vafrageymslu fyrir kökur og kjörstillingar á meðan þú vinnur.
    - Forðastu að nota gesta- eða einkavefskoðun nema það sé nauðsynlegt, því að það fleygir eða lokar fyrir ákveðið efni í sumum vöfrum.

    Frekari upplýsingar um lágmarkskröfur vafrans er að finna í [Lágmarkskröfur fyrir notkun [!INCLUDE [prod_short](includes/prod_short.md)]](product-requirements.md#browsers) 

## <a name="im-having-problems-with-the-camera-or-location-in-teams"></a>Vandamál kom upp með myndavélina eða staðsetningar í Teams 

Þegar eiginleikar [!INCLUDE [prod_short](includes/prod_short.md)] eru notaðir í upplýsingaglugganum sem þarf aðgang að staðsetningu þinni eða myndavél tækis, þarf fyrst að veita Teams samþykki fyrir því að fá aðgang að þessum möguleikum tækisins.  

- Fyrir Teams í vafranum skal ganga úr skugga um að vafrastillingar þínar leyfi aðgang að myndavél og staðsetningu fyrir https://teams.microsoft.com. 

- Fyrir Teams fyrir iOS eða Android skal ganga úr skugga um að tækjastillingarnar leyfi aðgang að myndavél og staðsetningu fyrir farsímaforrit Teams. 

Til að fá aðstoð við að breyta þessum stillingum skal sjá [Myndavélin mín virkar ekki í Teams](https://support.microsoft.com/office/my-camera-isn-t-working-in-teams-9581983b-c6f9-40e3-b0d8-122857972ade?ns=msftteams&version=16&ui=en-us&rs=en-us&ad=us) í notendaþjónustu Microsoft.

[!INCLUDE [prod_short](includes/prod_short.md)]-forritið styður ekki staðsetningu í skjáborðsforriti Teams. Frekari upplýsingar um staðsetningu er að finna í [Teams - Algengar spurningar](teams-faq.md#location).

Sumir vafrar, eins og nýi Microsoft Edge, gera þér kleift að velja hvaða myndavél tækis á að nota þegar tækið styður margar myndavélar. 

## <a name="teams-displays-mixed-languages-for-my-cards-and-card-details"></a>Teams sýnir ýmis tungumál fyrir mín spjöld og upplýsingar spjalds 

Til þess að spjöld og upplýsingar spjalds birti alltaf á sama tungumálinu í Teams verður tungumál Teams-biðlarans og tungumálið sem er notað í [!INCLUDE [prod_short](includes/prod_short.md)]-vefbiðlaranum að passa.

- Til að finna út úr því hvernig á að breyta tungumálinu í Teams skal skoða [Breyta stillingum í Teams](https://support.microsoft.com/en-us/office/change-settings-in-teams-b506e8f1-1a96-4cf1-8c6b-b6ed4f424bc7) í notendaþjónustu Microsoft. 

- Frekar upplýsingar um hvernig skuli breyta tungumálinu í [!INCLUDE [prod_short](includes/prod_short.md)] er að finna í [Breyta grunnstillingum - Tungumál](ui-change-basic-settings.md#language).

Frekari upplýsingar um hvernig tungumál virka á milli Teams og [!INCLUDE [prod_short](includes/prod_short.md)] er að finna í [Teams - Algengar spurningar](teams-faq.md#language).

## <a name="i-edited-a-field-in-the-details-window-but-my-change-wasnt-saved"></a>Ég breytti reit í upplýsingaglugganum, en breytingin vistaðist ekki

Breytingar sem gerðar eru á reit í upplýsingagluggum eru sjálfkrafa vistaðar þegar farið er úr reitnum. Áður en glugganum er lokað eftir að reit er breytt skal ganga úr skugga um að ýta á færslulykilinn eða smella/pikka utan reitsins.

## <a name="see-also"></a>Sjá einnig

[[!INCLUDE [prod_short](includes/prod_short.md)] og Microsoft Teams samþættingaryfirlit](across-teams-overview.md)  
[Setja upp [!INCLUDE [prod_short](includes/prod_short.md)]-forritið fyrir Microsoft Teams](across-install-app-for-teams.md)  
[Teams - Algengar spurningar](teams-faq.md)  
[Þróun fyrir samþættingu Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]