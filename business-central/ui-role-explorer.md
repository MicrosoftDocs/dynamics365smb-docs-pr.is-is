---
title: Skoða og fletta síðum og skýrslum eftir hlutverkum
description: Hægt er að fá yfirlit yfir alla viðskiptaeiginleikana sem eru tiltækir fyrir hlutverkið þitt og önnur hlutverk með hlutverkaleitinni.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'role explorer, find features, navigate'
ms.search.form: 'RoleExplorer, 9020, 9022, 9027, 9024'
ms.date: 07/15/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---

# Leita að síðum og skýrslum með hlutverkavafranum

Hægt er að fá yfirlit yfir alla viðskiptaeiginleikana sem eru tiltækir fyrir þitt hlutverk, og fyrir önnur hlutverk ef farið er skrefi lengra. Þessi grein vísar til aðgerðayfirlitsins sem *hlutverkavafrann*.

Hver eining í hlutverkavafranum er aðgerð sem opnar síðu eða skýrslu. Í samræmi við það er einnig hægt að nota hlutverkaleitina sem leið til að fletta í [!INCLUDE[prod_short](includes/prod_short.md)].

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## Opnið hlutverkaleitina

Hægt er að opna hlutverkavafra úr hlutverkamiðstöðinni og öllum listasíðum og í **glugganum Segja mér** .

- Á mínu hlutverki eða á listasíðunni er hnappurinn ![Valmynd valinn.](media/ui_menu_button.png "Valmyndarhnappur") Hægra megin við yfirlitsstiku eða Shift <kbd>F12 valið</kbd>+<kbd></kbd>.
- Í glugganum **Viðmótsleit** skaltu velja aðgerðina **skoða** neðst.

Þegar hlutverkamiðstöðin er opnuð í fyrsta sinn sýnir hún tengla á flesta eiginleika sem eru í boði fyrir hlutverkið þitt.

## Opna hlutverkavafra sem er afmarkaður til að sýna skýrslur 

Hægt er að opna hlutverkavafra í yfirliti sem er afmarkað til að sýna skýrslur frá hlutverkinu og öllum listasíðum og í **glugganum Tell Me** :

- Á mínu hlutverki eða á listasíðunni skal velja **Allar skýrslur**  tengja hægra megin við yfirlitsstiku.
-  **Í glugganum Segja mér** skal velja **aðgerðina Skoða skýrslur** neðst.

## Flettieiginleikar

Aðgerðum sem opnar síður eða skýrslur er raðað undir hnútum sem nefndir eru eftir aðgerðunum eða kerfishlutunum. Hægt er að fella saman eða stækka hvern hnút sérstaklega eða alla hnúta saman.

- Til að stækka/minnka einstaka hnúta skal velja hnútinn. Þetta á við um hnúta á efsta stigi og undirhnúta.
- Til að stækka/minnka alla hnúta á efsta stigi á síðunni, en skilja undirhnútana eftir eins og þeir eru, skal velja **...** efst uppi, síðan velja **Stækka** eða **Minnka**.
- Til að stækka/minnka alla hnúta á efsta stigi og alla undirhnúta undir þeim skal velja **...** efst uppi, síðan velja aðgerðina **Stækka allt** eða **Minnka allt**.

## Leita að eiginleikum

Til að finna aðgerðir á fljótlegan hátt skal velja **Finna**, rita síðan orð eða orðasambandi fyrir eiginleikann sem leitað er að. Mitt hlutverk merkir hvaða texta sem er. Ef eiginleiki er falinn í felldum hnút er fellihnúturinn merktur með hnút. 

## Kanna önnur hlutverk

Til að skoða önnur hlutverk en þitt eigið skaltu velja **Kanna fleiri hlutverk**. Hlutverkamiðstöðin sýnir hvert hlutverk fyrir sig undir eigin fyrirsögn með tenglum á eiginleika þeirra. Þú getur fundið og farið í eiginleika eins og þú gerir þegar þú skoðar hlutverk þitt.

> [!NOTE]
> Aðeins fæst aðgangur að hlutverkum sem eru sett upp til að birta í hlutverkavafranum. Ef hlutverk er ekki tiltækt er það líklega ekki sett upp fyrir það. Frekari upplýsingar eru í [Unnið með forstillingar](admin-users-profiles-roles.md). 

Þegar önnur hlutverk eru skoðuð er einnig hægt að þrengja niður skoðanakannanir með því að nota **aðgerðirnar Skýrsla & Greining** og **Stjórnun** efst í hlutverkamiðstöðinni.

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
|**Explore more roles**|All business features that are available for all roles including your own. When exploring all roles, the other actions work the same way, except for all roles shown. **NOTE:** You can only access roles that are set up to show in role explorer. For more information, see [Manage Profiles](admin-users-profiles-roles.md).  |
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
  -  <kbd>Velja skal Ctrl-vaktarlyklana</kbd>+<kbd></kbd> á meðan aðgerðin **Stækka** eða **Fella** saman í efra hægra horni.
  - Veldu **...** efst í hægra horninu, Veldu svo aðgerðina **Útvíkka allt** eða **Fella allt saman**.

## Sjá einnig .

[Finndu síður og upplýsingar með Viðmótsleit](ui-search.md)  
[Vinna með forstillingar](admin-users-profiles-roles.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
