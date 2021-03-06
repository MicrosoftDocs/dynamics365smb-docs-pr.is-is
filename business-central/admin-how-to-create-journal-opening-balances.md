---
title: Hvernig á að búa til opnunarstöður færslubóka | Microsoft Docs
description: Business Central inniheldur margar keyrslur sem fylgja til aðstoðar við flutningi á gömlum reikningstöðum til nýlega grunnstillts fyrirtækis. Auðvelt er að flytja þessi gögn með færslubókunum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 5e1bb8e34e70d1d906850c157107b9b9701c6c50
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779858"
---
# <a name="create-journal-opening-balances"></a>Stofna opnunarstöður færslubókar

[!INCLUDE[prod_short](includes/prod_short.md)] inniheldur margar keyrslur sem fylgja til aðstoðar við flutningi á gömlum reikningstöðum til nýlega grunnstillts fyrirtækis. Auðvelt er að flytja þessi gögn með færslubók viðskiptavinar, færslubók lánardrottins, birgðabókinni og fjárhagsbók.

Fyrsta skrefið er að stofna grunnstillingarpakka sem inniheldur uppsetningartöflurnar fyrir þessar færslubækur. Eftirfarandi aðferð gerir ráð fyrir því að þessu skrefi sé lokið. Frekari upplýsingar eru í [Setja upp grunnstillingu fyrirtækis](admin-set-up-company-configuration.md). Ferlið lýsir næstu skrefum, en í þeim felst að nota pakkann sem samstarfsaðili veitir.  

Áður en hafist er handa þarf að ganga úr skugga um að notandi sé á hlutverkasíðu stjórnunar því hún býður upp á rétt samhengi fyrir grunnstillingarvinnuna. Frekari upplýsingar eru í [Breyta grundvallarstillingum](ui-change-basic-settings.md).

## <a name="to-apply-the-entries-in-a-journal-to-a-new-company"></a>Til að jafna færslurnar í færslubók við nýtt fyrirtæki

1. Grunnstilla nýtt fyrirtæki og nota grunnstillingarpakka í því. Frekari upplýsingar eru í [Grunnstilla fyrirtæki með RapidStart-leiðsagnarforriti](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).  

    Nýja fyrirtækið inniheldur ekki upplýsingar um opnunarstöður færslubóka.  

2. Opna grunnstillingarvinnublaðið og flytja inn fyrirliggjandi gögn um viðskiptavini, vörur, lánardrottna og fjárhag. Frekari upplýsingar eru í [Yfirfæra gögn viðskiptamanns](admin-migrate-customer-data.md).  

    Nú ertu með aðalgögn á sínum stað. Næst skal bæta við opnunarstöðum. Eftirfarandi skref lýsa því hvernig á að stofna færslubókarlínur fyrir fjárhagsreikninga, en það sama gildir um stofnun færslubókarlína fyrir viðskiptamenn, lánardrottna og vörur.  
3. Velja skal aðgerðina **Stofna fjárhagsbókarlínur fjárhagsreiknings**.  
4. Fylla inn í flýtiflipann **Valkostir** þar sem við á, og setja afmarkanir eftir þörfum. Til dæmis í reitinn **Bókarsniðmát** er fært inn heiti.  
5. Velja hnappinn **Í lagi**. Færslurnar eru nú í færslubók, en upphæðirnar eru auður.  
6. Flytja út færslubókartöflua í Excel og færa handvirkt inn upplýsingar um bókunina og mótreikninginn úr gömlum gögnum.
7. Flytja inn og nota töfluupplýsingar í nýja fyrirtækinu. Færslubókarlínurnar eru tilbúnar til bókunar.  
8. Á grunnstillingarvinnublaðinu skal velja töflu færslubókarlínu og síðan velja aðgerðina **Gagnagrunnsgögn**.  
9. Yfirfara skal upplýsingarnar og síðan velja aðgerðina **Bóka**.  
10. Endurtaka skal skrefin til að flytja inn og bóka aðrar opnunarstöður.  

> [!TIP]
> Hægt er að nota sömu runuvinnslur til að bæta við opnunarstöðum í hvert sinn sem nýr viðskiptamaður eða lánardrottinn sem þú hefur stundað viðskipti með áður en er ekki skráður í [!INCLUDE [prod_short](includes/prod_short.md)]. Leitið einfaldlega að viðkomandi verki og veljið síðan viðkomandi tengil.

## <a name="see-also"></a>Sjá einnig

[Nota skilgreiningu á ný fyrirtæki](admin-apply-configuration-to-new-companies.md)  
[Uppsetning fyrirtækis með RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Stjórnun](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]