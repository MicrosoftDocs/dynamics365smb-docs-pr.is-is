---
title: Reikningsfæra bókanir í Business Central
description: Í þessu efnisatriði er útskýrt hvernig eigi að framkvæma magnreikningsfærslu úr Microsoft Bookings í Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: invoicing, bookings
ms.search.form: 1638, 6702, 6704
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 9cac5b50d2a674f3ca39f085a2d4448356277b64
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/14/2022
ms.locfileid: "7971173"
---
# <a name="bulk-invoicing-for-microsoft-bookings-in-prod_short"></a>Magnreikningsfærsla fyrir Microsoft Bookings í [!INCLUDE[prod_short](includes/prod_short.md)]

Ef fyrirtækið notar bókaútgáfu App í Microsoft 365 er hægt að gera fjöldareikningsfærslu fyrir fundi. Síðan **Óreikningsfærðar bókanir** í [!INCLUDE[prod_short](includes/prod_short.md)] býður upp á lista yfir fullunnar bókanir fyrirtækisins. Á þessari síðu getur valið snögglega þá fundi sem þú vilt reikningsfæra og búið til reikningsdrög fyrir þjónustu sem veitt var.  

## <a name="connect-to-bookings"></a>Tengjast Bookings

Til að tengja þitt [!INCLUDE[prod_short](includes/prod_short.md)] við Bookings er nauðsynlegt að tiltaka Bookings-fyrirtækið þitt, hvað skal stamstilla við Bookings, hversu oft á að samstilla og hvaða sniðmát skal nota. Settar eru upp upplýsingar á síðunni **Samstilla Bókanir Uppsetning**, sem hægt er að opna frá síðunni **Exchange Samstilla Uppsetning**, sem hægt er finna gegnum [Leit](ui-search.md).  

Ef þú vilt til dæmis samstilla viðskiptavini á milli Bookings og [!INCLUDE[prod_short](includes/prod_short.md)], er nauðsynlegt að tiltaka sjálfgefna sniðmátið sem nota á til að bæta nýjum viðskiptavinum við [!INCLUDE[prod_short](includes/prod_short.md)], út frá viðskiptavinum í Bookings-fyrirtækinu þínu.  

> [!NOTE]
> Bookings-forritið er hannað til að bóka fundi fyrir einstaka viðskiptavini frekar en fyrirtæki. Samstillingin við [!INCLUDE[prod_short](includes/prod_short.md)] mun fyrir vikið aðeins samstilla tengiliði viðskiptavina við gerð af „einstaklingi“. Einnig þarf netfang til að samstilla tengiliðinn.  

Með svipuðum hætti, ef þú vilt samstilla þjónustuvörur milli Bookings og [!INCLUDE[prod_short](includes/prod_short.md)], er nauðsynlegt að tiltaka sjálfgefna sniðmátið sem nota á til að bæta nýjum þjónustuvörum við [!INCLUDE[prod_short](includes/prod_short.md)], út frá þjónustunni í Bookings-fyrirtækinu okkar.  

> [!NOTE]
> Aðeins vörur af gerðinni *Þjónusta* munu samstillast milli Bookings og [!INCLUDE[prod_short](includes/prod_short.md)]. Sniðmátið sem þú setur upp á síðunni **Grunnstillingarsniðmát**, svo hægt sé að nota það fyrir samstillingu vöru, verður að skilgreina gerðina sem *Þjónusta*.

## <a name="invoice-appointments"></a>Reikningsfæra fundi

Þegar tímabært er að senda reikninga fyrir fullunnar bókanir, ferðu inn á síðuna **Óreikningsfærðar bókanir**. Það hvort listinn er langur eða stuttur fer eftir því hversu oft upplýsingarnar eru samstilltar. Hægt er að stofna reikninga fyrir allar bókanir á listanum eða eina í einu. Hægt er að velja eina eða fleiri færslur á listanum og reikningsfæra þær sérstaklega.  

Notendaþjónustan varðandi reikningsfærða fundi í Bookings er einfaldari en vinnsla með fullu verkflæði sölutilboða, sölupantana og sölureikninga. Frekari upplýsingar eru í [Reikningsfæra sölur](sales-how-invoice-sales.md). Þú getur valið að selja þjónustu þína með því að nota [!INCLUDE[prod_short](includes/prod_short.md)] eða að nota Bookings, allt eftir eðli viðskipta þinna.  

## <a name="see-also"></a>Sjá einnig

[Fjármál](finance.md)  
[Reikningsfæra sölur](sales-how-invoice-sales.md)  
[Uppsetning sölu](sales-setup-sales.md)  
[Microsoft Bookings](https://products.office.com/business/scheduling-and-booking-app)  


[!INCLUDE[footer-include](includes/footer-banner.md)]