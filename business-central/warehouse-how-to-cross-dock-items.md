---
title: Hjáskipa vörur
description: Lærðu að taka á móti og senda vörur án þess að setja þær í geymslu.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 03/08/2023
ms.custom: bap-template
ms.search.form: '15, 5703, 7302, 7332, 5768'
---
# <a name="cross-dock-items"></a>Hjáskipa vörur

Hjáskipunarvörur eru vörur sem þú færð án þess að leggja þær frá þér. Frágangs-og tínsluferlar krefjast takmarkaðrar meðhöndlunar á vörum. Hægt er að hjáskipunarvörur fyrir sendingar og framleiðslupantanir.

## <a name="cross-dock-bins-and-zones"></a>Hjáskipunarhólf og svæði

Ef hólf eru notuð skal setja upp að minnsta kosti eitt hjáskipunarhólf og tilgreina hólfið í  **reitnum Hjáskipunarhólfkóti**  á birgðageymslum. Setja skal upp hjáskipunarsvæði ef notaður er beinn frágangur og tínsla.

Þegar afhending eða tínsla vara er undirbúin og hólf eru notuð er varan sjálfkrafa tekin úr hjáskipunarhólfi en í öðru hólfi. Leita þarf á hjáskipunarsvæðinu til að sjá hvort þau atriði sem þörf er á eru til staðar þar áður en vörurnar eru veittar á venjulegu geymslusvæði þeirra.  

Ef magn magns af hjáskipunarlínum hefur verið reiknað út eru frágangslínur í hjáskipunarhólfi stofnaðar þegar móttakan er bókuð. Aðrar frágangslínur eru stofnaðar eins og venjulega.  

## <a name="cross-dock-select-lines-for-a-receipt"></a>Hjáskipunarlínur fyrir kvittun

Ef bóka skal hjáskipunarvörurnar strax þannig að þær séu tiltækar í tínslu þarf einnig að skrá frágang á hinum vörunum úr móttökulínunum, þ.e. þeim sem þarf að geyma. Ef aðeins sumum vörur á móttökulínu er hjáskipað þarf því að gæta að því að gengið sé frá öðrum vörum eins fljótt og hægt er. Einnig gæti það verið stefna vöruhússins að heilum móttökulínum sé hjáskipað þegar það er hægt.

Í frágangsleiðbeiningunum skal eyða taka og setja inn leiðbeiningalínur fyrir hverja móttökulínu fyrir vörurnar sem á að ganga frá. Hægt er að endurgera leiðbeiningalínur síðar sem frágangslínur frá vinnublaði frágangs eða bókuðu móttökunni. Þegar búið er að eyða leiðbeiningalínunum er hægt að ganga frá og skrá línurnar fyrir hjáskipunarvörur.  

## <a name="about-the-put-away-worksheet-page"></a>Um vinnublað frágangs

Ef kveikt er á  **vinnublaði**  notkunar frágangs á  **birgðageymsluspjaldinu**  og Móttaka með útreiknaðri hjáskipunarsíðu verður tiltæk verða allar móttökulínur tiltækar á vinnublaðinu. Upplýsingar um hjáhöfnina tapast og þær má ekki afþakka. Þess vegna ætti að nota hjáskipunaraðgerðir til að setja línur á frágangsvinnublaðið með því að eyða frágangsfyrirmælum frekar en að nota sjálfvirka Relay-aðgerðina sem lögð er til í  **reitnum nota frágangssniðmát** .  

Ef vöruhúsamóttakan er bókuð og  **slökkt er á Skiptiblaði fyrir notkun vinnublaðs**  eru hjáskipunarvörurnar aðskildar línur í frágangsleiðbeiningunum. Í  **reitnum Hjáskipunarupplýsingar**  í hverri frágangslínu kemur fram hvort í línunni er eftirfarandi:

* Hjáskipunarvörur.
* Allar vörur úr kvittun þarf að geyma.
* Nokkur atriði úr kvittun þarf að geyma og sum eiga að vera hjáskipunarvara.

[!INCLUDE [prod_short](includes/prod_short.md)] heldur ekki aðskildum færslum fyrir hjáskipunarvörur. Hann skráir þá sem venjulegan frágang frágangsfyrirmæla.  

## <a name="to-set-up-the-warehouse-for-cross-docking"></a>Vöruhúsið sett upp fyrir hjáskipun

