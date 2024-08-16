---
title: Útflutningur endurskoðunarskráar
description: 'Þessi grein útskýrir hvernig á að setja upp mismunandi útflutningssnið og nota þau síðan, samkvæmt kröfum endurskoðanda eða yfirvalda.'
author: altotovi
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.devlang: al
ms.search.keywords: 'audit, export, SIE, SAF-T, FAC, GDPdU, file export'
ms.search.form: '5260, 5261, 5264, 5266, 5267, 5270'
ms.date: 08/07/2024
ms.author: altotovi
ms.reviewer: bholtorf
---

# <a name="audit-file-export"></a>Útflutningur endurskoðunarskráar

Útflutningur á bókhaldsupplýsingum úr kerfinu er algeng beiðni sumra sveitarfélaga eða endurskoðenda. Útflutningur á sniðum og nauðsynlegum upplýsingum getur verið frábrugðinn. Færslur fyrir útflutning eru yfirleitt fjárhagur (fjárhags-) færslur eða virðisaukaskattsfærslur (VSK). Hins vegar er stundum þörf á öðrum upplýsingum.

**Útflutningur** endurskoðunarskráa er foruppsettur viðbót sem gerir kleift að flytja út mismunandi færslur, byggt á kröfum endurskoðanda eða yfirvalda. Burtséð frá tegund sniðs eða færslna er hægt að nota aðgerð viðbótarinnar til að stýra útflutningsferli gagna. Aðgerðin er ekki með foruppsett skrársnið til útflutnings. Því verður þú annaðhvort að setja upp forrit sem er með sérstöku sniði (til dæmis SIE, SAF-T eða FAC) eða þróa eigin.

> [!NOTE]
> Eins og er getur þú valið SIE (Svíþjóð), FEC (Frakkland) og SAF-T snið sem viðbótarforrit. Samstarfsaðilar geta einnig þróað sérsniðið snið. Fjöldi tiltækra sniða eykst með tímanum.

## <a name="set-up-audit-file-export"></a>Setja upp endurskoðunarskrá útflutning

