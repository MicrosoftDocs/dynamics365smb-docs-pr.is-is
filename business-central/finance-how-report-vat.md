---
title: Skila inn VSK-skýrslum til skattayfirvalda
description: 'Kynntu þér hvernig skal undirbúa skýrslu sem telur upp VSK-upphæðir af sölu yfir ákveðið tímabil, eða fyrir sölu og innkaup, og senda hana til skattyfirvalda.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'VAT, tax, report, EC sales list, statement'
ms.search.form: '321, 322, 323, 474, 475, 739, 740, 741, 742, 743, 744, 745, 746, 747, 748, 9401'
ms.date: 01/31/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="report-vat-to-tax-authorities"></a>Senda VSK skýrslu inn til skattayfirvalda

Þetta efnisatriði lýsir skýrslunum í [!INCLUDE[prod_short](includes/prod_short.md)] sem þú getur notað til að senda inn upplýsingar um virðisaukaskatt (VSK) upphæðir fyrir sölu og innkaup til skattayfirvalda á þínu svæði. Í skýrslunum geta verið tilteknar upplýsingar, eða viðbótarskýrslur sem þarf að senda, allt eftir tilteknu landi/svæði. Athuga skal greinarnar fyrir landið/svæðið í hlutanum [Staðbundnar aðgerðir](about-localization.md) .  

Hægt er að nota eftirfarandi innbyggðar skýrslur:

* Skýrslan **EB-söluyfirlit**  

    Í skýrslunni Sölulisti Evrópubandalagsins (EC) er listi yfir virðisaukaskattsupphæðir (VSK) sem innheimtar hafa verið fyrir sölu til VSK-skráðra viðskiptamanna í löndum/reglugerðum Evrópusambandsins (ESB).  
* Skýrslan **VSK-skil**  

    VSK-vöruskilaskýrslan inniheldur VSK fyrir sölu og innkaup til viðskiptamanna og frá lánardrottnum í öllum löndum/svæðum sem nota VSK.  

Í báðum tilvikum (eins og í öðrum VSK-skýrslum) er VSK reiknaður út frá VSK-bókunargrunninum og VSK-bókunarflokkunum sem settir hafa verið upp. [!INCLUDE[prod_short](includes/prod_short.md)] sýnir VSK-færslur á grundvelli VSK-dagsetningar **sem** aðalskýrsludagsetningu.  

> [!NOTE]
> Allar VSK-tengdar skýrslur keyra nú með **VSK-dagsetningunni** til að afmarka viðeigandi færslur. Jafnvel þótt notkun VSK-dagsetningar **sé sett upp** þar sem **Ekki nota aðgerðina** [!INCLUDE[prod_short](includes/prod_short.md)] VSK-dagsetning felur öll tilvik VSK-dagsetningar **í** jöfnuninni. Vsk-dagsetningin er þó **enn notuð í öllum skýrslum og er sjálfkrafa fyllt með** bókunardagsetningunni **.**

