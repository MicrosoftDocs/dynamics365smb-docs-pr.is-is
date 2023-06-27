---
title: Setja upp og skrá Intrastat
description: Lærið hvernig skal setja upp skráningareiginleika Intrastat og hvernig skal skrá viðskipti við fyrirtæki í öðrum ESB löndum.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, Intrastat, trade, EU, European Union
ms.search.form: 308, 309, 310, 311, 325, 326, 327, 328, 405, 406, 8451, 12202, 31077
ms.date: 05/23/2022
ms.author: bholtorf
ms.openlocfilehash: 5b54581c14d960b5cc52a896b41e7d7a864ee38d
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9608484"
---
# <a name="set-up-and-report-intrastat" /><a name="set-up-and-report-intrastat"></a>Setja upp og skrá Intrastat

Öll fyrirtæki í löndum innan Evrópusambandsins þurfa að gefa öðrum löndum/svæðum innan sambandsins skýrslur um viðskipti sín. Einnig þarf að gefa hagstofu viðkomandi lands/svæðis mánaðarlega skýrslu um hreyfingu vöru og skýrsluna þarf að afhenda skattayfirvöldum. Í kerfinu er þetta kallað Intrastat-skýrslur. **Intrastatbók** er notuð til að vinna reglulegar Intrastat-skýrslur.

[!INCLUDE[intrastat-2022w2](includes/intrastat-2022w2.md)]

## <a name="required-and-optional-setups" /><a name="required-and-optional-setups"></a>Áskilin og valfrjáls uppsetning

> [!IMPORTANT]
> Á viðskiptamanna- og lánardrottnaspjöldum er reitur, **Gerð Intrastat-viðskiptafélaga**, sem hefur sömu valkosti og reiturinn **Gerð viðskiptafélaga**: *„“ (tómt)*, *Fyrirtæki* og *Einstaklingur*. Reiturinn **Gerð Intrastat-viðskiptafélaga** hefur komið í stað reitsins **Gerð viðskiptafélaga** í Intrastat-skýrslugerð. **Gerð viðskiptafélaga** er notuð í SEPA til að skilgreina SEPA-beingreiðsluskemað (Core eða B2B). **Gerð Intrastat-viðskiptafélaga** er aðeins notaður fyrir Intrastat-skýrslugerð. Þannig er hægt að tilgreina mismunandi gildi fyrir reitina tvo ef á þarf að halda.
>
> Athugaðu þó að ef reiturinn **Gerð Intrastat-viðskiptafélaga** er skilinn eftir auður er gildið úr reitnum **Gerð viðskiptafélaga** notað við Intrastat-skýrslugerð.

Áður en þú getur notað Intrastat bókina til að gefa skýrslur í formi Intrastat upplýsinga, eru nokkrir hlutir sem þarf að setja upp.  

* **Uppsetning Intrastat**: Uppsetningarsíða Intrastat er notuð til að virkja skýrslugerð intrastat og setja á sjálfgefnar stillingar fyrir hana. Hægt er að tilgreina hvort eigi að gefa Intrastat-skýrslu um afhendingum (sendingum), kvittunum (komum) eða bæði, háð mörkum sem staðbundnar reglugerðir segja til um. Einnig er hægt að setja á sjálfgefnar færslugerðir fyrir venjuleg fylgiskjöl eða fylgiskjöl vöruskila, notaðar samkvæmt einkennum skýrslugerðar fyrir færslur.
* **Sniðmát Instrastatbókar**: Nauðsynlegt er að setja upp sniðmát og keyrslur Intrastatbókarinnar sem notaðar verða. Þar sem Intrastat-skýrslugerð er framkvæmd mánaðarlega verður að stofna 12 intrastatbókarkeyrslur sem miðast við sama sniðmát.  
* **Vörukóði**: Tolla- og skattyfirvöld hafa sett fram númerakóða sem flokka vörur og þjónustu. Þú tiltekur þessa kóða á vörum.
* **Eðliskóðar færslu**: Lönd og svæði hafa ólíka kóða fyrir tegundir Instrastat viðskipti, eins og venjuleg innkaup og sala, skipti á skilavörum, og skipti á vörum sem ekki hefur verið skilað. Setja upp alla kóða sem eiga við í þínu landi/svæði. Þú notar þessa kóða í  flýtiflipanum **Erlend viðskipti** í sölu- og innkaupaskjölum og þegar þú vinnur úr vöruskilum.

    > [!NOTE]
    > Intrastat gerir frá og með janúar 2022 kröfu um mismunandi eðliskóða viðskipta fyrir sendingar til einstaklinga sem eru ekki skráðir VSK-skyldir eða fyrirtækja sem eru skráð VSK-skyld. Við mælum með því að yfirfara og/eða bæta við nýjum eðliskóðum viðskipta á síðunni **Tegundir viðskipta** í samræmi við kröfurnar í þínu landi. Þú ættir einnig að fara yfir og uppfæra reitinn **Gerð Intrastat-viðskiptafélaga** í *Einstakling* fyrir einstaklinga eða VSK-skráð fyrirtæki á viðkomandi síðu **Viðskiptamanns**. Ef þú ert ekki viss um rétta gerð Intrastat-viðskiptafélaga eða tegund viðskipta sem á að nota mælum við með því að þú spyrjir sérfræðing í þínu landi eða svæði.

