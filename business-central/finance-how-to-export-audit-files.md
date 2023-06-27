---
title: Útflutningur endurskoðunarskráar
description: Í greininni er útskýrt hvernig á að setja upp mismunandi útflutningssnið og nota þau síðan samkvæmt kröfum endurskoðanda eða yfirvalda.
author: altotovi
ms.service: dynamics365-business-central
ms.topic: how-to
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'audit, export, SIE, SAF-T, FAC, GDPdU, file export'
ms.search.form: '5260, 5261, 5264, 5266, 5267, 5270'
ms.date: 04/04/2023
ms.author: altotovi
ms.reviewer: kfend
---

# <a name="audit-file-export"></a>Útflutningur endurskoðunarskráar

Útflutningur á upplýsingum um bókhald úr kerfinu er sameiginleg beiðni hjá einhverjum sveitarstjórnum eða endurskoðendum. Útflutningur sniða og nauðsynlegra upplýsinga getur verið mismunandi. Færslur fyrir útflutning eru yfirleitt fjárhagsfærslur (fjárhagsfærslur eða virðisauka-eða virðisaukandi færslur). Hins vegar er stundum krafist annarra upplýsinga.

**Útflutningur**  endurskoðunarskrár er foruppsett nafnauki sem leyfir notanda að flytja út mismunandi færslur, samkvæmt kröfum endurskoðanda eða yfirvalda. Ef um er að ræða sniðagerð eða færslur er hægt að nota aðgerðina framlenging til að stýra gagnaútflutningaferlinu. Aðgerðin er ekki með foruppsettu skrársniði fyrir útflutning. Þess vegna verður þú annaðhvort að setja upp App sem er með ákveðnu sniði (t.d. SIE, SAF-T eða FAC) eða þróa eigin.

> [!NOTE]
> Eins er hægt að velja SIE eða SAF-T snið sem viðbót við App. Félagar geta einnig þróað sérsniðið Form. Fjöldi tiltækan sniða eykst með tímanum.

## <a name="set-up-audit-file-export"></a>Setja upp útflutning endurskoðunarskráa

