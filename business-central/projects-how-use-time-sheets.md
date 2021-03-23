---
title: Vinna með vinnuskýrslur fyrir verk| Microsoft Docs
description: Lýsir því hvernig skal stofna vinnuskýrslu fyrir verk, afrita áætlunarlínur yfir í hana, skilgreina vinnutegund, fylla inn í skýrsluna og senda hana inn til samþykkis.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 42357da17222bf6500667bfdf160124e245d6bb0
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388349"
---
# <a name="use-time-sheets-for-jobs"></a>Nota vinnuskýrslur fyrir verk

Nota skal keyrsluna **Stofna vinnuskýrslur** til að setja upp vinnuskýrslur fyrir tilgreindan fjölda tímabila eða vikna. Notandi verður að hafa heimildir til að hægt sé að búa til vinnuskýrslur.

Hægt er að afrita og nota verkáætlunarlínur í vinnuskýrslu. Með því móti þarf aðeins að færa upplýsingarnar inn á einum stað og línuupplýsingarnar eru alltaf réttar.

Eftir að búið er að samþykkja vinnuskýrslufærslur fyrir verk er hægt að bóka þær á viðeigandi verkbók eða forðabók.

Áður en hægt er að nota vinnuskýrslur þarf að setja upp almennar upplýsingar og tilgreina stjórnanda og einn eða fleiri samþykkjendur vinnuskýrslna. Frekari upplýsingar eru í [Setja upp vinnuskýrslur](projects-how-setup-time-sheets.md).

## <a name="to-create-a-time-sheet"></a>Til að búa til vinnuskýrslu

Hægt er að nota keyrsluna **Stofna vinnuskýrslur** til að setja upp vinnuskýrslur fyrir tilgreindan fjölda tímabila eða vikna. Eigandi vinnuskýrslunnar getur þá opnað hana og skráð tíma sem eytt hefur verið í verk.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vinnuskýrslur** og veldu síðan tengda tengilinn.
2. Á síðunni **Vinnuskýrslulisti** skal velja aðgerðina **Stofna vinnuskýrslur**.
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Reitirnir **Nota vinnuskýrslu** og **Notandakenni eiganda vinnuskýrslu** verða að vera fylltir út á spjaldinu fyrir forða vinnuskýrslunnar.
4. Velja hnappinn **Í lagi**.  

Á síðunni **Vinnuskýrslulisti** er hægt að sjá allar vinnuskýrslur sem hafa verið stofnaðar.

## <a name="to-copy-job-planning-lines-to-a-time-sheet"></a>Til að afrita áætlunarlínur verks á vinnuskýrslu
Eftirfarandi ferli lýsir því hvernig eigi að flýtistofna verkáætlunarlínur á vinnuskýrslu.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vinnuskýrslur** og veldu síðan tengda tengilinn.  
2. Á síðunni **Vinnuskýrslulisti** skal velja vinnuskýrslu fyrir viðeigandi tímabil og svo **Breyta vinnuskýrslu** aðgerðina.  
3. Veljið aðgerðina **Stofna línur úr verkáætlun**. Allar verkáætlunarlínur í tímabili vinnublaðsins eru afritaðar í vinnublaðið fyrir manneskjuna eða vélina í **Tilfang nr.** reitinn á vinnublaðsins.

## <a name="to-define-work-types-and-add-one-to-a-time-sheet"></a>Til að skilgreina tegundir vinnu og bæta tegund vinnu við vinnuskýrslu
Hægt er að skilgreina tegund vinnu fyrir allar vinnuskýrslulínur fyrir verk. Með þeim hætti er hægt að bæta við upplýsingum sem þarf til að rukka viðskiptavininn og fyrir mismunandi tegundir af vinnu.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vinnuskýrslur** og veldu síðan tengda tengilinn.   
2. Opnið viðeigandi vinnuskýrslu.
3. Veljið reitinn **Lýsing**.  
4. Á síðunni **Upplýsingar um verk á vinnuskýrslulínu** skal velja reitinn **Vinnutegundarkóði** og velja vinnutegund af listanum, t.d. **Mílur**.  
5. Ef engin tegund vinnu er til skal velja aðgerðina **Nýtt**.
6. Fyllt er út í reiti eftir því sem á við á síðunni **Vinnutegundir**.
7. Endurtakið skref 4 til að úthluta nýju verktegundinni á vinnuskýrsluna.

