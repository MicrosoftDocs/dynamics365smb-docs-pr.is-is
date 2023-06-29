---
title: Vinna með endurteknar tekjur
description: Frekari upplýsingar um tiltæka valmöguleika sem gera þér kleift að senda greiðslureikninga til viðskiptavina þinna og skrá endurteknar tekjur.
author: AndreiPanko
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'recurring, invoicing, subscription, billing'
ms.search.form: 283
ms.reviewer: edupont
ms.date: 04/01/2021
ms.author: andreipa
---
# <a name="work-with-recurring-revenue-in-"></a><a name="work-with-recurring-revenue-in-"></a>Vinna með endurteknar tekjur í [!INCLUDE[prod_short](includes/prod_short.md)]

Mörg fyrirtæki eru að færa sig úr tekjulíkönum þar sem tekjur eru úr einskiptiskaupum viðskiptavinar í viðskiptalíkan þar sem tekjur eru gerðar á endurteknum grunni í skiptum fyrir stöðugt aðgengi að afhendingu góðrar vöru eða þjónustu.
[!INCLUDE[prod_short](includes/prod_short.md)] er með eftirfarandi valmöguleika til að gera sendingerferli reikninga í gegnum viðskiptavini og skráningu endurtekinna tekna sjálfvirkt. 

## <a name="register-revenue-with-a-recurring-general-journal"></a><a name="register-revenue-with-a-recurring-general-journal"></a>Skrá tekjur með ítrekunarfærslubók

Ítrekunarbók er færslubók með sérstökum reitum til að stjórna færslum sem eru bókaðar reglulega með litlum eða engum breytingum, t.d. leigu, áskriftum, rafmagni eða hita. Með því að nota þessa reiti fyrir endurteknar færslur er hægt að bóka bæði fastar og breytilegar upphæðir. Með ítrekunarbók þarf aðeins einu sinni að setja inn færslur sem bókaðar verða reglulega. Það þýðir að reikningar, víddir og víddargildi o.s.frv sem fært er inn verður áfram í færslubókinni að lokinni bókun. Óhjákvæmilegar leiðréttingar má gera við hverja bókun.

### <a name="why-use-this-option"></a><a name="why-use-this-option"></a>Af hverju að nota þennan möguleika

