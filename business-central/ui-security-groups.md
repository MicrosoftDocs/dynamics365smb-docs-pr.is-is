---
title: Stjórna aðgangi með öryggisflokkum
description: Í greininni er því lýst hvernig nota á öryggishópa til að skilgreina notendaleyfi.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'access, right, security, permissions'
ms.search.form: '1, 119, 8930, 9800, 9807, 9808, 9830, 9831, 9802, 9855, 9862'
ms.date: 02/08/2023
---

# Stjórna aðgangi að starfrækslu miðsvæðis með öryggisflokkum

[!INCLUDE [2023rw1-sec-group-long](includes/2023rw1-sec-group-long.md)]

Öryggisflokkar auðvelda stjórnendum að stjórna notendaleyfi í Dynamics 365 forritum, svo sem  SharePoint  netinu,  CRM Online og netútgáfunni af [!INCLUDE [prod_short](includes/prod_short.md)]. Stjórnendur bæta við heimildum til að sinna öryggishópum og þegar þeir bæta við notendum í hópinn heimildin gildir um alla félagsmenn. Til dæmis getur kerfisstjóri stofnað öryggisflokk sem gefur söluaðilum möguleika á að stofna og bóka sölupantanir. Eða látið kaupendur gera það sama fyrir innkaupapantanir.

Stofna öryggisflokka í  Microsoft 365  admin Center eða Azure Active Directory. Þessi grein lýsir skrefunum í  Microsoft 365  stjórnendamiðstöð en skrefin eru svipuð í báðum.

## Bæta við öryggisflokk í  Microsoft 365  stjórnsýslumiðstöðinni

1. Á  Microsoft 365  admin Center er farið  **í virku hópana & groups**  síðuna.
2. Veldu  **Bæta við hóp**.
3.  **Veldu Öryggisgerð**  flokks og veldu  **svo Next**.
4. Tilgreina grunnatriði fyrir hópinn þinn.
5. Valfrjálst: gera meðlimi hópsins tiltæka fyrir hlutverkaúthlutun. Til að fræðast meira um úthlutunum er farið í  [nota  Azure AD  flokka til að stjórna hlutverkaverkefnum](/azure/active-directory/roles/groups-concept).
6. Opnið flokkinn og Notið  **flipann bæta við meðlimi**  til að hafa fólk með í hópnum.

## Bæta við öryggishokk í miðborg fyrirtækja

Í  [!INCLUDE [prod_short](includes/prod_short.md)], Stofnið öryggisflokk og tengið hann við öryggisflokkinn í  Microsoft 365  admin-miðstöðinni. Nýi hópurinn þinn er með meðlimi sem þú bættist við í  Microsoft 365  admin Center.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, sláið inn  **öryggishópa** og veljið síðan tengda tengilinn.
2. Velja  **skal nýtt**  til að stofna hóp.
3.  **Í reitinn Heiti**  er fært inn heiti flokksins.
4.  **Í reitinn aad öryggisflokksheiti**  skal færa inn heiti öryggisflokksins nákvæmlega eins og hann birtist í  Microsoft 365  admin Center. [!INCLUDE [prod_short](includes/prod_short.md)] vilja finna þann hóp og tengja hann við þennan hóp.

> [!NOTE]
> Notendur sem sýna á  **Meðliakspjaldi**  í FACTBOX rúðunni eða  **meðlimi**  öryggisflokksins hafa aðeins bætt þeim við sem notendur í [!INCLUDE [prod_short](includes/prod_short.md)]. Til að fá frekari upplýsingar um að bæta við notendum skaltu fara í  [til að bæta við notendum eða uppfæra notendaupplýsingarnar og leyfisúthlutunum í Business Central](ui-how-users-permissions.md#adduser).  

### Úthluta heimildum til flokksins

1.  **Á síðunni öryggishópar**  er hópurinn valinn og svo er  **heimildaaðgerðin**  valin.
1. Úthluta heimildum á eftirfarandi hátt:
    * Til að úthluta Sérleyfistilsettum  **fyrir hvert fyrir sig er heimildin valin í**  reitnum leyfi.
    * Til að úthluta mörgum heimildalista skal velja  **aðgerðina velja heimildanamengi**  og velja síðan samstæður sem á að úthluta.

## Farið yfir heimildir í öryggisflokki

 **Á síðunni um öryggishópa**  sýnir upplýsingakrúðan hvaða  **heimildasamstæður**  eru tengdar við flokkinn. Hver notandi á listanum yfir  **meðlimi**  kortsins hefur þær heimildir. Sú heimild sem sett er  **eftir aðgerð öryggisflokks**  gefur nánari Yfirlit. Þar er einnig hægt að kanna einstakar heimildir í hverjum öryggisflokki.

Heimildir eru einnig aðgengilegar á  **síðunni notendur** . FactBox-Glugginn sýnir  **heimildasöfn úr öryggisvarsrúðu**  og  **öryggisvarsspjöldum**  fyrir valinn notanda.

## Öryggisflokkar og notendaflokkar

Ef um notendaflokka er að ræða er hægt að umbreyta hópunum í heimildir til að breyta stæðum í leigjanda með því að nota leiðbeiningar um  **uppsetningu notendaflokksins um Flutningsaðstoð** . Til að hefja leiðbeiningarnar, á  **síðunni Feature Management**, finnið  **þið lögun: breytið heimildum** notendaflokks og veljið  **svo alla notendur**  í  **virkjanum fyrir**  svæðið. Leiðbeiningar með uppsetningarleiðbeiningum aðstoðar eru eftirfarandi valkostir fyrir viðskiptin.

|Valkostur  |Description  |
|---------|---------|
|Úthluta til notanda     | Úthlutið heimildum notendaflokka beint til notendanna sem voru tengdir hópnum, og Fjarlægið notendahópúthlutanir þeirra.        |
|Breyta í heimildasamstæðu     | Stofnið nýja heimild fyrir heimildina í hverjum notendaflokki. Nýja heimildsettinu er úthlutað á alla meðlimi hvers notendaflokks.          |

## Sjá einnig

[Búa til notendur samkvæmt leyfum](ui-how-users-permissions.md)  
[Setja upp miðlægu aðgengi fyrir fyrirtæki í teymum með  Microsoft 365  leyfi](admin-access-with-m365-license-setup.md)  
[Nánar um hópa og aðgangsheimild í Azure Active Directory](/azure/active-directory/fundamentals/concept-learn-about-groups)  
[Öryggisflokkar Active Directory](/windows-server/identity/ad-ds/manage/understand-security-groups)  