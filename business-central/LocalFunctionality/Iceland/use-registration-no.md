---
title: Skráningarnúmer í íslenska staðfæringu
description: Í þessari grein eru leiðbeiningar um notkun skráningarnúmera í íslenskri staðfærslu.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 05/07/2024
ms.author: altotovi
ms.reviewer: solsen
ms.service: dynamics-365-business-central
---

# <a name="registration-numbers-in-the-icelandic-localization"></a>Skráningarnúmer í íslenska staðfæringu

> [!NOTE]
> Þessar breytingar eiga aðeins við úr útgáfu 24.0 ef notandinn virkjar nýja [íslenska staðfæringu](iceland-global-core-app.md).

## <a name="registration-number-in-documents"></a>Skráningarnúmer í skjölum

Reiturinn Númer númeraraðarinnar er opnaður **.** hefur verið bætt við haus eftirfarandi fylgiskjala: sölureikningur, sölupöntun og sölukreditreikningur.

## <a name="sender-registration-number-for-payments"></a>Skráningarnúmer sendanda fyrir greiðslur

Reiturinn **Nr. sendingarskilyrða** Reit hefur verið bætt við töfluna **Greiðsluútflutningur gagna** þegar notandinn flytur út greiðslur.

> [!NOTE]
> Þennan reit má nota á eftirfarandi lista yfir tilvik: _OnBeforeInsertPmtExportDataJnlFromGenJnlLine,OnPreparePaymentExportDataCLEOnBeforeTempPaymentExportDataInsert_ _og_ _OnBeforeInsertPmtExportDataJnlFromVendorLedgerEntry._

## <a name="see-also"></a>Sjá einnig .

[Listi yfir staðbundnar aðgerðir á Íslandi](iceland-local-functionality.md)  
[Vinna með [!INCLUDE[prod_short](../../includes/prod_short.md)]](../../ui-work-product.md)  
[Lönd/svæði í boði og studd tungumál](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations)  

## [!INCLUDE[prod_short](../../includes/free_trial_md.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
