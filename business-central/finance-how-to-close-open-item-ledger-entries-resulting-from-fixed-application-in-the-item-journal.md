---
title: Loka birgðafærslum sem voru búnar til með notkun fastrar jöfnunar
description: Lærðu hvernig þú getur stofnað handvirkt fasta jöfnun milli færslu á innleið og upphaflegrar færslu á útleið í birgðabók.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: 40
ms.date: 07/30/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Loka opnum birgðafærslum sem eru afleiðingar fastrar jöfnunar í birgðabókinni

Nota skal reitinn **Jafnað frá færslu** á síðunni **Birgðabók** til að stofna fasta jöfnun milli færslu á innleið og upphaflegrar færslu á útleið. Til dæmis til að leiðrétta viðskipti á útleið eða til að vinna úr skilum þeirra.  

> [!IMPORTANT]  
> Fastar jafnanir gerðar með þessum hætti nota aðeins kostnað, ekki magn. Í samræmi við það lokar bókaða jákvæða birgðafærslan ekki útleiðarfærslu sem er notuð og helst sjálf opin. Þetta á einnig við þegar föst jöfnun fyrir jákvæða færslu er bókuð í neikvæða færslu sem ekki hefur verið lokað af venjulegri jákvæðri færslu, þá haldast bæði neikvæða og jákvæða færslan opnar.  
>
> Þetta þýðir einnig að ekki er hægt að loka birgðatímabili sé slík færsla til.  

Hægt er að breyta og endurjafna jöfnunarfærslur við ákveðnar aðstæður með því að nota síðuna **Vinnublað jöfnunar**.  

Eftirfarandi ferli sýnir hvernig eigi að loka slíkum færslum með því að framkvæma tvær leiðréttar bókanir í birgðabókina.  

## Til að loka opnum birgðahöfuðbókarfærslum sem verða til úr fastri jöfnun í birgðabókinni  

1. Nota skal reitinn **Jafnað frá færslu** til að bóka jákvæða leiðréttingu með samsvarandi magn. Þetta lokar upprunalegu neikvæðu leiðréttingarfærslunni með fastri jöfnun.  

    Reiturinn **Jafnað frá færslu** tilgreinir númer útleiðarfærslu birgðahöfuðbókar sem hefur kostnað sem sendur er í innleiðarfærslu birgðahöfuðbókar þegar innleiðarfærsla af gerðinni **Aukning** eða **Innkaup** er bókuð í birgðabókinni.  
2. Nota skal reitinn **Jafnað frá færslu** til að bóka neikvæða leiðréttingu. Þetta lokar upprunalegu jákvæðu leiðréttingarfærslunni með fastri jöfnun.  

    Reiturinn **Jafna færslu** tilgreinir ef magnið í birgðabókarlínunni á að jafnast við fylgiskjal sem þegar er bókað. Ef svo er skal færa inn færslunúmer birgðafærslunnar sem jafna á birgðabókarlínuna við.

## Sjá einnig .

[Fjarlægja og endurjafna birgðafærslur](finance-how-to-remove-and-reapply-item-entries.md)    
[Vinna vöruskil og afturköllun sölu](sales-how-process-sales-returns-cancellations.md)    
[Uppsetning birgðavirðis og kostnaðarútreiknings](finance-set-up-inventory-valuation-and-costing.md)    
[Birgðakostnaði stjórnað](finance-manage-inventory-costs.md)    
[Hönnunarupplýsingar: Aðferð kostnaðarútreiknings](design-details-costing-methods.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]