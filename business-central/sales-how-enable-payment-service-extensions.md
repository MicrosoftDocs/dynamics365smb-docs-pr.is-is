---
title: Virkja greiðslur viðskiptavina með greiðsluþjónustum
description: Gerðu það auðveldara fyrir viðskiptavini að greiða reikninga sína með því að virkja viðskiptavinagreiðslur í gegnum greiðsluþjónustu.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: online payment
ms.search.forms: '1060, 1061, 1062'
ms.date: 06/25/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="enable-customer-payments-through-payment-services"></a>Virkja greiðslur viðskiptamanna um greiðsluþjónustur

Í stað þess að innheimta með millifærslu eða kreditkorti geta viðskiptavinir þínir greitt þér af reikningnum sínum með greiðsluþjónustu, svo sem PayPal eða WorldPay.  

Eftir að þú hefur virkjað greiðsluþjónustu í [!INCLUDE[prod_short](includes/prod_short.md)] er tengill í þjónustuna í boði á söluskjölum sem þú sendir með tölvupósti til viðskiptavina þinna. Viðskiptamenn geta notað tengilinn til að fara í greiðsluþjónustu og greiða reikninginn beint úr söluskjalinu. Ef þú vilt ekki hafa tengilinn með, til dæmis ef viðskiptamaður greiðir með peningum, getur þú fjarlægt greiðsluþjónustu af reikningnum áður en þú sendir hann.  

PayPal Payments Standard- og WorldPay Payments Standard-viðbætur eru settar upp í [!INCLUDE[prod_short](includes/prod_short.md)] og eru tilbúnar fyrir þig til að virkja.  

> [!CAUTION]
> Viðbótin WorldPay Payments Standard verður afskrifuð. Kótinn er markaður sem úreltur byrjun í 2023 gefa út bylgju 2. Forritið verður virkt fyrir næstu þrjár stærstu útgáfurnar og það verður fjarlægt.   

## <a name="to-enable-a-payment-service-in-"></a>Til að virkja greiðsluþjónustu í [!INCLUDE[prod_short](includes/prod_short.md)]

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Greiðsluþjónustur** og velja síðan viðkomandi tengil.  
2. Á síðunni **Greiðsluþjónustur** skal velja aðgerðina **Nýtt**.  
3. Veljið greiðsluþjónustu og lokið svo síðunni.  
4. Á síðunni **Greiðsluþjónustur** skal velja aðgerðina **uppsetning**.  
5. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. Lokaðu síðunni.  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a>Til að velja greiðsluþjónustu á sölureikning

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sölureikningar** og velja síðan viðkomandi tengil.  
2. Opnaðu sölureikninginn sem þú vilt greiða með því að nota greiðsluþjónustuna.  
3. Í reitnum **Greiðsluþjónusta** er greiðsluþjónustan valin.  

    > [!NOTE]  
    > **Greiðsluþjónustu** reiturinn er aðeins tiltækur greiðsluþjónustan hefur verið virkjuð.  

## <a name="see-also"></a>Sjá einnig .

[Uppsetning sölu](sales-setup-sales.md)  
[Sala](sales-manage-sales.md)  
[Sérstilling [!INCLUDE[prod_short](includes/prod_short.md)] með viðbótum](ui-extensions.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
