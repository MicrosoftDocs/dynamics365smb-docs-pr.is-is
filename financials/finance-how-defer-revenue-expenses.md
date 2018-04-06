---
title: "Fresta tekjum og útgjöldum| Microsoft Docs"
description: "Til að skrá tekjur og útgjöld á öðru tímabili en því sem færslan var bókuð á, geturðu sjálfkrafa seinkað eða frestað þeim fram yfir tiltekna áætlun."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 7b7b4ce9d2f464d6e2793a21fa5b321846ba9498
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="defer-revenues-and-expenses"></a>Fresta tekjum og öðrum útgjöldum
Hægt er að nota þessa aðgerð til samþykktar tekna á eða fyrir kostnað tímabil en tímabil sem færslan var bókuð í til sjálfkrafa defer tekjum og önnur útgjöld yfir tiltekinni áætlun.

Dreifa tekjur eða útgjöld fjárhagstímabila sem á að setja upp sniðmát deferral sem forðinn, varan eða fjárhagsreikningurinn sem tekjur eða kostnaðinn bókast. Þegar tengdar sölu eða innkaupaskjal er bókað fylgiskjal á tekjur eða kostnaðinn eru deferred til sögu reikningstímabil samkvæmt tímaáætlun deferral sem er stjórnað af stillingar í sniðmáti deferral og bókunardagsetningu.

## <a name="to-set-up-a-gl-account-for-deferral"></a>Verð sett upp fyrir fjárhagsreikning verks:
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **bókhaldslykill** og velja svo viðeigandi tengil.
2. Valið er **Nýtt** aðgerð.
3. Fyllt er út í reiti sem nauðsynlegt að stofna reikning fyrir deferred tekjur Fjárhags. Frekari upplýsingar er að finna í [Fjárhagur og bókhaldslyklar](finance-general-ledger.md).
4. Endurtaka skal þrep 2 og 3 eru endurtekin til að stofna nýjan reikning Fjárhags fyrir deferred útgjöld.

Fyrir báðar gerðir deferral, velja **Efnahagsreikningur** í reitnum **Tegund** og heiti reikninga athuga, t.d. "Óinnleystra Tekna" deferred tekjum og "Ógreidda Útgjöld" fyrir deferred útgjöld.

## <a name="to-set-up-a-deferral-template"></a>Uppsetning sniðmáts viðskiptamanns
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Sniðmát frestunnar** og velja svo viðeigandi tengil.
2. Valið er **Nýtt** aðgerð.
3. Fyllið inn í svæðin eftir þörfum.
4. Í á **Reikningsaðferð** er tilgreint hvernig **Upphæð** á hverju tímabili í á **Deferral Áætlun** glugganum reiknuð. Hægt er að velja um eftirfarandi kosti:

   * **Línuleg**: reglubundin deferral upphæðir eru reiknaðar fjölda tímabila dreift eftir lengd tímabils.
   * **Línuleg**: reglubundin deferral upphæðir eru reiknaðar fjölda tímabila dreift eftir lengd tímabils.
   * **Línuleg**: reglubundin deferral upphæðir eru reiknaðar fjölda tímabila dreift eftir lengd tímabils.
   * **Notandi Skilgreinir**: reglubundin deferral upphæðir eru ekki reiknaðir. Handvirkt þarf að fylla inn í reitinn **Upphæð** fyrir hvert tímabil í glugganum Frestunaráætlun. Frekari upplýsingar má fá í hlutanum "til Að breyta tímaáætlun deferral úr sölureikningi".
