---
title: Stjórna vistuðum stillingum fyrir skýrslur og runuvinnslur
description: Lýsir hwo admin getur sett upp fyrirfram skilgreinda valkosti og afmarkanir fyrir skýrslu og samnýtt þær stillingar með einum eða öllum notendum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 12/21/2021
ms.author: edupont
ms.openlocfilehash: 289603bcfb11b50711a854c355a99781a8e77264
ms.sourcegitcommit: 8837ed2aeb454806e153145c675cf049a020ea38
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944074"
---
# <a name="manage-saved-settings-for-reports-and-batch-jobs"></a>Stjórna vistuðum stillingum fyrir skýrslur og runuvinnslur

Þegar skýrslur eru keyrðar er notendum yfirleitt sýnd síða sem gerir þeim kleift að velja valkosti og síur fyrir breytingar á gögnum sem eru í mynduðu skýrslunni. Þessi síða heitir *beiðssían*. Skýrsla getur innihaldið eitt eða fleiri *vistaðar stillingar* sem notendur geta notað á skýrsluna úr beiðnisíðunni. *Vistuð stillingar* eru skoðaður fyrirfram skilgreind valkosti og afmarkanir. Notkun vistaðra stillinga er fljótleg og áreiðanleg leið til að búa til skýrslur sem innihalda rétt gögn. Frekari upplýsingar fást með því að [nota sjálfgefnar gildi fyrir forskilgreindar stillingar](ui-work-report.md#SavedSettings).

> [!NOTE]
> Þetta efnisatriði vísar í *skýrslur* en svipaðar upplýsingar eiga við um *runuvinnslur*.

Ef réttar heimildir eru til staðar er hægt að skoða, stofna og breyta vistuðum stillingum fyrir allar skýrslur fyrir alla notendur í fyrirtækinu. Hægt er að úthluta vistuðum stillingum fyrir skýrslu fyrir einstaka notendur eða alla notendur í fyrirtækinu.

## <a name="manage-saved-settings"></a>Stjórna vistuðum stillingum

Þú hefur umsjón með vistuðum stillingum á síðunni **Stillingar skýrsla**. Tvær aðferðir til að opna þessa síða:

- Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Stillingar skýrslu** og velja síðan viðkomandi tengil.
- Í beiðssíðu skýrslu skal velja uppflettinguna í **reitnum nota sjálfgefin gildi frá** svæðinu og velja svo **valið í Full list** aðgerð.

    Þetta svæði er aðeins sýnilegt hafi skýrslan verið keyrð að minnsta kosti einu sinni áður. Listinn sýnir aðeins þær stillingar sem eru tiltækar, annaðhvort vegna þess að þær eru þínar eigin stillingar, eða vegna þess að stillingarnar eru samnýttar með þér.

**Síðan Skýrslustillinga-** síða sýnir allar vistaðar stillingarstillingar fyrir alla notendur. Ef notandanafn er í **Úthlutað til** reitnum getur aðeins sá notandi notað vistuðu stillingarnar fyrir tengda skýrslu. Ef gátmerki er í **Deila með öllum notendum** reitnum geta allir notendur notað vistuðu stillingarnar fyrir skýrslu.  

> [!TIP]
> Þegar notandi hefur keyrt skýrslu sem styður samnýttar stillingar eru stillingarnar vistaðar og þeim bætt við þennan lista. Í flestum tilfellum getur admin breytt þeim stillingum og valið að samnýta stillingarnar með öllum notendum.
>
> Í sumum tilfellum er þó ekki hægt að samnýta stillingar og admin getur ekki breytt þeim heldur. Flestar runuvinnslur styðja ekki samnýttar stillingar.  

## <a name="create-or-modify-saved-settings-for-all-users"></a>Stofna eða breyta vistuðum stillingum fyrir alla notendur

Á síðunni **Skýrslustillingar** er hægt að:

- Veljið aðgerðina **Nýtt** til að stofna nýja færslu fyrir vistaðar stillingar frá grunni.
- Veljið færslu fyrir vistaðar stillingar af listanum og veljið aðgerðina **Afrita** til að búa til afrit.
- Veljið færslu fyrir vistaðar stillingar af listanum og veljið aðgerðina **Breyta** til að breyta færslu fyrir vistaðar stillingar.

> [!Important]
> Íhugaðu nafnið sem þú gefur færslu fyrir vistaðar stillingar. Ef þú býrð til færslu fyrir vistaðar stillingar fyrir alla notendur og þú gefur henni sama heiti og fyrirliggjandi færslu fyrir vistaðar stillingar sem er úthlutað á tiltekinn notanda, mun sá notandi ekki geta notað færsluna fyrir vistaðar stillingar sem er úthlutað á alla.  Undir **Vistaðar stillingar** á beiðnisíðu skýrslunnar mun notandinn sjá tvær vistaðar stillingar með sama heiti. Notandaskilgreinda færslan fyrir vistaðar stillingar verður notuð, sama hvor valmöguleikinn er valinn.

> [!NOTE]
> Möguleikinn á að vista stillingar er aðeins tiltækur á skýrslum þar sem [eiginleikinn savevalues](/dynamics365/business-central/dev-itpro/developer/properties/devenv-savevalues-property) á beiðssíðu skýrslunnar er stilltur á **Já**. **Eiginleikinn savevalues** er stilltur af sem verktaki.  

## <a name="see-also"></a>Sjá einnig

[Unnið með skýrslur, runuvinnslur og XMLports](ui-work-report.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]