1. Ef hólf eru notuð skal setja upp að minnsta kosti eitt hjáskipunarhólf. Setja skal upp hjáskipunarsvæði ef notaður er beinn frágangur og tínsla.  

    Hjáskipunarhólf er með reitinn **Hjáskipunarhólf** valinn og verður að hafa bæði hólfategundirnar **Móttaka** og **Tína** valdar. Frekari upplýsingar um hólfin er að fá með því að  [stofna hólf](warehouse-how-to-create-individual-bins.md)  og  [Setja upp hólfagerðir](warehouse-how-to-set-up-bin-types.md).  

    Ef svæði eru notuð skal stofna svæði fyrir hjáskipunarhólfin og velja reitinn **Svæði hjáskipunarhólfs**. Til að fræðast meira um svæði er farið í  [Setja upp staðsetningar til að nota hólf](warehouse-how-to-set-up-locations-to-use-bins.md).  

2. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Staðsetningu** og velja síðan viðkomandi tengil.  
3. Á síðunni **Birgðageymsla** er valin birgðageymsla þar sem á að setja upp vöruhús fyrir hjáskipun og svo velja **Breyta** aðgerðin.  
4.  **Á flipanum Vöruhús**  er kveikt á  **notkun milli**  skipta og fyllt út í  **hjáskipun skiladags Calc.**  svæðið með tímann til að leita að hjáskipunartækifærum.

    Valkosturinn **Nota hjáskipun** er aðeins tiltækur ef reitirnir **Krefjast móttöku**, **Krefjast afhendingar**, **Krefjast tínslu** og **Krefjast frágangs** eru valdir.  

5. Ef hólf eru notuð, á  **fastflipanum hólf**, er reiturinn Kóti hjáskipunarhólfs  **fylltur út**  með kóta hólfsins sem á að nota sem sjálfgefið hjáskipunarhólf.  
6. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Birgðahaldseiningu** og velja viðkomandi tengil.  
7. Fyrir hverja vöru eða birgðahaldseiningu sem óskað er eftir að geta hjáskipað, skal velja vöru og síðan skal velja aðgerðina **Breyta**.
8. Á síðunni **birgðahaldseining** veljið **Nota hjáskipun** gátreitur.  

> [!NOTE]  
>  Hjáskipun er eingöngu möguleg ef birgðageymslan er sett þannig upp að hún krefjist vöruhúsamóttöku- og frágangsvinnslu.  

## <a name="to-cross-dock-items-without-viewing-the-opportunities"></a>Vörum hjáskipað án þess að skoða tækifærin:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vöruhúsamóttökur** og velja síðan viðkomandi tengil.  
2. Vöruhúsamóttaka er stofnuð fyrir vöru sem er komin og hægt er að hjáskipa. Til að fræðast meira um móttöku er farið í að taka á  [móti vörum](warehouse-how-receive-items.md).  
3. Fyllið út í reitinn **Magn til móttöku** og veljið svo aðgerðina **Reikna hjáskipun**.  

    Upprunaskjöl fyrir úthreyfingar sem þarfnast varanna sem eiga að fara úr vöruhúsinu innan tímabils dagsetningarreglunnar eru skilgreind. [!INCLUDE[prod_short](includes/prod_short.md)] reiknar magn þannig að hjáskipa megi eins miklu og mögulegt til að forðast að ganga frá vörum og safna upp of mörgum vörum á hjáskipunarsvæði. Gildið í  **reitnum Magn til hjáskipunar**  er Samtala allra lína sem eru á útleið fyrir vöruna innan sama tímabils að frádregnu magninu sem þegar hefur verið sett í hjáskipunarsvæðið eða er gildið í  **reitnum Magn til móttöku**  á móttökulínunni, hvort sem er minni. Þú getur ekki hjáhliað meira en þú hefur fengið.  

4. Til að hjáskipunarmagnið sem lagt er til skal bóka móttökunina. Einnig er hægt að breyta magninu sem á að hjáskipa í hærra eða lægra gildi og bóka síðan móttökuna.  

    Magnið sem á að hjáskipa birtist nú sem línur í frágangsleiðbeiningunum að því gefnu að reiturinn **Nota vinnublað frágangs** sé auður. Magnið sem ekki á að hjáskipa kemur einnig í línum í frágangsleiðbeiningunum.  

    Ef hólf eru notuð hefur kerfið úthlutað hjáskipunarvörunum á sjálfgefna hjáskipunarhólfið sem skilgreint er á birgðageymsluspjaldinu.  

5. Eyða taka  **og**  setja línur fyrir vörur sem ekki eru  **hjáskipunarsett** .  
6. Frágangsleiðbeiningarnar með línunum sem eftir eru eru prentaðar út og móttökumagnið sem þarf að geyma sett í viðeigandi hólf eða svæði í vöruhúsinu. Hjáskipunarvaran er sett á svæðið eða í hólfið sem tilgreint er í vöruhúsareglum. Stundum segja vöruhúsareglur til um að það eigi að skilja þær eftir á móttökusvæðinu.  
7. Til að skrá það að hjáskipunarvörurnar séu frágengnar og tiltækar til tínslu, skal velja **Skráning** aðgerðina.  

