---
title: Hvernig á að takmarka og leyfa notkun á færslu
description: Eigi að varna því að færsla sé notuð er hægt að virkja tvö verkflæðissvör í verkflæði sem stýrir notkun færslunnar.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 09/08/2022
ms.author: edupont
ms.openlocfilehash: 2542dac4eba91d0d6d7dd3c773b19e1f6fd235a5
ms.sourcegitcommit: 9049f75c86dea374e5bfe297304caa32f579f6e4
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/23/2022
ms.locfileid: "9585973"
---
# <a name="restrict-and-allow-usage-of-a-record"></a>Takmarka og heimila notkun á færslu

Ef takmarka á færslu frá notkun í tiltekinni verkþætti, til dæmis þar til færslan hefur verið samþykkt, er hægt að fella tvö verkflæðisvör inn í verkflæðið sem stýrir notkun færslunnar. Ein svörun verkflæðis takmarkar notkun færslunnar eins og hún er skilgreind fyrir verkflæðistilvik og aðstæður. Önnur verkflæðissvörun leyfir notkun færslunnar eins og hún er skilgreind fyrir verkflæðistilvik og aðstæður. Tvö svör eru til í sjálfgefinni útgáfu í þessum tilgangi: [!INCLUDE[prod_short](includes/prod_short.md)] Bæta skráningu **takmörkun og** Fjarlægja takmörkun á **skráningu**.

> [!NOTE]  
> Sjálfgefin útgáfa [!INCLUDE[prod_short](includes/prod_short.md)] býður upp á stuðning við að takmarka færslu frá því að vera bókuð sem greiðsla og prenta út sem ávísun. Til að styðja öðrum takmarkanir, verður samstarfsaðila Microsoft að sérstilla kóða forritsins.  

> [!NOTE]  
> Verkflæðisaðgerð til að takmarka og leyfa að færslur séu notaðar tengist ekki þeirri aðgerð að loka að færslur fyrir vörur, viðskiptavini  og lánardrottna séu bókaðar.

Eftirfarandi ferli lýsir því hvernig á að takmarka innkaupapantanir frá bókun þar til þær hafa verið samþykktar. Nýja verkflæðið verður Byggt á sniðmáti fyrir verkflæði *fyrir* innkaupareikning.  

## <a name="create-a-workflow-step-that-restricts-posting-of-unapproved-purchase-orders"></a>Stofna verkflæðisskref sem takmarkar bókun ósamþykktra innkaupapantana

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **verkflæði** og velja síðan tengdan tengil.  
2. Á síðunni **Verkflæði** skal velja aðgerðina **Nýtt verkflæði úr sniðmáti**. Frekari upplýsingar um [Stofna verkflæði úr Verkflæðissniðmátum](across-how-to-create-workflows-from-workflow-templates.md).
3. **Í síðunni verkflæðissniðmát** skal velja *Sniðmát samþykkissniðmáts* innkaupareiknings.  

   Athugið að fyrstu tvær verkflæðisskrefin eru um takmörkun og síðan notkun á innkaupareikningum. Breyttu tilvikstilskilinu í fyrsta skref nýja verkflæðisins til að tilgreina að það eigi við um innkaupapantanir.  
4. **Í fastflipa Verkflæðisskrefsins**, skal velja **svæðið í condition** fyrir fyrsta skrefið, síðan fyrir **Afmörkun skjalgerðarinnar**, velja **pöntun**.  
5. Haldið er áfram að breyta, eyða eða bæta við öðrum verkflæðisskrefum til að endurspegla viðskiptaferli sem byrjar á því að takmarka ósamþykktar innkaupapantanir frá bókun.  

## <a name="see-also"></a>Sjá einnig .

[Nota samþykktarverkflæði](across-use-workflows.md)  
[Stofna samþykktarverkflæði](across-how-to-create-workflows.md)  
[Verkflæði](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
