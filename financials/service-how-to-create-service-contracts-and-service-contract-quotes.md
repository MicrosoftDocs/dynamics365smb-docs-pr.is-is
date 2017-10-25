---
title: "Hvernig á að: Vinna með þjónustusamninga og þjónustusamningstilboð | Microsoft Docs"
description: "Hægt er að stofna þjónustusamning annað hvort handvirkt eða úr þjónustusamningstilboði. Hægt er að stofna samning út frá samningstilboði."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/29/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: ab8ded6ef2b93c2ab038472609093ef7e5ad3d88
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-work-with-service-contracts-and-service-contract-quotes"></a>Hvernig á að: Vinna með þjónustusamninga og þjónustusamningstilboð
Hægt er að stofna þjónustusamning annað hvort handvirkt eða úr þjónustusamningstilboði. Hægt er að nota þjónustusamningstilboð sem aðdraganda að þjónustusamningi þar sem fyrirtækið gerir viðskiptamanni tilboð og fær samþykki hans svo að unnt sé að breyta tilboðinu í þjónustusamning. Ferlið við stofnun þjónustusamnings annars vegar og þjónustusamningstilboðs er nokkuð svipað.  
  
## <a name="to-create-a-service-contract-or-service-contract-quote"></a>Að stofna þjónustusamning eða þjónustusamningstilboð:  
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Þjónustusamningar** eða **Þjónustusamningstilboð** og velja svo viðeigandi tengil.  
2. Stofna nýjan þjónustusamning eða þjónustusamningstilboð.  
3. Fylla þarf út reitinn **Nr.**. . Þá birtist svargluggi, sem spyr hvort fylla eigi út í reitinn með almennum gögnum úr samningssniðmáti. Ef stofna á slíkan þjónustusamning eða þjónustusamningstilboð er hnappurinn **Já** valinn. Glugginn **Þjónustusamn.sniðmát - Listi** opnast.  
4. Velja skal viðeigandi sniðmát og velja svo **Í lagi** til að nota það til að stofna þjónustusamninginn eða þjónustusamningstilboðið.  
5. Í **Númer viðskiptamanns** reitinn skal velja viðskiptavin.  
6. Ef ekki á að dreifa upphæð ársmismunar sjálfkrafa skal velja **Heimila ójafnaðar upphæðir** gátreitinn. Gildin í reitunum **Árleg upphæð** og **Reiknuð árleg upphæð** eru ekki sjálfkrafa jöfnuð. Ef kerfið á sjálfkrafa að dreifa árlegum mismun sem gæti verið vegna breytingar á þjónustusamningi skal hafa gátreitinn **Heimila ójafnaðar upphæðir** auðan.  
7. Bæta við samningslínum í þjónustusamninginn eða þjónustusamningstilboðið.  
8. Aðrir reitir eru fylltir út eins og þörf er á.  

## <a name="to-convert-a-service-contract-quote-to-service-contract"></a>Þjónustusamningstilboði breytt í þjónustusamning:  
Þegar viðskiptamaður tekur tilboði um þjónustusamning er því breytt í þjónustusamning. Um leið geturðu stofnað þjónustureikning fyrir upphafstímabil samningsins ef upphafsdagsetning hans er fyrr en upphaf næsta reikningstímabils. 

Eftir að þú lýkur eftirfarandi skrefum er þjónustusamningur stofnaður með stöðuna **Undirritað**. Ef þjónustureikningur er stofnaður fyrir upphafstímabil samningsinser reikningsfærð upphæð reiknuð út sem hér segir, eftir því hvort samningurinn er sundurliðaður eða ekki.  
  
Fyrir sundurliðaða samninga er reikningsfærð upphæð reiknuð út á eftirfarandi hátt:  
  
* Reikningsfærð upphæð = samtals reikningsfærð upphæð fyrir hverja samningslínu.  
* Reikningsfærð upphæð vegna hverrar samningslínu = ((tilboðsvirði ÷ 12) × fjöldi mánaða í upphafstímabili) + ((tilboðsvirði ÷ fjöldi daga í ári) × fjöldi daga sem eftir er af upphafstímabili).  
* Ef samningslínan rennur út áður en upphafstímabili lýkur verður lokadagsetningin einnig lokadagsetning upphafstímabilsins í línunni.  
  
