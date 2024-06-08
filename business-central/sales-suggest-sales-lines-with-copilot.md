---
title: Leggja til sölulínur með Afrita
description: Læra að leggja til línur í sölupöntunum með Copilot.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'Copilot, AI, sell'
ms.search.form: null
ms.date: 02/02/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
ms.collection: bap-ai-copilot
---

# Leggja til línur í söluskjölum með Copilot (forskoðun)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Þessi grein útskýrir hvernig á að stofna söluskjöl hraðar með því að láta Copilot stinga upp á vörunum til að bæta við línum í söluskjölum fyrir viðskiptamennina.

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## Um sölulínutillögur með Copilot

Sölulínutillaga með Copilot getur aðstoðað við stofnun lína í söluskjölum, svo sem sölutilboðum, pöntunum og reikningum sem byggjast á skipulögðu ílagi eða náttúrulegu tungumáli. Eiginleikinn er ekki almennt spjall, heldur mjög sértæk og samþætt reynsla sem hægt er að nota á söluskjölum. Þessi eiginleiki býður upp á tvær aðskildar hæfni sem hjálpa til við að finna gögn um einstakar vörur eða öll skjölin.

* Finna afurðir

  Upplýsingar sem lýsa vörum eru geymdar á mörgum stöðum [!INCLUDE [prod_short](includes/prod_short.md)]. Til dæmis eru vörunúmer og lýsingar geymd í töflunni Vara **, mörg strikamerki geymd í** töflunni Vörutilvísun **og eiginleikar framleiðslu eru geymdir í** töflunni Vörueigindir **.**  Þó að beðið sé um *rauð reiðhjól* gæti sjálf varan verið *Crimson tourer*, þar sem *Reiðhjól* er vöruflokkur og *rauður er eigind* .

* Finna skjöl eftir tilvísun

  Notandi endurtekur oft fyrri pöntun eða notar hana að minnsta kosti sem upphafspunkt. En það gæti verið erfiður að finna rétta pöntun í bunka af pöntunum. Sumt af pöntunarkenninu gæti munað, sem getur verið fyrirtækið sem úthlutaði númeri eða tilvísunarnúmeri frá viðskiptamanni. Ef hægt er að nota kvaðningar eins og *Þörf á síðasta reikningi frá apríl* ætti að hjálpa þér að finna pöntun hraðar.

## Frumskilyrði

* Sölulínutillaga með Copilot er virk og virkjuð af stjórnanda. Til að fá nánari upplýsingar um hvernig á að gera ÓH kleift að vera virkur er farið í [Grunnstilla copilot og AI-getu](enable-ai.md).
* Þú kannast við að búa til sölupantanir.

## Landfræðilegt til ráðstöfunar

Eftirfarandi tafla sýnir Microsoft Azure landsvæðin sem eiginleiki hans er tiltækur á.

|Umhverfis azure-svæði  |Azure OpenAI þjónusta landfræði   |Stjórna aðgerð sem þarf til að aflæsa Stjórnunaraðgerð  |
|---------|---------|---------|
|Þýskaland (Norður, Vestur-Miðborg)     | Svíþjóð eða Sviss        |  Já       |
|Noregur (Austur, Vestur)     | Svíþjóð eða Sviss        | Já     |
|Singapúr     |         |         |
|Suður-Afríka (Norður, Vestur)     |   Bandaríkin      |   Já      |
|Sviss (Norður, Vesturland)     |  Svíþjóð eða Sviss       |    Já     |
|Sameinuðu Arabísku Furstadæmin (Norður, Vestur)     |    Bandaríkin     |   Já     |
|Bandaríkin (Mið, Austur, Norður miðsvæðis, Suður miðsvæðis, Vestur)     |   Bandaríkin      |   Nr.      |
|Evrópa (Vestur, Norður)     |   Svíþjóð eða Sviss      |   Já      |
|Asía og Kyrrahaf     |         |         |
|Ástralía (Suður-Austur)     |   Bandaríkin      |    Já     |
|Suður-Ameríka     |         |         |
|Indland (Mið, Suður)     |    Bandaríkin     |   Já      |
|Japan (Austur, Vestur)     |    Bandaríkin     |    Já     |
|Frakkland (Mið, Suður)     |    Svíþjóð eða Sviss     |    Já     |
|Kórea (Mið, Suður)     |    Bandaríkin     |    Já     |

## Dæmi um kvaðningar

Tillögur um sölulínur með Afrita geta séð um margs konar inntak kvaðningar. Í þessum hluta eru nokkur dæmi um kvaðningar vegna ýmissa aðstæðna sem við höfum prófað.

### Dæmi um fyrirspurn til að endurtaka fyrra skjalið

Kvaðning: *Þarfnast allra vara af reikningi 103031*

### Í símtali við notanda er snöggur listi yfir nauðsynlegar vörur og magn, ekki alltaf nógu nákvæmur eða með því að nota innri vöruheiti

Prompt: *2 Rauður krakkar Biicycle*

Athuga skal að kvaðningin virkar, einnig með mörgum ábendingum.

### Notandi afritar fyrirspurn úr samskiptum á innleið og límir hana á síðuna Sölulínur tillagna

Prompt: *Halló, ég hef áhuga á að kaupa nokkra fylgihluti fyrir XXXX Fartölvuna mína, svo sem þráðlausa mús, lyklaborðskáp og fartölvupoka. Ég velti fyrir mér hvort þú hafir einhverjar tillögur um þessi atriði. Ertu með sértilboð eða afslátt af tryggum viðskiptamönnum eins og mér? Góðar kveðju, V*

Athuga skal að XXXX Fartölvu er ekki innifalin í leit.

## Leggja til línur í söluskjali

Þetta ferli lýsir því hvernig á að leggja til línur í sölupöntun. Skrefin eru hin sömu fyrir sölutilboð og reikninga.

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sölupöntun** og velja síðan viðkomandi tengil.
1. Sölupöntunin er opnuð.
1. Á flýtiflipanum **Línur** skal velja **Sækja línutillögur**.
1.  **Í glugganum Leggja til línur með afrita** er kvaðningin færð inn eða kvaðning valin.

## Skoða, vista, fleygja eða endurgera tillögur

Þegar Copilot hefur verið lagt til að vörunum verði bætt við línur, tillögur hennar skoðaðar og ákveðið hvort þær eru það sem óskað er eftir:

* Til að fleygja einni línu sem lögð er til skal velja hana á listanum og velja svo aðgerðina **Eyða línu** .
* Til að fleygja öllum línum sem lagt er til og loka glugganum Afritalot skal velja hnappinn Henda (ruslpóst) við hliðina á hnappnum **Halda honum** .
* Til að millifæra línurnar sem birtast í glugganum Afrita skal velja **Halda honum**. 

Það er **áreiðanleikareitur** sem birtir **Hár (80+)**, **Miðlungs (60-80)** og **Lítill (60-)** stig og punktar í línur sem þarfnast athygli.

Þetta skref staðfestir að flytja eigi línurnar í söluskjal. Einnig er hægt að eyða eða breyta fluttu línunum þar eða eyða öllu skjalinu.

## Sjá einnig .

[Algengar spurningar fyrir sölulínutillögur með Copilot](faq-sales-suggest-sales-lines-with-copilot.md)
[Samskipa copilot og AI-getu](enable-ai.md)
