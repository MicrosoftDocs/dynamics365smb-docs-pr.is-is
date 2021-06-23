---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 05/27/2021
ms.author: edupont
ms.openlocfilehash: 59376b96dcd6f755040b07784ceca53e157bcf14
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115966"
---
<span data-ttu-id="e58c9-101">Á innkaupaskjölum og færslubókum er hægt að tilgreina fylgiskjalsnúmer sem vísar til númerakerfis lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="e58c9-101">On purchase documents and journals, you can specify a document number that refers to the vendor's numbering system.</span></span> <span data-ttu-id="e58c9-102">Notaðu þennan reit til að skrá númerið sem lánardrottinn úthlutaði pöntuninni, reikningnum eða kreditreikningnum.</span><span class="sxs-lookup"><span data-stu-id="e58c9-102">Use this field to record the number that the vendor assigned to the order, invoice, or credit memo.</span></span> <span data-ttu-id="e58c9-103">Síðar má nota númerið ef af einhverjum ástæðum þarf að leita að bókaðri færslu með þessu númeri.</span><span class="sxs-lookup"><span data-stu-id="e58c9-103">You can then use the number later if, for some reason, you need to search for the posted entry using this number.</span></span>

<span data-ttu-id="e58c9-104">Reiturinn **Nr. utanaðk. skjals áskilið** í **Uppsetning innkaupagrunns** síðunni tilgreinir hvort áskilið er að færa inn númer utanaðkomandi skjals við eftirfarandi aðstæður:</span><span class="sxs-lookup"><span data-stu-id="e58c9-104">The **Ext. Doc. No. Mandatory** field in the **Purchases & Payables Setup** page specifies whether it is mandatory to enter an external document number in the following situations:</span></span>

* <span data-ttu-id="e58c9-105">Í **Pöntunarnr. lánardr.** reitinn, **Pöntunarnr. lánardr.**</span><span class="sxs-lookup"><span data-stu-id="e58c9-105">In the **Vendor Invoice No.** field, **Vendor Order No.**</span></span> <span data-ttu-id="e58c9-106">reitinn, eða **Kr.reikn.nr. lánardr.**</span><span class="sxs-lookup"><span data-stu-id="e58c9-106">field, or the **Vendor Cr. Memo No.**</span></span> <span data-ttu-id="e58c9-107">reitnum á innkaupahaus</span><span class="sxs-lookup"><span data-stu-id="e58c9-107">field on a purchase header</span></span>

* <span data-ttu-id="e58c9-108">Í reitnum **External Númer ytra fylgiskjals** á færslubókarlínu, þar sem reiturinn **Tegund fylgiskjals** er stilltur á *Reikningur*, *Kreditreikningur* eða *Vaxtareikningur* og reiturinn **Tegund reiknings** er stillt á *Lánardrottinn*.</span><span class="sxs-lookup"><span data-stu-id="e58c9-108">In the **External Document No.** field on a general journal line, where the **Document Type** field is set to *Invoice*, *Credit Memo*, or *Finance Charge Memo*, and the **Account Type** field is set to *Vendor*.</span></span>

<span data-ttu-id="e58c9-109">Ef þú velur þennan reit verður ekki hægt að bóka reikning, kreditreikning eða færslubókarlínur eins og þá sem lýst er hér fyrir ofan án númers utanaðkomandi skjals.</span><span class="sxs-lookup"><span data-stu-id="e58c9-109">If you select this field, it will not be possible to post an invoice, a credit memo, or the type of general journal line described above without an external document number.</span></span>

<span data-ttu-id="e58c9-110">Númer ytra skjals fylgir með í bókuðum skjölum þar sem hægt er að leita eftir viðkomandi númeri.</span><span class="sxs-lookup"><span data-stu-id="e58c9-110">The external document number is included in posted documents where you can search by the relevant number.</span></span> <span data-ttu-id="e58c9-111">Einnig er hægt að leita eftir númeri ytra skjals þegar leitað er í lánardrottnafærslum.</span><span class="sxs-lookup"><span data-stu-id="e58c9-111">You can also search using the external document number when navigating on vendor ledger entries.</span></span>

<span data-ttu-id="e58c9-112">Önnur leið til að meðhöndla utanaðkomandi skjalanúmer er að nota reitinn **Tilvísunarnúmer notanda**.</span><span class="sxs-lookup"><span data-stu-id="e58c9-112">A different way to handle external document numbers is to use the **Your Reference** field.</span></span> <span data-ttu-id="e58c9-113">Ef reiturinn **Tilvísun þín** er notaður verður númerið tekið með í bókuðum skjölum og þú getur leitað eftir því á sama hátt og eftir gildum úr reitum **Nr. ytra skjals**.</span><span class="sxs-lookup"><span data-stu-id="e58c9-113">If you use the **Your Reference** field, the number will be included in posted documents, and you can search by it in the same way as for values from **External Document No.** fields.</span></span> <span data-ttu-id="e58c9-114">En reiturinn er ekki tiltækur í færslubókarlínum.</span><span class="sxs-lookup"><span data-stu-id="e58c9-114">But the field is not available on journal lines.</span></span>
