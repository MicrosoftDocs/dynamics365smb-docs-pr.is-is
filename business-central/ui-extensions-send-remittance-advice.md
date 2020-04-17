---
title: Senda greiðslutilkynningu viðbót | Microsoft Docs
description: Lýsir viðbótinni fyrir að senda greiðslutilkynningu sem gerir kleift að senda tölvupósta og endursenda greiðslutilkynningar frá færslum greiðslubókar og lánardrottnabókar.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, remittance, advice
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 439f9997e9ee70ff290a42e5044a9dbaff1112de
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3190348"
---
# <a name="send-remittance-advice"></a><span data-ttu-id="89db5-103">Senda greiðslutilkynningu</span><span class="sxs-lookup"><span data-stu-id="89db5-103">Send Remittance Advice</span></span>
<span data-ttu-id="89db5-104">Þar sem greiðslutilkynning er notuð til að tilkynna lánardrottnum um greiðslur sem eru gerðar, er nú hægt senda margar greiðslutilkynningar í tölvupósti úr greiðslubók sem og að endursenda eftir að greiðslur eru gerðar úr færslum lánardrottnabókar með sendisniði skjala.</span><span class="sxs-lookup"><span data-stu-id="89db5-104">Where remittance advice is used to notify vendors of payments being made, you can now email remittance advice in bulk from the payment journal as well as resend after payments are made from vendor ledger entries by using document sending profiles.</span></span>

> [!NOTE]
> <span data-ttu-id="89db5-105">Þessi virkni er aðeins studd í Business Central á netinu og á staðnum í eftirfarandi löndum: Bretlandi, Bandaríkjunum, Kanada, Ástralíu, Nýja-Sjálandi og Suður-Afríku.</span><span class="sxs-lookup"><span data-stu-id="89db5-105">This functionality is only supported in Business Central online and on-premises in following countries: United Kingdom, United States, Canada, Australia, New Zealand, and South Africa.</span></span>  

<span data-ttu-id="89db5-106">Hægt er að senda greiðslutilkynningu á tvo vegu:</span><span class="sxs-lookup"><span data-stu-id="89db5-106">You can send remittance advice in two different ways:</span></span>

* <span data-ttu-id="89db5-107">Á síðunni **Greiðslubók** skal velja **Fletta**, **Greiðslur**, **Senda greiðslutilkynningu** á tölvupóst greiðslutilkynningar fyrir eina eða margar greiðslubókarlínur</span><span class="sxs-lookup"><span data-stu-id="89db5-107">In the **Payment Journal** page, choose **Navigate**, **Payments**, **Send Remittance Advice** to email remittance advice for one or multiple payment journal lines</span></span>
* <span data-ttu-id="89db5-108">Á síðunni **Lánardrottnafærslur** skal velja Aðgerð, Virkni, Senda greiðslutilkynningu á tölvupóst greiðslutilkynningar eftir bókun á greiðslum lánardrottins fyrir eina eða margar færslur lánardrottnabókar</span><span class="sxs-lookup"><span data-stu-id="89db5-108">I the **Vendor Ledger Entries** page, choose Action, Functions, Send Remittance Advice to email remittance advice after posting of vendor payments, for one of multiple vendor ledger entries</span></span>

## <a name="see-also"></a><span data-ttu-id="89db5-109">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="89db5-109">See Also</span></span>
[<span data-ttu-id="89db5-110">Greiðslutillögur til lánardr.</span><span class="sxs-lookup"><span data-stu-id="89db5-110">Suggest Vendor Payments</span></span>](payables-how-suggest-vendor-payments.md)  
<span data-ttu-id="89db5-111">[Sérstilling [!INCLUDE[d365fin](includes/d365fin_md.md)] með viðbótum ](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="89db5-111">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="89db5-112">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="89db5-112">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
