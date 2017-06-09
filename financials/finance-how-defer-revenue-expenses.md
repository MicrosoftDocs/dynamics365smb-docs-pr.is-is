---
title: "Hvernig á að: fresta tekjum og útgjöldum| Microsoft Docs"
description: "Lýsir því hvernig hægt er að bera kennsl á tekjur og útgjöld á tímabilum, öðrum en þeim tímabilum sem færslan var bókuð í sjálfvirkt frestuðum tekjum og útgjöldum yfir tiltekinni áætlun."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 03/24/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 5d7dbdc6001f221df0659d5aca1e5939398e3a31
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-defer-revenues-and-expenses"></a>Hvernig á að: Defer Tekjum og önnur Útgjöld
Hægt er að nota þessa aðgerð til samþykktar tekna á eða fyrir kostnað tímabil en tímabil sem færslan var bókuð í til sjálfkrafa defer tekjum og önnur útgjöld yfir tiltekinni áætlun.

Dreifa tekjur eða útgjöld fjárhagstímabila sem á að setja upp sniðmát deferral sem forðinn, varan eða fjárhagsreikningurinn sem tekjur eða kostnaðinn bókast. Þegar tengdar sölu eða innkaupaskjal er bókað fylgiskjal á tekjur eða kostnaðinn eru deferred til sögu reikningstímabil samkvæmt tímaáætlun deferral sem er stjórnað af stillingar í sniðmáti deferral og bókunardagsetningu.

**Athugið**: Þessi virkni krefst að upplifun þín er stilltur á **Pakki**. Nánari upplýsingar, sjá [Sérstilli þína [!INCLUDE[d365fin](includes/d365fin_md.md)]upplifun](ui-experiences.md).

## <a name="to-set-up-a-gl-account-for-deferral"></a>Verð sett upp fyrir fjárhagsreikning verks:
1. Efst í hægra horni skal velja táknið fyrir **Leit að síðu eða skýrslu** táknið fyrir ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "táknið fyrir Leit að síðu eða skýrslu táknið"), slá inn **Bókhaldslykill**, og velja síðan viðeigandi tengil.
2. Valið er **Nýtt** aðgerð.
3. Fyllt er út í reiti sem nauðsynlegt að stofna reikning fyrir deferred tekjur Fjárhags. Frekari upplýsingar er að finna í [Fjárhagur og bókhaldslyklar](finance-general-ledger.md).
4. Endurtaka skal þrep 2 og 3 eru endurtekin til að stofna nýjan reikning Fjárhags fyrir deferred útgjöld.

Fyrir báðar gerðir deferral, velja **Efnahagsreikningur** í reitnum **Tegund** og heiti reikninga athuga, t.d. "Óinnleystra Tekna" deferred tekjum og "Ógreidda Útgjöld" fyrir deferred útgjöld.

## <a name="to-set-up-a-deferral-template"></a>Uppsetning sniðmáts viðskiptamanns
1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Sniðmát frestunar**, og velja síðan viðeigandi tengil.
2. Valið er **Nýtt** aðgerð.
3. Fyllið inn í svæðin eftir þörfum.
4. Í á **Reikningsaðferð** er tilgreint hvernig **Upphæð** á hverju tímabili í á **Deferral Áætlun** glugganum reiknuð. Hægt er að velja um eftirfarandi kosti:

   * **Línuleg**: reglubundin deferral upphæðir eru reiknaðar fjölda tímabila dreift eftir lengd tímabils.
   * **Línuleg**: reglubundin deferral upphæðir eru reiknaðar fjölda tímabila dreift eftir lengd tímabils.
   * **Línuleg**: reglubundin deferral upphæðir eru reiknaðar fjölda tímabila dreift eftir lengd tímabils.
   * **Notandi Skilgreinir**: reglubundin deferral upphæðir eru ekki reiknaðir. Handvirkt þarf að fylla inn í reitinn **Upphæð** fyrir hvert tímabil í glugganum Frestunaráætlun. Frekari upplýsingar má fá í hlutanum "til Að breyta tímaáætlun deferral úr sölureikningi".
