---
title: Þjónustuverðstjórnun
description: 'Þjónustuverðstjórnun gerir þér kleift að setja upp verðflokka, verðlagningu og verðleiðréttingar þjónustu og fleira.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="service-price-management"></a>Þjónustuverðstjórnun
Þjónustuverðsstjórnaraðgerðin gerir kleift að setja besta verðið á þjónustupantanir, setja upp sérsniðna þjónustuverðsamninga fyrir viðskiptavini, bæta skilvirkni þjónustustarfsmanna og hraða reikningaferlinu.  
  
Þjónustuverðsstjórn gerir kleift að setja upp mismunandi þjónustuverðflokka, taka tillit til þjónustuvörunnar (eða þjónustuvöruflokksins) og villugerðar sem þjónustuverkið felur í sér. Hægt er að setja þessa flokka upp fyrir ákveðin tímabil eða fyrir tiltekinn viðskiptavin eða gjaldmiðil. Hægt er að nota skipulag verðútreikninga sem sniðmát til að úthluta tilteknu verki tilteknu verði.  
  
Þannig er til dæmis hægt að úthluta tilteknum vörum sem innifaldar eru í þjónustuverðinu, auk innifalinnar vinnugerðar. Þetta gerir einnig kleift að nota mismunandi VSK- og afsláttarupphæðir fyrir mismunandi þjónustuverðflokka. Til þess að tryggja að rétt verð sé notað er hægt að úthluta föstu verði, lágmarksverði eða hámarksverði - í samræmi við samninga við viðskiptavini.  
  
Áður en verð þjónustuvöru í þjónustupöntun er leiðrétt sýnir kerfið hverjar niðurstöður verðleiðréttingarinnar verða. Hægt er að samþykkja þessar niðurstöður eða gera frekari breytingar ef niðurstaðan á að vera önnur. Leiðréttingin er gerð línu fyrir línu sem þýðir að engar nýjar línur eru stofnaðar.  
  
Loks gera upplýsingar um þjónustuverð og staðlaðar skýrslur gera kleift að fylgjast með arðsemi hvers þjónustuverðflokks.  
  
## <a name="service-price-adjustment-groups"></a>Þjónustuverðleiðréttingarflokkar
Þjónustuverðleiðréttingarflokkar eru notaðir til að setja upp mismunandi gerðir verðleiðréttinga fyrir þjónustulínur. Til dæmis er hægt að setja upp einn þjónustuverðleiðréttingarflokk sem leiðréttir verð á varahlutum, annan sem leiðréttir verð á vinnu, annan sem leiðréttir verð fyrir kostnað og svo framvegis. Einnig er hægt að tilgreina hvort aðeins eigi að gera þjónustuverðleiðréttingu á einni tiltekinni vöru eða forða eða á öllum vörum og öllum forða.  
  
Aðgerð verðleiðréttingar á þjónustu er ekki hægt að nota fyrir þjónustuvörur undir eftirfarandi skilyrðum:

* Varan tilheyrir þjónustusamningum. Aðeins er hægt að leiðrétta þjónustuverð á vörum sem tilheyra þjónustupöntun. 
* Ef þjónustuvaran er með ábyrgð. 
* Ef þjónustulínan hefur verið bókuð sem reikningur, annaðhvort að fullu eða að hluta til.  
  
Þegar þjónustuverðleiðréttingaraðgerðin er keyrð er öllum afsláttum í pöntuninni skipt út fyrir gildin í þjónustuverðleiðréttingunni.  
  
## <a name="service-price-groups"></a>Þjónustuverðflokkar
Hægt er að setja upp þjónustuverðflokka til að stofna flokka með þjónustuvörum sem fá sömu sérþjónustuverðlagningu. Þegar búið er að setja upp þjónustuverðflokka er hægt að úthluta þeim til þjónustuvara í þjónustuvörulínum. Einnig er hægt að úthluta þjónustuverðflokkum til þjónustuvöruflokka.  
  
Áður en hægt er að úthluta þjónustuvöru þjónustuverðflokki verður að ákveða hvaða villusvæði, gjaldmiðli og þjónustuverðleiðréttingaflokki þjónustuverðflokkurinn tilheyrir. Ákveða verður upphæð sem leiðrétta skal þjónustuverðið í og tilgreina hvort VSK og afsláttur skuli vera innifalinn í þessari upphæð. Einnig þarf að ákveða hvort þessi leiðrétting eigi við fasta upphæð eða hvort aðeins skuli beita henni við tilteknar aðstæður.  
  
