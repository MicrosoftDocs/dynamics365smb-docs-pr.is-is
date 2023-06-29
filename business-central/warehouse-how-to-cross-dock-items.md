---
title: Hjáskipa vörur
description: Hjáskipunaraðgerðin er tiltæk ef birgðageymslan hefur verið sett upp þannig að hún krefjist vöruhúsamóttöku-og frágangsvinnslu.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '15, 5703, 7302, 7332, 5768'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="cross-dock-items"></a><a name="cross-dock-items"></a>Hjáskipa vörur

Hjáskipunarvörur eru vörur sem þú færð án þess að leggja þær frá þér. Frágangs-og tínsluferlar krefjast takmarkaðrar meðhöndlunar á vörum. Hægt er að hjáskipunarvörur fyrir sendingar og framleiðslupantanir.

## <a name="cross-dock-bins-and-zones"></a><a name="cross-dock-bins-and-zones"></a>Hjáskipunarhólf og svæði

Ef hólf eru notuð skal setja upp að minnsta kosti eitt hjáskipunarhólf og tilgreina hólfið í  **reitnum Hjáskipunarhólfkóti**  á birgðageymslum. Setja skal upp hjáskipunarsvæði ef notaður er beinn frágangur og tínsla.

Þegar afhending eða tínsla vara er undirbúin og hólf eru notuð er varan sjálfkrafa tekin úr hjáskipunarhólfi en í öðru hólfi. Leita þarf á hjáskipunarsvæðinu til að sjá hvort þau atriði sem þörf er á eru til staðar þar áður en vörurnar eru veittar á venjulegu geymslusvæði þeirra.  

Ef magn magns af hjáskipunarlínum hefur verið reiknað út eru frágangslínur í hjáskipunarhólfi stofnaðar þegar móttakan er bókuð. Aðrar frágangslínur eru stofnaðar eins og venjulega.  

## <a name="cross-dock-select-lines-for-a-receipt"></a><a name="cross-dock-select-lines-for-a-receipt"></a>Hjáskipunarlínur fyrir kvittun

<!--If a receipt contains items that you want to store, that is, items that you are not cross-docking, you must register a put-away for those items.-->

Ef bóka skal hjáskipunarvörurnar strax þannig að þær séu tiltækar í tínslu þarf einnig að skrá frágang á hinum vörunum úr móttökulínunum, þ.e. þeim sem þarf að geyma. Ef aðeins sumum vörur á móttökulínu er hjáskipað þarf því að gæta að því að gengið sé frá öðrum vörum eins fljótt og hægt er. Einnig gæti það verið stefna vöruhússins að heilum móttökulínum sé hjáskipað þegar það er hægt.

Í frágangsleiðbeiningunum skal eyða taka og setja inn leiðbeiningalínur fyrir hverja móttökulínu fyrir vörurnar sem á að ganga frá. Hægt er að endurgera leiðbeiningalínur síðar sem frágangslínur frá vinnublaði frágangs eða bókuðu móttökunni. Þegar búið er að eyða leiðbeiningalínunum er hægt að ganga frá og skrá línurnar fyrir hjáskipunarvörur.  

## <a name="about-the-put-away-worksheet-page"></a><a name="about-the-put-away-worksheet-page"></a>Um frágang vinnublaðs

Ef kveikt er á vinnublaði  **fyrir**  notaðan frágang á birgðageymsluspjaldinu og móttakan bókuð með útreiknaðri hjáskipunarhlið verða allar móttökulínur tiltækar á vinnublaðinu. Upplýsingar um hjáhöfnina tapast og þær má ekki afþakka. Þess vegna ætti að nota hjáskipunaraðgerðir til að setja línur á frágangsvinnublaðið með því að eyða frágangsfyrirmælum frekar en að nota sjálfvirka Relay-aðgerðina sem lögð er til í  **reitnum nota frágangssniðmát** .  

