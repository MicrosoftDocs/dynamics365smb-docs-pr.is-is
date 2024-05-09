---
title: Nota Excel til að flytja inn gögn
description: Sjálfgefinn grunnstillingarpakki er notaður til að bæta við viðskiptamenn í Excel og flytja inn gögnin aftur í Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'migration, Excel'
ms.date: 04/26/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Flytja inn viðskiptagögn úr öðrum fjármálakerfum

Þegar notandi skráir sig í [!INCLUDE[prod_short](includes/prod_short.md)], er hægt að ákveða að búa til autt fyrirtæki svo hægt sé að hlaða upp eigin gögnum og prófa áfram nýja [!INCLUDE[prod_short](includes/prod_short.md)] fyrirtækið. Það fer eftir því fjárhagskerfi sem fyrirtækið notar í dag hvernig og hvort hægt er að millifæra upplýsingar um viðskiptamenn, lánardrottna, birgðir og bankareikninga.  

Hægt er að ræsa leiðarvísi um uppsetningu með hjálp frá Mitt hlutverk sem hjálpar til við að flytja viðskiptagögn úr Excel-skrá eða öðrum sniðum. Þær skráategundir sem hægt er að hlaða upp fer eftir viðbótunum sem í boði eru. Til dæmis er hægt að yfirfæra gögn úr QuickBooks vegna þess að [!INCLUDE[prod_short](includes/prod_short.md)] felur í sér viðbót sem sér um umbreytingu úr QuickBooks. Ef notandi vill yfirfæra gögn úr öðrum fjárhagskerfum þarf annað hvort að athuga hvort viðbót er í boði fyrir það kerfi eða flytja gögnin inn úr Excel.  

[!INCLUDE[prod_short](includes/prod_short.md)] inniheldur sniðmát fyrir viðskiptamenn, lánardrottna og birgðavörur sem hægt er að nota þegar gögnum er hlaðið upp. Til að flytja inn myndir af vörum er hægt að nota þar til gerða aðgerð á síðunni **Uppsetning birgða**. Frekari upplýsingar er að finna í [Flytja inn margar vörumyndir](inventory-how-import-item-pictures.md).

> [!TIP]  
> Mælt er með því að nota leiðsagnarforrit fyrir gagnafærslu til að flytja inn gögn frá Dynamics GP, Dynamics NAV eða QuickBooks. Frekari upplýsingar er að finna í [Flytja innanhússgögn í Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) í stjórnendaefninu eða [QuickBooks-gagnaflutning](ui-extensions-quickbooks-data-migration.md).

## Vinna með gögn í Excel

Hægt er að nota Excel-innbótina til að útbúa fyrirliggjandi efni til að nota í [!INCLUDE [prod_short](includes/prod_short.md)]. Frekari upplýsingar er að finna í [Skoða og breyta í Excel úr Business Central](across-work-with-excel.md).  

## Flytja inn gögn úr grunnstillingarpakka

Fyrir stærri innleiðingarverk geturðu sett upp lausnamiðaða grunnstillingapakka. Frekari upplýsingar eru í [Setja upp grunnstillingarpakka fyrirtækis](/dynamics365/business-central/dev-itpro/administration/set-up-standard-company-configuration-packages) (aðeins á ensku) í stjórnendaefninu.  

> [!NOTE]  
> Að vinna með grunnstillingapakka er ítarleg aðgerð og við mælum með að þú hafir samband við endursöluaðila þinn. Frekari upplýsingar eru í [Setja upp grunnstillingu fyrirtækis](/dynamics365/business-central/dev-itpro/administration/set-up-standard-company-configuration-packages) (aðeins á ensku).

Hægt er að flytja aðalgögn og sum færslugögn úr öðrum fjárhagskerfum á grundvelli sjálfgefins grunnstillingarpakka í [!INCLUDE[prod_short](includes/prod_short.md)]. Á síðunni **Grunnstillingarpakkar** er hægt að vinna með pakka til að flytja inn og staðfesta gögnin áður en pakkinn er notaður. Til dæmis er hægt að flytja grunnstillingapakkann út í Excel og setja gögnin þar upp. Síðan er hægt að flytja aftur inn gögnin úr Excel. Pakkinn samanstendur af 27 töflum, þar með talið aðalgögnum, svo sem viðskiptavinum, söluaðilum, hlutum og reikningum, öðrum grunnuppsetningartöflum eins og sendingarkostnaði og viðskiptatöflum eins og söluhaus og línum.  

Þegar sjálfgefinn grunnstillingarpakki er fluttur út í Excel inniheldur vinnubókin sem búin er til vinnublað fyrir hverja töflu í pakkanum. Til að einfalda verk er hægt að nýta XML-meðhöndlunarverkfærin sem byggð eru inn í Excel. Einnig er hægt að nota Excel innbyggðar aðgerðir til aðstoða við gagnsnið og að setja gögn í réttan flokk. Til dæmis, bætið við auðu vinnublaði og afritið eldri gögnin á það. Búið því næst til Excel-formúlu til að varpa gögnum í umbreytingarvinnublaðinu á milli reitanna í útflutta vinnublaðinu og eldri gögnum viðskiptamanns. Þegar búið er að varpa öllum gögnum, skal afrita afmörkun gagnanna á töflu á vinnublaðinu.  

> [!IMPORTANT]  
> Ekki breyta dálkum í vinnublöðunum. Ef gögnin eru færð, þeim breytt eða þeim eytt er ekki hægt að flytja vinnublaðið inn í [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Ekki er hægt að flytja út/flytja inn svæði af gerðinni Blob með Excel.

### Töflur í sjálfgefnum grunnstillingarpakka

Sjálfgefni grunnstillingarpakkinn styður eftirfarandi töflur:

- Greiðsluskilmálar
- Verðflokkur viðskiptamanna
- Afhendingarmáti
- Sölumaður/innkaupaaðili
- Birgðageymsla
- Fjárhagsreikningur
- Viðskiptavinur
- Lánardrottinn
- Atriði
- Söluhaus
- Sölulína
- Innkaupahaus
- Innkaupalína
- Almenn Færslubókarlína
- Birgðabókarlína
- Bókunarflokkur viðskm.
- Bókunarflokkur lánardr.
- Birgðabókunarflokkur
- Mælieining
- Almenn Viðskiptabókunarflokkur
- Almenn Afurðarbókunarflokkur
- Almennur bókunargrunnur
- Umsjónarsvæði
- Vöruflokkur
- Söluverð
- Innkaupsverð

## Sjá einnig

[Að flytja innanhússgögn í Business Central Online (aðeins á ensku)](/dynamics365/business-central/dev-itpro/administration/migrate-data)  
[Setja upp grunnstillingapakka fyrirtækis](/dynamics365/business-central/dev-itpro/administration/set-up-standard-company-configuration-packages)  
[QuickBooks gagnaflutningur](ui-extensions-quickbooks-data-migration.md)  
[Flytja inn margar vörumyndir](inventory-how-import-item-pictures.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]