* **Flutningsmáti**: Það eru sjö einstölu kóðar fyrir Intrastat flutningsmáta. **1** fyrir sjóleið, **2** fyrir lest, **3** fyrir akstur, **4** fyrir flug, **5** fyrir póstsendingar, **7** fyrir fastar uppsetningar, og **9** fyrir eigin knúningsafl (til dæmis, flytja bíl með því að aka honum). [!INCLUDE[prod_short](includes/prod_short.md)] fer ekki fram á þessa kóða, en við mælum engu að síður með því að lýsingarnar beri með sér svipaða merkingu.  
* **Viðskiptalýsingar**: Nota þær til að drýgja lýsingarnar af gerð viðskiptanna.  
* **Upprunaland**: Notaðu tveggja bókstafa ISO Alfa kóða fyrir landið þar sem varan var fengin eða framleidd. Ef varan var framleidd í fleiri en einu landi er upprunalandið síðasta landið þar sem töluvert var unnið með hana.
* **VSK-númer samstarfsaðila í aðildarríkinu þar sem innflutningur fer fram**: Þetta er VSK-númer samstarfsaðila í aðildarríkinu þar sem innflutningur fer fram. VSK-númerið er einnig notað til að skiptast á upplýsingum um útflutning milli aðildarríkja ESB og gerir aðildarríkjunum kleift að úthluta mótteknum gögnum til innflutningsfyrirtækisins í eigin landi. Tilkynningarskyldar vörur verða að tilgreina VSK-númer fyrirtækis sem taldi fram til tolls vegna vörukaupa í aðildarríkinu þar sem innflutningur fer fram.

> [!NOTE]
> VSK-númer viðskiptafélaga sem á að nota getur verið mismunandi eftir viðskiptaaðstæðum. Til dæmis getur númerið sem á að nota verið mismunandi fyrir aðstæður á borð við sölukeðju þar sem birgir selur vöru til annars lands og síðan endurselur það fyrirtæki vöruna til annars fyrirtækis í sama landinu, þríhliða viðskipti o.s.frv. Ef þú ert ekki viss um rétta VSK-númer sem á að nota mælum við með því að þú spyrjir sérfræðing í þínu landi eða svæði.

Einnig er hægt að setja upp:

* **Svæði**: Nota þau til að drýgja lýsingarnar um lönd og svæði.  
* **Komu/brottfarastaðir**: Nota þá til að tiltaka staðsetningar þar sem vöruafhending og móttaka fara fram í viðskiptum við önnur lönd. Heathrow flugstöðin er dæmi um komu-brottfararstað. Komu/brottfararstaði er hægt að færa inn í sölu- og innkaupskjöl á flýtiflipanum **Erlend viðskipti**. Þessar upplýsingar verða einnig afritaðar úr birgðafærslum þegar Intrastatbók er stofnuð.  

### <a name="to-set-up-intrastat-templates-and-batches" /><a name="to-set-up-intrastat-templates-and-batches"></a>Uppsetning Intrastat-sniðmáts og keyrslna.