Ef vöruhúsamóttakan er bókuð og  **slökkt er á Skiptiblaði fyrir notkun vinnublaðs**  eru hjáskipunarvörurnar aðskildar línur í frágangsleiðbeiningunum. Í  **reitnum Hjáskipunarupplýsingar**  í hverri frágangslínu kemur fram hvort í línunni er eftirfarandi:

* Hjáskipunarvörur.
* Allar vörur úr kvittun þarf að geyma.
* Nokkur atriði úr kvittun þarf að geyma og sum eiga að vera hjáskipunarvara.

Starfsmenn geta auðveldlega skilið hvers vegna allt magnið er ekki sett í geymslu.  

[!INCLUDE [prod_short](includes/prod_short.md)] heldur ekki aðskildum færslum fyrir hjáskipunarvörur en skráir þær sem venjulegan frágangsleiðbeiningar.  

## <a name="to-set-up-the-warehouse-for-cross-docking"></a><a name="to-set-up-the-warehouse-for-cross-docking"></a>Vöruhúsið sett upp fyrir hjáskipun

1. Ef hólf eru notuð skal setja upp að minnsta kosti eitt hjáskipunarhólf. Setja skal upp hjáskipunarsvæði ef notaður er beinn frágangur og tínsla.  

    Hjáskipunarhólf er með reitinn **Hjáskipunarhólf** valinn og verður að hafa bæði hólfategundirnar **Móttaka** og **Tína** valdar. Nánari upplýsingar er að finna í [Setja upp hólf](warehouse-how-to-create-individual-bins.md) og [Setja upp hólfategundir](warehouse-how-to-set-up-bin-types.md).  

    Ef svæði eru notuð skal stofna svæði fyrir hjáskipunarhólfin og velja reitinn **Svæði hjáskipunarhólfs**. Nánari upplýsingar er að finna í [Setja upp birgðageymslur til að þær noti hólf](warehouse-how-to-set-up-locations-to-use-bins.md).  

2. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Staðsetningu** og velja síðan viðkomandi tengil.  
3. Á síðunni **Birgðageymsla** er valin birgðageymsla þar sem á að setja upp vöruhús fyrir hjáskipun og svo velja **Breyta** aðgerðin.  
4.  **Á flipanum Vöruhús**  er kveikt á  **notkun milli**  skipta og fyllt út í  **hjáskipun skiladags Calc.**  svæðið með tímann til að leita að hjáskipunartækifærum.

    Valkosturinn **Nota hjáskipun** er aðeins tiltækur ef reitirnir **Krefjast móttöku**, **Krefjast afhendingar**, **Krefjast tínslu** og **Krefjast frágangs** eru valdir.  

5.  Ef hólf eru notuð er á flýtiflipanum **Hólf** færður inn kóti hólfsins sem nota á sem sjálfgefið hjáskipunarhólf í reitinn **Kóti hjáskipunarhólfs**.  
6.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Birgðahaldseiningu** og velja viðkomandi tengil.  
7.  Fyrir hverja vöru eða birgðahaldseiningu sem óskað er eftir að geta hjáskipað, skal velja vöru og síðan skal velja aðgerðina **Breyta**.
8. Á síðunni **birgðahaldseining** veljið **Nota hjáskipun** gátreitur.  

> [!NOTE]  
>  Hjáskipun er eingöngu möguleg ef birgðageymslan er sett þannig upp að hún krefjist vöruhúsamóttöku- og frágangsvinnslu.  

