---
title: Setja upp tölvupóstprentara
description: Hvernig á að lýsingu
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 01/26/2023
ms.custom: bap-template
---
# <a name="set-up-email-printers"></a>Setja upp tölvupóstprentara

Þessi grein útskýrir hvernig setja á upp prentara með tölvupósti með tölvupósti [!INCLUDE[prod_short](includes/prod_short.md)]. Með þessum prenturum, [!INCLUDE[prod_short](includes/prod_short.md)]  sendir prentverk til prentarans með netfangi prentarans.

> [!TIP]
> Til að [fá upplýsingar um aðra prentaramöguleika er farið í Yfirlit prentarastjórnunar](admin-printer-setup-overview.md). 

## <a name="prerequisites"></a>Frumskilyrði

- [!INCLUDE[prod_short](includes/prod_short.md)]2020 útgáfutímabil 1 eða nýrra
- Viðbótin **Senda á tölvupóstsprentara** er uppsett

    Þessi viðbót er uppsett sjálfgefið Fræðast meira um uppsetningu viðbóta við [uppsetningu og fjarlægingu viðbóta í Business Central](ui-extensions-install-uninstall.md).
- Tölvupóstvirkni er sett upp.

   Frekari upplýsingar eru á [Setja upp tölvupóst](admin-how-setup-email.md).

## <a name="add-an-email-printer"></a>Bæta við tölvupóstprentara

Síðan **Prentarastjórnun** sýnir þér prentarana sem eru settir upp. Síðan veitir þér einnig aðgang að síðunni **Stillingar** fyrir hvern prentara fyrir sig til að breyta núverandi uppsetningu eða til að setja upp nýjan prentara.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Prentarastjórnun** og velja síðan viðkomandi tengil.
2. Veldu **Tölvupóstprentun** og veldu síðan **Bæta við tölvupóstprentara**.
3. Á síðunni **Stillingar tölvupóstsprentara** skal fylla út reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > Velja verður viðeigandi pappírsstærð handvirkt fyrir prentara þar sem enginn staðbundinn prentari eða notandastillingar geta verið geymdir.
    >
    > Hafa skal í huga að póstprentaraviðbótin er sjálfgefin **á A4** pappírsstærð sem hentar ekki í Norður-Ameríku, til dæmis.

## <a name="privacy-notice"></a>Tilkynning um persónuvernd

Ef viðbót tölvupóstsprentara er notuð eru öll eða sum prentverk send á netfangið sem er skilgreint fyrir prentarann. Við mælum eindregið með því að einkvæmt tölvupóstskenni sé tengt við prenttæki með því að nota aðeins opinbera þjónustu sem framleiðandi vélbúnaðar veitir, svo sem HP ePrint, KonicaMinolta EveryonePrint eða Epson Email Print.

Nauðsynlegt er að gera allar nauðsynlegar persónuverndarráðstafanir, þar á meðal að tryggja að prentlausnin fyrir tölvupóst hafi rétt skilgreindar heimildir, persónuverndarstillingar og varðveislureglur. Það er á ábyrgð notanda að gefa upp rétt, staðfest og starfhæft netfang. Frekari upplýsingar má finna á [Yfirlýsing Microsoft um persónuvernd](https://privacy.microsoft.com/privacystatement).

## <a name="next-steps"></a>Næstu skref

[Setja upp sjálfgefna prentara](ui-specify-printer-selection-reports.md)

## <a name="see-also"></a>Sjá einnig .

[Yfirlit yfir prentarastjórnun](admin-printer-setup-overview.md)  
[Uppsetning alhliða prentara](admin-printer-setup-universal-print.md)
[prentunar með skýrslu](ui-work-report.md#PrintReport)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Keyra runuvinnslur](ui-how-run-batch-jobs.md)  
