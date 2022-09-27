---
title: Byrjaðu að búa til skipulag
description: Lærðu að búa til skipulag til að sérsníða útlit skýrslu þegar þau eru skoðuð, prentuð eða vistuð.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.search.form: 9650, 9652
ms.date: 03/23/2022
ms.author: jswymer
ms.openlocfilehash: 0b9c74b7bdd81151b2b290db6cae6bed791d5a23
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/19/2022
ms.locfileid: "9534400"
---
# <a name="get-started-creating-report-layouts"></a>Byrja að búa til Skýrsluskipulag

Business Central kemur með mörgum innbyggðum skipan sem hægt er að nota á skýrslurnar. Aðra skipan kann að hafa verið bætt við sem hluta af öðrum viðaukum. En það er líka hægt að búa til eigin skýrslur annað hvort frá grunni eða byggja fyrirliggjandi skipulag.

> [!IMPORTANT]
> Einnig er hægt að nota skýrsluskipulag til að bæta efni í bréfapóstum. Skýrsluútlit getur til dæmis sparað tíma og hjálpað til við að tryggja samræmi með því að endurnýta sama efni þegar þú átt samskipti við viðskiptavini þína. Ef nota á sérsniðna skýrslu með tölvupósti verður skrárgerðin fyrir útlitinu að vera Word. Ekki er hægt að nota RDLC-skrárgerðina. Nánari upplýsingar er að finna [í setja upp endurnýtanlega texta og skipulag](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts). 

## <a name="overview"></a>Yfirlit

Þegar unnið er með útlit skýrslu er auðveldara að hugsa um útlitið sem skrá sem er lesin inn og úthlutuð skýrslu. Óháð útlitagerð, hvernig skipulag í Viðskiptamiðinu er í grundvallaratriðum eins. Oftast er unnið út frá **síðu skýrsluuppsetningar**. Helsti munurinn er hvernig útlitið er hannað, það er gert með því að nota hugbúnaðarhugbúnaðinn sem skipulag er byggt á, eins Word, Excel eða SQL Server Report Smiður.

Með þetta hugtak í huga. Það eru í rauninni þrjú eða fjögur verk sem eiga þátt í að setja upp uppsetningu á skýrslu:

1. Ákvörðun um gerð útlits.
2. Flytja út afrit af fyrirliggjandi útliti sem á að nota sem byrjunarreit.
3. Gera breytingar á Útlitshönnun í viðeigandi forriti.
4. Bæta nýju útlitskrárskránni við skýrsluna.

