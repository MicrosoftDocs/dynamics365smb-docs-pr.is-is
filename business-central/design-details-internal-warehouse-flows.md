---
title: "Hönnunarupplýsingar - Innra vöruhúsaflæði | Microsoft Docs"
description: "Flæði vara á milli hólfa innan fyrirtækis snýst um að tína íhluti og taka frá endanleg vara fyrir framleiðslu- eða samsetningupantanir og tilfallandi hreyfingar, svo sem áfyllingu hólfs, án tengslum við upprunaskjöl."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: a52997195a95ff43eb049025b7b8ab3038381039
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-internal-warehouse-flows"></a>Hönnunarupplýsingar: Innra vöruhúsaflæði
Flæði vara á milli hólfa innan fyrirtækis snýst um að tína íhluti og taka frá endanleg vara fyrir framleiðslu- eða samsetningupantanir og tilfallandi hreyfingar, svo sem áfyllingu hólfs, án tengslum við upprunaskjöl. Umfang og eðli tengdra aðgerða eru mismunandi á milli grunnvörugeymslu og ítarlegri vörugeymslu.  

 Sumir innri flæði skarast við á flæði á innleið eða útleið flæði. Sumt af þessaru skörun er sýnt sem skref 4 og 5 í grafísku skýringarmyndir fyrir ítarlegt flæði á innleið og útleið. Nánari upplýsingar er að finna í [Hönnunarupplýsingar: vöruhúsaflæði inn](design-details-outbound-warehouse-flow.md).  

## <a name="internal-flows-in-basic-warehousing"></a>Innri flæðir almenn Vörugeymslur  
 Í grunnvöruhúsagrunnstillingu er flæði af vörum á milli hólfa innan fyrirtækisins snýst um að tína íhluti og ganga frá endanleg vara fyrir framleiðslu eða samsetningarpöntun og sértækar hreyfingar, svo sem hólfaáfyllingar, án tengsla við upprunaskjal.  

### <a name="flows-to-and-from-production"></a>Flæði til og frá framleiðslu  
 Aðalsamþættingin milli framleiðslupantana og grunnaðgerða í vöruhúsi er táknuð með færninni til að taka til framleiðsluíhluti með glugganum **Birgðatínsla** eða glugganum **Birgðahreyfing**.  

> [!NOTE]  
>  Í glugganum **Birgðatínsla** íhlutanotkun er bókuð með tínslubókun. Með því að nota gluggann **Birgðahreyfing**, eru aðeins leiðréttingar hólfa skráð, engar færslur í eiga sér stað í birgðahöfupbók.  

 Auk meðhöndlunar íhluta, samþættingu er táknuð með getu til að setja framleiddar vörur burtu með **Birgðafrágangur** glugga.  

 Reitirnir **Hólfkóti til framleiðslu**, **Hólfkóti frá framleiðslu** og **Opna hólfakóta vinnslusalar** á birgðageymsluspjaldi eða spjaldi vélar/vinnustöðvar tilgreina sjálfgefið flæði til og frá framleiðslusvæðum.  

 Frekari upplýsingar um hvernig íhlutanotkun er hreinsuð úr hólfkóða Til framleiðslu eða hólfkóða opins vinnustaðar eru í “Framleiðsluíhlutir hreinsaðir í vöruhúsinu” í þessu efnisatriði.  

### <a name="flows-to-and-from-assembly"></a>Flæði til og frá samsetningu  
 Aðalsamþættingin milli samsetningarpantana og grunnaðgerða í vöruhúsi er táknuð með færninni til að færa samsetningaríhluti á samsetningarsvæðið.  

 Þótt ekki sé til nein tiltekin vöruhússaðgerð til að ganga frá samsetningarvörum má stilla hólfakóðann á samsetningarpöntuninni á sjálfgefið frágangshólf. Bókun samsetningarpöntunar virkar þá eins og bókun frágangs. Hægt er að stjórna flutningi samsetningaríhluta í vöruhúsið í **Innri hreyfing** glugganum eða  glugganum, án tengingar við samsetningarpöntunina.  

 Eftirfarandi samsetningarflæði er til.  

|Flæði|Lýsing|  
|----------|---------------------------------------|  
|Setja saman í birgðir|Íhluta er þörf á samsetningarpöntun röð þar sem framleiðsla er geymt í vöruhúsi.<br /><br /> Þetta vöruhúsaflæði er stýrt í **Birgðahreyfing** glugga. Ein tökulína tilgreinir hvaða á að taka íhlutina. Ein staðarlína tilgreinir hvar á að setja íhlutina.|  
|Setja saman í pöntun|Íhluta er þörf á samsetningarpöntun sem er tengdur við sölupöntun sem er send þegar selda varan er sett saman.|  

