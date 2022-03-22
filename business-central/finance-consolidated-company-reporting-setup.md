---
title: Setja upp sameiningu fyrirtækis
description: Kynnið ykkur hvernig hægt er að skilgreina hvernig gögn frá mismunandi fyrirtækjum í Business Central eru skráð í samstæðufyrirtæki.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: consolidation, subsidiaries, consolidate
ms.search.form: 1826, 1827
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 7135eb7b7b9ccb845bac1fe3ec5503201dc7b035
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/04/2022
ms.locfileid: "8383216"
---
# <a name="set-up-company-consolidation"></a>Setja upp sameiningu fyrirtækis

Áður en hægt er að sameina fjárhagsfærslur tveggja eða fleiri fyrirtækja (dótturfyrirtækja) í samstæðufyrirtæki þarf fyrst að undirbúa bókhaldslykilinn og samstæðufyrirtækið.  

Það eru tvær leiðir til að setja upp sameiningu, háð margbreytileika fyrirtækja þinna:

* Ef ekki er þörf á ítarlegum stillingum, t.d. þeim sem notaðar eru til að setja upp fyrirtæki sem þú átt aðeins hlut í, geturðu notað **Fyrirtækjasamstæða** leiðsagnarforrit með aðstoð til að setja upp samstæðu með hraði. Leiðbeiningarnar aðstoða þig gegnum grunnatriðin.
* Ef þörf er á fleiri ítarlegum stillingum, geturðu sett upp samstæðufyrirtækið og fyrirtækjaeiningarnar sjálf(ur).
  * Í sérhverri fyrirtækiseiningu skal tilgreina hvaða fjárhagslykla á að hafa með í sameiningunni og tilgreina umreikniaðferð sameiningarinnar fyrir hvern reikning.
  * Í samstæðufyrirtækinu skal setja upp spjal fyrirtækiseiningar fyrir hvert fyrirtæki sem á að vera með í sameiningunni. Á spjaldi fyrirtækiseiningar eru upplýsingar á borð við dagsetningar á fjárhagsári fyrirtækiseiningar og prósenta hvers lykils sem á að hafa með í sameiningunni.

## <a name="simple-consolidation-setup"></a>Einföld uppsetning sameiningar

[!INCLUDE [2021_releasewave1](includes/2021_releasewave1.md)]
Ef samstæðan er einföld, til dæmis vegna þess að þú ert eigandi allra fyrirtækjaeininganna sem á að steypa saman, munu **Fyrirtækjasamstæða** leiðbeiningar um uppsetningu með aðstoð leiða þig í gegnum eftirfarandi skref:

* Veldur hvort á að stofna nýtt samstæðufyrirtæki, eða steypa gögnunum saman í fyrirtæki sem þú hefur þegar stofnað fyrir samstæðuna. Fyrirtækið ætti ekki að innihalda færslur. 
* Forskoða niðurstöður. [!INCLUDE[prod_short](includes/prod_short.md)] staðfestir að hægt sé að flytja aðalgögnin og færslur yfir í samstæðufyrirtækið án vandkvæða.

Fylgið eftirfarandi skrefum til að nota leiðbeiningar um uppsetningu með hjálp:

1. Í Hlutverkamiðstöð **Endurskoðandi** skal velja **Uppsetning með hjálp** aðgerðina.
2. Velja skal **Setja upp samstæðuskýrslugerð** og fylgja svo leiðbeiningunum fyrir hvert skref í uppsetningu með hjálp.

## <a name="advanced-consolidation-setup"></a>Ítarleg uppsetning sameiningar

Ef þörf er á fleiri ítarlegum stillingum fyrir samstæðuna, geturðu sett upp samstæðu handvirkt. Ef til dæmis um ræðir fyrirtæki sem þú átt aðeins hlut í, eða fyrirtæki sem þú vilt ekki að séu hluti af samstæðunni.  

### <a name="set-up-the-consolidated-company"></a>Setja upp fyrirtæki í samstæðu

Fyrst þarf að setja upp samstæðufyrirtækið. Samsteypufyrirtækið er sett upp á sama hátt og önnur fyrirtæki eru sett upp. Nánari upplýsingar er að finna á [Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md).  

Eftirfarandi listi sýnir lykilþætti í samstæðufyrirtækinu.

