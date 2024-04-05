---
title: Vinna söluvöruskilapantanir
description: 'Lýsir því hvernig skal stofna skilapöntun sölu til að vinna skil, afturköllun eða endurgreiðslu fyrir vöru eða þjónustu sem þú hefur fengið greiðslu fyrir.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'undo, credit memo, return, order'
ms.search.form: '44, 134, 144, 6629, 6630, 6633, 6662, 9302, 9304, Report_6646'
ms.date: 03/05/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Vinna söluvöruskilapantanir  

Ef þú þarft meiri stjórn á söluskilaferlinu, eins og t.d. vöruhúsaskjöl fyrir vöruafgreiðsluna eða betra yfirlit yfir móttöku vara frá mörgum söluskjölum með einum vöruskilum, geturðu stofnað söluvöruskilapöntun. Söluvöruskilapöntun gefur út sjálfkrafa tengdan sölukreditreikning og önnur skilatengd skjöl, eins og skiptivörusölupöntun, ef þarf.

Auk upprunalega bókaðs sölureiknings, er hægt að jafna sölukreditreikning eða söluvöruskilapöntun við öðrum söluskjölum, t.d. aðra bókað sölureikninga, þar sem viðskiptamaðurinn er einnig að skila vörum sem voru afhentar með viðkomandi reikningi.

## Stofna skilapöntun sölu byggða á einu eða fleiri bókuðu söluskjali  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Söluvöruskilapantanir** og velja síðan viðkomandi tengil.
2. Valið er **Nýtt** aðgerð.  
3. Fyllt er út í reitina á flýtiflipanum **Almennt** eftir þörfum.
4. Á flýtiflipanum **Línur** skal fylla þessar línur út handvirkt, eða afrita upplýsingar úr öðrum fylgiskjölum til að fylla út línurnar sjálfvirkt:

    - Hægt er að nota aðgerðina **Sækja bókaðar fylgiskjalalínur til að bakfæra** til að afrita eina eða fleiri bókaðar fylgiskjalalínur frá einu eða fleiri bókuðum fylgiskjölum. Þessi aðgerð bakfærir alltaf nákvæmlega kostnaðinn úr bókuðu fylgiskjalslínunni. Þessu aðgerð er lýst í eftirfarandi skrefum.    
    - Nota aðgerðina **Afrita úr skjali** til að afrita fyrirliggjandi fylgiskjal í vöruskilapöntun. Þessi aðgerð er notuð til að afrita allt fylgiskjalið. Það er annaðhvort bókað fylgiskjal eða fylgiskjal sem hefur ekki enn verið bókað. Þessi aðgerð býður aðeins upp á nákvæma bakfærslu kostnaðar þegar gátreiturinn **Bakfærsla nákvæms kostnaðar áskilinn** er valinn á síðunni **Sölugrunnur** .  

5. Veldu aðgerðina **Vinna úr**, veldu síðan aðgerðina **Sækja bókaðar fylgiskjalalínur til að bakfæra**.
6. Efst á síðunni **Bókaðar söluskjalalínur** skal velja gátreitinn **Sýna eingöngu** bakfæranlegar línur ef aðeins á að sjá línur sem hafa magn sem ekki er búið að skila. Ef bókað magn sölureiknings hefur til dæmis þegar verið skilað er ekki hægt að skila magninu í nýju fylgiskjali söluskila.

    > [!NOTE]  
    >  Þessi reitur virkar eingöngu fyrir bókaðar afhendingar eða móttökur og bókaðar reikningslínur, ekki fyrir bókuð vöruskil eða bókaðar kreditreikningslínur.

    Vinstra megin á síðunni er ólík tegund fylgiskjals og númerið í sviga sýnir númer skjalsins af tiltekinni tegund sem er til taks.

