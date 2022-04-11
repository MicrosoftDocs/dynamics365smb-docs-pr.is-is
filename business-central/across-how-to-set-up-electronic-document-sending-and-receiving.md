---
title: 'Hvernig á að: Setja upp sendingu og móttöku rafrænna skjala | Microsoft Docs'
description: Annar valkostur við að senda skrár sem viðhengi í tölvupósti er að senda og taka á móti viðskiptaskjölum á rafrænan hátt.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: bcc706a221c40019792167b4b75cb8826216457d
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2022
ms.locfileid: "8147217"
---
# <a name="set-up-electronic-document-sending-and-receiving"></a>Setja upp sendingu og móttöku rafrænna skjala

Annar valkostur við að senda skrár sem viðhengi í tölvupósti er að senda og taka á móti viðskiptaskjölum á rafrænan hátt. Með rafrænu skjali er átt við staðlaða og \-samþykkta skrá sem stendur fyrir skrárfærslu, s.s. sölureikning sem hægt er að taka á móti og umbreyta í innkaupareikning í [!INCLUDE[prod_short](includes/prod_short.md)]. Skipti rafrænna skjala á milli tveggja viðskiptafélaga er framkvæmd af ytri veitanda skjalaskiptaþjónustu. Almenn útgáfa [!INCLUDE[prod_short](includes/prod_short.md)] styður sendingu og móttöku rafrænna reikninga og kreditreikninga á PEPPOL-sniði, sem er stutt af stærstu skjalaskiptaþjónustukerfunum. Stór þjónustuveitandi skjalaskiptaþjónustu er forstilltur og tilbúinn til uppsetningar fyrir fyrirtækið.  

Úr PDF-skjölum eða myndaskrám sem standa fyrir skjöl á innleið er hægt að láta ytri OCR-þjónustu (sjónræn stafakennsl) stofna rafræn skjöl sem hægt er að umbreyta í skráarfærslur í [!INCLUDE[prod_short](includes/prod_short.md)], rétt eins og með rafræn PEPPOL-skjöl. Þegar reikningur berst frá lánardrottni á PDF-sniði er til dæmis hægt að senda hann til OCR-þjónustu af síðunni **Skjöl á innleið**. Eftir nokkrar sekúndur berst skráin aftur sem rafrænn reikningur sem hægt er að breyta í innkaupareikning fyrir lánardrottin. Ef skráin er send í OCR-þjónustu með tölvupósti er ný færsla fyrir skjal á innleið sjálfkrafa stofnum þegar tekið er aftur á móti rafræna skjalinu.  

The **PEPPOL** rafræna skjal snið er forstillt þannig að gera þér kleift að senda rafræna reikninga og trúnaður minnisblöð í PEPPOL sniði. Fyrst þarf að setja upp mismunandi aðalgögn, t.d. upplýsingar um fyrirtækið, viðskiptavini, atriði, og mælieiningar. Þau eru notuð til að bera kennsl á viðskiptafélaga og atriði þegar gögnum er umbreytt í reiti í [!INCLUDE[prod_short](includes/prod_short.md)] í einingar í skjalaskrá á útleið. Að lokum verður að velja snið á síðunni **Rafrænt snið skjals** fyrir hvern viðskiptamann sem á að senda rafræn PEPPOL-skjöl til. Nánari upplýsingar sjá [Senda rafræn skjöl](sales-how-to-send-electronic-documents.md).  

**PEPPOL – Reikningur** og **PEPPOL – Kreditreikningur** gagnaskiptaskilgreiningar eru forstilltar til að leyfa þér að taka við rafrænum reikningum og kreditreikningum á PEPPOL-sniði. Fyrst þarf að setja upp mismunandi aðalgögn, t.d. upplýsingar um fyrirtækið, lánardrottna, atriði, og mælieiningar. Þau eru notuð til að bera kennsl á viðskiptafélaga og atriði þegar gögnum er umbreytt í reiti í [!INCLUDE[prod_short](includes/prod_short.md)] í einingar í skjalaskrá á innleið. Að lokum verður að velja gagnaskiptaskilgreiningu á síðunni **Skjöl á innleið** fyrir hvert rafrænt skjal á innleið sem á að umbreyta í innkaupaskjal í [!INCLUDE[prod_short](includes/prod_short.md)].  

