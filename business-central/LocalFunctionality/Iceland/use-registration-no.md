---
title: Skráningarnúmer í íslenskri staðfærslu
description: Í þessari grein eru leiðbeiningar um notkun skráningarnúmera í íslenskri staðfærslu.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 04/02/2024
ms.author: altotovi
ms.reviewer: solsen
ms.service: dynamics-365-business-central
---

# Skráningarnúmer í íslenskri staðfærslu 

> [!NOTE]
> Þessar breytingar eiga aðeins við úr útgáfu 24.0 ef notandinn virkjar nýja [íslenska staðfæringu](iceland-global-core-app.md).  

## Númer skráningar í fylgiskjölum

Reiturinn Númer númeraraðarinnar er opnaður **.** hefur verið bætt við hausana í eftirfarandi fylgiskjölum **Sölureikningur**, **Sölupöntun** og **Sölukreditreikningur**.  

## Skráningarnr. sendanda fyrir greiðslur  

Reiturinn **Nr. sendingarskilyrða** Reit hefur verið bætt við Greiðsluútflutningsgögn **þegar** notandi flytur út greiðslur.  

> [!NOTE]
> Þennan reit má nota með eftirfarandi lista yfir tilvik: _OnBeforeInsertPmtExportDataJnlFromGenJnlLine,OnPreparePaymentExportDataCLEOnBeforeTempPaymentExportDataInsert_ _og_ _OnBeforeInsertPmtExportDataJnlFromVendorLedgerEntry._  

## Sjá einnig .

[Listi yfir staðbundnar aðgerðir á Íslandi](iceland-local-functionality.md)   
[Vinna með [!INCLUDE[prod_short](../../includes/prod_short.md)]](../../ui-work-product.md)
[lands-/svæðisbundið til ráðstöfunar og studd tungumál](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations)

## [!INCLUDE[prod_short](../../includes/free_trial_md.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
