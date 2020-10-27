---
title: Setja upp tölvupóstskráningu | Microsoft Docs
description: Kynntu þér hvernig tölvupóstsamskipti milli sölufólks og viðskiptavina geta skapað alvöru sölutækifærum.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: f02e78e0b5c7d7f6d3c22cd12e37bdaf74f4b90f
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3923621"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a><span data-ttu-id="30490-103">Fylgstu með tölvupóstsamskiptum milli sölufólks og tengiliða</span><span class="sxs-lookup"><span data-stu-id="30490-103">Track Email Message Exchanges Between Salespeople and Contacts</span></span>

<span data-ttu-id="30490-104">Fáðu meira út úr samskiptum sölumanna við núverandi eða mögulega viðskiptavini þína með því að rekja tölvupóstsamskipti og breyta þeim síðan í möguleg tækifæri.</span><span class="sxs-lookup"><span data-stu-id="30490-104">Get more out of the communications between salespeople and your existing or potential customers by tracking email exchanges, and then turning them into actionable opportunities.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="30490-105">getur unnið með Exchange Online til að halda skrá yfir skilaboð á inn- og útleið.</span><span class="sxs-lookup"><span data-stu-id="30490-105">can work with Exchange Online to keep a log of the inbound and outbound messages.</span></span> <span data-ttu-id="30490-106">Þú getur skoðað og greint innihald skilaboða á síðunni **Samskiptaskráningarfærslur** .</span><span class="sxs-lookup"><span data-stu-id="30490-106">You can view and analyze the contents of each message on the **Interaction Log Entries** page.</span></span>

## <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a><span data-ttu-id="30490-107">Setja upp almenningsmöppur og reglur fyrir tölvupóstsskráningu á Exchange Online</span><span class="sxs-lookup"><span data-stu-id="30490-107">Set up Public Folders and Rules for Email Logging in Exchange Online</span></span>

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

<span data-ttu-id="30490-108">Næst tengir þú [!INCLUDE[prodshort](includes/prodshort.md)] við Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="30490-108">Next, you connect [!INCLUDE[prodshort](includes/prodshort.md)] with Exchange Online.</span></span>

## <a name="setting-up-d365fin-to-log-email-messages"></a><span data-ttu-id="30490-109">Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)] til að skrá tölvupóstskilaboð</span><span class="sxs-lookup"><span data-stu-id="30490-109">Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)] to Log Email Messages</span></span>

<span data-ttu-id="30490-110">Hafist handa með tölvupóstskráningu í tveimur einföldum skrefum:</span><span class="sxs-lookup"><span data-stu-id="30490-110">Get started with email logging in two easy steps:</span></span>

1. <span data-ttu-id="30490-111">Tengið [!INCLUDE[d365fin](includes/d365fin_md.md)] við Exchange Online fyrir Microsoft 365-áskriftina.</span><span class="sxs-lookup"><span data-stu-id="30490-111">Connect [!INCLUDE[d365fin](includes/d365fin_md.md)] with Exchange Online for your Microsoft 365 subscription.</span></span> <span data-ttu-id="30490-112">Exchange Online sér um tölvupóstskilaboðin þín.</span><span class="sxs-lookup"><span data-stu-id="30490-112">Exchange Online handles your email messages.</span></span> <span data-ttu-id="30490-113">Við höfum einfaldað þetta skref með því að bjóða upp á uppsetningarleiðbeiningar.</span><span class="sxs-lookup"><span data-stu-id="30490-113">We've made this step easy by providing an assisted setup guide.</span></span> <span data-ttu-id="30490-114">Aðeins þarf innskráningarupplýsingar stjórnanda fyrir stjórnandareikning í Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="30490-114">You just need your administrator credentials for your administrator account in Microsoft 365.</span></span> <span data-ttu-id="30490-115">Til að hefja leiðsögnina skaltu fara í **Uppsetning með hjálp** og velja síðan **Setja upp tölvupóstskráningu** .</span><span class="sxs-lookup"><span data-stu-id="30490-115">To start the guide, go to **Assisted Setup** , and then choose **Set up email logging** .</span></span>  

