---
title: Um lokinn framleiðslupantanakostnað
description: Að ljúka framleiðslupöntun er lykillinn að því að ljúka við kostnaðarferli framleiðsluvöru. Lokakostnaður er reiknaður í runuvinnslunni Leiðr. kostnað - Birgðafærslur.
author: SorenGP
ms.topic: conceptual
ms.search.form: 99000867
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: dd9010e055e5e24cafb87846b8eed98f54d83474
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2022
ms.locfileid: "8147831"
---
# <a name="about-finished-production-order-costs"></a>Um lokinn framleiðslupantanakostnað

Það er mikilvægur þáttur í að ljúka kostnaðarferli þeirrar vöru sem verið er að framleiða að fullvinna framleiðslupöntunina. Lokakostnaður þ.m.t. frávik í stöðluðu kostnaðarumhverfi; rauntölur í FIFO-, meðaltals-, eða LIFO-kostnaðarumhverfi er reiknaður út með því að nota keyrsluna **Stilla kostnað - Birgðafærslur** sem gerir fjárhagslega afstemmingu af kostnaðinum af vöruframleiðslu mögulega. Framleiðslupöntun er bara tekin til kostnaðarleiðréttingar ef staða hennar er **Lokið**. Þess vegna er mikilvægt að þegar gerð framleiðslupöntunar er lokið sé stöðu hennar breytt í **Lokið**.  

## <a name="example"></a>Dæmi

Í umhverfi með stöðluðum kostnaði fara kostnaður vöru auk starfsmannakostnaðar og sameiginlegs kostnaðar í VÍV þegar efni er bókað til að framleiða vöru. Þegar vara er framleidd er VÍV minnkað um upphæð staðalkostnaðar vörunnar. Yfirleitt er útkoman úr þessu ekki núll. Ef útkoman á að verða núll, þarf því að nota keyrsluna **Stilla kostnað - Vörufærslur** og athuga að aðeins framleiðslupantanir með stöðuna **Lokið** séu teknar til leiðréttingar.  

## <a name="see-also"></a>Sjá einnig

[Birgðakostnaði stjórnað](finance-manage-inventory-costs.md)  
[Framleiðsla](production-manage-manufacturing.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]