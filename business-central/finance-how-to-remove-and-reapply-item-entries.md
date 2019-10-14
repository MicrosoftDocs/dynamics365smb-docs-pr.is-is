---
title: Hvernig á að fjarlægja og endurjafna birgðafærslur | Microsoft Docs
description: Hægt er að skoða og breyta handvirkt tilteknum birgðajöfnunarfærslum sem eru stofnaðar sjálfkrafa við birgðafærslur.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 3d9d602690b8d4ca7714b328759a705204c740ee
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2019
ms.locfileid: "2306053"
---
# <a name="remove-and-reapply-item-ledger-entries"></a>Fjarlægja og endurjafna birgðabókafærslur
Á síðunni **Vinnublað jöfnunar** er hægt að skoða og breyta handvirkt tilteknum birgðajöfnunarfærslum sem eru stofnaðar sjálfkrafa við birgðafærslur.  

Þegar bókuð eru viðskipti þar sem vörur eru færðar í eða úr birgðum er birgðajöfnun búin til milli hverrar birgðaaukningar og birgðaminnkunar. Þessar jafnanir ákvarða kostnaðarflæði úr þeim vörum sem er tekið á móti í birgðir á móti kostnaði þeirra vara sem fara út úr birgðum. Vegna þess hvernig kostnaðarverð er reiknað út gæti skökk birgðajöfnun leitt til skekkts meðalinnkaupaverðs og skekkts kostnaðarverðs. Nánari upplýsingar eru í Upplýsingar um hönnun: Vörujöfnun.

Eftirfarandi dæmi gætu krafist þess að birgðafærslur séu ógildar eða endurjafnaðar:

- Gleymst hefur að gera fasta jöfnun.
- Röng föst jöfnun var gerð.
- Skila þarf vöru sem búið er að jafna sölu við.

Nota skal skjal til að endurjafna birgðahöfuðbókarfærslu, ef það er hægt. Ef gera þarf til dæmis vöruskil á vöru sem þegar er búið að jafna sölu við er hægt að gera endurjöfnunina með því að stofna og bóka vöruskilaskjalið með réttri jöfnun í reitinn **Jafna birgðafærslu** á innkaupaskilalínunni. Hægt er að nota aðgerðina **Sækja bókaðar fylgiskjalalínur til að bakfæra** eða aðgerðina **Afrita skjal** í innkaupaskilaskjalinu til að gera þetta auðveldara. Þegar fylgiskjalið er birgðahöfuðbókafærslan endurjöfnuð sjálfkrafa. Nánari upplýsingar er að finna í [Vinna úr innkaupaskilum eða afturköllunum](purchasing-how-process-purchase-returns-cancellations.md).

Ef ekki er hægt að nota skjal til að endurjafna, s.s. þegar leiðrétta á fasta jöfnun, skal nota síðuna **Vinnublað jöfnunar** til að leiðrétta jöfnun.

> [!Warning]  
> Eftirfarandi er mikilvægt að hafa í huga þegar unnið er með jöfnunarvinnublaðið:
    - Ekki ætti að skilja jöfnunarfærslur eftir ójafnaðar í lengri tíma þar sem aðrir notendur geta ekki unnið úr vörum fyrr en jöfnunarfærslurnar eru endurjafnaðar eða síðunni **Vinnublað jöfnunar** er lokað. Notendur sem reyna til að framkvæma aðgerðir sem fela í sér jöfnunarfærslu sem afjöfnuð er handvirkt fá eftirfarandi villuboð: ”Ekki er hægt að framkvæma þessa aðgerð þar sem færslur fyrir vöru XXX eru afjafnaðar í Jöfnunarvinnublaðinu af notanda XXX."
    - Aðeins ætti að endurjafna birgðafærslur utan vinnu til að forðast hvers konar árekstra við aðra notendur sem eru að bóka færslur með sömu vörum.
    - Þegar jöfnunarvinnublaðinu er lokað framkvæmir [!INCLUDE[d365fin](includes/d365fin_md.md)] athugun til að tryggja það að allar færslur séu jafnaðar. Ef jöfnun magns er t.d. fjarlægð og ný jöfnun ekki stofnuð, áður en jöfnunarvinnublaðinu er lokað, verður ný jöfnun stofnuð. Þannig helst kostnaðurinn óbreyttur. Hins vegar verður að hafa í huga að ef föst jöfnun er fjarlægð er önnur jöfnun ekki stofnuð sjálfkrafa þegar vinnublaðinu er lokað. Það þarf að gera handvirkt með því að stofna nýja jöfnun í vinnublaðinu.
    - Hægt er að fjarlægja jöfnun úr fleiri en einni færslu í einu á jöfnunarvinnublaðinu. Hins vegar er ekki mögulegt að stofna jöfnun fyrir fleiri en eina færslu í einu af því að jöfnun færslna hefur áhrif á þær færslur sem eru fyrir hendi til jöfnunar.
    - Jöfnunarvinnublaðið getur ekki gert jöfnun við eftirfarandi aðstæður: Ef ekki er nógu mikið magn í birgðum til að jafna, jöfnunarvinnublaðið getur ekki gert jöfnun á meðan verið er að reyna að jafna birgðaminnkunarfærslu án vörurakningarupplýsinga við birgðaaukningarfærslu með vörurakningarupplýsingar.

