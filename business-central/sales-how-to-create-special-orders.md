---
title: Hvernig á að stofna sérpantanir
description: Kynntu þér hvernig á að stofna sérpöntun til að tiltekið vörulistaatriði sé sent tilteknum viðskiptamanni.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: edupont
---
# <a name="create-special-orders"></a>Sérstakar pantanir stofnaðar

Hægt er að stofna sérpöntun til að tiltekið vörulistaatriði sé sent tilteknum viðskiptamanni. Birgir sendir vöruna í vöruhús og þá má senda hana áfram til viðskiptamanns, annaðhvort sérstaklega eða með annarri pöntun.  

Sérpantanir gefa til kynna að innkaupa- og sölupöntun séu tengdar til að tryggja að sértækt vörulistaatriði sé tínt og afhent viðskiptamanni.  

Þessa aðgerð er ekki hægt að nota nema búið sé að setja upp spjald fyrir viðskiptamann, lánardrottin og vöru svo hægt sé að vinna pöntunina.  

## <a name="to-create-a-special-order"></a>Stofnuð sérpöntun:

1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sölupöntun** og velja síðan viðkomandi tengil.  
2. Valið er aðgerðin **Nýtt**. Búin er til ný  sölupöntun fyrir vöruna. Frekari upplýsingar eru í [Selja vörur](sales-how-sell-products.md).
3.  Á flýtiflipanum **Línur** er fyllt út í sölulínuna. Í reitnum **Innkaupakóti** veljið innkaupakóta sem er með reitinn **Sérpöntun** valinn.

    Nú þarf að stofna innkaupapöntun út frá innkaupatillögu.  
4. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnublað beiðni** og velja síðan viðkomandi tengil.  
5. Veljið aðgerðina **Sérpöntun** og veljið síðan aðgerðina **sækja sölupöntun**.  
6.  Á síðunni **Sækja sölupantanir** sýna niðurstöður þar sem **Númer fylgiskjals** er sölupöntunarnúmeri. Velja hnappinn **Í lagi**. Kerfið stofnar innkaupatillögulínu vegna vörunnar.  
7.  Í innkaupatillögulínunni skal velja **Nýtt** í reitnum **Aðgerðarboð**.  
8.  Á síðunni **Innkaupatillaga** veljið aðgerðina **Framkvæma aðgerðaboð**. Síðan **Framkv. aðgerðaboð - Beiðni** opnast. Velja hnappinn **Í lagi**.  

    Þá birtast boð þess efnis að innkaupapantanir hafi verið stofnaðar. Velja hnappinn **Í lagi**.  

Tekið er tillit til stofnaðrar innkaupapöntunar fyrir sérpöntun af kerfinu þar sem hún jafnar framboð og eftirspurn. Það er, innkaupapöntun (framboð) helst tengd við sölupöntun (eftirspurn) jafnvel þó innkaupapöntunin gæti lagt til fyrri eftirspurnar. Nánari upplýsingar eru í [Upplýsingar um hönnun: Endurpöntunarstefnur](design-details-reservation-order-tracking-and-action-messaging.md).  

> [!NOTE]  
>  Ekki er hægt að nota sérpöntunarkostinn ef varan er þegar frátekin. Þess vegna, fyrir vörur sem eru seldar með sérpöntunum, gakktu úr skugga um að **Frátekning** reiturinn á birgðaspjaldinu sé ekki stilltur á **Alltaf**.  

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft þjálfun](/training/modules/create-sales-documents-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig .

[Vinna með vörulista](inventory-how-work-nonstock-items.md)  
[Sala](sales-manage-sales.md)  
[Beinar sendingar](sales-how-drop-shipment.md)   
[Hönnunarupplýsingar: Endurpöntunarstefnur](design-details-reservation-order-tracking-and-action-messaging.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