Fyrir samninga sem eru ekki sundurliðaðir, er reikningsfærð upphæð reiknuð út á eftirfarandi hátt:  
  
* Reikningsfærð upphæð = (árleg upphæð ÷ fjöldi daga í ári) × fjöldi daga í upphafstímabili.  
* Ef samningslínan rennur út áður en upphafstímabili lýkur verður lokadagsetningin einnig lokadagsetning upphafstímabilsins.    
  
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Þjónustusamningstilboð** og velja svo viðeigandi tengil.  
2. Opna skal þjónustusamningstilboð sem breyta á í þjónustusamning.  
3. Velja **Gera samning** aðgerð.  
4. Ef upphafsdagsetning samningsin er fyrir upphafstímabil næsta reikningstímabils geturðu stofnað þjónustureikning fyrir upphafstímabil samningsins. Velja **Já**.  
  
 Þjónustureikningurinn er bókaður í þjónustureikning samningsins, þó að samningur hafi verið greiddur fyrirfram. 

## <a name="to-create-contract-service-credit-memos"></a>Til að búa til Samningsþjónustukreditreikninga
Samningsþjónustukreditreikninga má nota þegar viðskiptamaður ógildir fyrirframgreiddan þjónustusamning eða tekur þjónustuvöru úr fyrirframgreiddum samningi. Einnig nýtast þeir við að leiðrétta rangan þjónustureikning.  
  
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Þjónustukreditreikningar** og velja svo viðeigandi tengil.  
2. Nýr þjónustukreditreikningur er stofnaður.  
3. Fylla þarf út reitinn **Nr.**. .  
4. Í **Númer viðskiptamanns** reitnum, er ritað númer viðskiptamannsins í þjónustusamninginn.  
  
     Á **Reikningsfæra** sjást upplýsingar sem voru afritaðar af spjaldinu **Viðskiptamaður**. Ef bóka á kreditreikninginn á annan viðskiptamann en þann sem tilgreindur er á flýtiflipanum **Almennt** er fært inn númer þess viðskiptamanns í reitinn **Reikn.færist á viðskm.** reitinn. .  
  
    > [!NOTE]  
    >  Hægt er að bera kreditreikninginn saman við skjalið sem var upphaflega bókað í glugganum **Bókaðir þjónustureikningar**. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Bókaðir þjónustureikningar** og velja svo viðeigandi tengil.  
  
5. Fylltir eru út **Bókunardags.** og **Dagsetning fylgiskjals**.  
6. Í kreditreikningslínurnar eru færðar upplýsingar um vörurnar sem er skilað eða sem eru fjarlægðar, eða uppbót sem á að senda. Hægt er að nota keyrsluna **Sækja fyrirframgreiddar samningsfærslur**.  
  
 Til að stofna handvirkt kreditreikning þegar samningslínur eru fjarlægðar úr þjónustusamningi er farið í gluggann **Þjónustusamningur** , flýtiflipann **Sundurl. reikningur**, skal velja gátreitinn **Sjálfvirkir kreditreikningar**.  
  
 Til að stofna handvirkt kreditreikning þegar samningslínur eru fjarlægðar úr þjónustusamningi er farið í gluggann **Þjónustusamningur**, flipann **Aðgerðir**, flokkinn **Aðgerðir** og **Kreditreikningur** valinn.  

## <a name="updating-and-evaluating-contracts"></a>Uppfærsla og mat á samningum
Stundum þarf að breyta skilmálum samninga eftir að þeir eru stofnaðir. Yfirleitt er viðeigandi samningur opnaður í glugganum **Þjónustusamningur** og viðeigandi breytingar gerðar.  
  
