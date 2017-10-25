---
title: "Velja greiðslumáta rafrænna greiðslna | Microsoft Docs"
description: "Meðhöndla greiðslur til lánardrottna með því að flytja út skrá með greiðsluupplýsingum á færslubókarlínur."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 8b2e20e694279a8c06188e0e429ef3b4fb43aea2
ms.openlocfilehash: 20ae505bc76b8971c678de9e2664653aa5032d6e
ms.contentlocale: is-is
ms.lasthandoff: 09/27/2017

---
# <a name="make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer"></a><span data-ttu-id="871c9-103">Greiða með umreikningsþjónustu bankagagna eða SEPA-kreditfærslu</span><span class="sxs-lookup"><span data-stu-id="871c9-103">Make Payments with Bank Data Conversion Service or SEPA Credit Transfer</span></span>
<span data-ttu-id="871c9-104">Í **Greiðslubók** glugganum er hægt að meðhöndla greiðslur til lánardrottna með því að flytja út skrá með greiðsluupplýsingum á færslubókarlínur.</span><span class="sxs-lookup"><span data-stu-id="871c9-104">In the **Payment Journal** window, you can process payments to your vendors by exporting a file together with the payment information from the journal lines.</span></span> <span data-ttu-id="871c9-105">Þá er hægt að hlaða upp skránni í netbanka til að meðhöndla tengdan peningaflutning.</span><span class="sxs-lookup"><span data-stu-id="871c9-105">You can then upload the file to your electronic bank where the related money transfers are processed.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="871c9-106"> styður SEPA-kreditfærslusniðið, en í heimalandi þínu / svæði geta önnur snið fyrir rafrænar greiðslur kunna að vera tiltækir.</span><span class="sxs-lookup"><span data-stu-id="871c9-106"> supports the SEPA Credit Transfer format, but in your country/region, other formats for electronic payments may be available.</span></span>   

 <span data-ttu-id="871c9-107">Til að gera SEPA kredifærslur, verður þú fyrst að setja upp bankareikning, lánardrottin, og almenna bókarkeyrslurunu sem greiðslubók er byggt á.</span><span class="sxs-lookup"><span data-stu-id="871c9-107">To enable SEPA credit transfers, you must first set up a bank account, a vendor, and the general journal batch that the payment journal is based on.</span></span> <span data-ttu-id="871c9-108">Greiðslur til lánardrottna eru því næst undirbúnar með því að fylla sjálfkrafa út gluggann **Greiðslubók** með gjaldföllnum greiðslum með tilgreindum bókunardagsetningum.</span><span class="sxs-lookup"><span data-stu-id="871c9-108">You then prepare payments to vendors by automatically filling the **Payment Journal** window with due payments with specified posting dates.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="871c9-109">Þegar þú hefur staðfest að greiðslurnar hafi verið framkvæmdar af bankanum getur þú bókað greiðslubókarlínurnar.</span><span class="sxs-lookup"><span data-stu-id="871c9-109">When you have verified that the payments are successfully processed by the bank, you can proceed to post the payment journal lines.</span></span>  

 <span data-ttu-id="871c9-110">Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.</span><span class="sxs-lookup"><span data-stu-id="871c9-110">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="871c9-111">**Til að**</span><span class="sxs-lookup"><span data-stu-id="871c9-111">**To**</span></span>|<span data-ttu-id="871c9-112">**Sjá**</span><span class="sxs-lookup"><span data-stu-id="871c9-112">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="871c9-113">Virkjið eiginleikann UUmreikningsþjónusta fyrir bankagögn til að umbreyta hvers kyns bankayfirlitsskrá í snið sem hægt er að flytja inn eða til að umbreyta útfluttum greiðsluskrám í það snið sem bankinn krefst.</span><span class="sxs-lookup"><span data-stu-id="871c9-113">Activate the Bank Data Conversion Service feature to have any bank statement file converted to a format that you can import or to have your exported payment files converted to the format that your bank requires.</span></span>|[<span data-ttu-id="871c9-114">Hvernig á að: Setja upp umreikningsþjónustu fyrir bankagögn</span><span class="sxs-lookup"><span data-stu-id="871c9-114">How to: Set Up the Bank Data Conversion Service</span></span>](bank-how-setup-bank-statement-service.md)|  
