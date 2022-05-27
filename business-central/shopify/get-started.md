---
title: Hafist handa með tengibúnað fyrir Shopify
description: Fyrstu skrefin þegar tenging milli Viðskiptamiðseðla og Shopify
ms.date: 05/16/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
author: AndreiPanko
ms.author: andreipa
ms.openlocfilehash: 2b88995cad8cfe0c3688ca062643f2d339fed9bf
ms.sourcegitcommit: f071aef3660cc3202006e00f2f790faff849a240
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2022
ms.locfileid: "8768100"
---
# <a name="get-started-with-the-shopify-connector"></a>Byrjaðu með Shopify tengiflugi

[!INCLUDE [prod_short](../includes/prod_short.md)] gefur þér sveigjanleikann til að tengja verslunina þína Shopify (eða verslanir) við hana til að hámarka framleiðni fyrirtækisins þíns. Þú getur stjórnað og skoðað innsýn frá fyrirtæki þínu og Shopify vefversluninni sem eina einingu með því að Shopify nota tengitengið. Til að nota Shopify með [!INCLUDE [prod_short](../includes/prod_short.md)] þarf að fylgja nokkur skref. Þessi síða þjónar sem leiðarvísir til að ljúka samþættingu verslunar þinnar Shopify við [!INCLUDE [prod_short](../includes/prod_short.md)].

## <a name="prerequisites-for-shopify"></a>Forsendur fyrir Shopify

Heimilt verður að:

- Á Shopify reikning
- Í Shopify netverslun

Til að stofna nýjan Shopify reikning eða undirritað fyrir ókeypis 14 daga prufutíma, vafra til [Shopify](https://www.shopify.com/). Nánari upplýsingar um það hvernig eigi að stofna og sérsníða netverslun er að finna [Shopify í hjálparmiðstöðinni](https://help.shopify.com/).
  
- Aðrar sölurásir eru t.d. Shopify studdar sölurásum.

### <a name="recommended-settings"></a>Ráðleggingar um stillingar

- Afvirkja **sjálfvirkt** í **hlutanum**[**pöntunarvinnsla**](https://www.shopify.com/admin/settings/checkout) í útskráningarstillingum **Shopify í admin**.

Til að vita meira um Shopify stillingar fyrir kynningu og prufuáætlanir, sjá [próf-og þjálfunaráætlanir](/dynamics365/business-central/dev-itpro/administration/admin-shopify-connector#preparation).

## <a name="prerequisites-for-business-central"></a>Forsendur fyrir starfrækslu miðlægu

- Gakktu úr skugga um að **tenging til Shopify[!INCLUDE[prod_short](../includes/prod_short.md)]** Framlengingar sé uppsett.

Framlengingunni er foruppsett fyrir öll ný merki ups og rannsóknir. Ef setja þarf upp viðbætur af Markaðstaunum má heimsækja [skrárendingar og fjarlægja](../ui-extensions-install-uninstall.md#install) uppsetningu. Fylgdu skrefunum sem talin eru upp hér á eftir ef þú ert ekki með [!INCLUDE[prod_short](../includes/prod_short.md)].
<!--
## Installing the **Dynamics 365 Business Central** app to your Shopify online store

For existing [!INCLUDE[prod_short](../includes/prod_short.md)], this step is optional and can be skipped.

1. Locate the [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central) app on the [Shopify AppStore](https://apps.shopify.com/)
2. Choose the **Add App** button. Sign-in into your Shopify account if prompted. Select the required online shop if you've more than one.
3. After reviewing privacy and permissions, choose the **Install App** button.
  You can find and open the installed **Dynamics 365 Business Central** app in the **Apps** section on the sidebar of **Shopify admin**.
4. Choose **Sign up now** to start [!INCLUDE[prod_short](../includes/prod_short.md)] trial or **Sign in** if you already have [!INCLUDE[prod_short](../includes/prod_short.md)]. You'll be redirected to your [!INCLUDE[prod_short](../includes/prod_short.md)] at [Business Central](https://businesscentral.dynamics.com).
5. The next steps should be done in [!INCLUDE[prod_short](../includes/prod_short.md)].
-->
## <a name="connecting-business-central-to-the-shopify-online-store"></a>Tenging Viðskiptamiðlana við Shopify netverslunina

1. Farðu í Search ![ljósapera sem opnar aðgerðina Segðu mér.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Shopify búð** og veljið tengdan tengil.
2. Valið er aðgerðin **Nýtt**.  
3. **Í reitinn Kóti** er viðeigandi kóti færður inn.  
4. Í **Shopify svæðinu URL** skal slá inn vefslóð vefverslunar, sem þarf að tengjast.
5. Virkja **virkjunina** skipta, yfirfara og samþykkja skilmálana.
6. Ef beðið er, Skráðu þig inn í reikninginn þinn Shopify, farðu yfir persónuvernd og heimildir og veldu **síðan hnappinn setja upp App**.

Endurtakið skref 2-6 fyrir allar netverslanir sem þú vilt tengjast.

### <a name="next-steps"></a>Næstu skref

Nú er vefverslunin þín tengd [!INCLUDE[prod_short](../includes/prod_short.md)] /ur. Í næstu skrefum er skilgreint hvernig og hvað á að samstilla.

- [Samstilla vörur](synchronize-items.md)
- [Samstilla viðskiptavini](synchronize-customers.md)
- [Samstilla pantanir](synchronize-orders.md)

## <a name="see-also"></a>Sjá einnig

[Próf-og þjálfunaráætlanir](/dynamics365/business-central/dev-itpro/administration/admin-shopify-connector).

