---
title: Hjáskipa vörur
description: Læra hvernig á að taka á móti og senda vörur án þess að setja þær í geymslu.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 10/09/2023
ms.custom: bap-template
ms.search.form: '15, 5703, 7302, 7332, 5768'
---
# <a name="cross-dock-items"></a>Hjáskipa vörur

Hjáskipunarvörur eru vörur sem tekið er á móti og sendar án þess að gengið sé frá þeim. Frágangs- og tínsluferli krefjast takmarkaðrar meðhöndlunar á vörum. Hægt er að hjáskipa vörum í afhendingum og framleiðslupöntunum.

## <a name="cross-dock-bins-and-zones"></a>Hjáskipunarhólf og svæði

Ef hólf eru notuð skal setja upp að minnsta kosti eitt hjáskipunarhólf og tilgreina síðan hólfið í reitnum **Kóti** hjáskipunarhólfs í birgðageymslunum. Ef notaður er beinn frágangur og tínsla skal setja upp hjáskipunarsvæði.

Þegar afhending er undirbúin eða vörur tíndar fyrir framleiðslu og hólf eru notuð er varan sjálfkrafa tínd úr hjáskipunarhólfi á undan einhverju öðru hólfi. Skoða þarf hjáskipunarsvæðið til að athuga hvort vörurnar sem þörf er á séu tiltækar áður en vörurnar eru sýndar í venjulegum geymslusvæði.  

Hafi hjáskipunarmagn verið reiknað eru frágangslínur í hjáskipunarhólfið stofnaðar fyrir hjáskipunarútreikninga þegar móttakan er bókuð. Aðrar frágangslínur eru stofnaðar eins og venjulega.  

## <a name="cross-dock-select-lines-for-a-receipt"></a>Hjáskipun velur línur fyrir kvittun

Ef bóka skal hjáskipunarvörurnar strax þannig að þær séu tiltækar í tínslu þarf einnig að skrá frágang á hinum vörunum úr móttökulínunum, þ.e. þeim sem þarf að geyma. Ef aðeins sumum vörur á móttökulínu er hjáskipað þarf því að gæta að því að gengið sé frá öðrum vörum eins fljótt og hægt er. Einnig gæti það verið stefna vöruhússins að heilum móttökulínum sé hjáskipað þegar það er hægt.

Í frágangsleiðbeiningunum skal eyða Taka- og Setja-leiðbeiningalínum fyrir hverja móttökulínu fyrir vörurnar sem ganga skal frá. Hægt er að endurstofna leiðbeiningalínurnar síðar sem frágangslínur af frágangsvinnublaðinu eða bókuðu móttökunni. Þegar leiðbeiningalínunum hefur verið eytt er hægt að ganga frá og skrá línurnar fyrir hjáskipunarvörur.  

## <a name="about-the-put-away-worksheet-page"></a>Um síðuna Vinnublað frágangs

Ef kveikt er á víxlverksmiðjunni **Nota vinnublað** frágangs á **síðunni Birgðageymsluspjald** og móttakan bókuð með reiknuðum hjáskipunum verða allar móttökulínur tiltækar á vinnublaðinu. Upplýsingar um hjáskipun glatast og ekki er hægt að endurskipa þær. Ef nota á hjáskipunaraðgerðir ætti því að senda línur á frágangsvinnublaðið með því að eyða frágangsleiðbeiningum í stað þess að nota sjálfvirku aðgerðina sem fylgir í reitnum **Nota vinnublað** frágangs.  

Ef vöruhúsamóttakan er bókuð og **slökkt er á víxlunni Nota vinnublað** frágangs verða hjáskipunarvörurnar aðskildar línur í frágangsleiðbeiningunum. Í **reitnum Hjáskipunarupplýsingar** í hverri frágangslínu sést hvort í línunni er eftirfarandi:

* Hjáskipunarvörur.
* Geyma verður allar vörur úr móttöku.
* Geyma verður sumar vörur úr móttöku og hjáskipa þarf sumum.

[!INCLUDE [prod_short](includes/prod_short.md)] heldur ekki aðskildar færslur fyrir hjáskipunarvörur. Hún skráir þær sem venjulegar frágangsleiðbeiningar.  

## <a name="to-set-up-the-warehouse-for-cross-docking"></a>Vöruhúsið sett upp fyrir hjáskipun