## <a name="to-reuse-time-sheet-lines-in-other-time-sheets"></a>Til að endurnýta vinnuskýrslulínur í öðrum vinnuskýrslum
Ef upplýsingar tímablaðs haldast óbreyttar á milli tímabila má spara tíma með því að afrita línur úr fyrra tímabili. Síðan er tímanotkunin fyrir nýja tímabilið færð inn.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vinnuskýrslur** og veldu síðan tengda tengilinn.  
2. Opnið vinnuskýrsluna fyrir tímabil sem er síðar en tímabilið fyrir fyrirliggjandi vinnuskýrslu með línum.  
3. Veljið aðgerðina **Afrita línur úr fyrri vinnuskýrslu**.

Línurnar eru afritaðar, með upplýsingum eins og gerð og lýsingu. Til dæmis, ef línurnar eru tengdar við starf, er **Verk nr.** afritað. Allar afritað línur eru með stöðuna **Opna**. Þá er hægt að breyta línunum eftir þörfum.

## <a name="to-fill-in-a-time-sheet-lines-and-submit-for-approval"></a>Til að fylla út vinnuskýrslulínur og senda til samþykktar
Vinnuskýrsluskráning er rakin í klukkustundum, sem er stöðluð grunnmælieining fyrir forða. Sjálfgefið er að vinnuskýrsla sýni sameiginlega vinnudaga frá mánudegi til föstudags.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vinnuskýrslur** og veldu síðan tengda tengilinn.  
2. Veljið vinnuskýrslu fyrir viðeigandi tímabil og veljið svo aðgerðina **Breyta tímaskýrslu**.  
3. Fyllið í reitina í línu eins og þörf krefur. Færið inn fjölda stunda sem forðinn notar hvern dag vikunnar.

    > [!TIP]  
    >   Hægt er að fara yfir samtölu tímaskýrslustunda sem settar hafa verið inn í upplýsingakassann **Rauntími/áætlaður tími samantekt**  
4. Endurtakið skref 3 fyrir aðrar tegundir vinnu sem forðinn innir af hendi.
5. Veldu aðgerðina **Senda inn** og síðan aðgerðina **Allar opnar línur** til að senda inn allar línur eða aðgerðina **Aðeins valdar línur** til að senda inn aðeins línurnar sem eru valdar á síðunni **Vinnuskýrsla**.  

    > [!NOTE]  
    >   Aðeins er hægt að senda tímaskýrslulínur sem innihalda skráðan tíma.  
6. Til að breyta upplýsingum í línu sem hefur verið stillt á **Sent** skal velja línu og velja svo aðgerðina **Enduropna**.

    > [!NOTE]  
    >   Stundum gæti stjórnandi hafnað tímaskýrslulínu sem lögð er fram til samþykktar. Ef lína hefur stöðuna **Hafnað** er hægt að gera breytingar í línunni og velja **Senda** aftur.  
7. Velja hnappinn **Í lagi**.

## <a name="to-approve-or-reject-a-time-sheet"></a>Til að samþykkja eða hafna vinnuskýrslu
Senda þarf vinnuskýrslu til samþykkis áður en hægt er að nota hana. Hægt er að samþykkja og hafna einstaka línum í vinnuskýrslu eða senda þær aftur til sendanda fyrir frekari aðgerðir. Hægt er að samþykkja vinnuskýrslu með tvenns konar hætti:

