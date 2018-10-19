---
title: "Hvernig skal stofna skýrslur með XBRL | Microsoft Docs"
description: "XBRL (eXtensible Business Reporting Language) er XML-miðað tölvumál fyrir viðskiptaskýrslugerð og gerir fyrirtækjum kleift að vinna úr og deila gögnum sínum á árangursríkan og nákvæman hátt."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: f14191eb0a7b7564f5079a53bd90dfc39f176326
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="create-reports-with-xbrl"></a>Stofna skýrslur með XBRL
XBRL (eXtensible Business Reporting Language) er XML-miðað tölvumál fyrir viðskiptaskýrslugerð og gerir fyrirtækjum kleift að vinna úr og deila gögnum sínum á árangursríkan og nákvæman hátt. XBRL-áætlunin býður fjölda hugbúnaðarfyrirtækja sem framleiða bókhalds- og áætlunarkerfi og alþjóðlegum endurskoðendafyrirtækum altæka viðskiptaskýrslugerð. Markmið áætlunarinnar er að búa til staðal fyrir samræmda skýrslugerð viðskiptaupplýsinga fyrir banka, fjárfesta og ríkisstofnanir. Slíkar viðskiptaskýrslur geta falið í sér eftirfarandi atriði:  

 • Ársreikninga  
 • Viðskiptatengdar upplýsingar  
 • Upplýsingar sem eru ekki viðskiptatengdar  
 • Reglubundna skráningu, eins og ársreikninga og ársfjórðungsreikninga  

 [!INCLUDE[d365fin](includes/d365fin_md.md)] gerir fyrirtækjum kleift að breyta gögnum í XBRL og njóta þess hagræðis sem fylgir sveigjanleika og sjálfvirkni við að safna gögnum og deila þeim.  

## <a name="extensible-business-reporting-language"></a>eXtensible Business Reporting Language (XML-miðað tölvumál fyrir viðskiptaskýrslugerð)
XBRL (e **X**tensible **B**usiness **R**eporting **L**anguage) er XML-miðað tölvumál fyrir viðskiptaskýrslugerð. Með XBRL fæst staðall til samræmdrar skýrslugerðar fyrir alla notendur fjárhagslegra upplýsinga, svo sem opinber fyrirtæki og fyrirtæki í einkaeign, endurskoðendur, eftirlitsaðila, þá sem starfa við greiningu, fjárfesta, fjármagnsmarkaði og lánastofnanir, ennfremur aðra aðila, til dæmis forritara og þá sem starfa við gagnasöfn.  

Flokkunum er haldið við á www.xbrl.org. Hægt er að sækja flokkanir eða fá nánari upplýsingar á XBRL-vefsetrinu.  

Aðili sem vill skiptast á fjárhagslegum upplýsingum við notandann lætur hann hafa flokkun XML skjal með einu eða fleiri skemum, sem hvert er með einni eða tveimur línum til að fylla út. Línurnar samsvara einstökum fjárhagslegum upplýsingum sem sá sem sendir krefst þess að fá. Flokkunin er flutt inn í forritið og skemað eða skemun fyllt út með því að færa inn reikninginn eða reikningana sem eiga við hverja línu og hvaða tímamörk skuli nota, t.d. nettóbreytingu eða stöðu til dags. Í sumum tilvikum er hægt að færa inn fasta í stað, t.d., starfsmannafjölda. Nú er hægt að senda tilviksskjalið (XML-skjal) til aðilans sem bað um upplýsingarnar. Hugmyndin er að þetta gæti verið endurtekið tilvik svo að ekki séu flutt út ný tilviksskjöl fyrir ný tímabil nema beðið sé um það.  

## <a name="xbrl-is-comprised-of-the-following-components"></a>XBRL er myndað úr eftirfarandi hlutum  
XBRL **lýsingin** útskýrir hvað XBRL er og hvernig XBRL tilviksskjöl og flokkanir eru byggð upp. XBRL-lýsingin útskýrir XBRL með tæknilegum hugtökum og er fyrir tæknifólk.  

XBRL **skemun** eru grunnhlutar XBRL. Skemað er XSD-raunskráin sem lýsir því hvernig byggja á upp tilviksskjöl og flokkanir.  

XBRL- **tenglagrunnarnir** eru XML-raunskrárnar sem í eru ýmsar upplýsingar um einingarnar sem er að finna í XBRL-skemanu, svo sem merki á einu eða fleiri málum, hvernig þau tengjast, hvernig leggja á saman einingar o.s.frv.  

