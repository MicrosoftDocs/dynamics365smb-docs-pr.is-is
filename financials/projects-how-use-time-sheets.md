---
title: "Vinna með vinnuskýrslur fyrir verk| Microsoft Docs"
description: "Lýsir því hvernig skal stofna vinnuskýrslu fyrir verk, afrita áætlunarlínur yfir í hana, skilgreina vinnutegund, fylla inn í skýrsluna og senda hana inn til samþykkis."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 9d67198e172b82c20c9d998854a819e39ae523ff
ms.contentlocale: is-is
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-use-time-sheets-for-jobs"></a>Hvernig á að: Nota vinnuskýrslur fyrir verk
Nota skal keyrsluna **Stofna vinnuskýrslur** til að setja upp vinnuskýrslur fyrir tilgreindan fjölda tímabila eða vikna. Notandi verður að hafa heimildir til að hægt sé að búa til vinnuskýrslur.

Hægt er að afrita og nota verkáætlunarlínur í vinnuskýrslu. Með því móti þarf aðeins að færa upplýsingarnar inn á einum stað og línuupplýsingarnar eru alltaf réttar.

Eftir að búið er að samþykkja vinnuskýrslufærslur fyrir verk er hægt að bóka þær á viðeigandi verkbók eða forðabók.

Áður en hægt er að nota vinnuskýrslur þarf að setja upp almennar upplýsingar og tilgreina stjórnanda og einn eða fleiri samþykkjendur vinnuskýrslna. Frekari upplýsingar eru í [Hvernig á að: Setja upp vinnuskýrslur](projects-how-setup-time-sheets.md).

> [!NOTE]  
>   Þessi virkni krefst þess að upplifun þín sé stillt á **Pakki**. Nánari upplýsingar, sjá [Sérstilla þína [!INCLUDE[d365fin](includes/d365fin_md.md)] upplifun](ui-experiences.md).

## <a name="to-create-a-time-sheet"></a>Til að búa til vinnuskýrslu
Hægt er að nota keyrsluna **Stofna vinnuskýrslur** til að setja upp vinnuskýrslur fyrir tilgreindan fjölda tímabila eða vikna. Eigandi vinnuskýrslunnar getur þá opnað hana og skráð tíma sem eytt hefur verið í verk.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **vinnuskýrslur** og velja svo viðeigandi tengil.
2. Í glugganum **Vinnuskýrslulisti** skal velja aðgerðina **Búa til vinnuskýrslur**.
3. Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Reitirnir **Nota vinnuskýrslu** og **Notandakenni eiganda vinnuskýrslu** verða að vera fylltir út á spjaldinu fyrir forða vinnuskýrslunnar.

1. Velja hnappinn **Í lagi**.  

Í glugganum **Vinnuskýrslulisti** er hægt að sjá allar vinnuskýrslur sem hafa verið stofnaðar.

## <a name="to-copy-job-planning-lines-to-a-time-sheet"></a>Til að afrita áætlunarlínur verks á vinnuskýrslu
Eftirfarandi ferli lýsir því hvernig eigi að flýtistofna verkáætlunarlínur á vinnuskýrslu.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **vinnuskýrslur** og velja svo viðeigandi tengil.  
2. Í glugganum **Vinnuskýrslulisti** skal velja vinnuskýrslu fyrir viðeigandi tímabil og velja svo aðgerðina **Breyta vinnuskýrslu**.  
3. Veljið aðgerðina **Stofna línur úr verkáætlun**. Allar verkáætlunarlínur á tímabilinu í vinnuskýrslunni eru afritaðar í vinnuskýrslu aðilans eða vélarinnar í reitnum **Forði nr.** í vinnuskýrslunni.

## <a name="to-define-work-types-and-add-one-to-a-time-sheet"></a>Til að skilgreina tegundir vinnu og bæta tegund vinnu við vinnuskýrslu
Hægt er að skilgreina tegund vinnu fyrir allar vinnuskýrslulínur fyrir verk. Með þeim hætti er hægt að bæta við upplýsingum sem þarf til að rukka viðskiptavininn og fyrir mismunandi tegundir af vinnu.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **vinnuskýrslur** og velja svo viðeigandi tengil.   
2. Opnið viðeigandi vinnuskýrslu.
3. Veljið reitinn **Lýsing**.  
4. Í glugganum **Verkupplýsingar vinnuskýrslulínu** skal velja reitinn **Vinnutegundarkóti** og velja tegund vinnu úr listanum, s.s. **Mílur**.  
5. Ef engin tegund vinnu er til skal velja aðgerðina **Nýtt**.
6. Í glugganum **Tegundir vinnu** þarf að fylla reitina út eftir þörfum.
7. Endurtakið skref 4 til að úthluta nýju verktegundinni á vinnuskýrsluna.

