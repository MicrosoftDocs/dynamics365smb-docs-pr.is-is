---
title: Hvernig á að takmarka og leyfa notkun á færslu | Microsoft Docs
description: Eigi að varna því að færsla sé notuð í tilteknum aðgerðum, til dæmis, ekki fyrr en færslan hefur verið samþykkt, er hægt að virkja tvö verkflæðissvör sem stýrir notkun færslu.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: bbb22a00e878e8c4d75cb5fcdbcc27a28d9d22a4
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783992"
---
# <a name="restrict-and-allow-usage-of-a-record"></a>Takmarka og heimila notkun á færslu
Eigi að varna því að færsla sé notuð í tilteknum aðgerðum, til dæmis, ekki fyrr en færslan hefur verið samþykkt, er hægt að virkja tvö verkflæðissvör sem stýrir notkun færslu. Eitt verkflæðissvar mun takmarka notkun færslunnar eins og tilgreint er í verkflæðistilviki og skilyrðum. Annað verkflæðissvar mun heimila notkun færslunnar eins og tilgreint er í verkflæðistilviki og skilyrðum. Tvenns konar svörun er til í almennu útgáfunni af [!INCLUDE[prod_short](includes/prod_short.md)] í þessum tilgangi: **Takmarka notkun á færslu** og **heimila notkun á færslu**.

> [!NOTE]  
>  Í almennu útgáfunni af [!INCLUDE[prod_short](includes/prod_short.md)] er að finna stuðnig við það að takmarka bókun færslu, útflutning færslu sem greiðslu og prentun færslu sem ávísun væri. Til að styðja öðrum takmarkanir, verður samstarfsaðila Microsoft að sérstilla kóða forritsins.  

> [!NOTE]  
>  Verkflæðisaðgerð til að takmarka og leyfa að færslur séu notaðar tengist ekki þeirri aðgerð að loka að færslur fyrir vörur, viðskiptavini  og lánardrottna séu bókaðar.

Eftirfarandi ferli sýnir hvernig á að takmarka að innkaupapantanir séu bókað fyrr en þeir hafa verið samþykktar. Nýja verkflæði verður byggð á fyrirliggjandi verkflæðissniðmáti samþykktarverkflæðis innkaupareiknings.  

## <a name="to-create-a-workflow-step-that-restricts-posting-of-unapproved-purchase-orders"></a>Til að stofna verkflæðisskref sem takmarka bókun ósamþykktra innkaupapantanir  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verkflæði** og veldu síðan tengda tengilinn.  
2. Á síðunni **Verkflæði** er stofnuð nýtt verkflæði með heitinu Samþykktarverkflæði innkaupapöntunar. Frekari upplýsingar eru í [Búa til verkflæði](across-how-to-create-workflows.md).  
3. Valin er aðgerðin **Afrita úr verkflæðissniðmáti**.  
4. Veljið reitur **Verkflæðiskóði uppruna** og svo á síðunni **Sniðmát verkflæðis** skal velja verkflæðissniðmátið Samþykktarverkflæði innkaupapöntunar.  

     Takið eftir að fyrstu tvö þrep verkflæði fjalla um að takmarka fyrst og leyfa svo notkun á innkaupareikninga. Því næst skal breyta skilyrðum atburðarins í fyrsta skrefið í nýja verkflæði til að tilgreina að það eigi við innkaupapantanir.  
5. Á flýtiflipi **verkflæðisskref** skal velja reitur **Skilyrði tiliviks** og svo, fyrir síuna **tegund skjals**, skal velja **pöntun**.  
6. Haldið áfram til að breyta, eyða eða bæta við öðrum verkflæðisskrefum til að passa við viðskiptaferli sem hefst með því að takmarka ósamþykktar innkaupapantanir frá því að vera bókaðar.  

## <a name="see-also"></a>Sjá einnig  
[Búa til verkflæði](across-how-to-create-workflows.md)   
[Verkflæði](across-workflow.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]