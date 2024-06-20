---
author: brentholtorf
ms.topic: include
ms.date: 03/08/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

> [!NOTE]
> Þegar fyrirtæki er afritað í umhverfi þar sem Dataverse samþætting við sölu er virk, [!INCLUDE [prod_short](prod_short.md)]  hreinsar eftirfarandi stillingar við afritun yfir í markfyrirtækið:
>
> * Dataverse og Stillingar Dynamics tengingar til að tryggja að samþættingin eigi að hefjast rétt í markfyrirtækinu.
> * Samþættingarfærslur til að tryggja að markfyrirtækið bendi ekki á færslur sem eru paraðar í upprunafyrirtækinu.
> * Samþættingarverk til að stöðva samstillingu bakgrunnsverka.
> * Samstillingarvillur eru til, vegna þess að þær benda á villur í upprunafyrirtækinu og myndu aðeins teljast hávaði í markfyrirtækinu.