1. Uppsetning bókhaldslykla

    Frekari upplýsingar er að finna í [Uppsetning eða breyting á bókhaldslykli](finance-setup-chart-accounts.md).  

    Bókhaldslyklar geta verið eins á milli fyrirtækiseiningar og samstæðufyrirtækis, eða samstæðufyrirtækið getur haft annan bókhaldslykil. Ef bókhaldslykill fyrirtækiseiningar er frábrugðinn þeim sem er fyrir samstæðufyrirtækið, þarf að tilgreina vörpunina milli lykla í lyklunum í fyrirtækiseiningunni. Frekari upplýsingar er að finna í hlutanum [Undirbúa fjárhagslykla fyrir sameiningu](#glacc).

2. Bæta við fyrirtækiseiningum

    Þegar steypa á saman fjárhagsgögnum nokkurra fyrirtækja í samsteyptu fyrirtæki, þarf  að færa inn upplýsingar um dótturfyrirtækið sem fyrirtækiseiningar sem hlut eiga að máli og að hve miklu leyti taka eigi tölur þeirra inn í útreikninga.

    Frekari upplýsingar er að finna í hlutanum [Bæta við fyrirtækiseiningum](#busunit).
3. Hægt er að tilgreina gengi við samsteypu fjárhagsskýrslna fyrirtækiseininga ef skýrslurnar eru í erlendum gjaldmiðli.

    Gengin þrjú sem notast er við eru: **Meðalgengi (handvirkt)**, **Lokagengi** og **Síðasta lokagengi**. Frekari upplýsingar er að finna í hlutanum [Tilgreina gengi gjaldmiðla fyrir sameiningar](#exchrates).
4. Hægt er að sameina víddarupplýsingar sem og fjárhagsreikninga.

    Frekari upplýsingar er að finna í hlutanum [Taka með eða sleppa víddum](#dim).

### <a name="add-business-units"></a><a name="busunit"></a>Bæta við fyrirtækiseiningum

[!INCLUDE[prod_short](includes/prod_short.md)] gerir þér kleift að setja upp lista yfir fyrirtækiseiningar sem á að sameina, staðfesta bókhaldsgögn áður en þau eru sameinuð, flytja inn skrár og búa til samstæðuskýrslur.  

1. Skráðu þig inn samstæðufyrirtækið.
2. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptaeiningar** og velja síðan viðkomandi tengil.  
3. Veljið **Nýtt** og fyllið svo inn í viðeigandi svæði. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!IMPORTANT]
    > Þegar reitirnir **Upphafsdagsetning** og **Lokadagsetning** eru fylltir út skaltu vera viss um að þú uppfyllir reglur GAAP hvað varðar fjárhagstímabil fyrirtækiseiningar gagnvart móðurfyrirtækinu.
4. Endurtakið skref 3 fyrir hverja fyrirtækiseiningu til viðbótar

Ef fyrirtækið þitt notast við erlendan gjaldmiðil, er nauðsynlegt að tiltaka gengið sem nota skal í samstæðunni. Einnig verðu að slá inn samstæðuupplýsingar um fjárhagsreikninga fyrirtækiseiningarinnar. Þessum ferlum er lýst í eftirfarandi hlutum.

### <a name="prepare-general-ledger-accounts-for-consolidation"></a><a name="glacc"></a>Undirbúa fjárhagslykla fyrir sameiningu

Bókhaldslykill fyrirtækis sem á að sameina þarf að  tilgreina reikninga fyrir samsteypu. Fyrir hvern bókunarfjárhagsreikning fyrirtækja þarf að tilgreina fjárhagsreikninginn sem leggja skal inn á þegar samsteypa er framkvæmd. Þetta er vörpun sem leyfir sameiningu fyrirtækja með ólíka bókhaldslykla.

Ef bókhaldslyklar í fyrirtækjaeiningunni eru ekki þeir sömu og í samstæðufyrirtækinu er nauðsynlegt að búa til fjárhagslykla fyrir samlegðina. Þú getur tilgreint reikninga sem bóka á debet og kredit á, sem og þá aðferð sem nota skal við að umreikna gjaldmiðil í samstæðufyrirtækinu. Þetta er til dæmis gagnlegt ef þú keyrir skýrsluna oft.

1. Í hverju [!INCLUDE [prod_short](includes/prod_short.md)] viðskiptaeiningu skal velja ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bókhaldslykill** og velja síðan viðkomandi tengil.  
2. Opnaðu kortið fyrir reikninginn og fylltu svo út í reitina á **Samstæða** flýtiflipanum. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### <a name="specify-exchange-rates-for-consolidations"></a><a name="exchrates"></a>Tilgreina gengi gjaldmiðla fyrir samstæður

Ef fyrirtækjaeining notar annan gjaldmiðil en samstæðufyrirtækið, er nauðsynlegt að tiltaka hvaða aðferðir eru notaðar við útreikning gjaldmiðla á hverjum reikningi áður en þú steypir saman. Fyrir hvern fjárhagsreikning ákvarðar innihald reitsins **Umreikniaðferð samstæðunnar** hvaða gengi gjaldmiðla er notað. Í samstæðufyrirtækinu, á hverju spjaldi fyrirtækiseiningarinnar í **Töflunni Gengi gjaldmiðla** er tilgreint hvort samstæðan noti gengi gjaldmiðla frá fyrirtækiseiningunni eða samstæðufyrirtækinu. Ef notað er gengi gjaldmiðla frá samstæðufyrirtækinu er hægt að breyta gengi gjaldmiðla hjá fyrirtækiseiningunni. Fyrir fyrirtækiseiningu, ef **Gengistafla á spjaldi** fyrirtækjaeiningarinnar inniheldur **Staðbundið**, er hægt að breyta genginu af spjaldi fyrirtækjaeiningarinnar. Gengi er afritað af töflunni **Gengi** en það er hægt að breyta þeim áður en samruni á sér stað.

Í eftirfarandi töflu er gengisaðferðum sem hægt er að nota fyrir lykla lýst.

|Gengi | Dæmigerð notkun |
|---|---|
|Meðalgengi (handvirkt) | Þú reiknar handverk meðalgengi tímabilsins sem á að sameina. Reiknaðu meðaltalið annaðhvort sem reiknað meðaltal eða besta mat og tilgreindu niðurstöðurnar fyrir hverja fyrirtækiseiningu. Notað fyrir rekstrarreikninga.|
|Lokagengi | Notað fyrir efnahagslykla.|
|Síðasta lokagengi | Gengið sem gilti á gengismarkaði á dagsetningunni sem verið er að undirbúa efnahagsreikning og rekstrarreikning fyrir. Gengið er fært inn fyrir hverja fyrirtækiseiningu. Notað fyrir efnahagslykla.|
|Ferill gengis | Gengið sem var í gildi þegar viðskiptin áttu sér stað.|
|Samsett gengi | Upphæðir gildandi tímabils eru umreiknaðar á meðalgengi og bætt við áður skráða stöðu í samstæðufyrirtækinu. Þessi aðferð er iðulega notuð fyrir reikninga óráðstafaðs eigin fjár vegna þess að þeir innihalda upphæðir frá öðrum tímabilum sem eru þar af leiðandi samsettar upphæðir, umreiknaðar út frá ólíku gengi.|
|Gengi eiginfjár | Þetta er svipað og **Samsett**. Mismunur er bókaður á aðra fjárhagsreikninga.|

Til að tilgreina gengi gjaldmiðla fyrir fyrirtækiseiningar, skal fylgja eftirfarandi skrefum:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptaeiningar** og velja síðan viðkomandi tengil.  
2. Á síðunni **Listi yfir fyrirtækiseiningar** skal velja fyrirtækiseininguna, og síðan **Meðalgengi (handvirkt)** aðgerðina.  
3. Á síðunni **Breyta gengi gjaldmiðils** hefur efni í reitnum **Viðmiðunargengi** verið afritað úr töflunni **Gengi gjaldmiðils** en hægt er að breyta því. Lokaðu síðunni.  
4. Veldu aðgerðina **Lokagengi**.  
5. Í reitnum **Upphæð viðmiðunargengis** skal færa inn gengið.

### <a name="include-or-exclude-dimensions"></a><a name="dim"></a>Taka með eða útiloka víddir

Hægt er að sameina víddarupplýsingar sem og fjárhagsreikninga.

* Í viðeigandi vídd skal tilgreina reitinn **Samstæðukóði** eða skilja hann eftir auðan
  * Til að sleppa vídd í sameiningu skal skilja reitinn **Samstæðukóði** eftir auðan í víddinni og ekki velja víddirnar í reitunum **Afrita víddir** í neinni samstæðuaðgerð eða -skýrslu.
  * Til að hafa með víddarupplýsingar í sameiningunni skal skilja reitinn **Samstæðukóði** eftir auðan. Hins vegar virkar samsteypan eingöngu ef víddargildin í fyrirtækiseiningunni eru þau sömu og samsteypufyrirtækið.
  * Til að sameina víddargildiskóðann í fyrirtækiseiningunni með öðrum víddargildiskóða í samstæðufyrirtækinu skal fylla út reitinn **Samstæðukóði** í þeim víddum sem eiga við.  
* Bæta viðeigandi víddum við viðeigandi fjárhagslykla

### <a name="exclude-a-company-from-consolidation"></a><a name="exclude"></a>Útiloka fyrirtæki frá samstæðu

Ef þú vilt ekki að fyrirtæki sé hluti af samstæðunni, geturðu útilokað það. Til að gera það, skal fara í kort fyrirtækiseiningarinnar og hreinsa **Steypa saman** gátreitinn.

### <a name="include-a-partially-owned-company-in-consolidation"></a><a name="include"></a>Hafa fyrirtæki í hlutaeign með í samstæðu

Ef þú átt aðeins hlut í fyrirtæki geturðu tengt prósentutölu, sem samsvarar hlutaeigninni í fyrirtækinu, við hverja færslu. Ef þú átt til dæmis 70% hlut í fyrirtækinu, mun samlegðin ná til $70 af reikningi upp á $100. Til að tilgreina prósentutölu eignar þinnar í fyrirtækinu, skal fara í kort fyrirtækiseiningarinnar og slá inn prósentuna í reitnum **Samstæða %**.  

## <a name="see-also"></a>Sjá einnig

[Steypa saman fjárhagsgögnum frá mörgum fyrirtækjum](finance-consolidated-company-reporting.md)  
[Vinna með millifyrirtækjafærslur](intercompany-manage.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Flutningur viðskiptagagna í Excel](about-export-data.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]