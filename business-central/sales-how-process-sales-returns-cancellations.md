---
title: Meðhöndlun söluvöruskila eða afturkallana | Microsoft Docs
description: Lýsir því hvernig skal stofna kreditreikning, beint eða í gegnum söluvöruskilapöntun, til að vinna skil, afturköllun eða endurgreiðslu fyrir vöru eða þjónustu sem þú hefur fengið greiðslu fyrir.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 01/13/2020
ms.author: sgroespe
ms.openlocfilehash: 3d7c1fa772263aa863b6398e86f35be47998f455
ms.sourcegitcommit: ead69ebe5b29927876a4fb23afb6c066f8854591
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/14/2020
ms.locfileid: "2954004"
---
# <a name="process-sales-returns-or-cancellations"></a>Vinna söluskil eða afturkallanir
Ef viðskiptavinur vill skila eða endurgreiða fyrir vörur eða þjónustu sem þú hefur selt og fengið greiðslu fyrir verður þú að búa til og senda inn söluskuldbindingar sem tilgreinir umbeðnar breytingar. Til að taka réttar sölureikningsupplýsingar með, er hægt að stofna sölukreditreikning beint úr bókaða sölureikningnum eða þú getur stofnað nýja sölukreditreikning með afrituðum reikningsupplýsingum.

Ef þú þarft meiri stjórn á söluskilaferlinu, eins og t.d. vöruhúsaskjöl fyrir vöruafgreiðsluna eða betra yfirlit yfir móttöku vara frá mörgum söluskjölum með einum vöruskilum, geturðu stofnað söluvöruskilapöntun. Söluvöruskilapöntun gefur út sjálfkrafa tengdan sölukreditreikning og önnur skilatengd skjöl, eins og skiptivörusölupöntun, ef þarf. Frekari upplýsingar er að finna í [Að stofna vöruskilapöntun byggða á einu eða fleiri bókuðu söluskjali](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-return-order-based-on-one-or-more-posted-sales-documents).

> [!NOTE]  
>   Ef sölureikningur hefur ekki verið greiddur þá geturðu notað **Rétt** eða **Hætta við** aðgerðirnar á bókaða sölureikningnum til að snúa við viðskiptum. Þessar aðgerðir virka aðeins fyrir ógreiddar reikningar og styðja ekki hluta skilar eða afpöntunar. Frekari upplýsingar eru í [Ógreiddir sölureikningar leiðréttir eða afturkallaðir](sales-how-correct-cancel-sales-invoice.md).

Skil eða endurgreiðsla getur átt við um aðeins hluta af vörum eða þjónustum á upprunalega sölureikningnum. Í því tilviki þarf að breyta upplýsingum í línunum á sölukreditreikningnum eða söluvöruskilapöntun. Við bókun sölukreditreiknings eða söluvöruskilapöntun eru þau söluskjöl sem eru breytingin hefur áhrif á bakfærð og hægt er að stofna endurgreiðslu til viðskiptamannsins. Frekari upplýsingar eru í [Greiðslur framkvæmdar](payables-make-payments.md).  

Auk upprunalega bókaðs sölureiknings, er hægt að jafna sölukreditreikning eða söluvöruskilapöntun við öðrum söluskjölum, t.d. aðra bókað sölureikninga, þar sem viðskiptamaðurinn er einnig að skila vörum sem voru afhentar með viðkomandi reikningi.

Hægt er að senda bókaða sölukreditreikninga til viðskiptamannsins til að staðfesta vöruskil eða afturköllun og miðla því að virðið verði endurgreitt, til dæmis þegar vörum er skilað.

Bókun innkaupareiknings mun einnig snúa við öllum kostnaðarauka sem var úthlutað á bókaða skjalið, þannig að vöruvirðisfærslurnar eru þær sömu og áður en kostnaðaraukanum var úthlutað.

## <a name="inventory-costing"></a>Birgðakostnaður
Til að varðveita rétt birgðaverðmat, eru vanalega setja skilavörur aftur inn í birgðum á því kostnaðarverði sem þær voru seldar á, en ekki núgildandi kostnaðarverði. Þetta er kallað nákvæm bakfærsla kostnaðar.

Til er tvenns konar virkni, til að úthluta bakfærslu nákvæms kostnaðar sjálfvirkt:   