5. Í reitnum **Desc Tímabils.** Tilgreinir lýsingu sem verður birt í færslum fyrir bókun frestunar. Má færa kóta eftirfarandi frátaka fyrir dæmigerðum gildi sem er settur sjálfkrafa þegar tímabil lýsing birtist.

   * Tilgreinir bókunardagsetningu fylgiskjalsins.
   * Tilgreinir bókunardagsetningu fylgiskjalsins.
   * Tilgreinir bókunardagsetningu fylgiskjalsins.
   * Tilgreinir bókunardagsetningu fylgiskjalsins.
   * Tilgreinir bókunardagsetningu fylgiskjalsins.
   * Tilgreinir bókunardagsetningu fylgiskjalsins.

 er á undan bókunardagsetningunni. Ef fært er inn "Útgjöld deferred fyrir %4 %6" síðan birt lýsing verður "Útgjöld deferred fyrir Febrúar 2016".

## <a name="to-assign-a-deferral-template-to-an-item"></a>Til að úthluta sérþekkingarkóða á vöru
1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Sniðmát frestunar**, og velja síðan viðeigandi tengil.
2. Opna spjald fyrir vöruna sem tekjur eða útgjöld er verður að deferred á reikningstímabilin þegar varan var seld eða keypt.
3. Í reitnum **Sjálfgefin Sniðmát Deferral** er deferral viðeigandi sniðmát er valið.

## <a name="to-change-a-deferral-schedule-from-a-sales-invoice"></a>Til að breyta tímaáætlun deferral úr sölureikningi
**Bent**: liðir þessi aðferð er þau sömu og þegar breytt tímaáætlun deferral fyrir útgjöld, af innkaupareikningi.

1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Sölureikningar**, og velja síðan viðeigandi tengil.
2. Stofnaður sölureikningur fyrir vöru sem er til deferral sniðmát. Nánari upplýsingar eru í [Hvernig á að reikningsfæra sölu](sales-how-invoice-sales.md).

    Takið eftir að um leið og er að færa inn vöru (eða forða eða fjárhagsreiknings) í reikningslínunni, er **Deferral Kóta** fyllist með kóti sniðmáts deferral var úthlutað.
3. Valið er **Deferral Áætlun** aðgerð.
4. Í á **Deferral Áætlun** glugganum stillingar breytt í hausnum eða gildin í línunum, til dæmis til að defer upphæðinni öðrum reikningstímabil.
5. Valið er **Deferral Áætlun** aðgerð.
6. Velja hnappinn **Í lagi**. Áætlun deferral uppfærður til reikningnum. Sniðmát tengdar deferral er óbreytt.

## <a name="to-preview-how-deferred-revenues-or-expenses-will-be-posted-to-the-general-ledger"></a>Til að forskoða hvernig deferred tekjur eða útgjöld verða bókaðar í fjárhag.
**Bent**: liðir þessi aðferð er þau sömu og þegar er forskoða hvernig kostnaðinn deferrals eru bókuð.

1. Í reitnum **Bókaður Sölureikningur** er valið **leiðrétta** aðgerð.
2. Í reitnum **Forskoðun Bókunar ** , valin **Fjárhagsfærsla**, og velja síðan **Sýna Tengdar Færslur**.

Fjárhagsfærslur á að bóka reikning tilgreinda deferral, til dæmis Óinnleystra Tekna, eru þjónustukótinn stendur lýsingin sem færður er inn í reitinn **Desc Tímabils.** reit deferral sniðmátinu, til dæmis, "Útgjöld deferred fyrir Febrúar 2016" í.

## <a name="to-review-posted-deferrals-in-the-sales-deferral-summary-report"></a>Til að skoða bókaðar deferrals í skýrslunni Deferral yfirlit Yfir Sölu
**Bent**: liðir þessi aðferð er þau sömu og þegar er forskoða hvernig kostnaðinn deferrals eru bókuð.

1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Samantekt sölufrestunar**, og velja síðan viðeigandi tengil.
2. Í á **Deferral yfirlit Yfir Sölu** glugga í á **Staða sem er af** er færð inn dagsetningin þegar á að skoða deferred tekjur.
3. Veldu hnappinn **Vista**.

## <a name="see-also"></a>Sjá einnig
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Hvernig á að: Vinna með almennum færslubókum](ui-work-general-journals.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

