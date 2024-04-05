---
title: Stofna sölureikning verks til að reikningsfæra verk
description: Lýsir því hvernig reikningsfæra á viðskiptavini fyrir verkkostnað sem verkferla og kostnað sem safnast upp.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.search.keywords: project invoice
ms.search.form: '1002, 1007,'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
---
# Reikningsfæra verk

Meðan á verkefninu stendur getur kostnaður vegna forðanotkunar, efnis og verktengdra innkaupa safnast upp. Eftir því sem verkinu líður eru þessar færslur bókaðar í verkbókina. Mikilvægt er að allur kostnaður sé skráður í verkbókina áður en viðskiptavinurinn er reikningsfærður.

> [!NOTE]
> Einnig er hægt að kaupa ytri forða ótengdan verkefni, til dæmis til að reikningsfæra lánardrottin fyrir vinnu sem afhent er. Nánari upplýsingar eru í reitnum [Skrá innkaup](purchasing-how-record-purchases.md).

Hægt er að reikningsfæra allt verkið af síðunni **Verkhlutalínur verks** eða aðeins reikningsfæra valdar reikningshæfar línur af síðunni **Áætlunarlínur verks** . Hægt er að reikningsfæra eftir að verkinu er lokið eða með vissu millibili á meðan á vinnslu verksins stendur, byggt á reikningsáætlun.

> [!NOTE]  
> Ef reikningshæft er valið **í reitnum** Tegund **verklínu á innkaupaskjölunum fyrir verktengd innkaup þá eru stofnaðar verkáætlunarlínur sem eru tilbúnar til reikningsfærslu fyrir viðskiptavininn.**  Frekari upplýsingar eru í [Sjá um birgðir verkefna](projects-how-manage-project-supplies.md).

Einnig er hægt að reikningsfæra fyrirtæki sem er ekki endaviðskiptamaður. Stundum er sá aðili sem verkefni er unnið fyrir annar en sá sem er að borga reikninginn. Á síðunni **Verkefni** er hægt að tilgreina þann viðskiptamann sem mun njóta góðs af verkefninu í reitunum **Selt-til** og aðili á að reikningsfæra í reitina **Reikningsfært á** .

## Til að stofna marga sölureikninga verka

Hægt er að stofna reikning fyrir verk eða fyrir einn eða fleiri verkhluta fyrir viðskiptavin þegar verkinu sem á að reikningsfæra er lokið eða dagsetning reikningsfærslu sem byggist á reikningsfærsluáætlun er náð.

Eftirfarandi ferli sýnir hvernig á að nota keyrslu til að reikningsfæra mörg verk.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Verk Stofnað sölureikning** og velja síðan viðeigandi tengil.  
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Afmarkanir eru settar ef takmarka á verk sem keyrslan á að vinna.
4. Velja hnappinn **Í lagi** til að stofna reikningana.  

Hægt er að yfirfara og bóka stofnaða reikninga í glugganum **Sölureikningar**.

> [!NOTE]
> Einnig er hægt að reikningsfæra á viðskiptavin með því að velja verkið og velja svo aðgerðina **Stofna sölureikning** . 

## Til að stofna og bóka sölureikning verks úr verkáætlunarlínum

Hægt er að stofna reikning úr verkáætlunarlínum og gefa til kynna á þeim tíma magn vöru, forða eða fjárhagsreiknings sem á að reikningsfæra.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Verkefni** og velja síðan viðeigandi tengil.
2. Viðeigandi verkefni er opnað.
3. Veljið verkhluta þar sem í reitnum **Tegund** **verkhluta er Bókun** og veljið svo aðgerðina **Áætlunarlínur verks** .  
4. Í verkáætlunarlínu í reitnum **Magn. Til að færa í reitinn Millifæra á reikning** er fært inn magn vörunnar, forðans, fjárhagsreikningstegundarinnar sem á að reikningsfæra.  
5. Veljið aðgerðina **Stofna sölureikning**.
6. Á síðunni **Verkflutningur á sölureikning** er bókunardagsetningin færð inn og hvort stofna eigi nýjan reikning eða bæta þessum reikningi við fyrirliggjandi reikning.
7. Velja hnappinn **Í lagi**.  
8. Á síðunni **Áætlunarlínur** verkefnis skal velja aðgerðina **Sölureikningar/Kreditreikningar** .

    Síðan **Sölureikningur** opnast og sýnir það magn sem hefur verið flutt á reikninginn.
9. Gerið frekari breytingar og veljið svo aðgerðina **Bóka**.

> [!NOTE]  
> Ofangreint ferli svipar til stofnunar, endurskoða og bóka verktengdan sölukreditreikning.

## Sjá einnig .

[Stjórna verkum](projects-manage-projects.md)  
[Fjármál](finance.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Sala](sales-manage-sales.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
