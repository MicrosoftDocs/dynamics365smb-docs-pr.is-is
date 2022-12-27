---
title: Setja upp aðgang með Microsoft 365 leyfum
description: Leiðarvísir um hvernig stjórnendur geta grunnstillt aðgang að Business Central með Microsoft 365 leyfum.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 11/03/2022
ms.custom: bap-template
ms.search.keywords: License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams
ms.search.forms: 9061
ms.openlocfilehash: 89ea9cebe7db05d954b2005dcaffaa7aa1649da7
ms.sourcegitcommit: 9bba11d474e21711cc8e2afefee8efb473170707
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788212"
---
# <a name="set-up-access-with-microsoft-365-licenses"></a>Setja upp aðgang með Microsoft 365 leyfum 

Stjórnendur verða að ljúka mörgum aðgerðum áður en notendur geta fengið aðgang að Business Central með Microsoft 365 leyfinu sínu. Skrefin hér að neðan sýna lágmarksuppsetningu sem þarf til að hefjast handa.  

## <a name="deploy-the-business-central-app-for-teams"></a>Setja upp Business Central-forritið fyrir Teams 

Til að leyfishafar Business Central geti deilt gögnum í Teams og til að Microsoft 365 leyfishafar geti nálgast þau gögn verður hver og einn að vera með Business Central-forritið fyrir Teams uppsett. Þótt notendur geti sett upp forritið á eigin spýtur er mælt með að stjórnendur noti miðlæga innleiðingu. Miðlæg innleiðing gerir þér kleift að færa víðtækari notendahópi forritið í öllu fyrirtækinu og lágmarka einstaklingsframtak notanda. 