## <a name="to-remove-an-item-application-by-using-the-application-worksheet"></a>Að fjarlægja birgðajöfnunarfærslu með jöfnunarvinnublaðinu  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vinnublað jöfnunar** og veldu síðan tengda tengilinn.  
2.  Síðan **Vinnublaðsjöfnun** opnast og sýnir núverandi vörufærslur í færslubók fyrir allar vörur.  
3.  Færa inn afmarkanir á flýtiflipanum **Almennt** til að að einfalda leit að birgðafærslu sem gera á jöfnunarbreytingu á.  
4.  Valin er birgðabókarfærsla og svo **Jafnaðar færslur** aðgerðina. Síðan **Skoða jafnaðar færslur – Jafnaðar færslur** opnast og birtir birgðafærsluna eða birgðafærslurnar sem eru jafnaðar við völdu færsluna.  
5.  Valin er sú birgðafærsla sem á að fjarlægja jöfnun af.  
6.  Valið er **fjarlægja jöfnun** aðgerð. Þetta fjarlægir birgðajöfnunarfærsluna sem tengir birgðafærslurnar og færir hana á síðunni **Skoða jafnaðar færslur - ójafnaðar færslur**.  
7.  Loka síðunni **Skoða jafnaðar færslur - Jafnaðar færslur**.  

 Reiturinn **Eftirstöðvar (magn)** í birgðafærslunum tveimur hækka sem samsvarar því magni sem afjafnað var. Fjarlægða birgðafærslan er nú tiltæk til endurjöfnunar á síðunni **Skoða jafnaðar færslur – ójafnaðar færslur**.  

> [!IMPORTANT]  
>  Ekki ætti að skilja jöfnunarfærslur eftir ójafnaðar í lengri tíma þar sem aðrir notendur geta ekki unnið úr vörum fyrr en jöfnunarfærslurnar eru endurjafnaðar eða síðunni **Vinnublaðsjöfnun** er lokað. Eftirfarandi villuboð birtast ef reynt er að framkvæma aðgerðir sem fela í sér jöfnunarfærslu sem er gerð óvirk handvirkt.  
>   
>  **Ekki er hægt að framkvæma þessa aðgerð því færslur fyrir vöruna <item> vara hafa verið gerðar ógildar í Vinnublað jöfnunar af notandanum <user>.**  

## <a name="to-reapply-an-item-application-by-using-the-application-worksheet"></a>Að endurjafna birgðajöfnunarfærslu með jöfnunarvinnublaðinu  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vinnublað jöfnunar** og veldu síðan tengda tengilinn.  
2.  Síðan **Vinnublaðsjöfnun** opnast og sýnir núverandi vörufærslur í færslubók fyrir allar vörur.  
3.  Til að endurjafna færslunum sem voru fjarlægðar síðan vinnublaðið var opnað skal velja birgðabókarfærsluna sem á að endurjafna. Á flipanum **Aðgerðir** í flokknum **Eiginleikar** veljið **Endurjafna**.  

    > [!NOTE]  
    >  Þessi endurjöfnun á upphaflegu stöðunni verður einnig sjálfkrafa þegar síðunni **Vinnublaðsjöfnun** er lokað.  
4.  Til að jafna tiltækri opinni birgðabókarfærslu við aðra færslu skal velja birgðabókarfærsluna sem jafna á við. Valið er **Ójafnaðar Færslur** aðgerð. Síðan **Skoða jafnaðar færslur-ójafnaðar færslur** opnast.  
5.  Velja skal eina eða fleiri birgðafærslur sem jafna á við færsluna sem valin var á síðunni **Vinnublaðsjöfnun** og smella síðan á **Í lagi**.  

     Forritið stofnar birgðajöfnunarfærslu á milli birgðafærslnanna tveggja. Dregið er úr reitunum **Eftirstöðvar (magn)** í færslunum tveimur sem samsvarar jafnaða magninu.  

    > [!NOTE]  
    >  Ef valið var að jafna þar sem það stofnar óendanlega lykkju í kostnaðarleiðréttingarferlinu verður sú jöfnun ekki framkvæmd. Þetta getur gerst þegar upprunalegu færslurnar stofnuðu neikvæða birgðastöðu. Forritið er ekki gert. Því verður að velja aðra færslu fyrir jöfnunina.  
6.  Ef reiturinn **Sjálfvirk kostnaðarleiðrétting** í **Uppsetning birgða** er stilltur á **Alltaf** þá er kostnaðarleiðréttingarkeyrsla keyrð sjálfvirkt eftir að endurjöfnun er gerð. Annars er keyrslan **Kostnaðarleiðrétting - Birgðafærslur** keyrð til að tryggja það að allur kostnaður sé uppfærður.  

## <a name="see-also"></a>Sjá einnig  
[Loka opnum færslum birgðahöfuðbókar vegna fastrar jöfnunar í birgðabók](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)  
 [Meðhöndlun innkaupaskila eða afturkallana](purchasing-how-process-purchase-returns-cancellations.md)  
 [Birgðakostnaði stjórnað](finance-manage-inventory-costs.md)   
 [Hönnunarupplýsingar: Umsókn vöru](design-details-item-application.md)  
 [Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
