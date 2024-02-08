---
title: Nota Vinnuskýrslur
description: Lærðu að útbúa vinnuskýrslur og senda þær til samþykktar.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.search.keywords: 'project management, capacity, staff, resource, time sheets'
ms.search.form: '950, 951, 973'
ms.date: 07/27/2023
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="use-time-sheets"></a>Nota Vinnuskýrslur

Notið vinnuskýrslur til að rekja fjarvistir og til að rekja tíma og tilföng sem er varið í verk. Rakningartími auðveldar notandanum að auðkenna mál snemma og forðast tafir eða kostnað við útkeyrslur. Vinnuskýrslur auðvelda úrræði til að tilkynna tímanotkun fyrir einstakling eða vél þannig að stjórnendur geti farið yfir notkunina og úthlutun hennar. Í greininni er því lýst hvernig unnið er með vinnuskýrslur.  

Hægt er að afrita og nota verkáætlunarlínur í vinnuskýrslu. Með því móti þarf aðeins að færa upplýsingarnar inn á einum stað og línuupplýsingarnar eru alltaf réttar. Til að fá frekari upplýsingar er farið í  [til að afrita verkáætlunarlínur í vinnuskjal](#copy-job-planning-lines-to-a-time-sheet).

Eftir að búið er að samþykkja vinnuskýrslufærslur fyrir verk er hægt að bóka þær á viðeigandi verkbók eða forðabók. Til að fá frekari upplýsingar er farið í  [til að bóka tímablaðslínur í verkbók](#to-post-time-sheet-lines-in-a-job-journal)  og  [til að bóka tímablaðslínur í forðabók](#post-time-sheet-lines-in-a-resource-journal).

Áður en hægt er að nota vinnuskýrslur þarf að setja upp almennar upplýsingar og tilgreina stjórnanda og einn eða fleiri samþykkjendur vinnuskýrslna. Til að fræðast meira um uppsetningu vinnublaða er farið í að  [Setja upp vinnuskýrslur](projects-how-setup-time-sheets.md).  

> [!TIP]
> Hægt er að nota vinnuskýrslur á farsíma. Til að gera það gæti þurft að kveikja á  **notkun nýrra vinnublaða reynsla**  skipta á  [uppsetningarsíðu](https://businesscentral.dynamics.com/?page=462)  á forða.

## <a name="create-time-sheets"></a>Stofna vinnuskýrslur

Hægt er að nota  **síðuna stofna vinnuskýrslur**  til að setja upp vinnuskýrslur fyrir tiltekinn fjölda tímabila eða vikna. Eigandi vinnuskýrslunnar getur þá opnað hana og skráð tíma sem eytt hefur verið í verk. Einnig er hægt [tímasetja runuvinnsluna á að keyra sjálfkrafa](ui-work-report.md#ScheduleReport).  

> [!IMPORTANT]
> Notandi verður að hafa heimildir til að hægt sé að búa til vinnuskýrslur. Til að fræðast nánar um heimildir er farið í  [Setja upp vinnuskýrslur](projects-how-setup-time-sheets.md).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn  **vinnuskýrslur** Stofna og velja síðan tengda tengilinn.

    > [!TIP]
    > Einnig er hægt að  **nota aðgerðina stofna vinnuskýrslur**  á  **listasíðu forða**  og á  **síðunni Forðaspjald** .
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Áður en vinnuskýrslur eru stofnaðar fyrir forða þarf að ganga úr skugga um að  **Reitirnir nota vinnublað**  og  **tímaskjöl eiganda**  séu tilgreindir fyrir þau á  **síðunni Forðaspjald** .

    Einnig er hægt að velja  **tímasetningu**  aðgerðar til að tilgreina hversu oft á að keyra verkið sjálfkrafa. Til dæmis til að skilgreina verkið sem á að keyra vikulega í fjórar vikur,  **í áætluninni skrá-stofna vinnuskýrslur tímablöð**  í  **reitinn Næsta keyrsludagsetningarregla**  er færð inn  **4w**. Ef fræðast á um hvernig á að raða skýrslum er farið í að  [raða skýrslu í keyrslu](ui-work-report.md#ScheduleReport).  

Á síðunni **Vinnuskýrslur** er hægt að sjá allar vinnuskýrslur sem hafa verið stofnaðar. Hver vinnuskýrsla samanstendur af einni eða fleiri línum sem skilgreina tímann sem þú vilt til að senda inn til samþykkis. Eftirfarandi tafla lýsir gerðum lína sem hægt er að bæta við vinnuskýrsluna.

| **Reitur** | **Lýsing** |
|---|---|
| | Notið til að bæta við athugasemd eða merki í **lýsingarreitinn** á vinnuskýrslulínunni. Til dæmis má nota þennan reit til að flokka vinnuskýrslufærslur. Ef reiturinn Tegund  **er hafður**  auður fyrir tímablaðslínu er ekki hægt að færa inn tímavirði í reitina vikudagur fyrir þá línu. |
| Fjarvist | Notið til að skrá þann tíma sem notandi er fjarverandi meðan á vinnuviku stendur. Til að ljúka upplýsingum fyrir línuna skal tilgreina gerð fjarvistar í reitinn **Ástæðukóði fjarvistar**. |
| Samsetningarpöntun | Notað til að skrá tíma fyrir samsetningarpantanir. Vinnuskýrslulína af þessari gerð er stofnuð þegar bókaðar eru samsetningarpöntunarlínur sem hafa forða sem settur er þannig upp að hann noti vinnuskýrslur. Ekki er hægt að velja línu handvirkt af þessari gerð. |
| Verk | Notið til að skrá tímanotkun fyrir verk. Til að ljúka upplýsingum fyrir línuna skal tilgreina verknúmer og verkhlutanúmer sem ská á tíma fyrir. Hægt er að skrá tíma fyrir línur sem hafa ekki verið áætlaðar.|
| Forði | Notið til að skrá tímanotkun fyrir forða. Til að ljúka upplýsingum fyrir línuna skal gefa upp lýsingu á verkinu. |
| Þjónusta | Notið til að skrá tímanotkun fyrir þjónustupöntun eða þjónustukreditreikning. |

Til dæmis er óskað eftir að skila inn vinnublaði fyrir viku þar sem gert var hreinsunarverkefni og var frí vegna erinda læknis. Eftirfarandi tafla sýnir hvernig línum er bætt við vinnuskýrslu.

| Gerð | Heimildasamstæða | Vinnutegundarkóði | Tegund fjarvistarkóða |
|--|--|--|--|
| Forði | Vinnutími | Þrif |  |
| Fjarvist | Frí |  | Heilsa |
|  | Ég þurfti að taka af stað á þriðjudag vegna erinda læknis. |  |  |

Í þessu ímyndaða dæmi myndir þú síðan skrá réttan fjölda vinnustunda á viðeigandi dögum í reitina fyrir hvern vikudag.  

> [!TIP]
> Í flestum tilvikum verður fyrirtækið þitt með forskilgreindar vinnutegundir fyrir ýmsar línugerðir. Í þeim tilvikum velur þú bara viðeigandi vinnutegund af listanum og bætir svo við þinni eigin lýsingu.  
>
> Veldu vinnutegundina með því að velja hnappinn :::image type="icon" source="media/assist-edit-icon.png" border="false"::: í reitnum **Lýsing**, með því að velja aðgerðina **Upplýsingar um aðgerðir** og síðan tilgreina þær á síðunni sem opnast eða með því að velja þær í reitnum **Kóði vinnutegundar** eða í reitnum **Tegund fjarvistarkóða**. Í þessu tilfelli er hægt að hunsa  [til að skilgreina vinnugerðir og bæta einu við vinnublaðshluta](#define-work-types-and-add-one-to-a-time-sheet) .  

## <a name="reuse-time-sheet-lines-in-other-time-sheets"></a>Endurnota tímablaðslínur í öðrum vinnuskýrslum

Ef upplýsingar tímablaðs haldast óbreyttar á milli tímabila má spara tíma með því að afrita línur úr fyrra tímabili. Síðan er tímanotkunin fyrir nýja tímabilið færð inn.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnuskýrslur** og velja síðan viðkomandi tengil.  
2. Opnið vinnuskýrsluna fyrir tímabil sem er síðar en tímabilið fyrir fyrirliggjandi vinnuskýrslu með línum.  
3. Veljið aðgerðina **Afrita línur úr fyrri vinnuskýrslu**.

Línurnar eru afritaðar, með upplýsingum eins og gerð og lýsingu. Til dæmis, ef línurnar eru tengdar við starf, er **Verk nr.** afritað. Allar afritað línur eru með stöðuna **Opna**. Þá er hægt að breyta línunum eftir þörfum.

## <a name="copy-job-planning-lines-to-a-time-sheet"></a>Afrita verkáætlunarlínur í vinnuskjal

Eftirfarandi ferli lýsir því hvernig eigi að flýtistofna verkáætlunarlínur á vinnuskýrslu.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnuskýrslur** og velja síðan viðkomandi tengil.  
2. Á síðunni **Vinnuskýrslur** skal velja vinnuskýrslu fyrir viðeigandi tímabil.  
3. Veljið aðgerðina **Stofna línur úr verkáætlun**. Allar verkáætlunarlínur í tímabili vinnublaðsins eru afritaðar í vinnublaðið fyrir manneskjuna eða vélina í **Tilfang nr.** reitinn á vinnublaðsins.

## <a name="define-work-types-and-add-one-to-a-time-sheet"></a>Skilgreina vinnugerðir og bæta einu við vinnublað

Hægt er að skilgreina vinnugerðina fyrir allar línur í tímablaði fyrir þjónustupantanir, vinnupantanir og forða. Með þeim hætti er hægt að bæta við upplýsingum sem þarf til að rukka viðskiptavininn og fyrir mismunandi tegundir af vinnu.  

1. Í síðunni **Vinnuskýrslur** skal velja viðeigandi vinnuskýrslu.
2. Í fyrstu línunum í hlutanum **Línur** skal velja reitinn **Gerð** og síðan velja viðeigandi gerð eins og *Tilfang*.  
3. Veldu reitinn **Lýsing** og síðan á síðunni **Upplýsingar um tilfang vinnuskýrslulínu** skal fylla út reitina. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
    1. Veljið  **nýju**  aðgerðina ef engar tegundir vinnu eru til.
    2. Á síðunni **Vinnutegundir** skal fylla út reitina eftir þörfum og síðan fara aftur í vinnuskýrsluna.
4. Fylltu út það sem eftir er af vinnuskýrslunni. Sjá  [til að fylla út vinnubókarlínur og senda inn fyrir samþykktarhlutann](#fill-in-time-sheet-lines-and-submit-for-approval)  til að fá frekari upplýsingar.  

> [!TIP]
> Sambærileg skref eiga við þegar fjarvistarkóðar eru skilgreindir.

## <a name="fill-in-time-sheet-lines-and-submit-for-approval"></a>Fylla út tímablaðslínur og senda inn til samþykkis

Vinnuskýrsluskráning er rakin í klukkustundum, sem er stöðluð grunnmælieining fyrir forða. Sjálfgefið er að vinnuskýrsla sýni sameiginlega vinnudaga frá mánudegi til föstudags.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnuskýrslur** og velja síðan viðkomandi tengil.  
2. Veljið vinnuskýrslu fyrir viðeigandi tímabili.
3. Fyllið í reitina í línu eins og þörf krefur. Færið inn fjölda stunda sem forðinn notar hvern dag vikunnar.  

    Í flestum tilvikum bætirðu við línu af gerðinni *Tilfang* til að rekja vinnu og síðan skráir þú vinnustundir fyrir hvern dag fyrir sig. Ef þú vilt skrá fjarvist bætirðu við línu af gerðinni *Fjarvist*.  

    > [!TIP]  
    > Hægt er að fara yfir samtölu tímaskýrslustunda sem settar hafa verið inn í upplýsingakassann **Rauntími/áætlaður tími samantekt**  
4. Endurtakið skref 3 fyrir aðrar tegundir vinnu sem forðinn innir af hendi.  

    Næst er ákveðið hvort á að senda allar eða valdar línur á vinnublaðinu.  

    * Til að senda inn vinnuskýrsluna fyrir eina eða fleiri línur skaltu velja viðeigandi línu og síðan velja aðgerðina **Senda inn**.

        Á innsendingarsíðunni skal velja valkostinn **Aðeins valdar línur**. Ástand línunnar breytist frá  **opnum**  að  **innsendum**.
    * Til að senda inn vinnuskýrslu fyrir allar opnar línur skal velja aðgerðina **Senda inn** efst á síðunni **Vinnuskýrsla**.  

        Staðfestið að þú viljir senda allar opnar línur í gildandi vinnublaði.  

    > [!NOTE]  
    > Aðeins er hægt að senda tímaskýrslulínur sem innihalda skráðan tíma.  
5. Til að breyta upplýsingum í línu sem hefur verið stillt á **Sent** skal velja línu og velja svo aðgerðina **Enduropna**.

    > [!NOTE]  
    > Stjórnandi gæti hafnað vinnublaðslínu sem er send til samþykkis. Ef lína hefur stöðuna **Hafnað** er hægt að gera breytingar í línunni og velja **Senda** aftur.  
6. Velja hnappinn **Í lagi**.

## <a name="approve-or-reject-a-time-sheet"></a>Til að samþykkja eða hafna vinnuskýrslu

Senda þarf vinnuskýrslu til samþykkis áður en hægt er að nota hana. Hægt er að samþykkja og hafna einstökum línum á vinnublaði eða senda þær aftur til undirnefndar. Vinnuskjal er samþykkt á tvennan hátt:

* Vinnuskýrslustjóri getur samþykkt allar vinnuskýrslur.
* Einstaklingurinn sem er tilgreindur í reitnum **Notandakenni samþykkjanda vinnuskýrslu** á forðaspjaldi getur samþykkt vinnuskýrslur viðkomandi forða. Til að fræðast meira um uppsetningu samþykkis er farið að  [Setja upp vinnuskýrslur](projects-how-setup-time-sheets.md).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnuskýrslur verkstjóra** og velja síðan viðkomandi tengil.
2. Veljið vinnuskýrslu úr listanum.  
3.  **Á síðunni vinnublað** : 
    1. Velja aðgerðina **Vinna** og svo aðgerðina **Samþykkja**.
    2. Veljið aðgerðina **Allar sendar línur** til að samþykkja allar línur eða aðgerðina **Aðeins valdar línur** til að samþykkja aðeins línurnar sem eru valdar á síðunni **Vinnuskýrsla**.
4. Velja hnappinn **Í lagi**.  
5. Einnig er hægt að velja aðgerðina **Hafna** og fylgja skrefum 4 til 5.  

> [!TIP]  
> Nota skal upplýsingakassana **Staða vinnuskýrslu** og **Samantekt fyrir rauntíma/áætlaðan tíma** til að fá yfirlit yfir upplýsingar vinnuskýrsla.

Þegar vinnuskjal hefur verið samþykkt eða því ekki hægt að breyta því nema það sé fyrst enduropnað. Eftirfarandi ferli lýsir því hvernig á að enduropna vinnuskýrslu sem hefur verið samþykkt eða hafnað.

## <a name="reopen-a-time-sheet"></a>Opna vinnuskjal

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnuskýrslur verkstjóra** eða **Vinnuskýrslur** og velja síðan viðkomandi tengil.
2. Opnið vinnuskýrslu úr listanum.  

    > [!NOTE]  
    > Aðeins er hægt að enduropna línur sem hafa stöðuna **Samþykkt**. Ekki er hægt að opna aftur línur sem hafa stöðuna  **hafnað**  eða hefur verið bókuð.  
3.  **Á síðunni vinnublað**  skal velja  **opnar opnar**  Aðgerðir og velja  **síðan aðgerðina allar sendar línur**  til að opna aftur allar línur eða  **aðeins**  Aðgerðir valinna lína til að opna aðeins aftur línurnar sem eru valdar á  **síðunni vinnublað** .
4. Velja hnappinn **Í lagi**. Staða vinnuskýrslulínunnar eða -línanna breytist í **Sent**.  

## <a name="view-and-approve-time-sheets-by-job"></a>Skoða og samþykkja vinnuskýrslur eftir vinnslu

Í verki er hægt að tilgreina manneskju sem ber ábyrgð á verkinu. Þær upplýsingar eru tengdar við tímablaðslínur. Hlekkurinn gefur verkefnisstjórum lista yfir vinnuskýrslur sem á að samþykkja. Sem dæmi má nefna að Verkstjóri teymisins gæti verið ábyrgur fyrir ákveðnum störfum í fyrirtækinu. Í því tilviki ætti deildarstjóri að vera tilnefndur sem  **Ábyrgðarmaður**  á síðunni starfakort. Þessi yfirlit upplýsinga í tímablaði sýnir verkhluta sem tengjast verki og þeim tímafjölda sem er notaður.

> [!NOTE]
> Til að samþykkja vinnuskýrslur á  **vinnublaði stjórnanda eftir vinnslusíðu**  þarf fyrst að velja  **vinnuskýrslur eftir verksamþykkjvalkostinn**  á  **síðunni Uppsetning**  forða. Til að fræðast meira um uppsetningu á samþykktum fyrir forða er farið í að  [Setja upp tilföng](projects-how-setup-resources.md).

### <a name="approve-or-reject-a-time-sheet-by-job"></a>Samþykkja eða hafna vinnublaði eftir vinnslu

1. Í reitinn **Leit** skal færa inn **Vinnuskýrsla stjórnanda** og velja síðan viðkomandi tengil. [!INCLUDE[prod_short](includes/prod_short.md)] birtir lista yfir vinnuskýrslulínur tengdar verkunum sem voru í ábyrgð notanda.
2. Veldu aðgerðina **Samþykkja** og síðan aðgerðina **Allar sendar línur** til að samþykkja allar línur eða aðgerðina **Aðeins valdar línur** til að samþykkja aðeins línurnar sem eru valdar á síðunni **Vinnuskýrsla**.

    > [!NOTE]
    > Aðeins er hægt að samþykkja vinnuskýrslur sem hafa stöðuna **Sent**.

3. Til að afla frekari upplýsinga um samþykkið eða höfnunina skal velja  **tengdu**  aðgerðina, síðan  **athugasemdir** og svo  **línuathugasemdir**.
4. Velja hnappinn **Í lagi**.

> [!NOTE]
> Þegar tímablaðslína hefur verið samþykkt eða henni hafnað eftir vinnslu er ekki hægt að opna hana á  **síðunni vinnublað** .

## <a name="post-time-sheet-lines-in-a-resource-journal"></a>Bóka línur í tímabókun í forðabók

Eftir að búið er að samþykkja vinnuskýrslufærslur fyrir forða, er hægt að bóka þær á viðeigandi forðabók.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Forðabækur** og velja síðan viðkomandi tengil.  
2. Veljið aðgerðina **Stinga upp á línum úr vinnuskýrslum**.  
3.  **Á síðunni leggja til línur**  á færslubók tilg., í reitina eftir þörfum. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] 
4. Velja hnappinn **Í lagi**. Færslur fyrir notkun eru stofnaðar í forðabókinni þar sem hægt er að breyta upplýsingunum eftir þörfum.  
5. Valið er **Bóka** aðgerðin.  
6. Til að staðfesta bókunina skal velja aðgerðina **Verkfærslur**. Síðan **Forðafærslur** opnast og birtir niðurstöður á bókun forðabókar.

## <a name="post-time-sheet-lines-in-a-job-journal"></a>Bóka línur tímablaðs í verkbók

Eftir að búið er að samþykkja vinnuskýrslufærslur fyrir verk, er hægt að bóka þær á viðeigandi verkbók.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verkbækur** og velja síðan viðkomandi tengil.  
2. Veljið aðgerðina **Stinga upp á línum úr vinnuskýrslum**.  
3. Á síðunni **Stinga upp á vinnubókarlínu** þarf að fylla reitina út eftir þörfum. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] 
4. Velja hnappinn **Í lagi**. Færslur fyrir notkun eru stofnaðar í verkbókinni þar sem hægt er að breyta upplýsingunum eftir þörfum.  

    > [!NOTE]  
    > Upplýsingar um tegund vinnu og hvort Reikningshæft verk sé afritað úr tímafærínslínunni. Ef þörf krefur er hægt að fækka klukkustundum og bóka að hluta. Ef magninu er fækkað, næst þegar valdar eru línur sem leggja á  **til í aðgerðinni tímablöð**, inniheldur línan eftirstandandi tímafjölda.  
5. Valið er **Bóka** aðgerðin.  
6. Til að staðfesta bókunina skal velja aðgerðina **Verkfærslur**. Síðan **Verkfærslur** opnast og birtir niðurstöður á bókun forðabókar.

## <a name="archive-time-sheets"></a>Til að færa vinnuskýrslur í safn

Eftir að vinnuskýrslur hafa verið bókaðar er hægt að safnvista þær til síðari viðmælanda. Bóka verður allar línur á vinnublaði áður en hægt er að safnvista þær.

> [!NOTE]  
> Þegar vinnuskjal er Skjalasafn er það fjarlægt af listunum á vinnublaðsíðum og  **í**  **tímablöðum**  stjórnanda.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnuskýrslur** og velja síðan viðkomandi tengil.
2. Veljið aðgerðina **Færa vinnuskýrslur í safn**  
3. Á síðunni **Færa vinnuskýrslur í safn** skal fylla út reitina eftir þörfum og velja síðan hnappinn **Í lagi**.  
4. Til að fara yfir vinnuskýrslur í safni skal velja ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnuskýrslusafn** eða **Vinnuskýrslusafn** verkstjóra og velja síðan viðkomandi tengil.

## <a name="see-also"></a>Sjá einnig .

[Verkefnastjórnun](projects-manage-projects.md)  
[Setja upp verkefnastjórnun](projects-setup-projects.md)  
[Fjármál](finance.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Sala](sales-manage-sales.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
