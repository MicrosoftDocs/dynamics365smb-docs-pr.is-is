---
title: Vinna með Intrastat-skýrslugerð
description: Lærðu að tilkynna viðskipti með fyrirtæki í öðrum ESB-löndum með notkun Intrastat-kerfis.
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, Intrastat, trade, EU, European Union
ms.search.form: 308, 309, 310, 311, 325, 326, 327, 328, 405, 406, 4810, 4811, 8451, 12202, 31077
ms.date: 09/02/2022
ms.author: altotovi
ms.openlocfilehash: 9da61eb6cb33c2567590ba70b716d54d06c37e9a
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9608480"
---
# <a name="work-with-intrastat-reporting"></a>Vinna með Intrastat-skýrslugerð

Öll fyrirtæki Evrópusambandsins (ESB) verða að tilkynna viðskipti sín með öðrum ríkjum ESB/svæðum. Einnig þarf að gefa hagstofu viðkomandi lands/svæðis mánaðarlega skýrslu um hreyfingu vöru og skýrsluna þarf að afhenda skattayfirvöldum. Intrastat er kerfið til að safna talnagögnum um vörur í þessum löndum/svæðum. Intrastat-skýrsla **er notuð** til að ljúka reglubundinni Intrastat-skýrslugerð (að jafnaði mánaðarlega), söfnun, skráningu og skýrslugjöf um varnir eins og á við um staðbundna löggjöf um stjórnsýslu.

Intrastat-skýrslugerð byggir á grunnreglum ESB sem gilda um öll lönd; í reynd er þó einhver munur innan einstakra landa. Hvert land hefur sínar reglur um hvað nákvæmlega og hvernig á að tilkynna.

