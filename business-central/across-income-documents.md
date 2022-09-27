---
title: Vinna með móttekin skjöl
description: Hægt er að stjórna ytri viðskiptaskjölum á innleið, eins og greiðslukvittunum og PDF skrám, stjórna OCR verkum, og umbreyta skrám yfir í rafræn skjöl og færslur.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/14/2022
ms.author: edupont
ms.openlocfilehash: 8b84e6f832ca5ab7908d7ed00ff7976b073df082
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/19/2022
ms.locfileid: "9529758"
---
# <a name="incoming-documents"></a>Fylgiskjöl á innleið

Ytri viðskiptakjör geta komið inn á fyrirtækið sem viðhengi í tölvupósti eða á pappírsafriti sem þú skannað í skrá. Þessi atburðarás er dæmigerð fyrir innkaup, þar sem slíkar skrár á innleið tákna greiðslu fyrir útgjöld eða lítið innkaup.

Á síðunni **Skjöl á innleið** er hægt að nota ólíkar aðgerðir til að yfirfara kostnaðarkvittanir, sýsla með OCR-verk og breyta skjölum á innleið, handvirkt eða sjálfvirkt, yfir í viðkomandi skjöl eða færslubókarlínur í. Ytri skrárnar er hægt að hengja við tengd skjöl á öllum stigum úrvinnslunnar, þ.m.t. við bókuð skjöl og við færslur lánardrottins, viðskiptamanns eða fjárhags sem verða til.

## <a name="usage-scenario"></a>Notkunaraðstæður

Þú getur skráð skrár eða pappírseintök sem berast frá viðskiptafélögum þínum í [!INCLUDE[prod_short](includes/prod_short.md)] og búið til skjalaskrá. Til dæmis innkaupa-eða sölureikning, kreditreikning eða færslubókarlínu.