Frekari upplýsingar um miðlæga uppsetningu Business Central-forritsins fyrir Teams er að finna í [Setja upp Business Central-forritið með miðlægri innleiðingu](admin-teams-integration.md#installing-the-business-central-app-by-using-centralized-deployment).

> [!NOTE]
> Ef þú hefur keyrt miðlæga innleiðingu áður og aðeins innleitt forritið hjá öryggishópi heimilaðra Business Central-notenda þarftu að keyra hana aftur til að innleiða frekari hópa eða allt fyrirtækið, eftir því hvernig þú stillir aðganginn.

> [!TIP]
> Ertu að leita að fljótlegri leið til að hefjast handa þegar þú prófar þennan eiginleika? Prufunotendur geta sett upp forritið á [aka.ms/BCgetTeamsApp](https://aka.ms/BCgetTeamsApp).

## <a name="configure-permissions"></a>Grunnstillir heimildir

Hönnun Business Central er örugg og áhættan er lágmörkuð með því að veita engar heimildir til Microsoft 365 notenda í upphafi. Stjórnendur verða að grunnstilla heimildir hlutar sem ákvarða hvaða töflur, síður og skýrslur hægt er að nálgast í Teams með aðeins Microsoft 365 leyfi. Þessar heimildir eru fyrstu heimildirnar sem eru úthlutaðar þegar notandi skráir sig inn í fyrsta skipti með Microsoft 365 leyfinu. 

Grunnstilling fyrstu heimilda:

1. Leitaðu að **Grunnstilling leyfis** í Business Central.
2. Veldu Microsoft 365 leyfið.
3. Efst á leyfissíðunni **Microsoft 365** skaltu velja breytingartáknið ![Breyta tákni](media/edit-pencil.png) og kveiktu síðan á **Sérsníða heimildir**. 
4. Í hlutanum **Sérsniðnar heimildasamstæður** skaltu bæta við viðeigandi heimildasamstæðum og velja hvort þær eigi við eitt fyrirtæki eða öll fyrirtæki innan umhverfisins.

> [!NOTE]
> Þegar notendalistinn í Business Central er samstilltur við notendur í Microsoft 365 er aðeins notendum sem eru með Business Central-leyfi bætt við notendalista Business Central. Notendum með aðeins Microsoft 365 leyfi er bætt á notendalistann þegar þeir opna Business Central í fyrsta skipti. Frekari upplýsingar eru í [Búa til notendur samkvæmt leyfum](ui-how-users-permissions.md).

> [!TIP]
> Ertu að leita að fljótlegri leið til að hefjast handa þegar þú prófar þennan sandkassaeiginleika eða tilraunafyrirtæki? Úthlutaðu heimildasamstæðunni **D365 Lesa** sem veitir heimildir að flestum hlutum.  

Þegar unnið er með margs konar umhverfi þarf að nota grunnstillingu leyfis á hvert umhverfi og það getur verið mismunandi í hverju umhverfi. 

Frekari upplýsingar er að finna í [Úthluta heimildum á notendur og hópa](ui-define-granular-permissions.md) og [Búa til heimildasamstæður](/dynamics365/business-central/dev-itpro/developer/devenv-permissionset-composing).

## <a name="turn-on-access-with-microsoft-365-licenses"></a>Kveikja á aðgangi með Microsoft 365 leyfum

Sjálfgefið er slökkt á aðgangi með Microsoft 365 leyfum. Aðgangur verður að vera virkur fyrir hvert umhverfi fyrir sig, sem gefur stjórnendum stjórn og leyfir stigskipta útgáfu í öllu fyrirtækinu. Þú kveikir á aðgangi með því að nota stjórnendamiðstöð Business Central: 

1. Efst í hægra horninu skaltu velja **Stillingar** ![Stillingar.](media/ui-experience/settings_icon_small.png "Stillingatákn fyrir hlutverkamiðstöð") > **Stjórnendamiðstöð**  
2. Í stjórnendamiðstöðinni skal velja  **Umhverfi**, síðan velja umhverfið þar sem þú vilt breyta leyfisaðgangi. 
3. Á síðunni **Umhverfisupplýsingar** skaltu velja **Breyta** fyrir stillinguna **Aðgangur með Microsoft 365 leyfum**.
4. Á svæðinu **Microsoft 365 leyfi** skal kveikja á rofanum. 
5. Veldu **Vista** þegar því er lokið og samþykktu staðfestinguna. Breytingin tekur strax gildi.

## <a name="test-your-setup"></a>Prófaðu uppsetninguna

Til að staðfesta að uppsetningin sé tilbúin fyrir framleiðslu munu eftirfarandi skref hjálpa þér að treysta því að allt virki sem skyldi. 

1. Stofna eða auðkenna tvo prufunotendur (A og B).

   - Prufunotandi A verður að vera með Business Central-leyfi og Microsoft 365 leyfi með aðgang að Teams.
   - Prufunotandi B verður að vera aðeins með Microsoft 365 leyfi með aðgang að Teams.

2. Skráðu þig inn í vefbiðlara Business Central sem prufunotandi A.

   1. Opnaðu færslu sem prufunotandi B á að hafa aðgang að, t.d. **Birgðaspjald** í viðeigandi fyrirtæki eða umhverfi.
   2. Veldu **Deila** ![!Deildu með öðrum forritum á síðum.](media/share-icon.png) > **Deila með Teams** til að fá upp gluggann „Deila með Teams“.
   3. Í reitnum **Deila með** skaltu bæta við prufunotanda B sem viðtakanda. 
   4. Bíddu eftir að tengillinn stækki í spjald og veldu „Deila“. 

3. Skráðu þig inn í Microsoft Teams sem prufunotandi B.

   1. Veldu „Spjalla“ og opnaðu samtalið með prufunotanda A. 
   2. Veldu upplýsingahnappinn á spjaldinu í skilaboðunum sem prufunotandi A sendi. Uppsetningin tókst ef Business Central-biðlarinn er sýndur og er ritvarinn. 

> [!TIP]
> Fór eitthvað úrskeiðis? Athugaðu [Úrræðaleita aðgang með Microsoft 365 leyfum](admin-access-with-m365-license-troubleshooting.md).

## <a name="see-also"></a>Sjá einnig .

[Aðgangur að Business Central með Microsoft 365 leyfum](admin-access-with-m365-license.md#minimum-requirements)  
[Úrræðaleita aðgang með Microsoft 365 leyfum](admin-access-with-m365-license-troubleshooting.md)  
[Business Central og Microsoft Teams samþætting](across-teams-overview.md)  