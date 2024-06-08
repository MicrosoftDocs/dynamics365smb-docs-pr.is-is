---
title: Stilla tengingu E-Skjala með ytri endastöðvum
description: Þessi grein útskýrir hvernig setja á upp E-skjöl þegar hún er tengd ytri endastöðvum.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, access-point, endpoint'
ms.search.form: '359, 360, 6103, 6133'
ms.date: 12/13/2023
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Stilla tengingu E-Skjala með ytri endastöðvum

Þessi grein útskýrir hvernig setja á upp E-skjöl þegar hún er tengd ytri endastöðvum.

Áður en þú notar aðgerðina sem er lýst í þessari grein skal setja upp **E-Documents Connector með forritinu Ytri endastöðvar** efst í altæku **E-Document Core** forritinu. Þetta forrit er hægt að nota til sjálfgefinnar samþættingar við ytri (þriðja aðila) aðgangsstaði til að gera e-skjalaflæðið sjálfvirkt. Þar sem þetta forrit táknar aðeins einhverja af völdum tengjum er ekki takmarkað við fyrirliggjandi samþættingar við það. Flest tengi verða tiltæk á AppSource í framtíðinni.

## Setja upp tenginguna

Til að hefja uppsetninguna skal fylgja skrefunum í [kjarnaforriti E-skjals](finance-how-setup-edocuments.md). Þegar lokið hefur verið við þessi skref skal fara aftur í þessa grein og ljúka eftirfarandi skrefum:

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **E-Document Services** og velja síðan viðeigandi tengil.
2. Í reitnum **Þjónustuheildun** skal velja einn af samþættingarkótunum sem eru í boði fyrir þjónustuuppsetningu endastöðvarinnar.
3. Velja skal **Uppsetning þjónustuheildunar**.
4. Á síðunni **Uppsetning utanaðkomandi tengingar utanaðkomandi skjals skal velja** Kóti **beiðniheimildar**. Þú ert bein(ur) á vefsíðu ytri þjónustuheimildar og beðin(n) um innskráningarupplýsingar.
5. Afrita heimildarkótann í reitinn **Færa inn heimildarkóta** .
6. Valið er **Endurnýja aðgangstákn** til að ganga úr skugga um að hægt sé að endurnýja táknið.

    > [!NOTE]
    > Þessi tenging krefst samskipta við utanaðkomandi þjónustuaðila sem gætu fallið undir viðbótargreiðslu og krafist samninga við þá. Til að fá öll nauðsynleg skilríki skal hafa samband við þjónustuveitendur.

7. Á síðunni **Uppsetning** utanaðkomandi tengingar utanaðkomandi skjals skal fylla út eftirfarandi reiti:

    | Heiti reits | Heimildasamstæða |
    |---|---|
    | API-vefslóð skrár | Tilgreina API-URL skráarinnar. |
    | Vefslóð skráarhluta | Tilgreina URL skráarparts. |
    | API-vefslóð skjals | Tilgreina API-URL skjalsins. |
    | Kenni fyrirtækis | Tilgreina kenni fyrirtækis. |
    | Sendingarhamur | Tilgreina skal sendingarham. Hægt er að velja **Framleiðsla**, **Prófun** eða **Vottun**. |

    > [!NOTE]
    > Biðja þjónustuveituna um allar fyrri upplýsingar til að koma á tengingu við aðgangsstað.

## Setja upp stofngögn

Áður en byrjað er að nota e-skjöl skal uppfæra **síðuna Stofngögn** með því að ljúka eftirfarandi skrefum:

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Stofngögn** og velja síðan viðeigandi tengil.
2. Auk þess að fylla út venjulega reiti þarf einnig að fylla út eftirfarandi reiti:

    | Heiti reits | Heimildasamstæða |
    |---|---|
    | SWIFT-kóði | Tilgreina SWIFT-kóða (alþjóðlegan bankakenniskóta) aðalbankans. |
    | Bankanúmer | Tilgreinið fjögurra stafa útibúsnúmer bankans. |
    | VSK-númer. | Tilgreina virðisaukaskattsnúmer fyrirtækisins (VSK). |

3. Loka síðunni.

## Setja upp viðskiptamenn til að taka á móti tölvupóstskjölum

Til að gera viðskiptamönnum kleift að taka á móti e-skjölum skal ljúka eftirfarandi skrefum:

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **Viðskiptamenn** og velja síðan viðeigandi tengil.
2. Opna skal **viðskiptamannaspjaldið** .
3. Auk þess að fylla út venjulega reiti í reitnum **GLN**, tilgreina viðskiptamanninn í tengslum við sendingu rafrænna skjala.
4. Reiturinn **Nota GLN í rafræn skjölum** er merktur til að tilgreina hvort Altækt birgðageymslunúmer (GLN) sé notað sem kenninúmer aðila í rafrænum skjölum.
5. Loka síðunni.

## Önnur uppsetning

Áður en byrjað er að vinna með tölvupóstskjöl skal setja upp verkflæði tölvupóstskjala **og** **skjalasendingarsnið** til að nota verkflæðin. Þegar þjónustutengingu hefur verið náð er hægt að byrja að nota e-skjalslausnina.

## Tiltækir þjónustuaðilar

Microsoft vill hvetja aðgangsstaðaveitur til að bæta við tengjum sínum efst í E-Document Core **rammanum.** 

Eins og er er Pagero eini aðgangsstaðarveitan sem kerfið nær yfir. Microsoft er ekki með samningsbundnar skuldbindingar við Pagero. Þess vegna þarf að gera samning við þá til að fá öll nauðsynleg skilríki.

Við munum uppfæra þennan lista þegar við fáum nýja aðgangsstaðarþjónustu fyrir tölvupóst.

## Sjá einnig .

[Hvernig á að setja upp tölvupóstskjöl í Business Central](finance-how-setup-edocuments.md)  
[Hvernig á að nota e-skjöl í Business Central](finance-how-use-edocuments.md)  
[Hvernig á að framlengja tölvupóstskjöl í Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)  
[Fjármálastjórnun](finance.md)  
[Reikningsfæra sölur](sales-how-invoice-sales.md)  
[Skrá innkaup með innkaupareikningum og pöntunum](purchasing-how-record-purchases.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
