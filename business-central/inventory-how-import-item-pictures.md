---
title: Flytja inn margar myndir af vörum úr ZIP-skrá
description: 'Til að flytja inn margar myndir af vörum skaltu gefa myndaskrám nafn sem samsvarar vörunúmerunum þínum, þjappaðu þeim í ZIP-skrá og notaðu síðan síðuna Flytja inn vörumyndir.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'product, image'
ms.search.form: '30, 461'
ms.date: 06/16/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Flytja inn margar vörumyndir
Hægt er að flytja inn margar vörumyndir í einu. Gefðu einfaldlega myndaskránum þínum heiti sem samsvarar vörunúmerunum þínum, þjappaðu þeim í zip-skrá og notaðu síðan síðuna fyrir innflutning á vörumyndum til að stýra því hvaða vörumyndir á að flytja inn.

Öll helstu skráarsnið eru studd.

## Að skíra myndaskrár eftir vöruheitum og undirbúa ZIP-skrána
1. Á staðsetningunni sem vörumyndirnar þínar eru geymdar skal nefna hverja skrá samkvæmt númeri tengdrar vöru. Dæmi:

    |Vörunr.|Skrárnafn|
    |-|-|
    |1000|1000.bmp|
    |1001|1001.bmp|
    |1002|1002.bmp|

2. Safnaðu öllum skrám í ZIP-skrá. Til dæmis í Windows Explorer skal velja skrárnar og síðan velja **Senda til**, **Þjöppuð mappa (zip-þjöppuð)**.     

## Að flytja inn myndir af vörum
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning birgða** og velja síðan viðkomandi tengil.
2. Velja skal aðgerðina **Flytja inn myndir**.
3. Í reitnum **Velja ZIP-skrá** skal velja viðeigandi Zip-möppu og síðan velja hnappinn **Opna**.

    Lína fyrir hverja vöru og mynd er búin til á síðunni **Flytja inn vörumyndir**.

    > [!NOTE]
    > Fyrir vöruspjöld sem eru þegar með mynd er gátreiturinn **Mynd er þegar til** valinn. Ef þú vilt ekki að fyrirliggjandi myndum verði skipt út skal hætta við val á gátreitnum **Skipta út myndum**. Ef þú vilt ekki að einstökum myndum sem eru til verði skipt út skal eyða línunum sem um ræðir.

3. Velja skal aðgerðina **Flytja inn myndir**.

Reiturinn **Staða innflutnings** er uppfærður til að sýna hvort innflutningur á mynd hafi verið sleppt eða kláraður.       

## Sjá einnig
[Skrá nýjar vörur](inventory-how-register-new-items.md)  
[Stofnun númeraraða](ui-create-number-series.md)  
[Birgðir](inventory-manage-inventory.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Sala](sales-manage-sales.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]