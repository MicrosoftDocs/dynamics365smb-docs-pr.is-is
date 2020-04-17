---
title: Vinnsla sölutækifæra í söluferli| Microsoft Docs
description: Hægt er að skoða, loka eða eyða sölutækifærum, og líka stofna tilboð og sölupantanir fyrir tækifæri, og færa tækifæri á milli þrepa í söluferlinu.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: e4e56b2594820cc1af4861d0117b9e7d6af891ec
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3181330"
---
# <a name="process-sales-opportunities"></a>Meðhöndla sölutækifæri
Þegar tækifæri er stofnað eru margar aðgerðir til að stjórna tækifæri og vinna það til enda.

## <a name="to-view-opportunities"></a>Skoða tækifæri
Fyrirliggjandi sölutækifæri eru tiltæk á síðunni **Tækifæralisti**. Það eru til mismunandi leiðir til að fá aðgang að þessari síðu til að vinna úr sölutækifærum:

| Skoða tækifæri fyrir | Þá |
| --- | --- |
| Alla sölumenn og tengiliði |Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Möguleikalisti** og veldu síðan tengda tengilinn. |
| Tiltekin sölumaður |Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **sölumenn** og veldu síðan tengda tengilinn. Veldu sölumaður, veldu aðgerðina **tækifæri**, og veldu síðan aðgerðina **listi**. |
| Tiltekinn tengilið |Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Tengiliðir** og veldu síðan tengda tengilinn. Veldu tengilið úr listanum, og veldu svo aðgerðina **tækifæri**. |

Hver þesara verkefna opnar **Tækifæralisti** síðuna.

## <a name="to-close-opportunities"></a>Tækifærum lokað
Hægt er að loka tækifærum þegar samningaviðræðum er lokið. Þegar tækifæri er lokað er hægt að tilgreina hvort það hafi nýst eða tapast, og ástæðu fyrir lokuninni. Til að tilgreina ástæðu, þarf að setja upp kóða fyrir lokuð tækifæri.

1. Á síðunni **Tækifæralisti** skal velja tækifæri og velja **Loka** aðgerð. Síðan **Loka tækifæri** birtist.
2. Fyllið út viðeigandi reitina og smellið á hnappinn **Í lagi**.

   Reitirnir **Kóði lokunar tækifæris** og **Lokað dags** eru skyldureitir og verða að vera fylltir út áður en hægt er að velja **Í lagi** takkann

   Í reitnum **Kóði vegna lokunar tækifæris** í hægt er að velja úr einn af fyrirliggjandi kóðum vegna lokunar tækifæris eða bæta við nýjan kóða. Til að bæta inn nýja kóða úr fellilistanum er valið **Valið úr tæmandi listi**, og síðan valið **nýtt**. Á nýju auðri línu, fyllt út í á **kóða**, **Tegund**, og **Lýsing** reitina, og síðan valið **í lagi** hnappinn.

## <a name="to-create-quotes-for-opportunities"></a>Tilboð stofnuð fyrir tækifæri
Hægt er að stofna sölutilboð fyrir tengiliði sem ekki eru skráðir sem viðskiptamenn.

1. Á síðunni **Tækifæralisti** skal velja tækifæri og velja síðan **úthluta sölutilboðum** aðgerð. Síðan **Sölutilboð** opnast.
2. Viðeigandi reitir eru fylltir út.

## <a name="to-create-sales-orders-for-opportunities"></a>Sölupantanir stofnaðar fyrir tækifæri
Hægt er að búa til sölupantanir úr sölutilboðunum sem stofnuð hafa verið fyrir tækifærin. Áður en hægt er að stofna sölupantanir fyrir tengiliði þarf að stofna tengiliðinn sem viðskiptamann. Frekari upplýsingar eru í [Stofna tengiliði](marketing-create-contact-companies.md).

1. Á síðunni **Tækifæralisti** skal velja tækifærið sem sölutilboð hefur verið stofnað fyrir.
2. Velja skal **Úthluta sölutilboði** aðgerð. Síðan **Sölutilboð** opnast, og sýnir hann sölutilboðið sem tækifærinu var úthlutað.
3. Fyllið út aukalegu reitina og veljið  aðgeðrina **búa til pöntun**.

Þegar unnið er með sölutækifæri getur þurft að stofna tilboð fyrir tengiliðinn sem tækifærið er tengt við,

## <a name="to-delete-opportunities"></a>Tækifærum eytt
Hægt er að eyða tækifærum, til dæmis þegar sala hefur náðst. Hinsvegar, Aðeins er hægt að eyða  lokuðum tækifærum. Tvær aðferðir til að eyða lokuð tækifæri. Er hægt að eyða einstökum lokuðum tækifærum af síðunni **Tækifæralisti** eða þú getur keyrt **Eyða Lokuð Tækifæri** runuvinnsluna til að eyða mörgum tækifærum byggða á tilgreindum skilyrðum.

Til að eyða lokuðum tækifærum af **Tækifæralisti** síðunni, valin tækifæri og velja síðan **eyða** aðgerð.

Til að eyða lokuðum tækifærum með því að nota **Eyða Lokuð Tækifæri** runuvinnslu, fylgja skal eftirfarandi skrefum:

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eyða tækifærum** og veldu síðan tengda tengilinn.
2. Í **Tækifæri** hlutanum, skal setja upp síur sem tilgreina lokuð tækifæri til að eyða.
3. Velja hnappinn **Í lagi**.

Þegar tækifæri hefur verið eytt er það sjálfkrafa fjarlægt af síðunni **Tækifæralisti**.

## <a name="to-move-an-opportunity-through-sales-cycle-stages"></a>Færa tækifæri gegnum þrep söluferlis
Ef tækifæri kemur í kjölfar söluferlis, er hægt að flytja það fram eða aftur gegnum mismunandi stig, eins og flutningur á næstu eða fyrra þrep og jafnvel hoppa yfir þrep.

1. Á síðunni **Tækifæralisti** er smellt á **uppfæra** aðgerðina. **Uppfæra tækifæri** opnast.
2. Nota á **gerð aðgerðar** reitinn til að færa tækifærið gegnum söluferliþrep:
   * **Næsta** flytur tækifærið fram um eitt stig.
   * **Sleppa** flytur tækifærið fram um eitt eða fleiri stig í söluferlinu sem tilgreint er í reitnum **Framsetningu** . Aðeins er hægt að sleppa þrepum sem hafa verið settar upp til að leyfa því að vera sleppt.
   * **Fyrra** flytur tækifærið aftur um eitt stig.
   * **Hoppa** flytur tækifærið aftur um eitt eða fleiri stig í söluferlinu sem tilgreint er í reitnum **Framsetningu** .
   * **Uppfæra** gerir kleift að breyta upplýsingar (t.d. breyta mati á líkum á árangri og áætluðu virði) án fara á annað stig.
3. Fyllið út aðra reitina að þörfum og smellið veljið síðan hnappinn **Í lagi**.

## <a name="see-also"></a>Sjá einnig
[Sala](sales-manage-sales.md)  
[Stofnun og stjórnun tengiliða](marketing-contacts.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