|Virkni|Description|  
|------------------|---------------------------------------|  
|**Sækja bókaðar fylgiskjalalínur til að bakfæra** aðgerð á síðunni **Söluvöruskilapöntun**|Afritar línur úr einu eða fleiri bókuðum fylgiskjölum sem á að bakfæra til söluvöruskilapöntun. Frekari upplýsingar er að finna í [Að stofna vöruskilapöntun byggða á einu eða fleiri bókuðu söluskjali](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-return-order-based-on-one-or-more-posted-sales-documents).|  
|**Afrita skjal** aðgerð í **Sölukreditreikningur** og á síðunni **Söluvöruskilapöntun**|Afritar bæði haus og línur af einu bókuðu fylgiskjali sem á að bakfæra.<br /><br /> Krefst þess að **Nákvæm bakfærsla kostnaðar** gátreitur sé valinn á síðunni **Uppsetning fyrir Sölu & Viðskiptaskuldir**.|

Til að úthluta nákvæmri bakfærslu kostnaðar, skal velja reitinn **Jafna frá birgðafærslu** á einhverja gerð skilaskjalslínu, og velja síðan númer upphaflega sölufærslunnar. Það tengir sölukreditreikninginn eða söluvöruskilapöntunina við upphaflega sölufærslu og tryggir að varan er metin út frá upphaflegu einingarverði.

Nánari upplýsingar, sjá [Upplýsingar um hönnun: Birgðakostnaður](design-details-inventory-costing.md)

## <a name="to-create-a-sales-credit-memo-from-a-posted-sales-invoice"></a>Að stofna nýjan sölukreditreikning úr bókuðum sölureikningi.
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Bókaðir sölureikningar** og veldu síðan tengda tengilinn.  
2. Á síðunni **Bókaðir sölureikningar** skal velja þá bókuðu sölureikninga sem á að bakfæra og veljið síðan aðgerðina **Stofna leiðréttan kreditreikning**.

    Minnispunktur fyrir sölureikninginn inniheldur nokkrar upplýsingar frá staða sölureikningsins. Hægt er að breyta þessu, til dæmis með nýjar upplýsingar sem endurspegla endursenda samkomulagið.  
3. Breyttu upplýsingum um línurnar í samræmi við samninginn, svo sem fjölda skilaðra hluta eða fjárhæðin sem endurgreiða.
4. Valið er **Jafna Færslur** aðgerð.
5. Á síðunni **Jafna viðskm.færslur** skal velja línuna með bókaða söluskjalinu sem á að jafna sölukreditreikninginn við og veljið síðan aðgerðina **Kenni jöfnunar**.

    Kennimerki söluskuldbindinga birtist á **kenni jöfnunar**.
6. Sláðu inn **Upphæð til að jafna** sem þú vilt sækja um í upphæðin sem á að sækja um ef hún er minni en upphafleg upphæð.  

    Neðst á síðunni **Jafna viðskm.færslur** er hægt að skoða heildarupphæðina sem á að nota til að bakfæra allar færslur, nefnilega þegar gildið í reitnum **Staða** er núll.
7. Velja hnappinn **Í lagi**. Þegar þú sendir inn sölutilboðið, þá er það sótt á staða söluskráanna.

    Eftir að þú hefur stofnað línur fyrir sölukreditreikningana eða breytt þeim og ein eða fleiri jöfnun tilgreind, er hægt að bóka sölukreditreikninginn.   
8. Veljið aðgerðina **Bóka og senda**.  

Í **Bóka og Senda staðfestingu** svargluggi opnast og sýnir notuð valda sendingaraðferð fyrir viðskiptamanninn. Hægt er að breyta sendingaraðferð með því að velja uppflettihnappinn í reitnum **Senda skjal** til. Frekari upplýsingar er að finna á [Setja upp sendisnið skjala](sales-how-setup-document-send-profiles.md).  

Bókuðu söluskjölin sem jafnað var við kreditreikninginn eru nú bakfærðir og endurgreiðslu má nú búa til fyrir viðskiptamanninn. Sölukreditreikningurinn er fjarlægður og skipt út fyrir nýtt fylgiskjal á lista bókaðra sölukreditreikninga.

