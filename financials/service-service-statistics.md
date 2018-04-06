---
title: "Þjónustuupplýsingar | Microsoft Docs"
description: "Fáðu snöggt yfirlit yfir innihald alls þjónustuskjalsins, þ.m.t. pantanir, tilboð, reikninga eða kreditreikninga, sundurliðun á ákveðnum þjónustulínum og þjónustuvörur."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/04/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 6effbb7bd316eed24b20943e71f4e0bf8e9e8a3e
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---

# <a name="viewing-service-statistics"></a>Þjónustuupplýsingar skoðaðar
Financials getur gefið upplýsingar sem hægt er að nota til að greina þjónustuskjöl og ákvarða hversu vel þú stjórnar þjónustuferlinu. Þú getur greint þjónustusamninga, vörur, tilboð, pantanir, reikninga og kreditreikninga með því að velja aðgerðina **Upplýsingar**. Fyrir þjónustuvörur og samninga, geturðu líka notað **Þjónustuvara Trendscape** eða **Samningur Trendscape** til að skoða yfirlit yfir þjónustufærslur fyrir sérstaka þjónustuvöru.   

## <a name="viewing-statistics-for-service-orders"></a>Skoðun upplýsinga um þjónustupantanir
Eiginleikinn upplýsingar um þjónustupöntun veitir einfalt yfirlit yfir innihald allrar þjónustupöntunarinnar, upplýsingar um tilteknar þjónustulínur og upplýsingar sem tengjast reikningsfærslu, afhendingu og notkun, sem og stöðu viðskiptamanns.  

Upplýsingar um þjónustupöntun eru sýndar í glugganum **Upplýsingar um þjónustupöntun** fyrir pöntunina sem um ræðir. Hægt er að opna viðeigandi upplýsingaglugga úr þjónustupöntuninni. Í glugganum **Þjónustupantanir** skal velja **Upplýsingar**. Flýtifliparnir í þessum glugga sýna upplýsingar eins og magn, upphæð, VSK, kostnað og hámarksskuld viðskiptamanns. Upphæðirnar í glugganum eru á gjaldmiðli þjónustupöntunarinnar nema annað sé gefið til kynna.  

### <a name="view-totals-for-a-service-order"></a>Skoða samtölur fyrir þjónustupöntun  
Þú getur skoðað heildarupphæðir í þjónustulínum, með og án VSK, VSK hluta og kostnað og framlegð á þjónustulínum. Glugginn sýnir einnig sérstakar vörutengdar upplýsingar um vörurnar, svo sem þyngd, rúmmál og magn pakkninga.  

### <a name="view-shipping-information"></a>Skoða afhendingarupplýsingar  
Þú getur skoðað upplýsingar um vörur, forða eða kostnað til afhendingar. Til að veita upplýsingarnar eru gildin sem tilgreind eru í reitnum **Magn til afhendingar** notuð á hverja þjónustulínu í pöntuninni.  

### <a name="view-order-details"></a>Skoða pöntunarupplýsingar  
Hægt er að sjá upplýsingar um vörur, forðastundir og kostnað sem verða reikningsfærðar og notaðar. Eftirfarandi tafla lýsir upplýsingunum.  

|Dálkur | Lýsing|  
|------------|---------------------------------------|  
|**Reikningsfæra**|Birtir upphæðir sem bókaðar verða sem reikningsfærðar úr þjónustupöntuninni.|  
|**Notkun**|Birtir magn og kostnað við vörur eða forða sem bókaðar verða sem notaðar.|  
|**Samtals**|Birtir samtölur upphæðanna á þjónustupöntuninni sem fást með því að leggja reikningsfærsluupphæðir við notkunarupphæðir.|  

### <a name="analyze-service-order-lines"></a>Greina þjónustupöntunarlínur  
Hægt er að greina upplýsingarnar eftir tegundum þjónustulína sem hafðar eru með í þjónustupöntuninni. Upphæðir sýndar sérstaklega fyrir:  

* Birgðir  
* Forði  
* Kostnaður og fjárhagslyklar  

### <a name="view-customer-information"></a>Skoða upplýsingar um viðskiptamann  
Skoða stöðuna á reikningi viðskiptamanns og jafnframt hámarks kredit sem hægt er að úthluta viðskiptamanni sem þjónustuskjalið var búið til fyrir.

## <a name="viewing-service-item-statistics"></a>Skoða upplýsingar um þjónustuvöru
Í glugganum **Upplýsingar um þjónustuvöru** er hægt að skoða nýjustu upplýsingar um þjónustuvöru byggða á eftirfarandi þjónustufærslutegundum:  

* Forði  
* Birgðir  
* Þjónustukostn.  
* Þjónustusamninga  
* Samtals  

Fyrir hverja færslutegund er hægt að skoða reikningsfærða upphæð, notkun (upphæð), kostnaðarupphæð, magn, reikningsfært magn og notað magn, framlegðarupphæð og prósentu. Framlegðarprósentan er reiknuð í samkvæmt eftirfarandi formúlu:  

* (Reikningsfærð upphæð Notkun (Kostnaður)) x 100 Reikningsfærð upphæð  

## <a name="using-trendscapes"></a>Nota Trendscapes
Fyrir þjónustuvörur og þjónustusamninga, veita gluggarnir **þjónustuvara Trendscape** eða **Þjónustusamningur Trendscape** skrunanlega samantekt yfir þjónustubókarfærslur yfir tiltekið tímabil fyrir tiltekna þjónustuvöru eða þjónustusamning. Til að skoða Trendscape, skal opna þjónustuvöruna eða þjónustusamninginn, velja **Upplýsingar** aðgerðina og síðan velja **Trendscape**.