## <a name="to-cross-dock-items-without-viewing-the-opportunities"></a><a name="to-cross-dock-items-without-viewing-the-opportunities"></a>Vörum hjáskipað án þess að skoða tækifærin:
1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vöruhúsamóttökur** og velja síðan viðkomandi tengil.  
2.  Stofna vöruhúsamóttöku fyrir vöru sem hefur borist og er til dæmis hægt að hjáskipa. Frekari upplýsingar eru í [Móttaka vara](warehouse-how-receive-items.md).  
3.  Fyllið út í reitinn **Magn til móttöku** og veljið svo aðgerðina **Reikna hjáskipun**.  

    Upprunaskjöl fyrir úthreyfingar sem þarfnast varanna sem eiga að fara úr vöruhúsinu innan tímabils dagsetningarreglunnar eru skilgreind.  [!INCLUDE[prod_short](includes/prod_short.md)] reiknar magn þannig að hjáskipa megi eins miklu og mögulegt til að forðast að ganga frá vörum og safna upp of mörgum vörum á hjáskipunarsvæði. Gildið í reitnum **Magn til hjáskipunar** er því samtala allra útleiðalína sem þarfnast vörunnar innan leitartímabilsins að frádregnu magninu, sem þegar hefur verið sett á hjáskipunarsvæðið, eða gildið í reitnum **Magn til móttöku** á móttökulínunni, eftir því hvort er minna. Ekki er hægt að hjáskipa meira magni en móttekið hefur verið.  

4.  Ef hjáskipa á magninu sem lagt er til er móttakan bókuð. Einnig er hægt að breyta magninu sem á að hjáskipa í hærra eða lægra gildi og bóka síðan móttökuna.  

    Magnið sem á að hjáskipa birtist nú sem línur í frágangsleiðbeiningunum að því gefnu að reiturinn **Nota vinnublað frágangs** sé auður. Magnið sem ekki á að hjáskipa kemur einnig í línum í frágangsleiðbeiningunum.  

    Ef hólf eru notuð hefur kerfið úthlutað hjáskipunarvörunum á sjálfgefna hjáskipunarhólfið sem skilgreint er á birgðageymsluspjaldinu.  

5.  Eyða skal **Taka-** og **Setja-** línum fyrir vörur sem ekki á að hjáskipa.  
6.  Frágangsleiðbeiningarnar með línunum sem eftir eru eru prentaðar út og móttökumagnið sem þarf að geyma sett í viðeigandi hólf eða svæði í vöruhúsinu. Hjáskipunarvaran er sett á svæðið eða í hólfið sem tilgreint er í vöruhúsareglum. Stundum segja vöruhúsareglur til um að það eigi að skilja þær eftir á móttökusvæðinu.  
7.  Til að skrá það að hjáskipunarvörurnar séu frágengnar og tiltækar til tínslu, skal velja **Skráning** aðgerðina.  

## <a name="to-cross-dock-items-after-viewing-the-opportunities"></a><a name="to-cross-dock-items-after-viewing-the-opportunities"></a>Vörur hjáskipaðar eftir að tækifæri hafa verið skoðuð:
1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vöruhúsamóttökur** og velja síðan viðkomandi tengil.  
2.  Stofna vöruhúsamóttöku fyrir vöru sem hefur borist og er til dæmis hægt að hjáskipa. Frekari upplýsingar eru í [Móttaka vara](warehouse-how-receive-items.md).  

    Æskilegt er að skoða línur í upprunaskjalinu sem kalla eftir vörunni áður en móttakan er bókuð.  
3.  Veldu aðgerðina **Reikna út Hjáskipun**.  

    Á síðunni **Hjáskipunarvalmöguleikar** er hægt að sjá mikilvægustu upplýsingarnar um línurnar þar sem beðið er um vöruna, eins og gerð fylgiskjals, umbeðið magn og gjalddaga. Þessar upplýsingar koma að gagni við að ákveða hve miklu á að hjáskipa, hvar setja eigi vörurnar á hjáskipunarsvæðinu eða hvernig eigi að flokka þær.  

