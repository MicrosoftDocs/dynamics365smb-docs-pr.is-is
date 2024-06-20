---
title: Settu upp stafræna fylgiskjöl
description: Þessi grein útskýrir hvernig á að setja upp og nota framfylgdar stafrænar fylgiskjöl í Microsoft Dynamics 365 Business Central.
author: altotovi
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.search.keywords: 'digital voucher, voucher, attachment, setup'
ms.search.form: '5579, 5582, 5587'
ms.date: 11/17/2023
ms.custom: bap-template
ms.reviewer: bholtorf
---

# <a name="set-up-digital-vouchers"></a>Settu upp stafræna fylgiskjöl

Stjórnendur geta notað stafræna fylgiskjöl til að krefjast þess að skjöl séu fest við tilteknar færslur þegar þau eru bókuð. Þess vegna gerir þessi virkni heimild fyrir upprunadrifinni nálgun og veitir betri endurskoðunarslóð. Hægt er að stilla mismunandi gerðir fullnustu í þessum tilgangi, allt eftir skjölum eða færslubókargerðum.

Hugtakið *stafrænt fylgiskjal* vísar til stafræns eða rafræns forms hefðbundins fylgiskjals í bókhaldi. Skírteini er skjal sem er notað til að styðja og heimila fjárhagsfærslur. Í bókhaldi þjónar skírteini venjulega sem sönnun um útgjöld eða móttöku fjármuna. Skírteinið gæti innihaldið upplýsingar eins og dagsetningu viðskipta, lýsingu, upphæð og allar heimildarundirskriftir.

> [!IMPORTANT]
> Í sumum löndum og svæðum gætirðu verið takmarkaður við að stilla suma valkosti, vegna þess að sérstakar uppsetningar gætu verið bundnar af lagaskilyrðum. Ef þú lendir í þessum takmörkunum skaltu leita að ítarlegri skýringu á skjalasíðunni fyrir landið þitt eða svæði.

## <a name="enable-digital-vouchers"></a>Virkja stafræna fylgiskjöl

Fylgdu þessum skrefum til að virkja virkni stafræns fylgiskjals.

