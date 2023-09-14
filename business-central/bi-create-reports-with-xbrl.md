---
title: Hvernig á að Stofna skýrslur með XBRL
description: XBRL er XML-miðað tölvumál til að merkja fjárhagsgögn og gera fyrirtækjum kleift að vinna úr og deila gögnum sínum á árangursríkan og nákvæman hátt.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/14/2022
ms.author: bholtorf
---
# Stofna skýrslur með XBRL

> [!NOTE]
> Verið er að fjarlægja eiginleika fyrir XBRL-skýrslugerð úr [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar á [Breytingar í 2022 útgáfutímabili 1](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1).

XBRL (e**X**tensible **B**usiness **R**eporting **L**anguage) er tungumál, byggt á XML (eXtensible Markup Language), til að merkja fjárhagsgögn, sem gerir fyrirtækjum kleift að vinna úr og deila gögnum sínum á skilvirkan og nákvæman hátt. XBRL-áætlunin býður fjölda hugbúnaðarfyrirtækja sem framleiða bókhalds- og áætlunarkerfi (ERP) og alþjóðlegum endurskoðendafyrirtækum altæka viðskiptaskýrslugerð. Markmið áætlunarinnar er að búa til staðal fyrir samræmda skýrslugerð viðskiptaupplýsinga fyrir banka, fjárfesta og ríkisstofnanir. Slíkar viðskiptaskýrslur geta falið í sér eftirfarandi atriði:  

* Fjárhagsskýrslur  
* Fjárhagsupplýsingar  
* Upplýsingar sem ekki eru fjárhagslegar  
* Reglubundna skráningu, eins og ársreikninga og ársfjórðungsreikninga  

> [!NOTE]
> Hægt er að flytja inn fjárhagstengd skema og búa til XBRL-tilviksskjöl með því að varpa fjárhagsgögnum úr fjárhag yfir í einingar í flokkunum sem voru hannaðar fyrir fjárhagsskýrslur á borð við efnahagsreikninga, rekstrarreikninga og svo framvegis.
>
> XBRL-möguleikarnir í Business Central styðja flokkunarfræði fyrir forskrift 2.1. Hins vegar getur flokkunarfræði innihaldið óstudda þætti á borð við tenglagrunna formúlu eða iXBRL (innfellt XBRL) eða verið með annars konar skipulagsþætti. Mælt er með því að villuleita XBRL-möguleikann áður en hann er notaður í skýrslugerð.
>
> Fullur stuðningur við flokkunarfræði gæti þurft XBRL-merkingu og verkfæri þriðja aðila. Alþjóðleg stofnun XBRL er með lista yfir verkfæri og þjónustu; en það fer eftir tilkynningakröfum XBRL fyrir tiltekna flokkunarfræði hvort þú viljir kanna þessi úrræði. Frekari upplýsingar er að finna í [Hafist handa fyrir Business](https://go.microsoft.com/fwlink/?linkid=2153466) og [Verkfæri og þjónusta](https://go.microsoft.com/fwlink/?linkid=2153356).

## eXtensible Business Reporting Language (XML-miðað tölvumál fyrir viðskiptaskýrslugerð)

XBRL-flokkunum er haldið við á www.xbrl.org. Hægt er að sækja flokkanir eða fá nánari upplýsingar á XBRL-vefsetrinu.  

Segjum að einhver vilji fjárhagsupplýsingar frá þér. Þau lát þig hafa flokkun XML skjal með einu eða fleiri skemum, sem hvert er með einni eða tveimur línum til að fylla út. Línurnar samsvara einstökum fjárhagslegum upplýsingum sem sá sem sendir krefst þess að fá. Þú flytur þessa flokkunarfræði inn, fyllir síðan út skemað/skemun með því að slá inn reikning(a) sem passar við hverja línu þar sem útreikningur er réttur, t.d. nettóbreyting eða staða við dagsetningu. Í sumum tilvikum er hægt að færa inn fasta í stað, t.d., starfsmannafjölda. Nú er hægt að senda tilviksskjalið (XML-skjal) til aðilans sem bað um það. Hugmyndin er að þetta gæti verið endurtekið tilvik svo að ekki séu flutt út ný tilviksskjöl fyrir ný tímabil nema beðið sé um það.

## XBRL samanstendur af eftirfarandi hlutum

XBRL **lýsingin** útskýrir hvað XBRL er og hvernig XBRL tilviksskjöl og XBRL-tilviksskjöl eru byggð upp. XBRL-lýsingin útskýrir XBRL með tæknilegum hugtökum og er fyrir tæknifólk.  

XBRL **skemun** eru grunnhlutar XBRL. Skemað er XSD-raunskráin (kallast líka XML-skemaskilgreining) sem sýnir hvernig XBRL-tilviksskjöl og flokkunarfræði eru búin til.

XBRL- **tenglagrunnarnir** eru XML-raunskrárnar sem í eru upplýsingar um einingarnar sem er að finna í XBRL-skemanu, svo sem merki á einu eða fleiri málum, hvernig þau tengjast, hvernig leggja á saman einingar o.s.frv.  

XBRL **flokkun** er „orðalisti“ eða „orðabók“ sem hópur býr til, sem samhæfist við XBRL-forskrift, sem gerir kleift að skiptast á viðskiptaupplýsingum.  

XBRL **Tilviksskjal** er viðskiptaskýrsla, t.d. ársreikningur, sem gerður er samkvæmt XBRL-lýsingu. Merking gildanna í tilviksskjalinu er útskýrð í flokkuninni. Tilviksskjal er í reynd gagnslítið nema maður þekki flokkunina sem það er útbúið eftir.  

## Lagskiptar flokkanir

Flokkun getur samanstaðið af grunnflokkun, t.d. US GAAP (almennt samþykktar bókhaldsreglur í Bandaríkjunum) eða IAS (alþjóðlegir bókhaldsstaðlar) og verið síðan með eina eða fleiri viðbætur. Þetta er endurspeglað með því að flokkun vísar til eins eða fleiri skema þar sem öll eru sérstakar flokkanir. Þegar viðbótarflokkanirnar eru settar inn í gagnagrunninn er nýju einingunum einfaldlega bætt aftan við fyrirliggjandi einingar.  

## Tenglagrunnar

Í XBRL lýsingu 2 er flokkuninni lýst í nokkrum XML-skrám. Aðal-XML-skráin er flokkunarskemaskráin sjálf (.xsd-skrá) sem í er aðeins óraðaður listi eininga eða staðreynda sem eiga að vera í skýrslunni. Þessu til viðbótar eru yfirleitt tengdar tenglagrunnsskrár .xml. Í tenglagrunnsskránum eru gögn sem eru nauðsynleg fyrir flokkunarskemaskrána .xsd-skrána. Til eru sex tegundir tenglagrunnsskráa og fjórar þeirra eru notaðar í [!INCLUDE[prod_short](includes/prod_short.md)]. Þær eru:

* Merkjatenglagrunnur: í þessum tenglagrunni eru merki eða heiti einingar. Skráin kann að innihalda merki á mismunandi tungumálum sem eru auðkennd með XML-eiginleikanum sem kallast 'lang'. XML-tungumálskenni innihalda venjulega tveggja stafa skammstöfun og þó að auðvelt sé að giska á hvað skammstöfunin þýðir er engin tenging við Microsoft Windows-tungumálakóðann eða tungumálakóðana sem skilgreindir eru í sýndargögnunum. Þegar þú flettir upp tungumálunum fyrir tiltekna flokkun geturðu séð allar merkingarnar fyrir fyrstu eininguna í flokkuninni, sem þýðir að þú getur séð dæmi fyrir hvert tungumál. Flokkun getur haft nokkur merkistenglagrunna tengda honum ef þessir tenglagrunnar innihalda ólík tungumál.  
* Tenglagrunnur framsetningar: Í þessum tenglagrunni eru upplýsingar um skipan eininganna, eða nánar tiltekið, hvernig útgefandi flokkunarinnar leggur til að forritið setji flokkunina fram fyrir notandann. Tenglagrunnurinn inniheldur röð tengla sem hver tengir tvær einingar í tengslum yfireiningar-undireiningar. Þegar öllum tenglunum er beitt má sjá einingarnar í stigveldisröð. Athuga skal að tenglagrunnur framsetningar snýst aðeins um þetta: framsetningu eininga fyrir notandann.
* Tenglagrunnur útreiknings: Í þessum tenglagrunni eru upplýsingar um hvernig einingarnar raðast saman. Skipanin er nauðalík þeirri sem er á tenglagrunni framsetningar, nema að hver tengill eða 'ör', eins og þeir eru kallaðir, hefur vægiseiginleika. Vægið getur verið 1 eða -1 eftir því hvort einingunni skuli bætt við eða hún dregin frá yfireiningu sinni. Athuga skal að samtölurnar þurfa ekki endilega að samræmast sýnilegri framsetningu.  
* Tilvísunartenglagrunnur: Þessi tenglagrunnur er xml-skrá sem inniheldur viðbótarupplýsingar um gögnin sem krafist er af útgefanda flokkunarinnar.

## Etja upp XBRL línur

Þegar búið er að flytja flokkunina inn eða uppfæra hana verður að fylla út línur skemanna með ölllum upplýsingum sem þarf til að uppfylla tilteknar kröfur fjárhagsskýrslugerðar. Þessar upplýsingar fela í sér grunnupplýsingar fyrirtækisins, raunverulegar fjárhagsskýrslur, athugasemdir við fjárhagsskýrslur, viðbótaráætlanir og svo framvegis.  

XBRL-línur eru settar upp með því að varpa gögnum úr flokkuninni í gögn í fjárhag.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **XBRL-flokkanir** og velja síðan viðkomandi tengil.  
2. Á síðunni **XBRL-flokkanir** veljið flokkun af listanum.  
3. Veljið aðgerðina **Línur**.  
4. Valin er lína og fyllt út í reitina.  
5. Nánari upplýsingar um það sem þarf að fylla út fást ef smellt er á aðgerðina **Upplýsingar**.  
6. Ef setja á upp vörpun fjárhagsreikninga í bókhaldslykli til XBRL-lína er valin aðgerðin **Fjárhagsvörpunarlínur**.  
7. Ef bæta á athugasemd við fjárhagsskýrslu er valin aðgerðin **Athugasemdir**.  

   > [!TIP]
   > Til að útiloka línur úr útflutningi gagna skal velja **Á EKKI VIÐ** sem upprunagerðina.

   > [!NOTE]  
   > Aðeins er hægt að flytja út gögn sem samsvara valinu í reitnum **Tegund uppruna**. Þar á meðal eru lýsingar og athugasemdir.  

   > [!NOTE]  
   > Flokkanir gætu innihaldið einingar sem [!INCLUDE[prod_short](includes/prod_short.md)] styður ekki. Ef eining er ekki studd sýnir reiturinn **Tegund uppruna** **Á ekki við** og reiturinn **Lýsing** sýnir villuboð, á borð við **Óvænt gerð: „ekki borin kennsl á tiltekna gerð“**. Ef það þarf að flytja út eininguna skal velja samsvarandi upprunagerð. Yfirleitt er þetta fasti eða lýsing. Þetta gerir notendum kleift að flytja gögn inn og út, en slíkar einingar gætu verið með villuleitarreglur sem ekki er hægt að athuga fyrir útflutning.

## Flytja inn XBRL-flokkun

Fyrsta skrefið þegar beita á XBLR-aðgerðum er að flytja inn flokkun í gagnagrunn fyrirtækisins. Flokkun er mynduð úr einu eða fleiri skemum og nokkrum tenglagrunnum. Þegar búið er að flytja inn bæði skemu og tenglagrunna og þetta tengt saman er hægt að setja upp línur og varpa fjárhagsreikningum í bókhaldslykli í viðeigandi flokkunarlínur.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **XBRL-flokkanir** og velja síðan viðkomandi tengil.  
2. Á síðunni **XBRL flokkanir** er búin til ný lína og heiti og lýsing flokkunarinnar færð inn.  
3. Velja skal aðgerðina **Skemu** og síðan færa inn lýsinguna á skemanum.  
4. Ef flytja á skemað inn, á  **XBRL-skemanu**  síðan, skal velja  **aðgerðina Flytja**, og gera síðan eftirfarandi til að senda skrána:

   [!INCLUDE[file-upload](includes/file-upload.md)]
5. Ef flytja á tenglagrunninn á  **síðunni XBRL-skemill**  skal velja  **tenglagrunnaðgerðina**  og gera eina af eftirfarandi skrefum til að senda skrána:

   [!INCLUDE[file-upload](includes/file-upload.md)] 
6. Nú er hægt að tengja tenglagrunninn skemanu. Þetta er endurtekið þar til búið er að flytja inn alla tenglagrunnana.  
7. Velja aðgerðina **Jafna í flokkun** til að tengja tenglagrunninn við skemað.  

> [!IMPORTANT]  
> Í stað þess að tengja tenglagrunnana hvern um sig þegar innflutningi er lokið er hægt að bíða þar til búið er að flytja inn alla tenglagrunnana og tengja þá síðan alla á sama tíma. Það er gert með því að velja **NEI** þegar beðið er um að tenglagrunninum sem verið var að flytja inn sé jafnað við skemað. Síðan skal velja línurnar með tenglagrunnana sem á að notast við.  

## Uppfæra XBRL-flokkun

Þegar flokkun breytist þarf að uppfæra gildandi flokkun samkvæmt því. Ástæða uppfærslunnar getur verið breytt skema, breyttur tenglagrunnur eða nýr tenglagrunnur. Þegar flokkunin hefur verið uppfærð þarf aðeins að varpa línunum vegna nýju eða breyttu línanna.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **XBRL-flokkanir** og velja síðan viðkomandi tengil.  
2. Á síðunni **XBRL-flokkun** skal velja aðgerðina **Skemu**.  
3. Til að uppfæra skema, er skemað sem á að uppfæra valið og síðan aðgerðin **Flytja inn**.  
4. Til að uppfæra eða bæta við nýjum tenglagrunni skal velja **Tenglagrunnar** aðgerðina.  
5. Velja skal viðeigandi tengbase eða velja  <kbd>CTRL</kbd>+<kbd>N</kbd>  fyrir nýja línu, velja gerð tengbase og setja inn lýsingu.  
6. Til að flytja inn tenglagrunninn skal velja aðgerðina **Flytja inn**.  
7. Veldu **Já** til að nota tenglagrunninn á skemað.  

## Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/xbrl-reports-dynamics-365-business-central/index).

## Sjá einnig .

[Viðskiptagreind fjármála](bi.md)  
[Fjármál](finance.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
