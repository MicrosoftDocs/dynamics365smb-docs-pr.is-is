---
title: Yfirlit yfir uppsetningu og stjórnun prentara
description: Fræðast um hver mismunandi prentaratækifæri í Business Central
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
ms.topic: overview
ms.date: 09/28/2023
ms.custom: bap-template
---

# <a name="printer-setup-and-management-overview"></a>Yfirlit yfir uppsetningu og stjórnun prentara

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Að prenta skjöl og skýrslur úr [!INCLUDE[prod_short](includes/prod_short.md)] er mikilvægt verk fyrir fyrirtækjanotendur. Þú vilt gjarnan senda prentverk beint á einn af prenturum&mdash; fyrirtækisins sama [!INCLUDE[prod_short](includes/prod_short.md)] hvaða biðlara eða forrit þú ert að nota. Vegna þess að [!INCLUDE[prod_short](includes/prod_short.md)] á netinu er skýjaþjónusta getur það ekki náð beint til prentara á staðnum sem tengjast tækjum notendum, en það getur tengst við prentara í skýinu.

## <a name="what-are-your-printer-possibilities-in-business-central"></a>Hver eru prentaramöguleikar í Business Central?

Til að styðja við prentþarfirnar býður [!INCLUDE[prod_short](includes/prod_short.md)] upp á eftirfarandi eiginleika:

|Sérkenni|Description|Vefbiðlari| Fartækjaforrit|Forrit fyrir Teams|
|-------|-----------|----------|-----------|--------------|
|Skýjaprentun|Skýjaprentun er prentstjórnunarlausn sem er í boði sem skýjaþjónusta frá Microsoft. Með þessum eiginleika er hægt að setja upp prentara í skýjaprentun, síðan skrá þá til að nota í [!INCLUDE[prod_short](includes/prod_short.md)]. Þessi aðgerð krefst alhliða **prentunar áskriftar og altækrar samþættingar** viðbót við prentun.|![vinnur á netinu.](media/check.png)|![vinnur á netinu.](media/check.png)|![vinnur á netinu](media/check.png)|
|Tölvupóstprentun|Þessi eiginleiki gerir kleift að setja upp tölvupóstsprentara. [!INCLUDE[prod_short](includes/prod_short.md)] sendir þá prentverk til prentara með netfangi prentarans. Þessi eiginleiki krefst netfangaprentara og viðbótarinnar **Senda á tölvupóstsprentara**.|![vinnur á netinu.](media/check.png)|![vinnur á netinu](media/check.png)|![vinnur á netinu](media/check.png)|
|Prentun í vafra|Prentvirkni í vafra notandans sér um prentverk. Ef skýjaprentari er ekki uppsettur, eða ef uppsettur prentari mistekst, verða prentvalkostir vafrans sjálfgefið valdir. Reiturinn **Prentari** á síðu skýrslubeiðni sýnir *(Vafri sér um prentun)*.|![vinnur á netinu](media/check.png)|||

Megnið af vinnunni við uppsetningu prentara er hægt að vinna á síðunni **Prentarastjórnun**  [!INCLUDE[prod_short](includes/prod_short.md)]. Þó svo að með Universal Print prenturum gæti einnig þurft að vinna í Microsoft 365 stjórnunarmiðstöð eða Azure Portal.

> [!IMPORTANT]
> Fyrir Business Central innanhúss krefst alhliða prentunar og tölvupóstsprentunar að Microsoft Entra auðkenni eða NavUserPassword sannvottun sé notuð.

## <a name="custom-printer-extensions"></a>Sérsniðnar prentaraviðbætur

[!INCLUDE[prod_short](includes/prod_short.md)] styður aðrar sérstilltar prentaraviðbætur til að bæta við enn fleiri prenteiginleikum. Þannig að ef þú ert með einhverjar sérsniðnar prentaraviðbætur uppsettar getur forritið verið með prenteiginleika sem ekki er lýst í þessari grein.

Ef þú ert verktaki og vilt fræðast um hvernig á að búa til viðbætur við prentara er farið [í Þróun prentaraviðbóta í Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-reports-printing).

## <a name="next-steps"></a>Næstu skref

- [Setja upp alhliða prentara](admin-printer-setup-universal-print.md)  
- [Setja upp tölvupóstprentara](admin-printer-setup-email.md)  
- [Setja upp sjálfgefna prentara](ui-specify-printer-selection-reports.md)
