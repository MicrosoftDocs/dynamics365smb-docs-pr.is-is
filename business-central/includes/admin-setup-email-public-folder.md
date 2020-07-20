---
author: edupont04
ms.service: dynamics365-accountant
ms.topic: include
ms.date: 06/25/2020
ms.author: edupont
ms.openlocfilehash: 8c5f4205128d52ec88f432cea7ece98e0310546d
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/01/2020
ms.locfileid: "3528011"
---
<span data-ttu-id="22948-101">Áður en hægt er að setja upp tölvupóstsskráningu þarf að undirbúa Exchange Online með [opnum möppum](/exchange/collaboration/public-folders/public-folders?view=exchserver-2019).</span><span class="sxs-lookup"><span data-stu-id="22948-101">Before you can set up email logging, you must prepare your Exchange Online with [public folders](/exchange/collaboration/public-folders/public-folders?view=exchserver-2019).</span></span> <span data-ttu-id="22948-102">Hægt er að gera þetta í [Exchange stjórnendamiðstöðinni](/Exchange/architecture/client-access/exchange-admin-center?view=exchserver-2019) eða nota [Exchange Management Shell](/powershell/exchange/exchange-management-shell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="22948-102">You can do this in the [Exchange admin center](/Exchange/architecture/client-access/exchange-admin-center?view=exchserver-2019), or you can use the [Exchange Management Shell](/powershell/exchange/exchange-management-shell?view=exchange-ps).</span></span>  

> [!TIP]
> <span data-ttu-id="22948-103">Ef þú vilt nota [Exchange Management Shell](/powershell/exchange/exchange-management-shell?view=exchange-ps) getur þú fengið innblástur hvernig á að setja upp forskrift í sýnisforskrift sem við birtum í [BCTech-geymslunni](https://github.com/microsoft/BCTech/tree/master/samples/EmailLogging).</span><span class="sxs-lookup"><span data-stu-id="22948-103">If you want to use the [Exchange Management Shell](/powershell/exchange/exchange-management-shell?view=exchange-ps), you can find inspiration for how to set up your script in a sample script that we published to [the BCTech repo](https://github.com/microsoft/BCTech/tree/master/samples/EmailLogging).</span></span>

<span data-ttu-id="22948-104">Eftirfarandi listi lýsir helstu skrefum til að fá frekari upplýsingar um tengla.</span><span class="sxs-lookup"><span data-stu-id="22948-104">The following list describes the main steps with links to learn more.</span></span>  

- <span data-ttu-id="22948-105">Stofna stjórnandahlutverk fyrir almenningsmöppur á grunni upplýsinganna í eftirfarandi töflu:</span><span class="sxs-lookup"><span data-stu-id="22948-105">Create an admin role for public folders based on the information in the following table:</span></span>

  |<span data-ttu-id="22948-106">Eiginleiki</span><span class="sxs-lookup"><span data-stu-id="22948-106">Property</span></span>        |<span data-ttu-id="22948-107">Gildi:</span><span class="sxs-lookup"><span data-stu-id="22948-107">Value</span></span>                     |
  |----------------|--------------------------|
  |<span data-ttu-id="22948-108">Name</span><span class="sxs-lookup"><span data-stu-id="22948-108">Name</span></span>            |<span data-ttu-id="22948-109">Stjórnun almenningsmappa</span><span class="sxs-lookup"><span data-stu-id="22948-109">Public Folders Management</span></span> |
  |<span data-ttu-id="22948-110">Valin hlutverk</span><span class="sxs-lookup"><span data-stu-id="22948-110">Selected roles</span></span>  |<span data-ttu-id="22948-111">Opnar möppur</span><span class="sxs-lookup"><span data-stu-id="22948-111">Public Folders</span></span>            |
  |<span data-ttu-id="22948-112">Valdir meðlimir</span><span class="sxs-lookup"><span data-stu-id="22948-112">Selected members</span></span>|<span data-ttu-id="22948-113">Tölvupóstur notandareiknings sem Business Central mun nota til að keyra verk tölvupóstsskráningar</span><span class="sxs-lookup"><span data-stu-id="22948-113">The email of the user account that Business Central will use to run the email logging job</span></span>|

  <span data-ttu-id="22948-114">Frekari upplýsingar eru í [Stjórna hlutverkahópum](/exchange/permissions/role-groups?view=exchserver-2019).</span><span class="sxs-lookup"><span data-stu-id="22948-114">For more information, see [Manage role groups](/exchange/permissions/role-groups?view=exchserver-2019).</span></span>

- <span data-ttu-id="22948-115">Stofnið nýtt pósthólf með opna möppu á grundvelli upplýsinganna í eftirfarandi töflu:</span><span class="sxs-lookup"><span data-stu-id="22948-115">Create a new public folder mailbox based on the information in the following table:</span></span>

  |<span data-ttu-id="22948-116">Eiginleiki</span><span class="sxs-lookup"><span data-stu-id="22948-116">Property</span></span>        |<span data-ttu-id="22948-117">Gildi:</span><span class="sxs-lookup"><span data-stu-id="22948-117">Value</span></span>                     |
  |----------------|--------------------------|
  |<span data-ttu-id="22948-118">Name</span><span class="sxs-lookup"><span data-stu-id="22948-118">Name</span></span>            |<span data-ttu-id="22948-119">Opið pósthólf</span><span class="sxs-lookup"><span data-stu-id="22948-119">Public MailBox</span></span>            |

  <span data-ttu-id="22948-120">Frekari upplýsingar er að finna á [Búa til pósthólf með opinni möppu í Exchange Server](/exchange/collaboration/public-folders/create-public-folder-mailboxes).</span><span class="sxs-lookup"><span data-stu-id="22948-120">For more information, see [Create a public folder mailbox in Exchange Server](/exchange/collaboration/public-folders/create-public-folder-mailboxes).</span></span>  

- <span data-ttu-id="22948-121">Stofna nýjar almenningsmöppur</span><span class="sxs-lookup"><span data-stu-id="22948-121">Create new public folders</span></span>

  - <span data-ttu-id="22948-122">Stofnið nýja opna möppu með heitinu *Tölvupóstsskráning* í rótinni þannig að slóðin á möppuna verði ```\Email Logging\```</span><span class="sxs-lookup"><span data-stu-id="22948-122">Create a new public folder with the name *Email Logging* in the root so that the full path to the folder becomes ```\Email Logging\```</span></span>
  - <span data-ttu-id="22948-123">Búa til tvær undirmöppur þannig að útkoman sé eftirfarandi heilar slóðir í möppurnar:</span><span class="sxs-lookup"><span data-stu-id="22948-123">Create two subfolders so that the the result is the following full paths to the folders:</span></span>
    - ```\Email Logging\Queue\```
    - ```\Email Logging\Storage\```

  <span data-ttu-id="22948-124">Nánari upplýsingar má finna í [Búa til opna möppu](/exchange/collaboration/public-folders/create-public-folders?view=exchserver-2019).</span><span class="sxs-lookup"><span data-stu-id="22948-124">For more information, see [Create a public folder](/exchange/collaboration/public-folders/create-public-folders?view=exchserver-2019).</span></span>

- <span data-ttu-id="22948-125">Virkja tölvupóst fyrir *biðröð* opinnar möppu</span><span class="sxs-lookup"><span data-stu-id="22948-125">Mail-enable the *Queue* public folder</span></span>

  <span data-ttu-id="22948-126">Frekari upplýsingar er að finna á [Kveika eða slökkva á tölvupósti fyrir opna möppu](/exchange/collaboration/public-folders/mail-enable-or-disable?view=exchserver-2019)</span><span class="sxs-lookup"><span data-stu-id="22948-126">For more information, see [Mail-enable or mail-disable a public folder](/exchange/collaboration/public-folders/mail-enable-or-disable?view=exchserver-2019)</span></span>

- <span data-ttu-id="22948-127">Þegar tölvupóstur er virkjaður er hægt að senda tölvupóst á *biðröð* opnu möppunnar með Outlook eða Exchange Management Shell</span><span class="sxs-lookup"><span data-stu-id="22948-127">Mail-enable sending emails to the *Queue* public folder using Outlook or the Exchange Management Shell</span></span>

  <span data-ttu-id="22948-128">Frekari upplýsingar er að finna á [Heimila ónafngreindum notendum að senda tölvupóst í opna möppu þar sem búið er að virkja tölvupóst](/exchange/collaboration/public-folders/mail-enable-or-disable?view=exchserver-2019#allow-anonymous-users-to-send-email-to-a-mail-enabled-public-folder)</span><span class="sxs-lookup"><span data-stu-id="22948-128">For more information, see [Allow anonymous users to send email to a mail-enabled public folder](/exchange/collaboration/public-folders/mail-enable-or-disable?view=exchserver-2019#allow-anonymous-users-to-send-email-to-a-mail-enabled-public-folder)</span></span>

- <span data-ttu-id="22948-129">Stillið notanda tölvupóstsskráningar sem eiganda að báðum opnu möppunum, opnu möppunum *Biðröð* og *Geymsla* með Outlook eða Exchange Management Shell á grundvelli upplýsinganna sem birtast í eftirfarandi töflu:</span><span class="sxs-lookup"><span data-stu-id="22948-129">Set the email logging user as an owner of both public folders, *Queue* and *Storage* public folders  using Outlook or the Exchange Management Shell based on the information in the following table:</span></span>

  |<span data-ttu-id="22948-130">Eiginleiki</span><span class="sxs-lookup"><span data-stu-id="22948-130">Property</span></span>        |<span data-ttu-id="22948-131">Gildi:</span><span class="sxs-lookup"><span data-stu-id="22948-131">Value</span></span>                     |
  |----------------|--------------------------|
  |<span data-ttu-id="22948-132">Notandi</span><span class="sxs-lookup"><span data-stu-id="22948-132">User</span></span>            |<span data-ttu-id="22948-133">Tölvupóstur notandareiknings sem Business Central mun nota til að keyra verk tölvupóstsskráningar</span><span class="sxs-lookup"><span data-stu-id="22948-133">The email of the user account that Business Central will use to run the email logging job</span></span>|
  |<span data-ttu-id="22948-134">Heimildarstig</span><span class="sxs-lookup"><span data-stu-id="22948-134">Permission level</span></span>|<span data-ttu-id="22948-135">Eigandi</span><span class="sxs-lookup"><span data-stu-id="22948-135">Owner</span></span>                     |

  <span data-ttu-id="22948-136">Frekari upplýsingar er að finna í [Úthluta heimildum fyrir opnu möppuna](/exchange/collaboration-exo/public-folders/set-up-public-folders#step-3-assign-permissions-to-the-public-folder).</span><span class="sxs-lookup"><span data-stu-id="22948-136">For more information, see [Assign permissions to the public folder](/exchange/collaboration-exo/public-folders/set-up-public-folders#step-3-assign-permissions-to-the-public-folder).</span></span>

- <span data-ttu-id="22948-137">Búa til tvær reglur um póstflæði út frá upplýsingunum í eftirfarandi töflu</span><span class="sxs-lookup"><span data-stu-id="22948-137">Create two mail flow rules based on the information in the following table</span></span>

  |<span data-ttu-id="22948-138">Tilgangur</span><span class="sxs-lookup"><span data-stu-id="22948-138">Purpose</span></span>  |<span data-ttu-id="22948-139">Name</span><span class="sxs-lookup"><span data-stu-id="22948-139">Name</span></span> |<span data-ttu-id="22948-140">Skilyrði</span><span class="sxs-lookup"><span data-stu-id="22948-140">Conditions</span></span>                        |<span data-ttu-id="22948-141">Aðgerð</span><span class="sxs-lookup"><span data-stu-id="22948-141">Action</span></span>                                       |
  |---------|-----|----------------------------------|---------------------------------------------|
  |<span data-ttu-id="22948-142">Regla fyrir móttekinn tölvupóst</span><span class="sxs-lookup"><span data-stu-id="22948-142">A rule for incoming email</span></span> |<span data-ttu-id="22948-143">Skrá tölvupóst sem sendur er til þessa fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="22948-143">Log Email Sent to This Organization</span></span>|<span data-ttu-id="22948-144">*Sendandi* er staðsettur *utan fyrirtækis* og *viðtakandinn* er staðsettur *innan fyrirtækis*</span><span class="sxs-lookup"><span data-stu-id="22948-144">*The sender* is located *Outside the organization*, and *the recipient* is located *Inside the organization*</span></span>|<span data-ttu-id="22948-145">Sendu falið afrit til netfangsins sem tilgreint er fyrir *biðröð* opnu möppurnar</span><span class="sxs-lookup"><span data-stu-id="22948-145">BCC the email account that is specified for the *Queue* public folder</span></span>|
  |<span data-ttu-id="22948-146">Regla fyrir sendan tölvupóst</span><span class="sxs-lookup"><span data-stu-id="22948-146">A rule for outgoing email</span></span> | <span data-ttu-id="22948-147">Skrá tölvupóst sem sendur er frá þessu fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="22948-147">Log Email Sent from This Organization</span></span> |<span data-ttu-id="22948-148">*Sendandi* er staðsettur *innan fyrirtækisins* og *viðtakandinn* er staðsettur *utan fyrirtækis*</span><span class="sxs-lookup"><span data-stu-id="22948-148">*The sender* is located *Inside the organization*, and *the recipient* is located *Outside the organization*</span></span>|<span data-ttu-id="22948-149">Sendu falið afrit til netfangsins sem tilgreint er fyrir *biðröð* opnu möppurnar</span><span class="sxs-lookup"><span data-stu-id="22948-149">BCC the email account that is specified for the *Queue* public folder</span></span>|
  
  <span data-ttu-id="22948-150">Frekari upplýsingar er að finna á [Reglum um póstflæði í Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules) og [Aðgerðum reglu um póstflæði í Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-action).</span><span class="sxs-lookup"><span data-stu-id="22948-150">For more information, see [Manage mail flow rules in Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules) and [Mail flow rule actions in Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-action).</span></span>

> [!NOTE]
> <span data-ttu-id="22948-151">Ef gerðar eru breytingar á Exchange Management Shell verða breytingarnar sýnilegar í stjórnunarmiðstöð Exchange eftir nokkra töf.</span><span class="sxs-lookup"><span data-stu-id="22948-151">If you make changes in the Exchange Management Shell, the changes become visible in the Exchange admin center after a delay.</span></span> <span data-ttu-id="22948-152">Einnig verða breytingar sem gerðar hafa verið í Exchange í boði í [!INCLUDE[prodshort](prodshort.md)] eftir seinkun.</span><span class="sxs-lookup"><span data-stu-id="22948-152">Also, the changes made in Exchange will be available in [!INCLUDE[prodshort](prodshort.md)] after a delay.</span></span>
