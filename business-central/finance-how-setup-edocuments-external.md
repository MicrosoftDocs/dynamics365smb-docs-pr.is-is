---
title: Stilltu E-Documents tengið með ytri endapunktum
description: Þessi grein útskýrir hvernig á að setja upp E-Documents virkni þegar það er tengt við ytri endapunkta.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, access-point, endpoint'
ms.search.form: '359, 360, 6103, 6133'
ms.date: 12/13/2023
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Stilltu E-Documents tengið með ytri endapunktum

Þessi grein útskýrir hvernig á að setja upp E-Documents virkni þegar það er tengt við ytri endapunkta.

Áður en þú notar virknina sem lýst er í þessari grein skaltu setja upp **E-Documents Connector with External Endpoints** appið efst á alþjóðlegu **E- Document Core** app. Þetta app er hægt að nota fyrir sjálfgefna samþættingu við ytri (þriðju aðila) aðgangsstaði til að gera rafræn skjalaflæði sjálfvirkt. Vegna þess að þetta app táknar aðeins sum af völdum tengjunum ertu ekki takmörkuð við núverandi samþættingar í því. Flest tengin verða fáanleg á AppSource í framtíðinni.

## Settu upp tenginguna

Til að hefja uppsetningu þína skaltu fylgja skrefunum í [E-skjala kjarnaforritinu](finance-how-setup-edocuments.md). Eftir að þú hefur lokið þessum skrefum skaltu fara aftur í þessa grein og ljúka eftirfarandi skrefum:

1. Veldu ![peru sem opnar Segðu mér eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, sláðu inn **E-Document Services** og veldu síðan tengda hlekkinn.
2. Í reitnum **Þjónustusamþætting** velurðu einn af samþættingarkóðum sem eru í boði fyrir uppsetningu endapunktaþjónustu.
3. Veldu **Setup Service Integration**.
4. Á síðunni **E-Document External Connection Setup**  skaltu velja **Request Authorization Code**. Þér er vísað áfram á ytri þjónustuheimildarsíðuna og beðinn um innskráningarupplýsingar þínar.
5. Afritaðu heimildarkóðann í **Sláðu inn heimildarkóða** reitinn.
6. Veldu **Refresh Access Token** til að tryggja að þú getir endurnýjað táknið.

    > [!NOTE]
    > Þessi tenging krefst samskipta við utanaðkomandi þjónustuaðila sem gætu verið háð aukagreiðslu og krefst samninga við þá. Hafðu samband við þjónustuveitendur til að fá öll nauðsynleg skilríki.

7. Á síðunni **E-Document External Connection Setup**  skaltu fylla út eftirfarandi reiti:

    | Heiti reits | Heimildasamstæða |
    |---|---|
    | API-vefslóð skrár | Tilgreindu API vefslóð skrárinnar. |
    | Vefslóð skráarhluta | Tilgreindu slóð skráarhluta. |
    | API-vefslóð skjals | Tilgreindu API slóð skjalsins. |
    | Kenni fyrirtækis | Tilgreindu auðkenni fyrirtækisins. |
    | Sendingarhamur | Tilgreindu sendingarhaminn. Þú getur valið **Framleiðsla**, **Próf** eða **Vottun**. |

    > [!NOTE]
    > Biðjið þjónustuveituna um allar fyrri upplýsingar til að koma á tengingu við aðgangsstað sinn.

## Settu upp upplýsingar um fyrirtæki

Áður en þú byrjar að nota rafræn skjöl skaltu uppfæra **Fyrirtækisupplýsingar** síðuna þína með því að ljúka eftirfarandi skrefum:

1. Veldu ![peru sem opnar Segðu mér eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, sláðu inn **Fyrirtækisupplýsingar** og veldu síðan tengda hlekkinn.
2. Auk þess að fylla út venjulega reiti verður þú einnig að fylla út eftirfarandi reiti:

    | Heiti reits | Heimildasamstæða |
    |---|---|
    | SWIFT-kóði | Tilgreindu SWIFT kóða (alþjóðabankaauðkenniskóða) aðalbankans þíns. |
    | Bankanúmer | Tilgreinið fjögurra stafa útibúsnúmer bankans. |
    | VSK-númer. | Tilgreinið skráningarnúmer virðisaukaskatts (VSK) fyrirtækisins. |

3. Loka síðunni.

## Settu upp viðskiptavini til að fá rafræn skjöl

Til að gera viðskiptavinum kleift að fá rafræn skjöl þín skaltu ljúka eftirfarandi skrefum:

1. Veldu ![peru sem opnar Segðu mér eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, sláðu inn **Viðskiptavinir** og veldu síðan tengda hlekkinn.
2. Opnaðu **viðskiptavina** kortið.
3. Auk þess að fylla út venjulega reiti skal tilgreina viðskiptavin í reitnum **GLN**  í tengslum við sendingu rafrænna skjala.
4. Merktu við **Notaðu GLN í rafrænum skjölum** reitinn til að gefa til kynna hvort Global Location Number (GLN) sé notað sem auðkennisnúmer aðila í rafrænum skjölum.
5. Loka síðunni.

## Önnur uppsetning

Áður en þú byrjar að vinna með e-skjöl skaltu setja upp e-skjal **vinnuflæði** og **skjalasendingarsnið** til notaðu vinnuflæðið þitt. Eftir að þjónustutengingunni hefur verið komið á geturðu byrjað að nota rafræna skjalalausnina þína.

## Tiltækir þjónustuaðilar

Microsoft vill hvetja aðgangsstaðaveitendur til að bæta tengjum sínum ofan á **E-Document Core** ramma okkar.

Sem stendur er Pagero eini aðgangsstaðaveitan sem fellur undir þetta kerfi. Microsoft ber enga samningsbundna skuldbindingu við Pagero. Þess vegna verður þú að gera samning við þá til að fá öll nauðsynleg skilríki.

Við munum uppfæra þennan lista eftir því sem við fáum nýja þjónustuveitendur til að skiptast á rafrænum skjölum.

## Sjá einnig .

[Hvernig á að setja upp rafræn skjöl í Business Central](finance-how-setup-edocuments.md)  
[Hvernig á að nota rafræn skjöl í Business Central](finance-how-use-edocuments.md)  
[Hvernig á að framlengja rafræn skjöl í Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)  
[Fjármálastjórnun](finance.md)  
[Reikningsfæra sölur](sales-how-invoice-sales.md)  
[Skráðu innkaup með innkaupareikningum og pöntunum](purchasing-how-record-purchases.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
