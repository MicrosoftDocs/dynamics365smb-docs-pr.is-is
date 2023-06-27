---
title: Flytja vörur á milli birgðageymslna
description: 'Frekari upplýsingar um hvernig á að flytja birgðir frá einum stað eða vöruhúsi til annars, annað hvort með endurflokkunarbók eða flutningspöntunum.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'move, warehouse'
ms.search.forms: '5746, 5745, 5759, 5753, 5743, 5758, 5752, 5744, 5749, 5740, 5741, 5742, 5757, 5748, 5747, 9285, 5756, 5755'
---
# <a name="transfer-inventory-between-locations" />Flytja birgðir milli birgðageymslna

Það er hægt að flytja birgðavörur milli tveggja staða með því að búa til flutningspantanir. Einnig er hægt að nota vöruendurflokkunarbók.

> [!NOTE]
> Til að flytja vörur þarf að setja upp staðsetningar og flutningsleiðir. Til að fræðast meira um uppsetningu staðsetningar er farið í  [Setja upp staðsetningar](inventory-how-setup-locations.md). Ekki er hægt að nota flutningspantanir fyrir  *auða*  staði.

## <a name="transfer-orders" />Flutningspöntunum

Hægt er að senda sendingu út frá einum stað og fá heimflutning á áfangastað. Hægt er að:

* Rekja magn í flutningi
* Skilgreinið dagatöl, leiðir og afgreiðslutíma á innleið og útleið fyrir dagsetningarútreikninga og áætlanagerð. Til að fræðast meira um áætlanagerð er farið í  [um áætlunaraðgerðir](production-about-planning-functionality.md).
* Nota mismunandi vöruhúsaaðgerðir fyrir inn-og útleiðarstaði.
* Með sumum takmörkunum er hægt að nota flutningspantanir fyrir beinan flutning.

## <a name="item-reclassification-journals" />Endurflokkunarbækur vöru

