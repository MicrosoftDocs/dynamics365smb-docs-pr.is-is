---
title: "Nota OCR til að breyta PDF í rafræn skjöl| Microsoft Docs"
description: "Lýsir því hvernig hægt er að nota OCR þjónustu til að breyta PDF-skrám eða myndaskrám á innleið yfir í rafræn skjöl í Financials."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 020aeed82d6147641936dee2d7b860791c76d2ee
ms.contentlocale: is-is
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-use-ocr-to-turn-pdf-and-image-files-into-electronic-documents"></a>Hvernig á að nota OCR til að breyta PDF og myndaskrám í rafræn skjöl
Úr PDF-skjölum eða myndaskrám sem standa fyrir skjöl á innleið er hægt að láta ytri OCR-þjónustu (sjónræn stafakennsl) stofna rafræn skjöl sem hægt er að umbreyta í skráarfærslur í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Til dæmis Þegar reikningur berst frá lánardrottni á PDF-sniði er til dæmis hægt að senda hann til OCR-þjónustu úr glugganum **Skjöl á innleið**. Þessu er lýst í fyrsta verkferlinu.

Sem valkostur við að senda skrá frá glugganum **Skjöl á innleið**, getur þú sent skrána í OCR þjónustu með tölvupósti. Þá, þegar þú færð rafræna skjal aftur, er tengd færsla fyrir skjal á innleið búin til sjálfkrafa. Þessu er lýst í öðru verkferlinu.

Eftir nokkrar sekúndur berst skráin aftur sem rafrænn reikningur sem hægt er að breyta í innkaupareikning fyrir lánardrottin. Þessu er lýst í þriðja verkferlinu.

Vegna þess að OCR byggist á sjónrænum stafakennslum getur OCR-þjónustan túlkað bókstafi í PDF-skjali eða myndaskrám á rangan hátt, til dæmis fyrst þegar hún vinnur úr skjölum frá tilteknum lánardrottni. Hún túlkar merki fyrirtækisins hugsanlega ekki sem nafn lánardrottins eða mistúlkar heildarupphæð á kostnaðarkvittun vegna þess hvernig hún er sett upp. Til að forðast þessar villur fara fram, er hægt að leiðrétta villur í sérstakri útgáfu af glugganum **Skjal á innleið**. Leiðréttingar eru svo sendar aftur til OCR þjónustu til að þjálfa hana í að túlka sértákn rétt næst þegar það ferli PDF eða myndskjal fyrir sama lánardrottinn. Frekari upplýsingar er að finna á hlutanum "Þjálfa OCR-þjónustu til að forðast villur"

Umferð skráa til og frá OCR þjónustu er unnin af sérstakri verkraðarfærslu, sem eru búin til sjálfkrafa þegar þú kveikir á viðeigandi þjónustu tengingu. Nánari upplýsingar er að finna í [Hvernig á að setja upp skjöl á innleið](across-how-setup-income-documents.md).

## <a name="to-send-a-pdf-or-image-file-to-the-ocr-service-from-the-incoming-documents-window"></a>Til að senda PDF eða myndaskrá til OCR þjónustu frá glugganum **Skjöl á innleið**.
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **skjöl á innleið** og velja svo viðeigandi tengil.
2. Búið til nýja færslu fyrir skjal á innleið og hengið skrána við. Frekari upplýsingar eru í [Hvernig á að stofna færslur fyrir skjal á innleið ](across-how-create-income-document-records.md).  
3. Í glugganum **skjöl á innleið**, á veldu eina eða fleiri línur og veldu svo **Senda í verkröð** aðgerðina.

    Gildið í reitnum  **OCR-staða** breytist í **Tilbúið**. Meðfylgjandi PDF eða ímynd skrá er send til OCR þjónustu af verkröðinni samkvæmt áætlun, að því tilskildu að engar villur eru.
4. Einnig, Í glugganum **skjöl á innleið**, á veldu eina eða fleiri línur og veldu svo **OCR-þjónusta** aðgerðina.

Gildið í reitnum **OCR-staða** breytist í **Sent** ef engar villur hafa komið upp.

