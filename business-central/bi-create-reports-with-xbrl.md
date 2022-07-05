---
title: Hvernig á að Stofna skýrslur með XBRL
description: XBRL er XML-miðað tölvumál til að merkja fjárhagsgögn og gera fyrirtækjum kleift að vinna úr og deila gögnum sínum á árangursríkan og nákvæman hátt.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: b282ea2aeec8e28b36bdadfdb57065e8c9e0c727
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/29/2022
ms.locfileid: "9075057"
---
# <a name="create-reports-with-xbrl"></a>Stofna skýrslur með XBRL

> [!NOTE]
> Við erum að vinna í því að fjarlægja aðgerðirnar fyrir XBRL skýrslugerð [!INCLUDE[prod_short](includes/prod_short.md)]. Nánari upplýsingar má finna [í breytingum á 2022 1](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1).

XBRL (eXtensible Business Reporting Language) er XML-miðað tölvumál fyrir viðskiptaskýrslugerð og gerir fyrirtækjum kleift að vinna úr og deila gögnum sínum á árangursríkan og nákvæman hátt. XBRL-áætlunin býður fjölda hugbúnaðarfyrirtækja sem framleiða bókhalds- og áætlunarkerfi og alþjóðlegum endurskoðendafyrirtækum altæka viðskiptaskýrslugerð. Markmið áætlunarinnar er að búa til staðal fyrir samræmda skýrslugerð viðskiptaupplýsinga fyrir banka, fjárfesta og ríkisstofnanir. Slíkar viðskiptaskýrslur geta falið í sér eftirfarandi atriði:  

 • Ársreikninga  
 • Viðskiptatengdar upplýsingar  
 • Upplýsingar sem eru ekki viðskiptatengdar  
 • Reglubundna skráningu, eins og ársreikninga og ársfjórðungsreikninga  

