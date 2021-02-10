---
title: Stjórna notendastillingum og kjörstillingum í Dynamics 365 Business Central
description: Stjórna notendastillingum og kjörstillingum í Dynamics 365 Business Central.
author: sorenfriisalexandersen
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user settings, preferences, language, region, time zone, regional settings
ms.date: 10/01/2020
ms.author: soalex
ms.openlocfilehash: 25b3c8a795c1a3f9d08ae0971da88b78e4d29b25
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752576"
---
# <a name="manage-user-settings-and-preferences"></a><span data-ttu-id="939b2-103">Stjórna notendastillingum og kjörstillingum</span><span class="sxs-lookup"><span data-stu-id="939b2-103">Manage user settings and preferences</span></span>

<span data-ttu-id="939b2-104">Sem stjórnandi getur þú nýtt notandastillingar í [!INCLUDE[prod_short](includes/prod_short.md)], svipað því og einstakir notendur geta stjórnað eigin kjörstillingum á síðunni **Mínar stillingar**.</span><span class="sxs-lookup"><span data-stu-id="939b2-104">As an administrator, you can user settings in [!INCLUDE[prod_short](includes/prod_short.md)], similar to how individual users can manage their own preferences in the **My Settings** page.</span></span>  

## <a name="types-of-user-settings"></a><span data-ttu-id="939b2-105">Gerðir notendastillinga</span><span class="sxs-lookup"><span data-stu-id="939b2-105">Types of user settings</span></span>

<span data-ttu-id="939b2-106">*Notandastillingar* eru ekki þær sömu og *Notandauppsetning*, sem er um notandann sem eining og aðgangur notanda í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="939b2-106">*User settings* is not the same as *user setup*, which is about the user as an entity and the user's access in the system.</span></span> <span data-ttu-id="939b2-107">Notandastillingar hafa ennfremur ekkert að gera með sérstillingar notanda, t.d. minniháttar breytingum á notandaviðmóti.</span><span class="sxs-lookup"><span data-stu-id="939b2-107">Furthermore, user settings has nothing to do with a user's personalization, such as lightweight changes to the user interface.</span></span> <span data-ttu-id="939b2-108">Notendastillingar tilgreina kjörstillingar notandans á ýmsan máta sem forritið birtist notandanum.</span><span class="sxs-lookup"><span data-stu-id="939b2-108">User settings determine the user's preferences in various aspects of the way the application presents itself to the user.</span></span> <span data-ttu-id="939b2-109">Eftirfarandi málsgrein sýnir fimm gerðir notendastillinga og kjörstillingar sem einstakur notandi getur stillt eða stjórnandi stillir miðlægt:</span><span class="sxs-lookup"><span data-stu-id="939b2-109">The following paragraph lists the five types of user settings and preferences that can be set by the individual or centrally by the administrator:</span></span>

- <span data-ttu-id="939b2-110">**Fyrirtæki**</span><span class="sxs-lookup"><span data-stu-id="939b2-110">**Company**</span></span>  

  <span data-ttu-id="939b2-111">Þessi stilling ákvarðar fyrirtækið sem er skráð inn í næstu innskráningu.</span><span class="sxs-lookup"><span data-stu-id="939b2-111">This setting determines the company to be logged into at the next login.</span></span> <span data-ttu-id="939b2-112">Notandi getur haft aðgang að mörgum fyrirtækjum og getur verið virkur í nokkrum fyrirtækjum.</span><span class="sxs-lookup"><span data-stu-id="939b2-112">A user can have access to multiple companies and can be active in several companies.</span></span>

