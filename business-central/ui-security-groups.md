---
title: Stjórna aðgangi með því að nota öryggishópa
description: Þessi grein lýsir því hvernig á að nota öryggishópa til að skilgreina notendaheimildir.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'access, right, security, permissions'
ms.search.form: '1, 119, 8930, 9800, 9807, 9808, 9830, 9831, 9802, 9855, 9862'
ms.date: 11/29/2023
ms.service: dynamics-365-business-central
---

# Stjórna aðgangi að Business Central með því að nota öryggishópa

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Öryggishópar auðvelda stjórnendum að stjórna notendaheimildum. Til dæmis, fyrir [!INCLUDE [prod_short](includes/prod_short.md)] á netinu, eru þau endurnýtanleg í Dynamics 365 forritum, eins og SharePoint Online, CRM Online og [!INCLUDE [prod_short](includes/prod_short.md)]. Stjórnendur bæta heimildum við [!INCLUDE [prod_short](includes/prod_short.md)] öryggishópa sína og þegar þeir bæta notendum við hópinn gilda heimildirnar fyrir alla meðlimi. Til dæmis getur stjórnandi búið til [!INCLUDE [prod_short](includes/prod_short.md)] öryggishóp sem gefur sölufólki möguleika á að búa til og bóka sölupantanir. Eða láttu kaupendur gera það sama fyrir innkaupapantanir.

## Business Central á netinu og á staðnum

Þú getur notað öryggishópa fyrir net- og staðbundnar útgáfur af [!INCLUDE [prod_short](includes/prod_short.md)]. Búðu til hópa á einn af eftirfarandi leiðum, allt eftir útgáfunni þinni:

* Notaðu Microsoft Entra öryggishópa fyrir netútgáfuna. Til að læra meira um að búa til hópinn skaltu fara í [Búa til, breyta eða eyða öryggishópi í Microsoft 365 stjórnendamiðstöðinni](/microsoft-365/admin/email/create-edit-or-delete-a-security-group).
* Fyrir innanhúss eru öryggishópar aðeins studdir ef uppsetningin notar Windows auðkenningu. Til að búa til öryggishópa fyrir innanhúss skaltu nota Windows Active Directory hópa. Til að læra meira, farðu í [Búa til hópreikning í Windows Active Directory](/windows/security/operating-system-security/network-security/windows-firewall/create-a-group-account-in-active-directory). 

