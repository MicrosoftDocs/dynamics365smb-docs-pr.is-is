---
title: Birgða- og vöruhúsaskýrslur og greiningar
description: Finna út hvaða birgða- og vöruhúsaskýrslur eru í boði í staðlaðri útgáfu Business Central til að halda utan um reksturinn.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: reporting
ms.search.form: 'Report_707, Report_716, Report_813, Report_1001, Report_5807, Report_5808, Report_5809, Report_7313, Report_7319, Report_7320'
ms.date: 03/21/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Birgða- og vöruhúsaskýrslur og greiningar

Birgða- og vöruhúsaskýrslur gefa [!INCLUDE [prod_short](includes/prod_short.md)] innsýn í birgðir og viðskiptafræðinga og upplýsingar um núgildandi og eldri birgða- og vöruhúsaaðgerðir.  

## Skýrslur

[!INCLUDE [inventory_WMS_reports](includes/inventory-WMS-reports-include.md)]

## Verkefni

Eftirfarandi greinar lýsa sumum lykilverkum til að greina stöðu fyrirtækisins:

* [Stofna greiningarskýrslur](bi-how-create-analysis-views-reports.md)  
* [Skoða tiltækileika vöru](inventory-how-availability-overview.md)

## Prenta og skanna strikamerki

Notkun strikamerkis getur hjálpað til við að straumlínulaga ferli á innleið, útleið og innanhúss vöruhúss. 

[!INCLUDE [barcode-mobile-app](includes/barcode-mobile-app.md)]

Þegar forritið hefur verið sett upp er hægt að nota aðgerðina Prenta límmiða **til** að prenta 1D og 2D strikamerki af síðunum sem taldar eru upp í eftirfarandi töflu.

|Síða  |Svæðisgildi strikamerki geta innihaldið  |
|---------|---------|
|Vörur, Birgðaspjald     |Vörunr., Lýsing og GTIN         |
|Vörutilvísunarlisti, Vörutilvísun     |Vörunr., Lýsing, Mælieining og Tilvísunarnr.         |
|Lotunr. Upplýsingalisti, Lotunr. Merki     |Vörunr., Lýsing og Lotunúmer       |
|SN-merki     |Nr., Lýsing og Raðnúmer         |

> [!NOTE]
> Sumir prentarar og strikamerkis-/QR-kótasnið krefjast sérstakrar útfærslu. Það gæti þurft að hlaða upp öðru Word-sniðmáti eða klóna skýrsluna til að búa til eigin sérsniðnu útgáfu.


## Skoða birgðaskýrslur með skýrsluvafra

Til að fá yfirlit yfir þær skýrslur sem eru tiltækar fyrir birgðir skal velja **Allar skýrslur** á heimasíðunni. Þessi aðgerð opnar Hlutverkavafrann sem er afmarkaður við aðgerðirnar í valkostinum **Skýrsla & Greining** . Undir hausnum **Sala og Markaðssetning** skal velja **Skoða**.

:::image type="content" source="media/report-explorer-sales.png" alt-text="Dæmi um skýrslur í fjármálahlutverkamiðstöðinni." lightbox="media/report-explorer-sales.png":::

Nánari upplýsingar eru í [Finna skýrslur með hlutverkavafranum](ui-role-explorer.md).


## Sjá einnig .

[Tilfalengd greining á birgðagögnum](ad-hoc-analysis-inventory.md)  
[Yfirlit birgðagreiningar](inventory-analytics-overview.md)   
[Uppsetning birgða](inventory-setup-inventory.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Yfirlit yfir vöruhúsakerfi](design-details-warehouse-management.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
