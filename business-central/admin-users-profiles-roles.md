---
title: "Meðhöndla notendur og hlutverk | Microsoft Docs"
description: "Lærið að meðhöndla notendur og Mitt hlutverk í Business Central."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: profiles, users
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 1a94d023424c6eceb93af6e9ca89a90a3a94e996
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="understanding-users-profiles-and-role-centers"></a>Að skilja notendur, forstillingar og Mitt hlutverk

Í [!INCLUDE[d365fin](includes/d365fin_md.md)], eru notendum bætt við af stjórnanda sem gefur einnig notendum aðgang að þeim svæðum [!INCLUDE[d365fin](includes/d365fin_md.md)] sem þeir þurfa í starfi sínu.  

Aðgangur að virkni er stjórnað með *notendahópum* og *notandasíðum*. Sem stjórnandi geturðu bætt við og fjarlægt notendur sem hluta af [!INCLUDE[d365fin](includes/d365fin_md.md)] áskrift þinni og þú getur úthlutað leyfum til notenda í gegnum notendaflokka.  

## <a name="adding-users"></a>Bæta við notendum

Til að bæta við notendum í [!INCLUDE[d365fin](includes/d365fin_md.md)] á netinu, verður stjórnandi Office 365 í fyrirtækinu fyrst að búa til notendur í Office 365 stjórnendamiðstöðinni. Frekari upplýsingar, sjá [Bæta notendum við Office 365 for business](https://aka.ms/CreateOffice365Users).

Síðan getur kerfisstjórinn úthlutað sérhverjum notanda og flokkum notenda leyfi. Frekari upplýsingar eru í [Stjórna notendum og heimildum](ui-how-users-permissions.md).  

### <a name="users-of-on-premises-deployments"></a>Notendur uppsetningar á staðnum

Fyrir uppsetningu á staðnum fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] getur stjórnandi valið á milli mismunandi auðkenningarbúnaðs skilríkja fyrir notendur. Þegar þú býrð til notanda gefur þú síðan mismunandi upplýsingar eftir því hvaða skilríki þú notar í tilteknu [!INCLUDE[server](includes/server.md)] tilviki. Nánari upplýsingar er að finna í [Gerðir auðkenningar og persónuskilríkja](/dynamics365/business-central/dev-itpro/administration/users-credential-types) í stjórnunarhluta þróunaraðila og ITPro efni fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="profiles"></a>Forstillingar

Fólkið í þínu fyrirtæki sem hefur aðgang að [!INCLUDE[d365fin](includes/d365fin_md.md)] er öllum úthlutað *Forstilling* sem veitir þeim aðgang að *Hlutverkamiðstöð*.

Forstillingar eru söfn [!INCLUDE[d365fin](includes/d365fin_md.md)] notenda sem hafa sömu hlutverkamiðstöð (Mitt hlutverk). Hlutverkamiðstöð er aðgangsstaður og heimasíða fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] sem gefur þér skjótan aðgang að mikilvægustu verkum þínum og birtir ýmsar innsýnir og afkastavísa um vinnu þína.  

> [!NOTE]  
>  Í núverandi útgáfu af [!INCLUDE[d365fin](includes/d365fin_md.md)] á netinu, er ekki hægt að bæta við, breyta eða eyða snið.  

## <a name="configuration-and-personalization"></a>Grunnstilling og sérstillingar
<!--The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:  

-   Configuration, performed by the administrator  

-   Personalization, performed by users  

The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.  -->
Notendur sérsníða notendaviðmót sinnar útgáfu með því að sérsníða notendaviðmót undir eigin notandinafni. Stjórnandinn getur eytt þessari aðlögun. Frekari upplýsingar eru í [Sérstilling vinnusvæðisins þíns](ui-personalization-user.md).  

## <a name="see-also"></a>Sjá einnig  
[Vinna með notendur og heimildir](ui-how-users-permissions.md)  
[Stjórnun sérstillinga sem stjórnandi](ui-personalization-manage.md)  
[Sérstillingar verksvæðis](ui-personalization-user.md)  

