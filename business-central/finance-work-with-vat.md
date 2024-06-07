---
title: Hvernig á að vinna með VSK í sölu og innkaupum
description: 'Í þessu efnisatriði er því lýst mismunandi leiðum til að vinna með VSK bæði handvirkt og með sjálfvirka uppsetningu, til að aðstoða notanda við að uppfylla sérstakar reglugerðir um land/svæði.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'VAT, sales, purchases'
ms.search.form: '7, 118, 130, 142, 459, 460, 525'
ms.date: 06/16/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="work-with-vat-on-sales-and-purchases"></a>Unnið með VSK í sölu og innkaupum

Ef landið eða svæðið þitt krefst þess að reiknaður sé virðisaukaskattur (VSK) á sölu- og innkaupafærslur er hægt að setja upp [!INCLUDE[prod_short](includes/prod_short.md)] til að reikna VSK. Frekari upplýsingar, sjá [Uppsetning fyrir útreikning og bókunaraðferðir virðisaukaskatts](finance-setup-vat.md).

Það eru samt sem áður VSK-tengd verkefni sem þú getur innt af hendi handvirkt. Þú gætir t.d. þurft að leiðrétta bókaða upphæð ef þú uppgötvar að lánardrottinn notar annars konar sléttunaraðferð.  

> [!TIP]
> Hægt er að láta [!INCLUDE[prod_short](includes/prod_short.md)] villuleita VSK-númer og aðrar upplýsingar um fyrirtæki þegar skjöl eru búin til eða uppfærð. Frekari upplýsingar er að finna í [Villuleita VSK-númer](finance-how-validate-vat-registration-number.md).

## <a name="calculating-and-displaying-vat-amounts-on-sales-and-purchase-documents"></a>Útreikningur og birting VSK-upphæða á sölu- og innkaupaskjölum

Þegar þú velur vörunúmer í **Nr.** reitnum á sölu- eða innkaupaskjali, [!INCLUDE[prod_short](includes/prod_short.md)] fyllir út reitina **Einingarverð** og **Línuupphæð**. Einingarverðið er reiknað og flutt úr annaðhvort **birgða** spjaldinu eða leyfilegum vöruverðum vörunnar og viðskiptamannsins. [!INCLUDE[prod_short](includes/prod_short.md)] reiknar einungis Línuupphæð þegar magn er fært inn fyrir línuna.  

