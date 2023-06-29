---
title: Reitarvörpum við innflutning SEPA CAMT skráa | Microsoft Docs
description: Á Evrópumörkuðum er hægt að flytja inn bankayfirlitsskrár með svæðisbundnum SEPA stöðlum (sameiginlegt evrópskt greiðslusvæði).
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 01/06/2023
ms.custom: bap-template
---
# <a name="field-mapping-when-importing-sepa-camt-files"></a><a name="field-mapping-when-importing-sepa-camt-files"></a>Reitarvörpum við innflutning SEPA CAMT skráa

[!INCLUDE[prod_short](includes/prod_short.md)] styður svæðisbundinn SEPA-staðall (sameiginlegt evrópskt greiðslusvæði) fyrir innflutning SEPA-bankayfirlita (CAMT-snið). Frekari upplýsingar eru í [Nota AMC Banking 365 Fundamentals-viðbótina](ui-extensions-amc-banking.md).  

 SEPA CAMT-staðallinn er með staðbundin afbrigði. Því gæti þurft að breyta almennum gagnaskiptaskilgreiningum (táknað  **SEPA CAMT**  Code á  **síðunni skilgreiningar**  á gögnum) til að aðlaga það að staðbundnum breytileika staðalsins. Eftirfarandi töflur sýna vörpun frá einingu í reit fyrir töflur 81, 273 og 274 í SEPA CAMT-framkvæmd í [!INCLUDE[prod_short](includes/prod_short.md)].  

 Frekari upplýsingar um að búa til eða stilla gagnaskiptaskilgreiningu eru í [Setja upp gagnaskiptaskilgreiningar](across-how-to-set-up-data-exchange-definitions.md).  

## <a name="camt-data-mapping-to-fields-in-the-general-journal-table-81"></a><a name="camt-data-mapping-to-fields-in-the-general-journal-table-81"></a>CAMT gagnakortalagning á reitum í færslubókarlínu (81)

|Slóð staks|Skilaboðaeining|Gagnagerð|Lýsing|Auðkenni neikvæðs formerkis|Nr. reits|Heiti reits|  
|------------------|---------------------|---------------|-----------------|-------------------------------|---------------|----------------|  
|Stmt/Ntry/Amt|Upphæð|Tugakerfið|Peningaupphæð reiðufésfærslunnar.||13|Upphæð|  
|Stmt/Ntry/CdtDbtInd|CreditDebitIndicator|Texti|Sýnir hvort færsla er kredit-eða debet færslu|DBIT|13|Upphæð|  
|Stmt/Ntry/BookgDt/Dt|Dagsetning|Dagsetning|Dagsetning þegar færsla er bókuð á reikning á bókum reikningsstofnunar||5|Bókunardags.|  
|Stmt/Ntry/BookgDt/DtTm|Dagsetning og tími|Dagsetning og tími|Dagsetning og tími þegar færsla er bókuð á reikning á bókum reikningsstofnunar||5|Bókunardags.|  
|Stmt/Ntry/NtryDtls/TxDtls/RltdPties/Dbtr/Nm|Heiti|Texti|Nafn aðilans sem skuldar lánveitanda (til þrautavara) tiltekna fjárhæð.||1221|Upplýsingar um greiðanda|  
|Stmt/Ntry/NtryDtls/TxDtls/RmtInf/Ustrd|Óskipulagt|Texti|Upplýsingarnar til að gera samsvörun / afstemmingu á færslu með þeim vörum sem greiðsla er ætlað að stemma af, svo sem viðskiptareikningar í reikningskröfukerfi í ómótaðan formi||8|Lýsing|  
|Stmt/Ntry/AddtlNtryInf|AdditionalEntryInformation|Texti|Viðbótarupplýsingar um færslu||1222|Færsluupplýsingar|  

## <a name="camt-data-mapping-to-fields-in-the-bank-acc-reconciliation-table-273"></a><a name="camt-data-mapping-to-fields-in-the-bank-acc-reconciliation-table-273"></a>CAMT gagnakortalagning á reitum í bankanum Acc. Afstemming töflu (273)

|Slóð staks|Skilaboðaeining|Gagnagerð|Lýsing|Auðkenni neikvæðs formerkis|Nr. reits|Heiti reits|  
|------------------|---------------------|---------------|-----------------|-------------------------------|---------------|----------------|  
|Stmt/CreDtTm|CreationDateTime|Dagsetning|Dagsetning og tími þegar skilaboðin voru búin til||3|Dags. yfirlits|  
|Stmt/Bal/Amt|Upphæð|Tugakerfið|Upphæð sem skilar nettóupphæðum fyrir allar debet- og kreditfærslur.||4|Lokastaða yfirlits|  

## <a name="camt-data-mapping-to-fields-in-the-bank-acc-reconciliation-line-table-274"></a><a name="camt-data-mapping-to-fields-in-the-bank-acc-reconciliation-line-table-274"></a>CAMT gagnakortalagning á reiti í bankanum Acc. Afstemming línutölfu (274)

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

 Stök í hnútnum **Færsla** sem eru flutt inn í [!INCLUDE[prod_short](includes/prod_short.md)] en ekki tengd við neina reiti eru vistuð í töflunni **Bókunarskipti Dálkur Skilgreining**. Notendur geta skoðað þessar einingar á síðunum **Greiðsluafstemmingarbók**, **Greiðslujafnanir** og **Afstemming bankareiknings** með því að velja **Upplýsingar um bankayfirlitslínu** aðgerðina. Frekari upplýsingar eru í [afstemma greiðslur með því að nota sjálfvirk jöfnun](receivables-how-reconcile-payments-auto-application.md)

> [!IMPORTANT]
> Í innflutningi á CAMT-bankayfirlitum, býst [!INCLUDE[prod_short](includes/prod_short.md)] við að hver færsla sé einkvæm, sem þýðir að reiturinn **Færslukenni** sem kemur úr merkinu *Stmt/Ntry/NtryDtls/TxDtls/Refs/EndToEndId* í CAMT-skránni, verður að vera einkvæmt innan opnu afstemmingar bankareikningsins. Ef upplýsingarnar eru ekki til staðar, hunsar [!INCLUDE[prod_short](includes/prod_short.md)] greiðsluna. Ef fyrri bankaafstemming á sama bankareikningi var bókuð með sama færslukenninu eins og í núverandi innflutningi, afstemmist núverandi færsla ekki sjálfkrafa en er enn hægt að flytja inn.

## <a name="see-also"></a><a name="see-also"></a>Sjá einnig

[Setja upp gagnaskipti](across-set-up-data-exchange.md)  
[Rafræn gagnaskipti](across-data-exchange.md)  
[Nota AMC Banking 365 Fundamentals viðbótina](ui-extensions-amc-banking.md)  
[Nota XML-skema til að undirbúa skilgreiningar gagnaskipta](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)  
[Afstemma greiðslur með sjálfvirkri jöfnun](receivables-how-reconcile-payments-auto-application.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