1. Veldu ![peruna sem opnar Segðu mér eiginleikann 3.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, sláðu inn **Uppsetning stafræns fylgiskjals** og veldu síðan tengda hlekkinn.
2. Veldu gátreitinn **Virkt** .

## <a name="set-up-digital-vouchers-1"></a>Settu upp stafræna fylgiskjöl

Þú getur notað mismunandi uppsetningar fyrir eftirfarandi skjöl og dagbækur.

| Tegund færslu | Heimildasamstæða |
|------------|-------------|
| Söluskjal | Tilgreinir færslur sem eru kláraðar úr söluskjölum. |
| Innkaupaskjal | Tilgreinir færslur sem eru kláraðar úr innkaupaskjölum. |
| Almenn bók | Tilgreinir færslur sem eru kláraðar úr almennu færslubókinni fyrir allar reikningsgerðir nema þær sem tengjast viðskiptamanni og lánardrottni. Ef þú velur eina af þessum reikningsgerðum breytir þú stjórn á bókunarferlinu. Ef þú velur **Viðskiptavinur** sem reikningsgerð, athugar kerfið uppsetninguna þína sem tengist sölubókinni. Ef þú velur **Lánardrottinn** sem reikningsgerð, athugar kerfið uppsetninguna þína sem tengist innkaupabókinni. |
| Sölubók | Tilgreinir þær færslur sem eru kláraðar úr sölubókinni og almennu færslubókinni þar sem **Viðskiptavinur** er valinn sem reikningsgerð. |
| Innkaupabók | Tilgreinir þær færslur sem eru kláraðar úr innkaupabókinni og almennu færslubókinni þar sem **Lánardrottinn** er valinn sem reikningsgerð. |

Fylgdu þessum skrefum til að skilgreina hvernig fyrirtæki þitt notar framfylgdar stafrænar fylgiskjöl.

1. Veldu ![peruna sem opnar Segðu mér eiginleikann 3.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, sláðu inn **Uppsetning stafræns fylgiskjalsfærslu** og veldu svo tengda tengil. Að öðrum kosti, á síðunni **Uppsetning stafræns fylgiskjals**, skaltu velja **Entry Setup**.
2. Í dálknum **Tegund færslu**  skaltu velja valkost.
3. Í **Athugunartegund** dálknum skaltu velja framfylgdarvalkost. Ef þú velur **Ekkert** geturðu bókað valda tegund færslu án stafræns fylgiskjals. Ef þú velur **Viðhengi** verður færslan að innihalda viðhengi. Ef þú velur **Viðhengi eða Athugasemd** geturðu látið viðhengi eða athugasemd við færsluna fylgja með. 
4. Veldu **Búa til sjálfkrafa** gátreitinn til að búa til stafræna skírteini sjálfkrafa. Til dæmis, ef þú vilt ekki bæta sölureikningi handvirkt við færsluna þína skaltu velja þennan gátreit. Þá þarftu bara að senda skjalið. Kerfið býr sjálfkrafa til skjalið, byggt á uppsetningu skýrslunnar, og tengir það við færsluna.
5. Veldu gátreitinn **Sleppa ef handvirkt bætt við** gátreitinn ef þú vilt ekki bæta við sjálfkrafa mynduðu stafrænu fylgiskjali ef notandinn hefur þegar bætt við handvirku viðhengi.

### <a name="use-source-codes-for-setup"></a>Notaðu frumkóða fyrir uppsetningu

Til að nota fullnustu fyrir færslubækur, en ekki fyrir allar færslugerðir, tengdu tiltekna frumkóðann til að auðkenna færslutegundina almenna færslubók, sölubók eða innkaupabók.

Fylgdu þessum skrefum til að setja upp sérstaka frumkóða fyrir stafræna fylgiskjöl.

1. Á síðunni **Stafræn innsláttarmiðauppsetning**  skaltu velja **Upprunakóðar**.
2. Á síðunni **Fundarkóðar innsláttarmiða**  skaltu velja frumkóðana sem þú vilt stilla.
3. Loka síðunni.

## <a name="use-the-functionality"></a>Notaðu virknina

Opnaðu innkaupa- eða söluskjal og sláðu inn upplýsingar í nauðsynlega reiti. Áður en þú birtir skjalið verður þú að fylgja þessum skrefum til að hengja stafrænt fylgiskjal við.

1. Í **Incoming Document Files** Factbox skaltu velja **Attach File**.
2. Dragðu skrá beint á  **Insert File** síðuna, eða flettu að skránni af þessari síðu.

Skjalið er fylgt við **Incoming Document Files** FactBox. Fyrir hverja línu er hægt að finna nafn og gerð skjalsins.

Ef þú festir óvart rangt fylgiskjal skaltu fylgja þessum skrefum til að eyða því áður en þú birtir skjalið.

1. Í **Skjalaskrár sem berast**  FactBox úr skjalalínunni, veldu **Skjal á innleið**.
2. Á **Innkomið skjal**  síðu, veldu **Eyða**.

> [!NOTE]
> Ef viðhengi á stafrænu fylgiskjali er stillt sem skylda, og þú reynir að bóka skjöl eða færslubækur án þess að hengja fylgiskjali, kemur kerfið í veg fyrir að þú bókir. Þú færð eftirfarandi villuboð: "Ekki hægt að senda inn án þess að hengja stafræna skírteinið við."

### <a name="find-attached-vouchers-in-transactions"></a>Finndu meðfylgjandi fylgiskjöl í viðskiptum

Þú getur fundið meðfylgjandi skírteini úr settu skjali eða frá **Fjárhagsfærslur**  síðu með því að fletta í **Skjalaskrár sem berast**  FactBox.

Þú getur ekki eytt meðfylgjandi skjali eftir að færslu er lokið. Hins vegar geturðu bætt við fleiri viðhengjum eftir að færslu er lokið.

## <a name="see-also"></a>Sjá einnig .

[Fjármálastjórnun](finance.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