Ef þú vilt að einingarverð og línuupphæðir innihaldi VSK, til dæmis ef þú selur neytendum smásölu skaltu velja gátreitinn **Verð með VSK** í skjalinu. Frekari upplýsingar er að finna í [Taka með eða útiloka VSK í verðum og línuupphæðum](#including-or-excluding-vat-in-prices-and-line-amounts). 

Hægt er að reikna og birta VSK-upphæðir í sölu- og innkaupaskjölum á mismunandi máta, samkvæmt tegund viðskiptamannsins eða lánardrottinsins sem notandi á viðskipti við. Einnig er til dæmis hægt að breyta reiknuðum VSK-upphæðum handvirkt svo þær passi við VSK-upphæðina sem reiknuð er af lánardrottni viðkomandi færslu.

### <a name="including-or-excluding-vat-in-prices-and-line-amounts"></a>Með eða án VSK í verði og línuupphæðum

Ef gátreiturinn **Verð með VSK er** valinn í söluskjali eru vsk í reitunum **Ein.verð** og **Línuupphæð** með VSK. Gildin í þessum reitum eru sjálfgefið ekki með VSK. Heiti reitanna endurspegla hvort VSK sé innifalinn í verðinu.  

Hægt er að setja upp sjálfgefna stillingu á **Verð með VSK** fyrir öll söluskjöl viðskiptamanns í reitnum **Verð með VSK** á spjaldinu **Viðskiptamaður**. Einnig er hægt að setja upp vöruverð þannig að þau séu með eða án VSK. Yfirleitt munu verð í birgðaspjaldinu ekki innihalda VSK. 

Eftirfarandi tafla birtir yfirlit yfir það hvernig forritið reiknar upphæðir einingarverðs fyrir söluskjöl þegar engin verð eru sett upp á síðunni **Söluverð**:  

|**Verð með VSK í birgðaspjaldi**|**Verð með VSK reit**|**Aðgerð framkvæmd**|  
|-----------------------------------------------|----------------------------------------------------|--------------------------|  
|Ekki virkt|Ekki virkt|**Einingarverð** á birgðaspjaldinu er afritað í reitinn **Ein.verð án VSK** í sölulínunum.|  
|Ekki virkt|Virk|Forritið reiknar VSK-upphæð á einingu og bætir við **Ein.verð** á Vöruspjaldinu. Heildareiningarverðið er svo fært inn í reitinn **Ein. verð með Vsk** í sölulínunum.|  
|Virk|Ekki virkt|Forritið reiknar VSK-upphæðina sem er innifalin í **Einingaverð** reitnum á **Birgðaspjald** með VSK-prósentunni sem tengist samsetningu VSK-viðskiptabókunarflokksins (verð) og VSK-vörubókunarflokksins. **Einingaverðið** í birgðaspjaldinu, mínus VSK-upphæðin, er því næst fært inn í reitinn **Ein.verð án VSK** í sölulínunum. Frekari upplýsingar er að finna í [Notkun VSK-viðskiptabókunarflokka og verðflokka viðskiptamanns](finance-work-with-vat.md#using-vat-business-posting-groups-and-customer-price-groups).|  
|Virk|Virk|**Einingarverðið** í birgðaspjaldinu er afritað í reitinn **Ein.verð með VSK** í sölulínunum.|

#### <a name="using-vat-business-posting-groups-and-customer-price-groups"></a>Notkun VSK-viðskiptabókunarflokka og verðflokka viðskiptamanna

Ef þú vilt að VSK sé innifalinn í verði geturðu notað VSK-viðskiptabókunarflokka til að reikna út upphæðina út frá VSK-bókunargrunni fyrir flokkinn. Frekari upplýsingar er að finna í [Setja upp VSK-viðskiptabókunarflokka](finance-setup-vat.md#set-up-vat-business-posting-groups).

Þú getur úthlutað VSK-viðskiptabókunarflokk á viðskiptamanna- eða söluskjöl á eftirfarandi hátt, eftir því hvað þú vilt gera:

* Til að nota sama VSK-hlutfall fyrir alla viðskiptamenn er hægt að velja reitinn **VSK-viðskiptabókunarflokkur (verð)** á síðunni **Uppsetning sölugrunns**.
* Til að nota VSK-hlutfall fyrir tiltekinn viðskiptamann geturðu valið flokk í reitnum **VSK-viðskiptabókunarflokkur (verð)** á síðunni **Viðskiptamannaspjald**. 
* Til að nota VSK-hlutfall fyrir tiltekna viðskiptamenn geturðu valið flokk í reitnum **VSK-viðskiptabókunarflokkur (verð)** á síðunni **Verðflokkur viðskiptamanns**. Þetta er til dæmis gagnlegt þegar þú vilt að verð gildi um alla viðskiptamenn á ákveðnu landfræðilegu svæði eða í tiltekinni atvinnugrein.
* Í öllum söluskjölum í reitnum **VSK-viðskiptabókunarflokkur**. VSK-upphæðin sem tilgreind er fyrir flokkinn er aðeins notaður fyrir skjalið sem þú ert að vinna í þessa stundina.

> [!NOTE]
> Ef þú tilgreinir ekki flokk í reitnum **VSK-viðskiptabókunarflokkur (verð)** verður VSK ekki með í verðinu.

#### <a name="examples"></a>Dæmi

Þættir á borð við landið eða svæðið sem þú selur í eða tegund atvinnugreinar sem þú selur til getur haft áhrif á VSK-upphæðina sem gera þarf grein fyrir. Veitingastaður gæti til dæmis rukkað 6% VSK fyrir máltíðir sem eru borðaðar á staðnum og 17% fyrir sóttan mat. Til að ná því býrðu til VSK-viðskiptabókunarflokk (verð) fyrir á staðnum og einn fyrir sótt.

## <a name="working-with-vat-date"></a>Unnið með VSK dags.

### <a name="vat-date-in-documents"></a>VSK-dagsetning í skjölum

Þegar þú býrð til ný sölu- eða innkaupaskjöl verður **VSK-dagsetning** byggð á stillingunni í reitnum **Sjálfgefinn VSK-dagur** á síðunni **Fjárhagsgrunnur**. Þetta sjálfgefna gildi getur verið það sama og **Bókunardagsetning** eða **Dagsetning skjals**. Ef þú þarft aðra VSK-dagsetningu getur þú breytt gildinu handvirkt í reitnum **VSK-dagsetning**. Þegar þú bókar skjalið verður **VSK-dagsetning** sýnd í bókunarskjalinu og í VSK- og fjárhagsfærslum.

> [!NOTE]
> Ef reiturinn **VSK-dagsetning** er ekki tiltækur í fylgiskjölum eða færslubókum merkir það að **aðgerðin** Nota ekki VSK-dagsetningu er valin í reitnum **Notkun VSK-dagsetningar** á síðunni **Fjárhagsgrunnur** .  

> [!IMPORTANT]
>  **Ef stjórna VSK-tímabili**  **í fjárhagsgrunninum** sem **Loka bókun innan lokaðs tímabils** eða **Loka bókun innan lokaðs og viðvörunar fyrir útgefin tímabil** er aðeins hægt að bóka fylgiskjal eða færslubók ef dagsetningin í reitnum **VSK-dagsetning** er ekki í lokuðu tímabili **VSK-vöruskila**. Jafnvel þótt tímabilið í **VSK-skilatímabilum** sé opið er hægt að fá viðvörun byggða á **stöðu** VSK-vöruskila og grunnstillingu í glugganum Stjórna VSK-tímabili **·**.

> [!IMPORTANT]
> Hafist er handa í útgáfu 23.1 er hægt að koma í veg fyrir eða leyfa bókun **VSK-dagsetninga** fyrir tiltekið gagnasvið með því að nota reitina **Leyfa VSK-dagsetningu frá** og **Leyfa VSK-dagsetningu** til í **VSK-grunninum** og **notandauppsetningunni**. Ef eldri útgáfur eru notaðar er hægt að koma í veg fyrir eða leyfa bókun **VSK-dagsetninga** fyrir tiltekið gagnasvið með því að **nota reitina** Bókun leyfð frá **og** Leyfa bókun á í **Fjárhagsgrunni** og **Uppsetning** notanda.  

> [!NOTE]
>  **Ef VSK-dagsetningin er látin** vera auð [!INCLUDE [prod_short](includes/prod_short.md)]  notar hún sjálfgefna uppsetningu úr **Sjálfgefinni VSK-dagsetningu** í **Fjárhagsgrunni** sem **VSK-dagsetningu** í bókuðu færslunni.  

### <a name="modifying-the-vat-date-in-posted-entries"></a>Breyta VSK-dagsetningu í bókuðum færslum

Ef þörf krefur er hægt að breyta bókuðum skjölum með VSK-dagsetningu. Til að breyta dagsetningunni í reitnum **VSK-dagsetning** fyrir bókuð fylgiskjöl skal fylgja eftirfarandi skrefum:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **VSK-færslur** og velja síðan viðkomandi tengil. 
2. Finna færslu með rangri VSK dagsetningu.  
3. Veljið aðgerðina **Breyta lista** og færið rétta dagsetningu inn í reitinn **VSK-dags** .  
4. Þegar síðunni er lokað breytist VSK-dagsetningin í tengdum **fjárhagsfærslum** og í bókaða fylgiskjalinu.  

> [!NOTE]
> Aðeins er hægt að breyta reitnum **VSK-dagsetning** í **VSK-færslum** ef núverandi dagsetning er ekki í lokuðu VSK-skilatímabili. Jafnvel þótt tímabilið í reitnum **VSK-skilatímabil** sé opið birtist viðvörun sem byggð er á **stöðu** VSK-vöruskila.  

> [!NOTE]
> Ef skjalið er með fleiri en eina **VSK-færslu** þarf aðeins að breyta gildinu í reitnum **VSK-dagsetning** í einni færslu sem tengist skjalinu. Til að halda færslum samræmdum [!INCLUDE[prod_short](includes/prod_short.md)]  breytist VSK-dagsetningin sjálfkrafa í VSK-færslum sem tengjast þessari færslu. [!INCLUDE [prod_short](includes/prod_short.md)] uppfærir **VSK-dagsetninguna** í öðrum töflum (FJÁRHAGSfærslur og fylgiskjöl) en aðeins tengd þessari færslu.  

## <a name="correcting-vat-amounts-manually-on-sales-and-purchase-documents"></a>Leiðrétting VSK-upphæða handvirkt á sölu- og innkaupaskjölum

Hægt er að leiðrétta bókaðar VSK-færslur svo hægt sé að breyta samtals VSK-upphæð fyrir sölu og innkaup án þess að breyta VSK-stofninum. Ef þú færð til dæmis reikning frá lánardrottni með rangri VSK-upphæð.  

Jafnvel þótt ein eða fleiri samsetningar hafi verið settar upp til að afgreiða VSK vegna innflutnings, þarf að setja upp að minnsta kosti einn VSK-vörubókunarflokk. Til dæmis er hægt að gefa honum heitið **LEIÐRÉTTA** fyrir leiðréttingu, nema hægt sé að nota sama fjárhagsreikning í reitnum **Reikningur innskatts** í VSK-bókunargrunnslínunni. Frekari upplýsingar, sjá [Uppsetning fyrir útreikning og bókunaraðferðir virðisaukaskatts](finance-setup-vat.md).

Ef greiðsluafsláttur er reiknaður af reikningsupphæð sem inniheldur VSK er mögulegt að bakfæra greiðsluafsláttarhluta VSK þegar greiðsluafsláttur er veittur. Athygli er vakin á því að virkja þarf reitinn **Leiðrétta v. greiðsluafsl.** bæði í fjárhagsgrunni almennt og í VSK-bókunargrunni fyrir tilteknar samsetningar á VSK-viðskiptabókunarflokki og VSK-vörubókunarflokki.  

### <a name="to-set-the-system-up-for-manual-vat-entry-in-sales-documents"></a>Til að setja kerfið upp fyrir handvirka VSK-færslu í söluskjölum
Eftirfarandi lýsir því hvernig á að virkja handvirkar VSK-breytingar á söluskjölum. Skrefin eru svipuð á síðunni **Uppsetning innkaupa og viðskiptaskulda**.

1. Í glugganum **Uppsetning fjárhags** er tilgreindur **leyfður hámarks VSK-mismunur** milli upphæðarinnar sem reiknuð er af forritinu og handvirkt reiknuðu upphæðarinnar.  
2. Á síðunni **Uppsetning Sala & Útistandandi** skal setja gátmerki í reitinn **Leyfa VSK-mismun**.  

### <a name="to-adjust-vat-for-a-sales-document"></a>Breyting VSK fyrir söluskjöl:

1. Viðeigandi sölupöntun er opnuð.  
2. Veldu **Upplýsingar** aðgerðina.  
3. Í flýtiflipanum **Reikningsfærsla** skal velja gildið í reitnum **Nr. skattalína**.
4. Breyttu reitnum **VSK-upphæð**.   

> [!NOTE]  
> Heildarupphæð VSK fyrir reikninginn, sem flokkaður er samkvæmt kennimerki VSK, er birt í línunum. Hægt er að breyta upphæðinni handvirkt í reitnum **VSK-upphæð** í línum hvers kennimerkis VSK. Þegar **VSK-upphæð** er breytt gengur forritið úr skugga um VSK hafi ekki verið breytt um meira en þá upphæð sem tilgreind er sem leyfður hámarksmismunur. Ef upphæðin er utan **Hám. VSK-mismunur leyfður** birtist viðvörun þar sem hámarksmismunur er tekinn fram. Ekki er hægt að halda áfram fyrr en upphæðin hefur verið leiðrétt. Smellt er á **Í lagi** og önnur **VSK-upphæð** sem er innan hámarksmismunar færð inn. Ef VSK-mismunur er jafn og eða lægri en hámarkið er VSK deilt hlutfallslega á milli fylgiskjalalínanna sem eru með sama kennimerki VSK.  

## <a name="calculating-vat-manually-using-journals"></a>ÚtreikningUR VSK handvirkt með því að nota færslubækur
Einnig er hægt að breyta VSK-upphæðum í almennum færslubókum, sölu- og innkaupabókum. Þetta kann t.d. að reynast nauðsynlegt þegar lánardrottinsreikningur er færður inn í færslubók notanda og mismunur er á milli VSK-upphæðarinnar sem reiknuð er af [!INCLUDE[prod_short](includes/prod_short.md)] og VSK-upphæðarinnar sem er á mótteknum reikningi frá lánardrottninum.  

### <a name="to-set-the-system-up-for-manual-vat-entry-in-a-general-journals"></a>Til að setja kerfið upp fyrir handvirka VSK-færslu í almennum færslubókum
Eftirfarandi skref þarf að klára áður en VSK er fært handvirkt inn í almenna færslubók.  

1. Í glugganum **Uppsetning fjárhags** er tilgreindur **leyfður hámarks VSK-mismunur** milli upphæðarinnar sem reiknuð er af forritinu og handvirkt reiknuðu upphæðarinnar.  
2. Á síðunni **Sniðmát færslubókar** skal velja **Leyfa VSK-mismun** gátreitinn fyrir viðeigandi færslubók.  

### <a name="to-set-the-system-up-for-manual-vat-entry-in-a-sales-and-purchase-journals"></a>Til að setja kerfið upp fyrir handvirka VSK-færslu í sölu- og innkaupabókum

Eftirfarandi skref þarf að klára áður en VSK er fært handvirkt inn í sölu- eða innkaupabók.

1. Á síðunni **Uppsetning innkaup & viðskiptaskuldir** skal velja **Leyfa VSK-mismun** gátreitinn.  
2. Endurtaktu skref 1 fyrir síðuna **Uppsetning sölugrunns**.
3. Þegar uppsetningunni er lokið eins og lýst er hér að ofan er hægt að breyta reitnum **VSK-upphæð** í færslubókarlínunni eða reitnum  **Mótreikningur VSK-upph.** í sölu- eða innkaupabókarlínunum. [!INCLUDE[prod_short](includes/prod_short.md)] gengur úr skugga um að mismunurinn sé ekki meiri en tilgreint hámark.  

> [!NOTE]  
> Ef mismunurinn er of mikill birtist viðvörun þar sem hámarksmismunurinn er tekinn fram. Ekki er hægt að halda áfram fyrr en upphæðin hefur verið leiðrétt. Smellt er á **Í lagi** og upphæð sem er innan hámarksmismunar færð inn. Ef VSK-mismunurinn er jafn og eða lægri en leyfilegt hámark birtir [!INCLUDE[prod_short](includes/prod_short.md)] mismuninn í reitnum **Mismunur á VSK**.  

## <a name="posting-import-vat-with-purchase-invoices"></a>Bókun VSK vegna innflutnings með innkaupareikningum
Í stað þess að nota færslubækur til að bóka VSK-reikning vegna innflutnings er hægt að nota innkaupareikning.  

### <a name="to-set-up-purchasing-for-posting-import-vat-invoices"></a>Til að setja upp innkaup fyrir bókun VSK-reikninga vegna innflutnings

1. Lánardrottnaspjald er sett upp fyrir innflutningsyfirvöld sem senda VSK-reikning vegna innflutnings. **Alm. viðsk.bókunarflokkur** og **VSK viðsk.bókunarflokkur** verða að vera uppsettir á sama hátt og fjárhagsreikningurinn fyrir VSK vegna innflutnings.  
2. **Alm. vörubókunarflokkur** búinn til fyrir VSK vegna innflutnings og **Sjálfg. VSK-vörubókunarfl.** fyrir VSK vegna innflutnings er settur upp fyrir tengdan **Alm. vörubókunarflokk**.  
3. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bókhaldslykill** og velja síðan viðkomandi tengil.  
4. Veldu fjárhagsreikning VSK-innflutnings og svo aðgerðina **Breyta**.  
5. Á flýtiflipanum **Bókun** er uppsetningin **Almennur framleiðslubókunarflokkur** settur upp fyrir VSK innflutning. [!INCLUDE[prod_short](includes/prod_short.md)] fyllir sjálfkrafa inn í reitinn **VSK viðsk.bókunarflokkur.**.  
6. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning almennrar bókunar** og velja síðan viðkomandi tengil.  
7. Búa til samsetningu **Alm. viðsk.bókunarflokks** fyrir VSK yfirvöld og **Alm. vörubókunarflokks** fyrir VSK vegna innflutnings. Fyrir þessa nýju samsetningu er fjárhagsreikningur fyrir VSK vegna innflutnings valinn í reitnum **Innkaupareikningur**.  

### <a name="to-create-a-new-invoice-for-the-import-authority-vendor-once-you-have-completed-the-setup"></a>Að stofna nýjan reikning fyrir lánardrottnayfirvald innflutninga þegar uppsetningunni er lokið

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupareikningar** og velja síðan viðkomandi tengil.  
2. Stofnið nýja innkaupareikning.  
3. Í reitnum **Númer afh.aðila** er lánardrottnayfirvald innflutninga valið og síðan smellt á **Í lagi**.  
4. Í innkaupalínunni í reitnum **Tegund** er **fjárhagsreikningur** valinn og í reitnum **Nr.** er fjárhagsreikningur fyrir VSK vegna innflutnings valinn.  
5. Ritað er **1** í reitnum **Magn**.  
6. Í reitnum **Innk.verð án VSK** er VSK upphæðin tilgreind.  
7. Bóka skal reikninginn.  

## <a name="processing-certificates-of-supply"></a>Vinnsla birgðavottorða

Þegar vörur eru seldar viðskiptamanni í öðru land/svæði innan Evrópusambandsins þarftu að senda viðskiptamanninum afhendingarvottorð sem hann þarf að skrifa undir og skila þér. Eftirfarandi ferli eru fyrir meðhöndlun framboðsvottorða fyrir söluafhendingar, en sömu skref gilda um þjónustuafhendingu vara og skilaafhendingar til lánardrottna.  

### <a name="to-view-certificate-of-supply-details"></a>Til að skoða upplýsingar afhendingarvottorðs
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") tákn, skal færa inn **Bókaðar söluafhendingar** og velja síðan viðkomandi tengil.  
2. Veldu viðeigandi sölusendingu til viðskiptamaður í öðru landi/svæði Evrópusambandsins  
3. Velja skal **Upplýsingar um afhendingarvottorð**  
4. Sjálfgefið er að ef uppsetning VSK-bókunarflokkur fyrir viðskiptamann hefur **Afhendingarvottorð áskilið** er gátreitur valinn og reiturinn **Staða** stilltur á **Áskilinn**. Hægt er að uppfæra reitinn til að tákna hvort vottorðið hafi borist frá viðskiptamanninum.  

> [!Note]  
>  EF uppsetning VSK-bókunarflokks er ekki með **Afhendingarvottorð áskilið** er gátreitur valinn og færsla stofnuð og reiturinn **Staða** stilltur á **Ekki áskilið**. Hægt er að uppfæra reitinn til að endurspegla réttar stöðuupplýsingar. Hægt er að breyta stöðunni handvirkt úr **Á ekki við** í **Áskilið** og úr **Áskilið** í **Á ekki við** eins og þörf er á.  

   Þegar þú uppfærir reitinn **Staða** í **Áskilið**, **Móttekið** eða **Ekki móttekið** stofnast vottorð.  

> [!TIP]  
>  Hægt er að nota síðuna **Afhendingarvottorð** til að sjá stöðu allra bókaðra sendinga þar sem afhendingarvottorð hefur verið búið til.  

5. Velja **Prenta Afhendingarvottorð**  

> [!Note]  
>  Hægt er að forskoða eða prenta skjalið. Þegar þú velur **Prenta afhendingarvottorð** og prentar skjalið, er gátreiturinn **Prentað** sjálfkrafa valinn. Að auki er staða vottorðsins uppfærð í **Áskilið** ef það er ekki þegar skilgreint. Þú setur inn prentaða vottorðið með sendingunni ef þurfa þykir.  

### <a name="to-print-a-certificate-of-supply"></a>Til að prenta afhendingarvottorð

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") tákn, skal færa inn **Bókaðar söluafhendingar** og velja síðan viðkomandi tengil.  
2. Veldu viðeigandi sölusendingu til viðskiptamaður í öðru landi/svæði Evrópusambandsins  
3. Velja aðgerðina **Prenta afhendingarvottorð**.  

> [!NOTE]  
>  Einnig geturðu prentað vottorð af síðunni **Afhendingarvottorð**.  

4. Til að hafa upplýsingar úr línunum á afhendingarskjalinu í vottorðinu skal velja gátreitinn **Prenta línuupplýsingar**.  
5. Veljið gátreitinn **Stofna framboðsvottorð ef engin eru til staðar** til að láta [!INCLUDE[prod_short](includes/prod_short.md)] stofna vottorð fyrir bókaðar afhendingar sem eru ekki með vottorð við keyrslu. Þegar gátreiturinn er valinn stofnast nýtt vottorð fyrir allar bókaðar sendingar sem eru ekki með vottorð innan valda bilsins.  
6. Sjálfgefið er að síustillingar séu fyrir sendiskjalið sem hefur verið valið. Fyllið út afmörkunarupplýsingarnar til að velja tiltekið afhendingarvottorð sem prenta á út.  
7. Á síðunni **Afhendingarvottorð** veljið aðgerðina **Prenta** til þess að prenta skýrsluna eða veljið aðgerðina **Forskoðun** til að birta hana á skjánum.  

> [!Note]  
> **Staða afhendingarvottorðs** reiturinn og **Prentað** reiturinn uppfærast fyrir sendinguna á **Afhendingarvottorð** síðunni.  

8. Þú verður að senda prentaða afhendingarvottorðið til viðskiptamannsins til undirritunar.  

### <a name="to-update-the-status-of-a-certificate-of-supply-for-a-shipment"></a>Til að uppfæra stöðu afhendingarvottorðs fyrir sendingu.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") tákn, skal færa inn **Bókaðar söluafhendingar** og velja síðan viðkomandi tengil.  
2. Veldu viðeigandi sölusendingu til viðskiptamaður í öðru landi/svæði Evrópusambandsins  
3. Í reitnum **Staða** veljið viðeigandi valkost.  

   Ef viðskiptamaðurinn hefur skilað afhendingarvottorði skal velja **Móttekið**. Reiturinn **móttökudagsetning** er uppfærður. Sjálfgefið er að´ móttökudagsetning sé stillt á núverandi vinnudag.  

   Hægt er að breyta dagsetningunni þannig að hún endurspegli dagsetninguna þegar þú fékkst afhent undirritaða afhendingarvottorðið frá viðskiptamanninum. Einnig er hægt að bæta við tengli í undirritað vottorð með staðlaðri [!INCLUDE[prod_short](includes/prod_short.md)] tengingu.  

   Ef viðskiptamaðurinn skilar ekki undirrituðu afhendingarvottorði skal velja **Ekki móttekið**. Þú verður að senda viðskiptamanninum nýjan reikning sem inniheldur VSK þar sem upphaflegi reikningurinn er ekki samþykktur af skattyfirvöldum.  

Til að skoða vottorðahóp byrjarðu á síðunni **Afhendingarvottorð** og uppfærir svo upplýsingarnar um stöðu útistandandi vottorða þegar þú færð þau til baka frá viðskiptamanninum. Þetta getur komið að gagni þegar leita á að öllum vottorðum sem eru með tiltekna stöðu, til dæmis **Nauðsynlegt**, þar sem á að uppfæra stöðuna í **Ekki móttekið**.  

### <a name="to-update-the-status-of-a-group-of-certificates-of-supply"></a>Til að uppfæra stöðu vottorðahóps fyrir framboð

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Framboðsvottorð** og velja síðan viðkomandi tengi.  
2. Afmarkið reitinn **Staða** við gildið sem óskað er til þess að búa til lista yfir vottorð sem hafa á umsjón með.  
3. Til að uppfæra stöðuupplýsingarnar velurðu **Breyta lista**.  
4. Í reitnum **Staða** veljið viðeigandi valkost.  

   Ef viðskiptamaðurinn hefur skilað afhendingarvottorði skal velja **Móttekið**. Reiturinn **móttökudagsetning** er uppfærður. Sjálfgefið er að´ móttökudagsetning sé stillt á núverandi vinnudag.  

   Hægt er að breyta dagsetningunni þannig að hún endurspegli dagsetninguna þegar þú fékkst afhent undirritaða afhendingarvottorðið. Einnig er hægt að bæta við tengli í undirritað vottorð með staðlaðri [!INCLUDE[prod_short](includes/prod_short.md)] skjal tengingu.  

> [!NOTE]
> Ekki er hægt að stofna nýtt afhendingarvottorð á síðunni **Afhendingarvottorð** þegar þú velur hann með þessu ferli. Til að stofna vottorð fyrir afhendingu þar sem ekki var þörf á því skal opna bókuðu söluafhendinguna og nota annað af tveimur ferlum sem er lýst hér að ofan:  
>
> * Til að stofna vottorð afhendingarvottorðs handvirkt  
> * Til að prenta afhendingarvottorð.

## <a name="see-also"></a>Sjá einnig

[Uppsetning fyrir útreikning og bókunaraðferðir virðisaukaskatts](finance-setup-vat.md)  
[Senda VSK skýrslu inn til skattayfirvalda](finance-how-report-vat.md)  
[Staðfesting VSK-númers](finance-how-validate-vat-registration-number.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
