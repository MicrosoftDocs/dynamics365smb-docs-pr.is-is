---
title: Notkun Word-sniðmáta fyrir laus samskipti
description: Word-sniðmát geta auðveldað að búa til mörg skjöl í einu sem eru sérsniðin fyrir tilteknar einingar.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/01/2023
ms.custom: bap-template
ms.search.forms: '9989, 13,'
ms.service: dynamics-365-business-central
---

# Nota Word-notuð fyrir mörg samskipti í einu

Microsoft Word-sniðmát geta auðveldað mörg samskipti í einu á prenti eða í tölvupósti með einingum á borð við tengiliði, viðskiptamenn og lánardrottna. Til dæmis er hægt að stofna:

* Bæklinga til að gera viðskiptamönnum viðvart um söluherferð
* Bréf til að láta lánardrottna vita um nýja innkaupastefnu
* Fundarboð til að laða að tengiliði að komandi viðburði

> [!NOTE]
> Þegar Word-sniðmát eru sett upp verður að nota tæki með Microsoft Word 2019 eða nýrra og Windows-stýrikerfið uppsett.

## Uppsetning gagnagjafa

Einingar eru notaðar sem [!INCLUDE[prod_short](includes/prod_short.md)] gagnareitir fyrir sniðmátið og bætt við sameinuðum reitum til að sérsníða skjöl fyrir hverja einingu. Innfellingarsvæðin koma úr einingunni í [!INCLUDE[prod_short](includes/prod_short.md)]. Þegar Word-sniðmát er notað í einingu verða gögn úr innfellingarsvæðunum sett inn í skjalið.

Á síðunni Word-sniðmát **hjálpar notandinn** að fylgja eftirfarandi skrefum þegar nýtt sniðmát er stofnað.

