---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 30214f3fdd02343b064432a0f4f621e7a87765e9
ms.sourcegitcommit: 2c972dfc94d27245eaa99efcf638d030dedafb22
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/09/2022
ms.locfileid: "8104053"
---
Eftirfarandi tafla lýsir sumum helstu skýrslunum í verkskýrslugerð.

|Skýrsla |Kenni hlutar|Description  |
|---------|---------|---------|
|**Verkgreining**|1008|Greinir verk notanda með því að nota stillingar sem notandi tilgreindi. Til dæmis má gera skýrslu sem sýnir áætlað verð, notkunarverð og reikningshæft verð, og gerir síðan samanburð á þessu þrennu.<br>Nota skal samsetningu **Upphæð** reita til að búa til eigin greiningu. Fyrir hvern reit skal velja eftirfarandi verð, kostnað eða framlegðargildi: Áætlun, Notkun, Samningur og Reikningsfært. <br>Velja skal hvort gjaldmiðillinn er tilgreindur sem Staðbundinn gjaldmiðill eða Erlendur gjaldmiðill. |
|**Áætlunarlínur verks**|1006|Í þessari skýrslu eru sýndar mismunandi verkáætlanir og verkefnalínur - þar á meðal línategund, magn, mælieiningar, heildarkostnað o.s.frv.|
|**Verk afgreitt í áætlun**|1009|Bera saman tímasettar og notaðar upphæðir tiltekinna verka. Allar línur í völdu verki sýna magn, heildarkostnað og línuupphæð. <br>Skýrslan er ætluð fyrir lokin verk, þótt nota megi hana hvenær sem er meðan á verki stendur.<br>Þessi skýrsla er ekki tiltæk í Bandaríkjunum, Kanada og Mexíkó. Í staðinn skal nota skýrslurnar **Raunkostnaður verks í kostnað á fjárhagsáætlun (kostnaður)** (10210) eða **Raunverð verks í verð á fjárhagsáætlun (verð)** (10211).|
|**Reikningatillögur verka**|1011|Þessi skýrsla sýnir lista yfir öll verk, flokkuð eftir viðskiptamönnum. Hún sýnir hversu mikið þegar hefur verið reikningsfært á viðskiptamanninn, og hve mikið eftir er að reikningsfæra (tillaga um útgáfu reikninga). <br>Þessi skýrsla er ekki tiltæk í Bandaríkjunum, Kanada og Mexíkó. Þess í stað skal nota skýrsluna um **Tillögur að greiðslukostnaði verks** (10219).|
|**Verk á viðskiptamann**|1012|Þessi skýrsla sýnir lista yfir öll verk, flokkuð eftir viðskiptamönnum. Hún auðveldar samanburð á áætlað verð, prósentum lokinna verka, reikningsfærðu verði og prósentu reikningsfærðra upphæða fyrir hvern viðskiptamann sem **reikningsfært er á**.|
|**Vörur á verk** eða **Verk á vöru**|1013 eða 1014|Yfirlit yfir hluti sem eru notaðir í verki. Hægt er að setja upp viðbótarsíu eftir því hvaða skýrslu á að nota til að fá yfirlit yfir fyrirhugaða hluti fyrir verk. Skýrslan sýnir viðeigandi hkluti og uppsafnað gildi kostnaðarins.|
|**Verk - Sundurl. færslur**|1007|Í þessari skýrslu er yfirlit yfir bókuð verkefni eins og tilföng og atriði. Inniheldur ítarlegar upplýsingar um heildarkostnað og heildarverð auk upplýsinga um línuafslátt o.s.frv. Skýrslan sýnir gögn úr verkbókarfærslum.|
|**VÍV verks í fjárhag**|1010|Sýnir virði verks í vinnslu fyrir valin verk samanborið við upphæðina sem bókuð hefur verið í fjárhag.|