---
title: "Meðhöndla notendur og hlutverk | Microsoft Docs"
description: "Lærið að meðhöndla notendur og Mitt hlutverk í Business Central."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: profiles, users
ms.date: 10/24/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 7ecd8a5ad2b321d4d1683047e70ede90c7ce229f
ms.contentlocale: is-is
ms.lasthandoff: 11/26/2018

---
# <a name="understanding-users-profiles-and-role-centers"></a><span data-ttu-id="24790-103">Að skilja notendur, forstillingar og Mitt hlutverk</span><span class="sxs-lookup"><span data-stu-id="24790-103">Understanding Users, Profiles, and Role Centers</span></span>

<span data-ttu-id="24790-104">Í [!INCLUDE[d365fin](includes/d365fin_md.md)], eru notendum bætt við af stjórnanda sem gefur einnig notendum aðgang að þeim svæðum [!INCLUDE[d365fin](includes/d365fin_md.md)] sem þeir þurfa í starfi sínu.</span><span class="sxs-lookup"><span data-stu-id="24790-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], users are added by an administrator who also gives users access to the areas of [!INCLUDE[d365fin](includes/d365fin_md.md)] that they need in their work.</span></span>  

<span data-ttu-id="24790-105">Aðgangur að virkni er stjórnað með *notendahópum* og *notandasíðum*.</span><span class="sxs-lookup"><span data-stu-id="24790-105">Access to functionality is managed through *user groups* and *profiles*.</span></span> <span data-ttu-id="24790-106">Sem stjórnandi geturðu bætt við og fjarlægt notendur sem hluta af [!INCLUDE[d365fin](includes/d365fin_md.md)] áskrift þinni og þú getur úthlutað leyfum til notenda í gegnum notendaflokka.</span><span class="sxs-lookup"><span data-stu-id="24790-106">As an administrator, you can add and remove users as part of your [!INCLUDE[d365fin](includes/d365fin_md.md)] subscription, and you can assign users permissions through user groups.</span></span>  

## <a name="adding-users"></a><span data-ttu-id="24790-107">Bæta við notendum</span><span class="sxs-lookup"><span data-stu-id="24790-107">Adding Users</span></span>

<span data-ttu-id="24790-108">Til að bæta við notendum í [!INCLUDE[d365fin](includes/d365fin_md.md)] á netinu, verður stjórnandi Office 365 í fyrirtækinu fyrst að búa til notendur í Office 365 stjórnendamiðstöðinni.</span><span class="sxs-lookup"><span data-stu-id="24790-108">To add users in [!INCLUDE[d365fin](includes/d365fin_md.md)] online, your company's Office 365 administrator must first create the users in the Office 365 Admin Center.</span></span> <span data-ttu-id="24790-109">Frekari upplýsingar, sjá [Bæta notendum við Office 365 for business](https://aka.ms/CreateOffice365Users).</span><span class="sxs-lookup"><span data-stu-id="24790-109">For more information, see [Add Users to Office 365 for business](https://aka.ms/CreateOffice365Users).</span></span>

