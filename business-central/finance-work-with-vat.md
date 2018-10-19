---
title: "Hvernig á að: vinna með VSK í sölu og innkaupum | Microsoft Docs"
description: "Þetta efnisatriði lýsir því hvernig framkvæma skal verk á borð leiðréttingu bókaðs VSK í ESB-löndum/svæðum, allar sölu- og innkaupafærslur falla undir VSK-útreikning. Í þessu efnisatriði er því lýst hvernig það er gert."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, sales, purchases,
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 0abbc8f6d7aa80a7a89296568d9a4ecb0ead0f5f
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="work-with-vat-on-sales-and-purchases"></a>Unnið með VSK í sölu og innkaupum
Ef þitt land eða svæði krefst þess að reiknaður sé VSK skattur á sölu- og innkaupafærslur svo hægt sé talið upphæðirnar fram til skattayfirvalda, geturðu sett upp [!INCLUDE[d365fin](includes/d365fin_md.md)] þannig að VSK verði reiknaður sjálfkrafa á sölu- og innkaupaskjölum. Frekari upplýsingar, sjá [Uppsetning fyrir útreikning og bókunaraðferðir virðisaukaskatts] (finance-setup-vat.md).

Það eru samt sem áður VSK-tengd verkefni sem þú getur innt af hendi handvirkt. Þú gætir t.d. þurft að leiðrétta bókaða upphæð ef þú uppgötvar að lánardrottinn notar annars konar sléttunaraðferð.

## <a name="calculating-and-displaying-vat-amounts-in-sales-and-purchase-documents"></a>Útreikningur og birting VSK-upphæða í sölu- og innkaupaskjölum  
Hægt er að reikna og birta VSK-upphæðir í sölu- og innkaupaskjölum á mismunandi máta, samkvæmt tegund viðskiptamannsins eða lánardrottinsins sem notandi á viðskipti við. Einnig er hægt að hnekkja VSK-upphæðum sem kerfið reiknaði svo þær passi við VSK-upphæðina sem reiknuð er af lánardrottni viðkomandi færslu.  

### <a name="unit-price-and-line-amount-includingexcluding-vat-on-sales-documents"></a>Einingaverð og línuupphæð með/án VSK á söluskjölum  
Þegar þú velur vörunúmer í **Nr.** reitnum á söluskjali, fyllir [!INCLUDE[d365fin](includes/d365fin_md.md)] einnig út reitinn **Ein.verð**. Einingarverðið er reiknað og flutt úr annaðhvort **birgða** spjaldinu eða leyfilegum vöruverðum vörunnar og viðskiptamannsins. [!INCLUDE[d365fin](includes/d365fin_md.md)]reiknar einungis **Línuupphæð** þegar magn er fært inn fyrir línuna.  

Ef selt er til smásöluneytenda, viltu kannski að verð í söluskjali sé með VSK. Þetta er hægt að gera með því að velja gátreitinn **Verð með VSK** í fylgiskjalinu.  

### <a name="including-or-excluding-vat-on-prices"></a>Taka með eða útiloka VSK í verði
Ef gátreiturinn **Verð með VSK** er valinn á söluskjali eru reitirnir **Ein.verð** og **Línuupphæð** með VSK og Reitaheitin endurspegla einnig þetta. Sjálfgefið er VSK ekki tekið með í þessum reitum.  

Ef reiturinn er ekki valinn fyllir kerfið út reitina **Ein.verð** og **Línuupphæð** án VSK. Reitaheitin endurspegla það.  

Hægt er að setja upp sjálfgefna stillingu á **Verð með VSK** fyrir öll söluskjöl viðskiptamanns í reitnum **Verð með VSK** á spjaldinu **Viðskiptamaður**. Einnig er hægt að setja upp vöruverð þannig að þau séu með eða án VSK. Yfirleitt er vöruverð í birgðaspjaldi verð án VSK. Kerfið notar upplýsingarnar úr reitnum **Verð með VSK** í **birgðaspjaldinu** til að ákvarða einingarverðið fyrir söluskjölin.  

Eftirfarandi tafla birtir yfirlit yfir það hvernig kerfið reiknar upphæðir einingarverðs fyrir söluskjöl þegar engin verð eru sett upp í glugganum **Söluverð**:  