XBRL **flokkun** er "orðalisti" eða "orðabók" búin til í samvinnu og samhæf XBRL-lýsingunni og notuð til að skiptast á viðskiptaupplýsingum.  

XBRL **Tilviksskjal** er viðskiptaskýrsla, t.d. ársreikningur, sem gerður er samkvæmt XBRL-lýsingu. Merking gildanna í tilviksskjalinu er útskýrð í flokkuninni. Tilviksskjal er gagnslítið nema maður þekki flokkunina sem það er útbúið eftir.  

## <a name="layered-taxonomies"></a>Lagskiptar flokkanir  
Flokkun getur verið sett saman úr grunnflokkun, t.d. us-gaap eða IAS, og haft einn eða fleiri viðauka. Þetta er endurspeglað með því að flokkun vísar til eins eða fleiri skema sem öll eru sérstakar flokkanir. Þegar viðbótarflokkanirnar eru settar inn í gagnagrunninn er nýju einingunum einfaldlega bætt aftan við fyrirliggjandi einingar.  

## <a name="linkbases"></a>Tenglagrunnar  
 Í XBRL lýsingu 2 er flokkuninni lýst í nokkrum XML-skrám. Aðal-XML-skráin er flokkunarskemaskráin sjálf (.xsd-skrá) sem í er aðeins óraðaður listi eininga eða staðreynda sem eiga að vera í skýrslunni. Þessu til viðbótar eru yfirleitt tengdar tenglagrunnsskrár (.xml). Í tenglagrunnsskránum eru gögn sem eru nauðsynleg fyrir flokkunarskemaskrána (.xsd-skrána). Til eru sex tegundir tenglagrunnsskráa og fjórar þeirra eru notaðar í afurðarheiti XBRL. Þær eru:  

-   Merkjatenglagrunnur: í þessum tenglagrunni eru merki eða heiti einingar. Skráin kann að innihalda merki á mismunandi tungumálum sem eru auðkennd með XML-eiginleikanum sem kallast 'lang'. XML-tungumálskenni innihalda venjulega tveggja stafa skammstöfun og þó að auðvelt sé að giska á hvað skammstöfunin þýðir er engin tenging við Windows-tungumálakóðann eða tungumálakóðana sem skilgreindir eru í sýndargögnunum. Þegar notandi flettir upp tungumálunum fyrir tiltekna flokkun getur hann því séð allar merkingarnar fyrir fyrstu eininguna í flokkuninni, sem þýðir að hann sér dæmi fyrir hvert tungumál. Flokkun getur haft nokkur merkistenglagrunna tengda honum ef þessir tenglagrunnar innihalda ólík tungumál.  

-   Tenglagrunnur framsetningar Í þessum tenglagrunni eru upplýsingar um skipan eininganna, eða nánar tiltekið, hvernig útgefandi flokkunarinnar leggur til að forritið setji flokkunina fram fyrir notandann. Tenglagrunnurinn inniheldur röð tengla sem hver tengir tvær einingar sem yfir- og undireiningu. Þegar öllum tenglunum er beitt má sjá einingarnar í stigveldisröð. Athuga skal að tenglagrunnur framsetningar snýst aðeins um þetta: framsetningu eininga fyrir notandann.  

-   Tenglagrunnur útreikninga: Í þessum tenglagrunni eru upplýsingar um það hvaða einingar eru lagðar saman úr hverjum. Skipanin er nauðalík þeirri sem er á tenglagrunni framsetningar, nema að hver tengill eða 'ör', eins og þeir eru kallaðir, hefur vægiseiginleika. Vægið getur verið 1 eða -1 eftir því hvort einingunni skuli bætt við eða hún dregin frá yfireiningu sinni. Athuga skal að samtölurnar þurfa ekki endilega að samræmast sýnilegri framsetningu.  

-   Tilvísunartenglagrunnur: Þessi tenglagrunnur er xml-skrá sem inniheldur viðbótarupplýsingar um gögnin sem krafist er af útgefanda flokkunarinnar.

## <a name="to-set-up-xbrl-lines"></a>XBRL línur settar upp  
Þegar búið er að flytja flokkunina inn eða uppfæra hana verður að setja nauðsynlegar upplýsingar í skemalínurnar. Meðal þessara upplýsinga eru grunnupplýsingar um fyrirtækið, réttir ársreikningar, athugasemdir við ársreikninga, viðbótarskemu og aðrar upplýsingar sem krafist er við skýrslugerðina.  

