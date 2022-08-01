---
title: Hvernig á að takmarka og leyfa notkun á færslu
description: Eigi að varna því að færsla sé notuð er hægt að virkja tvö verkflæðissvör í verkflæði sem stýrir notkun færslunnar.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 7873091d64e55460986437cf255d98cd0d00b6d3
ms.sourcegitcommit: f1e272485a0e675d337a694aba3e35a5daf43920
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/09/2022
ms.locfileid: "9130146"
---
# <a name="restrict-and-allow-usage-of-a-record"></a>Takmarka og heimila notkun á færslu

Eigi að varna því að færsla sé notuð í tilteknum aðgerðum, til dæmis, ekki fyrr en færslan hefur verið samþykkt, er hægt að virkja tvö verkflæðissvör sem stýrir notkun færslu. Eitt verkflæðissvar mun takmarka notkun færslunnar eins og tilgreint er í verkflæðistilviki og skilyrðum. Annað verkflæðissvar mun heimila notkun færslunnar eins og tilgreint er í verkflæðistilviki og skilyrðum. Tvö svör eru til í sjálfgefinni útgáfu í þessum tilgangi: [!INCLUDE[prod_short](includes/prod_short.md)] Bæta skráningu **takmörkun og** Fjarlægja takmörkun á **skráningu**.

> [!NOTE]  
> Sjálfgefin útgáfa [!INCLUDE[prod_short](includes/prod_short.md)] býður upp á stuðning við að takmarka færslu frá því að vera bókuð sem greiðsla og prenta út sem ávísun. Til að styðja öðrum takmarkanir, verður samstarfsaðila Microsoft að sérstilla kóða forritsins.  

> [!NOTE]  
> Verkflæðisaðgerð til að takmarka og leyfa að færslur séu notaðar tengist ekki þeirri aðgerð að loka að færslur fyrir vörur, viðskiptavini  og lánardrottna séu bókaðar.

Eftirfarandi ferli lýsir því hvernig á að takmarka innkaupapantanir frá bókun þar til þær hafa verið samþykktar. Nýja verkflæðið verður Byggt á sniðmáti fyrir verkflæði fyrir innkaupareikning.  

## <a name="to-create-a-workflow-step-that-restricts-posting-of-unapproved-purchase-orders"></a>Til að stofna verkflæðisskref sem takmarka bókun ósamþykktra innkaupapantanir

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Verkflæði** og velja síðan viðkomandi tengil.  
2. Á síðunni **Verkflæði** skal velja aðgerðina **Nýtt verkflæði úr sniðmáti**. Nánari upplýsingar eru í [Stofna verkflæði út frá verkflæðissniðmátum](across-how-to-create-workflows-from-workflow-templates.md).
3. **Í síðunni verkflæðissniðmát** skal velja *Sniðmát samþykkissniðmáts* innkaupareiknings.  

   Takið eftir að fyrstu tvö þrep verkflæði fjalla um að takmarka fyrst og leyfa svo notkun á innkaupareikninga. Því næst skal breyta skilyrðum atburðarins í fyrsta skrefið í nýja verkflæði til að tilgreina að það eigi við innkaupapantanir.  
4. **Á flipanum flýtiflæðisskref** er reiturinn fyrir skilyrði **valinn** fyrir fyrsta skrefið og síðan fyrir **Afmörkun skjalgerðarinnar**, veljið **pöntun**.  
5. Haldið áfram til að breyta, eyða eða bæta við öðrum verkflæðisskrefum til að passa við viðskiptaferli sem hefst með því að takmarka ósamþykktar innkaupapantanir frá því að vera bókaðar.  

## <a name="see-also"></a>Sjá einnig .

[Búa til verkflæði](across-how-to-create-workflows.md)  
[Verkflæði](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]