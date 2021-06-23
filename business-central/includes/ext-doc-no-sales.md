---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 05/27/2021
ms.author: edupont
ms.openlocfilehash: 50b4b331f00bdcdf030bac2332ffb5dafdfd2de6
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115969"
---
<span data-ttu-id="60f2c-101">Á söluskjölum og færslubókum er hægt að tilgreina fylgiskjalsnúmer sem vísar til númerakerfis lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="60f2c-101">On sales documents and journals, you can specify a document number that refers to the customer's numbering system.</span></span> <!--You can enter a maximum of ten characters, both numbers and letters.--> <span data-ttu-id="60f2c-102">Notaðu þennan reit til að skrá númerið sem viðskiptavinurinn úthlutaði pöntuninni, reikningnum eða kreditreikningnum.</span><span class="sxs-lookup"><span data-stu-id="60f2c-102">Use this field to record the number that the customer assigned to the order, invoice, or credit memo.</span></span> <span data-ttu-id="60f2c-103">Síðar má nota númerið ef af einhverjum ástæðum þarf að leita að bókaðri færslu með þessu númeri.</span><span class="sxs-lookup"><span data-stu-id="60f2c-103">You can then use the number later if, for some reason, you need to search for the posted entry using this number.</span></span>  

<span data-ttu-id="60f2c-104">Reiturinn **Nr. utanaðk. skjals** áskilið á **Uppsetning sölugrunns** tilgreinir hvort það er skylt að færa númer ytra skjals í reitinn **Númer ytra fylgiskjals** á söluhaus eða í reitinn **Númer ytra fylgiskjals** á færslubókarlínu.</span><span class="sxs-lookup"><span data-stu-id="60f2c-104">The **Ext. Doc. No. Mandatory** field on the **Sales & Receivables Setup** page specifies whether it is mandatory to enter an external document number in the **External Document No.** field on a sales header and the **External Document No.** field on a general journal line.</span></span>

<span data-ttu-id="60f2c-105">Ef þessi reitur er valinn er ekki hægt að bóka reikning eða færslubókarlínu án númers utanaðkomandi skjals.</span><span class="sxs-lookup"><span data-stu-id="60f2c-105">If you select this field, it will not be possible to post an invoice or a general journal line without an external document number.</span></span>

<span data-ttu-id="60f2c-106">Númer ytra skjals fylgir með í bókuðum skjölum þar sem hægt er að leita eftir viðkomandi númeri.</span><span class="sxs-lookup"><span data-stu-id="60f2c-106">The external document number is included in posted documents where you can search by the relevant number.</span></span> <span data-ttu-id="60f2c-107">Einnig er hægt að leita eftir númeri ytra skjals þegar leitað er í viðskiptavinafærslum.</span><span class="sxs-lookup"><span data-stu-id="60f2c-107">You can also search using the external document number when navigating on customer ledger entries.</span></span>

<span data-ttu-id="60f2c-108">Önnur leið til að meðhöndla utanaðkomandi skjalanúmer er að nota reitinn **Tilvísunarnúmer notanda**.</span><span class="sxs-lookup"><span data-stu-id="60f2c-108">A different way to handle external document numbers is to use the **Your Reference** field.</span></span> <span data-ttu-id="60f2c-109">Ef reiturinn **Tilvísun þín** er notaður verður númerið tekið með í bókuðum skjölum og þú getur leitað eftir því á sama hátt og eftir gildum úr reitum **Nr. ytra skjals**.</span><span class="sxs-lookup"><span data-stu-id="60f2c-109">If you use the **Your Reference** field, the number will be included in posted documents, and you can search by it in the same way as for values from **External Document No.** fields.</span></span> <span data-ttu-id="60f2c-110">En reiturinn er ekki tiltækur í færslubókarlínum.</span><span class="sxs-lookup"><span data-stu-id="60f2c-110">But the field is not available on journal lines.</span></span>
