---
title: Vinna við birgðatímabil
description: Hægt er að stjórna tímarammanum þar sem fólk getur bókað breytingar á birgðum með því að skilgreina birgðatímabil.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'inventory, periods'
ms.search.form: 5828
ms.date: 07/29/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="work-with-inventory-periods"></a>Vinna við birgðatímabil

Birgðatímabil skilgreina tímabil þar sem hægt er að bóka breytingar á birgðum. Birgðatímabil afmarkast af dagsetningunni sem því lýkur á. Þegar birgðatímabili er lokað er ekki hægt að bóka neinar breytingar á birgðum, hvort sem er áætlað eða reikningsfært, fyrir þessa lokadagsetningu. Ekki er hægt að bóka ný gildi í birgðir fyrir lokadagsetninguna. Ef opnar birgðafærslur eru í lokuðu tímabili, sem þýðir jákvætt magn sem ekki hefur verið jafnað við færslur á útleið, er samt hægt að jafna magn á útleið við þessar færslur, jafnvel þótt tímabilið sé lokað.  

Eftirfarandi hlutar útskýra hvernig á að standa að:

* Stofna birgðatímabil.  
* Lokun birgðatímabila.  
* Enduropna birgðatímabil.  

## <a name="to-create-an-inventory-period"></a>Til að stofna birgðatímabil

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Birgðatímabil** og velja síðan viðkomandi tengil.  
2. Stofnið nýja línu.  
3. Í reitinn **Lokadagsetning** er slegin inn síðasta dagsetningin í birgðatímabilinu sem ætlunin er að skilgreina. Þegar tímabilinu er lokað verður ekki hægt að bóka breytingar á birgðum fyrir þessa dagsetningu.  
4. Færa inn lýsandi heiti í reitinn **Heiti**. Velja hnappinn **Í lagi**.  

## <a name="to-close-inventory-periods"></a>Birgðatímabilum lokað

Reiturinn **Lokað** gefur til kynna hvort birgðatímabilið er lokað fyrir breytingum á birgðagildum eður ei. Ekki er hægt að breyta þessum reit.  

Hægt er að loka hvaða birgðatímabili sem er, ef eftirfarandi á við:  

* Engar birgðafærslur eru opnar það er að segja ekki neikvætt birgðamagn, á því tímabili.  
* Kostnaður allra vara hefur verið leiðréttur með keyrslunni **Leiðr. kostnað - Birgðafærslur**.  

Þetta þýðir að jafna þarf allt færslumagn á útleið, eins og magnið í sölupöntunum, millifærslum á útleið, sölureikningsfærslum, vöruskilum eða innkaupakreditreikningum við magn sem er fyrir í birgðum.  

### <a name="to-close-an-inventory-period"></a>Til að loka birgðatímabili

1. Áður en birgðatímabili er lokað er **Leiðr. kostnað - Birgðafærslur** aðgerðin valin til að tryggja það að allar kostnaðarleiðréttingar séu bókaðar.

    Keyrð **er skýrslan Loka birgðatímabili – Prófun** til að ákvarða hvort einhverjar opnar birgðafærslur á útleið séu innan birgðatímabilsins eða einhverjar vörur þar sem kostnaður hefur ekki verið leiðréttur.  
2. Veljið aðgerðina **Prófunarskýrsla**.  

    Keyrð er keyrslan **Bóka birgðabreytingar** til að tryggja það að allur kostnaður sé bókaður í fjárhaginn.  
3. Velja skal aðgerðina **Bóka birgðir í fjárhag**.  
4. Á síðunni **Birgðatímabil** skal velja birgðatímabilið sem á að loka.  
5. Velja aðgerðina **Loka tímabili**. Þegar birgðatímabilinu hefur verið lokað er ekki hægt að bóka breytingar á birgðum fyrir lokadagsetninguna. Leiðrétta þarf kostnað allra vara með keyrslunni **Leiðr. kostnað - Birgðafærslur** áður en birgðatímabilinu er lokað.  
6. Veldu hnappinn **Já** til að staðfesta það að ætlunin sé að loka tímabilinu, eða veldu **Nei** til að hætta við lokunina.  
7. Birgðatímabili er lokað og staðfestingarboð birtast þegar því er lokið.  

## <a name="reopening-inventory-periods"></a>Enduropnun birgðatímabila
Þegar birgðatímabilinu hefur verið lokað er ekki hægt að eyða birgðatímabilinu. Hægt er hins vegar að enduropna það til að leyfa bókun áður en að lokadagsetningu birgðatímabilsins er komið. Enduropnun tímabils enduropnar líka öll birgðatímabil með lokadagsetningar seinni en það tímabil sem er enduropnað.  

### <a name="to-reopen-an-inventory-period"></a>Til að enduropna birgðatímabil
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Birgðatímabil** og velja síðan viðkomandi tengil.  
2. Velja skal birgðatímabilið sem á að enduropna.  
3. Velja aðgerðina **Enduropna tímabili**. Staðfesta að það eigi að enduropna tímabilið.  
4. Allir birgðahaldstímar með lokadagsetningu sem kemur síðar en valið tímabilið eru enduropnaðir.  

## <a name="see-also"></a>Sjá einnig .
[Upplýsingar um hönnun: Birgðatímabil](design-details-inventory-periods.md)    
[Fjármál](finance.md)    
[Birgðir](inventory-manage-inventory.md)    
[Vinna með Financials](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
