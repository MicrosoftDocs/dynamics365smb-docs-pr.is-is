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

# <a name="control-access-to-business-central-using-security-groups"></a>Stjórna aðgangi að starfrækslu miðsvæðis með öryggisflokkum

Öryggisflokkar auðvelda stjórnendum að stjórna notendaleyfi. Til dæmis  [!INCLUDE [prod_short](includes/prod_short.md)]  á netinu eru þær Endurnýtanlegar yfir Dynamics 365 forritum, svo sem  SharePoint  online,  CRM Online, og [!INCLUDE [prod_short](includes/prod_short.md)]. Stjórnendur bæta við heimildum til að sinna  [!INCLUDE [prod_short](includes/prod_short.md)]  öryggishópum og þegar þeir bæta við notendum í hópinn heimildin gildir um alla félagsmenn. Til dæmis getur kerfisstjóri stofnað  [!INCLUDE [prod_short](includes/prod_short.md)]  öryggisflokk sem gefur söluaðilum möguleika á að stofna og bóka sölupantanir. Eða látið kaupendur gera það sama fyrir innkaupapantanir.

## <a name="business-central-online-and-on-premises"></a>Viðskipti miðsvæðis á netinu og innanhúss

Hægt er að nota öryggishópa fyrir lager-og innanhússútgáfur [!INCLUDE [prod_short](includes/prod_short.md)]. Stofna skal flokka með eftirfarandi hætti eftir því hvaða útgáfa er stofnuð:

* Fyrir netútgáfuna, Notið  Microsoft Entra  öryggisflokka. Til að fræðast meira um stofnun flokksins er farið í að  [Stofna, breyta eða eyða öryggisflokki í  Microsoft 365  admin Center](/microsoft-365/admin/email/create-edit-or-delete-a-security-group).
* Ef um er að ræða innanhúss eru notaðir Windows Active Directory-Flokkar. Til að fá frekari upplýsingar er farið að  [Stofna Flokkareikning í Active Directory](/windows/security/operating-system-security/network-security/windows-firewall/create-a-group-account-in-active-directory).

