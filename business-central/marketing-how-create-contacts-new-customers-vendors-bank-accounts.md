---
title: "Stofna viðskiptamann eða lánardrottinn út frá tengilið| Microsoft Docs"
description: "Hægt er að skrá fyrirliggjandi tengilið sem viðskiptamann, lánadrottinn eða bankareikninga með því að nota fyrirliggjandi upplýsingar og tiltaka eðli viðskiptasambands."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: e1f1d9e89d4164f36fb90c027cd636da67bc40d9
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="create-a-customer-vendor-or-bank-account-from-a-contact"></a><span data-ttu-id="3c3fd-103">Stofna viðskiptamanni, lánadrottni eða bankareikning úr tengilið</span><span class="sxs-lookup"><span data-stu-id="3c3fd-103">Create a Customer, Vendor, or Bank Account From a Contact</span></span>
<span data-ttu-id="3c3fd-104">Suma fyrirliggjandi tengiliði er ef til vill æskilegt að skrá sem viðskiptamenn, lánadrottna eða bankareikninga.</span><span class="sxs-lookup"><span data-stu-id="3c3fd-104">You may want to record some of your existing contacts as customers, vendors, or bank accounts.</span></span> <span data-ttu-id="3c3fd-105">Stofna viðskiptamanni, lánadrottni eða bankareikning úr tengilið gerir þér kleift að nota fyrirliggjandi gögn.</span><span class="sxs-lookup"><span data-stu-id="3c3fd-105">Creating a customer, vendor, or bank account from a contact enables you use existing data.</span></span> <span data-ttu-id="3c3fd-106">Þegar þú stofnar viðskiptavin, lánardrottinn, eða bankareikning á þennan hátt er það samstillt við tengiliðinn.</span><span class="sxs-lookup"><span data-stu-id="3c3fd-106">When you create a customer, vendor, or bank account this way, it is synchronized with the contact.</span></span> <span data-ttu-id="3c3fd-107">Samstilling gerir upplýsingarnar sem eru sameiginleg tengiliði og viðskiptamenn, lánardrottna eða bankareikninga þær sömu.</span><span class="sxs-lookup"><span data-stu-id="3c3fd-107">Synchronization makes information that is common between contacts and customers, vendors, or bank account the same.</span></span>

<span data-ttu-id="3c3fd-108">áður en þú getur skráð tengiliði á þennan hátt, verðurðu að tilgreina viðskiptatengslakóða fyrir viðskiptavini, lánardrottna, og bankareikninga í glugganum **uppsetning markaðssetningar**</span><span class="sxs-lookup"><span data-stu-id="3c3fd-108">Before you can record contacts this way, you must specify a business relation code for customers, vendors, and bank accounts in the **Marketing Setup** window.</span></span> <span data-ttu-id="3c3fd-109">Ef þú munt skrá tengiliði sem bankareikning verður einnig að tilgreina númeraraðir fyrir bankareikninga í glugganum **Fjárhagsgrunnur**.</span><span class="sxs-lookup"><span data-stu-id="3c3fd-109">If you will be recording contacts as bank accounts, you must also specify numbers series for bank accounts in the **General Ledger Setup** window.</span></span>

## <a name="to-create-a-contact-as-a-customer-vendor-or-bank-account"></a><span data-ttu-id="3c3fd-110">Tengiliðir stofnaðir sem viðskiptamenn, lánadrottnar eða bankareikningar:</span><span class="sxs-lookup"><span data-stu-id="3c3fd-110">To create a contact as a customer, vendor, or bank account</span></span>
1. <span data-ttu-id="3c3fd-111">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Tengiliðir** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="3c3fd-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Contacts**, and then choose the related link.</span></span>
2. <span data-ttu-id="3c3fd-112">Velja skal tengiliðinn sem stofna á sem viðskiptamann, lánadrottinn eða bankareikning.</span><span class="sxs-lookup"><span data-stu-id="3c3fd-112">Select the contact you want to create as a customer, vendor, or bank account.</span></span>
3. <span data-ttu-id="3c3fd-113">Veldu aðgerðina **Stofna sem** og síðan valinn annað hvort **Viðskiptamaður**, **Lánadrottinn** eða **Banki**.</span><span class="sxs-lookup"><span data-stu-id="3c3fd-113">Choose the **Create As** action, and then choose either **Customer**, **Vendor**, or **Bank**.</span></span>
4. <span data-ttu-id="3c3fd-114">Staðfesta þarf eftirfarandi skilaboð.</span><span class="sxs-lookup"><span data-stu-id="3c3fd-114">Confirm the subsequent message.</span></span>

<span data-ttu-id="3c3fd-115">Tengslaupplýsingarnar eru fluttar úr spjaldinu **Tengiliður** yfir í spjaldið **Bankareikningur**, spjaldið **Viðskiptamaður**, eða spjaldið **Lánardrottinn**.</span><span class="sxs-lookup"><span data-stu-id="3c3fd-115">The contact information is transferred from the **Contact** card to the **Bank Account** card, the **Customer** card, or the **Vendor** card.</span></span> <span data-ttu-id="3c3fd-116">Hugsanlega þarf að bæta við tilteknum upplýsingum við hvert spjald, svo sem um reikningsfærslu og greiðsluupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="3c3fd-116">You may want to add specific information to each of the cards, such as invoicing and payment details.</span></span>

## <a name="see-also"></a><span data-ttu-id="3c3fd-117">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="3c3fd-117">See Also</span></span>
[<span data-ttu-id="3c3fd-118">Stofna fyrirtækjatengilið</span><span class="sxs-lookup"><span data-stu-id="3c3fd-118">Create Contact Companies</span></span>](marketing-create-contact-companies.md)  
[<span data-ttu-id="3c3fd-119">Stofna einstaklingstengilið</span><span class="sxs-lookup"><span data-stu-id="3c3fd-119">Create Contact Persons</span></span>](marketing-create-contact-persons.md)  
[<span data-ttu-id="3c3fd-120">Uppsetning tengslastjórnunar</span><span class="sxs-lookup"><span data-stu-id="3c3fd-120">Setting Up Relationship Management</span></span>](marketing-setup-marketing.md)  
[<span data-ttu-id="3c3fd-121">Samstilla tengiliði við viðskiptavini, seljendur og bankareikninga</span><span class="sxs-lookup"><span data-stu-id="3c3fd-121">Synchronizing Contacts With Customers, Vendors, and Bank Accounts</span></span>](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[<span data-ttu-id="3c3fd-122">Tengja tengiliði við núverandi viðskiptavini, seljendur eða bankareikninga</span><span class="sxs-lookup"><span data-stu-id="3c3fd-122">Link Contacts to Existing Customers, Vendors, or Bank Accounts</span></span>](marketing-how-link-contact.md)  
[<span data-ttu-id="3c3fd-123">Úthluta viðskiptatengslum á tengilið</span><span class="sxs-lookup"><span data-stu-id="3c3fd-123">Assign Business Relations to a Contact</span></span>](marketing-business-relations.md#AssignBusRelContact)  
[<span data-ttu-id="3c3fd-124">Vinna með Business Central</span><span class="sxs-lookup"><span data-stu-id="3c3fd-124">Working with Business Central</span></span>](ui-work-product.md)