1. Ef hólf eru notuð skal setja upp að minnsta kosti eitt hjáskipunarhólf. Ef notaður er beinn frágangur og tínsla skal setja upp hjáskipunarsvæði.  

    Hjáskipunarhólf er með reitinn **Hjáskipunarhólf** valinn og verður að hafa bæði hólfategundirnar **Móttaka** og **Tína** valdar. Nánari upplýsingar um hólf eru notaðar með því að [fara í Stofna hólf](warehouse-how-to-create-individual-bins.md) og [setja upp hólfategundir](warehouse-how-to-set-up-bin-types.md).  

    Ef svæði eru notuð skal stofna svæði fyrir hjáskipunarhólfin og velja reitinn **Svæði hjáskipunarhólfs**. Nánari upplýsingar um svæði eru í [Setja upp birgðageymslur til að nota hólf](warehouse-how-to-set-up-locations-to-use-bins.md).  

2. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Staðsetningu** og velja síðan viðkomandi tengil.  
3. Á síðunni **Birgðageymsla** er valin birgðageymsla þar sem á að setja upp vöruhús fyrir hjáskipun og svo velja **Breyta** aðgerðin.  
4. Á flýtiflipanum **Vöruhús** skal kveikja á vífæra **hjáskipun og fylla út** reikn. hjáskipunardags **.** með tímanum þegar leitað er að hjáskipunarmöguleikum.

    Valkosturinn **Nota hjáskipun** er aðeins tiltækur ef valdir eru reitirnir **Krefjast móttöku**, **Krefjast afhendingar**, **Krefjast tínslu** og **Krefjast frágangs** .  

5. Ef hólf eru notuð er á flýtiflipanum **Hólf** fyllt út í **reitinn Hjáskipunarhólfskóti** með kóta hólfsins sem á að nota sem sjálfgefið hjáskipunarhólf.  
6. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Birgðahaldseiningu** og velja viðkomandi tengil.  
7. Fyrir hverja vöru eða birgðahaldseiningu sem óskað er eftir að geta hjáskipað, skal velja vöru og síðan skal velja aðgerðina **Breyta**.
8. Á síðunni **birgðahaldseining** veljið **Nota hjáskipun** gátreitur.  

> [!NOTE]  
>  Hjáskipun er eingöngu möguleg ef birgðageymslan er sett þannig upp að hún krefjist vöruhúsamóttöku- og frágangsvinnslu.  

## <a name="to-cross-dock-items-without-viewing-the-opportunities"></a>Vörum hjáskipað án þess að skoða tækifærin:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vöruhúsamóttökur** og velja síðan viðkomandi tengil.  
2. Stofna vöruhúsamóttöku fyrir vöru sem er komin og hægt er að hjáskipa. Nánari upplýsingar um móttöku fást með því að fara á [Mótteknar vörur](warehouse-how-receive-items.md).  
3. Fyllið út í reitinn **Magn til móttöku** og veljið svo aðgerðina **Reikna hjáskipun**.  

    Upprunaskjöl fyrir úthreyfingar sem þarfnast varanna sem eiga að fara úr vöruhúsinu innan tímabils dagsetningarreglunnar eru skilgreind. [!INCLUDE[prod_short](includes/prod_short.md)] reiknar magn þannig að hjáskipa megi eins miklu og mögulegt til að forðast að ganga frá vörum og safna upp of mörgum vörum á hjáskipunarsvæði. Gildið í reitnum **Magn til hjáskipunar** er samtala allra útleiðarlína fyrir vöruna innan leitartímabilsins að frádregnu magninu sem þegar hefur verið sett á hjáskipunarsvæðið eða það er gildið í reitnum **Magn til móttöku** á móttökulínunni, hvort sem er minna. Ekki er hægt að hjáskipa meira en móttekið hefur verið.  

4. Móttakan er bókuð til að hjáskipa magninu sem lagt er til. Einnig er hægt að breyta magninu sem á að hjáskipa í hærra eða lægra gildi og bóka síðan móttökuna.  

    Magnið sem á að hjáskipa birtist nú sem línur í frágangsleiðbeiningunum að því gefnu að reiturinn **Nota vinnublað frágangs** sé auður. Magnið sem ekki á að hjáskipa kemur einnig í línum í frágangsleiðbeiningunum.  

    Ef hólf eru notuð hefur kerfið úthlutað hjáskipunarvörunum á sjálfgefna hjáskipunarhólfið sem skilgreint er á birgðageymsluspjaldinu.  

5. Eyða skal **Taka-** og **Setja-línunum** fyrir vörur sem ekki á að hjáskipa.  
6. Frágangsleiðbeiningarnar með línunum sem eftir eru eru prentaðar út og móttökumagnið sem þarf að geyma sett í viðeigandi hólf eða svæði í vöruhúsinu. Hjáskipunarvaran er sett á svæðið eða í hólfið sem tilgreint er í vöruhúsareglum. Stundum segja vöruhúsareglur til um að það eigi að skilja þær eftir á móttökusvæðinu.  
7. Til að skrá það að hjáskipunarvörurnar séu frágengnar og tiltækar til tínslu, skal velja **Skráning** aðgerðina.  

