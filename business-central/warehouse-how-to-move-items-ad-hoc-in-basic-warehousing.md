---
title: Flytja vörur óáætlað í grunnskilgreiningar vöruhúss
description: Þessi grein skýrir ófyrirhugaðar innri hreyfingar milli hóla án kröfu frá upprunaskjali.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/16/2022
ms.custom: bap-template
ms.search.form: '393, 7382'
---
# <a name="move-items-internally-in-basic-warehouse-configurations" />Flytja vörur inn í grunn Vöruhúsafbrigða

Það gæti verið æskilegt að flytja vörur milli hólfa án þess að eftirspurn sé eftir upprunaskjali. T.d. sem hluti af eftirfarandi verkþáttum:

* Endurskipuleggja vöruhúsið.
* Koma vörum á eftirlitssvæði.
* Færa aukavörur til og frá framleiðslusvæði. 

Hvernig vörur eru færðar fer eftir því hvernig vöruhúsið er sett upp sem Birgðageymsla. Frekari upplýsingar um  [uppsetningu vöruhúsastjórnunar](warehouse-setup-warehouse.md).

Í vöruhúsaleiðingum þar sem  **skiptiuppsetning á hólfi skylduskipti**  er kveikt, en ekki  **beinn tínsla-**  og frágangsfrágangur er hægt að skrá óáætlaðar hreyfingar á eftirfarandi síðum:  

*  **Á síðu hreyfingarinnar**  innanhúss.
*  **Á síðu Birgðaendurflokkunarbókar** .  

## <a name="internal-movements" />Innri hreyfingum

 **Síðan Innanhússhreyfingar**  gerir kleift að tilgreina taka og setja inn línur þegar engin eftirspurn er eftir upprunaskjali. Síða Innanhússhreyfinga er eins og vinnublað til að skipuleggja hlutina. Ekki er hægt að vinna úr raunverulegri hreyfingu beint út frá því. Þegar lína er fyllt út er aðgerðin stofna Birgðahreyfingalokun  **notuð**  til að senda línuna á  **síðuna birgðahreyfing**, sem er þar sem unnið er úr og skráð hreyfingin.

### <a name="to-move-items-as-an-internal-movement" />Til að færa vörur sem innri hreyfingu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, Sláðu inn  **innri hreyfingar** og veldu síðan tengda tengilinn.  
2. Veljið aðgerðina **Nýtt**. Gakktu úr skugga um að **Nr.** reiturinn á flýtiflipanum **Almennt** er fylltur út.
3. Í reitnum **Kóti birgðageymslu** er færð inn birgðageymslan þar sem hreyfingin á sér stað.  

    Ef staðsetningin er sjálfgefin staðsetning sem vöruhúsastarfsmaður bætir birgðageymslukótinn við sjálfkrafa.  
4.  **Í reitinn Kóti til-hólfs**  er ritaður kóti hólfsins sem færa á vörurnar í.

    Til dæmis í framleiðslu gæti hólfið verið opið vinnugólfhólf sem tilgreint er á birgðageymsluspjaldinu eða vinnustöðunum.  
