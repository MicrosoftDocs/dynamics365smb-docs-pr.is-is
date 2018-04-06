---
title: "Hvernig á að ganga frá vörum með vöruhúsafrágangi | Microsoft Docs"
description: "Þegar birgðageymslan er sett þannig upp að hún krefst vöruhúsafrágangs- og vöruhúsamóttökuvinnslu eru vöruhúsafrágangsskjöl aðgerðin notuð til að stjórna frágangi á vörum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/31/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: bf7b58fad1aa587079b51b505e9d757bb66f39c9
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="put-items-away-with-warehouse-put-aways"></a>Ganga frá vörum með vöruhúsafrágangi
Þegar birgðageymslan er sett þannig upp að hún krefst vöruhúsafrágangs- og vöruhúsamóttökuvinnslu eru vöruhúsafrágangsskjöl aðgerðin notuð til að stjórna frágangi á vörum.  

Þegar vöruhúsamóttaka er bókuð uppfærir kerfið upprunaskjölin, s.s. innkaup, millifærslu inn eða söluvöruskilapöntun, bókar móttekið magn á birgðahöfuðbók og sendir línurnar um vörurnar sem mótteknar voru í frágangsaðgerð vöruhússins. Ef innanhússfrágangur og tínsla er notuð getur innanhússfrágangurinn einnig stofnað línur fyrir frágang.  

Það fer eftir uppsetningu vöruhússins hvort línurnar verða tiltækar á vinnublaði frágangs eða notaðar til að stofna frágangsleiðbeiningar strax. Frekari upplýsingar, sjá [Áætla frágang á vinnublöðum](warehouse-how-to-plan-put-aways-in-worksheets.md).  

Auk staðlaðra aðferða til að stofna vöruhúsafrágang eins og lýst er í þessu efnisatriði er hægt að hægt að stofna frágang úr tengdri bókaðri vöruhúsamóttöku. Þetta kemur að notum ef búið er að eyða frágangslínum, eða ef notuð hafa verið beinn frágangur og tínsla og ákvörðun hefur verið tekin um að nota ekki vinnublað frágangs, vegna þess að hægt að stofna eða endurstofna frágangsleiðbeiningar fyrir bókaðar móttökulínur.  

## <a name="to-put-items-away-without-directed-put-away-and-pick"></a>Frágangur á vörum án beins frágangs og tínslu  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Frágangur** og velja svo viðeigandi tengil.  
2.  Opnar vöruhúsafrágang sem er tilbúin til meðhöndlunar.  

    Hægt er að raða frágangslínunum eftir ýmsum skilyrðum, til dæmis vöru, hillunúmeri eða lokadagsetningu og betrumbæta þannig frágangsferlið.  
3.  Í hverri línu í reitnum **Magn til afgreiðslu** er ritað magnið sem ganga skal frá.  
4.  Þegar lokið hefur verið við að ganga frá vörunum er smellt á **Skrá frágang** aðgerðina til að skrá það að aðgerðinni sé lokið og gera vörurnar tiltækar fyrir tínslu.  

## <a name="to-put-items-away-with-directed-put-away-and-pick"></a>Frágangur á vörum með beinum frágangi og tínslu  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Frágangur** og velja svo viðeigandi tengil.
    Hafi frágangsleiðbeiningar verið stofnaðar sést frágangur í vöruhúsi.  
2.  Opnar vöruhúsafrágang sem á að vinna með.  
3.  Ef það er krafa vöruhússins er kenni notanda fært inn í flýtiflipann **Almennt** þegar byrjað er að vinna við tiltekinn frágang.  
4.  Aðgerðirnar Taka og Setja í reitnum **Aðgerð** eru framkvæmdar.  

    Bent er á að hver móttökulína verður að minnst tveimur línum í frágangi vöruhúss:  

    -   Fyrsta línan sem hefur **Taka** í reitnum **Aðgerð** sýnir hvar vörurnar eru staðsettar á móttökusvæðinu. Ekki er hægt að breyta reitunum svæði og hólf á þessari línu.  
    -   Næstu línur þar sem **Setja** er í reitnum **Aðgerð** sýna hvar setja skal vörurnar í geymslu vöruhússins. Ef mikið af vörum hefur borist vöruhúsinu í einni móttökulínu gæti þurft að ganga frá þeim í mörg hólf og þá er ein Setja lína fyrir hvert hólf.  

        Ef Taka- og Setja-línurnar fyrir hverja móttöku koma ekki hver á eftir annarri eins og óskað er eftir er hægt að raða línunum með því að velja **Vara** í reitnum **Röðunaraðferð** á flýtiflipanum **Almennt**.  

        Ef skipulag sjálfs vöruhússins endurspeglar hólfaflokkunina er hægt að nota röðunaraðferðina **Hólfaflokkun** til að útbúa frágangsleið sem dregur úr snúningum í vöruhúsinu.  

5.  Þegar allar vörurnar hafa verið settar í hólf samkvæmt skal velja aðgerðina **Skrá frágang**.  

Í birgðageymslum sem eru settar upp þannig að þær noti beinan frágang og tínslu, eru eftirfarandi stillingar forkröfur fyrir ferlinu hér að framan:  

- Frágangssniðmát er sett upp: Frekari upplýsingar eru í [Setja upp frágangssniðmát](warehouse-how-to-set-up-put-away-templates.md).  
- Þyngd, rúmmál og sérstakar geymsluþarfir vörunnar eða birgðaeiningarinnar eru skilgreindar. Frekari upplýsingar eru í Heildarþyngd.  
- Afkastagetan, hólfategund og hólfaflokkun hólfanna. Nánari upplýsingar eru í Hólfaflokkun.  

Tekið er mið af hólfaflokkuninni þegar fleiri en eitt hólf uppfylla skilyrði frágangssniðmátsins. Ef bæði skilyrði frágangssniðmáts og hólfaflokkun eru þau sömu er valið hólf með hærra númeri.

## <a name="to-create-a-put-away-from-a-posted-receipt"></a>Til að búa til frágang úr bókaðri uppskrift  
 Ef birgðageymsla notar bæði frágangsvinnslu og móttökuvinnslu og búið er að eyða frágangslínum, eða ef notuð hafa verið beinn frágangur og tínsla og ákvörðun hefur verið tekin um að nota ekki vinnublað frágangs, þá er hægt að stofna eða endurstofna frágangsleiðbeiningar fyrir bókaðar móttökulínur.

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **bókað vöruhúsamóttaka** og velja svo viðeigandi tengil.  
2.  Velja skal bókaða móttöku sem hugsanlega þarf að ganga frá.  
3.  Velja aðgerðina **Spjald**.  

    Ef reiturinn **Staða fylgiskjals** er auður hefur alls ekki verið gengið frá móttökunni. Annars sýnir reiturinn að móttaka hafi verið frágengin að hluta eða öllu leyti.  

4.  Ef gengið hefur verið frá móttökunni að hluta eða alls ekki er smellt á aðgerðina **stofna frágang**.  
5.  Beiðnigluggi keyrslunnar er fylltur út til að stofna fráganginn eins og best þykir og síðan er **Í lagi** hnappurinn valinn.   

## <a name="see-also"></a>Sjá einnig  
[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
[Samsetningardeild](assembly-assemble-items.md)    
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

