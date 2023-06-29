---
title: Hönnunarupplýsingar - Vörurakning og áætlun | Microsoft Docs
description: 'Vegna þess að þær eru geymdar í frátekningarkerfi, eru vörurakningarnúmer að fullu samstillt við pöntunarrakningarfærslur.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: edupont
---
# <a name="design-details-item-tracking-and-planning"></a><a name="design-details-item-tracking-and-planning"></a>Hönnunarupplýsingar: vörurakning og áætlun
Vegna þess að þær eru geymdar í frátekningarkerfi, eru vörurakningarnúmer að fullu samstillt við pöntunarrakningarfærslur. Þetta þýðir að vörur með pöntunarrakningarfærslur má úthluta vörurakningarnúmerum. Hins vegar geta vörur með vörurakningarnúmerum orðið vörurakningarfærslur. Nánari upplýsingar eru í [Hönnunarupplýsingar: Vörurakningarhönnun](design-details-item-tracking-design.md).

Frekari upplýsingar um samþætt kerfi eru í [Hönnunarupplýsingar: Frátekningar, pöntunarrakning og aðgerðaboð](design-details-reservation-order-tracking-and-action-messaging.md).

Þar sem pöntunarrakning varðar aðeins tiltekna vörujöfnun gilda hnitin með vörurakningarnúmerum aðeins fyrir vörurnar sem eru settar upp til að nota tiltekna vörurakningu. Þetta er stillt með **SN sértæk rakning** og **Lotusértæk rakning** reitunum á birgðaspjaldinu, sem tilgreinir eftirfarandi:

- Varan verður að vera með raðnúmer eða lotunúmer þegar hún er bókuð.
- Varan verður að eiga við sama raðnúmer eða lotunúmer þegar hún er bókuð á útleið.

Í samræmi við staðlaðar jöfnunarreglur framboðs/eftirspurnar passar áætlanagerðarkerfi og tengdur pöntunarrakningareiginleiki aðeins við framboð og eftirspurn með vörurakningarnúmerum ef varan sem um ræðir notar tiltekna vörurakningu. Í öllum öðrum tilvikum hunsar áætlunargerðar- og pöntunarrakningarkerfin vörurakningarnúmer þegar þau beita framboði til að mæta eftirspurn eða beita eftirspurn á framboð. Nánari upplýsingar eru í [Upplýsingar um hönnun: Frátekning, Vörurakning og aðgerðaboð](design-details-reservation-order-tracking-and-action-messaging.md).

Til dæmis þegar pöntunarrakning er til fyrir tiltekna vöru gefur það til kynna að færslur fyrir vöruna eru þegar í töflunni **Frátekningarfærsla** sem er kjarni frátekningarkerfisins, áður en vörurakningarnúmerin eru skilgreind. Því gilda eftirfarandi tengitakmarkanir um vörurakningarnúmer sem rekja á til pöntunar:

- Eftirspurn með raðnúmeri eða lotunúmeri getur aðeins náð yfir framboð með sama raðnúmeri eða lotunúmeri.
- Eftirspurn án raðnúmers eða lotunúmers getur náð yfir hvaða framboð sem er, með eða án rað- eða lotunúmers.

Fyrir utan afleiðingar hennar á gagnvirka pöntunarrakningu hafa tengitakmarkanir vörurakningar ekki nein veruleg áhrif á kerfi áætlanagerðar.

Hvað varðar framboð er rað- eða lotunúmer yfirleitt ekki fært inn fyrr en rétt áður en pöntun er bókuð, t.d. sem innkaupakvittun í vöruhús. Þegar slegið er inn rað- eða lotunúmer eftirspurnarmegin, t.d. sölupöntun, er það rað- eða lotunúmer þegar í birgðum. Samkvæmt því eru vörurakningarnúmer yfirleitt ekki vandamál í framboðsáætlun.

Fyrir vörur sem nota tiltekna vörurakningu verður að stemma alla eftirspurn með rað- eða lotunúmer við tilheyrandi framboð. Í flestum tilfellum er ekki skynsamlegt að endurpanta ákveðin rað- eða lotunúmer, þannig að áætlanagerð innkaupa eða framleiðsluframboð verður líklega ekki fyrir áhrifum. Ef vörur eru hinsvegar fluttar frá einni staðsetningu til annarrar er líklegt að flutningurinn sé fyrir tiltekna lotu, sem þýðir að tiltekin tengitakmörkun geti hugsanlega haft áhrif á áætlun flutningsbirgða.

Nánari upplýsingar eru í [Hönnunarupplýsingar: Flutningur í áætlun](design-details-transfers-in-planning.md).

## <a name="balancing-demand-and-supply"></a><a name="balancing-demand-and-supply"></a>Jöfnun eftirspurnar og framboðs
Ef vara þarf ákveðna vörurakningu er pöntunarrakningartengill búinn til úr allri eftirspurn vörurakningar í allt samsvarandi framboð vörurakningar, með þeirri einu takmörkun að framboð ætti að koma á undan eftirspurn. Ef ekkert vörurakningarframboð finnst sem samsvarar tiltekinni vörurakningareftirspurn við þessar kringumstæður, er nýtt vörurakningarframboð strax búið til og án þess að íhuga pantanastærð, áætlanagerðarfæribreytur eða enduráætlun núverandi framboðs með sama raðnúmer eða lotunúmer.

Ef vörurakningarnúmerum er úthlutað á eftirspurnarhliðinni eða á framboðshliðinni án þess að tiltekinnar vörurakningar sé krafist er pöntunarrakningartengill búinn til úr eftirspurninni fyrir það framboð, á grunni hentugustu tímasetningar og magns, eins og í venjulegu afstemmingaraðferðinni. Tilgreint vörurakningarnúmer fer í pöntunarrakningarfærsluna á sama hátt og sérhvert vörurakningarmagn skilgreinir annan enda pöntunarrakningartengils. Þetta þýðir að vörurakningarnúmerið sem slegið er inn varðveitist á meðan það er einnig hluti af pöntunarrakningarfærslunni.

Ef vörurakningarnúmerum er úthlutað á framboðshliðinni án þess að tiltekinnar vörurakningar sé krafist lítur áætlanakerfið á þetta framboð sem fast. Ekki stungið upp á breytingum á stærð eða áætlun fyrir þetta framboð en framboðið er tekið með í reikninginn þegar áætlanakerfið reynir að uppfylla brúttóþörfina.

Nánari upplýsingar er að finna í [Hönnunarupplýsingar: Jöfnun eftirspurnar og framboðs](design-details-balancing-demand-and-supply.md).  

## <a name="see-also"></a><a name="see-also"></a>Sjá einnig
[Hönnunarupplýsingarn: vörurakning hönnun](design-details-item-tracking-design.md)  
[Hönnunarupplýsingar: Jöfnun eftirspurn og framboð](design-details-balancing-demand-and-supply.md)  
[Hönnunarupplýsingar: Pöntun, pöntunarrakning og stöðuboð](design-details-reservation-order-tracking-and-action-messaging.md)   
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
