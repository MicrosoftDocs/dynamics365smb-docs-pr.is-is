---
title: Setja upp aðgang með Microsoft 365 leyfum
description: Leiðarvísir um hvernig stjórnendur geta samskipað aðgangi að Viðskiptamiðinu með Microsoft 365 leyfum.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 11/03/2022
ms.custom: bap-template
ms.search.keywords: License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams
ms.openlocfilehash: f509c0a8bf5e9320eb0f2712863984221b7138b9
ms.sourcegitcommit: 61fdaded30310ba8bdf95f99e76335372f583642
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/04/2022
ms.locfileid: "9745104"
---
# <a name="set-up-access-with-microsoft-365-licenses"></a>Setja upp aðgang með Microsoft 365 leyfum 

Stjórnendur verða að ljúka mörgum verkþáttum áður en notendur geta fengið aðgang að Viðskiptamiðinu með sínu Microsoft 365 leyfi. Skrefin hér að neðan tákna lágmarksskipulag sem þarf til að byrja.  

## <a name="deploy-the-business-central-app-for-teams"></a>Virkjaðu Viðskiptablaðið Central App fyrir hópana 

Til að fá handhafa aðalleyfis til að deila gögnum í teymum, og fyrir Microsoft 365 leyfisveitahópa til að nálgast þessi gögn, þarf hver um sig að hafa viðskipti miðlægt App fyrir teymi uppsett. Þrátt fyrir að notendur geti sett upp App með sér er mælt með því að stjórnendur noti miðlæga virkjun. Miðlæg innleiðing gerir þér kleift að fara út í app til að breikka áhorfendur þvert á skipulag og lágmarka einstaka notendaviðleitni. 

