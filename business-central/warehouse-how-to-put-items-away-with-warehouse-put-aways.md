---
title: Hvernig gengið er frá vörum með vöruhúsafrágangi
description: Fræðast um mismunandi leiðir til að nota vöruhúsafrágang til að ganga frá mótteknum vörum.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 04/23/2024
ms.custom: bap-template
ms.search.forms: '7352, 7333'
---
# <a name="put-items-away-with-warehouse-put-aways"></a>Gengið frá vörum með vöruhúsafrágangi

Vörur [!INCLUDE[prod_short](includes/prod_short.md)] eru mótteknar og gengið frá þeim með einni af fjórum aðferðum eins og lýst er í eftirfarandi töflu.

|Aðferð|Ferli á innleið|Krefjast móttöku|Krefjast frágangs|Flóknarastig (Fræðast meira um [vöruhúsakerfisyfirlit](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Bóka móttöku og frágang frá pöntunarlínunni|||Engin sérstök vöruhúsaaðgerð.|  
|Á|Bóka móttöku og frágang frá birgðafrágangsskjali||Kveikt|Grunnur: Pöntun-fyrir-pöntun.|  
|U|Bóka móttöku og frágang frá vöruhúsamóttökuskjali|Kveikt||Grunnur: Bókuð móttaka/sending í mörgum pöntunum.|  
|D|Bóka móttöku frá vöruhúsamóttökuskjali og bóka frágang frá vöruhúsafrágangsskjali|Kveikt|Kveikt|Ítarlegt|  

Nánari upplýsingar í Vöruhúsaflæði á [innleið](design-details-inbound-warehouse-flow.md).

Þessi grein vísar í aðferð D í töflunni og gerir ráð fyrir að móttaka hafi þegar gerst. Nánari upplýsingar um móttöku [vara](warehouse-how-receive-items.md).

Þegar birgðageymsla er sett þannig upp að krafist sé vöruhúsafrágangsvinnslu og vöruhúsamóttökuvinnslu eru vöruhúsafrágangsskjöl notuð til að stjórna því hvernig gengið er frá vörum. Þegar vöruhúsamóttaka er bókuð eru upprunaskjöl eins og innkaupa-, millifærslu- eða söluvöruskilapantanir uppfærð. Móttekið magn er bókað í birgðahöfuðbók og línurnar fyrir mótteknar vörur eru sendar í frágangsaðgerðina í vöruhúsinu.

Línurnar eru annaðhvort tiltækar á frágangsvinnublaðinu **eða notaðar til að búa til frágangsskjöl samstundis, allt eftir gildinu í** reitnum Nota vinnublað frágangs á **birgðageymsluspjaldinu**. Nánari upplýsingar um [uppsetningu vöruhúsastjórnunar](warehouse-setup-warehouse.md).  

Auk staðlaðra leiða til að stofna vöruhúsafrágang sem þessi hluti lýsir er hægt að stofna frágang úr tengdri bókuðu vöruhúsamóttöku. Þetta er gagnlegt ef frágangslínum hefur verið eytt eða ef ekki á að nota frágangsvinnublaðið því hægt er að stofna eða endurstofna frágangsleiðbeiningar úr bókuðu móttökulínunum.

## <a name="zone-and-bin-codes"></a>Svæðis- og hólfakótar

Í birgðageymslum sem eru settar upp til að nota beinan frágang og tínslu þarf eftirfarandi stillingar til að ákvarða besta staðinn til að setja vörurnar:  

* Frágangssniðmát er sett upp: Nánari upplýsingar um [uppsetning frágangssniðmáta](warehouse-how-to-set-up-put-away-templates.md).  
* Þyngd, rúmmál og sérstakar geymsluþarfir vörunnar eða birgðahaldseiningarinnar eru skilgreindar.
* Afkastageta, hólfategund og hólfaflokkun eru skilgreind fyrir hólfin.  

Hólfaflokkunin er notuð þegar fleiri en eitt hólf uppfylla skilyrðin í frágangssniðmátinu. Ef bæði skilyrði frágangssniðmáts og hólfaflokkun eru þau sömu er valið hólf með hærra númeri.

## <a name="to-create-put-away-documents-in-bulk-with-the-put-away-worksheet"></a>Frágangsskjöl stofnuð í magni á frágangsvinnublaðinu

[!INCLUDE [edit-in-excel](includes/edit-in-excel.md)]

Hægt er að stofna frágangsskjöl fyrir margar móttökur samtímis á síðunni **Vinnublað** frágangs.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Vinnublöð frágangs** og velja síðan viðeigandi tengil.  
2. Valið er **Sækja vöruhúsaskjöl** aðgerð. Síðan **Frágangsval** opnast.  

    Á listanum eru allar bókaðar móttökur sem eru tilbúnar til frágangs, þar á meðal þær sem frágangsleiðbeiningarnar hafa þegar verið stofnaðar fyrir. Skjöl með frágangslínur sem gengið hefur verið frá að fullu og skráðar birtast ekki á þessum lista.  
3. Skjölin sem vinna á með eru valin. Hægt er að vinna með línur úr nokkrum skjölum í einu.  

    > [!NOTE]  
    > Ef valið er móttöku- eða innanhússfrágangsskjal sem leiðbeiningar hafa þegar verið stofnaðar fyrir allar línur [!INCLUDE[prod_short](includes/prod_short.md)], er tilkynnt að ekkert sé til meðhöndlunar.  

4. Reiturinn **Röðunaraðferð** er fylltur út til að raða línunum.  

    > [!NOTE]  
    > Það hvernig línunum er raðað á vinnublaðinu flyst ekki sjálfkrafa í frágangsleiðbeiningarnar. Hins vegar eru sömu tækifæri til að flokka og hólfaflokkun vera til. Hægt er að endurgera línupöntunina sem áætluð er á vinnublaðinu þegar frágangsleiðbeiningarnar eru stofnaðar eða raðað í frágangsleiðbeiningunum.

5. Fylla inn í reitinn **Magn til afgreiðslu**. Velja aðgerðina **Færa sjálfkr. magn til afgr.** eða fyllið út reitina handvirkt.  
6. Línunum er breytt handvirkt ef með þarf. Hægt er að eyða línum, til dæmis ef ganga þarf frá sumum vörum í hólfi sem er langt frá hólfunum fyrir hinar vörurnar.  

    > [!NOTE]  
    > Þegar línum er eytt er þeim aðeins eytt úr þessu vinnublaði. Þeim er ekki eytt úr frágangsvali.  

7. Veldu aðgerðina **Stofna frágang**. Síðan **Stofna fylgiskjal** opnast, þar sem hægt er að bæta við upplýsingum í fráganginn sem verið er að stofna.  

    * Hægt er að úthluta fráganginum á tiltekinn starfsmann.  
    * Hægt er að raða frágangsleiðbeiningalínum eins og gert var á vinnublaðinu eða eftir flokkun hólfa. Þegar raðað er eftir hólfaflokkun *birtast Taka-línurnar* fyrst þar sem flest móttökuhólf eru með 0 hólfaflokkun. Setja-línurnar *birtast* síðast og byrja á hólfunum með lægstu hólfaflokkunina. Hafi vöruhúsið verið skipulagt þannig að hólf með svipaða hólfaflokkun séu hlið við hlið sparar röðun á þennan hátt skref fyrir vöruhúsastarfsmenn.  
    * Hægt er að taka ekki með línurnar sem [!INCLUDE [prod_short](includes/prod_short.md)] stofnaðar voru þegar stórri mælieiningu var breytt í smærri mælieiningar með því að velja reitinn **Setja einingaskiptaafmörkun** . Fá nánari upplýsingar um einingaskipti í [Gera sjálfvirka einingaskipti virka með beinum frágangi og tínslu](warehouse-enable-automatic-breaking-bulk-with-directed-put-away-and-pick.md).  
    * Hægt er að velja að ekki sé sjálfkrafa fyllt út í reitinn **Magn til afgreiðslu** í frágangsleiðbeiningunum.  
    * Hægt er að prenta skjalið strax.  

8. Velja skal **Í lagi** til að stofna fráganginn.  

## <a name="to-create-a-put-away-from-a-posted-receipt"></a>Til að búa til frágang úr bókaðri uppskrift

Ef birgðageymsla notar bæði frágangsvinnslu og móttökuvinnslu og frágangslínum hefur verið eytt eða ef notaður er beinn frágangur og tínsla og ekki á að nota frágangsvinnublaðið er hægt að stofna eða endurstofna frágangsleiðbeiningar fyrir bókaðar móttökulínur.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **Bókaðar vöruhúsamóttökur** og velja síðan viðeigandi tengil.  
2. Valin er bókuð móttaka til frágangs.  
3. Velja aðgerðina **Spjald**.  

    Ef reiturinn **Staða fylgiskjals** er auður hefur alls ekki verið gengið frá móttökunni. Annars gefur reiturinn til kynna hvort móttakan sé að hluta til eða frágengin að fullu.  

4. Ef gengið hefur verið frá móttökunni að hluta eða alls ekki er smellt á aðgerðina **stofna frágang**.  
5. Reitirnir eru fylltir út eftir þörfum og síðan er valið **Í lagi**.  

## <a name="to-put-items-away"></a>Gengið frá vörum

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **vöruhúsafrágang** og velja síðan viðeigandi tengil.

2. Vöruhúsafrágangurinn sem er tilbúinn til afgreiðslu er opnaður.  
3. Ef þess er krafist í vöruhúsinu er kenni notanda fært inn þegar vinna hefst við frágang.  

    Hægt er að raða frágangslínum eftir ýmsum skilyrðum, til dæmis eftir vöru, hillunúmeri eða gjalddaga. Röðun getur hjálpað til við að fínstilla frágangsferlið, til dæmis:

    * Ef Taka- og Setja-línurnar fyrir hverja móttökulínu fylgja ekki hver annarri á ekki strax að fylgja og þess er óskað skal raða línunum með því að velja **Vara** í reitnum **Röðunaraðferð** .  
    * Ef hólfaflokkanir endurspegla raunútlit vöruhússins er röðunaraðferðin Hólfaflokkun **notuð** til að skipuleggja verkið eftir hólfastaðsetningum.

  > [!NOTE]  
  > Línum er raðað í hækkandi röð eftir völdum skilyrðum. Ef raðað er eftir fylgiskjali fer röðun fyrst eftir tegund fylgiskjals samkvæmt reitnum **Upprunaskjal vöruhúsaaðgerðar** . Ef raðað er eftir sendist-til er röðun framkvæmd fyrst eftir tegund áfangastaðar sem byggð er á reitnum **Tegund** viðtöku vöruhúss.

4. Framkvæma aðgerðirnar.

    Ef hólfakóti er áskilinn fyrir birgðageymslurnar verður hver móttökulína að minnsta kosti tvær línur í vöruhúsafrágangi eins og hér er lýst.  

    * Fyrsta línan sem hefur **Taka** í reitnum **Aðgerð** sýnir hvar vörurnar eru staðsettar á móttökusvæðinu. Ekki er hægt að breyta svæði og hólfi í línunni.  
    * Næsta lína, með **Setja** í reitnum **Aðgerð**, sýnir hvar setja á vörurnar í vöruhúsinu. Ef tekið er á móti mörgum vörum í einni móttökulínu gæti þurft að ganga frá vörunum í mörg hólf svo að það er Setja-lína fyrir hvert hólf. 

    > [!NOTE]
    > Ef setja þarf vörur í eina línu í fleiri en eitt hólf, til dæmis vegna þess að merkta hólfið er fullt, skal nota aðgerðina **Skipta línu** á flýtiflipanum **Línur** . Aðgerðin stofnar línu fyrir eftirstandandi magn sem á að meðhöndla.

5. Þegar allar vörurnar hafa verið settar í hólf samkvæmt skal velja aðgerðina **Skrá frágang**.  

## <a name="see-also"></a>Sjá einnig .

[Yfirlit yfir vöruhúsakerfi](design-details-warehouse-management.md)
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
