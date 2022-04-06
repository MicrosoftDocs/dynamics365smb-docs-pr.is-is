---
title: Stofna ný fyrirtæki með hjálp uppsetningarleiðbeininga
description: Það er auðvelt að stofna nýtt, autt fyrirtæki í Business Central. Leiðbeiningar um uppsetningu með stuðningi hjálpa þér í gegnum skrefin, og þú getur flutt inn fyrirliggjandi viðskiptagögn þín.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: company, setup wizard
ms.search.form: 1803, 9020, 9022, 9026, 9027, 9030, 9000, 9004, 9005, 9018, 9006, 9007, 9010, 9016, 9017
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: bef90a9dab30391f310458cb0dde58cc4fac5268
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8519356"
---
# <a name="create-new-companies-in-prod_short"></a>Stofna ný fyrirtæki í[!INCLUDE[prod_short](includes/prod_short.md)]

Í [!INCLUDE[prod_short](includes/prod_short.md)] er vísað til hólfanna fyrir viðskiptagögn, sem tilheyra fyrirtækjaeiningu eða lögaðila, sem *fyrirtæki*. Þegar þú skráir þig í [!INCLUDE[prod_short](includes/prod_short.md)], færðu sýnifyrirtæki og autt fyrirtæki, *Mitt fyrirtæki*. Auðvelt er að skipta á milli fyrirtækja, þú opnar einfaldlega **Mínar stillingar** og færir þig yfir í hitt fyrirtækið. En þú getur líka stofnað ný fyrirtæki í [!INCLUDE[prod_short](includes/prod_short.md)] allt eftir þörfum þíns fyrirtækis.  

