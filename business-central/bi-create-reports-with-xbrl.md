---
title: Hvernig á að Stofna skýrslur með XBRL
description: XBRL er XML-miðað tölvumál til að merkja fjárhagsgögn og gera fyrirtækjum kleift að vinna úr og deila gögnum sínum á árangursríkan og nákvæman hátt.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 09/14/2022
ms.author: edupont
ms.openlocfilehash: 3aabe61906cd6b8111a3fcadb616a4cdfae6277c
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9605300"
---
# <a name="create-reports-with-xbrl"></a>Stofna skýrslur með XBRL

> [!NOTE]
> Við erum að vinna í því að fjarlægja aðgerðirnar fyrir XBRL skýrslugerð [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar á [breytingum í 2022 1](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1).

XBRL (e **X** heilsuverndarstöðvar **B** usiness **R** eporting **L** -mál) er tungumál, Byggt á extensible markmáli (XML), til merkinga á fjárhagslegum gögnum, sem gera fyrirtækjum kleift að gera betur og nákvæmlega upp ferli og deila gögnum sínum. XBRL-frumátt gerir altækar fjárhagsskýrslur með því að hafa fjölmörg Enterprise Resource áætlunarflug (ERP) hugbúnaðarfyrirtæki og alþjóðleg bókhaldsfélög. Markmið frumvarpsins er að veita staðlað fyrir samræmda skýrslugjöf um fjárhagsupplýsingar til banka, fjárfesta og stjórnvalda. Slíkar viðskiptaskýrslur geta falið í sér eftirfarandi atriði:  

* Ársreikningur  
* Fjárhagsupplýsingar  
* Ófjárhagslegum upplýsingum  
* Regluvörslu, s.s. ársreikninga og ársfjórðungslega ársreikninga  

> [!NOTE]
> Hægt er að flytja inn almennar bókartengdar skemu og stofna XBRL-tilviksskjöl með því að varpa fjárhag (fjárhags-) gögnum í bókhaldslykla til eininga í Flokkanir sem eru hannaðar fyrir ársskýrslur, eins og efnahagsyfirlit, rekstraryfirlit o. s. frv.
>
> XBRL-hæfni í flokkanir í Aðalstuðningsmáta fyrir lýsingu 2,1. Hins vegar geta Flokkanir innihaldið Óstuddir þættir eins og formúlutenglagrunn eða iXBRL (innfærslur XBRL) eða aðrir skipulagsmunir. Mælt er með því að villuleita XBRL-getu áður en hann er notaður til skýrslugerðar.
>
> Allur stuðningur við Flokkanir gæti krafist XBRL-merkinga og verkfæra frá þriðja aðila. XBRL International-fyrirtækið er með lista yfir tól og þjónustur; eftir því sem kröfur XBRL-gerðar eru gefnar upp í tiltekinni flokkun er hugsanlegt að kanna þær auðlindir. Lærðu meira [að byrja fyrir viðskipti](https://go.microsoft.com/fwlink/?linkid=2153466) og [tól og þjónustu](https://go.microsoft.com/fwlink/?linkid=2153356).

## <a name="extensible-business-reporting-language"></a>eXtensible Business Reporting Language (XML-miðað tölvumál fyrir viðskiptaskýrslugerð)

www.xbrl.org er viðhaldið XBRL-flokkunum. Hægt er að sækja Flokkanir og lesa ítarlegri upplýsingar á XBRL-vefsvæðinu.  

Segjum að einhver vilji fjárhagslegar upplýsingar frá þér. Þær veita þér flokkun (XML-skjal) sem inniheldur eitt eða fleiri skemu, hvert með eina eða fleiri línur til að fylla út. Línurnar samsvara einstökum fjárhagslegum staðreyndum sem sendandi krefst. Þessi flokkun er flutt inn og síðan er skemað fyllt út með því að færa inn reikningana sem samsvara hverri línu og hvaða útreikningar eru þrálátir, eins og hreyfing eða staða til dags. Í sumum tilfellum er hægt að slá föstu í staðinn, t.d. vegna fjölda starfsmanna. Nú er hægt að senda tilviksskjalið (XML-skjal) til aðilans sem bað um það. Hugmyndin er að þetta gæti verið endurtekið tilvik svo að ekki séu flutt út ný tilviksskjöl fyrir ný tímabil nema beðið sé um það.

## <a name="xbrl-comprises-the-following-components"></a>XBRL samanstendur af eftirfarandi íhlutum

XBRL **-skilgreiningin** ÚTSKÝRIR hvað XBRL er og hvernig XBRL tilviksskjöl og flokkanir eru byggð upp. XBRL-skilgreiningin útskýrir XBRL í tæknilegum skilmálum og er ætlað tækniáheyranda.  

XBRL **skemun** eru grunnhlutar XBRL. Skemað er efnislegt XSD (einnig kallað XML-skema-Skilgreining) sem tekur með sér hvernig á að byggja XBRL-tilviksskjöl og Flokkanir.

Í XBRL **-tenglagrunnum** eru efnislegar skrár sem innihalda upplýsingar um einingarnar sem eru SKILGREINDAR í XBRL-skemanu, svo sem merki á einu eða fleiri tungumálum, hvernig þær tengjast hver annarri, hvernig á að Samtala einingum og svo framvegis.  

XBRL **-Flokkun** er "Orðalisti" eða "orðabók" útbúin af hópi, sem fylgir XBRL-lýsingunni, sem gerir það að verkum að viðskiptaupplýsingar eru ekki til.  

XBRL **Tilviksskjal** er viðskiptaskýrsla, t.d. ársreikningur, sem gerður er samkvæmt XBRL-lýsingu. Merking gildanna í tilviksskjalinu er útskýrð í flokkuninni. Í rauninni er tilviksskjal nokkuð gagnslaust nema þú þekkir flokkunina sem það er útbúið fyrir.  

## <a name="layered-taxonomies"></a>Skordýr flokkades

Flokkun getur verið samsett úr grunnflokkun, til dæmis okkur GAAP (Bandaríkin samþykkja almennt bókhaldsreglur) eða IAS (International Reikningsskilastaðlar) og hafa síðan einn eða fleiri viðauka. Til að endurspegla þetta vísar flokkunin til einnar eða fleiri skemu, sem hver um sig er aðskilin flokkunum sjálfum. Þegar viðbótarflokkanirnar eru settar inn í gagnagrunninn er nýju einingunum einfaldlega bætt aftan við fyrirliggjandi einingar.  

## <a name="linkbases"></a>Tenglagrunnar

Í XBRL Spec. 2 er flokkuninni lýst í nokkrum XML-skrám. Aðal-XML-skráin er flokkunarskemaskráin sjálf (.xsd-skrá) sem í er aðeins óraðaður listi eininga eða staðreynda sem eiga að vera í skýrslunni. Auk þessa eru yfirleitt nokkrar tenggrunnsskrár (. XML). Í tenggrunnsskránum eru gögn sem eru viðbót við hráflokkunina (. XSD-skrána). Það eru sex tegundir tenglagrunna-skráa sem fjórar hafa mikilvægi fyrir [!INCLUDE[prod_short](includes/prod_short.md)]. Þær eru:

* Merkjatenglagrunnur: í þessum tenglagrunni eru merki eða heiti einingar. Skráin kann að innihalda merki á mismunandi tungumálum sem eru auðkennd með XML-eiginleikanum sem kallast 'lang'. Kenni XML-tungumáls inniheldur yfirleitt tveggja bókstafa skammstöfun og þó svo að auðvelt sé að giska á hvað skammstöfunin þýðir er engin tenging við Microsoft Windows tungumálakóta eða tungumálakótana sem skilgreindir eru í sýnigögnunum. Því þegar tungumálin eru flett upp fyrir ákveðinni flokkun þá sjást öll merki fyrsta einingarinnar í flokkuninni, sem þýðir að hægt er að sjá dæmi um hvert tungumál. Hægt er að tengja flokkun við margar merkjatenglagrunna svo framarlega sem þær tenglagrunna innihalda ólík tungumál.  
* Kynning tengbase: Þessi tenggrunnur inniheldur upplýsingar um uppbyggingu eininga eða, nánar hvernig útgefandi flokkunar leggur til að forritið kynnir flokkun á þér. Tenglagrunnurinn inniheldur röð tengla sem hver tengir tvo þætti í sambandi við vensl foreldris-barns. Þegar öllum tenglunum er beitt má sjá einingarnar í stigveldisröð. Athygli er vakin á því að í kynningarlinkunni er fjallað um bara: framsetningu eininga til þín.
* Reiknigrunnur útreiknings: í tengrunni eru upplýsingar um hvernig einingarnar rúlla upp. Skipulagið er nokkuð svipað og í kynningartenglinum, nema að hver tengill, eða,, ARC "eins og þeir kallast, hefur þunga eiginleika. Þyngdin getur verið annað hvort 1 eða – 1, sem gefur til kynna hvort bæta eigi einingu við eða draga frá yfirvigt hennar. Athugið að rúllan þarf ekki endilega að samræma við sjónræna framsetningu.  
* Tilvísunartenglagsgrunnur: Þessi tenggrunnur er XML-skrá með fylgiupplýsingum um gögnin sem krafist er af útgefanda flokkunarinnar.

## <a name="set-up-xbrl-lines"></a>Setja upp XBRL-línur

Eftir að búið er að flytja inn eða uppfæra flokkunina verður að fylla út línur skemu með allar upplýsingar sem þarf til að fullnægja tilteknum kröfum fjárhagsskýrslugerðar. Þessar upplýsingar hafa að geyma grunnupplýsingar um fyrirtækið, sjálfa ársreikninginn, athugasemdir við ársreikninginn, viðbótaráætlanir o. þ. frv.  

XBRL-línur eru settar upp með því að varpa gögnunum í flokkunina í gögnin í fjárhag.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **XBRL-flokkun** og velja síðan tengda tengilinn.  
2. Á síðunni **XBRL-flokkanir** veljið flokkun af listanum.  
3. Veljið aðgerðina **Línur**.  
4. Valin er lína og fyllt út í reitina.  
5. Nánari upplýsingar um það sem þarf að fylla út fást ef smellt er á aðgerðina **Upplýsingar**.  
6. Til að setja upp fjárhagsreikninga í bókhaldslykli í XBRL-línum er aðgerðin g. Línuvörpun **valin**.  
7. Ef bæta á athugasemd við fjárhagsskýrslu er valin aðgerðin **Athugasemdir**.  

   > [!TIP]
   > Ef útiloka á línur úr útfluttum gögnum skal velja **sem** upprunagerð.

   > [!NOTE]  
   > Aðeins er hægt að flytja út gögn sem samsvara valinu í reitnum **Tegund uppruna**. Þar á meðal eru lýsingar og athugasemdir.  

   > [!NOTE]  
   > Flokkanir gætu innihaldið einingar sem [!INCLUDE[prod_short](includes/prod_short.md)] styðja ekki. Ef eining er ekki studd sýnir reiturinn **Tegund uppruna** **Á ekki við** og reiturinn **Lýsing** sýnir villuboð, á borð við **Óvænt gerð: „ekki borin kennsl á tiltekna gerð“**. Ef það þarf að flytja út eininguna skal velja samsvarandi upprunagerð. Yfirleitt er þetta fasti eða lýsing. Með því að gera þetta kleift að færa inn og flytja út gögn gætu slíkar einingar haft villuleitarreglur sem ekki er hægt að athuga áður en útflutningur er gerður.

## <a name="import-an-xbrl-taxonomy"></a>XBRL-flokkun flutt inn

Fyrsta skrefið í vinnu við XBRL-aðgerðina er að flytja inn flokkun inn í gagnagrunn fyrirtækisins. Flokkun er mynduð úr einu eða fleiri skemum og nokkrum tenglagrunnum. Þegar búið er að flytja inn bæði skemu og tenglagrunna og þetta tengt saman er hægt að setja upp línur og varpa fjárhagsreikningum í bókhaldslykli í viðeigandi flokkunarlínur.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **XBRL-flokkun** og velja síðan tengda tengilinn.  
2. Á síðunni **XBRL flokkanir** er búin til ný lína og heiti og lýsing flokkunarinnar færð inn.  
3. **Aðgerðin skemu** er valin, síðan er lýsing á skemanu sett inn.  
4. Ef flytja á skemað inn, á **XBRL-skemanu** síðan, skal velja **innflutningsaðgerðina** og velja síðan möppu og XSD-skrá. Veldu **Opna**.  
5. Ef flytja á tenglagrunninn, á **síðunni XBRL-skemill**, skal velja **tenglagrunnaðgerðina** og velja síðan möppu og XML-skrá. Veldu **Opna**.  
6. Nú er hægt að tengja tenglagrunninn skemanu. Þetta er endurtekið þar til búið er að flytja inn alla tenglagrunnana.  
7. Velja aðgerðina **Jafna í flokkun** til að tengja tenglagrunninn við skemað.  

> [!IMPORTANT]  
> Í stað þess að tengja tenglagrunnana hvern um sig þegar innflutningi er lokið er hægt að bíða þar til búið er að flytja inn alla tenglagrunnana og tengja þá síðan alla á sama tíma. Það er gert með því að velja **Nei** þegar beðið er um að nota nýinnflutta linkingargrunninn í skemað. Síðan skal velja línurnar með tenglagrunnana sem á að notast við.  

## <a name="update-an-xbrl-taxonomy"></a>Uppfæra XBRL-flokkun

Þegar flokkun breytist þarf að uppfæra gildandi flokkun samkvæmt því. Ástæða uppfærslunnar getur verið breytt skema, breyttur tenglagrunnur eða nýr tenglagrunnur. Þegar flokkunin hefur verið uppfærð þarf aðeins að varpa línunum vegna nýju eða breyttu línanna.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **XBRL-flokkun** og velja síðan tengda tengilinn.  
2. Á síðunni **XBRL-flokkun** skal velja aðgerðina **Skemu**.  
3. Skema er uppfært með því að velja skemað sem á að uppfæra og velja **síðan innflutningsaðgerðina**.  
4. Til að uppfæra eða bæta við nýjum tenglagrunni skal velja **Tenglagrunnar** aðgerðina.  
5. Veljið viðeigandi tengbase eða ýtið á CTRL + N fyrir nýja línu, Veljið gerð tenggrunnsins, setjið síðan inn lýsingu.  
6. Til að flytja inn tenglagrunninn skal velja aðgerðina **Flytja inn**.  
7. Velja **skal Já** til að jafna tengbase við grindina.  

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengdar þjálfun kl [Microsoft Learn](/learn/modules/xbrl-reports-dynamics-365-business-central/index).

## <a name="see-also"></a>Sjá einnig .

[Upplýsingarit um Fjármál fyrirtækja](bi.md)  
[Fjármál](finance.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
