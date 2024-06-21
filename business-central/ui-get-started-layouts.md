---
title: Hefjast handa við að búa til útlit
description: 'Kynntu þér hvernig skal búa til útlit til að sérsníða útlit skýrslu þegar hún er skoðuð, prentuð eða vistuð.'
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9650, 9652'
ms.date: 03/23/2022
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---
# <a name="get-started-creating-report-layouts"></a>Hefjast handa við að búa til skýrsluútlit

Business Central kemur með mikið af innbyggðu útliti sem hægt er að nota á skýrslur. Það getur verið að fleiri útlitum hafi verið bætt við sem hluti af öðrum viðbótum. En einnig er hægt að búa til eigin skýrslur annaðhvort frá grunni eða út frá fyrirliggjandi útliti.

> [!IMPORTANT]
> Einnig er hægt að nota skýrsluútlit til að bæta efni við tölvupóstskeyti. Til dæmis getur skýrsluútlit sparað tíma og tryggt samræmi með því að endurnota sama efnið þegar haft er samband við viðskiptamenn. Til að nota sérsniðið skýrsluútlit með tölvupósti verður skráargerðin fyrir útlitið að vera Word. Ekki er hægt að nota RDLC-skráargerðina. Frekari upplýsingar eru í [Setja upp endurnýtanlega texta og útlit tölvupósts](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts). 

## <a name="overview"></a>Yfirlit

Þegar unnið er með skýrsluútlit hjálpar það að hugsa um útlit sem skrá sem flutt er inn og úthlutað á skýrslu. Hvernig þú stjórnar útlitum í Business Central er nánast það sama burtséð frá útlitsgerðinni. Yfirleitt er unnið á síðunni **Skýrsluútlit**. Helsti munurinn er hvernig maður hannar útlitið, sem er gert með því að nota hugbúnaðinn sem útlitið byggir á, eins og Word, Excel eða SQL Server Report Builder.

Með þessa hugmynd í huga. þrjú eða fjögur verk eru hluti af uppsetningu útlits í skýrslu:

1. Taktu ákvörðun um útlitsgerðina.
2. Flyttu út afrita af fyrirliggjandi útliti til að nota sem upphafspunkt.
3. Gerðu breytingar á útlitsskránni í viðeigandi forriti.
4. Bæta nýju útlitsskránni við skýrsluna.