Síðan þarf að stofna samsvarandi öryggiaflokk í  [!INCLUDE [prod_short](includes/prod_short.md)] og tengja hann síðan við flokkinn sem var stofnaður. Til að fá frekari upplýsingar er farið í að  [Bæta við öryggisflokki í Business Central](#add-a-security-group-in-business-central).

> [!NOTE]
> Ef sett hefur verið upp Sérstök tegund notanda með leyfigerð Windows-flokks í útgáfu  [!INCLUDE [prod_short](includes/prod_short.md)]  on-forforvarna sem er á undan 2023-bylgju 1, þegar uppfærsla  [!INCLUDE [prod_short](includes/prod_short.md)]  er umbreytir notandanum í öryggisflokk. Nýi öryggisflokkurinn hefur sama heiti og heiti Windows-flokksins. Í öryggisflokknum fæst betri yfirsýn yfir flokksmenn og skilvirkar heimildir þeirra.

## <a name="add-a-security-group-in-business-central"></a>Bæta við öryggishokk í miðborg fyrirtækja

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, sláið inn  **öryggishópa** og veljið síðan tengda tengilinn.
1. Velja  **skal nýtt**  til að stofna hóp.
1. Búðu til tengilinn fyrir hópinn þinn, eins og hér er:

    * Veljið flokkinn í  [!INCLUDE [prod_short](includes/prod_short.md)]  reitnum aad öryggisflokksheiti  **fyrir**  netið.
    *  [!INCLUDE [prod_short](includes/prod_short.md)] Velja skal flokkinn í  **reitnum Heiti**  Windows-flokks innanhúss.

> [!NOTE]
> Notendur sýna á  **félagakortsglugganum**  á FactBox rúðunni eða  **meðlimi**  öryggisflokksins aðeins ef þeim er bætt við sem notendur í [!INCLUDE [prod_short](includes/prod_short.md)]. Til að fá frekari upplýsingar um að bæta við notendum skaltu fara í  [til að bæta við notendum eða uppfæra notendaupplýsingarnar og leyfisúthlutunum í Business Central](ui-how-users-permissions.md#adduser).  

### <a name="assign-permissions-to-a-security-group"></a>Úthluta heimildum til öryggisflokks

1.  **Á síðunni öryggishópar**  er hópurinn valinn og svo er  **heimildaaðgerðin**  valin.
1. Úthluta heimildum á eftirfarandi hátt:

    * Til að úthluta Sérleyfistilsettum  **fyrir hvert fyrir sig er heimildin valin í**  reitnum leyfi.
    * Til að úthluta mörgum heimildalista skal velja  **aðgerðina velja heimildanamengi**  og velja síðan samstæður sem á að úthluta.

## <a name="review-the-permissions-in-a-security-group"></a>Farið yfir heimildir í öryggisflokki

 **Á síðunni um öryggishópa**  sýnir upplýsingakrúðan hvaða  **heimildasamstæður**  eru tengdar við flokkinn. Hver notandi á listanum yfir  **meðlimi**  kortsins hefur þær heimildir. Sú heimild sem sett er  **eftir aðgerð öryggisflokks**  gefur nánari Yfirlit. Þar er einnig hægt að kanna einstakar heimildir í hverjum öryggisflokki.

Heimildir eru einnig aðgengilegar á  **síðunni notendur** . FactBox-Glugginn sýnir  **heimildasöfn úr öryggisvarsrúðu**  og  **öryggisvarsspjöldum**  fyrir valinn notanda.

## <a name="security-groups-and-user-groups"></a>Öryggisflokkar og notendaflokkar

> [!NOTE]
> Notendaflokkar verða ekki lengur aðgengilegir í síðari útgáfu.

Öryggisflokkar eru mjög Svipaðir notendaflokkum sem nú eru tiltækir. Hins vegar eiga notendaflokkar aðeins  [!INCLUDE [prod_short](includes/prod_short.md)] við. Öryggisflokkar eru byggðir á flokkum í  Azure Active Directory  Active Directory eða Windows, eftir því hvort verið er að nota  [!INCLUDE [prod_short](includes/prod_short.md)]  netið eða innanhúss, eftir því sem við á. Flokka fríðindastjóra vegna þess að þeir geta notað önnur Dynamics 365 apps. Til dæmis, ef sölumenn nota  [!INCLUDE [prod_short](includes/prod_short.md)]  og  SharePoint þurfa stjórnendur ekki að afþakka hópinn og meðlimi hans.

### <a name="optional-convert-user-groups-to-permission-sets"></a>Valfrjálst: umbreyta notendaflokkum í heimildasöfn

Í 2023 út bylgju 1 og síðar er hægt að breyta notendahópum í heimildasöfn í leigjanda. Heimildasöfn veita sömu virkni og notendaflokkar. Hér eru nokkur dæmi:

* Hægt er að nota  **upplýsingakassa notendur**  til að stjórna heimildum fyrir notendur.
* Hægt er að kafa niður í heiti heimildstæðis til að bæta öðrum heimildum við samstæðurnar sem unnið er í. Til að fá frekari upplýsingar er farið í  [til að bæta við öðrum heimildum](ui-define-granular-permissions.md#to-add-other-permission-sets).

 **Notið Uppsetningarleiðbeiningar notendaflokksins flutningur**  aðstoðar til að umbreyta hópunum. Til að hefja leiðbeiningarnar, á  **síðunni Feature Management**, finnið  **þið lögun: breytið heimildum** notendaflokks og veljið  **svo alla notendur**  í  **virkjanum fyrir**  svæðið. Leiðbeiningar með uppsetningarleiðbeiningum aðstoðar eru eftirfarandi valkostir fyrir viðskiptin.

|Valkostur  |Heimildasamstæða  |
|---------|---------|
|Úthluta til notanda     | Úthlutið heimildum notendaflokka beint til notendanna sem voru tengdir hópnum, og Fjarlægið notendahópúthlutanir þeirra.        |
|Breyta í heimildasamstæðu     | Stofnið nýja heimild fyrir heimildina í hverjum notendaflokki. Nýja heimildsettinu er úthlutað á alla meðlimi hvers notendaflokks.          |

### <a name="license-configurations-still-apply"></a>Leyfisskilgreiningar eiga enn við

Hægt er að skilgreina heimildir á  [!INCLUDE [prod_short](includes/prod_short.md)]  grundvelli leyfa. Þeim heimildum er beinlínis úthlutað til nýrra notenda. Þessar skilgreiningar eiga enn við, jafnvel þó að byrjað sé að nota öryggishópa.

Ef nota á öryggisflokka sem eingöngu er mælt með að fjarlægja leyfissamskipanir. Frekari upplýsingar um leyfissamskipanir er að fá til að  [Stofna notendur samkvæmt leyfum](ui-how-users-permissions.md).

Hægt er að fjarlægja leyfissamskipanir á  **síðunni leyfissamstillingar** . Veldu leyfi og eyddu svo öllum leyfisstæðum sem úthlutað er á það.

## <a name="see-also"></a>Sjá einnig

[Búa til notendur samkvæmt leyfum](ui-how-users-permissions.md)  
[Setja upp miðlægu aðgengi fyrir fyrirtæki í teymum með  Microsoft 365  leyfi](admin-access-with-m365-license-setup.md)  
[Nánar um hópa og aðgangsheimild í Azure Active Directory](/azure/active-directory/fundamentals/concept-learn-about-groups)  
[Öryggisflokkar Active Directory](/windows-server/identity/ad-ds/manage/understand-security-groups)  
