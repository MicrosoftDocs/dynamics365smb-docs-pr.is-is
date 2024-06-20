---
title: Búa til framleiðslupantanir úr sölupöntunum
description: Læra mismunandi leiðir til að stofna framleiðslupantanir fyrir framleiddar vörur beint úr sölupöntunum.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 02/27/2023
ms.custom: bap-template
ms.search.form: '99000883, 99000884,'
ms.service: dynamics-365-business-central
---
# <a name="create-production-orders-from-sales-orders"></a>Búa til framleiðslupantanir úr sölupöntunum

Hægt er að búa til framleiðslupantanir fyrir framleiðsluvörur beint frá sölupöntunum.  

## <a name="to-create-a-production-order-from-a-sales-order"></a>Framleiðslupantanir búnar til í sölupöntunum:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.  
2. Veldu sölupöntun sem þú vilt búa til framleiðslupöntun fyrir.  
3. Veldu aðgerðina **Áætlun**. Síðan **Áætlun** sölupöntunar sýnir það sem er til ráðstöfunar af vörunni.  
4. Veldu aðgerðina **Stofna framl.pöntun**.  
5. Velja skal stöðu og pöntunartegund.  
6. Veldu hnappinn **Já** til að búa til eina eða fleiri framleiðslupantanir fyrir línurnar sem eru með **Framl.pöntun** í reitnum **Áfyllingarkerfi**.

    > [!NOTE]  
    > Eftirspurnarlínur sem eru með **framleiðslupöntun** í reitnum **Áfyllingarkerfið** tákna undirliggjandi framleiðslupantanir. Þegar þessar framleiðslupantanir hafa verið búnar til þarf að muna að auðkenna óuppfyllta eftirspurn íhluta eftir þeim. Nota skal síðuna **Pantanaáætlun** eða **Enduráætla** aðgerð til að auðkenna óuppfyllta eftirspurn.
    >
    > Þegar framleiðslupantanir eru búnar til fyrir sölupantanir með síðunni Áætlun sölupöntunar er tenglum eftir pöntunum beitt milli eftirspurnar og framboðs. Þegar pantanatenglar eru til staðar tekur áætlunarkerfið ekki með tengdar framboð eða birgðir í mótfærsluferlinu. Nánari upplýsingar um jöfnun fást með því að fara á [tengla fyrir pöntun.til að fá nánari](design-details-central-concepts-of-the-planning-system.md#order-to-order-links) upplýsingar um jöfnun.

## <a name="order-type"></a>Gerð pöntunar

Eftirfarandi tafla lýsir tveimur leiðum til að stofna framleiðslupantanir.

|Valkostur|Heimildasamstæða|
|------|-----------|
|Vörupöntun|Ein framleiðslupöntun er stofnuð fyrir hverja vöru sem lína sýnir á síðunni **Áætlun** sölupöntunar.|
|Verkpöntun|Ein framleiðslupöntun samvals er stofnuð fyrir allar vörur sem línur birtast á síðunni **Áætlun** sölupöntunar. Þegar verkefnispantanir eru notaðar er **í reitnum** Tegund **uppruna í framleiðslupöntuninni Söluhaus**. Pöntunin er með eina línu fyrir hverja sölulínuvöru sem þarf að framleiða.|

## <a name="see-also"></a>Sjá einnig

[Uppsetning framleiðslu](production-configure-production-processes.md)  
[Framleiðsla](production-manage-manufacturing.md)  
[Birgðir](inventory-manage-inventory.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)  
[Uppsetning bestu venja: Framboðsáætlun](setup-best-practices-supply-planning.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