Ef þú vilt skoða allan feril VSK færslna, þá býr hver VSK-bókun til færslu á **VSK-færslur** síðunni. Þessar færslur eru notaðar til að reikna VSK-upphæðir s.s. greiðslur og endurgreiðslur á tilteknu tímabili. Til að skoða VSK-færslur skal velja ![Ljósaperuna sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **VSK-færslur** og velja síðan viðkomandi tengil.

> [!NOTE]
> Hvert [!INCLUDE[prod_short](includes/prod_short.md)] umhverfi á að meðhöndla reglubundnar skýrslur í einu einu landi/svæði. Til dæmis sér hollensk útgáfa um [!INCLUDE[prod_short](includes/prod_short.md)] VSK-skýrslur í Hollandi en ekki í öðrum löndum/svæðum. Á svipaðan hátt sér Útgáfa Bandaríkjanna um [!INCLUDE[prod_short](includes/prod_short.md)] 1099 skýrslugerð í Bandaríkjunum og styður ekki kröfur um VSK-skýrslur í öðrum löndum/svæðum, nema með viðauka sem vistkerfi samstarfsaðila okkar fær eða breytingu á sértækum kóta viðskiptamanna.

## <a name="about-the-ec-sales-list-report"></a><a name="ecsaleslist"></a>Um EC söluyfirlitsskýrslu

Innan Evrópusambandsins (ESB) og í Bretlandi þurfa öll fyrirtæki sem selja viðskiptavinum og þjónustu vsk-skráðra viðskiptamanna, þar á meðal viðskiptamenn í öðrum löndum/svæðum Evrópusambandsins (ESB) að senda rafræna útgáfu af sölulista Evrópubandalagsins (EC) til tolla- og skattayfirvalda. Skýrslan **EC sölulisti** vinnur aðeins fyrir lönd/svæði í ESB.

Skýrslan inniheldur eina línu fyrir hverja tegund af viðskiptum við viðskiptavini, og sýnir heildarupphæð fyrir hverja tegund viðskipta. Hægt er að skrá þrjár gerðir viðskipta í skýrslunni:  

* B2B vörur  
* B2B þjónusta  
* B2B Þríhliða vörur  

*B2B* vörur og þjónusta tiltaka hvort þú seldir vörur eða þjónustu, og sért undir stjórn stillingarinnar **ESB Þjónusta** í uppsetningu bókunar á VSK. *B2B Þríhliða vörur* gefa það til kynna hvort þú stundaðir viðskipti við þriðja aðila og sért undir stjórn stillingarinnar **ESB þríhliða viðskipti** í söluskjölum, eins og sölupantanir, reikningar, kreditreikningar osfrv.  

Eftir að skattayfirvöld fara yfir skýrsluna, munu þau senda tengilið fyrirtækisins tölvupóst. Í [!INCLUDE[prod_short](includes/prod_short.md)] er tengiliðurinn tiltekinn á síðunni **Upplýsingar um fyrirtækið**. Áður en þú sendir inn skýrsluna skaltu vera viss um að tengiliður hafi verið valinn.  

### <a name="submit-an-ec-sales-list-report"></a>Senda inn EB-söluyfirlitsskýrslu

[!INCLUDE [finance-ecsaleslist](includes/finance-ecsaleslist.md)]

## <a name="about-the-vat-return-report"></a><a name="vatreturn"></a>Um skýrsluna um VSK skil

Nota þessa skýrslu til að skila inn VSK fyrir sölu- og innkaupaskjöl, eins og innkaupa- og sölupantanir, reikninga og kreditreikninga. Upplýsingarnar koma fram með sama sniði í skýrslunni og á skýrslublaði frá tolla- og skattayfirvöldum.  

Fyrir VSK skilin geturðu tiltekið hvaða færslur skuli teknar með:

* Senda inn aðeins opnar færslur, eða opnar og lokaðar. Til dæmis, þetta er gagnlegt þegar verið er að undirbúa hin árlegu VSK lokaskil.
* Tilgreinir hvort á að taka með VSK-færslur aðeins fyrir tilgreint tímabil eða einnig frá fyrri tímabilum innan tilgreinds árs. Þetta er gagnlegt fyrir uppfærslu VSK skila sem þú hefur þegar sent inn, til dæmis, ef lánardrottin sendir þér síðbúinn reikning.    

## <a name="to-connect-to-your-tax-authoritys-web-service"></a>Til að tengjast vefþjónustu skattayfirvalda býður
[!INCLUDE[prod_short](includes/prod_short.md)] býður upp á þjónustutengingar sem tengjast við vefsíður skattayfirvalda. Ef þú ert t.d. í Bretlandi, er hægt að virkja **GovTalk** þjónustutenginguna til að senda inn EC Sölulista og VSK skýrslum rafrænt. Ef þú vilt senda skýrsluna inn handvirkt, til dæmis með því að færa gögnin inn á vefsíðu skattayfirvalda, er það ekki nauðsynlegt.   

Til að skila VSK til skattayfirvalda á rafrænu formi, þarf að tengja [!INCLUDE[prod_short](includes/prod_short.md)] við vefþjónustu skattayfirvalda. Til þess þarf að setja upp reikning hjá þínum skattayfirvöldum. Þegar þú ert komin(n) með reikning, geturðu virkjað þjónustutengingu sem við bjóðum upp á í [!INCLUDE[prod_short](includes/prod_short.md)].

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 2.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, farðu í **Þjónustutengingar** og veldu síðan viðeigandi tengil.
2. Fylltu út nauðsynlega reiti. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > Ráðlegt er að er að prófa tenginguna. Til að gera það skal velja **Prufustilling** gátreitinn, svo undirbúa og senda inn VSK skýrslurnar eins og lýst er í [Að undirbúa og senda inn VSK skýrslu](#to-prepare-and-submit-a-vat-report) hlutanum. Þegar þjónustan er á Prufustillingu, prófar hún hvort skattayfirvöld geti tekið á móti skýrslunni, og staðan á skýrslunni mun gefa til kynna hvort prufuinnsendingin hafi heppnast. Mikilvægt er að muna að þetta er ekki raunveruleg innsending. Ef senda á skýrsluna inn í raun, þarf að að hreinsa gátreitinn **Prufustilling** og endurtaka innsendingarferlið.

## <a name="to-set-up-vat-reports-in-"></a>Að setja upp VSK-skýrslur í [!INCLUDE[prod_short](includes/prod_short.md)]

[!INCLUDE [vat-report-setup](includes/vat-report-setup.md)]

### <a name="to-set-up-vat-return-periods"></a>Að setja upp tímabil VSK-skila

Ef fyrirtækið þitt er ekki í Bretlandi getur þú notað síðuna **Tímabil VSK-skila** til að setja upp tímasett VSK-skil. ef fyrirtæki þitt er staðsett í Bretlandi skaltu skoða [Að gera skatt á stafrænu formi á Bretlandi](LocalFunctionality/UnitedKingdom/making-tax-digital-submit-vat-return.md).  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Tímabil VSK-skila** og velja síðan viðkomandi tengil.  
2. Á síðunni **Tímabil VSK-skila** skal fylla út í reitina og setja upp fyrsta tímabilið. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)].  
3. Endurtaktu skref 2 ef þú vilt bæta fleiri tímabilum við.  