7. Í reitnum **Afmörkun fylgiskjalsgerðar** skal velja tegund bókaðra lína fylgiskjals sem nota skal.  
8. Velja skal línurnar sem á að afrita í nýja fylgiskjalið.  

    > [!NOTE]  
    >  Ef Ctrl A er notað <kbd>til að velja allar línur eru allar línur innan afmörkunarinnar sem settar hafa verið afritaðar en afmörkunin</kbd>+<kbd>Sýna eingöngu</kbd> bakfært magn hunsuð. **·**  Til dæmis er búið að afmarka línurnar við tiltekið fylgiskjalsnúmer með tveimur línu, og búið er að skila annarri. Jafnvel þótt reiturinn **Sýna eingöngu** bakfært magn sé valinn, ef Valið <kbd>er Ctrl</kbd>+<kbd>A</kbd> til að afrita allar línur, þá eru báðar línur afritaðar, í staðinn fyrir aðeins þá sem enn hafa ekki verið bakfærðar.  

9. Veldu hnappinn **Í lagi** ef afrita á línurnar í nýja skjalið.  

    Eftirfarandi ferli fara fram:  

    -   Fyrir bókaðar fylgiskjalslínur af tegundinni **Vara** er búin til ný fylgiskjalslína sem er afrit af bókuðu fylgiskjalslínunni með magninu sem ekki hefur verið bakfært. Fyllt er inn í **jafna við birgðafærslu** svæðið, fyrir innkaupaskjöl, eins og við á, með færslunúmeri birgðahöfuðbókar bókaðrar skjalslínu.  

    -   Fyrir bókaðar fylgiskjalslínur sem ekki eru af tegundinni **Vara**, t.d. kostnaðarauki, er búin til ný fylgiskjalslína sem er afrit af upphaflegu bókuðu fylgiskjalslínunni.  

    -   Reiknar reitinn **Kostn.verð (SGM)** í nýju línunni úr kostnaði í samsvarandi birgðafærslu.  

    -   Ef afritaða fylgiskjalið er bókuð afhending, bókuð móttaka, bókuð vöruskilamóttaka eða bókuð vöruskilaafhending er kostnaðarverðið úr birgðaspjaldinu reiknað sjálfkrafa.  

    -   Ef bókaða fylgiskjalið er bókaður reikningur eða kreditreikningur er kostnaðarverðið, reikningsafsláttur og línuafsláttur afritað úr bókuðu fylgiskjalslínunni.  

    -   Ef bókaða fylgiskjalslínan inniheldur vörurakningarlínu er reiturinn **Jafna við birgðafærslu** í vörurakningarlínunni fylltur með viðeigandi birgðafærslunúmerum úr bókuðu vörurakningarlínunum.  

     Þegar bókaður reikningur eða bókaður kreditreikningur er afritaður afritar forritið viðeigandi reikningsafslætti og línuafslætti sem gilda við bókun fylgiskjalsins úr bókuðu fylgiskjalslínunni í nýju fylgiskjalslínunni. Hins vegar þarf að hafa í huga að ef valkosturinn **Reikna reikn.afsl.** er ræstur í **Uppsetning Sala & Útistandandi** síðunni, er reikningsafslátturinn nýreiknaður þegar nýja fylgiskjalslínan er bókuð. Línuupphæðin fyrir nýju línuna getur því verið önnur en línuupphæðin fyrir bókuðu fylgiskjalslínuna, samkvæmt nýjum útreikningi á reikningsafslætti.  

     > [!NOTE]  
     >  Ef hluti magns bókuðu fylgiskjalslínunnar hefur þegar verið bakfært eða selt eða notað, er eingöngu stofnuð lína fyrir magnið sem eftir er í birgðum eða sem ekki hefur verið skilað. Ef búið er að bakfæra allt magn í bókaðri fylgiskjalslínu er ný fylgiskjalslína ekki stofnuð.  
     >   
     >  Ef flæði vara í bókuðu fylgiskjali er það sama og flæði vara í nýja fylgiskjalinu er einfaldlega stofnað afrit af upphaflegu bókuðu fylgiskjalslínunni í nýja fylgiskjalinu. Ekki er fyllt út í reitinn **Jafna frá birgðafærslu** vegna þess að bakfærsla nákvæms kostnaðar er ekki möguleg í þessu tilviki. Ef aðgerðin **Sækja bókaðar fylgiskjalalínur til að bakfæra** er t.d. notuð til að sækja bókaða sölukreditreikninga fyrir nýjan sölukreditreikning er eingöngu upphaflega bókaða kreditreikningslínan afrituð í nýja kreditreikninginn.  

