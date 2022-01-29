---
title: Nota vinnuskýrslur
description: Lýsir því hvernig stofna á vinnuskjal, skilgreina vinnugerðir, fylla út vinnublaðið og senda það til samþykkis.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource, time sheets
ms.search.form: 950, 951, 973
ms.date: 12/13/2021
ms.author: edupont
ms.openlocfilehash: bd163b5e8c4d96a28a1dd557d53b04dafe6829fd
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/14/2022
ms.locfileid: "7973126"
---
# <a name="use-time-sheets"></a>Nota vinnuskýrslur

Hægt er að nota vinnuskýrslur [!INCLUDE [prod_short](includes/prod_short.md)] til að rekja fjarvistir og til að rekja tíma og tilföng sem er varið í verk. Með tímastjórnun er hægt að auðkenna mál snemma og forðast tafir eða kostnað við útkeyrslur. Með vinnuskýrslum getur forði auðveldlega tilkynnt tímanotkun fyrir einstakling eða vél og getur stjórnandi auðveldlega farið yfir notkunina og úthlutun hennar. Í greininni er fjallað um hvernig stofna skal vinnuskjal, skilgreina vinnugerðir, fylla út vinnublaðið og senda það til samþykkis.  

Hægt er að afrita og nota verkáætlunarlínur í vinnuskýrslu. Með því móti þarf aðeins að færa upplýsingarnar inn á einum stað og línuupplýsingarnar eru alltaf réttar.

Eftir að búið er að samþykkja vinnuskýrslufærslur fyrir verk er hægt að bóka þær á viðeigandi verkbók eða forðabók.

Áður en hægt er að nota vinnuskýrslur þarf að setja upp almennar upplýsingar og tilgreina stjórnanda og einn eða fleiri samþykkjendur vinnuskýrslna. Frekari upplýsingar eru í [Setja upp vinnuskýrslur](projects-how-setup-time-sheets.md).  