Hægt er að breyta stöðu samningsins, sem í fyrstu er stillt á **Læst**, bæta við og fjarlægja samningslínur og hætta við samning. Hægt er að sjá hvernig fyrirtækið stendur sig hvað varðar gróða og tap með því að fá flýtigreiningu á fyrirtækinu með eiginleikanum framvinda samnings.

## <a name="to-add-a-contract-line-to-a-service-contract-or-contract-quote"></a>Samningslínum bætt við þjónustusamning eða samningstilboð:  
Þegar viðskiptamaður kaupir nýja vöru og vill að hún sé innifalin í þjónustusamningi eða samningstilboði sem til er fyrir er hægt að skrá vöruna sem þjónustuvöru og bæta henni við samninginn eða samningstilboðið sem nýrri samningslínu.  
  
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Þjónustusamningar** og velja svo viðeigandi tengil.  
2. Opna skal viðeigandi þjónustusamning eða þjónustusamningstilboð sem bæta á nýrri samningslínu við.  
3. Veldu aðgerðina **Opna samning** til að opna þjónustusamninginn eða samningstilboðið þannig að hægt sé að gera breytingar.  
4. Á flýtiflipanum **Sundurl. reikningur** skal velja reitinn **Heimila ójafnaðar upphæðir** ef breyta á árlegri upphæð og skipta mismun árlegrar upphæðar handvirkt í samningslínunum. Annars skal hreinsa gátreitinn í reitnum **Heimila ójafnaðar upphæðir**. Það verður til þess að kerfið velur að  skipta mismun árlegrar upphæðar sjálfkrafa í samningslínunum þegar árlegu upphæðinni hefur verið breytt.   
5. Í flýtiflipanum **Línur** er þjónustuvara eða vara, eða textalýsing sett inn í hverja samningslínu. Einnig er hægt að setja inn samningstilboðslínur. Hægt er að stofna marga samninga fyrir hverja þjónustuvöru til að hún verði tekin með í mismunandi þjónustusamningum eða samningstilboðum á sama tíma.  
6. Staðfesta og leiðrétta númerin í reitunum **Línuafsl.%**, **Afsl.upphæð línu**, **Svartími**, **Þjónustutímabil** og öðrum reitum eftir þörfum. 

## <a name="to-remove-contract-lines"></a>Samningslínur fjarlægðar  
Nauðsyn gæti reynst að eyða samningslínum úr þjónustusamningi um leið og samsvarandi þjónustuvörur eru fjarlægðar úr þjónustusamningnum. Yfirleitt er fjarlægð samningslína sem er útrunnin eða sem svarar til þjónustuvörunnar sem hefur bilað.  

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Þjónustusamningar** og velja svo viðeigandi tengil.  
2. Opna skal þjónustusamninginn sem fjarlægja á samningslínur úr.  
3. Veldu aðgerðina **Opna samning** til að opna þjónustusamninginn þannig að hægt sé að gera breytingar.  
4. Veldu samningslínuna sem á að fjarlægja. Fylla inn í reitinn **Samningur útrunninn - dags.** með dagsetningunni þegar á að fjarlægja línuna. T.d. er hægt að færa inn dagsetninguna sem þjónustuvaran bilaði.  
5. Veldu **Fjarlægja línur úr samningi**. Þá opnast glugginn **Fjarlægja línur úr samningi**.  
6. Fylltu út sjálfgefnar síur **Samningsnr.**, afmörkunin **Nr. þjónustuvöru** og afmörkunin **Tegund samnings**. Ef þörf krefur er hægt að setja fleiri afmarkanir eða breyta þeim sem fyrir eru.  
7. Reitirnir á flýtiflipanum **Valkostir** eru fylltir út. Í reitnum **Aðgerð** er valið að **Eyða línum**.  
  
