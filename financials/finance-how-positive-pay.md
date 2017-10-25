---
title: "Flytja út jákvæðar greiðsluskrár| Microsoft Docs"
description: "Hægt er að ganga úr skugga um að bankinn þinn taki eingöngu við fullgildum ávísunum með því að flytja út jákvæða greiðsluskrá sem inniheldur upplýsingar um lánardrottna og greiðslur."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, clearing
ms.date: 06/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: dfae1975a78c9380b5b6d4086569d63fe3793832
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-export-a-positive-pay-file"></a>Hvernig á að: flytja út jákvæða greiðsluskrá
Til að ganga úr skugga um að bankinn þinn eingöngu taki til fullgiltar athuganir og fjárhæðir getur þú flutt greiðslubréf sem inniheldur upplýsingar um söluaðila, athuga fjölda og greiðslu upphæð sem þú sendir til bankans til viðmiðunar þegar þú vinnur greiðslur.

[!INCLUDE[d365fin](includes/d365fin_md.md)] er forstillt á að styðja jákvæðar greiðsluskrár fyrir Bank of America og City Bank.

## <a name="to-set-up-a-bank-account-for-positive-pay"></a>Að setja upp bankareikning fyrir Positive Pay
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **bankareikningar** og velja svo viðeigandi tengil.
2. Opnaðu kortið fyrir bankann sem þú vilt nota Jákvæð Borga fyrir.
3. Sláðu inn POSPAYBANK í reitnum **Útflutningskóði jákvæðrar greiðslu**.
4. Glugganum er lokað.

## <a name="to-export-a-positive-pay-file"></a>Til að flytja út jákvæða greiðsluskrá
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **bankareikningar** og velja svo viðeigandi tengil.
2. Veldu bankareikninginn sem þú vilt flytja út jákvæð greiðsluskilríki fyrir.
3. Veldu **Útflutningur jákvæðrar greiðslu** aðgerðina.

    Gluggi með **jákvæðu greiðslumiðlun** opnast með því að birta greiðslur sem hafa verið gerðar á bankareikningnum frá síðasta upphleðsludegi, eins og sýnt er í **Síðasti dagur** og **Siðast hlaðið inn**.
4. Tilgreindu **Lokadagsetning upphleðslu** áður en greiðsla er ekki innifalin í útfluttri skrá í Afhendingarsímabilinu.
5. Veldu **Export** aðgerðina.
6. Í glugganum **Flytja út skrá** skaltu velja **Vista** hnappinn og síðan vistaðu skrána á þægilegan stað.
7. Hladdu skránni í rafræna bankasíða þína.
8. Skrifaðu niður eða afritaðu staðfestingarnúmerið sem birtist þegar skráarupphæðin tekst vel.

Til að skoða útfluttar jákvæðar greiðslur

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **bankareikningar** og velja svo viðeigandi tengil.
2. Veldu bankareikninginn sem þú vilt skoða.
3. Veldu aðgerðina **Jákvæðar greiðslufærslur**.

    Í glugganum **Jákvæðar greiðslufærslur** er hægt að sjá allar greiðslur fyrir jákvæð greiðsla fyrir bankareikninginn.
4. Í **Staðfestingarnúmer** skaltu slá inn, fyrir hvern útflutningsskrá, staðfestingarnúmerið sem þú færð þegar skráarupphæðin til bankans hefur náð árangri.
5. Til að skoða tengda greiðslulínur skaltu velja aðgerðina **Sundurliðun færslu á jákvæðri greiðslu**.

Til að flytja út jákvæðar greiðslur

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **bankareikningar** og velja svo viðeigandi tengil.
2. Veldu bankareikninginn sem þú vilt endurútgefa jákvæð greiðslur fyrir.
3. Veldu aðgerðina **Jákvæðar greiðslufærslur**.
4. Veldu línuna fyrir útflutningsskrána fyrir jákvæð greiðsla sem þú vilt endurútgefa.
5. Í reitnum **Jákvæðar greiðslur** skaltu velja **Endurútflytja jákvæðar greiðslur** í skrá aðgerðina.

## <a name="see-also"></a>Sjá einnig
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Vinna í færslubókum](ui-work-general-journals.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

