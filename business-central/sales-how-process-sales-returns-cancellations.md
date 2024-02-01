---
title: Vinna söluskil eða afturkallanir
description: 'Lýsir því hvernig skal stofna kreditreikning til að vinna skil, afturköllun eða endurgreiðslu fyrir vöru eða þjónustu sem þú hefur fengið greiðslu fyrir.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'undo, credit memo, return'
ms.search.form: '44, 134, 143, 6629, 6630, 6633, 6662, 9302, 9304, Report_6646'
ms.date: 09/27/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="process-sales-returns-or-cancellations"></a>Vinna söluskil eða afturkallanir

Ef viðskiptavinur vill skila eða endurgreiða fyrir vörur eða þjónustu sem þú hefur selt og fengið greiðslu fyrir verður þú að búa til og senda inn söluskuldbindingar sem tilgreinir umbeðnar breytingar. Til að hafa með réttar upplýsingar um sölureikning er hægt að gera eftirfarandi:  

- Stofnaðu sölukreditreikning beint úr bókuðum sölureikningi.
- Stofnaðu nýjan sölukreditreikning með afrituðum reikningsupplýsingum.

Ef þú þarft meiri stjórn á söluskilaferlinu, eins og t.d. vöruhúsaskjöl fyrir vöruafgreiðsluna eða betra yfirlit yfir móttöku vara frá mörgum söluskjölum með einum vöruskilum, geturðu stofnað söluvöruskilapöntun. Söluvöruskilapöntun gefur út sjálfkrafa tengdan sölukreditreikning og önnur skilatengd skjöl, eins og skiptivörusölupöntun, ef þarf. Frekari upplýsingar er að finna í [Vinna söluvöruskilapantanir](sales-how-process-sales-returns-orders.md).

> [!NOTE]  
> Ef sölureikningur hefur ekki verið greiddur þá geturðu notað **Rétt** eða **Hætta við** aðgerðirnar á bókaða sölureikningnum til að snúa við viðskiptum. Þessir eiginleikar virka aðeins fyrir ógreidda reikninga og styðja ekki vöruskil að hluta eða afturkallanir. Frekari upplýsingar eru í [Ógreiddir sölureikningar leiðréttir eða afturkallaðir](sales-how-correct-cancel-sales-invoice.md).

Skil eða endurgreiðsla getur átt við um aðeins hluta af vörum eða þjónustum á upprunalega sölureikningnum. Í því tilviki þarf að breyta upplýsingum í línunum á sölukreditreikningnum eða söluvöruskilapöntun. Við bókun sölukreditreiknings eða söluvöruskilapöntun eru þau söluskjöl sem eru breytingin hefur áhrif á bakfærð og hægt er að stofna endurgreiðslu til viðskiptamannsins. Frekari upplýsingar eru í [Greiðslur framkvæmdar](payables-make-payments.md).  

Bókun innkaupareiknings mun einnig snúa við öllum kostnaðarauka sem var úthlutað á bókaða skjalið, þannig að vöruvirðisfærslurnar eru þær sömu og áður en kostnaðaraukanum var úthlutað.

> [!NOTE]
> Bókhaldsþættir söluvöruskila, svo sem greiðslur til viðskiptamanna sem endurgreiðsla, teljast bókhaldsverk og er ekki lýst hér. Nánari upplýsingar er að finna í [Stjórna skuldum](payables-manage-payables.md).

## <a name="to-create-a-sales-credit-memo-from-a-posted-sales-invoice"></a>Að stofna nýjan sölukreditreikning úr bókuðum sölureikningi.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bókaðir sölureikningar** og velja síðan viðkomandi tengil.  
2. Á síðunni **Bókaðir sölureikningar** skal velja þá bókuðu sölureikninga sem á að bakfæra, veljið **Hætta við** og veljið síðan aðgerðina **Stofna leiðréttan kreditreikning**.

    Minnispunktur fyrir sölureikninginn inniheldur nokkrar upplýsingar frá staða sölureikningsins. Hægt er að breyta þessu, til dæmis með nýjar upplýsingar sem endurspegla endursenda samkomulagið.  
