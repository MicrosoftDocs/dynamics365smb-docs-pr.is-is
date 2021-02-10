---
title: Senda greiðslutilkynningu viðbót | Microsoft Docs
description: Lýsir viðbótinni fyrir að senda greiðslutilkynningu sem gerir kleift að senda tölvupósta og endursenda greiðslutilkynningar frá færslum greiðslubókar og lánardrottnabókar.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, remittance, advice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3ae8d131b714b0d7ffb60727d1a991cd6e4ab692
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757068"
---
# <a name="send-remittance-advice"></a><span data-ttu-id="6f5a3-103">Senda greiðslutilkynningu</span><span class="sxs-lookup"><span data-stu-id="6f5a3-103">Send Remittance Advice</span></span>

<span data-ttu-id="6f5a3-104">Þar sem greiðslutilkynning er notuð til að tilkynna lánardrottnum um greiðslur sem eru gerðar, er nú hægt senda margar greiðslutilkynningar í tölvupósti úr greiðslubók sem og að endursenda eftir að greiðslur eru gerðar úr færslum lánardrottnabókar með sendisniði skjala.</span><span class="sxs-lookup"><span data-stu-id="6f5a3-104">Where remittance advice is used to notify vendors of payments being made, you can now email remittance advice in bulk from the payment journal as well as resend after payments are made from vendor ledger entries by using document sending profiles.</span></span>

> [!NOTE]
> <span data-ttu-id="6f5a3-105">Þessi virkni er aðeins studd í Business Central á netinu og á staðnum í eftirfarandi löndum: Bretlandi, Bandaríkjunum, Kanada, Ástralíu, Nýja-Sjálandi og Suður-Afríku.</span><span class="sxs-lookup"><span data-stu-id="6f5a3-105">This functionality is only supported in Business Central online and on-premises in following countries: United Kingdom, United States, Canada, Australia, New Zealand, and South Africa.</span></span>  

<span data-ttu-id="6f5a3-106">Hægt er að senda greiðslutilkynningu á tvo vegu:</span><span class="sxs-lookup"><span data-stu-id="6f5a3-106">You can send remittance advice in two different ways:</span></span>

* <span data-ttu-id="6f5a3-107">Á síðunni **Greiðslubók** skal velja **Tengd**, **Greiðslur**, **Senda greiðslutilkynningu** til að senda greiðslutilkynningi í tölvupósti fyrir eina eða margar greiðslubókarlínur.</span><span class="sxs-lookup"><span data-stu-id="6f5a3-107">In the **Payment Journal** page, choose **Related**, **Payments**, **Send Remittance Advice** to email remittance advice for one or multiple payment journal lines</span></span>
* <span data-ttu-id="6f5a3-108">Á síðunni **Lánardrottnafærslur** skal velja **Aðgerðir**, **Virkni**, **Senda greiðslutilkynningu** á tölvupóst greiðslutilkynningar eftir bókun á greiðslum lánardrottins fyrir eina eða margar færslur lánardrottnabókar</span><span class="sxs-lookup"><span data-stu-id="6f5a3-108">In the **Vendor Ledger Entries** page, choose **Actions**, **Functions**, **Send Remittance Advice** to email remittance advice after posting of vendor payments, for one or multiple vendor ledger entries</span></span>

## <a name="see-also"></a><span data-ttu-id="6f5a3-109">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="6f5a3-109">See Also</span></span>

[<span data-ttu-id="6f5a3-110">Greiðslutillögur til lánardr.</span><span class="sxs-lookup"><span data-stu-id="6f5a3-110">Suggest Vendor Payments</span></span>](payables-how-suggest-vendor-payments.md)  
<span data-ttu-id="6f5a3-111">[Sérstilling [!INCLUDE[prod_short](includes/prod_short.md)] með viðbótum ](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="6f5a3-111">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)</span></span>  
<span data-ttu-id="6f5a3-112">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6f5a3-112">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="6f5a3-113">Senda skjöl í tölvupósti</span><span class="sxs-lookup"><span data-stu-id="6f5a3-113">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
