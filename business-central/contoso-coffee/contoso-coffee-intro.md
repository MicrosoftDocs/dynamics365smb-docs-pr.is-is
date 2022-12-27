---
title: Kynning á sýnigögnum Contoso Coffee
description: Yfirlit yfir aðstæður þar sem sýnigögn Contoso Coffee geta hjálpað þér að læra hvernig á að nota framleiðslumöguleikana í Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 4760
author: edupont04
ms.author: andreipa
ms.openlocfilehash: 41dac60578399e09b9a67ac5747d48648a872f9c
ms.sourcegitcommit: 9bba11d474e21711cc8e2afefee8efb473170707
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788213"
---
# <a name="introduction-to-contoso-coffee-demo-data"></a>Kynning á sýnigögnum Contoso Coffee

Contoso Coffee er skáldað fyrirtæki sem framleiðir kaffivélar fyrir neytendur og fyrirtæki. **Contoso Coffee** forritin fyrir Business Central bæta við sýnigögnum sem hægt er að nota til að komast að því hvernig á að nota framleiðslumöguleikana í Business Central.  

Forritið býður upp á fjórar vörur sem eru fínstilltar fyrir mismunandi aðstæður:

- **SP-SCM1009 Airpot**  

  Þessi vara er uppskrift með undirsamsetningu, **Leið**. Notaðu það til að sýna hefðbundið framleiðsluflæði. Hún er sett upp með öðrum leiðum sem hægt er að nota til að sýna ýmsar aðstæður sem fela í sér undirverktaka. Kostnaðarútreikningurinn er *Staðlaður*.  

- **SP-SCM1011 Airpot Duo**  

  Þessi vara þarf vörurakningu og er með íhlut sem þarf líka vörurakningu. Kostnaðarútreikningurinn er *Sértækur*.  

- **SP-SCM1004 Autodrip**  

  Þessi vara er uppskrift með undirsamsetningu, **Leið**. Við mælum með því til að sýna ýmsar birgðaskráningaaðferðir bæði fyrir íhluti og aðgerðir. Kostnaðarútreikningurinn er *Staðlaður*.

- **SP-SCM1006 AutoDripLite**

  Þessi vara er með þremur afbrigðum og þremur uppskriftum sem hægt er að úthluta á birgðahaldseiningar. Varan notar hugmyndina á bak við skuggauppskrift. Kostnaðarútreikningurinn er *Staðlaður*.

Framleiðsluaðgerðir fyrir allar aðstæður nota staðsetninguna *NORÐUR*.  

