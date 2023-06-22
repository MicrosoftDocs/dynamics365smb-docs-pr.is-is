---
title: Nota Vinnuskýrslur
description: 'Lýsir því hvernig skal stofna vinnuskýrslu, skilgreina vinnutegundir, fylla út í vinnuskýrsluna og senda hana inn til samþykkis.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'project management, capacity, staff, resource, time sheets'
ms.search.form: '950, 951, 973'
ms.date: 03/01/2022
ms.author: edupont
---
# <a name="use-time-sheets" />Nota Vinnuskýrslur

Hægt er að nota vinnuskýrslur í [!INCLUDE [prod_short](includes/prod_short.md)] til að rekja fjarvist og til að rekja tíma og tilföng sem eytt er í verkefni. Með stjórnun tíma er hægt að bera kennsl á vandamál snemma og forðast tafir eða umframkostnað. Með vinnuskýrslu getur starfskraftur auðveldlega skráð tímanotkun fyrir einstakling eða væl og stjórnandi getur á auðveldan hátt skoðað notkun og úthlutun. Í þessari grein er því lýst hvernig skal stofna vinnuskýrslu, skilgreina vinnutegundir, fylla út í vinnuskýrsluna og senda hana inn til samþykkis.  

Hægt er að afrita og nota verkáætlunarlínur í vinnuskýrslu. Með því móti þarf aðeins að færa upplýsingarnar inn á einum stað og línuupplýsingarnar eru alltaf réttar.

Eftir að búið er að samþykkja vinnuskýrslufærslur fyrir verk er hægt að bóka þær á viðeigandi verkbók eða forðabók.

Áður en hægt er að nota vinnuskýrslur þarf að setja upp almennar upplýsingar og tilgreina stjórnanda og einn eða fleiri samþykkjendur vinnuskýrslna. Frekari upplýsingar eru í [Setja upp vinnuskýrslur](projects-how-setup-time-sheets.md).  