Intrastat keyrslurnar ná aðeins yfir birgðafærslur, en ekki fjárhagsfærslur. Ef birgðafærslur eru til staðar sem eru gjaldgengar fyrir Intrastat-skýrslu, verður að færa þær inn handvirkt. Ef fyrirtækið kaupir t.d. tölvu frá öðru landsvæði innan ESB, er tölvan ekki sett í birgðir heldur bókuð í fjárhagsreikning. Slíka færslu verður að færa handvirkt inn í Intrastat-færslubókina.  

Hægt er að flytja færsluna út í skrá sem þú getur sent til Instrat yfirvalda. Einnig er hægt að prenta skýrslu, færa upplýsingarnar handvirkt inn í formið frá yfirvöldum, og svo senda upplýsingarnar inn.

> [!NOTE]
> Mælt er með því að keyrsla Intrastatbóka sé stofnuð fyrir hvern mánuð.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sniðmát Intrastatbókar** og velja síðan viðkomandi tengil.  
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Stofna sniðmát fyrir hvert Instrastat form sem er notað.  
3. Til að búa til keyrslur skaltu velja aðgerðina **Runur**.  
4. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]. Stofna sniðmát fyrir hvert Instrastat form sem er notað.

> [!NOTE]
> Í reitinn **Upplýsingatímabil** er upplýsingatímabilið fært inn sem fjögurra stafa númer og tákna fyrstu tveir tölustafirnir árið og þeir sem á eftir koma mánuðinn. Til dæmis er 1706 fært inn fyrir júní 2017.

### <a name="to-set-up-transport-methods" /><a name="to-set-up-transport-methods"></a>Uppsetning Flutningsmátar

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Flutningsaðferðir** og velja síðan viðkomandi tengil.  
2. Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="to-set-up-which-intrastat-report-fields-are-mandatory" /><a name="to-set-up-which-intrastat-report-fields-are-mandatory"></a>Til að setja upp hvaða Intrastat skýrslureitir eru nauðsynlegir

Í sumum löndum, eins og Spáni og Bretlandi, krefjast yfirvöld að Intrastatskýrslur innihaldi til dæmis sendingaraðferðina fyrir kaup eða nokkur önnur gildi þegar salan er yfir ákveðnum mörkum. Á síðunni **Uppsetning Intrastat** getur þú valið að gera **Uppsetning Instrastat-gátlista** til að stilla áskilda reiti á síðunni **Intrastatbók**.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning Intrastat** og velja síðan viðkomandi tengil.
2. Veldu aðgerðina **Uppsetning Intrastat-gátlista**.
3. Á síðunni **Uppsetning Intrastat-gátlista**, veldu **Reitarheiti** til að ná Intrastat skýrslureit sem þú vilt gera skyldu að fylla út.

### <a name="czechia" /><a name="czechia"></a>Tékkland

Fyrir tékknesk fyrirtæki verður þú einnig að setja upp vörukóða og færslukóða.  

#### <a name="to-set-up-commodity-codes" /><a name="to-set-up-commodity-codes"></a>Uppsetning vörukóða

Allar vörur sem eru keyptar eða selda verða að hafa vörukóða.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörukóðar** og velja síðan viðkomandi tengil.  
2. Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Til að úthluta vörukóða til vöru, skal fara í **Birgðaspjald** síðuna, útvíkka **Kostnaður & Bókanir** flýtiflipann og síðan færa inn kóðann í **Vörukóði** reitinn.

### <a name="italy" /><a name="italy"></a>Ítalía

Fyrir ítölsk fyrirtæki. verður þú einnig að setja upp vörukóða og færslukóða.  

#### <a name="to-set-up-transaction-nature-codes" /><a name="to-set-up-transaction-nature-codes"></a>Uppsetning eðliskóða viðskipta

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eðliskóða viðskipta** og velja síðan viðkomandi tengil.  
2. Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

> [!TIP]
> Ef sérstakur eðliskóði viðskipta er notaður oft, geturðu gert hann sjálfgefinn. Til að gera það, skal fara á **Uppsetning Intrastat** síðuna, og velja kóðann.

## <a name="to-report-intrastat" /><a name="to-report-intrastat"></a>Setja fram Intrastat skýrslu

