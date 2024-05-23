---
title: Stofna verkspjald fyrir verk og tilgreina verk
description: Fyrir nýtt verkefni er stofnað verkspjald sem inniheldur verkhluta og áætlunarlínur til að aðstoða við stjórnun framvindu og fjárhagsáætlana.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'project management, task'
ms.search.form: '88, 275, 276, 1001, 1002, 1003, 1004, 1005, 1006, 1007, 1020'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="create-projects"></a>Stofna verk

Þegar nýtt verk er hafið þarf að stofna verkspjald með samþættum verkhlutum og verkáætlunarlínum, sem skipt er upp í tvennu lagi.  

Fyrsta lagið samanstendur af verkhlutum. Stofna verður að minnsta kosti einn verkhluta fyrir hvert verk þar sem öll bókun vísar til verkhluta. Ef a.m.k. einn verkhluti er í verkefninu er hægt að setja upp áætlunarlínur verks og bóka notkun í verkið.

Annað lag samanstendur af verkáætlunarlínum þar sem tilgreind er nákvæm notkun forða, vara og ýmis fjárhagsleg útgjöld.

Lagskiptingin gerir kleift að skipta verkefninu í smærri verk og notast við ítarlegri upplýsingar um fjárhagsáætlun, tilboð og skráningu. Þar að auki veitir það innsýn í framvindu verkefnisins. Til dæmis er hægt að rekja hvort notandinn nái tilskildum áföngum, eða hvort hann sé á réttri leið til að ná væntingum áætlunar.

> [!TIP]
> Velja skal aðgerðina **Nýtt verkefni** í **Hlutverkamiðstöð verkefnastjóra** til að opna leiðsagnarforrit með aðstoð sem fer í gegnum skrefin til að stofna verkefni með samþættum verkum og áætlunarlínum. Eftirfarandi ferli sýnir hvernig á að framkvæma skrefin handvirkt. <!-- For an example of how to create a project manually, go to [Video: How to create a project in Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw).-->

## <a name="invoice-one-or-more-customers-for-project-tasks"></a>Reikningsfæra einn eða fleiri viðskiptavini fyrir verkhluta

Stundum er sá aðili sem fær þjónustu annað en sá aðili sem borgar reikninginn. Stundum gæti einnig þurft að reikningsfæra marga viðskiptamenn fyrir verk í verkefninu. Á síðunni **Verkspjald** er reiturinn **Reikningsaðferð verkhluta notaður** til að tilgreina hvort verið er að reikningsfæra einn viðskiptamann eða marga viðskiptamenn.

Ef viðskiptamaðurinn sem fær þjónustuna greiðir einnig reikninginn skal velja **Sjálfgefið (viðskiptamaður)** og Sjálfgefið (Selt-til **aðsetur)**  í reitunum **Reikningsfært á og**  **Sendist-til**.

Ef þú ert að reikningsfæra marga viðskiptamenn er hægt að tilgreina viðskiptamanninn sem fær þjónustuna og viðskiptamanninn sem á að reikningsfæra fyrir hvern verkhluta í verkefninu. Einnig er hægt að útvega eftirfarandi upplýsingar:

* Þar sem vinnan mun gerast með því að velja úr lista yfir sendist til aðsetur fyrir viðskiptamanninn.
* Bæta við upplýsingum um ytri tilvísanir til að einfalda samskipti um verkefnið.
* Skrifaðu yfir stöðluðu fjármálaskilmála verksins.

## <a name="invoice-one-customer-for-multiple-project-tasks"></a>Reikningsfæra einn viðskiptavin fyrir mörg verk

Hægt er að einfalda reikningsfærsluferlið með því að senda einn reikning til viðskiptavinar fyrir mörg verkefni. Bæta verkáætlunarlínum úr mörgum verkum við sölureikning í einu tilviki. Þetta ferli svipar til þess að stofna sölureikning úr verkáætlunarlínu og færa inn gildi í **Tengja við sölureikningsnr.** Ef reiturinn er auður er

Hér er yfirlit yfir ferlið.

1. Nýr sölureikningur er búinn til og reiturinn **Selt-til viðskm.nr. fylltur út.** . Ef þörf krefur er reiturinn **Reikn.færist á viðskm. einnig fylltur út.** og **Gjaldmiðilskóti** .
2. Á flýtiflipanum **Línur** skal velja aðgerðina **Sækja áætlunarlínur verkefnis** . Síðan **Sækja verkáætlunarlínur** sýnir reikningshæfar verkáætlunarlínur úr verkefnum fyrir viðskiptamann sem selt er til, reikningsfærsluviðskiptamanninum og reikningsfærslugjaldmiðli þar sem magnið sem á að reikningsfæra er meira en núll. 
3. Línurnar sem á að bæta við reikninginn eru velja **Í lagi**.

Þessi þrep eru endurtekin ef bæta á við öðru safni af áætlunarlínum verks. Einnig er hægt að eyða reikningnum eða línunum og byrja upp á við.

