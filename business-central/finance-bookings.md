---
title: Reikningsfæra bókanir í Business Central
description: Í þessu efnisatriði er útskýrt hvernig eigi að framkvæma magnreikningsfærslu úr Microsoft Bookings í Business Central.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: invoicing, bookings
ms.search.form: 1638, 6702, 6704
ms.date: 05/20/2022
ms.author: edupont
ms.openlocfilehash: 4423b51e7cac952bb2abcf41f9e9364d7bc098c0
ms.sourcegitcommit: 93f30ce3349233cbcd03f300e74b654b49fa5518
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/24/2022
ms.locfileid: "8799717"
---
# <a name="bulk-invoicing-for-microsoft-bookings-in-prod_short"></a>Magnreikningsfærsla fyrir Microsoft Bookings í [!INCLUDE[prod_short](includes/prod_short.md)]

Ef fyrirtækið notar bókaútgáfu App í Microsoft 365 er hægt að gera fjöldareikningsfærslu fyrir fundi. **Ekki er til listi yfir bókaðar** bókanir í [!INCLUDE[prod_short](includes/prod_short.md)] bókuninni sem er lokið á bókunum. Á þessari síðu getur valið snögglega þá fundi sem þú vilt reikningsfæra og búið til reikningsdrög fyrir þjónustu sem veitt var.  

## <a name="connect-to-bookings"></a>Tengjast Bookings

Til að tengja þitt [!INCLUDE[prod_short](includes/prod_short.md)] við Bookings er nauðsynlegt að tiltaka Bookings-fyrirtækið þitt, hvað skal stamstilla við Bookings, hversu oft á að samstilla og hvaða sniðmát skal nota. Settar eru upp upplýsingar á síðunni **Samstilla Bókanir Uppsetning**, sem hægt er að opna frá síðunni **Exchange Samstilla Uppsetning**, sem hægt er finna gegnum [Leit](ui-search.md).  

Ef þú vilt til dæmis samstilla viðskiptavini á milli Bookings og [!INCLUDE[prod_short](includes/prod_short.md)], er nauðsynlegt að tiltaka sjálfgefna sniðmátið sem nota á til að bæta nýjum viðskiptavinum við [!INCLUDE[prod_short](includes/prod_short.md)], út frá viðskiptavinum í Bookings-fyrirtækinu þínu.  

> [!NOTE]
> Bookings-forritið er hannað til að bóka fundi fyrir einstaka viðskiptavini frekar en fyrirtæki. Samstillingin með [!INCLUDE[prod_short](includes/prod_short.md)] mun því aðeins samstilla tengiliði viðskiptavinar við tegund *manns*. Einnig þarf netfang til að samstilla tengiliðinn.  

Með svipuðum hætti, ef þú vilt samstilla þjónustuvörur milli Bookings og [!INCLUDE[prod_short](includes/prod_short.md)], er nauðsynlegt að tiltaka sjálfgefna sniðmátið sem nota á til að bæta nýjum þjónustuvörum við [!INCLUDE[prod_short](includes/prod_short.md)], út frá þjónustunni í Bookings-fyrirtækinu okkar.  

> [!NOTE]
> Aðeins vörur af gerðinni *Þjónusta* munu samstillast milli Bookings og [!INCLUDE[prod_short](includes/prod_short.md)]. Sniðmátið sem þú setur upp á síðunni **Grunnstillingarsniðmát**, svo hægt sé að nota það fyrir samstillingu vöru, verður að skilgreina gerðina sem *Þjónusta*.

## <a name="invoice-appointments"></a>Reikningsfæra fundi

Þegar það er kominn tími á að senda reikninga fyrir fullfrágengnar bókanir ferðu í **bókanir ekki reikningsfærð**. Það hvort listinn er langur eða stuttur fer eftir því hversu oft upplýsingarnar eru samstilltar. Hægt er að stofna reikninga fyrir allar bókanir á listanum eða eina í einu. Hægt er að velja eina eða fleiri færslur á listanum og reikningsfæra þær sérstaklega.  

Notendaþjónustan varðandi reikningsfærða fundi í Bookings er einfaldari en vinnsla með fullu verkflæði sölutilboða, sölupantana og sölureikninga. Frekari upplýsingar eru í [Reikningsfæra sölur](sales-how-invoice-sales.md). Þú getur valið að selja þjónustu þína með því að nota [!INCLUDE[prod_short](includes/prod_short.md)] eða að nota Bookings, allt eftir eðli viðskipta þinna.  

> [!NOTE]
> Í maí 2022 uppgötvuðum við mál í sameiningu við Bókaútgefendur. Sem stendur, Samkeyrsla frá bókunum til að [!INCLUDE [prod_short](includes/prod_short.md)] geta krafist þess að reikningar séu tengdir handvirkt við viðskiptamenn [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="see-also"></a>Sjá einnig

[Fjármál](finance.md)  
[Reikningsfæra sölur](sales-how-invoice-sales.md)  
[Uppsetning sölu](sales-setup-sales.md)  
[Microsoft Bookings](https://products.office.com/business/scheduling-and-booking-app)  


[!INCLUDE[footer-include](includes/footer-banner.md)]