---
title: Stofna númeraraðir
description: Lærðu hvernig á að setja upp númeraröð sem úthlutar einstökum auðkenniskóðum til reikninga og skjala í Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'numbers, numbering'
ms.search.form: '456_Primary, 457_Primary, 458_Primary, 459, 460, 461, 21, 22, 26, 27, 31'
ms.date: 05/07/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="create-number-series"></a>Stofna númeraraðir

Fyrir hvert fyrirtæki sem þú setur upp þarftu að úthluta einstökum kennitölum við hluti eins og aðalbókarreikninga, viðskiptavinar- og seljanda, reikninga og önnur skjöl. Númeraröð skiptir ekki aðeins máli til auðkenningar. Vel hannað númerakerfi gerir fyrirtækið einnig auðveldara að greina og draga úr gagnainnslætti.

> [!Important]
> Sjálfgefið er að eyða er ekki heimil í númeraröð því nákvæm saga fjárhagslegra færslna verður að vera tiltæk til endurskoðunar samkvæmt lögum, og því verður að fylgja óskráð röð án númera sem hefur verið eytt.
>
> Ef leyfa á eyðublöð í ákveðnum númeraröðum skal hafa samráð við endurskoðanda eða aðalbókara til að tryggja að lagaskilyrði séu sett í viðkomandi landi/svæði. Frekari upplýsingar er að finna í hlutanum [Eyður í númeraröðum](#gaps-in-number-series).

> [!NOTE]  
> Við mælum með að þú notir sömu númeraraða kóða eins og þú sérð skráða á síðunni **nr. Raðarlisti** í CRONUS sýnifyrirtækinu. Codes eins og *P-INV +* gætu ekki skilað þér strax, en [!INCLUDE[prod_short](includes/prod_short.md)] hefur marga sjálfgefna stillingar sem eru háð þessum númeraröðakóðum.

Númerakerfi er stofnað með því að setja upp einn eða fleiri kóta fyrir hverja tegund aðalgagna eða skjala. Til dæmis má setja upp einn kóta fyrir númerun viðskiptamanna, annan kóta fyrir númerun sölureikninga og annan fyrir númerun skjala í almennri færslubók. Þegar kóti hefur verið settur upp verður að setja upp minnst eina númeraraðarlínu. Í númeraraðarlínunni eru upplýsingar líkt og fyrsta og síðasta talan í röðinni og upphafsdagsetningin. Hægt er að setja upp fleiri en eina númeraraðarlínu á hvern númeraraðarkóta með mismunandi upphafsdagsetningu fyrir hverja línu. Raðirnar verða notaðar hver á eftir annarri og hver röð hefst á tilgreindum upphafsdegi.

> [!NOTE]
> Hámarkslengd númers í númeraröð er 20 stafir. Við sumar aðstæður mun [!INCLUDE[prod_short](includes/prod_short.md)] bæta við númeri með kerfismynduðu auðkenni. Til dæmis þegar skjöl á borð við reikninga eru notuð til að nota færslur, svo sem greiðslur, myndar [!INCLUDE[prod_short](includes/prod_short.md)] auðkenni fyrir notaðar færslur. Auðkennið er samsett úr númeri númeraraðar og sex stafa auðkenni sem kerfið myndar, t.d. -12345. Ef búist er við því að unnið verði úr meira en 9999 skjölum í bankafærslubók eða gíróbók, eða inngreiðslubókum, skal setja upp númeraröð fyrir skjöl af þessu tagi sem á að hafa færri en 14 stafi.

Þú setur venjulega upp númeraröðina þína til að setja inn næsta röð í röð á nýjum kortum eða skjölum sem þú býrð til. Þú getur hins vegar einnig stillt númeraröð til að leyfa þér að slá inn nýja númerið handvirkt. Þetta er tilgreint með reitunum **Handfærð nr.** innhólfinu.

Hægt er að nota fleiri en einn númeraraðarkóta fyrir hverja tegund frumgagna með því að nota númeraraðatengsl, til dæmis til að nota mismunandi númeraraðir fyrir mismunandi vöruflokka.

## <a name="gaps-in-number-series"></a>Eyður í númeraröð

Ekki allar færslur sem stofnaðar eru í [!INCLUDE[prod_short](includes/prod_short.md)] eru fjárhagsfærslur sem þarf að nota í röð númeraraðar. Viðskiptamannaspjald, sölutilboð og vöruhúsaaðgerðir eru dæmi um færslur sem eru úthlutaðar númeri úr númeraröðum en eru ekki háðar fjárhagsendurskoðun og/eða er hægt að eyða þeim. Hægt er að velja reitinn **Leyfa eyður í nr.röð fyrir slíka númeraröð.** í reitnum **Nr. Síðunni Raðarlínur** . Einnig er hægt að breyta þessari stillingu eftir að búið er að stofna númeraröðina. Frekari upplýsingar eru í [Búa til nýja númeraröð](ui-create-number-series.md#to-create-a-new-number-series).

## <a name="behavior-of-the-no-field-on-documents-and-cards"></a>Hegðun nr. reitur á skjölum og kortum

Á sölu-, innkaupa-, millifærslu- og þjónustuskjölum og á öllum spjöldum er reiturinn **Nr.** hægt er að fylla út í reitinn sjálfkrafa úr fyrirframskilgreindum númeraröðum eða bæta honum við handvirkt. Undir ákveðnum kringumstæðum er **nr.** reiturinn ósýnilegur til að koma í veg fyrir að þú breytir honum.  

**númer** reitinn má fylla út á þrjá vegu:

1. Ef aðeins ein númeraröð fyrir tegund skjals eða spjalds er til staðar og reiturinn **Sjálfgefin nr.** er valinn og reiturinn **Handvirk nr.** er ekki valinn fyrir þá númeraröð, þá er fyllt út í reitinn sjálfkrafa fyllt með næsta númeri í röðinni. **númer** reiturinn verður ekki sýnilegur á spjaldinu eða skjalinu.  

    Jafnvel þótt þú skilgreinir sniðmát með ýmsum númeraröðum fyrir viðskiptamenn, ef númeraröðin sem er skilgreind á síðunni **Uppsetning sölugrunns** er sett upp á þennan hátt, þá verður **Nr.** reiturinn ósýnilegur á viðskiptamannaspjaldinu, sama hvaða sniðmát þú notar. Það sama á við um aðrar tegundir spjalda og skjala.  

    > [!NOTE]  
    > Ef númeraröðin virkar ekki, til dæmis vegna þess að hún hefur náð síðasta númerinu sem skilgreint er fyrir bilið er reiturinn **Nr.** Birtast þannig að hægt sé að færa inn númer handvirkt. Hægt er að leysa vandamál í reitnum **Nr. Raðasíðu** .

2. Ef um er að ræða fleiri en eina númeraröð fyrir tegund fylgiskjals eða spjalds og Reitirnir **Sjálfg. nr.** ekki er valinn fyrir úthlutaða númeraröð, reitinn **Nr.** Og hægt er að fara í reitinn **Nr. Raða** síðu og velja númeraröðina sem á að nota. Næsta númer í röðinni er síðan sett í **Nr.** .

3. Ef ekki hafa verið settar upp númeraraðir fyrir tegund fylgiskjals eða spjalds eða reitsins **Handfærð nr.röð nr.** er valinn fyrir númeraröðina, reiturinn **Nr.** Birtast og færa þarf númer inn handvirkt. Rita má allt að 20 stöfum, bæði tölu- og bókstafi.

Þegar nýtt fylgiskjal eða spjald sem númeraröð er til fyrir er reiturinn **Nr. opnaður. Síðan Raðauppsetning** opnast þannig að hægt er að setja upp númeraraðir fyrir þá tegund fylgiskjals eða spjalds og halda áfram að vinna.

> [!NOTE]  
> Ef gera þarf handvirka tölusetningu virka, til dæmis, ný birgðaspjöld sem stofnuð voru með gagnaflutningsferli sem hefur falið **nr.** Sjálfgefið er að fara á síðuna **Birgðagrunnur** og velja reitinn Vörunr **.** til að opna og stilla tengda númeraröð á **Handfærð nr.röð**.
>
> Það sama á við ef þjónustukerfisaðgerðir eru notaðar. Til að leysa það mál er farið á síðuna **Þjónustukerfisgrunnur** og reiturinn **Nr. þjónustuvöru valinn.** til að stilla númeraröðina á **Handfærð nr.röð**

## <a name="to-create-a-new-number-series"></a>Til að búa til nýja númeraröð

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Númeraraðir** og velja síðan viðkomandi tengil.
2. Valið er aðgerðin **Nýtt**.  
3. Fyllt er í reitina í nýju línunni. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Veljið aðgerðina **Línur**.  
5. Á síðunni **Númeraraðarlínur nr.** fyllið inn reitina til að skilgreina raunnotkun og innihald númeraraðarinnar sem var stofnuð í skrefi 2.  
6. Endurtakið skref 5 fyrir sem margar mismunandi notkun á númeraröðinni sem þörf er á. Reiturinn **Upphafsdagsetning** skilgreinir svæðið sem númeraröðin er virk.  

> [!TIP]
> Til að gera notendum kleift að tilgreina númer handvirkt þegar þeir skrá nýjan viðskiptamann eða lánardrottin skal til dæmis velja reitinn **Handvirk nr.** í sjálfri númeraröðinni. Til að koma í veg fyrir handvirka tölusetningu skal hreinsa reitinn.

Hægt er að úthluta númeraröðum á sniðmátin sem sett eru upp fyrir mismunandi tegundir viðskiptamanna og lánardrottna sem sölumenn og innkaupaaðilar bæta oftast við. Í því tilviki skaltu setja upp viðkomandi númeraraðir, tengja þær í gegnum vensl og bæta síðan fyrstu númeraröðinni í viðkomandi vensl við viðkomandi uppsetningarsíðu. Síðan, þegar notandi býr til viðskiptamann, velur hann viðeigandi sniðmát og nýi viðskiptamaðurinn fær úthlutað númeri úr númeraröðinni sem er skilgreind fyrir það sniðmát.  

## <a name="to-create-relationships-between-number-series"></a>Stofnun tengsla milli númeraraða

Ef settir hafa verið upp fleiri númeraraðakótar en einn fyrir sömu tegund grunnupplýsinga eða færslna er hægt að stofna tengsl milli kótanna. Með þessari aðgerð er auðvelt að velja á milli kóta þegar númer er notað. Þegar komið er á tengslum milli flokka af númeraröðum eru allar skyldar raðir tengdar einum númeraraðarkóta. Síðan getur þú slegið þann kóða inn í reit í flýtiflipanum **Tölusetning** á einni viðeigandi uppsetningarsíðu, t.d. **Sölugrunnur**.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Númeraraðir** og velja síðan viðkomandi tengil.
2. Velja skal línuna með númeraröðinni sem á að stofna tengsl við. og veljið síðan **Tengsl**.
3. Færður er inn í reitinn **Raðarkóti** kóti fyrir númeraröðina sem á að tengja við röðina sem valin var í 2. þrepi.
4. Bætt er við línu fyrir hvern kóta sem á að tengja völdum númeraröðum.
5. Lokaðu síðunni.

Þegar eitthvað er sett upp eftir þetta sem þarfnast númers er hægt að nota tengslin sem voru stofnuð til að velja úr skyldum númeraröðum.

## <a name="to-set-up-where-a-number-series-is-used"></a>Til að setja upp hvar númeraröð er notuð

Eftirfarandi málsmeðferð sýnir hvernig á að setja númeraröð fyrir sölustaðinn. Skrefin eru svipuð fyrir önnur svæði.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptakröfur og viðskiptaskuldir** og velja svo viðeigandi tengil.
2. Á síðunni **Sala**, í **Númeraröð**, veldu viðkomandi númeraröð fyrir hvert sölukort eða skjal.

Völdu númerið verður nú notað til að fylla út **Nr.** Sviði á viðkomandi korti eða skjali, í samræmi við þær stillingar sem þú gerðir á númeraröðinni.  

## <a name="see-also"></a>Sjá einnig .

[Uppsetning [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
