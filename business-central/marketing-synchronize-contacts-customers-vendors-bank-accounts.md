---
title: Tengiliðir samstilltir við viðskiptamenn og lánardrottnar| Microsoft Docs
description: Hægt er að tengja eða samstilla tengiliðaupplýsingar frá tengiliðum sem líka eru viðskiptamenn, lánardrottnar eða bankareikningar, þannig að þú uppfærir upplýsingarnar aðeins á einum stað.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, CRM, integration, couple
ms.date: 04/01/2019
ms.author: edupont
redirect_url: marketing-create-contact-companies
ms.openlocfilehash: 96ec0862cf93cf9b0bf240ef65bc7ff79b3ccfb5
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2019
ms.locfileid: "934073"
---
# <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a><span data-ttu-id="ed6ed-103">Tengiliðir samstilltir við viðskiptamenn, lánardrottna og bankareikninga</span><span class="sxs-lookup"><span data-stu-id="ed6ed-103">Synchronizing Contacts With Customers, Vendors, and Bank Accounts</span></span>
<span data-ttu-id="ed6ed-104">Ef einhverjir tengiliðir eru einnig viðskiptamenn, lánardrottnar eða bankareikningar er hægt að samstilla tengiliðaupplýsingarnar við viðvomandi viðskiptavin, lánardrottinn, eða bankareikning.</span><span class="sxs-lookup"><span data-stu-id="ed6ed-104">If some of your contacts are also customers, vendors, or bank accounts, you can synchronize the contact information with the related customer, vendor, or bank account.</span></span> <span data-ttu-id="ed6ed-105">Samstilling gerir upplýsingarnar sem eru sameiginleg tengiliði og viðskiptamenn, lánardrottna eða bankareikninga þær sömu.</span><span class="sxs-lookup"><span data-stu-id="ed6ed-105">Synchronization makes information that is common between contacts and customers, vendors, or bank account the same.</span></span>  

## <a name="different-ways-to-synchronize-contacts-with-customers-vendors-and-bank-accounts"></a><span data-ttu-id="ed6ed-106">Mismunandi leiðir fyrir tengiliðir til að vera samstilltir við viðskiptamenn, lánardrottna og bankareikninga</span><span class="sxs-lookup"><span data-stu-id="ed6ed-106">Different Ways to Synchronize Contacts with Customers, Vendors and Bank Accounts</span></span>
<span data-ttu-id="ed6ed-107">Hægt er að samstilla tengiliðina við viðskiptamenn, lánardrottna eða bankareikninga á þrenna vegu:</span><span class="sxs-lookup"><span data-stu-id="ed6ed-107">You can synchronize your contacts with customers, vendors, or bank accounts by three methods:</span></span>