Hlaða inn mótteknu skránum — eða nota myndavél tækisins til að taka ljósmynd — og búa til færslur til að tákna ytri skjölin. Með PDF-eða myndskrám er hægt að hafa ytri OCR-þjónustu (Optical Stafsviðurkenning) mynda rafræn skjöl sem síðan er hægt að umbreyta í færslur innan frá [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> OCR-aðgerðin er veitt af utanaðkomandi veitum. Veljið uppfærslupakka sem er viðeigandi fyrir fyrirtækið og/eða landið/svæðið. Finna þjónustur sem [!INCLUDE[prod_short](includes/prod_short.md)] eru samhæfðar og upplýsingar um tiltæka eiginleika í [AppSource . microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).

Þegar reikningur berst frá lánardrottni á PDF-sniði er til dæmis hægt að senda hann til OCR-þjónustu af síðunni **Skjöl á innleið**. Einnig hafa sumir OCR-veitur möguleika á að vinna skrár sem framsendar eru að sérhæfðu netfangi sem stofnar síðan sjálfkrafa tengda færslu á innleið. Eftir nokkrar sekúndur berst skráin aftur sem rafrænn reikningur sem hægt er að breyta í innkaupareikning fyrir lánardrottin.

> [!TIP]
> Stofna skjalaskrár á innleið í [!INCLUDE[prod_short](includes/prod_short.md)] beint úr tölvupósti sem sendur er af lánardrottnum með Outlook viðbóunni. Frekari upplýsingar er að finna [í notkun Viðskiptaseðla sem fyrirtækið innheldur í Outlook](work-outlook-addin.md).

## <a name="incoming-document-features"></a>Skjalaeiginleikar í komandi skjali

Ferlið vegna skjal á innleið getur samanstaðið af eftirfarandi aðgerðir:

* Skrá ytri skjöl innan [!INCLUDE[prod_short](includes/prod_short.md)] með því að stofna línur á síðunni **skjöl á innleið** með öðrum hvorum eftirfarandi hætti:
  * Handvirkt, annaðhvort úr PC eða úr farsíma, á einn eftirfarandi hátt:
    * **Notaðu hnappinn skrá Create in File**, senda inn skrá og fylltu síðan út viðeigandi reiti á **síðunni komandi skjal**.
    * **Notaðu hnappinn Nýtt**, fylltu út viðeigandi reiti á **síðunni utanaðkomandi skjal** og tengdu handvirkt skrána.
    * Frá töflu eða síma skal nota **hnappinn Búa til úr myndavél** til að búa til nýja skjalaskráningu sem er með innbyggðri myndavél tækisins.
  * Sjálfkrafa, með því að taka á móti skjalinu frá OCR Service sem rafrænt skjal eftir að þú hefur hlaðið upp eða send tenginu PDF eða myndskrá til OCR þjónustu. Flýtiflipinn **Fjárhagsupplýsingar** er fylltur út sjálfkrafa á síðunni **skjal á innleið**.
* Notaðu utanáliggjandi OCR-þjónustu til að hafa PDF-eða myndskrár er snúa að rafrænum skjölum sem hægt er að umbreyta í skjalaskýrslur í [!INCLUDE[prod_short](includes/prod_short.md)].
* Stofnið ný skjöl eða almenn færslubókarlínur fyrir færslur fyrir skjöl á innleið með því að slá inn upplýsingar um leið og þú lest þær úr skrám fyrir skjöl á innleið.
* Festið skjöl á innleið við innkaupa og söluskjöl með hvaða stöðu sem er, þar með talinn færslur fyrir lánardrottins, viðskiptamaður eða fjárhagsfærslur sem koma úr bókun.
* Skoða skjal á innleið og viðhengi þeirra úr hvaða innkaupa eða söluskjali eða færslu eða finna allar fjárhagsfærslur án færslna fyrir skjöl á innleið af síðunni **bókhaldslykill**.

> [!NOTE]
> Skrár sem tengjast spjöldum og skjölum á **flipanum viðhengi** eru ekki hafðar með á **síðunni utanaðkomandi skjöl**. Frekari upplýsingar er að finna í [Stjórna viðhengjum, tenglum og athugasemdum á spjöldum og fylgiskjölum](ui-how-add-link-to-record.md).

| Til | Sjá |
| --- | --- |
| Setja upp **aðgerðina utanaðkomandi skjöl** og setja upp OCR-þjónustu. |[Setja upp skjöl á innleið](across-how-setup-income-documents.md) |
| Búa til færslur fyrir skjöl á innleið handvirkt eða sjálfvirkt með því að taka mynd af pappírskvittun, til dæmis. |[Stofna færslur skjala á innleið](across-how-create-income-document-records.md) |
| Notið OCR-þjónustu til að breyta PDF eða myndaskrár í rafræn skjöl sem hægt er að breyta í innkaupareikninga í [!INCLUDE[prod_short](includes/prod_short.md)], til dæmis. Þjálfa OCR-þjónustu til að forðast villur næst þegar það vinnur álíka gögn. |[Nota OCR til að breyta PDF og myndaskrám í rafræn skjöl](across-how-use-ocr-pdf-images-files.md) |
| Tengja eða fjarlægja færslur fyrir skjal á innleið við óbókuð sölu- eða innkaupaskjöl og við viðskiptamaður, lánardrottin eða fjárhagsfærsla úr skjali eða færslu. |[Stofna færslur yfir Skjöl á innleið, beint úr Skjöl og Færslur](across-how-connect-disconnect-income-document-records.md) |
| **Í bókhaldslykilinn og** **á síðum bókhaldanna** skal nota Leitaraðgerð til að finna fjárhagsfærslur fyrir bókuð skjöl sem hafa ekki innsendar skjalaskýrslur og tengja síðan miðmiðafærslum við fyrirliggjandi færslur eða stofna nýjar með viðhengum skjalaskrám. |[Finna bókuð fylgiskjöl án færslu skjals á innleið](across-how-find-posted-documents-without-income-document-records.md) |
| Fá betri yfirsýn með því að setja komandi skjalaskrár til *vinnslu* og fjarlægja þær úr sjálfgefnu yfirliti. |[Vinna með margar færslur skjala á innleið](across-how-manage-many-income-document-records.md) |

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/incoming-documents-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig .

[Innkaup](purchasing-manage-purchasing.md)  
[Breyta bókuðum skjölum](across-edit-posted-document.md)  
[Rafræn gagnaskipti](across-data-exchange.md)  
[Business Central og OneDrive fyrir Business Integration](across-onedrive-overview.md)  
[Nota viðskipti miðlægt sem Viðskiptahólf í Outlook](work-outlook-addin.md)  
[Senda skjöl og tölvupóst](ui-how-send-documents-email.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