**OCR – reikningur** gagnaskiptaskilgreining er forstillt til að leyfa þér að fá rafræn skjöl sem eru mynduð í stafakennslaþjónustu. Til að taka við, til dæmis, reikningi sem á rafræns OCR-skjals eru sett upp aðaldagsetning og síðan er skjalið meðhöndlað líkt og þegar rafrænt PEPPOL-skjal er móttekið. Frekari upplýsingar eru í [Hvernig á að nota OCR til að breyta PDF og myndaskrám í rafræn skjöl](across-how-use-ocr-pdf-images-files.md).  

Forstillt þjónusta fyrir skjalaskipti og OCR verður að vera virkt fyrir sendingu eða móttöku. Frekari upplýsingar, sjá [Setja upp skjalaskiptaþjónustu](across-how-to-set-up-a-document-exchange-service.md).  

Þetta efnisatriði inniheldur eftirfarandi ferli:  

* Til að setja upp fyrirtæki til að senda rafræna skjal og fá  
* Til að setja upp fyrirtæki til að senda rafræna skjal og fá  
* Til að setja upp fyrirtæki til að senda rafræna skjal og fá  
* Til að setja upp fyrirtæki til að senda rafræna skjal og fá  
* Til að setja upp mælieiningar til að senda rafræna skjal og fá  
* Til að setja upp viðskiptavini fyrir rafræna skjal senda  
* Til að velja **PEPPOL** rafræn skjal snið fyrir rafræna skjal sendiríkisins  
* Til að setja upp viðskiptavini fyrir rafræna skjal senda  
* Til að velja **PEPPOL-Invoice** gögn skipti skýring fyrir rafræna skjal móttöku  
* Til að setja upp G / L reikninginn til að nota á nýjum innkaupareikninguslínum fyrir \-ógreinanlegt atriði og aðra hluti\-  

### <a name="to-set-up-the-company-for-electronic-document-sending-and-receiving"></a>Til að setja upp fyrirtæki til að senda rafræna skjal og fá

1. Í reitinn **Leita** skal færa inn **Stofngögn** og velja síðan viðkomandi tengi.  
2. Á flýtiflipanum **Almennt** þarf að fylla reitina út eins og lýst er í eftirfarandi töflu.  

    |Svæði|Description|  
    |---------------------------------|---------------------------------------|  
    |**GLN**|Auðkennið fyrirtækið.<br /><br /> Til dæmis, þegar þú sendir rafræna reikninga í PEPPOL sniði, gildi á þessu sviði er notað til að byggja á **EndPointID** einingu undir **AccountingSupplierParty** hnút í skránni. Talan er byggt á GS1 staðall, sem er í samræmi við ISO 6523.|  
    |**VSK-númer**|Tilgreinið VSK-númer fyrirtækisins.|  
    |**Ábyrgðarstöð**|Ef fyrirtækið er settur upp með ábyrgðarstöð skal tryggja að reiturinn **Lands-/svæðiskóði** sé fylltur út.|  

### <a name="to-set-up-vat-posting-for-electronic-document-sending-and-receiving"></a>Til að setja upp fyrirtæki til að senda rafræna skjal og fá

1. Í reitinum **Leit** skal færa inn **VSK-bókunargrunn** og velja síðan viðkomandi tengil.  
2. Fyrir hverja VSK staða skipulag línu sem þú munt nota til rafrænna skjala, fylla á sviði eins og lýst er í eftirfarandi töflu.  

    |Svæði|Description|  
    |---------------------------------|---------------------------------------|  
    |**Skattaflokkur**|Tilgreina VSK flokk.<br /><br /> Til dæmis, þegar þú sendir rafræna reikninga í PEPPOL sniði, gildi á þessu sviði er notað til að byggja á **TaxApplied** frumefni undir **AccountingSupplierParty** hnút í skránni. Talan er byggt á UNCL5305 staðall.|  

