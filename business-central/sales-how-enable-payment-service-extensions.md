---
title: Virkja greiðslur viðskiptamanna gegnum greiðsluþjónustu| Microsoft Docs
description: Gerðu það auðveldara fyrir viðskiptavini að greiða reikninga sína með því að virkja greiðsluþjónustu.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 5fa58c177629fdf386bca0ebfce2b668a55cbc8f
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5393350"
---
# <a name="enable-customer-payments-through-payment-services"></a>Virkja greiðslur viðskiptamanna um greiðsluþjónustur
Í stað þess að innheimta með millifærslu eða kreditkorti geta viðskiptamenn þínir greitt þér af reikningnum sínum með greiðsluþjónustu, svo sem Microsoft Pay, PayPal eða WorldPay.  

Eftir að þú hefur virkjað greiðsluþjónustu í [!INCLUDE[prod_short](includes/prod_short.md)] er tengill í þjónustuna í boði á söluskjölum sem þú sendir með tölvupósti til viðskiptavina þinna. Viðskiptamenn geta notað tengilinn til að fara í greiðsluþjónustu og greiða reikninginn beint úr söluskjalinu. Ef þú vilt ekki hafa tengilinn með, til dæmis ef viðskiptamaður greiðir með peningum, getur þú fjarlægt greiðsluþjónustu af reikningnum áður en þú sendir hann.  

Microsoft Pay, PayPal Payments Standard og WorldPay Payments Standard-viðbætur eru settar upp í [!INCLUDE[prod_short](includes/prod_short.md)], og eru tilbúnar fyrir þig til að virkja.  

## <a name="to-enable-a-payment-service-in-prod_short"></a>Til að virkja greiðsluþjónustu í [!INCLUDE[prod_short](includes/prod_short.md)]
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Greiðsluþjónustur** og veldu síðan tengda tengilinn.  
2. Á síðunni **Greiðsluþjónustur** skal velja aðgerðina **Nýtt**.  
3. Veljið greiðsluþjónustu og lokið svo síðunni.  
4. Á síðunni **Greiðsluþjónustur** skal velja aðgerðina **uppsetning**.  
5. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. Lokaðu síðunni.  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a>Til að velja greiðsluþjónustu á sölureikning
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölureikningar** og veldu síðan tengda tengilinn.  
2. Opnaðu sölureikninginn sem þú vilt greiða með því að nota greiðsluþjónustuna.  
3. Í reitnum **Greiðsluþjónusta** er greiðsluþjónustan valin.  

    > [!NOTE]  
    > **Greiðsluþjónustu** reiturinn er aðeins tiltækur greiðsluþjónustan hefur verið virkjuð.  

## <a name="see-also"></a>Sjá einnig  
[Uppsetning sölu](sales-setup-sales.md)  
[Sala](sales-manage-sales.md)  
[Sérstilling [!INCLUDE[prod_short](includes/prod_short.md)] með viðbótum](ui-extensions.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]