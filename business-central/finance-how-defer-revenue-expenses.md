---
title: Fresta tekjum og öðrum útgjöldum
description: Til að skrá tekjur og útgjöld á tímabilum þegar færslan var ekki bókuð, geturðu sjálfkrafa seinkað eða frestað þeim fram yfir tiltekna áætlun.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.search.form: 1700, 1701, 1702, 1703, 1704, 1705, 1706, 1707
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: a99b8e5e14d7224fb23da3f59a5fe5274b2eef33
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/14/2022
ms.locfileid: "7971146"
---
# <a name="defer-revenues-and-expenses"></a>Fresta tekjum og öðrum útgjöldum

Hægt er að nota þessa aðgerð til samþykktar tekna á eða fyrir kostnað tímabil en tímabil sem færslan var bókuð í til sjálfkrafa defer tekjum og önnur útgjöld yfir tiltekinni áætlun.

Dreifa tekjur eða útgjöld fjárhagstímabila sem á að setja upp sniðmát deferral sem forðinn, varan eða fjárhagsreikningurinn sem tekjur eða kostnaðinn bókast. Þegar tengdar sölu eða innkaupaskjal er bókað fylgiskjal á tekjur eða kostnaðinn eru deferred til sögu reikningstímabil samkvæmt tímaáætlun deferral sem er stjórnað af stillingar í sniðmáti deferral og bókunardagsetningu.

## <a name="to-set-up-a-gl-account-for-deferral"></a>Verð sett upp fyrir fjárhagsreikning verks:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bókhaldslykill** og velja síðan viðkomandi tengil.
2. Valið er **Nýtt** aðgerð.
3. Fyllt er út í reiti sem nauðsynlegt að stofna reikning fyrir deferred tekjur Fjárhags. Frekari upplýsingar er að finna í [Fjárhagur og bókhaldslyklar](finance-general-ledger.md).
4. Endurtaka skal þrep 2 og 3 eru endurtekin til að stofna nýjan reikning Fjárhags fyrir deferred útgjöld.

Fyrir báðar gerðir deferral, velja **Efnahagsreikningur** í reitnum **Tegund** og heiti reikninga athuga, t.d. "Óinnleystra Tekna" deferred tekjum og "Ógreidda Útgjöld" fyrir deferred útgjöld.

## <a name="to-set-up-a-deferral-template"></a>Uppsetning sniðmáts viðskiptamanns

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sniðmát frestunar** og velja síðan viðkomandi tengil.
2. Valið er **Nýtt** aðgerð.
3. Fyllið inn í svæðin eftir þörfum.
4. Á síðunni **Reikningsaðferð** er tilgreint hvernig **Upphæð** á hverju tímabili í á **Deferral Áætlun** glugganum reiknuð. Hægt er að velja um eftirfarandi kosti:

   * **Línuleg**: reglubundin deferral upphæðir eru reiknaðar fjölda tímabila dreift eftir lengd tímabils.
   * **Línuleg**: reglubundin deferral upphæðir eru reiknaðar fjölda tímabila dreift eftir lengd tímabils.
   * **Línuleg**: reglubundin deferral upphæðir eru reiknaðar fjölda tímabila dreift eftir lengd tímabils.
   * **Notandi Skilgreinir**: reglubundin deferral upphæðir eru ekki reiknaðir. Handvirkt þarf að fylla inn í reitinn **Upphæð** fyrir hvert tímabil á síðunni Frestunaráætlun. Frekari upplýsingar má fá í hlutanum "til Að breyta tímaáætlun deferral úr sölureikningi".
5. Í reitnum **Lýsing á tímabili** Tilgreinir lýsingu sem verður birt í færslum fyrir bókun frestunar. Má færa kóta eftirfarandi frátaka fyrir dæmigerðum gildi sem er settur sjálfkrafa þegar tímabil lýsing birtist.

   * %1 = Mánaðardagur fyrir bókunardagsetningu tímabils
   * %2 = Vikunúmer fyrir bókunardagsetningu tímabils
   * %3 = Mánaðarnúmer fyrir bókunardagsetningu tímabils
   * %4 = Mánaðarheiti fyrir bókunardagsetningu tímabils
   * %5 = Heiti reikningstímabils fyrir bókunardagsetningu tímabils
   * %6 = Fjárhagsár fyrir bókunardagsetningu tímabils

 er á undan bókunardagsetningunni. Ef fært er inn „Útgjöldum frestað fyrir %4 %6“, verður lýsingin sem birtist „Útgjöldum frestað fyrir febrúar 2016“.

