---
title: "Hvernig á að setja upp grunndagatal | Microsoft Docs"
description: "Hægt er að úthluta fyrirtækinu og viðskiptafélögum, viðskiptamönnum, birgjum og stöðvum grunndagatali. Afhendingar –og móttökudagsetningar á væntanlegum sölupöntunum, innkaupapöntunum, millifærslupöntunum og framleiðslupöntunarlínum eru reiknaðar eftir virkum dögum á dagatalinu."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 61ad86f72f86cd9f6e1667dac445bfaa930d339f
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-base-calendars"></a>Setja upp grunndagatöl
Hægt er að úthluta fyrirtækinu og viðskiptafélögum, viðskiptamönnum, birgjum og stöðvum grunndagatali. Afhendingar –og móttökudagsetningar á væntanlegum sölupöntunum, innkaupapöntunum, millifærslupöntunum og framleiðslupöntunarlínum eru reiknaðar eftir virkum dögum á dagatalinu. Þegar nýtt grunndagatal er sett upp felst meginverkefnið í að tilgreina og skilgreina þá frídaga sem eiga að gilda.  

## <a name="to-set-up-a-base-calendar"></a>Uppsetning grunndagatals  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Grunndagatal** og velja svo viðeigandi tengil.  
2.  Valið er **Nýtt** aðgerð.  
3.  Reiturinn **Kóti** er fylltur út.  
4. Velja skal **Viðhalda breytingum á Grunndagatali** aðgerðina.
5. Í glugganum **Breytingar á grunndagatali** er notaður reiturinn **Ítrekun Kerfi** til þess að merkja tiltekna dagsetningu eða dag sem fastan frídag. Í boði eru tveir kostir, **Árleg ítrekun** eða **Vikuleg ítrekun**.  

    Ef valin er **Árleg ítrekun** þarf einnig að færa inn viðkomandi dagsetningu í reitinn **Dagsetning**.  

    Ef valin er **Vikuleg ítrekun** þarf einnig að færa inn viðkomandi vikudag í reitinn **Dagur**. Ef reiturinn er hafður auður verður að fylla út reitinn **Dagsetning**. Reiturinn **Dagur** er fylltur sjálfkrafa út.  

Þegar færsla er færð inn er reiturinn **Frídagar** valinn. Hægt er að velja til að hreinsa gátmerkið til að gera þetta virkum degi.  
 Þegar horfið er aftur til grunndagatalsspjaldsins sést að frídagafærslurnar sem gerðar voru hafa verið uppfærðar. Þessar færslur birtast nú í rauðu og reiturinn **Engin vinna**.  

> [!NOTE]  
>  Þegar nýtt grunndagatal er sett upp má velja línur úr dagatali sem tiltækt er og afrita þær. Þetta er gert í glugganum **Breytingar á grunndagatali**.  

> [!IMPORTANT]  
>  Hvers kyns grunndagatal sem skilgreint er fyrir lánadrottininn eða birgðageymsluna hefur áhrif á það hvernig dagsetningarnar eru reiknaðar út og sléttaðar til virkra daga.
Tilgreinir dagsetningarformúlu fyrir þann tíma sem það tekur að fylla á vöruna. Hann er notaður til að reikna reitinn **Áætluð dagsetning innhreyfingar** ef reiknað er út áfram og reitinn **Pöntunardagsetning** ef reiknað er út afturábak. Sjá hlutann „Útreiknaður afhendingartími“.

## <a name="lead-time-calculation"></a>Útreikn. afhendingartíma
Hvers kyns grunndagatal sem skilgreint er fyrir lánadrottininn eða birgðageymsluna hefur áhrif á það hvernig dagsetningarnar eru reiknaðar út og sléttaðar til virkra daga. Í samræmi við það eru dagsetningarreitirnir tveir í innkaupapöntunarlínunum reiknaðir á eftirfarandi hátt við ólík skilyrði.

|Stefna útreiknings|Dagatal lánardrottins skilgreint|Dagatal lánardrottins ekki skilgreint|
|---------------------|-----------------------|---------------------------|
|Framvirk|áætluð móttökudagsetning = pöntunardagsetning + afhendingartími lánardrottins (samkvæmt dagatali lánardrottins, sléttað upp í næsta virka dag, fyrst í dagatali lánardrottins og síðan í dagatali birgðageymslu)|áætluð móttökudagsetning = pöntunardagsetning + afhendingartími lánardrottins (samkvæmt birgðageymsludagatali)|
|Afturvirk|pöntunardagsetning = ráðgerð móttökudagsetning - afhendingartími lánardrottins (samkvæmt dagatali lánardrottins, sléttað upp í síðasta virka dag, fyrst í dagatali lánardrottins og síðan í dagatali birgðageymslu)|pöntunardagsetning = ráðgerð móttökudagsetning - afhendingartími lánardrottins (samkvæmt birgðageymsludagatali)|

> [!NOTE]
> Auk útreiknings afhendingartíma sem hefur áhrif á ráðgerða móttökudagsetningu og pöntunardagsetningu, eins og sýnt er í töflunni hér að ofan, getur afgreiðslutíma vöruhúss og öryggisforskoti verið bætt við reiknireglurnar sem reikna gildið í reitnum **Áætluð dagsetning innhreyfingar**, sem hér segir: Ráðgerð dagsetning innhreyfingar + öryggisforskot + á innleið afgreiðslutími vöruhúss  = Áætluð dagsetning innhreyfingar.

> [!Important]
> Ef birgðageymslan notar dagatal sem er mjög frábrugðið dagatali lánardrottna er mikilvægt að setja upp sérstök dagatöl fyrir þá lánardrottna til að reikna réttan afhendingartíma. Upplýsingar um hvernig á að setja upp dagatöl lánardrottna eru að finna í hlutanum „Úthlutun grunndagatals“.