## <a name="to-create-a-sales-credit-memo-by-copying-a-posted-sales-invoice"></a>Að stofna sölukreditreikning með því að afrita bókuðum sölureikningi
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölukreditreikningar** og veldu síðan tengda tengilinn.
2. Veljið aðgerðina **Nýtt** til að opna nýjan auðan sölukreditreikning.
3. Í reitnum **Viðskiptamaður** er fært inn nafn núverandi viðskiptamanns.
4. Valið er **Afrita fylgiskjal** aðgerð.
5. Á síðunni **Afrita söluskjal** í reitnum **Gerð skjals** skal velja **Bókaður reikningur**.
6. Velja reitinn **Númer fylgiskjals** til að opna síðuna **Bókaðar sölureikningar** og síðan velja bókaða sölureikninginn sem inniheldur línur sem á að bakfæra.
7. Veljið gátreitinn **Endurreikna línur**, ef bókaða sölureikningslínan sem var afrituð á að uppfærast með breytingum á vöruverði og kostnaðarverði síðan reikningurinn var bókaður.
8. Velja hnappinn **Í lagi**. Afrituðu reikningslínurnar eru settar inn í sölukreditreikninginn.
9. Sölukreditreikningnum er lokið eins og útskýrt er í [Að stofna sölukreditreikning úr bókuðum sölureikningi](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-credit-memo-from-a-posted-sales-invoice).

## <a name="to-create-a-sales-return-order-based-on-one-or-more-posted-sales-documents"></a>Til að stofna skilapöntun sölu byggða á einu eða fleiri bókuðu söluskjali
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Söluvöruskilapantanir** og veldu síðan tengda tengilinn.
2. Valið er **Nýtt** aðgerð.  
3. Fyllt er út í reitina á flýtiflipanum **Almennt** eftir þörfum.
4. Á flýtiflipanum **Línur** skal fylla þessar línur út handvirkt, eða afrita upplýsingar úr öðrum fylgiskjölum til að fylla út línurnar sjálfvirkt:

    - Hægt er að nota aðgerðina **Sækja bókaðar fylgiskjalalínur til að bakfæra** til að afrita eina eða fleiri bókaðar fylgiskjalalínur frá einu eða fleiri bókuðum fylgiskjölum. Þessi aðgerð bakfærir alltaf nákvæmlega kostnaðinn úr bókuðu fylgiskjalslínunni. Þessu aðgerð er lýst í eftirfarandi skrefum.    
    - Nota aðgerðina **Afrita skjal** til að afrita fyrirliggjandi fylgiskjal í vöruskilapöntun. Þessi aðgerð er notuð til að afrita allt fylgiskjalið. Það er annað hvort bókað fylgiskjal eða fylgiskjal sem hefur ekki enn verið bókað. Þessi aðgerð gerir aðeins kleift að bakfæra kostnað á nákvæman hátt þegar **Nákvæm bakfærsla kostnaða áskilin** gátreiturinn er valinn á síðunni **Uppsetning fyrir Sölu & Útistandandi**.  

5. Velja aðgerðina **Sækja bókaðar fylgiskjalalínur til að bakfæra**.
6. Efst á síðunni **Bókaðar línur söluskjals** er valið gátmerki **Sýna eingöngu bakfæranlegar línur** ef eingöngu á að birta línur sem eru með magn sem enn hefur ekki verið skilað. Til dæmis ef bókað magn sölureiknings hefur verið skilað kann ekki að vera æskilegt að skila magninu í nýtt fylgiskjal söluvöruskila.

    > [!NOTE]  
    >  Þessi reitur virkar eingöngu fyrir bókaðar afhendingar eða móttökur og bókaðar reikningslínur, ekki fyrir bókuð vöruskil eða bókaðar kreditreikningslínur.

    Vinstra megin á síðunni er ólík tegund fylgiskjals og númerið í sviga sýnir númer skjalsins af tiltekinni tegund sem er til taks.

7. Í reitnum **Afmörkun fylgiskjalsgerðar** skal velja tegund bókaðra lína fylgiskjals sem nota skal.  
8. Velja skal línurnar sem á að afrita í nýja fylgiskjalið.  

    > [!NOTE]  
    >  Ef Ctrl+A er notað til að velja allar línur eru allar línur afritaðar innan afmörkunarinnar sem er virk en hundsar afmörkunina **Sýna eingöngu bakfært magn**. Til dæmis er búið að afmarka línurnar við tiltekið fylgiskjalsnúmer með tveimur línu, og búið er að skila annarri. Jafnvel þótt gátreiturinn **Sýna eingöngu bakfært magn** sé valinn afritar forritið eingöngu tvær línur þegar ýtt er á Ctrl+A til að afrita báðar línur, í stað þess að afrita eingöngu þá línu sem ekki hefur verið bakfærð.  

