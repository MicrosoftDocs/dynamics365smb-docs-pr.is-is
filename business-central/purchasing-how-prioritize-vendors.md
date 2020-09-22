---
title: Úthluta forgangsstigi til lánardrottins | Microsoft Docs
description: Þú getur úthlutað númerum til lánardrottins eða birgja til að forgangsraða þeim og auðvelda greiðslutillögur í Business Central.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier, payment priority
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 6dfa7237cde2a88c8d36baa2daa69f4cde97a4eb
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2020
ms.locfileid: "3783100"
---
# <a name="prioritize-vendors"></a>Forgangsraða lánardrottnum
[!INCLUDE[d365fin](includes/d365fin_md.md)] getur lagt til ýmsar greiðslur til lánardrottna t.d. greiðslur sem eru bráðum á gjalddaga eða greiðslur sem hægt er að fá afslátt af. Frekari upplýsingar er að finna í [Greiðslutillögur til lánardrottna](payables-how-suggest-vendor-payments.md).

Fyrst verður að forgangsraða lánardrottnum með því að úthluta númerum á þá.
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE3PRGa?rel=0]

## <a name="to-prioritize-vendors"></a>Lánardrottnum forgangsraðað
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Lánardrottnar** og veldu síðan tengda tengilinn.
2. Veljið viðeigandi lánardrottin og veljið því næst **Breyta**.
3. Í reitinn **Forgangur** skal færa inn númer.

[!INCLUDE[d365fin](includes/d365fin_md.md)] setur lægsta númerið, fyrir utan 0, efst í forgangsröðina. Þannig að t.d. ef notaðar eru tölurnar 1, 2 og 3 þá er 1 fyrst í forgangsröðinni.

Ef ekki á að forgangsraða lánardrottni er reiturinn **Forgangur** skilinn eftir auður. Síðan ef notuð er aðgerðin greiðslutillaga er lánardrottininn settur á lista á eftir öllum lánardrottnunum sem hafa forgangsnúmer. Hægt er að færa inn eins mörg forgangsstig og nauðsynlegt er.

## <a name="see-also"></a>Sjá einnig
[Uppsetning innkaupa](purchasing-setup-purchasing.md)  
[Stjórna skuldum](payables-manage-payables.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