> [!IMPORTANT]
> Áður en þú keyrir einhverjar aðstæður fyrir Contoso Coffee skaltu bóka allar birgðabókarlínur með opnunarstöðum. Frekari kröfur er að finna í hlutanum [Setja upp gögn Contoso Coffee](#set-up-contoso-coffee-data).

## <a name="set-up-contoso-coffee-data"></a>Setja upp Contoso Coffee gögn

Til að nota sýnigögn Contoso Coffee þarftu að setja upp tvö forrit í viðeigandi fyrirtæki í [!INCLUDE [prod_short](../includes/prod_short.md)]:  

- **Gagnamengi Contoso Coffee**  

    Þetta forrit afhendir sýnigögn fyrir grunnforritið.  
- **Sýnigagnamengi Contoso Coffee (auðkenni lands)**  

    Þetta forrit bætir landsbundnu efni við efst í grunnforritið.

Bættu forritunum við autt fyrirtæki í greiddri áskrift eða sem hluti af prufuáskrift. Stofnaðu til dæmis nýtt fyrirtæki með engin sýnigögn úr uppsetningarleiðbeiningunni **Stofna nýtt fyrirtæki** sem hægt er að opna úr listanum **Fyrirtæki**. Bættu síðan við forritunum úr [markaðstorginu](../ui-extensions-install-uninstall.md#install) ef þau eru ekki þegar sýnd á síðunni **Viðbótastjórnun**.  

Þegar viðeigandi forrit hafa verið sett upp skal fara á síðuna [Sýnigögn Contoso Coffee](https://businesscentral.dynamics.com/?page=4760) í [!INCLUDE [prod_short](../includes/prod_short.md)] og breyta sjálfgefnum stillingum svo þær henti þínum þörfum. Eftirfarandi töflur lýsa stillingunum.  

|Svæði  |Lýsing  |
|---------|---------|
|**Upphafsár** |Tilgreinir fyrsta árið sem á að nota fyrir sýnigögn Contoso Coffee. Árið er annað hvort almanaksár eða reikningsár en það fer eftir uppsetningu fyrirtækisins.|
|**Framleiðslustaður** |Tilgreinir vöruhúsið sem á að nota fyrir framleiðsluaðgerðir. *NORÐUR* er sjálfgefið en hægt er að breyta því eftir þörfum.|
|**Tegund fyrirtækis**    |Tilgreinir hvort núverandi fyrirtæki þurfi að tilkynna um virðisaukaskatt eða söluskatt. |
|**Innlendur – almennur viðskiptabókunarflokkur**|Tilgreinir viðskiptakóða fyrir innlenda viðskiptavini og lánardrottna. Viðskiptakóðarnir eru notaðir þegar færslur eru bókaðar. |
|**Afkastageta – almennur vörubókunarflokkur**    |Tilgreinir kóða fyrir vörur eða tilföng sem verður að nota til að bóka afkastagetu.|
|**Smásala – almennur vörubókunarflokkur**    |Tilgreinir kóða fyrir vörur eða tilföng sem verður að nota til að bóka smásölu.|
|**Hráefni – almennur vörubókunarflokkur**    |Tilgreinir kóða fyrir vörur eða tilföng sem verður að nota til að bóka hráefni. |
|**Grunnkóði virðisaukaskatts**    |Tilgreinir fyrirliggjandi vöruflokk virðisaukaskatts sem verður notaður fyrir vörur.|
|**Kóði fyrir fullbúið**    |Tilgreinir fyrirliggjandi vöruflokk sem verður notaður fyrir tilbúnar vörur.|
|**Verðstuðull**     |Tilgreinir stuðul til að umbreyta verði úr USD/EUR í staðbundinn gjaldmiðil. *1* þýðir að verðið er sama upphæð í hvaða gjaldmiðli sem er. Hærri tala verður notuð til að fá verðið í staðbundnum gjaldmiðli. |
|**Sléttunarnákvæmni**  |Skilgreinir hvernig reiknað notkunarmagn er sléttað þegar það er fært inn á notkunarbókarlínur. Magn undir 0,5 verður sléttað niður Magn sem er 0,5 eða meira verður sléttað upp.|

Þegar allt er til reiðu skaltu velja aðgerðina **Búa til sýnigögn**. Það tekur nokkrar mínútur að bæta gögnunum við undirliggjandi gagnagrunn en eftir það er allt til reiðu til að keyra ýmsar aðstæður.  

## <a name="scenarios"></a>Dæmi

Sýnigögn Contoso Coffee styðja núna eftirfarandi aðstæður fyrir prófun og þjálfun:

1. [Stofna nýja framleiðsluuppskrift og uppskriftarútgáfu](create-new-production-bom-version.md)  
2. [Stofna nýja leið](create-new-routing.md)  
3. [Stofna fastáætlaða framleiðslupöntun og breyta henni](create-firm-planned-production-order-change.md)  
4. [Sameina sjálfvirka og handvirka birgðaskráningu](combine-automatic-manual-flushing.md)  
5. [Nota pantanaáætlun til að búa til og bakfæra framboð](order-planning-create-reserve-supply.md)  
6. [Setja upp og vinna úr úthýsingaraðgerð](set-up-process-subcontracting-operation.md)  
7. [Setja upp nýja getu](set-up-new-capacity.md)  
8. [Spá fyrir um eftirspurn eftir vöruafbrigðum með mismunandi uppskriftum úthlutuðum](variants.md)  

Lestu skrefin fyrir hverjar aðstæður í viðkomandi grein.  

> [!IMPORTANT]
> Þessar kynningar krefjast þess að upplifun notanda sé stillt á *Premium* á síðunni **Fyrirtækjaupplýsingar**.

## <a name="see-also"></a>Sjá einnig .

[Framleiðsla](../production-manage-manufacturing.md)  
[Framleiðsluskýrslur og greiningar í Business Central](../production-reports.md)  
