---
title: Setja upp Verkflæði samþykktar (inniheldur myndskeið)
description: 'Settu upp verkflæði, notendur verkflæðis og samþykkjendur til að tengja kerfisverk viðskiptaferlis sem þessi notendur framkvæma.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/13/2022
ms.author: bholtorf
---
# <a name="set-up-approval-workflows"></a>Setja upp Verkflæði samþykktar

Hægt er að setja upp og nota verkflæði sem tengja viðskiptaferlisverk sem framkvæmd erf af ólíkum notandi. Kerfisverk, s.s. sjálfvirk bókun, er hægt að hafa sem skerf í verkflæði, á undan eða eftir notandaverkum. Að óska eftir samþykki eða samþykkja nýjar færslur eru dæmigerð skref í verkflæði. Frekari upplýsingar má finna á [Nota Samþykktarverkflæði](across-use-workflows.md).

Áður en byrjað er að nota samþykktarverkflæði verður að setja upp notendur verkflæðis og samþykktarnotendur, tilgreina hvernig notendur fá tilkynningar um skref verkflæðis og stofna svo verkflæðin.

Á síðunni **Verkflæði** er hægt að stofna verkflæði með því að skrá viðkomandi skref í línurnar. Hvert skref samanstendur af atburði verkflæðis, breytt eftir atburður skilyrði, og verkflæðissvar, breytt eftir svarvalkostir. Þú skilgreinir verkflæðisskref með því að fylla út í reiti í verkflæðislínum úr föstum listum yfir gildi tilvika og svara sem standa fyrir verkflæðissviðsmyndir sem kóði forritsins styður.

[!INCLUDE[workflow](includes/workflow.md)]

Eftirfarandi tafla lýsir röð verkefna með tenglum í greinar þar sem þeim er lýst.

|**Til að**|**Sjá**|  
|------------|-------------|  
|Setja upp notendur og notendahópa verkflæðis.|[Setja upp notendur verkflæðis](across-how-to-set-up-workflow-users.md)|  
|Setja upp notendur verkflæðis sem taka þátt í samþykktarverkflæði.|[Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md)|  
|Tilgreinið hvernig notendum verkflæðis er tilkynnt um skref verkflæðis, þ.m.t. samþykktarbeiðnir.|[Setja upp tilkynningar verkflæðis](across-setting-up-workflow-notifications.md)|  
|Tilgreina hvort notendur fái tilkynningu með tölvupósti eða athugasemd og hversu oft tilkynningar eru sendar.|[Tilgreina hvenær og hvernig á að fá tilkynningar](across-how-to-specify-when-and-how-to-receive-notifications.md)|  
|Sérsníða innihald á tilkynningu tölvupósts með því að breyta skýrslu 1320, Tilkynningapóstur.|[Búa til og breyta sérsniðnum skýrsluútlitum](ui-how-create-custom-report-layout.md)|  
|Uppsetning SMTP-netþjóns til að virkja tölvupóstssamskipti inn og út af [!INCLUDE[prod_short](includes/prod_short.md)].|[Setja upp tölvupóst](admin-how-setup-email.md)|
|Tilgreina ólík skref verkflæðis eftir tengdum verkflæðistilvikum með verkflæðisviðbrögðum.|[Stofna verkflæði samþykktar](across-how-to-create-workflows.md)|  
|Nota verkflæðissniðmát til að stofna ný verkflæði.|[Stofna samþykktarverkflæði úr verkflæðissniðmáti](across-how-to-create-workflows-from-workflow-templates.md)|  
|Deila verkflæði með öðrum [!INCLUDE[prod_short](includes/prod_short.md)] gagnagrunnum.|[Flytja samþykktarverkflæði inn og út](across-how-to-export-and-import-workflows.md)|  
|Lærið að setja upp verkflæði fyrir söluskjöl sem eru til samþykktar með því að fylgja verkferli frá upphafi til enda.|[Kynning: Uppsetning og notkun á samþykktarverkflæði innkaupa](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)|  

## <a name="example-of-an-approval-workflow"></a>Dæmi um samþykktarverkflæði

Þetta myndband sýnir hvernig á að setja upp verkflæði sem fer fram á að notandi óski eftir samþykki einhvers annars áður en hægt er að breyta upplýsingum um fyrirliggjandi viðskiptamann, eða búa til nýjan viðskiptamann.  
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4jzHI?rel=0]

## <a name="see-also"></a>Sjá einnig .

[Nota Samþykktarverkflæði](across-use-workflows.md)  
[Verkflæði](across-workflow.md)  
[Kynning: Uppsetning og notkun á samþykktarverkflæði innkaupa](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Vinna með Business Central](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
