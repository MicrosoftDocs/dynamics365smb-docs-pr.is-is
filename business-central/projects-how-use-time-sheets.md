---
title: Nota vinnuskýrslur
description: 'Læra hvernig á að stofna, senda, samþykkja og bóka vinnuskýrslur fyrir forða, verk og þjónustu.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.search.keywords: 'project management, capacity, staff, resource, time sheets'
ms.search.form: '950, 951, 973'
ms.date: 02/05/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="use-time-sheets"></a>Nota vinnuskýrslur

Í þessari grein er því lýst hvernig á að nota vinnuskýrslur til að rekja fjarvistir og rekja tíma og tilföng sem eytt er í verkefni. Rakningartími auðveldar auðkenningu á vandamálum snemma og að koma í veg fyrir tafir eða yfirfærslur kostnaðar. Vinnuskýrslur auðvelda forða að tilkynna um tímanotkun fyrir einstakling eða vél svo að stjórnendur geti yfirfarið notkunina og úthlutun þess. 

Hægt er að afrita og nota verkáætlunarlínur í vinnuskýrslu. Með því móti þarf aðeins að færa upplýsingarnar inn á einum stað og línuupplýsingarnar eru alltaf réttar. Til að fræðast meira er farið í Til að [afrita verkáætlunarlínur í vinnuskýrslu](#copy-job-planning-lines-to-a-time-sheet).

Þegar búið er að samþykkja vinnuskýrslufærslur fyrir verk er hægt að bóka þær í viðeigandi verkbók eða forðabók. Til að fræðast meira er farið í Til að bóka vinnuskýrslulínur í verkbók [og](#post-time-sheet-lines-in-a-job-journal) Til að [bóka vinnuskýrslulínur í forðabók](#post-time-sheet-lines-in-a-resource-journal).

Áður en hægt er að nota vinnuskýrslur þarf að setja upp almennar upplýsingar og tilgreina stjórnanda og einn eða fleiri samþykkjendur vinnuskýrslna. Nánari upplýsingar um uppsetningu vinnuskýrslna eru í [Setja upp vinnuskýrslur](projects-how-setup-time-sheets.md).  

> [!TIP]
> Hægt er að nota vinnuskýrslur í farsíma. Til að gera það gæti þurft að kveikja á vífæringu nýrrar **vinnuskýrslu** á síðunni [Forðagrunnur](https://businesscentral.dynamics.com/?page=462) .

## <a name="create-time-sheets"></a>Stofna vinnuskýrslur

Hægt er að nota síðuna **Stofna vinnuskýrslur** til að setja upp vinnuskýrslur fyrir tiltekin tímabil eða vikur. Eigandi vinnuskýrslunnar getur síðan opnað hana og skráð tíma sem eytt er í verk. Einnig er hægt [tímasetja runuvinnsluna á að keyra sjálfkrafa](ui-work-report.md#ScheduleReport).  

> [!IMPORTANT]
> Notandi verður að hafa heimildir til að stofna vinnuskýrslur. Nánari upplýsingar um heimildir eru í [Setja upp vinnuskýrslur](projects-how-setup-time-sheets.md).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Stofna vinnuskýrslur** og velja síðan viðeigandi tengil.

    > [!TIP]
    > Einnig er hægt að nota aðgerðina **Stofna vinnuskýrslur** á listasíðunni **Forði** og á síðunni **Forðaspjald** .
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Áður en vinnuskýrslur eru stofnaðar fyrir forða þarf að ganga úr skugga um að **reitirnir Nota vinnuskýrslu** og **Notandakenni** eiganda vinnuskýrslu séu tilgreindir fyrir þá á **forðaspjaldssíðunni** .

    Valfrjálst er að velja **Tímasetningaraðgerð** til að tilgreina hversu oft eigi að keyra verkið sjálfvirkt. Til dæmis, til að grunnstilla **verkið þannig að það keyri vikulega í fjórar vikur, á síðunni** Tímasetja skýrslu - Stofna vinnuskýrslur **, í reitnum** Dagsetningarregla næstu keyrslu er fært inn **4V**. Nánari upplýsingar um tímasetningu skýrslna eru í [Áætlun skýrslu í Keyrslu.](ui-work-report.md#ScheduleReport)  

Hægt er að skoða vinnuskýrslurnar sem eru búnar til á síðunni **Vinnuskýrslur** . Hver vinnuskýrsla samanstendur af einni eða fleiri línum sem skilgreina tímann sem þú vilt til að senda inn til samþykkis. Eftirfarandi tafla lýsir gerðum lína sem hægt er að bæta við vinnuskýrsluna.

| **Reitur** | **Lýsing** |
|---|---|
| | Notið til að bæta við athugasemd eða merki í **lýsingarreitinn** á vinnuskýrslulínunni. Til dæmis má nota þennan reit til að flokka vinnuskýrslufærslur. Ef reiturinn **Tegund** er hafður auður fyrir vinnuskýrslulínu er ekki hægt að færa inn tímagildi í vikudagsreitina fyrir þá línu. |
| Fjarvist | Notaðu til að skrá tímann sem þú ert fjarverandi í vinnuviku. Til að ljúka upplýsingum fyrir línuna skal tilgreina gerð fjarvistar í reitinn **Ástæðukóði fjarvistar**. |
| Samsetningarpöntun | Notað til að skrá tíma fyrir samsetningarpantanir. Vinnuskýrslulína af þessari tegund er stofnuð við bókun samsetningarpantanalína sem forðinn er settur upp fyrir til að nota vinnuskýrslur. Ekki er hægt að velja línu af þessari tegund handvirkt. |
| Verk | Notið til að skrá tímanotkun fyrir verk. Til að ljúka upplýsingum fyrir línuna skal tilgreina verknúmer og verkhlutanúmer sem ská á tíma fyrir. Hægt er að skrá tíma fyrir línur sem ekki hafa verið áætlaðar.|
| Forði | Notið til að skrá tímanotkun fyrir forða. Til að ljúka upplýsingum fyrir línuna skal gefa upp lýsingu á verkinu. |
| Þjónusta | Notið til að skrá tímanotkun fyrir þjónustupöntun eða þjónustukreditreikning. |

Til dæmis er óskað eftir að senda vinnuskýrslu fyrir viku þar sem þrifin fóru fram og áttu frí í læknisfræði. Eftirfarandi tafla sýnir hvernig línum er bætt við vinnuskýrsluna.

| Gerð | Heimildasamstæða | Vinnutegundarkóði | Tegund fjarvistarkóða |
|--|--|--|--|
| Forði | Vinnutími | Þrif |  |
| Fjarvist | Frí |  | Heilsa |
|  | Ég þurfti að fara á þriðjudag vegna læknisfræðilegs erindis. |  |  |

Í þessu dæmi er hægt að skrá stundirnar á viðkomandi dögum fyrir hvern virkan dag.  

> [!TIP]
> Í flestum tilvikum verður fyrirtækið þitt með forskilgreindar vinnutegundir fyrir ýmsar línugerðir. Í þeim tilvikum velur þú bara viðeigandi vinnutegund af listanum og bætir svo við þinni eigin lýsingu.  
>
> Veldu vinnutegundina með því að velja hnappinn :::image type="icon" source="media/assist-edit-icon.png" border="false"::: í reitnum **Lýsing**, með því að velja aðgerðina **Upplýsingar um aðgerðir** og síðan tilgreina þær á síðunni sem opnast eða með því að velja þær í reitnum **Kóði vinnutegundar** eða í reitnum **Tegund fjarvistarkóða**. Í þessu tilfelli er hægt að hunsa [til að skilgreina tegundir vinnu og bæta einni við hluta vinnuskýrslu](#define-work-types-and-add-one-to-a-time-sheet) .  

## <a name="reuse-time-sheet-lines-in-other-time-sheets"></a>Endurnota vinnuskýrslulínur í öðrum vinnuskýrslum

Ef upplýsingar vinnuskýrslunnar eru þær sömu frá tímabili til tímabils, afrita línurnar frá fyrra tímabili til að spara tíma. Færið þá inn tímanotkun fyrir nýja tímabilið.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnuskýrslur** og velja síðan viðkomandi tengil.  
2. Opnið vinnuskýrsluna fyrir tímabil sem er síðar en tímabilið fyrir fyrirliggjandi vinnuskýrslu með línum.  
3. Veljið aðgerðina **Afrita línur úr fyrri vinnuskýrslu**.

Línurnar eru afritaðar, með upplýsingum eins og gerð og lýsingu. Til dæmis, ef línurnar eru tengdar við starf, er **Verk nr.** afritað. Allar afritað línur eru með stöðuna **Opna**. Þá er hægt að breyta línunum eftir þörfum.

## <a name="copy-project-planning-lines-to-a-time-sheet"></a>Afrita verkáætlunarlínur í vinnuskýrslu

Eftirfarandi ferli lýsir því hvernig eigi að flýtistofna verkáætlunarlínur á vinnuskýrslu.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnuskýrslur** og velja síðan viðkomandi tengil.  
2. Á síðunni **Vinnuskýrslur** skal velja vinnuskýrslu fyrir viðeigandi tímabil.  
3. Veljið aðgerðina **Stofna línur úr verkáætlun**. Allar verkáætlunarlínur í tímabili vinnublaðsins eru afritaðar í vinnublaðið fyrir manneskjuna eða vélina í **Tilfang nr.** reitinn á vinnublaðsins.

## <a name="define-work-types-and-add-one-to-a-time-sheet"></a>Skilgreina tegundir vinnu og bæta einni við vinnuskýrslu

Hægt er að skilgreina tegund vinnu fyrir allar vinnuskýrslulínur fyrir þjónustupantanir, verkpantanir og forða. Með þeim hætti er hægt að bæta við upplýsingum sem þarf til að rukka viðskiptavininn og fyrir mismunandi tegundir af vinnu.  

1. Á síðunni **Vinnuskýrslur** skal velja viðeigandi vinnuskýrslu.
2. Í fyrstu línunum í hlutanum **Línur** skal velja reitinn **Gerð** og síðan velja viðeigandi gerð eins og *Tilfang*.  
3. Veldu reitinn **Lýsing** og síðan á síðunni **Upplýsingar um tilfang vinnuskýrslulínu** skal fylla út reitina. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
    1. Ef engar tegundir vinnu eru til skal velja aðgerðina **Nýtt** .
    2. Á síðunni **Vinnutegundir** skal fylla út reitina eftir þörfum og síðan fara aftur í vinnuskýrsluna.
4. Fylltu út það sem eftir er af vinnuskýrslunni. Nánari upplýsingar eru í [Til að fylla út vinnuskýrslulínur og senda til samþykktarhluta](#fill-in-time-sheet-lines-and-submit-for-approval) .  

> [!TIP]
> Hægt er að fylgja svipuðum skrefum til að skilgreina fjarvistarkóta.

## <a name="fill-in-time-sheet-lines-and-submit-for-approval"></a>Fylla út vinnuskýrslulínur og senda til samþykktar

Vinnuskýrsluskráning er rakin í klukkustundum, sem er stöðluð grunnmælieining fyrir forða. Sjálfgefið er að vinnuskýrsla sýni sameiginlega vinnudaga frá mánudegi til föstudags.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnuskýrslur** og velja síðan viðkomandi tengil.  
2. Veljið vinnuskýrslu fyrir viðeigandi tímabili.
3. Fyllið í reitina í línu eins og þörf krefur. Færið inn fjölda stunda sem forðinn notar hvern dag vikunnar.  

    Í flestum tilfellum, til að rekja vinnu, er línu af tegundinni *Forði* bætt við og stundum síðan eytt á hverjum degi. Ef skrá á fjarvistir er línu af tegundinni *Fjarvist* bætt við.  

    > [!TIP]  
    > Hægt er að fara yfir samtölu vinnuskýrslustunda sem færðar eru inn í upplýsingakassann **Raunverulegt/Áætlað samantekt** .  
4. Endurtakið skref 3 fyrir aðrar tegundir vinnu sem forðinn innir af hendi.  

    Næst skal ákveða hvort senda eigi alla eða valdar línur á vinnuskýrslunni.  

    * Til að senda inn vinnuskýrsluna fyrir eina eða fleiri línur skaltu velja viðeigandi línu og síðan velja aðgerðina **Senda inn**.

        Á síðunni Sending skal velja aðeins **valkostinn** Valdar línur. Staða línunnar breytist úr **Opið** í **Sent**.
    * Til að senda inn vinnuskýrslu fyrir allar opnar línur skal velja aðgerðina **Senda inn** efst á síðunni **Vinnuskýrsla**.  

        Staðfesta þarf að senda eigi allar opnar línur á gildandi vinnuskýrslu.  

    > [!NOTE]  
    > Aðeins er hægt að senda tímaskýrslulínur sem innihalda skráðan tíma.  
5. Til að breyta upplýsingum í línu sem hefur verið stillt á **Sent** skal velja línu og velja svo aðgerðina **Enduropna**.

    > [!NOTE]  
    > Yfirmaður gæti hafnað vinnuskýrslulínu sem send er til samþykktar. Ef lína hefur stöðuna **Hafnað** er hægt að gera breytingar í línunni og velja **Senda** aftur.  
6. Velja hnappinn **Í lagi**.

## <a name="approve-or-reject-a-time-sheet"></a>Samþykkja eða hafna vinnuskýrslu

Senda þarf vinnuskýrslu til samþykkis áður en hægt er að nota hana. Hægt er að samþykkja og hafna einstökum línum á vinnuskýrslu eða senda þær aftur til sendandans. Vinnuskýrslur eru samþykktar á tvo vegu:

* Vinnuskýrslustjóri getur samþykkt allar vinnuskýrslur.
* Einstaklingurinn sem er tilgreindur í reitnum **Notandakenni samþykkjanda vinnuskýrslu** á forðaspjaldi getur samþykkt vinnuskýrslur viðkomandi forða. Nánari upplýsingar um uppsetningu samþykktar eru í [Setja upp vinnuskýrslur](projects-how-setup-time-sheets.md).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnuskýrslur verkstjóra** og velja síðan viðkomandi tengil.
2. Veljið vinnuskýrslu úr listanum.  
3. Á síðunni **Vinnuskýrslur** : 
    1. Velja aðgerðina **Vinna** og svo aðgerðina **Samþykkja**.
    2. Veljið aðgerðina **Allar sendar línur** til að samþykkja allar línur eða aðgerðina **Aðeins valdar línur** til að samþykkja aðeins línurnar sem eru valdar á síðunni **Vinnuskýrsla**.
4. Velja hnappinn **Í lagi**.  
5. Einnig er hægt að velja aðgerðina **Hafna** og fylgja skrefum 4 til 5.  

> [!TIP]  
> Nota skal upplýsingakassana **Staða vinnuskýrslu** og **Samantekt fyrir rauntíma/áætlaðan tíma** til að fá yfirlit yfir upplýsingar vinnuskýrsla.

Þegar búið er að samþykkja eða hafna vinnuskýrslu er ekki hægt að breyta henni nema hún sé fyrst opnuð aftur. Eftirfarandi ferli lýsir því hvernig á að enduropna vinnuskýrslu sem hefur verið samþykkt eða hafnað.

## <a name="reopen-a-time-sheet"></a>Opna vinnuskýrslu aftur

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnuskýrslur verkstjóra** eða **Vinnuskýrslur** og velja síðan viðkomandi tengil.
2. Opnið vinnuskýrslu úr listanum.  

    > [!NOTE]  
    > Aðeins er hægt að enduropna línur með stöðuna **Samþykkt**. Ekki er hægt að enduropna línur með stöðuna **Hafnað** eða sem eru bókaðar.  
3. Á síðunni **Vinnuskýrsla** skal velja aðgerðina **Enduropna** og velja svo aðgerðina **Allar sendar línur til að enduropna allar línur** eða aðgerðina **Valdar línur** til að enduropna aðeins línurnar sem valdar eru á síðunni **Vinnuskýrsla** .
4. Velja hnappinn **Í lagi**. Staða vinnuskýrslulínunnar eða -línanna breytist í **Sent**.  

## <a name="view-and-approve-time-sheets-by-project"></a>Skoða og samþykkja vinnuskýrslur eftir verki

Í verki er hægt að tilgreina manneskju sem ber ábyrgð á verkinu. Upplýsingarnar eru tengdar vinnuskýrslulínum. Tengillinn gefur verkefnastjórum lista yfir vinnuskýrslur sem á að samþykkja. Til dæmis gæti verkefnastjóri teymisins verið ábyrgur fyrir ákveðnum störfum í fyrirtækinu. Í því tilviki á yfirmaðurinn að vera sá sem **ber ábyrgð** á síðunni Verkspjald. Þessi yfirlit yfir upplýsingar vinnuskýrslu sýnir verkhluta sem tengjast verki og fjölda stunda sem notaður er.

> [!NOTE]
> Til að samþykkja vinnuskýrslur á síðunni **Vinnuskýrslu stjórnanda eftir verki** þarf fyrst að velja **vinnuskýrslu með valkostinum Verksamþykkt** á síðunni **Forðagrunnur** . Til að fræðast um hvernig setja á upp samþykktir fyrir forða er farið í [Setja upp forða](projects-how-setup-resources.md).

### <a name="approve-or-reject-a-time-sheet-by-project"></a>Samþykkja eða hafna vinnuskýrslu eftir verki

1. Í reitinn **Leit** skal færa inn **Vinnuskýrsla stjórnanda** og velja síðan viðkomandi tengil. [!INCLUDE[prod_short](includes/prod_short.md)] birtir lista yfir vinnuskýrslulínur sem tengjast verkum sem notandi ber ábyrgð á.
2. Veldu aðgerðina **Samþykkja** og síðan aðgerðina **Allar sendar línur** til að samþykkja allar línur eða aðgerðina **Aðeins valdar línur** til að samþykkja aðeins línurnar sem eru valdar á síðunni **Vinnuskýrsla**.

    > [!NOTE]
    > Aðeins er hægt að samþykkja vinnuskýrslur með stöðuna **Sent**.

3. Til að veita viðbótarupplýsingar um samþykkt eða höfnun skal velja aðgerðina **Tengdar**, síðan **Athugasemdir** og síðan **Línuathugasemdir**.
4. Velja hnappinn **Í lagi**.

> [!NOTE]
> Þegar búið er að samþykkja eða hafna vinnuskýrslulínu fyrir verk er ekki hægt að enduropna eða breyta henni á **vinnuskýrslusíðunni** .

## <a name="post-time-sheet-lines-in-a-resource-journal"></a>Bóka vinnuskýrslulínur í forðabók

Eftir að búið er að samþykkja vinnuskýrslufærslur fyrir forða, er hægt að bóka þær á viðeigandi forðabók.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Forðabækur** og velja síðan viðkomandi tengil.  
2. Veljið aðgerðina **Stinga upp á línum úr vinnuskýrslum**.  
3. Á síðunni **Tillaga forðabókarlínur** skal í reitunum eins og þörf krefur. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] 
4. Velja hnappinn **Í lagi**. Færslur fyrir notkun eru stofnaðar í forðabókinni þar sem hægt er að breyta upplýsingunum eftir þörfum.  
5. Valið er **Bóka** aðgerðin.  
6. Til að staðfesta bókunina skal velja aðgerðina **Verkfærslur**. Síðan **Forðafærslur** opnast og sýnir niðurstöður bókunar forðabókarinnar.

## <a name="post-time-sheet-lines-in-a-project-journal"></a>Bóka vinnuskýrslulínur í verkbók

Eftir að búið er að samþykkja vinnuskýrslufærslur fyrir verk, er hægt að bóka þær á viðeigandi verkbók.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verkbækur** og velja síðan viðkomandi tengil.  
2. Veljið aðgerðina **Stinga upp á línum úr vinnuskýrslum**.  
3. Á síðunni **Stinga upp á vinnubókarlínu** þarf að fylla reitina út eftir þörfum. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] 
4. Velja hnappinn **Í lagi**. Færslur fyrir notkun eru stofnaðar í verkbókinni þar sem hægt er að breyta upplýsingunum eftir þörfum.  

    > [!NOTE]  
    > Upplýsingar um tegund vinnu og hvort vinnan er reikningshæf eru afrituð úr vinnuskýrslulínunni. Ef þörf krefur er hægt að fækka klukkustundum og bóka að hluta. Ef magnið er minnkað næst þegar aðgerðin **Leggja til línur úr vinnuskýrslum** er valin inniheldur línan það fjölda stunda sem eftir er.  
5. Valið er **Bóka** aðgerðin.  
6. Til að staðfesta bókunina skal velja aðgerðina **Verkfærslur**. Síðan **Verkfærslur** opnast og birtir niðurstöður á bókun forðabókar.

## <a name="archive-time-sheets"></a>Vinnuskýrslur í skjalasafni

Þegar vinnuskýrslur hafa verið bókaðar er hægt að geyma þær til framtíðar. Bóka verður allar línur á vinnuskýrslu áður en hægt er að geyma hana.

> [!NOTE]  
> Þegar vinnuskýrsla er sett í geymslu er hún fjarlægð úr listunum á síðunum **Vinnuskýrslur**  **og** Verkefnastjóri.

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