<span data-ttu-id="24790-110">Síðan getur kerfisstjórinn úthlutað sérhverjum notanda og flokkum notenda leyfi.</span><span class="sxs-lookup"><span data-stu-id="24790-110">Then, the administrator can assign permissions to each user and groups of users.</span></span> <span data-ttu-id="24790-111">Frekari upplýsingar eru í [Stjórna notendum og heimildum](ui-how-users-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="24790-111">For more information, see [Managing Users and Permissions](ui-how-users-permissions.md).</span></span>  

<span data-ttu-id="24790-112">Öflugustu heimildir sem notandi getur haft er SUPER-heimildasamstæðan.</span><span class="sxs-lookup"><span data-stu-id="24790-112">The most powerful permissions that a user can have is the SUPER permission set.</span></span> <span data-ttu-id="24790-113">Hvert fyrirtæki verður að hafa að minnsta kosti einn notanda með þessa heimildasamstæðu, en það er best að gefa hverjum notanda heimildir sem samsvara vinnuþörfum hans í [!INCLUDE[prodshort](includes/prodshort.md)] og ekki meira en það.</span><span class="sxs-lookup"><span data-stu-id="24790-113">Each company must have at least one user with this permission set, but it is a best practice to give each user permissions that match their work needs in [!INCLUDE[prodshort](includes/prodshort.md)] and not more than that.</span></span> <span data-ttu-id="24790-114">Þetta hjálpar til við að tryggja að notendur hafi aðeins aðgang að gögnum sem tengjast vinnu þeirra, til dæmis.</span><span class="sxs-lookup"><span data-stu-id="24790-114">This helps ensure that users only have access to data that is relevant to their work, for example.</span></span>  

> [!TIP]
> <span data-ttu-id="24790-115">Það er best að ganga úr skugga um að Office 365 stjórnandinn hafi einnig SUPER-heimildasamstæðuna í [!INCLUDE[prodshort](includes/prodshort.md)] vegna þess að það auðveldar mörg stjórnunarverk, þar á meðal að setja upp samþættingu við önnur forrit.</span><span class="sxs-lookup"><span data-stu-id="24790-115">It's a best practice to make sure that the Office 365 administrator also has the SUPER permission set in [!INCLUDE[prodshort](includes/prodshort.md)] because that makes many administrative tasks easier, including setting up integration with other apps.</span></span>

### <a name="users-of-on-premises-deployments"></a><span data-ttu-id="24790-116">Notendur uppsetningar á staðnum</span><span class="sxs-lookup"><span data-stu-id="24790-116">Users of on-premises deployments</span></span>

<span data-ttu-id="24790-117">Fyrir uppsetningu á staðnum fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] getur stjórnandi valið á milli mismunandi auðkenningarbúnaðs skilríkja fyrir notendur.</span><span class="sxs-lookup"><span data-stu-id="24790-117">For on-premises deployments of [!INCLUDE[d365fin](includes/d365fin_md.md)], the administrator can choose between different credential authorization mechanisms for users.</span></span> <span data-ttu-id="24790-118">Þegar þú býrð til notanda gefur þú síðan mismunandi upplýsingar eftir því hvaða skilríki þú notar í tilteknu [!INCLUDE[server](includes/server.md)] tilviki.</span><span class="sxs-lookup"><span data-stu-id="24790-118">Then, when you create a user, you provide different information depending on the credential type that you are using in the specific [!INCLUDE[server](includes/server.md)] instance.</span></span> <span data-ttu-id="24790-119">Nánari upplýsingar er að finna í [Gerðir auðkenningar og persónuskilríkja](/dynamics365/business-central/dev-itpro/administration/users-credential-types) í stjórnunarhluta þróunaraðila og ITPro efni fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="24790-119">For more information, see the [Authentication and Credential Types](/dynamics365/business-central/dev-itpro/administration/users-credential-types) in the Administration section of the developer and ITPro content for [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="profiles"></a><span data-ttu-id="24790-120">Forstillingar</span><span class="sxs-lookup"><span data-stu-id="24790-120">Profiles</span></span>

<span data-ttu-id="24790-121">Fólkið í þínu fyrirtæki sem hefur aðgang að [!INCLUDE[d365fin](includes/d365fin_md.md)] er öllum úthlutað *Forstilling* sem veitir þeim aðgang að *Hlutverkamiðstöð*.</span><span class="sxs-lookup"><span data-stu-id="24790-121">The people in your company who have access to [!INCLUDE[d365fin](includes/d365fin_md.md)] are all assigned a *profile* that gives them access to a *Role Center*.</span></span>

<span data-ttu-id="24790-122">Forstillingar eru söfn [!INCLUDE[d365fin](includes/d365fin_md.md)] notenda sem hafa sömu hlutverkamiðstöð (Mitt hlutverk).</span><span class="sxs-lookup"><span data-stu-id="24790-122">Profiles are collections of [!INCLUDE[d365fin](includes/d365fin_md.md)] users who share the same Role Center.</span></span> <span data-ttu-id="24790-123">Hlutverkamiðstöð er aðgangsstaður og heimasíða fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] sem gefur þér skjótan aðgang að mikilvægustu verkum þínum og birtir ýmsar innsýnir og afkastavísa um vinnu þína.</span><span class="sxs-lookup"><span data-stu-id="24790-123">A Role Center is the entry point and home page for [!INCLUDE[d365fin](includes/d365fin_md.md)] that gives you quick access to your most important tasks and displays various insights and key performance indicators (KPIs) about your work.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="24790-124">Í núverandi útgáfu af [!INCLUDE[d365fin](includes/d365fin_md.md)] á netinu, er ekki hægt að bæta við, breyta eða eyða snið.</span><span class="sxs-lookup"><span data-stu-id="24790-124">In the current version of [!INCLUDE[d365fin](includes/d365fin_md.md)] online, you cannot add, edit, or delete profiles.</span></span>  

### <a name="CreateProfile"></a><span data-ttu-id="24790-125">Stofna forstillingu</span><span class="sxs-lookup"><span data-stu-id="24790-125">Create a profile</span></span>