Eftir að þú hefur fyllt út Intrastatbókina geturðu keyrt aðgerðina **Gátlistaskýrslu** til að ganga úr skugga um að allar upplýsingar í bókinni séu réttar. Áskildir reitir sem þú hefur stillt á síðunni **Uppsetning Intrastat-gátlista** þar sem vantar gildi verða sýndir í upplýsingareitnum „Villur og viðvörun“ á síðunni **Intrastatbók**. Eftir það er hægt að intrastat-skýrsla prentuð á eyðublað eða stofnuð sem skrá og því næst send til skattayfirvalda viðkomandi landssvæðis.  

### <a name="to-fill-in-intrastat-journals" /><a name="to-fill-in-intrastat-journals"></a>Fært inn í Intrastatbækur:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Intrastatbók** og velja síðan viðkomandi tengil.  
2. Á **Intrastat bók** síðunni, í reitnum **Heiti keyrslu** skal velja viðeigandi færslubókarkeyrslu og velja því næst hnappinn **Í lagi**.  
3. Veljið aðgerðina **Leggja til línur**. Reitirnir **Upphafsdags.** og **Lokadagsetning** eru þegar komnir með dagsetningarnar sem tilgreindar eru fyrir upplýsingatímabilið í bókarkeyrslunni.  
4. Hægt er að færa prósentu í reitinn **Kostnaðarregla %** (til að ná yfir flutning og tryggingar). Ef færð er inn prósenta verður efni reitsins **Upplýsingagildi** í færslubókinni hlutfallslega hærra.  
5. Smellt er á **Í lagi** til að hefja keyrsluna.  

Keyrslan sækir allar birgðafærslur á upplýsingatímabilinu og setur þær inn í Intrastatbókina sem línur. Hægt er að breyta línunum ef þörf er á.  

> [!IMPORTANT]  
> Keyrslan sækir aðeins þær færslur sem eru með lands-/svæðiskóða og fengið hafa Intrastatkóða á síðunni **Lönd/svæði**. Þess vegna er brýnt að færa inn Intrastatkóta fyrir lands-/svæðiskótana sem keyrslan er fyrir. Runuvinnslan stilltir reitinn **VSK-númer samstarfsaðila** á *QV999999999999* fyrir einstaklinga eða fyrirtæki sem ekki eru með VSK-númer (viðskiptamenn með reitinn **Intrastat-viðskiptafélagar** stilltan á *Einstaklingur*) og hann notar gildið í reitnum **Færslugerði** á bókaðri birgðafærslu eða verkfærslu.

### <a name="to-modify-intrastat-journals-lines" /><a name="to-modify-intrastat-journals-lines"></a>Til að breyta Intrastat-bókarlínum

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Intrastatbók** og velja síðan viðkomandi tengil.  
2. Á **Intrastat bók** síðunni, í reitnum **Heiti keyrslu** skal velja viðeigandi færslubókarkeyrslu og velja því næst hnappinn **Í lagi**.  
3. Notaðu síusvæði til að sía færslulínur Intrastatbókar á sumum skilyrðum. Til dæmis geturðu síað reitina **VSK-númer samstarfsaðila** með gildinu *QV999999999999*.
4. Veldu táknið **Deila** ![Deila síðu í öðru forriti](media/share-icon.png). og velja **Breyta í Excel**.
5. Í Excel skal breyta línum Intrastatbókar sem voru síaðar frá. Til dæmis breyta gildum í reitnum **Færslugerð**.  
6. Birtu breytingarnar sem þú hefur gert í Excel aftur í [!INCLUDE[prod_short](includes/prod_short.md)]

