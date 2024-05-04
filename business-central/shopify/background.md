---
title: Keyra verk í bakgrunni og endurtekið
description: Grunnstilltu samstillingu gagna á milli Business Central og Shopify í bakgrunni.
ms.date: 03/26/2024
ms.topic: article
ms.service: dynamics-365-business-central
ms.reviewer: solsen
author: brentholtorf
ms.author: bholtorf
---

# <a name="run-tasks-in-the-background"></a>Keyra verk í bakgrunni

Það er skilvirkt að keyra sum verkefni samtímis og á sjálfvirkan hátt. Þú getur framkvæmt slík verk í bakgrunni og getur einnig sett áætlun um hvenær þú vilt að þessi verk keyri sjálfkrafa. Til að keyra verk í bakgrunni eru tvær stillingar studdar:

- Verk sem ræst eru handvirkt eru tímasett strax í gegnum **Verkraðarfærslur**.
- Endurtekin verk eru tímasett í **Verkraðarfærslur**.

## <a name="run-tasks-in-the-background-for-a-specific-shop"></a>Keyra verk í bakgrunni fyrir tiltekna verslun

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, opna **Shopify Verslun** og veldu tengda tengilinn.
2. Velja skal verkstæðið sem á að keyra samstillingu fyrir til að opna **Shopify síðuna Vinnusalarspjald** .
3. Kveikja á **vífæringu á Samstilla** bakgrunn bakgrunns.

Þegar samstillingaraðgerðin hefst biður hann þig að bíða í stað þess að keyra verk í forgrunni. Þegar því lýkur er hægt að fara í næstu aðgerð. Verkið er stofnað sem **verkraðarfærsla** og hefst strax.

## <a name="to-schedule-recurring-tasks"></a>Að tímasetja endurtekin verk

Þú getur tímasett eftirfarandi endurteknar aðgerðir sem á að framkvæma á sjálfvirkan hátt. Frekari upplýsingar um tímasetningu verka er að finna í [Verkröð](../admin-job-queues-schedule-tasks.md).

|Verkefni|Hlutur|
|------|------------|
|**Samstilla pantanir frá Shopify**|Skýrsla 30104 Samstilla pantanir frá Shopify|
|**Vinna úr Shopify pöntunum**|Skýrsla 30103 Shopify stofna sölupantanir|
|**Samstilla sendingar við Shopify**|Skýrsla 30109 Samstilla sendingu við Shopify|
|**Samstilla vörur og/eða verð**|Skýrsla 30108 Shopify samstilla vörur|
|**Samstilla birgðir**|Skýrsla 30102 Samstilla birgðir við Shopify|
|**Samstilla myndir**|Skýrsla 30107 Shopify samstilla myndir|
|**Samstilla viðskiptamenn**|Skýrsla 30100 Shopify samstilla viðskiptamenn|
|**Samstilla fyrirtæki**|Skýrsla 30114 Shopify samstillt fyrirtæki (B2B)|
|**Samstilla greiðslur**|Skýrsla 30105 Shopify samstilla greiðslur|
|**Samstilla vörulista**|Samstilla vörulista skýrslu 30115 Shopify (B2B)|
|**Samstilla verð vörulista**|Skýrsla 30116 Shopify samstillt verð vörulista (B2B)|

> [!NOTE]
> Sumar einingar gætu verið uppfærðar af nokkrum verkum, t.d. þegar þú flytur inn pantanir, eftir því hver stillingin er í **Shopify verslunarspjald**, kerfið gæti einnig flutt inn og uppfært viðskiptamanna- og/eða framleiðslugögn. Mundu að nota sama verkraðarflokkinn til að forðast árekstra.

Aðrir verkhlutar sem geta verið gagnlegir til að gera frekari vinnslu söluskjala sjálfvirka:

- Skýrsla 297 Fjöldabóka sölureikninga
- Skýrsla 296 Fjöldabóka sölupantanir

Hægt er að nota reitinn Pöntunarnr **Shopify .** Til að auðkenna söluskjöl sem voru flutt inn úr Shopify.

Til að fræðast meira um bókun sölupantana í keyrslu er farið í Til að [stofna verkraðarfærslu fyrir fjöldabókun sölupantana](../ui-batch-posting.md#to-create-a-job-queue-entry-for-batch-posting-of-sales-orders).

## <a name="to-check-the-status-of-synchronization"></a>Til að kanna stöðu samstillinga

Í hlutverki **viðskiptastjóra** býður hlutinn **Shopify Aðgerðir** upp á nokkrar bendingar sem geta hjálpað til við að finna á fljótlegan hátt hvort vandamál séu með Shopify Connector.

- **Ójafnaðar viðskiptamenn**  Shopify  eru fluttir inn en eru ekki tengdir við samsvarandi viðskiptamannsfærslu í [!INCLUDE [prod_short](../includes/prod_short.md)].
- **Ójafnaðar vörur-vara**  Shopify  er flutt inn en er ekki tengd samsvarandi birgðafærslu í [!INCLUDE [prod_short](../includes/prod_short.md)].
- **Óvinnufærðar pantanir**  Shopify  eru fluttar inn en söluskjöl í [!INCLUDE [prod_short](../includes/prod_short.md)] voru ekki stofnuð, oft vegna ómeðhinsaðra vara eða viðskiptamanna.
- **Óvinnufærðar afhendingar** - Bókaðar söluafhendingar Shopify úr pöntunum eru ekki samstilltar við Shopify.
- **AfhendingarVillur-Tengill**  Shopify  gat ekki samstillt bókaðar söluafhendingar við Shopify.
- **Samstillingarvillur** - Það eru misheppnaðar verkraðarfærslur sem tengjast samstillingu við Shopify.

## <a name="see-also"></a>Sjá einnig .

[Hafist handa með tengilinn fyrir Shopify](get-started.md)  