## <a name="to-reuse-time-sheet-lines-in-other-time-sheets"></a>Til að endurnýta vinnuskýrslulínur í öðrum vinnuskýrslum
Ef upplýsingar tímablaðs haldast óbreyttar á milli tímabila má spara tíma með því að afrita línur úr fyrra tímabili. Síðan er tímanotkunin fyrir nýja tímabilið færð inn.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **vinnuskýrslur** og velja svo viðeigandi tengil.  
2. Opnið vinnuskýrsluna fyrir tímabil sem er síðar en tímabilið fyrir fyrirliggjandi vinnuskýrslu með línum.  
3. Veljið aðgerðina **Afrita línur úr fyrri vinnuskýrslu**.

Línurnar eru afritaðar, með upplýsingum eins og gerð og lýsingu. Ef línan tengist til dæmis verki skal **Verknr.** afritað. Allar afritað línur eru með stöðuna **Opna**. Þá er hægt að breyta línunum eftir þörfum.

## <a name="to-fill-in-a-time-sheet-lines-and-submit-for-approval"></a>Til að fylla út vinnuskýrslulínur og senda til samþykktar
Vinnuskýrsluskráning er rakin í klukkustundum, sem er stöðluð grunnmælieining fyrir forða. Sjálfgefið er að vinnuskýrsla sýni sameiginlega vinnudaga frá mánudegi til föstudags.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **vinnuskýrslur** og velja svo viðeigandi tengil.  
2. Veljið vinnuskýrslu fyrir viðeigandi tímabil og veljið svo aðgerðina **Breyta tímaskýrslu**.  
3. Fyllið í reitina í línu eins og þörf krefur. Færið inn fjölda stunda sem forðinn notar hvern dag vikunnar.

    > [!TIP]  
>   Hægt er að fara yfir samtölu tímaskýrslustunda sem settar hafa verið inn í upplýsingakassann **Rauntími/áætlaður tími samantekt**  
4. Endurtakið skref 3 fyrir aðrar tegundir vinnu sem forðinn innir af hendi.
5. Veljið aðgerðina **Senda** og veljið svo aðgerðina **Allar opnar línur** til að senda allar línur eða aðgerðina **Aðeins valdar línur** til að senda aðeins þær línur sem eru valdar í glugganum **Vinnuskýrsla**.  

    > [!NOTE]  
>   Aðeins er hægt að senda tímaskýrslulínur sem innihalda skráðan tíma.  
6. Til að breyta upplýsingum í línu sem hefur verið stillt á **Sent** skal velja línu og velja svo aðgerðina **Enduropna**.

    > [!NOTE]  
>   Stundum gæti stjórnandi hafnað tímaskýrslulínu sem lögð er fram til samþykktar. Ef lína hefur stöðuna **Hafnað** er hægt að gera breytingar í línunni og velja **Senda** aftur.  
7. Velja hnappinn **Í lagi**.

## <a name="to-approve-or-reject-a-time-sheet"></a>Til að samþykkja eða hafna vinnuskýrslu
Senda þarf vinnuskýrslu til samþykkis áður en hægt er að nota hana. Hægt er að samþykkja og hafna einstaka línum í vinnuskýrslu eða senda þær aftur til sendanda fyrir frekari aðgerðir. Hægt er að samþykkja vinnuskýrslu með tvenns konar hætti:

* Vinnuskýrslustjóri getur samþykkt allar vinnuskýrslur.
* Einstaklingurinn sem er tilgreindur í reitnum **Notandakenni samþykkjanda vinnuskýrslu** á forðaspjaldi getur samþykkt vinnuskýrslur viðkomandi forða. Frekari upplýsingar eru í [Hvernig á að: Setja upp vinnuskýrslur](projects-how-setup-time-sheets.md).

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Stjórnandi vinnuskýrslur** og velja svo viðeigandi tengil.
2. Veljið vinnuskýrslu úr listanum.  
3. Í glugganum **Vinnuskýrsla** skal velja aðgerðina **Samþykkja** og velja svo aðgerðina **Allar sendar línur** til að samþykkja allar línur eða aðgerðina **Aðeins valdar línur** til að samþykkja aðeins þær línur sem eru valdar í glugganum **Vinnuskýrsla**.
4. Velja hnappinn **Í lagi**.  
5. Einnig er hægt að velja aðgerðina **Hafna** og fylgja skrefum 4 til 5.  

> [!TIP]  
>   Nota skal upplýsingakassana **Staða vinnuskýrslu** og **Samantekt fyrir rauntíma/áætlaðan tíma** til að fá yfirlit yfir upplýsingar vinnuskýrsla.

