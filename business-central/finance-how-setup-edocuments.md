---
title: Settu upp rafræn skjöl
description: Lærðu hvernig á að setja upp virkni rafrænna skjala.
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice'
ms.search.form: '359, 360, 6103, 6133'
ms.date: 10/05/2023
ms.author: altotovi
---

# Settu upp rafræn skjöl

> [!IMPORTANT]
> E-Documents kjarnaeiningin er rammi. Sjálfgefið er að það er enginn **Þjónustusamþætting** reitur. Ef þú finnur valmöguleikana **skjalasnið**  sjálfgefið skaltu hafa í huga að þeir eru í boði sem dæmi og að staðsetning verður að veita nákvæmt snið. Þessar upplýsingar eru hluti af staðsetningarforritum vegna þess að þær eru sértækar fyrir staðbundnar kröfur.

> [!NOTE]
> Frá og með útgáfu 23.2 er stöðluðu PEPPOL skjalasniði bætt við sem alþjóðlegt snið í  **skjalasniði** reitnum. Hafðu í huga að þú getur líklega ekki notað þetta snið eins og það er. Það er W1 snið sem er til staðar til að sýna hvernig á að nota þennan eiginleika. Við mælum með því að þú prófir núverandi PEPPOL snið áður en þú byrjar að nota þetta snið.

Fyrsta skrefið í uppsetningu rafrænna skjala (e-skjala) er að setja upp E-Documents Service þar sem þú stillir heildarhegðun kerfisins þíns þar sem það tengist rafrænum skjalasamskiptum.

## Settu upp rafræna skjalaþjónustuna

Fylgdu þessum skrefum til að setja upp E-skjalaþjónustuna.