> [!IMPORTANT]
> Ekki er hægt að breyta eða skipta um útlitsviðbót sem er útlit sem á uppruna sinn í viðbót. Aðeins er hægt að breyta eða skipta um útlit sem er skilgreint af notendum. Á síðunni **Skýrsluútlit** er hægt að sjá hvort útlit er útlitsviðbót eða notandaskilgreint útlit með því að skoða dálkinn **Viðbót**. Útlitsviðbót sýnir upplýsingar um uppruna viðbótar í dálkinum. Dálkurinn **Viðbót** verður auður fyrir notandaskilgreint útlit.
>
> Til að fræðast um muninn á útlitsviðbótum og notandaskilgreindum útlitum skal skoða [Uppruni útlits](ui-manage-report-layouts.md#layout-sources).

## <a name="get-started"></a>Hafist handa

Verkefnin eru mismunandi eftir því hver staðan er hjá þér. Notaðu eftirfarandi töflu til að koma þér af stað.

|Hvað á að gera?|Sjá...|
|-----------------------|------|
|Finndu út hvaða hver er besta útlitsgerðin til að nota fyrir mínar aðstæður|[Taka ákvörðun um hvers konar útlit þú vilt](#decide)|
|Búðu til nýtt útlit fyrir skýrslu sem byggir á fyrirliggjandi útliti og halda fyrirliggjandi útliti óbreyttu.|[Búa til nýtt útlit](#create)|
|Gera breytingar á fyrirliggjandi útliti sem notað er í skýrslu|[Breyta útliti](#modify)|
|Ég er með nýja útgáfu af útlitsskrá fyrir skýrslu. Ég vil skipta út fyrirliggjandi útlitsskrá.|[Skipta um útlit](#replace)|
|Skipta núverandi útliti sem skýrsla notar yfir í annað útlit|[Setja upp útlitið sem skýrsla notar](ui-set-report-layout.md)|
|Breyta heiti og lýsingu útlits|[Endurnefna útlit](#rename)|

## <a name="decide-what-type-of-layout-you-want"></a><a name="decide"></a>Taktu ákvörðun um hvers konar útlit þú vilt nota

Það fyrsta sem þarf að gera þegar útlit er búið til er að ákveða hvaða [útlitsgerð](ui-manage-report-layouts.md#layout-types) maður vill. Þú getur valið annað hvort Word, Excel eða RDLC. Útlitsgerðin fer eftir því hvernig þú vilt að mynduð skýrsla komi til með að líta út. Auk þess fer það eftir þekkingu þinni á hugbúnaðinum til að búa til útlit, eins og Word, Excel og SQL Server Report Builder.

<!--
* The process for setting up Word, Excel, and RDLC layouts on reports is the same. The main difference is in the way you modify the layouts. Excel and Word layouts are typically easier to create and modify than RDLC layouts because you use Word and Excel. RDLC report layouts are modified by using SQL Server Report builder, which targets more advanced users.-->

* Excel-útlit er almennt auðveldast að búa til og breyta vegna þess að eiginleikarnir til að taka saman gögn, bæta við myndum og stíl eru algengir eiginleikar í Excel.

* Ekki eru allar skýrslur og skjöl með gagnasafn sem er fínstillt til að nota með Excel-útliti. Til dæmis virka uppsafnanir og flóknir útreikningar best með RDLC eða Word-útliti. Það sama á við um skjöl.

* Ef aðeins eru gerðar stílbreytingar eins og leturgerð, stærð, litur er Word-útlit líka góður kostur.

* Að bæta við gagnareitum eða endurraða gagnareitum í Word eða RDLC er þróaðra en í Excel.

* Word- og RDLC-útlit eru góð til að nota fyrir skýrslur sem verða að lokum prentaðar.  

* Almenna hönnunin fyrir Word og RDLC-útlit eru svipaðar. Hins vegar er hver gerð með tiltekin hönnunareinkenni sem hafa áhrif á það hvernig skýrslan sem mynduð er birtist í [!INCLUDE[prod_short](includes/prod_short.md)]. Sama skýrslan gæti litið öðruvísi út þegar Word-útlit er notað í samanburði við RDLC-útlit.

## <a name="create-a-new-layout"></a><a name="create"></a>Búa til nýtt útlit

Til eru tvær leiðir til að búa til nýtt útlit úr fyrirliggjandi útliti. Ein leið er að vista fyrirliggjandi útlit í afrit. Hin leiðin er að flytja út fyrirliggjandi útlit.

## [Afrita](#tab/copy)

Afritun er fljótleg leið til að búa til nýtt útlit sem er það sama og fyrirliggjandi útlit. Þegar þú ert með afritið gerirðu breytingar með því að flytja út útlitið. 

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Veldu útlitið sem á að taka afrit af fyrir nýja útlitið, veldu síðan aðgerðina **Breyta upplýsingum**.

    Ef þú valdir útlitsviðbót verður þú spurð(ur) hvort þú viljir breyta afritinu. Til að halda áfram skaltu velja **Já**.

    > [!TIP]
    > Til að hjálpa þér að finna útlitið skaltu nota reitinn **Leita**, svæðið **Sía** og dálkaröðun.
3. Breyttu **Heiti útlits**.
4. Snúðu rofanum **Vista breytingar á afriti** á **Kveikt**, veldu síðan **Í lagi**.

   Nýja útlitið birtist á síðunni **Skýrsluútlit**.
5. Ef þú vilt gera breytingar á nýja útlitinu skaltu skoða [Breyta fyrirliggjandi útliti](#modify).

### [Útflutningur/innflutningur](#tab/export)

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Veldu útlitið sem þú vilt fá afrit af fyrir nýja útlitið og veldu síðan aðgerðina **Flytja út útlit**.

   Útlitsskránni er hlaðið niður í tækið þitt. 

    > [!TIP]
    > Til að hjálpa þér að finna útlitið skaltu nota reitinn **Leita**, svæðið **Sía** og dálkaröðun.

3. Opnaðu útlitsskrána í viðeigandi forriti, eins og Word (fyrir .docx-skrá) eða Excel (fyrir .xlsx-skrá).

   Frekari upplýsingar má finna á

   * [Vinna með Word-útlit](ui-how-add-fields-word-report-layout.md)
   * [Vinna með Excel-útlit](ui-excel-report-layouts.md)
   * [Vinna með RDLC-útlit](ui-rdlc-report-layouts.md)

   Gerðu breytingar á skránni og vistaðu hana.

4. Í **Skýrsluútlitinu** skaltu velja aðgerðina **Nýtt útlit**.
5. Fyllið inn eftirfarandi reiti:

   |Svæði|Lýsing|Áskilið|
   |-----|-----------|---------|
   |Skýrslukenni|Stillt á auðkennið sem skýrslunni er úthlutað|já|
   |Heiti uppsetningar| Sláðu inn stutt lýsandi heiti á útlitinu til að auðvelda þér að finna það.|já|
   |Lýsing| Sláðu inn nákvæmari upplýsingar um útlitið. |nei|
   |Sniðvalkostir|Stilltu þennan reit á að samsvara gerð útlitsins, eins og Word, Excel eða RDLC.|já|

6. Velja skal **Í lagi** og gera síðan eitt af eftirfarandi skrefum til að hlaða upp útlitsskránni fyrir skýrsluna:

   [!INCLUDE[file-upload](includes/file-upload.md)]

   Valdri skrá er hlaðið upp í útlitið og þú ferð aftur á síðuan **Skýrsluútlit**.

Ef þú vilt sjá hvernig skýrslan lítur út með nýja útlitinu skaltu velja útlitið á listanum og velja svo **Keyra skýrslu**.

---

## <a name="modify-a-layout"></a><a name="modify"></a>Breyta útliti

Fylgdu þessum skrefum til að breyta fyrirliggjandi notandaskilgreindu útliti.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Veldu útlitið sem á að breyta, veldu síðan aðgerðina **Flytja út útlit**.

   Útlitsskránni er hlaðið niður í tækið þitt. 

   > [!TIP]
   > Til að hjálpa þér að finna útlitið skaltu nota reitinn **Leita**, svæðið **Sía** og dálkaröðun.

3. Opnaðu útlitsskrána í viðeigandi forriti, eins og Word (fyrir .docx-skrá) eða Excel (fyrir .xlsx-skrá).

   Frekari upplýsingar má finna á

   * [Vinna með Word-útlit](ui-how-add-fields-word-report-layout.md)
   * [Vinna með Excel-útlit](ui-excel-report-layouts.md)
   * [Vinna með RDLC-útlit](ui-rdlc-report-layouts.md)

   Gerðu breytingar á skránni og vistaðu hana.

4. Á síðunni **Skýrsluútlit** skaltu velja fyrirliggjandi útlit, síðan velja aðgerðina **Skipta um útlit**.
5. Veldu **Í lagi** > **Veldu** til að opna skráavafrann í tækinu þínu.
6. Finndu og veldu Excel skrána og veldu síðan **Opna**.

   Valdri skrá er hlaðið upp í útlitið og þú ferð aftur á síðuan **Skýrsluútlit**.
7. Ef þú vilt sjá hvernig skýrslan lítur út með nýja útlitinu skaltu velja útlitið á listanum og velja svo **Keyra skýrslu**.

## <a name="replace-a-layout"></a><a name="replace"></a>Skipta um útlit

Fylgdu þessum skrefum til að skipta út fyrirliggjandi notandaskilgreinda útlitsskrá fyrir nýja skrá.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Veldu fyrirliggandi útlit, veldu svo aðgerðina **Skipta um útlit**.
3. Veldu **Í lagi** > **Veldu** til að opna skráavafrann í tækinu þínu.
4. Finndu og veldu Excel skrána og veldu síðan **Opna**.

   Valdri skrá er hlaðið upp í útlitið og þú ferð aftur á síðuan **Skýrsluútlit**.
5. Ef þú vilt sjá hvernig skýrslan lítur út með nýja útlitinu skaltu velja útlitið á listanum og velja svo **Keyra skýrslu**.

## <a name="rename-a-layout"></a><a name="rename"></a>Endurnefna útlit

Fylgdu þessum skrefum ef þú vilt breyta heiti og lýsingu á notandaskilgreindu útliti.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Veldu útlitið sem þú vilt endurnefna, veldu síðan aðgerðina **Breyta upplýsingum**.

    > [!TIP]
    > Til að hjálpa þér að finna útlitið skaltu nota reitinn **Leita**, svæðið **Sía** og dálkaröðun.
3. Breyttu **Heiti útlits**, veldu síðan **Í lagi**.

## <a name="see-also"></a>Sjá einnig

[Stjórnun skýrsluútlita](ui-manage-report-layouts.md)  
[Unnið með Word-útlit](ui-how-add-fields-word-report-layout.md)  
[Unnið með Excel-útlit](ui-excel-report-layouts.md)  
[Unnið með skýrslur, runuvinnslur og XMLports](ui-work-report.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