XBRL-línur eru settar upp með því að varpa gögnum úr flokkuninni í gögn í fjárhag.  

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **XBRL-flokkanir** og veldu síðan tengda tengilinn.  
2.  Í glugganum **XBRL-flokkanir** veljið flokkun af listanum.  
3.  Veljið aðgerðina **Línur**.  
4.  Valin er lína og fyllt út í reitina.   
5.  Nánari upplýsingar um það sem þarf að fylla út fást ef smellt er á aðgerðina **Upplýsingar**.  
6.  Ef setja á upp vörpun fjárhagsreikninga í bókhaldslykli til XBRL-lína er valin aðgerðin **Fjárhagskortslínur**.  
7.  Ef bæta á athugasemd við fjárhagsskýrslu er valin aðgerðin **Athugasemdir**.  

> [!NOTE]  
>  Aðeins er hægt að flytja út gögn sem samsvara því sem hefur verið valið í reitnum **Tegund uppruna**, þar á meðal lýsingu og athugasemdir.  

> [!NOTE]  
>  Línur sem ekki skipta máli er hægt að merkja sem línutegund **Á EKKI VIÐ** og eru þá ekki fluttar út.

 ## <a name="to-import-an-xbrl-taxonomy"></a>Til að flytja inn XBRL-flokkun  
Fyrsta skrefið þegar beita á XBLR-aðgerðum er að flytja inn flokkunina í gagnagrunn fyrirtækisins. Flokkun er mynduð úr einu eða fleiri skemum og nokkrum tenglagrunnum. Þegar búið er að flytja inn bæði skemu og tenglagrunna og þetta tengt saman er hægt að setja upp línur og varpa fjárhagsreikningum í bókhaldslykli í viðeigandi flokkunarlínur.  

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **XBRL-flokkanir** og veldu síðan tengda tengilinn.  
2.  Í glugganum **XBRL flokkanir** er búin til ný lína og heiti og lýsing flokkunarinnar færð inn.  
3.  Velja skal aðgerðina **Skemu** og síðan færa inn lýsinguna á skemanum.  
4.  Skema er flutt inn með því að fara í gluggann **XBRL-grindur**, velja þar aðgerðina **Flytja inn** og velja síðan möppu og XSD-skrá. Velja hnappinn **Opna**.  
5.  Tenglagrunnur er fluttur inn með því að fara í gluggann **XBRL-grindur**, velja aðgerðina **Tenglagrunnar** og velja síðan möppu og XML-skrá. Velja hnappinn **Opna**.  
6.  Nú er hægt að tengja tenglagrunninn skemanu. Þetta er endurtekið þar til búið er að flytja inn alla tenglagrunnana.  
7. Velja aðgerðina **Jafna í flokkun** til að tengja tenglagrunninn við skemað.  

> [!IMPORTANT]  
>  Í stað þess að tengja tenglagrunnana hvern um sig þegar innflutningi er lokið er hægt að bíða þar til búið er að flytja inn alla tenglagrunnana og tengja þá síðan alla á sama tíma. Það er gert með því að velja hnappinn **NEI** þegar beðið er um að tenglagrunninum sem verið var að flytja inn sé jafnað við skemað. Síðan skal velja línurnar með tenglagrunnana sem á að notast við.  

## <a name="to-update-an-xbrl-taxonomy"></a>Til að uppfæra XBRL-flokkun  
Þegar flokkun breytist þarf að uppfæra gildandi flokkun samkvæmt því. Ástæða uppfærslunnar getur verið breytt skema, breyttur tenglagrunnur eða nýr tenglagrunnur. Þegar flokkunin hefur verið uppfærð þarf aðeins að varpa línunum vegna nýju eða breyttu línanna.  

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **XBRL-flokkanir** og veldu síðan tengda tengilinn.  
2.  Í glugganum **XBRL-flokkun** skal velja aðgerðina **Skemu**.  
3.  Til að uppfæra skema, er skemað sem á að uppfæra valið og síðan aðgerðin **Flytja inn**.  
4.  Til að uppfæra eða bæta við nýjum tenglagrunni skal velja **Tenglagrunnar** aðgerðina.  
5.  Valinn er viðeigandi tenglagrunnur eða stutt á Ctrl+N til að fá nýja línu, tegund tenglagrunns valin og lýsing því næst sett inn.  
6.  Til að flytja inn tenglagrunninn skal velja aðgerðina **Flytja inn**.  
7.  Velja **Já** til að tengja tenglagrunninn við skemað.  

## <a name="see-also"></a>Sjá einnig
[Fjármál](finance.md)    
[Viðskiptaupplýsingar](bi.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

