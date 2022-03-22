---
title: Stjórnun OneDrive samþættingar við Business Central
description: Kynntu þér hvað þú getur gert til að stýra samþættingu milli Business Central og OneDrive for Business.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OneDrive, share, browser
ms.date: 05/12/2021
ms.author: bholtorf
ms.openlocfilehash: 5debd01f9d26e5e1dc1abc1a0123073d0f7ee234
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/04/2022
ms.locfileid: "8382872"
---
# <a name="managing-onedrive-integration-with-business-central"></a>Stjórnun OneDrive samþættingar við Business Central 
Í þessari grein er að finna yfirlit yfir það sem stjórnandi getur gert til að stýra samþættingu OneDrive for Business við [!INCLUDE[prod_short](includes/prod_short.md)]. Viðskiptavinir [!INCLUDE[prod_short](includes/prod_short.md)] á netinu njóta góðs af sjálfvirkri samþættingu, án viðbótaruppsetningar sem þarf til að nota þessa eiginleika. 

## <a name="minimum-requirements"></a>Lágmarkskröfur

* Hver notandi verður að hafa leyfi fyrir [!INCLUDE[prod_short](includes/prod_short.md)] og OneDrive sem hluta af Microsoft 365 áætlun.
* OneDrive verður að vera sett upp fyrir hvern notanda fyrir sig.

## <a name="governance"></a>Stjórnunarhættir
Stjórnendamiðstöð SharePoint veitir víðtæka stjórn á reglum sem gilda um notkun á OneDrive í öllu fyrirtækinu. Altækir stjórnendur eða notendur sem eru með SharePoint stjórnandahlutverkið geta sett upp reglur sem skera úr um hver fær aðgang að OneDrive þar sem gögn eru geymd, líftími efnis og margt fleira. Eftirfarandi tenglar veita upplýsingar um oft notaða eiginleika og stillingar sem geta aukið samþættingu þína við [!INCLUDE[prod_short](includes/prod_short.md)]. 

