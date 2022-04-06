---
title: Hvernig á að skipuleggja tínslur á vinnublaðinu
description: Kynntu þér hvernig hægt er að gera línur afhendingarskjala aðgengilegar í tiltektarvinnublöðum fyrir starfsmenn vöruhúss.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/13/2021
ms.author: edupont
ms.openlocfilehash: 09b9f0d4d707da3872ae4b085f1405a99f69a9bc
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8515200"
---
# <a name="plan-picks-in-worksheets"></a>Skipuleggja tínslur á vinnublaðinu

Ef vöruhúsið er sett upp þannig að það krefjist bæði tiltektar- og afhendingarvinnslu geturðu valið að gera línur afhendingarskjala aðgengilegar á vinnublöðum tiltektar í staðinn fyrir tiltektarleiðbeiningar.  

> [!NOTE]  
> Hafi tiltektarleiðbeiningar vöruhúss þegar verið búnar til og sameina á þær í einni tiltektarleiðbeiningu þarf að eyða hverri vöruhúsatiltekt fyrir sig. Línurnar sem á að tína má nú birta á vinnublaði tiltektar.  

Á síðunni **Vinnublöð tínslu** er hægt að setja upp tiltektarlista sem hjálpa starfsmönnum að safna saman vörum í vöruhúsinu. Á síðunni er hægt að sjá tiltækt magn í hjáskipunarhólfum, sem er gagnlegt við áætlanagerð vinnuúthlutunar í aðstæðum hjáskipunar. [!INCLUDE[prod_short](includes/prod_short.md)] mun alltaf fyrst leggja til tiltekt úr hjáskipunarhólfi. Línurnar í vinnublaðinu geta komið úr nokkrum upprunaskjölum. Þær gætu til dæmis komið úr fleiri en einni sölupöntun. 

> [!NOTE]  
> Að tína vörur sem er safnað saman fyrir sölupöntun sem á að senda fylgir sömu skrefunum og fyrir venjulega tiltekt vöruhúss fyrir sendingar. Hins vegar gæti fjöldi tínslulína miðað við afhendingarmagn verið af gerðinni margt í eitt þar sem hlutir eru tíndir en ekki samsetningarvaran.  
>
> Vöruhúsatínslulínurnar eru stofnaðar fyrir gildið í reitnum **Eftirstöðvar** í línum samsetningarpöntunarinnar sem tengist sölupöntunarlínunni sem verið er að afhenda. Þetta tryggir að allir íhlutir eru tíndir í einni aðgerð. Frekari upplýsingar er að finna í [Selja birgðavörur í flæðum samsetningar í pöntun](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  
>
> Upplýsingar um almenna tínslu íhluta fyrir samsetningarpantanir, þar á meðal þegar samsetningaríhlutur er ekki hluti af söluafhendingu, eru í [Tína fyrir framleiðslu eða samsetningu í grunngerð ítarlegs vöruhúss](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).  

## <a name="sorting-lines-on-a-pick-worksheet"></a>Röðun lína á vinnublaði tiltektar
Hægt er að raða línum eftir vöru, hillunúmeri, upprunaskjali, gjalddaga eða áfangastað. Hér eru nokkur dæmi um hvernig röðun getur reynst gagnleg.

* Ef raðað er eftir gjalddaga er hægt að eyða öllum línum öðrum en þeim sem þarf að sinna strax. Minna áríðandi línum er ekki eytt þannig séð, heldur fara þær aftur á vinnublaðið **Tínsluval**. Þegar tínslan er stofnuð hefur línunum þegar verið raðað eftir gjalddaga og hægt er að úthluta tínslunni á starfsmann.
* Ef hólfin eru númeruð til að passa við eiginlegt útlit vöruhússins getur röðun á línum eftir hólfanúmeri gert tínslu auðveldari fyrir margar sendingar samtímis. 
* Ef notuð er hólfaflokkun getur röðun eftir flokki sparað tíma. 
* Hægt er að raða eftir áfangastað, sem gerir þér kleift að safna saman og senda pantanir fyrir hvern viðskiptamann.

## <a name="to-plan-picks-in-the-worksheet"></a>Tínslur skipulagðar á vinnublaðinu:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnublað tínslu** og velja síðan viðkomandi tengil.  
2. Valið er **Sækja vöruhúsaskjöl** aðgerð.  
3. Afhendingarnar sem undirbúa á tínslu fyrir eru valdar. Hægt er að raða línunum en röðunin verður ekki notuð í tiltektarleiðbeiningunum. Einnig er hægt að eyða línum til að gera tínsluna skilvirkari. Ef til að mynda til eru margar línur með vörum sem eru í hjáskipunarhólfum væri hægt að stofna tínslu fyrir allar línurnar. Hjáskipunarvörurnar verða sendar (ásamt hinum vörunum í afhendingunum) og hjáskipunarhólfin hafa pláss fyrir fleiri vörur.  
4. Veldu aðgerðina **Stofna tínslu** og fylltu út síðuna **Stofna tínslu**. Röðunin hér raðar tínslulínunum sem stofnaðar eru. Til dæmis er hægt að stofna eina tínslu fyrir hvert svæði og raða línum eftir hólfaflokkum innan hverrar tínslu.  
5. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vöruhúsatínslur** og velja síðan viðkomandi tengil. Síðan **Vöruhúsatínslur** opnast.  
6. Nú er hægt að finna tínsluúthlutunina með því að velja tínsluna með hæsta númerið.  
7. Ef þörf er á er hægt að úthluta öðrum notanda eða raða línunum á annan hátt.  
8. Veldu hnappinn **Prenta** til þess að prenta tínsluleiðbeiningarnar.  
9. Eftir að tínslu er lokið skal velja aðgerðina **Skrá**.  

## <a name="see-also"></a>Sjá einnig

[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Samsetningardeild](assembly-assemble-items.md)  
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]