---
title: "Setja upp stjórnunarstig fyrir tengiliði| Microsoft Docs"
description: "Hægt er að skilgreina stjórnunarstig og úthluta því til tengiliðs til að gefa til kynna stöðuna sem hann hefur í fyrirtækinu, til dæmis forstjóri."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: d101076c8a51b1c7a79606d207f79a826c89bf29
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-organizational-levels-for-contact-persons"></a>Hvernig skal: Setja upp stjórnunarstig fyrir tengiliði
Hægt er að úthluta stjórnunarstigum á tengiliði til að tilgreina hvaða stöðu þeir hafa innan fyrirtækis, til dæmis forstjóri. Þessar upplýsingar er hægt að nota þegar færðar eru inn upplýsingar um tengiliði.

Notkun viðskiptatengsla á tengiliði er tveggja þrepa ferli. Fyrst að skilgreina viðskiptatengslakóðann. Aðeins þarf að framkvæma þetta skref í eitt skipti fyrir hver viðskiptatengsl. Þegar kominn er viðskiptatengslakóði er hægt að byrja að úthluta kóðanum til tengiliða.

## <a name="to-define-an-organizational-level-code"></a>Skilgreining viðskiptatengslakóða
Viðskiptatengslakóði skilgreinir tegund eða flokk stjórnunarstigs, eins og framkvæmdastjóri eða fjármálastjóri. Hægt er að hafa nokkra viðskiptatengslakóða. Glugginn **Stjórnunarstig** er notaður til að skilgreina stjórnunarstigið.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Stjórnunarstig** og velja svo viðeigandi tengil.
2. Valið er **Nýtt** aðgerð og fyllt er inn kóði og lýsing. Kóðinn má vera mest 11 stafir, og getur verið hvaða samasetning sem er af tölustafir og bókstafir.

## <a name="to-assign-organizational-levels-to-a-contact-person"></a>Að úthluta skipulagsstigum til tengiliðs
Aðeins er hægt að úthluta stjórnunarstigum á einstaklinga, ekki á fyrirtæki. Aðeins er hægt að úthluta einu stjórnunarstigi á hvern tengilið.

1. Tengiliðurinn er opnaður.
2. Í reitnum **Stjórnunarstig** skal velja kóðann sem á að úthluta.

Þegar tengiliðum hefur verið úthlutað stjórnunarstigi er hægt að nota þær upplýsingar til að stofna hluta.

Eftir að tengiliðum hefur verið úthlutað starfsábyrgðum er hægt að nota þessar upplýsingar til að velja tengiliði í hluta. Sjá frekari upplýsingar hér [Hvernig á að bæta tengiliðum við hluta:](marketing-add-contact-segment.md)

## <a name="see-also"></a>Sjá einnig
[Fyrirtækjatengiliðir stofnaðir](marketing-create-contact-companies.md)  
[Einstaklingstengiliðir stofnaðir](marketing-create-contact-persons.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