1.  <span data-ttu-id="24790-126">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Forstillingalisti** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="24790-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Profile List**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="24790-127">Á síðunni **Forstillingalisti** skal velja aðgerðina **Nýtt** til að opna síðuna **Nýtt forstillingarspjald**.</span><span class="sxs-lookup"><span data-stu-id="24790-127">On the **Profile List** page, choose the **New** action to open the **New Profile Card** page.</span></span>  

3.  <span data-ttu-id="24790-128">Í reitnum **Kenni forstillingar** færið inn nafn sem lýsir ætluðum hlutverk notenda.</span><span class="sxs-lookup"><span data-stu-id="24790-128">In the **Profile ID** field, enter a name that describes the intended role of the users.</span></span>  

4.  <span data-ttu-id="24790-129">Í reitinn **Lýsing** er slegin inn lýsing á kenni forstillingar, t.d. **Pantanavinnsla**.</span><span class="sxs-lookup"><span data-stu-id="24790-129">In the **Description** field, enter a description of the Profile ID, for example, **Order Processor**.</span></span>  

5.  <span data-ttu-id="24790-130">Stilltu **Kenni fyrir Mitt hlutverk** reitinn á Mitt hlutverk sem þú vilt tengja við forstillinguna.</span><span class="sxs-lookup"><span data-stu-id="24790-130">Set the **Role Center ID** field to the Role Center that you want to assign to the profile.</span></span>  

<span data-ttu-id="24790-131">Ferlið til þess að breyta fyrirliggjandi forstillingu er hið sama, nema að valin er eldri forstilling á síðunni **Forstillingalisti** í stað þess að velja aðgerðina **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="24790-131">The procedure for modifying an existing profile is the same, except you select an existing profile on the **Profile List** page instead of choosing the **New** action.</span></span>  


### <a name="copy-a-profile"></a><span data-ttu-id="24790-132">Afrita forstillingu</span><span class="sxs-lookup"><span data-stu-id="24790-132">Copy a profile</span></span>
<span data-ttu-id="24790-133">Afritun forstillingar getur sparað tíma ef nota á sambærilegar stillingar á forstillingu og eingöngu á að breyta nokkrum stillingum.</span><span class="sxs-lookup"><span data-stu-id="24790-133">Copying a profile can save you time if you want to use similar settings on a profile and you only want to change a few settings.</span></span>

1.  <span data-ttu-id="24790-134">Opnaðu forstillinguna sem þú vilt afrita og veldu svo **Afrita forstillingu** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="24790-134">Open the profile that you want to copy, and then choose the **Copy Profile** action.</span></span>

2.  <span data-ttu-id="24790-135">Í reitnum **Nýtt kenni forstillingar** er slegið inn nafn á forstillingunni sem á að afrita.</span><span class="sxs-lookup"><span data-stu-id="24790-135">In **New Profile ID** field, enter a name for the profile that you want to copy.</span></span>

3.  <span data-ttu-id="24790-136">Stilltu **Nýtt umfang forstillingar** reitinn á eitt af eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="24790-136">Set the **New Profile Scope** field to one of the following:</span></span>

    - <span data-ttu-id="24790-137">**Kerfi** til að gera nýja forstillingu aðgengilega fyrir alla gagnagrunna leigjenda sem nota forritið.</span><span class="sxs-lookup"><span data-stu-id="24790-137">**System** to make the new profile available to all tenant databases that use the application.</span></span>
    - <span data-ttu-id="24790-138">**Leigjandi** til að gera nýja forstillingu aðgengilega aðeins fyrir núverandi gagnagrunn leigjenda.</span><span class="sxs-lookup"><span data-stu-id="24790-138">**Tenant** to make the new profile available to just the current tenant database.</span></span>
4. <span data-ttu-id="24790-139">Velja hnappinn **Í lagi** að því loknu.</span><span class="sxs-lookup"><span data-stu-id="24790-139">Choose the **OK** button when done.</span></span>

### <a name="ExportImportProfile"></a><span data-ttu-id="24790-140">Útflutningur og innflutningur forstillinga</span><span class="sxs-lookup"><span data-stu-id="24790-140">Export and import profiles</span></span>

