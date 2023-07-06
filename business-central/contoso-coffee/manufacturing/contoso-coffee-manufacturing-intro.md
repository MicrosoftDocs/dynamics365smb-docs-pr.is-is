---
title: Kynning á contoso Coffee framleiðslu
description: Yfirlit yfir aðstæður þar sem sýnigögn Contoso Coffee geta hjálpað þér að læra hvernig á að nota framleiðslumöguleikana í Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 4760
author: edupont04
ms.author: andreipa
---

# <a name="introduction-to-contoso-coffee-manufacturing"></a><a name="introduction-to-contoso-coffee-manufacturing"></a><a name="introduction-to-contoso-coffee-manufacturing"></a>Kynning á contoso Coffee framleiðslu

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
> Áður en þú keyrir einhverjar aðstæður fyrir Contoso Coffee skaltu bóka allar birgðabókarlínur með opnunarstöðum. Nánari kröfur er að finna í kaflanum um  [contoso Coffee](#set-up-contoso-coffee-manufacturing-data) .

## <a name="set-up-contoso-coffee-manufacturing-data"></a><a name="set-up-contoso-coffee-manufacturing-data"></a><a name="set-up-contoso-coffee-manufacturing-data"></a>Setja upp contoso Coffee framleiðslugögn

Til að nota contoso Coffee framleiðslu sýnigögnin þarf að setja upp tvö forrit í viðkomandi fyrirtæki í [!INCLUDE [prod_short](../../includes/prod_short.md)]:  

- **Gagnamengi Contoso Coffee**  

    Þetta forrit afhendir sýnigögn fyrir grunnforritið.  
- **Sýnigagnamengi Contoso Coffee (auðkenni lands)**  

    Þetta forrit bætir landsbundnu efni við efst í grunnforritið.

Bættu forritunum við autt fyrirtæki í greiddri áskrift eða sem hluti af prufuáskrift. Stofnaðu til dæmis nýtt fyrirtæki með engin sýnigögn úr uppsetningarleiðbeiningunni **Stofna nýtt fyrirtæki** sem hægt er að opna úr listanum **Fyrirtæki**. Bættu þá appinu við af  [markaðstorginu](../../ui-extensions-install-uninstall.md#install)  ef þær eru ekki þegar á skrá á  **síðu framlengingarstjórnunar** .  

Þegar viðeigandi forrit eru sett upp er farið á  [kaffisíðuna contoso Coffee](https://businesscentral.dynamics.com/?page=4760)  í  [!INCLUDE [prod_short](../../includes/prod_short.md)] og breytt sjálfgefnum stillingum sem henta þínum þörfum. Eftirfarandi tafla lýsir stillingum:  

|Svæði  |Description  |
|---------|---------|
|**Upphafsár** |Tilgreinir fyrsta árið sem óskað er eftir að notuð séu útsýnandi Kaffisýnigögn. Árið er annað hvort almanaksár eða reikningsár en það fer eftir uppsetningu fyrirtækisins.|
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

## <a name="scenarios"></a><a name="scenarios"></a><a name="scenarios"></a>Dæmi

Útlitsprófið á contoso Coffee sýnigögnunum styður nú við eftirfarandi Aðstæður til prófs og þjálfunar:

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

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Sjá einnig .

[Framleiðsla](../../production-manage-manufacturing.md)  
[Framleiðsluskýrslur og Greinaskil í Viðskiptamiðinu](../../production-reports.md)  
