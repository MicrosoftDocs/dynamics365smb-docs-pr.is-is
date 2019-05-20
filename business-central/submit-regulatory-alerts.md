---
title: Senda inn lögboðnar viðvaranir | Microsoft Docs
description: Ef þú veist um nýja löggjöf sem þú telur að þurfi stuðning eiginleika í Business Central, getur þú fylgst með þessum leiðarvísi til að senda lögboðna viðvörun til framleiðsluteymis.
author: sorenfriisalexandersen
ms.service: dynamics365-business-central
ms.topic: article
ms.reviewer: edupont
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: soalex
ms.openlocfilehash: d4ceef0780306015795c0a2406245514c2a26de5
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1250320"
---
# <a name="submit-alerts-about-countryregion-specific-regulatory-features"></a>Sendu inn viðvaranir um eftirlitseiginleika sem miðast við tiltekið land/svæði

Við bjóðum þér að nota Microsoft Dynamics Lifecycle Services (LCS) til að leggja fram lögboðnar viðvaranir í gegnum innsendingarþjónustu á lögboðnum viðvörunum í Dynamics.  

## <a name="to-submit-a-regulatory-alert-in-lcs"></a>Innsending lögboðinnar viðvörunar í LCS

1. Farðu í https://lcs.dynamics.com og skráðu þig inn. Þú færð að sjá verkin sem þú hefur aðgang að

2. Veldu verkið **Lögboðnar viðvaranir - um allan heim**. Þetta opnar verkið og sýnir ýmislegt sem tengist þessu verki

3. Veldu **Viðvörunarþjónusta** hægra megin í hlutanum **Fleiri verkfæri**. Þar sérðu lista yfir viðvaranir með fyrirsögninni **Innsending á lögboðnum viðvörunum Dynamics**

4. Þú getur bætt við nýrri viðvörun með því að smella á plústáknið **(+)** sem er efst á listanum. Þá birtast þér leiðbeiningar í fjórum skrefum um hvernig skuli búa til viðvörun. Leiðbeiningin samanstendur af eftirfarandi skrefum:
    - Leita að fyrirliggjandi vörum

        Leitaðu að upplýsingum sem þú telur að skipti máli fyrir viðvörunina sem þú ætlar að búa til. Ef þú finnur ekki viðeigandi leitarniðurstöður geturðu valið hnappinn **Senda inn lögboðna viðvörun** neðst á síðunni til að halda áfram með innsendingu á viðvörun.
    - Hengja viðskiptaferla við

        Þessi hluti skiptir ekki máli fyrir Dynamics 365 Business Central. Veldu **Sleppa** til að fara í næsta skref.
    - Lýsið viðvöruninni

        Færðu inn upplýsingar um viðvörunina í viðeigandi reiti. Rauð stjarna (\*) auðkennir alla áskilda reiti í leiðbeiningunni.

        |Svæði        |Description                               |
        |-------------|------------------------------------------|
        |Titill  | Færðu inn lýsandi titil til að gefa til kynna um hvað málið snýst. Færðu til dæmis inn *Breytingar á reikningsskjali frá og með 1. júlí 2019*. |
        |Description  | Færðu inn stutta samantekt á lögunum. Lýsingin ætti að vera um vandamál sem tengjast skipulagsáætlun fyrirtækisins (ERP) svo notandinn geti almennilega skilið kröfurnar án þess að þurfa að lesa reglugerðina fyrst.|
        |Land  | Tilgreindu landið eða svæðið sem reglugerðin nær yfir.|
        |Iðnaður| Tilgreindu atvinnugreinina ef krafan á aðeins við um tilteknar atvinnugreinar. Veldu til dæmis **Opinberi geirinn**, **Smásala** eða **Framleiðsla**.|
        |Tilvísun eiginleika  | Þetta skiptir ekki máli fyrir Dynamics 365 Business Central, en þú getur slegið inn tilvísun eiginleika ef þú þekkir hana. Listi yfir eiginleika fyrir tiltekið land er hægt að finna í [Staðfærslugátt](https://mbs.microsoft.com/customersource/global/ax/support/support-news/GFMLocalizationPortalMC). |
        |Dagsetning þegar lög taka gildi  | Tilgreindu dagsetninguna þegar viðskiptavinir verða að fylgja lögunum.|
        |Dagsetning tilkynningar frá yfirvöldum  | Tilgreindu dagsetningu þegar yfirvöld tilkynntu breytinguna.|
        |Síðasta innlagningardagsetning  | Veldu tímamörk fyrir fyrstu innsendingu á nýju eða breyttu skýrslunni.|
        |Tengill á löggjöf  | Sláðu inn einn eða fleiri tengla á birtu lögin, túlkunarreglur, leiðbeiningar um innleiðingu eða önnur gagnleg skjöl sem auðvelda notendum að skilja eða innleiða kröfuna.|
        |Heiti fyrirtækis  | Færðu inn heiti fyrirtækis fyrir einstaklinginn sem sendir inn viðvörunina.|
        |Nafn tengiliðar  | Færðu inn nafn einstaklingsins sem sendir inn skýrsluna. |
        |Netfang tengiliðar  | Netfang einstaklingsins sem sendir inn viðvörunina.|
        |Viðskiptaferli  | Viðskiptaferlið sem þú valdir í gegnum leiðsagnarforritið **Innsending viðvörunar**|
        |Athugasemdir  | Færðu inn viðbótarupplýsingar sem gætu hjálpað notendum að skilja eða innleiða kröfuna. Smelltu á **Senda inn** til að vista athugasemd. Bæta má við mörgum athugasemdum og þær skal senda inn aðskildar. Athugasemdir eru vistaðar í þeirri röð sem þær eru sendar. |
        |Ég vil sjá ...  | Smelltu á hnappinn **Hlaða upp** og flettu síðan til að velja skrá sem skal bæta við sem viðhengi. Eftir að þú hefur valið skrána er henni hlaðið upp og birtist sem tengd skrá. Þú getur bætt við allt að þremur skrám sem eru að hámarki 5 MB hver. Til að eyða skrám sem hafa verið hengdar við skal smella á **Fjarlægja** undir fyrirsögn skráarinnar. Viðhengi verður að vera efni sem er opið almenningi. Þau geta ekki verið viðskiptavinamiðuð eða samstarfsaðilamiðuð.|

        Smelltu á **Senda inn** til að vista og senda inn viðvörunina.

        Ef þú ert ekki með allar nauðsynlegar upplýsingar, eða ert ekki enn tilbúin/n til að senda inn viðvörunina, geturðu vistað viðvörun sem er aðeins lokið að hluta til.

    - Staðfesting á sendingu

      Eftir að þú hefur sent viðvörunina færðu staðfestingu á að viðvörunin hafi verið send inn til Microsoft.

## <a name="see-also"></a>Sjá einnig

[Velkomin(n) í Business Central](index.md)  
[Hafist handa](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
