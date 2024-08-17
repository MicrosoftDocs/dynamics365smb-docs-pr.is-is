---
title: Uppsetning VSK-yfirlits
description: Í þessum greinar kemur fram hvernig setja á upp sniðmát VSK-yfirlits og heiti VSK-yfirlits til að uppfylla breytingar á kröfum skattyfirvalda.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'VAT, posting, tax, value-added tax'
ms.search.form: '317, 318, 320, 474'
ms.date: 08/13/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Setja upp sniðmát VSK-yfirlits og heiti VSK-yfirlits

Skattayfirvöld geta breytt, og gera breytingar á, kröfum sínum hvað varðar bókun á VSK. Sniðmát VSK-yfirlita og Heiti VSK-yfirlita geta hjálpað þér að undirbúa fyrir komandi breytingar og gera umskiptin yfir í nýju kröfurnar þægilegri. Nota má sniðmát VSK-yfirlits til að setja upp mismunandi skýrslur þegar valið er að prenta yfirlitið. Hvert sniðmát VSK-yfirlits getur haft mörg VSK-yfirlitsheiti sem síðan skilgreina útreikningana, og hægt er að búa til nýtt heiti VSK-yfirlits þegar þörfum er breytt. Til dæmis kann eitt heiti að reikna út VSK fyrir þetta árið á grundvelli gildandi þarfa, og annað gæti reiknað út VSK samkvæmt þörfum fyrir næsta ár. Heiti eru einnig til upplýsingar um feril sniða VSK-yfirlits, til dæmis, til að hægt sé að skoða hvernig þú hefur reiknað út VSK á fyrri árum.

## Að skilgreina VSK-yfirlit

VSK-yfirlit bjóða upp á að reikna út VSK-uppgjörsupphæð á ákveðnu tímabili, til dæmis fyrir ársfjórðung.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **VSK-yfirlit** og velja síðan viðkomandi tengil.  
2. Veljið reitinn **Heiti** og veljið síðan **Nýtt** á síðunni **Heiti VSK-yfirlita**.
3. Fylltu út nauðsynlega reiti. Yfirleitt þyrfti að vera stilling fyrir hverja samsetningu VSK viðsk.bókunarflokkur / VSK-vörubókunarflokkur. Með línunúmerum er skynsamlegt að nota jafngild númer eða kóta eins og í opinberu VSK-yfirliti notanda. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

> [!Tip]
> Hægt er að sía upplýsingarnar sem koma fram á yfirlitinu, fer eftir því hvað valið er í reitnum **Gerð**. **Samtala fjárhags** er gagnleg þegar þú vilt VSK af tilteknum lykli.
**Samtala VSK-færslna** fær VSK frá lyklunum sem er úthlutað á valið í reitunum **Alm. bókunartegund**, **VSK viðsk.bókunarflokkur** og/eða **VSK-vörubókunarflokkur**. **Samtala línu** leyfir þér að slá inn gildi eða skilyrði flýtiafmörkunar í reitnum **Samtala línu**. Frekari upplýsingar er að finna í [Leita í, afmarka og raða gögnum](ui-enter-criteria-filters.md). **Lýsing** er oft notuð til að bæta við athugasemd við yfirlitið. Til dæmis er hægt að nota hana sem fyrirsögn þegar þú hefur notað samtölu línu.

## Til að forskoða virðisaukaskattsyfirlitið

Eftir að þú hefur skilgreint VSK-yfirlit geturðu forskoðað það til að ganga úr skugga um að það mæti kröfum þínum.
> [!Tip]
> Best er að vera með einn hluta í VSK-yfirliti með því að nota **Gerð** **Samtala VSK-færslu** og annan hluta hér að neðan með því að nota **Gerð** **Samtala fjárhags** til að stemma af upphæðir á grundvelli **VSK-færslu** í samræmi við upphæðina á **fjárhagsreikningunum**. Einnig er hægt að nota skýrsluna **Fjárhagur - VSK-afstemming** í þessum tilgangi.

1. Veljið **Forskoða**.
2. Sett er afmörkun á dagsetningu til að takmarka yfirlitið við tiltekið tímabil. Nánari upplýsingar um hvernig á að sérsníða síðuna til að dagsetningarafmörkun birtist eru í [Leita í, afmarka og raða gögnum](ui-enter-criteria-filters.md).
3. Hægt er að velja milli ýmissa valkosta til að skilgreina tegund VSK-færslna sem á að hafa með í yfirlitinu.
4. Í línunum þar sem reiturinn **Tegund** innheldur **Samtala VSK-færslna** er hægt að sjá lista yfir VSK-færslur með því að smella á upphæðina í reitnum **Upphæð dálks**.
5. Hægt er að nota sérstillingu til að sýna fleiri svæði á línunum. Til dæmis áætluð stofnupphæð og áætlað VSK-upphæð ef áætlaður VSK er notaður.

## Sjá einnig .

[Setja upp virðisaukaskatt](finance-setup-vat.md)    
[Uppsetning áætlaðs virðisaukaskatts](finance-setup-unrealized-vat.md)    
[Tilkynna VSK til skattyfirvalda](finance-how-report-vat.md)    
[Unnið með VSK í sölu og innkaupum](finance-work-with-vat.md)    
[Staðbundin virkni í Business Central](about-localization.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