5.  **Í reitinn Gjalddagi**  skal slá inn dagsetninguna sem á að ljúka hreyfingunni.  
6. Fyllt er í reitina eftir þörfum í hverri línu. Innhreyfingskjöl innanhúss eru með eina línu á hverja hreyfingu. Í línunni eru bæði tek og sæti aðgerðir.
7.  **Veldu Vörunr.**  til að opna  **listasíðuna**  innihald hólfs. Velja vöru sem á að fara eftir ráðstöfunartekjum hennar í hólfum. Einnig er hægt að velja  **aðgerðina Sækja innihald**  hólfs til að færa inn innri hreyfingalínur sem byggðar eru á afmörkunum.  

    Eftir að varan  **hefur verið valin er reiturinn frá-kóti**  sjálfkrafa fylltur út í samræmi við valið hólfainnihald. Hægt er að velja hólf þar sem varan er tiltæk.  **Vörunr.**  og  **frá hólfakóta**  eru tengdar. Ef gildið er breytt í einum reit gæti það breytt gildinu í hinu.  

     **Reiturinn Kóti**  til-hólfs er fylltur út með gildinu sem fært var inn í hausinn. Hægt er að breyta henni í línu í annan kóta hólfs sem er ekki lokaður eða hollur í sérstökum tilgangi. Frekari upplýsingar á  [Tileinkuðu sviði](warehouse-how-to-create-individual-bins.md#the-dedicated-field).  

8. Þegar búið er að skilgreina hvaða hólf eigi að flytja vörurnar af og til skal færa inn magnið sem á að færa í  **reitinn Magn** .  

    > [!NOTE]  
    > Magnið verður að vera tiltækt í hólfinu sem er tilgreint í  **reitnum Kóti frá-hólfs** .  

9. Þegar þú ert tilbúin (ur) til að vinna úr hreyfingunni, Veldu þá  **Stofna birgðahreyfingaðgerð** .  

    > [!NOTE]  
    >  Eftir að hreyfingin hefur verið stofnuð er innanhússhreyfilínum eytt.  

Framkvæmið hina óskipulögðu hreyfingu á  **síðunni Vöruhreyfill**  á sama hátt og óskað er eftir í hreyfingu samkvæmt upprunaskjölum.

### <a name="to-record-the-inventory-movement" />Birgðahreyfingin skráð

1.  **Opnið skjalið á síðunni birgðahreyfingar**  til að skrá hreyfinguna fyrir.  
2.  **Í reitnum Hólfkóti**  í hreyfingalínunum er hólfið þar sem vörurnar verða teknar til úr, þar sem varan er tiltæk. Hægt er að skipta um hólf ef með þarf.
3. Flytjið og Færið inn upplýsingar fyrir fært magn í  **reitinn Magn til afgreiðslu** . Gildið á línum Taka og Setja verður að vera það sama. Annars er ekki hægt að skrá hreyfinguna.

    Ef taka þarf vörurnar fyrir í línu úr fleiri en einu hólfi, til dæmis vegna þess að heildarmagn er ekki í hólfinu, skal nota  **aðgerðina skipta línu**  á  **fastflipanum línur** . Aðgerðin býr til línu fyrir eftirstandandi magn sem á að afgreiða.  
4.  **Veldu Register Invt. Hreyfingarleysis** .  

Eftirfarandi gerist á meðan á bókunarferlinu stendur:

* Vöruhúsafærslur gefa til kynna að magnið sé flutt úr Take-hólfum í stað hólfa.

## <a name="to-move-items-with-the-item-reclassification-journal" />Til að færa vörur með vöruendurflokkunarbók

Í stað þess að nota hreyfingarskjöl er hægt að skrá hreyfingar með því að endurflokkun hólfakóta á vörum. Frekari upplýsingar til að  [telja, leiðrétta og endurflokka birgðir með notkun færslubóka](inventory-how-count-adjust-reclassify.md).

> [!NOTE]  
> Hreyfingar bókaðar með endurflokkunarbókum ekki gera Hreyfðu skjölin tilbúin til að flytja.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vöruendurflokkunarbók** og velja síðan viðkomandi tengil.  
2. Í hverri færslubókarlínu eru hólfin skilgreind til að færa vörurnar frá og til með því að fylla  **út hólfakóta**  og  **nýja hólfakóta** .  

    1. Ef flytja á allt innihald hólfs yfir í annað hólf, skal velja aðgerðina **Sækja innihald hólfs**.  
    2. Notaðu afmarkanir til að finna hólfið sem inniheldur atriðin sem þú vilt flytja og veldu  **svo í lagi**. Færslubókarlínur eru fylltar út með efni hólfsins.  
3. Aðrir reitir eru fylltir út fyrir hverja færslubókarlínu.
4. Bóka skal endurflokkunarbók.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## <a name="see-related-microsoft-trainingtrainingmodulesmanage-internal-warehouse-processes" />Sjá tengda [Microsoft þjálfun](/training/modules/manage-internal-warehouse-processes/)

## <a name="see-also" />Sjá einnig .

[Yfirlit](design-details-warehouse-management.md)
[vöruhúsakerstjórnunar birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Samsetningardeild](assembly-assemble-items.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