|**Verð með VSK í birgðaspjaldi**|**Reiturinn Verð með VSK í söluhaus**|**Aðgerð framkvæmd**|  
|-----------------------------------------------|----------------------------------------------------|--------------------------|  
|Ekkert gátmerki|Ekkert gátmerki|**Einingarverð** á birgðaspjaldinu er afritað í reitinn **Ein.verð án VSK** í sölulínunum.|  
|Ekkert gátmerki|Gátmerki|Kerfið reiknar VSK-upphæð á einingu og bætir við **Ein.verð** á Vöruspjaldinu. Heildareiningarverðið er svo fært inn í reitinn **Ein. verð með Vsk** í sölulínunum.|  
|Gátmerki|Ekkert gátmerki|Kerfið reiknar VSK-upphæðina sem er tekin í **Ein.verð** í birgðaspjaldinu með VSK-prósentunni sem tengist samsetningu VSK-viðskiptabókunarflokksins (verð) og VSK-vörubókunarflokksins. **Einingaverðið** í birgðaspjaldinu, mínus VSK-upphæðin, er því næst fært inn í reitinn **Ein.verð án VSK** í sölulínunum.|  
|Gátmerki|Gátmerki|**Einingarverðið** í birgðaspjaldinu er afritað í reitinn **Ein.verð með VSK** í sölulínunum.|

## <a name="correcting-vat-amounts-manually-in-sales-and-purchase-documents"></a>Handvirk breyting VSK-upphæða í sölu- og innkaupaskjölum  
Hægt er að gera leiðréttingar á bókuðum VSK-færslum. Þannig er hægt að breyta heildarupphæðum VSK sölu eða innkaupa án þess að breyta VSK-stofninum. Þetta gæti verið nauðsynlegt til dæmis ef viðkomandi berst reikningur frá lánardrottni sem hefur misreiknað VSK.  

Jafnvel þótt ein eða fleiri samsetningar hafi verið settar upp til að afgreiða VSK vegna innflutnings, þarf að setja upp að minnsta kosti einn VSK-vörubókunarflokk. Til dæmis er hægt að gefa honum heitið **LEIÐRÉTTA** fyrir leiðréttingu, nema hægt sé að nota sama fjárhagsreikning í reitnum **Reikningur innskatts** í VSK-bókunargrunnslínunni. Frekari upplýsingar, sjá [Uppsetning fyrir útreikning og bókunaraðferðir virðisaukaskatts](finance-setup-vat.md).

Ef greiðsluafsláttur er reiknaður af reikningsupphæð sem inniheldur VSK er mögulegt að bakfæra greiðsluafsláttarhluta VSK þegar greiðsluafsláttur er veittur. Athygli er vakin á því að virkja þarf reitinn **Leiðrétta v. greiðsluafsl.** bæði í fjárhagsgrunni almennt og í VSK-bókunargrunni fyrir tilteknar samsetningar á VSK-viðskiptabókunarflokki og VSK-vörubókunarflokki.  

#### <a name="to-manually-enter-vat-in-sales-documents"></a>Til að færa VSK handvirkt inn í söluskjöl  
1. Í glugganum **Uppsetning fjárhags**, skaltu tilgreina **leyfðan hámarks VSK-mismun** á milli upphæðinnar sem reiknuð er af kerfinu og handvirkt reiknuðu upphæðinnar.  
2. Setja gátmerki í reitinn **Leyfa VSK-mismun** í glugganum **Sölugrunnur**.  

#### <a name="to-adjust-vat-for-a-sales-document"></a>Breyting VSK fyrir söluskjöl:  
1. Viðeigandi sölupöntun er opnuð.  
2. Veldu **Upplýsingar** aðgerðina.  
3. Smellt er á flýtiflipann **Reikningsfæra**.  
  
    > [!NOTE]  
    >  Heildarupphæð VSK fyrir reikninginn, sem flokkaður er samkvæmt kennimerki VSK, er birt í línunum. Hægt er að breyta upphæðinni handvirkt í reitnum **VSK-upphæð** í línum hvers kennimerkis VSK. Þegar **VSK-upphæð** er breytt gengur kerfið úr skugga um VSK hafi ekki verið breytt um meira en þá upphæð sem tilgreind er sem leyfður hámarksmismunur. Ef upphæðin er utan **Hám. VSK-mismunur leyfður** birtist viðvörun þar sem hámarksmismunur er tekinn fram. Ekki er hægt að halda áfram fyrr en upphæðin hefur verið leiðrétt. Smellt er á **Í lagi** og önnur **VSK-upphæð** sem er innan hámarksmismunar færð inn. Ef VSK-mismunur er jafn og eða lægri en hámarkið er VSK deilt hlutfallslega á milli fylgiskjalalínanna sem eru með sama kennimerki VSK.  

