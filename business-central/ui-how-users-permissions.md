---
title: "Úthluta eða breyta notendaheimild | Microsoft Docs"
description: "Lýsir því hvernig skal bæta Office 365 notendum við Business Central, og svo úthluta heimildum, aðgangsréttindum og öryggisstillingum."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 58077ae917d7943e6dd2da06847dfbb0eef5defd
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="managing-users-and-permissions"></a>Vinna með notendur og heimildir
Til að bæta notendum í [!INCLUDE[d365fin](includes/d365fin_md.md)], verður kerfisstjóri Office 365 í fyrirtækinu fyrst að stofna notendur í stjórnstöð Office 365. Frekari upplýsingar, sjá [Bæta notendum við Office 365 for business](https://aka.ms/CreateOffice365Users).

Þegar notendur hafa verið búnir til í Office 365, geta þeir verið fluttir inn í **Notendur** gluggann í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Notendum er úthlutað heimildarsöfnum samkvæmt áætlun sem notandanum er úthlutað í Office 365. Fyrir nánari upplýsingar um leyfisveitingu, sjá [Microsoft Dynamics 365 Business Central leyfishandbók](https://aka.ms/BusinessCentralLicensing).

Má því næst úthluta notendum heimildarsöfnum til að skilgreina hvaða hluti úr gagnagrunni, og þar með hvaða einingar Viðmótsins, þeir hafa aðgang að og í hvaða fyrirtækjum. Þú getur bætt notendum við notendahópa. Þannig er auðveldara að úthluta sama heimildarsöfn á mörgum notendum.

Heimildasafn er safn heimildir fyrir tiltekna hluti í gagnagrunninum. Öllum notendum verða að hafa verið úthlutað eitt eða fleiri heimildasöfn áður en þeir geta opnað [!INCLUDE[d365fin](includes/d365fin_md.md)].

Frá **Notandakort** glugganum geturðu opnað **Virkar heimildir** gluggann til að sjá hvaða heimildir notandinn hefur og í gegnum hvaða heimildasamstæður þau eru veitt. Hér getur þú einnig breytt heimildarupplýsingum fyrir heimildarsamstæður af tegundinni **Notandaskilgreint**. Nánari upplýsingar er að finna í „Skoða eða breyta heimildum notanda“ hlutanum.

Stjórnendur geta notað **Notandauppsetningu** gluggann til að skilgreina tímabil þegar tilgreindir notendur geta bókað, og geta einnig tilgreint hvort kerfið skrái tímann sem notandinn er skráður inn.

Annað kerfi sem skilgreinir hvað notendur geta nálgast er upplifunarstillingin. Frekari upplýsingar, sjá [Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md).

## <a name="to-add-a-user-in-business-central"></a>Að bæta við notanda í Business Central
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **notendur** og veldu síðan tengda tengilinn.
2. Veldu **Fá notendur frá Office 365** aðgerð.

Sérhver nýr notandi sem hefur verið búinn til fyrir Office 365 áskriftina þína verður bætt í **Notendur** gluggann.

## <a name="to-group-users-in-a-user-group"></a>Til hópanotenda í notendahóp
Þú getur sett upp notendahópa til að hjálpa þér að stjórna heimildasamstæðum fyrir hópa notenda í fyrirtæki þínu.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Notendahópar** og veldu síðan tengda hlekkinn.
2. Einnig, í glugganum **Notendur**, veldu aðgerðina **Notandaflokkar**.
3. Í glugganum **Notandaflokkur** er valin aðgerðin **Meðlimir notandaflokks**.
4. Í glugganum **Meðlimir notandaflokks** er valin aðgerðin **Bæta við notendum**.

Þegar notendur eða notendahópar eru búnar til þarftu að úthluta heimildasamstæðum til hvers þeirra, til að skilgreina hvaða hlutur notandi getur nálgast. Fyrst verður þú að skipuleggja viðeigandi heimildir í heimildasamstæðum. Nánari upplýsingar er að finna í kaflanum „Til að búa til eða breyta heimildasamstæðu“.

## <a name="to-copy-a-user-group-and-all-its-permission-sets"></a>Til að afrita notendaflokk og öll heimildarsöfn
Til að fljótt skilgreina nýja notendaflokka geturðu afritað öll heimildarsöfn frá núgildandi notendaflokki yfir í nýjan notendaflokk.

Meðlimir úr notendaflokki eru ekki afritaðar í nýja notendaflokkinn. Þú verður að bæta þeim við handvirkt eftir á.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Notendahópar** og veldu síðan tengda hlekkinn.
2. Veldu notendaflokkinn sem þú vilt afrita og veldu síðan aðgerðina **Afrita notendaflokk**.
3. Í reitinn **Nýr kóði notendaflokks** skal færa inn heiti fyrir flokkinn og velja síðan hnappinn **Í lagi**.

Nýja notendaflokknum er bætt við gluggann **Notendaflokkar**. Halda áfram að bæta við notendum. Nánari upplýsingar er að finna í kaflanum „Að flokka notendur í notendaflokka“.  

## <a name="to-set-up-user-time-constraints"></a>Til að setja upp tímaskorður notanda
Stjórnendur geta skilgreint tímabil þegar tilgreindir notendur geta bókað, og geta einnig tilgreint hvort kerfið skrái tímann sem notandinn er skráður inn. Stjórnendur geta einnig úthlutað ábyrgðarstöðvum á notendur. Frekari upplýsingar eru í [Vinna með ábyrgðarstöðvar](inventory-responsibility-centers.md).

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Notandauppsetning** og veldu síðan tengda tengilinn.
2. Í glugganum **Notandauppsetning** opnast, skal velja **Nýtt** aðgerð.
3. Í reitnum **Kenni notanda**, skal færa inn kenni notanda, eða velja reitinn til að sjá alla núverandi Windows notendur innan kerfisins.
4. Fyllið inn í reitina eftir þörfum.

## <a name="to-create-or-edit-a-permission-set"></a>Að búa til eða breyta heimildasamstæðu
Heimildasamstæður virka sem geymir fyrir heimildir, svo að þú getir auðveldlega stjórnað mörgum heimildum í einni skrá. Þegar þú hefur búið til heimildasamstæðu verður þú að bæta við raunverulegum heimildum. Nánari upplýsingar er að finna í hlutanum „Að búa til eða breyta heimildum“.

> [!NOTE]  
> [!INCLUDE[d365fin](includes/d365fin_md.md)] lausn inniheldur yfirleitt fjölda fyrirfram skilgreindra heimildasamstæðna sem eru bætt við af Microsoft eða hugbúnaðarveitunni þinni. Þessar heimildasamstæður eru af tegund **Kerfi** eða **Viðbót**. Þú getur ekki búið til eða breytt þessum gerðum heimildasamstæða eða heimildir innan þeirra. Hins vegar getur þú afritað þau til að skilgreina eigin heimildasamstæður og heimildir. <br /><br />
Heimildasamstæður sem notendur búa til, ný eða sem afrit, eru af gerðinni **Notandaskilgreint** og er hægt að breyta.

1. Veldu ![Ljósaperu sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Heimildasamstæður**, og veldu síðan tengda hlekkinn.
2. Til að búa til nýtt heimildasamstæðu, veldu **Nýtt** aðgerðina.
3. Fyllt er í reitina í nýju línunni. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="to-copy-a-permission-set"></a>Til að afrita heimildasamstæðu
Þegar þú býrð til nýtt heimildasamstæður, getur þú notað afritunaraðgerð til að flytja allar heimildir annars heimildasamstæðu á nýtt heimildasamstæðu.

> [!NOTE]  
> Ef heimildasamstæða Kerfis sem þú hefur afritað er breytt, færð þú senda tilkynning (eftir vali þínu), svo að þú getir íhugað hvort breytingarnar séu viðeigandi til að afrita eða skrifa inn í notendaskilgreinda heimildasamstæðu þína.

1. Í **heimildasamstæður** gluggi, velja línuna fyrir heimildasamstæðu sem þú vilt afrita og síðan velja **Afrita heimildasamstæðu** aðgerðina.
2. Í **Afrita heimildasamstæðu** glugga, tilgreindu nafn hins nýja heimildasamstæðu, og þá velja **Í lagi** hnappinn.
3. Veldu **tilkynna um breyttan heimildasamstæðu** gátreitinn ef þú vilt viðhalda tengil á milli upprunalegu og afrituðu heimildasamstæðanna. Tengillinn er síðan notaður til að láta þig vita ef nafnið eða innihald upprunalegu heimildasamstæðu breytist í framtíðarútgáfunni sem lausnin er uppfærð í seinna.

Nýja heimildasamstæðan, sem inniheldur öll heimildir afritaðs heimildasamstæðu, er bætt við sem nýr lína í **heimildasamstæða** gluggann. Athugaðu að línurnar eru flokkaðar í stafrófsröð innan hvers tegundar.

## <a name="to-create-or-edit-permissions"></a>Til að búa til eða breyta heimildum
1. Í **heimildasamstæður** gluggi, velja línuna fyrir heimildasamstæðu, og þá velja **heimildir** aðgerð.
2. Í glugganum **Heimildir**, búðu til nýjan línu eða breyttu reitum á núverandi línu.

Í hverju af fimm reitum yfir aðgangstegundir, **Lesa heimild** , **Setja inn heimild**, **Breyta heimild**, **Eyða leyfi** og **Framkvæma heimildir**, þú getur valið eitt af eftirfarandi þremur heimildarvalkostum:

|Valkostur|Description|Flokkun|
|------|-----------|
|**Já**|Notandinn getur framkvæmt aðgerðina á hlutnum sem um ræðir.|Hæst|
|**Óbeint**|Notandinn getur framkvæmt aðgerðina á hlutnum sem um ræðir en aðeins í gegnum aðra tengda hlut sem notandinn hefur fulla aðgang að.|Næst hæsta|
|**Autt**|Notandinn getur ekki framkvæmt aðgerðina á hlutnum sem um ræðir.|Lægstur|

> [!NOTE]  
> Þegar þú breytir heimild og þar með tengdum heimildasamstæðu munu breytingarnar einnig eiga við um aðra notendur sem hafa heimildasamstæðu úthlutað.

## <a name="to-assign-permission-sets-to-users-or-user-groups"></a>Til að úthluta heimildasamstæðu til notenda eða notendahópa
Þú getur úthlutað heimildum til notenda á tvo vegu:
- Skilgreindu heimildasamstæður á notandakort notandans.
- Veldu gátreitinn fyrir notanda, í dálki, fyrir tengda heimildasamstæðu, í röð, í **heimildasamstæða eftir notanda** glugga.
    Með þessari aðferð er einnig hægt að úthluta heimildir fyrir notendahópa.

### <a name="to-assign-a-permission-set-on-a-user-card"></a>Til að úthluta heimildasamstæðu á notendakorti
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **notendur** og veldu síðan tengda tengilinn.
2. Veldu notandann sem á að úthluta á þessum viðskiptamanni til.
Öll heimildasöfn sem er nú þegar úthlutuð til notandans eru birtar í upplýsingakassanum **Heimildasöfn**.
3. Veldu **breyta** aðgerðina til að opna gluggann **Notandapjald** .
4. Á flýtiflipanum **Heimildasöfn notanda** skal fylla út reitina eins og þörf krefur í nýrri línu. Nánari upplýsingar er að finna í kaflanum „Til að búa til eða breyta heimildasamstæðu“.

### <a name="to-assign-a-permission-set-in-the-permission-set-by-user-window"></a>Til að úthluta heimildasamstæðu í **Heimildasamstæða eftir notanda** glugganum  
Eftirfarandi ferli útskýrir hvernig á að úthluta heimildasamstæðum til notanda í **heimildasamstæðu eftir notanda** glugganum. Skrefin eru svipuð í **heimildasamstæða eftir notendahópi** glugganum.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **notendur** og veldu síðan tengda tengilinn.
2. Í **Notendur** gluggi, veldu viðeigandi notanda, og þá velja **heimildasamstæða eftir notanda** aðgerð.
3. Í **heimildasamstæða eftir notanda** glugganum, veldu **[notandanafnið]** gátreitinn á línu fyrir viðkomandi heimildasamstæðu til að tengja samstæðuna við notandann.
4. Veldu **Allir notendur** gátreitinn til að úthluta heimildasamstæðunni til allra notenda.

## <a name="to-view-or-edit-a-users-permissions"></a>Til að skoða eða breyta heimildum notanda
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **notendur** og veldu síðan tengda tengilinn.
2. Opnaðu kort viðkomandi notanda.
3. Velja **Virkar heimildir** aðgerð.

    **Heimildir** hlutinn listar allar gagnagrunnshlutir sem notandinn hefur aðgang að. Þú getur ekki breytt þessum hluta.

    **Eftir heimildasamstæðu** hlutinn sýnir þær úthlutaðar heimildasamstæður sem notandinn fær heimildir sínar í gegnum, uppruna og gerð heimildasamstæðunnar, og að hvaða marki mismunandi aðgangsgerðir eru leyfðar.

    Fyrir hverja röð sem þú velur í **heimildir** hlutanum, sýnir **eftir heimildasamstæðu** hlutinn hvaða heimildasamstæða eða -samstæður heimildin er veitt í gegnum. Í þessum kafla er hægt að breyta gildinu í hverjum af fimm reitum aðgangsgerðar, **Lesa heimild**, **Setja inn heimild**, **Breyta heimild**, **Eyða heimild**, **Framkvæma heimild**.   

    > [!NOTE]  
    > Einungis heimildasamstæður af tegund **Notandaskilgreint** geta verið breytt.<br /><br />
    > Línur uppruna réttinda eru komnar frá áskriftinni. Heimildagildi réttindanna yfirtaka gildi í öðrum heimildasamstæðum ef þeir hafa hærri röðun. Gildi í réttindalausri heimildasamstæðu sem hefur hærra röðun en tengt gildi í réttindunum verður innan sviga til að gefa til kynna að það sé ekki virkt, þar sem það verður yfirtekið af réttindunum. Fyrir skýringu á röðun, sjáðu „Að búa til eða breyta heimildum“ hlutann.  

4. Til að breyta heimildasamstæðu skaltu í **Eftir heimildasamstæðu** hlutanum, á línu fyrir viðeigandi heimildasamstæðu af tegund **Notandaskilgreint**, skaltu velja einn af fimm reitum aðgangsgerðar og velja annað gildi.

5. Til að breyta einstökum heimildum innan heimildasamstæðunnar skaltu velja gildi í **heimildasamstæðu** reitnum til að opna **Heimildir** gluggann. Fylgdu leiðbeiningunum sem lýst er í hlutanum „Að búa til eða breyta heimildum“.  

> [!NOTE]  
> Þegar þú breytir heimildasamstæðu munu breytingarnar einnig eiga við um aðra notendur sem hafa heimildarsamstæðuna úthlutað.

## <a name="see-also"></a>Sjá einnig
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md)   
[Stjórnun](admin-setup-and-administration.md)  
[Bæta notendum við Office 365 fyrir fyrirtæki](https://aka.ms/CreateOffice365Users)  
[Microsoft Dynamics 365 Business Central leyfishandbók](https://aka.ms/BusinessCentralLicensing)

