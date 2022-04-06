---
title: Stofna Bankainnlán
description: Hægt er að gera innborganir til að viðhalda færslufærslu sem inniheldur upplýsingar sem hægt er að nota á útistandandi reikninga og kreditreikninga.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 10140, 10141, 10143, 10144, 10146, 10147, 10148, 36646
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: b7863252c436d04f95609911c1196af5697b5d70
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8524215"
---
# <a name="create-bank-deposits"></a>Stofna Bankainnlán
> [!NOTE]
> Möguleikinn til að stofna bankainnlán er nýr í Business Miðbær 2022 út Wave 1 fyrir mikið af Country útgáfum. Ef þú varst með Viðskiptaaðalstöðvar í Bandaríkjunum, Kanada eða Mexíkó áður en sú úttekt var notuð gætir þú verið að nota fyrri getu. Hægt er að halda áfram en nýr hæfileiki kemur í stað þeirra gömlu í framtíðarútgáfu. Til að byrja að nota þá nýju eiginleika sem lýst er í þessari grein getur Stjórnandinn farið **á síðuna Feature Management og kveikt á** aðgangsuppfærslu: stöðluð bankaafstemmingar og **Inngreiðslukerfi**.  

**Notaðu síðuna Bankainnlánin** til að skrá innborganir sem eitt skjal sem bókar eina eða fleiri færslur á bankareikning. Algengast er að bankainnstæður séu notaðar til að skrá staðgreiðsluinnlán. Síðan Bankainnlánin eru aðgengileg á **valmyndinni Sjóðstjórn** í hlutverkamiðstöð viðskiptastjóra og annarra hlutverkamiðstöðva sem fást við sjóðsstýringu.

Upphæðir á innlánsreikningum banka geta komið frá nokkrum aðilum:

* Sala, með fjárhagsreikningi vegna tekna.
* Viðskiptavinir greiðslur.
* Endurgreiðsla vegna endurgreiðslu frá lánardrottnum, eða peningagreiðslur til þeirra. 

Bankainnborgunarlínur innihalda upplýsingar um einstakar innborganir, s.s. ávísanir frá viðskiptavinum. Samtala upphæða í línunum verður að bæta við heildarupphæð innborganna.

Þegar búið er að fylla út Innborguð upplýsingar og línur þarf að bóka það. Bókun uppfærir viðeigandi fjárhag. Flokkarnir hafa að geyma fjárhaginn og fjárhag bankans, viðskiptamanna og lánardrottna. Bókaðar innborganir eru geymdar fyrir framtíðartilvísun á **síðunni bókaðar bankainnborganir**.

**Bankainnborgunarskýrslan** birtir innborganir viðskiptamanna og lánardrottna með upphaflegri innborgunarupphæð, upphæð innborgaðs sem helst opnast og upphæð sem er jöfnuð. Skýrslan sýnir einnig heildarupphæð bókaðs innborgunarupphæðar til afstemmingar.

## <a name="before-you-start"></a>Verður að byrja fyrir
Ýmislegt þarf að setja fram áður en hægt er að nota bankainnlán. Það verður að vera númeraröð og færslubókarsniðmát sem er tilbúið. Einnig ætti að tilgreina hvort bóka eigi upphæðir fyrir bankainnborgunum sem samtölu. Sem er, sem samtala allra upphæða í innborgunarlínunum. Annars er hver lína bókuð sem stök færsla. Ef innborgun er bókuð sem ein bankafærsla getur það auðveldað afstemmingu banka.

### <a name="number-series-and-lump-sum-deposits"></a>Númeraröð og Samtala innborgaðra
Setja verður upp númeraröð fyrir bankainnlán og tilgreina síðan raðirnar í **reitnum Bankainnborgunartími** á **uppsetningarsíðu** sölu&. Sjá [Create númeraröð](ui-create-number-series.md) fyrir frekari upplýsingar. 

Einnig á **uppsetningarsíðu** sölu& ef óskað er eftir að bóka innborganir sem klúður sums frekar en einstakar línur, snúa á **eftir Bankainnlánum sem klúður summu**. Ef innborgun er bókuð sem samtala innborgaðs, sem býr til eina bankainnslátt fyrir heildarupphæðina, getur verið auðveldara að stemma bankaafstemmingu.

