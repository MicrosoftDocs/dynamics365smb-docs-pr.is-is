---
title: Stjórna vistuðum stillingum fyrir skýrslur og keyrslur
description: Lýsir því hvernig stjórnandi getur sett upp fyrirframskilgreinda valkosti og síur fyrir skýrslu og deilt stillingunum með einum eða öllum notendum.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'customization, personalization'
ms.date: 12/21/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Stjórna vistuðum stillingum fyrir skýrslur og keyrslur

Þegar skýrslur eru keyrðar er notendum yfirleitt sýnd síða sem gerir þeim kleift að velja valkosti og síur fyrir breytingar á gögnum sem eru í mynduðu skýrslunni. Þessi síða er kölluð *beiðnisíða*. Skýrsla getur innihaldið eitt eða fleiri *vistaðar stillingar* sem notendur geta notað á skýrsluna úr beiðnisíðunni. *Vistuð stillingar* eru skoðaður fyrirfram skilgreind valkosti og afmarkanir. Notkun vistaðra stillinga er fljótleg og áreiðanleg leið til að búa til skýrslur sem innihalda rétt gögn. Frekari upplýsingar eru í [Nota vistaðar stillingar](ui-work-report.md#SavedSettings).

> [!NOTE]
> Þetta efnisatriði á við um *skýrslur* en svipaðar upplýsingar eiga við um *runuvinnslur*.

Ef réttar heimildir eru til staðar er hægt að skoða, stofna og breyta vistuðum stillingum fyrir allar skýrslur fyrir alla notendur í fyrirtækinu. Hægt er að úthluta vistuðum stillingum fyrir skýrslu fyrir einstaka notendur eða alla notendur í fyrirtækinu.

## Stjórna vistuðum stillingum

Þú hefur umsjón með vistuðum stillingum á síðunni **Stillingar skýrsla**. Tvær aðferðir til að opna þessa síða:

- Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Stillingar skýrslu** og velja síðan viðkomandi tengil.
- Á beiðnisíðu skýrslu skal velja uppflettingu í reitnum **Nota sjálfgildi úr** og velja svo aðgerðina **Velja úr öllum listanum**.

    Þessi reitur er aðeins sýnilegur ef búið er að keyra skýrsluna a.m.k. einu sinni áður. Listinn mun aðeins sýna stillingar sem standa þér til boða, annaðhvort vegna þess að þær eru þínar eigin stillingar eða vegna þess að stillingunum er deilt með þér.

Síðan **Skýrslustillingar** birtir allar fyrirliggjandi vistaðar stillingafærslur fyrir alla notendur. Ef notandanafn er í **Úthlutað til** reitnum getur aðeins sá notandi notað vistuðu stillingarnar fyrir tengda skýrslu. Ef gátmerki er í **Deila með öllum notendum** reitnum geta allir notendur notað vistuðu stillingarnar fyrir skýrslu.  

> [!TIP]
> Þegar notandi hefur keyrt skýrslu sem styður samnýttar stillingar eru stillingar hans vistaðar og þeim bætt við þennan lista. Í flestum tilvikum getur stjórnandi þá breytt þessum stillingum og valið að deila þeim með öllum notendum.
>
> Í sumum tilvikum er þó ekki hægt að deila stillingum og stjórnandi getur ekki heldur breytt þeim. Flestar runuvinnslur styðja ekki samnýttar stillingar.  

## Stofna eða breyta vistuðum stillingum fyrir alla notendur

Á síðunni **Skýrslustillingar** er hægt að:

- Veljið aðgerðina **Nýtt** til að stofna nýja færslu fyrir vistaðar stillingar frá grunni.
- Veljið færslu fyrir vistaðar stillingar af listanum og veljið aðgerðina **Afrita** til að búa til afrit.
- Veljið færslu fyrir vistaðar stillingar af listanum og veljið aðgerðina **Breyta** til að breyta færslu fyrir vistaðar stillingar.

> [!Important]
> Íhugaðu nafnið sem þú gefur færslu fyrir vistaðar stillingar. Ef þú býrð til færslu fyrir vistaðar stillingar fyrir alla notendur og þú gefur henni sama heiti og fyrirliggjandi færslu fyrir vistaðar stillingar sem er úthlutað á tiltekinn notanda, mun sá notandi ekki geta notað færsluna fyrir vistaðar stillingar sem er úthlutað á alla.  Undir **Vistaðar stillingar** á beiðnisíðu skýrslunnar mun notandinn sjá tvær vistaðar stillingar með sama heiti. Notandaskilgreinda færslan fyrir vistaðar stillingar verður notuð, sama hvor valmöguleikinn er valinn.

> [!NOTE]
> Getan til að vista stillingar er aðeins í boði í skýrslum þar sem eiginleikinn [SaveValues](/dynamics365/business-central/dev-itpro/developer/properties/devenv-savevalues-property) fyrir beiðnisíðu skýrslunnar er stillt á **Já**. Eiginleikinn **SaveValues** er stilltur af þróunaraðila.  

## Sjá einnig

[Vinna með skýrslur, runuvinnslur og XMLports](ui-work-report.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]