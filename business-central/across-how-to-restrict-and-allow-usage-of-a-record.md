---
title: Hvernig á að takmarka og leyfa notkun á færslu
description: Eigi að varna því að færsla sé notuð er hægt að virkja tvö verkflæðissvör í verkflæði sem stýrir notkun færslunnar.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/08/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="restrict-and-allow-usage-of-a-record"></a>Takmarka og heimila notkun á færslu

Eigi að varna því að færsla sé notuð í tilteknum aðgerðum, til dæmis, ekki fyrr en færslan hefur verið samþykkt, er hægt að virkja tvö verkflæðissvör sem stýrir notkun færslu. Eitt verkflæðissvar takmarkar notkun færslunnar eins og tilgreint er í verkflæðistilviki og skilyrðum. Hitt verkflæðissvarið leyfir notkun færslunnar eins og hún er skilgreind af verkflæðistilvikinu og skilyrðunum. Tvö svör eru til í sjálfgefnu útgáfunni af [!INCLUDE[prod_short](includes/prod_short.md)] í þessum tilgangi: **Bæta takmörkun við færslu** og **Fjarlægja takmörkun við færslu**.

> [!NOTE]  
> Í sjálfgefnu útgáfunni af [!INCLUDE[prod_short](includes/prod_short.md)] er að finna stuðning við það að takmarka bókun færslu, útflutning færslu sem greiðslu og prentun færslu sem ávísun væri. Til að styðja öðrum takmarkanir, verður samstarfsaðila Microsoft að sérstilla kóða forritsins.  

> [!NOTE]  
> Verkflæðisaðgerð til að takmarka og leyfa að færslur séu notaðar tengist ekki þeirri aðgerð að loka að færslur fyrir vörur, viðskiptavini  og lánardrottna séu bókaðar.

Eftirfarandi ferli útskýrir hvernig á að takmarka að innkaupapantanir séu bókaðar fyrr en þær hafa verið samþykktar. Nýja verkflæðið verður byggt á sniðmátinu *Samþykktarverkflæði innkaupareiknings*.  

## <a name="create-a-workflow-step-that-restricts-posting-of-unapproved-purchase-orders"></a>Stofna verkflæðisskref sem takmarka bókun ósamþykktra innkaupapantanir

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Verkflæði** og velja síðan viðkomandi tengil.  
2. Á síðunni **Verkflæði** skal velja aðgerðina **Nýtt verkflæði úr sniðmáti**. Frekari upplýsingar eru í [Búa til verkflæði úr verkflæðissniðmátum](across-how-to-create-workflows-from-workflow-templates.md).
3. Á síðunni **Verkflæðissniðmát** skal velja sniðmátið *Samþykktarverkflæði innkaupareiknings*.  

   Takið eftir að fyrstu tvö þrep verkflæði fjalla um að takmarka fyrst og leyfa svo notkun á innkaupareikninga. Breyta skilyrðum atburðarins í fyrsta skrefið í nýja verkflæði til að tilgreina að það eigi við innkaupapantanir.  
4. Í flýtiflipanum **Verkflæðisskref** skal velja reitinn **Á skilyrði** fyrir fyrsta skrefið, síðan fyrir síuna **Tegund skjals** skal velja **Pöntun**.  
5. Haldið áfram til að breyta, eyða eða bæta við öðrum verkflæðisskrefum til að endurspegla viðskiptaferli sem hefst með því að takmarka ósamþykktar innkaupapantanir frá því að vera bókaðar.  

## <a name="see-also"></a>Sjá einnig .

[Nota Samþykktarverkflæði](across-use-workflows.md)  
[Stofna verkflæði samþykktar](across-how-to-create-workflows.md)  
[Verkflæði](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
