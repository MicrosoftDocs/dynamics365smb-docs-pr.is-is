---
title: Stjórna notendastillingum og kjörstillingum sem stjórnandi
description: Stjórna notendastillingum og kjörstillingum í Dynamics 365 Business Central.
author: sorenfriisalexandersen
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.keywords: user settings, preferences, language, region, time zone, regional settings
ms.search.form: 9204
ms.date: 04/01/2021
ms.author: soalex
ms.openlocfilehash: b3b4c857f006970fa3973a1203a7ddd8cffc2298
ms.sourcegitcommit: 8464b37c4f1e5819aed81d9cfdc382fc3d0762fc
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/19/2022
ms.locfileid: "8011758"
---
# <a name="manage-user-settings-and-preferences"></a>Stjórna notendastillingum og kjörstillingum

Sem stjórnandi getur þú skilgreint notandastillingar í [!INCLUDE[prod_short](includes/prod_short.md)], svipað því og einstakir notendur geta stjórnað eigin kjörstillingum á síðunni **Mínar stillingar**.  

Fáið yfirlit yfir alla notendur í listanum **Notendur** og breytið einstaka stillingum með því að velja aðgerðina **Notandastillingar** fyrir notandann sem á við.

> [!TIP]
> Listinn **Notandastillingar** sýnir núverandi stillingar fyrir hvern notanda. Til að skoða eða breyta einstökum notendum skal velja aðgerðina **Skoða** eða **Breyta**.

Síðan **Spjald notandastillinga** er svipuð og síðan **Mínar stillingar** sem hver notandi hefur aðgang að og er hún öflugt verkfæri fyrir stjórnendur til að stilla sjálfgefnar stillingar og hreinsa sérstilltar síður sem dæmi.  

## <a name="types-of-user-settings"></a>Gerðir notendastillinga

*Notandastillingar* eru ekki þær sömu og *Notandauppsetning*, sem er um notandann sem eining og aðgangur notanda í kerfinu. Notandastillingar hafa ennfremur ekkert að gera með sérstillingar notanda, t.d. minniháttar breytingum á notandaviðmóti. Notendastillingar ákvarða forskilgreindar  stillingar fyrir hvern notanda á þann ólíka hátt sem forritið birtist notandanum. Eftirfarandi málsgrein sýnir fimm gerðir notendastillinga og kjörstillingar sem einstakur notandi getur stillt eða stjórnandi stillir miðlægt:

- **Fyrirtæki**  

  Þessi stilling ákvarðar fyrirtækið sem er skráð inn í næstu innskráningu. Notandi getur haft aðgang að mörgum fyrirtækjum og getur verið virkur í nokkrum fyrirtækjum.

- **Hlutverk**  

  Hlutverkið eð forstillingin lýsir hlutverki notanda í fyrirtækinu, t.d. *Sölustjóri*, *Bókari* eða *Innkaupafulltrúi*. Forstillingin ákvarðar síðan hlutverkamiðstöð notandans, heimasíðuna sem notendur sjá þegar hann skráir sig inn. Forstillingin hefur ekki áhrif á aðgangsheimild að virkni í [!INCLUDE[prod_short](includes/prod_short.md)].  

- **Tungumál**  

  Skilgreinir forritstungumál sem [!INCLUDE[prod_short](includes/prod_short.md)] birtir texta, textar og villuskilaboð á. Ef [!INCLUDE[prod_short](includes/prod_short.md)] notendur eru samstilltir frá Microsoft 365 eru Tungumálastillingarnar frá því Microsoft 365 notaðar, miðað við að notandinn vilji nota sömu stillingar í skrifstofuvörum og [!INCLUDE[prod_short](includes/prod_short.md)]. Stjórnandinn getur breytt sjálfgefinni stillingu og hver notandi getur valið á milli tiltækra tungumála á síðunni Mínar stillingar. En þau verða endurstillt í gildið frá Microsoft 365 því að næsta samstilling fer fram.

  Ef tungumálastillingin úr Microsoft 365 samsvarar studdu tungumáli [!INCLUDE[prod_short](includes/prod_short.md)] verður þetta tungumál valið fyrir notandann.  

  > [!NOTE]
  > Hugsanlega þarf að setja upp tungumálaforrit fyrir [!INCLUDE[prod_short](includes/prod_short.md)] til að birta tungumálið á réttan hátt. Þar af leiðandi er það góð venja að setja upp nauðsynleg tungumálaforrit áður en einhver notandi skráir sig inn í fyrsta skipti þannig að þeir fái góða upplifun frá byrjun. Frekari upplýsingar er að finna í listanum yfir [studd tungumál](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations).  
  
