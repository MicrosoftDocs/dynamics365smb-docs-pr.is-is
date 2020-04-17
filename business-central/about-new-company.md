---
title: Stofna ný fyrirtæki með notkun leiðbeininga um uppsetningu með stuðningi | Microsoft Docs
description: Það er auðvelt að stofna nýtt, autt fyrirtæki í Business Central. Leiðbeiningar um uppsetningu með stuðningi hjálpa þér í gegnum skrefin, og þú getur flutt inn fyrirliggjandi viðskiptagögn þín.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: company, setup wizard
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 48f540bd1f8de19ab6ae0284febf6c9c87ababdb
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3188901"
---
# <a name="creating-new-companies-in-d365fin"></a>Stofna ný fyrirtæki í [!INCLUDE[d365fin](includes/d365fin_md.md)]
Í [!INCLUDE[d365fin](includes/d365fin_md.md)] er vísað til hólfanna fyrir viðskiptagögn, sem tilheyra fyrirtækjaeiningu eða lögaðila, sem *fyrirtæki*. Þegar þú skráir þig í [!INCLUDE[d365fin](includes/d365fin_md.md)], færðu sýnifyrirtæki og autt fyrirtæki, *Mitt fyrirtæki*. Auðvelt er að skipta á milli fyrirtækja, þú opnar einfaldlega **Mínar stillingar** og færir þig yfir í hitt fyrirtækið. En þú getur líka stofnað ný fyrirtæki í [!INCLUDE[d365fin](includes/d365fin_md.md)] allt eftir þörfum þíns fyrirtækis. Þegar þú stofnar nýtt fyrirtæki, munu leiðbeiningar um uppsetningu með stuðningi hjálpa þér við grunnuppsetninguna. Þá geturðu flutt inn tilheyrandi gögn úr eldri kerfum eða öðrum fyrirtækjum í [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="creating-a-new-company"></a>Búa til nýtt fyrirtæki
Ef þú ákveður að bæta fyrirtæki við þitt [!INCLUDE[d365fin](includes/d365fin_md.md)], geturðu notað **Stofna nýtt fyrirtæki** leiðbeiningar um uppsetningu með hjálp til að komast af stað. Leiðsagnarforritið fyrir uppsetningu er tiltækt á síðunni **Fyrirtæki** og í uppflettingu í reitnum **Fyrirtæki** á síðunni **Mínar stillingar**.  

Leiðsagnarforritið fyrir uppsetningu býður upp á þrenns konar sniðmát:

-   **Mat - Sýnigögn**  
    Hér er stofnað fyrirtæki sem svipar til sýnifyrirtækisins hvað varðar sýnigögn og uppsetningargögn.  
-   **Framleiðsla - Aðeins uppsetningargögn**  
    Hér er stofnað fyrirtæki sem svipar til **Mitt fyrirtæki** hvað varðar uppsetningargögn, en er án sýnigagna.
-   **Ítarlegt mat - Heildarsýnigögn** Þetta býr til fyrirtæki með uppsetningargögnum og heildarsýnigögnum fyrir allar aðgerðir, þar á meðal framleiðslu og þjónustukerfi.
-   **Stofna nýtt - Engin gögn**  
    Hér er stofnað autt fyrirtæki án uppsetningargagna.  

Ef þú vilt byrja auðveldlega með nýtt fyrirtæki, skal velja **Framleiðsla - Aðeins uppsetningargögn** og síðan flytja inn þín eigin viðskiptagögn, eins og viðskiptamenn, vörur og lánardrottnar. Veldu sniðmátið **Nýtt** ef þú vilt setja allt upp frá grunni. Í því tilfelli, geturðu nýtt þér **Uppsetning fyrirtækis** leiðsagnarforrit með stuðningi til að stíga fyrstu skrefin með nauðsynleg uppsetningargögn.  

> [!NOTE]  
>   Þegar þú stofnar nýtt fyrirtæki, líða nokkrar mínútur áður en þú getur komist inn í það í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Uppsetningarstaðan á síðunni **Fyrirtæki** sýnir hvenær nýja fyrirtækið er tilbúið fyrir þig. Þá geturðu skipt yfir í nýja fyrirtækið með því að nota **Mínar stillingar**.  

Á 30 daga reynslutímabilinu geturðu stofnað eins mörg fyrirtæki og þú vilt, en þau verða aðeins aðgengileg á meðan reynslutímabilinu stendur. Nánari upplýsingar má nálgast með því að hafa samband við [!INCLUDE[d365fin](includes/d365fin_md.md)] samstarfsaðila þinn.  

## <a name="copying-a-company"></a>Afritun fyrirtækis
Á síðunni **Fyrirtæki** er hægt að nota aðgerðina **Afrita** til að stofna annað fyrirtæki út frá efni fyrirliggjandi fyrirtækis. Þetta er til dæmis gagnlegt þegar þú vilt prófa fyrirtæki án þess að það hafi áhrif á framleiðslugögn.

> [!Important]
> Ekki er hægt að nota þessa aðgerð til að taka öryggisafrit af fyrirtæki. Öryggisafrit er tekið af fyrirtækinu með því að flytja út úr gagnagrunn sem .bacpac-skrá. Frekari upplýsingar er að finna í [Útflutningur gagnagrunna](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-database-export) í hjálp Developer og ITPro.

## <a name="company-setup"></a>Uppsetning fyrirtækis
Þegar þú skráir þig inn í nýtt fyrirtæki, mun **Uppsetning fyrirtækis** leiðsagnarforritið opnast sjálfvirkt og aðstoða þig við að komast af stað. Spurt verður um upplýsingar um fyrirtækið, eins og t.d. aðsetur, bankaupplýsingar, og aðferð kostnaðarútreiknings birgða. Við spyrjum um þessar upplýsingar þar sem þær eru notaðar sem grunnur á mörgum sviðum í [!INCLUDE[d365fin](includes/d365fin_md.md)], sem þú þarft þá ekki að setja handvirkt upp síðar.  

Aðsetur fyrirtækisins er til dæmis innifalið í reikningum og öðrum skjölum, bankaupplýsingar eru notaðar í greiðslum, og aðferð kostnaðarútreiknings er notuð til að reikna út bæði verð og birgðaverðmat.  

Þegar grunnatriðin eru komin á sinn stað, geturðu sett upp þau grunnsvæði sem eftir eru. Þá er hægt að bæta inn viðskiptagögnum á borð við viðskiptamenn og lánardrottna. Nánari upplýsingar er að finna í [Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md).  

## <a name="see-also"></a>Sjá einnig
[Sérstilla Business Central](ui-customizing-overview.md)  
[Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Grunnstillingum breytt](ui-change-basic-settings.md)  
[Hafist handa](product-get-started.md)  