* Einfaldur, Beinn flutningur á vörum milli birgðageymslna.
* Flytja vörur milli hólfa. Frekari upplýsingar um flutning vara milli hólfa er að  [flytja Óáætlaðar vörur í Grunnvöruhúsafbrigðum](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)
* Breyta lotu eða raðnúmeri á nýja lotu eða raðnúmeri. Til að fræðast meira um raðnúmer og lotunúmer er farið í  [endurflokka rað-eða lotunúmer](inventory-how-work-item-tracking.md#to-reclassify-serial-or-lot-numbers).
* Chang gildistíma til nýju dagsetningarinnar.
* Endurflokka vörur úr  *auða*  birgðageymslu í raunverulega staðsetningu.
* Vöruhúsaaðgerðum er ekki stjórnað. Vöruhúsafærslur verða stofnaðar.

## <a name="to-transfer-items-with-a-transfer-order" />Vörur fluttar með flutningspöntun

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Flutningspantanir** og velja síðan viðkomandi tengil.
2. Fyllt er út í reiti eftir því sem á við á síðunni **Flutningspöntun**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   Ef Millisendingarkóti, Kóti flutningsfyrirtækisins og  **Flutningsþjónusta** eru fylltir út  **í valnum leiðanna** **.**  **·**  síðu þegar Flutningsleiðin er sett upp eru samsvarandi svæði í millisendingarpöntuninni sjálfkrafa fyllt út.

    Þegar fyllt er út í reitinn **Flutningsþjónusta** reiknar kerfið út móttökudagsetningu fyrir flutt-til birgðageymslu með því að bæta flutningstíma flutningsþjónustunnar við afhendingardagsetninguna.

3. Nokkrar leiðir eru til að fylla út línurnar:

    |Valkostur  |Description  |
    |---------|---------|
    |Með íhlutun notanda     |  **Á vöruflipanum línur**  er fyllt út lína fyrir vöru eða aðgerðin velja atriði  **notuð**  til að velja margar vörur.        |
    |Sjálfvirk aðferð     | * Velja  **aðgerðina Sækja innihald**  hólfs til að velja vörur úr tilteknu hólfi á staðnum.<br><br>* Velja skal  **Sækja móttökulínur**  til að velja vörur sem eru nýkomnar í sendist-frá birgðageymslunni.        |

    Nú er hægt að senda vörurnar.
4. Veldu aðgerðina **Bóka** veldu **Senda** valkostinn og veldu síðan **Í lagi** hnappinn.

    Atriðin eru nú í flutningi milli tilgreindra staða, í samræmi við tilgreint flutningsleið.

    Sem starfsmaður vörugeymslu við flutninginn frá staðsetninginni skaltu halda áfram að fá vörurnar. Flutningspöntunarlínurnar eru þær sömu og við sendingu og er ekki hægt að breyta þeim.
5. Veldu aðgerðina **Bóka**, veldu **Móttaka** valkostinn og veldu síðan **Í lagi** hnappinn.

### <a name="post-multiple-transfer-orders-in-a-batch" />Bóka margar flutningspantanir í runu

Eftirfarandi ferli skýrir hvernig á að bóka flutningspantanir í runu.

1. 1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Flutningspantanir** og velja síðan viðkomandi tengil.  
2.  **Á síðunni flutningspantanir**  eru valdar pantanirnar sem á að bóka.
3. Í reitnum **númer** Skal opna samhengisvalmyndina og velja  **Velja meira**.
4. Veljið gátreitinn fyrir línurnar fyrir hverja pöntun sem á að bóka.
5.  **Veljið bókunaraðgerðina**  og veljið  **síðan bóka runu**.
6.  **Reitirnir á eftir flutningspöntun**  eru fylltir út eftir þörfum.

   > [!TIP]
    > Fyrir flutningspantanir sem nota millisendingarstaði er hægt að velja annað hvort  **sendingar**  eða  **móttöku**. Endurtakið þetta skref ef þið þurfið að gera hvort tveggja. Fyrir pantanir þar sem  **kveikt er á beinni bókun**  virka báðir Valkostir á sama hátt og bóka pöntunina alveg.

7. Veldu  **í lagi**.
8. Til að skoða hugsanleg vandamál skaltu opna  **Villuskilaboðadagskrá**  síðunnar.

    > [!NOTE]
    > Bókun margra skjala gæti tekið nokkurn tíma og útilokað aðra notendur. Íhugaðu að virkja bakgrunnsbókun. Frekari upplýsingar, sjá [Nota verkraðir til að tímaraða verkhlutum](/dynamics365/business-central/admin-job-queues-schedule-tasks).

### <a name="schedule-a-job-queue-entry-to-post-multiple-documents-in-a-batch" />Áætla færslu í Verkröð til að bóka mörg skjöl í runu

Einnig er hægt að nota verkraðarinn til að áætla að bókun gerist í einu sem er hentugt fyrir fyrirtækið. Það gæti til dæmis verið skynsamlegt fyrir fyrirtæki að keyra tilteknar venjur þegar mest er um gagnafærslu dagsins.

Eftirfarandi ferli sýnir hvernig á að setja upp  **skýrsluna runubókun flutningspantanir**  til að bóka sjálfkrafa beinar flutningspantanir á 4 PM á virkum dögum. Þessi tími er bara dæmi. Skrefin eru hin sömu fyrir önnur skjöl.  

1.  **Leitaðu að síðunni Vinnsluraðarfærslur**  og veldu síðan tengda tengilinn.  
2. Valið er aðgerðin **Nýtt**.  
3. Í reitnum **Gerð hlutar sem á að keyra** skal velja **Skýrsla**.  
4.  **Í HLUTAKENNI til keyrslu**  er valið  **5707, runubókun-millifærslupantanir**.
5. Gátreiturinn skýrslubeiðsíðuhafi  **er**  valinn.
6.  **Á beiðnisíðu keyrslna flutningspantanir**  er valið valkostinn sendist  **, sía í**  beinan flutning  **og síðan valið** í  **lagi**.

   > [!IMPORTANT]
   > Mikilvægt er að setja afmarkanir. Annars,  [!INCLUDE [prod_short](includes/prod_short.md)]  munum eftir öllum skjölum, þó þau séu ekki tilbúin. Íhuga skal að setja afmörkun á  **reitinn Staða**  fyrir gildið  **Útgefin** og afmörkun á  **reitnum Bókunardags**  . fyrir gildið  **... í dag**. Frekari upplýsingar um afmarkanir er að fara til að  [raða, leita og sía](/dynamics365/business-central/ui-enter-criteria-filters).

7. Velja skal alla gátreiti  **sem keyra á á mánudögum**  til  **keyrslu á föstudögum**.
8.  **Í reitinn Upphafstími**  er FÆRT  **4 PM**.
9. Velja aðgerðina **Stilla stöðu á Tilbúin**.

## <a name="to-transfer-items-with-the-item-reclassification-journal" />Til að flytja vörur með vöruendurflokkunarbók

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vöruendurflokkunarbók** og velja síðan viðkomandi tengil.
2. Á síðunni **Birgðaendurflokkunarbók** skal fylla út reitina eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Í reitnum **Kóði birgðageymslu** er færð inn birgðageymslan þar sem vörurnar eru nú geymdar.

    > [!NOTE]  
    > Til að flytja hluti sem ekki hafa staðsetningarkóða skal skilja reitinn **Staðsetningarkóða** eftir auðan.
4. Í reitnum **Nýr staðsetningarkóði**, sláðu inn staðinn sem þú vilt flytja hlutina í.
5. Valið er **Bóka** aðgerðin.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## <a name="undo-a-transfer-shipment" />Afturkalla flutningsendingu

Ef mistök finnast í magni í bókaðri flutningspöntun, svo framarlega sem sendingin berst ekki er auðvelt að leiðrétta magnið.  **Á síðunni Póstsendingarsending**  er búið að  **leiðrétta afhendingarlínur**, eins og hér segir:

* Gildið í  **reitnum Magn afhent**  er lækkað með magninu sem hefur verið afturkallað.
* Gildið í  **reitnum Magn til sendingar**  hækkar eftir því magni sem hefur verið afturkallað.
*  **Gátreiturinn leiðrétting**  er valinn fyrir línurnar.

Ef magnið var sent í vöruhúsaafhendingu er leiðréttingarlína stofnuð í bókuðu vöruhúsaafhendinguna.

Til að ljúka leiðréttingu þarf að opna millifærslapöntunina, færa inn rétt magn og bóka pöntunina. Ef vöruhúsaafhending er notuð til að senda pöntunina, Stofnið og bókið nýja vöruhúsaafhendingu.

## <a name="see-related-microsoft-training" />Sjá tengda [Microsoft þjálfun](/training/modules/transfer-items/)

## <a name="see-also" />Sjá einnig .

[Stjórna birgðum](inventory-manage-inventory.md)  
[Uppsetning birgðageymsla](inventory-how-setup-locations.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