> [!NOTE]
> Í [!INCLUDE[prod_short](includes/prod_short.md)] útgáfum sem styðja ekki [**Breyta í Excel**](across-work-with-excel.md#edit-in-excel) fyrir færslubækur er hægt að búa til grunnstillingarpakka til að flytja út og inn línur Intrastatbókar í Excel. Frekari upplýsingar er að finna í [Flytja inn innanhússgögn í Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) í efnisstjórnunarefninu.

### <a name="report-intrastat-on-a-form-or-a-file" /><a name="report-intrastat-on-a-form-or-a-file"></a>Senda Intrastat-skýrslu á eyðublaði eða sem skrá

Prenta þarf skýrsluna **Intrastat – Eyðublað** til að fá upplýsingarnar sem þarf fyrir INTRASTAT-eyðublaðið frá hagstofu. Áður en hægt er að gera þetta þarf að undirbúa Intrastatbókina og fylla hana út. Ef bæði er um sölu- og innkaupafærslur að ræða þarf að fylla út sérstakt eyðublað fyrir hvora tegundina fyrir sig svo að þörf er á að prenta skýrsluna tvisvar.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Intrastatbækur** og velja síðan viðkomandi tengil.  
2. Á **Intrastat bók** síðunni, í reitnum **Heiti keyrslu** skal velja viðeigandi færslubókarkeyrslu.  
3. Fylla skal handvirkt út í færslubókina, ef það hefur ekki verið gert nú þegar, eða velja aðgerðina **Leggja til línur**.  
4. Veljið aðgerðina **Prentar Intrastatbók**.  
5. Á flýtiflipanum **Intrastatbókalína** er bætt við afmörkuninni **Tegund** til að velja einn af eftirfarandi valkostum: **Móttaka** eða **Afhending**.  
6. Til að prenta skýrsluna skal velja **Senda til**.  

### <a name="report-intrastat-in-a-file" /><a name="report-intrastat-in-a-file"></a>Senda Intrastat-skýrslu sem skrá

Hægt er að senda Intrastat-skýrsluna sem skrá. Áður en skráin er búin til er hægt að prenta gátlista með upplýsingunum sem verða í skránni.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Intrastatbók** og velja síðan viðkomandi tengil.  
2. Á **Intrastat bók** síðunni, í reitnum **Heiti keyrslu** skal velja viðeigandi færslubókarkeyrslu.  
3. Fylla skal handvirkt út í færslubókina, ef það hefur ekki verið gert nú þegar, eða með því að velja aðgerðina **Leggja til línur**.  
4. Aðgerðin **Stofna Skrá** er valin.  
5. Á síðu runuvinnslunnar skaltu velja hnappinn **Í lagi**.  
6. Velja **Vista**.  
7. Flett er að möppunni þar sem vista á skrána og skráarheiti fært inn og síðan valið **Vista**.

> [!NOTE]
> Þegar lína í Intrastat-skýrslunni hefur viðbótarmælieiningu verður þyngd vörunnar ekki sýnd þar sem ekki er þörf á þessu gildi.

## <a name="reorganize-intrastat-journals" /><a name="reorganize-intrastat-journals"></a>Endurskipuleggja Intrastatbækur

Þar sem Intrastat-skýrslu þarf að senda inn mánaðarlega og búa til nýja færslubókarkeyrslu fyrir hverja þeirra, muntu að lokum hafa margar bókarkeyrslur. Færslubókarlínurnar eyðast ekki sjálfkrafa. Ef til vill á að endurraða heitum færslubókarkeyrslnanna eftir tímabilum. Það er gert með því að eyða færslubókarkeyrslunum sem ekki er lengur þörf fyrir. Færslubókarlínunum í þessum keyrslum er einnig eytt.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Intrastatbækur** og velja síðan viðkomandi tengil.  
2. Í glugganum  er reiturinn **Heiti keyrslu** valinn til að sjá valkosti.  
3. Veldu bókarkeyrslurnar sem á að eyða og svo hnappinn **Eyða**.  

## <a name="tariff-numbers" /><a name="tariff-numbers"></a>Tollflokkar

Í mörgum löndum hafa tolla- og skattayfirvöld komið á 8 stafa vörukóða vegna ýmiss konar vörur. Ef birgðafærslur eiga að fela í sér nauðsynlegar upplýsingar þegar kerfið flytur þær í intrastatbókarlínu verða upplýsingar um tollflokk að hafa verið færðar inn á síðun **Tollflokkar**. Finna skal kóða þeirra vörutegunda sem fyrirtæki notanda verslar með og færa þá inn í gluggann **Tollflokkar**.

Á síðunni **Tollflokkar** skal bæta við öllum kóðum sem eru notaðir. Áður en bókun hefst skal færa kóða inn á birgðaspjald. Þegar kóðar hafa verið settir upp skulu þeir færðir inn í reitinn **Tollflokkar** á birgðaspjaldinu. Einnig skal fylla út reitinn **Nettóvigt** á birgðaspjaldi.

## <a name="see-related-training-at-microsoft-learn" /><a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/process-intrastat-dynamics-365-business-central/index).

## <a name="see-also" /><a name="see-also"></a>Sjá einnig .

[Fjármálastjórnun](finance.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
