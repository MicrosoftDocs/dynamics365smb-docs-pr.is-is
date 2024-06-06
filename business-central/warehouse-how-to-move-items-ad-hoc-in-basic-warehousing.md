---
title: Færa vörur óáætlaðar í einfaldri vöruhúsagrunnstillingu
description: Þessi grein útskýrir óáætlaðar innanhússhreyfingar milli hólfa án eftirspurnar úr upprunaskjali.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 12/16/2022
ms.custom: bap-template
ms.search.form: '393, 7382'
---
# <a name="move-items-internally-in-basic-warehouse-configurations"></a>Færa vörur innri vinnslu í einfaldri vöruhúsagrunnstillingu

Hugsanlega þarf að færa vörur milli hólfa án eftirspurnar úr upprunaskjali. Til dæmis sem hluta af eftirfarandi aðgerðum:

* Endurskipuleggja vöruhúsið.
* Koma vörum á eftirlitssvæði.
* Flytja aukavörur til og frá framleiðslusvæði. 

Hvernig vörur eru færðar veltur á því hvernig vöruhúsið er sett upp sem birgðageymsla. Nánari upplýsingar um [uppsetningu vöruhúsastjórnunar](warehouse-setup-warehouse.md).

Í vöruhúsagrunnstillingum þar sem **kveikt er á uppsetningaráskildum** hólfum en ekki **beinum tínslu og frágangi** er hægt að skrá óáætlaðar hreyfingar á eftirfarandi síðum:  

* Á síðunni **Innri hreyfing** .
* Á síðunni **Endurflokkunarbók** birgða.  

## <a name="internal-movements"></a>Innri hreyfingar

Síðan Innri **hreyfingar** gerir kleift að tilgreina Taka og Setja línur þegar ekki er eftirspurn úr upprunaskjali. Síðan Innanhússhreyfing er eins og vinnublað til að skipuleggja hluti. Ekki er hægt að vinna raunverulega hreyfingu beint úr henni. Þegar lína er fyllt út skal nota aðgerðina **Stofna birgðahreyfingu** til að senda línuna á **síðuna Birgðahreyfing**, sem er þar sem unnið er og skrá hreyfinguna.

### <a name="to-move-items-as-an-internal-movement"></a>Til að færa vörur sem innri hreyfingu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Innri hreyfingar** og velja síðan viðeigandi tengil.  
2. Veljið aðgerðina **Nýtt**. Gakktu úr skugga um að **Nr.** reiturinn á flýtiflipanum **Almennt** er fylltur út.
3. Í reitnum **Kóti birgðageymslu** er færð inn birgðageymslan þar sem hreyfingin á sér stað.  

    Ef birgðageymssla er sjálfgefin birgðageymsla sem starfsmaður í vöruhúsi er birgðageymslukótanum sjálfkrafa bætt við.  
4. Í reitinn **Kóti til-hólfs er færður** inn kóti hólfsins sem færa á vörurnar í.

    Í framleiðslu gæti hólfið til dæmis verið opið vinnusalarhólf sem skilgreint er á birgðageymsluspjaldinu eða vinnustöðinni.  