Innihald **Biðtími Útreikningur** reitsins er afritað annað hvort úr birgðaspjaldinu eða birgðahaldseiningarspjaldinu, ef biðtími er skilgreindur fyrir vöruna, eða í glugganum **Vörulisti lánardrottins**, ef biðtíminn er skilgreindur fyrir lánardrottin.

## <a name="to-customize-a-calendar"></a>Dagatal sérsniðið:
Þegar grunndagatal er sérsniðið fyrir fyrirtækið eða einhvern viðskiptafélaga eru breytingar á frídögum og virkum dögum færðar inn.

Til dæmis sýnir grunndagatal yfirleitt alla laugardaga sem frídaga, en sérsniðið dagatal fyrir tiltekna stöð kann að sýna alla laugardaga í nóvember og desember fram að jólum sem virka daga.

Í eftirfarandi dæmi er stuðst við vinnustöð. Nú þegar er tiltækt uppsett grunndagatal fyrir þessa stöð.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Staðsetningar** og velja svo viðeigandi tengil.
2. Opna birgðageymsluna sem á að uppfæra og velja síðan **Sérsniðið Dagatal** reitinn. Athugið að dagatal verður að vera valið í **grunndagatalskóta** svæðinu.
3. Í glugganum **Sérsniðnar dagatalsfærslur**.opnast skal velja **Vinna með breytingar á sérsniðnum dagatölum** aðgerðina.
4. Bæta við línum fyrir sérsniðnar dagatalsfærslur í **Breytingar á sérsniðnar dagatalsfærslur**.

    Þegar lína er færð inn er gátreiturinn **Frídagar** valinn. Fjarlægja má gátmerkið ef gera á daginn aftur að virkum degi.

    Reiturinn **Ítrekunarkerfi** er notaður til þess að merkja tiltekna dagsetningu eða dag sem fastan frídag. Í boði eru tveir kostir, **Árleg ítrekun** eða **Vikuleg ítrekun**.

    Ef valin er **Árleg ítrekun** þarf einnig að færa inn viðkomandi dagsetningu í reitinn **Dagsetning**. Ef valin er **Vikuleg ítrekun** þarf einnig að færa inn viðkomandi vikudag í reitinn **Dagur**. Ef reiturinn er hafður auður verður að fylla út reitinn **Dagsetning**. Reiturinn **Dagur** er fylltur sjálfkrafa út. Þetta getur komið sér vel ef merkja á staka dagsetningu sem frídag eða virkan dag.

5. Velja hnappinn **Í lagi**.

Í glugganum **Sérsniðnar dagatalsfærslur** sjást dagsetningarfærslurnar sem eru uppfærðar samkvæmt breytingunum sem hafa verið gerðar.

Á spjaldinu Birgðageymsla sést að í reitnum **Sérsniðið dagatal** stendur orðið **Já** og sýnir að sérsniðið dagatal hefur verið sett upp.

> [!Important]
> Ef ekki er fyllt út í reitinn **Kóti birgðageymslu** í pöntunarlínu verður dagatal fyrirtækisins notað.


Ef ekki er fyllt út í reitinn **Kóti flutningsaðila** í pöntunarlínu er dagatal fyrirtækisins notað.

> [!NOTE]  
> Ef breytingar eru gerðar á grunndagatali sem sérsniðin dagatöl eru byggð á uppfærir kerfið líka öll sérsniðin dagatöl sjálfvirkt.

## <a name="to-assign-a-base-calendar"></a>Úthlutun grunndagatals  
Hér á eftir er tekið dæmi af áætlun afhendingardagsetninga á sölupöntunarlínum fyrir viðskiptamann.

Grunndagatöl eru tengd fyrirtæki notanda, viðskiptamönnum, lánardrottnum, birgðastöðvum og flutningsaðilum á eftirfarandi hátt:  

-   Á spjöldunum **Stofngögn** og **Viðskiptamaður** er grunndagatalið tengt við flýtiflipann **Afhending** .  
-   Á spjaldinu **Lánardrottinn** er grunndagatalið úthlutað á flýtiflipann **Móttaka**.  
-   Á spjaldinu **Birgðageymsla** er grunndagatalinu úthlutað á flýtiflipann **Vöruhús**.  
-   Í glugganum **Flutningsaðilar** er grunndagatalið tengt við gluggann **Flutningsþjónusta**.  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **viðskiptamenn** og velja svo viðeigandi tengil.  
2.  Opna spjaldið **Viðskiptamaður** sem fær úthlutað grunndagatali.  
3.  Á flýtiflipanum **Afhending**, í reitnum **Kóti grunndagatals**, er valið er það grunndagatal sem á að úthluta.  

> [!IMPORTANT]  
>  -   Ef fyrirtæki er ekki úthlutað grunndagatali reiknar kerfið alla daga út sem virka daga.  
> -   Ef engin birgðastöð er tilgreind á pöntunarlínu reiknar kerfið alla daga út sem virka daga.  
> -   Hvers kyns grunndagatal sem skilgreint er fyrir lánadrottininn eða birgðageymsluna hefur áhrif á það hvernig dagsetningarnar eru reiknaðar út og sléttaðar til virkra daga.

> [!NOTE]  
>  Ekki er hægt að búa til sérsniðnar dagatalsfærslur fyrr en fyrirtækinu hefur verið úthlutað grunndagatal.  

## <a name="see-also"></a>Sjá einnig
[Innkaup](purchasing-manage-purchasing.md)  
[Framleiðsla](production-manage-manufacturing.md)    
[Birgðir](inventory-manage-inventory.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