1. Velja skal hnappinn leitarhnappur  ![stækkunargler sem opnast aðgerðin segja mér.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera"), færa inn  **uppsetningu útflutningskráruppsetningar** og velja síðan tengda tengilinn.
2.  **Á uppsetningarsíðu**  endurskoðunarskráa er eftirfarandi þrepum fylgt:

    1.  **Á flipanum Almennt**, í  **reitnum útflutningssniði**  útflutnings, Tilgreinið kóðann fyrir sjálfgefna útflutningssnið í endurskoðunarskrá. Aðeins þau snið sem voru virkjuð þegar ákveðið skrársnið var uppsett úr aðgangsstjórnun og þau sem var bætt við sem sérsniðið snið eru tiltæk.
    2. Á Gæðasvæðinu  **gæði**  skal velja  **gátreitinn kanna reikningsskil**  til að fá tilkynningu um Fyrirtækjaupplýsingar sem hafa ekki verið rétt settar upp.
    3.  **Veljið gátreitinn athuga viðskiptavin**  til að fá tilkynningu um reiti sem hafa ekki verið rétt settir upp fyrir tiltekna viðskiptamenn.
    4.  **Veljið gátreitinn athuga lánardrottin**  til að fá tilkynningu um reiti sem hafa ekki verið rétt settir upp fyrir tiltekna lánardrottna.
    5.  **Veljið gátreitinn athuga bankareikning**  til að fá tilkynningu um reiti sem hafa ekki verið rétt settir upp fyrir tiltekna bankareikninga.
    6.  **Veljið GÁTREITINN póstnúmer**  til að fá tilkynningu um póstnúmer sem hefur ekki verið rétt uppsett.
    7.  **Veljið gátreitinn kanna aðsetur**  sem á að tilkynna þegar netfang hefur ekki verið rétt sett upp.
    8.  **Í reitinn sjálfgefið póstnúmer**  skal færa inn póstnúmerið sem á að nota ef ekkert póstnúmer er tilgreint á spjaldi viðskiptamanns eða lánardrottins.

3. Velja skal hnappinn leitarhnappur  ![stækkunargler sem opnast aðgerðin segja mér.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera"), færa inn  **uppsetningu** útflutningssniðs og velja síðan tengda tengilinn.
4. Á uppsetningarsíðu  **fyrir**  útflutningssnið endurskoðunarskráa er eftirfarandi:

    1. Velja útflutningsskrársnið endurskoðunarskrár sem á að samskipa. Aðeins þau snið sem voru virkjuð þegar ákveðið skrársnið var uppsett úr aðgangsstjórnun og þau sem var bætt við sem sérsniðið snið eru tiltæk.
    2.  **Í reitnum Heiti**  endurskoðunarskrár er tilgreint sjálfgefið skrárheiti eða sniðmát skrárheitsins fyrir þá endurskoðunarskrá sem á að flytja út.
    3.  **Veljið Skjalasafn í zip**  -gátreit til að skrá sjálfkrafa útfluttar skrár.

## <a name="provide-the-gl-account-mapping-for-audit-file-export"></a>Kveða á um vörpun fjárhagsreikningsins fyrir útflutning endurskoðunarskráa

Flest snið sem stjórnvöld þurfa fyrir fjárhagsreikninga krefjast ákveðins staðlaðs bókhaldslykils. Því eftir að fjárhagsreikningar hafa verið samskipaðar verður útflytjandi skráin byggð á vörpun. Hægt er að nota fleiri varpanir í kerfinu.

Fylgið þessum skrefum til að veita vörpun fjárhagsreikningsins til útflutnings í endurskoðun skráa.

1. Veldu hnappinn Leita á hnappinn  ![stækkunargler sem opnar aðgerðina](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") segja mér upp, færa inn  **vörpun** fjárhagsreiknings og velja síðan tengda tengilinn.
2.  **Á fjárhagsvörpunarsíðunni**  skal velja  **nýtt**  til að stofna vörpun.
3.  **Í reitnum kóti**  er kortlagakótinn tilgreindur sem táknar skýrslutímabilið.
4.  **Í reitinn stöðluð tegund**  reiknings er valin gerð staðlaðra fjárhagsreikninga.
5.  **Í reitnum útflutningssniði**  endurskoðunar er tilgreint útflutningssnið endurskoðunarskrárinnar sem staðlaður fjárhagsreikningur er tengdur við.
6.  **Í reitnum Tegund**  tímabils tilgreinir kerfið fjárhagstímabil eða tegund sérsniðins tímabils sem hefur sveigjanlegan upphafsdag og tíma, Byggt á valinu. Ef valið er ákveðið bókhaldstímabil verður svæðið stillt á  **bókhaldstímabil**. Að öðrum kosti verður það sett á  **Gagnasvið**.
7.  **Í reitnum Reikningstímabil**  er tilgreindur Upphafsdagur reikningstímabilsins sem verður notað sem skýrslutímabil, ef óskað er að þau séu eins.
8. Ef reiturinn reikningstímabil  **er stilltur**  er sjálfkrafa stillt á upphafs  **-og**  lokadagsetningar  **-grundvelli tímabilsins sem tilgreint var.**  Annars er hægt að stilla upphafs-og lokadagsetningar fyrir skýrslugerð þína handvirkt.
9. Ef þú hefur þegar bætt við stöðluðum bókhaldslykli, Fylgdu þessum skrefum:

    1.  **Í stöðluðu Reikningategund nr.** Er tilgreindur Flokkur staðlaða reikningsins eða flokkunarkóðanum sem er notaður við vörpun.
    2.  **Í Staðalreikningi nr.**  er tilgreindur Staðlaður Lykilkóði eða flokkunarkóði sem notaður er við vörpun.

10.  **Veljið gátreitinn hafa aðsenda stöðu**  til að líta á stöðu fjárhagsreiknings  **·**  fyrir vörpun í stað nettóbreytinga á skýrslutímabilinu.
11. Til að hefja kortlagningu er eftirfarandi þrepum fylgt:

    1. Til að búa til línur á  **vörpunarsíðu**  fjárhagsreikningsins, samkvæmt fyrirliggjandi bókhaldslykli, skal velja  **frumstillt fyrir vörpun**. Til að afrita vörpun fjárhagsreikningsins úr öðrum vörpakóta er valið  **Afrita úr annarri vörpun**. Þegar búið er að stofna línur verða allir fjárhagsreikningar sem hafa bókfærðar færslur merktir með grænum.
    2. Til að merkja aðeins fjárhagsreikninga sem eru með færslur er valið  **að uppfæra Fjárhagsfærsluaðgengi**.  **Ef valkosturinn taka með aðsenda**  er virkjaður eru allar bókaðar fjárhagsfærslur taldar til útreiknings. Annars teljast aðeins fjárhagsfærslur af skýrslutímabilinu.

## <a name="export-the-audit-file"></a>Flytja út endurskoðunarskrána

1. Velja skal hnappinn leitarhnappur  ![stækkunargler sem opnar aðgerðina segja mér upp.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera"), færa inn  **útflutningsskjöl** í endurskoðunarskrá og velja síðan tengda tengilinn.
2.  **Á síðu útflutningsskjala**  endurskoðunarskráa er valið  **nýtt**.
3.  **Á flipanum Almennt**  skal fara eftir þessum skrefum:

    1.  **Í reitnum útflutningssniði**  endurskoðunar er valið sniðið sem er notað til að flytja endurskoðunarskrána út.
    2.  **Í reitnum Vörslukóti**  fjárhagsreikningsins er valinn vörslukóði fjárhagsreikningsins fyrir skýrslutímabilið.
    3. Hakið í gátreitinn skipta eftir mánuðum  **ef mynduð er**  mörg endurskoðunarskrá fyrir mánuði.
    4. Veljið gátreitinn skipta eftir dagsetningu  **ef búa á til**  margar endurskoðunarskrár á dag.
    5.  **Í reitnum fyrirsögn athugasemd**  er færð inn athugasemdin sem á að vera í haus endurskoðunarskrárinnar.
    6.  **Í reitnum tengiliður**  skal tilgreina tengiliðinn sem er fluttur út í haus endurskoðunarskrárinnar.
    7.  **Veljið gátreitinn stofna marga ZIP-skrár**  til að mynda margar ZIP-skrár.

        > [!IMPORTANT]
        > Veljið aðeins þennan gátreit ef eitthvert snið apps hefur verið uppsett eða stofnað sérsniðið. Uppsetning eins eða fleiri af tilgreindum sniðum mun líklegast bæta við reitum og aðgerðum til að  **Flytja út**  Aðgerðir endurskoðunarskrár, út frá sniðkröfum.

4.  **Í vinnslufastanum**  er eftirfarandi þrepum fylgt:

    1.  **Veljið gátreitinn samhliða vinnslu**  ef vinna á við myndun endurskoðunarskrár er unnin með hliðstæðum bakgrunnsvinnslum. Hreinsið gátreitinn til að flytja gögn í gildandi lotu.
    2. Ef gátreiturinn samhliða vinna  **var valinn**  í reitnum  **Max nr.** Í reitnum er tilgreindur Hámarksfjöldi bakgrunnsverka sem hægt er að keyra á sama tíma.
    3.  **Í reitnum fyrsti Upphafsdagur/-tími**  er tilgreindur Fyrsti dagur og tími sem þarf að keyra bakvinnsluna í. Ef ferlið er keyrt með því að velja  **Ræsa** er hægt að rekja stöðuna á  **flipunum vinnsla**  og  **línur** .

5. Þegar þú hefur lokið við skaltu velja  **Sækja sem skrá**  til að hlaða niður endurskoðunarskrá völdu línunnar.

> [!IMPORTANT]
> Ef þú ert með margar færslur í útflutningi mælum við ekki með því að þær séu útflutt í gildandi lotu vegna hugsanlegra afkastamáta. Þess í stað mælum við með að þú beitir þér samhliða vinnslu þar sem ekki eru Vinnudagar eða tímar.

## <a name="see-also"></a>Sjá einnig .
[Fjármálastjórnun](finance.md)  
[Skilningur á fjárhag og bókhaldslyklum](finance-general-ledger.md)  
[Vinna með víddir](finance-dimensions.md)  
[Vinna með Business Central](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