## <a name="to-cross-dock-items-after-viewing-the-opportunities"></a>Vörur hjáskipaðar eftir að tækifæri hafa verið skoðuð:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vöruhúsamóttökur** og velja síðan viðkomandi tengil.  
2. Vöruhúsamóttaka er stofnuð fyrir vöru sem er komin og hægt er að hjáskipa.  

    Æskilegt er að skoða línur í upprunaskjalinu sem kalla eftir vörunni áður en móttakan er bókuð.  
3. Veldu aðgerðina **Reikna út Hjáskipun**.  

   Á síðunni **Hjáskipunarvalmöguleikar** er hægt að sjá mikilvægustu upplýsingarnar um línurnar þar sem beðið er um vöruna, eins og gerð fylgiskjals, umbeðið magn og gjalddaga. Þessar upplýsingar koma að gagni við að ákveða hve miklu á að hjáskipa, hvar setja eigi vörurnar á hjáskipunarsvæðinu eða hvernig eigi að flokka þær.  

4. Veljið  **autofill magn til að hjáskipunaraðgerð**  til að sýna hvernig magnið í móttökulínum er reiknað. Þegar fjölda vara er breytt í  **reitnum Magn til hjáskipunar í hverri línu eru uppfærslur útreikninganna** . Uppfærslan þýðir ekki að afhendingin eða framleiðslupöntunin fái þær vörur sem lagðar eru til fyrir hjáskipun. Þetta á eingöngu við um prófmálefni. Ferlið getur þó verið fræðandi ef fleiri en ein mælieining koma við sögu.  
5. Til að taka frá magn af vörunni fyrir pöntunarlínu er línan valin og síðan er  **valin varaaðgerðin** .  **Á frátekningarsíðunni**, skal taka frá tiltækt magn af vörunni. Úttektin er eins og önnur frátekt og hefur ekki hærri forgang því hún var stofnuð í tengslum við hjáskipun. Til að fá frekari upplýsingar um frátekningar er farið í  [frátektir vörur](inventory-how-to-reserve-items.md).   
6. Þegar lokið er við að endurreikna eða taka frá að nýju skal velja  **OK**  hnappinn til að koma útreikningi  **á reitinn Magn til hjáskipunar**  á móttökulínunni eða  **hnappinn hætta**  við til að fara aftur í vöruhúsamóttakið og reikna hjáhöfnina aftur.  
7. Móttakan er bókuð. Hægt er að halda áfram í frágangsleiðbeiningunum eins og lýst er í skrefum 3 til 7 í  [hjáskipunarvörum án þess að skoða tækifærin](#to-cross-dock-items-without-viewing-the-opportunities).  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

    > [!NOTE]  
    > Í vöruhúsafrágangi er hægt að halda áfram að breyta magninu sem gengið er frá í geymslu eða hjáskipað eftir þörfum. Til dæmis er hægt að hjáskipa viðbótarmagni til að flýta hjáskipunarskráningunni.  

## <a name="to-view-cross-docked-items-in-a-shipment-or-pick-worksheet"></a>Hjáskipunarvörur skoðaðar í afhendingum eða tínsluvinnublaði

Ef hólf eru notuð þegar sending er opnuð eða tínslublað er magn hverrar vöru í uppfærslum á hjáskipunarhólfum. Þegar varan er tiltæk í hjáskipunarhólfinu er hægt að stofna tínslu fyrir vörurnar í afhendingunni. Á tínsluvinnublaðinu er hægt að breyta línunum eftir þörfum.  

Þegar framleiðslupöntun er gefin út eru línurnar tiltækar á vinnublaði tínsluna og  **í reitnum Magn í hjáskipunarhólfi**  sést hvort vörurnar hafa borist og eru í hjáskipunarhólfum. Þegar tínsluleiðbeiningar eru stofnaðar er  [!INCLUDE [prod_short](includes/prod_short.md)]  stungið upp á því að velja hjáskipunarvörurnar fyrst. Vörur í geymsluhólfum eru lagðar eftirá.  

Ef hólf eru ekki notuð þarf að muna að leita að hjáskipunarsvæðinu frá tíma til þess eða treysta á að tilkynningar frá innhreyfingar að vörum í framleiðslu séu komnar.  

## <a name="see-also"></a>Sjá einnig

[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
[Samsetningardeild](assembly-assemble-items.md)    
[Yfirlit yfir](design-details-warehouse-management.md)
[vöruhúsastjórnun vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
