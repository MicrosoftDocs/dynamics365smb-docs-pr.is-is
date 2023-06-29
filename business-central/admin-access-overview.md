---
title: Stjórna aðgangi að miðborg viðskipta-
description: Stjórnendur nota markvisst nálgun til að stýra aðgangi að miðborg og getu fyrirtækja.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: jswymer
ms.topic: overview
ms.date: 04/04/2023
ms.custom: bap-template
---

# <a name="manage-access-to-business-central"></a><a name="manage-access-to-business-central"></a>Stjórna aðgangi að miðborg viðskipta-

Í þessari grein gefst stjórnendum og forriturum mikið yfirlit yfir hvernig stýra eigi aðgangi að  [!INCLUDE [prod_short](includes/prod_short.md)]  og eiginleikum hans. Notaðu krækjurnar til að fara í aðrar greinar sem gefa nánari upplýsingar um viðfangsefnin.

## <a name="layered-access"></a><a name="layered-access"></a>Layered aðgang

[!INCLUDE [prod_short](includes/prod_short.md)] styðst við öryggiskoeftir eins og lýst er í eftirfarandi skýringarmynd. Til að fræðast nánar um hvert lag er farið í  [Umsóknaröryggi í miðborg](/dynamics365/business-central/dev-itpro/security/security-application).

:::image type="content" source="media/security-overview.png" alt-text="Markvisst hugbúnaðaröryggi í viðskiptum miðsvæðis.":::

## <a name="licenses"></a><a name="licenses"></a>Leyfi

Úthluta  [!INCLUDE [prod_short](includes/prod_short.md)]  notendum á  **Dynamics 365 Business Central**  leyfi svo þeir geti skoðað, breytt og unnið úr viðskipagögnum sínum í hvaða notendaviðmóti sem er. Frekari upplýsingar um leyfi er að fara  [í leyfi í Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/deployment/licensing).

Hins vegar getur gott fólk sem stundum þarf lesefni til að fá upplýsingar í  [!INCLUDE [prod_short](includes/prod_short.md)]  geta nýtt sér  **Microsoft 365**  leyfi. Til að fá meiri upplýsingar um að gefa takmarkaðan aðgang er farið í  [miðlægu aðgengi fyrirtækja með  Microsoft 365  leyfum](admin-access-with-m365-license.md).

