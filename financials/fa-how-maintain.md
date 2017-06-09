---
title: "Hvernig á að: viðhalda eignum |  Microsoft Docs"
description: "Lýsir því hvernig á að viðhalda eign."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 03/23/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 2e23ba3079dfa87f6a33fa7c0a6eb67826f3c271
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-maintain-fixed-assets"></a>Hvernig á að: Viðhalda Eignir
Viðhaldskostnaður er reglubundinn kostnaður sem varið er til þess að viðhalda virði eigna. Ólíkt viðbótarfjárfestingum eykur hann ekki verðgildi.

Hægt er að skrá og viðhalda dagréttri skrá um viðhald og þjónustu við eignir og hafa þannig fullkomnar viðhaldsskrár um eignir aðgengilegar. Í hvert sinn sem eign fær þjónustu skráir notandi allar viðeigandi upplýsingar eins og dagsetningu, númer lánardrottins og símanúmer þjónustuaðila. Skráning viðhalds er færð vegna allra eigna á viðeigandi eignaspjaldi.

Endurmat er notað til að laga virði að almennum verðbreytingum. Hægt er að nota keyrsluna **Endurmat eigna** til að endurreikna viðhaldskostnað.

## <a name="to-record-maintenance-work-on-a-fixed-asset"></a>Skrá viðhaldsvinna á eign
Í hvert sinn sem viðhaldi hefur verið framkvæmt, eins og þjónustuheimsókn, er hægt að skrá það á viðeigandi eign í glugganum **Skráning viðhalds**.  

1. Efst í hægra horninu skal velja **Leit að síðu eða skýrslu** táknið ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið"), slá inn **Eignir** og velja svo tengdan tengil.  
2. Valin er eignin sem á að skrá viðhald fyrir og veldu síðan aðgerðina **skráning viðhalds**.
3. Í glugganum **skráning viðhalds** þarf að fylla reitina út eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-post-maintenance-costs-from-a-fixed-asset-gl-journal"></a>Bóka viðhaldskostnað úr fjárhagsbók eigna
1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Listi afskriftarbóka**, og velja síðan viðeigandi tengil.  
2. Veljið afskriftabókina sem er tengd eigninni og veljið síðan aðgerðina **breyta**.
3. Í glugganum **Afskriftabókarspjald** skal ganga úr skugga um að gátreiturinn **Viðhald** er ekki valinn. Þetta tryggir að viðhaldskostnaðar eru ekki bókaðar í fjárhag.
4. Efst í hægra horninu skal velja **Leit að síðu eða skýrslu** táknið ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið"), slá inn **Eignafjárhagsbækur** og velja svo tengdan tengil.  
5. Stofnaður er upprunaleg Færslubókarlína og reitirnir fylltir út eftir þörfum.
6. Í reitnum **Eignabókunartegund** er valinn **viðhald**.
7. Valið er **Setja inn mótreikn. eigna** aðgerð. Seinni færslubókarlína er búin til fyrir mótreiknings sem er sett upp fyrir bókun viðhalds.

    **Athugasemd:** Skref 7 virkar eingöngu ef búið er að setja upp eftirfarandi: Í **Eignabókunarflokksspjald** glugganum fyrir bókunarflokkur eigna, inniheldur reiturinn **Viðhaldsreikningur** debetreikning fjárhags og reiturinn **Mótreikningur viðhalds** inniheldur fjárhagsreikninginn sem á að bóka mótfærslur í fyrir endurmat. Nánari upplýsingar eru í "setja upp bókunarflokka eigna" hlutanum í [Hvernig: Setja Upp almennar upplýsingar um eignir](fa-how-setup-general.md).
8. Valið er **bóka ** aðgerð.

## <a name="to-follow-up-on-fixed-assets-service-visits"></a>Til að fylgja eftir þjónustuheimsóknum eigna:
Þú getur Prenta skýrsluna **Viðhald - Næsta þjónusta** til að skoða fyrir hvaða eignir er búið að áætla þjónustuheimsóknir. Einnig er hægt að nota þessa skýrslu þegar reiturinn **Næsta þjónustudags.** á eignspjöldunum er uppfærður.  

1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Viðhald næsta þjónusta**, og velja síðan viðeigandi tengil.  
2. Reitirnir **Upphafsdagsetning** og **Lokadagsetning** eru fylltir út.  
3. Veljið hnappinn **Prenta** eða **Forskoðun**.

## <a name="to-monitor-maintenance-costs"></a>Fylgst með viðhaldskostnaði
Hægt er að skoða viðhaldskostnaðinn þegar skoðaðar eru upplýsingar um eign.  

1. Efst í hægra horninu skal velja **Leit að síðu eða skýrslu** táknið ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið"), slá inn **Eignir** og velja svo tengdan tengil.
2. Valin er eignin sem á að skoða viðhaldskostnað fyrir og veldu síðan aðgerðina **afskriftabækur**.
3. Í reitnum **Eignaafskriftabækur** er valin viðeigandi eignaafskriftabók og síðan valið **upplýsingar** aðgerð.
4. Í glugganum **Eignaupplýsingar** er valið **viðhald** .

Glugginn **viðhaldsbókarfærslur** opnast og sýnir færslur sem mynda upphæðina í reitnum **viðhald**.

## <a name="to-view-or-print-maintenance-costs-for-multiple-fixed-assets"></a>Skoða eða prenta viðhaldskostnað fyrir margar eignir
Í skýrslunni **Viðhald - Greining** er hægt er að velja að sjá viðhalds byggt á einn, tvo eða þrjá viðhaldskóta á tilgreindri dagsetningu eða tímabili. Einnig er hægt að sjá samtölu allra valinna eigna eða samtölu hverrar eignar fyrir sig.

1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Greining viðhalds**, og velja síðan viðeigandi tengil.
2. Fyllið inn í svæðin eftir þörfum.
3. Veljið hnappinn **Prenta** eða **Forskoðun**.

## <a name="to-view-maintenance-ledger-entries"></a>Skoðun viðhaldsfærslna:
Hægt er einnig að sjá viðhaldskostnaðinn með því að skoða viðhaldsbókarfærslurnar.  

1. Efst í hægra horninu skal velja **Leit að síðu eða skýrslu** táknið ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið"), slá inn **Eignir** og velja svo tengdan tengil.
2. Valin er eignin sem á að skoða fjárhagsfærslur fyrir og veldu síðan aðgerðina **afskriftabækur**.
3. Í reitnum **Eignaafskriftabækur** er valin viðeigandi eignaafskriftabók og síðan valið **viðhaldsbókarfærslur** aðgerð.

## <a name="to-view-or-print-maintenance-ledger-entries-for-multiple-fixed-assets"></a>Skoða eða prenta viðhaldsbókarfærslur fyrir margar eignir
Í **Viðhald - Sundurliðun** skýrslu er hægt að skoða eða prenta viðhaldsbókarfærslur fyrir eina eða margar eignir.  

1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Upplýsingar um viðhald**, og velja síðan viðeigandi tengil.
2. Fyllið inn í svæðin eftir þörfum.
3. Veljið hnappinn **Prenta** eða **Forskoðun**.

## <a name="see-also"></a>Sjá einnig
[Eignir](fa-manage.md)  
[Uppsetning eigna](fa-setup.md)  
[Fjármál](finance.md)  
[Velkomin í [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]] (index.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

