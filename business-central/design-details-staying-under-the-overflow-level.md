---
title: "Hönnunarupplýsingar - undir yfirflæðisstigi | Microsoft Docs"
description: "Þegar hámarksmagn og fast endurpöntunarmagn er notað einblínir áætlanakerfið aðeins á ætlaðar birgðir í tilgreindum tímaramma. Þetta þýðir að áætlanakerfið geta stinga upp á óþarfa framboð þegar neikvæð eftirspurn eða jákvæðar breytingar á framboð koma fram utan ákveðins tímaramma."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: e532893b1823ef84256403fb7bf5ef9fabd59f2e
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-staying-under-the-overflow-level"></a>Hönnunarupplýsingar: undir yfirflæðisstigi
Þegar reglur um hámarksmagn og fast endurpöntunarmagn eru notaðar einblínir áætlanakerfið aðeins á ætlaðar birgðir í tilgreindum tímaramma. Þetta þýðir að áætlanakerfið geta stinga upp á óþarfa framboð þegar neikvæð eftirspurn eða jákvæðar breytingar á framboð koma fram utan ákveðins tímaramma. Ef, af þessum sökum, umframframboð er stungið upp á, reiknar áætlanagerðarkerfið hvaða magn framboðið skal minnka í (eða eytt) til að forðast umframframboð. Þetta magn er kallað „yfirflæðisstig“. Yfirflæðið er miðlað sem áætlanalína með **Breyta magni (Lækkun)** eða **Hætta við** aðgerð og eftirfarandi viðvörun skilaboð:  

*Athugið: Áætlaðar birgðir [xx] er hærra en yfirflæðisstig [xx] á gjalddaga [xx].*  

![Yfirflæðisstig birgða](media/supplyplanning_2_overflow1_new.png "Yfirflæðisstig birgða")  

##  <a name="calculating-the-overflow-level"></a>Reiknar yfirflæðisstig  
Yfirflæðisstigið er reiknað út á mismunandi hátt, allt eftir uppsetningu áætlana.  

### <a name="maximum-qty-reordering-policy"></a>Endurpöntunarstefna fyrir Hámarksmagn  
Yfirflæðisstig = Hámarksbirgðir  

> [!NOTE]  
>  Ef lágmarkspöntunarmagn er til, þá verður því bætt við eins og hér segir: Yfirflæðisstig = Hámarksbirgðir + lágmarkspöntunarmagn.  

### <a name="fixed-reorder-qty-reordering-policy"></a>Endurpöntunarstefna fasts endurpöntunarmagn  
Yfirflæðisstig = Endurpöntunarmagn + Endurpöntunarmark  

> [!NOTE]  
>  Ef lágmarkspöntunarmagn er yfir endurpöntunarmarkinu er því skipt út eins og hér segir: Yfirflæðisstig = Endurpöntunarmagn + lágmarkspöntunarmagn  

### <a name="order-multiple"></a>Margföld pöntun  
Ef margföld pöntun er til mun hún leiðrétta yfirflæðisstigið fyrir endurpöntunarstefnurnar fyrir bæði hámarksmagn og fast endurpöntunarmagn.  

##  <a name="creating-the-planning-line-with-overflow-warning"></a>Stofna áætlunarlínu með yfirfallsviðvörun  
Þegar núverandi framboð veldur því að áætlaðar birgðir eru meiri en yfirflæðisstigið við lok tímaramma er búin til áætlunarlína. Til að vara við hugsanlega óþarft framboð, er áætlunarlínan með viðvörunarboð, **Samþykkja aðgerðaboð** reiturinn er ekki valinn, og aðgerðaboð eru annaðhvort Hætta við eða Breyta Magni.  

### <a name="calculating-the-planning-line-quantity"></a>Reiknar magn áætlunarlínu  
Magn áætlunarlínu = Núverandi framboðsmagn – (Áætlaðar birgðir – Yfirflæðisstig)  

> [!NOTE]  
>  Eins og í öllum viðvörunarlínum verður hámarks-/lágmarkspöntunarmagn eða endurtekin pöntun hundsuð.  

### <a name="defining-the-action-message-type"></a>Skilgreina tegund aðgerðaboða  

-   Ef magn áætlunarlínu er meira en 0 eru aðgerðaboðin Breyta magni.  
-   Ef magn áætlunarlínu er jafnt og eða minna en 0 eru aðgerðaboðin Hætta við.  

### <a name="composing-the-warning-message"></a>Semja viðvörunarmerkið  
Í tilviki yfirflæðis birtir glugginn **Óraktar áætlunareiningar** viðvörun skilaboð með eftirfarandi upplýsingum:  

-   Áætlað birgðastig sem setti af stað viðvörunina.  
-   Reiknaða yfirflæðisstigið  
-   Lokadagur framboðstilviks.  

Dæmi Áætlaðar birgðir 120 eru meiri en yfirflæðisstigið 60 á 28-01-11  

## <a name="scenario"></a>Aðstæður  
Í þessari atburðarás, breytir viðskiptamaður sölupöntun frá 70 í 40 stykki milli tveggja áætlunarkeyrslna. Yfirflæðisbúnaðurinn grípur inn í til að draga úr innkaupunum sem lögð voru til fyrir upphaflega sölumagnið.  

### <a name="item-setup"></a>Vöruuppsetning  

|Endurpöntunarstefna|Hámarksmagn|  
|-----------------------|------------------|  
|Hámarksmagn pöntunar|100%|  
|Endurpöntunarmark|50|  
|Birgðir|80|  

### <a name="situation-before-sales-decrease"></a>Staða fyrir söluminnkun  

|Atburður|Breyta magni|Áætlaðar birgðir|  
|-----------|-----------------|-------------------------|  
|Dagur eitt|Ekkert|80|  
|Sala|-70|10|  
|Lok tímaramma|Ekkert|10|  
|Leggja til nýja innkaupapöntun|+90|100%|  

### <a name="situation-after-sales-decrease"></a>Staða eftir söluminnkun  

|Breyting|Breyta magni|Áætlaðar birgðir|  
|------------|-----------------|-------------------------|  
|Dagur eitt|Ekkert|80|  
|Sala|-40|40|  
|Innkaup|+90|130|  
|Lok tímaramma|Ekkert|130|  
|Stinga upp á að minnka innkaup<br /><br /> panta frá 90 til 60|-30|100%|  

### <a name="resulting-planning-lines"></a>Áætlunarlínur  
 Ein áætlunarlína (viðvörun) er stofnuð til að draga úr innkaupum um 30 úr 90 í 60 til að halda áætluðum birgðum í 100 samkvæmt yfirflæðisstiginu.  

![Áætla samkvæmt yfirflæðisstigi](media/nav_app_supply_planning_2_overflow2.png "Áætla samkvæmt yfirflæðisstigi")  

> [!NOTE]  
>  Ef búnaðurinn Yfirfall er ekki til staðar er ekki stofnuð nein viðvörun ef áætlaðar birgðir eru meiri en hámarksbirgðir. Þetta kann að valda óþörfu framboði upp á 30.  

## <a name="see-also"></a>Sjá einnig  
[Hönnunarupplýsingar: Endurpöntunarstefnur](design-details-reordering-policies.md)   
[Hönnunarupplýsingar: Áætlunarfæribreytur](design-details-planning-parameters.md)   
[Hönnunarupplýsingar: Meðhöndlun endurpöntunarstefna](design-details-handling-reordering-policies.md)   
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)

