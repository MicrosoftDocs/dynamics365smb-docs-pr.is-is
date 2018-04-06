---
title: "Hvernig á að takmarka og leyfa notkun á færslu | Microsoft Docs"
description: "Eigi að varna því að færsla sé notuð í tilteknum aðgerðum, til dæmis, ekki fyrr en færslan hefur verið samþykkt, er hægt að virkja tvö verkflæðissvör sem stýrir notkun færslu."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 4636cdedc2c99d1aa7cfc2dc361f7135aa3c4199
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="restrict-and-allow-usage-of-a-record"></a>Takmarka og heimila notkun á færslu
Eigi að varna því að færsla sé notuð í tilteknum aðgerðum, til dæmis, ekki fyrr en færslan hefur verið samþykkt, er hægt að virkja tvö verkflæðissvör sem stýrir notkun færslu. Eitt verkflæðissvar mun takmarka notkun færslunnar eins og tilgreint er í verkflæðistilviki og skilyrðum. Annað verkflæðissvar mun heimila notkun færslunnar eins og tilgreint er í verkflæðistilviki og skilyrðum. Tvenns konar svörun er til í almennu útgáfunni af [!INCLUDE[d365fin](includes/d365fin_md.md)] í þessum tilgangi: **Takmarka notkun á færslu** og **heimila notkun á færslu**.

> [!NOTE]  
>  Í almennu útgáfunni af [!INCLUDE[d365fin](includes/d365fin_md.md)] er að finna stuðnig við það að takmarka bókun færslu, útflutning færslu sem greiðslu og prentun færslu sem ávísun væri. Til að styðja öðrum takmarkanir, verður samstarfsaðila Microsoft að sérstilla kóða forritsins.  

> [!NOTE]  
>  Verkflæðisaðgerð til að takmarka og leyfa að færslur séu notaðar tengist ekki þeirri aðgerð að loka að færslur fyrir vörur, viðskiptavini  og lánardrottna séu bókaðar.

Eftirfarandi ferli sýnir hvernig á að takmarka að innkaupapantanir séu bókað fyrr en þeir hafa verið samþykktar. Nýja verkflæði verður byggð á fyrirliggjandi verkflæðissniðmáti samþykktarverkflæðis innkaupareiknings.  

## <a name="to-create-a-workflow-step-that-restricts-posting-of-unapproved-purchase-orders"></a>Til að stofna verkflæðisskref sem takmarka bókun ósamþykktra innkaupapantanir  
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Verkflæði** og velja svo viðeigandi tengil.  
2. Í glugganum **Verkflæði** er stofnuð nýtt verkflæði með heitinu Samþykktarverkflæði innkaupapöntunar. Frekari upplýsingar eru í [Búa til verkflæði](across-how-to-create-workflows.md).  
3. Valin er aðgerðin **Afrita úr verkflæðissniðmáti**.  
4. Veljið reitur **Verkflæðiskóði uppruna** og svo í glugganum **Sniðmát verkflæðis** skal velja verkflæðissniðmátið Samþykktarverkflæði innkaupapöntunar.  

     Takið eftir að fyrstu tvö þrep verkflæði fjalla um að takmarka fyrst og leyfa svo notkun á innkaupareikninga. Því næst skal breyta skilyrðum atburðarins í fyrsta skrefið í nýja verkflæði til að tilgreina að það eigi við innkaupapantanir.  
5. Á flýtiflipi **verkflæðisskref** skal velja reitur **Skilyrði tiliviks** og svo, fyrir síuna **tegund skjals**, skal velja **pöntun**.  
6. Haldið áfram til að breyta, eyða eða bæta við öðrum verkflæðisskrefum til að passa við viðskiptaferli sem hefst með því að takmarka ósamþykktar innkaupapantanir frá því að vera bókaðar.  

## <a name="see-also"></a>Sjá einnig  
[Búa til verkflæði](across-how-to-create-workflows.md)   
[Verkflæði](across-workflow.md)   