3. Breyttu upplýsingum um línurnar í samræmi við samninginn, svo sem fjölda skilaðra hluta eða fjárhæðin sem endurgreiða.
4. Veldu aðgerðina **Undirbúa** og veldu svo aðgerðina **Nota færslur**.
5. Á síðunni **Jafna viðskm.færslur** skal velja línuna með bókaða söluskjalinu sem á að jafna sölukreditreikninginn við og veljið síðan aðgerðina **Kenni jöfnunar**.

    Kennimerki söluskuldbindinga birtist á **kenni jöfnunar**.
6. Sláðu inn **Upphæð til að jafna** sem þú vilt sækja um í upphæðin sem á að sækja um ef hún er minni en upphafleg upphæð.  

    Neðst á síðunni **Jafna viðskm.færslur** er hægt að skoða heildarupphæðina sem á að nota til að bakfæra allar færslur, nefnilega þegar gildið í reitnum **Staða** er núll.
7. Velja hnappinn **Í lagi**. Þegar þú sendir inn sölutilboðið, þá er það sótt á staða söluskráanna.

    Eftir að þú hefur stofnað línur fyrir sölukreditreikningana eða breytt þeim og ein eða fleiri jöfnun tilgreind, er hægt að bóka sölukreditreikninginn.  
8. Veldu aðgerðina **Bókun**, veldu síðan aðgerðina **Bóka og senda**.  

Í **Bóka og Senda staðfestingu** svargluggi opnast og sýnir notuð valda sendingaraðferð fyrir viðskiptamanninn. Hægt er að breyta sendingaraðferð með því að velja uppflettihnappinn í reitnum **Senda skjal** til. Frekari upplýsingar er að finna á [Setja upp sendisnið skjala](sales-how-setup-document-send-profiles.md).  

Bókuðu söluskjölin sem jafnað var við kreditreikninginn eru nú bakfærðir og endurgreiðslu má nú búa til fyrir viðskiptamanninn. Sölukreditreikningurinn er fjarlægður og skipt út fyrir nýtt fylgiskjal á lista bókaðra sölukreditreikninga.

## <a name="to-create-a-sales-credit-memo-by-copying-a-posted-sales-invoice"></a>Að stofna sölukreditreikning með því að afrita bókuðum sölureikningi

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sölukreditreikningar** og velja síðan viðkomandi tengil.
2. Veljið aðgerðina **Nýtt** til að opna nýjan auðan sölukreditreikning.
3. Í reitnum **Nafn viðskiptamanns** er fært inn nafn núverandi viðskiptamanns.
4. Veldu aðgerðina **Undirbúa**, veldu síðan aðgerðina **Afrita skjal**.
5. Á síðunni **Afrita söluskjal** í reitnum **Gerð skjals** skal velja **Bókaður reikningur**.
6. Velja reitinn **Númer fylgiskjals** til að opna síðuna **Bókaðar sölureikningar** og síðan velja bókaða sölureikningsfærslu sem inniheldur línur sem á að bakfæra.
7. Veljið gátreitinn **Endurreikna línur**, ef bókaða sölureikningslínan sem var afrituð á að uppfærast með breytingum á vöruverði og kostnaðarverði síðan reikningurinn var bókaður.
8. Velja hnappinn **Í lagi**. Afrituðu reikningslínurnar eru settar inn í sölukreditreikninginn.
9. Sölukreditreikningnum er lokið eins og útskýrt er í [Að stofna sölukreditreikning úr bókuðum sölureikningi](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-credit-memo-from-a-posted-sales-invoice).

