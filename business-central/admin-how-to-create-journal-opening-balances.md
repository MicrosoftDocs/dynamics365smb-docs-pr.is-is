---
title: "Hvernig á að búa til opnunarstöður færslubóka | Microsoft Docs"
description: "Business Central inniheldur margar keyrslur sem fylgja til aðstoðar við flutningi á gömlum reikningstöðum til nýlega grunnstillts fyrirtækis. Auðvelt er að flytja þessi gögn með færslubókunum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: fc8e8f34220643b7cd3fd357aea3807641cee911
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="create-journal-opening-balances"></a>Stofna opnunarstöður færslubókar
[!INCLUDE[d365fin](includes/d365fin_md.md)] inniheldur margar keyrslur sem fylgja til aðstoðar við flutningi á gömlum reikningstöðum til nýlega grunnstillts fyrirtækis. Auðvelt er að flytja þessi gögn með færslubók viðskiptavinar, færslubók lánardrottins, birgðabókinni og fjárhagsbók.

Fyrsta skrefið er að stofna grunnstillingarpakka sem inniheldur uppsetningartöflurnar fyrir þessar færslubækur. Eftirfarandi aðferð gerir ráð fyrir því að þessu skrefi sé lokið. Frekari upplýsingar eru í [Setja upp grunnstillingu fyrirtækis](admin-set-up-company-configuration.md). Ferlið lýsir næstu skrefum, en í þeim felst að nota pakkann sem samstarfsaðili veitir.  

Áður en hafist er handa þarf að ganga úr skugga um að notandi sé á hlutverkasíðu RapidStart Services innleiðara því hún býður upp á rétt samhengi fyrir grunnstillingarvinnuna. Frekari upplýsingar, sjá [Breyta grunnstillingum](ui-change-basic-settings.md).

## <a name="to-apply-the-entries-in-a-journal-to-a-new-company"></a>Til að jafna færslurnar í færslubók við nýtt fyrirtæki  
1. Grunnstilla nýtt fyrirtæki og nota grunnstillingarpakka í því. Frekari upplýsingar eru í [Grunnstilla fyrirtæki með RapidStart-leiðsagnarforriti](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).  

    Nýja fyrirtækið inniheldur ekki upplýsingar um opnunarstöður færslubóka.  

2. Opna grunnstillingarvinnublaðið og flytja inn fyrirliggjandi gögn um viðskiptavini, vörur, lánardrottna og fjárhag. Frekari upplýsingar eru í [Yfirfæra gögn viðskiptamanns](admin-migrate-customer-data.md).  
3. Til dæmis skal velja aðgerðina **Stofna fjárhagsbókarlínur**.  
4. Fylla inn í flýtiflipann **Valkostir** þar sem við á, og setja afmarkanir eftir þörfum. Til dæmis í reitinn **Bókarsniðmát** er fært inn heiti.  
5. Velja hnappinn **Í lagi**. Færslurnar eru nú í færslubók, en upphæðirnar eru auður.  
6. Flytja út færslubókartöflua í Excel og færa handvirkt inn upplýsingar um bókunina og mótreikninginn úr gömlum gögnum.
7. Flytja inn og nota töfluupplýsingar í nýja fyrirtækinu. Færslubókarlínurnar eru tilbúnar til bókunar.  
8. Á grunnstillingarvinnublaðinu skal velja töflu færslubókarlínu og síðan velja aðgerðina **Gagnagrunnsgögn**.  
9. Yfirfara skal upplýsingarnar og síðan velja aðgerðina **Bóka**.  
10. Endurtaka skal skrefin til að flytja inn og bóka aðrar opnunarstöður.  

## <a name="see-also"></a>Sjá einnig  
[Nota skilgreiningu á ný fyrirtæki](admin-apply-configuration-to-new-companies.md)  
[Uppsetning fyrirtækis með RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Stjórnun](admin-setup-and-administration.md)

