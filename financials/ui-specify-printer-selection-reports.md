---
title: "Setja upp skýrslur til að prenta á sérstökum prenturum | Microsoft Docs"
description: "Kynntu þér hvernig skal tilgreina prentara fyrir skýrslu og nota gluggann prentaraval."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online printing
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 42fb4adbcc01c443722fe90bb59edafceb34ff06
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="specify-printer-selection-for-reports"></a>Tilgreina prentaraval fyrir skýrslur
Þessi síða er auð vegna þess að ekki er hægt að setja upp ákveðnar prentara fyrir tilteknar skýrslur. Við erum að vinna að því að leysa þetta.

Í millitíðinni þarf að hlaða niður skýrslu sem á að prenta sem PDF-skjali fyrst með því að velja **Senda til** hnappinn. Þá er tegund skráar valin til að hlaða niður skýrslunni eins og **PDF-skjal** valið. Nú er hægt að opna PDF-skjalið strax og prenta það, eða vista það og prentað það síðar.

<!--

You can set up reports so that they must be printed on a specific printer. The following are some uses of printer selection:

- You can print reports on special company letterhead.
- You can print reports on different paper sizes.
- You can print reports on the default printer of a specified employee.

You use the **Printer Selections** window to set different values to obtain different output. If you set a specific printer selection, then it takes precedence over a more general printer selection. For example, you can set a printer selection that has values in the **User ID**, **Report ID**, and **Printer Name** fields. This printer selection takes precedence over a printer selection that has blank entries in the **User ID** or **Report ID** fields.

The following table describes the combination of values to specify when you set up printer selections for a report.

|To                                                 |Set the following values                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Print a report to a specific printer for all users |Specify values in the **Report ID** and **Printer Name** fields and leave the **User ID** field blank.|
|Print all reports to a specific printer for a specific user|Specify values in the **User ID** and **Printer Name** fields and leave the **Report ID** field blank.|
|Set the default printer for all reports|Specify a value in the **Printer Name** field and leave the **User ID** and **Report ID** fields blank.|
|Print a specific report to the user’s default printer|Specify a value in the **Report ID** field and leave the **Printer Name** and **User ID** fields blank.|
|Print a specific report to a specific printer for a specific user|Specify values in all three fields.|
-->

## <a name="see-also"></a>Sjá einnig
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Hvernig á að: Keyra runuvinnslur](ui-how-run-batch-jobs.md)  
[Hvernig á að: Senda skjöl í tölvupósti](ui-how-send-documents-email.md)  

