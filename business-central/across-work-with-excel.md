---
title: Skoða og breyta í Excel From Business Central
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
ms.openlocfilehash: 7e3abf36444c4701229ffaac7ceade11bb1879cc
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786933"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Skoða og breyta í Excel From Business Central

Með síðum sem birta lista yfir færslur í línum og dálkum, eins og lista yfir viðskiptavini, sölupantanir eða reikninga, geturðu einnig skoðað færslur með Microsoft Excel. Til að gera þetta hefur þú tvo valkosti. Þú getur annaðhvort valið aðgerina **Opna í Excel** eða aðgerðina **Breyta í Excel** á síðunni. Munurinn á aðgerðunum tveimur er sem hér segir:  

## <a name="open-in-excel"></a>Opna í Excel

- Með þessari aðgerð tekur Excel allar síur á síðunni til greina sem takmarka færslurnar sem eru sýndar. Excel-vinnubókin mun innihalda sömu línur og dálka sem birtast á síðunni í [!INCLUDE[prod_short](includes/prod_short.md)].

- Þú getur gert breytingar á færslum í Excel, en þú getur ekki birt þær aftur í [!INCLUDE[prod_short](includes/prod_short.md)]. Þú getur aðeins vistað breytingarnar í Excel-skrá í tölvunni þinni.

- Þessi aðgerð virkar bæði í Windows og macOS.

> [!NOTE]
> **Open í Excel** aðgerðin er sjálfgefið tiltæk fyrir [!INCLUDE[prod_short](includes/prod_short.md)] innanhúss. Ef þú setur hins vegar upp [!INCLUDE[prod_short](includes/prod_short.md)] innanhúss fyrir breytingar í Excel er **Opna í Excel** aðgerðinni skipt út fyrir aðgerðina **Breyta í Excel**.

## <a name="edit-in-excel"></a>Breyta í Excel

- Með þessari aðgerð tekur Excel flestar síur á síðunni til greina sem takmarka færslurnar sem eru sýndar, þannig að Excel-vinnubókin innihaldi nánast sömu færslur og dálka.

- Kosturinn við aðgerðina **Breyta í Excel** er að þú getur gert breytingar á færslum í Excel og síðan birt breytingarnar aftur í [!INCLUDE[prod_short](includes/prod_short.md)].

- Það virkar aðeins á Windows; ekki macOS.

- Hægt er að skipta um fyrirtæki sem unnið er með. Til að skipta um fyrirtæki skal velja **Valkostir** táknið, ![Valkostir Excel-innbótar](media/cogwheel.png "Valkostir Excel-innbótar") í svæði Excel-innbótar og síðan velja fyrirtækið í reitnum **Fyrirtæki**.  

    > [!IMPORTANT]
    > Þegar skipt er um fyrirtæki skal ganga úr skugga um að reiturinn **Umhverfi** sé ekki auður. Ef svo er skal stilla hann á einn af tiltækum valkostum, annars virkar innbótin ekki sem skyldi.  

Ef verið er að gera breytingar á innbótinni verður að endurhlaða hana til að uppfæra tenginguna. Til að endurhlaða skal nota valmyndina ![Excel-innbót](media/excel-addin-menu.png "Valkostir Excel-innbótar") efst í hægra horni innbótarinnar. Ef ekki er hægt að hlaða innbótinni skal tala við kerfisstjóra. Ef notandi er kerfisstjóri skal skoða [Setja upp Excel-innbótina fyrir Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

> [!NOTE]
> Fyrir [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum er aðgerðin **Breyta í Excel** aðeins í boði ef stjórnandi hefur stillt Excel-innbótina og aðeins í boði fyrir vefbiðlara. Ef stjórnendur langar að fræðast betur um hvernig eigi að setja upp Excel-innbótina má finna upplýsingar um það í [Setja upp Excel-innbótina fyrir Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

### <a name="see-the-differences-between-the-options"></a>Sjá muninn á milli valkostanna
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig

[Greina fjárhagsskýrslur í Microsoft Excel](finance-analyze-excel.md)  
[Unnið með Business Central](ui-work-product.md)  
[Endurbætur á Excel-samþættingu í 2019 útgáfu 2](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]