- <span data-ttu-id="939b2-113">**Forstillingar (hlutverk)**</span><span class="sxs-lookup"><span data-stu-id="939b2-113">**Profile (Roles)**</span></span>  

  <span data-ttu-id="939b2-114">Forstillingin lýsir hlutverki notanda í fyrirtækinu, t.d. *Sölustjóri*, *Bókari* eða *Innkaupafulltrúi*.</span><span class="sxs-lookup"><span data-stu-id="939b2-114">The profile describes the user's function in the company, such as *Sales Manager*, *Bookkeeper*, or *Purchasing Agent*.</span></span> <span data-ttu-id="939b2-115">Forstillingin ákvarðar síðan hlutverkamiðstöð notandans, heimasíðuna sem notendur sjá þegar hann skráir sig inn.</span><span class="sxs-lookup"><span data-stu-id="939b2-115">The profile then determines the user's role center, the home page that users will see when they sign in.</span></span> <span data-ttu-id="939b2-116">Forstillingin hefur ekki áhrif á aðgangsheimild að virkni í [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="939b2-116">The profile does not impact access rights to functionality in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

- <span data-ttu-id="939b2-117">**Auðkenni málstaðals (svæðisstillingar)**</span><span class="sxs-lookup"><span data-stu-id="939b2-117">**Locale ID (Regional settings)**</span></span>  

  <span data-ttu-id="939b2-118">Skilgreinir hvernig dagsetningar og tölustafir birtast í [!INCLUDE[prod_short](includes/prod_short.md)] -biðlaranum, svo sem hvort nota eigi evrópskar eða bandarískar dagsetningarsnið eða hvernig á að birta tugabrotin og þúsund skiltákn í upphæðum.</span><span class="sxs-lookup"><span data-stu-id="939b2-118">Defines how dates and numbers are presented in the [!INCLUDE[prod_short](includes/prod_short.md)] client, such as whether to use European or American date formats, or how to display the decimal sign and thousand separators in amounts.</span></span> <span data-ttu-id="939b2-119">Ef [!INCLUDE[prod_short](includes/prod_short.md)] notendur eru samstilltir frá Microsoft 365  eru svæðisstillingarnar frá Microsoft 365  notaðar, að því gefnu að notandinn vill nota sömu stillingar í Office-vörum og [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="939b2-119">If [!INCLUDE[prod_short](includes/prod_short.md)] users are synchronized from Microsoft 365, the regional settings from Microsoft 365 are used, assuming that the user wants to use the same settings in Office products and [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="939b2-120">Stjórnandi eða notandi getur breytt þessum stillingum handvirkt í [!INCLUDE[prod_short](includes/prod_short.md)], en þær verða endurstilltar á gildið frá Microsoft 365 þegar næsta samstilling er framkvæmd.</span><span class="sxs-lookup"><span data-stu-id="939b2-120">An administrator or user can change these settings manually in [!INCLUDE[prod_short](includes/prod_short.md)], but they will be reset to the value from Microsoft 365 once the next synchronization is performed.</span></span>

- <span data-ttu-id="939b2-121">**Tungumál**</span><span class="sxs-lookup"><span data-stu-id="939b2-121">**Language**</span></span>  

  <span data-ttu-id="939b2-122">Skilgreinir forritstungumál sem [!INCLUDE[prod_short](includes/prod_short.md)] birtir texta, textar og villuskilaboð á.</span><span class="sxs-lookup"><span data-stu-id="939b2-122">Defines the application language that [!INCLUDE[prod_short](includes/prod_short.md)] presents text, captions, and error messages in.</span></span> <span data-ttu-id="939b2-123">Ef [!INCLUDE[prod_short](includes/prod_short.md)] notendur eru samstilltir frá Microsoft 365  eru tungumálastillingar frá Microsoft 365  notaðar, að því gefnu að notandinn vilji nota sömu stillingar í Office-vörum og [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="939b2-123">If [!INCLUDE[prod_short](includes/prod_short.md)] users are synchronized from Microsoft 365, the language settings from Microsoft 365 are used, assuming that the user wants to use the same settings in Office products and [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="939b2-124">Stjórnandi eða notandi getur breytt þessum stillingum handvirkt í [!INCLUDE[prod_short](includes/prod_short.md)], en þær verða endurstilltar á gildið frá Microsoft 365 þegar næsta samstilling er framkvæmd.</span><span class="sxs-lookup"><span data-stu-id="939b2-124">An administrator or user can change these settings manually in [!INCLUDE[prod_short](includes/prod_short.md)], but they will be reset to the value from Microsoft 365 once the next synchronization is performed.</span></span>

  <span data-ttu-id="939b2-125">Ef tungumálastillingin úr Microsoft 365 samsvarar studdu tungumáli í [!INCLUDE[prod_short](includes/prod_short.md)] verður slíkt tungumál valið fyrir notandann.</span><span class="sxs-lookup"><span data-stu-id="939b2-125">If the language setting from Microsoft 365 matches a supported language in [!INCLUDE[prod_short](includes/prod_short.md)], this language will be chosen for the user.</span></span>  

  > [!NOTE]
  > <span data-ttu-id="939b2-126">Hugsanlega þarf að setja upp tungumálaforrit fyrir [!INCLUDE[prod_short](includes/prod_short.md)] til að birta tungumálið á réttan hátt.</span><span class="sxs-lookup"><span data-stu-id="939b2-126">You may have to install a language app for [!INCLUDE[prod_short](includes/prod_short.md)] to properly display the language.</span></span> <span data-ttu-id="939b2-127">Þar af leiðandi er það góð venja að setja upp nauðsynleg tungumálaforrit áður en einhver notandi skráir sig inn í fyrsta skipti þannig að þeir fái góða upplifun frá byrjun.</span><span class="sxs-lookup"><span data-stu-id="939b2-127">Therefore, it is a good practice to install the necessary language apps before any user logs in the first time so that they have a good experience from their first day.</span></span> <span data-ttu-id="939b2-128">Frekari upplýsingar er að finna í listanum yfir [studd tungumál](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations).</span><span class="sxs-lookup"><span data-stu-id="939b2-128">For more information, see the list of [supported languages](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations).</span></span>  
  
- <span data-ttu-id="939b2-129">**Tímabelti**</span><span class="sxs-lookup"><span data-stu-id="939b2-129">**Time zone**</span></span>  

  <span data-ttu-id="939b2-130">Skilgreinir tímabeltið þar sem notandinn er staðsettur.</span><span class="sxs-lookup"><span data-stu-id="939b2-130">Defines the time zone in which the user is located.</span></span> <span data-ttu-id="939b2-131">Sem stendur er þetta ekki samstillt af Microsoft 365 og verður að stilla handvirkt.</span><span class="sxs-lookup"><span data-stu-id="939b2-131">Currently this is not synchronized from Microsoft 365 and must be set manually.</span></span>  

> [!NOTE]
> <span data-ttu-id="939b2-132">Ef samstilling Microsoft 365-notanda er gerð á meðan notendur eru skráðir inn í [!INCLUDE[prod_short](includes/prod_short.md)] verða slíkir notendur að uppfæra vafrann eða skrá sig út og aftur inn í [!INCLUDE[prod_short](includes/prod_short.md)] til að sjá þeir geti séð annað tungumál sem er stillt með samstillingaraðgerðinni.</span><span class="sxs-lookup"><span data-stu-id="939b2-132">If a Microsoft 365 user synchronization is made while users are logged into [!INCLUDE[prod_short](includes/prod_short.md)], these users must refresh the browser or log out and back in to [!INCLUDE[prod_short](includes/prod_short.md)] to see a potential different language set by the synchronization action.</span></span>

## <a name="overview-of-all-user-settings"></a><span data-ttu-id="939b2-133">Yfirlit yfir allar notendastillingar</span><span class="sxs-lookup"><span data-stu-id="939b2-133">Overview of all user settings</span></span>

<span data-ttu-id="939b2-134">Stjórnendur hafa möguleika á því að stilla eða breyta þessum stillingum fyrir notendur í hverju fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="939b2-134">Administrators have the option to set or change these settings for users in each company.</span></span> <span data-ttu-id="939b2-135">Þetta er gert á síðunni **Sérstillingar notanda**.</span><span class="sxs-lookup"><span data-stu-id="939b2-135">This is done on the **User Personalizations** page.</span></span> <span data-ttu-id="939b2-136">Færslurnar á þessari síðu sýna val tiltekins notanda á stillingunum hér á undan, eða eina færslu á hvern notanda.</span><span class="sxs-lookup"><span data-stu-id="939b2-136">Records on this page will reflect the individual user's choices for the above settings, one record per user.</span></span> <span data-ttu-id="939b2-137">Þegar notendur gera breytingar á stillingum sínum á síðunni **Mínar stillingar** birtast slíkar breytingar á listanum **Sérstillingar notanda**.</span><span class="sxs-lookup"><span data-stu-id="939b2-137">As users make changes to their settings in the **My Settings** page, these changes will be reflected in the **User Personalizations** list.</span></span> <span data-ttu-id="939b2-138">Stjórnendur geta einnig breytt þessum stillingum fyrir notendur áður en þeir skrá sig inn í fyrsta sinn, þannig að notendur þurfa ekki að gera það sjálfir og gefur þeim betri upplifun við að *hefjast handa*.</span><span class="sxs-lookup"><span data-stu-id="939b2-138">Administrators can also set these settings for users before they log in the first time, so users do not have to do it themselves, providing them a better *getting started* experience.</span></span>

> [!NOTE]
> <span data-ttu-id="939b2-139">Sérstillingar notanda tengjast á engan hátt minniháttar *sérstillingum* sem notandi gerir á upplifun notanda.</span><span class="sxs-lookup"><span data-stu-id="939b2-139">User personalizations do not have anything to do with the *personal* lightweight changes a user can make to the user experience.</span></span>

## <a name="to-review-or-make-changes-to-user-settings"></a><span data-ttu-id="939b2-140">Til að yfirfara eða gera breytingar á notandastillingum</span><span class="sxs-lookup"><span data-stu-id="939b2-140">To review or make changes to user settings</span></span>

1. <span data-ttu-id="939b2-141">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu tákn") slá inn **Sérstillingar notanda** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="939b2-141">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **User Personalizations**, and then choose the related link.</span></span>
2. <span data-ttu-id="939b2-142">Þetta sýnir lista yfir notendur og stillingar þeirra.</span><span class="sxs-lookup"><span data-stu-id="939b2-142">This shows the list of users and their settings.</span></span> <span data-ttu-id="939b2-143">Til að breyta stillingum notanda er smellt á **kenni notanda** eða á **stjórna** og síðan á **breyta**.</span><span class="sxs-lookup"><span data-stu-id="939b2-143">To modify a user's settings, click the **User ID** or choose **Manage** and then **Edit**.</span></span>
3. <span data-ttu-id="939b2-144">Spjaldið **Sérstilling notanda** fyrir stillingar tiltekins notanda er sýnt og hægt er að gera breytingar á stillingum sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="939b2-144">The **User Personlization** card for the specific user's settings is shown and desired changes can be made.</span></span>  

## <a name="see-also"></a><span data-ttu-id="939b2-145">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="939b2-145">See Also</span></span>

[<span data-ttu-id="939b2-146">Hafist handa</span><span class="sxs-lookup"><span data-stu-id="939b2-146">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="939b2-147">Lönd/svæði í boði og studd tungumál</span><span class="sxs-lookup"><span data-stu-id="939b2-147">Country/regional availability and supported languages</span></span>](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations)  
[<span data-ttu-id="939b2-148">Breyta tungumáli og landsstaðli</span><span class="sxs-lookup"><span data-stu-id="939b2-148">Changing Language and Locale</span></span>](about-locale-language.md)  