9. Veldu hnappinn **Í lagi** ef afrita á línurnar í nýja skjalið.  

    Eftirfarandi ferli fara fram:  

    -   Fyrir bókaðar fylgiskjalslínur af tegundinni **Vara** er ný fylgiskjalslína stofnuð sem er afrit af bókuðu fylgiskjalslínunni með magni sem ekki hefur verið bakfært. Fyllt er inn í **jafna við birgðafærslu** svæðið, fyrir innkaupaskjöl, eins og við á, með færslunúmeri birgðahöfuðbókar bókaðrar skjalslínu.  

    -   Fyrir bókaðar fylgiskjalslínur sem eru ekki af tegundinni **Vara** t.d. kostnaðarauki er ný fylgiskjalslína stofnuð sem er afrit af upphaflegu bókuðu fylgiskjalslínunni.  

    -   Reiknar reitinn **Kostn.verð (SGM)** í nýju línunni úr kostnaði í samsvarandi birgðafærslu.  

    -   Ef afritaða fylgiskjalið er bókuð afhending, bókuð móttaka, bókuð vöruskilamóttaka eða bókuð vöruskilaafhending er kostnaðarverðið úr birgðaspjaldinu reiknað sjálfkrafa.  

    -   Ef bókaða fylgiskjalið er bókaður reikningur eða kreditreikningur er kostnaðarverðið, reikningsafsláttur og línuafsláttur afritað úr bókuðu fylgiskjalslínunni.  

    -   Ef bókaða fylgiskjalslínan inniheldur vörurakningarlínu er reiturinn **Jafna við birgðafærslu** í vörurakningarlínunni fylltur með viðeigandi birgðafærslunúmerum úr bókuðu vörurakningarlínunum.  

     Þegar bókaður reikningur eða bókaður kreditreikningur er afritaður afritar forritið viðeigandi reikningsafslætti og línuafslætti sem gilda við bókun fylgiskjalsins úr bókuðu fylgiskjalslínunni í nýju fylgiskjalslínunni. Hins vegar þarf að hafa í huga að ef valkosturinn **Reikna reikn.afsl.** er ræstur í **Uppsetning Sala & Útistandandi** síðunni, er reikningsafslátturinn nýreiknaður þegar nýja fylgiskjalslínan er bókuð. Þess vegna getur verið að línuupphæðin fyrir nýju línuna sé önnur en línuupphæðin fyrir bókuðu fylgiskjalslínuna, allt eftir nýja útreikningnum á reikningsafslættinum.  

     > [!NOTE]  
     >  Ef hluti magns bókuðu fylgiskjalslínunnar hefur þegar verið bakfært eða selt eða notað, er eingöngu stofnuð lína fyrir magnið sem eftir er í birgðum eða sem ekki hefur verið skilað. Ef búið er að bakfæra allt magn í bókaðri fylgiskjalslínu er ný fylgiskjalslína ekki stofnuð.  
     >   
     >  Ef flæði vara í bókuðu fylgiskjali er það sama og flæði vara í nýja fylgiskjalinu er einfaldlega stofnað afrit af upphaflegu bókuðu fylgiskjalslínunni í nýja fylgiskjalinu. Ekki er fyllt út í reitinn **Jafna frá birgðafærslu** vegna þess að bakfærsla nákvæms kostnaðar er ekki möguleg í þessu tilviki. Ef aðgerðin **Sækja bókaðar fylgiskjalalínur til að bakfæra** er t.d. notuð til að sækja bókaða sölukreditreikninga fyrir nýjan sölukreditreikning er eingöngu upphaflega bókaða kreditreikningslínan afrituð í nýja kreditreikninginn.  

10. Á síðunni **Söluvöruskilapöntun** í reitnum **Ástæðukóði skila** á hverri línu, skal velja ástæðu skilanna.
11. Valið er **Bóka** aðgerðin.

## <a name="to-create-a-replacement-sales-order-from-a-sales-return-order"></a>Stofnuð sölupöntun fyrir skiptuvöru úr söluskilapöntun
Ef til vill á að bjóða viðskiptamanni bætur vegna vöru sem honum var seld með því að skipta á henni. Hægt er að bjóða sömu vöru í skiptum eða aðra vöru. Þessi staða getur komið upp ef til dæmis hefur verið send röng vara.  

1. Á síðunni **Söluvöruskilapöntun** fyrir virkt skilaferli, er í auðri línu búin til neikvæð færsla vegna skiptivörunnar með því að færa inn neikvætt magn í reitinn **Magn**.  
2. Velja aðgerðina **Flytja neikvæðar línur**.
3. Á síðunni **Flytja neikvæðar sölulínur** skal fylla út reitina eins og þörf krefur.
4. Velja hnappinn **Í lagi**. Neikvæðu línunni fyrir skilavörunni er eytt úr söluvöruskilapöntun og sett inn í nýja síðu af gerðinni **Sölupöntun**. Frekari upplýsingar eru í [Selja vörur](sales-how-sell-products.md).

