---
title: Setja upp verkflæði (inniheldur myndefni)
description: Settu upp verkflæði, notendur verkflæðis og samþykkjendur til að tengja kerfisverk viðskiptaferlis sem þessi notendur framkvæma.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 7676e05255c31bd2b9906951d98d1a87622a0fcf
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/19/2022
ms.locfileid: "9530271"
---
# <a name="set-up-workflows"></a>Setja upp verkflæði

Hægt er að setja upp og nota verkflæði sem tengja viðskiptaferlisverk sem framkvæmd erf af ólíkum notandi. Kerfisverk, s.s. sjálfvirk bókun, er hægt að hafa sem skerf í verkflæði, á undan eða eftir notandaverkum. Að óska eftir samþykki eða samþykkja nýjar færslur eru dæmigerð skref í verkflæði. Sjá [Use verkflæði](across-use-workflows.md) fyrir frekari upplýsingar.  

Áður en þú byrjar að nota verkflæði þarf að setja upp verkflæðinotendur og samþykktarnotendur, til að tilgreina hvernig notendur fá tilkynningar um verkflæðisskref og búa svo til verkflæði.  

Á síðunni **Verkflæði** er hægt að stofna verkflæði með því að skrá viðkomandi skref í línurnar. Hvert skref samanstendur af atburði verkflæðis, breytt eftir atburður skilyrði, og verkflæðissvar, breytt eftir svarvalkostir. Þú skilgreinir skref í verkflæði með því að fylla út í reiti á verkflæðislínum úr föstum listum yfir tilvik og svör gildi sem standa fyrir verkflæðissviðsmyndir sem eru studd af kóða forritsins.  

[!INCLUDE[workflow](includes/workflow.md)]

Eftirfarandi tafla lýsir röð verkefna með tenglum í greinar þar sem þeim er lýst.  

|**Til að**|**Sjá**|  
|------------|-------------|  
|Setja upp notendur og notendahópa verkflæðis.|[Setja upp notendur verkflæðis](across-how-to-set-up-workflow-users.md)|  
|Setja upp notendur verkflæðis sem taka þátt í samþykktarverkflæði.|[Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md)|  
|Tilgreinið hvernig notendum verkflæðis er tilkynnt um skref verkflæðis, þ.m.t. samþykktarbeiðnir.|[Setja upp tilkynningar verkflæðis](across-setting-up-workflow-notifications.md)|  
|Tilgreina hvort notendur fái tilkynningu með tölvupósti eða athugasemd og hversu oft tilkynningar eru sendar.|[Tilgreina hvenær og hvernig á að fá tilkynningar](across-how-to-specify-when-and-how-to-receive-notifications.md)|  
|Aðlaga skal efni tilkynningar í tölvupósti með því að breyta skýrslu 1320, netfang tilkynningar.|[Búa til og breyta sérsniðnum skýrsluútlitum](ui-how-create-custom-report-layout.md)|  
|Uppsetning SMTP-netþjóns til að virkja tölvupóstssamskipti inn og út af [!INCLUDE[prod_short](includes/prod_short.md)].|[Setja upp tölvupóst](admin-how-setup-email.md)|
|Tilgreinið mismunandi skref verkflæðis með því að tengjast verkflæðistilvikum með verkflæðisviðbrögðum.|[Búa til verkflæði](across-how-to-create-workflows.md)|  
|Nota verkflæðissniðmát til að stofna ný verkflæði.|[Búa til verkflæði úr verkflæðissniðmátum](across-how-to-create-workflows-from-workflow-templates.md)|  
|Deila verkflæði með öðrum [!INCLUDE[prod_short](includes/prod_short.md)] gagnagrunnum.|[Flytja verkflæði inn og út](across-how-to-export-and-import-workflows.md)|  
|Lærið að setja upp verkflæði fyrir söluskjöl sem eru til samþykktar með því að fylgja verkferli frá upphafi til enda.|[Kynning: Uppsetning og notkun á samþykktarverkflæði innkaupa](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)|  

## <a name="example-of-an-approval-workflow"></a>Dæmi um verkflæði samþykkis

Þetta myndband sýnir hvernig verkflæði er sett upp sem gerir notanda kleift að biðja einhvern annan um samþykki áður en hægt er að breyta upplýsingum um viðskiptamann sem fyrir er eða stofna nýjan viðskiptavin.  
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4jzHI?rel=0]

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/create-workflows/)

## <a name="see-also"></a>Sjá einnig .

[Nota verkflæði](across-use-workflows.md)  
[Verkflæði](across-workflow.md)  
[Kynning: Uppsetning og notkun á samþykktarverkflæði innkaupa](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Vinna með Viðskiptaseðla-](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
