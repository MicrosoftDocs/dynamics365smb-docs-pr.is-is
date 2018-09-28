---
title: "Setja upp SEPA kreditfærsla | Microsoft Docs"
description: "Kynntu þér hvernig á að setja upp SEPA-kreditfærslur í Business Central."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sepa, credit, transfer, payment,
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 64abd01caa2a2f6845bb3d54c7721333a0a360b3
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-sepa-credit-transfer"></a>Setja upp SEPA-kreditfærslur
Frá glugganum **Greiðslubók** er hægt að flytja út greiðslur í skrá til upphals í netbanka til vinnslu á tengdum peningamillifærslum. [!INCLUDE[d365fin](includes/d365fin_md.md)] styður SEPA-kreditfærslusniðið, en í heimalandi þínu / svæði geta önnur snið fyrir rafrænar greiðslur kunna að vera tiltækir.  

Til að opna fyrir útflutning af skráasniði bankaskrár sem ekki eru studdar af [!INCLUDE[d365fin](includes/d365fin_md.md)] er hægt að setja upp gagnaskiptaskilgreiningu með því að nota gagnaskiptaumgjörð. Frekari upplýsingar er að finna í [Setja upp skilgreiningar gagnaskipta](across-how-to-set-up-data-exchange-definitions.md).  

Áður en þú getur afgreitt greiðslu rafrænt með því að flytja greiðsluskrár í SEPA-kreditfærslusnið, verður þú að framkvæma eftirfarandi uppsetningarskref:  

* Setja upp viðkomandi bankareikning til að meðhöndla SEPA-kreditfærslusnið.  
* Setja upp lánardrottinn spjöld með því að flytja skrár úr í SEPA-kreditmillifærslur sniði.  
* Setja upp viðeigandi bókarkeyrslu til að gera virkan útflutning greiðslu úr **greiðslubók** glugga.  
* Tengja gagnaskiptaskilgreiningu fyrir eina eða fleiri greiðslugerðir með viðeigandi greiðslumáta.  

### <a name="to-set-up-a-bank-account-for-sepa-credit-transfer"></a>Að setja upp bankareikning fyrir SEPA-kreditfærslu  
1. Í reitinn **Leita** skal færa inn **Bankareikningar** og velja síðan viðkomandi tengi.  
2. Opnið spjald bankareikningsins sem á að flytja greiðsluskrár úr á SEPA-kreditfærslusniði.  
3. Á flýtiflipanum **Millifærsla**, í reitnum **Útflutningssvið greiðslu** skal velja **SEPADD**.  
4. Í **SEPA Kreditfærsla skilaboð kenni númeraröð** reitnum skal velja númeraröð sem tölum eru úthlutað úr til SEPA-kreditfærslu.  
5. Gangið úr skugga um að reiturinn **IBAN** sé útfylltur.  

    > [!NOTE]  
    >  Reiturinn **Gjaldmiðilskóði** verður að vera stilltur á **EUR**, því SEPA-kreditmillifærslur er aðeins hægt að gera í evrum.  

### <a name="to-set-up-a-vendor-card-for-sepa-credit-transfer"></a>Að setja upp lánardrottin fyrir SEPA-kreditfærslu  
1. Í reitnum **Leita** skal færa inn **Lánardrottnar** og velja síðan viðkomandi tengi.  
2. Opnið spjald lánardrottins sem á að greiða til rafrænt útflutningi greiðsluskráa á SEPA-kreditfærslusniði.  
3. Á flýtiflipanum **Greiðsla**, í reitnum **Kóði greiðslumáta** skal velja **BANKI**.  
4. Í **Valinn bankareikningur** reitnum, veldu banka sem fé verður flutt inn á þegar það er unnið með rafrænum bankann þinn.  

     Gildið í reitnum **Valinn bankareikningur** er afritað í reitinn **Móttökubankareikningur** í **Greiðslubók** glugganum.  

### <a name="to-set-the-payment-journal-up-to-export-payment-files"></a>Að stilla greiðslubók upp til að flytja greiðsluskrár  
1. Í reitnum **Leit** skal færa inn **Greiðslubækur** og velja síðan viðkomandi tengil.  
2. Opnið greiðslubókina sem á að nota til vinna greiðslur með því að flytja skrár á SEPA-kreditfærslusniði.  
3. Í reitnum **Heiti keyrslu** er felli\-lista hnappurinn valinn.  
4. Í glugganum **Færslubókarkeyrslur** á flipanum **Heim**, í flokknum **Stjórna**, skal velja **Breyta lista**.  
5. Á línunni fyrir greiðslubókina sem notuð verður til að flytja út greiðslur skal velja gátreitinn **Leyfa greiðsluútflutning**.  

### <a name="to-connect-the-data-exchange-definition-for-one-or-more-payment-types-with-the-relevant-payment-method-or-methods"></a>Tengja gagnaskiptaskilgreiningu fyrir eina eða fleiri greiðslugerðir með viðeigandi greiðslumáta.  
1. Í reitnum **Leit** skal færa inn **Greiðsluhættir** og velja síðan viðkomandi tengil.  
2. Í **Greiðslumáti** glugganum skaltu velja greiðslumáta sem er notað til að flytja út greiðslur frá, og þá velja **Greiðsluútflutningur Línuskilgreining** reitinn.  
3. Í **Greiðsluútflutningur Línuskilgreining** glugganum skal velja kóðann sem var tilgreindur í **Kóði** reitnum á **Línuskilgreiningar** flýtiflipanum í skrefi 4 í „Að lýsa sniði lína og dálka í skránni“ hlutanum í [Setja upp gagnaskiptaskilgreiningar](across-how-to-set-up-data-exchange-definitions.md) aðgerðinni.  

    Umboðið fyrir beingreiðslur er sjálfkrafa sett inn í **Kenni umboðs fyrir beint debet** reitinn þegar sölureikningur er stofnaður fyrir viðskiptamann sem var valinn í skrefi 2. Nánari upplýsingar er að finna í [Stofna ítrekaðar sölu og innkaupalínur](sales-how-work-standard-lines.md).  

## <a name="see-also"></a>Sjá einnig  
[Innheimta greiðslur með SEPA-beingreiðslum](finance-collect-payments-with-sepa-direct-debit.md)  
[Setja upp skilgreiningar gagnaskipta](across-how-to-set-up-data-exchange-definitions.md)  
[Stofna ítrekaðar sölu- og innkaupalínur](sales-how-work-standard-lines.md)  
[Rafræn gagnaskipti](across-data-exchange.md)  

