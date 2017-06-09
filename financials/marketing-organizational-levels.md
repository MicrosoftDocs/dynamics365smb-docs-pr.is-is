---
title: "Setja upp skipulagsstig fyrir tengiliði | Microsoft Docs"
description: "Lýsir skipulagsstigi fyrir tengiliði í fjármálum"
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: bde26a2d5fcb7ec10dcd70fdd30c74893bcb34d5
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-organizational-levels-for-contact-persons"></a>Uppsetning stjórnunarstiga fyrir tengiliði
Hægt er að úthluta stjórnunarstigum á tengiliði til að tilgreina hvaða stöðu þeir hafa innan fyrirtækis, til dæmis forstjóri. Þessar upplýsingar er hægt að nota þegar færðar eru inn upplýsingar um tengiliði.

Notkun viðskiptatengsla á tengiliði er tveggja þrepa ferli. Fyrst að skilgreina viðskiptatengslakóðann. Aðeins þarf að framkvæma þetta skref í eitt skipti fyrir hver viðskiptatengsl. Þegar kominn er viðskiptatengslakóði er hægt að byrja að úthluta kóðanum til tengiliða.

## <a name="to-define-an-organizational-level-code"></a>skilgreining viðskiptatengslakóða
Viðskiptatengslakóði skilgreinir tegund eða flokk stjórnunarstigs, eins og framkvæmdastjóri eða fjármálastjóri. Hægt er að hafa nokkra viðskiptatengslakóða. Glugginn **Stjórnunarstig** er notaður til að skilgreina stjórnunarstigið.

1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Stjórnunarstig**, og velja síðan viðeigandi tengil.
2. Valið er **Nýtt** aðgerð og fyllt er inn kóði og lýsing. Kóðinn má vera mest 11 stafir, og getur verið hvaða samasetning sem er af tölustafir og bókstafir.

## <a name="to-assign-organizational-levels-to-a-contact-person"></a>að úthluta skipulagsstigum til tengiliðs
Aðeins er hægt að úthluta stjórnunarstigum á einstaklinga, ekki á fyrirtæki. Aðeins er hægt að úthluta einu stjórnunarstigi á hvern tengilið.

1. Tengiliðurinn er opnaður.
2. Í reitnum **Stjórnunarstig** skal velja kóðann sem á að úthluta.

Þegar tengiliðum hefur verið úthlutað stjórnunarstigi er hægt að nota þær upplýsingar til að stofna hluta.

Eftir að tengiliðum hefur verið úthlutað starfsábyrgðum er hægt að nota þessar upplýsingar til að velja tengiliði í hluta. Sjá frekari upplýsingar hér [Hvernig á að bæta tengiliðum við hluta:](marketing-add-contact-segment.md)

## <a name="see-also"></a>Sjá einnig
[Fyrirtækjatengiliðir stofnaðir](marketing-create-contact-companies.md)  
[Einstaklingstengiliðir stofnaðir](marketing-create-contact-persons.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