## <a name="calculating-vat-manually-using-journals"></a>Reikna VSK handvirkt með því að nota Færslubækur  
Einnig er hægt að breyta VSK-upphæðum í almennum færslubókum, sölu- og innkaupabókum. Þetta kann t.d. að reynast nauðsynlegt þegar lánardrottinsreikningur er færður inn í færslubók notanda og mismunur er á milli VSK-upphæðarinnar sem reiknuð er af [!INCLUDE[d365fin](includes/d365fin_md.md)] og VSK-upphæðarinnar sem er á mótteknum reikningi frá lánardrottninum.  

#### <a name="before-you-manually-enter-vat-on-a-general-journal"></a>Áður en hægt er að færa VSK handvirkt inn í færslubók  
1. Í glugganum **Uppsetning fjárhags**, skaltu tilgreina **leyfðan hámarks VSK-mismun** á milli upphæðinnar sem reiknuð er af kerfinu og handvirkt reiknuðu upphæðinnar.  
2. Í glugganum **Sniðmát færslubókar**, veldu **Leyfa VSK-mismun** gátreitinn fyrir viðeigandi færslubók.  

#### <a name="before-you-manually-enter-vat-on-sales-and-purchase-journals"></a>Áður en VSK er fært handvirkt inn í sölu- og innkaupabækur  
1. Í glugganum **Uppsetning innkaup & viðskiptaskuldir**, veldu **Leyfa VSK-mismun**.  
2. Þegar uppsetningunni er lokið eins og lýst er hér að ofan er hægt að breyta reitnum **VSK-upphæð** í færslubókarlínunni eða reitnum  **Mótreikningur VSK-upph.** í sölu- eða innkaupabókarlínunum. [!INCLUDE[d365fin](includes/d365fin_md.md)] gengur úr skugga um að mismunurinn sé ekki meiri en tilgreint hámark.  
  
    > [!NOTE]  
    > Ef mismunurinn er of mikill birtist viðvörun þar sem hámarksmismunurinn er tekinn fram. Ekki er hægt að halda áfram fyrr en upphæðin hefur verið leiðrétt. Smellt er á **Í lagi** og upphæð sem er innan hámarksmismunar færð inn. Ef VSK-mismunurinn er jafn og eða lægri en leyfilegt hámark birtir [!INCLUDE[d365fin](includes/d365fin_md.md)] mismuninn í reitnum **Mismunur á VSK**.  

## <a name="to-post-import-vat-with-purchase-invoices"></a>Hvernig á að bóka VSK vegna innflutnings með innkaupareikningum
Í stað þess að nota færslubók til að bóka VSK-reikning vegna innflutnings er hægt að nota innkaupareikning.  

### <a name="to-set-up-purchasing-for-posting-import-vat-invoices"></a>Til að setja upp innkaup fyrir bókun VSK-reikninga vegna innflutnings  
1. Lánardrottnaspjald er sett upp fyrir innflutningsyfirvöld sem senda VSK-reikning vegna innflutnings. **Alm. viðsk.bókunarflokkur** og **VSK viðsk.bókunarflokkur** verða að vera uppsettir á sama hátt og fjárhagsreikningurinn fyrir VSK vegna innflutnings.  
2. **Alm. vörubókunarflokkur** búinn til fyrir VSK vegna innflutnings og **Sjálfg. VSK-vörubókunarfl.** fyrir VSK vegna innflutnings er settur upp fyrir tengdan **Alm. vörubókunarflokk**.  
3. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **bókhaldslykill** og veldu síðan tengda tengilinn.  
4. Veljið fjárhagsreikning VSK vegna innflutnings og veljið því næst **Breyta** úr flokknum **Stjórna** á flipanum **Heim**.  
5. Á flýtiflipanum **Bókun** er uppsetningin **Almennur framleiðslubókunarflokkur** settur upp fyrir VSK innflutning. [!INCLUDE[d365fin](includes/d365fin_md.md)] fyllir sjálfkrafa inn í reitinn **VSK viðsk.bókunarflokkur.**.  
6. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning almenns bókunargrunns** og veldu síðan tengda tengilinn.  
7. Búa til samsetningu **Alm. viðsk.bókunarflokks** fyrir VSK yfirvöld og **Alm. vörubókunarflokks** fyrir VSK vegna innflutnings. Fyrir þessa nýju samsetningu er fjárhagsreikningur fyrir VSK vegna innflutnings valinn í reitnum **Innkaupareikningur**.  