10. Á síðunni **Söluvöruskilapöntun** í reitnum **Ástæðukóði skila** á hverri línu, skal velja ástæðu skilanna.
11. Valið er **Bóka** aðgerðin.

## Stofnuð sölupöntun fyrir skiptuvöru úr söluskilapöntun
Notandi gæti ákveðið að bæta viðskiptamanni bætur vegna vöru sem hann hefur selt með því að skipta á henni. Hægt er að bjóða sömu vöru í skiptum eða aðra vöru. Þessi staða getur komið upp ef til dæmis hefur verið send röng vara.  

1. Á síðunni **Söluvöruskilapöntun** fyrir virkt skilaferli, er í auðri línu búin til neikvæð færsla vegna skiptivörunnar með því að færa inn neikvætt magn í reitinn **Magn**.  
2. Velja aðgerðina **Flytja neikvæðar línur**.
3. Á síðunni **Flytja neikvæðar sölulínur** skal fylla út reitina eins og þörf krefur.
4. Velja hnappinn **Í lagi**. Neikvæðu línunni fyrir skilavörunni er eytt úr söluvöruskilapöntun og sett inn í nýja síðu af gerðinni **Sölupöntun**. Frekari upplýsingar eru í [Selja vörur](sales-how-sell-products.md).

## Stofna skilatengd skjöl fyrir söluvöruskilapöntun
Hægt að stofna sölupantanir fyrir skiptivöru, vöruskilapantanir innkaupa og innkaupapantanir fyrir skiptivöru sjálfvirkt á meðan á ferli söluvöruskila stendur. Þessa aðgerð er hægt að nota til dæmis þegar vinna á með vöru í ábyrgð frá lánardrottnum.

1. Á síðunni **Söluvöruskilapöntun** skal velja **Stofna skilatengd skjöl** aðgerðina fyrir virkt skilaferli.
2. Í reitinn **Nr. lánardrottins** eru skráð númer lánardrottins ef þú vilt stofna lánardrottnaskjöl sjálfkrafa.
3. Ef skilavöru þarf að skila til lánardrottins, skal velja **Stofna innk.vörusk.pönt.** gátreitinn.
4. Ef panta þarf skilavöru frá lánardrottins, skal velja **Stofna innkaupapöntun** gátreitinn.
5. Ef sölupöntun fyrir skiptivöru þarf að stofna, velja **Stofna sölupöntun** gátreitinn.

## Stofnað endurkaupagjald
Ef til vill á að innheimta endurkaupagjald viðskiptamanns til að standa straum af kostnaði við vöruskil. Þetta getur til dæmis verið hentugt ef viðskiptamaður hefur fyrir mistök pantað ranga vöru eða hætt við pöntun eftir móttöku vörunnar sem honum var seld.

Hægt er að bóka þessa hækkun kostnaðar sem kostnaðarauka á kreditreikningi eða vöruskilapöntun og úthluta því á bókaða afhendingu. Eftirfarandi lýsir því söluvöruskilapöntun, en sömu skref eiga við um sölukreditreikning.

1. Opna síðuna **Söluvöruskilapöntun** fyrir virkt skilaferli.
2. Á nýja línu í reitnum **Tegund** er valinn **Kostnaðarauki Vöru**.  
3. Fyllið inn í reitina eins og þeir séu kostnaðaraukalínur. Frekari upplýsingar er að finna í [Nota kostnaðarauka til að gera grein fyrir viðbótar viðskiptakostnaði](payables-how-assign-item-charges.md).  

Þegar söluskilapöntunin er bókuð er endurkaupagjaldi bætt við viðkomandi upphæð sölufærslu. Þannig er hægt að vinna með nákvæmt birgðaverðmat.  

## Sjá einnig .

[Sala](sales-manage-sales.md)  
[Uppsetning sölu](sales-setup-sales.md)  
[Stjórna skuldum](payables-manage-payables.md)  
[Senda skjöl í tölvupósti](ui-how-send-documents-email.md)  
[Meðhöndlun innkaupaskila eða afturkallana](purchasing-how-process-purchase-returns-cancellations.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
