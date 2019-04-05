---
title: 'Hönnunarupplýsingar - Kóðaeining 12 Breytingar: Vörpun altækra breyta fyrir bókunarlínu færslubókar | Microsoft Docs'
description: Eftirfarandi breytingar hafa verið settar í þessa útgáfu af Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 9cb19558c8c441eac188504e798ca36d86b599d5
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "800323"
---
# <a name="codeunit-12-changes-mapping-global-variables-for-general-journal-post-line"></a>Kóðaeining 12 Breytingar: Vörpun altækra breyta fyrir bókunarlínu færslubókar
Eftirfarandi breytingar hafa verið settar í þessa útgáfu af [!INCLUDE[d365fin](includes/d365fin_md.md)].  

|**Microsoft Dynamics NAV 2009 R2**|**Microsoft Dynamics NAV 2013 R2**|**Athugasemd**|  
|----------------------------------------|----------------------------------------|-----------------|  
|GLSetup@1009 : Record 98;|GLSetup@1009 : Record 98;|Óbreytt|  
|SalesSetup@1010 : Record 311;||Breytt í staðbundið|  
|PurchSetup@1011 : Record 312;||Breytt í staðbundið|  
|AccountingPeriod@1012 : Record 50;||Breytt í staðbundið|  
|GLAcc@1013 : Record 15;||Breytt í staðbundið|  
|GLEntry@1014 : Record 17;|GlobalGLEntry@1014 : Record 17;|Endurnefnt|  
|GLEntryTmp@1015 : TEMPORARY Record 17;|TempGLEntryBuf@1010 : TEMPORARY Record 17;|Endurnefnt|  
|TempGLEntryVAT@1016 : TEMPORARY Record 17;|TempGLEntryVAT@1016 : TEMPORARY Record 17;|Óbreytt|  
|OrigGLEntry@1017 : Record 17;||Eytt|  
|VATPostingSetup@1019 : Record 325;||Breytt í staðbundið|  
|Cust@1020 : Record 18;||Breytt í staðbundið|  
|Vend@1021 : Record 23;||Breytt í staðbundið|  
|GenJnlLine@1022 : Record 81;||Breytt í staðbundið|  
|GLReg@1029 : Record 45;|GLReg@1029 : Record 45;|Óbreytt|  
|CustPostingGr@1030 : Record 92;||Breytt í staðbundið|  
|VendPostingGr@1031 : Record 93;||Breytt í staðbundið|  
|Currency@1032 : Record 4;||Breytt í staðbundið|  
|AddCurrency@1033 : Record 4;|AddCurrency@1033 : Record 4;|Óbreytt|  
|ApplnCurrency@1034 : Record 4;||Breytt í staðbundið|  
|CurrExchRate@1035 : Record 330;|CurrExchRate@1035 : Record 330;|Óbreytt|  
|VATEntry@1038 : Record 254;|VATEntry@1038 : Record 254;|Óbreytt|  
|BankAcc@1039 : Record 270;||Breytt í staðbundið|  
|BankAccLedgEntry@1040 : Record 271;||Breytt í staðbundið|  
|CheckLedgEntry@1041 : Record 272;||Breytt í staðbundið|  
|CheckLedgEntry2@1042 : Record 272;||Breytt í staðbundið|  
|BankAccPostingGr@1043 : Record 277;||Breytt í staðbundið|  
|GenJnlTemplate@1044 : Record 80;||Breytt í staðbundið|  
|TaxJurisdiction@1045 : Record 320;||Breytt í staðbundið|  
|TaxDetail@1046 : Record 322;|TaxDetail@1046 : Record 322;|Óbreytt|  
|FAGLPostBuf@1047 : TEMPORARY Record 5637;||Breytt í staðbundið|  
|UnrealizedCustLedgEntry@1084 : Record 21;|UnrealizedCustLedgEntry@1084 : Record 21;|Óbreytt|  
|UnrealizedVendLedgEntry@1085 : Record 25;|UnrealizedVendLedgEntry@1085 : Record 25;|Óbreytt|  
|GLEntryVATEntryLink@1087 : Record 253;|GLEntryVATEntryLink@1087 : Record 253;|Óbreytt|  
|TempVATEntry@1088 : TEMPORARY Record 254;|TempVATEntry@1088 : TEMPORARY Record 254;|Óbreytt|  
|ReversedGLEntryTemp@1089 : TEMPORARY Record 17;||Fært í Codeunit17|  
|CostAccSetup@1092 : Record 1108;||Breytt í staðbundið|  
|GenJnlCheckLine@1048 : Codeunit 11;|GenJnlCheckLine@1001 : Codeunit 11;|Óbreytt|  
|ExchAccGLJnlLine@1049 : Codeunit 366;||Breytt í staðbundið|  
|FAJnlPostLine@1050 : Codeunit 5632;||Breytt í staðbundið|  
|SalesTaxCalculate@1051 : Codeunit 398;||Breytt í staðbundið|  
|GenJnlApply@1052 : Codeunit 225;||Breytt í staðbundið|  
|DimMgt@1053 : Codeunit 408;||Breytt í staðbundið|  
|JobPostLine@1028 : Codeunit 1001;||Breytt í staðbundið|  
|TransferGlEntriesToCA@1091 : Codeunit 1105;||Breytt í staðbundið|  
||PaymentToleranceMgt@1002 : Codeunit 426;|Bætt við|  
||AddCurrencyCode@1117 : Code[10];|Bætt við|  
|FiscalYearStartDate@1054 : Date;|FiscalYearStartDate@1011 : Date;|Óbreytt|  
|NextEntryNo@1055 : Integer;|NextEntryNo@1022 : Integer;|Óbreytt|  
|BalanceCheckAmount@1056 : Decimal;|BalanceCheckAmount@1056 : Decimal;|Óbreytt|  
|BalanceCheckAmount2@1057 : Decimal;|BalanceCheckAmount2@1057 : Decimal;|Óbreytt|  
|BalanceCheckAddCurrAmount@1058 : Decimal;|BalanceCheckAddCurrAmount@1058 : Decimal;|Óbreytt|  
|BalanceCheckAddCurrAmount2@1059 : Decimal;|BalanceCheckAddCurrAmount2@1059 : Decimal;|Óbreytt|  
|CurrentBalance@1060 : Decimal;|CurrentBalance@1060 : Decimal;|Óbreytt|  
|SalesTaxBaseAmount@1061 : Decimal;||Breytt í staðbundið|  
|TotalAddCurrAmount@1062 : Decimal;|TotalAddCurrAmount@1062 : Decimal;|Óbreytt|  
|TotalAmount@1063 : Decimal;|TotalAmount@1063 : Decimal;|Óbreytt|  
|UnrealizedRemainingAmountCust@1086 : Decimal;|UnrealizedRemainingAmountCust@1086 : Decimal;|Óbreytt|  
|UnrealizedRemainingAmountVend@1074 : Decimal;|UnrealizedRemainingAmountVend@1074 : Decimal;|Óbreytt|  
|NextVATEntryNo@1064 : Integer;|NextVATEntryNo@1064 : Integer;|Óbreytt|  
|FirstNewVATEntryNo@1065 : Integer;|FirstNewVATEntryNo@1065 : Integer;|Óbreytt|  
|NextTransactionNo@1066 : Integer;|NextTransactionNo@1066 : Integer;|Óbreytt|  
|NextConnectionNo@1067 : Integer;|NextConnectionNo@1067 : Integer;|Óbreytt|  
|InsertedTempGLEntryVAT@1068 : Integer;|InsertedTempGLEntryVAT@1027 : Integer;|Óbreytt|  
|LastDocNo@1069 : Code[20];|LastDocNo@1023 : Code[20];|Óbreytt|  
|LastLineNo@1070 : Integer;||Eytt|  
|LastDate@1071 : Date;|LastDate@1021 : Date;|Óbreytt|  
|LastDocType@1072 : ' ,Payment,Invoice,Credit Memo,Finance Charge Memo,Reminder';|LastDocType@1025 : ' ,Payment,Invoice,Credit Memo,Finance Charge Memo,Reminder';|Óbreytt|  
|NextCheckEntryNo@1073 : Integer;|NextCheckEntryNo@1028 : Integer;|Óbreytt|  
|AddCurrGLEntryVATAmt@1075 : Decimal;|AddCurrGLEntryVATAmt@1017 : Decimal;|Óbreytt|  
|CurrencyDate@1076 : Date;|CurrencyDate@1020 : Date;|Óbreytt|  
|CurrencyFactor@1077 : Decimal;|CurrencyFactor@1019 : Decimal;|Óbreytt|  
|UseCurrFactorOnly@1078 : Boolean;|UseCurrFactorOnly@1078 : Boolean;|Óbreytt|  
|NonAddCurrCodeOccured@1079 : Boolean;|NonAddCurrCodeOccured@1079 : Boolean;|Óbreytt|  
|FADimAlreadyChecked@1080 : Boolean;|FADimAlreadyChecked@1080 : Boolean;|Óbreytt|  
|AllApplied@1081 : Boolean;||Breytt í staðbundið|  
|OverrideDimErr@1018 : Boolean;|OverrideDimErr@1018 : Boolean;|Óbreytt|  
|JobLine@1036 : Boolean;|JobLine@1036 : Boolean;|Óbreytt|  
|Prepayment@1037 : Boolean;||Eytt|  
|CheckUnrealizedCust@1082 : Boolean;|CheckUnrealizedCust@1082 : Boolean;|Óbreytt|  
|CheckUnrealizedVend@1083 : Boolean;|CheckUnrealizedVend@1083 : Boolean;|Óbreytt|  
|GLEntryNo@1090 : Integer;|GLEntryNo@1026 : Integer;|Óbreytt|  
||GLSetupRead@1015 : Boolean;|Bætt við|  
||AmountRoundingPrecision@1012 : Decimal;|Bætt við|  
||CrCardTransactionEntryNo@1013 : Integer;|Bætt við|  

## <a name="see-also"></a>Sjá einnig  
 [Hönnunarupplýsingar - Kóðaeining 12 Breytingar: Breytingar á bókunaraðferðum í færslubók](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)
