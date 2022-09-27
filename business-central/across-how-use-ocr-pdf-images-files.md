---
title: Notaðu OCR til að kveikja PDF í E-reikningum
description: Lýsir því hvernig hægt er að nota OCR þjónustu til að breyta PDF-skrám eða myndaskrám á innleið yfir í rafræn skjöl.
documentationcenter: ''
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/14/2022
ms.author: edupont
ms.openlocfilehash: 74263e606c11b0491a1f84277d75493c26cf8efe
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/19/2022
ms.locfileid: "9534346"
---
# <a name="use-ocr-to-turn-pdf-and-image-files-into-electronic-documents"></a>Nota OCR til að breyta PDF og myndaskrám í rafræn skjöl

Úr PDF-skjölum eða myndaskrám sem standa fyrir skjöl á innleið er hægt að láta ytri OCR-þjónustu (sjónræn stafakennsl) stofna rafræn skjöl sem hægt er að umbreyta í skráarfærslur í [!INCLUDE[prod_short](includes/prod_short.md)]. Sem dæmi má nefna að þegar reikningur er mótteinn á PDF-formi frá söluaðila er hægt [að senda hann í OCR-þjónustuna af **síðunni aðsend skjöl**](#to-send-a-pdf-or-image-file-to-the-ocr-service-from-the-incoming-documents-page).

Þar sem valkostur við að senda skrána af **síðunni utanaðkomandi skjöl** getur OCR Service boðið upp á þann valkost að [vinna skrár sem framsendar eru á sérhæfðu netfangi](#to-send-a-pdf-or-image-file-to-the-ocr-service-by-email). Þegar rafræna skjalið er móttekið er síðan sjálfkrafa stofnuð tengd færsla á innleið í [!INCLUDE[prod_short](includes/prod_short.md)].

Eftir nokkrar sekúndur sendir OCR þjónustuna unna skrá **á síðu aðsend skjöl** sem rafræna skjalaskrá sem hægt [er að umbreyta í innkaupareikning fyrir lánardrottni](#to-receive-the-resulting-electronic-document-from-the-ocr-service), sölureikning, kreditreikning eða bókarfærslu.

Þar sem OCR byggir á sjónlagsviðurkenningu er líklegt að OCR-þjónustan túlki stafi í PDF-eða myndskrám ranglega þegar það vinnur fyrst tiltekin skjöl lánardrottins, td. Það má ekki túlka merki fyrirtækisins sem nafn seljanda eða það kann að misinta heildarfjárhæð á kvittun vegna útlits þess. Til að forðast þessar villur fara fram, er hægt að leiðrétta villur í sérstakri útgáfu af síðunni **Skjal á innleið**. Þá er leiðréttingin send til baka til OCR Service til að þjálfa hana til að túlka tiltekna stafi og reiti rétt næst þegar hann vinnur úr PDF-eða myndskjali fyrir sama lánardrottinn. Nánari upplýsingar má finna [í lest OCR Service til að komast hjá villum](across-how-use-ocr-pdf-images-files.md#to-train-the-ocr-service-to-avoid-errors).

Umferð skráa til og frá OCR-þjónustunni er unnin með sérhæfðu vinnsluraðarinnfærslu. Þessi vinnslubiðröð er stofnuð sjálfkrafa þegar þú virkjar ytri OCR-þjónustutenginguna. Frekari upplýsingar eru í [Setja upp skjöl á innleið](across-how-setup-income-documents.md).

> [!NOTE]
> OCR-aðgerðin er veitt af utanaðkomandi veitum. Veljið uppfærslupakka sem er viðeigandi fyrir fyrirtækið og/eða landið/svæðið. Finna þjónustur sem [!INCLUDE[prod_short](includes/prod_short.md)] eru samhæfðar og upplýsingar um tiltæka eiginleika í [AppSource . microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).

## <a name="to-send-a-pdf-or-image-file-to-the-ocr-service-from-the-incoming-documents-page"></a>PDF eða myndskrá send til OCR-þjónustunnar af síðu utanaðkomandi skjala

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Skjöl á innleið** og velja síðan viðkomandi tengil.
2. Búið til nýja færslu fyrir skjal á innleið og hengið skrána við. Frekari upplýsingar eru í [Stofna færslur skjala á innleið](across-how-create-income-document-records.md).  
3. Á síðunni **Skjöl á innleið**, á veldu eina eða fleiri línur og veldu svo **Senda í verkröð** aðgerðina.

   Gildið í reitnum  **OCR-staða** breytist í **Tilbúið**. Meðfylgjandi PDF eða myndskrá er send til OCR-þjónustunnar með starfbiðröð samkvæmt áætlun ef engar villur eru til staðar.
4. Á **síðunni utanaðkomandi skjöl** er einnig hægt að velja eina eða fleiri línur og velja **svo aðgerðina senda til OCR Service** til að senda þegar í stað skrár til vinnslu.

   Gildið í **svæðinu OCR Status** breytist í **sent**, ef engar villur eru til staðar.

## <a name="to-send-a-pdf-or-image-file-to-the-ocr-service-by-email"></a>Til að senda PDF eða myndaskrá til OCR þjónustu með tölvupósti

Í tölvupósti umsókn þinni getur þú framvísað tölvupósti til OCR þjónustuveitanda með PDF eða myndskrá meðfylgjandi. Upplýsingar um netfangið sem senda á til er að finna á heimasíðu OCR-þjónustunnar.

Þar sem engin móttekin skjalaskráning er til fyrir skrána verður ný færsla stofnuð sjálfkrafa á **síðunni utanaðkomandi skjöl** þegar OCR sendir rafræna skjalið sem leiðir út. Frekari upplýsingar eru í [Stofna færslur skjala á innleið](across-how-create-income-document-records.md).

> [!NOTE]  
> Ef þú vinnur á töflu eða síma, getur þú sent skrána í OCR þjónustu eins fljótt og þú hefur tekið mynd af skjalinu, eða þú getur búið til skjal á innleið beint. Sjá [Create it Document Record til að fá frekari upplýsingar með því að taka mynd](across-how-create-income-document-records.md#to-create-an-incoming-document-record-by-taking-a-photo).

## <a name="to-receive-the-resulting-electronic-document-from-the-ocr-service"></a>Að fá meðfylgjandi rafrænt skjal frá OCR Service

Rafrænt skjal sem er stofnaði af OCR-þjónustu úr PDF eða myndaskrá er sjálfkrafa mótteknar á síðunni **skjöl á innleið** af verkraðarfærslu sem er sett upp þegar þú virkjar OCR þjónustan.

Ef vinnslubiðröð er ekki notuð eða á að taka við loknu OCR-skjali fyrr en fyrir hverja raðaröðun er hægt að velja **aðgerðina Móttaka úr OCR-þjónustu**. Þessi valkostur mun fá einhver skjöl sem lokið er við þjónustu OCR.

> [!NOTE]  
> Ef OCR þjónustan er stillt þannig að krafist er handvirka sannprófun fyrir unnin skjöl, þá mun reiturinn **OCR Staða** inihalda **Bíður sannprófunar**. Ef svo er skal framkvæma eftirfarandi skref til að skrá sig inn á vefsvæði OCR til að sannreyna OCR-skjal handvirkt.

1. Í á reitnum **OCR Stöðu** er valið **Bíður sannprófunar** tengilinn.
2. Á þjónustuvef OCR, Skráðu þig inn með því að nota skilríki á OCR Service reikningnum þínum. Frekari upplýsingar er að finna [í setja upp OCR-þjónustu](across-how-setup-income-documents.md#to-set-up-an-ocr-service).

   Upplýsingar um skjalið OCR birtist, þar sem sýndar eru bæði upprunalegt efni PDF skjalsins eða myndskrárinnar og afleidd OCR-gildi reita.
3. Skoða gildi svæðisins og breyta handvirkt eða færa inn gildi í reitum sem OCR þjónustan hefur merkt sem óvissu.
4. Velja hnappinn **Í lagi**. OCR-ferlinu er lokið og er meðfylgjandi rafrænu skjali sent **á síðu utanaðkomandi skjala** í [!INCLUDE[prod_short](includes/prod_short.md)], samkvæmt verkáætlun.
5. Endurtakið skref 2 til 4 fyrir önnur OCR-skjal sem á að sannprófa.

Nú er hægt að byrja að stofna færslur skjala fyrir móttekin rafrænar fylgiskjöl í [!INCLUDE[prod_short](includes/prod_short.md)], handvirkt eða sjálfvirkt. Nánari upplýsingar er að finna í næsta ferli. Einnig [er hægt að tengja nýju komandi skjalaskráninguna við fyrirliggjandi bókuð eða óbókuð skjöl](across-how-connect-disconnect-income-document-records.md) svo að auðvelt sé að nálgast [!INCLUDE[prod_short](includes/prod_short.md)] upprunaskrána.

## <a name="to-create-a-purchase-invoice-from-an-electronic-document-received-from-the-ocr-service"></a>Stofna innkaupareikning út frá rafræna skjalinu mótteknu úr OCR

Eftirfarandi ferli sýnir hvernig á að stofna færslu innkaupareiknings úr reikningur lánardrottins sem var móttekin sem rafrænt skjal úr OCR-þjónustu. Ferlið er það sama þegar búið er til, til dæmis, færslubókarlína úr kostnaðarkvittun eða söluvöruskilapöntun frá viðskiptamanni.

> [!NOTE]  
> **Lýsingin** og **nr.** á stofnuðum skjalalínum verða aðeins fylltir út ef þú hefur fyrst varpað texta á OCR-skjali á reitunum tveimur í [!INCLUDE[prod_short](includes/prod_short.md)]. Hægt er að gera þessa vörpun sem tilvísun vöru, fyrir skjalalínur af gerðinni vara. Frekari upplýsingar er að finna í [Nota vörutilvísanir](inventory-how-use-item-cross-refs.md). Einnig er hægt að nota texta-og **Lyklavörpunaraðgerðina**. Frekari upplýsingar er að finna [í varpa texta á skjal á innleið til ákveðins lánardrottins, fjárhags eða bankareiknings](across-how-use-ocr-pdf-images-files.md#to-map-text-on-an-incoming-document-to-a-specific-vendor-account).

1. Velja skal línu fyrir skjal á innleið og svo **Stofna skjal** virknina.

Innkaupareikningur verður stofnaður í [!INCLUDE[prod_short](includes/prod_short.md)] og byggist á upplýsingum í rafrænu skjali lánardrottins sem tekið var á móti frá OCR-þjónustu. Upplýsingar verða settar inn í nýja innkaupareikninginn samkvæmt vörpun sem þú hefur skilgreint sem tilvísun eða sem textavörpun.

Villuvillur, sem eru yfirleitt rangar eða vantar gögn í [!INCLUDE[prod_short](includes/prod_short.md)], verða sýndar á **flipanum villur og flýtiviðvaranir**. Frekari upplýsingar er að finna [í handflutningsvillum við móttöku rafrænna skjala](across-how-use-ocr-pdf-images-files.md#to-handle-errors-when-receiving-electronic-documents).

### <a name="to-map-text-on-an-incoming-document-to-a-specific-vendor-account"></a>Til að varpa texta á tiltekinn lánardrottinn, fjárhag eða bankareikning

Fyrir skjal á innleið er yfirleitt notuð **varpa texta á reikning** aðgerð til að skilgreina að tilteknum texta á reikning lánardrottins sem var móttekinn frá OCR-þjónustu er varpað á tilteknum lánardrottnareikning. Fara fram, hvaða hluti viðkominnar skjals sem er til sem kortlagningartexti þýðir að **reiturinn lánardrottinn** þar sem á leiðir til skjala-eða færslubókarlína af gerðinni *fjárhagsreikningur* er fylltur út með lánardrottninum sem um ræðir.

Auk þess að varpa á lykil lánardrottins-eða fjárhagsreikninga er einnig hægt að varpa texta á bankareikning. Þessi valkostur er til dæmis gagnlegur fyrir rafræn skjöl fyrir útgjöld sem þegar eru greidd og þar sem stofna á færslubókarlínu sem er tilbúin til bókunar á bankareikning.

1. Viðkomandi lína skjals á innleið er valin og svo aðgerðin **Varpa Texta á reikning**. Síðan **vörpun texta á reikning** opnast.
2. Í reitinn **Vörpun texta** skal slá inn þann texta sem kemur fram á reikningum lánardrottins sem á að búa til innkaupaskjöl eða færslubókarlínur fyrir. Hægt er að færa inn allt að 50 stafi.
3. Í **Númer lánardrottins** reitinn skal færa inn númer lánardrottins sem innkaupaskjal eða færslubókarlína verður stofnað fyrir.
4. Í reitinn **Debetreikningsnúmer** skal færa inn fjárhagsreikning af debetgerð sem verður settur inn á viðkomandi innkaupaskjal eða færslubókarlínu af gerðinni fjárhagsreikningur.
5. Í reitinn **Kreditreikningsnúmer** skal færa inn fjárhagsreikning af kreditgerð sem verður settur inn á viðkomandi innkaupaskjal eða færslubókarlínu af gerðinni fjárhagsreikningur.

   > [!NOTE]
   > Ekki skal nota **Upprunagerð stöðu** og **Upprunanúmer stöðu** reitina í tengslum við skjöl á innleið. Þeir eru aðeins notaðir fyrir afstemmingu sjálfvirkra greiðslna. Frekari upplýsingar er að finna í [Varpa texta um endurteknar greiðslur í reikninga fyrir sjálfvirka afstemmingu](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).
6. Endurtakið skref 2 til 5 fyrir allan texta í skjölum á innleið sem á búa sjálfkrafa til skjöl fyrir.

## <a name="to-handle-errors-when-receiving-electronic-documents"></a>Hvernig á að: Meðhöndla villur við móttöku rafrænna skjala

1. **Á síðunni utanaðkomandi skjöl** er valin lína fyrir rafrænt skjal sem móttekið er frá OCR þjónustunni með villum, sem tilgreindar *eru í villugildinu* í **OCR-stöðunni**.
2. Veldu **breyta** aðgerðina til að opna síðuna **skjal á innleið** .
3. Í Flýtiflipanum **Villur og Viðvaranir** skal velja skilaboðin og síðan valið á **Opna Tengdar Skrá** aðgerð.
4. Síðan sem inniheldur gölluð eða týnd gögn, t.d. viðskiptamannaspjald þar sem gildir vantar, opnast.
5. Leiðréttið villuna eða villurnar sem lýst er í hverju villuboðum.
6. Haldið áfram að vinna úr skjölum á innleið með því að velja aftur aðgerðina **Stofna handvirkt**.
7. Skref 5 til 6 eru endurtekin fyrir allar villur sem eftir eru þar til hægt er að taka á móti rafrænu skjali.

## <a name="to-train-the-ocr-service-to-avoid-errors"></a>Þjálfa OCR-þjónustu til að forðast villur

Þar sem OCR byggir á Optical-viðurkenningu getur OCR-þjónustan ranglega túlkað stafi í PDF-eða myndskrám þegar það vinnur fyrst úr skjölum frá tilteknum lánardrottni, til dæmis. Það má ekki túlka logo fyrirtækisins sem nafn lánardrottins eða það getur misinterað heildarupphæð á útgjaldakvittun vegna útlits þess. Til að komast hjá því að slíkar villur berist áfram er hægt að leiðrétta gögn úr OCR-þjónustu og senda athugasemdirnar aftur til þjónustuaðilans.

Síðan **OCR-gagnalreiðrétting**, sem er opnuð af síðunni **skjal á innleið**, birtir reiti úr flýtiflipanum **Fjárhagsupplýsingar** í tveimur dálkum, einum þar sem hægt er að breyta OCR-gögnum og öðrum þar sem OCR-gögnin eru skrifvarin. Þegar hnappurinn **Senda OCR-athugasemdir** er valinn er innihald síðunnar **OCR-gagnaleiðrétting** sent OCR-þjónustunni. Næst þegar þjónustuferlarnir PDF eða myndskrár sem um ræðir eru endurinnfelldir verða leiðréttingar til að bæta skjalaskráningu.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Skjöl á innleið** og velja síðan viðkomandi tengil.
2. Opna komandi skjalaskrá sem inniheldur gögn sem berast frá OCR-þjónustunni sem á að leiðrétta.
3. Á síðunni **Skjal á innleið** skal velja aðgerðina **leiðrétta OCR-gögn**.
4. Á síðunni **OCR-gagnalreiðrétting** skal yfirskrifa gögnin í dálkinum sem hægt er að breyta fyrir hvern reit með rangt gildi.
5. Til að afturkalla leiðréttingar sem hafa verið gerðar síðan **OCR-gagnaleiðrétting** var opnuð skal velja aðgerðina **Endurstilla OCR-gögn**.
6. Til að senda leiðréttingar til OCR-þjónustu, veldu senda **OCR-leiðréttingarathugasemdir** aðgerðina.
7. Til að vista leiðréttingarnar skal loka síðunni **OCR-gagnalreiðrétting**.

Reitirnir í flýtiflipanum **Fjárhagsupplýsingar** á síðunni **Skjal á innleið** eru uppfærðir með öllum nýjum gildum sem færð voru ínn í skrefi 4.

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/incoming-documents-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig .

[Stofna komandi skjalaskrár](across-how-create-income-document-records.md)
[Stofna skjalafærslur beint úr skjölum og](across-how-connect-disconnect-income-document-records.md)
[innsendum skjölum](across-income-documents.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
