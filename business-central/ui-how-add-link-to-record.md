---
title: 'Bæta við viðhengjum, tenglum og athugasemdum á færslum'
description: 'Tengja tengil við skjal eða vefsvæði við tiltekna færslu, til dæmis viðskiptavin eða skjal.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: how-to
ms.date: 02/24/2023
ms.custom: bap-template
---
# Stjórna viðhengjum, tenglum og athugasemdum á spjöldum og fylgiskjölum

Á flestum listasíðum, kortum og fylgiskjölum er hægt að tengja skrár, bæta við tenglum og skrifa athugasemdir á  **viðhengis**  -flipanum í  **FACTBOX**  rúðunni. Talan í titli flipans gefur til kynna hversu margar viðhengdar skrár, tenglar eða athugasemdir eru til fyrir spjaldið eða skjalið.

 **Á flipanum Línur**  er einnig hægt að nota viðhengið  **·**  til að tengja skjöl við tiltekna línu. Til dæmis gæti verið æskilegt að tengja hönnunarlýsingar við vöru á innkaupareikningi.

Viðhengi, tenglar og Minnismiðar vera tengdir kortinu eða skjalinu meðan unnið er í öðrum ríkjum. Til dæmis frá áframhaldandi sölupöntuninni í bókaðan sölureikning. Hins vegar eru engar viðhengisgerðirnar úttak úr kerfinu, til dæmis við prentun eða þegar verið er að vista í skrá.

Einnig er hægt að bæta viðhengjum við tölvupóstinn sem sendur er úr [!INCLUDE [prod_short](includes/prod_short.md)]. Þegar sendur er tölvupóstur beint úr skjali eins og sölutilboð,  **leyfir aðgerðin bæta skrá úr upprunaskjali**  að velja skrár sem tengjast því. Aðeins er hægt að velja skrár sem tengdar eru við skjalið. Ekki er hægt að velja skrár sem tengdar eru línum.

> [!NOTE]
> Þegar verið er að senda og reikningsfæra sölu- eða innkaupapöntun verður viðhengið aðeins hengt við endanlegan reikning pöntunarinnar. Á sama hátt, þegar verið er að reikningsfæra með frestunaraðgerðinni, tengist viðhengið aðeins fjárhagsfærslum skjalsins en ekki fyrir frestunarfærslur.
>
> Ef pöntun er eytt áður en hún er reikningsfærð er viðhengið einnig fjarlægt. Þegar innkaupapantanir eru reikningsfærðar með aðgerðinni Sækja móttökulínur úr innkaupareikningi er viðhenginu á innkaupapöntunum ekki bætt við innkaupareikninginn.

## Til að hengja skrá við innkaupareikning