1. Velja skal leitarhnappinn ![Stækkunarglershnapp sem opnar aðgerðina Segja mér.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera"), færa inn **endurskoðunarskrá Uppsetning** útflutnings og velja síðan viðeigandi tengja.
2. Á síðunni **endurskoðunarskrá Flytja út uppsetningaruppsetningu** skal fylgja eftirfarandi skrefum:

    1. Á flýtiflipanum **Almennt** í reitnum **Endurskoðunarskrá Flytja út sniðskóta** er tilgreindur kóti fyrir sjálfgefið endurskoðunarskrá útflutningssnið. Aðeins þau snið sem voru virkjuð þegar tiltekið skrársnið var sett upp frá Eiginleikastjórnun og þau sem bætt var við sem sérsniðið snið eru tiltæk.
    2. Á flýtiflipanum **Gæði** gagna er gátreiturinn **Kanna stofngögn** til tilkynningar um upplýsingareiti fyrirtækis sem ekki hafa verið rétt settir upp.
    3. Velja skal gátreitinn **Kanna viðskm** . til að fá tilkynningu um reiti sem ekki hafa verið settir upp rétt fyrir tiltekna viðskiptamenn.
    4. Velja skal gátreitinn **Kanna lánardrottin** til að fá tilkynningu um reiti sem ekki hafa verið settir upp rétt fyrir tiltekna lánardrottna.
    5. Velja skal gátreitinn **Tékki bankareiknings** til tilkynningar um reiti sem ekki hafa verið settir upp rétt fyrir tiltekna bankareikninga.
    6. Velja skal gátreitinn **Kanna póstnúmer** til tilkynningar um póstnúmer sem ekki hefur verið sett upp rétt.
    7. Velja skal gátreitinn **Tékkaaðsetur** sem á að tilkynna þegar aðsetur hefur ekki verið rétt sett upp.
    8. Í reitinn **Sjálfgefið póstnúmer** er fært inn póstnúmerið sem á að nota ef ekkert póstnúmer er tilgreint á spjaldi viðskiptamanns eða lánardrottins.

3. Hnappurinn Leitarhnappurinn ![Stækkunargler opnar aðgerðina Segja mér er](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") valinn, slegið inn **endurskoðunarskrá Uppsetning útflutningssniðs** og tengd tengja valið.
4. Á síðunni **endurskoðunarskrá Uppsetning útflutningssniðs** skal fylgja eftirfarandi skrefum:

    1. Velja skal endurskoðunarskrá útflutningssniðið sem á að grunnstilla. Aðeins þau snið sem voru virkjuð þegar tiltekið skrársnið var sett upp frá Eiginleikastjórnun og þau sem bætt var við sem sérsniðið snið eru tiltæk.
    2. Í reitnum **endurskoðunarskrá Heiti** er tilgreint sjálfgefið skrárheiti eða skrárheitissniðmát fyrir endurskoðunarskrá sem á að flytja út.
    3. Velja skal gátreitinn **Safn til zip** til að nota sjálfkrafa útfluttar skrár.

## <a name="provide-the-gl-account-mapping-for-audit-file-export"></a>Veita fjárhagsreikningnum vörpun fyrir útflutning endurskoðunarskrá

Flest snið sem yfirvöld þurfa fyrir fjárhagsreikninga krefjast sérstaks staðlaðs bókhaldslykils. Þess vegna er útflutt skráin byggð á vörpunum þegar fjárhagsreikningar hafa verið grunnstilltir. Hægt er að nota fleiri vörpun í kerfinu.

Fylgið þessum skrefum til að veita fjárhagsreikningnum vörpun fyrir endurskoðunarskrá útflutning.

1. Velja skal leitarhnappinn ![Stækka glerhnapp sem opnar aðgerðina Segja mér.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera"), færa inn **vörpun fjárhagsreikning** og velja síðan viðeigandi tengja.
2.  **Á vörpun síðu fjárhagsreiknings**  er Ný valið **til** að stofna vörpun.
3. Í reitnum **Kóti** er tilgreindur vörpun kóti sem táknar skýrslutímabilið.
4. Í reitnum **Tegund** staðlaðs reiknings er valin tegund staðlaðra fjárhagsreikninga.
5. Í reitnum **endurskoðunarskrá Útflutningssnið** er tilgreint endurskoðunarskrá útflutningssniðið sem staðlaðir fjárhagsreikningar eru tengdir við.
6. Í reitnum **Tegund** tímabils tilgreinir kerfið reikningstímabil eða sérsniðna tímabilstegund með sveigjanlega upphafsdagsetningu og tíma samkvæmt því sem valið var. Ef valið er tiltekið reikningstímabil er reiturinn stilltur á **Reikningstímabil**. Annars er hún stillt á **Gagnasvið**.
7. Í reitnum **Reikningstímabil** er tilgreind upphafsdagsetning reikningstímabilsins sem á að nota sem skýrslutímabil ef það á að vera eins.
8. Ef reiturinn **Reikningstímabil** **er stilltur eru reitirnir Upphafsdagsetning** og **Lokadagsetning** sjálfkrafa stilltir á grundvelli þess tímabils sem var tilgreint. Annars er hægt að stilla upphafs- og lokadagsetningar fyrir skýrslugerð handvirkt.
9. Ef staðlaðum bókhaldslykli hefur þegar verið bætt við skal fylgja eftirfarandi skrefum:

    1. Í reitnum Flokksnr **. staðlaðs reiknings** Skal tilgreina tegund staðlaða reikningsins eða flokkunarkótans sem notaður er fyrir vörpun.
    2. Í reitnum **Stöðluð reikningur nr.** skal tilgreina staðlaða reikningskótann eða flokkunarkótann sem notaður er fyrir vörpun.

10.  **Velja skal gátreitinn Taka innfærða stöðu** með til að taka tillit til innfærðrar stöðu fjárhagsreiknings af gerðinni **Efnahagsreikningur** fyrir vörpun í stað hreyfingar á skýrslutímabilinu.
11. Til að hefja vörpun skal fylgja eftirfarandi skrefum:

    1. Til að búa til línur á **vörpun síðu fjárhagsreiknings**, á grundvelli fyrirliggjandi bókhaldslykils, er Uppruni valinn **frumstilla fyrir vörpun**. Ef afrita á fjárhagsreikninginn vörpun úr öðrum vörpun kóta er Afrita úr öðrum vörpun **valið**. Þegar lokið hefur verið við að búa til línur verða allir fjárhagsreikningar sem hafa bókaðar færslur merktir með grænum hætti.
    2. Til að merkja aðeins fjárhagsreikninga með færslum er valið **Uppfæra til ráðstöfunar** fjárhagsfærslu. Ef valkosturinn **Taka innstöðu** með er virkjaður eru allar bókaðar fjárhagsfærslur teknar með við útreikninga. Annars eru aðeins tillit til fjárhagsfærslna skýrslutímabilsins.

## <a name="export-the-audit-file"></a>Flytja út endurskoðunarskrá

1. Hnappurinn Leitarhnappurinn ![Stækkunargler opnar aðgerðina Segja mér er](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") valinn endurskoðunarskrá **Flytja út skjöl** og velja síðan viðeigandi tengja.
2. Á síðunni **endurskoðunarskrá Flytja út skjöl** skal velja **Nýtt**.
3. Á flýtiflipanum **Almennt** skal fylgja eftirfarandi skrefum:

    1. Í reitnum **endurskoðunarskrá Flytja út snið** er valið sniðið sem er notað til að flytja út endurskoðunarskrá.
    2. Í reitnum **Vörpun kóti** fjárhagsreiknings er valinn kóti fjárhagsreiknings vörpun fyrir skýrslutímabilið.
    3. Gátreiturinn **Skipta eftir mánuðum** er valinn ef mynda á margar endurskoðunarskrár fyrir hvern mánuð.
    4. Gátreiturinn **Skipta eftir dagsetningu** er valinn ef búa á til margar endurskoðunarskrár á dag.
    5. Í reitinn **Athugasemd** hauss er færð inn athugasemd á endurskoðunarskrá haus.
    6. Í reitnum **Tengiliður** er tilgreindur tengiliðurinn sem hefur verið fluttur út í haus endurskoðunarskrá.
    7. Velja skal gátreitinn **Stofna fleiri en einingarskrár** til að búa til margar zip-skrár.

        > [!IMPORTANT]
        > Aðeins skal velja þennan gátreit ef einhver sniðforrit voru sett upp áður eða sérsniðið var búið til. Uppsetning eins eða fleiri tilgreindra sniða bætir líklega reitum og aðgerðum við **útflutningsaðgerðina Útflutningur** endurskoðunarskráa, byggt á sniðþörfum.

4. Á flýtiflipanum **Vinnsla** skal fylgja eftirfarandi skrefum:

    1. Gátreiturinn Samhliða **vinnslu** er valinn ef vinna á endurskoðunarskrá með samhliða bakgrunnsvinnslum. Hreinsið gátreitinn til að flytja út gögn í núgildandi lotu.
    2. Ef gátreiturinn Samhliða **vinnslu** var valinn er í reitnum **Hámarksnr. Í reitnum Verk** er tilgreindur hámarksfjöldi bakgrunnsverka sem hægt er að keyra samtímis.
    3. Í reitnum **Fyrsta upphafsdagsetning/-tími** skal tilgreina elstu dagsetningu og tíma þegar keyra þarf bakgrunnsverkið. Ef ferlið er keyrt með því að velja Byrjun **er** hægt að rekja stöðuna á **flýtiflipunum Vinnsla** og **Línur** .

5. Þegar lokið er við er Sækja sem skrá **valið** til að sækja endurskoðunarskrá fyrir völdu línuna.

> [!IMPORTANT]
> Ef margar færslur eru til útflutnings er ekki mælt með því að þær séu fluttar út í þessari lotu vegna hugsanlegra vandamála við afköst. Þess í stað er mælt með því að notuð sé samhliða vinnsla á virkum dögum eða klukkustundum.

## <a name="see-also"></a>Sjá einnig .
[Fjármálastjórnun](finance.md)    
[Að átta sig á fjárhagur og bókhaldslykli](finance-general-ledger.md)    
[Vinna með víddir](finance-dimensions.md)    
[Vinna með Business Central](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