### <a name="to-create-a-new-invoice-for-the-import-authority-vendor-once-you-have-completed-the-setup"></a>Að stofna nýjan reikning fyrir lánardrottnayfirvald innflutninga þegar uppsetningunni er lokið  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innkaupareikningar** og veldu síðan tengda tengilinn.  
2. Stofnið nýja innkaupareikning.  
3. Í reitnum **Númer afh.aðila** er lánardrottnayfirvald innflutninga valið og síðan smellt á **Í lagi**.  
4. Í innkaupalínunni í reitnum **Tegund** er **fjárhagsreikningur** valinn og í reitnum **Nr.** er fjárhagsreikningur fyrir VSK vegna innflutnings valinn.  
5. Ritað er **1** í reitnum **Magn**.  
6. Í reitnum **Innk.verð án VSK** er VSK upphæðin tilgreind.  
7. Bóka skal reikninginn.  

## <a name="to-process-certificates-of-supply"></a>Vinna framboðsvottorð
Þegar vörur eru seldar viðskiptamanni í öðru land/svæði innan Evrópusambandsins þarftu að senda viðskiptamanninum afhendingarvottorð sem hann þarf að skrifa undir og skila þér. Eftirfarandi ferli eru fyrir meðhöndlun framboðsvottorða fyrir söluafhendingar, en sömu skref gilda um þjónustuafhendingu vara og skilaafhendingar til lánardrottna.  

### <a name="to-view-certificate-of-supply-details"></a>Til að skoða upplýsingar afhendingarvottorðs  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Bókaðar söluafhendingar** og veldu síðan tengda hlekkinn.  
2. Veldu viðeigandi sölusendingu til viðskiptamaður í öðru landi/svæði Evrópusambandsins  
3. Velja skal **Upplýsingar um afhendingarvottorð**  
4. Sjálfgefið er að ef uppsetning VSK-bókunarflokkur fyrir viðskiptamann hefur **Afhendingarvottorð áskilið** er gátreitur valinn og reiturinn **Staða** stilltur á **Áskilinn**. Hægt er að uppfæra reitinn til að tákna hvort vottorðið hafi borist frá viðskiptamanninum.  

    > [!Note]  
    >  EF uppsetning VSK-bókunarflokks er ekki með **Afhendingarvottorð áskilið** er gátreitur valinn og færsla stofnuð og reiturinn **Staða** stilltur á **Ekki áskilið**. Hægt er að uppfæra reitinn til að endurspegla réttar stöðuupplýsingar. Hægt er að breyta stöðunni handvirkt úr **Á ekki við** í **Áskilið** og úr **Áskilið** í **Á ekki við** eins og þörf er á.  

   Þegar þú uppfærir reitinn **Staða** í **Áskilið**, **Móttekið** eða **Ekki móttekið** stofnast vottorð.  
  
    > [!TIP]  
    >  Hægt er að nota gluggann **Afhendingarvottorð** til að sjá stöðu allra bókaðra sendinga þar sem afhendingarvottorð hefur verið búið til.  

5. Velja **Prenta Afhendingarvottorð**  
  
    > [!Note]  
    >  Hægt er að forskoða eða prenta skjalið. Þegar þú velur **Prenta afhendingarvottorð** og prentar skjalið, er gátreiturinn **Prentað** sjálfkrafa valinn. Að auki er staða vottorðsins uppfærð í **Áskilið** ef það er ekki þegar skilgreint. Þú setur inn prentaða vottorðið með sendingunni ef þurfa þykir.  

### <a name="to-print-a-certificate-of-supply"></a>Til að prenta afhendingarvottorð  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Bókaðar söluafhendingar** og veldu síðan tengda hlekkinn.  
2. Veldu viðeigandi sölusendingu til viðskiptamaður í öðru landi/svæði Evrópusambandsins  
3. Velja aðgerðina **Prenta afhendingarvottorð**.  

    > [!NOTE]  
    >  Einnig geturðu prentað vottorð úr glugganum **afhendingarvottorð**.  