> [!NOTE]  
>  Ef vörur eru settar saman í pöntun setur birgðatínsla tengdu sölupöntunarinnar af stað birgðahreyfingu fyrir alla samsetningaríhlutina, ekki bara fyrir seldu vöruna eins og þegar birgðavörur eru afhentar.  

 Reitirnir **Í samsetningu hólfakóði**, **Úr samsetningu hólfakóði** og **Setja saman í pöntun hólfakóði** á birgðageymsluspjaldi tilgreina sjálfgefið flæði á og af samsetningarsvæðum.  

> [!NOTE]  
>  Reiturinn **Setja saman í pöntun hólfakóði** virkar eins og frá-samsetningu-hólf í samsetning-fyrir-pöntun sviðsmyndir.  

### <a name="ad-hoc-movements"></a>Ad-hoc Hreyfingar  
 Í grunnvöruhúsavinnslu er hreyfingu vara frá hólfi til hólfs án tengsla við upprunaskjöl stjórnað í **Innri hreyfing** glugga og skráð í **Birgðahreyfing** glugga.  

 Önnur leið til að færa vörur tímabundið á milli hólfa er að bóka jákvæðar færslur í **Nýr hólfakóði** reitnum í **Endurröðunarbók vöru** glugganum.  

## <a name="internal-flows-in-advanced-warehousing"></a>Innri flæði í ítarlegt Vörugeymslur  
 Í ítarlegum vöruhús stillingar, flæði af vörum á milli hólfa innan fyrirtækisins snýst um að tína íhluti og setja í burtu endanlegar vörur fyrir framleiðslu pantanir og tína íhluti fyrir samsetningarpantanir. Að auki koma fram innri flæði eins sértækar hreyfingar, svo sem hólfáfyllingar, án tengslum við upprunaskjöl.  

### <a name="flows-to-and-from-production"></a>Flæði til og frá framleiðslu  
 Aðalsamþætting framleiðslupantana og ítarlegra vöruhússaðgerða er táknuð með færninni til að velja íhluti samsetningar, bæði með glugganum **Vöruhús – Tína** og glugganum **Vinnublað tínslu** og möguleikanum á að ganga frá framleiðsluvörum með glugganum **Innanhússfrág. vöruhúss**.  

 Annar samþættingarpunktur í framleiðslu er fáanlegur í glugganum **Vöruhúsahreyfing** , ásamt Hreyfing Vinnublað glugganum, sem gerir þér kleift að staðsetja íhluti og taka framleidda vörur fyrir útgefnar framleiðslupantanir.  

 Reitirnir **Hólfkóti til framleiðslu**, **Hólfkóti frá framleiðslu** og **Opna hólfakóta vinnslusalar** á birgðageymsluspjaldi eða spjaldi vélar/vinnustöðvar tilgreina sjálfgefið flæði til og frá framleiðslusvæðum.  

 Frekari upplýsingar um hvernig íhlutanotkun er hreinsuð úr hólfkóða Til framleiðslu eða hólfkóða opins vinnustaðar eru í “Framleiðsluíhlutir hreinsaðir í vöruhúsinu” í þessu efnisatriði.  

### <a name="flows-to-and-from-assembly"></a>Flæði til og frá samsetningu  
 Aðalsamþætting samsetningarpantana og ítarlegra vöruhússaðgerða er táknuð með færninni til að velja íhluti samsetningar, bæði með glugganum **Vöruhús – Tína** og glugganum **Vinnublað tínslu**. Þessi virkni virkar líkt og þegar íhlutir eru teknir til fyrir framleiðslupöntun.  

 Þótt ekki sé til nein tiltekin vöruhússaðgerð til að ganga frá samsetningarvörum má stilla hólfakóðann á samsetningarpöntuninni á sjálfgefið frágangshólf. Bókun samsetningarpöntunar virkar þá eins og bókun frágangs. Hægt er að stjórna flutningi samsetningaríhluta í vöruhúsið í **Hreyfing Vinnublað** glugganum eða **Innanhúss frágangur vöruhúss** glugganum, án tengingar við samsetningarpöntunina.  

> [!NOTE]  
>  Ef vörur eru settar saman í pöntun setur vöruhúsaafhending tengdu sölupöntunarinnar af stað vöruhúsatínslu fyrir alla samsetningaríhlutina, ekki bara fyrir seldu vöruna eins og þegar birgðavörur eru afhentar.  

 Reitirnir **Hólfkóti samsetn. á innleið** og **Hólfkóti samsetningar á útleið** á birgðageymsluspjaldi tilgreina sjálfgefið flæði á og af samsetningarsvæðum.  

