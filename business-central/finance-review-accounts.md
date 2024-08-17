---
title: Skoða fjárhagur reikninga
description: Þú getur rakið framvinduna þegar þú endurskoðar upphæðir í fjárhagur reikningum.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 08/06/2024
ms.custom: bap-template
ms.search.form: '22207,'
ms.service: dynamics-365-business-central
---

# Fara yfir upphæðir í fjárhagur reikningum

Þú gætir hafa fjárhagur reikninga sem þú hefur oft auga með. Einnig gæti þurft að flýta endurskoðunarferlinu í lok mánaðar. Til að fá aðstoð við að fylgjast með því sem þú hefur gert og til að flýta dómum skal nota aðgerðina **Fara yfir færslur** á síðunni **Bókhaldslykill** eða **Fjárhagsspjald** fyrir hvern reikning. 

## Setja upp reikninga fyrir umsagnir

Á síðunni **Fjárhagsspjald** fyrir hvern reikning skal tilgreina hvernig hægt er að skoða umsagnir í reitnum Endurskoða **stefnu** .

|Fara yfir reglu  |Heimildasamstæða  |
|---------|---------|
|Engin     | Ekki er hægt að merkja færslur reikningsins sem yfirfarið. Þessi valkostur er til dæmis notaður fyrir reikninga eins og safnreikninga, útistandandi reikninga og bankareikninga þar sem aðrar leiðir eru til að fara yfir upphæðir þeirra.        |
|Leyfa yfirferð     | Ekki þarf að taka færslur með í endurskoðun og upphæðir debet- og kreditfærslna þurfa ekki að jafna. Þú fjarlægir endurskoðun, til dæmis ef þú hefur gert mistök.        |
|Leyfa yfirferð og að jafna stöðu     | Heildarupphæðir debet- og kreditfærslna í endurskoðuninni verða að samsvara. Reitirnir Debet **og** Kredit **sýna upphæðirnar og í reitnum** Staða er samtalan **.**  Með þessari stillingu er einnig hægt að fjarlægja yfirferð. Þegar endurskoðun er fjarlægð úr einni eða fleiri færslum verða debet- og kreditfærslurnar enn að stemma.        |

## Merkja færslur sem endurskoðaðar

Veldu færslurnar sem þú hefur skoðað og notaðu **svo Setja valið sem yfirfarið** aðgerð. Í hvert sinn sem ein eða fleiri færslur eru merktar sem yfirfarnar fá færslurnar sama númer í dálknum **Yfirfarið kenni** . Kenni endurskoðunar er hentug leið til að fylgjast með færslunum sem voru endurskoðaðar samtímis. [!INCLUDE [prod_short](includes/prod_short.md)] skráir einnig notandann sem sá um endurskoðunina og hvenær hann gerði það.

Ef færslur eru merktar sem yfirfarnar, en sé eftir því að gera það skal nota aðgerðina **Setja valið sem ekki yfirfarið** .

* Ef endurskoðaðri stefnu er úthlutað á reikninginn, endurstillir aðgerðin endurskoðað kenni á 0 og fjarlægir einstakling og dagsetningu og tíma endurskoðunar. 
* Ef reglunni Yfirfara leyfða stöðu og samsvörun er úthlutað verður kredit- og debetið enn að stemma. Ef ein af færslunum í endurskoðuninni er til dæmis mistök er hægt að velja aðra færslu með réttu gildi. Skiptifærslan þarf ekki að hafa sama kennið yfirfarið.

> [!TIP]
> Fljótleg leið til að velja margar færslur er að halda niðri Ctrl eða Vakt á meðan færslurnar eru valin. *Ctrl gerir kleift að velja tilteknar færslur og* Vakt *velur allar færslur milli fyrstu og síðustu færslnanna* sem valdar eru.

## Fara yfir reikninga með gömlum færslum

Hugsanlega eru færslur frá liðnu tímabili sem þegar er búið að endurskoða eða þarfnast ekki endurskoðunar. Notandi vill bara byrja að endurskoða færslur frá, til dæmis upphaf árs eða reikningstímabils. Hægt er að láta færslurnar eins og er. Eigi hinsvegar að greina gögn í Excel eða með því að nota greiningarham er færslurnar merktar sem yfirfarnar. Farið er í Greiningarfærslur til að [fræðast meira um greiningu færslna](#analyze-entries). Til að merkja færslurnar sem yfirfarnar er afmörkun bætt við á afmörkunarsvæðinu til að birta aðeins þær færslur og velja **svo Merkja valdar færslur sem yfirfarnar** aðgerð.

## Afmarka færslur

Til að fá skýrari mynd eru nokkrar leiðir til að afmarka færslur á síðunni **Skoða fjárhagsfærslur** .

* Nota aðgerðina **Sýna skoðaðar færslur** og **Fela yfirfarnar** færslur til að sýna aðeins þær færslur sem notandi hefur eða hefur ekki yfirfarið. Til að hreinsa afmarkanirnar skal nota aðgerðina **Sýna allar færslur** .
* Nota skal afmörkunarsvæðið. Til dæmis er hægt að afmarka eftir reikningsnúmeri eða, ef um er að ræða eldri færslur og merkja þær allar sem yfirfarnar, með bókunardagsetningu.

## Greina færslur

Það eru nokkrar leiðir til að greina fjárhagur færslurnar sem þú hefur skoðað.

* Kveikja á greiningarstillingu, til dæmis til að flokka færslur eftir kenni þeirra. Nánari upplýsingar um greiningarstillingu er farið í [Greiningarsíðugögn með greiningarstillingu](analysis-mode.md).
* Flytja færslurnar út í Excel.

## Sjá einnig .

[Skilja fjárhagur og bókhaldslykil](finance-general-ledger.md)    
[Setja upp eða breyta bókhaldslyklum](finance-setup-chart-accounts.md)    
