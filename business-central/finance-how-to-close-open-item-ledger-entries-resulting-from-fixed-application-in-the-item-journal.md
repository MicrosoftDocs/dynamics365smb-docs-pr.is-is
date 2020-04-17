---
title: Hvernig á að loka opnum færslum birgðahöfuðbókar vegna fastrar jöfnunar í birgðabók | Microsoft Docs
description: Nota skal reitinn **Jafnað frá færslu** á síðunni **Birgðabók** til að stofna fasta jöfnun milli færslu á innleið og upphaflegrar færslu á útleið. Til dæmis til að leiðrétta viðskipti á útleið eða til að vinna úr skilum þeirra.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 4cec244feb09cf490692e92aa3b58429d4c3e16d
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3183453"
---
# <a name="close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a>Loka opnum færslum birgðahöfuðbókar vegna fastrar jöfnunar í birgðabók
Nota skal reitinn **Jafnað frá færslu** á síðunni **Birgðabók** til að stofna fasta jöfnun milli færslu á innleið og upphaflegrar færslu á útleið. Til dæmis til að leiðrétta viðskipti á útleið eða til að vinna úr skilum þeirra. Frekari upplýsingar eru í Jafnað frá færslu.  

> [!IMPORTANT]  
>  Fastar jafnanir gerðar með þessum hætti nota aðeins kostnað, ekki magn. Í samræmi við það lokar bókaða jákvæða birgðafærslan ekki útleiðarfærslu sem er notuð og helst sjálf opin. Þetta á einnig við þegar föst jöfnun fyrir jákvæða færslu er bókuð í neikvæða færslu sem ekki hefur verið lokað af venjulegri jákvæðri færslu, þá haldast bæði neikvæða og jákvæða færslan opnar.  
>   
>  Þetta þýðir einnig að ekki er hægt að loka birgðatímabili sé slík færsla til.  

Eftirfarandi ferli sýnir hvernig eigi að loka slíkum færslum með því að framkvæma tvær leiðréttar bókanir í birgðabókina.  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a>Til að loka opnum birgðahöfuðbókarfærslum sem verða til úr fastri jöfnun í birgðabókinni  

1.  Nota skal reitinn **Jafnað frá færslu** til að bóka jákvæða leiðréttingu með samsvarandi magn. Þetta lokar upprunalegu neikvæðu leiðréttingarfærslunni með fastri jöfnun.  
2.  Nota skal reitinn **Jafnað frá færslu** til að bóka neikvæða leiðréttingu. Þetta lokar upprunalegu jákvæðu leiðréttingarfærslunni með fastri jöfnun.  

## <a name="see-also"></a>Sjá einnig  
[ Fjarlægja og endurjafna birgðabókafærslur](finance-how-to-remove-and-reapply-item-entries.md)  
 [Vinna söluskil eða afturkallanir](sales-how-process-sales-returns-cancellations.md)   
 [Uppsetning birgðaverðmats og kostnaðar](finance-set-up-inventory-valuation-and-costing.md)   
 [Birgðakostnaði stjórnað](finance-manage-inventory-costs.md)   
 [Hönnunarupplýsingar: Aðferð kostnaðarútreiknings](design-details-costing-methods.md)