### <a name="ad-hoc-movements"></a>Ad-hoc Hreyfingar  
 Í háþróaður vörugeymsla, hreyfingu vara frá hólfi til hólfs án tengslum við upprunaskjöl er stjórnað í **Hreyfing Vinnublað** glugga og skráð í Vöruhúsahreyfingar glugga.  

## <a name="flushing-production-components-in-the-warehouse"></a>Framleiðsluíhlutir hreinsaðir í vöruhúsinu.  
 Ef þeir eru settir upp á birgðaspjaldinu eru íhlutir sem teknir eru til með vöruhúsatiltekt bókaðir og notaðir af framleiðslupöntuninni þegar vöruhúsatiltektin er skráð. Með því að nota **Tínsla + Fram** aðferð og **Tínsla + afturábak** birgðaskráningaaðferð er kveikir tínsluaðferð bókun samsvarandi notkunar þegar fyrsta virknin hefst eða þeirri síðustu lýkukr.  

 Íhuga eftirfarandi atburðarás byggt á [!INCLUDE[d365fin](includes/d365fin_md.md)] sýnigagnagrunni, staðsetning WHITE.  

 Framleiðslupöntun fyrir 15 stykk af vöru LS-100 er til staðar. Sumar af vörunum á íhlutalista verða að vera birgðaskráðar handvirkt í notkunarbók og aðrar vörur í  listanum verða að vera teknar til og birgðaskráðar sjálfvirkt með **Tína+Afturábak** birgðaskráningaraðferð.  

> [!NOTE]  
>  **Tína + framsending** virkar aðeins ef notkun annarrar framleiðsluleiðarlínu notar leiðartengilskóða. Að losa áætlaða framleiðslupöntun setur af stað hreinsun íhluta stillt á **Tína + Áframsenda** Hins vegar getur birgðaskráningin ekki farið fram fyrr en tiltekt íhlutanna er skráð, sem getur aðeins gerst þegar pöntunin er gefin út.  

 Eftirfarandi skref lýsa aðgerðum mismunandi notenda og tilheyrandi viðbrögð:  

1.  Yfirmaður vinnusalar losar framleiðslupöntunina. Vörur með birgðaskráningaaðferðina **Framvirk** og engan leiðartengilskóð er dregnar frá hólfkóta opins vinnslusalar.  
2.  Yfirmaður vinnusalar velur hnappinn **Stofna vöruhúsatiltekt** í framleiðslupöntuninni. Tínsluskjal vöruhúss er stofnuð tínsla fyrir vörur með birgðaskráningaaðferðunum **Handvirkt**, **Tína + afturábak** og **Tína + Framvirk**. Þessar vörur eru settar í hólfkóða framleiðslu á útleið.  
3.  Stjórnandi vöruhússins úthlutar tiltekt á starfsmann vöruhúss.  
4.  Starfsmaður vöruhússins tínir vörurnar úr viðkomandi hólfum og kemur þeim fyrir í hólfkóða framleiðslu á útleið eða í hólfið sem tiltekið er í tínslu vöruhúss, sem kann að vera hólf vinnustöðvar eða vélastöðvar.  
5.  Starfsmaður í vöruhúsi skráir tínsluna. Magnið er dregið frá tiltektarhólfunum go bætt við notkunarhólfið. Reiturinn **Tínt magn** á íhlutalistanum fyrri allar tíndar vörur er uppfærður.  

    > [!NOTE]  
    >  Aðeins er hægt að nota magn sem er tínt.  

6.  Starfsmaður á vél upplýsir framleiðslustjóra um það þegar endanlegar vörur eru fullunnar.  
7.  Yfirmaður vinnusalar notar notkunarbókina eða framleiðslubókina til a bóka notkun hluta vöru sem nota annað hvort **handvirka** flæðiaðferð eða **framsendingar** eða **taka til + framsenda** flæðiaðferð með leiðartengilkóðum.  
8.  Framleiðslustjórinn bókar framleiðslu framleiðslupöntunarinnar og breytir stöðunni í **fullunnin**. Magn íhlutavöru sem notar **Afturvirkt** birgðaskráningu er dregið frá hólfkóða opins vinnslusalar **Tína+Afturábak** birgðaskráning er dregin frá hólfkóða framleiðslu á innleið.  

 Eftirfarandi mynd sýnir þegar reiturinn **Hólfkóti** á efnisþáttalista er fylltur út út frá staðsetningu notanda eða uppsetningu vinnuvélar-/vinnustöðvarmiðstöðvar.  

 ![Yfirlit yfir hvenær/hvernig hólfakóðareitinn er fyllt inn](media/binflow.png "Yfirlit yfir hvenær/hvernig hólfakóðareitinn er fyllt inn")  

## <a name="see-also"></a>Sjá einnig  
 [Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)