> [!TIP]
> Frá og með 2021 útgáfutímabili 2 er hægt að stjórna úthlutuðum vinnuskýrslum í fartæki. Stjórnandinn þinn gæti samt sem áður þurft að virkja eiginleikann **Eiginleikauppfærsla: Ný upplifun fyrir vinnuskýrslu** á síðu [Eiginleikastjórnunar](https://businesscentral.dynamics.com/?page=2610) til að nota þennan möguleika. Frekari upplýsingar eru í [Setja upp vinnuskýrslur](projects-how-setup-time-sheets.md).

## <a name="to-create-time-sheets"></a>Til að stofna vinnuskýrslur

Hægt er að nota keyrsluna **Stofna vinnuskýrslur** til að setja upp vinnuskýrslur fyrir tilgreindan fjölda tímabila eða vikna. Eigandi vinnuskýrslunnar getur þá opnað hana og skráð tíma sem eytt hefur verið í verk.  

> [!IMPORTANT]
> Notandi verður að hafa heimildir til að hægt sé að búa til vinnuskýrslur. Frekari upplýsingar eru í [Setja upp vinnuskýrslur](projects-how-setup-time-sheets.md).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnuskýrslur** og velja síðan viðkomandi tengil.
2. Á **síðunni tímablöð** skal velja **aðgerðina stofna vinnuskýrslur**.
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Reitirnir **Nota vinnuskýrslu** og **Notandakenni eiganda vinnuskýrslu** verða að vera fylltir út á spjaldinu fyrir forða vinnuskýrslunnar.
4. Velja hnappinn **Í lagi**.  

Hægt er að skoða þau vinnublöð sem eru búin til á **síðunni tímablöð**. Hvert vinnublað er samsett úr einni eða fleiri línum sem skilgreinir tímann sem á að senda til samþykkis. Eftirfarandi tafla lýsir gerðum lína sem hægt er að bæta við vinnublaðið.

| **Sviði** | **Lýsing** |
|---|---|
| | Notið til að bæta athugasemd eða merki í **reitnum Lýsing í** tímablaðslínunni. Til dæmis er hægt að nota þennan reit til að flokka færslur í tímafærslum. Ef **reiturinn Tegund er hafður** auður fyrir tímablaðslínu er ekki hægt að færa inn tímavirði í reitina vikudagur fyrir þá línu. |
| Fjarveru | Notaðu til að skrá tímann sem þú ert fjarverandi í vinnuviku. Til að ljúka upplýsingum fyrir línuna þarf að tilgreina tegund fjarvista í **reitnum Kóti Fjarvistafóði**. |
| Samsetningarpöntun | Notað til að skrá tíma fyrir samsetningarpantanir. Tímablaðslína af þessari gerð er stofnuð við bókun samsetningarpöntunarlína sem tilfang er sett upp fyrir til að nota vinnuskýrslur. Ekki er hægt að velja línu handvirkt af þessari gerð. |
| Vinnsla | Nota til að skrá tímanotkun fyrir verk. Til að ljúka upplýsingum fyrir línuna þarf að tilgreina verknúmerið og númer verkverksins sem á að skrá tíma. Hægt er að skrá tíma fyrir línur sem ekki hefur verið raðað.|
| Forði | Notið til að skrá tímanotkun á forða. Til að ljúka við upplýsingar fyrir línuna skal gefa upp lýsingu á vinnunni. |
| Þjónusta | Notið til að skrá tímanotkun fyrir þjónustupöntun eða þjónustukreditreikning. |

Til dæmis að senda inn vinnublað fyrir vinnuviku þar sem unnið var að hreinsunarverkefnum flesta daga en hafði einn daginn slökkt á erindum, bætt var við línum sem Sýnidæmi í eftirfarandi töflu.

| Tegund | Description | Kóti vinnutegundar | Kóti fjarvistategða |
|--|--|--|--|
| Forði | Vinnustundum | Þrif |  |
| Fjarveru | Skipti um |  | Heilsu |
|  | Ég þurfti að taka Þriðjudagsnámskeið vegna læknierinda. |  |  |

Í þessu lágværa dæmi væri svo hægt að skrá viðkomandi tíma yfir viðkomandi daga á svæðunum fyrir hvern virkan dag.  

> [!TIP]
> Í flestum tilvikum mun fyrirtækið hafa fyrirframskilgreindar vinnugerðir fyrir ýmsar gerðir lína. Í þeim tilfellum velur þú bara viðkomandi tegund vinnu af listanum og svo bætir þú við þinni eigin lýsingu.  
>
> Tegund vinnu er valin með því að velja :::image type="icon" source="media/assist-edit-icon.png" border="false"::: hnappinn í **reitnum Lýsing með því að** Velja **aðgerðina verkþáttarupplýsingar** og tilgreina hana síðan í síðunni sem opnast eða með því að velja hana í **reitnum Kóti vinnutegundar** eða reitnum **Kóti fjarvistar**. Í þessu tilfelli er hægt að hunsa [til að skilgreina vinnugerðir og bæta einu við](#to-define-work-types-and-add-one-to-a-time-sheet) vinnublaðshluta.  

## <a name="to-reuse-time-sheet-lines-in-other-time-sheets"></a>Til að endurnýta vinnuskýrslulínur í öðrum vinnuskýrslum

Ef upplýsingar tímablaðs haldast óbreyttar á milli tímabila má spara tíma með því að afrita línur úr fyrra tímabili. Síðan er tímanotkunin fyrir nýja tímabilið færð inn.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnuskýrslur** og velja síðan viðkomandi tengil.  
2. Opnið vinnuskýrsluna fyrir tímabil sem er síðar en tímabilið fyrir fyrirliggjandi vinnuskýrslu með línum.  
3. Veljið aðgerðina **Afrita línur úr fyrri vinnuskýrslu**.

Línurnar eru afritaðar, með upplýsingum eins og gerð og lýsingu. Til dæmis, ef línurnar eru tengdar við starf, er **Verk nr.** afritað. Allar afritað línur eru með stöðuna **Opna**. Þá er hægt að breyta línunum eftir þörfum.

## <a name="to-copy-job-planning-lines-to-a-time-sheet"></a>Til að afrita áætlunarlínur verks á vinnuskýrslu
Eftirfarandi ferli lýsir því hvernig eigi að flýtistofna verkáætlunarlínur á vinnuskýrslu.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnuskýrslur** og velja síðan viðkomandi tengil.  
2. Á **síðunni tímablöð** skal velja vinnuskýrslur fyrir viðkomandi tímabil.  
3. Veljið aðgerðina **Stofna línur úr verkáætlun**. Allar verkáætlunarlínur í tímabili vinnublaðsins eru afritaðar í vinnublaðið fyrir manneskjuna eða vélina í **Tilfang nr.** reitinn á vinnublaðsins.

## <a name="to-define-work-types-and-add-one-to-a-time-sheet"></a>Til að skilgreina tegundir vinnu og bæta tegund vinnu við vinnuskýrslu

Hægt er að skilgreina vinnugerðina fyrir allar tímalínur fyrir þjónustupantanir, starfspantanir og forða. Með þeim hætti er hægt að bæta við upplýsingum sem þarf til að rukka viðskiptavininn og fyrir mismunandi tegundir af vinnu.  

1. Í **síðunni tímablöð** skal velja viðkomandi vinnuskýrslur.
2. Í fyrstu línunum í **hlutanum** línur er **reiturinn Tegund valinn** og viðeigandi gerð er valin, eins og til dæmis *Forði*.  
3. **Reiturinn** Lýsing er valinn og í **síðunni upplýsingar um forða í tímablaði** er fyllt út í reitina. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
    1. Ef engin tegund vinnu er til skal velja aðgerðina **Nýtt**.
    2. Á **síðunni Vinnugerðir** eru reitirnir fylltir út eftir þörfum og síðan er snúið aftur til vinnublaðsins.
4. Fyllið út restina af vinnublaðinu. Sjá [til að fylla út vinnubókarlínur og senda inn fyrir samþykktarhlutann til að fá frekari upplýsingar](#to-fill-in-time-sheet-lines-and-submit-for-approval).  

> [!TIP]
> Svipaðar ráðstafanir gilda um skilgreiningu fjarvistarkóða.

## <a name="to-fill-in-time-sheet-lines-and-submit-for-approval"></a>Til að fylla út vinnuskýrslulínur og senda til samþykktar

Vinnuskýrsluskráning er rakin í klukkustundum, sem er stöðluð grunnmælieining fyrir forða. Sjálfgefið er að vinnuskýrsla sýni sameiginlega vinnudaga frá mánudegi til föstudags.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnuskýrslur** og velja síðan viðkomandi tengil.  
2. Veljið vinnuskýrslu fyrir viðeigandi tímabili.
3. Fyllið í reitina í línu eins og þörf krefur. Færið inn fjölda stunda sem forðinn notar hvern dag vikunnar.  

    Í flestum tilfellum, til að fylgjast með vinnu, er bætt við *forðagæingu* og síðan er klukkustundum eytt í dag. Ef skrá á fjarvist er bætt við línu af gerðinni *fjarvist*.  

    > [!TIP]  
    > Hægt er að fara yfir samtölu tímaskýrslustunda sem settar hafa verið inn í upplýsingakassann **Rauntími/áætlaður tími samantekt**  
4. Endurtakið skref 3 fyrir aðrar tegundir vinnu sem forðinn innir af hendi.  

    Næst þarf að ákveða hvort senda eigi allar línur á vinnublaðinu eða hvort senda eigi inn einstakar línur.  

    * Til að senda vinnublaðið fyrir eina eða fleiri línur skal velja viðkomandi línu og velja síðan **senda** aðgerðina.

        Velja **aðeins valkostinn línur á innsendingarsíðu**. Línan breytir stöðu úr *opin* yfir í *innsend*.
    * Til að senda vinnublaðið fyrir allar opnar línur skal velja **senda** aðgerðina efst á **síðu vinnublaðs**.  

        Þú munt vera beðinn um að staðfesta að þú viljir senda allar opnu línurnar í gildandi vinnublaði.  

    > [!NOTE]  
    > Aðeins er hægt að senda tímaskýrslulínur sem innihalda skráðan tíma.  
5. Til að breyta upplýsingum í línu sem hefur verið stillt á **Sent** skal velja línu og velja svo aðgerðina **Enduropna**.

    > [!NOTE]  
    >   Stundum gæti stjórnandi hafnað tímaskýrslulínu sem lögð er fram til samþykktar. Ef lína hefur stöðuna **Hafnað** er hægt að gera breytingar í línunni og velja **Senda** aftur.  
6. Velja hnappinn **Í lagi**.

## <a name="to-approve-or-reject-a-time-sheet"></a>Til að samþykkja eða hafna vinnuskýrslu
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

## <a name="to-reopen-a-time-sheet"></a>Til að enduropna vinnuskýrslu
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnuskýrslur verkstjóra** eða **Vinnuskýrslur** og velja síðan viðkomandi tengil.
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

1. Í reitinn **Leit** skal færa inn **Vinnuskýrsla stjórnanda** og velja síðan viðkomandi tengil. [!INCLUDE[prod_short](includes/prod_short.md)] birtir lista yfir vinnuskýrslulínur tengdar verkunum sem voru í ábyrgð notanda.
2. Veldu aðgerðina **Samþykkja** og síðan aðgerðina **Allar sendar línur** til að samþykkja allar línur eða aðgerðina **Aðeins valdar línur** til að samþykkja aðeins línurnar sem eru valdar á síðunni **Vinnuskýrsla**.

    > [!NOTE]
    > Aðeins er hægt að samþykkja vinnuskýrslur sem hafa stöðuna **Sent**.

3. Til að veita frekari upplýsingar um samþykki eða höfnun skal velja aðgerðina **Tengt** og svo **Athugasemdir** og síðan **Línuathugasemdir** og setja inn athugasemdir.
4. Velja hnappinn **Í lagi**.

> [!NOTE]
> Þegar búið er að samþykkja eða hafna vinnuskýrslulínu eftir verki er ekki hægt að enduropna eða breyta þeim í glugganum **Vinnuskýrsla**.

## <a name="to-post-time-sheet-lines-in-a-resource-journal"></a>Til að bóka vinnuskýrslulínur í forðabók
Eftir að búið er að samþykkja vinnuskýrslufærslur fyrir forða, er hægt að bóka þær á viðeigandi forðabók.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Forðabækur** og velja síðan viðkomandi tengil.  
2. Veljið aðgerðina **Stinga upp á línum úr vinnuskýrslum**.  
3. Á síðunni **Stinga upp á forðabókarlínum**, í reitina eftir því sem þörf krefur.  
4. Velja hnappinn **Í lagi**. Færslur fyrir notkun eru stofnaðar í forðabókinni þar sem hægt er að breyta upplýsingunum eftir þörfum.  
5. Valið er **Bóka** aðgerðin.  
6. Til að staðfesta bókunina skal velja aðgerðina **Verkfærslur**. Síðan **Forðafærslur** opnast og birtir niðurstöður á bókun forðabókar.

## <a name="to-post-time-sheet-lines-in-a-job-journal"></a>Til að bóka vinnuskýrslulínur í verkbók
Eftir að búið er að samþykkja vinnuskýrslufærslur fyrir verk, er hægt að bóka þær á viðeigandi verkbók.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verkbækur** og velja síðan viðkomandi tengil.  
2. Veljið aðgerðina **Stinga upp á línum úr vinnuskýrslum**.  
3. Á síðunni **Stinga upp á vinnubókarlínu** þarf að fylla reitina út eftir þörfum.  
4. Velja hnappinn **Í lagi**. Færslur fyrir notkun eru stofnaðar í verkbókinni þar sem hægt er að breyta upplýsingunum eftir þörfum.  

    > [!NOTE]  
    >   Upplýsingar um tegund verks og hvort verkið er reikningshæft eru afritaðar úr vinnuskýrslulínu. Ef þörf krefur er hægt að fækka klukkustundum og bóka að hluta. Ef magnið er minnkað mun línan sem stofnuð er innihalda eftirstandandi klukkustundir næst þegar aðgerðin **Stinga upp á línum úr vinnuskýrslum** er valin.  
5. Valið er **Bóka** aðgerðin.  
6. Til að staðfesta bókunina skal velja aðgerðina **Verkfærslur**. Síðan **Verkfærslur** opnast og birtir niðurstöður á bókun forðabókar.

## <a name="to-archive-time-sheets"></a>Til að færa vinnuskýrslur í safn
Þegar búið er að bóka vinnuskýrslu, er hægt að safna þeim fyrir seinni tíma tilvísun. Bóka þarf allar vinnuskýrslulínur áður en hægt er að færa vinnuskýrslu í skjalasafn.

> [!NOTE]  
>   Þegar vinnuskýrsla er sett í safn er hún fjarlægð úr listunum á síðunni **Vinnuskýrslur** og síðunni **Vinnuskýrsla stjórnanda**.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnuskýrslur** og velja síðan viðkomandi tengil.
2. Veljið aðgerðina **Færa vinnuskýrslur í safn**  
3. Á síðunni **Færa vinnuskýrslur í safn** skal fylla út reitina eftir þörfum og velja síðan hnappinn **Í lagi**.  
4. Til að fara yfir eldri vinnuskýrslur skal velja þá ![ljósaperu sem opnar aðgerðina segja.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnuskýrslusafn** eða **Vinnuskýrslusafn** verkstjóra og velja síðan viðkomandi tengil.

## <a name="see-also"></a>Sjá einnig
[Verkefnastjórnun](projects-manage-projects.md)  
[Setja upp verkefnastjórnun](projects-setup-projects.md)  
[Fjármál](finance.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Sala](sales-manage-sales.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]