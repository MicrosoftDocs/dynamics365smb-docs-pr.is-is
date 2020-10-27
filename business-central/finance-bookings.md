---
title: Reikningsfærið bókanir í Business Central | Microsoft Docs
description: Fræðist um hvernig á að magnreikningsfæra frá Microsoft Bookings í Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: invoicing, bookings
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 6b69d64e67428cc4f1e7dc75e6267b2749e182c1
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3913447"
---
# <a name="bulk-invoicing-for-microsoft-bookings-in-d365fin"></a>Magnreikningsfærsla fyrir Microsoft Bookings í [!INCLUDE[d365fin](includes/d365fin_md.md)]
Ef fyrirtækið þitt notar Bókanir forrit í Microsoft 365 geturðu framkvæmt magnreikningsfærslu fyrir fundi. Síðan **Óreikningsfærðar bókanir** í [!INCLUDE[d365fin](includes/d365fin_md.md)] býður upp á lista yfir fullunnar bókanir fyrirtækisins. Á þessari síðu getur valið snögglega þá fundi sem þú vilt reikningsfæra og búið til reikningsdrög fyrir þjónustu sem veitt var.  

## <a name="connect-to-bookings"></a>Tengjast Bookings
Til að tengja þitt [!INCLUDE[d365fin](includes/d365fin_md.md)] við Bookings er nauðsynlegt að tiltaka Bookings-fyrirtækið þitt, hvað skal stamstilla við Bookings, hversu oft á að samstilla og hvaða sniðmát skal nota. Settar eru upp upplýsingar á síðunni **Samstilla Bókanir Uppsetning** , sem hægt er að opna frá síðunni **Exchange Samstilla Uppsetning** , sem hægt er finna gegnum [Leit](ui-search.md).  

Ef þú vilt til dæmis samstilla viðskiptavini á milli Bookings og [!INCLUDE[d365fin](includes/d365fin_md.md)], er nauðsynlegt að tiltaka sjálfgefna sniðmátið sem nota á til að bæta nýjum viðskiptavinum við [!INCLUDE[d365fin](includes/d365fin_md.md)], út frá viðskiptavinum í Bookings-fyrirtækinu þínu.  

> [!NOTE]
> Bookings-forritið er hannað til að bóka fundi fyrir einstaka viðskiptavini frekar en fyrirtæki. Samstillingin við [!INCLUDE[d365fin](includes/d365fin_md.md)] mun fyrir vikið aðeins samstilla tengiliði viðskiptavina við gerð af „einstaklingi“. Einnig þarf netfang til að samstilla tengiliðinn.  

Með svipuðum hætti, ef þú vilt samstilla þjónustuvörur milli Bookings og [!INCLUDE[d365fin](includes/d365fin_md.md)], er nauðsynlegt að tiltaka sjálfgefna sniðmátið sem nota á til að bæta nýjum þjónustuvörum við [!INCLUDE[d365fin](includes/d365fin_md.md)], út frá þjónustunni í Bookings-fyrirtækinu okkar.  

> [!NOTE]
> Aðeins vörur af gerðinni *Þjónusta* munu samstillast milli Bookings og [!INCLUDE[d365fin](includes/d365fin_md.md)]. Sniðmátið sem þú setur upp á síðunni **Grunnstillingarsniðmát** , svo hægt sé að nota það fyrir samstillingu vöru, verður að skilgreina gerðina sem *Þjónusta* .

## <a name="invoice-appointments"></a>Reikningsfæra fundi
Þegar tímabært er að senda reikninga fyrir fullunnar bókanir, ferðu inn á síðuna **Óreikningsfærðar bókanir** . Það hvort listinn er langur eða stuttur fer eftir því hversu oft upplýsingarnar eru samstilltar. Hægt er að stofna reikninga fyrir allar bókanir á listanum eða eina í einu. Hægt er að velja eina eða fleiri færslur á listanum og reikningsfæra þær sérstaklega.  

Notendaþjónustan varðandi reikningsfærða fundi í Bookings er einfaldari en vinnsla með fullu verkflæði sölutilboða, sölupantana og sölureikninga. Frekari upplýsingar eru í [Reikningsfæra sölur](sales-how-invoice-sales.md). Þú getur valið að selja þjónustu þína með því að nota [!INCLUDE[d365fin](includes/d365fin_md.md)] eða að nota Bookings, allt eftir eðli viðskipta þinna.  

## <a name="see-also"></a>Sjá einnig
[Fjármál](finance.md)  
[Reikningsfæra sölur](sales-how-invoice-sales.md)  
[Uppsetning sölu](sales-setup-sales.md)  
[Microsoft Bookings](https://products.office.com/business/scheduling-and-booking-app)  