* [Stjórna samnýtingarstillingum](/sharepoint/turn-external-sharing-on-or-off)
* [Nota upplýsingatálma með SharePoint](/sharepoint/information-barriers)
* [Kynntu þér gagnatapsvörn](/microsoft-365/compliance/dlp-learn-about-dlp)
* [Stilla sjálfgefið geymslupláss fyrir OneDrive notendur](/onedrive/set-default-storage-space)
* [Bæta við og fjarlægja stjórnendur fyrir OneDrive notanda](/sharepoint/manage-user-profiles#add-and-remove-admins-for-a-users-onedrive)
* [Gera stofnun OneDrive óvirka fyrir suma notendur](/sharepoint/manage-user-profiles#disable-onedrive-creation-for-some-users)
* [Fjölbreyttir landfræðilegir eiginleikar í OneDrive og SharePoint á netinu](/microsoft-365/enterprise/multi-geo-capabilities-in-onedrive-and-sharepoint-online-in-microsoft-365)

> [!NOTE]
> Sumir eiginleikar eru hugsanlega aðeins í boði fyrir tilteknar áskriftarleiðir.

## <a name="managing-privacy"></a>Umsjón með persónuvernd
Stjórnendur og notendur stjórna efninu sem geymt er í OneDrive og þessi gögn eru eingöngu í eigu fyrirtækisins þíns. Frekari upplýsingar er að finna í [Hvernig SharePoint og OneDrive tryggja öryggi gagna þinna í skýinu](/sharepoint/safeguarding-your-data). Þú getur einnig farið í [Persónuverndaryfirlýsingu Microsoft](https://privacy.microsoft.com/en-us/privacystatement) sem útskýrir gögnin sem Microsoft vinnur úr, hvernig Microsoft vinnur úr þeim og í hvaða tilgangi.

## <a name="restoring-onedrive-and-prod_short"></a>Að endurheimta OneDrive og [!INCLUDE[prod_short](includes/prod_short.md)]
Sem hluti af æfingu til að endurheimta eftir áfall gætu stjórnendur þurft að endurheimta [!INCLUDE[prod_short](includes/prod_short.md)] umhverfi í öryggisafriti aftur í tíma og samstilla OneDrive geymslu til þess tíma. OneDrive veitir ýmis verkfæri fyrir þetta, t.d. endurheimt á OneDrive notanda aftur í tíma, endurheimta eldri útgáfu einstakrar skráar eða endurheimta eyddar skrár. Frekari upplýsingar er að finna í eftirfarandi greinum:

* Fyrir [!INCLUDE[prod_short](includes/prod_short.md)] skal skoða [Að endurheimta umhverfi í stjórnendamiðstöðinni](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-backup-restore).
* Fyrir OneDrive skal skoða [Endurheimta OneDrive](https://support.microsoft.com/en-us/office/restore-your-onedrive-fa231298-759d-41cf-bcd0-25ac53eb8a15?ui=en-us&rs=en-us&ad=us)

## <a name="configuring-business-central-on-premises"></a>Að grunnstilla Business Central á staðnum

Stjórnandi verður að setja upp tenginguna milli [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum og OneDrive. Ólíkt [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum er tengingin ekki sjálfvirk. Ef tengingin er ekki stillt geta notendur ekki notað eiginleikana fyrir OneDrive. 

[!INCLUDE[prod_short](includes/prod_short.md)] á staðnum er aðeins hægt að tengja við OneDrive sem Microsoft hýsir í skýinu. Að tengja [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum við gagnageymslu minna svæða á SharePoint Server er ekki stutt.

> [!IMPORTANT]
> Með því að stilla þennan eiginleika virkjar þú einnig eldri eiginleika sem senda skrár til OneDrive.  
>
>* Eiginleikinn Opna í Excel mun sjálfkrafa afrita Excel-skrána í OneDrive, síðan opna hana í Excel Online. 
>* Að flytja út skýrslu í skrá mun sjálfkrafa afrita skrána í OneDrive, síðan opna hana í Excel Online, Word Online eða OneDrive. 
>* Aðrir eiginleikar gætu einnig opnast sjálfkrafa í OneDrive.

### <a name="to-prepare-prod_short-on-premises-for-connecting-to-onedrive"></a>Að undirbúa [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum undir tengingu við OneDrive

<!-- 
1. For the best experience Configure Azure Active Directory (AD) authentication.

   For more information, see [Authenticating Business Central Users with Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-active-directory)-->

Bættu við skráðri umsókn um Business Central í Azure AD leigjanda áætlunarinnar Microsoft 365. Eins og aðrar Azure-þjónustur sem vinna með Business Central þarf OneDrive á skráningu forrits að halda í Azure Active Directory (Azure AD). Forritsskráningin býður upp á sannvottun og sannvottunarþjónustu milli Business Central og SharePoint, sem OneDrive notar.

Grunnstilltu skráða forritið með eftirfarandi úthlutuðum heimildum fyrir SharePoint API:

- AllSites.Write
- MyFiles.Write
- User.Read.All 

Þú gerir þetta verk í Azure-gáttinni. Vertu viss um að afrita auðkenni forrits (biðlara) og leyniorð biðlara sem skráða forritið notar. Þú þarft þessar upplýsingar fyrir næsta verki.

Frekari upplýsingar um skráningu forrits og stillingar á heimildum er að finna í [Skrá forrit í Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory) í hjálparefni þróunaraðila og upplýsingatækni.

> [!TIP]
> Ef forrit hefur þegar verið skráð sem hluti af samþættingu við aðra vöru Microsoft á borð við Power BI, þá getur þú notað forritsskráninguna aftur. Í þessu tilviki þarftu bara að stilla SharePoint heimildirnar.

### <a name="to-set-up-the-connection-in-prod_short-on-premises"></a>Að setja upp tenginguna í [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum

<!--
> [!NOTE]
> This requires the following types of authentication credentials:
>
> * Windows
> * NavUserPassword
> * Azure Active Directory
-->
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning Microsoft SharePoint-tengingar** og velja síðan viðkomandi tengil.
2. Í reitinn **Lýsing** skal færa inn lýsingu fyrir tenginguna, á borð við **OneDrive**.
3. Í reitinn **Mappa** skal færa inn **Business Central**.
4. Í reitinn **Staðsetning** skal færa inn vefslóðina fyrir OneDrive.

    Vefslóðin fyrir OneDrive er yfirleitt á eftirfarandi sniði: `https://<tenant name>-my.sharepoint.com`. Frekari upplýsingar er að finna í [OneDrive Vefslóðir fyrir notendur fyrirtækisins](/onedrive/list-onedrive-urls) í OneDrive fylgigögnum.
5. Í reitinn **Auðkenni biðlara** skal færa inn biðlarakennið úr forritsskráningunni.
6. Í reitinn **Leynilykill biðlara** skal færa inn leynilykilinn úr forritsskráningunni. 
   <!-- 
   For information about how to find the URLs, see the following:
   * [How to find your SharePoint server URL]
   * [How to find your OneDrive URL]-->

> [!IMPORTANT]
> Uppsetningarsíða SharePoint tengingar er notuð til að stilla marga eldri eiginleika. Í **Almenna** hlutanum er tengingin við OneDrive stillt og hlutinn **Samnýtt skjöl** framsendir skrár í SharePoint í staðinn. Eldri SharePoint eiginleikinn verður tekinn úr umferð á næstunni. Við mælum með að þú stillir ekki hlutann **Samnýtt skjöl**.

## <a name="see-also"></a>Sjá einnig
[Business Central og OneDrive fyrir Business Integration](across-onedrive-overview.md)  
[Opna Business Central Files í OneDrive](across-share-onedrive.md)  
[OneDrive ALGENGAR SPURNINGAR](admin-onedrive-faq.md)

