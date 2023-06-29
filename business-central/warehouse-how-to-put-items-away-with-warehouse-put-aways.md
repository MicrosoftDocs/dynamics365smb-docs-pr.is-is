---
title: Hvernig á að setja vörur af stað með vöruhúsafrágangi
description: Fræðast um mismunandi leiðir til að nota vöruhúsafrágang til að ganga frá mótteknum vörum.
author: bholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/24/2023
ms.custom: bap-template
ms.search.forms: '7352, 7333'
---
# <a name="put-items-away-with-warehouse-put-aways"></a><a name="put-items-away-with-warehouse-put-aways"></a>Ganga frá vörum með vöruhúsafrágangi

Í  [!INCLUDE[prod_short](includes/prod_short.md)] eru vörur afhentar og þær síðan notaðar með einni af fjórum aðferðum, eins og lýst er í eftirfarandi töflu.

|Aðferð|Ferli á innleið|Krefjast kvittana|Krefjandi frágangur|Flókið stig (frekari upplýsingar um  [Vöruhúsakerfi-Yfirlit](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Bóka móttöku og frágang frá pöntunarlínunni|||Engin sérstök vöruhúsaaðgerð.|  
|B|Bóka móttöku og frágang frá birgðafrágangsskjali||Kveikt|Grunnur: pöntun-eftir pöntun.|  
|N|Bóka móttöku og frágang frá vöruhúsamóttökuskjali|Kveikt||Grunnur: Samstæða móttöku/skipa bóka fyrir margar pantanir.|  
|D|Bóka móttöku frá vöruhúsamóttökuskjali og bóka frágang frá vöruhúsafrágangsskjali|Kveikt|Kveikt|Ítarlegt|  

Frekari upplýsingar um vöruflæði á  [innleið](design-details-inbound-warehouse-flow.md).

Með þessari grein er átt við aðferð D í töflunni og gert ráð fyrir að móttaka hafi þegar gerst. Frekari upplýsingar um  [móttöku vara](warehouse-how-receive-items.md).

Þegar Birgðageymsla er sett þannig upp að hún krefjist vöruhúsafrágangs og vöruhúss sem tekur við vinnslu, skal nota vöruhúsafrágangsskjöl til að stjórna hvernig gengið er frá vörum. Þegar vöruhúsamóttaka er bókuð eru upprunaskjöl eins og innkaupa-, Millifærsla-eða vöruskilapantanir, uppfærðar. Móttekið magn er bókað í birgðahöfuðbók og línurnar fyrir mótteknar vörur eru sendar í frágangsaðgerðina í vöruhúsinu.

Eftir gildinu í  **reitnum nota vinnublað**  notkunar á  **birgðageymsluspjaldinu** er línurnar sem eru annaðhvort gerðar tiltækar við vinnublað frágangs eða notaðar til að mynda strax frágang fylgiskjala. Frekari upplýsingar um  [uppsetningu vöruhúsastjórnunar](warehouse-setup-warehouse.md).  

Auk staðlaðra aðferða til að stofna vöruhúsafrágang sem þessi grein lýsir er hægt að stofna frágang úr tengdri bókaðri vöruhúsamóttöku. Þetta er gagnlegt ef búið er að eyða frágangslínum eða ef ákveðið er að nota vinnublaðið sem frágangurinn er, því hægt er að stofna eða endurafþakka frágangsleiðbeiningar úr bókuðu móttökulínunum.

## <a name="zone-and-bin-codes"></a><a name="zone-and-bin-codes"></a>Svæði og hólfakóta

Á birgðageymslum sem eru sett upp þannig að notaður sé beinn frágangur og tínsla eru eftirtaldar stillingar nauðsynlegar til að ákvarða besta staðinn til að setja vörurnar:  

* Frágangssniðmát er sett upp: Frekari upplýsingar er að  [Setja upp frágang sniðmáta](warehouse-how-to-set-up-put-away-templates.md).  
* Þyngd, rúmmál og sérstök GEYMSLUSKILYRÐI vörunnar eða birgðahaldseining eru skilgreind.
* Afkastageta, tegund hólfs og hólfaflokkun eru skilgreind fyrir hólfin.  

Hólfaflokkun er notuð þegar fleiri en eitt hólf eru í samræmi við skilyrðin í frágangssniðmátinu. Ef bæði skilyrði frágangssniðmáts og hólfaflokkun eru þau sömu er valið hólf með hærra númeri.

## <a name="to-create-put-away-documents-in-bulk-with-the-put-away-worksheet"></a><a name="to-create-put-away-documents-in-bulk-with-the-put-away-worksheet"></a>Frágangur skjala í magni búið til með því að setja vinnublaðið í gang

Hægt er að stofna frágangsskjöl fyrir margar innhreyfingar á sama tíma og á  **vinnublaðsíðunni**  Frágangur frágangs.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn  **frágang vinnublaða** og velja síðan tengda tengil.  
2. Valið er **Sækja vöruhúsaskjöl** aðgerð. Síðan **Frágangsval** opnast.  

    Listinn inniheldur allar bókaðar innhreyfingar sem eru tilbúnar til frágangs, þar með talið þær sem frágangsleiðbeiningar hafa þegar verið stofnaðar fyrir. Skjöl með frágangslínur sem gengið hefur verið frá að fullu og skráðar birtast ekki á þessum lista.  
3. Velja skjölin sem vinna á við. Hægt er að vinna með línur úr nokkrum skjölum í einu.  

    > [!NOTE]  
    >  Ef valið er kvittun eða innanhússfrágangsskjal sem þegar hefur verið búið að fá leiðbeiningar fyrir allar línur,  [!INCLUDE[prod_short](includes/prod_short.md)] ] mun upplýsa þig um að það sé ekkert hægt að afgreiða.  

4.  **Reiturinn röðunaraðferð**  er fylltur út til að raða línunum.  

    > [!NOTE]  
    >  Því hvernig línunum er raðað á vinnublaðinu er ekki sjálfkrafa haldið við í frágangsleiðbeiningunum. Hins vegar eru sömu tækifæri til flokkunar og hólfaflokkunar. Hægt er að endurgera línupöntunina sem er áætlun í vinnublaðinu þegar frágangsleiðbeiningarnar eru stofnaðar eða raðað eftir frágangsleiðbeiningunum.

5. Fylla inn í reitinn **Magn til afgreiðslu**. Velja aðgerðina **Færa sjálfkr. magn til afgr.** eða fyllið út reitina handvirkt.  
6. Breytið línunum handvirkt ef þörf krefur. Hægt er að eyða línum, til dæmis ef ganga þarf frá einhverjum vörum í hólfi sem er fjarri hólfunum fyrir hinar vörurnar.  

    > [!NOTE]  
    > Þegar línum er eytt eyðast þær aðeins úr þessu vinnublaði. Þeim er ekki eytt úr valnum frágangi.  

7. Veldu aðgerðina **Stofna frágang**.  **Síðan stofna skjal**  opnast, þar sem þú getur bætt við meiri upplýsingum við fráganginn sem þú ert að búa til.  

    * Hægt er að úthluta fráganginum á tiltekinn starfsmann.  
    * Hægt er að raða frágangsleiðbeiningalínum eins og gert var á vinnublaðinu eða eftir flokkun hólfa. Þegar raðað er eftir hólfaflokkun birtast línur sem  *·*  fyrst, þar sem flest móttökuhólf eru með 0 hólfaflokkun.  *Línur í stað*  koma síðast og byrja á hólfum með lægstu hólfaflokkun. Hafi vöruhúsið verið skipulagt þannig að hólf með svipaða flokkun séu á hlið eru röðunarlínur á þessari leið vistaðar fyrir starfsmenn vöruhúss.  
    * Hægt er að velja að línurnar sem  [!INCLUDE[prod_short](includes/prod_short.md)] ekki á að búa til hafi verið breytt með því að umbreyta stórri mælieiningu í smærri mælieiningar með því að velja  **reitinn setja einingasíuafmörkun** . Frekari upplýsingar um rofmagn til að  [Virkja sjálfvirka rofa fjöldafrágangs með beinan frágang og tínslu](warehouse-enable-automatic-breaking-bulk-with-directed-put-away-and-pick.md).  
    * Hægt er að velja að ekki sé sjálfkrafa fyllt út í reitinn **Magn til afgreiðslu** í frágangsleiðbeiningunum.  
    * Hægt er að prenta skjalið strax.  

8. Valið  **er í lagi**  til að búa til frágang.  

## <a name="to-create-a-put-away-from-a-posted-receipt"></a><a name="to-create-a-put-away-from-a-posted-receipt"></a>Til að búa til frágang úr bókaðri uppskrift

Ef Birgðageymsla er notuð fyrir bæði frágangsvinnslu og móttöku og eytt er frágangslínum eða ef beinn frágangur og tínsla eru notuð og ákveðið er að nota ekki frágangsvinnublaðið er hægt að stofna eða endurgera leiðbeiningar fyrir bókuðu móttökulínurnar.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teikn, færa inn  **bókaðar vöruhúsamóttökur** og velja síðan tengda tengilinn.  
2. Velja bókaða kvittun sem á að ganga frá.  
3. Velja aðgerðina **Spjald**.  

    Ef reiturinn **Staða fylgiskjals** er auður hefur alls ekki verið gengið frá móttökunni. Að öðrum kosti gefur reiturinn til kynna hvort móttakan er að hluta til eða alveg fráganginn.  

4. Ef gengið hefur verið frá móttökunni að hluta eða alls ekki er smellt á aðgerðina **stofna frágang**.  
5. Reitirnir eru fylltir út eftir þörfum og síðan er valið  **í lagi**.  

## <a name="to-put-items-away"></a><a name="to-put-items-away"></a>Að setja vörur í burtu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn  **vöruhúsafrágang** og veljið síðan tengda tengilinn.

2. Opna vöruhúsafráganginn sem er tilbúinn til afgreiðslu.  
3. Ef vöruhúsið krefst er NOTANDAKENNI fært inn þegar vinna við frágang er hafin.  

    Hægt er að raða frágangslínunum eftir ýmsum skilyrðum, til dæmis eftir vöru, Hillunúmer eða gjalddaga. Sorpurðun getur hjálpað til við að fínstilla frágangsferlið, t.d.:

    * Ef taka og setja línur fyrir hverja móttökulínu eiga ekki strax að fylgja annarri annarri og á þeim er hægt að raða línunum með því að velja  **atriði**  í  **reitnum röðunaraðferð** .  
    * Ef bin fremstur endurspeglar efnislegt skipulag vöruhúss skal nota  **röðunaraðferð hólfaflokkun**  til að skipuleggja vinnu eftir hólfastöðum.

4. Framkvæma aðgerðirnar.

    Ef hólfakóða er skylda fyrir birgðageymslur verða hver móttökulína að minnsta kosti tvær línur í vöruhúsafrágangi, sem hér segir.  

    * Fyrsta línan sem hefur **Taka** í reitnum **Aðgerð** sýnir hvar vörurnar eru staðsettar á móttökusvæðinu. Ekki er hægt að breyta svæði og hólfi í þessari línu.  
    * Næsta lína, með  **stað**  í  **reitnum Tegund**  aðgerðar, sýnir hvar verður að setja vörurnar í vöruhúsinu. Ef mikið af vörum er fengið í einni móttökulínu gæti þurft að ganga frá vörunum í nokkrum hólfum svo það sé sæti lína fyrir hvert hólf. 

    > [!NOTE]
    > Ef setja þarf vörur einnar línu í fleiri en eitt hólf, til dæmis þar sem merkt er við fullt, er aðgerðin Skipta Línuaðgerð  **á**  fastflipanum línur  **notaðar** . Aðgerðin býr til línu fyrir eftirstandandi magn sem á að afgreiða.

5. Þegar allar vörurnar hafa verið settar í hólf samkvæmt skal velja aðgerðina **Skrá frágang**.  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft þjálfun](/training/modules/receive-put-away-items/)

## <a name="see-also"></a><a name="see-also"></a>Sjá einnig .

[Yfirlit](design-details-warehouse-management.md)
[vöruhúsakerstjórnunar birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
