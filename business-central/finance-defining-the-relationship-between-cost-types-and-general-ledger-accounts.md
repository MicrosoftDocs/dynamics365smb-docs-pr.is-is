---
title: "Skilgreining á venslum milli kostnaðargerða og fjárhagsreikninga | Microsoft Docs"
description: "Lærðu hvernig á að skilgreina tengsl milli kostnaðartegundarinnar og fjárhagsreikningsins."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost types, general ledger
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 7709edb214804f52ee9b495c43b5302e2a23bd6b
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="defining-the-relationship-between-cost-types-and-general-ledger-accounts"></a>Skilgreining á venslum milli kostnaðargerða og fjárhagsreikninga
Tengsl milli kostnaðartegundarinnar og almenna fjárhagslykilsins eru stofnuð í kostnaðartegundinni og í fjárhagsreikningnum.  

* Reiturinn **Fjárhagsreikningssvið** í töflunni **Kostnaðargerð** mælir fyrir um hvaða fjárhagsreikningur tilheyrir tegund kostnaðar.  
* Reiturinn **Númer kostnaðartegundar** í reikningatöflu mælir fyrir um hvaða tegund kostnaðar fjárhagsreikningur tilheyrir.  

Þessir tveir reitir eru fylltir út sjálfkrafa þegar aðgerðin **Sækja kostnaðargerðir úr bókhaldslykli** er notuð.  

## <a name="relationship-between-general-ledger-accounts-and-cost-types"></a>Tengsl milli fjárhagsreiknings og kostnaðartegunda  
Til eru n:1 vensl milli fjárhagsreikninga og kostnaðargerðar. Nokkrir fjárhagsreikningar geta tilheyrt einni kostnaðartegund, en hver fjárhagsreikningur tilheyrir aðeins einni kostnaðargerð. Eftirfarandi tafla lýsir upplýsingunum í tengslunum.  

|Tengsl|**Reikningsbil fjárhags**|**Kostnaðartegundarnr.**|  
|------------------|------------------------------------------------|-------------------------------------------|  
|Einn fjárhagsreikningur fyrir hverja kostnaðartegund|Einn fjárhagsreikningur|Ein kostnaðartegund|  
|Nokkrir fjárhagsreikningar fyrir hverja kostnaðartegund|Svið fjárhagsreikninga, til dæmis 7110..7193 fyrir hvern fjárhagsreikning|Fyrir hvern fjárhagsreikning í bilinu, er aðeins ein kostnaðartegund|  
|Kostnaðartegundir án samsvarandi tengsla við fjárhaglykla|<Empty>||  
|Fjárhagsreikningar með færslur sem ekki verið fluttar||<Empty>|  

## <a name="cost-types-without-a-relationship-to-the-general-ledger"></a>Kostnaðartegundir án tengsla við fjárhag  
Kostnaðartegund má ekki hafa tengsl við fjárhagsreikninga ef annað af eftirfarandi skilyrðum á við:  

* Reikningar fyrir rekstarbókhald, eins og Reikn. vextir og Afskriftir, taka einungis kostnað frá rekstrarbókhaldi.  
* Aukakostnaðartegundir, t.d. kostnaðargerðir 9901, 9902 og 9903 í [!INCLUDE[d365fin](includes/d365fin_md.md)]-gagnagrunninum, eru notaðir sem kredit- og debetreikningar fyrir úthlutanir.  
* Hjálparreikningurinn, 9920 í [!INCLUDE[d365fin](includes/d365fin_md.md)] gagnagrunninn, inniheldur raunverulegar uppsafnanir sem sýna muninn milli kostnaðar og gjalda úr fjárhag.  

## <a name="see-also"></a>Sjá einnig  
[Kostnaðarreikningur](finance-manage-cost-accounting.md)  
[Uppsetning kostnaðarbókhalds](finance-set-up-cost-accounting.md)   
[Um kostnaðarbókhald](finance-about-cost-accounting.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

