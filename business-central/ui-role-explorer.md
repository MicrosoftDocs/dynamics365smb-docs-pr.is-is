---
title: Skoða og fletta í síðum eftir hlutverki
description: Hægt er að fá yfirlit yfir alla viðskiptaeiginleikana sem eru tiltækir fyrir hlutverkið þitt og önnur hlutverk með hlutverkaleitinni.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'role explorer, find features, navigate'
ms.search.form: 'RoleExplorer, 9020, 9022, 9027, 9024'
ms.date: 08/01/2021
ms.author: jswymer
ms.service: dynamics-365-business-central
---

# Að finna síður með hlutverkaleit

Hægt er að fá yfirlit yfir alla viðskiptaeiginleikana sem eru tiltækir fyrir þitt hlutverk, og fyrir önnur hlutverk ef farið er skrefi lengra. Í eftirfarandi fylgigögnum er þetta yfirlit yfir eiginleika kallað *Hlutverkaleit*.

Hver eining á hlutverkaleit er aðgerð sem opnar síðu. Í samræmi við það er einnig hægt að nota hlutverkaleitina sem leið til að fletta í [!INCLUDE[prod_short](includes/prod_short.md)].

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## Opnið hlutverkaleitina

Hægt er að opna hlutverkaleit úr Mitt hlutverk og öllum listasíðum og úr **Viðmótsleit** .

- Í Mitt hlutverk eða einhverri listasíðu skal velja ![Valmyndarhnappinn.](media/ui_menu_button.png "Valmyndarhnappur") Hnappinn hægra megin við yfirlitsreinina eða velja  <kbd>Shift</kbd>+<kbd>F12</kbd>.
- Í glugganum **Viðmótsleit** skaltu velja aðgerðina **skoða** neðst.

Þegar hlutverkamiðstöðin er opnuð í fyrsta sinn sýnir hún tengla á flesta eiginleika sem eru í boði fyrir hlutverkið þitt.

## Flettieiginleikar

Aðgerðunum sem opna síður er raðað undir hnútum sem nefndir eru eftir eiginleikum eða kerfishlutum. Hægt er að draga saman eða víkka út hvern hnút fyrir sig og alla í einu.

- Til að stækka/minnka einstaka hnúta skal velja hnútinn. Þetta á við um hnúta á efsta stigi og undirhnúta.
- Til að stækka/minnka alla hnúta á efsta stigi á síðunni, en skilja undirhnútana eftir eins og þeir eru, skal velja **...** efst uppi, síðan velja **Stækka** eða **Minnka**.
- Til að stækka/minnka alla hnúta á efsta stigi og alla undirhnúta undir þeim skal velja **...** efst uppi, síðan velja aðgerðina **Stækka allt** eða **Minnka allt**.

## Leita að eiginleikum

Til að finna eiginleika á fljótlegan hátt skal velja **Leita**, síðan slá inn orð eða setningu fyrir eiginleikann sem leitað er að. Hlutverkamiðstöðin mun auðkenna alla samsvörun í texta. Ef eiginleiki er falinn í samandregnum hnút er samandreginn hnútur merktur sem punktur. 

## Kanna önnur hlutverk

Til að skoða önnur hlutverk en þitt eigið skaltu velja **Kanna fleiri hlutverk**. Hlutverkamiðstöðin sýnir hvert hlutverk fyrir sig undir eigin fyrirsögn með tenglum á eiginleika þeirra. Síðan er hægt að fletta og finna eiginleika rétt eins og gert er þegar hlutverk eru könnuð.

> [!NOTE]
> Þú sérð aðeins hlutverk sem eru sett þannig upp að þau sjáist í hlutverkaleitinni. Þannig að ef þú sérð ekki hlutverk sem þú bjóst við að sjá er það líklega ekki sett þannig upp. Frekari upplýsingar eru í [Unnið með forstillingar](admin-users-profiles-roles.md). 

Þegar önnur hlutverk eru skoðuð er einnig hægt að þrengja leitina með því að nota aðgerðirnar **Skýrslur og greiningar** og **Stjórnun** efst í hlutverkamiðstöðinni.

- **Skýrslur og greiningar** sýnir aðeins eiginleikana sem eru flokkaðir sem skýrslu- og greiningareiginleikar.
- **Stjórnun** sýnir aðeins eiginleikana sem eru flokkaðir sem stjórnunareiginleikar.

> [!TIP]
> Fyrir þróunaraðila eru síður og skýrslur flokkaðar með því að stilla eiginleika [UsageCategory](/dynamics365/business-central/dev-itpro/developer/properties/devenv-usagecategory-property) í AL-kóða hlutarins.
<!--
 
## Role explorer actions

There a several actions along the top of the role explorer to help you locate features of your role and other roles.

|Action|Description|
|------|------|
|**All**|Shows all features that are related to the role.|
|**Find**|Lets you enter a word or phrase to quickly locate feature names that match.|
|**Explore more roles**|All business features that are available for all roles including your own. When exploring all roles, the other actions work the same way, except for all roles shown. **NOTE:** You will only see roles that are set up to show in role explorer. For more information, see [Manage Profiles](admin-users-profiles-roles.md).  |
|**Report & Analysis**|This action Shows only those features that are categorized as reports and analysis features.|
|**Administration**|Shows only those features that are categorized as administration features.|



<!--
Choose the **Find** action at the top of the role explorer to quickly locate feature names that contain a certain term.

Choose the **Explore more roles** action at the top of the role explorer to get an overview of all business features that are available for all roles including your own.

> [!NOTE]
> Only Role Center actions for profiles where the **Show in Role Explorer** check box is selected will appear on the extended version of the role explorer (shown with the **Explore more roles** action). For more information, see [Manage Profiles](admin-users-profiles-roles.md).
-->

## Stækka og minnka hnúta í hlutverkaleitinni

Aðgerðunum sem opna síður er raðað undir hnútum sem nefndir eru eftir eiginleikum eða kerfishlutum. Hægt er að draga saman eða víkka út hvern hnút fyrir sig og alla í einu.

- Til að víkka út/draga saman hnút skal velja hnútinn. Þetta á við um hnúta á efsta stigi og undirhnúta.
- Til að víkka/draga saman alla helstu hnúta á síðunni skaltu velja **Víkka** eða **Draga saman** aðgerðina efst í hægra horninu.
- Til að víkka/draga saman allan efsta hnút og alla undirhnúta undir honum skal gera eitt af eftirfarandi:
  -  <kbd>Veljið CTRL</kbd>+<kbd>Shift</kbd>  lyklana á meðan þú velur  **aðgerðina víkka**  eða  **fella**  inn efst í hægra horninu.
  - Veldu **...** efst í hægra horninu, Veldu svo aðgerðina **Útvíkka allt** eða **Fella allt saman**.

## Sjá einnig
[Finndu síður og upplýsingar með Viðmótsleit](ui-search.md)  
[Vinna með forstillingar](admin-users-profiles-roles.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]