- **Svæði**  

  Skilgreinir hvernig dagsetningar og tölustafir birtast í [!INCLUDE[prod_short](includes/prod_short.md)] -biðlaranum, svo sem hvort nota eigi evrópskar eða bandarískar dagsetningarsnið eða hvernig á að birta tugabrotin og þúsund skiltákn í upphæðum. Ef [!INCLUDE[prod_short](includes/prod_short.md)] notendur eru samstilltir frá Microsoft 365 eru svæðistilstillingarnar sem Microsoft 365 notaðar eru, forsenda þess að notandinn vilji nota sömu stillingar í skrifstofuvörum og [!INCLUDE[prod_short](includes/prod_short.md)]. Kerfisstjóri eða notandi getur breytt þessum stillingum handvirkt í [!INCLUDE[prod_short](includes/prod_short.md)] en þær verða endurstilltar í gildi frá Microsoft 365 því að næsta samstilling fer fram.

- **Tímabelti**  

  Skilgreinir tímabeltið þar sem notandinn er staðsettur. Sem stendur er þetta ekki samstillt út frá Microsoft 365 og verður að vera stillt handvirkt.  

- **Kennsluábendingar**

  [!INCLUDE [ua-teachingtips](includes/ua-teachingtips.md)] Sem stjórnandi geturðu slökkt á fróðlegum ábendingum fyrir alla notendur, t.d. ef þú ert að innleiða notendur sem eru nú þegar kunnugir [!INCLUDE [prod_short](includes/prod_short.md)].  

> [!NOTE]
> Ef Microsoft 365 samstilling notanda er gerð á meðan notendur eru skráðir inn [!INCLUDE[prod_short](includes/prod_short.md)] verða þeir notendur að endurnýja vafrann eða skrá sig út og aftur í [!INCLUDE[prod_short](includes/prod_short.md)] til að sjá hugsanlegt annað tungumál sem er samstillt aðgerðinni.

## <a name="overview-of-all-user-specific-changes"></a>Yfirlit yfir notandabundnar breytingar

Sem stjórnandi geturðu fengið yfirlit yfir einstaka breytingar á [!INCLUDE [prod_short](includes/prod_short.md)] sem hver notandi gæti hafa gert á ýmsum síðum í [!INCLUDE [prod_short](includes/prod_short.md)]. Þegar notendur gera breytingar á upplifun sinni í [!INCLUDE [prod_short](includes/prod_short.md)] munu þær koma fram í listanum **Sérstillingar notanda**. <!--Administrators can also set these settings for users before they log in the first time, so users do not have to do it themselves, providing them a better *getting started* experience.-->

<!-- >[!NOTE]
> User personalizations do not have anything to do with the *personal* lightweight changes a user can make to the user experience.-->

## <a name="to-review-or-delete-user-personalizations"></a>Að yfirfara eða eyða sérstillingum notanda

1. Veldu ![Leita að síðu eða skýrslu.](media/ui-search/search_small.png "Leit að síðu eða skýrslu tákn") táknið, farðu í **Sérsniðnar síður** og veldu svo viðeigandi tengil.
2. Þetta birtir lista yfir notendur og sérstilltar síður þeirra. Til að hreinsa sérstillingu notanda er smellt á viðeigandi línu eða valið **Stjórna** og síðan valið **Eyða**.

Þetta eyðir sérstillingum og upplifun notandans á viðkomandi síðu fer aftur í sjálfgefna stöðu.

## <a name="see-also"></a>Sjá einnig

[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Lönd/svæði í boði og studd tungumál](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations)  
[Breyta tungumáli og landsstaðli](about-locale-language.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