Hægt er að tengja hvaða tegund af skrá fyrir sig, til dæmis texta, mynd eða myndskrár, á spjald, fylgiskjal eða í línu í skjali. Þetta er til dæmis gagnlegt þegar óskað er eftir að vista reikning lánardrottins sem PDF-skrá á tengdum innkaupareikningi í [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Skrár sem eru tengdar við eiginleikann skjöl eru ekki hafðar með á  **flipanum viðhengi**  . Nánari upplýsingar er að finna  [í incoming skjölum](across-income-documents.md). Sama gildir um skrár sem hengdar eru á línur í skjölum.

Eftirfarandi ferli byggist á innkaupareikningur. Skrefin eru svipuð fyrir öll önnur studd skjöl og kort.

> [!TIP]
> Ef viðhengið er tiltekið í línu í skjali er hægt að hengja það við línuna. Línan er valin og síðan er  **valin aðgerðin viðhengi** .

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupareikningar** og velja síðan viðkomandi tengil.
2. Opna innkaupareikning sem á að tengja skrá við.
3.  **Í FACTBOX**  rúðunni skal velja  **flipann viðhengi** .
4. Veljið gildið fyrir aftan reitinn **Skjöl**, eins og „0“.
5. Á síðunni **Skjöl í viðhengi** í reitnum **Viðhengi** skal velja hnappinn **Velja skrá**.
6. Veldu skrá frá hvaða staðsetningu sem er og veldu svo hnappinn **Opna**.

Skráin er nú hengd við innkaupareikninginn.

## Til að skoða viðhengda skrá

1.  **Opnið**  flipann viðhengja  **á FACTBOX**  rúðunni.
2. Veljið gildið fyrir aftan reitinn **Skjöl**, eins og „1“.
3. Á síðunni **Viðhengd fylgiskjöl** skaltu velja aðgerðina **Forskoðun**.
4. Opnaðu skrána sem var hlaðið niður.

## Vista skjal sem PDF-viðhengi

Í hvert sinn sem vista þarf skjal sem skrá er hægt að nota aðgerðina **Hengja við sem PDF** til að ná í núverandi innihald skjals sem PDF-skrá hengda við FactBox skjalsins. Þetta er gagnlegt, til dæmis þegar skjöl fylgja mörgum skrefum í ferli, svo sem söluferli eða samþykktarverkflæði og ætlunin er að vísa til útprentunar af fyrra skrefi.

Eftirfarandi ferli byggist á sölupöntun. Skrefin eru svipuð fyrir öll studd skjöl.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.
2. Veldu sölupöntun og veldu síðan aðgerðina **Hengja við sem PDF**.

PDF-skrá með núverandi innihaldi sölupöntunarinnar er bætt við flipann **Viðhengi** í FactBox.

## Til að bæta við tengli af birgðaspjaldi

Hægt er að bæta við tengli af korti eða skjali á einhverja vefslóð. Þetta er gagnlegt, til dæmis þegar tengja á birgðaspjald við vörulista birgis.

Eftirfarandi aðferð er byggð á birgðaspjaldi. Skrefin eru svipuð fyrir öll önnur studd kort og skjöl.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur** og velja síðan viðkomandi tengil.
2. Veldu vöruna sem þú vilt bæta við tengli úr og veldu svo flipann **Viðhengi** í upplýsingareitnum.
3. Í **Tenglar** skal velja **+** táknið.
4. Í svæðinu **Veffang tengils** skal slá inn tengilinn.

    Tengillinn verður að vera gild vefslóð eða slóð innra nets.

5. Í reitinn **Lýsing** skal færa inn upplýsingar um tengilinn.  
6. Velja hnappinn **Í lagi**.

Tengillinn er nú tengdur við birgðaspjaldið.  

## Til að skrifa athugasemd á sölupöntun

Hægt er að skrifa athugasemd á skjal eða kort, til dæmis til að skrifa sérstakar leiðbeiningar fyrir aðra notendur skjalsins eða kortsins. Hægt er að hafa skráartengla og vefslóðir með í athugasemdum.

> [!NOTE]
> Athugasemdirnar á flipanum **Viðhengi** eru ekki tengdar virkni innri athugasemda, sem eru aðallega notaðar til að eiga samskipti á milli notenda verkflæðis. Nánari upplýsingar er að finna í [Uppsetning Verkflæði Tilkynningar](across-setting-up-workflow-notifications.md).

Eftirfarandi ferli byggist á sölupöntun. Skrefin eru svipuð fyrir öll önnur studd skjöl og kort.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.
2. Veljið sölupöntunina sem á að afskrifa athugasemd við og veljið svo flipann **Viðhengi** í upplýsingareitnum.
3. Í hlutanum **Athugasemdir** skal velja **+** táknið.
4. Í reitinn **Athugasemd** skal færa inn hvaða texta sem er, t.d. „Þetta er áríðandi pöntun“.
5. Velja hnappinn **Í lagi**.

Athugasemdin er nú hengd við sölupöntunina.

## Sjá einnig  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Skjöl á innleið](across-income-documents.md)  
[Setja upp tilkynningar verkflæðis](across-setting-up-workflow-notifications.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