> [!NOTE]
> Hægt er að flytja inn fjárhagstengd skema og búa til XBRL-tilviksskjöl með því að varpa fjárhagsgögnum úr bókhaldslyklinum yfir í einingar í flokkunum sem voru hannaðar fyrir fjárhagsskýrslur á borð við efnahagsreikninga, rekstrarreikninga og svo framvegis.
> 
> XBRL-möguleikarnir í Business Central styðja flokkanir fyrir lýsingu 2.1, þó gætu flokkanir innihaldið óstuddar einingar á borð við tenglagrunna formúlu, iXBRL eða verið með annars konar mismunandi byggingu. Mælt er með því að villuleita XBRL-möguleikann áður en þú notar í skýrslugerð.
> 
> Fullur stuðningur við flokkanir gæti þurft XBRL-merkingu og verkfæri þriðja aðila. Alþjóðleg stofnun XBRL er með lista yfir verkfæri og þjónustu sem hægt er að nota fyrir XBRL-skýrslugerð. Það fer eftir XBRL-skýrslukröfunum fyrir tiltekna flokkun hvort þú viljir skoða þessi úrræði eitthvað frekar. Frekari upplýsingar er að finna [Hefjast handa fyrir Business](https://go.microsoft.com/fwlink/?linkid=2153466) og [Verkfæri og þjónusta](https://go.microsoft.com/fwlink/?linkid=2153356).

## <a name="extensible-business-reporting-language"></a>eXtensible Business Reporting Language (XML-miðað tölvumál fyrir viðskiptaskýrslugerð)
XBRL (e **X** tensible **B** usiness **R** eporting **L** anguage) er XML-miðað tölvumál fyrir viðskiptaskýrslugerð. Með XBRL fæst staðall til samræmdrar skýrslugerðar fyrir alla notendur fjárhagslegra upplýsinga, svo sem opinber fyrirtæki og fyrirtæki í einkaeign, endurskoðendur, eftirlitsaðila, þá sem starfa við greiningu, fjárfesta, fjármagnsmarkaði og lánastofnanir, ennfremur aðra aðila, til dæmis forritara og þá sem starfa við gagnasöfn.  

Flokkunum er haldið við á www.xbrl.org. Hægt er að sækja flokkanir eða fá nánari upplýsingar á XBRL-vefsetrinu.  

Aðili sem vill skiptast á fjárhagslegum upplýsingum við notandann lætur hann hafa flokkun XML skjal með einu eða fleiri skemum, sem hvert er með einni eða tveimur línum til að fylla út. Línurnar samsvara einstökum fjárhagslegum upplýsingum sem sá sem sendir krefst þess að fá. Flokkunin er flutt inn og skemað eða skemun fyllt út með því að færa inn reikninginn eða reikningana sem eiga við hverja línu og hvaða tímamörk skuli nota, t.d. nettóbreytingu eða stöðu til dags. Í sumum tilvikum er hægt að færa inn fasta í stað, t.d. starfsmannafjölda. Nú er hægt að senda tilviksskjalið (XML-skjal) til aðilans sem bað um það. Hugmyndin er að þetta gæti verið endurtekið tilvik svo að ekki séu flutt út ný tilviksskjöl fyrir ný tímabil nema beðið sé um það.  

## <a name="xbrl-is-comprised-of-the-following-components"></a>XBRL er myndað úr eftirfarandi hlutum  
XBRL **lýsingin** útskýrir hvað XBRL er og hvernig XBRL tilviksskjöl og flokkanir eru byggð upp. XBRL-lýsingin útskýrir XBRL með tæknilegum hugtökum og er fyrir tæknifólk.  

XBRL **skemun** eru grunnhlutar XBRL. Skemað er XSD-raunskráin sem lýsir því hvernig byggja á upp tilviksskjöl og flokkanir.  

XBRL- **tenglagrunnarnir** eru XML-raunskrárnar sem í eru ýmsar upplýsingar um einingarnar sem er að finna í XBRL-skemanu, svo sem merki á einu eða fleiri málum, hvernig þau tengjast, hvernig leggja á saman einingar o.s.frv.  

XBRL **flokkun** er "orðalisti" eða "orðabók" búin til í samvinnu og samhæf XBRL-lýsingunni og notuð til að skiptast á viðskiptaupplýsingum.  

XBRL **Tilviksskjal** er viðskiptaskýrsla, t.d. ársreikningur, sem gerður er samkvæmt XBRL-lýsingu. Merking gildanna í tilviksskjalinu er útskýrð í flokkuninni. Tilviksskjal er gagnslítið nema maður þekki flokkunina sem það er útbúið eftir.  

## <a name="layered-taxonomies"></a>Lagskiptar flokkanir  
Flokkun getur verið sett saman úr grunnflokkun, t.d. us-gaap eða IAS, og haft einn eða fleiri viðauka. Þetta er endurspeglað með því að flokkun vísar til eins eða fleiri skema þar sem öll eru sérstakar flokkanir. Þegar viðbótarflokkanirnar eru settar inn í gagnagrunninn er nýju einingunum einfaldlega bætt aftan við fyrirliggjandi einingar.  

## <a name="linkbases"></a>Tenglagrunnar  
 Í XBRL lýsingu 2 er flokkuninni lýst í nokkrum XML-skrám. Aðal-XML-skráin er flokkunarskemaskráin sjálf (.xsd-skrá) sem í er aðeins óraðaður listi eininga eða staðreynda sem eiga að vera í skýrslunni. Þessu til viðbótar eru yfirleitt tengdar tenglagrunnsskrár (.xml). Í tenglagrunnsskránum eru gögn sem eru nauðsynleg fyrir flokkunarskemaskrána (.xsd-skrána). Til eru sex tegundir tenglagrunnsskráa og fjórar þeirra eru notaðar í afurðarheiti XBRL. Þær eru:  

-   Merkjatenglagrunnur: í þessum tenglagrunni eru merki eða heiti einingar. Skráin kann að innihalda merki á mismunandi tungumálum sem eru auðkennd með XML-eiginleikanum sem kallast 'lang'. XML-tungumálskenni innihalda venjulega tveggja stafa skammstöfun og þó að auðvelt sé að giska á hvað skammstöfunin þýðir er engin tenging við Windows-tungumálakóðann eða tungumálakóðana sem skilgreindir eru í sýndargögnunum. Þegar notandi flettir upp tungumálunum fyrir tiltekna flokkun getur hann því séð allar merkingarnar fyrir fyrstu eininguna í flokkuninni, sem þýðir að hann sér dæmi fyrir hvert tungumál. Flokkun getur haft nokkur merkistenglagrunna tengda honum ef þessir tenglagrunnar innihalda ólík tungumál.  

-   Tenglagrunnur framsetningar Í þessum tenglagrunni eru upplýsingar um skipan eininganna, eða nánar tiltekið, hvernig útgefandi flokkunarinnar leggur til að forritið setji flokkunina fram fyrir notandann. Tenglagrunnurinn inniheldur röð tengla sem hver tengir tvær einingar sem yfir- og undireiningu. Þegar öllum tenglunum er beitt má sjá einingarnar í stigveldisröð. Athuga skal að tenglagrunnur framsetningar snýst aðeins um þetta: framsetningu eininga fyrir notandann.  

-   Tenglagrunnur útreikninga: Í þessum tenglagrunni eru upplýsingar um það hvaða einingar eru lagðar saman úr hverjum. Skipanin er nauðalík þeirri sem er á tenglagrunni framsetningar, nema að hver tengill eða 'ör', eins og þeir eru kallaðir, hefur vægiseiginleika. Vægið getur verið 1 eða -1 eftir því hvort einingunni skuli bætt við eða hún dregin frá yfireiningu sinni. Athuga skal að samtölurnar þurfa ekki endilega að samræmast sýnilegri framsetningu.  

-   Tilvísunartenglagrunnur: Þessi tenglagrunnur er xml-skrá sem inniheldur viðbótarupplýsingar um gögnin sem krafist er af útgefanda flokkunarinnar.

## <a name="to-set-up-xbrl-lines"></a>XBRL línur settar upp  
Þegar búið er að flytja flokkunina inn eða uppfæra hana verður að setja nauðsynlegar upplýsingar í skemalínurnar. Meðal þessara upplýsinga eru grunnupplýsingar um fyrirtækið, réttir ársreikningar, athugasemdir við ársreikninga, viðbótarskemu og aðrar upplýsingar sem krafist er við skýrslugerðina.  

XBRL-línur eru settar upp með því að varpa gögnum úr flokkuninni í gögn í fjárhag.  

1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **XBRL-flokkanir** og velja síðan viðkomandi tengil.  
2.  Á síðunni **XBRL-flokkanir** veljið flokkun af listanum.  
3.  Veljið aðgerðina **Línur**.  
4.  Valin er lína og fyllt út í reitina.   
5.  Nánari upplýsingar um það sem þarf að fylla út fást ef smellt er á aðgerðina **Upplýsingar**.  
6.  Ef setja á upp vörpun fjárhagsreikninga í bókhaldslykli til XBRL-lína er valin aðgerðin **Fjárhagskortslínur**.  
7.  Ef bæta á athugasemd við fjárhagsskýrslu er valin aðgerðin **Athugasemdir**.  

   > [!TIP]
   > Til að útiloka línur úr útflutningi skal velja **Á EKKI VIÐ** sem upprunagerðina.

   > [!NOTE]  
   > Aðeins er hægt að flytja út gögn sem samsvara valinu í reitnum **Tegund uppruna**. Þar á meðal eru lýsingar og athugasemdir.  

   > [!NOTE]  
   > Flokkanir gætu innihaldið einingar sem [!INCLUDE[prod_short](includes/prod_short.md)] styður ekki. Ef eining er ekki studd sýnir reiturinn **Tegund uppruna** **Á ekki við** og reiturinn **Lýsing** sýnir villuboð, á borð við **Óvænt gerð: „ekki borin kennsl á tiltekna gerð“**. Ef það þarf að flytja út eininguna skal velja samsvarandi upprunagerð. Yfirleitt er þetta fasti eða lýsing. Þetta gerir notendum kleift að flytja gögn inn og út, en slíkar einingar gætu verið með villuleitarreglur sem ekki er hægt að athuga fyrir útflutning.

 ## <a name="to-import-an-xbrl-taxonomy"></a>Til að flytja inn XBRL-flokkun  
Fyrsta skrefið þegar beita á XBLR-aðgerðum er að flytja inn flokkunina í gagnagrunn fyrirtækisins. Flokkun er mynduð úr einu eða fleiri skemum og nokkrum tenglagrunnum. Þegar búið er að flytja inn bæði skemu og tenglagrunna og þetta tengt saman er hægt að setja upp línur og varpa fjárhagsreikningum í bókhaldslykli í viðeigandi flokkunarlínur.  

1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **XBRL-flokkanir** og velja síðan viðkomandi tengil.  
2.  Á síðunni **XBRL flokkanir** er búin til ný lína og heiti og lýsing flokkunarinnar færð inn.  
3.  Velja skal aðgerðina **Skemu** og síðan færa inn lýsinguna á skemanum.  
4.  Skema er flutt inn með því að fara á síðuna **XBRL-grindur**, velja þar aðgerðina **Flytja inn** og velja síðan möppu og XSD-skrá. Velja hnappinn **Opna**.  
5.  Tenglagrunnur er fluttur inn með því að fara á síðuna **XBRL-grindur**, velja aðgerðina **Tenglagrunnar** og velja síðan möppu og XML-skrá. Velja hnappinn **Opna**.  
6.  Nú er hægt að tengja tenglagrunninn skemanu. Þetta er endurtekið þar til búið er að flytja inn alla tenglagrunnana.  
7. Velja aðgerðina **Jafna í flokkun** til að tengja tenglagrunninn við skemað.  

> [!IMPORTANT]  
>  Í stað þess að tengja tenglagrunnana hvern um sig þegar innflutningi er lokið er hægt að bíða þar til búið er að flytja inn alla tenglagrunnana og tengja þá síðan alla á sama tíma. Það er gert með því að velja hnappinn **NEI** þegar beðið er um að tenglagrunninum sem verið var að flytja inn sé jafnað við skemað. Síðan skal velja línurnar með tenglagrunnana sem á að notast við.  

## <a name="to-update-an-xbrl-taxonomy"></a>Til að uppfæra XBRL-flokkun  
Þegar flokkun breytist þarf að uppfæra gildandi flokkun samkvæmt því. Ástæða uppfærslunnar getur verið breytt skema, breyttur tenglagrunnur eða nýr tenglagrunnur. Þegar flokkunin hefur verið uppfærð þarf aðeins að varpa línunum vegna nýju eða breyttu línanna.  

1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **XBRL-flokkanir** og velja síðan viðkomandi tengil.  
2.  Á síðunni **XBRL-flokkun** skal velja aðgerðina **Skemu**.  
3.  Til að uppfæra skema, er skemað sem á að uppfæra valið og síðan aðgerðin **Flytja inn**.  
4.  Til að uppfæra eða bæta við nýjum tenglagrunni skal velja **Tenglagrunnar** aðgerðina.  
5.  Valinn er viðeigandi tenglagrunnur eða stutt á Ctrl+N til að fá nýja línu, tegund tenglagrunns valin og lýsing því næst sett inn.  
6.  Til að flytja inn tenglagrunninn skal velja aðgerðina **Flytja inn**.  
7.  Velja **Já** til að tengja tenglagrunninn við skemað.  

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/xbrl-reports-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig
[Fjármál](finance.md)    
[Viðskiptaupplýsingar](bi.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]