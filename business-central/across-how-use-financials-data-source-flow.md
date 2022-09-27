---
title: Nota Viðskiptamiðað í Power Automate streymi
description: Setja upp og nota Power Automate flæðisafn sem stofnar aðalgögn fyrirtækja eða breytir því.
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, OData, Power App, SOAP, Entity set not found, workflowWebhookSubscriptions
ms.date: 05/12/2022
ms.author: edupont
author: jswymer
ms.openlocfilehash: 056fe537df2fba23e02cb4e70675937cde724fbf
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/19/2022
ms.locfileid: "9533025"
---
# <a name="use-prod_short-in-power-automate-flows"></a>Notkun [!INCLUDE[prod_short](includes/prod_short.md)] í Power Automate flæðigryfjur

Notandi getur notað [!INCLUDE[prod_short](includes/prod_short.md)]-gögnin sín sem hluta af verkflæði í Microsoft Power Automate. Búðu til þitt eigið flæði og Tengdu gögnin þín við [!INCLUDE [prod_short](includes/prod_short.md)] tengivirkið.  

> [!NOTE]  
> Notandi verður að vera með gildan reikning hjá [!INCLUDE[prod_short](includes/prod_short.md)] og hjá Power Automate.  

> [!TIP]
> Auk þess er hægt að Power Automate nota sniðmát samþykktarverkflæðis í [!INCLUDE[prod_short](includes/prod_short.md)]. Þó að þau séu tvö aðskilin verkflæðiskerfi er einhverju samþykktarverksniðmáti sem búið er að stofna með Power Automate bætt við listann yfir verkflæði að innan [!INCLUDE[prod_short](includes/prod_short.md)]. Sjá [verkflæði](across-workflow.md) fyrir frekari upplýsingar.  

## <a name="automated-workflows"></a>Sjálfvirk verkflæði

Með Power Automate er hægt að búa til viðskiptastreymi beint í hús og treysta á eldri hönnuði. Frekari upplýsingar er að finna [í setja upp sjálfvirk verkflæði](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) í innihaldi stjórnunar.  

## <a name="manual-instant-flows"></a>Handhæg skyndilausnir

Stjórnun [!INCLUDE [prod_short](includes/prod_short.md)] online getur [kveikt á eiginleiki](admin-feature-management.md) á netinu til að gera það mögulegt að keyra Power Automate flæði frá flestum síðum. 2022 Frekari upplýsingar er að finna [í setja upp sjálfvirk verkflæði](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) í innihaldi stjórnunar.  

Þegar admin hefur tengst [!INCLUDE [prod_short](includes/prod_short.md)] við Power Automate er hægt að sjá hvaða flæði fyrirtækið hefur bætt við þegar aðgerðin automate **er valin** á viðeigandi síðum. Þú keyrir streyminn án þess að fara [!INCLUDE [prod_short](includes/prod_short.md)].  

Þessi sjálfvirku verkflæði opna í rúðu inni [!INCLUDE [prod_short](includes/prod_short.md)] á netinu þannig að þú helst innan samhengis við viðskiptaferlið sem þú varst í miðri. Á sumum síðum **felur automate** -aðgerðin undir **valmyndinni fleiri Valkostir** en að finna hana, velja **Power Automate** valmyndaratriðið og velja síðan viðeigandi tengil til að ræsa verkflæðið. Tengingin Power Automate sem þegar er uppsett fyrir þig.  

Flest flæði gerir kröfu um að fyllt sé í reit eða tvo áður en aðgerðin keyra flæði **er valin**.  

> [!TIP]
> Ef þú sérð **ekki automate** aðgerð þá [!INCLUDE [prod_short](includes/prod_short.md)] hefur líklega ekki enn verið sett upp notkun Power Automate. Nánari upplýsingar er að biðja um admin.

## <a name="add-more-automated-flows-and-manual-instant-flows"></a>Bæta við fleiri sjálfvirkum flæðum og handvirku skyndilausnum

Hægt er að búa til streymi á [heimasíðu powerautomate.microsoft.com](https://powerautomate.microsoft.com). Hins vegar ef admin hefur kveikt á getu til að keyra flæði frá innu Power Automate á netinu er hægt að hefja vinnslu á flæði úr [!INCLUDE [prod_short](includes/prod_short.md)]**sjálfkeyrandi** aðgerðinni á viðkomandi síðum. Á sumum síðum **felur automate** -aðgerðin undir **valmyndinni fleiri Valkostir** en að **Power Automate** finna hana, velja valmyndaratriðið og velja **síðan flæðiaðgerðina** Create. Power Automate Þá opnast í nýjum vafraflipa og þá skráir notandi sig inn sjálfkrafa.

## <a name="manage-workflows"></a>Stjórna verkflæði

Hægt er að fá yfirlit yfir öll verkflæði sem notandi hefur aðgang að með því að velja **aðgerðina stjórna verkflæði** í **Power Automate** valmyndinni. Listinn opnast í nýjum vafraflipa og þú skráir þig inn Power Automate sjálfkrafa. Þar er hægt að sjá hvenær hvert rennsli hljóp mest nýlega.  

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/use-power-automate/)

## <a name="see-also"></a>Sjá einnig .

[[!INCLUDE[prod_short](includes/prod_short.md)] Úrræðaleit vegna sjálfvirkra verkflæða](across-flow-troubleshoot.md)  
[Vertu klár í rekstur fyrirtækja](ui-get-ready-business.md)  
[Verkflæði](across-workflow.md)  
[Flytja inn viðskiptagögn úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Úthluta leyfi til notenda og hópa](ui-define-granular-permissions.md)  
[Setja upp[!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Fjármál](finance.md)  
[Setja upp sjálfvirk verkflæði](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
