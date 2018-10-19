---
title: "Setja upp tillögur um reitagildi | Microsoft Docs"
description: "Til að forðast handvirka útreikninga og klára verkhluta fljótt og nákvæmlega, geturðu sett upp sjálfvirka gagnafærslu þannig að Business Central fyllir upp í valda reiti."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 6436ef2e70c594f16097d02a3a1bef4ed40e77c0
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="letting-included365finincludesd365finmdmd-suggest-values"></a>Að láta [!INCLUDE[d365fin](includes/d365fin_md.md)] leggja til gildi
[!INCLUDE[d365fin](includes/d365fin_md.md)] getur hjálpað við að ljúka verkefni hraðar og réttara með því að forfylla í reiti eða klára línur með gögnum sem þú myndir annars þurfa að reikna og færa inn sjálfur. Þótt slíka sjálfvirka færslan er ekki alltaf rétt má breyta eftirá.

Virkni sem færir reitiargildi fyrir þig eru yfirleitt boðnir fyrir verk þar sem þú færir inn mikið magn af færslugögnum og vilt komast hjá villum og spara tíma. Í þessu efnisatriði er hluti af slíkri virkni. Fleiri hlutar bætist við í framtíðinni fyrir uppfært [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="the-suggest-balancing-amount-check-box-in-the-general-journal-batches-window"></a>Gátreiturinn **Leggja til Upphæð Mótreiknings** í **færslubókarkeyrsla** glugganum
Þegar til dæmis þu ert að færa inn færslubókarlína fyrir margir útgjöld sem þurfa allir að vera bókaðir á sama bankareikninginn, þá hvert skipti sem þú færir inn nýja færslubókarlínu fyrir útgjöld, geturðu haft **upphæðar** reitinn á bankareikningslínunni sjálfkrafa uppfærða í þá upphæð sem kemur jafnvægi á útgjöld. Nánari upplýsingar um að vinna með færslubækur sjá [Vinna með færslubækur](ui-work-general-journals.md).

### <a name="to-have-the-amount-field-on-balancing-general-journal-lines-filled-automatically"></a>Til að láta í **Upphæð** reitinn á færslubókarlínur fyllast út sjálfkrafa
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Færslubækur** og veldu síðan tengda tengilinn.
2. Á línunni fyrir keyrsla færslubók er valin á **Leggja til afstemmingarUpphæð** gátreitinn.
3. Opnaðu færslubókina og farðu í að skrá og bóka færslur með því að nota lýsta virkni fyrir sjálfvirka færslu á reitagildum.       

Fyrir upplýsingar um hvernig skuli setja upp persónulega færslubókarkeyrslu, til dæmis, fyrir meðhöndlun útgjalda, sjá [Vinna með færslubækur](ui-work-general-journals.md)

## <a name="the-automatically-fill-date-received-field-in-the-payment-registration-window"></a>Reiturinn **Dagsetning móttöku fyllt út sjálfkrafa** í glugganum **Skráning greiðslna** glugga
Glugginn **skráning greiðslna**Sýnir útistandandi væntanlega innkomu á línum sem tákna söluskjöl þar sem upphæð er fallinn á gjalddaga. Fyrir frekari upplýsingar um jöfnun greiðsla viðskiptavinar sjá [Stemma handvirkt af greiðslur viðskiptamanns úr lista yfir ógreidda söluskjöl.](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md)

Aðal aðgerðir þínar í glugganum eru að fylla í gátreitur **greiðslur framkvæmdar** og **Dagsetning Móttöku** reit. Verkefni er hægt að setja [!INCLUDE[d365fin](includes/d365fin_md.md)] upp til að sjálfvirkt færa inn vinnudagsetninguna í á **Dagsetning Móttöku** reit þegar valið er **greiðsla framkvæmd** gátreitinn.

### <a name="to-have-the-date-received-field-in-the-payment-registration-window-filled-automatically"></a>Til að láta **Sjálfkrafa fylla inn í Dagsetning Móttöku** í á **Greiðslu Skráning** glugga
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning skráning greiðslna** og veldu síðan tengda hlekkinn.
2. Veldu gátreitinn **Dagsetning móttöku fyllt út sjálfkrafa**
3. Opnaðu Glugginn **Greiðslu Skráning** og byrja að vinna innsend greiðslur viðskiptamanns með þeim aðgerðum sem var lýst fyrir sjálfvirka innfærslu fyrir reitargildi.

## <a name="see-also"></a>Sjá einnig
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Fjármál](finance.md)

