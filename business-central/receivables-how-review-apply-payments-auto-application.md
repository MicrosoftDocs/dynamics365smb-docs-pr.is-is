---
title: Staðfesta sjálfvirkt jafnaðar greiðslur, og endurjafna greiðslur handvirkt | Microsoft Docs
description: Eftir að greiðslur hafa verið jafnaðar sjálfvirkt, geturðu endurskoðað allar færslurnar fyrir greiðslu og endurjafnað handvirkt þær sem voru ekki jafnaðar rétt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, reconcile payment, expenses, cash receipts
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: bcb3ffbf7bab30b71cea7c2f1005124415ab2ae4
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748519"
---
# <a name="review-or-apply-payments-manually-after-automatic-application"></a>Endurskoða eða jafna greiðslur handvirkt eftir sjálfvirka jöfnun
Fyrir hverja færslubókarlínu sem táknar greiðslu í **greiðsluafstemmingarbók** síðunni geturðu opnað **greiðslujafnanir** síðuna til að sjá alla möguleika opinna færslna fyrir greiðsluna og skoðað ítarlegar upplýsingar fyrir hverja færslu um gagnasamsvaranir sem greiðslujöfnun byggir á. Hér er hægt að jafna handvirkt greiðslur eða endurjafna greiðslur sem voru jafnaðar sjálfkrafa á ranga færslu. Nánari upplýsingar um sjálfvirka jöfnun eru í [Afstemma greiðslur með því að nota sjálfvirka jöfnun](receivables-how-reconcile-payments-auto-application.md).

> [!IMPORTANT]  
>   Þegar bankareikningurinn sem þú ert að jafna greiðslur fyrir er settur upp fyrir staðbundinn gjaldmiðil, þá sýnir síðan **Greiðslujöfnun** allar opnar færslur í staðbundna gjaldmiðlinum, þ.m.t. opnar færslur fyrir skjöl sem voru upphaflega reikningsfærð í erlendum gjaldmiðli. Greiðslur sem beitt er til færslna með breyttum gjaldmiðlum má því birta með mismunandi magni en á upprunalegu skjali vegna hugsanlega mismunandi gengis sem bankinn notar og [!INCLUDE[prod_short](includes/prod_short.md)] í sömu röð.

Því mælum við með því að þú leitir að erlendum gjaldmiðilskóðum í reitnum **Gjaldmiðilskóði** á síðunni **Greiðslujafnanir** til að kanna hvort jafnanir byggi á umreiknuðum gjaldmiðlum. Til að skoða upprunalegu upphæðina á skjalinu í erlenda gjaldmiðlinum og sjá gengið sem er notað, velurðu **Jafna við færslu nr.** reitinn, og svo, á flýtivalmyndinni, velurðu Kafa niður til að opna **Viðskiptamannafærslur** eða **Lánardrottnafærslur** síðuna.

Allar leiðréttingar á hagnaði og tapi sem eru nauðsynlegar vegna umreiknings gjaldmiðils eru ekki meðhöndlaðar sjálfvirkt af [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]  
>   Ekki er hægt að jafna færslur með öðru merki en merkinu á greiðslunni. Til að loka t.d. bæði kreditreikningi með neikvæðu merki, og tengdum reikningi með jákvæðu merki, verður fyrst að jafna kreditreikninginn við reikninginn, og svo jafna greiðsluna við reikninginn með lægri upphæðinni sem er eftirstandandi.

> [!WARNING]  
>   Ef þú notar greiðsluafslátt og greiðsludagur er á undan gjalddaga, þá mun reiturinn **Eftirstöðvar með afslætti** á síðunni **Greiðslujafnanir** verða notaður fyrir pörun. Annars verður gildið í reitnum **Eftirstöðvar** notað. Ef greiðslan fór fram með afsláttarupphæð eftir gjalddaga greiðslunnar, eða upphæðin var greidd að fullu en aflsáttur gefinn, þá mun upphæðin ekki passa.

> [!NOTE]  
>   Aðeins er hægt að jafna greiðslu við einn reikning. Ef þú vilt deila jöfnuninni á margar opnar færslur, t.d. til að jafna fasta greiðslu, þá þurfa opnu færslurnar að vera fyrir sama reikning. Frekari upplýsingar eru að finna í skrefi 7 og 8 í ferlinu fyrir þetta efnisatriði.

## <a name="to-review-or-apply-payments-after-automatic-application"></a>Til að endurskoða eða jafna greiðslur eftir sjálfvirk jöfnun
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Greiðsluafstemmingarbækur** og veldu síðan tengda tengilinn.
2. Opna skal greiðsluafstemmingarbók fyrir bankareikning sem á að stemma af greiðslur fyrir. Frekari upplýsingar eru í [afstemma greiðslur með því að nota sjálfvirk jöfnun](receivables-how-reconcile-payments-auto-application.md)
3. Á síðunni **Greiðsluafstemmingarbók** skal velja greiðslu sem á að fara yfir eða jafna handvirkt við eina eða fleiri opnar færslur og veljið síðan aðgerðina **Jafna handvirkt**.
4. Veljið gátreitinn **Jafnað** á línunni fyrir opnu færsluna sem á að jafna greiðsluna við.
5. Greiðsluupphæðin, sem birtist einnig í reitnum **Færsluupphæð** á síðunni **Greiðslujafnanir** er sett inn í reitinn **Jöfnuð upphæð**, en hægt er að breyta reitnum, til dæmis ef jafna á upphæðina við nokkrar opnar færslur.
6. Til að jafna hluta af greiddri upphæð á aðra opna færslu fyrir reikninginn, t.d. til að jafna fastgreiðslu, velurðu gátreitinn **Jafnað** fyrir línuna. Jafnaða upphæðin er sjálfkrafa dregin frá færsluupphæðinni til að endurspegla dreifinguna á opnu færslunum tveimur.
7. Til að jafna hluta af greiðslu við eina eða fleiri opnar færslur sem eru ekki til í gagnagrunninum er ný lína stofnuð undir línunni fyrir sama reikning. Í reitnum **Jöfnuð upphæð** skal færa inn upphæðina sem jafna á í nýju línuna, og leiðrétta síðan reitinn **Jöfnuð Upphæð** á línunni sem fyrir var.
8. Endurtakið skref 5, 6 eða 7 fyrir aðrar opnar færslur sem á að jafna hluta eða alla greiðsluupphæðina við.
9. Þegar farið hefur verið yfir greiðslujafnanir eða jafnað handvirkt við eina eða fleiri færslur, skal velja aðgerðina **Samþykkja jöfnun**.

Síðunni **Greiðslujafnanir** er lokað og á síðunni **Greiðsluafstemmingarbók** er gildinu í reitnum **Áreiðanleiki samsvörunar** breytt í **Samþykkt** til að tákna að þú hafir endurskoðað eða handvirkt jafnað greiðsluna.

## <a name="see-also"></a>Sjá einnig
[Stjórnun skulda](receivables-manage-receivables.md)  
[Sala](sales-manage-sales.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