## <a name="to-create-return-related-documents-from-a-sales-return-order"></a>Stofna skilatengd skjöl fyrir söluvöruskilapöntun
Hægt að stofna sölupantanir fyrir skiptivöru, vöruskilapantanir innkaupa og innkaupapantanir fyrir skiptivöru sjálfvirkt á meðan á ferli söluvöruskila stendur. Þessa aðgerð er hægt að nota til dæmis þegar vinna á með vöru í ábyrgð frá lánardrottnum.

1. Á síðunni **Söluvöruskilapöntun** skal velja **Stofna skilatengd skjöl** aðgerðina fyrir virkt skilaferli.
2. Í reitinn **Nr. lánardrottins** eru skráð númer lánardrottins ef þú vilt stofna lánardrottnaskjöl sjálfkrafa.
3. Ef skilavöru þarf að skila til lánardrottins, skal velja **Stofna innk.vörusk.pönt.** gátreitinn.
4. Ef panta þarf skilavöru frá lánardrottins, skal velja **Stofna innkaupapöntun** gátreitinn.
5. Ef sölupöntun fyrir skiptivöru þarf að stofna, velja **Stofna sölupöntun** gátreitinn.

## <a name="to-create-a-restock-charge"></a>Stofnað endurkaupagjald
Ef til vill er rétt að krefja viðskiptamann um endurkaupagjald til að standa straum af kostnaði við vöruskil. Þetta getur til dæmis verið hentugt ef viðskiptamaður hefur fyrir mistök pantað ranga vöru eða hætt við pöntun eftir móttöku vörunnar sem honum var seld.

Hægt er að bóka þessa hækkun kostnaðar sem kostnaðarauka á kreditreikningi eða vöruskilapöntun og úthluta því á bókaða afhendingu. Eftirfarandi lýsir því söluvöruskilapöntun, en sömu skref eiga við um sölukreditreikning.

1. Opna síðuna **Söluvöruskilapöntun** fyrir virkt skilaferli.
2. Á nýja línu í reitnum **Tegund** er valinn **Kostnaðarauki Vöru**.  
3. Fyllið inn í reitina eins og þeir séu kostnaðaraukalínur. Frekari upplýsingar er að finna í [Nota kostnaðarauka til að gera grein fyrir viðbótar viðskiptakostnaði](payables-how-assign-item-charges.md).  

Þegar söluskilapöntunin er bókuð er endurkaupagjaldi bætt við viðkomandi upphæð sölufærslu. Þannig er hægt að vinna með nákvæmt birgðaverðmat.  

## <a name="to-create-a-sales-allowance"></a>Til að bóka söluuppbót:
Hægt er að senda viðskiptamanni kreditreikning með verðlækkun hafi viðskiptamaðurinn fengið vörurnar lítillega skaddaðar eða of seint.  
Hægt er að bóka þetta lægra verð sem kostnaðarauka á kreditreikningi eða vöruskilapöntun og úthluta því á bókaða afhendingu. Eftirfarandi lýsir því fyrir sölukreditreikning, en sömu skref eiga við um söluvöruskilapöntun.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölukreditreikningar** og veldu síðan tengda tengilinn.
2. Veljið aðgerðina **Nýtt** til að opna nýjan auðan sölukreditreikning.
3. Kreditreikningshausinn er fylltur út með öllum viðeigandi upplýsingum um viðskiptamanninn sem á að veita söluuppbót.  
4. Á flýtiflipanum **Línur** í reitnum **Tegund** er valin **Gjald (vara)**.  
5.  Í reitnum **númer** er valið viðeigandi vörugjaldsnúmer.  
     Gott gæti verið að stofna sérstakt kostnaðaraukanúmer fyrir söluuppbætur.  
6.  Fært er inn **1** í reitinn **Magn**.  
7.  Í reitinn **Ein.verð** er upphæð söluuppbótarinnar færð inn.  
8.  Söluuppbótinni er  úthlutað sem vörugjaldi á vörurnar í bókuðu afhendingunni. Frekari upplýsingar er að finna í [Nota kostnaðarauka til að gera grein fyrir viðbótar viðskiptakostnaði](payables-how-assign-item-charges.md). Þegar uppbótinni hefur verið úthlutað er snúið aftur á síðuna **Sölukreditreikningur**.  

