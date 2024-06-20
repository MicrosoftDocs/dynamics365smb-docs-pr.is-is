---
title: Stjórna aðgangi að Business Central
description: Stjórnendur nota lagskipta aðferð til að stýra aðgangi að Business Central og getu þess.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: overview
ms.date: 04/04/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="manage-access-to-business-central"></a>Stjórna aðgangi að Business Central

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Þessi grein gefur stjórnendum og forriturum yfirsýn yfir hvernig hægt er að stýra aðgangi að [!INCLUDE [prod_short](includes/prod_short.md)] og eiginleikum hennar. Notaðu tenglana til að fara í aðrar greinar sem veita nánari upplýsingar um efnisatriðin.

## <a name="layered-access"></a>Lagaðgangur

[!INCLUDE [prod_short](includes/prod_short.md)] notar lagaða aðferð við öryggi forritsins, eins og lýst er í eftirfarandi skýringarmynd. Til að [fræðast meira um hvert lag er farið í Application Security í Business Central](/dynamics365/business-central/dev-itpro/security/security-application).

:::image type="content" source="media/security-overview.png" alt-text="Öryggisöryggi lagskipt í Business Central.":::

## <a name="licenses"></a>Leyfi

Úthluta [!INCLUDE [prod_short](includes/prod_short.md)] notendum **Dynamics 365 Business Central** leyfi svo þeir geti skoðað, breytt og unnið með viðskiptagögn sín úr hvaða notandaviðmóti sem er. Til að [fá nánari upplýsingar um leyfi er farið í Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/deployment/licensing) Leyfisveitingu.

Hins vegar fólk sem stundum þarf lesaðgang að upplýsingum í [!INCLUDE [prod_short](includes/prod_short.md)] getur notað **Microsoft 365** leyfi. Til að fræðast meira um að veita takmarkaðan aðgang er farið í [Business Central Access með Microsoft 365 leyfi.](admin-access-with-m365-license.md)

Fyrir alhliða upplýsingar um mismunandi tegundir leyfis og hvernig leyfi virkar í [!INCLUDE[prod_short](includes/prod_short.md)] skal [sækja Dynamics 365 Licensing Guide](https://go.microsoft.com/fwlink/?LinkId=866544).

## <a name="business-central-administrator-tasks"></a>Stjórnandi Business Central verkefna

Í eftirfarandi töflu er listi yfir hvernig stjórnendur geta stýrt aðgangi að [!INCLUDE [prod_short](includes/prod_short.md)] og eiginleikarnir sem notendur nota. Sum verkanna hjálpa einnig til við að halda aðgangsstillingum uppfærðum.

|Verkefni| Frekari upplýsingar |
|--|--|--|
|Hver einstaklingur verður að hafa notandareikning áður en hann getur skráð sig inn á [!INCLUDE [prod_short](includes/prod_short.md)]. Auðveldasta leiðin til að setja upp notendur er að bæta einum við í einu í [Microsoft 365 stjórnunarmiðstöðinni](https://go.microsoft.com/fwlink/p/?linkid=2024339). |[Bæta við notendum og úthluta leyfum samtímis](/microsoft-365/admin/add-users/add-users)|
|Stjórna aðgangi allra notenda á umhverfisstigi.  Microsoft Entra Stofna öryggishóp og úthluta honum á umhverfið.<br><br> Einnig er hægt að nota öryggisflokka til að stjórna aðgangi að tilteknum hópum notenda. | [Stjórna aðgangi að umhverfi](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access)<br><br>[Stjórna aðgangi að Business Central með öryggishópum](ui-security-groups.md) |
|Stofna notendur inn [!INCLUDE [prod_short](includes/prod_short.md)] og skilgreina hver getur skráð sig inn. | [Búa til notendur samkvæmt leyfum](ui-how-users-permissions.md) |
|Í tengslum við notendaleyfi skilgreina heimildir hlutina sem notandi hefur aðgang að innan hvers gagnagrunns eða umhverfis. Tilgreina hvort fólk geti lesið, breytt eða fært gögn inn í gagnagrunnshluti. |[Úthluta leyfi til notenda og hópa](ui-define-granular-permissions.md)|
|Ef utanaðkomandi endurskoðandi hefur umsjón með bókum þínum og ársskýrslum skal bjóða þeim til þín [!INCLUDE [prod_short](includes/prod_short.md)]. Þeir geta unnið betur með þér við fjárhagsgögnin þín.|[Endurskoðandi upplifun í [!INCLUDE[prod_long](includes/prod_long.md)]](finance-accounting.md)|
|Ef þú ert [!INCLUDE [prod_short](includes/prod_short.md)] endursöluaðili getur þú sent viðskiptavini tölvupóst til að biðja um samband söluaðila. Hægt er að hafa framseljandi stjórnunarréttindi fyrir Microsoft Entra auðkenni og Microsoft 365 tölvupóst.| [Úthlutaður umsjónarmaður aðgang að Business Central Online](/dynamics365/business-central/dev-itpro/administration/delegated-admin)|
|Azure þjónustumerki táknar hóp af IP-tölum sem umferð um þjónustu getur komið frá eða farið til. Nota þjónustumerki til að setja upp eldveggi til að leyfa aðeins umferð frá tiltekinni þjónustu. Með **Dynamics365BusinessCentral** merkinu er hægt að nota reglur um eldvegg og netöryggishóp til að takmarka umferð við og frá [!INCLUDE [prod_short](includes/prod_short.md)].| [Azure öryggi þjónustu merki](/dynamics365/business-central/dev-itpro/security/security-service-tags)|
|Þegar sannvottun er notuð Microsoft Entra með er mælt með [!INCLUDE [prod_short](includes/prod_short.md)] því að notandi noti [Microsoft Entra auðkenningu með mörgum þáttum (MFA).](/azure/active-directory/authentication/concept-mfa-howitworks) MFA verndar ennfremur aðgang að forritinu og gögnunum.|[Sannvottun margra þátta fyrir Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/security/multifactor-authentication)|

## <a name="business-central-developer-tasks"></a>Business Central verkefnum verkefna

Það er líka þróunarsaga til að sjá um aðgang að [!INCLUDE [prod_short](includes/prod_short.md)]. Forritarar og stjórnendur geta til dæmis byggt upp og tengt forrit til þess að [!INCLUDE [prod_short](includes/prod_short.md)] njóta viðskiptanna:  

* Straumlínu-viðskiptaferli
* Bæta samskipti viðskiptavina
* Taktu betri ákvarðanir, hraðar

Eftirfarandi töflutenglar eru í upplýsingum um hvernig forrit og viðbætur eru veittar. [!INCLUDE [prod_short](includes/prod_short.md)] 

| Verkefni | Frekari upplýsingar |
|--|--|
|Tvö meginhugtökin til að skilgreina aðgang að eiginleikum eru réttindi og heimildir. Réttindi gefa víðtækan aðgang að hlutum samkvæmt leyfum eða Microsoft Entra hlutverkum. Með heimildum og heimildum má fínstilla aðgang að hlutum. |[Yfirlit yfir réttindi og heimildasafn](/dynamics365/business-central/dev-itpro/developer/devenv-entitlements-and-permissionsets-overview)|

## <a name="see-also"></a>Sjá einnig

[Öryggi í Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection)
