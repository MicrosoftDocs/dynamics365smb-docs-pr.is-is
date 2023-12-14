---
title: Láta Business Central leggja til gildi
description: 'Til að forðast handvirka útreikninga og klára verkhluta fljótt og nákvæmlega, geturðu sett upp sjálfvirka gagnafærslu þannig að Business Central fyllir upp í valda reiti.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '39, 251, 981'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Að láta [!INCLUDE[prod_short](includes/prod_short.md)] leggja til gildi
[!INCLUDE[prod_short](includes/prod_short.md)] getur hjálpað við að ljúka verkefni hraðar og réttara með því að forfylla í reiti eða klára línur með gögnum sem þú myndir annars þurfa að reikna og færa inn sjálfur. Þótt slíka sjálfvirka færslan er ekki alltaf rétt má breyta eftirá.

Virkni sem færir reitiargildi fyrir þig eru yfirleitt boðnir fyrir verk þar sem þú færir inn mikið magn af færslugögnum og vilt komast hjá villum og spara tíma. Í þessu efnisatriði er hluti af slíkri virkni. Fleiri hlutar bætist við í framtíðinni fyrir uppfært [!INCLUDE[prod_short](includes/prod_short.md)].

## Gátreiturinn **Leggja til Upphæð Mótreiknings** á síðunni **færslubókarkeyrsla**
Þegar til dæmis þu ert að færa inn færslubókarlína fyrir margir útgjöld sem þurfa allir að vera bókaðir á sama bankareikninginn, þá hvert skipti sem þú færir inn nýja færslubókarlínu fyrir útgjöld, geturðu haft **upphæðar** reitinn á bankareikningslínunni sjálfkrafa uppfærða í þá upphæð sem kemur jafnvægi á útgjöld. Nánari upplýsingar um að vinna færslubækur sjá [Vinna Með Færslubækur](ui-work-general-journals.md).

### Til að láta í **Upphæð** reitinn á færslubókarlínur fyllast út sjálfkrafa
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Færslubækur** og velja síðan viðkomandi tengil.
2. Á línunni fyrir keyrsla færslubók er valin á **Leggja til afstemmingarUpphæð** gátreitinn.
3. Opnaðu færslubókina og farðu í að skrá og bóka færslur með því að nota lýsta virkni fyrir sjálfvirka færslu á reitagildum.       

Fyrir upplýsingar um hvernig skuli setja upp persónulega færslubókarkeyrslu, til dæmis, fyrir meðhöndlun útgjalda, sjá [vinna með færslubækur](ui-work-general-journals.md)

## Reiturinn **Dagsetning móttöku fyllt út sjálfkrafa** á síðunni **Skráning greiðslna** glugga
Síðan **skráning greiðslna** Sýnir útistandandi væntanlega innkomu á línum sem tákna söluskjöl þar sem upphæð er fallinn á gjalddaga. Fyrir frekari upplýsingar um jöfnun greiðsla viðskiptavinar skal sjá [Stemma af greiðslur viðskiptamanns úr lista yfir ógreidd söluskjöl](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md).

Aðal aðgerðir þínar á síðunni eru að fylla í gátreitinn **greiðslur framkvæmdar** og reitinn **Dagsetning Móttöku**. Verkefni er hægt að setja [!INCLUDE[prod_short](includes/prod_short.md)] upp til að sjálfvirkt færa inn vinnudagsetninguna í á **Dagsetning Móttöku** reit þegar valið er **greiðsla framkvæmd** gátreitinn.

### Til að láta fylla sjálfkrafa inn í reitinn **Gögn móttekin** á síðunni **Skráning greiðslu**
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning greiðsluskráningar** og velja síðan viðkomandi tengil.
2. Veldu gátreitinn **Dagsetning móttöku fyllt út sjálfkrafa**
3. Opnaðu síðuna **Greiðslu Skráning** og byrja að vinna innsend greiðslur viðskiptamanns með þeim aðgerðum sem var lýst fyrir sjálfvirka innfærslu fyrir reitargildi.

## Sjá einnig
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Fjármál](finance.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]