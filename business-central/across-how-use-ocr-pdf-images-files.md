---
title: Nota OCR til að breyta PDF í rafræn skjöl| Microsoft Docs
description: Lýsir því hvernig hægt er að nota OCR þjónustu til að breyta PDF-skrám eða myndaskrám á innleið yfir í rafræn skjöl.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: c35ccb10ca67e66697002add56d518f3a7bacc0d
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305165"
---
# <a name="use-ocr-to-turn-pdf-and-image-files-into-electronic-documents"></a>Nota OCR til að breyta PDF og myndaskrám í rafræn skjöl
Úr PDF-skjölum eða myndaskrám sem standa fyrir skjöl á innleið er hægt að láta ytri OCR-þjónustu (sjónræn stafakennsl) stofna rafræn skjöl sem hægt er að umbreyta í skráarfærslur í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Þegar reikningur berst frá lánardrottni á PDF-sniði er til dæmis hægt að senda hann til OCR-þjónustu af síðunni **Skjöl á innleið**. Þessu er lýst í fyrsta verkferlinu.

Sem valkostur við að senda skrá af síðunni **Skjöl á innleið**, getur þú sent skrána í OCR þjónustu með tölvupósti. Þá, þegar þú færð rafræna skjal aftur, er tengd færsla fyrir skjal á innleið búin til sjálfkrafa. Þessu er lýst í öðru verkferlinu.

Eftir nokkrar sekúndur berst skráin aftur sem rafrænn reikningur sem hægt er að breyta í innkaupareikning fyrir lánardrottin. Þessu er lýst í þriðja verkferlinu.

