---
title: "Leyfa Dynamics 365 for Financials að stinga upp á gildum | Microsoft Docs"
description: "Lýsir því hvernig eigi að láta kerfið forfylla í reiti með gildunum sem annars væru reiknaðir og fylltir út handvirkt."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 03/15/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 785ad537f81b8388aa14654f375599a13b66e3c5
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="letting-dynamics-365-for-financials-suggest-values"></a>Leyfa Dynamics 365 for Financials að stinga upp á gildum
[!INCLUDE[d365fin](includes/d365fin_md.md)] getur hjálpað við að ljúka verkefni hraðar og réttara með því að forfylla í reiti eða klára línur með gögnum sem þú myndir annars þurfa að reikna og færa inn sjálfur. Þótt slíka sjálfvirka færslan er ekki alltaf rétt má breyta eftirá.

Virkni sem færir reitiargildi fyrir þig eru yfirleitt boðnir fyrir verk þar sem þú færir inn mikið magn af færslugögnum og vilt komast hjá villum og spara tíma. Í þessu efnisatriði er hluti af slíkri virkni. Fleiri hlutar bætist við í framtíðinni fyrir uppfært [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="the-suggest-balancing-amount-check-box-in-the-general-journal-batches-window"></a>Gátreiturinn **Leggja til Upphæð Mótreiknings** í **færslubókarkeyrsla** glugganum
Þegar til dæmis þu ert að færa inn færslubókarlína fyrir margir útgjöld sem þurfa allir að vera bókaðir á sama bankareikninginn, þá hvert skipti sem þú færir inn nýja færslubókarlínu fyrir útgjöld, geturðu haft **upphæðar ** reitinn á bankareikningslínunni sjálfkrafa uppfærða í þá upphæð sem kemur jafnvægi á útgjöld. Nánari upplýsingar um að vinna færslubækur sjá [Vinna í færslubókum](ui-work-general-journals.md).

### <a name="to-have-the-amount-field-on-balancing-general-journal-lines-filled-automatically"></a>Til að láta í **Upphæð** reitinn á færslubókarlínur fyllast út sjálfkrafa
1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Færslubækur**, og velja síðan viðeigandi tengil.
2. Á línunni fyrir keyrsla færslubók er valin á **Leggja til afstemmingarUpphæð** gátreitinn.
3. Opnaðu færslubókina og farðu í að skrá og bóka færslur með því að nota lýsta virkni fyrir sjálfvirka færslu á reitagildum.       

Fyrir upplýsingar um hvernig skuli setja upp persónulega færslubókarkeyrslu, til dæmis, fyrir meðhöndlun útgjalda, sjá [Vinna í færslubókum](ui-work-general-journals.md)

## <a name="the-automatically-fill-date-received-field-in-the-payment-registration-window"></a>Reiturinn **Dagsetning móttöku fyllt út sjálfkrafa** í glugganum **Skráning greiðslna** glugga
Glugginn **skráning greiðslna**Sýnir útistandandi væntanlega innkomu á línum sem tákna söluskjöl þar sem upphæð er fallinn á gjalddaga. Fyrir frekari upplýsingar um jöfnun greiðsla viðskiptavinar sjá [Hvernig skal stemma handvirkt af greiðslur  viðskiptamanns úr lista yfir ógreidda söluskjöl.](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md)

Aðal aðgerðir þínar í glugganum eru að fylla í gátreitur **greiðslur framkvæmdar** og **Dagsetning Móttöku** reit. Verkefni er hægt að setja [!INCLUDE[d365fin](includes/d365fin_md.md)] upp til að sjálfvirkt færa inn vinnudagsetninguna í á **Dagsetning Móttöku** reit þegar valið er **greiðsla framkvæmd ** gátreitinn.

### <a name="to-have-the-date-received-field-in-the-payment-registration-window-filled-automatically"></a>Til að láta **Sjálfkrafa fylla inn í Dagsetning Móttöku** í á **Greiðslu Skráning** glugga
1. Efst í hægra horni skal velja reitinn **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Uppsetning greiðsluskráningar**, og velja síðan viðeigandi tengil.
2. Veldu gátreitinn **Dagsetning móttöku fyllt út sjálfkrafa**
3. Opnaðu Glugginn **Greiðslu Skráning** og byrja að vinna innsend greiðslur viðskiptamanns með þeim aðgerðum sem var lýst fyrir sjálfvirka innfærslu fyrir reitargildi.

## <a name="see-also"></a>Sjá einnig
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Fjármál](Finance.md)