1. Veldu ![peruna sem opnar Segðu mér eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, sláðu inn **E-Document Services** og veldu síðan tengda hlekkinn.
2. Veldu **Nýtt** og síðan á **E-skjalaþjónustu** síðunni á **Almennt** FastTab, stilltu reitina eins og lýst er í eftirfarandi töflu.

    | Svæði | Heimildasamstæða |
    |-------|-------------|
    | Kóði | Veldu rafræna útflutningsuppsetningarkóðann. |
    | Heimildasamstæða | Færðu inn stutta lýsingu á rafrænni útflutningsuppsetningu. |
    | Skjalasnið | <p>Útflutningssnið rafrænu útflutningsuppsetningarinnar.</p><p>Sjálfgefið er að það séu tveir valkostir á þessu sviði. Þú getur valið **PEPPOL BIS 3** sem almennt kóða byggt snið eða **Data Exchange** þegar þú verður að setja upp fyrirfram -skjöl með tilteknu sniði á **Gagnaskiptaskilgreiningu** Hraðflipanum.</p> |
    | Samþætting þjónustu | Veldu samþættingarkóðann fyrir rafræna útflutningsuppsetninguna. Í Wave 1 er eini kosturinn **Engin samþætting**. |
    | Nota runuvinnslu | Tilgreina hvort þjónustan noti runuvinnslu fyrir útflutning. |

3. Á  **Innfluttar færibreytur** Hraðflipanum skaltu stilla reitina eins og lýst er í eftirfarandi töflu.

    | Svæði | Heimildasamstæða |
    |-------|-------------|
    | Staðfesta móttökufyrirtæki | Tilgreinið hvort staðfesta þurfi móttökufyrirtækisupplýsingarnar við innflutning. |
    | Leysa mælieiningu | Tilgreinið hvort mælieininguna eigi að leysa við innflutning. |
    | Fletta upp tilvísun í atriði | Tilgreindu hvort leita eigi að vöru með vörutilvísun við innflutning. |
    | Fletta upp GTIN-númeri atriðis | Tilgreinið hvort leita eigi að vöru með Global Trade Item Number (GTIN) við innflutning. |
    | Fletta upp reikningsvörpun | Tilgreindu hvort leita ætti að reikningi í **Reikningskortlagningu** eftir innkomnum texta við innflutning. |
    | Staðfesta línuafslátt | Tilgreinið hvort línuafsláttur skuli gilda við innflutning. |
    | Nota reikningsafslátt | Tilgreinið hvort nota eigi reikningsafslátt við innflutning. |
    | Staðfesta samtölur | Tilgreinið hvort sannreyna eigi heildarreikning reiknings við innflutning. |
    | Uppfæra pöntun | Tilgreindu hvort samsvarandi innkaupapöntun þurfi að uppfæra. |
    | Stofna færslubókarlínur | Tilgreinið hvort stofna þurfi færslubókarlínu í stað innkaupaskjals. Veldu þennan valkost þegar þú vilt nota færslubækur sem áfangastað fyrir reikninga þína. |
    | Heiti sniðmáts færslubókar | Tilgreindu heiti sniðmáts fyrir almenna færslubók sem er notað til að búa til færslubókarlínur. Þessi reitur á við þegar þú vilt nota færslubækur sem áfangastað fyrir reikninga þína. |
    | Heiti færslubókarkeyrslu | Tilgreindu nafn almennu færslubókarlotunnar sem er notuð til að búa til færslubókarlínur. Þessi reitur á við þegar þú vilt nota færslubækur sem áfangastað fyrir reikninga þína. |
    | Sjálfvirkur innflutningur | Tilgreina hvort skjöl eigi að flytja sjálfkrafa inn úr þjónustunni. |
    | Upphafstími keyrslu | Tilgreindu upphafstíma innflutningsverka. |
    | Mínútur á milli keyrslna | Tilgreindu fjölda mínútna á milli innflutningsverka. |

4. Ef þú valdir **Gagnaskipti** í reitnum **skjalasnið** á reitnum **Almennt** Fastflipann, notaðu **Gagnaskiptaskilgreininguna** Fastflipann til að stilla eftirfarandi reiti.

    | Svæði | Heimildasamstæða |
    |-------|-------------|
    | Gerð fylgiskjals | Tilgreindu skjalagerðina sem notar gagnaskipti til að flytja inn og flytja gögnin út. Dæmi eru **Sölureikningur**, **Sölukreditreikningur** og **Kaupreikningur**. |
    | Skilgreiningarkóði gagnaskipta í innflutningi | Tilgreindu gagnaskiptakóðann sem er notaður til að flytja inn gögnin. Notaðu þennan reit eingöngu til að fá skjal í kaupferlinu. |
    | Skilgreiningarkóði gagnaskipta í útflutningi | Tilgreindu gagnaskiptakóðann sem er notaður til að flytja gögnin út. Notaðu þennan reit eingöngu til að afhenda skjöl í söluferlinu. |

> [!NOTE]
> Það eru tilbúnar gagnaskiptiskilgreiningar fyrir PEPPOL sniðið sem tengjast stöðluðu sölu- og innkaupaskjali. Hins vegar geturðu líklega ekki notað þessar skilgreiningar eins og þær eru. Þau eru öll W1 snið sem eru til staðar til að sýna hvernig á að nota þennan eiginleika. Við mælum með því að þú prófir núverandi PEPPOL snið áður en þú byrjar að nota þau.

Ef þú hefur stillt **Data Exchange Definition** sniðið í staðsetningu þinni geturðu bætt við línu fyrir hverja skjalategund sem þú þarft. Bættu við línum sem passa við sjálfgefna gagnaskiptadæmið fyrir W1 PEPPOL sniðið. Hins vegar skaltu fyrst velja **Document Type** valkostinn fyrir hverja línu sem þú þarft. Fyrir hverja gagnategund skaltu velja **Import Data Exchange Def. Kóði** eða **Export Data Exchange Def. Kóða** gildi sem þú vilt nota.

Ef þú notar ekki **Skilgreining gagnaskipta**  sniði geturðu búið til og stillt snið með því að nota [viðmót](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments). Stilltu upplýsingarnar á **Flytja út kortlagning**  og **Flytja inn kortlagningu**  línur, þar sem þú getur fundið töflur og reiti til að stilla umbreytingarreglur. Í þessu tilviki verður þú að bæta við nýjum valkosti í **Skjalsnið**  reit sem tengist sniðinu þínu.

## Settu upp skjalasendingarsnið

Þú getur sett upp valinn aðferð til að senda söluskjöl fyrir hvern viðskiptavin. Á þennan hátt þarftu ekki að velja sendingarvalkost í hvert skipti sem þú velur **Posta og senda**  aðgerð. Á **Skjalasendingarsnið**  síðu geturðu sett upp mismunandi sendingarsnið og síðan valið meðal þeirra í **Sendingarsnið skjals**  reit á viðskiptavinakorti. Þú getur valið **Sjálfgefið** gátreitinn til að tilgreina að skjalasendingarsnið sé sjálfgefið snið fyrir alla viðskiptavini, nema viðskiptavini þar sem **Sendingarsnið skjala** reitur er stilltur á annan sendingarsnið.

Þessi virkni er notuð til að setja upp sjálfvirkni rafrænna reikninga. Þegar þú velur **Posta og Senda** á söluskjali sýnir  **Posta og Senda Staðfesting**  gluggann sendingarsniðið sem er notað: annað hvort sniðið sem er sett upp fyrir viðskiptavininn eða sjálfgefið snið fyrir alla viðskiptavini.

Fylgdu þessum skrefum til að setja upp skjalasendingarsnið.

1. Veldu ![peru sem opnar Segðu mér eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, sláðu inn **Sendingarprófíl skjala** og veldu síðan tengda hlekkinn.
2. Á síðunni **Skilasendingarsnið**  skaltu velja **Nýtt**.
3. Á **Almennt** flýtiflipanum skaltu slá inn allar nauðsynlegar reitupplýsingar.
4. Á **Sendingarvalkostir** Hraðflipanum skaltu stilla reitina eins og lýst er í eftirfarandi töflu.

    | Svæði | Heimildasamstæða |
    |-------|-------------|
    | Rafrænt skjal | Tilgreindu hvort skjalið sé sent sem rafrænt skjal sem viðskiptavinurinn getur flutt inn í kerfið sitt þegar þú velur **Posta og Senda**. Til að nota þennan valkost verður þú einnig að stilla reitinn **Format** eða **Rafræn skjalaþjónustuflæðiskóði** . Að öðrum kosti er hægt að vista skrána á disk. |
    | Snið | Tilgreindu sniðið sem á að nota til að senda rafrænt skjal. Þessi reitur er nauðsynlegur ef þú velur **Gegnum skjalaskipti** í reitnum **Rafræn skjal** . |
    | Kóði þjónustuflæðis fyrir rafræn skjöl | Tilgreindu rafræna þjónustuflæðið sem er notað til að senda skjöl. Þessi reitur er nauðsynlegur ef þú velur **Extended E-Document Service Flow** í reitnum **Rafræn skjal** . |

    > [!NOTE]
    > Ef þú velur **Extended E-Document Service Flow** í reitnum **Rafræn skjal**, verður þú nú þegar að hafa verkflæðið stillt fyrir rafræn skjöl þín.

## Settu upp verkflæðið

Fylgdu þessum skrefum til að setja upp verkflæðið sem er notað í e-skjalavirkni.

1. Veldu ![peru sem opnar Segðu mér eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, sláðu inn **Workflow Templates** og veldu síðan tengda tengilinn.
2. Ef þú finnur ekki **E-Document Workflow Templates** á  **Workflow Templates** síðunni skaltu velja **Endurstilla Microsoft sniðmát**. **E-Document Workflow Templates** ættu þá að birtast. Loka síðunni.
3. Veldu ![peru sem opnar Segðu mér eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, sláðu inn **Workflows** og veldu síðan tengda hlekkinn.
4. Keyrðu  **Nýtt verkflæði úr sniðmáti** aðgerðinni til að velja sniðmát fyrir rafræn skjöl. Tiltæk sniðmát eru **Senda á eina þjónustu** og **Senda á margar þjónustur**.
5. Veldu **Í lagi** til að klára uppsetningu verkflæðisins.
6. Í reitnum **Þá svar**, veldu **Senda rafræn skjal með uppsetningu** til að stilla verkflæðissvörin.
7. Veldu E-Document Service sem þú bjóst til sem valkost, veldu **OK** og virkjaðu síðan verkflæðið.

> [!NOTE]
> Þú getur búið til þitt eigið verkflæði fyrir rafræn skjöl án þess að nota fyrirfram skilgreind verkflæðissniðmát. Ef þú ert með fleiri þjónustu geturðu notað mismunandi verkflæði.

Til að nota fleiri verkflæði skaltu stilla þau í gegnum skjalasendingarsnið fyrir mismunandi viðskiptavini. Þegar þú setur upp verkflæðið skaltu tilgreina skjalasendingarsniðið í **Á ástandi** dálknum á **Workflow Steps** Fastflipanum, vegna þess að þú getur ekki haft tvær þjónustur sem nota sama skjalasendingarsnið í verkflæði.

Þegar þú stillir verkflæðið þitt á **Workflow** síðunni skaltu benda á **On Condition** reitinn á **Verkflæðisskref** FastTab. Á síðunni **Skilyrði viðburðar**, í reitnum **Sía**, veldu skjalasendingarsniðið sem þú vilt nota.

## Settu upp varðveislustefnu fyrir rafræn skjöl

Rafræn skjöl geta verið viðfangsefni mismunandi staðbundinna laga sem tengjast því tímabili sem rafræn skjöl eru geymd í. Þess vegna höfum við bætt við uppsetningu varðveislustefnu fyrir allar mikilvægar upplýsingar sem tengjast rafrænum skjölum. Stjórnendur geta skilgreint varðveislustefnur sem tilgreina hversu oft Dynamics 365 Business Central eyðir úreltum skrám sem tengjast rafrænum skjölum. Til að læra meira um varðveislustefnur, sjá [Skilgreina varðveislustefnur](admin-data-retention-policies.md).

Til að setja upp varðveislustefnur tengdar rafrænum skjölum skaltu fylgja þessum skrefum.

1. Á  **E-Document Services** síðunni skaltu keyra **Retention Policy** aðgerðina.
2. Þegar aðgerðinni er lokið skaltu velja eina af eftirfarandi varðveislustefnu til að setja upp:

    - Skrá rafræns skjals
    - Samþættingarskrá rafrænna skjala
    - Vörpunarskrá rafræns skjals
    - Gagnageymsla rafrænna skjala

## Sjá einnig .

[Hvernig á að nota rafræn skjöl í Business Central](finance-how-use-edocuments.md)  
[Hvernig á að framlengja rafræn skjöl í Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)  
[Fjármálastjórnun](finance.md)  
[Reikningsfæra sölur](sales-how-invoice-sales.md)  
[Skráðu innkaup með innkaupareikningum og pöntunum](purchasing-how-record-purchases.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
