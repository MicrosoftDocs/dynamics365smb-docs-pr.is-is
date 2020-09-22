---
title: Reglur settar upp fyrir sjálfvirka jöfnun á greiðslum
description: Á síðunni fyrir greiðslujöfnunarreglur eru settar upp reglur til að stjórna því hvernig greiðslur/bankafærslur eiga að vera sjálfkrafa jafnaðar við tengdar opnar fjárhagsfærslur þegar þú notar aðgerðina Notað sjálfkrafa á síðunni Greiðsluafstemmingarbók.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 07/23/2020
ms.author: edupont
ms.openlocfilehash: 255f7c66dc040f10aeae76b5ed08920ad8c1f77f
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2020
ms.locfileid: "3782750"
---
# <a name="set-up-rules-for-automatic-application-of-payments"></a>Reglur settar upp fyrir sjálfvirka jöfnun á greiðslum

Á síðunni **Greiðslujöfnunarreglur** seturðu upp reglur til að stjórna því hvernig greiðslutexti (á bankafærslu) er sjálfkrafa jafnaður við texta á opnum færslum í eftirfarandi tveimur ferlum:

- Jafna greiðslur sjálfkrafa við tengda opna (ógreidda) reikninga, kreditreikninga eða aðrar færslur þegar aðgerðin **Nota sjálfkrafa** er notuð á síðunni **Greiðsluafstemmingarbók**. Frekari upplýsingar eru í [afstemma greiðslur með því að nota sjálfvirk jöfnun](receivables-how-reconcile-payments-auto-application.md)

- Jafna sjálfkrafa bankafærslur við tengdar, innri fjárhagsfærslur bankareiknings þegar þú velur aðgerðina **Jafna sjálfkrafa** á síðunni **Afstemming bankareiknings**. Frekari upplýsingar er að finna í [Afstemma bankareikninga](bank-how-reconcile-bank-accounts-separately.md).

Hægt er að setja upp greiðslujöfnunarreglur með því að velja hvaða gerðir gagna á greiðsluafstemmingarbókarlínu verða að passa við gögn á einni eða fleiri opinni færslu áður en tengda greiðslan er sjálfkrafa jöfnuð við opnu færslurnar. Gæði hverrar sjálfvirkrar jöfnunar er sýnd sem gildið **Lágt** til **Hátt** í reitnum **Áreiðanleiki jöfnunar** á síðunni **Greiðsluafstemmingarbók** samkvæmt greiðslujöfnunarreglunni sem var notuð.

Hver röð á síðunni **Greiðslujöfnunarreglur** stendur fyrir greiðslujöfnunarreglu. Reglur eru notaðar í þeirri röð sem tilgreind er í reitnum **Flokkunarröð**. Ef margar reglur eru notaðar á sama tíma þá er áreiðanleiki samsvörunar af hæstu reglu notaður.

Sjálfvirk virkni jöfnunar byggir á vörpunarskilyrðum með forgangi. Fyrst reynir fallið, í forgangsröð, að para saman texta í reitunum fimm sem merktir eru **Tengdur aðili** á færslubókarlínu með texta í bankareikningi, nafni eða aðsetri viðskiptamanna eða lánardrottna með ógreidd skjöl sem tákna opnar færslur. Síðan reynir aðgerðin að para saman texta í reitunum **Færslutexti** og **Viðbótarfærsluupplýsingar** í færslubókarlínu við texta í reitunum **Nr. ytra skjals** og **Nr. fylgiskjals** í opnum færslum. Að lokum reynir aðgerðin að tengja upphæðina í reitnum **Upphæð yfirlits** í færslubókarlínu við upphæðina á opnum færslum.

> [!NOTE]
> Textajöfnun er aðeins möguleg fyrir texta sem er lengri en fjórir stafir.

Auk jöfnunarskilyrðanna í töflunni gildir eftirfarandi um merki greiðsluupphæðarinnar:

- Fyrir mínustölur er fyrst jafnað við opnar færslur sem tákna reikninga viðskiptavina og svo við kreditreikninga lánardrottins.
- Fyrir plústölur er fyrst jafnað við opnar færslur sem tákna reikning lánardrottins og svo við kreditreikninga viðskiptamanns.

## <a name="to-set-up-a-payment-application-rule"></a>Til að setja upp greiðslujafnanarreglu
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Greiðslujöfnunarreglur** og veldu síðan tengda tengilinn.
2. Skilgreina skal nýja eða breytta greiðslujöfnunarreglu með því að fylla inn í reitina í línu eins og lýst er í eftirfarandi töflu.