## <a name="to-send-a-pdf-or-image-file-to-the-ocr-service-by-email"></a>Til að senda PDF eða myndaskrá til OCR þjónustu með tölvupósti
Úr tölvupóstforritinu er hægt að senda tölvupóst til OCR-þjónustuveitanda með viðhengdu PDF-skjali eða myndaskrá. Upplýsingar um netfang til að senda á er að finna á vefsvæði OCR-þjónustuveitanda.

Vegna þess að engin færsla er til fyrir skrána á innleið verður ný færsla búin til sjálfkrafa í **Skjöl á innleið**glugganum þegar þú færð rafræna skjalið sem búið var til frá OCR þjónustu. Frekari upplýsingar eru í [Hvernig á að stofna færslur fyrir skjal á innleið ](across-how-create-income-document-records.md).

> [!NOTE]  
>   Ef þú vinnur á töflu eða síma, getur þú sent skrána í OCR þjónustu eins fljótt og þú hefur tekið mynd af skjalinu, eða þú getur búið til skjal á innleið beint. Frekari upplýsingar í "Að stofna færslur fyrir skjöl á innleið með því að taka mynd" hlutanum í [Hvernig á að: Stofna færslur fyrir skjöl á innleið](across-how-create-income-document-records.md).

## <a name="to-receive-the-resulting-electronic-document-from-the-ocr-service"></a>Til að taka á móti viðkomandi rafrænt skjal frá OCR-þjónusta.
Rafrænt skjal sem er stofnaði af OCR-þjónustu úr PDF eða myndaskrá er sjálfkrafa mótteknar á glugganum **skjöl á innleið** af verkraðarfærslu sem er sett upp þegar þú virkjar OCR þjónustan.

Ef ekki eru notaðar verkröð eða þú vilt taka á móti loknu OCR-skjali fyrr en áætlun verkraðar segir til um, er hægt að velja **Móttöku úr OCR Þjónustu** hnappinn. Þetta fær öll skjöl sem eru kláruð af OCR-þjónustunni.

> [!NOTE]  
>   Ef OCR þjónustan er stillt þannig að krafist er handvirka sannprófun fyrir unnin skjöl, þá mun reiturinn **OCR Staða** inihalda **Bíður sannprófunar**. Í því tilfelli skal framkvæma eftirfarandi skref til að skrá sig inn á OCR-þjónustusíðu til að sannreyna OCR-skjal handvirkt.

1. Í á reitnum **OCR Stöðu** er valið **Bíður sannprófunar** tengilinn. Einnig má velja **bíður sannprófunar** gluggareit á heimasíðunni.
2. Á OCR-þjónustu vefsvæðið skal skrá inn með skilríki OCR-þjónustureiknings. Það eru sömu skilríki og voru notuð þegar þjónustan var sett upp. Nánari upplýsingar er að finna í "Setja upp OCR-þjónusta" hlutanum í [Hvernig á að setja upp skjöl á innleið](across-how-setup-income-documents.md).

    Ef þú ferð inn á vefsvæði úr reitnum **OCR Staða** er viðkomandi skjali birt strax eftir innskráningu. Ef vefsvæðið er opnað með því að velja gluggareitur á heimasíðu, á fyrsta OCR þjónustusíðu sem opnast, verður að velja **Hefja** hnappinn á **sannprófa** flipanum eða tvísmellt á skjalið sem á að sannprófa.

    Upplýsingar um skjalið OCR birtist, þar sem sýndar eru bæði upprunalegt efni PDF skjalsins eða myndskrárinnar og afleidd OCR-gildi reita.
3. Fara ber yfir mismunandi gildi og breyta eða færa inn handvirkt gildi í reitina sem OCR-þjónusta hefur merkt sem óvissa.
4. Velja hnappinn **Í lagi**. OCR vinnslunni er lokið og verða rafrænar skjal er sent á **Skjöl á innleið** í [!INCLUDE[d365fin](includes/d365fin_md.md)] eftir röð áætlun verksins.

    Ef vefsvæðið er opna með því að velja gluggareitur á heimasíðu, þá eru öll önnur OCR-skjöl til að sannprófa sjálfkrafa birt á vefsvæði.
5. Liðir 4 eru endurteknir fyrir öll önnur OCR-skjöl til að sannprófa.