1. Velja skal eina eða fleiri einingar til að nota sem uppruna gagna. Eigi til dæmis að stofna bækling fyrir söluherferð er einingin Viðskiptamaður líklega valin sem uppruni.
2. Velja aðrar einingar sem aukauppruna gagna. Nánari upplýsingar um [bæta við færslum sem eru tengdar eða Ótengd upprunaeiningunni](#add-entries-that-are-related-or-unrelated-to-the-source-entity).
3. Sækja autt sniðmát. Hægt er að setja sniðmátið upp í Word tafarlaust eða hlaða upp auðu sniðmáti og ljúka leiðbeiningunum. Þegar sniðmátið er tilbúið skal nota aðgerðina **Hlaða** upp á síðunni **Word-sniðmát** til að skipta út auðu sniðmáti með fulluðu sniðmáti. Nánari upplýsingar um [sniðmátið eru sett upp í Word](#set-up-the-template-in-word).
4. Hlaða upp sniðmátinu sem búið er að undirbúa.
5. Færður er inn kóti og heiti sem auðkennir sniðmátið.

Þegar sniðmát er sótt fæst .zip skrá með tveimur skrám.

|Skrá  |Heimildasamstæða  |
|---------|---------|
|DataSource.xlsx     | Gagnagjafaskráin býður upp á reitina sem hægt er að nota í sniðmátinu. Ekki breyta gagnagjafaskránni. Aðeins er hægt að nota Word-sniðmátið og gagnagjafaskrárnar sem sóttar eru og geyma þarf skrárnar á sama stað.     |
|Word-sniðmát     | .docx skrá sem nota á sem sniðmát.        |

Til að fræðast um uppsetningu sniðmáts í Word er farið að [Setja upp sniðmát í Word](#set-up-the-template-in-word).

## Bæta við færslum sem tengjast eða ótengdar upprunaeiningunni

Einnig er hægt að sameina gögn frá öðrum einingum. Til að bæta við öðrum einingum sem gagnaveitum skal nota eina af eftirfarandi aðgerðum á síðunni **Word-sniðmát** eða þegar uppsetningarleiðbeiningar með aðstoð eru notaðar:

|Aðgerð  |Heimildasamstæða  |
|---------|---------|
|**Bæta við tengdri einingu**  | Nota gögn frá einingum sem eru tengdar upprunaeiningunni. Til dæmis er hægt að sameina gögn úr tengiliðaeiningunni fyrir viðskiptamannaeininguna. Einingar eru tengdar þegar reitur á einni einingu vísar til annarrar. Reitur á viðskiptamannaeiningunni vísar til reits á tengiliðaeiningunni svo að hann tengist. Samnýtta reiturinn er oft kenni, svo sem heiti, kóti eða kenni.        |
|**Bæta við ótengdri einingu**| Nota gögn frá einingum sem eru ekki tengdar upprunaeiningunni. Til dæmis er verið að stofna sniðmát fyrir viðskiptamannaeininguna. Hægt er að bæta við stofngögnum svo hægt sé að hafa tengiliðaupplýsingarnar með. Lykilviðskipti eru sú að ef tengiliðaupplýsingum er breytt uppfærist hún sjálfkrafa í sniðmátinu. Þegar búið er að bæta við ótengdri einingu er hægt að bæta við einingum sem tengjast henni.         |

Fyrir ótengdar færslur er valin tiltekin færsla. Þar sem aðeins er hægt að bæta einingu við einu sinni, til að nota aðra færslu verður að eyða einingunni og bæta henni aftur við með nýju færslunni.

Hægt er að búa til stigveldi eininga, bæði tengt og ótengt. Tengslin eru sýnd sem trjáskipulag. Reiturinn **Einingartengsl** sýnir einnig upplýsingar um tengslin. Fyrir ótengdar einingar sýnir svæðið færsluna sem stofnar tengslin.

Þegar einingum er bætt við er reiturinn **Reitaforskeyti** notaður til að tilgreina forskeyti fyrir reitaheitin. Síðar þegar reitum er bætt við sniðmátið auðveldar forskeytið að greina á milli reita frá uppruna og annarra eininga.

### Velja skal þá reiti sem taka á með

Fyrir hverja einingu er hægt að tilgreina þá reiti sem á að vera tiltækir fyrir sniðmátið. Velja skal númerið í dálknum **Fjöldi valinna reita** til að fá aðgang að lista yfir reiti sem eru tiltækir. Á síðunni **Reitaval** er gátreiturinn **Taka með** til að tilgreina reitina. Sjálfgefið er að reitir sem fyrirtæki nota séu sjálfgefið innifaldir í sumum einingum. Hægt er að breyta listanum til dæmis til að fjarlægja sjálfgefnu reitina. Breytingarnar eiga aðeins við um það sniðmát sem unnið er með.

> [!NOTE]
> Heildarfjöldi reita sem hægt er að bæta við frá öllum einingum er 250.

> [!NOTE]
> Notandi eða samstarfsaðili Microsoft geta bætt sérsniðnum reitum við einingar. Þegar það er gert forskeytum við heiti reitanna með **CALC** og gefum þeim reitategundina **Reiknað**. Tegund reitarins er reiknuð til að gefa til kynna að reiturinn geti sýnt mismunandi tegundir gilda, svo sem texta, tölur, dagsetningar, og svo framvegis.

## Búa til Word-sniðmát í Business Central

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Word-sniðmát** og velja síðan viðkomandi tengil.
2. Veldu **Nýtt**, síðan **Búa til sniðmát** og fylgdu síðan eftirfarandi skrefum í uppsetningu með hjálp. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Einnig er hægt að búa til sniðmát beint af síðunni fyrir einingu með því að velja aðgerðina **Nota Word-sniðmát** til að opna hjálparuppsetninguna og síðan **Nýtt sniðmát**. Þegar þú gerir það er gagnagjafinn valinn fyrir þig út frá gerð einingarinnar.

## Setja upp sniðmátið í Word

Þegar sniðmát er sett upp í Word er hægt að bæta blöðrunarreitum við á **flipanum Póstar með því að velja Setja inn blæðingarreit**  **.** Í sameiningarreitunum koma úr gagnagjafaskránni sem sótt var fyrir eininguna. Þau virka sem staðgenglar sem segja Word hvar í skjalinu á að setja upplýsingarnar um eininguna.

:::image type="content" source="media/word-tmpl-merge-field.PNG" alt-text="Innfellingarsvæðum bætt við í Microsoft Word":::

## Nota sniðmát

Þegar Word-sniðmátið er tilbúið er hægt á síðunni **Word-sniðmát** að velja **Nota** til að búa til skjölin. Þegar Word-sniðmát er notað í einingu verða gögn úr innfellingarsvæðunum sett inn í skjalið. Annaðhvort er hægt að búa til eitt skjal sem inniheldur hluta fyrir hverja einingu eða valið **Skipta upp** til að búa til nýtt skjal fyrir hverja einingu.

Hægt er að nota aðgerðina **Nota Word-sniðmát** til að nota sniðmát fyrir eina eða fleiri sömu gerð einingar, t.d. viðskiptamann, beint í samhengi síðunnar fyrir einingu. Til dæmis síðurnar **Viðskiptamaður** eða **Lánardrottinn** .

## Nota Word-sniðmát með tölvupósti

Þú getur notað Word-sniðmát til að bæta efni við tölvupóstskeyti. Þegar úr býrð til tölvupóst getur þú valið aðgerðina **Nota Word-sniðmát** til að nota efnið úr sniðmáti fyrir skilaboðin. Sniðmát verða að hafa verið stofnuð fyrir eininguna. Hægt er að nota eitt sniðmát í einu og þegar skipt er á milli sniðmáta breytast skilaboðin til að endurspegla efnið úr völdu sniðmáti.

Þar að auki er hægt að nota aðgerðina **Bæta við skrá úr Word-sniðmáti** til að hengja efni sniðmátsins við tölvupóstinn sem skrá. Skráin mun nota sniðið sem þú tilgreindir fyrir úttak sniðmátsins.

:::image type="content" source="media/email-word-tmpl.PNG" alt-text="Valmöguleikar við notkun efnis úr Word-sniðmáti í tölvupósti":::

## Breyta Word-sniðmáti

Hægt er að gera eftirfarandi breytingar á Word-sniðmátunum:

* Til að breyta texta eða sameiningarreitum í sniðmátinu skal nota aðgerðina **Sækja**, gera breytingarnar og nota svo aðgerðina **Hlaða** upp
* Til að breyta uppruna gagna skal nota aðgerðina **Breyta tengdum einingum** 
* Til að skipta Word-sniðmátinu út fyrir nýtt sniðmát skal nota aðgerðina **Hlaða** upp
* Eyða sniðmátinu

## Sjá einnig

[Stjórna útliti skýrslna og skjala](ui-manage-report-layouts.md)  
[Setja upp tölvupóst](admin-how-setup-email.md)  
