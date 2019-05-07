---
title: Skoðun á Síðum í Business Central
description: Notið eiginleika fyrir eftirlit með síðu til að skoða sérstaklega upplýsingar um síðuhönnun og gagnaveitu. Síðuskoðun hentar vel við úrræðaleit á vandamálum varðandi gögnin þín.
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: dynamics365-business-central
author: jswymer
ms.date: 04/01/2019
ms.openlocfilehash: eb9d4ec76c0dbbd59763f7622ca51137c9563a91
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/16/2019
ms.locfileid: "969879"
---
# <a name="inspecting-pages-in-business-central"></a>Skoðun á Síðum í Business Central

Eiginleiki fyrir eftirlit með síðu gerir þér kleift að ná í upplýsingar um síðu, veitir innsýn inn í síðuhönnun, mismunandi þætti sem síðan samanstendur af og uppruna gagnanna sem eru sýnd. Eftirlit með síðu er sérstaklega hönnuð fyrir stjórnendur, kraftnotendur, starfsfólk notendaþjónustu og þróunaraðila. Hún er tilvalin í að fræðast um gagnalíkanið á bak við síðu og úrræðaleit. Ef þú átt til að mynda í vandræðum með síðu er hægt að nota eftirlit með síðu til að fá upplýsingar sem eru sendar áfram til kerfisstjórans eða starfsfólk notendaþjónustu.

## <a name="working-with-page-inspection"></a>Vinna með síðueftirlit

Til að skoða síðu skal velja ![Stillingartákn](media/ui-experience/settings_icon_small.png) efst í hægra horninu, síðan velja **Skoða**. Eða hægt er að nota flýtileiðina **Ctrl+Alt+F1**.

Rúðan **Eftirlit með síðu** opnast á hliðinni. Eftirfarandi skýringarmynd sýnir rúðuna **Eftirlit með síðu** á síðunni **Sölupöntun**.

![Eftirlit með síðu](media/page-inspection-example.png)

Þegar rúðan **Eftirlit með síðu** opnast fyrst, sýnir hún upplýsingar sem á við um hlut aðalsíðunnar.

Notaðu lyklaborðið eða benditækið til að færa fókusinn á aðrar einingar á síðunni. Þegar Upplýsingakassi er valinn eða hluti á aðalsíðunni verður afmarkaða svæðið auðkennt með ramma og rúðan **Eftirlit með síðu** birtir upplýsingar um valda einingu. Til dæmis sýnir skýringarmyndin hér á undan upplýsingar um listahlutann á síðunni **Sölupöntun**. Þar sem þú ferð yfir á aðrar síður í forritinu mun rúðan **Eftirlit með síðu** uppfærast sjálfkrafa með síðuupplýsingum um leið og þú ferð á milli.

Frekari upplýsingar um hvað er sýnt í síðueftirliti er að finna í [Síður eftirlits og úrræðaleitar](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-inspecting-pages) í hjálpinni fyrir Business Central Developer og IT Pro.

Ef upplýsingarnar sjást ekki sem þú býst við að sjá í rúðunni **Eftirlit með síðu** ertu líklega ekki með nauðsynlegar heimildir eins og er lýst í næsta hluta.

## <a name="controlling-access-to-page-inspection-details"></a>Upplýsingar um stjórnun á aðgangi að síðueftirliti

Sem stjórnandi er hægt að stýra aðgangi að ítarlegum upplýsingum sem eru sýndar í rúðunni **Eftirlit með síðu** með því að stilla heimildir sem notendur eru með. Til að veita aðgangsheimild notanda að ítarlegum upplýsingum skal gefa notendum heimildina **Keyra** í **Kerfis** hlutanum **5330**. Hægt er að veita þessa heimild með því að nota heimildasamstæðu (t.d. **D365 úrræðaleit**) eða notendaflokk (t.d. **D365 úrræðaleit**). Frekari upplýsingar um heimildir er að finna í [Stjórnun notenda og heimilda](ui-how-users-permissions.md).

Notendur sem fá heimildir í **Kerfishlutur 5330** geta enn opnað rúðuna **Eftirlit með síðu**, en þeir munu aðeins sjá reitina **Síða** og **Tafla** sem birta grunnupplýsingar sem hægt er að senda áfram til þjónustudeildar.

## <a name="see-also"></a>Sjá einnig

[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
