---
title: Yfirlit yfir uppsetningar og stjórnun prentara
description: Lærðu hvað mismundandi prentarar möguleikar í viðskiptum miðsvæðis
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
ms.topic: overview
ms.date: 09/28/2023
ms.custom: bap-template
---

# Yfirlit yfir uppsetningar og stjórnun prentara

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Að prenta skjöl og skýrslur úr [!INCLUDE[prod_short](includes/prod_short.md)] er mikilvægt verk fyrir fyrirtækjanotendur. Vanalega er ætlunin að senda prentverk beint á prentara &mdash; [!INCLUDE[prod_short](includes/prod_short.md)]  fyrirtækisins, sama biðlara eða forritsins sem verið er að nota. Vegna þess að [!INCLUDE[prod_short](includes/prod_short.md)] á netinu er skýjaþjónusta getur það ekki náð beint til prentara á staðnum sem tengjast tækjum notendum, en það getur tengst við prentara í skýinu.

## Hverjir eru prentarar möguleikar þínir í Viðskiptamiðinu?

Til að styðja við prentþarfirnar býður [!INCLUDE[prod_short](includes/prod_short.md)] upp á eftirfarandi eiginleika:

|Sérkenni|Description|Vefbiðlari| Fartækjaforrit|Forrit fyrir Teams|
|-------|-----------|----------|-----------|--------------|
|Skýjaprentun|Skýjaprentun er prentstjórnunarlausn sem er í boði sem skýjaþjónusta frá Microsoft. Með þessum eiginleika er hægt að setja upp prentara í skýjaprentun, síðan skrá þá til að nota í [!INCLUDE[prod_short](includes/prod_short.md)]. Þessi eiginleiki krefst alhliða prentáskriftar og Framlengingar á  **Universal PRINT-samþættingaráskrift** .|![vinnur á netinu.](media/check.png)|![vinnur á netinu.](media/check.png)|![vinnur á netinu](media/check.png)|
|Tölvupóstprentun|Þessi eiginleiki gerir kleift að setja upp tölvupóstsprentara. [!INCLUDE[prod_short](includes/prod_short.md)] sendir þá prentverk til prentara með netfangi prentarans. Þessi eiginleiki krefst netfangaprentara og viðbótarinnar **Senda á tölvupóstsprentara**.|![vinnur á netinu.](media/check.png)|![vinnur á netinu](media/check.png)|![vinnur á netinu](media/check.png)|
|Prentun í vafra|Prentvirkni í vafra notandans sér um prentverk. Ef skýjaprentari er ekki uppsettur, eða ef uppsettur prentari mistekst, verða prentvalkostir vafrans sjálfgefið valdir. Reiturinn **Prentari** á síðu skýrslubeiðni sýnir *(Vafri sér um prentun)*.|![vinnur á netinu](media/check.png)|||

Flest verk fyrir uppsetningu prentara er hægt að gera  **á síðunni prentarastjórnun**  í [!INCLUDE[prod_short](includes/prod_short.md)]. Þó svo að með Universal PRINT prenturum gætir þú einnig þurft að vinna í  Microsoft 365  admin Center eða Azure gáttinni.

> [!IMPORTANT]
> Til að nota innanhúss, Universal PRINT og prentun tölvupósts þurfa þessi auðkenni eða NavUserPassword sannvottun að  Microsoft Entra  vera notuð.

## Sérsniðinn Viðaukar prentara

[!INCLUDE[prod_short](includes/prod_short.md)] styður aðrar sérstilltar prentaraviðbætur til að bæta við enn fleiri prenteiginleikum. Þannig að ef þú ert með einhverjar sérsniðnar prentaraviðbætur uppsettar getur forritið verið með prenteiginleika sem ekki er lýst í þessari grein.

Ef þú ert AL-verktaki og vilt fræðast um hvernig prentaraviðbætur eru stofnaðar skaltu fara að  [þróa prentaraviðbætur í Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-reports-printing).

## Næstu skref

- [Setja upp Universal PRINT prentarar](admin-printer-setup-universal-print.md)  
- [Setja upp email prentara](admin-printer-setup-email.md)  
- [Uppsetning sjálfgefinna prentara](ui-specify-printer-selection-reports.md)