Þegar þjónustuvöru er úthlutað þjónustuverðflokki er öll sérþjónustuverðlagning sem sett er upp í þessum flokki notuð fyrir þessa þjónustuvöru.  
  
## <a name="service-pricing"></a>Þjónustuverðlagning
Sett er upp tegund þjónustuverðlagningar (verðleiðréttingartegund og verð) fyrir samsetningu á þjónustuverðflokkum og viðskiptavinaverðflokkum. Fyrir hverja tegund þjónustuverðlagningar er valinn þjónustuverðleiðréttingarflokkur. Einnig er verðleiðréttingartegund, föst, hámark eða lágmark, tilgreind og raunverulegt verð.  
  
Til dæmis er hægt að setja upp tegundir þjónustuverðlagningar fyrir útvarpsþjónustuverðflokk. Hægt er að ákveða þjónustuverðlagningu með hámarksverði á vinnu verðleiðréttingarflokkur vegna vinnu, fyrir þá viðskiptamenn sem ekki heyra til verðlagningarflokks. Hægt er að ákveða þjónustuverðlagningu með föstu verði á vinnu sami verðleiðréttingarflokkur vegna vinnu, fyrir þá viðskiptamenn sem heyra til tiltekins verðlagningarflokks.  

#### [Núverandi reynsla](#tab/current-experience)
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustuvörur** og svo velja viðeigandi tengil.  
2. Veljið þjónustuvöruna, stækkið flýtiflipann **Verð og sala**, veljið aðgerðina **Tilfang**, **Vara** eða **Fjárhagsreikningur**.
3. Á síðunum **Forðaverð verks**, **Vöruverð verks** eða **Fjárhagsreikningsverð verks** skal fylla út reitina eins og þörf krefur.

  
## <a name="service-price-adjustment"></a>leiðréttingarþjónustuverð
Þjónustuverðleiðrétting gerir kleift að leiðrétta verð á vöru, forða, fjárhagsreikningi eða kostnaði í þjónustupöntun.  
  
Þegar vara hefur verið færð inn í þjónustuvörulínu eru allar upplýsingar um kostnað þessarar vöru færðar inn í þjónustulínurnar. Þegar aðgerðin Leiðrétta þjónustuverð er keyrð er hægt að forskoða verðbreytingar. Hægt er að gera lagfæringar ef þörf krefur. Þegar lagfæringarnar eru staðfestar reiknar kerfið út leiðréttingarnar og flytur þær síðan yfir í þjónustulínurnar. Þá er þjónustupöntunin bókuð.  
  
Heildarupphæð leiðréttinganna er reiknuð háð tegund þjónustuverðleiðréttinga.  
  
Eftirfarandi tafla lýsir útreikningunum.  
  
|Valkostur | Description |  
|----------------------------------|---------------------------------------|  
|**Fast verð**|Þetta þýðir að innheimt er fast verð fyrir þjónustuvöruna, forðann, fjárhagsreikninginn eða kostnaðinn, óháð raunverulegum kostnaði eða reglulegum gjöldum. Ef þessi kostur er valinn verður upphæð þjónustuverðleiðréttingar nákvæmlega sú upphæð sem tilgreind er í þjónustuverðflokknum.|  
|**Hámark**|Þetta þýðir að sett eru efri mörk á þau gjöld sem viðskiptavinur greiðir, óháð raunverulegum kostnaði eða reglulegum gjöldum. Ef þessi kostur er valinn verður þjónustuverðleiðréttingin aðeins gerð ef heildarverðið er hærra en sú upphæð sem tilgreind er í þjónustuverðflokknum.|  
|**Lágmark**|Þetta þýðir að sett eru neðri mörk á þau gjöld sem viðskiptavinur greiðir, óháð raunverulegum kostnaði eða reglulegum gjöldum. Ef þessi kostur er valinn verður þjónustuverðleiðréttingin aðeins gerð ef heildarupphæðin er lægri en sú upphæð sem tilgreind er í þjónustuverðflokknum.|  
  
## <a name="see-also"></a>Sjá einnig
[Setja upp verðlagningu og aukakostnað fyrir þjónustu](service-how-setup-service-costs-pricing.md)  
[Þjónustustýring sett upp](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