## <a name="to-assign-a-deferral-template-to-an-item"></a>Til að úthluta sérþekkingarkóða á vöru

> [!NOTE]  
> Liðir í þessu ferli eru þeir sömu og þegar þú úthlutar frestunarsniðmáti til fjárhagsreiknings eða tilfangs.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vara** og velja síðan viðkomandi tengil.
2. Opna spjald fyrir vöruna sem tekjur eða útgjöld er verður að deferred á reikningstímabilin þegar varan var seld eða keypt.
3. Í reitnum **Sjálfgefin Sniðmát Deferral** er deferral viðeigandi sniðmát er valið.

## <a name="to-change-a-deferral-schedule-from-a-sales-invoice"></a>Til að breyta tímaáætlun deferral úr sölureikningi

> [!NOTE]  
> Liðir í þessu ferli eru þeir sömu og þegar frestunaráætlun er breytt, fyrir útgjöld, af innkaupareikningi.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sölureikningar** og velja síðan viðkomandi tengil.
2. Stofnaður sölureikningur fyrir vöru sem er til deferral sniðmát. Frekari upplýsingar eru í [Reikningsfæra sölur](sales-how-invoice-sales.md).

    Takið eftir að um leið og er að færa inn vöru (eða forða eða fjárhagsreiknings) í reikningslínunni, er **Deferral Kóta** fyllist með kóti sniðmáts deferral var úthlutað.
3. Valið er **Deferral Áætlun** aðgerð.
4. Á síðunni **Deferral Áætlun** stillingar breytt í hausnum eða gildin í línunum, til dæmis til að fresta upphæðinni á annað reikningstímabil.
5. Valið er **Deferral Áætlun** aðgerð.
6. Velja hnappinn **Í lagi**. Áætlun deferral uppfærður til reikningnum. Sniðmát tengdar deferral er óbreytt.

## <a name="to-preview-how-deferred-revenues-or-expenses-will-be-posted-to-the-general-ledger"></a>Til að forskoða hvernig deferred tekjur eða útgjöld verða bókaðar í fjárhag.

> [!NOTE]  
> Liðir í þessu ferli eru þeir sömu og þegar þú forskoðar hvernig kostnaðarfrestanir eru bókaðar.

1. Á síðunni **Sölureikningur** er valin aðgerðin **Forskoðun bókunar**.
2. Á síðunni **Forskoðun bókunar** er valin aðgerðin **Fjárhagsfærsla** og síðan valin aðgerðin **Sýna tengdar færslur**.

Fjárhagsfærslur sem á að bóka á tilgreindan frestunarreikning, til dæmis Óinnleystar tekjur, eru auðkenndar með lýsingunni sem er færð inn í reitinn **Lýsing á tímabili** reit í sniðmáti frestunar, til dæmis, „Frestuð útgjöld fyrir Febrúar 2016“.

## <a name="to-review-posted-deferrals-in-the-sales-deferral-summary-report"></a>Til að skoða bókaðar deferrals í skýrslunni Deferral yfirlit Yfir Sölu

> [!NOTE]  
> Liðir í þessu ferli eru þeir sömu og þegar þú endurskoðar skýrslu um samantekt á innkaupafrestun.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Samantekt frestunar sölu** og velja síðan viðkomandi tengil.
2. Á síðunni **Samantekt frestunar sölu** í reitnum **Staða frá og með** skal færa inn dagsetninguna upp að því marki sem þú vilt skoða frestaðar tekjur.
3. Veldu hnappinn **Vista**.

## <a name="see-also"></a>Sjá einnig

[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Vinna í færslubókum](ui-work-general-journals.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]