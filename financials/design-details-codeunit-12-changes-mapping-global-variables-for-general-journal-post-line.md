---
title: "Hönnunarupplýsingar - Kóðaeining 12 Breytingar: Vörpun altækra breyta fyrir bókunarlínu færslubókar | Microsoft Docs"
description: "Eftirfarandi breytingar hafa verið settar í þessa útgáfu af Finance and Operations, Business Edition."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: d1199adb2912d88c545cabcc84d5c9bf27b0892a
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="codeunit-12-changes-mapping-global-variables-for-general-journal-post-line"></a>Kóðaeining 12 Breytingar: Vörpun altækra breyta fyrir bókunarlínu færslubókar
Eftirfarandi breytingar hafa verið settar í þessa útgáfu af [!INCLUDE[d365fin](includes/d365fin_md.md)].  

|**Microsoft Dynamics NAV 2009 R2**|**Microsoft Dynamics NAV 2013 R2**|**Athugasemd**|  
|----------------------------------------|----------------------------------------|-----------------|  
|GLSetup@1009 : Færsla 98;|GLSetup@1009 : Færsla 98;|Óbreytt|  
|SalesSetup@1010 : Færsla 311;||Breytt í staðbundið|  
|PurchSetup@1011 : Færsla 312;||Breytt í staðbundið|  
|AccountingPeriod@1012 : Færsla 50;||Breytt í staðbundið|  
|GLAcc@1013 : Færsla 15;||Breytt í staðbundið|  
|GLEntry@1014 : Færsla 17;|GlobalGLEntry@1014 : Færsla 17;|Endurnefnt|  
|GLEntryTmp@1015 : TÍMABUNDIN Færsla 17;|TempGLEntryBuf@1010 : TÍMABUNDIN Færsla 17;|Endurnefnt|  
|TempGLEntryVAT@1016 : TÍMABUNDIN Færsla 17;|TempGLEntryVAT@1016 : TÍMABUNDIN Færsla 17;|Óbreytt|  
|OrigGLEntry@1017 : Færsla 17;||Eytt|  
|VATPostingSetup@1019 : Færsla 325;||Breytt í staðbundið|  
|Cust@1020 : Færsla 18;||Breytt í staðbundið|  
|Vend@1021 : Færsla 23;||Breytt í staðbundið|  
|GenJnlLine@1022 : Færsla 81;||Breytt í staðbundið|  
|GLReg@1029 : Færsla 45;|GLReg@1029 : Færsla 45;|Óbreytt|  
|CustPostingGr@1030 : Færsla 92;||Breytt í staðbundið|  
|VendPostingGr@1031 : Færsla 93;||Breytt í staðbundið|  
|Currency@1032 : Færsla 4;||Breytt í staðbundið|  
|AddCurrency@1033 : Færsla 4;|AddCurrency@1033 : Færsla 4;|Óbreytt|  
|ApplnCurrency@1034 : Færsla 4;||Breytt í staðbundið|  
|CurrExchRate@1035 : Færsla 330;|CurrExchRate@1035 : Færsla 330;|Óbreytt|  
|VATEntry@1038 : Færsla 254;|VATEntry@1038 : Færsla 254;|Óbreytt|  
|BankAcc@1039 : Færsla 270;||Breytt í staðbundið|  
|BankAccLedgEntry@1040 : Færsla 271;||Breytt í staðbundið|  
|CheckLedgEntry@1041 : Færsla 272;||Breytt í staðbundið|  
|CheckLedgEntry2@1042 : Færsla 272;||Breytt í staðbundið|  
|BankAccPostingGr@1043 : Færsla 277;||Breytt í staðbundið|  
|GenJnlTemplate@1044 : Færsla 80;||Breytt í staðbundið|  
|TaxJurisdiction@1045 : Færsla 320;||Breytt í staðbundið|  
|TaxDetail@1046 : Færsla 322;|TaxDetail@1046 : Færsla 322;|Óbreytt|  
|FAGLPostBuf@1047 : TÍMABUNDIN Færsla 5637;||Breytt í staðbundið|  
|UnrealizedCustLedgEntry@1084 : Færsla 21;|UnrealizedCustLedgEntry@1084 : Færsla 21;|Óbreytt|  
|UnrealizedVendLedgEntry@1085 : Færsla 25;|UnrealizedVendLedgEntry@1085 : Færsla 25;|Óbreytt|  
|GLEntryVATEntryLink@1087 : Færsla 253;|GLEntryVATEntryLink@1087 : Færsla 253;|Óbreytt|  
|TempVATEntry@1088 : TÍMABUNDIN færsla 254;|TempVATEntry@1088 : TÍMABUNDIN færsla 254;|Óbreytt|  
|ReversedGLEntryTemp@1089 : TÍMABUNDIN Færsla 17;||Fært í Codeunit17|  
|CostAccSetup@1092 : Færsla 1108;||Breytt í staðbundið|  
|GenJnlCheckLine@1048 : Codeunit 11;|GenJnlCheckLine@1001 : Codeunit 11;|Óbreytt|  
|ExchAccGLJnlLine@1049 : Codeunit 366;||Breytt í staðbundið|  
|FAJnlPostLine@1050 : Codeunit 5632;||Breytt í staðbundið|  
|SalesTaxCalculate@1051 : Codeunit 398;||Breytt í staðbundið|  
|GenJnlApply@1052 : Codeunit 225;||Breytt í staðbundið|  
|DimMgt@1053 : Codeunit 408;||Breytt í staðbundið|  
|JobPostLine@1028 : Codeunit 1001;||Breytt í staðbundið|  
|TransferGlEntriesToCA@1091 : Codeunit 1105;||Breytt í staðbundið|  
||PaymentToleranceMgt@1002 : Codeunit 426;|Bætt við|  
||AddCurrencyCode@1117 : Kóði[10];|Bætt við|  
|FiscalYearStartDate@1054 : Dagsetning;|FiscalYearStartDate@1011 : Dagsetning;|Óbreytt|  
|NextEntryNo@1055 : Heiltala;|NextEntryNo@1022 : Heiltala;|Óbreytt|  
|BalanceCheckAmount@1056 : Tugastafur;|BalanceCheckAmount@1056 : Tugastafur;|Óbreytt|  
|BalanceCheckAmount2@1057 : Tugastafur;|BalanceCheckAmount2@1057 : Tugastafur;|Óbreytt|  
|BalanceCheckAddCurrAmount@1058 : Tugastafur;|BalanceCheckAddCurrAmount@1058 : Tugastafur;|Óbreytt|  
|BalanceCheckAddCurrAmount2@1059 : Tugastafur;|BalanceCheckAddCurrAmount2@1059 : Tugastafur;|Óbreytt|  
|CurrentBalance@1060 : Tugastafur;|CurrentBalance@1060 : Tugastafur;|Óbreytt|  
|SalesTaxBaseAmount@1061 : Tugastafur;||Breytt í staðbundið|  
|TotalAddCurrAmount@1062 : Tugastafur;|TotalAddCurrAmount@1062 : Tugastafur;|Óbreytt|  
|TotalAmount@1063 : Tugastafur;|TotalAmount@1063 : Tugastafur;|Óbreytt|  
|UnrealizedRemainingAmountCust@1086 : Tugastafur;|UnrealizedRemainingAmountCust@1086 : Tugastafur;|Óbreytt|  
|UnrealizedRemainingAmountVend@1074 : Tugastafur;|UnrealizedRemainingAmountVend@1074 : Tugastafur;|Óbreytt|  
|NextVATEntryNo@1064 : Heiltala;|NextVATEntryNo@1064 : Heiltala;|Óbreytt|  
|FirstNewVATEntryNo@1065 : Heiltala;|FirstNewVATEntryNo@1065 : Heiltala;|Óbreytt|  
|NextTransactionNo@1066 : Heiltala;|NextTransactionNo@1066 : Heiltala;|Óbreytt|  
|NextConnectionNo@1067 : Heiltala;|NextConnectionNo@1067 : Heiltala;|Óbreytt|  
|InsertedTempGLEntryVAT@1068 : Heiltala;|InsertedTempGLEntryVAT@1027 : Heiltala;|Óbreytt|  
|LastDocNo@1069 : Kóði[20];|LastDocNo@1023 : Kóði[20];|Óbreytt|  
|LastLineNo@1070 : Heiltala;||Eytt|  
|LastDate@1071 : Dagsetning;|LastDate@1021 : Dagsetning;|Óbreytt|  
|LastDocType@1072 : ' ,Greiðsla,Reikningur,Kreditreikningur,Vaxtareikningur,Innheimtubréf;|LastDocType@1025 : ' ,Greiðsla,Reikningur,Kreditreikningur,Vaxtareikningur,Innheimtubréf;|Óbreytt|  
|NextCheckEntryNo@1073 : Heiltala;|NextCheckEntryNo@1028 : Heiltala;|Óbreytt|  
|AddCurrGLEntryVATAmt@1075 : Tugastafur;|AddCurrGLEntryVATAmt@1017 : Tugastafur;|Óbreytt|  
|CurrencyDate@1076 : Dagsetning;|CurrencyDate@1020 : Dagsetning;|Óbreytt|  
|CurrencyFactor@1077 : Tugastafur;|CurrencyFactor@1019 : Tugastafur;|Óbreytt|  
|UseCurrFactorOnly@1078 : Boole-gildi;|UseCurrFactorOnly@1078 : Boole-gildi;|Óbreytt|  
|NonAddCurrCodeOccured@1079 : Boole-gildi;|NonAddCurrCodeOccured@1079 : Boole-gildi;|Óbreytt|  
|FADimAlreadyChecked@1080 : Boole-gildi|FADimAlreadyChecked@1080 : Boole-gildi|Óbreytt|  
|AllApplied@1081 : Boole-gildi;||Breytt í staðbundið|  
|OverrideDimErr@1018 : Boole-gildi;|OverrideDimErr@1018 : Boole-gildi;|Óbreytt|  
|JobLine@1036 : Boole-gildi;|JobLine@1036 : Boole-gildi;|Óbreytt|  
|Prepayment@1037 : Boole-gildi||Eytt|  
|CheckUnrealizedCust@1082 : Boole-gildi;|CheckUnrealizedCust@1082 : Boole-gildi;|Óbreytt|  
|CheckUnrealizedVend@1083 : Boole-gildi;|CheckUnrealizedVend@1083 : Boole-gildi;|Óbreytt|  
|GLEntryNo@1090 : Heiltala;|GLEntryNo@1026 : Heiltala;|Óbreytt|  
||GLSetupRead@1015 : Boole-gildi;|Bætt við|  
||AmountRoundingPrecision@1012 : Tugastafur;|Bætt við|  
||CrCardTransactionEntryNo@1013 : Heiltala;|Bætt við|  

## <a name="see-also"></a>Sjá einnig  
 [Hönnunarupplýsingar - Kóðaeining 12 Breytingar: Breytingar á bókunaraðferðum í færslubók](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)