> [!NOTE]
> Nokkrar takmarkanir eru gerðar:
>
> * Aðgerðin **Sækja verkáætlunarlínur** er ekki tiltæk á sölupöntunum eða sölutilboðum.
> * Ekki er hægt að afmarka reitina **Sendist-til kóti** eða **Tengiliður nr.** Reitir

## <a name="to-create-a-project-card"></a>Til að stofna verkspjald

Stofnað er verkspjald og síðan stofnaðar verkhlutalínur og verkáætlunarlínur fyrir það.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Verkefni** og velja síðan viðeigandi tengil.  
2. Veljið aðgerðina **Nýtt** og fyllið svo út reitina eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Til að byggja verkið á upplýsingum frá öðru verki skal velja aðgerðina **Afrita verk**, fylla út reitina eftir þörfum og velja svo hnappinn **Í lagi** .

> [!NOTE]  
> Ef vinnuskýrslur eru notaðar í verkefninu þarf einnig að tilnefna ábyrgðarmann. Þessi einstaklingur getur samþykkt vinnuskýrslur fyrir verk sem tengjast verkinu. Frekari upplýsingar eru í [Setja upp vinnuskýrslur](projects-how-setup-time-sheets.md).

Merkja má aðgerðir sem útilokaðar með því að nota reitinn **Útilokað**. eftirfarandi tafla lýsir áhrif valkostanna fyrir þessa reiti.

|Valkostur  |Lýsing  |
|---------|---------|
|Autt |Allar aðgerðir eru leyfðar.|
|Bóka    |Hægt er að vinna með áætlunarlínur en bókun vegna verksins er lokuð. Ef þessi kostur er valinn er ekki hægt að bóka notkun eða sölu á verkefnið.|
|Allt  |Allar aðgerðir eru lokaðar.|

## <a name="to-create-tasks-for-a-project"></a>Til að stofna verk fyrir verk

Lykilatriði í stofnun verks er að tilgreina þá verkhluta sem verkið felur í sér. Verk eru tilgreind með því að stofna eina línu fyrir hvert verk á **flýtiflipanum Verkhlutar** á síðunni **Verkspjald** . Hvert verk verður að hafa að minnsta kosti eitt verk.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Verkefni** og velja síðan viðeigandi tengil.
2. Opna verkspjald fyrir viðeigandi verk.
3. Á flýtiflipanum **Verkhlutar** skal fylla út reitina eins og þörf krefur í nýrri línu.
4. Til að færa inn verkhluta og stofna stigveldi skal velja aðgerðina **Verkhlutar** og velja **svo aðgerðina Inndráttur** verkhluta.
5. Þrep 3 og 4 eru endurtekin fyrir alla verkhluta sem þörf er á fyrir verkið.
6. Til að tilgreina verkhlutana með upplýsingum um aðra verkhluta skal velja aðgerðina **Afrita verkhluta úr** aðgerð, fylla út reitina eftir þörfum og velja **svo hnappinn Í lagi** .

## <a name="to-create-planning-lines-for-a-project"></a>Til að stofna áætlunarlínur fyrir verk

Hægt er að fínstilla nýju verkhlutana í verkáætlunarlínum. Áætlunarlína getur náð yfir upplýsingarnar sem á að rekja til verks. Til dæmis er hægt að rekja forðann sem verkefnið krefst eða vöru sem þörf er á. Til dæmis er um að ræða verk til að fá viðskiptamann til að samþykkja verkefni. Þú tengir verkið vði áætlunarlínur fyrir vörur eins og að hitta viðskiptamanninn og úthluta tilfangi.  

Áætlunarlína getur haft eina af eftirfarandi tegundum.  

| Gerð | Heimildasamstæða |
| --- | --- |
| **Fjárhagsáætlun** |Sýnir áætlaða notkun og kostnað við verkefnið, yfirleitt í verkefni af tíma- og efnisgerð. Ekki er hægt að reikningsfæra áætlunarlínur af þessari tegund. |
| **Reikningshæft** |Sýnir áætlaða reikningsfærslu til viðskiptamanns, yfirleitt í verkefni með fast verð. |
| **Bæði fjárhagsáætlun og reikningshæft** |Sýnir áætlaða notkun sem jafngildir því sem á að reikningsfæra. |

> [!NOTE]
> Kostnaðarupplýsingar eru færðar inn á áætlunarlínur verks sjálfkrafa. Sem dæmi má taka að kostnaður, verð og afsláttur tilfanga og vara byggir á upplýsingum frá tilfanginu og vörunni.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Verkefni** og velja síðan viðeigandi tengil.
2. Viðeigandi verkspjald er opnað.
3. Veljið verkhluta þar sem í reitnum **Tegund** **verkhluta er Bókun** og veljið svo aðgerðina **Áætlunarlínur verks** .  
4. Á síðunni **Áætlunarlínur** verkefnis, í nýrri línu, skal fylla út reitina eins og þörf krefur.
5. Þrep 3 og 4 eru endurtekin fyrir allar áætlunarlínur sem þarf fyrir verkhlutann.

## <a name="see-also"></a>Sjá einnig .

[Verkefnastjórnun](projects-manage-projects.md)  
[Myndband: Hvernig á að stofna verkefni í Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Fjármál](finance.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Sala](sales-manage-sales.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