### <a name="to-set-up-countriesregions-for-electronic-document-sending-and-receiving"></a>Til að setja upp fyrirtæki til að senda rafræna skjal og fá

1. Í reitnum **Leit** skal færa inn **Kostnaðarúthlutanir** og velja síðan viðkomandi tengil.  
2. Fyrir hverja VSK staða skipulag línu sem þú munt nota til rafrænna skjala, fylla á sviði eins og lýst er í eftirfarandi töflu.  

    |Svæði|Description|  
    |---------------------------------|---------------------------------------|  
    |**VSK-skema**|Auðkennir innlendan aðila sem gefur út VSK-númer fyrir land\/svæði í tengslum við sendingu rafræns skjals.<br /><br /> Til dæmis, þegar þú sendir rafræna reikninga í PEPPOL sniði, gildi á þessu sviði er notað til að byggja á **SchemeID** eigind fyrir **EndPointID** einingu undir bæði **AccountingSupplierParty** hnúði og **AccountingCustomerParty** í skránni.<br /><br /> Reitur **VSK-skema** er aðeins notaður ef **GLN** reitur á síðunni **Stofngögn** er ekki fylltur út. **Athugið:** Gildið í reitnum **Kóði** í **Lönd\/Svæði** síðunni verða að vera í samræmi við ISO 3166\-1:Alpha2.|  

### <a name="to-set-up-items-for-electronic-document-sending-and-receiving"></a>Til að setja upp fyrirtæki til að senda rafræna skjal og fá

1. Í reitnum **Leita** skal færa inn **Vörur** og velja síðan viðkomandi tengi.  
2. Fylla inn í reitinn eins og lýst er í eftirfarandi töflu fyrir hverja vöru sem er keypt eða seld í rafrænum skjölum.  

    |Svæði|Description|  
    |---------------------------------|---------------------------------------|  
    |**GTIN**|Auðkennir vöru sem tengist sendingu eða móttöku rafrænt skjal. Fyrir PEPPOL snið, er svæðið notað sem hér segir:<br /><br /> Ef **StandardItemIdentification\/ID** einingin er með **SchemeID** eigind stillta á **GTIN** þá er einingunni varpað á reitinn **GTIN** reitinn á vöruspjaldinu.|  

### <a name="to-set-up-units-of-measure-for-electronic-document-sending-and-receiving"></a>Til að setja upp mælieiningar til að senda rafræna skjal og fá