> [!TIP]
> Frá og með 2021 útgáfutímabili 2 er hægt að stjórna úthlutuðum vinnuskýrslum í fartæki. Stjórnandinn þinn gæti samt sem áður þurft að virkja eiginleikann **Eiginleikauppfærsla: Ný upplifun fyrir vinnuskýrslu** á síðu [Eiginleikastjórnunar](https://businesscentral.dynamics.com/?page=2610) til að nota þennan möguleika. Frekari upplýsingar eru í [Setja upp vinnuskýrslur](projects-how-setup-time-sheets.md).

## <a name="to-create-time-sheets" />Til að stofna vinnuskýrslur

Hægt er að nota keyrsluna **Stofna vinnuskýrslur** til að setja upp vinnuskýrslur fyrir tilgreindan fjölda tímabila eða vikna. Eigandi vinnuskýrslunnar getur þá opnað hana og skráð tíma sem eytt hefur verið í verk. Einnig er hægt [tímasetja runuvinnsluna á að keyra sjálfkrafa](ui-work-report.md#ScheduleReport).  

> [!IMPORTANT]
> Notandi verður að hafa heimildir til að hægt sé að búa til vinnuskýrslur. Frekari upplýsingar eru í [Setja upp vinnuskýrslur](projects-how-setup-time-sheets.md).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnuskýrslur** og velja síðan viðkomandi tengil.
2. Á síðunni **Vinnuskýrslur** skal velja aðgerðina **Stofna vinnuskýrslur**.
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Reitirnir **Nota vinnuskýrslu** og **Notandakenni eiganda vinnuskýrslu** verða að vera fylltir út á spjaldinu fyrir forða vinnuskýrslunnar.

    Það má líka velja aðgerðina **Tímasetja** til að tilgreina hversu oft á að keyra verkið sjálfkrafa. Til að grunnstilla verkið á að keyra vikulega í fjórar vikur skal til dæmis á síðunni **Tímasetja skýrslu - Stofna vinnuskýrslur** stilla reitinn **Dagsetningarformúla næstu keyrslu** á *4W*. Frekari upplýsingar eru í [Tímasetja keyrslu skýrslu](ui-work-report.md#ScheduleReport).  
4. Velja hnappinn **Í lagi**.  

Á síðunni **Vinnuskýrslur** er hægt að sjá allar vinnuskýrslur sem hafa verið stofnaðar. Hver vinnuskýrsla samanstendur af einni eða fleiri línum sem skilgreina tímann sem þú vilt til að senda inn til samþykkis. Eftirfarandi tafla lýsir gerðum lína sem hægt er að bæta við vinnuskýrsluna.

| **Reitur** | **Lýsing** |
|---|---|
| | Notið til að bæta við athugasemd eða merki í **lýsingarreitinn** á vinnuskýrslulínunni. Til dæmis má nota þennan reit til að flokka vinnuskýrslufærslur. Ef reiturinn **Tegund** er skilinn eftir auður í tímablaðslínu er ekki hægt að færa tímagildi inn í vikudagareiti þeirrar línu. |
| Fjarvist | Notið til að skrá fjarvistartíma í vinnuviku. Til að ljúka upplýsingum fyrir línuna skal tilgreina gerð fjarvistar í reitinn **Ástæðukóði fjarvistar**. |
| Samsetningarpöntun | Notað til að skrá tíma fyrir samsetningarpantanir. Vinnuskýrslulína af þessari gerð er stofnuð þegar bókaðar eru samsetningarpöntunarlínur sem hafa forða sem settur er þannig upp að hann noti vinnuskýrslur. Ekki er hægt að velja línu af þessari gerð handvirkt. |
| Verk | Notið til að skrá tímanotkun fyrir verk. Til að ljúka upplýsingum fyrir línuna skal tilgreina verknúmer og verkhlutanúmer sem ská á tíma fyrir. Hægt er að skrái vinnutíma fyrir línur sem ekki hefur verið raðað.|
| Forði | Notið til að skrá tímanotkun fyrir forða. Til að ljúka upplýsingum fyrir línuna skal gefa upp lýsingu á verkinu. |
| Þjónusta | Notið til að skrá tímanotkun fyrir þjónustupöntun eða þjónustukreditreikning. |

Til að senda inn vinnuskýrslu fyrir vinnuviku þar sem þú vannst við að hreinsa verk flesta daga en varst með einn frídag vegna læknisheimsóknar myndir þú til dæmis bæta við línum eins og sýnt er í eftirfarandi töflu.

| Gerð | Lýsing | Vinnutegundarkóði | Tegund fjarvistarkóða |
|--|--|--|--|
| Forði | Vinnutími | Þrif |  |
| Fjarvist | Frí |  | Heilsa |
|  | Ég þurfti að taka mér frí á þriðjudaginn vegna læknisheimsóknar. |  |  |

Í þessu ímyndaða dæmi myndir þú síðan skrá réttan fjölda vinnustunda á viðeigandi dögum í reitina fyrir hvern vikudag.  

> [!TIP]
> Í flestum tilvikum verður fyrirtækið þitt með forskilgreindar vinnutegundir fyrir ýmsar línugerðir. Í þeim tilvikum velur þú bara viðeigandi vinnutegund af listanum og bætir svo við þinni eigin lýsingu.  
>
> Veldu vinnutegundina með því að velja hnappinn :::image type="icon" source="media/assist-edit-icon.png" border="false"::: í reitnum **Lýsing**, með því að velja aðgerðina **Upplýsingar um aðgerðir** og síðan tilgreina þær á síðunni sem opnast eða með því að velja þær í reitnum **Kóði vinnutegundar** eða í reitnum **Tegund fjarvistarkóða**. Í slíku tilfelli geturðu sleppt hlutann [Að skilgreina vinnutegundir og bæta einni við vinnuskýrslu](#to-define-work-types-and-add-one-to-a-time-sheet).  

## <a name="to-reuse-time-sheet-lines-in-other-time-sheets" />Til að endurnýta vinnuskýrslulínur í öðrum vinnuskýrslum

Ef upplýsingar tímablaðs haldast óbreyttar á milli tímabila má spara tíma með því að afrita línur úr fyrra tímabili. Síðan er tímanotkunin fyrir nýja tímabilið færð inn.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnuskýrslur** og velja síðan viðkomandi tengil.  
2. Opnið vinnuskýrsluna fyrir tímabil sem er síðar en tímabilið fyrir fyrirliggjandi vinnuskýrslu með línum.  
3. Veljið aðgerðina **Afrita línur úr fyrri vinnuskýrslu**.

Línurnar eru afritaðar, með upplýsingum eins og gerð og lýsingu. Til dæmis, ef línurnar eru tengdar við starf, er **Verk nr.** afritað. Allar afritað línur eru með stöðuna **Opna**. Þá er hægt að breyta línunum eftir þörfum.

## <a name="to-copy-job-planning-lines-to-a-time-sheet" />Til að afrita áætlunarlínur verks á vinnuskýrslu
Eftirfarandi ferli lýsir því hvernig eigi að flýtistofna verkáætlunarlínur á vinnuskýrslu.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnuskýrslur** og velja síðan viðkomandi tengil.  
2. Á síðunni **Vinnuskýrslur** skal velja vinnuskýrslu fyrir viðeigandi tímabil.  
3. Veljið aðgerðina **Stofna línur úr verkáætlun**. Allar verkáætlunarlínur í tímabili vinnublaðsins eru afritaðar í vinnublaðið fyrir manneskjuna eða vélina í **Tilfang nr.** reitinn á vinnublaðsins.

## <a name="to-define-work-types-and-add-one-to-a-time-sheet" />Til að skilgreina tegundir vinnu og bæta tegund vinnu við vinnuskýrslu

Hægt er að skilgreina tegund vinnu fyrir allar línur í vinnuskýrslu fyrir þjónustupantanir, vinnupantanir og forða. Með þeim hætti er hægt að bæta við upplýsingum sem þarf til að rukka viðskiptavininn og fyrir mismunandi tegundir af vinnu.  

1. Í síðunni **Vinnuskýrslur** skal velja viðeigandi vinnuskýrslu.
2. Í fyrstu línunum í hlutanum **Línur** skal velja reitinn **Gerð** og síðan velja viðeigandi gerð eins og *Tilfang*.  
3. Veldu reitinn **Lýsing** og síðan á síðunni **Upplýsingar um tilfang vinnuskýrslulínu** skal fylla út reitina. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
    1. Ef engin tegund vinnu er til skal velja aðgerðina **Nýtt**.
    2. Á síðunni **Vinnutegundir** skal fylla út reitina eftir þörfum og síðan fara aftur í vinnuskýrsluna.
4. Fylltu út það sem eftir er af vinnuskýrslunni. Nánari upplýsingar eru í [Til að fylla út vinnuskýrslulínur og senda til samþykktar](#to-fill-in-time-sheet-lines-and-submit-for-approval).  

> [!TIP]
> Sambærileg skref eiga við þegar fjarvistarkóðar eru skilgreindir.

## <a name="to-fill-in-time-sheet-lines-and-submit-for-approval" />Til að fylla út vinnuskýrslulínur og senda til samþykktar

Vinnuskýrsluskráning er rakin í klukkustundum, sem er stöðluð grunnmælieining fyrir forða. Sjálfgefið er að vinnuskýrsla sýni sameiginlega vinnudaga frá mánudegi til föstudags.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnuskýrslur** og velja síðan viðkomandi tengil.  
2. Veljið vinnuskýrslu fyrir viðeigandi tímabili.
3. Fyllið í reitina í línu eins og þörf krefur. Færið inn fjölda stunda sem forðinn notar hvern dag vikunnar.  

    Í flestum tilvikum bætirðu við línu af gerðinni *Tilfang* til að rekja vinnu og síðan skráir þú vinnustundir fyrir hvern dag fyrir sig. Ef þú vilt skrá fjarvist bætirðu við línu af gerðinni *Fjarvist*.  

    > [!TIP]  
    > Hægt er að fara yfir samtölu tímaskýrslustunda sem settar hafa verið inn í upplýsingakassann **Rauntími/áætlaður tími samantekt**  
4. Endurtakið skref 3 fyrir aðrar tegundir vinnu sem forðinn innir af hendi.  

    Næst verður þú að ákveða hvort þú viljir senda inn allar línur vinnuskýrslunnar eða hvort þú viljir senda inn einstakar línur.  

    * Til að senda inn vinnuskýrsluna fyrir eina eða fleiri línur skaltu velja viðeigandi línu og síðan velja aðgerðina **Senda inn**.

        Á innsendingarsíðunni skal velja valkostinn **Aðeins valdar línur**. Staða línunnar breytist úr *Opin* í *Innsend*.
    * Til að senda inn vinnuskýrslu fyrir allar opnar línur skal velja aðgerðina **Senda inn** efst á síðunni **Vinnuskýrsla**.  

        Þú verður beðin(n) um að staðfesta að þú viljir senda inn allar opnar línur á núverandi vinnuskýrslu.  

    > [!NOTE]  
    > Aðeins er hægt að senda tímaskýrslulínur sem innihalda skráðan tíma.  
5. Til að breyta upplýsingum í línu sem hefur verið stillt á **Sent** skal velja línu og velja svo aðgerðina **Enduropna**.

    > [!NOTE]  
    >   Stundum gæti stjórnandi hafnað tímaskýrslulínu sem lögð er fram til samþykktar. Ef lína hefur stöðuna **Hafnað** er hægt að gera breytingar í línunni og velja **Senda** aftur.  
6. Velja hnappinn **Í lagi**.

## <a name="to-approve-or-reject-a-time-sheet" />Til að samþykkja eða hafna vinnuskýrslu
Senda þarf vinnuskýrslu til samþykkis áður en hægt er að nota hana. Hægt er að samþykkja og hafna einstaka línum í vinnuskýrslu eða senda þær aftur til sendanda fyrir frekari aðgerðir. Hægt er að samþykkja vinnuskýrslu með tvenns konar hætti:

* Vinnuskýrslustjóri getur samþykkt allar vinnuskýrslur.
* Einstaklingurinn sem er tilgreindur í reitnum **Notandakenni samþykkjanda vinnuskýrslu** á forðaspjaldi getur samþykkt vinnuskýrslur viðkomandi forða. Frekari upplýsingar eru í [Setja upp vinnuskýrslur](projects-how-setup-time-sheets.md).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnuskýrslur verkstjóra** og velja síðan viðkomandi tengil.
2. Veljið vinnuskýrslu úr listanum.  
3. Á síðunni **Vinnuskýrsla**. 
    1. Velja aðgerðina **Vinna** og svo aðgerðina **Samþykkja**.
    2. Veljið aðgerðina **Allar sendar línur** til að samþykkja allar línur eða aðgerðina **Aðeins valdar línur** til að samþykkja aðeins línurnar sem eru valdar á síðunni **Vinnuskýrsla**.
4. Velja hnappinn **Í lagi**.  
5. Einnig er hægt að velja aðgerðina **Hafna** og fylgja skrefum 4 til 5.  

> [!TIP]  
>   Nota skal upplýsingakassana **Staða vinnuskýrslu** og **Samantekt fyrir rauntíma/áætlaðan tíma** til að fá yfirlit yfir upplýsingar vinnuskýrsla.

Þegar búið er að samþykkja eða hafna vinnuskýrslu er ekki hægt að breyta henni nema hún sé enduropnuð fyrst. Eftirfarandi ferli lýsir því hvernig á að enduropna vinnuskýrslu sem hefur verið samþykkt eða hafnað.

## <a name="to-reopen-a-time-sheet" />Til að enduropna vinnuskýrslu
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnuskýrslur verkstjóra** eða **Vinnuskýrslur** og velja síðan viðkomandi tengil.
2. Opnið vinnuskýrslu úr listanum.  

    > [!NOTE]  
    >   Aðeins er hægt að enduropna línur sem hafa stöðuna **Samþykkt**. Ekki er hægt að enduropna línur með stöðuna **Hafnað**. Ekki er hægt að opna vinnuskýrslu á ný hafi nú verið bókuð.  
3. Á síðunni **Vinnuskýrsla** skal velja aðgerðina **Opna aftur** og síðan aðgerðina **Allar sendar línur** til að opna aftur allar línur eða aðgerðina **Aðeins valdar línur** til að opna aftur aðeins línurnar sem eru valdar á síðunni **Vinnuskýrsla**.
4. Velja hnappinn **Í lagi**. Staða vinnuskýrslulínunnar eða -línanna breytist í **Sent**.  

## <a name="to-view-and-approve-time-sheets-by-job" />Að skoða og samþykkja vinnuskýrslur eftir verki

Í verki er hægt að tilgreina manneskju sem ber ábyrgð á verkinu. Þær upplýsingar eru tengdar við línur í vinnuskýrslu, og þær má nota til að setja fram lista yfir vinnuskýrslur sem verkefnastjóri verður að endurskoða og samþykkja. Til dæmis getur verkstjóri teymis verið ábyrgur fyrir ákveðnum vinnslum í fyrirtækinu. Í því tilviki ætti að tilgreina stjórnanda sem **Ábyrgðaraðila** á verkspjaldinu. Í þessu upplýsingayfirliti vinnuskýrslna, er hægt að skoða verkhlutana sem tengjast starfi og magni tíma sem notaður er.

> [!NOTE]
> Til að geta samþykkt vinnuskýrslur í glugganum **Vinnuskýrsla stjórnanda eftir verki**, þarf fyrst að velja valkostinn **Vinnuskýrsla eftir samþykkt verks** á síðunni **Uppsetning tilfanga**. Frekari upplýsingar eru í [Setja upp tilföng](projects-how-setup-resources.md).

### <a name="to-approve-or-reject-a-time-sheet-by-job" />Að samþykkja eða hafna vinnuskýrslu eftir verki

1. Í reitinn **Leit** skal færa inn **Vinnuskýrsla stjórnanda** og velja síðan viðkomandi tengil. [!INCLUDE[prod_short](includes/prod_short.md)] birtir lista yfir vinnuskýrslulínur tengdar verkunum sem voru í ábyrgð notanda.
2. Veldu aðgerðina **Samþykkja** og síðan aðgerðina **Allar sendar línur** til að samþykkja allar línur eða aðgerðina **Aðeins valdar línur** til að samþykkja aðeins línurnar sem eru valdar á síðunni **Vinnuskýrsla**.

    > [!NOTE]
    > Aðeins er hægt að samþykkja vinnuskýrslur sem hafa stöðuna **Sent**.

3. Til að veita frekari upplýsingar um samþykki eða höfnun skal velja aðgerðina **Tengt** og svo **Athugasemdir** og síðan **Línuathugasemdir** og setja inn athugasemdir.
4. Velja hnappinn **Í lagi**.

> [!NOTE]
> Þegar búið er að samþykkja eða hafna vinnuskýrslulínu eftir verki er ekki hægt að enduropna eða breyta þeim í glugganum **Vinnuskýrsla**.

## <a name="to-post-time-sheet-lines-in-a-resource-journal" />Til að bóka vinnuskýrslulínur í forðabók
Eftir að búið er að samþykkja vinnuskýrslufærslur fyrir forða, er hægt að bóka þær á viðeigandi forðabók.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Forðabækur** og velja síðan viðkomandi tengil.  
2. Veljið aðgerðina **Stinga upp á línum úr vinnuskýrslum**.  
3. Á síðunni **Stinga upp á forðabókarlínum**, í reitina eftir því sem þörf krefur.  
4. Velja hnappinn **Í lagi**. Færslur fyrir notkun eru stofnaðar í forðabókinni þar sem hægt er að breyta upplýsingunum eftir þörfum.  
5. Valið er **Bóka** aðgerðin.  
6. Til að staðfesta bókunina skal velja aðgerðina **Verkfærslur**. Síðan **Forðafærslur** opnast og birtir niðurstöður á bókun forðabókar.

## <a name="to-post-time-sheet-lines-in-a-job-journal" />Til að bóka vinnuskýrslulínur í verkbók
Eftir að búið er að samþykkja vinnuskýrslufærslur fyrir verk, er hægt að bóka þær á viðeigandi verkbók.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verkbækur** og velja síðan viðkomandi tengil.  
2. Veljið aðgerðina **Stinga upp á línum úr vinnuskýrslum**.  
3. Á síðunni **Stinga upp á vinnubókarlínu** þarf að fylla reitina út eftir þörfum.  
4. Velja hnappinn **Í lagi**. Færslur fyrir notkun eru stofnaðar í verkbókinni þar sem hægt er að breyta upplýsingunum eftir þörfum.  

    > [!NOTE]  
    >   Upplýsingar um tegund verks og hvort verkið er reikningshæft eru afritaðar úr vinnuskýrslulínu. Ef þörf krefur er hægt að fækka klukkustundum og bóka að hluta. Ef magnið er minnkað mun línan sem stofnuð er innihalda eftirstandandi klukkustundir næst þegar aðgerðin **Stinga upp á línum úr vinnuskýrslum** er valin.  
5. Valið er **Bóka** aðgerðin.  
6. Til að staðfesta bókunina skal velja aðgerðina **Verkfærslur**. Síðan **Verkfærslur** opnast og birtir niðurstöður á bókun forðabókar.

## <a name="to-archive-time-sheets" />Til að færa vinnuskýrslur í safn
Þegar búið er að bóka vinnuskýrslu, er hægt að safna þeim fyrir seinni tíma tilvísun. Bóka þarf allar vinnuskýrslulínur áður en hægt er að færa vinnuskýrslu í skjalasafn.

> [!NOTE]  
>   Þegar vinnuskýrsla er sett í safn er hún fjarlægð úr listunum á síðunni **Vinnuskýrslur** og síðunni **Vinnuskýrsla stjórnanda**.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnuskýrslur** og velja síðan viðkomandi tengil.
2. Veljið aðgerðina **Færa vinnuskýrslur í safn**  
3. Á síðunni **Færa vinnuskýrslur í safn** skal fylla út reitina eftir þörfum og velja síðan hnappinn **Í lagi**.  
4. Til að fara yfir vinnuskýrslur í safni skal velja ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnuskýrslusafn** eða **Vinnuskýrslusafn** verkstjóra og velja síðan viðkomandi tengil.

## <a name="see-also" />Sjá einnig
[Verkefnastjórnun](projects-manage-projects.md)  
[Setja upp verkefnastjórnun](projects-setup-projects.md)  
[Fjármál](finance.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Sala](sales-manage-sales.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