> [!IMPORTANT]
> Ekki er hægt að breyta eða skipta um framlengingarútlit, sem er skipulag sem á uppruna sinn í framlengingu. Aðeins er hægt að breyta eða skipta um notandaskilgreinda skipan. **Á síðunni skipulag uppsetningar** er hægt að segja til um hvort útlit er fyrir útliti eða Notandaskilgreint útlit með því að skoða **aukadáldálk**. Með viðaukaútliti munu birtast upplýsingar um uppruna eftirnafn í dálkinum. **Viðaukadálkurinn** verður tómur fyrir útlit notandaskilgreindrar.
>
> Til að fræðast um muninn á útliti og notandaskilgreiningu er að finna [í layout Source](ui-manage-report-layouts.md#layout-sources).

## <a name="get-started"></a>Hafist handa

Raunveruleg verkefni eru breytileg eftir því hver staðan er. Notaðu eftirfarandi töflu til að hjálpa þér að byrja.

|Hvað á að gera?|Sjá...|
|-----------------------|------|
|Reikna út hvað er besta útlitsgerðin til að nota fyrir aðstæður mínar|[Ákveðið hvaða gerð af útliti á](#decide)|
|Búa til nýtt útlit fyrir skýrslu sem er byggð á fyrirliggjandi útliti og halda þeirri uppsetningu sem fyrir er.|[Búa til nýtt útlit](#create)|
|Gera breytingar á fyrirliggjandi útliti sem eru notaðar í skýrslu|[Breyta útliti](#modify)|
|Ég er með nýja útgáfu af layout skrá fyrir skýrslu. Ég vil skipta út fyrirliggjandi útlitsskrá.|[Skipta um útlit](#replace)|
|Skipta gildandi útliti úr skýrslu í annað útlit|[Uppsetning á uppsetningu sem notuð er í skýrslu](ui-set-report-layout.md)|
|Breyta heiti og lýsingu á útliti|[Endurnefna útlit](#rename)|

## <a name="decide-what-type-of-layout-you-want"></a><a name="decide"></a> Ákveðið hvaða gerð af útliti á

Það fyrsta þegar stofnað er til útlits er að ákveða hvaða [gerð](ui-manage-report-layouts.md#layout-types) útlits á að vera. Hægt er að velja annað hvort Word, Excel eða RDLC. Gerð útskipanar veltur á því hvernig á að leita að skýrslunni sem mynduð er. Auk þess fer það eftir þekkingu notanda á forritshugbúnaði við stofnun uppsetningar, eins og Word, Excel og SQL Server Report Builder.

<!--
* The process for setting up Word, Excel, and RDLC layouts on reports is the same. The main difference is in the way you modify the layouts. Excel and Word layouts are typically easier to create and modify than RDLC layouts because you use Word and Excel. RDLC report layouts are modified by using SQL Server Report builder, which targets more advanced users.-->

* Excel-útlit er almennt það auðveldasta að stofna og breyta því að aðgerðir til að draga saman gögn, bæta við myndum og stílbreyt eru algengar Excel-aðgerðir.

* Ekki eru allar skýrslur og fylgiskjal með DataSet sem er bestuð til notkunar með Excel útliti. Til dæmis, uppsöfnun og flóknir útreikningar virka best með RDLC eða Ritvinnsluskipan. Sama gildir um skjöl.

* Ef aðeins er verið að gera stílbreytingar eins og leturgerð, stærð og litum, þá er ritútlit líka gott val.

* Því að bæta við gagnasvæðum eða endurraða gagnasvæðum í Word eða RDLC er þrítugt en með Excel.

* Word og RDLC-skipulag er gott að nota fyrir skýrslur sem verða á endanum prentaðar út.  

* Almenn hönnunarhugtök fyrir skipulag Word og RDLC eru svipuð. Hins vegar er hver gerð með tiltekin hönnunareinkenni sem hafa áhrif á það hvernig skýrslan sem mynduð er birtist í [!INCLUDE[prod_short](includes/prod_short.md)]. Í sömu skýrslu gæti litið öðruvísi út þegar Word-útlitið er notað í samanburði við RDLC-útlitið.

## <a name="create-a-new-layout"></a><a name="create"></a> Búa til nýtt útlit

Tvær leiðir eru til að búa til nýtt útlit úr fyrirliggjandi útliti. Ein leið er að vista það útlit sem til er fyrir afrit. Hin leiðin er að flytja út núverandi skipulag.

## <a name="copying"></a>[Afritun](#tab/copy)

Afritun er fljótleg leið til að búa til nýtt útlit sem er eins og tiltækt útlit. Þegar búið er að afrita, verða breytingar gerðar með því að flytja útlitið út. 

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Veljið útlitið sem óskað er eftir eintaki af nýju útlitinu og veljið **síðan Edit info** aðgerðina.

    Ef framlengingarskipan var valin er beðið um hvort breyta eigi afriti. Veldu **Já** til að halda áfram.

    > [!TIP]
    > Til að hjálpa þér að finna útlitið skaltu nota **leitargluggann**, **síurúðuna** og dálkana raða.
3. **Breyta heiti** útlits.
4. **Kveikja á Vista breytingar á afritun** rofa í **on**, velja **síðan í lagi**

   Nýtt skipulag sýnir á **síðu skýrsluuppsetningar**.
5. Ef gera á breytingar á nýju útliti er sjá [breyta fyrirliggjandi útliti](#modify).

### <a name="exportingimporting"></a>[Útflutningur/innflutningur](#tab/export)

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Veljið útlitið sem óskað er eftir eintaki af nýju útlitinu og veljið **síðan aðgerðina útflutningsútlit**.

   Útlitsskráin er sótt í tækið þitt. 

    > [!TIP]
    > Til að hjálpa þér að finna útlitið skaltu nota **leitargluggann**, **síurúðuna** og dálkana raða.

3. Opnið útlitskrárskrána í viðeigandi forriti, eins og Word (fyrir. docx-skrána) eða Excel (fyrir. xlsx File).

   Nánari upplýsingar veitir:

   * [Vinna með Orðskipulag](ui-how-add-fields-word-report-layout.md)
   * [Vinna við Excel-skipulag](ui-excel-report-layouts.md)
   * [Vinna með RDLC-skipan](ui-rdlc-report-layouts.md)

   Gera breytingar á skránni og vista hana.

4. Aftur á **útlit** skýrslunnar er nýja útlitaðgerðin **valin**.
5. Eftirfarandi reitir eru fylltir út:

   |Svæði|Lýsing|Áskilið|
   |-----|-----------|---------|
   |Skýrslukenni|Stilla á KENNIÐ sem skýrslan er tengd|já|
   |Heiti uppsetningar| Sláið inn stutta lýsingu á heitinu til að auðvelda auðvelt að auðkenna það.|já|
   |Lýsing| Sláðu inn ítarlegri upplýsingar um útlitið. |nei|
   |Sniðvalkostir|Stilla þetta svæði til að stemma af gerð útlits, eins og Word, Excel eða RDLC.|já|

6. Veldu **OK** > **Veldu** til að opna skrárexplorer í tækinu.
7. Finna og velja Excel-skrána og velja **síðan opna**.

   Völdu skránni er hlaðið upp í útlitið og síðan er snúið aftur á **síðuna útlit** skýrslu.

Ef þú vilt sjá hvernig skýrslan lítur út með nýja útlitinu skaltu velja útlitið á listanum og velja **síðan Keyra skýrslu**.

---

## <a name="modify-a-layout"></a><a name="modify"></a> Breyta útliti

Fylgdu þessum skrefum til að breyta útliti sem fyrir er Notandaskilgreint.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Velja útlitið sem á að breyta og velja **síðan aðgerðina Flytja út útlit**.

   Útlitsskráin er sótt í tækið þitt. 

   > [!TIP]
   > Til að hjálpa þér að finna útlitið skaltu nota **leitargluggann**, **síurúðuna** og dálkana raða.

3. Opnið útlitskrárskrána í viðeigandi forriti, eins og Word (fyrir. docx-skrána) eða Excel (fyrir. xlsx File).

   Nánari upplýsingar veitir:

   * [Vinna með Orðskipulag](ui-how-add-fields-word-report-layout.md)
   * [Vinna við Excel-skipulag](ui-excel-report-layouts.md)
   * [Vinna með RDLC-skipan](ui-rdlc-report-layouts.md)

   Gera breytingar á skránni og vista hana.

4. Aftur á **síðunni útlit** skýrslu, veljið núverandi útlit og veljið **síðan aðgerðina skipta út**.
5. Veldu **OK** > **Veldu** til að opna skrárexplorer í tækinu.
6. Finna og velja Excel-skrána og velja **síðan opna**.

   Völdu skránni er hlaðið upp í útlitið og síðan er snúið aftur á **síðuna útlit** skýrslu.
7. Ef þú vilt sjá hvernig skýrslan lítur út með nýja útlitinu skaltu velja útlitið á listanum og velja **síðan Keyra skýrslu**.

## <a name="replace-a-layout"></a><a name="replace"></a> Skipta um útlit

Fylgið þessum skrefum til að skipta út gildandi skráasafni fyrir notandaskilgreinda notendur með nýja skrá.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Veljið fyrirliggjandi útlit og veljið **síðan aðgerðina skipta út**.
3. Veldu **OK** > **Veldu** til að opna skrárexplorer í tækinu.
4. Finna og velja Excel-skrána og velja **síðan opna**.

   Völdu skránni er hlaðið upp í útlitið og síðan er snúið aftur á **síðuna útlit** skýrslu.
5. Ef þú vilt sjá hvernig skýrslan lítur út með nýja útlitinu skaltu velja útlitið á listanum og velja **síðan Keyra skýrslu**.

## <a name="rename-a-layout"></a><a name="rename"></a> Endurnefna útlit

Fylgið þessum skrefum ef breyta á heiti og lýsingu á Notandaskilgreindu útliti.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Veljið útlitið sem á að endurnefna og veljið síðan **Edit info** aðgerðina.

    > [!TIP]
    > Til að hjálpa þér að finna útlitið skaltu nota **leitargluggann**, **síurúðuna** og dálkana raða.
3. Breyttu heiti **útlits og veldu** svo í lagi **.**

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig

[Stjórnun skýrsluútlita](ui-manage-report-layouts.md)  
[Unnið með Ritskipulag](ui-how-add-fields-word-report-layout.md)  
[Unnið með Excel-skipulag](ui-excel-report-layouts.md)  
[Unnið með skýrslur, runuvinnslur og XMLports](ui-work-report.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
