---
title: Hvernig á að takmarka og leyfa notkun á færslu
description: Til að takmarka að færsla sé notuð er hægt að taka tvö verkflæðissvör í verkflæði sem stýrir notkun færslunnar.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 04/26/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="restrict-and-allow-usage-of-a-record"></a>Takmarka og leyfa notkun á færslu

Ef takmarka á að færsla sé notuð í ákveðnum aðgerðum, til dæmis þar til færslan hefur verið samþykkt, er hægt að bæta við tveimur verkflæðissvörum í því verkflæði sem stýrir notkun færslunnar. Eitt verkflæðissvar takmarkar notkun færslunnar eins og tilgreint er í verkflæðistilviki og skilyrðum. Hitt svar verkflæðis leyfir notkun færslunnar eins og það er skilgreint af verkflæðisvikinu og skilyrðum. Tvö svör eru til í sjálfgefnu útgáfunni af [!INCLUDE[prod_short](includes/prod_short.md)] í þessum tilgangi: **Bæta takmörkun við færslu** og **Fjarlægja takmörkun við færslu**.

> [!NOTE]  
> Í sjálfgefnu útgáfunni af [!INCLUDE[prod_short](includes/prod_short.md)] er að finna stuðning við það að takmarka bókun færslu, útflutning færslu sem greiðslu og prentun færslu sem ávísun væri. Til að styðja öðrum takmarkanir, verður samstarfsaðila Microsoft að sérstilla kóða forritsins.  

> [!NOTE]  
> Verkflæðisaðgerð til að takmarka og leyfa að færslur séu notaðar tengist ekki þeirri aðgerð að loka að færslur fyrir vörur, viðskiptavini  og lánardrottna séu bókaðar.

Eftirfarandi ferli útskýrir hvernig á að takmarka að innkaupapantanir séu bókaðar fyrr en þær hafa verið samþykktar. Nýja verkflæðið er byggt á sniðmátinu *Samþykktarverkflæði innkaupareiknings* .  

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