## <a name="to-create-a-sales-allowance"></a>Til að bóka söluuppbót:
Hægt er að senda viðskiptamanni kreditreikning með verðlækkun hafi viðskiptamaðurinn fengið vörurnar lítillega skaddaðar eða of seint.  
Hægt er að bóka þetta lægra verð sem kostnaðarauka á kreditreikningi eða vöruskilapöntun og úthluta því á bókaða afhendingu. Eftirfarandi lýsir því fyrir sölukreditreikning, en sömu skref eiga við um söluvöruskilapöntun.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sölukreditreikningar** og velja síðan viðkomandi tengil.
2. Veljið aðgerðina **Nýtt** til að opna nýjan auðan sölukreditreikning.
3. Kreditreikningshausinn er fylltur út með öllum viðeigandi upplýsingum um viðskiptamanninn sem á að veita söluuppbót.  
4. Á flýtiflipanum **Línur** í reitnum **Tegund** er valin **Gjald (vara)**.  
5. Í reitnum **númer** er valið viðeigandi vörugjaldsnúmer.  
     Gott gæti verið að stofna sérstakt kostnaðaraukanúmer fyrir söluuppbætur.  
6. Fært er inn **1** í reitinn **Magn**.  
7. Í reitinn **Ein.verð án skatts** er upphæð söluuppbótarinnar færð inn.  
8. Söluuppbótinni er  úthlutað sem vörugjaldi á vörurnar í bókuðu afhendingunni. Frekari upplýsingar er að finna í [Nota kostnaðarauka til að gera grein fyrir viðbótar viðskiptakostnaði](payables-how-assign-item-charges.md). Þegar uppbótinni hefur verið úthlutað er snúið aftur á síðuna **Sölukreditreikningur**.  

Þegar söluvöruskilapöntunin er bókuð er söluafslætti bætt við viðkomandi upphæð sölufærslu. Þannig er hægt að vinna með nákvæmt birgðaverðmat.

## <a name="to-combine-return-receipts"></a>Hvernig á að sameina vöruskilamóttökur
Hægt er að sameina vöruskilamóttökur ef viðskiptamaður er að skila mörgum vörum sem margar söluskilapantanir eiga við um.  

Þegar varan er móttekin í vöruhúsi er viðkomandi söluvöruskilapöntun bókuð sem móttekin. Þetta býr til bókaðar vöruskilamóttökur  

Þegar kemur að því að reikningsfæra viðskiptamanninn er hægt að stofna sölukreditreikning og afrita sjálfkrafa bókaðar innkaupaskilasendingarlínur í skjalið, í stað þess að reikningsfæra hverja söluskilapöntun sérstaklega. Þá má bóka sölukreditreikning og reikningsfæra allar opnar sölupantanir í einu.  

Til að sameina vöruskilamóttökur þarf að velja gátreitinn **Sameina afhendingar** á síðunni **Viðskiptamannaspjald**.  

### <a name="to-manually-combine-return-receipts"></a>Til að sameina vöruskilamóttökur handvirkt:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sölukreditreikningar** og velja síðan viðkomandi tengil.  
2. Valið er aðgerðin **Nýtt**.
3. Fyllt er út í reiti eftir því sem er nauðsynlegt í flýtiflipanum **Almennt**.  
4. Velja aðgerðina **Sækja vöruskilamóttökulínur**.  
5. Valdar eru vöruskilamóttökulínurnar sem á að taka með í kreditreikninginn.  

    - Til að setja allar línur inn eru allar línur valdar og svo smellt á **Í lagi** hnappinn.  

    - Til að setja sérstakar línur inn eru línurnar valdar og svo smellt á **Í lagi** hnappinn.  
6.  Ef röng afhendingarlína var valin eða byrja á aftur er línunum einfaldlega eytt í kreditreikningnum aðgerðin **Sækja vöruskilamóttökulínur** keyrð aftur.  
7.  Bóka skal reikninginn.  

### <a name="to-automatically-combine-return-receipts"></a>Til að sameina vöruskilamóttökur sjálfvirkt