> [!NOTE]  
>  Ef samningurinn er ekki sundurliðaður þarf að uppfæra virðið í reitnum **Árleg upphæð** á flýtiflipanum **Sundurl. reikningur** í glugganum **Þjónustusamningur** svo að ljóst sé að þjónustuvaran hafi fallið út úr samningnum.  
>   
>  Ef samningurinn er sundurliðaður og fyrirframgreiddur og búið er að bóka reikninga vegna hans er hægt að búa til kreditreikning fyrir samninginn. Í flipanum **Aðgerðir** í flokknum **Eiginleikar** veljið **Stofna kreditreikning**. Þetta er óþarfa ef gátreiturinn í reitnum **Sjálfv. kreditreikningar** í flýtiflipanum **Reikningsupplýsingar** er valinn. Í því tilviki er kreditreikningur stofnaður sjálfkrafa næst þegar samningslína er fjarlægð. 

## <a name="service-line-cost-and-value"></a>Kostnaður og gildi þjónustulínu
Á þjónustusamningslínum eru upphæðirnar í **Línukostnaður** og **Línuvirði** reiknaðar á eins og lýst er í eftirfarandi töflum.

| Valkostir línukostnaðar | Description|
|----------------------------------|---------------------------------------|  
|**Þjónustuvara** | Kostnaðurinn er sóttur sjálfkrafa úr reitnum **Sjálfgefinn samningskostnaður** í töflunni **Þjónustuvara** og afritaður í reitinn **Línukostnaður**. Eftirfarandi reikniregla er notuð til að reikna línukostnaðinn:<br /><br /> Kostnaðarverð í sölu x Samningsvirði % ÷ 100|  
|**Vara** | Kostnaðurinn er sjálfkrafa sóttur í reitinn **Kostn.verð** í töflunni **Vara** og gildið í reitnum **Samningsvirðis %** í töflunni **Þjónustukerfisgrunnur**. Eftirfarandi reikniregla er notuð til að reikna línukostnaðinn:<br /><br /> Kostnaðarverð * Samningsvirðis % / 100.|  
|**Textalýsing** | Gildið í reitnum **Línukostnaður** er stillt á núll.|  

| Valkostir línuvirðis | Description|
|----------------------------------|---------------------------------------|  
|**Þjónustuvara** | Verðið er sótt sjálfkrafa úr reitnum **Sjálfgefið samningsvirði** í töflunni **Þjónustuvara** og afritað í reitinn **Línuvirði**.|  
|**Vara** | Háð gildinu í reitnum **Reikningsaðferð samningsvirðis** í töflunni **Þjónustukerfisgrunnur** er upphæðin sótt úr reitnum **Ein.verð** eða **Kostn.verð** í töflunni **Vörur**. Að því loknu er þetta gildi margfaldað með efninu í reitnum **Samningsvirðis %** í töflu í **Þjónustukerfisgrunninum** og deilt í 100.  Upphæðin er afrituð í reitinni **Línuvirði**.<br /><br /> **ATHUGASEMD:** Ef reiturinn **Reikningsaðferð samningsvirðis** er stilltur á **Ekkert** er efnið í reitnum **Línuvirði** ekki reiknað.|  
|**Textalýsing** | Innihald reitsins **Línuvirði** er stillt á núll.|  

## <a name="to-add-a-contract-discount-to-service-contract-quotes"></a>Samningsafslætti bætt við þjónustusamningstilboð  
Hægt er að bæta við samningsafsláttum af þjónustu vegna samningstilboða og þjónustusamninga. Afslátturinn getur átt við varahluti í tilteknum þjónustuvöruflokkum, vinnustundum forða í tilteknum forðaflokkum og á tilteknum þjónustukostnaði. 
  
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Þjónustusamningstilboð** og svo viðeigandi tengil.  
2. Veljið tilboð sem á að bæta afslætti við.  
3. Velja aðgerðina **Þjónustuafsláttur**. Glugginn **Samnings/þjónustuafsláttur** opnast.  
4. Til að búa til nýjan þjónustusamningsafslátt skal velja aðgerðina **Nýtt**.  
5. Fyllið út reitina í línunni eins og þörf er á. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].  
  
> [!Tip]  
>  Til að bæta samningsafslætti beint við þjónustusamning eru farnar svipaðar leiðir í glugganum **Þjónustusamningur**.  

