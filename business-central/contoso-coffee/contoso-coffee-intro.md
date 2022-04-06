---
title: Kynning á contoso kaffi sýnigögnum
description: Yfirlit yfir áætlanir um hvernig contoso kaffi sýnishorn gögn geta aðstoðað við að læra hvernig hægt er að nýta framleiðslugetu í Viðskiptamiðinu.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.openlocfilehash: 782e8258bb04ac09ee0596fff34fccdca592e26e
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8524197"
---
# <a name="introduction-to-contoso-coffee-demo-data"></a>Kynning á contoso kaffi sýnigögnum

Contoso Coffee er skálduð fyrirtæki sem framleiðir neytendaumbúðir og viðskiptalegar Kaffivélar. **Contoso-kaffiforrit** fyrir miðborg bæta við sýnigögnum sem nota má til að læra hvernig á að nota framleiðslugetu í viðskiptamiðinu.  

Forritið gefur fjórar vörur sem eru bestar fyrir mismunandi atburðarás:

- **SP-SCM1009 Airpot**  

  Þessi vara er uppskrift með millisamsetningu, **leið**. Nota það til að sýna staðlað framleiðsluflæði. Það er sett upp með öðrum leiðum sem hægt er að nota til að sýna fram á ýmsar aðstæður sem fela í sér undirverktaka. Aðferð kostnaðarútreiknings er *stöðluð*.  

- **SP-SCM1011 Airpot Duo**  

  Þessi vara krefst vörurakningar og er með íhlut sem einnig krefst vörurakningar. Aðferð við slitameðferð er *Sérstök*.  

- **SP-SCM1004 Autodrip**  

  Þessi vara er UPPSKRIFT með millisamsetningu, **leið**. Mælt er með því að sýna hinar ýmsu andlitsmeðferðir bæði fyrir íhluti og aðgerðir. Aðferð kostnaðarútreiknings er *stöðluð*.

- **SP-SCM1008 AutoDripLite**

  Þessi vara hefur þrjú afbrigði og þrjár uppskriftir sem hægt er að tengja birgðaeiningum við. Afurðin notar skuggauppskriftahugmyndina. Aðferð kostnaðarútreiknings er *stöðluð*.

Framleiðsluverkþættir fyrir allar aðstæður nota *norðurstaðsetningu*.  