|Svæði|Description|
|-|-|
|**Áreiðanleiki samsvörunar**|Tilgreinir áreiðanleikamat þitt á jöfnunarreglu sem er tilgreind fyrir línuna. <br /></br>Gildi sem þú skilgreinir í þessum reit birtist í reitnum **Áreiðanleiki samsvörunar** á síðunni **Greiðsluafstemmingarbók** í samræmi við gæði sjálfvirkrar greiðslujöfnunar í færslubókarlínunni.|
|**Forgangur**|Tilgreinir forgang jöfnunarreglunnar í tengslum við aðrar jöfnunarreglur sem eru skilgreindar sem línur á síðunni **Greiðslujöfnunarreglur**. 1 táknar hæsta forgang.|
|**Samsvörun fannst fyrir tengdan aðila**|Tilgreinir hversu miklar upplýsingar um viðskiptamann eða lánardrottin, t.d heimilisfang, borgarheiti og bankareikningsnúmer, á færslubókarlínu greiðsluafstemmingar þurfa að passa við upplýsingar um opnu færsluna áður en jöfnunarreglan verður notuð til að jafna sjálfvirkt greiðslu sjálfkrafa við opnu færsluna.|
|**Samsvörun fannst fyrir skjalsnr./nr. ytra skjals**|Tilgreinir hvort texti á færslubókarlínu greiðsluafstemmingar þarf að samsvara gildinu í reitnum **Nr. fylgiskjals** eða reitnum **Númer ytra skjals** á opnu færslunni áður en jöfnunarreglan verður notuð til að jafna sjálfvirkt greiðslu við opnu færsluna.|
|**Samsvörun fannst fyrir upphæð með vikmörkum**|Tilgreinir hversu margar færslur fyrir viðskiptamann eða lánardrottin þurfa að samsvara upphæðinni með greiðsluvikmörkum áður en jöfnunarreglan verður notuð til að jafna sjálfvirkt greiðslu við opnu færsluna.|

Eftirfarandi tafla sýnir hvaða greiðslujafnanarreglur eru settar upp í almennri útgáfu [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!Important]
> Greiðslujöfnunarreglur kunna að vera mismunandi í innleiðingu þinni á [!INCLUDE[d365fin](includes/d365fin_md.md)].

| Áreiðanleiki samsvörunar | Forgangur | Samsvörun fannst fyrir tengdan aðila | Skjalsnr./nr. ytra skjals Samsvörun | Samsvörun fannst fyrir upphæð með vikmörkum |
|------------------|----------|-----------------------|--------------------------------|--------------------------------|
| Hátt             | 1        | Öll                 | Já - margt                 | Ein niðurstaða                      |
| Hátt             | 2        | Öll                 | Já - margt                 | Margar niðurstöður               |
| Hátt             | 3        | Öll                 | Já                            | Ein niðurstaða                      |
| Hátt             | 4        | Öll                 | Já                            | Margar niðurstöður               |
| Hátt             | 5        | Að hluta             | Já - margt                 | Ein niðurstaða                      |
| Hátt             | 6        | Að hluta             | Já - margt                 | Margar niðurstöður               |
| Hátt             | 7        | Að hluta             | Já                            | Ein niðurstaða                      |
| Hátt             | 8        | Öll                 | Nr                             | Ein niðurstaða                      |
| Hátt             | 9        | Nr                    | Já - margt                 | Ein niðurstaða                      |
| Hátt             | 10       | Nr                    | Já - margt                 | Margar niðurstöður               |
| Miðlungs           | 1        | Öll                 | Já - margt                 | Ekki tekið með                 |
| Miðlungs           | 2        | Öll                 | Já                            | Ekki tekið með                 |
| Miðlungs           | 3        | Öll                 | Nr                             | Margar niðurstöður               |
| Miðlungs           | 4        | Að hluta             | Já - margt                 | Ekki tekið með                 |
| Miðlungs           | 5        | Að hluta             | Já                            | Ekki tekið með                 |
| Miðlungs           | 6        | Nr                    | Já                            | Ein niðurstaða                      |
| Miðlungs           | 7        | Nr                    | Já-margt                   | Ekki tekið með                 |
| Miðlungs           | 8        | Að hluta             | Nr                             | Ein niðurstaða                      |
| Miðlungs           | 9        | Nr                    | Já                            | Ekki tekið með                 |
| Lítill              | 1        | Öll                 | Nr                             | Engar niðurstöður                     |
| Lítill              | 2        | Að hluta             | Nr                             | Margar niðurstöður               |
| Lítill              | 3        | Að hluta             | Nr                             | Engar niðurstöður                     |
| Lítill              | 4        | Nr                    | Nr                             | Ein niðurstaða                      |
| Lítill              | 5        | Nr                    | Nr                             | Margar niðurstöður               |

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/reconciliation-journals-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig
[Afstemma greiðslur með sjálfvirkri jöfnun](receivables-how-reconcile-payments-auto-application.md)  
[Stjórnun skulda](receivables-manage-receivables.md)  
[Sala](sales-manage-sales.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
