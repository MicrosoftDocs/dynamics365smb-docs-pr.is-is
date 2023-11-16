---
title: Vinna með skjöl á innleið
description: 'Hægt er að stjórna ytri viðskiptaskjölum á innleið, eins og greiðslukvittunum og PDF skrám, stjórna OCR verkum, og umbreyta skrám yfir í rafræn skjöl og færslur.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: bholtorf
---
# <a name="incoming-documents"></a>Fylgiskjöl á innleið

Ytri viðskiptaskjöl geta komið inn í fyrirtækið þitt sem tölvupóstviðhengi eða pappírseintök sem þú skannar á skrá. Þessi sviðsmynd er dæmigerð fyrir innkaup, þar sem slíkar skrár fyrir skjal á innleið standa fyrir greiðslukvittanir eða lítil innkaup.

Á síðunni **Skjöl á innleið** er hægt að nota ólíkar aðgerðir til að yfirfara kostnaðarkvittanir, sýsla með OCR-verk og breyta skjölum á innleið, handvirkt eða sjálfvirkt, yfir í viðkomandi skjöl eða færslubókarlínur í. Ytri skrárnar er hægt að hengja við tengd skjöl á öllum stigum úrvinnslunnar, þ.m.t. við bókuð skjöl og við færslur lánardrottins, viðskiptamanns eða fjárhags sem verða til.

## <a name="usage-scenario"></a>Notkunarsvið

Þú getur skráð skrár eða pappírseintök sem þú hefur fengið frá viðskiptafélögum þínum í [!INCLUDE[prod_short](includes/prod_short.md)] og búið til skjalaskrá. Til dæmis innkaupa- eða söluskjal, kreditreikning eða færslubókarlínu.