2. <span data-ttu-id="30490-116">Gakktu úr skugga um að gild netföng hafi verið slegin inn í [!INCLUDE[d365fin](includes/d365fin_md.md)] fyrir sölufólk og tengiliði, sem er háð því hvort um sé að ræða mögulega eða núverandi viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="30490-116">Make sure that valid email addresses have been entered in [!INCLUDE[d365fin](includes/d365fin_md.md)] for your sales people and contacts, depending on whether they are potential or existing customers.</span></span> <span data-ttu-id="30490-117">Til að gera það fyrir hvern viðskiptavin eða sölumann skal opna spjaldið **Tengiliður** eða **Sölumaður/innkaupaaðili** og kíkja í reitinn **Netfang** .</span><span class="sxs-lookup"><span data-stu-id="30490-117">To do that, for each customer or salesperson, open the **Contact** or **Salesperson/Purchaser** card and have a look in the **Email** field.</span></span>

> [!Tip]
> <span data-ttu-id="30490-118">Eftir að þú hefur lokið skrefum leiðsagnarinnar geturðu athugað hvort tengingin hafi borið árangur.</span><span class="sxs-lookup"><span data-stu-id="30490-118">After you complete the steps in the guide you can check whether the connection was successful.</span></span> <span data-ttu-id="30490-119">Leitaðu að **Uppsetning markaðssetningar** , veldu **Ferli** , síðan **Aðgerðir** og að lokum **Staðfesta uppsetningu tölvupóstskráningar** .</span><span class="sxs-lookup"><span data-stu-id="30490-119">Search for **Marketing Setup** , choose **Process** , then **Functions** , and then **Validate Email Logging Setup** .</span></span>

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a><span data-ttu-id="30490-120">Að skoða tölvupóstsamskipti í samskiptaskránni</span><span class="sxs-lookup"><span data-stu-id="30490-120">Viewing Email Message Exchanges in the Interaction Log</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="30490-121">býr til færslu á síðunni **Samskiptaskrá** í hvert skipti sem sölumaður og tengiliður skiptast á tölvupóstskilaboðum.</span><span class="sxs-lookup"><span data-stu-id="30490-121">creates an entry on the **Interaction Log** page each time a salesperson and a contact exchange an email message.</span></span> <span data-ttu-id="30490-122">Til að skoða samskiptakladdann skal opna spjaldið **Tengiliður** eða **Sölumaður innkaupaaðila** fyrir einstaklinginn og síðan velja **Ferill** og síðan velja **Færslur í samskiptaskráningu** .</span><span class="sxs-lookup"><span data-stu-id="30490-122">To view the interaction log, open the **Contact** or **Salesperson Purchaser** card for the person, and then choose **History** , and then choose **Interaction Log Entries** .</span></span> <span data-ttu-id="30490-123">Við getum gert nokkra hluti við hverja færslu í skránni, til dæmis:</span><span class="sxs-lookup"><span data-stu-id="30490-123">There are a few things we can do with each entry in the log, for example:</span></span>

- <span data-ttu-id="30490-124">Skoðaðu innihald tölvupóstsins sem var sendur á milli með því að smella á aðgerðina **Sýna viðhengi** .</span><span class="sxs-lookup"><span data-stu-id="30490-124">View the content of the email message that was exchanged by clicking the **Show Attachments** action.</span></span>
- <span data-ttu-id="30490-125">Breyttu tölvupóstsamskiptum í sölutækifæri - Þú getur skapað tækifæri úr færslu sem lofar góðu og náð sölu út úr henni.</span><span class="sxs-lookup"><span data-stu-id="30490-125">Turn an email exchange into a sales opportunity - If an entry looks promising, you can turn it into an opportunity and then manage its progress toward a sale.</span></span> <span data-ttu-id="30490-126">Til að gera það skaltu velja færsluna og síðan aðgerðina **Stofna tækifæri** .</span><span class="sxs-lookup"><span data-stu-id="30490-126">To do that, choose the entry, and then choose the **Create Opportunity** action.</span></span> <span data-ttu-id="30490-127">Nánari upplýsingar er að finna í [Umsjón sölutækifæra](marketing-manage-sales-opportunities.md).</span><span class="sxs-lookup"><span data-stu-id="30490-127">For more information, see [Managing Sales Opportunities](marketing-manage-sales-opportunities.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="30490-128">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="30490-128">See Also</span></span>
[<span data-ttu-id="30490-129">Stjórnun tengsla</span><span class="sxs-lookup"><span data-stu-id="30490-129">Managing Relationships</span></span>](marketing-relationship-management.md)