Þegar komið er að því að skila VSK-skýrslu fyrir tímabil VSK-skila skal velja tímabilið á síðunni **Tímabil VSK-skila** og síðan velja aðgerðina **Stofna VSK-skil**. Síðan í spjaldinu **VSK-skil** skal velja aðgerðina **Stinga upp á línum** eins og lýst er í skrefi 3 í eftirfarandi ferli.  

## <a name="to-prepare-and-submit-a-vat-report"></a>Undirbúa og senda inn VSK-skýrslu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 3.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, farðu í **EB-söluyfirlit** eða **VSK skil** og veldu síðan tengda tengilinn.  
2. Veljið **Nýtt** og fyllið svo inn í viðeigandi svæði. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Til að útbúa efni skýrslunnar, veljið aðgerðina **Leggja til línur**.  

    > [!NOTE]  
    >  Hægt er að endurskoða færslurnar varðandi EC söluyfirlit, sem eru innifaldar í skýrslulínunni, áður en þú skilar inn skýrslunni. Til að gera það, skaltu velja línuna og svo aðgerðina **Sýna VSK færslur**.  

4. Til að staðfesta og undirbúa skýrsluna til innsendingar skal velja aðgerðina **Losa**.  

    > [!NOTE]  
    > [!INCLUDE[prod_short](includes/prod_short.md)] staðfestir hvort skýrslan sé rétt sett upp. Ef staðfestingin mistekst, eru villurnar sýndar í **Villur og viðvaranir** svo hægt sé að gera viðeigandi breytingar. Ef skilaboðin snúast um stillingu sem vantar í [!INCLUDE[prod_short](includes/prod_short.md)], geturðu smellt á skilaboðin til að opna síðuna sem inniheldur upplýsingarnar sem þarf að leiðrétta.  
5. Til að senda skýrsluna inn skal velja aðgerðina **Innsending**.  

Eftir að þú skilar inn skýrslunni, fylgist [!INCLUDE[prod_short](includes/prod_short.md)] með þjónustunni og heldur skrá yfir samskipti þín. Reiturinn **Staða** gefur til kynna hvar skýrslan er stödd í ferlinu. Þegar t.d. yfirvöld fara yfir skýrsluna, breytist staða skýrslunnar yfir í **Heppnaðist**. Ef skattayfirvöld finna mistök í skýrslunni sem þú sendir þeim, mun staða skýrslunnar breytast yfir í **Mistókst**. Þú getur skoðað villur undir **Villur og viðvaranir**, leiðrétt þær og svo sent skýrsluna inn aftur. Til að skoða allar EC söluyfirlitsskýrslur þínar, farðu á **EC söluyfirlitsskýrslur** síðuna.  

### <a name="vat-return-statuses"></a>Staða VSK-vöruskila

VSK-vöruskil geta haft mismunandi stöðu eins og lýst er í eftirfarandi töflu.