## <a name="to-change-the-owner-of-a-service-contract"></a>Skipt um eiganda þjónustusamninga:  
Verið getur að skipta þurfi um eiganda þjónustusamnings. Ef þjónustuvara í þjónustusamningi er skráð í mörgum samningum í eigu sama viðskiptavinar sem ekki hefur verið hætt við er eiganda allra þjónustusamninga sem innihalda þessa þjónustuvöru og allra annarra þjónustuvara sem innifaldar eru í þessum samningum uppfærður sjálfkrafa.  
  
> [!NOTE]  
>  Í þessu tilviki eru aðeins teknir með samningar sem ekki hefur verið hætt við. Ekki er hirt um stöðu samningstilboða.  
  
> [!IMPORTANT]  
>  Þjónustuvörur og samningar geta tengst. Skipt um eiganda þjónustusamninga getur haft áhrif á eftirfarandi vensl.  
>   
>  Gerum t.d. ráð fyrir að þjónustuvara nr. 8 innfalin í samningunum SC00003 og SC00015. Samningur SC00015 inniheldur einnig þjónustuvöru nr. 15 sem er einnig innifalin í samningi SC00080. Í þessu tilviki yrði eiganda breytt í öllum þremur samningunum og í þjónustuvörunum.  

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Þjónustusamningar** og velja svo viðeigandi tengil. Opna skal viðeigandi þjónustusamning sem breyta á eiganda fyrir.  
2. Veldu aðgerðina **Opna samning** til að opna samninginn þannig að hægt sé að gera breytingar.  
3. Veljið aðgerðina **Skipta um viðskiptavin**. Glugginn **Breyta viðsk.mann í samningi** birtist.  
4. Í **Samningsnr.** og **Þjónustuvörunr.** sjást númer samningsins og þjónustuvörunnar sem valinn viðskiptamaður á. Ef viðskiptamaðurinn á fleiri en einn samning sem felur í sér fleiri en eina þjónustuvöru þá verður gildið í þessum reitum **Mörg**. Til að sjá lista yfir tengda samninga eða þjónustuvörur skal velja þessi reitargildi.  
5. Í **Númer nýs viðskiptamanns** reitinn skal velja nýjan viðskiptavin.  
6. Í reitnum **Nýr sendist-til-kóði** skal velja aðsetur.  
7. Veldu hnappinn **Í lagi** til að breyta viðskiptamanni og sendist-til - kóða þjónustusamninganna.  
8. Veldu **Læsa samningi** til að læsa samningnum og ganga úr skugga um að breytingarnar verði hluti samningsins.  

## <a name="to-update-a-service-contract-price"></a>Til að uppfæra verð þjónustusamninga  
Hægt er að uppfæra verð vegna þjónustusamninga með því að tilgreina prósentu verðuppfærslu.  

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Uppfæra þjónustusamningsverð** og velja svo viðeigandi tengil. 
2. Velja þjónustusamninginn.  
3. Á reitnum **Uppfæra til dags.**, er færð inn dagsetning. Keyrslan uppfærir verð vegna samninga sem á að uppfæra verðið á eða fyrir þennan dag.  
4. Í reitinn **Verðuppfærslu%** er færð inn prósentan sem á að uppfæra verðið með.  
5. Í reitnum **Aðgerð** er valið að **Uppfæra samningsverð**.  

## <a name="to-post-prepaid-contract-entries"></a>Bókun fyrirframgreiddra samningsfærslna  
Ef tíðkast að greiða þjónustusamninga fyrirfram þarf reglubundið að bóka fyrirframgreiddar samningsfærslur, og þar með að flytja fyrirframgreiðslur af fyrirframgreiddum samningsreikningum til venjulegra samningsreikninga.  
  
Áður en hægt er að bóka fyrirframgreiddar samningsfærslur þarf að tilgreina númeraröð í reitnum **Nr.röð bók.fyrirfr.gr.skjala** í glugganum **Þjónustukerfisgrunnur**.  

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Bóka fyrirframgreiddar samningsfærslur** og velja svo viðeigandi tengil.  
2. Á **Bóka til dags.** er dagsetning færð inn. Keyrslan bókar fyrirframgreiddar þjónustufærslur með bókunardagsetningu fram að þessari dagsetningu.  
4. Í reitnum **Bókunardags.** er færð inn dagsetningin sem á að nota sem bókunardagsetningu í færslubókarlínunni.  
5. Í reitnum **Aðgerð** er valið **Bóka fyrirframgreiddar samningsfærslur**.  
6. Veljið **Í lagi** til að bóka færslurnar.