Þegar skrunað er upp eða niður eru upphæðirnar reiknaðar eftir því tímabili sem er valið í staðbundnum gjaldmiðli. Reiknaðar eru allar upphæðir af bókuðum þjónustufærslum, sem eru færslur sem eru stofnaðar þegar þjónustupantanir eða þjónustureikningar eru bókaðir.

Hægt er að afmarka listann með því að tilgreina þjónustuvörurnar sem á að taka með.  

> [!Tip]  
>  Ef tímabilið hefur verið sett á **Dagur** og skruna á yfir langt tímabil þá er hægt að gera það hraðar með því að skipta yfir í stærra millibil, svo sem **Fjórðungur**. Þegar tilhlýðilegt tímabil er fundið er hægt að skipta aftur í upprunaleg tímabil til að skoða gögnin nánar.   

## <a name="viewing-gains-and-losses-on-contracts"></a>Skoða hagnað og tap samninga  
Hagnaðar- eða tapfærslur samnings eru myndar í hvert sinn sem samningstilboði er breytt í þjónustusamning, þegar samningslínum er bætt við eða þeim eytt úr þjónustusamningum eða þegar samningar eru ógiltir. Hægt er að skoða hagnað eða tap samnings á eftirfarandi síðum.  

|Síða | Lýsing|  
|----------------|---------------------------------------|  
|**Hagn./tap samnings (samningar)**|Ef skoða á hagnaðar-/tapfærslur eftir þjónustusamningi.|  
|**Hagn./tap samnings (flokkar)**|Ef skoða á hagnaðar-/tapfærslur eftir þjónustusamningsflokki.|  
|**Hagn./tap samn. (viðsk.menn)**|Ef skoða á hagnaðar-/tapfærslur eftir viðskiptamanni.|  
|**Hagn./tap samnings (ástæður)**|Ef skoða á hagnaðar-/tapfærslur eftir ástæðukóta.|  
|**Hagn./tap samn. (ábyrgðarstöð)**|Ef skoða á hagnaðar-/tapfærslur eftir ábyrgðarstöð.|  

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn heiti síðunnar sem á að birta, og velja svo viðeigandi tengil.  
2. Fylla inn í afmörkunarskilyrði sem á að nota. Til dæmis í glugganum **Hagn./tap samnings (ástæður)** skal velja gildi fyrir **Afmörkun ástæðukóða**.  
3. Veljið aðgerðina **Sýna fylki**.

## <a name="viewing-statistics-for-posted-service-documents"></a>Skoðun upplýsinga fyrir bókuð þjónustuskjöl
Eiginleikinn Þjónustuupplýsingar gerir mögulegt að fá yfirlit yfir upplýsingar um innihald bókaðra þjónustuskjala, eins og til dæmis bókaðra afhendinga, bókaðra reikningsfærslna og bókaðra kreditreikninga.  

Upplýsingarnar sem eiga við samsvarandi bókað þjónustuskjal eru sýndar í upplýsingaglugganum. Hægt er að opna viðeigandi upplýsingaglugga úr bókaðri þjónustuafhendingu, bókuðum þjónustureikningi eða bókuðum þjónustukreditreikningi. Fyrir hverja þessara tegund skjala, á flipanum **Heim**, í flokknum **Vinna**, skal velja **Upplýsingar**. Til dæmis úr glugganum **Bókaðir þjónustureikningar**, á flipanum **Heim**, í flokknum **Vinnsla**, skal velja **Upplýsingar**.  

### <a name="posted-service-shipment-statistics"></a>Upplýsingar þjónustuafhendingar  
Í glugganum **Upplýsingar þjónustuafhendingar** er hægt að fá yfirlit yfir bókaðar þjónustuafhendingar. Þar á meðal eru upplýsingar um efnislegt innihald afhendingar, eins og til dæmis magn afhentrar vöru, forðastundir eða kostnað og þyngd og rúmmál afhentrar vöru.  

### <a name="posted-service-invoice-statistics"></a>Upplýsingar um bókaðan þjónustureikning  
Hægt er að skoða tölfræðilegt yfirlit um bókaðan þjónustureikning í glugganum **Reikningsupplýsingar þjónustu**. Hægt er að skoða samtölur bókaðrar þjónustureikninga. Í gögnunum eru samtölur í þjónustulínum (með og án VSK) sem búið er að bóka sem reikninga, VSK hluta og kostnað og framlegð á bókuðum reikningum. Í glugganum eru einnig eftirfarandi upplýsingar:  

* Um vörurnar í þjónustureikningslínunum, svo sem þyngd, rúmmál og magn pakkninga.  
* Stöðuna á reikningi viðskiptamanns og hámarks kredit sem hægt er að úthluta viðskiptamanni.  

### <a name="posted-service-credit-memo-statistics"></a>Upplýsingar um bókaðan þjónustukreditreikning  
Hægt er að nota gluggann **Kreditreikningsupplýsingar þjónustu** til þess að fá upplýsingar um línurnar í bókuðum þjónustukreditreikningi. Yfirlitið getur innihaldið:

* Samtölur bókaðra kreditreikninga, sýndar sem magn, upphæð, VSK, kostnað og framlegð. Einnig upplýsingar um vörurnar í þjónustulínum bókaðs kreditreiknings, eins og magn, þyngd og rúmmál.  
* Almennar upplýsingar um viðskiptamann, eins og t.d. lánamark viðskiptamanns og stöðu reiknings.  

## <a name="see-also"></a>Sjá einnig  
[Stofna Þjónustupantanir](service-how-to-create-service-orders.md)   
[Stofna þjónustuatriði](service-how-to-create-service-items.md)   
[Áætla þjónustu](service-plan-service.md)  

