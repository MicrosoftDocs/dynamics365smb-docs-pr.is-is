---
title: Vinna með eignir
description: Kynntu þér virkni eigna og fáðu yfirsýn yfir það hvernig skuli vinna með og stjórna eignum.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'machinery, buildings'
ms.search.form: '5604, 5606, 5664, 5601, 5602, 5658, 5603, 5671, 5641, 5629, 5633, 5634, 5649, 5622, 5650'
ms.date: 05/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="manage-fixed-assets"></a>Vinna með eignir

Með aðgerðinni Eignir í [!INCLUDE[prod_short](includes/prod_short.md)] fæst yfirlit yfir eignir notanda og hjálpar til við að tryggja að afskriftir þeirra séu réttar. Með honum er einnig auðveldara að rekja viðhaldskostnað, stjórna vátryggingarskilmálum, bóka eignafærslur og búa til ýmsar skýrslur og upplýsingar.

## <a name="what-is-a-fixed-asset"></a>Hvað er eign?

Eignir eru frábrugðnar öðrum vörum í vöruhúsinu. Eign, sem einnig er nefnd fjármagnseign, er áþreifanlegur hlutur eignar, verksmiðju eða búnaðar (PP&E) sem þú átt eða hefur umsjón með með þeirri væntingu að hún muni halda áfram að búa til tekjur. Eign er föst þegar vara sem fyrirtækið notar ekki, selur eða skiptist í reiðufé innan næsta almanaksárs. Eignir eru aðrar en núgildandi eignir sem eru með reiðufé eða skellt í reiðufé á næstu 12 mánuðum. Eignir eru einnig frábrugðnar birgðum þar sem birgðir eru yfirleitt notaðar innan skamms tíma.

## <a name="types-of-fixed-assets"></a>Tegundir eigna

Fyrirtæki fjárfesta yfirleitt í nokkrum tegundum eigna. Nokkur dæmi eru:

- Byggingar og aðstaða
- Tölvubúnaður og hugbúnaður
- Húsgögn og innréttingar
- Tæki
- Ökutæki

## <a name="understanding-fixed-asset-accounting"></a>Að skilja eignabókhald

Eignabókhald merkir að halda nákvæmar fjárhagslegar færslur um fjármagnseignir. Meðal þessara færslna eru upplýsingar um þrepin fimm í lífskjörum eignar. Eftir upphaflegu innkaupin felur lífeyri hverrar eignar í sér að minnsta kosti þrjú af eftirfarandi þrepum:

- Kaup: Nýrri eign er bætt við bækurnar.
- Afskriftir: Reglubundin hlutfall eignar er skráð sem afskriftaaðferð er notuð til að reikna. Nánari upplýsingar eru notaðar með því að [fara í Eignaafskriftaútreikning](LocalFunctionality/India/FA_Depreciation.md).
- Endurmat: Skráð er úttekt á núverandi sanngjörnu markaðsvirði eignar. Nánari upplýsingar eru notaðar með því að fara í [Endurmeta eignir](fa-how-revalue.md).
- Virðisrýrnun: Lækkun virðis er skráð vegna atburða eða aðstæðna.
- Afskráning: Selt er, úrkast eða með öðrum hætti afskráð eign í lok líftíma hennar.

Endurskoðendur eru einnig innifaldir í nákvæmum ávísunum á bókhaldsskrár fyrirtækisins eftir að bókum er lokað á fjármálaárinu. Hvort sem um er að ræða innri eða ytri endurskoðanir þar sem ósamræmi er milli athugasemda og raunverulegrar stöðu eigna. Endurskoðendur stuðla að gegnsæi í eignunum og bókhaldinu ef þú tapar meiri peningum en fyrirhugað er.

## <a name="video-overview"></a>Myndbandsyfirlit

Eftirfarandi myndband fjallar um grunnatriði eigna:

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4AegS?rel=0]

## <a name="initial-setup-of-fixed-assets"></a>Upphafleg uppsetning eigna

Áður en hægt er að stjórna eignum þarf að fylla út eftirfarandi uppsetningar:

- Sjálfgildi
- Eignabókhald
- Bókunarflokkar og tegundir
- Úthlutunarlyklar
- Eignabækur

Nánari upplýsingar eru í [Uppsetning eigna](fa-setup.md).

## <a name="fixed-assets-analytics"></a>Greiningar á eignum