## <a name="changing-the-service-contract-status"></a>Breyting á þjónustusamningsstöðu
Þegar þjónustusamningurinn er undirritaður er gildið í reitnum **Breyta stöðu** sjálfkrafa stillt á **Læst**. Ef breyta þarf upplýsingum í þjónustusamningi eða þjónustusamningstilboði verður fyrst að breyta stöðu samningsins eða samningstilboðsins úr **Læst** í **Opið**. Athygli er vakin á því að ekki er hægt að stofna þjónustureikninga fyrir þjónustusamninginn með breytingarstöðuna **Opið**. Þegar samningur eða samningstilboð hefur verið leiðrétt verður að breyta stöðunni aftur í **Læst** til að hægt verði að stofna þjónustureikninga og fjárhagsfærslur fyrir þjónustusamninginn, að meðtöldum breytingum sem gerðar hafa verið.  
  
> [!NOTE]  
>  Reiturinn **Breytingarstaða** tengist ekki reitnum **Losunarstaða** í þjónustupöntunarhausnum, sem stýrir vöruhúsameðhöndlun þjónustuvara.  

## <a name="to-cancel-a-service-contract"></a>Afturköllun þjónustusamnings:  
Hugsanlega þarf að hætta við þjónustusamning þegar samningurinn er útrunninn eða hætt hefur verið við hann.  
  
> [!NOTE]  
>  Þú getur ekki opnað samning eftir að honum hefur verið lokað.  

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Þjónustusamningar** og velja svo viðeigandi tengil.  
2. Opna skal viðeigandi þjónustusamning til að hætta við hann.  
3. Veldu aðgerðina **Opna samning** til að opna þjónustusamninginn þannig að hægt sé að gera breytingar.  
4. Í reitnum **Ástæðukóti afturköllunar** veljið viðeigandi ástæðukóta. Til að bæta við fleiri ástæðukóðum skal velja **Ítarlegt**.  
  
     Ef gátreiturinn í reitnum **Nota ástæðukóta afturk. samn.** í glugganum **Þjónustukerfisgrunnur** er valinn þarf að tilgreina ástæðukóta afturköllunar þegar hætt er við samninga.  
  
5. Í reitnum **Staða** er valið **Hætt við**.  
6. Ef óbókaðir reikningar, eða kreditreikningar eða opnar fyrirframgreiddar færslur eru til staðar fyrir samninginn sem á að hætta við birtast staðfestingarboð. Í boðaglugganum er valið **Nei** til að fara aftur í samninginn og bóka skjölin eða **Já** til að halda áfram afturköllunarferli.  

## <a name="filing-a-service-contract-or-contract-quote"></a>Skráning þjónustusamning eða samningstilboðs  
Hægt er að skrá þjónustusamninga og samningstilboð hvenær sem er til að vista afrit samnings eða samningstilboðs í kerfinu. [!INCLUDE[d365fin](includes/d365fin_md.md)] skráir þjónustusamninga sjálfkrafa þegar þjónustutilboði er breytt í þjónustusamning, eða þegar hætt er við þjónustusamning. Hægt er að skrá samning eða tilboð með því að velja **Skrá samning** á **Þjónustusamningar** eða **Þjónustusamningstilboð** síðunum. Til að skoða vistaða samninga með tilboðum skal leita að **Skráðir samningar**.

## <a name="see-also"></a>Sjá einnig  
[Hvernig á að: setja upp þjónustusamninga](service-how-setup-service-contracts.md)  
[Þjónustukerfi](service-service.md)  
[Hvernig á að umbreyta þjónustusamningum sem innihalda VSK upphæðir](service-how-to-convert-service-contracts.md)  