Þegar þú stofnar nýtt fyrirtæki, munu leiðbeiningar um uppsetningu með stuðningi hjálpa þér við grunnuppsetninguna. Þá geturðu flutt inn tilheyrandi gögn úr eldri kerfum eða öðrum fyrirtækjum í [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="choose-the-right-template"></a>Velja rétt sniðmát

Ef þú ákveður að bæta fyrirtæki við þitt [!INCLUDE[prod_short](includes/prod_short.md)], geturðu notað **Stofna nýtt fyrirtæki** leiðbeiningar um uppsetningu með hjálp til að komast af stað. Leiðsagnarforritið fyrir uppsetningu er tiltækt á síðunni **Fyrirtæki** og í uppflettingu í reitnum **Fyrirtæki** á síðunni **Mínar stillingar**.  

Leiðsagnarforrit uppsetningar býður upp á tvö sniðmát og auða valkosti:

- **Mat - Sýnigögn**  
    Hér er stofnað fyrirtæki sem svipar til sýnifyrirtækisins hvað varðar sýnigögn og uppsetningargögn. Þessi tegund af fyrirtæki býðst þér án þess að skipta yfir á [30 daga prufutíma](across-preview.md#add-your-own-data-to-an-empty-trial-company), sem hinar Gerðirnar gera.  
- **Framleiðsla - Aðeins uppsetningargögn**  
    Hér er stofnað fyrirtæki sem svipar til **Mitt fyrirtæki** hvað varðar uppsetningargögn, en er án sýnigagna. Það verður hægt að nota þetta fyrirtæki í [30 daga prufutíma](across-preview.md#add-your-own-data-to-an-empty-trial-company).  
- **Stofna nýtt - Engin gögn**  
    Hér er stofnað autt fyrirtæki án uppsetningargagna. Það verður hægt að nota þetta fyrirtæki í [30 daga prufutíma](across-preview.md#add-your-own-data-to-an-empty-trial-company).  

Ef þú vilt byrja auðveldlega með nýtt fyrirtæki, skal velja **Framleiðsla - Aðeins uppsetningargögn** og síðan flytja inn þín eigin viðskiptagögn, eins og viðskiptamenn, vörur og lánardrottnar. Veldu sniðmátið **Nýtt** ef þú vilt setja allt upp frá grunni. Í því tilfelli, geturðu nýtt þér **Uppsetning fyrirtækis** leiðsagnarforrit með stuðningi til að stíga fyrstu skrefin með nauðsynleg uppsetningargögn.  

> [!NOTE]  
> Þegar þú stofnar nýtt fyrirtæki, líða nokkrar mínútur áður en þú getur komist inn í það í [!INCLUDE[prod_short](includes/prod_short.md)]. Uppsetningarstaðan á síðunni **Fyrirtæki** sýnir hvenær nýja fyrirtækið er tilbúið fyrir þig. Þá geturðu skipt yfir í nýja fyrirtækið með því að nota **Mínar stillingar**.  

Á 30 daga reynslutímabilinu geturðu stofnað eins mörg fyrirtæki og þú vilt, en þau verða aðeins aðgengileg á meðan reynslutímabilinu stendur. Nánari upplýsingar má nálgast með því að hafa samband við [!INCLUDE[prod_short](includes/prod_short.md)] samstarfsaðila þinn. Sjá einnig [Dynamics 365 Business Central reynslusögur PRÓFAÐRA FAQ](trial-faq.md) gr.  

## <a name="copy-a-company"></a>Afrita fyrirtæki

Á síðunni **Fyrirtæki** er hægt að nota aðgerðina **Afrita** til að stofna annað fyrirtæki út frá efni fyrirliggjandi fyrirtækis. Þetta er til dæmis gagnlegt þegar þú vilt prófa fyrirtæki án þess að það hafi áhrif á framleiðslugögn.

> [!Important]
> Ekki er hægt að nota þessa aðgerð til að taka öryggisafrit af fyrirtæki. Öryggisafrit er tekið af fyrirtækinu með því að flytja út úr gagnagrunn sem .bacpac-skrá. Frekari upplýsingar er að finna í [Flytja út gagnagrunna](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-database-export) í hjálp við þróun og stjórnun.

## <a name="set-up-the-company"></a>Setja upp fyrirtækið

Þegar þú skráir þig inn í nýtt fyrirtæki, mun **Uppsetning fyrirtækis** leiðsagnarforritið opnast sjálfvirkt og aðstoða þig við að komast af stað. Spurt verður um upplýsingar um fyrirtækið, eins og t.d. aðsetur, bankaupplýsingar, og aðferð kostnaðarútreiknings birgða. Við spyrjum um þessar upplýsingar þar sem þær eru notaðar sem grunnur á mörgum sviðum í [!INCLUDE[prod_short](includes/prod_short.md)], sem þú þarft þá ekki að setja handvirkt upp síðar.  

Aðsetur fyrirtækisins er til dæmis innifalið í reikningum og öðrum skjölum, bankaupplýsingar eru notaðar í greiðslum, og aðferð kostnaðarútreiknings er notuð til að reikna út bæði verð og birgðaverðmat.  

Þegar grunnatriðin eru komin á sinn stað, geturðu sett upp þau grunnsvæði sem eftir eru. Þá er hægt að bæta inn viðskiptagögnum á borð við viðskiptamenn og lánardrottna. Nánari upplýsingar er að finna í [Uppsetning [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md).  

## <a name="companies-and-environments"></a>Fyrirtæki og umhverfi

[!INCLUDE [company_environment](includes/company_environment.md)]

Frekari upplýsingar eru í [Skipta yfir í annað fyrirtæki eða umhverfi](ui-organization-switch.md). Nánari upplýsingar um umhverfismál er að finna [í skilningi laga um innviði Viðskiptamiðs](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology) (á ensku Only).  

## <a name="changing-a-companys-name"></a>Breyta nafni fyrirtækis

Þegar fyrirtæki hefur verið stofnað er ekki hægt að breyta heiti þess. En hægt er að breyta **Birtingarheiti** sem er texti sem verður sýndur fyrir fyrirtækið í gegnum forritið.  

> [!TIP]
> Hægt er að endurnefna fyrirtæki ef [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum er notað.

## <a name="add-contoso-coffee"></a>Bættu við contoso kaffinu

Í contoso Coffee forritinu eru til sýnigögn sem geta hjálpað þér að kanna ítarlega getu [!INCLUDE [prod_short](includes/prod_short.md)]. Finndu App í AppSource, og Settu það upp í tómt fyrirtæki, t.d. fyrirtæki í sandkassa umhverfi. Nánari upplýsingar má finna [í kynningu á kaffi sýnishornum](contoso-coffee/contoso-coffee-intro.md).  

## <a name="see-also"></a>Sjá einnig

[Sérstilla Business Central](ui-customizing-overview.md)  
[Uppsetning [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Grunnstillingum breytt](ui-change-basic-settings.md)  
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Prufuútgáfa og áskrift](across-preview.md)  
[Skilningur á innviðum viðskipta miðlægt á netinu (Enska Only)](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology)  

[!INCLUDE[footer-include](includes/footer-banner.md)]