* <span data-ttu-id="ed6ed-108">Tengja tengiliði við viðskiptamenn sem fyrir eru, lánardrottna, eða bankareikninga á tengiliðaspjaldinu.</span><span class="sxs-lookup"><span data-stu-id="ed6ed-108">Link contacts with existing customers, vendors, or bank accounts from the contact card.</span></span> <span data-ttu-id="ed6ed-109">Frekari upplýsingar eru í [Tengja tengiliði við viðskiptamenn, lánardrottna og bankareikninga.](marketing-how-link-contact.md)</span><span class="sxs-lookup"><span data-stu-id="ed6ed-109">For more information, see [Link Contacts With Customers, Vendors, and Bank Accounts](marketing-how-link-contact.md).</span></span>
* <span data-ttu-id="ed6ed-110">Stofna viðskiptamenn , lánardrottna, eða bankareikninga úr tengilið.</span><span class="sxs-lookup"><span data-stu-id="ed6ed-110">Create customers, vendors, or bank accounts from the contact.</span></span> <span data-ttu-id="ed6ed-111">Fyrir frekar upplýsingar, sjá sjá [stofna Viðskiptamann, Lánadrottinn eða Bankareikning út frá tengilið](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="ed6ed-111">For more information, see [Create a Customer, Vendor, or Bank Account From a Contact](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span></span>
* <span data-ttu-id="ed6ed-112">Stofna tengiliði úr viðskiptamönnum, lánadrottnum eða bankareikningum.</span><span class="sxs-lookup"><span data-stu-id="ed6ed-112">Create contacts from customers, vendors or bank accounts.</span></span> <span data-ttu-id="ed6ed-113">Nánari upplýsingar er að finna í [Búa til tengilið frá viðskiptavini, seljanda eða bankareikningi](marketing-how-create-contact-companies.md).</span><span class="sxs-lookup"><span data-stu-id="ed6ed-113">For more information, see [Create a company contact from a customer, vendor, or bank account](marketing-how-create-contact-companies.md).</span></span>

## <a name="consequences-of-synchronization"></a><span data-ttu-id="ed6ed-114">Afleiðingar samstillingar</span><span class="sxs-lookup"><span data-stu-id="ed6ed-114">Consequences of Synchronization</span></span>
<span data-ttu-id="ed6ed-115">Meðan tengiliður er samstillt viðskiptavini, lánardrottni eða bankareikningi:</span><span class="sxs-lookup"><span data-stu-id="ed6ed-115">When the contact is synchronized with the customer, vendor, bank account:</span></span>

* <span data-ttu-id="ed6ed-116">Aðeins þarf að uppfæra upplýsingar á einum stað.</span><span class="sxs-lookup"><span data-stu-id="ed6ed-116">You only have to update information in one place.</span></span> <span data-ttu-id="ed6ed-117">Ef símanúmeri, til dæmis, er breytt fyrir tengilið, er símanúmerið uppfært sjálfkrafa með sömu breytingum á viðskiptavini, lánardrottni eða bankareikningi.</span><span class="sxs-lookup"><span data-stu-id="ed6ed-117">For example, if you modify the phone number on the contact, the phone number is automatically updated with the same modification on the customer, the vendor, or the bank account.</span></span>
* <span data-ttu-id="ed6ed-118">Hafi númeraröð verið tilgreind fyrir tengilið stofnar kerfið sjálfkrafa tengiliðaspjald fyrir viðskiptamenn, lánardrottna eða bankareikninga í hvert sinn sem stofnað er viðskiptamannaspjald, lánardrottna spjald eða bankareikningsspjald.</span><span class="sxs-lookup"><span data-stu-id="ed6ed-118">If you have specified a number series for contacts, when you create a customer card, a vendor card, or a bank account card, a contact card is automatically created for the customer, vendor or bank account.</span></span>
* <span data-ttu-id="ed6ed-119">Hægt er að stofna sölutilboð og –pantanir, ásamt innkaupabeiðnum og –pöntunum úr tengilið.</span><span class="sxs-lookup"><span data-stu-id="ed6ed-119">You can create sales quotes and orders, and purchase quotes and orders from the contact.</span></span>
* <span data-ttu-id="ed6ed-120">Hægt er að láta skrá samskipti þegar aðgerðir eins og að prenta pantanir, standandi pantanir, stofna söluþjónustupantanir, senda tölvupóst og svo framvegis, eru framkvæmdar.</span><span class="sxs-lookup"><span data-stu-id="ed6ed-120">You can have your interactions recorded when you perform actions such as printing orders, blanket orders, creating sales service orders, sending e-mails, and so on.</span></span>
* <span data-ttu-id="ed6ed-121">Ef tengilið er eytt sem tengdur er viðskiptamanni, lánardrottni eða bankareikningi, er tengiliður eingöngu fjarlægðu.</span><span class="sxs-lookup"><span data-stu-id="ed6ed-121">If you delete a contact linked to a customer, vendor or bank account, only the contact is removed.</span></span> <span data-ttu-id="ed6ed-122">viðskiptamann, lánardrottin eða bankareikning verður áfram eftir.</span><span class="sxs-lookup"><span data-stu-id="ed6ed-122">The customer, vendor, or bank account remains.</span></span>
* <span data-ttu-id="ed6ed-123">Ef eytt er viðskiptamanni, lánardrottni eða bankareikningi sem tengist tengilið er eingöngu tengiliður eftir.</span><span class="sxs-lookup"><span data-stu-id="ed6ed-123">If you delete a customer, vendor, bank account linked to a contact, the contact remains.</span></span>

> [!NOTE]  
>   <span data-ttu-id="ed6ed-124">Sumar upplýsingar, s.s. um reikningsfærslur og bókunarupplýsingar, koma ekki fram á tengiliðarspjaldinu.</span><span class="sxs-lookup"><span data-stu-id="ed6ed-124">Some details, such as invoicing and posting details, do not appear on the contact card.</span></span> <span data-ttu-id="ed6ed-125">Því gæti verið ráðlegt að bæta þeim handvirkt í viðskiptamannaspjaldið, lánardrottnaspjaldið eða bankareikningsspjaldið þegar tengiliðir eru stofnaðir sem viðskiptamenn, lánardrottnar eða bankareikningar.</span><span class="sxs-lookup"><span data-stu-id="ed6ed-125">Therefore, you may want to add them manually on the customer card, vendor card, or bank account card when you create contacts as customers, vendors or bank accounts.</span></span>

## <a name="see-also"></a><span data-ttu-id="ed6ed-126">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="ed6ed-126">See Also</span></span>
[<span data-ttu-id="ed6ed-127">Vinna með tengiliði</span><span class="sxs-lookup"><span data-stu-id="ed6ed-127">Managing Contacts</span></span>](marketing-contacts.md)  
<span data-ttu-id="ed6ed-128">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ed6ed-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
