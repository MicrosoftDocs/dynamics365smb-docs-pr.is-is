---
title: Viðhald eigna| Microsoft Docs
description: Haldið skrá yfir viðhald, það er allar viðgerðir á og þjónustu við eignina.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: b7116d54844aeeaf1289efb4401ab5556d3f03ec
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2019
ms.locfileid: "931026"
---
# <a name="maintain-fixed-assets"></a>Umsjón eigna
Viðhaldskostnaður er reglubundinn kostnaður sem varið er til þess að viðhalda virði eigna. Ólíkt viðbótarfjárfestingum eykur hann ekki verðgildi.

Hægt er að skrá og viðhalda dagréttri skrá um viðhald og þjónustu við eignir og hafa þannig fullkomnar viðhaldsskrár um eignir aðgengilegar. Í hvert sinn sem eign fær þjónustu skráir notandi allar viðeigandi upplýsingar eins og dagsetningu, númer lánardrottins og símanúmer þjónustuaðila. Skráning viðhalds er færð vegna allra eigna á viðeigandi eignaspjaldi.

Endurmat er notað til að laga virði að almennum verðbreytingum. Hægt er að nota keyrsluna **Endurmat eigna** til að endurreikna viðhaldskostnað.

## <a name="to-record-maintenance-work-on-a-fixed-asset"></a>Skrá viðhaldsvinna á eign
Í hvert sinn sem viðhaldi hefur verið framkvæmt, eins og þjónustuheimsókn, er hægt að skrá það á viðeigandi eign á síðunni **Skráning viðhalds**.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eignir** og veldu síðan tengda tengilinn.  
2. Valin er eignin sem á að skrá viðhald fyrir og veldu síðan aðgerðina **skráning viðhalds**.
3. Fyllt er út í reiti eftir því sem á við á síðunni **Skráning viðhalds**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-post-maintenance-costs-from-a-fixed-asset-gl-journal"></a>Bóka viðhaldskostnað úr fjárhagsbók eigna
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Afskriftabókarlisti** og veldu síðan tengda tengilinn.  
2. Veljið afskriftabókina sem er tengd eigninni og veljið síðan aðgerðina **breyta**.
3. Á síðunni **Afskriftabókarspjald** skal ganga úr skugga um að gátreiturinn **Viðhald** er ekki valinn. Þetta tryggir að viðhaldskostnaðar eru ekki bókaðar í fjárhag.
4. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eignafjárhagsbækur** og veldu síðan tengda tengilinn.  
5. Stofnaður er upprunaleg Færslubókarlína og reitirnir fylltir út eftir þörfum.
6. Í reitnum **Eignabókunartegund** er valinn **viðhald**.
7. Valið er **Setja inn mótreikn. eigna** aðgerð. Seinni færslubókarlína er búin til fyrir mótreiknings sem er sett upp fyrir bókun viðhalds.

    > [!NOTE]  
    >   Skref 7 virkar eingöngu ef búið er að setja upp eftirfarandi: Í **Eignabókunarflokksspjald** síðunni fyrir bókunarflokkur eigna, inniheldur reiturinn **Viðhaldsreikningur** debetreikning fjárhags og reiturinn **Mótreikningur viðhalds** inniheldur fjárhagsreikninginn sem á að bóka mótfærslur í fyrir uppfærslu. Frekari upplýsingar er að finna í [Að setja upp bókunarflokka eigna](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
8. Valið er **Bóka** aðgerðin.

## <a name="to-follow-up-on-fixed-assets-service-visits"></a>Til að fylgja eftir þjónustuheimsóknum eigna:
Þú getur Prenta skýrsluna **Viðhald - Næsta þjónusta** til að skoða fyrir hvaða eignir er búið að áætla þjónustuheimsóknir. Einnig er hægt að nota þessa skýrslu þegar reiturinn **Næsta þjónustudags.** á eignspjöldunum er uppfærður.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Næsta viðhaldsþjónusta** og veldu síðan tengda tengilinn.  
2. Reitirnir **Upphafsdagsetning** og **Lokadagsetning** eru fylltir út.  
3. Veljið hnappinn **Prenta** eða **Forskoðun**.

## <a name="to-monitor-maintenance-costs"></a>Fylgst með viðhaldskostnaði
Hægt er að skoða viðhaldskostnaðinn þegar skoðaðar eru upplýsingar um eign.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eignir** og veldu síðan tengda tengilinn.
2. Valin er eignin sem á að skoða viðhaldskostnað fyrir og veldu síðan aðgerðina **afskriftabækur**.
3. Á síðunni **Eignaafskriftabækur** er valin viðeigandi eignaafskriftabók og síðan er aðgerðin **Upplýsingar** valin.
4. Á síðunni **Eignaupplýsingar** er valið **viðhald** .

Síðan **viðhaldsbókarfærslur** opnast og sýnir færslur sem mynda upphæðina í reitnum **viðhald**.

## <a name="to-view-or-print-maintenance-costs-for-multiple-fixed-assets"></a>Skoða eða prenta viðhaldskostnað fyrir margar eignir
Í skýrslunni **Viðhald - Greining** er hægt er að velja að sjá viðhalds byggt á einn, tvo eða þrjá viðhaldskóta á tilgreindri dagsetningu eða tímabili. Einnig er hægt að sjá samtölu allra valinna eigna eða samtölu hverrar eignar fyrir sig.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðhaldsgreining** og veldu síðan tengda tengilinn.
2. Fyllið inn í svæðin eftir þörfum.
3. Veljið hnappinn **Prenta** eða **Forskoðun**.

## <a name="to-view-maintenance-ledger-entries"></a>Skoðun viðhaldsfærslna:
Hægt er einnig að sjá viðhaldskostnaðinn með því að skoða viðhaldsbókarfærslurnar.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eignir** og veldu síðan tengda tengilinn.
2. Valin er eignin sem á að skoða fjárhagsfærslur fyrir og veldu síðan aðgerðina **afskriftabækur**.
3. Á síðunni **Eignaafskriftabækur** er valin viðeigandi eignaafskriftabók og síðan er aðgerðin **Viðhaldsbókarfærslur** valin.

## <a name="to-view-or-print-maintenance-ledger-entries-for-multiple-fixed-assets"></a>Skoða eða prenta viðhaldsbókarfærslur fyrir margar eignir
Í **Viðhald - Sundurliðun** skýrslu er hægt að skoða eða prenta viðhaldsbókarfærslur fyrir eina eða margar eignir.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðhaldsupplýsingar** og veldu síðan tengda tengilinn.
2. Fyllið inn í svæðin eftir þörfum.
3. Veljið hnappinn **Prenta** eða **Forskoðun**.

## <a name="see-also"></a>Sjá einnig
[Eignir](fa-manage.md)  
[Uppsetning eigna](fa-setup.md)  
[Fjármál](finance.md)  
[Hafist handa](product-get-started.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
