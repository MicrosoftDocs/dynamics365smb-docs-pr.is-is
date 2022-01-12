---
title: Skoðun og breytingar í Excel frá Viðskiptamiðinu (inniheldur Video)
description: Lærðu hvernig hægt er að opna síðurnar í Microsoft Excel frá Business Central til að fá betri gagnagreiningar.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 7800eb9d9852e8cc13eed26ce3e42fa318f7e185
ms.sourcegitcommit: 4c97f38fc53c1c1ec534054a4a100d8cfb73175b
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2021
ms.locfileid: "7940252"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Skoða og breyta í Excel From Business Central

Með síðum sem birta lista yfir færslur í línum og dálkum, eins og lista yfir viðskiptavini, sölupantanir eða reikninga, geturðu flutt út listannn í Microsoft Excel og skoðað hann þar. Þú hefur tvo valkosti til að skoða í Excel en það fer eftir síðunni. Báðir valkostirnir eru í boði undir tákninu **Deila** ![Deila síðu í öðru forriti.](media/share-icon.png) efst á síðu. Þú getur annaðhvort valið aðgerina **Opna í Excel** eða aðgerðina **Breyta í Excel** á síðunni. Í þessari grein er munurinn á aðgerðunum tveimur útskýrður.

## <a name="open-in-excel"></a>Opna í Excel

Með aðgerðinni **Opna í Excel** er hægt að gera breytingar á færslum í Excel, en þú getur ekki birt þær aftur í [!INCLUDE[prod_short](includes/prod_short.md)]. Þú getur aðeins vistað breytingarnar í Excel-skrá án þess að það hafi áhrif á gögn í [!INCLUDE[prod_short](includes/prod_short.md)].

- Með þessari aðgerð tekur Excel allar síur á síðunni til greina sem takmarka færslurnar sem eru sýndar. Excel-vinnubókin mun innihalda sömu línur og dálka sem birtast á síðunni í [!INCLUDE[prod_short](includes/prod_short.md)].

- Þessi aðgerð virkar bæði í Windows og macOS.

- Frá og með uppfærslu 18.3 er einnig hægt að skoða lista sem eru sýndir í síðuhlutum, eins og línurnar í sölupöntun. 

> [!NOTE]
> **Open í Excel** aðgerðin er sjálfgefið tiltæk fyrir [!INCLUDE[prod_short](includes/prod_short.md)] innanhúss. Ef þú setur hins vegar upp [!INCLUDE[prod_short](includes/prod_short.md)] innanhúss fyrir breytingar í Excel er **Opna í Excel** aðgerðinni skipt út fyrir aðgerðina **Breyta í Excel**.

[!INCLUDE [send-report-excel](includes/send-report-excel.md)]  

## <a name="edit-in-excel"></a>Breyta í Excel

Aðgerðin **Breyta í Excel** er í boði í flestum listum en ekki öllum. Með aðgerðinni **Breyta í Excel** gerir þú breytingar á færslum í Excel og birtir síðan breytingarnar aftur í [!INCLUDE[prod_short](includes/prod_short.md)]. Þegar Excel opnast sérðu gluggann **Excel-innbót** hægra megin.

- Með þessari aðgerð tekur Excel flestar síur á síðunni til greina sem takmarka færslurnar sem eru sýndar, þannig að Excel-vinnubókin innihaldi nánast sömu færslur og dálka.

- Til að fá nýjustu gögnin úr [!INCLUDE[prod_short](includes/prod_short.md)] skal velja **Uppfæra** í glugga Excel-innbótar.

- Hægt er að skipta um fyrirtæki sem unnið er með. Til að skipta um fyrirtæki velur þú táknið **Valkostir** ![Valkostir Excel-innbótar.](media/cogwheel.png "Valkostir Excel-innbótar") í glugga Excel-innbótar skal síðan velja fyrirtækið í reitnum **Fyrirtæki**.  

    > [!IMPORTANT]
    > Þegar skipt er um fyrirtæki skal ganga úr skugga um að reiturinn **Umhverfi** sé ekki auður. Ef svo er skal stilla hann á einn af tiltækum valkostum, annars virkar innbótin ekki sem skyldi.  

Ef verið er að gera breytingar á innbótinni verður að endurhlaða hana til að uppfæra tenginguna. Til að endurhlaða skal nota valmyndina ![Excel-innbót](media/excel-addin-menu.png "Valkostir Excel-innbótar") efst í hægra horni innbótarinnar. Ef ekki er hægt að hlaða innbótinni skal tala við kerfisstjórann. Ef þú ert kerfisstjórinn skaltu skoða [Sækja innbót Business Central fyrir Excel](admin-deploy-excel-addin.md).

> [!NOTE]
> Innbótin virkar með Excel fyrir vefinn (á netinu) úr hvaða tæki sem er svo lengi sem þú notar viðurkenndan vafra. Hún virkar einnig með Excel-forritinu fyrir Windows (PC); en ekki fyrir macOS.
>
> Fyrir [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum er aðgerðin **Breyta í Excel** aðeins í boði ef stjórnandi hefur stillt Excel-innbótina og aðeins í boði fyrir vefbiðlara. Ef stjórnendur langar að fræðast betur um hvernig eigi að setja upp Excel-innbótina má finna upplýsingar um það í [Setja upp Excel-innbótina fyrir Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).


<!-- Note for later: here we're immediately jumping to pretty advanced topics like changing company or reloading the addin. Fine to keep them for now. In the future, we will first need to explain in more detail the actual functionality of the addin, primarily these sub-sections:

Refreshing record data in Excel
Editing and publishing back to Business Central
Creating new records from Excel
Crafting your own editable Excel.
Point (4) is where it gets interesting for changing/specifying company, environment and other connection settings-->

### <a name="first-time-sign-in"></a>Fyrsta innskráning

Aðgerðin **Breyta í Excel** krefst þess að innbót Business Central sé uppsett í Excel. Í sumum tilvikum gæti kerfisstjórinn hafa sett upp innbótina til að setja sjálfkrafa upp fyrir þig. Í þessu tilviki þarftu bara að skrá þig inn í Business Central í glugga **Excel-innbótar** með notandanafni og lykilorði. Annars opnast glugginn **Ný Office-innbót**. Til að setja upp innbótina skal velja **Treysta þessari innbót** sem mun setja upp innbótina beint úr Office-versluninni.

Ef uppsetning innbótarinnar gengur ekki af einhverjum ástæðum skaltu hafa samband við stjóranda eða reyna að setja hana upp handvirkt. Frekari upplýsingar er að finna í [Setja upp innbótina handvirkt til eigin nota](admin-deploy-excel-addin.md#install).

## <a name="see-the-differences-between-the-options"></a>Sjá muninn á milli valkostanna
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig

[Greina fjárhagsskýrslur í Microsoft Excel](finance-analyze-excel.md)  
[Unnið með Business Central](ui-work-product.md)  
[Endurbætur á Excel-samþættingu í 2019 útgáfu 2](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]