Vegna þess að OCR byggist á sjónrænum stafakennslum getur OCR-þjónustan túlkað bókstafi í PDF-skjali eða myndaskrám á rangan hátt, til dæmis fyrst þegar hún vinnur úr skjölum frá tilteknum lánardrottni. Hún túlkar merki fyrirtækisins hugsanlega ekki sem nafn lánardrottins eða mistúlkar heildarupphæð á kostnaðarkvittun vegna þess hvernig hún er sett upp. Til að forðast þessar villur fara fram, er hægt að leiðrétta villur í sérstakri útgáfu af síðunni **Skjal á innleið**. Leiðréttingar eru svo sendar aftur til OCR þjónustu til að þjálfa hana í að túlka sértákn rétt næst þegar það ferli PDF eða myndskjal fyrir sama lánardrottinn. Frekari upplýsingar, sjá [Að þjálfa OCR-þjónustu til að forðast villur](across-how-use-ocr-pdf-images-files.md#to-train-the-ocr-service-to-avoid-errors).

Umferð skráa til og frá OCR þjónustu er unnin af sérstakri verkraðarfærslu, sem eru búin til sjálfkrafa þegar þú kveikir á viðeigandi þjónustu tengingu. Frekari upplýsingar eru í [Setja upp skjöl á innleið](across-how-setup-income-documents.md).

## <a name="to-send-a-pdf-or-image-file-to-the-ocr-service-from-the-incoming-documents-page"></a>Til að senda PDF eða myndaskrá til OCR þjónustu frá síðunni **Skjöl á innleið**
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Skjöl á innleið** og veldu síðan tengda tengilinn.
2. Búið til nýja færslu fyrir skjal á innleið og hengið skrána við. Frekari upplýsingar eru í [Stofna færslur skjala á innleið](across-how-create-income-document-records.md).  
3. Á síðunni **Skjöl á innleið**, á veldu eina eða fleiri línur og veldu svo **Senda í verkröð** aðgerðina.

    Gildið í reitnum  **OCR-staða** breytist í **Tilbúið**. Meðfylgjandi PDF eða ímynd skrá er send til OCR þjónustu af verkröðinni samkvæmt áætlun, að því tilskildu að engar villur eru.
4. Að öðrum kosti skal velja á síðunni **Skjöl á innleið** eina eða fleiri línur og velja svo aðgerðina **Senda til OCR-þjónustu**.

Gildið í reitnum **OCR-staða** breytist í **Sent** ef engar villur hafa komið upp.

## <a name="to-send-a-pdf-or-image-file-to-the-ocr-service-by-email"></a>Til að senda PDF eða myndaskrá til OCR þjónustu með tölvupósti
Úr tölvupóstforritinu er hægt að senda tölvupóst til OCR-þjónustuveitanda með viðhengdu PDF-skjali eða myndaskrá. Upplýsingar um netfang til að senda á er að finna á vefsvæði OCR-þjónustuveitanda.

Vegna þess að engin færsla er til fyrir skrána á innleið verður ný færsla búin til sjálfkrafa í **Skjöl á innleið** síðunni þegar þú færð rafræna skjalið sem búið var til frá OCR þjónustu. Frekari upplýsingar eru í [Stofna færslur skjala á innleið](across-how-create-income-document-records.md).

> [!NOTE]  
>   Ef þú vinnur á töflu eða síma, getur þú sent skrána í OCR þjónustu eins fljótt og þú hefur tekið mynd af skjalinu, eða þú getur búið til skjal á innleið beint. Frekari upplýsingar er að finna í [Að stofna færslur skjala á innleið með því að taka mynd](across-how-create-income-document-records.md#to-create-an-incoming-document-record-by-taking-a-photo).

## <a name="to-receive-the-resulting-electronic-document-from-the-ocr-service"></a>Til að taka á móti viðkomandi rafrænt skjal frá OCR-þjónusta.
Rafrænt skjal sem er stofnaði af OCR-þjónustu úr PDF eða myndaskrá er sjálfkrafa mótteknar á síðunni **skjöl á innleið** af verkraðarfærslu sem er sett upp þegar þú virkjar OCR þjónustan.

Ef ekki eru notaðar verkröð eða þú vilt taka á móti loknu OCR-skjali fyrr en áætlun verkraðar segir til um, er hægt að velja **Móttöku úr OCR Þjónustu** hnappinn. Þetta fær öll skjöl sem eru kláruð af OCR-þjónustunni.

> [!NOTE]  
>   Ef OCR þjónustan er stillt þannig að krafist er handvirka sannprófun fyrir unnin skjöl, þá mun reiturinn **OCR Staða** inihalda **Bíður sannprófunar**. Í því tilfelli skal framkvæma eftirfarandi skref til að skrá sig inn á OCR-þjónustusíðu til að sannreyna OCR-skjal handvirkt.

1. Í á reitnum **OCR Stöðu** er valið **Bíður sannprófunar** tengilinn.
2. Á OCR-þjónustu vefsvæðið skal skrá inn með skilríki OCR-þjónustureiknings. Það eru sömu skilríki og voru notuð þegar þjónustan var sett upp. Frekari upplýsingar eru í [Að setja upp OCR-þjónustu](across-how-setup-income-documents.md#to-set-up-an-ocr-service).

    Upplýsingar um skjalið OCR birtist, þar sem sýndar eru bæði upprunalegt efni PDF skjalsins eða myndskrárinnar og afleidd OCR-gildi reita.
3. Fara ber yfir mismunandi gildi og breyta eða færa inn handvirkt gildi í reitina sem OCR-þjónusta hefur merkt sem óvissa.
4. Velja hnappinn **Í lagi**. OCR-vinnslunni er lokið og rafræna skjalið er sent á síðuna **Skjöl á innleið** í [!INCLUDE[d365fin](includes/d365fin_md.md)] samkvæmt áætlun verkraðar.
5. Liðir 4 eru endurteknir fyrir öll önnur OCR-skjöl til að sannprófa.

Nú er hægt að byrja að stofna færslur skjala fyrir móttekin rafrænar fylgiskjöl í [!INCLUDE[d365fin](includes/d365fin_md.md)], handvirkt eða sjálfvirkt. Nánari upplýsingar er að finna í næsta ferli. Einnig er hægt að tengja nýja færslu skjals á innleið við fyrirliggjandi bókað eða óbókað skjal þannig að upprunaskrá sé auðvelt að fá aðgang úr [!INCLUDE[d365fin](includes/d365fin_md.md)]. Nánari upplýsingar er að finna í [vinna skjöl á innleið](across-process-income-documents.md).

## <a name="to-create-a-purchase-invoice-from-an-electronic-document-received-from-the-ocr-service"></a>Stofna innkaupareikning út frá rafræna skjalinu mótteknu úr OCR
Eftirfarandi ferli sýnir hvernig á að stofna færslu innkaupareiknings úr reikningur lánardrottins sem var móttekin sem rafrænt skjal úr OCR-þjónustu. Ferlið er það sama þegar búið er til, til dæmis, færslubókarlína úr kostnaðarkvittun eða söluvöruskilapöntun frá viðskiptamanni.

> [!NOTE]  
>   **Lýsingin** og **nr.** á stofnuðum skjalalínum verða aðeins fylltir út ef þú hefur fyrst varpað texta á OCR-skjali á reitunum tveimur í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hægt er að gera þessa vörpun sem millivísun vöru, fyrir skjalalínur af gerðinni vara. Frekari upplýsingar er að finna í [Nota millivísanir vöru](inventory-how-use-item-cross-refs.md). Einnig er hægt að nota virknina vörpun texta á reikning. Nánari upplýsingar er að finna í [Að varpa texta í skjali á innleið á tiltekinn lánardrottin, fjárhag eða bankareikning](across-how-use-ocr-pdf-images-files.md#to-map-text-on-an-incoming-document-to-a-specific-vendor-account).

1. Velja skal línu fyrir skjal á innleið og svo **Stofna skjal** virknina.

Innkaupareikningur verður stofnaður í [!INCLUDE[d365fin](includes/d365fin_md.md)] og byggist á upplýsingum í rafrænu skjali lánardrottins sem tekið var á móti frá OCR-þjónustu. Upplýsingar verða settar inn í nýja innkaupareikninginn byggt á vörpun sem hefur verið tilgreind sem millivísun eða sem vörpun texta á reikning.

Allar villur við villuleit, sem tengjast gjarnan gölluðum eða skemmdum gögnum í [!INCLUDE[d365fin](includes/d365fin_md.md)] verða sýndar á flýtiflipanum **Villuboð**. Nánari upplýsingar eru í [Að meðhöndla villur þegar tekið er á móti rafrænum skjölum](across-how-use-ocr-pdf-images-files.md#to-handle-errors-when-receiving-electronic-documents).

### <a name="to-map-text-on-an-incoming-document-to-a-specific-vendor-account"></a>Til að varpa texta á tiltekinn lánardrottinn, fjárhag eða bankareikning
Fyrir skjal á innleið er yfirleitt notuð **varpa texta á reikning** aðgerð til að skilgreina að tilteknum texta á reikning lánardrottins sem var móttekinn frá OCR-þjónustu er varpað á tilteknum lánardrottnareikning. Í framhaldinu merkja allir hlutar lýsingar fyrir skjal á innleið sem er til sem vörpunartexti að reiturinn **nr.** í afleiddum skjala- eða færslubókarlínum af gerðinni fjárhagur eru innfylltir með viðkomandi lánardrottni.

Til viðbótar við vörpun á lánardrottnareikning eða fjárhagsreikninga er einnig hægt að varpa á bankareikning. Þetta er hagkvæmt, til dæmis, fyrir rafræn skjöl tengd útgjöldum sem eru nú þegar greitt þegar þú vilt stofna færslubókarlíni sem er tilbúin til að bóka á bankareikning.

1. Viðkomandi lína skjals á innleið er valin og svo aðgerðin **Varpa Texta á reikning**. Síðan **vörpun texta á reikning** opnast.
3. Í reitinn **Vörpun texta** skal slá inn þann texta sem kemur fram á reikningum lánardrottins sem á að búa til innkaupaskjöl eða færslubókarlínur fyrir. Hægt er að færa inn allt að 50 stafi.
4. Í **Númer lánardrottins** reitinn skal færa inn númer lánardrottins sem innkaupaskjal eða færslubókarlína verður stofnað fyrir.
5. Í reitinn **Debetreikningsnúmer** skal færa inn fjárhagsreikning af debetgerð sem verður settur inn á viðkomandi innkaupaskjal eða færslubókarlínu af gerðinni fjárhagsreikningur.
6. Í reitinn **Kreditreikningsnúmer** skal færa inn fjárhagsreikning af kreditgerð sem verður settur inn á viðkomandi innkaupaskjal eða færslubókarlínu af gerðinni fjárhagsreikningur.

    > [!NOTE]
    > Ekki skal nota **Upprunagerð stöðu** og **Upprunanúmer stöðu** reitina í tengslum við skjöl á innleið. Þeir eru aðeins notaðir fyrir afstemmingu sjálfvirkra greiðslna. Frekari upplýsingar er að finna í [Varpa texta um endurteknar greiðslur í reikninga fyrir sjálfvirka afstemmingu](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

7. Endurtakið skref 2 til 5 fyrir allan texta í skjölum á innleið sem á búa sjálfkrafa til skjöl fyrir.

## <a name="to-handle-errors-when-receiving-electronic-documents"></a>Hvernig á að: Meðhöndla villur við móttöku rafrænna skjala
1. Á síðunni **Skjöl á innleið** skal velja línuna fyrir rafrænt skjal sem var móttekið frá OCR-þjónustu með villum. Þetta er gefið til kynna með Villugildinu í reitnum **OCR Stöðu**.
2. Veldu **breyta** aðgerðina til að opna síðuna **skjal á innleið** .
3. Í Flýtiflipanum **Villur og Viðvaranir** skal velja skilaboðin og síðan valið á **Opna Tengdar Skrá** aðgerð.
4. Síðan sem inniheldur gölluð eða týnd gögn, t.d. viðskiptamannaspjald þar sem gildir vantar, opnast.
5. Leiðréttið villuna eða villurnar sem lýst er í hverju villuboðum.
6. Haldið áfram að vinna úr skjölum á innleið með því að velja aftur aðgerðina **Stofna handvirkt**.
7. Skref 5 til 6 eru endurtekin fyrir allar villur sem eftir eru þar til hægt er að taka á móti rafrænu skjali.

## <a name="to-train-the-ocr-service-to-avoid-errors"></a>Þjálfa OCR-þjónustu til að forðast villur
Vegna þess að OCR byggist á sjónrænum stafakennslum getur OCR-þjónustan túlkað bókstafi í PDF-skjali eða myndaskrám á rangan hátt, til dæmis fyrst þegar hún vinnur úr skjölum frá tilteknum lánardrottni. Hún túlkar merki fyrirtækisins hugsanlega ekki sem nafn lánardrottins eða mistúlkar heildarupphæð á kostnaðarkvittun vegna þess hvernig hún er sett upp. Til að komast hjá því að slíkar villur berist áfram er hægt að leiðrétta gögn úr OCR-þjónustu og senda athugasemdirnar aftur til þjónustuaðilans.

Síðan **OCR-gagnalreiðrétting**, sem er opnuð af síðunni **skjal á innleið**, birtir reiti úr flýtiflipanum **Fjárhagsupplýsingar** í tveimur dálkum, einum þar sem hægt er að breyta OCR-gögnum og öðrum þar sem OCR-gögnin eru skrifvarin. Þegar hnappurinn **Senda OCR-athugasemdir** er valinn er innihald síðunnar **OCR-gagnaleiðrétting** sent OCR-þjónustunni. Næst þegar þjónustuaðilinn vinnur úr PDF-skjali eða myndaskrá sem inniheldur umrædd gögn verða stuðst við leiðréttingar notanda til að komast hjá sömu villu.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Skjöl á innleið** og veldu síðan tengda tengilinn.
2. Opnaðu færslu fyrir skjal á innleið semn inniheldur gögn sem berast frá OCR þjónustu, sem þú vilt leiðrétta.
3. Á síðunni **Skjal á innleið** skal velja aðgerðina **leiðrétta OCR-gögn**.
4. Á síðunni **OCR-gagnalreiðrétting** skal yfirskrifa gögnin í dálkinum sem hægt er að breyta fyrir hvern reit með rangt gildi.
5. Til að afturkalla leiðréttingar sem hafa verið gerðar síðan **OCR-gagnaleiðrétting** var opnuð skal velja aðgerðina **Endurstilla OCR-gögn**.
6. Til að senda leiðréttingar til OCR-þjónustu, veldu senda **OCR-leiðréttingarathugasemdir** aðgerðina.
7. Til að vista leiðréttingarnar skal loka síðunni **OCR-gagnalreiðrétting**.

Reitirnir í flýtiflipanum **Fjárhagsupplýsingar** á síðunni **Skjal á innleið** eru uppfærðir með öllum nýjum gildum sem færð voru ínn í skrefi 4.

## <a name="see-also"></a>Sjá einnig
[Vinnsla skjala á innleið](across-process-income-documents.md)  
[Skjöl á innleið](across-income-documents.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
