---
title: Um útreikning kostnaðarverðs
description: Kynntu þér hvernig kostnaðarútreikningur og aðrir þættir hafa áhrif á reit einingarkostnaðar í birgðaspjaldinu.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: article
ms.date: 04/19/2024
---
# <a name="about-unit-cost-calculation"></a>Um útreikning kostnaðarverðs

Hvert atriði er með einingarkostnað sem er reiknaður út samkvæmt kostnaðarútreikningi fyrirtækisins og öðrum þáttum. Sem regla, með kostnaðarútreikninginn *Staðlaður*, er gildið í reitnum **Einingarkostnaður** byggt á staðalkostnaði fyrir vöruna. Fyrir allar aðra kostnaðarútreikninga (*FIFO*, *LIFO*, *Tiltekinn* og *Meðaltal*) er einingarkostnaður reiknaður út samkvæmt meðalkostnaðarverði yfir tímabil.  

Frekari upplýsingar eru í [Stjórnun birgðakostnaðar](finance-manage-inventory-costs.md).  

## <a name="when-is-the-unit-cost-field-updated"></a>Hvenær er reitur einingarkostnaðar uppfærður?

Valinn kostnaðarútreikningur hefur áhrif á hvenær reiturinn **Einingarkostnaður** er uppfærður.

Þegar kostnaðarútreikningurinn er stilltur sem *Staðlaður* er reiturinn **Einingarkostnaður** uppfærður í hvert skipti sem staðalkostnaðinum er breytt og notendur geta ekki breytt reitnum **Einingarkostnaður**. Frekari upplýsingar er að finna í [Uppfærsla staðlaðs kostnaðarverðs](finance-how-to-update-standard-costs.md).

Ef kostnaðarútreikningurinn er *FIFO*, *LIFO*, *Tiltekinn* eða *Meðaltal* þá er **Einingarkostnaður** uppfærður í eftirfarandi tilfellum:

* Þegar kostnaður er leiðréttur fyrir vöru, sjálfkrafa eða með verkinu [Leiðrétta kostnað](inventory-how-adjust-item-costs.md#to-adjust-item-costs-manually).
* Við bókun innkaupareikninga, úttaks, eða jákvæða leiðréttingu ef eitt eftirfarandi skilyrða er satt:
  * Nettó reikningsfært magn vörunnar breytist úr neikvæðu eða núlli í jákvætt.
  * Núverandi einingakostnaður er núll.

Ef eitt af þessum skilyrðum á við, þá er reiturinn **Einingarkostnaður** uppfærður með gildinu í reitnum **Síðasti beini kostnaður** á birgðaspjaldinu.

> [!NOTE]
> Reiturinn **Einingarkostnaður** er ekki uppfærður ef núverandi einingarkostnaður er hærri en eða jafnt og núll og nýi einingarkostnaðurinn er núll. Litið er á einingarkostnað upp á núll sem undantekningu frá venjulegum viðskiptum. Því er núgildandi einingarkostnaður haldið eftir til að gefa upp síðasta þekkta viðeigandi gildi. Þessi undantekning á við jafnvel þótt birgðir hafi verið endurmetnar á núll.

Í reitnum **Einingarkostnaður** í birgðaspjaldinu er hægt að kafa niður til að skoða færslusöguna um hvernig meðalkostnaður eininga á lager er reiknaður út í glugganum **Yfirlit yfir útreikning á meðalkostnaði**.

## <a name="unit-cost-calculation-for-purchases"></a>Útreikningur kostnaðarverðs fyrir innkaup

Þegar vörur eru keyptar afritar kerfið alltaf gildið í reitnum **Síðasta innk.verð** á birgðaspjaldinu yfir í reitinn **Innk.verð** í innkaupalínu eða í línuna **Einingarkostnaður** í birgðabókarlínu.

Það sem valið er í reitnum **Aðferð kostnaðarútreiknings** hefur áhrif á hvernig [!INCLUDE[prod_short](includes/prod_short.md)] reiknar innihald reitarins **Einingarkostnaður** á línunum.

### <a name="costing-method-fifo-lifo-specific-or-average"></a>Aðferð kostn.útreiknings FIFO, LIFO, Innslegið eða Meðal

[!INCLUDE[prod_short](includes/prod_short.md)] reiknar út í reitinn **Einingarkostnaður SGM** í innkaupalínunni eða í reitinn **Einingarkostnaður** í birgðabókarlínunni eftir þessari reiknireglu:

*Kostn.verð (SGM) = (Beinn kostnaður – (Afsláttarupphæð / Magn)) x (1 + “Óbein kostnaðar % / 100) + Hlutf. sameiginl. Kostn*

### <a name="costing-method-standard"></a>Stöðluð aðferð kostn.útreiknings

Reiturinn **Kostn.verð (ISK)** á innkaupalínunni eða reiturinn **Kostnaðarverð** hefur verið fylltur út í birgðabókarlínunni með gildinu í reitnum **Kostnaðarverð** á birgðaspjaldinu. Þegar aðferð kostnaðarútreiknings er *Stöðluð* byggist þetta gildi alltaf á stöðluðum kostnaði.

Þegar innkaup eru bókuð þá notar [!INCLUDE[prod_short](includes/prod_short.md)] einingarkostnaðinn úr innkaupalínunni eða færslubókarlínunni yfir í reikningsfærslu innkaupavörunnar. Þú getur séð þetta á færslulistanum fyrir vöruna.

### <a name="all-costing-methods"></a>Allar aðferðir kostn.útreiknings

Kostnaðarverðið í upprunaskjalslínunni er notað til að reikna út efni reitsins **Kostnaðarupphæð raunveruleg** eða, ef við á reitinn **Kostnaðarupphæð (væntanleg)** sem tengist þessari birgðafærslu, sama hvaða kostnaðaraðferð er notuð á vöruna.

## <a name="unit-cost-calculation-for-sales"></a>Útreikningur kostnaðarverðs fyrir sölu

Þegar vörur eru seldar er kostnaðarverðið afritað úr reitnum **Einingarkostnaður** á birgðaspjaldinu yfir í sölulínu eða birgðabókarlínu.

Við bókun er kostnaðarverðið afritað yfir á birgðafærslu sölureiknings og má skoða það á færslulista vörunnar. [!INCLUDE[prod_short](includes/prod_short.md)] notar kostnaðarverðið í upprunaskjalslínunni til að reikna út efni reitsins **Kostnaðarupphæð (raunveruleg)** eða, ef við á **Kostnaðarupphæð (væntanleg)** reitinn í gildisfærslunni sem tengist þessar vörufærslu.

## <a name="see-also"></a>Sjá einnig .

[Birgðakostnaði stjórnað](finance-manage-inventory-costs.md)  
[Skráning á nýjum vörum](inventory-how-register-new-items.md)  
[Um birgðakostnað](finance-learn-about-costing.md)  
[Birgðir](inventory-manage-inventory.md)  
[Sala](sales-manage-sales.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Hönnunarupplýsingar: Ófrádráttarbærar bestu venjur VSK-uppsetningar](design-details-nondeductible-vat.md)
[: Aðferð kostnaðarútreiknings](setup-best-practices-costing-method.md)  
[Hönnunarupplýsingar: Aðferð kostnaðarútreiknings](design-details-costing-methods.md)  
[Hönnunarupplýsingar: kostnaðarleiðrétting](design-details-cost-adjustment.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