|<span data-ttu-id="871c9-115">Setja upp bankareikning, lánardrottin og greiðslubók fyrir SEPA-millifærslur.</span><span class="sxs-lookup"><span data-stu-id="871c9-115">Set up a bank account, a vendor, and a payment journal for SEPA credit transfer.</span></span>|[<span data-ttu-id="871c9-116">Hvernig á að: Setja upp SEPA-kreditfærslur</span><span class="sxs-lookup"><span data-stu-id="871c9-116">How to: Set Up SEPA Credit Transfer</span></span>](finance-how-to-set-up-sepa-credit-transfer.md)|  
|<span data-ttu-id="871c9-117">Fyllið út greiðslubókina með línum fyrir greiðslu á gjalddaga til lánardrottna með möguleikanum á að setja inn bókunardagsetningar byggt á gjalddaga tengdra innkaupaskjala.</span><span class="sxs-lookup"><span data-stu-id="871c9-117">Fill the payment journal with lines for due payments to vendors, with the option to insert posting dates based on the due date of the related purchase documents.</span></span>|[<span data-ttu-id="871c9-118">Umsjón viðskiptaskulda</span><span class="sxs-lookup"><span data-stu-id="871c9-118">Manage Payables</span></span>](payables-manage-payables.md)|  
|<span data-ttu-id="871c9-119">Flytja út greiðslubókarlínur í skrá í SEPA lánsfjármillifærslusniði.</span><span class="sxs-lookup"><span data-stu-id="871c9-119">Export payment journal lines to a file in the SEPA Credit Transfer format.</span></span>|[<span data-ttu-id="871c9-120">Hvernig á að: Flytja út greiðslur í bankaskrá</span><span class="sxs-lookup"><span data-stu-id="871c9-120">How to: Export Payments to a Bank File</span></span>](payables-how-export-payments-bank-file.md)|  
|<span data-ttu-id="871c9-121">Endurskoða hvaða greiðslur hafa verið flutt út og inn í hvaða skrár.</span><span class="sxs-lookup"><span data-stu-id="871c9-121">Review which payments have been exported and into which files.</span></span>|<span data-ttu-id="871c9-122">Skráningar kreditmillifærslna</span><span class="sxs-lookup"><span data-stu-id="871c9-122">Credit Transfer Registers</span></span>|  
|<span data-ttu-id="871c9-123">Þegar rafræna greiðslan hefur verið unnin að fullu af bankanum skal bóka greiðslurnar.</span><span class="sxs-lookup"><span data-stu-id="871c9-123">When the electronic payment is successfully processed by the bank, post the payments.</span></span>|[<span data-ttu-id="871c9-124">Vinna í færslubókum</span><span class="sxs-lookup"><span data-stu-id="871c9-124">Working with General Journals</span></span>](ui-work-general-journals.md)|  

## <a name="see-also"></a><span data-ttu-id="871c9-125">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="871c9-125">See Also</span></span>  
[<span data-ttu-id="871c9-126">Hvernig á að: Setja upp umreikningsþjónustu fyrir bankagögn</span><span class="sxs-lookup"><span data-stu-id="871c9-126">How to: Set Up the Bank Data Conversion Service</span></span>](bank-how-setup-bank-statement-service.md)  
[<span data-ttu-id="871c9-127">Hvernig á að: Setja upp SEPA-kreditfærslur</span><span class="sxs-lookup"><span data-stu-id="871c9-127">How to: Set Up SEPA Credit Transfer</span></span>](finance-how-to-set-up-sepa-credit-transfer.md)  
<span data-ttu-id="871c9-128">[Gjaldföllnu stjórnað](payables-manage-payables.md) </span><span class="sxs-lookup"><span data-stu-id="871c9-128">[Manage Payables](payables-manage-payables.md) </span></span>  
[<span data-ttu-id="871c9-129">Vinna í færslubókum</span><span class="sxs-lookup"><span data-stu-id="871c9-129">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="871c9-130">Innheimta greiðslur með SEPA-beingreiðslum</span><span class="sxs-lookup"><span data-stu-id="871c9-130">Collecting Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)   