5. Í reitinn **Gjalddagi** er færð inn dagsetningin þegar ljúka á hreyfingunni.  
6. Reitirnir eru fylltir út eftir þörfum í hverri línu. Innanhússhreyfingarskjöl hafa eina línu fyrir hverja hreyfingu. Í línunni eru bæði aðgerðirnar taka og setja.
7. Reiturinn Vörunr. er valinn **.** til að opna síðuna **Innihald hólfs** . Velja vöruna sem á að færa eftir því hvað er til ráðstöfunar í hólfum. Einnig er hægt að velja aðgerðina **Sækja innihald hólfs** til að fylla innri hreyfingalínur á grundvelli afmarkananna.  

    Þegar varan hefur verið valin er reiturinn **Kóti** frá-hólfs sjálfkrafa fylltur út samkvæmt völdu hólfainnihaldi. Hægt er að velja hvaða hólf sem er þar sem varan er tiltæk. Reiturinn Vörunr **.** og **Reitirnir Kóti** frá-hólfs eru tengdir. Ef gildinu í einum reit er breytt gæti gildið í hinum breytt.  

     **Gildið sem fært var inn í hausinn er fært inn í reitinn Kóti** til-hólfs. Henni má breyta í línunni í aðra hólfkóta sem hvorki er lokað né sérstakur í sérstökum tilgangi. Nánari upplýsingar á [reitnum Hollur.](warehouse-how-to-create-individual-bins.md#the-dedicated-field)  

8. Þegar búið er að skilgreina hvaða hólf á að færa vörurnar úr og í er magnið sem á að færa fært inn í reitinn **Magn fært** .  

    > [!NOTE]  
    > Magnið verður að vera tiltækt í hólfinu sem tilgreint er í reitnum **Kóti** frá-hólfs.  

9. Þegar notandi er tilbúinn að vinna hreyfinguna skal velja aðgerðina **Stofna birgðahreyfingu** .  

    > [!NOTE]  
    >  Þegar hreyfingin hefur verið stofnuð er innri hreyfingarlínunum eytt.  

Framkvæma aðra óáætlaða hreyfingu á síðunni **Birgðahreyfing** á sama hátt og hreyfing á grundvelli upprunaskjala.

### <a name="to-record-the-inventory-movement"></a>Til að skrá birgðahreyfingu

1. Á síðunni **Birgðahreyfing er** skjalið opnað til að skrá hreyfinguna fyrir.  
2. Í reitnum **Hólfkóti** á hreyfingalínunum er hólfið sem vörurnar verða tíndar úr þar sem varan er tiltæk. Hægt er að skipta um hólf ef með þarf.
3. Færa skal inn og færa inn upplýsingar um fært magn í reitinn **Magn til afgreiðslu** . Gildið á línum Taka og Setja verður að vera það sama. Annars er ekki hægt að skrá hreyfinguna.

    Ef taka þarf vörurnar í línu úr fleiri en einu hólfi, til dæmis vegna þess að allt magnið er ekki í hólfinu, skal nota aðgerðina **Skipta línu** á flýtiflipanum **Línur** . Aðgerðin stofnar línu fyrir eftirstandandi magn sem á að meðhöndla.  
4. Velja skal Reitinn **Dagbók birgða Hreyfingaaðgerð** .  

Eftirfarandi gerist í bókunarferlinu:

* Vöruhúsafærslur gefa til kynna að magnið sé flutt úr taka-hólfunum í staðhólfin.

## <a name="to-move-items-with-the-item-reclassification-journal"></a>Til að færa vörur með vöruendurflokkunarbók

Í stað þess að nota hreyfingaskjöl er hægt að skrá hreyfingar með því að endurflokka hólfakóta á vörur. Nánari upplýsingar um [talningu, leiðréttingu og endurflokkun birgða með færslubókum](inventory-how-count-adjust-reclassify.md).

> [!NOTE]  
> Hreyfingar sem bókaðar eru með endurflokkunarbókum gera hreyfingaskjöl ekki tilbúin til hreyfinga.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vöruendurflokkunarbók** og velja síðan viðkomandi tengil.  
2. Í hverri færslubókarlínu eru hólfin skilgreind sem færa á vörurnar úr og til með því að fylla út reitina **Hólfkóti** og **Nýr hólfkóti** .  

    1. Ef flytja á allt innihald hólfs yfir í annað hólf, skal velja aðgerðina **Sækja innihald hólfs**.  
    2. Afmarkanirnar eru notaðar til að finna hólfið sem inniheldur vörurnar sem á að færa og velja **síðan Í lagi**. Færslubókarlínur eru fylltar út með efni hólfsins.  
3. Aðrir reitir eru fylltir út fyrir hverja færslubókarlínu.
4. Bóka skal endurflokkunarbók.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## <a name="see-also"></a>Sjá einnig .

[Yfirlit yfir vöruhúsakerfi](design-details-warehouse-management.md)
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Samsetningardeild](assembly-assemble-items.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