Hladdu upp mótteknum skrám – eða notaðu myndavél tækisins til að taka mynd – og stofnaðu færslur sem standa fyrir ytri skjölin. Valfrjálst með PDF-skjölum eða myndaskrám geturðu látið ytri OCR-þjónustu (stafakennsl) búa til rafræn skjöl sem hægt er að umbreyta í færslur í [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> OCR-eiginleikinn er í boði ytri veitu. Veljið uppfærslupakka sem er viðeigandi fyrir fyrirtækið og/eða landið/svæðið. Finndu þjónustu sem er samhæf [!INCLUDE[prod_short](includes/prod_short.md)] og upplýsingar um eiginleika í boði á [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).

Þegar reikningur berst frá lánardrottni á PDF-sniði er til dæmis hægt að senda hann til OCR-þjónustu af síðunni **Skjöl á innleið**. Einnig bjóða sumar OCR-veitur upp á að vinna úr skrám sem sendar eru áfram á sérstakt netfang, sem býr þá sjálfkrafa til skrá yfir tengd skjöl á innleið. Eftir nokkrar sekúndur berst skráin aftur sem rafrænn reikningur sem hægt er að breyta í innkaupareikning fyrir lánardrottin.

> [!TIP]
> Búðu til færslur fyrir skjal á innleið í [!INCLUDE[prod_short](includes/prod_short.md)] beint úr tölvupóstum sem lánardrottnar senda með Outlook-innbótinni. Nánari upplýsingar, sjá [Nota Business Central sem viðskiptainnboxið þitt í Outlook](work-outlook-addin.md).

## <a name="incoming-document-features"></a>Eiginleikar skjals á innleið

Ferlið vegna skjal á innleið getur samanstaðið af eftirfarandi aðgerðir:

* Skrá ytri skjöl innan [!INCLUDE[prod_short](includes/prod_short.md)] með því að stofna línur á síðunni **skjöl á innleið** með öðrum hvorum eftirfarandi hætti:
  * Handvirkt, annaðhvort úr tölvu eða farsíma, með einni af eftirfarandi leiðum:
    * Notaðu hnappinn **Búa til úr skrá**, hladdu upp skrá og fylltu svo út viðeigandi reiti á síðunni **Skjal á innleið**.
    * Notaðu hnappinn **Nýtt**, fylltu út í viðeigandi reiti á síðunni **Skjal á innleið** og hengdu handvirkt tengda skrá við.
    * Úr spjaldtölvu eða síma, notaðu hnappinn **Búa til úr myndavél** til að stofna nýja færslu fyrir skjal á innleið með innbyggðri myndavél tækisins.
  * Sjálfkrafa, með því að taka á móti skjal frá OCR-þjónustu sem rafrænu skjali eftir að hafa hlaðið upp eða sent tengda PDF- eða myndaskrá í tölvupósti til OCR-þjónustu. Flýtiflipinn **Fjárhagsupplýsingar** er fylltur út sjálfkrafa á síðunni **skjal á innleið**.
* Notaðu ytri OCR-þjónustu til að breyta PDF eða myndaskrám í rafræn skjöl sem hægt er að breyta í færslur fyrir skjöl í [!INCLUDE[prod_short](includes/prod_short.md)].
* Stofnið ný skjöl eða almenn færslubókarlínur fyrir færslur fyrir skjöl á innleið með því að slá inn upplýsingar um leið og þú lest þær úr skrám fyrir skjöl á innleið.
* Festið skjöl á innleið við innkaupa og söluskjöl með hvaða stöðu sem er, þar með talinn færslur fyrir lánardrottins, viðskiptamaður eða fjárhagsfærslur sem koma úr bókun.
* Skoða skjal á innleið og viðhengi þeirra úr hvaða innkaupa eða söluskjali eða færslu eða finna allar fjárhagsfærslur án færslna fyrir skjöl á innleið af síðunni **bókhaldslykill**.

> [!NOTE]
> Skrár sem hengdar eru við spjöld eða skjöl í flipanum **Viðhengi** eru ekki hafðar með á síðunni **Skjöl á innleið**. Frekari upplýsingar er að finna í [Stjórna viðhengjum, tenglum og athugasemdum á spjöldum og fylgiskjölum](ui-how-add-link-to-record.md).

| Til | Sjá |
| --- | --- |
| Setja upp valkostinn fyrir **skjal á innleið** og setja upp OCR-þjónustu. |[Setja upp skjöl á innleið](across-how-setup-income-documents.md) |
| Búa til færslur fyrir skjöl á innleið handvirkt eða sjálfvirkt með því að taka mynd af pappírskvittun, til dæmis. |[Stofna færslur skjala á innleið](across-how-create-income-document-records.md) |
| Notið OCR-þjónustu til að breyta PDF eða myndaskrár í rafræn skjöl sem hægt er að breyta í innkaupareikninga í [!INCLUDE[prod_short](includes/prod_short.md)], til dæmis. Þjálfa OCR-þjónustu til að forðast villur næst þegar það vinnur álíka gögn. |[Nota OCR til að breyta PDF og myndaskrám í rafræn skjöl](across-how-use-ocr-pdf-images-files.md) |
| Tengja eða fjarlægja færslur fyrir skjal á innleið við óbókuð sölu- eða innkaupaskjöl og við viðskiptamaður, lánardrottin eða fjárhagsfærsla úr skjali eða færslu. |[Stofna færslur yfir Skjöl á innleið, beint úr Skjöl og Færslur](across-how-connect-disconnect-income-document-records.md) |
| Af síðunum **Bókhaldslyklar** og **Fjárhagsfærslur** er hægt að nota leitaraðgerð til að finna fjárhagsfærslur fyrir bókuð skjöl sem hafa ekki færslur fyrir skjöl á innleið og tengjast miðlægt við fyrirliggjandi færslur eða stofna nýjar með viðhengdum skrám. |[Finna bókuð fylgiskjöl án færslu skjals á innleið](across-how-find-posted-documents-without-income-document-records.md) |
| Fáðu betri yfirsýn með því að stilla færslur fyrir skjöl á innleið á *Unnið* og fjarlægja þær úr sjálfgefna yfirlitinu. |[Vinna með margar færslur skjala á innleið](across-how-manage-many-income-document-records.md) |

## <a name="see-also"></a>Sjá einnig .

[Innkaup](purchasing-manage-purchasing.md)  
[Breyting á bókuðum skjölum](across-edit-posted-document.md)  
[Rafræn gagnaskipti](across-data-exchange.md)  
[Business Central og OneDrive fyrir Business Integration](across-onedrive-overview.md)  
[Nota Business Central sem fyrirtækjainnhólf í Outlook](work-outlook-addin.md)  
[Senda skjöl og tölvupósta](ui-how-send-documents-email.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
