---
title: Láta Business Central leggja til gildi
description: 'Til að forðast handvirka útreikninga og klára verkhluta fljótt og nákvæmlega, geturðu sett upp sjálfvirka gagnafærslu þannig að Business Central fyllir upp í valda reiti.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '39, 251, 981'
ms.date: 07/16/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Leggja [!INCLUDE[prod_short](includes/prod_short.md)] til gildi
[!INCLUDE[prod_short](includes/prod_short.md)] getur hjálpað við að ljúka verkefni hraðar og réttara með því að forfylla í reiti eða klára línur með gögnum sem þú myndir annars þurfa að reikna og færa inn sjálfur. Þótt slíka sjálfvirka færslan er ekki alltaf rétt má breyta eftirá.

Virkni sem færir reitiargildi fyrir þig eru yfirleitt boðnir fyrir verk þar sem þú færir inn mikið magn af færslugögnum og vilt komast hjá villum og spara tíma. Þessi grein inniheldur úrval slíkra aðgerða. Fleiri hlutar bætist við í framtíðinni fyrir uppfært [!INCLUDE[prod_short](includes/prod_short.md)].

## Gátreiturinn **Leggja til Upphæð Mótreiknings** á síðunni **færslubókarkeyrsla**
Þegar, til dæmis, er verið að færa inn færslubókarlínur fyrir mörg útgjöld sem þarf að bóka á sama bankareikning og síðan er í hvert sinn sem ný færslubókarlína er færð inn fyrir kostnað er hægt að láta **reitinn Upphæð** í bankareikningslínunni uppfærast sjálfkrafa í þá upphæð sem stemmir á kostnaðinn. Nánari upplýsingar um að vinna færslubækur sjá [Vinna Með Færslubækur](ui-work-general-journals.md).

### Til að láta í **Upphæð** reitinn á færslubókarlínur fyllast út sjálfkrafa
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Færslubækur** og velja síðan viðkomandi tengil.
2. Á línunni fyrir keyrsla færslubók er valin á **Leggja til afstemmingarUpphæð** gátreitinn.
3. Opnaðu færslubókina og farðu í að skrá og bóka færslur með því að nota lýsta virkni fyrir sjálfvirka færslu á reitagildum.       

Fyrir upplýsingar um hvernig skuli setja upp persónulega færslubókarkeyrslu, til dæmis, fyrir meðhöndlun útgjalda, sjá [vinna með færslubækur](ui-work-general-journals.md)

## Reiturinn **Dagsetning móttöku fyllt út sjálfkrafa** á síðunni **Skráning greiðslna** glugga
Síðan **Skrá greiðslur** viðskm. sýnir útistandandi greiðslur á innleið sem línur sem tákna söluskjöl þar sem upphæð er komin á gjalddaga. Fyrir frekari upplýsingar um jöfnun greiðsla viðskiptavinar skal sjá [Stemma af greiðslur viðskiptamanns úr lista yfir ógreidd söluskjöl](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md).

Helstu aðgerðir þínar á síðunni eru að fylla út gátreitinn **Greiðslugerð** og Reiturinn **Dagsetning móttöku** . Verkefni er hægt að setja [!INCLUDE[prod_short](includes/prod_short.md)] upp til að sjálfvirkt færa inn vinnudagsetninguna í á **Dagsetning Móttöku** reit þegar valið er **greiðsla framkvæmd** gátreitinn.

### Til að láta fylla sjálfkrafa inn í reitinn **Gögn móttekin** á síðunni **Skráning greiðslu**
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning greiðsluskráningar** og velja síðan viðkomandi tengil.
2. Veldu gátreitinn **Dagsetning móttöku fyllt út sjálfkrafa**
3. Opna síðuna **Skrá greiðslur viðskiptamanns og vinna greiðslur** á innleið viðskiptamanna með því að nota lýstar aðgerðir fyrir sjálfvirka færslu á gildi reits.

## Sjá einnig .
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Fjármál](finance.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]