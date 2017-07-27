---
title: "Staðfesta sjálfvirkt jafnaðar greiðslur, og endurjafna greiðslur handvirkt | Microsoft Docs"
description: "Eftir að greiðslur hafa verið jafnaðar sjálfvirkt, geturðu endurskoðað allar færslurnar fyrir greiðslu og endurjafnað handvirkt þær sem voru ekki jafnaðar rétt."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, reconcile payment, expenses, cash receipts
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 2998cd0841452813cb86ee3859804de93cb9bde9
ms.contentlocale: is-is
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-review-or-apply-payments-manually-after-automatic-application"></a>Hvernig á að endurskoða eða jafna greiðslur handvirkt eftir sjálfvirka jöfnun
Fyrir hverja færslubókarlínu sem táknar greiðslu í glugganum **Greiðsluafstemmingarbók** er hægt að opna gluggann **Greiðslujafnanir** til að sjá alla möguleika opinna færslna fyrir greiðsluna og skoðað ítarlegar upplýsingar fyrir hverja færslu um gagnasamsvaranir sem greiðslujöfnun byggir á. Hér er hægt að jafna handvirkt greiðslur eða endurjafna greiðslur sem voru jafnaðar sjálfkrafa á ranga færslu. Nánari upplýsingar um sjálfvirka jöfnun eru í [Hvernig á að: Afstemma greiðslur með því að nota sjálfvirka jöfnun](receivables-how-reconcile-payments-auto-application.md).

> [!IMPORTANT]  
>   Þegar bankareikningurinn sem þú ert að jafna greiðslur fyrir er settur upp fyrir staðbundinn gjaldmiðil, þá sýnir glugginn **Greiðslujöfnun** allar opnar færslur í staðbundna gjaldmiðlinum, þ.m.t. opnar færslur fyrir skjöl sem voru upphaflega reikningsfærð í erlendum gjaldmiðli. Greiðslur sem beitt er til færslna með breyttum gjaldmiðlum má því birta með mismunandi magni en á upprunalegu skjali vegna hugsanlega mismunandi gengis sem bankinn notar og [!INCLUDE[d365fin](includes/d365fin_md.md)] í sömu röð.

Því mælum við með því að þú leitir að erlendum gjaldmiðilskóðum í reitnum **Gjaldmiðilskóði** í glugganum **Greiðslujafnanir** til að kanna hvort jafnanir byggi á umreiknuðum gjaldmiðlum. Til að endurskoða upphaflega upphæð fylgiskjalsins í erlendum gjaldmiðli og til að skoða gengið sem notað er skal velja reitinn **Jafna-við Færslu nr.** og síðan á flýtivalmyndinni skal velja hnappinn kafa niður til að opna gluggann **Færslur í viðskiptamannabók** eða **Færslur í lánardrottnabók**.

Allar leiðréttingar á hagnaði og tapi sem eru nauðsynlegar vegna umreiknings gjaldmiðils eru ekki meðhöndlaðar sjálfvirkt af [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!NOTE]  
>   Ekki er hægt að jafna færslur með öðru merki en merkinu á greiðslunni. Til að loka t.d. bæði kreditreikningi með neikvæðu merki, og tengdum reikningi með jákvæðu merki, verður fyrst að jafna kreditreikninginn við reikninginn, og svo jafna greiðsluna við reikninginn með lægri upphæðinni sem er eftirstandandi.

> [!WARNING]  
>   Ef þú notar greiðsluafslátt og greiðsludagur er á undan gjalddaga, þá mun reiturinn **Eftirstöðvar með afslætti** í glugganum **Greiðslujafnanir** verða notaður fyrir pörun. Annars verður gildið í reitnum **Eftirstöðvar** notað. Ef greiðslan fór fram með afsláttarupphæð eftir gjalddaga greiðslunnar, eða upphæðin var greidd að fullu en aflsáttur gefinn, þá mun upphæðin ekki passa.

> [!NOTE]  
>   Aðeins er hægt að jafna greiðslu við einn reikning. Ef þú vilt deila jöfnuninni á margar opnar færslur, t.d. til að jafna fasta greiðslu, þá þurfa opnu færslurnar að vera fyrir sama reikning. Frekari upplýsingar eru að finna í skrefi 7 og 8 í ferlinu fyrir þetta efnisatriði.

## <a name="to-review-or-apply-payments-after-automatic-application"></a>Til að endurskoða eða jafna greiðslur eftir sjálfvirk jöfnun
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **greiðsluafstemmingarbækur** og velja svo viðeigandi tengil.
2. Opna skal greiðsluafstemmingarbók fyrir bankareikning sem á að stemma af greiðslur fyrir. Frekari upplýsingar eru í [hvernig á að afstemma greiðslur með því að nota sjálfvirka jöfnun](receivables-how-reconcile-payments-auto-application.md)
3. Í glugganum **Greiðsluafstemmingarbók** skal velja greiðslu sem á að fara yfir eða jafna handvirkt við eina eða fleiri opnar færslur og veljið síðan aðgerðina **Jafna handvirkt**.
4. Veljið gátreitinn **Jafnað** á línunni fyrir opnu færsluna sem á að jafna greiðsluna við.
5. Greiðsluupphæðin, sem birtist einnig í reitnum **Færsluupphæð** í glugganum **Greiðslujafnanir** er sett inn í reitinn **Jöfnuð upphæð**, en hægt er að breyta reitnum, til dæmis ef jafna á upphæðina við nokkrar opnar færslur.
6. Til að jafna hluta af greiddri upphæð á aðra opna færslu fyrir reikninginn, t.d. til að jafna fastgreiðslu, velurðu gátreitinn **Jafnað** fyrir línuna. Jafnaða upphæðin er sjálfkrafa dregin frá færsluupphæðinni til að endurspegla dreifinguna á opnu færslunum tveimur.
7. Til að jafna hluta af greiðslu við eina eða fleiri opnar færslur sem eru ekki til í gagnagrunninum er ný lína stofnuð undir línunni fyrir sama reikning. Í reitnum **Jöfnuð upphæð** skal færa inn upphæðina sem jafna á í nýju línuna, og leiðrétta síðan reitinn **Jöfnuð Upphæð** á línunni sem fyrir var.
8. Endurtakið skref 5, 6 eða 7 fyrir aðrar opnar færslur sem á að jafna hluta eða alla greiðsluupphæðina við.
9. Þegar farið hefur verið yfir greiðslujafnanir eða jafnað handvirkt við eina eða fleiri færslur, skal velja aðgerðina **Samþykkja jöfnun**.

Glugganum **Greiðslujafnanir** er lokað og í glugganum **Greiðsluafstemmingarbók** er gildinu í reitnum **Áreiðanleiki samsvörunar** breytt í **Samþykkt** til að tákna að þú hafir endurskoðað eða handvirkt jafnað greiðsluna.

## <a name="see-also"></a>Sjá einnig
[Stjórnun skulda](receivables-manage-receivables.md)  
[Sala](sales-manage-sales.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