| Staða | Heimildasamstæða |
|------------|-------------------------|
| Opinn | Þegar ný VSK-vöruskil eru stofnuð. Hægt er að keyra aðgerðina **Leggja til línur** . Ef leiðrétta þarf gildi er hægt að keyra aðgerðina **Leggja til línur** aftur. Ekki er hægt að skila VSK-vöruskilum sem hafa þessa stöðu. |
| Losað | Stöðunni verður breytt þegar aðgerðin **Gefa út** er notuð. [!INCLUDE[prod_short](includes/prod_short.md)] birtir **flýtiflipann Villur og viðvaranir** . Ekki er hægt að gera breytingar eða nota aðgerðina **Leggja til línur** . Til að gera breytingar þarf að enduropna VSK-vöruskilin. |
| Hafnað | Hafi sendingin ekki heppnast (ef sannvottun brást, til dæmis, breytist **staðan í Hafnað**. Ekki er hægt að enduropna VSK-vöruskil sem hafa þessa stöðu. |
| Sent inn | VSK-vöruskilin eru send með aðgerðinni **Senda** eða merkt sem send með aðgerðinni **Merki sem send** . |
| Samþykkt | VSK-vöruskilin hafa þessa stöðu ef skýrslan er merkt sem samþykki með því að nota aðgerðina **Merki sem samþykkt** . Ef skýrslan **VSK-vöruskil** er merkt sem **Samþykkt** er hægt að keyra aðgerðina **Reikna og Bóka VSK-uppgjör** . |

## <a name="viewing-communications-with-your-tax-authority"></a>Skoða samskipti við skattayfirvöld

Í sumum löndum/svæðum er skipst á skilaboðum til skattyfirvalda þegar skýrslur eru sendar. Hægt er að skoða fyrstu og síðustu skilaboðin sem voru send eða móttekin með því að velja aðgerðirnar **Hala niður innsendingarskilaboðum** og **Hala niður svarskilaboðum**.  

## <a name="submitting-vat-reports-manually"></a>Sendir inn VSK-skýrsla handvirkt
Ef þú notast við aðra aðferð til að senda skýrsluna inn, t.d. með því að flytja út XML og hlaða því svo upp á vefsíðu skattayfirvalda, geturðu eftir á valið **Merkja sem Búið að skila** til að loka skýrslutímabilinu. Eftir að þú merkir skýrsluna sem Búið að skila, er ekki hægt að breyta henni. Ef breyta þarf skýrslunni eftir að hún hefur verið merkt sem útgefin þarf fyrst að enduropna hana.

## <a name="vat-settlement"></a>VSK-uppgjör
Reglulega þarf að greiða nettó-VSK til skattayfirvalda. Ef þú þarft að gera upp VSK oft, er hægt að nota keyrsluna **Reikna og bóka VSK-uppgjör** til að loka opnum VSK-færslum og flytja VSK-upphæðir innkaupa og sölu í VSK-uppgjörsreikning.

Þegar þú færir VSK-upphæðir inn á uppgjörsreikninginn, eru VSK-upphæðirnar sem reiknaðar voru á yfirlitstímabilinu lagðar inn á reikning innskatts og teknar út af reikningi útskatts. Nettóupphæðin er lögð inn eða tekin út, ef innskattsupphæðin er hærri, á VSK-uppgjörsreikninginn. Hægt er að bóka uppgjörið strax eða prenta prófunarskýrslu fyrst.  

> [!Note]
> Ef þú tiltekur ekki **VSK Viðskiptabókunarflokkur** og **VSK Vörubókunarflokkur** þegar notuð er **Reikna út og bóka VSK Uppgjör** runuvinnslan, munu færslur með öllum viðskiptabókunarflokkur og vörubókunarflokkur kóðar teknir með.

## <a name="configuring-your-own-vat-reports"></a>Grunnstilla þínar eigin VSK skýrslur

Hægt er að nota tilbúna skýrslu af **EB-söluyfirliti**. Hins vegar er einnig hægt að búa til eigin skýrslur ef þú ert með þróunarleyfi svo þú getir búið til kóðaeiningar. Hafðu samband við samstarfsaðila Microsoft ef þig vantar aðstoð.  

Eftirfarandi tafla lýsir kóðaeiningunum sem þú þarft að stofna fyrir skýrsluna þína.  

| Codeunit | Það sem hún þarf að gera |
|----|-----|
|Tillögulínur| Ná í upplýsingar frá **VSK færslutöflunni** og birta þær í línum VSK skýrslunnar.|
|Efni | Stjórna sniði skýrslunnar. Til dæmis hvort þú notar XML eða JSON. Gerð sniðs sem á að nota fer eftir skilyrðum vefþjónustu skattayfirvalda. |
|Sending | Stjórnaðu því hvernig og hvenær þú sendir inn skýrsluna, með tilliti til skilyrða skattayfirvalda. |
|Svarstjóri | Stýra skilum frá skattayfirvöldum. Þau gætu t.d. sent tengilið fyrirtækisins tölvupóst. |
|Hætta við | Senda inn afturköllun VSK skýrslu sem var send inn áður til skattayfirvalda. |  

> [!Note]
> Þegar stofnaðar eru kóðaeiningar fyrir skýrsluna skal veita athygli gildinu í reitnum **VSK skýrsla útgáfa**. Þessi reitur verður að endurspegla útgáfuna af skýrslunni sem er eða var send til skattayfirvalda. Þú gætir til dæmis fært inn **2021** í reitinn til að gefa til kynna að skýrslan samræmist þeim kröfum sem voru í gildi það ár. Til að finna núgildandi útgáfu skal hafa samband við skattayfirvöld.  

## <a name="see-also"></a>Sjá einnig .

[Uppsetning fyrir útreikning og bókunaraðferðir virðisaukaskatts](finance-setup-vat.md)  
[Unnið með VSK í sölu og innkaupum](finance-work-with-vat.md)  
[Uppsetning sölu](sales-setup-sales.md)  
[Reikningsfæra sölur](sales-how-invoice-sales.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
