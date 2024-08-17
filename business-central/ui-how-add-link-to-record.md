---
title: 'Bæta við viðhengjum, tenglum og athugasemdum á færslum'
description: 'Tengja tengla við skjal eða vefsvæði við tiltekna færslu, t.d. viðskiptamann eða fylgiskjal.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 09/15/2023
ms.custom: bap-template
ms.search.form: 8896
ms-service: dynamics-365-business-central
ms.service: dynamics-365-business-central
---
# Vinna með viðhengi, tengla og athugasemdir á spjöldum og skjölum

Á flestum listasíðum, spjöldum og skjölum er hægt að hengja við skrár, bæta við tenglum og skrifa athugasemdir á flipanum **Viðhengi** á **upplýsingakassasvæðinu** . Númerið í titlinum gefur til kynna hversu margar viðhengdar skrár, tenglar eða athugasemdir eru til fyrir spjaldið eða skjalið.

Á flýtiflipanum **Línur** er einnig hægt að nota aðgerðina **Viðhengi** til að tengja skjöl við tiltekna línu. Til dæmis gæti notandi viljað hengja hönnunarlýsingar við vöru á innkaupareikningi.

Viðhengi, tenglar og athugasemdir eru hengdar við kortið eða skjalið á meðan unnið er úr þeim í öðrum ríkjum. Til dæmis, frá sölupöntun í bókaðan sölureikning. Hins vegar eru engar viðhengisgerðirnar úttak úr kerfinu, til dæmis við prentun eða þegar verið er að vista í skrá.

Þú getur einnig bætt viðhengjum við tölvupóstinn sem þú sendir frá [!INCLUDE [prod_short](includes/prod_short.md)]. Þegar tölvupóstur er sendur beint úr skjali, t.d. sölutilboði, gerir Aðgerðin **Bæta við skrá úr upprunaskjali** kleift að velja skrár sem eru tengdar því. Aðeins er hægt að velja skrár sem eru tengdar skjalinu. Ekki er hægt að velja skrár sem eru tengdar línum.

> [!NOTE]
> Þegar verið er að senda og reikningsfæra sölu- eða innkaupapöntun verður viðhengið aðeins hengt við endanlegan reikning pöntunarinnar. Á sama hátt og þegar seinkanir eru reikningsfærðar er viðhengið hengt við fjárhagsfærslur skjalsins en ekki frestunarfærslurnar.
>
> Ef pöntun er eytt áður en hún er reikningsfærð er viðhengið einnig fjarlægt.
>
> Þegar aðgerðin **Sækja móttökulínur** er notuð á innkaupareikningi er viðhenginu á tengdri innkaupapöntun bætt við innkaupareikninginn.

## Til að hengja skrá við innkaupareikning

Hægt er að hengja hvaða gerð af skrá sem er, t.d. texta, mynd eða myndskrár, við spjald, skjal eða línu í skjali. Þetta er til dæmis gagnlegt þegar óskað er eftir að vista reikning lánardrottins sem PDF-skrá á tengdum innkaupareikningi í [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Skrár sem tengjast aðgerðinni Skjöl á innleið eru ekki á **flipanum Viðhengi** . Nánari upplýsingar [eru í Skjöl á](across-income-documents.md) innleið. Hið sama á við um skrár sem eru tengdar línum í skjölum.

Eftirfarandi ferli byggist á innkaupareikningur. Skrefin eru svipuð fyrir öll önnur studd skjöl og kort.

> [!TIP]
> Ef viðhengið á sérstaklega við línu í skjali er hægt að hengja það við línuna. Veljið línuna og veljið svo aðgerðina **Viðhengi** .

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupareikningar** og velja síðan viðkomandi tengil.
2. Innkaupareikningurinn sem tengja á skrá við er opnaður.
3.  **Á upplýsingakassasvæðinu** er flipinn **Viðhengi** valinn.
4. Veljið gildið fyrir aftan reitinn **Skjöl**, eins og „0“.
5. Á síðunni **Tengt skjöl** í reitnum **Viðhengi** .
6.  **Á svarglugganum Hengja skjal við er** eitt af eftirfarandi skrefum gert til að hengja við skrá:

   [!INCLUDE[file-upload](includes/file-upload.md)]

Skráin er nú hengd við innkaupareikninginn.

## Til að skoða viðhengda skrá

1. Flipinn Viðhengi **er opnaður á upplýsingakassanum** .
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

## Sjá einnig .  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Skjöl á innleið](across-income-documents.md)  
[Setja upp tilkynningar verkflæðis](across-setting-up-workflow-notifications.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
