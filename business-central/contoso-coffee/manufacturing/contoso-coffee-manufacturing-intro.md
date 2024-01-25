---
title: Kynning á Contoso kaffiframleiðslu
description: Yfirlit yfir aðstæður þar sem sýnigögn Contoso Coffee geta hjálpað þér að læra hvernig á að nota framleiðslumöguleikana í Business Central.
ms.date: 04/01/2023
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '4765,'
author: brentholtorf
ms.author: bholtorf
---

# <a name="introduction-to-contoso-coffee-manufacturing"></a>Kynning á Contoso kaffiframleiðslu

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

Framleiðslustarfsemin fyrir allar aðstæður notar *AÐAL* staðsetninguna.  

> [!IMPORTANT]
> Áður en þú keyrir einhverjar aðstæður fyrir Contoso Coffee skaltu bóka allar birgðabókarlínur með opnunarstöðum. Fyrir frekari kröfur, sjá [Setja upp Contoso kaffigögn](#set-up-contoso-coffee-manufacturing-data) hlutann.

## <a name="set-up-contoso-coffee-manufacturing-data"></a>Settu upp Contoso Coffee Manufacturing gögn

[!INCLUDE [contoso-coffee-app-install](../../includes/contoso-coffee-app-install.md)]

|Svæði  |Heimildasamstæða  |
|---------|---------|
|**Framleiðslustaður** |Tilgreinir vöruhúsið sem á að nota fyrir framleiðsluaðgerðir. Sjálfgefið er *MAIN*, en þú getur breytt því til að henta þínum þörfum.|


Þegar allt er til reiðu skaltu velja aðgerðina **Búa til sýnigögn**. Það tekur nokkrar mínútur að bæta gögnunum við undirliggjandi gagnagrunn en eftir það er allt til reiðu til að keyra ýmsar aðstæður.  

## <a name="scenarios"></a>Dæmi

Sýningargögnin um Contoso kaffiframleiðslu styðja eins og er eftirfarandi aðstæður fyrir próf og þjálfun:

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

[Framleiðsla](../../production-manage-manufacturing.md)  
[Framleiðsluskýrslur og greiningar í Business Central](../../production-reports.md)  
