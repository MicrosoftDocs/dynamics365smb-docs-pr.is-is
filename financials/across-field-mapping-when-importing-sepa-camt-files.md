---
title: "Reitarvörpum við innflutning SEPA CAMT skráa | Microsoft Docs"
description: "Á Evrópumörkuðum er hægt að flytja inn bankayfirlitsskrár með svæðisbundnum SEPA stöðlum (sameiginlegt evrópskt greiðslusvæði)."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/18/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 9f99b1fce3c44fdf2053a74b8fa090c6b69aef1a
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="field-mapping-when-importing-sepa-camt-files"></a>Reitarvörpum við innflutning SEPA CAMT skráa
[!INCLUDE[d365fin](includes/d365fin_md.md)] styður svæðisbundinn SEPA-staðall (sameiginlegt evrópskt greiðslusvæði) fyrir innflutning SEPA-bankayfirlita (CAMT-snið). Nánari upplýsingar er að finna í [Setja upp umreikningsþjónustu fyrir bankagögn](bank-how-setup-bank-data-conversion-service.md).  

 SEPA CAMT-staðallinn er með staðbundin afbrigði. Því kann að vera nauðsynlegt að breyta almennri skilgreiningu gagnaskipta táknað með **SEPA CAMT** kóðanum í **Skilgreiningar fyrir bókunarskipti** glugganum til að laga hana að staðbundnum útgáfum staðalsins. Eftirfarandi töflur sýna vörpun frá einingu í reit fyrir töflur 81, 273 og 274 í SEPA CAMT-framkvæmd í [!INCLUDE[d365fin](includes/d365fin_md.md)].  

 Frekari upplýsingar um að búa til eða stilla gagnaskiptaskilgreiningu eru í [Setja upp gagnaskiptaskilgreiningar](across-how-to-set-up-data-exchange-definitions.md).  

## <a name="camt-data-mapping-to-fields-in-the-general-journal-table-81"></a>CAMT gagnakortalagning á reitum í færslubókarlínu (81)  

|Slóð staks|Skilaboðaeining|Gagnagerð|Lýsing|Auðkenni neikvæðs formerkis|Nr. reits|Heiti reits|  
|------------------|---------------------|---------------|-----------------|-------------------------------|---------------|----------------|  
|Stmt/Ntry/Amt|Upphæð|Tugakerfið|Peningaupphæð reiðufésfærslunnar.||13|Upphæð|  
|Stmt/Ntry/CdtDbtInd|CreditDebitIndicator|Texti|Sýnir hvort færsla er kredit-eða debet færslu|DBIT|13|Upphæð|  
|Stmt/Ntry/BookgDt/Dt|Dagsetning|Dagsetning|Dagsetning þegar færsla er bókuð á reikning á bókum reikningsstofnunar||5|Bókunardags.|  
|Stmt/Ntry/BookgDt/DtTm|Dagsetning og tími|Dagsetning og tími|Dagsetning og tími þegar færsla er bókuð á reikning á bókum reikningsstofnunar||5|Bókunardags.|  
|Stmt/Ntry/NtryDtls/TxDtls/RltdPties/Dbtr/Nm|Heiti|Texti|Nafn aðilans sem skuldar lánveitanda (til þrautavara) tiltekna fjárhæð.||1221|Upplýsingar um greiðanda|  
|Stmt/Ntry/NtryDtls/TxDtls/RmtInf/Ustrd|Óskipulagt|Texti|Upplýsingarnar til að gera samsvörun / afstemmingu á færslu með þeim vörum sem greiðsla er ætlað að stemma af, svo sem viðskiptareikningar í reikningskröfukerfi í ómótaðan formi||8|Lýsing|  
|Stmt/Ntry/AddtlNtryInf|AdditionalEntryInformation|Texti|Viðbótarupplýsingar um færslu||1222|Færsluupplýsingar|  

## <a name="camt-data-mapping-to-fields-in-the-bank-acc-reconciliation-table-273"></a>CAMT gagnakortalagning á reitum í bankanum Acc. Afstemming töflu (273)  