Með þessum valkosti eru sveigjanleg reikningsfærslutímabil skilgreind með [Dagsetningarformúlum](ui-enter-date-ranges.md#use-date-formulas).

Með þessum valkosti er hins vegar ekki hægt að prenta og senda reikninga í sjálfgefinni útgáfu af [!INCLUDE[prod_short](includes/prod_short.md)].  

Nánari upplýsingar eru í [Vinna með Ítrekunarbækur](ui-work-general-journals.md#work-with-recurring-journals).  

## <a name="create-multiple-invoices-based-on-a-recurring-job-journal"></a><a name="create-multiple-invoices-based-on-a-recurring-job-journal"></a>Stofna marga reikninga byggða á ítrekunarverkbók verka

Ítrekunarbók vinnslunnar er ítarlegri valkostur en almenn færslubók. Hægt er að skilgreina vörur, tilföng og fjárhagsreikninga sem þarf að endurtaka fyrir hvert verk, og tilgreina tíðni endurtekninga.  

Þegar búið er að bóka endurtekna verkbók er hægt að búa til marga reikninga með **Stofna verksölureikning**. Hægt er að yfirfara og bóka stofnaða reikninga á síðunni **Sölureikningar** .

### <a name="why-use-this-option-1"></a><a name="why-use-this-option-1"></a>Af hverju að nota þennan möguleika

Með þessum valkosti fylgir staðlað reikningsfærsluferli með öllum fríðindum þess, þar á meðal stöðluðu og útliti viðskiptavinar fyrir samskipti. Einnig er hægt að skilgreina verð fyrir hvert verk fyrir sig.

Fyrir hvern nýjan viðskiptavin verður hins vegar að stofna nýtt starf og bæta línum við ítrekunarbókina. 

Frekari upplýsingar er að finna í [Stofna verkbókarlínur](projects-how-record-job-usage.md#to-create-job-journal-lines-manually) og [Búa til marga sölureikninga verks](projects-how-invoice-jobs.md#to-create-multiple-job-sales-invoices).

## <a name="create-multiple-invoices-based-on-recurring-sales-lines"></a><a name="create-multiple-invoices-based-on-recurring-sales-lines"></a>Stofna marga reikninga byggða á endurteknum sölulínum

Ef þú þarft oft að stofna innkaupa- og sölulínur með svipuðum upplýsingum, geturðu sett upp endurtekntar sölulínur, sem þú getur svo fært inn í ítrekuð sölu- og innkaupaskjöl, til dæmis fyrir endurteknar áfyllingapantanir. Notaðu runuvinnsluna **Stofna ítrekaða sölureikninga** til að stofna sölureikninga samkvæmt endurteknum sölulínum sem eru tengdar við viðskiptamenn og með bókunardagsetningum innan gildir-frá og gildir-til dagsetningum sem hafa verið tilgreindar í endurteknum sölulínum.  

### <a name="why-use-this-option-2"></a><a name="why-use-this-option-2"></a>Af hverju að nota þennan möguleika

Með þessum valkosti er hægt að úthluta sömu ítrekunarlínum á marga viðskiptamenn. Hægt er að skilgreina gildistímabil fyrir endurteknar sölulínur tiltekins viðskiptavinar. Hægt er að úthluta mörgum ítrekunarlínum á sama viðskiptavin og allir þeirra verða teknir með í reikningunum.

Hins vegar er engin leið til að setja fast verð fyrir vörur vegna þess að [!INCLUDE[prod_short](includes/prod_short.md)] notar raunverulegt verð og afslátt á dagsetningu skjals, og reynir að finna bestu samsetningu sem gefur lægsta verðið.  

Nánari upplýsingar er að finna í [Stofna ítrekaðar sölu og innkaupalínur](sales-how-work-standard-lines.md).

## <a name="recurring-invoices-with-service-contract"></a><a name="recurring-invoices-with-service-contract"></a>Endurteknir reikningar með þjónustusamning

Þjónustusamningur inniheldur samkomulag viðskiptamanna og fyrirtækisins um þjónustusamning. Í þjónustusamningi er samkomulag um þjónustustig og þjónustuvörurnar sem þjónustaðar eru samkvæmt samningnum.  

Hægt er að skilgreina upphafsdagsetningu samningsins, reikningstímabilsins, hvort samningurinn er fyrirframgreiddur og verðuuppfærslum ef þú ætlar að breyta verði þegar samningurinn er virkur. Hægt er að nota bæði þjónustuvörur eða vörur í þjónustusamningslínum.
Hægt er að  stofna samningssniðmát til að skilgreina hvernig eigi að stofna ákveðnar tegundir samninga.  

### <a name="why-use-this-option-3"></a><a name="why-use-this-option-3"></a>Af hverju að nota þennan möguleika

Með þessum valkosti er notaður hluti af virkni ítarlegrar þjónustustýringar sem takmarkast ekki við útgáfu af endurteknum reikningum heldur styður viðgerðir og vettvangsaðferðir.

Þessi valkostur krefst hins vegar Premium-leyfis. Uppsetning þjónustustjórnunar og viðhald þess skilar e.t.v. ekki miklum ávinningi í einfaldari áskriftaraðstæðum.  

Frekari upplýsingar, sjá [Vinna með þjónustusamninga og þjónustusamningstilboð](service-how-to-create-service-contracts-and-service-contract-quotes.md) og [Rukka nokkra þjónustusamninga](service-how-create-invoices.md#to-invoice-several-service-contracts).

## <a name="related-features"></a><a name="related-features"></a>Tengdir eiginleikar
Nokkrir tengdir eiginleikar eru í [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="blanket-sales-orders"></a><a name="blanket-sales-orders"></a>Standandi sölupantanir

Standandi sölupöntun er rammi fyrir langtímasamning milli fyrirtækisins þíns og viðskiptavinarins þíns.
Standandi pöntun er yfirleitt stofnuð þegar viðskiptamaður hefur skuldbundið sig til kaupa á miklu magni sem afhenda á í nokkrum minni afhendingum á ákveðnu tímabili. Standandi pantanir ná oft eingöngu yfir eina vöru með fyrirframákveðnum afhendingardögum. Aðalástæðan fyrir notkun standandi pantana í stað sölupantana er sú að magn sem tilgreint er á standandi pöntun hafa ekki áhrif á framboð vöru, en hægt er að nota það í áætlanagerð.

#### <a name="why-use-this-option-4"></a><a name="why-use-this-option-4"></a>Af hverju að nota þennan möguleika

Með þessum valkosti er hægt að nota áætlaða eftirspurn þannig að upplýsingarnar standist eðlilegar áætlunarvenjur. Frekari upplýsingar er að finna í [Eftirspurnarspá og standandi pantanir](design-details-central-concepts-of-the-planning-system.md#demand-forecasts-and-blanket-orders).  

Sjálfgefin útgáfa býður hins vegar ekki upp á þann möguleika að vinna úr mörgum standandi pöntunum í fjöldahjálparglugga án breytinga.

Nánari upplýsingar eru í [Vinna með standandi sölupantanir](sales-how-to-create-blanket-sales-orders.md).

### <a name="recurring-orders-norway"></a><a name="recurring-orders-norway"></a>Endurteknar pantanir (Noregur)

Hægt er að nota endurteknar pantanir til að stofna standandi pöntunarsniðmát þannig að hægt sé að stofna sölupantanir út frá dagsetningabilum sem eru skilgreind. Ef sama sölupöntun er t.d. afhent á tveggja vikna fresti er hægt að nota standandi sölupöntun og stofna endurteknar pantanir.
Hægt er að nota endurtekna flokka til að skilgreina svið færibreytna sem sýna hvernig pantanir eru gerðar. Þessum flokkum er úthlutað á standandi pantanir sem þarf að stofna reglulega. Til að búa til endurteknar pantanir þarf reglulega að keyra ferli til að stofna endurteknar pantanir. 

#### <a name="why-use-this-option-5"></a><a name="why-use-this-option-5"></a>Af hverju að nota þennan möguleika

Með þessum valkosti er hægt að velja á milli fastra verða og „bestu“ verða.

Þetta er hins vegar aðeins í boði í Noregi. Hægt er að skilgreina gildistímabil á ítrekunarflokksstigi.

Nánari upplýsingar eru í [Endurteknar pantanir](LocalFunctionality/Norway/recurring-orders.md).

### <a name="recurring-revenue-and-subscription-billing-by-other-providers"></a><a name="recurring-revenue-and-subscription-billing-by-other-providers"></a>Endurteknar tekjur og áskriftarreikningar frá öðrum veitum

Á [AppSource.microsoft.com](https://appsource.microsoft.com/), er hægt að fá viðbætur fyrir Business Central. Sumar viðbætur eru veittar af Microsoft, og aðrar viðbætur eru veittar af öðrum fyrirtækjum. Listi yfir viðbætur frá öðrum fyrirtækjum lengist í hverjum mánuði. Fylgstu því með á [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646) og fáðu forrit sem aðstoða þig í vinnunni í Business Central.  

## <a name="see-also"></a><a name="see-also"></a>Sjá einnig .

[Dagsetningarreiknireglur](ui-enter-date-ranges.md#use-date-formulas)  
[Vinna með Ítrekunarbækur](ui-work-general-journals.md#work-with-recurring-journals)  
[Stofna færslubókarlínur verks](projects-how-record-job-usage.md#to-create-job-journal-lines-manually)  
[Búa til marga sölureikninga verks](projects-how-invoice-jobs.md#to-create-multiple-job-sales-invoices)  
[Stofna ítrekaðar sölu- og innkaupalínur](sales-how-work-standard-lines.md)  
[Vinna með þjónustusamninga og þjónustusamningstilboð](service-how-to-create-service-contracts-and-service-contract-quotes.md)  
[Reikningsfæra nokkra þjónustusamninga](service-how-create-invoices.md#to-invoice-several-service-contracts)  
[Eftirspurnarspá og standandi pantanir](design-details-central-concepts-of-the-planning-system.md#demand-forecasts-and-blanket-orders)  
[Vinna með standandi sölupantanir](sales-how-to-create-blanket-sales-orders.md)  
[Endurteknar pantanir (Noregur)](LocalFunctionality/Norway/recurring-orders.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