<span data-ttu-id="24790-141">Hægt er að flytja forstillingu inn og út sem XML-skrár til og frá [!INCLUDE[d365fin](includes/d365fin_md.md)] gagnagrunninum.</span><span class="sxs-lookup"><span data-stu-id="24790-141">You can export and import profiles as XML files to and from the a [!INCLUDE[d365fin](includes/d365fin_md.md)] database.</span></span> <span data-ttu-id="24790-142">Inn- og útflutningur forstillingar getur sparað þér tíma þegar þú stillir notendaviðmótið þar sem þú endurnýjar núverandi uppsetningu stillingar í stað þess að þurfa að stilla forstillingu frá grunni.</span><span class="sxs-lookup"><span data-stu-id="24790-142">Exporting and importing a profile can save you time when configuring the user interface because you reuse an existing profile configuration instead of having to configure a profile from scratch.</span></span> <span data-ttu-id="24790-143">Ef þú ert með forstillingu sem er stillt í [!INCLUDE[d365fin](includes/d365fin_md.md)] gagnagrunni og vilt endurnýta allar eða nokkrar uppsetningarstillingar í öðrum gagnagrunni getur þú flutt sniðið út í XML-skrá.</span><span class="sxs-lookup"><span data-stu-id="24790-143">If you have a profile that is configured in a [!INCLUDE[d365fin](includes/d365fin_md.md)] database and you would like to reuse all or some of the same profile configurations in another database, you can export the profile to an XML file.</span></span> <span data-ttu-id="24790-144">Þá er hægt að flytja inn XML-skrá forstillingarinnar í hinn gagnagrunninn.</span><span class="sxs-lookup"><span data-stu-id="24790-144">Then, you can import the profile XML file into the other database.</span></span>

-   <span data-ttu-id="24790-145">Til að flytja út forstillingu er annaðhvort hægt að velja aðgerðina **Flytja út forstillingar** frá síðunni **Forstillingalisti** eða **Forstillingarspjald** eða leita að og opna síðuna **Flytja út forstillingar**.</span><span class="sxs-lookup"><span data-stu-id="24790-145">To export a profile, you can either choose the **Export Profiles** action from the **Profile List** or **Profile Card** page or you can search for and open the **Export Profiles** page.</span></span> <span data-ttu-id="24790-146">Vistið XML-skrána á stað í tölvu eða á neti.</span><span class="sxs-lookup"><span data-stu-id="24790-146">Save the XML file to a location on your computer or network.</span></span>

-   <span data-ttu-id="24790-147">Til að flytja inn forstillingu er annaðhvort hægt að velja aðgerðina **Flytja inn forstillingar** frá síðunni **Forstillingalisti** eða leita að og opna síðuna **Flytja inn forstillingar**.</span><span class="sxs-lookup"><span data-stu-id="24790-147">To import a profile, you can either choose the **Import Profile** action from the **Profile List** page, or you can search for and open the **Import Profiles** page.</span></span> 

    > [!NOTE]  
    >  <span data-ttu-id="24790-148">Ekki er hægt að flytja inn forstillingu sem þegar er til í gagnagrunninum, jafnvel þótt XML-skráin hafi annað heiti eða annað innihald.</span><span class="sxs-lookup"><span data-stu-id="24790-148">You cannot import a profile that already exists in the database, even though the XML file is named differently or has different content.</span></span> <span data-ttu-id="24790-149">Eyða verður forstillingumsem fyrir eru áður en hægt er að flytja inn nýju forstillinguna.</span><span class="sxs-lookup"><span data-stu-id="24790-149">You must delete the existing profile before you can import the new profile.</span></span>


## <a name="configuration-and-personalization"></a><span data-ttu-id="24790-150">Grunnstilling og sérstillingar</span><span class="sxs-lookup"><span data-stu-id="24790-150">Configuration and Personalization</span></span>
<!--The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:  

-   Configuration, performed by the administrator  

-   Personalization, performed by users  

The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.  -->

<span data-ttu-id="24790-151">Notendur sérsníða notendaviðmót sinnar útgáfu með því að sérsníða notendaviðmót undir eigin notandinafni.</span><span class="sxs-lookup"><span data-stu-id="24790-151">Users personalize the user interface of their personal version by customizing the user interface under their own user logon.</span></span> <span data-ttu-id="24790-152">Stjórnandinn getur eytt þessari aðlögun.</span><span class="sxs-lookup"><span data-stu-id="24790-152">This personalization can be deleted by the administrator.</span></span> <span data-ttu-id="24790-153">Frekari upplýsingar eru í [Sérstilling vinnusvæðisins þíns](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="24790-153">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="24790-154">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="24790-154">See Also</span></span>  
[<span data-ttu-id="24790-155">Vinna með notendur og heimildir</span><span class="sxs-lookup"><span data-stu-id="24790-155">Managing Users and Permissions</span></span>](ui-how-users-permissions.md)  
[<span data-ttu-id="24790-156">Stjórnun sérstillinga sem stjórnandi</span><span class="sxs-lookup"><span data-stu-id="24790-156">Managing Personalization as an Administrator</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="24790-157">Sérstillingar verksvæðis</span><span class="sxs-lookup"><span data-stu-id="24790-157">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  