* Vinnuskýrslustjóri getur samþykkt allar vinnuskýrslur.
* Einstaklingurinn sem er tilgreindur í reitnum **Notandakenni samþykkjanda vinnuskýrslu** á forðaspjaldi getur samþykkt vinnuskýrslur viðkomandi forða. Frekari upplýsingar eru í [Setja upp vinnuskýrslur](projects-how-setup-time-sheets.md).

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vinnuskýrslur verkstjóra** eða vinnuskýrslur og veldu síðan tengda tengilinn.
2. Veljið vinnuskýrslu úr listanum.  
3. Á síðunni **Vinnuskýrsla** skal velja aðgerðina **Samþykkja** og síðan aðgerðina **Allar sendar línur** til að samþykkja allar línur eða aðgerðina **Aðeins valdar línur** til að samþykkja aðeins línurnar sem eru valdar á síðunni **Vinnuskýrsla**.
4. Velja hnappinn **Í lagi**.  
5. Einnig er hægt að velja aðgerðina **Hafna** og fylgja skrefum 4 til 5.  

> [!TIP]  
>   Nota skal upplýsingakassana **Staða vinnuskýrslu** og **Samantekt fyrir rauntíma/áætlaðan tíma** til að fá yfirlit yfir upplýsingar vinnuskýrsla.

Þegar búið er að samþykkja eða hafna vinnuskýrslu er ekki hægt að breyta henni nema hún sé enduropnuð fyrst. Eftirfarandi ferli lýsir því hvernig á að enduropna vinnuskýrslu sem hefur verið samþykkt eða hafnað.

## <a name="to-reopen-a-time-sheet"></a>Til að enduropna vinnuskýrslu
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **stjórnandi vinnuskýrslur** eða **Vinnuskýrslur** og veldu síðan tengda tengilinn.
2. Opnið vinnuskýrslu úr listanum.  

    > [!NOTE]  
    >   Aðeins er hægt að enduropna línur sem hafa stöðuna **Samþykkt**. Ekki er hægt að enduropna línur með stöðuna **Hafnað**. Ekki er hægt að opna vinnuskýrslu á ný hafi nú verið bókuð.  
3. Á síðunni **Vinnuskýrsla** skal velja aðgerðina **Opna aftur** og síðan aðgerðina **Allar sendar línur** til að opna aftur allar línur eða aðgerðina **Aðeins valdar línur** til að opna aftur aðeins línurnar sem eru valdar á síðunni **Vinnuskýrsla**.
4. Velja hnappinn **Í lagi**. Staða vinnuskýrslulínunnar eða -línanna breytist í **Sent**.  

## <a name="to-view-and-approve-time-sheets-by-job"></a>Að skoða og samþykkja vinnuskýrslur eftir verki

Í verki er hægt að tilgreina manneskju sem ber ábyrgð á verkinu. Þær upplýsingar eru tengdar við línur í vinnuskýrslu, og þær má nota til að setja fram lista yfir vinnuskýrslur sem verkefnastjóri verður að endurskoða og samþykkja. Til dæmis getur verkstjóri teymis verið ábyrgur fyrir ákveðnum vinnslum í fyrirtækinu. Í því tilviki ætti að tilgreina stjórnanda sem **Ábyrgðaraðila** á verkspjaldinu. Í þessu upplýsingayfirliti vinnuskýrslna, er hægt að skoða verkhlutana sem tengjast starfi og magni tíma sem notaður er.

> [!NOTE]
> Til að geta samþykkt vinnuskýrslur í glugganum **Vinnuskýrsla stjórnanda eftir verki**, þarf fyrst að velja valkostinn **Vinnuskýrsla eftir samþykkt verks** á síðunni **Uppsetning tilfanga**. Frekari upplýsingar eru í [Setja upp tilföng](projects-how-setup-resources.md).

### <a name="to-approve-or-reject-a-time-sheet-by-job"></a>Að samþykkja eða hafna vinnuskýrslu eftir verki

1. Í reitinn **Leit** skal færa inn **Vinnuskýrsla stjórnanda** og velja síðan viðkomandi tengil. Microsoft Dynamics NAV birtir lista yfir vinnuskýrslulínur tengdar verkunum sem voru í ábyrgð notanda.
2. Á flipanum **Heim** veljið **Samþykkja**. Velja **Allir** til að samþykkja allar línur. Velja **Valið** til að samþykkja aðeins valdar línur.

    > [!NOTE]
    > Aðeins er hægt að samþykkja vinnuskýrslur sem hafa stöðuna **Sent**.