Þegar söluvöruskilapöntunin er bókuð er söluafslætti bætt við viðkomandi upphæð sölufærslu. Þannig er hægt að vinna með nákvæmt birgðaverðmat.

## <a name="to-combine-return-receipts"></a>Hvernig á að sameina vöruskilamóttökur
Hægt er að sameina vöruskilamóttökur ef viðskiptamaður er að skila mörgum vörum sem margar söluskilapantanir eiga við um.  

Þegar varan er móttekin í vöruhúsi er viðkomandi söluvöruskilapöntun bókuð sem móttekin. Þetta býr til bókaðar vöruskilamóttökur  

Þegar kemur að því að reikningsfæra viðskiptamanninn er hægt að stofna sölukreditreikning og afrita sjálfkrafa bókaðar innkaupaskilasendingarlínur í skjalið, í stað þess að reikningsfæra hverja söluskilapöntun sérstaklega. Þá má bóka sölukreditreikning og reikningsfæra allar opnar sölupantanir í einu.  

Til að sameina vöruskilamóttökur þarf að velja gátreitinn **Sameina afhendingar** á síðunni **Viðskiptamannaspjald**.  

### <a name="to-manually-combine-return-receipts"></a>Til að sameina vöruskilamóttökur handvirkt:  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölukreditreikningur** og veldu síðan tengda tengilinn.  
2. Valið er **Nýtt** aðgerð.
3. Fyllt er út í reiti eftir því sem er nauðsynlegt í flýtiflipanum **Almennt**.  
4. Velja aðgerðina **Sækja vöruskilamóttökulínur**.  
5. Valdar eru vöruskilamóttökulínurnar sem á að taka með í kreditreikninginn.  

    -   Til að setja allar línur inn eru allar línur valdar og svo smellt á **Í lagi** hnappinn.  

    -   Til að setja sérstakar línur inn eru línurnar valdar og svo smellt á **Í lagi** hnappinn.  

6.  Ef röng afhendingarlína var valin eða byrja á aftur er línunum einfaldlega eytt í kreditreikningnum aðgerðin **Sækja vöruskilamóttökulínur** keyrð aftur.  
7.  Bóka skal reikninginn.  

### <a name="to-automatically-combine-return-receipts"></a>Til að sameina vöruskilamóttökur sjálfvirkt  
Hægt er að sameina vöruskilamóttökur sjálfvirkt og hafa möguleikann á að bóka kreditreikninga sjálfvirkt með aðgerðinni **Sameina vöruskilamóttökur**.  

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sameina vöruskilamóttökur** og veldu síðan tengda tengilinn.
2. Á síðunni **sameina innkaupamóttökur** skal fylla inn í reitina til að velja viðeigandi vöruskilamóttökur.
3. Velja skal gátreitinn **Bóka kreditreikninga**. Ef ekki, verður að handvirkt bóka viðeigandi innkaupakreditreikninga.
4.  Velja hnappinn **Í lagi**.  

### <a name="to-remove-a-received-and-invoiced-return-order"></a>Mótteknar og reikningsfærðar vöruskilamóttökur fjarlægðar  
Þegar vöruskilamóttökur eru reikningsfærðar á þennan hátt eru vöruskilapantanir sem vöruskilamóttökurnar voru bókaðar úr enn til staðar, jafnvel þótt þær hafi verið mótteknar og reikningsfærðar að fullu.  

Þegar vöruskilamóttökur eru sameinaðar í kreditreikningi og svo bókaðar er bókaður sölukreditreikningur stofnaður fyrir kreditfærðu línurnar. Reiturinn **Reikningsfært magn** úr upphaflegu söluvöruskilamóttökunni er uppfærður samkvæmt reikningsfærðu magni.   
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eyða reikningsfærðum söluvöruskilapöntunum** og veldu síðan tengilinn.  
2.  Tilgreinið í **Nr.**. afmörkunarreitnum hvaða vöruskilapöntunum á að eyða.  
3.  Velja hnappinn **Í lagi**.  

Að öðrum kosti skal eyða einstökum söluvöruskilapöntunum handvirkt.   

## <a name="see-related-training-at-microsoft-learnlearnpathsreturn-items-dynamics-365-business-central"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/paths/return-items-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig
[Sala](sales-manage-sales.md)  
[Uppsetning sölu](sales-setup-sales.md)  
[Senda skjöl í tölvupósti](ui-how-send-documents-email.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
