---
title: Nota Word sniðmát fyrir Fjöldasamskipti
description: Word-sniðmát geta auðveldað að búa til mörg skjöl í einu sem eru sérsniðin fyrir tilteknar einingar.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/01/2023
ms.custom: bap-template
ms.search.forms: '9989, 13,'
---

# <a name="use-word-templates-for-bulk-communication"></a><a name="use-word-templates-for-bulk-communication"></a><a name="use-word-templates-for-bulk-communication"></a>Nota Word-notuð fyrir mörg samskipti í einu

Microsoft Word-sniðmát geta auðveldað mörg samskipti í einu á prenti eða í tölvupósti með einingum á borð við tengiliði, viðskiptamenn og lánardrottna. Til dæmis er hægt að stofna:

* Bæklingar til að hafa viðvaranir til viðskiptavina um söluherferð
* Bréf til að upplýsa lánardrottna um nýja innkaupastefnu
* Boð um að laða tengiliði á komandi viðburði

> [!NOTE]
> Þegar Word sniðmát eru sett upp þarf að nota tæki með  Microsoft Word  2019 eða nýrri og Windows-stýrikerfið uppsett.

## <a name="set-up-the-source-of-data"></a><a name="set-up-the-source-of-data"></a><a name="set-up-the-source-of-data"></a>Setja upp uppruna gagna

Notið einingar í  [!INCLUDE[prod_short](includes/prod_short.md)]  sem Uppruni gagna fyrir sniðmátið og bætið blöndunarsvæðum við til að sérsníða skjöl fyrir hverja einingu. Innfellingarsvæðin koma úr einingunni í [!INCLUDE[prod_short](includes/prod_short.md)]. Þegar Word-sniðmát er notað í einingu verða gögn úr innfellingarsvæðunum sett inn í skjalið.

 **Á síðunni Word-sniðmát**  þegar nýtt sniðmát er búið til aðstoðar Uppsetningarleiðbeiningar með eftirfarandi skrefum:

1. Velja skal einn eða fleiri einingar sem nota á sem uppruna gagnanna. Til dæmis, ef óskað er eftir að stofna bækling fyrir söluherferð er líklega hægt að velja einingareininguna sem Uppruninn.
2. Velja aðra aðila sem auka uppruna gagna.  [Frekari upplýsingar um bæta við færslum sem eru tengdar eða ótengdar Upprunaeiningunni](#add-entries-that-are-related-or-unrelated-to-the-source-entity).
3. Sækja autt sniðmát. Hægt er að setja upp sniðmátið í Word strax, annars getur þú hlaðið upp auðu sniðmátinu og klárað leiðbeiningarnar. Þegar sniðmátið er tilbúið skal nota  **upphleðsluaðgerðina**  á  **síðunni Word-sniðmát**  til að skipta út auðu sniðmátinu með tilbúnu sniðmátinu. Læra meira at  [Stilla upp sniðmátið í Word](#set-up-the-template-in-word).
4. Hlaða upp sniðmátinu sem þú hefur undirbúið.
5. Ritaður er kóti og heiti sem auðkennir sniðmátið.

Þegar sniðmát er sótt fæst. zip-skrá sem inniheldur tvær skrár.

|Skrá  |Description  |
|---------|---------|
|Gagnagjafi. xlsx     | Gagnagjafaskráin býður upp á reitina sem hægt er að nota í sniðmátinu. Ekki breyta upprunaskrá gagnagjafa. Aðeins er hægt að nota Word sniðmátið og skrár gagnagjafa sem sóttar eru og geyma verður skrárnar á sama stað.     |
|Word-sniðmát     | A. docx-skrá sem nota á sem sniðmát.        |

Til að fræðast um uppsetningu sniðmáts í Word er farið í að  [Setja upp sniðmát í Word](#set-up-the-template-in-word).

## <a name="add-entries-that-are-related-or-unrelated-to-the-source-entity"></a><a name="add-entries-that-are-related-or-unrelated-to-the-source-entity"></a><a name="add-entries-that-are-related-or-unrelated-to-the-source-entity"></a>Bæta við færslum sem eru tengdar eða ótengdar upprunaeiningunni

Einnig er hægt að sameina gögn frá öðrum einingum. Ef bæta á öðrum einingum við sem gagnagjafa er notuð ein af eftirfarandi aðgerðum á  **síðunni Word-sniðmát**  eða þegar leiðbeiningar um uppsetningu á aðstoðarmanni eru notaðar:

|Aðgerð  |Description  |
|---------|---------|
|**Bæta við tengdri einingu**  | Nota gögn úr einingum sem tengjast upprunaeiningunni. Til dæmis, fyrir einingareininguna er einnig hægt að sameina gögn úr Tengiliðaeiningunni. Einingar tengjast þegar svæði í einni einingu vísar til annars. Svæði á Viðskiptamannseininu vísar til reita í einingunni Tengiliður, svo þeir séu skyldir. Samnýtta svæðið er oft auðkenni eins og heiti, Kóti eða AUÐKENNI.        |
|**Bæta við ótengdu einingu**| Nota gögn úr einingum sem ekki tengjast upprunaeiningunni. Til dæmis er hægt að búa til sniðmát fyrir Viðskiptavinareininguna. Hægt væri að bæta við einingunni fyrirtæki upplýsingum svo hægt sé að hafa tengiliðalýsingar. Lykilávinningur er sá að ef upplýsingum um tengilið er breytt uppfærist hún sjálfkrafa í sniðmátinu. Þegar ótengdu einingunni er bætt við er hægt að bæta við einingum sem tengjast honum.         |

Fyrir ótengdar færslur er ákveðin færsla valin. Þar sem aðeins er hægt að bæta við einingunni einu sinni til að nota aðra færslu verður að eyða einingunni og bæta henni við aftur með nýju færslunni.

Hægt er að stofna stigveldi eininga, bæði tengt og ótengt. Tengslin eru sýnd sem trjábygging.  **Svæðið einingarvensl**  sýnir einnig upplýsingar um tengslin. Fyrir ótengdar einingar sýnir svæðið færsluna sem stofnar tengslin.

Þegar einingum er bætt við eru þær  **notaðar í svæðið forskeyti**  til að tilgreina forskeyti fyrir svæðanöfn. Síðar, þegar reitum er bætt við sniðmátið, hjálpar forskeytið til að greina milli svæða frá upprunnum og öðrum einingum.

### <a name="select-the-fields-to-include"></a><a name="select-the-fields-to-include"></a><a name="select-the-fields-to-include"></a>Velja svæðin sem eiga að vera með

Fyrir hverja einingu er hægt að tilgreina svæðin sem eiga að vera tiltæk fyrir sniðmátið. Velja skal númerið í  **fjölda valinna reita**  dálka til að fá aðgang að lista yfir svæði sem eru tiltæk.  **Notið**  gátreitinn í gátreitnum taka  **með til að tilgreina svæðin á svæðinu** . Fyrir suma aðila eru reitir sem fyrirtæki nota yfirleitt sjálfkrafa teknir með. Hægt er að breyta listanum, til dæmis til að fjarlægja sjálfgefna reiti. Breytingarnar eiga aðeins við sniðmátið sem unnið er í.

> [!NOTE]
> Heildarfjöldi reita sem hægt er að bæta við úr öllum einingum er 250.

> [!NOTE]
> Þú eða Microsoft Partner þinn geta bætt sérsniðuðum svæðum við einingar. Þegar þú gerir það forskeyti ég heiti reita með  **Calc**  og læt þá tegund  **svæðisins reiknast**. Tegund svæðis kallast reiknað til að gefa til kynna að svæðið geti sýnt mismunandi gerðir gilda, svo sem texta, tölur, dagsetningar o. s. frv.

## <a name="to-create-a-word-template-in-business-central"></a><a name="to-create-a-word-template-in-business-central"></a><a name="to-create-a-word-template-in-business-central"></a>Búa til Word-sniðmát í Business Central

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Word-sniðmát** og velja síðan viðkomandi tengil.
2. Veldu **Nýtt**, síðan **Búa til sniðmát** og fylgdu síðan eftirfarandi skrefum í uppsetningu með hjálp. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Einnig er hægt að búa til sniðmát beint af síðunni fyrir einingu með því að velja aðgerðina **Nota Word-sniðmát** til að opna hjálparuppsetninguna og síðan **Nýtt sniðmát**. Þegar þú gerir það er gagnagjafinn valinn fyrir þig út frá gerð einingarinnar.

## <a name="set-up-the-template-in-word"></a><a name="set-up-the-template-in-word"></a><a name="set-up-the-template-in-word"></a>Sniðmát sett upp í Word

Þegar verið er að setja upp sniðmát í Word á  **flipanum póstsendingar**  er hægt að bæta við blöndunarsvæðum með því að velja  **Setja inn blöndunarsvæði**. Blöndunarreitirnir koma úr gagnaveituskránni sem sótt var um fyrir eininguna. Þau virka sem staðgenglar sem segja Word hvar í skjalinu á að setja upplýsingarnar um eininguna.

:::image type="content" source="media/word-tmpl-merge-field.PNG" alt-text="Innfellingarsvæðum bætt við í Microsoft Word":::

## <a name="apply-a-template"></a><a name="apply-a-template"></a><a name="apply-a-template"></a>Nota sniðmát

Þegar Word-sniðmátið er tilbúið er hægt á síðunni **Word-sniðmát** að velja **Nota** til að búa til skjölin. Þegar Word-sniðmát er notað í einingu verða gögn úr innfellingarsvæðunum sett inn í skjalið. Annaðhvort er hægt að búa til eitt skjal sem inniheldur hluta fyrir hverja einingu eða valið **Skipta upp** til að búa til nýtt skjal fyrir hverja einingu.

Hægt er að nota  **aðgerðina nota Word-sniðmát**  til að nota sniðmát fyrir eina eða fleiri af sömu gerð einingarinnar, til dæmis viðskiptavin, beint í samhengi síðunnar fyrir eininguna. Til dæmis  **viðskiptamanna-eða**  lánardrottnasíðurnar **·** .

## <a name="use-word-templates-with-email"></a><a name="use-word-templates-with-email"></a><a name="use-word-templates-with-email"></a>Notaðu Word sniðmát með tölvupósti

Þú getur notað Word-sniðmát til að bæta efni við tölvupóstskeyti. Þegar úr býrð til tölvupóst getur þú valið aðgerðina **Nota Word-sniðmát** til að nota efnið úr sniðmáti fyrir skilaboðin. Stofnuð verða sniðmát fyrir eininguna. Hægt er að nota eitt sniðmát í einu og þegar skipt er á milli sniðmáta breytast skilaboðin til að endurspegla efnið úr völdu sniðmáti.

Þar að auki er hægt að nota aðgerðina **Bæta við skrá úr Word-sniðmáti** til að hengja efni sniðmátsins við tölvupóstinn sem skrá. Skráin mun nota sniðið sem þú tilgreindir fyrir úttak sniðmátsins.

:::image type="content" source="media/email-word-tmpl.PNG" alt-text="Valmöguleikar við notkun efnis úr Word-sniðmáti í tölvupósti":::

## <a name="edit-a-word-template"></a><a name="edit-a-word-template"></a><a name="edit-a-word-template"></a>Ritfærslusniðmáti breytt

Hægt er að gera eftirfarandi breytingar á Word sniðmátunum:

* Ef breyta á meginmáli megintexta eða blöndunarsvæða í sniðmátinu skal nota  **aðgerðina Sækja**, gera breytingarnar og nota  **síðan upphleðsluaðgerðina** 
* Ef breyta á uppruna gagna er notuð  **aðgerðin breyta tengdum einingum** 
* Ef skipta á um Word sniðmátinu með nýju sniðmáti skal nota  **upphleðsluaðgerðina** 
* Eyða sniðmátinu

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Sjá einnig

[Stjórna útliti skýrslna og skjala](ui-manage-report-layouts.md)  
[Setja upp tölvupóst](admin-how-setup-email.md)  