Hægt er að sameina vöruskilamóttökur sjálfvirkt og hafa möguleikann á að bóka kreditreikninga sjálfvirkt með aðgerðinni **Sameina vöruskilamóttökur**.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sameina vöruskilamóttökur** og velja síðan viðkomandi tengil.
2. Á síðunni **sameina innkaupamóttökur** skal fylla inn í reitina til að velja viðeigandi vöruskilamóttökur.
3. Velja skal gátreitinn **Bóka kreditreikninga**. Ef ekki, verður að handvirkt bóka viðeigandi innkaupakreditreikninga.
4. Velja hnappinn **Í lagi**.  

### <a name="to-remove-a-received-and-invoiced-return-order"></a>Mótteknar og reikningsfærðar vöruskilamóttökur fjarlægðar

Þegar vöruskilamóttökur eru reikningsfærðar á þennan hátt eru vöruskilapantanir sem vöruskilamóttökurnar voru bókaðar úr enn til staðar, jafnvel þótt þær hafi verið mótteknar og reikningsfærðar að fullu.  

Þegar vöruskilamóttökur eru sameinaðar í kreditreikningi og svo bókaðar er bókaður sölukreditreikningur stofnaður fyrir kreditfærðu línurnar. Reiturinn **Reikningsfært magn** úr upphaflegu söluvöruskilamóttökunni er uppfærður samkvæmt reikningsfærðu magni.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eyða reiknf. innk.söluskilapöntunum** og velja síðan viðkomandi tengil.  
2. Tilgreinið í **Nr.**. afmörkunarreitnum hvaða vöruskilapöntunum á að eyða.  
3. Velja hnappinn **Í lagi**.  

Að öðrum kosti skal eyða einstökum söluvöruskilapöntunum handvirkt.  

## <a name="inventory-costing"></a>Birgðakostnaður

Til að varðveita rétt birgðaverðmat, eru vanalega setja skilavörur aftur inn í birgðum á því kostnaðarverði sem þær voru seldar á, en ekki núgildandi kostnaðarverði. Þetta er kallað nákvæm bakfærsla kostnaðar.

Til er tvenns konar virkni, til að úthluta bakfærslu nákvæms kostnaðar sjálfvirkt:  

|Virkni|Description|  
|------------------|---------------------------------------|  
|**Sækja bókaðar fylgiskjalalínur til að bakfæra** aðgerð á síðunni **Söluvöruskilapöntun**|Afritar línur úr einu eða fleiri bókuðum fylgiskjölum sem á að bakfæra til söluvöruskilapöntun. Frekari upplýsingar er að finna í [Stofna vöruskilapöntun byggða á einu eða fleiri bókuðu söluskjali](sales-how-process-sales-returns-orders.md#create-a-sales-return-order-based-on-one-or-more-posted-sales-documents).|  
|**Afrita skjal** aðgerð í **Sölukreditreikningur** og á síðunni **Söluvöruskilapöntun**|Afritar bæði haus og línur af einu bókuðu fylgiskjali sem á að bakfæra.<br /><br /> Krefst þess að **Nákvæm bakfærsla kostnaðar** gátreitur sé valinn á síðunni **Uppsetning fyrir Sölu & Viðskiptaskuldir**.|

Til að úthluta nákvæmri bakfærslu kostnaðar, skal velja reitinn **Jafna frá birgðafærslu** á einhverja gerð skilaskjalslínu, og velja síðan númer upphaflega sölufærslunnar. Það tengir sölukreditreikninginn eða söluvöruskilapöntunina við upphaflega sölufærslu og tryggir að varan er metin út frá upphaflegu einingarverði.

Nánari upplýsingar, sjá [Upplýsingar um hönnun: Birgðakostnaður](design-details-inventory-costing.md)

## <a name="see-also"></a>Sjá einnig

[Sala](sales-manage-sales.md)  
[Uppsetning sölu](sales-setup-sales.md)  
[Stjórna skuldum](payables-manage-payables.md)  
[Senda skjöl í tölvupósti](ui-how-send-documents-email.md)  
[Meðhöndlun innkaupaskila eða afturkallana](purchasing-how-process-purchase-returns-cancellations.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