Síðan skaltu búa til samsvarandi öryggishóp í [!INCLUDE [prod_short](includes/prod_short.md)] og tengja hann síðan við hópinn sem þú bjóst til. Til að fá frekari upplýsingar skaltu fara á [Bæta við öryggishópi í Business Central](#add-a-security-group-in-business-central).

> [!NOTE]
> Ef þú hefur sett upp sérstaka tegund notanda með Windows Group leyfistegund í útgáfu af [!INCLUDE [prod_short](includes/prod_short.md)] on-prem sem er fyrr en 2023 útgáfubylgja 1, þegar þú uppfærir [!INCLUDE [prod_short](includes/prod_short.md)] breytir notandann í öryggishóp. Nýi öryggishópurinn hefur sama nafn og Windows hópnafnið. Öryggishópurinn gefur þér betri yfirsýn yfir hópmeðlimi og skilvirkar heimildir þeirra.

## Bættu við öryggishópi í Business Central

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, sláðu inn **Öryggishópar** og veldu svo tengda hlekkinn.
1. Veldu **Nýtt** til að búa til hóp.
1. Búðu til hlekkinn á hópinn þinn, eins og hér segir:

    * Fyrir [!INCLUDE [prod_short](includes/prod_short.md)] á netinu skaltu velja hópinn í  **Microsoft Entra heiti öryggishóps** reitsins.
    * Fyrir [!INCLUDE [prod_short](includes/prod_short.md)] á staðnum skaltu velja hópinn í **Windows hópheiti** reitnum.

> [!NOTE]
> Notendur birta á **Meðlima** kortinu á FactBox glugganum eða  **Öryggishópsmeðlimir** síðunni aðeins ef þeir eru bætt við sem notendum í [!INCLUDE [prod_short](includes/prod_short.md)]. Til að læra meira um að bæta við notendum skaltu fara á [Til að bæta við notendum eða uppfæra notendaupplýsingar og leyfisúthlutun í Business Central](ui-how-users-permissions.md#adduser).  

### Úthlutaðu heimildum til öryggishóps

1. Á síðunni **Öryggishópar**  skaltu velja hópinn og velja síðan aðgerðina **Heimildir** .
1. Úthlutaðu heimildum á eftirfarandi hátt:

    * Til að úthluta heimildasettum fyrir sig, í reitnum **heimildasett**, veldu heimildirnar sem á að úthluta.
    * Til að úthluta mörgum heimildasettum skaltu velja  **Velja heimildasett** aðgerðina og velja síðan settin sem á að úthluta.

## Skoðaðu heimildirnar í öryggishópi

Á  **Öryggishópum** síðunni sýnir FactBox gluggann  **heimildasettin** sem eru úthlutað til hópsins. Hver notandi sem skráður er á **Meðlima** kortinu hefur þessar heimildir. Aðgerðin **Leyfi sett af öryggishópi**  veitir ítarlegri sýn. Þar er einnig hægt að kanna einstakar heimildir í hverjum öryggishópi.

Heimildir eru einnig fáanlegar á  **Notendum** síðunni. FactBox gluggann sýnir **heimildasett frá öryggishópi** og **Öryggishópsaðild** kortum fyrir valinn notanda.

## Öryggishópar og notendahópar

> [!NOTE]
> Notendahópar verða ekki lengur tiltækir í framtíðarútgáfu.

Öryggishópar eru mjög svipaðir notendahópum sem eru í boði núna. Hins vegar eiga notendahópar aðeins við fyrir [!INCLUDE [prod_short](includes/prod_short.md)]. Öryggishópar eru byggðir á hópum í Microsoft Entra ID eða Windows Active Directory, eftir því hvort þú notar [!INCLUDE [prod_short](includes/prod_short.md)] á netinu eða á staðnum, í sömu röð. Hópar gagnast stjórnendum vegna þess að þeir geta notað þá með öðrum Dynamics 365 forritum. Til dæmis, ef sölumenn nota [!INCLUDE [prod_short](includes/prod_short.md)] og SharePoint, þurfa stjórnendur ekki að endurskapa hópinn og meðlimi hans.

### Valfrjálst: Umbreyttu notendahópum í heimildasett

Í 2023 útgáfubylgju 1 og síðar geturðu breytt notendahópum í heimildasett hjá leigjanda þínum. Heimildasettin veita sömu virkni og notendahópar. Hér eru nokkur dæmi:

* Þú getur notað **Notendur** FactBox til að stjórna heimildum notenda.
* Þú getur borið niður á heiti heimildasettsins til að bæta öðrum heimildasettum við settið sem þú ert að vinna að. Til að læra meira skaltu fara á [Til að bæta við öðrum heimildasettum](ui-define-granular-permissions.md#to-add-other-permission-sets).

Notaðu **User Group Migration** uppsetningarleiðbeiningar með aðstoð til að breyta hópunum þínum. Til að hefja handbókina skaltu finna **Eiginleikastjórnun** síðuna **Eiginleiki: Umbreyta heimildum notendahóps** og velja síðan  **Allir notendur** í reitnum **Virkjað fyrir** . Uppsetningarleiðbeiningar með aðstoð býður upp á eftirfarandi valkosti fyrir viðskiptin.

|Valkostur  |Heimildasamstæða  |
|---------|---------|
|Úthluta til notanda     | Úthlutaðu heimildum í notendahópum beint til notenda sem voru úthlutaðir til hópsins og fjarlægðu úthlutun notendahóps þeirra.        |
|Breyta í heimildasamstæðu     | Búðu til nýja heimild fyrir heimildirnar í hverjum notendahópi. Nýja heimildasettinu er úthlutað öllum meðlimum hvers notendahóps.          |

### Leyfisstillingar gilda enn

Þú getur stillt heimildir í [!INCLUDE [prod_short](includes/prod_short.md)] byggðar á leyfum. Þessum heimildum er beint til nýrra notenda. Þessar stillingar eiga enn við, jafnvel þótt þú byrjir að nota öryggishópa.

Til að nota öryggishópa eingöngu mælum við með að þú fjarlægir leyfisstillingarnar. Til að læra meira um leyfisstillingar skaltu fara í [Búa til notendur í samræmi við leyfi](ui-how-users-permissions.md).

Þú getur fjarlægt leyfisstillingar á síðunni **Leyfisstillingar** . Veldu leyfi og eyddu síðan öllum heimildasettum sem því er úthlutað.

## Sjá einnig

[Búa til notendur samkvæmt leyfum](ui-how-users-permissions.md)  
[Settu upp Business Central aðgang í teymum með Microsoft 365 leyfum](admin-access-with-m365-license-setup.md)  
[Lærðu um hópa og aðgangsrétt í Microsoft Entra ID](/azure/active-directory/fundamentals/concept-learn-about-groups)  
[Microsoft Entra öryggishópa](/windows-server/identity/ad-ds/manage/understand-security-groups)  