Fyrir yfirgripsmiklar upplýsingar um mismunandi tegundir leyfa og hvernig leyfisveitingar eru gerðar í  [!INCLUDE[prod_short](includes/prod_short.md)],  [Sækja leiðbeiningar](https://go.microsoft.com/fwlink/?LinkId=866544) um leyfisveitingu fyrir Dynamics 365.

## <a name="business-central-administrator-tasks"></a><a name="business-central-administrator-tasks"></a>Verkefni seðlabankastjóra

Í eftirfarandi töflu er listi yfir hvernig kerfisstjórar geta stjórnað aðgangi að  [!INCLUDE [prod_short](includes/prod_short.md)]  og hvaða möguleika þeir nota. Sum verkefnanna hjálpa einnig til við að halda aðgangsheimilum upp-til skv.

|Verkefni| Frekari upplýsingar |
|--|--|--|
|Hver einstaklingur verður að hafa notandareikning áður en hann getur skráð sig inn [!INCLUDE [prod_short](includes/prod_short.md)]. Auðveldasta leiðin til að setja upp notendur er að bæta þeim við eitt í einu í  [Microsoft 365  admin Center](https://go.microsoft.com/fwlink/p/?linkid=2024339). |[Bæta notendum við og úthluta leyfum á sama tíma](/microsoft-365/admin/add-users/add-users)|
|Stjórna aðgangi fyrir alla notendur á umhverfistigi.  Azure Active Directory Stofna (Azure AD) öryggiaflokk og úthluta umhverfinu.<br><br> Einnig er hægt að nota öryggishópa til að stjórna aðgangi fyrir tiltekna flokka notenda. | [Stjórna aðgangi að umhverfi](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access)<br><br>[Stjórna aðgangi að starfrækslu miðsvæðis með öryggisflokkum](ui-security-groups.md) |
|Stofna notendur í  [!INCLUDE [prod_short](includes/prod_short.md)], og skilgreina hverjir geta skráð sig inn. | [Búa til notendur samkvæmt leyfum](ui-how-users-permissions.md) |
|Í samsetningu notendaleyfum skilgreina heimildir þá hluti sem notandi getur fengið aðgang að í hverjum gagnagrunni eða umhverfi. Tilgreinið hvort fólk geti lesið, breytt eða fært inn gögn í gagnagrunnshlutum. |[Úthluta leyfi til notenda og hópa](ui-define-granular-permissions.md)|
|Ef ytri endurskoðandi hefur umsjón með bókunum og fjárhagsskýrslugerð skal bjóða þær út [!INCLUDE [prod_short](includes/prod_short.md)]. Þeir munu geta unnið meira náið með þér á þínum fjárhagsgögnum.|[Endurskoðandi upplifun í [!INCLUDE[prod_long](includes/prod_long.md)]](finance-accounting.md)|
|Ef þú ert  [!INCLUDE [prod_short](includes/prod_short.md)]  endursöluaðili getur þú sent tölvupóst á viðskiptamann til að óska eftir því að fá samband við endursöluaðila. Hægt er að hafa stjórnunarheimildir úthlutað fyrir  Azure Active Directory  og  Microsoft 365  í tölvupósti.| [Fulltrúi kerfisstjóra aðgang að miðlægu neti fyrirtækja](/dynamics365/business-central/dev-itpro/administration/delegated-admin)|
|Azure þjónustumerki stendur fyrir hóp IP vistfanga sem umferð um þjónustu getur komið frá eða farið í. Notaðu þjónustumerki til að setja upp eldveggi til að leyfa umferð aðeins út frá ákveðinni þjónustu.  **Dynamics365BusinessCentral**  -merkið leyfir notanda að nota reglur eldveggjar og netöryggisflokka til að takmarka umferð til og frá [!INCLUDE [prod_short](includes/prod_short.md)].| [Þjónustumerki Azure](/dynamics365/business-central/dev-itpro/security/security-service-tags)|
|Þegar sannvottun er notuð  Azure Active Directory  með  [!INCLUDE [prod_short](includes/prod_short.md)] er mælt með því að nýta sér  [Azure AD  fjölþátta AUÐKENNINGU (MFA)](/azure/active-directory/authentication/concept-mfa-howitworks). MFA hefur til viðbótar Öryggisverðir aðgang að umsókninni og gögnum.|[Fjölþátta sannvottun fyrir Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/security/multifactor-authentication)|

## <a name="business-central-developer-tasks"></a><a name="business-central-developer-tasks"></a>Verkefni á vegum Aðalverktakar

Einnig er forritunarsaga til að stjórna aðgangi að [!INCLUDE [prod_short](includes/prod_short.md)]. Hönnuðir og stjórnendur geta til dæmis smíðað og tengt forrit við  [!INCLUDE [prod_short](includes/prod_short.md)]  það sem gagnast þeim við viðskiptin:  

* Viðskiptaferlar straumlínulítil
* Bæta samskipti viðskiptavina
* Taka betri ákvarðanir, festa

Eftirfarandi tafla tengir upplýsingar um hvernig á að gefa apps og viðaukar aðgang að  [!INCLUDE [prod_short](includes/prod_short.md)]  gögnum.

| Verkefni | Frekari upplýsingar |
|--|--|
|Tvö meginhugtökin fyrir skilgreiningu aðgangs að eiginleikum eru frumhugtök og heimildir. Entitlements veitir víðtækan aðgang að hlutum í samræmi við leyfi eða  Azure Active Directory  hlutverk. Heimildir og heimildasöfn leyfa þér að fínstilla aðgang að hlutum. |[Kröfur og yfirlit yfir heimildasöfn](/dynamics365/business-central/dev-itpro/developer/devenv-entitlements-and-permissionsets-overview)|

## <a name="see-also"></a><a name="see-also"></a>Sjá einnig

[Öryggi í viðskiptum miðsvæðis](/dynamics365/business-central/dev-itpro/security/security-and-protection)
