---
title: Um lokinn framleiðslupantanakostnað | Microsoft Docs
description: Það er mikilvægur þáttur í að ljúka kostnaðarferli þeirrar vöru sem verið er að framleiða að fullvinna framleiðslupöntunina. Lokakostnaður þ.m.t. frávik í stöðluðu kostnaðarumhverfi; rauntölur í FIFO-, meðaltals-, eða LIFO-kostnaðarumhverfi er reiknaður út með því að nota runuvinnsluna Stilla kostnað - Birgðafærslur.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e1116d99a2893c3fef8fd2306b79cb2252c04d77
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5389425"
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