Til að læra hvernig á að nota forritið Central App fyrir teymum, má sjá [Setja upp Business Central App með miðstýringu innleiðingar](admin-teams-integration.md#installing-the-business-central-app-by-using-centralized-deployment).

> [!NOTE]
> Ef keyrð hefur verið miðlæg innleiðing áður og forritið virkjað það í öryggisflokki leyfðra miðlægrar notendanna þarf að keyra það aftur til að virkja fleiri flokka eða allt skipulagið eftir því hvernig aðgangur er skilgreindur.

> [!TIP]
> Ertu að leita að fljótari leið til að byrja þegar þú reynir á þessa aðgerð? Prófunarnotendur geta sett upp app á [aka.ms/BCgetTeamsApp](https://aka.ms/BCgetTeamsApp).

## <a name="configure-permissions"></a>Skilgreina heimildir

Viðskiptamiðið er öruggt með því að hanna og lágmarka áhættu með því að Microsoft 365 veita ekki heimildir notendum út úr kassanum. Kerfisstjórar verða að samskipa hlutaheimildum sem ákvarða hvaða töflur, síður og skýrslur er hægt að nálgast í teymum með aðeins Microsoft 365 leyfi. Þessar heimildir eru þær upphafsheimildir sem úthlutað er þegar notandi undirritar í fyrsta sinn með leyfi sínu Microsoft 365. 

Uppsetning upphafsheimilda:

1. Í Viðskiptamiðinu er leitað að **skilgreiningu** leyfis.
2. Microsoft 365 Veljið leyfið.
3. Efst á **Microsoft 365** leyfissíðum er valið ![teiknið Breyta Edit ](media/edit-pencil.png) og síðan er kveikt á **Sérsníða heimildir**. 
4. **Í sérsnilega kaflanum um sérsniðin leyfi** er bætt við viðeigandi heimildum og valið hvort þau eiga við um stök fyrirtæki eða öll fyrirtæki innan umhverfisins.

> [!NOTE]
> Þegar Notendalisti samstillir í aðalleyfi með notendum Microsoft 365 er samstilltar er aðeins notendum sem eru með starfsleyfi og seðlabanka bætt við notendalista seðlabanka. Notendur með aðeins Microsoft 365 leyfi bætast við lista notenda þegar þeir nálgast viðskipti miðlægt í fyrsta sinn. Frekari upplýsingar eru að búa til hjá [notendum samkvæmt leyfum](ui-how-users-permissions.md).

> [!TIP]
> Ertu að leita að fljótari leið til að byrja þegar þú reynir að koma þessum eiginleika sandkassa eða matsfyrirtækis á framfæri? **Úthlutið D365 lestrarheimildasamstæðu** sem veitir heimild til flestra hluta.  

Þegar unnið er með mörg umhverfi verður Skilgreining leyfis að gilda fyrir hvert umhverfi fyrir sig og getur verið mismunandi í hverju umhverfi. 

Frekari upplýsingar um [Úthlutun heimilda til notenda og hópa](ui-define-granular-permissions.md) og [semja heimildasöfn](/dynamics365/business-central/dev-itpro/developer/devenv-permissionset-composing).

## <a name="turn-on-access-with-microsoft-365-licenses"></a>Kveikja á aðgangi með Microsoft 365 leyfum

Sjálfgefið er að aðgangur með Microsoft 365 leyfi er sjálfgefinn. Virkja þarf aðgang fyrir hvert umhverfi fyrir sig, gefa stjórnendum stjórn og leyfa fyrir sviðsstýrinu þvert á fyrirtækið. Þú kveikir á aðgangi með því að nota Business miðlægu stjórnendamiðstöð: 

1. Í efra hægra horninu skal velja **stillingar**![.](media/ui-experience/settings_icon_small.png "Stillingatákn fyrir hlutverkamiðstöð") > **Stjórnun miðstöðvarinnar**.  
2. Í admin Center velurðu  **umhverfi** og velur síðan umhverfið þar sem þú vilt breyta aðgangsheimilandi aðgangi. 
3. **Á upplýsingasíðu um umhverfið** velurðu **Modify** fyrir **aðganginn með Microsoft 365 leyfi** stilling.
4. **Microsoft 365 Kveikt er á rofann í rúðunni leyfi**. 
5. Velja **Save** þegar það er gert og samþykkja staðfestinguna. Breytingin kemur í gildi strax.

## <a name="test-your-setup"></a>Prófa uppsetninguna

Til að sannreyna að uppsetningin sé tilbúin fyrir framleiðsluna hjálpar eftirfarandi skref til við að byggja upp traustið sem allt virkar eins og það á að vera. 

1. Stofna eða auðkenna tvo Reynandi notendur (A og B).

   - Prófunarnotandi A skal hafa Aðalstarfsleyfi og Microsoft 365 leyfi fyrir aðgang að teymum.
   - Prófunarnotandi B þarf að hafa einungis Microsoft 365 leyfi með aðgangi að teymum.

2. Skráðu þig inn í Aðalvefbiðlara Viðskiptamiðis sem prófa notanda A.

   1. Opna skal færslu sem prófunarnotandi B ætti að hafa aðgang að, svo sem **Birgðaspjald** í viðeigandi fyrirtæki og umhverfi.
   2. Veldu **Share**![ ! Samnýta í önnur forrit aðgerðir á síðum.](media/share-icon.png) > **Samnýta í teymum** til að koma upp glugganum samnýta í teymi.
   3. **Í reitnum samnýta á** skal bæta við Prófunarnotanda B sem viðtakanda. 
   4. Bíddu með því að tengja til að stækka við spjald og velja Share. 

3. Skrá inn Microsoft Teams sem prófunarnotanda B.

   1. Veldu spjall og Opnaðu samtalið með reynslunotendum A. 
   2. Í skilaboðunum sem eru send með Test notandasíðu sinni skaltu velja hnappinn upplýsingar á spjaldinu. Ef Aðalviðskiptavinur fyrirtækisins birtist og er skrifvarin þá heppnaðist Uppsetning þín vel. 

> [!TIP]
> Eitthvað fór úrskeiðis? [Skoðaðu úrræðaleit með Microsoft 365 leyfum](admin-access-with-m365-license-troubleshooting.md).

## <a name="see-also"></a>Sjá einnig .

[Aðgangur að miðborg með Microsoft 365 leyfum](admin-access-with-m365-license.md#minimum-requirements)  
[Úrræðaleit vegna aðgangs með Microsoft 365 leyfi](admin-access-with-m365-license-troubleshooting.md)  
[Rekstur miðsvæðis og Microsoft Teams Samþætting](across-teams-overview.md)  