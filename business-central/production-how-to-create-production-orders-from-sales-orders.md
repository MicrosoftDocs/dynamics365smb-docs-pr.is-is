---
title: Búa til framleiðslupantanir úr sölupöntunum
description: Lærðu mismunandi leiðir til að stofna framleiðslupantanir fyrir framleiddar vörur beint úr sölupöntunum.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/27/2023
ms.custom: bap-template
ms.search.form: '99000883, 99000884,'
---
# <a name="create-production-orders-from-sales-orders"></a><a name="create-production-orders-from-sales-orders"></a><a name="create-production-orders-from-sales-orders"></a>Búa til framleiðslupantanir úr sölupöntunum

Hægt er að búa til framleiðslupantanir fyrir framleiðsluvörur beint frá sölupöntunum.  

## <a name="to-create-a-production-order-from-a-sales-order"></a><a name="to-create-a-production-order-from-a-sales-order"></a><a name="to-create-a-production-order-from-a-sales-order"></a>Framleiðslupantanir búnar til í sölupöntunum:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.  
2. Veldu sölupöntun sem þú vilt búa til framleiðslupöntun fyrir.  
3. Veldu aðgerðina **Áætlun**.  **Síðan áætlun**  sölupöntunar sýnir ráðstöfunarmagn vörunnar.  
4. Veldu aðgerðina **Stofna framl.pöntun**.  
5. Velja skal stöðu og pöntunartegund.  
6. Veldu hnappinn **Já** til að búa til eina eða fleiri framleiðslupantanir fyrir línurnar sem eru með **Framl.pöntun** í reitnum **Áfyllingarkerfi**.

    > [!NOTE]  
    > Eftirspurnarlínur sem hafa  **framl. pöntun**  í  **áfyllingarkerfisvæðinu**  tákna undirliggjandi framleiðslupantanir. Eftir að þessar framleiðslupantanir eru myndaðar, munið að auðkenna alla óuppfyllta eftirspurn íhluta eftir þeim.  **Notaðu síðuna pantanáætlanagerð**  eða  **aðgerðina endurkrafa**  til að auðkenna óuppfyllta eftirspurn.
    >
    > Þegar stofnaðar eru framleiðslupantanir fyrir sölupantanir með síðunni áætlun sölupantana eru tenglar til pöntunarpöntunar notaðir milli eftirspurnar og framboðs. Þegar pöntunartenglar eru til staðar er áætlanakerfið ekki með tengdu framboði eða birgðum í mótunarferlinu. Til að fræðast meira um jöfnun er farið í  [pantanatengingu](design-details-central-concepts-of-the-planning-system.md#order-to-order-links) til að panta.

## <a name="order-type"></a><a name="order-type"></a><a name="order-type"></a>Gerð pöntunar

Eftirfarandi tafla lýsir tveimur leiðum til að stofna framleiðslupantanir.

|Valkostur|Description|
|------|-----------|
|Vörupöntun|Ein framleiðslupöntun er stofnuð fyrir hverja vöru sem er táknuð með línu á  **síðunni áætlun**  sölupantana.|
|Verkefnispöntun|Ein samvalapöntun framleiðslupöntunar er stofnuð fyrir allar vörur sem eru  **táknaðar með línum á síðunni áætlun**  sölupöntunar. Þegar verkpantanir eru notaðar er  **reiturinn Tegund**  uppruna í framleiðslupöntuninni  **í söluhausnum**. Pöntunin er með eina línu fyrir hverja vöru sölulínu sem þarf að framleiða.|

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Sjá einnig

[Uppsetning framleiðslu](production-configure-production-processes.md)  
[Framleiðsla](production-manage-manufacturing.md)  
[Birgðir](inventory-manage-inventory.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)  
[Uppsetning bestu venja: Framboðsáætlun](setup-best-practices-supply-planning.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