> [!IMPORTANT]
> Áður en þú keyrir einhvern af atburðarásinni fyrir contoso Coffee, bóka allar birgðabókarlínur með opnunarstöðum. Nánari kröfur er að finna í kaflanum um [contoso Coffee](#set-up-contoso-coffee-data).

## <a name="set-up-contoso-coffee-data"></a>Setja upp contoso-Kaffigögn

Til að nota contoso Coffee sýnigögnin þarf að setja upp tvö forrit í viðkomandi fyrirtæki í [!INCLUDE [prod_short](../includes/prod_short.md)]:  

- **Contoso kaffi sýnishorn DataSet**  

    Þetta App afhendir sýnigögn fyrir grunnforritið.  
- **Útlitslækinn kaffi sýnishorn DataSet (Country ID)**  

    Þetta App bætir landlegu efni ofan á grunnforritið.

Bættu appinu við tómt fyrirtæki í borgandi áskrift eða sem hluta af prufu. Til dæmis, stofna nýtt fyrirtæki með engin sýnishorn af gögnum úr **uppsetningarleiðbeiningum fyrir nýja fyrirtæki** sem hægt er að opna í **listanum fyrirtæki**. Bættu þá appinu við af [markaðstorginu](../ui-extensions-install-uninstall.md#install) ef þær eru ekki þegar á skrá á **síðu framlengingarstjórnunar**.  

Þegar viðeigandi forrit eru sett upp er farið á [kaffisíðuna contoso Coffee](https://businesscentral.dynamics.com/?page=4760) í [!INCLUDE [prod_short](../includes/prod_short.md)] og breytt sjálfgefnum stillingum sem henta þínum þörfum. Eftirfarandi töflur lýsa stillingum:  

|Svæði  |Description  |
|---------|---------|
|**Upphafsár** |Tilgreinir fyrsta árið sem óskað er eftir að nota á contoso-Kaffisýnigögnin. Allt frá uppsetningu félagsins er árið annað hvort almanaksárið eða reikningsár.|
|**Staðsetning framleiðslu** |Tilgreinir vöruhúsið sem nota á fyrir framleiðsluaðgerðir. Sjálfið er fyrir norðan *en hægt er* að breyta því þannig að það henti þörfum.|
|**Gerð fyrirtækis**    |Tilgreinir hvort gildandi fyrirtæki verði að tilkynna virðisaukaskatt eða virðisaukaskatt. |
|**Innlendir-Almennir viðskiptabókunarflokkar**|Tilgreinir viðskiptakóta fyrir innlenda viðskiptavini og lánardrottna. Viðskiptakóðar eru notaðir þegar færslur eru bókaðar. |
|**Afkastageta-almennur vörubókunarflokkur**    |Tilgreinir kóta vara eða forða sem þarf að nota til að bóka afkastagetu.|
|**Smásala-almennur vörubókunarflokkur**    |Tilgreinir kóta vara eða forða sem þarf að nota til að bóka smásölu.|
|**Hráefni almennur vörubókunarflokkur**    |Tilgreinir kóta vara eða forða sem nota þarf við bókun hráefnis. |
|**VSK-kóði**    |Tilgreinir fyrirliggjandi VSK-afurðaflokk sem verður notaður fyrir vörur.|
|**Afbúinn Kóði**    |Tilgreinir vöruflokk sem verður notaður fyrir tilbúnar vörur.|
|**Verðstuðull**     |Tilgreinir hvaða Stuðull á að umreikna verð frá USD/EUR yfir í staðbundinn gjaldmiðil. *1* merkir að verðið sé sama fjárhæð í hvaða gjaldmiðli sem er. Hærri tala verður notuð til að fá verð í gjaldmiðli landsins. |
|**Sléttunarnákvæmni**  |Skilgreinir hvernig útreiknaða notkunarmagn er sléttað þegar það er fært inn í línur í notkun færslubókar. Magn sem er minna en 0,5 verður sléttað niður. Magn jöfn eða hærri en 0,5 verður sléttað.|

Þegar þú ert tilbúin, Veldu þá aðgerðina búa til **sýnigögn**. Það tekur nokkrar mínútur að bæta gögnunum við undirliggjandi gagnagrunn, en þá Ertu tilbúinn að keyra hinar ýmsu aðstæður.  

## <a name="scenarios"></a>Dæmi

Útlaginn kaffi sýnikennsla styður nú við eftirfarandi Aðstæður til prófs og þjálfunar:

1. [Stofna nýja framl. UPPSKRIFT og UPPSKRIFTARÚTGÁFU](create-new-production-bom-version.md)  
2. [Stofna nýja leið](create-new-routing.md)  
3. [Stofna fastáætlaða framleiðslupöntun og breyta henni](create-firm-planned-production-order-change.md)  
4. [Sameina sjálfvirka og handvirka Flushing](combine-automatic-manual-flushing.md)  
5. [Nota Pantanáætlanagerð til að stofna og taka frá framboð](order-planning-create-reserve-supply.md)  
6. [Setja upp og vinna Úthýsingaraðgerð](set-up-process-subcontracting-operation.md)  
7. [Setja upp nýtt geymslurými](set-up-new-capacity.md)  
8. [Spáreftirspurn fyrir vöruafbrigði með mismunandi uppskriftum](variants.md)  

Lestu leiðbeiningar fyrir hverja atburðarás í viðkomandi grein.  

> [!IMPORTANT]
> Þessir gönguhópar krefjast þess að notendaupplifun sé stillt á *aukagjald* á **upplýsingasíðu** félagsins.

## <a name="see-also"></a>Sjá einnig .

[Framleiðsla](../production-manage-manufacturing.md)  
[Framleiðsluskýrslur og Greinaskil í Viðskiptamiðinu](../production-reports.md)  