Þegar búið er að samþykkja eða hafna vinnuskýrslu er ekki hægt að breyta henni nema hún sé enduropnuð fyrst. Eftirfarandi ferli lýsir því hvernig á að enduropna vinnuskýrslu sem hefur verið samþykkt eða hafnað.

## <a name="to-reopen-a-time-sheet"></a>Til að enduropna vinnuskýrslu
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Stjórnandi vinnuskýrslur** eða **Vinnuskýrslur** og velja svo viðeigandi tengil.
2. Opnið vinnuskýrslu úr listanum.  

    > [!NOTE]  
>   Aðeins er hægt að enduropna línur sem hafa stöðuna **Samþykkt**. Ekki er hægt að enduropna línur með stöðuna **Hafnað**. Ekki er hægt að opna vinnuskýrslu á ný hafi nú verið bókuð.  
3. Í glugganum **Vinnuskýrsla** skal velja aðgerðina **Enduropna** og velja svo aðgerðina **Allar sendar línur** til að enduropna allar línur eða aðgerðina **Aðeins valdar línur** til að enduropna aðeins þær línur sem eru valdar í glugganum **Vinnuskýrsla**.
4. Velja hnappinn **Í lagi**. Staða vinnuskýrslulínunnar eða -línanna breytist í **Sent**.  

## <a name="to-post-time-sheet-lines-in-a-resource-journal"></a>Til að bóka vinnuskýrslulínur í forðabók
Eftir að búið er að samþykkja vinnuskýrslufærslur fyrir forða, er hægt að bóka þær á viðeigandi forðabók.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **forðabók** og velja svo viðeigandi tengil.  
2. Veljið aðgerðina **Stinga upp á línum úr vinnuskýrslum**.  
3. Fyllið inn í svæðin eftir þörfum.  
4. Velja hnappinn **Í lagi**. Færslur fyrir notkun eru stofnaðar í forðabókinni þar sem hægt er að breyta upplýsingunum eftir þörfum.  
5. Valið er **bóka** aðgerð.  
6. Til að staðfesta bókunina skal velja aðgerðina **Verkfærslur**. Glugginn **Forðafærslur** opnast og sýnir niðurstöður bókunar forðabókarinnar.

## <a name="to-post-time-sheet-lines-in-a-job-journal"></a>Til að bóka vinnuskýrslulínur í verkbók
Eftir að búið er að samþykkja vinnuskýrslufærslur fyrir verk, er hægt að bóka þær á viðeigandi verkbók.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Verkbækur** og velja svo viðeigandi tengil.  
2. Veljið aðgerðina **Stinga upp á línum úr vinnuskýrslum**.  
3. Fyllið inn í svæðin eftir þörfum.  
4. Velja hnappinn **Í lagi**. Færslur fyrir notkun eru stofnaðar í verkbókinni þar sem hægt er að breyta upplýsingunum eftir þörfum.  

    > [!NOTE]  
>   Upplýsingar um tegund verks og hvort verkið er reikningshæft eru afritaðar úr vinnuskýrslulínu. Ef þörf krefur er hægt að fækka klukkustundum og bóka að hluta. Ef magnið er minnkað mun línan sem stofnuð er innihalda eftirstandandi klukkustundir næst þegar aðgerðin **Stinga upp á línum úr vinnuskýrslum** er valin.  
5. Valið er **bóka** aðgerð.  
6. Til að staðfesta bókunina skal velja aðgerðina **Verkfærslur**. Glugginn **Verkfærslur** opnast og sýnir niðurstöður bókunar forðabókarinnar.

## <a name="to-archive-time-sheets"></a>Til að færa vinnuskýrslur í safn
Þegar búið er að bóka vinnuskýrslu, er hægt að safna þeim fyrir seinni tíma tilvísun. Bóka þarf allar vinnuskýrslulínur áður en hægt er að færa vinnuskýrslu í skjalasafn.

> [!NOTE]  
>   Þegar vinnuskýrsla er sett í safn er hún fjarlægð úr listunum í bæði  **Vinnuskýrslur** og **Vinnuskýrsla stjórnanda** gluggunum.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Færa vinnuskýrslur í safn** og velja svo viðeigandi tengil.  
2. Fyllið út aðra reitina að þörfum og smellið veljið síðan hnappinn **Í lagi**.  
3. Til að fara yfir vinnuskýrslur í safni skal velja ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið") tákn, færa inn **Vinnuskýrsluskrár** eða **Vinnuskýrsluskrár stjórnanda**, og velja síðan viðeigandi tengil.

## <a name="see-also"></a>Sjá einnig
[Verkefnastjórnun](projects-manage-projects.md)  
[Setja upp verkefnastjórnun](projects-setup-projects.md)    
[Fjármál](finance.md)  
[Innkaup](purchasing-manage-purchasing.md)         
[Sala](sales-manage-sales.md)     
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