Nú er hægt að byrja að stofna færslur skjala fyrir móttekin rafrænar fylgiskjöl í [!INCLUDE[d365fin](includes/d365fin_md.md)], handvirkt eða sjálfvirkt. Nánari upplýsingar er að finna í næsta ferli. Einnig er hægt að tengja nýja færslu skjals á innleið við fyrirliggjandi bókað eða óbókað skjal þannig að upprunaskrá sé auðvelt að fá aðgang úr [!INCLUDE[d365fin](includes/d365fin_md.md)]. Nánari upplýsingar er að finna í [vinna skjöl á innleið](across-process-income-documents.md).

## <a name="to-create-a-purchase-invoice-from-an-electronic-document-received-from-the-ocr-service"></a>Stofna innkaupareikning út frá rafræna skjalinu mótteknu úr OCR
Eftirfarandi ferli sýnir hvernig á að stofna færslu innkaupareiknings úr reikningur lánardrottins sem var móttekin sem rafrænt skjal úr OCR-þjónustu. Ferlið er það sama þegar búið er til, til dæmis, færslubókarlínu úr kostnaðarkvittun.

> [!NOTE]  
>   **Lýsingin** og **nr.** á stofnuðum skjalalínum verða aðeins fylltir út ef þú hefur fyrst varpað texta á OCR-skjali á reitunum tveimur í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hægt er að gera þetta annað hvort sem millivísun vöru, fyrir skjalalínur af gerðinni vara, eða sem vörpun texta á reikning, fyrir skjal eða færslubókarlínur af gerðinni Fjárhagsreikningur. Nánari upplýsingar sjá ábending fyrir **millivísanir** aðgerð á birgðaspjöldunum og tengdu ferli, [Hvernig á að: varpa texta á endurteknar greiðslur á reikninga fyrir sjálfvirka afstemmingu](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

Fyrir skjal á innleið er yfirleitt notuð **varpa texta á reikning** aðgerð til að skilgreina að tilteknum texta á reikning lánardrottins sem var móttekinn frá OCR-þjónustu er varpað á tilteknum lánardrottnareikning. Í framhaldinu merkja allir hlutar lýsingar fyrir skjal á innleið sem er til sem vörpunartexti að reiturinn **nr.** í afleiddum skjala- eða færslubókarlínum af gerðinni fjárhagur eru innfylltir með viðkomandi lánardrottni.

Til viðbótar við vörpun á lánardrottnareikning eða fjárhagsreikninga er einnig hægt að varpa á bankareikning. Þetta er hagkvæmt, til dæmis, fyrir rafræn skjöl tengd útgjöldum sem eru nú þegar greitt þegar þú vilt stofna færslubókarlíni sem er tilbúin til að bóka á bankareikning.

1. Velja línu fyrir skjal á innleið fyrir rafrænt skjal lánardrottins sem var móttekið úr OCR-þjónustunni.
2. Til að Varpa texta skjalsins á reikning lánardrottins, debetreikning, skal velja aðgerðina **Varpa texta á reikning** og síðan fylla út í **Vörpun texta á reikning** glugganum með upplýsingar sem eiga við lánardrottininn þaðan í frá. Fyrir frekar upplýsingar, sjá [Hvernig á að varpa texta á endurteknar greiðslur á reikninga fyrir sjálfvirka afstemmingu](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)
3. Til að varpa vörunúmerin á skjalinu í lýsingar þínar á vörum lánardrottins, skal opna kortið fyrir hverja vöru, og velja síðan **millivísanir** aðgerð til að setja upp millivísanir á milli þinna vörulýsinga og þess sem tilheyrir lánardrottinsins.
4. Í glugganum **Skjal á innleið** skal velja aðgerðina **stofna skjal**

Innkaupareikningur verður stofnaður í [!INCLUDE[d365fin](includes/d365fin_md.md)] og byggist á upplýsingum í rafrænu skjali lánardrottins sem tekið var á móti frá OCR-þjónustu.

Allar villur við villuleit, sem tengjast gjarnan gölluðum eða skemmdum gögnum í [!INCLUDE[d365fin](includes/d365fin_md.md)] verða sýndar á flýtiflipanum **Villuboð**. Nánari upplýsingar eru í "meðhöndlun villna þegar tekið er á móti rafræn skjöl" hlutanum.

## <a name="to-handle-errors-when-receiving-electronic-documents"></a>Hvernig á að: Meðhöndla villur við móttöku rafrænna skjala
1. Í glugganum **skjöl á innleið** skal velja línuna fyrir rafrænt skjal sem var móttekið frá OCR-þjónustu með villum. Þetta er gefið til kynna með Villugildinu í reitnum **OCR Stöðu**.
2. Veldu **breyta** aðgerðina til að opna gluggann **skjal á innleið** .
3. Í Flýtiflipanum **Villur og Viðvaranir** skal velja skilaboðin og síðan valið á **Opna Tengdar Skrá** aðgerð.
4. Glugginn sem inniheldur gölluð eða týnd gögn, t.d. viðskiptamannaspjald þar sem gildir vantar, opnast.
5. Leiðréttið villuna eða villurnar sem lýst er í hverju villuboðum.
6. Haldið áfram að vinna úr skjölum á innleið með því að velja aftur aðgerðina **Stofna handvirkt**.
7. Skref 5 til 6 eru endurtekin fyrir allar villur sem eftir eru þar til hægt er að taka á móti rafrænu skjali.

## <a name="to-train-the-ocr-service-to-avoid-errors"></a>Þjálfa OCR-þjónustu til að forðast villur
Vegna þess að OCR byggist á sjónrænum stafakennslum getur OCR-þjónustan túlkað bókstafi í PDF-skjali eða myndaskrám á rangan hátt, til dæmis fyrst þegar hún vinnur úr skjölum frá tilteknum lánardrottni. Hún túlkar merki fyrirtækisins hugsanlega ekki sem nafn lánardrottins eða mistúlkar heildarupphæð á kostnaðarkvittun vegna þess hvernig hún er sett upp. Til að komast hjá því að slíkar villur berist áfram er hægt að leiðrétta gögn úr OCR-þjónustu og senda athugasemdirnar aftur til þjónustuaðilans.

Glugginn **OCR-gagnalreiðrétting**, sem er opnaður úr glugga **skjal á innleið**, birtir reiti úr flýtiflipanum **Fjárhagsupplýsingar** í tveimur dálkum, einum þar sem hægt er að breyta OCR-gögnum og öðrum þar sem OCR-gögnin eru skrifvarin. Þegar hnappurinn **Senda leiðréttingarathugasemdir** er valinn er innihald gluggans **OCR-gagnalreiðrétting** sent OCR-þjónustunni. Næst þegar þjónustuaðilinn vinnur úr PDF-skjali eða myndaskrá sem inniheldur umrædd gögn verða stuðst við leiðréttingar notanda til að komast hjá sömu villu.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **skjöl á innleið** og velja svo viðeigandi tengil.
2. Opnaðu færslu fyrir skjal á innleið semn inniheldur gögn sem berast frá OCR þjónustu, sem þú vilt leiðrétta.
3. Í glugganum **Skjal á innleið** skal velja aðgerðina **leiðrétta OCR-gögn**
4. Í glugganum **OCR-gagnalreiðrétting** skal yfirskrifa gögnin í dálkinum sem hægt er að breyta fyrir hvern reit með rangt gildi.
5. Til að Afturkalla leiðréttingar sem hafa verið gerðar síðan glugginn **OCR-gagnalreiðrétting** var opnaður, veldu aðgerðina **endurstilla OCR-gögn**.
6. Til að senda leiðréttingar til OCR-þjónustu, veldu senda **OCR-leiðréttingarathugasemdir** aðgerðina.
7. Til að vista leiðréttingarnar skal loka glugganum **OCR-gagnalreiðrétting**.

Reitirnir í flýtiflipanum **Fjárhagsupplýsingar** í glugganum  **Skjal á innleið** eru uppfærðir með öllum nýjum gildum sem færð voru ínn í skrefi 4.

## <a name="see-also"></a>Sjá einnig
[Vinnsla skjala á innleið](across-process-income-documents.md)  
[Skjöl á innleið](across-income-documents.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