## <a name="to-cross-dock-items-after-viewing-the-opportunities"></a>Vörur hjáskipaðar eftir að tækifæri hafa verið skoðuð:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vöruhúsamóttökur** og velja síðan viðkomandi tengil.  
2. Stofna vöruhúsamóttöku fyrir vöru sem er komin og hægt er að hjáskipa.  

    Æskilegt er að skoða línur í upprunaskjalinu sem kalla eftir vörunni áður en móttakan er bókuð.  
3. Veldu aðgerðina **Reikna út Hjáskipun**.  

   Á síðunni **Hjáskipunarvalmöguleikar** er hægt að sjá mikilvægustu upplýsingarnar um línurnar þar sem beðið er um vöruna, eins og gerð fylgiskjals, umbeðið magn og gjalddaga. Þessar upplýsingar koma að gagni við að ákveða hve miklu á að hjáskipa, hvar setja eigi vörurnar á hjáskipunarsvæðinu eða hvernig eigi að flokka þær.  

4. Veljið **Sjálfg. magn til hjáskipunar** aðgerðar til að sýna hvernig magnið í móttökulínunum er reiknað. Þegar vörufjölda er breytt í reitnum **Magn til hjáskipunar** í hverri línu uppfærist útreikningurinn. Uppfærslan þýðir ekki að afhendingarnar eða framleiðslupöntunin fái í raun vörurnar sem lagt er til að verði hjáskipað. Ūađ er til prķfunar eingöngu til prķfunar. Ferlið getur þó verið fræðandi ef fleiri en ein mælieining koma við sögu.  
5. Til að taka frá magn af vörunni fyrir pöntunarlínu skal velja línuna og velja svo aðgerðina **Taka frá** . Á síðunni **Frátekning** skal taka frá tiltækt magn af vörunni. Frátekningin er eins og aðrar frátektir og hefur ekki meiri forgang vegna þess að hún var stofnuð í tengslum við hjáskipun. Nánari upplýsingar um frátekningar fást með því að fara í [Taka frá vörur](inventory-how-to-reserve-items.md).   
6. Þegar lokið er við að endurreikna eða taka frá skal velja **Í lagi** hnappinn til að færa útreikningana **í reitinn Magn til hjáskipunar** á móttökulínunni eða velja **hnappinn Hætta við** til að fara aftur í vöruhúsamóttökuna og reikna hjáskipunina aftur.  
7. Móttakan er bókuð. Hægt er að halda áfram í frágangsleiðbeiningunum eins og lýst er í þrepum 3 til 7 í [Til að hjáskipa vörum án þess að skoða tækifærin](#to-cross-dock-items-without-viewing-the-opportunities).  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

    > [!NOTE]  
    > Í vöruhúsafrágangi er hægt að halda áfram að breyta magninu sem gengið er frá í geymslu eða hjáskipað eftir þörfum. Til dæmis er hægt að hjáskipa viðbótarmagni til að flýta hjáskipunarskráningunni.  

## <a name="to-view-cross-docked-items-in-a-shipment-or-pick-worksheet"></a>Hjáskipunarvörur skoðaðar í afhendingum eða tínsluvinnublaði

Ef hólf eru notuð uppfærist magn hverrar vöru í hjáskipunarhólfunum þegar afhending eða tínsluvinnublað er opnað. Þegar varan er tiltæk í hjáskipunarhólfinu er hægt að stofna tínslu fyrir vörurnar í afhendingunni. Á vinnublaði tínslunnar er hægt að breyta línunum eftir þörfum.  

Þegar framleiðslupöntun er gefin út eru línurnar tiltækar á vinnublaði tínslunnar og í reitnum **Magn í hjáskipunarhólfi** sést hvort vörurnar hafi borist og eru í hjáskipunarhólfum. Þegar tínsluleiðbeiningar [!INCLUDE [prod_short](includes/prod_short.md)]  eru stofnaðar er lagt til að hjáskipunarvörurnar séu tíndar fyrst. Lagt er til vörur í geymsluhólfum síðar.  

Ef hólf eru ekki notuð skal muna að athuga hjáskipunarsvæðið öðru hverju eða treysta á tilkynningar frá móttökum um að vörur fyrir framleiðsluna hafi borist.  

## <a name="see-also"></a>Sjá einnig

[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
[Samsetningardeild](assembly-assemble-items.md)    
[Yfirlitsvinna vöruhúsastjórnunar](design-details-warehouse-management.md)
[með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
