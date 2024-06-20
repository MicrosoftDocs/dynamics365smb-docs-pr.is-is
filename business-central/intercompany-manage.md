---
title: Vinna með millifyrirtækjafærslur
description: Með milli-fyrirtækjavirkninni getur einfaldað fyrirtækjaferli og færslur á milli dótturfyrirtækja innan sama fyrirtækis.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 05/24/2024
ms.custom: bap-template
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary'
ms.search.form: '605,'
ms.service: dynamics-365-business-central
---
# <a name="managing-intercompany-transactions"></a>Vinna með millifyrirtækjafærslur

Fyrirtæki með fleiri en einn lögaðila með aðskildar bókhaldsaðgerðir geta haft gagn af færslum milli fyrirtækja. Það er til dæmis gagnlegt fyrir fyrirtæki sem hafa dótturfyrirtæki á mörgum alþjóðlegum mörkuðum eða svæðum. Einnig gæti fyrirtæki verið með nokkur fyrirtæki en skortir sambærilegan fjölda bókhalds- og stjórnunarteyma. Færslur milli fyrirtækja einfaldar og straumlínuviðskiptaferli og færslur milli fyrirtækja í samstarfi milli fyrirtækja.

Þegar búið er að tilgreina tengsl viðskiptamanns og lánardrottins fyrir færslur milli fyrirtækja færa félagar inn upplýsingar einu sinni í sölu- og innkaupaskjöl. Samsvarandi fylgiskjal er stofnað hjá öðrum félaganum sem tengist færslunni. Vörpun bókhaldslykils og vídda tryggir að upplýsingarnar birtist á réttum stöðum.  

Fjórir meginkostir eru fyrir aðgerðir milli fyrirtækja:  

* Tímasparnaður og einfaldari færslur auka afköst  
* Lágmarks mistök með einu sinni innslátt upplýsinga og sjálfvirkra uppfærslna í kerfinu  
* Gegnsæ slóð endurskoðunar og fullur sýnileiki inn í viðskiptastarf og færslusagnir  
* Skilvirk viðskipti við tengd fyrirtæki og dótturfyrirtæki  

## <a name="streamline-the-flow-of-business-activities"></a>Straumlína flæði viðskiptaaðgerða

Færslur milli fyrirtækja gera kleift að dreifa sölu- og innkaupaskjölum og færslubókarfærslum á allar skrifstofur í gervihnöttum, söluskrifstofum eða dótturfyrirtækjum. Dreifing færslna sparar tíma og eykur skilvirkni alls staðar í fyrirtækinu með því að minnka gagnafærslu. Það sker úr um nauðsyn þess að senda, taka á móti, prenta og geyma sölu- og innkaupaskjöl.  

Þú hefur fulla stjórn á öllum færsluskjölum. Til dæmis er hægt að hafna skjali sem sent er og nota **aðgerðirnar Bakfæra bókanir** og **Afturkalla móttökur/afhendingar** til að gera leiðréttingar. Eða þegar keypt er frá félaga eða dótturfyrirtæki er hægt að uppfæra innkaupapöntunina ef fyrirtækið sem seljandi hefur ekki sent vörurnar.  

Þegar færsla er færð inn þarf ekki að tilgreina reikningana sem á að nota. Millifyrirtækjafélaginn er valinn. Aðgerðin milli fyrirtækja stofnar færslubókarlínur sem stemma af bækur beggja fyrirtækja sem taka þátt í færslunni. Í Útistandandi og viðskiptaskuldir er MF-félagakóta úthlutað á hvaða viðskiptamann eða lánardrottin sem er. Frá þeirri stundu framleiða allar pantanir og reikningar fyrir viðskipti milli þessara fyrirtækja samsvarandi skjala í fyrirtæki félagans. Útkoman er jafnaður reikningur á réttan hátt.  

Milli-fyrirtækja einbeitir sér að sölu- og innkaupaskjölum og færslubókarlínum og leyfir færslur milli margra [!INCLUDE [prod_short](includes/prod_short.md)] gagnagrunna. Dæmi:

* Mismunandi lönd/svæði
* Margir gjaldmiðlar
* Mismunandi bókhaldslyklar
* Mismunandi víddir
* Mismunandi vörunúmer  

Færslur milli fyrirtækja notast við nokkrar gerðir færslna og skjala:  

* Færslur í færslubók
* Innkaupa- og sölupantanir
* Innkaupa- og sölureikningar
* Kreditreikningar
* Skilapantanir

Þegar færslur milli fyrirtækja eru settar upp er listi yfir MF-félaga stofnaður, MF-bókhaldslykill og millifyrirtækjavíddir. Síðan er hægt að stofna færslur í færslubókum milli fyrirtækja.

> [!NOTE]
> Færslubókin inniheldur ekki gjaldmiðla. Hún breytir öllum upphæðum í staðarmynt á gildandi gengi.

Þegar viðskiptafélagar hafa verið settir upp sem viðskiptamenn og lánardrottnar og þeim úthlutað MF-félagakótum geta þeir skipst á innkaupa- og söluskjölum milli fyrirtækja, þar á meðal vörum og kostnaðarauka. 

> [!NOTE]
> Fyrirtæki geta ekki notað milli-fyrirtækja til að skiptast á öllum gerðum gagna. Innkaupreikningar eru ekki sendir til viðskiptafélaga í gegnum ferli milli fyrirtækja. Hins vegar verða sölureikningar sem lagðir eru inn í gegnum ferli milli fyrirtækja stofnaðir sem innkaupareikningar í móttökufyrirtækinu.

Sameining fjárhagsgagna gæti skipt máli fyrir ferli milli fyrirtækja. Frekari upplýsingar er að finna í [Steypa saman fjárhagsgögnum frá mörgum fyrirtækjum](finance-consolidated-company-reporting.md).

Eftirfarandi tafla lýsir röð verkefna með tenglum í greinar þar sem þeim er lýst.

|Til |Sjá|
|---|---|
|Stofna lánardrottna milli fyrirtækja og viðskiptamenn sem samstarfsaðila og setja upp bókhaldslykil milli fyrirtækja.|[Uppsetning milli fyrirtækja](intercompany-how-setup.md)|
|Milli-fyrirtækjaskjöl eða færslubækur eru notuð til að bóka viðskipti við milli-fyrirtækjafélaga.|[Unnið með samstæðuskjöl og færslubækur](intercompany-how-work-documents-journals.md)|
|Skipuleggja og vinna færslur á inn- og útleið sem þú og millifyrirtækjafélagar þínir sendið ykkar á milli.|[Stjórna millifyrirtækja innhólfsfærslur og úthólfsfærslur](intercompany-how-manage-intercompany-inbox.md)|
|Nota færslur milli fyrirtækja til að dreifa kostnaði á milli samstarfsfyrirtækja.|[Úthluta kostnaði til millifyrirtækjafélaga](intercompany-allocate-costs.md)|

## <a name="see-also"></a>Sjá einnig

[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Vinna í færslubókum](ui-work-general-journals.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