|Slóð staks|Skilaboðaeining|Gagnagerð|Lýsing|Auðkenni neikvæðs formerkis|Nr. reits|Heiti reits|  
|------------------|---------------------|---------------|-----------------|-------------------------------|---------------|----------------|  
|Stmt/CreDtTm|CreationDateTime|Dagsetning|Dagsetning og tími þegar skilaboðin voru búin til||3|Dags. yfirlits|  
|Stmt/Bal/Amt|Upphæð|Tugakerfið|Upphæð sem skilar nettóupphæðum fyrir allar debet- og kreditfærslur.||4|Lokastaða yfirlits|  

## <a name="camt-data-mapping-to-fields-in-the-bank-acc-reconciliation-line-table-274"></a>CAMT gagnakortalagning á reiti í bankanum Acc. Afstemming línutölfu (274)  

|Slóð staks|Skilaboðaeining|Gagnagerð|Lýsing|Auðkenni neikvæðs formerkis|Nr. reits|Heiti reits|  
|------------------|---------------------|---------------|-----------------|-------------------------------|---------------|----------------|  
|Stmt/Ntry/Amt|Upphæð|Tugakerfið|Peningaupphæð reiðufésfærslunnar.||7|Upphæð yfirlits|  
|Stmt/Ntry/CdtDbtInd|CreditDebitIndicator|Texti|Sýnir hvort færsla er kredit-eða debet færslu|DBIT|7|Upphæð yfirlits|  
|Stmt/Ntry/BookgDt/Dt|Dagsetning|Dagsetning|Dagsetning þegar færsla er bókuð á reikning á bókum reikningsstofnunar||5|Dags. færslu|  
|Stmt/Ntry/BookgDt/DtTm|Dagsetning og tími|Dagsetning og tími|Dagsetning og tími þegar færsla er bókuð á reikning á bókum reikningsstofnunar||5|Dags. færslu|  
|Stmt/Ntry/ValDt/Dt|Dagsetning|Dagsetning|Dagsetning þegar eignir verða í boði til reikningseiganda við kreditfærslu, eða hætta að vera til staðar til reikningseiganda við debetfærslu||12|Gildisdagur|  
|Stmt/Ntry/ValDt/DtTm|Dagsetning og tími|Dagsetning og tími|Dagsetning og tími þegar eignir verða í boði til reikningseiganda við kreditfærslu, eða hætta að vera til staðar til reikningseiganda við debetfærslu||12|Gildisdagur|  
|Stmt/Ntry/NtryDtls/TxDtls/RltdPties/Dbtr/Nm|Heiti|Texti|Nafn aðilans sem skuldar lánveitanda (til þrautavara) tiltekna fjárhæð.||15|Upplýsingar um greiðanda|  
|Stmt/Ntry/NtryDtls/TxDtls/RmtInf/Ustrd|Óskipulagt|Texti|Upplýsingarnar til að gera samsvörun / afstemmingu á færslu með þeim vörum sem greiðsla er ætlað að stemma af, svo sem viðskiptareikningar í reikningskröfukerfi í ómótaðan formi||6|Lýsing|  
|Stmt/Ntry/AddtlNtryInf|AdditionalEntryInformation|Texti|Viðbótarupplýsingar um færslu||16|Færsluupplýsingar|  

 Stök í hnútnum **Færsla** sem eru flutt inn í [!INCLUDE[d365fin](includes/d365fin_md.md)] en ekki tengd við neina reiti eru vistuð í töflunni **Bókunarskipti Dálkur Skilgreining**. Notendur geta skoðað þessar einingar frá **Greiðsluafstemmingarbók** **Greiðslujafnanir** og **Afstemming bankareiknings** gluggum með því að velja **Upplýsingar um bankayfirlitslínu** aðgerðina. Frekari upplýsingar eru í [afstemma greiðslur með því að nota sjálfvirk jöfnun](receivables-how-reconcile-payments-auto-application.md)  
## <a name="see-also"></a>Sjá einnig  
[Setja upp gagnaskipti](across-set-up-data-exchange.md)  
[Rafræn gagnaskipti](across-data-exchange.md)  
[Setja upp umskráningarþjónustu fyrir bankagögn](bank-how-setup-bank-data-conversion-service.md)   
[Nota XML-skema til að undirbúa skilgreiningar gagnaskipta](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)  
[Afstemma greiðslur með sjálfvirkri jöfnun](receivables-how-reconcile-payments-auto-application.md)  