5. Í reitnum **Lýsing á tímabili** skal tiltaka lýsingu sem verður birt í færslum fyrir bókun frestunar. Má færa kóta eftirfarandi frátaka fyrir dæmigerðum gildi sem er settur sjálfkrafa þegar tímabil lýsing birtist.

   * Tilgreinir bókunardagsetningu fylgiskjalsins.
   * Tilgreinir bókunardagsetningu fylgiskjalsins.
   * Tilgreinir bókunardagsetningu fylgiskjalsins.
   * Tilgreinir bókunardagsetningu fylgiskjalsins.
   * Tilgreinir bókunardagsetningu fylgiskjalsins.
   * Tilgreinir bókunardagsetningu fylgiskjalsins.

 er á undan bókunardagsetningunni. Ef fært er inn "Útgjöld deferred fyrir %4 %6" síðan birt lýsing verður "Útgjöld deferred fyrir Febrúar 2016".

## <a name="to-assign-a-deferral-template-to-an-item"></a>Til að úthluta sérþekkingarkóða á vöru
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Sniðmát frestunnar** og velja svo viðeigandi tengil.
2. Opna spjald fyrir vöruna sem tekjur eða útgjöld er verður að deferred á reikningstímabilin þegar varan var seld eða keypt.
3. Í reitnum **Sjálfgefin Sniðmát Deferral** er deferral viðeigandi sniðmát er valið.

## <a name="to-change-a-deferral-schedule-from-a-sales-invoice"></a>Til að breyta tímaáætlun deferral úr sölureikningi
> [!NOTE]  
>   Liðir í þessu ferli eru þeir sömu og þegar frestunaráætlun er breytt, fyrir útgjöld, af innkaupareikningi.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Innkaupareikningar** og velja svo viðeigandi tengil.
2. Stofnaður sölureikningur fyrir vöru sem er til deferral sniðmát. Frekari upplýsingar eru í [Reikningsfæra sölur](sales-how-invoice-sales.md).

    Takið eftir að um leið og er að færa inn vöru (eða forða eða fjárhagsreiknings) í reikningslínunni, er **Deferral Kóta** fyllist með kóti sniðmáts deferral var úthlutað.
3. Valið er **Deferral Áætlun** aðgerð.
4. Í á **Deferral Áætlun** glugganum stillingar breytt í hausnum eða gildin í línunum, til dæmis til að defer upphæðinni öðrum reikningstímabil.
5. Valið er **Deferral Áætlun** aðgerð.
6. Velja hnappinn **Í lagi**. Áætlun deferral uppfærður til reikningnum. Sniðmát tengdar deferral er óbreytt.

## <a name="to-preview-how-deferred-revenues-or-expenses-will-be-posted-to-the-general-ledger"></a>Til að forskoða hvernig deferred tekjur eða útgjöld verða bókaðar í fjárhag.
> [!NOTE]  
>   Liðir í þessu ferli eru þeir sömu og þegar þú forskoðar hvernig kostnaðarfrestanir eru bókaðar.

1. Í reitnum **Bókaður Sölureikningur** er valið **leiðrétta** aðgerð.
2. Í reitnum **Forskoðun Bókunar** , valin **Fjárhagsfærsla**, og velja síðan **Sýna Tengdar Færslur**.

Fjárhagsfærslur sem á að bóka á tilgreindan frestunarreikning, til dæmis Óinnleystra Tekna, eru merktar með lýsingunni sem þú færðir inn í reitinn **Lýsing á tímabili** í frestunarsniðmátinu, til dæmis, „Útgjöldum frestað fyrir febrúar 2016“.

## <a name="to-review-posted-deferrals-in-the-sales-deferral-summary-report"></a>Til að skoða bókaðar deferrals í skýrslunni Deferral yfirlit Yfir Sölu
> [!NOTE]  
>   Liðir í þessu ferli eru þeir sömu og þegar þú endurskoðar skýrslu um samantekt á innkaupafrestun.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Samantekt á sölufrestun** og velja svo viðeigandi tengil.
2. Í á **Deferral yfirlit Yfir Sölu** glugga í á **Staða sem er af** er færð inn dagsetningin þegar á að skoða deferred tekjur.
3. Veldu hnappinn **Vista**.

## <a name="see-also"></a>Sjá einnig
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Vinna í færslubókum](ui-work-general-journals.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