3. Til að veita frekari upplýsingar um samþykki eða höfnun skal velja vinnuskýrslulínu og fara í flipann **Færsluleit** og velja **Athugasemdir**. Í reitnum **Dagsetning** færið inn dagsetningu og síðan athugasemd í reitinn **Athugasemd**.
4. Velja hnappinn **Í lagi**.

> [!NOTE]
> Þegar búið er að samþykkja eða hafna vinnuskýrslulínu eftir verki er ekki hægt að enduropna eða breyta þeim í glugganum **Vinnuskýrsla**.

## <a name="to-post-time-sheet-lines-in-a-resource-journal"></a>Til að bóka vinnuskýrslulínur í forðabók
Eftir að búið er að samþykkja vinnuskýrslufærslur fyrir forða, er hægt að bóka þær á viðeigandi forðabók.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Forðabók** og veldu síðan tengda tengilinn.  
2. Veljið aðgerðina **Stinga upp á línum úr vinnuskýrslum**.  
3. Fyllið inn í svæðin eftir þörfum.  
4. Velja hnappinn **Í lagi**. Færslur fyrir notkun eru stofnaðar í forðabókinni þar sem hægt er að breyta upplýsingunum eftir þörfum.  
5. Valið er **Bóka** aðgerðin.  
6. Til að staðfesta bókunina skal velja aðgerðina **Verkfærslur**. Síðan **Forðafærslur** opnast og birtir niðurstöður á bókun forðabókar.

## <a name="to-post-time-sheet-lines-in-a-job-journal"></a>Til að bóka vinnuskýrslulínur í verkbók
Eftir að búið er að samþykkja vinnuskýrslufærslur fyrir verk, er hægt að bóka þær á viðeigandi verkbók.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verkbók** og veldu síðan tengda tengilinn.  
2. Veljið aðgerðina **Stinga upp á línum úr vinnuskýrslum**.  
3. Fyllið inn í svæðin eftir þörfum.  
4. Velja hnappinn **Í lagi**. Færslur fyrir notkun eru stofnaðar í verkbókinni þar sem hægt er að breyta upplýsingunum eftir þörfum.  

    > [!NOTE]  
    >   Upplýsingar um tegund verks og hvort verkið er reikningshæft eru afritaðar úr vinnuskýrslulínu. Ef þörf krefur er hægt að fækka klukkustundum og bóka að hluta. Ef magnið er minnkað mun línan sem stofnuð er innihalda eftirstandandi klukkustundir næst þegar aðgerðin **Stinga upp á línum úr vinnuskýrslum** er valin.  
5. Valið er **Bóka** aðgerðin.  
6. Til að staðfesta bókunina skal velja aðgerðina **Verkfærslur**. Síðan **Verkfærslur** opnast og birtir niðurstöður á bókun forðabókar.

## <a name="to-archive-time-sheets"></a>Til að færa vinnuskýrslur í safn
Þegar búið er að bóka vinnuskýrslu, er hægt að safna þeim fyrir seinni tíma tilvísun. Bóka þarf allar vinnuskýrslulínur áður en hægt er að færa vinnuskýrslu í skjalasafn.

> [!NOTE]  
>   Þegar vinnuskýrsla er sett í safn er hún fjarlægð úr listunum á síðunni **Vinnuskýrslur** og síðunni **Vinnuskýrsla stjórnanda**.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Færa vinnuskýrslur til safnvistunar** og veldu síðan tengda tengilinn.  
2. Fyllið út aðra reitina að þörfum og smellið veljið síðan hnappinn **Í lagi**.  
3. Til að endurskoða safnvistuð vinnuskýrslur, veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **vinnuskýrslusöfn** eða **Stjórnandi vinnuskýrslusöfn** og veldu síðan tengda tengilinn.

## <a name="see-also"></a>Sjá einnig
[Verkefnastjórnun](projects-manage-projects.md)  
[Setja upp verkefnastjórnun](projects-setup-projects.md)    
[Fjármál](finance.md)  
[Innkaup](purchasing-manage-purchasing.md)         
[Sala](sales-manage-sales.md)     
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]