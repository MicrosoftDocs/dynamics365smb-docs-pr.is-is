---
title: Staðlaðar ítrekaðar innkaupalínur
description: Setja upp innkaupalínur sem oft eru notaðar til að setja þær inn í innkaupaskjöl og fylla fljótt út línurnar með stöðluðum upplýsingum.
author: rubenseishima
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, purchase, replenishment
ms.search.form: 177
ms.date: 07/06/2022
ms.author: a-reishima
ms.openlocfilehash: 08fda9bb2478cb7453bd16d5392139fba1408f87
ms.sourcegitcommit: 5560a49ca4ce85fa12e50ed9e14de6d5cba5f5c3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/13/2022
ms.locfileid: "9146334"
---
# <a name="create-recurring-purchase-lines"></a>Stofna endurteknar innkaupalínur

Ef oft þarf að stofna innkaupalínur með svipuðum upplýsingum er hægt að setja upp staðlaðar línur sem hægt er að setja inn í ítrekunarinnkaupaskjöl, til dæmis fyrir endurteknar áfyllingarpantanir.

## <a name="set-up-recurring-purchase-lines"></a>Setja upp endurteknar innkaupalínur

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **endurteknar innkaupalínur** og velja síðan tengda tengilinn.
2. **Á síðunni endurteknar innkaupalínur** er valin sú **nýja** aðgerð.
3. Fyllt er út í reiti eftir því sem er nauðsynlegt í flýtiflipanum **Almennt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. **Á fastflipanum línur** eru færðar inn upplýsingar í reitina sem endurspegla stöðluðu línurnar sem búist er við að nota sem endurteknar línur á innkaupaskjölum.

> [!NOTE]
> Ekki er hægt að skilgreina verð í endurteknum innkaupalínum þar sem verð, afslættir o. fl. eru reiknuð út á raunveruleg innkaupaskjöl eftir að ítrekunarinnkaupalínum er skotið inn.

[!INCLUDE [line-no-info](includes/line-no-info.md)]

## <a name="assign-recurring-purchase-lines-to-a-vendor"></a>Úthluta endurteknum innkaupalínum á lánardrottin

Úthlutið einni eða fleiri endurteknum innkaupalínum til lánardrottins þannig að þær séu tiltækar til að setja inn innkaupaskjöl frá þeim lánardrottni.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Lánardrottnar** og síðan velja viðkomandi tengil.
2. Opnaðu kortið fyrir viðeigandi lánardrottin.
3. **Velja endurteknar aðgerðir innkaupalínum**.
4. **Á síðunni endurteknar innkaupalínur** velurðu kóta fyrir endurteknar innkaupalínur sem þú vilt geta sett inn innkaupaskjöl fyrir lánardrottininn.
5. Önnur svæði eru fyllt út til að skilgreina hvenær, hvernig og hvar á að nota ítrekunarinnkaupalínurnar.
6. Í svæðunum fjórum þar sem er valið hvernig línurnar eru settar inn í hverja skjalagerð er valinn einn af eftirtöldum valkostum:

|Valkostur|Lýsing|
|------|-----------|
|**Handvirkt**|Hægt er að fletta upp handvirkt og setja inn endurtekna innkaupalínu sem er til fyrir lánardrottininn.|
|**Sjálfvirkt**|Ef margar endurteknar innkaupalínur eru til fyrir lánardrottin birtist tilkynning þar sem hægt er að velja hvaða eina sem setja á inn. Ef aðeins ein endurtekin innkaupalína er til staðar verður hún sett inn sjálfvirkt.<br /><br />Þetta virkar aðeins ef nýja skjalið var búið til úr skjalalista, til dæmis með því að **Velja nýja** aðgerð á **síðunni innkaupapantanir**. Það virkar ekki ef skjalið var búið til af lánardrottnaspjaldi, td.|
|**Spyrja alltaf**|Tilkynning birtist og allar tiltækar endurteknar innkaupalínur eru sýndar þannig að hægt er að velja eina.

## <a name="insert-recurring-purchase-lines-on-a-purchase-invoice"></a>Setja endurteknar innkaupalínur inn á innkaupareikning

Ef til eru endurteknar innkaupalínur fyrir lánardrottininn er hægt að setja þær inn eða bæta þeim sjálfkrafa við á öllum tegundum innkaupaskjala, til dæmis innkaupareikningi. Ef notandi hefur virkjað **alltaf Valkostir spyrna** á meðan lánardrottnum er úthlutað til lánardrottna verður upplýst hvort endurteknar innkaupalínur séu til.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupareikningar** og velja síðan viðkomandi tengil.
2. Opna innkaupareikning sem óskað er að setja eina eða fleiri staðlaðar innkaupalínur á.
3. **Velja aðgerðina Sækja endurteknar innkaupalínur**.
4. **Á síðunni endurteknar innkaupalínur** er uppflettihnappurinn valinn í **reitnum kóti** og síðan er valin stöðluð innkaupalínur.
5. Velja skal **OK** hnappinn til að setja inn stöðluðu innkaupalínurnar á reikningnum þar sem hægt er að endurnýta þær eins og er eða breyta upplýsingunum.

## <a name="see-also"></a>Sjá einnig .

[Innkaup](purchasing-manage-purchasing.md)  
[Setja upp innkaup](purchasing-setup-purchasing.md)  
[Stofna endurtekna sölu](sales-how-work-standard-lines.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]