> [!IMPORTANT]
> Þessi grein lýsir nýrri Intrastat-reynslu sem er tiltæk [!INCLUDE[prod_short](includes/prod_short.md)] til að ræsa í 2022 losunarbylgju 2, sem felur í sér aukna eiginleika og [verður að vera kveikt á fyrir fyrirtæki sem til eru](finance-how-setup-report-intrastat.md#enable-the-new-intrastat-experience). Hafa skal samband við kerfisstjóra til að skipta á og setja upp nýja möguleika.
>
> Lesa Intrastat-uppsetningu og notkunargrein síðustu útgáfu með [því að setja upp og Intrastat-](finance-how-setup-report-intrastat-v20.md) skýrslu.

> [!NOTE]
> Upplýsingar um Intrastat eiga ekki við um tilfærslu þjónustu milli landa heldur einungis á vörum (vörum og eignum). Ef staðbundin stjórnvöld krefjast skráningar á þjónustu á milli landa er hægt að gera það með **aðgerðinni Þjónustuskýrsla**.
>
> Við eigum nú von á að þessi eiginleiki verði fáanlegur frá nóvember 2022 sem App kl [AppSource](https://go.microsoft.com/fwlink/?linkid=2081646). Að þeim tíma loknum, til að nota hann, verður þú fyrst að setja hann upp á **síðu Framlengingarstjórnunar**.

## <a name="fill-in-the-intrastat-report"></a>Fylla út Intrastat-skýrsluna

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Intrastat-lista** og veljið tengdan tengil.
2. Velja **skal nýja** aðgerð til að stofna nýja **Intrastat-skýrslu**.
3. Ef færa þarf inn innri upplýsingar um **Intrastat-skýrsluna** eru þessar upplýsingar færðar inn í **reitinn Lýsing**.
4. **Í reitnum talnagögn talnagagna** er tilgreindur Mánuðurinn sem á að skrá gögn fyrir. Færið inn tímabilið sem fjögurra stafa tölu með engum bilum eða táknum. Það fer eftir þínu landi hvort þú færð inn mánuðinn fyrst og síðan árið, eða öfugt. Sem dæmi má nefna annaðhvort *2206* eða *0622* fyrir Júní 2022.
5. Veljið aðgerðina **Leggja til línur**. **Reitirnir Upphafsdagsetning** og **Lokadagsetning** hafa þegar innihaldið dagsetningarnar sem eru tilgreindar fyrir talnagagnatímabilið í haus Intrastat-skýrslunnar.
6. Hægt er að færa prósentu í reitinn **Kostnaðarregla %** (til að ná yfir flutning og tryggingar). Ef færð er inn prósenta verður efni reitsins **Upplýsingagildi** í færslubókinni hlutfallslega hærra. En ef nota á þessa aðgerð verður að skipta upphæðinni með **reitnum Kostnaðargjald** í **Já**.
7. Hægt er að setja loksins upp auka afbrigði á **viðbótar** festiflipanum:
   1. **Sleppa endurútreikningi núll upphæðir** til að tilgreina að línur án upphæðar verði ekki endurreiknaðar í keyrslunni.
   2. **Sleppa núlli upphæðir** til að tilgreina að birgðafærslur án upphæðanna verði ekki í keyrslunni.
   3. **Sýna færslur** kostnaðarauka sem á að tilgreina ef Sýna á beinan kostnað sem fyrirtækið hefur úthlutað og bókað sem kostnaðarauka.
   4. **Sleppa færslum** sem ekki eru reikningsfærðar til að tilgreina ef birgðafærslur sem eru sendar eða mótteknar en ekki enn reikningsfærðar verða að vera undanskildar.
8. Smellt er á **Í lagi** til að hefja keyrsluna.

Keyrslan sækir allar birgðafærslur á talnagagnatímabilinu og setur þær inn sem línur í **Intrastat-skýrslulínunum**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="modify-the-intrastat-report"></a>Breyta Intrastat-skýrslu

Ef þörf krefur er hægt að breyta línunum en þegar gildi er breytt í Intrastat-skýrslulínunni er **leiðréttingarreiturinn** sjálfkrafa merktur sem **Já**. Að lokum er hægt að bæta nýrri línu við handvirkt ef ástæða er til þess. Nýrri línu bætt við handvirkt:

1. **Á síðunni Intrastat-skýrsla** skal velja **nýju línuaðgerðina** í **fastflipanum línur**.
2. Valkosturinn Móttaka eða afhending er **valinn í** reitnum Tegund **.** **·**
3. **Í reitnum Tegund** uppruna er ein af heimildum valin: **Birgðafærsla**, **eignafærsla** eða **Verkfærsla**.
4. **Á grundvelli upprunagerð** í **reitnum Vörunr.** er hægt að velja **vöru** (í bæði tilvikum, **birgðafærslu** eða **verkfærslu**) eða **eignum**.
5. Aðrir reitir eru fylltir út eftir þörfum fyrir Intrastat-skýrslugerð.

> [!NOTE]
> Þegar ný lína er bætt handvirkt við Intrastat-skýrslu **verður dagsetningarsvæðið** í línunni innan þess **tímabils** talnagagna sem bætt var við í hausnum.

## <a name="validate-intrastat-lines"></a>Villuleita í Intrastat-línum

Þegar búið er að fylla út **Intrastat-skýrsluna** er hægt að keyra **skýrsluaðgerð** gátlista til að tryggja að allar upplýsingar í **Intrastat-skýrslunni** séu réttar. Skyldusvæði sem búið er að setja upp á **gátlista** Intrastat-skýrslu sem vantar verður sýnt með **villum og viðvörunarupplýsingakassa** á **síðunni Intrastat-skýrsla**.

**Skýrslan Gátlistar** Intrastat-skýrslu er keyrð til að kanna Intrastat-línur áður en þær eru fluttar út í sniðið sem er nauðsynlegt. Ávísunum er keyrt inni í **Intrastat-skýrslunni**.

## <a name="recalculating-weight-or-supplementary-unit-of-measure"></a>Þyngd eða viðbótarmælieiningamælingu

Ef villuboðin *' Heildarþyngd ' í línu Intrastat-skýrslu verður ekki auð* er líklega vegna þess að ekki var búið að **Stilla reitinn Nettóþyngd** á notuðum uppruna, vöru eða eign. Í því tilviki þarf að leita að vörunni eða eignaspjaldinu og bæta við tilskilið gildi. Eftir það þarf bara að opna **Intrastat skýrsluna** og fylgja eftirfarandi:

1. Velja skal **muna. Þyngd/Suppl. UOM** aðgerð til að endurreikna **Heildarþyngd** og/eða **viðbótarmagn**.
2. Veldu einn af valkostunum:

    1. **Þyngd** – til að endurreikna aðeins **Heildarþyngd**, Byggt á gildandi upplýsingum um **nettóþyngd** á vöru og eignaspjöldum.
    2. **Viðbótarmagn** til viðbótar – til að endurreikna aðeins **viðbótarmagnið** **í línu Intrastat-skýrslu** ef það er til, Byggt á gildandi upplýsingum um **aukaverk** á vörunni og eignaspjöldum.
    3. **Hvort tveggja** – til að endurreikna bæði **Heildarþyngd** og **aukamagn**, Byggt á gildandi upplýsingum á vörunni og eignaspjöldum.
3. Smellt er á **Í lagi** til að hefja keyrsluna.

## <a name="report-intrastat-in-a-file"></a>Senda Intrastat-skýrslu sem skrá

Hægt er að senda Intrastat skýrsluna sem skrá sem byggist á mismunandi kröfum sveitarfélaga. Áður en skráin er stofnuð ætti að keyra **gátlistaskýrsluna** til að kanna hvort allar línur innihaldi allar nauðsynlegar og gildar upplýsingar. Skrá búin til:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Intrastat-lista** og veljið síðan tengda tengilinn.
2. Valið **er Intrastat-skýrsla** sem á að tilkynna sem skrá.
3. Hafi þetta ekki þegar verið gert skal fylla út **Intrastat-skýrsluna** handvirkt eða velja **aðgerðina leggja til línur**.
4. Aðgerðin **Stofna Skrá** er valin.
5. Intrastat-skráin verður vistuð með tilskildum sniði.

Þegar þú hefur stofnað skrána, [!INCLUDE[prod_short](includes/prod_short.md)] fyllir sjálfkrafa á eftirfarandi upplýsingar um skýrslugerð:

* **Dagsetning útflutnings** til að tilgreina dagsetninguna þegar skýrslan var flutt út.
* Á **útflutningstíma** til að tilgreina tímann þegar skýrslan hefur verið flutt út.

> [!NOTE]
> Næst þegar skrá **er stofnuð verða reitirnir útflutningstími** **og** útflutningur að geyma aðeins upplýsingar um síðustu skrána.

## <a name="intrastat-rules"></a>Reglur um Intrastat

### <a name="grouping-lines"></a>Flokkun lína

Í **Intrastat-skýrslulínum** er engin flokkun eftir svæðum. Allar færslur eru afritaðar frá upprunalegu frumunni, þannig að fljótlegt er að staðsetja þær samkvæmt samsetningu **upprunagerð** og **Upprunafærslna nr**.

Flokkun sem krafist er af yfirvöldum verður veitt í útfluttu skrá. Stilla þarf þetta í **Gagnaskiptaskilgreiningunni** sem er fullkomlega stillanleg. Frekari upplýsingar er að setja í upplýsingar um [Gagnaflutgengisskilgreiningar](across-how-to-set-up-data-exchange-definitions.md).

### <a name="fixed-assets-reporting"></a>Eignir skýrslur

Eignir verða aðeins sýndar í Intrastat-línum ef:

* **Eignabókunargerðin** í **reitnum VSK-færsla** er **stofnkostnaður** og ef **Tegund** fylgiskjals er **Reikningur** í tilviki innkaupa-og
* Eignabókunargerðin í reitnum VSK-færsla **er** haldið áfram með afskráningu **og ef** Tegund **fylgiskjals er** Reikningur **í tilviki sölu.** **·**

### <a name="intrastat-report-statuses"></a>Stöður Intrastat-skýrslu

Þegar unnið er með **Intrastat-skýrsluna** birtist **Stöðureitur** í haus skjalsins. Eftirtaldar stöður má finna ásamt tilheyrandi reglum:

* *Opna* : Þessi staða er stofnuð sjálfkrafa þegar ný Intrastat-skýrsla er stofnuð og hægt er að gera allar aðgerðir í stöðunni.
* *Losað* : [!INCLUDE[prod_short](includes/prod_short.md)] breytir sjálfkrafa stöðunni í *Útgefin* þegar þú stofnar skrá. Frá því augnabliki er ekki hægt að breyta **Intrastat-skýrslunni**. Ef breyta þarf einhverju og tilkynna aftur er hægt að nota **Opna** aðgerðina til að opna Intrastat-skýrsluna. Þegar skjalið hefur verið enduropnað er hægt að nota **úttektaraðgerðina** til að losa skjalið aftur.
* **Tilkynnt** : Tilgreinir hvort færslan hafi þegar verið tilkynnt skattyfirvöldum. Þetta er ekki venjuleg staða heldur sjálfstæð svæði og jafnvel þótt þú hafir enduropnað Intrastat-skýrsluna þá myndi hún samt sýna að skráin sé þegar stofnuð fyrir þessa skýrslu.

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengdar þjálfun kl [Microsoft Learn](/learn/modules/process-intrastat-dynamics-365-business-central/index).

## <a name="see-also"></a>Sjá einnig .

[Setja upp Intrastat-skýrslugerð](finance-how-setup-report-intrastat.md)  
[Fjármálastjórnun](finance.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