1. Í reitnum **Leit** skal færa inn **Birgðahaldseining** og velja síðan viðkomandi tengil.  
2. Fyrir hverja VSK staða skipulag línu sem þú munt nota til rafrænna skjala, fylla á sviði eins og lýst er í eftirfarandi töflu.  

    |Svæði|Description|  
    |---------------------------------|---------------------------------------|  
    |**Alþjóðlegur staðlakóði**|Tilgreina mælieiningu kóða tjáð samkvæmt UNECERec20 staðall í tengslum við sendingu rafrænna skjala.<br /><br /> Til dæmis, þegar þú sendir rafræna reikninga í PEPPOL sniði, gildi á þessu sviði er notað til að byggja á **unitCode** eigindi á **InvoicedQuantity** frumefni undir **InvoiceLine** hnút. **Athugið:** Ef reiturinn **Mælieining** í sölulína er auður er staðlað gildi UNECERe20 fyrir „Stykki“ \(H87\) sett inn sjálfgefið. Frekari upplýsingar og skrá yfir fullnægjandi mælieiningarkóði er að finna í [Tilmæli nr. 20 \- Mælieiningar sem notaðar eru í alþjóðaviðskiptum](https://www.unece.org/fileadmin/DAM/cefact/recommendations/rec20/rec20_rev3_Annex2e.pdf).|  

### <a name="to-set-up-customers-for-electronic-document-sending"></a>Til að setja upp viðskiptavini fyrir rafræna skjal senda

1. Í reitinn **Leita** skal færa inn **Viðskiptamenn** og velja síðan viðkomandi tengi.  
2. Fyrir hvern viðskiptamann sem rafræn skjöl eru send til skal fylla inn í reitina eins og lýst er í eftirfarandi töflu.  

    |Svæði|Description|  
    |---------------------------------|---------------------------------------|  
    |**GLN**|Auðkennið viðskiptamanninn.<br /><br /> Sem dæmi má nefna að þegar sendir eru rafrænir reikningur í PEPPOL-sniði er gildið í þessum reit notað til að fylla út í talnaeininguna **EndPointID** undir hnútnum **AccountingCustomerParty** í skránni. Talan er byggt á GS1 staðall, sem er í samræmi við ISO 6523.<br /><br /> Ef **GLN** reiturinn er auður er gildið í reitnum **VSK-númer** notað.|  
    |**VSK-númer**|Tilgreinið VSK-skráningarnúmer viðskiptamannsins. **Ábending:** Í studdum staðfærðum útgáfum skal velja köfunarhnappinn til að nota vefþjónustu sem staðfestir hvort númerið sé til í fyrirtækjaskrá landsins.|  
    |**Ábyrgðarstöð**|Ef viðskiptamaður er settur upp með ábyrgðarstöð skal tryggja að reiturinn **Lands-/svæðiskóði** sé fylltur út.|  

    Hægt er að setja hvern viðskiptamaður upp með valinni aðferð við að senda viðskiptaskjöl til að þurfa ekki að velja sendingarvalkost í hvert skipti sem viðskiptamanni eru send skjöl. Frekari upplýsingar er að finna á [Setja upp sendisnið skjala](sales-how-setup-document-send-profiles.md).  

### <a name="to-select-the-peppol-electronic-document-format-for-electronic-document-sending"></a>Til að velja PEPPOL-snið fyrir rafræn skjöl við sendingu rafrænna skjala  
1. Í reitnum **Leita** skal færa inn **Sendingarsnið skjala** og velja síðan viðkomandi tengil.  
2. Opna forstillingu fyrir sendingu skjala sem þegar er til eða stofna nýja. Frekari upplýsingar er að finna á [Setja upp sendisnið skjala](sales-how-setup-document-send-profiles.md).  
3. Á síðunni **Forstilling skjalasendingar** skal velja **Rafrænt snið**, línu fyrir PEPPOL og velja síðan hnappinn **Í lagi**.  
4. Í reitnum **Rafrænt skjal** skal velja **Já (í gegnum skjalaskiptaþjónusta)**.  

    > [!NOTE]  
    >  [!INCLUDE[prod_short](includes/prod_short.md)] greinir sjálfkrafa hvort skjalið er reikningur eða kreditreikningur og beitir PEPPOL-sniði samkvæmt því.  

5. Til að nota þessa forstillingu sendingar á skjölum fyrir alla viðskiptamenn skal velja gátreit **Sjálfgefið** á flýtiflipanum **Almennt**. Til að nota það aðeins fyrir tiltekna viðskiptamenn skal fylla út í reitinn **Forstilling skjalasendingar** á viðkomandi viðskiptamannaspjaldi. Frekari upplýsingar er að finna á [Setja upp sendisnið skjala](sales-how-setup-document-send-profiles.md).  

    Núna er hægt að senda rafrænt skjal sem inniheldur umbreyttu gögnin. Nánari upplýsingar sjá [Senda rafræn skjöl](sales-how-to-send-electronic-documents.md).  

### <a name="to-set-up-vendors-for-electronic-document-receiving"></a>Til að setja upp viðskiptavini fyrir rafræna skjal senda  
1. Í reitnum **Leita** skal færa inn **Lánardrottnar** og velja síðan viðkomandi tengi.  
2. Fyrir hvern lánardrottin sem sendir rafræn skjöl skal fylla inn í reitina eins og lýst er í eftirfarandi töflu.  

    |Svæði|Description|  
    |---------------------------------|---------------------------------------|  
    |**GLN**|Auðkennið lánardrottin.<br /><br /> Sem dæmi má nefna að þegar mótteknir eru rafrænir reikningar í PEPPOL-sniði er gildið í þessum reit notað til að fylla út í talnaeininguna **EndPointID** undir hnútnum **AccountingSupplierParty** í skránni. Talan er byggt á GS1 staðall, sem er í samræmi við ISO 6523.<br /><br /> Ef **GLN** reiturinn er auður er gildið í reitnum **VSK-númer** notað.|  
    |**VSK-númer**|Tilgreinið VSK-númer lánardrottins. **Ábending:** Í studdum staðfærðum útgáfum skal velja köfunarhnappinn til að nota vefþjónustu sem staðfestir hvort númerið sé til í fyrirtækjaskrá landsins.|  
    |**Ábyrgðarstöð**|Ef lánardrottinn er settur upp með ábyrgðarstöð skal tryggja að reiturinn **Lands-/svæðiskóði** sé fylltur út.|  

### <a name="to-select-the-peppol---invoice-data-exchange-definition-for-electronic-document-receiving"></a>Til að velja PEPPOL-gagnaskiptaskilgreiningu við móttöku rafrænna skjala  
1. Í reitnum **Leit** skal færa inn **Fylgiskjöl á innleið** og velja síðan viðkomandi tengil.  
2. Í línu fyrir rafrænt skjal sem á að taka á móti og umbreyta skal velja reitinn **Gagnaskipti** og velja síðan **PEPPOLINVOICE**.  

     Ef skjalið sem á að taka við er kreditreikningur er valið **PEPPOLCREDITMEMO**.  

    Nú er hægt að taka á móti rafrænu skjali með því að hefja umbreytingarferli gagna á síðunni **Skjöl á innleið**. Frekari upplýsingar, sjá [Taka við og umbreyta rafrænum skjölum](purchasing-how-to-receive-and-convert-electronic-documents.md).  

### <a name="to-set-up-the-gl-account-to-use-on-new-purchase-invoice-lines-for-non-identifiable-items-and-non-items"></a>Til að setja upp G / L reikning til að nota á nýjum línum kaup reikningi fyrir utan aðgreinanlegra atriði og erlendra liða  
1. Í reitnum **Leit** skal færa inn **Innkaup & Útistandandi** og velja síðan viðkomandi tengil.  
2. Á síðunni **Sjálfgefnir lyklar** skal fylla inn í reitina eins og lýst er í eftirfarandi töflu.  

    |Svæði|Description|  
    |---------------------------------|---------------------------------------|  
    |**Fjárhagsreikningur fyrir línur sem eru ekki vörulínur**|Tilgreinir fjárhagsreikning sem er sjálfkrafa settur inn í innkaupalínu sem eru stofnaðar úr rafrænum skjölum þegar skjalalína skjals á innleið inniheldur ekki auðkennanlegt atriði. Allar línur skjala á innleið sem hafa ekki GTIN eða vörunúmer lánardrottins verður breytt í innkaupalína af gerðinni **Fjárhagsreikningur** og **Nr.** reiturinn í innkaupalínunni mun innihalda reikning sem valinn var í reitnum **Fjárhagsreikningur fyrir línur sem eru ekki vörulínur**.<br /><br /> Ef reiturinn **Fjárhagsreikningur fyrir línur sem eru ekki vörulínur** er hafður auður og skjal á innleið hefur línur án auðkennanlegra atriða verður innkaupaskjal ekki stofnað. Villuboð munu óska eftir því að fyllt sé í reitinn **Fjárhagsreikningur fyrir línur sem eru ekki vörulínur** áður en hægt er að ljúka verkinu.|  

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/electronic-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig  
[Rafræn gagnaskipti](across-data-exchange.md)   
[Reikningsfæra sölur](sales-how-invoice-sales.md)   
[Skrá innkaup](purchasing-how-record-purchases.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]