### <a name="general-journal-templates-for-bank-deposits"></a>Sniðmát almennrar færslubókar fyrir bankainnstæður
Einnig þarf að stofna færslubókarsniðmát fyrir innborganir. Almennar færslubækur eru notaðar til að bóka færslur til banka, viðskiptamanna, lánardrottna, eigna og fjárhagslykla. Sniðmát færslubókar hanna almenna færslubók sem hentar starfi þínu. Þ.e. Reitirnir í bókarsniðmátinu eru nákvæmlega þeir sem þörf er á. 

Innborganir verða inngreiðslukvittanir og því er æskilegt að nota númeraröð fyrir inngreiðslufærslubækur. Ef þörf er á að greina á milli færslna í færslubók bankainnborgunar og staðgreiðslufærslur er notuð önnur númeraröð.

Einnig þarf að stofna runuvinnslu fyrir sniðmátið. Keyrslan er stofnuð á **síðunni sniðmát** almenns færslubókar með því að velja **aðgerðina Runa**. Frekari upplýsingar er að finna [í notkun færslubókarsniðmáta og runur](ui-work-general-journals.md#use-journal-templates-and-batches).

## <a name="dimensions-on-bank-deposit-lines"></a>Víddir í línum Bankainnborganna
Línurnar í bankainnborgunum nota sjálfkrafa sjálfgefnu víddirnar sem tilgreindar voru í **svæðunum Deildarkóti** og **kóti** viðskiptavinahóps. Þegar viðskiptamaður eða lánardrottinn er valinn **í reitnum Tegund** reiknings eru víddirnar sem eru tilgreindar fyrir viðskiptavininn eða lánardrottininn í **stað sjálfgilda.** **·** Hægt er að breyta víddunum í línunum ef þarf.

> [!TIP]
> Víddir í línum eru stilltar samkvæmt sjálfgefinni Víddarforgangsröðun. Línuvíddir forgangsröðuðu með haus vídda. Til að forðast árekstra er hægt að búa til reglur sem forgangsraða Hvenær á að nota vídd eftir uppruna. Ef óskað er að breyta því hvernig víddum er forgangsraðað er hægt að breyta flokkun þeirra á **síðunni Sjálfgefin vídd forgangs**. Sjá [til að setja upp sjálfgefinn víddarforgang](finance-dimensions.md#to-set-up-default-dimension-priorities) fyrir frekari upplýsingar.

## <a name="create-a-bank-deposit"></a>Stofna Bankainnborgun
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, Sláðu inn **Bankainnborganir** og veldu svo tengda tengilinn.
2. Velja **skal nýtt** til að opna **bankainnborgunarsíðuna**. 
3. Valið er Sniðmát færslubókar sem stofnað var fyrir bankainnlán.  

    > [!NOTE]
    > Ef færslubókarsniðmátið er með fleiri en eina runu birtist kvaðning um að velja eina.

4. **Í reitnum Bankareikningur nr.** er Bankareikningur valinn þar sem innborgunum er velt.

    > [!TIP]
    > Hægt er að tvísmella á réttan reikning með því **að nota reikningafærslur** og **reikningsfærslur** til að fletta upp færslum fyrir valda bankareikninginn. Til dæmis að sjá hvort svipaðar innborganir voru gerðar upp í reikninginn.

5. **Í reitinn heildarupphæð Innborgaðs upphæðar** er færð inn heildarupphæð innborgaðs fjárhæðarinnar. Þessi Samtala verður að vera samtala upphæðanna í öllum línum.
6. Fyllið inn í eftirstandandi reiti eftir þörfum. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

    Dagsetningin í **reitnum Bókunardags. og-víddir í** reitunum Deildarkóti **og** kóti **viðskiptavinahóps verða tengd línunum sem stofnaðar eru fyrir bankainnborgunina**. Hægt er að breyta þeim ef þörf krefur. 

7. Eftir því hvort bóka eigi bankainnborgunum sem klúður, eða hverja línu fyrir sig í fjárhag, er snúið við **eftir því sem samtala** er á eða slökkt á. Sjálfgefin stilling kemur frá sama skipta á **uppsetningarsíðu** sölu &.

    > [!NOTE]
    > **Reiturinn Gjaldmiðilskóti** sýnir gjaldmiðilinn sem tilgreindur er fyrir bankareikninginn sem valinn var. Ekki er hægt að velja annan gjaldmiðil.

8. **Stofnið nýja línu fyrir hverja peningagreiðslu sem á að innborgun á línunarfastanum**.
9. **Tilgreinið í reitnum Tegund** reiknings hvaðan greiðslan er upprunnin. Fyrir bankainnlán er tegundin vanalega **Viðskiptamaður** eða **Lánardrottinn**. 

    > [!NOTE]
    > Einnig er hægt að skrá staðgreiðslu til lánardrottins. Til að gera það er valið **Lánardrottinn** og síðan er Greiðsluupphæðin færð inn sem neikvætt númer í **reitinn kreditupphæð** í línunni. 

10. **Í reitinn Númer fylgiskjals** er fært fylgiskjalsnúmer reikningsins sem kreditupphæðin varð fyrir. Hægt er að nota fylgiskjalsnúmer fyrir hverja línu eða sama númer fyrir allar línur.

    > [!TIP]
    > Yfirleitt þarf ekki að fylla út **reitinn Tegund** fylgiskjals fyrir fjárhagslegar færslur. Ef þú ert til dæmis að fá reiðufé úr sölu á dag er reiturinn hafður auður. Ef þú ert að flytja inn reiðufé úr greiðslu viðskiptavinar, velur **þú greiðslu**.

11. Ef verið er að jafna staðgreiðslu fyrir ákveðinn reikning viðskiptavinar skal velja **aðgerðina nota færslur** og færa síðan reikningsnúmerið í **reitinn jöfnun jöfnunar**. 
12. Ef þú ert tilbúinn að bóka bankainnborgunar skaltu velja **aðgerðina Post**.

    > [!TIP]
    > Áður en innborgun er bókuð er hægt að nota **Prófunarskýrsluaðgerð** til að fara yfir gögnin. Skýrslan sýnir hvort einhver atriði, eins og vantar gögn, muni koma í veg fyrir bókun.  

## <a name="finding-posted-bank-deposits"></a>Finna bókaðar innborganir banka
Á **síðunni bókaðar bankainnstæður** skráir þú inn fyrri innborganir fyrirtækisins. Í listanum er hægt að fara yfir þær athugasemdir og víddir sem tilgreindar voru fyrir innborganir. Hægt er að opna bankarinnið til að skoða nánar og þaðan er hægt að rannsaka frekar. Til dæmis er hægt að velja aðgerðina finna færslur til að skoða bókaðar bankareikningsfærslur. Í bankafærslunni er að finna samsvarandi bókaða fjárhagsfærslu.

Ef fletta á upp öllum fjárhagsfærslum fyrir bókuðu innborgunarlínurnar er farið á **síðuna Fjárhagsskrá** og aðgerðin Fjárhagur **notuð**. Þar finnur þú allar fjárhagsfærslur, þar á meðal færslur fyrir viðskiptamenn og lánardrottna.

## <a name="reversing-a-posted-bank-deposit"></a>Bakfæra bókaða Bankainnborgun
Til að bakfæra bókaða innborgun er farið á **síðuna Fjárhagsdagbækur**, fundið afgreiðslukassa innborgaðs og síðan valið **aðgerðina bakfæra**.

> [!NOTE]
> Aðeins er hægt að bakfæra dagbók sem inniheldur eina tegund færslu. Það er, afgreiðslubókin verður að innihalda aðeins viðskiptamannafærslur eða lánardrottnafærslur, en ekki báðar. Ef bæði dagbók inniheldur bæði verður að bakfæra innborgunarverðið handvirkt.      

## <a name="see-also"></a>Sjá einnig
[Fjármál](finance.md)  
[Uppsetning á fjármálum](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]