Í þessum hluta er lýst þeim greiningartólum sem hægt er að nota til að fá innsýn í gögn um eignir.

| Til... | Sjá |
| --- | --- |
| Fræðast um getu til að greina gögn um eignir. | [Yfirlit yfir greiningar á eignum](fa-analytics-overview.md) |
| Gera tilfallanda greiningu eignagagna beint á listasíðum og fyrirspurnum. | [Tilfallandi gagnagreining eigna](ad-hoc-analysis-fa.md) |
| Skoða innbyggðar skýrslur fyrir eignir. | [Innbyggðar eignaskýrslur](fa-reports.md) |
| Fylgjast með viðhaldskostnaði. | [Fylgjast með viðhaldskostnaði](fa-how-maintain.md#monitor-maintenance-costs)|
| Fylgjast með vátryggingasviði. | [Eftirlit með vátryggingasviði](fa-how-insure.md#to-monitor-insurance-coverage) |
| Skoða afskráningarbókarfærslur. | [Skoða afskráningarbókarfærslur](fa-how-dispose-retire.md#to-view-disposal-ledger-entries) |
| Skoða áætluð afskráningargildi. | [Skoða áætlað virði afskráninga](fa-how-manage-budgets.md#to-view-projected-disposal-values) |

## <a name="register-fixed-assets"></a>Skrá eignir

Setja verður upp spjald fyrir hverja eign með upplýsingum um þær. Til dæmis er hægt að setja byggingar eða framleiðslubúnað upp sem aðaleignir með íhlutalista. Hægt er að flokka eignir á ýmsa vegu, svo sem eftir flokki, deild eða staðsetningu. Síðan er hægt að eignast, viðhalda og selja eignirnar. Hægt er einnig að setja upp áætlaðar eignir. Með fjárhagsáætlun er hægt að taka með fyrirsjáanlega kaup og sölu í skýrslum.

| Til  | Sjá |
| --- | --- |
| Stjórna fjárhagsáætlana eigna, áætlun stofnkostnaðar, áætlun afskráninga eigna og áætlun afskrifta. |[Umsjón fjárhagsáætlana fyrir eignir](fa-how-manage-budgets.md) |
| Stofna eignir, úthluta afskriftaaðferðum, bóka eignakaup, hrakvirði og prenta eignalista. |[Komast yfir eignir](fa-how-acquire.md) |

## <a name="set-up-depreciations-for-your-fixed-assets"></a>Setja upp afskriftir fyrir eignir

Til að rekja eignaafskriftir og aðrar fjárhagslegar færslur fyrir eignir er sett upp ein eða fleiri afskriftabækur fyrir hverja þeirra. Nokkur þrep eru til að afskrifa eignir:

1. Keyra skýrslu sem reiknar tímabilsafskriftir.
1. Færslurnar sem leiða til eru færðar inn í færslubókina.
1. Bóka skal færslubókina.

[!INCLUDE[prod_short](includes/prod_short.md)] styður nokkrar afskriftaraðferðir. Nánari upplýsingar eru notaðar [með því að](fa-depreciation-methods.md) fara í Afskriftaaðferðir. Hægt er að setja upp margar afskriftabækur fyrir hverja eign í mismunandi tilgangi, svo sem eina fyrir skattskýrslugerð og aðra fyrir innri skýrslugerð.

| Til  | Sjá |
| --- | --- |
| Læra um mismunandi Aðferðir við afskriftir eigna |[Afskriftaaðferðir](fa-depreciation-methods.md) |
| Reikna afskriftir, bóka afskriftir og greina afskriftir í eignaskýrslum. |[Afskrifa eða greiða af eignum](fa-how-depreciate-amortize.md) |
| Skoða breytt virði afskriftabókar. | [Skoða breytt afskriftabókargildi](fa-how-trans-split-combine.md#to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification) |
| Skrá handvirkt eignafærslur á síðunni **Eignafjárhagsbók** eða á **síðunni Eignabók** eftir því hvort færslurnar eru fyrir fjárhagslega skýrslugerð eða fyrir innri stjórnun. | [Setja upp eignaafskriftir](fa-how-setup-depreciation.md) |

## <a name="fixed-assets-maintenance-and-insurance"></a>Eignaviðhald og tryggingar

Hægt er að skrá viðhaldskostnað og næstu þjónustudagsetningu fyrir hverja eign. Rakning viðhaldskostnaðar getur skipt máli vegna fjárhagsáætlunar og ákveðið hvort skipta skuli um eign. Hægt er að tengja hverja eign einum eða fleiri vátryggingarskilmálum og sannreyna að iðgjöld vegna iðgjalda séu samræmd verðmæti eignanna.

| Til  | Sjá |
| --- | --- |
| Skrá þjónustuheimsóknir, bókun viðhaldskostnaðar og fylgjast með viðhaldskostnaði. |[Umsjón eigna](fa-how-maintain.md) |
| Fylgjast með viðhaldskostnaði. | [Fylgjast með viðhaldskostnaði](fa-how-maintain.md#monitor-maintenance-costs)|
| Uppfæra vátryggingarupplýsingar, bóka stofnkostnað á vátryggingarskilmála, breyta vátryggingasviði, skoða vátryggingaupplýsingar og gera lista yfir vátryggingaskírteini. |[Tryggja eignir](fa-how-insure.md) |
| Fylgjast með vátryggingasviði. | [Eftirlit með vátryggingasviði](fa-how-insure.md#to-monitor-insurance-coverage) |

## <a name="reclassify-transfer-split-upcombine-adjust-value-write-down-and-dispose-fixed-assets"></a>Endurflokka, flytja, skipta upp/sameina, leiðrétta virði, niðurfærslu og afskrá eignir

| Til  | Sjá |
| --- | --- |
| Endurflokka eignir, flytja eignir á aðra staði, skipta upp eignum eða sameina þær. |[Flytja, skipta upp eða sameina eignir](fa-how-trans-split-combine.md) |
| Leiðrétta verð eigna, bóka afskriftir og bóka niðurfærslur. |[Endurmeta eignir](fa-how-revalue.md) |
| Bóka afskráningarfærslur, skoða afskráningarbókarfærslur og bóka afskráningar að hluta. |[Afskrá eða innkalla eignir](fa-how-dispose-retire.md) |
| Skoða afskráningarbókarfærslur. | [Skoða afskráningarbókarfærslur](fa-how-dispose-retire.md#to-view-disposal-ledger-entries) |
| Skoða áætluð afskráningargildi. | [Skoða áætlað virði afskráninga](fa-how-manage-budgets.md#to-view-projected-disposal-values) |

## <a name="tips-for-improving-your-fixed-asset-accounting"></a>Ábendingar um bætt eignabókhald

Nokkur atriði er hægt að innleiða í bókhaldsáætlun fyrir eignir sem geta hjálpað til við að tryggja það að hagnaður sé hámarks.

- Stofna þröskuld fyrir eignfærslu. Þegar vara er keypt er ákveðin föst upphæð fyrir eignfærslu. Upphæðin tryggir að bókhaldsbækurnar séu samræmdar og auðveldar gestum og teyminu að koma í stað villna í bókhaldinu.
- Endurmeta björgunartíma tækja. Mikilvægt er að áætla réttan tíma sem hægt er að nota eignirnar í upprunalegum tilgangi. Þar sem bókhald og afskriftir reiða sig á nákvæmar líftímaáætlanir skal endurmeta þegar þörf krefur vegna þess að það gæti breyst með tímanum.
- Merkið eignirnar. Nauðsynlegt er að rekja og merkja eignirnar allan lífstíl þeirra vegna þess að margir þættir geta haft áhrif á verðmæti þeirra. Tagging hjálpar til við að rekja vörurnar í gegnum þrepin í björgunarstarfi þeirra og koma í veg fyrir þjófnað, útrýma ýmsum atriðum og styðja við fjárhagslegar tölfræðilegar upplýsingar.
- Gera innsýn sjálfvirka með hugbúnaði fyrir eignabókhald. Með því að gera handvirkar aðgerðir sjálfvirkar til að rekja gögnin með hugbúnaði fyrir eignabókhald er auðveldara að ljúka því. Lykilorð vernd getur hjálpað til við að veita aðeins þeim sem þurfa á því að halda og eru þjálfaðir fyrir það.

## <a name="see-also"></a>Sjá einnig .

[Uppsetning eigna](fa-setup.md)  
[Yfirlit yfir greiningar á eignum](fa-analytics-overview.md)  
[Yfirlit yfir Fjármál](finance.md)  
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