4.  Veljið **Sjálfvirk útfylling magns til hjáskipunar** aðgerðina til að sjá hvernig magnið á móttökulínunum er reiknað. Þegar fjölda vara er breytt í reitnum **Magn til hjáskipunar** í hverri línu eru útreikningarnir uppfærðir eftir því sem breytingar eru gerðar. Það þýðir ekki að tiltekin afhending eða framleiðslupöntun fái í raun vörurnar sem lagt er til að verði hjáskipað þar sem þessar tilfæringar eru aðeins í tilraunaskyni. Ferlið getur þó verið fræðandi ef fleiri en ein mælieining koma við sögu.  
5.  Ef taka á hluta af vörunum frá fyrir tiltekna pöntunarlínu er bendillinn settur í þá línu og í reitnum og síðan er valin aðgerðin **aka frá**. Á síðunni **Frátekning** er nú hægt að taka frá allt tiltækt magn vörunnar fyrir þessa tilteknu pöntun. Þessi frátekt er eins og aðrar frátektir og hefur ekki meiri forgang vegna þess að hún var stofnuð í tengslum við hjáskipun. Nánari upplýsingar, sjá [Taka frá vörur](inventory-how-to-reserve-items.md).   
6.  Þegar lokið hefur verið við endurútreikninga eða frátektir er smellt á **Í lagi** til að flytja breyttu útreikningana í reitinn **Magn til hjáskipunar** á móttökulínunni eða smellt á **Hætta við** ef fara á aftur í vöruhúsamóttökuna þar sem hægt er að reikna hjáskipunina aftur ef vill.  
7.  Nú er móttakan bókuð og þá er hægt að halda áfram með frágangsleiðbeiningarnar eins og lýst er í skrefum 3 til 7 í hlutanum „Vörur hjáskipaðar án þess að skoða tækifærin.".  

> [!NOTE]  
>  Í vöruhúsafrágangi er hægt að halda áfram að breyta magninu sem gengið er frá í geymslu eða hjáskipað eftir þörfum. Til dæmis er hægt að hjáskipa viðbótarmagni til að flýta hjáskipunarskráningunni.  

## <a name="to-view-cross-docked-items-in-a-shipment-or-pick-worksheet"></a><a name="to-view-cross-docked-items-in-a-shipment-or-pick-worksheet"></a>Hjáskipunarvörur skoðaðar í afhendingum eða tínsluvinnublaði
Ef hólf eru notuð er hægt að sjá uppfærða útreikninga á magni hverrar vöru í hjáskipunarhólfi í hvert sinn sem afhending eða tínsluvinnublað er opnað. Þetta eru dýrmætar upplýsingar ef beðið er eftir því að varan komi inn. Þegar það sést að varan er tiltæk í hjáskipunarhólfinu er fljótlegt að stofna tínslu fyrir allar vörurnar í afhendingunni. Á vinnublaði tínslunnar er hægt að breyta þessum línum eins og við á og síðan stofna tínslu.  

Fyrst þarf að leita að vörum á hjáskipunarsvæðinu þegar vörur eru tíndar fyrir afhendingu. Hafi upprunaskjölin sem hjáskipun var byggð á verið skrifuð niður meðan á móttöku stóð hefur notandinn betri hugmynd um það hvort vöruna er að finna á hjáskipunarsvæðinu eða ekki.  

Þegar framleiðslupöntun hefur verið gefin út eru línurnar tiltækar á vinnublaði tínslunnar og í reitnum **Magn í hjáskipunarhólfi** sést hvort vörurnar sem beðið er eftir hafi borist og þær verið settar í hjáskipunarhólf. Þegar tínsluleiðbeiningar eru stofnaðar leggur forritið til að fyrst séu hjáskipunarvörur tíndar og aðeins eftir það verður leitað að vörum í geymsluhólfum.  

Ef hólf eru ekki notuð skal hafa hugfast að athuga hjáskipunarsvæðið annað veifið eða treysta á tilkynningar frá móttöku um það að vörur fyrir framleiðsluna hafi borist.  

## <a name="see-also"></a><a name="see-also"></a>Sjá einnig
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
[Samsetningardeild](assembly-assemble-items.md)    
[Yfirlit yfir](design-details-warehouse-management.md)
[vöruhúsastjórnun vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