4. Til að hafa upplýsingar úr línunum á afhendingarskjalinu í vottorðinu skal velja gátreitinn **Prenta línuupplýsingar**.  
5. Veljið gátreitinn **Stofna framboðsvottorð ef engin eru til staðar** til að láta [!INCLUDE[d365fin](includes/d365fin_md.md)] stofna vottorð fyrir bókaðar afhendingar sem eru ekki með vottorð við keyrslu. Þegar gátreiturinn er valinn stofnast nýtt vottorð fyrir allar bókaðar sendingar sem eru ekki með vottorð innan valda bilsins.  
6. Sjálfgefið er að síustillingar séu fyrir sendiskjalið sem hefur verið valið. Fyllið út afmörkunarupplýsingarnar til að velja tiltekið afhendingarvottorð sem prenta á út.  
7. Í glugganum **Afhendingarvottorð** veljið aðgerðina **Prenta** til þess að prenta skýrsluna eða veljið aðgerðina **Forskoðun** til að birta hana á skjánum.  

    > [!Note]  
    > **Staða afhendingarvottorðs** reiturinn og **Prentað** reiturinn uppfærast fyrir sendinguna í **Afhendingarvottorð** glugganum.  

8. Þú verður að senda prentaða afhendingarvottorðið til viðskiptamannsins til undirritunar.  

### <a name="to-update-the-status-of-a-certificate-of-supply-for-a-shipment"></a>Til að uppfæra stöðu afhendingarvottorðs fyrir sendingu.  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Bókaðar söluafhendingar** og veldu síðan tengda hlekkinn.  
2. Veldu viðeigandi sölusendingu til viðskiptamaður í öðru landi/svæði Evrópusambandsins  
3. Í reitnum **Staða** veljið viðeigandi valkost.  

   Ef viðskiptamaðurinn hefur skilað afhendingarvottorði skal velja **Móttekið**. Reiturinn **móttökudagsetning** er uppfærður. Sjálfgefið er að´ móttökudagsetning sé stillt á núverandi vinnudag.  

   Hægt er að breyta dagsetningunni þannig að hún endurspegli dagsetninguna þegar þú fékkst afhent undirritaða afhendingarvottorðið frá viðskiptamanninum. Einnig er hægt að bæta við tengli í undirritað vottorð með staðlaðri [!INCLUDE[d365fin](includes/d365fin_md.md)] tengingu.  

   Ef viðskiptamaðurinn skilar ekki undirrituðu afhendingarvottorði skal velja **Ekki móttekið**. Þú verður að senda viðskiptamanninum nýjan reikning sem inniheldur VSK þar sem upphaflegi reikningurinn er ekki samþykktur af skattyfirvöldum.  

Til að skoða vottorðahóp byrjarðu í **Afhendingarvottorð** glugganum og uppfærir svo upplýsingarnar um stöðu útistandandi vottorða þegar þú færð þau til baka frá viðskiptamanninum. Þetta getur komið að gagni þegar leita á að öllum vottorðum sem eru með tiltekna stöðu, til dæmis **Nauðsynlegt**, þar sem á að uppfæra stöðuna í **Ekki móttekið**.  

### <a name="to-update-the-status-of-a-group-of-certificates-of-supply"></a>Til að uppfæra stöðu vottorðahóps fyrir framboð  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Framboðsvottorð** og veldu tengda hlekkinn.  
2. Afmarkið reitinn **Staða** við gildið sem óskað er til þess að búa til lista yfir vottorð sem hafa á umsjón með.  
3. Til að uppfæra stöðuupplýsingarnar velurðu **Breyta lista**.  
4. Í reitnum **Staða** veljið viðeigandi valkost.  

   Ef viðskiptamaðurinn hefur skilað afhendingarvottorði skal velja **Móttekið**. Reiturinn **móttökudagsetning** er uppfærður. Sjálfgefið er að´ móttökudagsetning sé stillt á núverandi vinnudag.  

   Hægt er að breyta dagsetningunni þannig að hún endurspegli dagsetninguna þegar þú fékkst afhent undirritaða afhendingarvottorðið. Einnig er hægt að bæta við tengli í undirritað vottorð með staðlaðri [!INCLUDE[d365fin](includes/d365fin_md.md)] skjal tengingu.  

    > [!NOTE]  
    >  Ekki er hægt að stofna nýtt afhendingarvottorð í **Afhendingarvottorð** glugganum þegar þú velur hann með þessu ferli. Til að stofna vottorð fyrir afhendingu þar sem ekki var þörf á því skal opna bókuðu söluafhendinguna og nota annað af tveimur ferlum sem er lýst hér að ofan:  
    >   
    > * Til að stofna vottorð afhendingarvottorðs handvirkt  
    > * Til að prenta afhendingarvottorð.

## <a name="see-also"></a>Sjá einnig  
[Uppsetning fyrir útreikning og bókunaraðferðir virðisaukaskatts](finance-setup-vat.md)   
[Hvernig á að: Senda VSK skýrslu inn til skattayfirvalda](finance-how-report-vat.md)   

