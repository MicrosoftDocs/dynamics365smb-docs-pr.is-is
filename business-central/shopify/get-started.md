---
title: Hafist handa með tengibúnað fyrir Shopify
description: Fyrstu skrefin þegar tenging milli Viðskiptamiðseðla og Shopify
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
ms.search.form: 30100, 30101, 30102, 30103, 30104, 30135,
author: AndreiPanko
ms.author: andreipa
ms.openlocfilehash: b79691660ca84309057c3abab3d3a3df47271f58
ms.sourcegitcommit: 5bb13966e9ba8d7a3c2f00dd32f167acccf90b82
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728411"
---
# <a name="get-started-with-the-shopify-connector"></a>Byrjaðu með Shopify tengiflugi

Tengdu þína Shopify verslun (eða verslanir) við [!INCLUDE [prod_short](../includes/prod_short.md)] og hámarkar framleiðni fyrirtækisins. Stjórnaðu og Skoðaðu innsýn frá þínu fyrirtæki og þinni Shopify verslun sem eina einingu.

Í Shopify tengivirkinu felst eftirfarandi hæfileiki:

- Aðstaða fyrir fleiri en eina Shopify búð.
  - Hver búð hefur sitt skipulag, þar á meðal safn vara, birgðageymslur sem eru notaðar til að reikna út birgðir og verðlista.  
- Bi-stefnumarkandi samstillingu á vörum eða vörum.
  - Í Connector eru samkeyrðar myndir, vöruafbrigði, strikamerki, vörunúmer lánardrottins, lengdir textar og seðlar.  
  - Flytja út eigindi vöru í Shopify.  
  - Nota valda verðflokka viðskiptamanna og afslætti til að skilgreina verð sem fluttur er út í Shopify.  
  - Ákveða hvort vörur megi stofna sjálfvirkt eða leyfa ekki uppfærslur á fyrirliggjandi afurðum.  
- Samstilling birgðastita.
  - Velja skal nokkra eða alla tiltæka staði í [!INCLUDE [prod_short](../includes/prod_short.md)].  
  - Uppfæra birgðastig á mörgum stöðum í Shopify.  
- Bi-stefnumarkandi samstillingu viðskiptavina.
  - Snjallkort viðskiptavina með síma og tölvupósti.  
  - Nota skal landssniðmát þegar Viðskiptavinir eru stofnaðir, sem hjálpar til að tryggja að skattastillingar séu réttar.  
- Innflutningur pantana frá Shopify.
  - Við innflutninginn er hægt að stofna viðskiptamenn sjálfkrafa í [!INCLUDE [prod_short](../includes/prod_short.md)] eða ákveða að stjórna viðskiptavinunum í Shopify.  
  - Taka með pantanir sem Shopify stofnaðar eru á öðrum leiðum, til dæmis POS eða Amazon.  
  - Sendingarkostnaður, gjafakort, ábendingar, siglinga-og greiðsluaðferðir, tilfærslur og hætta á svikum.  
  - Fá upplýsingar um útborgun úr Shopify greiðslum.  
- Rekja upplýsingar um uppfyllingu.
  - Að öðrum kosti er valið að flytja vörurakningarupplýsingar úr [!INCLUDE [prod_short](../includes/prod_short.md)] í Shopify.  

Til að nota Shopify með [!INCLUDE [prod_short](../includes/prod_short.md)] þarf að gera nokkra hluti fyrst. Þessi grein þjónar sem leiðarvísir til að samþætta Shopify verslunina við [!INCLUDE [prod_short](../includes/prod_short.md)].

## <a name="prerequisites-for-shopify"></a>Forsendur fyrir Shopify

Heimilt verður að:

- Sér Shopify reikning.
- Shopify Netverslun.

Til að búa til nýjan Shopify lykil eða skilti fyrir ókeypis 14 daga prufutíma, Farðu til [Shopify . com](https://www.shopify.com/). Frekari upplýsingar um hvernig á að stofna og sérsníða netverslun á [Shopify Hjálparstöð](https://help.shopify.com/).
  
Aðrar sölurásir eru t.d. Shopify studdar sölurásum.

### <a name="recommended-settings"></a>Ráðleggingar um stillingar

- Afvirkja **sjálfvirkt** í **hlutanum**[**pöntunarvinnsla**](https://www.shopify.com/admin/settings/checkout) í útskráningarstillingum **Shopify í admin**.

Frekari upplýsingar um Shopify stillingar fyrir kynningu og prófaðstæður við [próf og þjálfunaráætlanir](/dynamics365/business-central/dev-itpro/administration/admin-shopify-connector#preparation).

## <a name="prerequisites-for-business-central"></a>Forsendur fyrir starfrækslu miðlægu

- Gakktu úr skugga um að **[Shopify forritið tengi](https://go.microsoft.com/fwlink/?linkid=2196238)** uppsett.

Forritið er fyrirfram uppsett fyrir allar nýjar skrápur og rannsóknir. Frekari upplýsingar um uppsetningu á forritum frá AppSource at [Setja upp og fjarlægja viðauka](../ui-extensions-install-uninstall.md#install). Fylgdu skrefunum sem talin eru upp hér á eftir ef þú ert ekki með [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="install-the-dynamics-365-business-central-app-to-your-shopify-online-store"></a>Dynamics 365 Business Central Settu upp App í netverslunina þína Shopify

Fyrir fyrirliggjandi [!INCLUDE[prod_short](../includes/prod_short.md)] er þetta þrep valfrjálst og því má sleppa.

1. [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central) Finndu App [Shopify í AppStore](https://apps.shopify.com/)
2. **Veldu hnappinn Bæta við forriti**. Skráðu þig inn á reikninginn þinn Shopify ef beðið er um. Veldu nauðsynlega vefbúð ef þú ert með fleiri en einn.
3. Eftir að **hafa áfrýjað persónuvernd og heimildum skal velja hnappinn setja upp App**.

   Þú getur fundið og opnað uppsett **Dynamics 365 Business Central** App í **apps** appinu á hliðarstikunni á **Shopify admin** síðunni.
4. Veldu **skrá núna** til að byrja að [!INCLUDE[prod_short](../includes/prod_short.md)] prufa eða **skrá þig inn** ef þú ert þegar með [!INCLUDE[prod_short](../includes/prod_short.md)]. Þú munt vera framseldur á [aðalsíðu](https://businesscentral.dynamics.com) fyrirtækisins.
5. Næstu skref ættu að vera höfð í [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="connect-business-central-to-the-shopify-online-store"></a>Tengja Viðskiptamiðað Shopify við vefverslunina

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Shopify búð** og veljið tengdan tengil.
2. Valið er aðgerðin **Nýtt**.  
3. **Í reitnum kóti** er færður inn kótinn sem auðveldar að finna [!INCLUDE[prod_short](../includes/prod_short.md)] inn. Til dæmis gæti nafn endurspeglað það sem búð selur, t.d. "húsgögn" eða "kaffi", eða það land eða svæði sem það þjónar.
4. **Shopify Í reitinn URL** er FÆRÐ inn vefslóð vefverslunar sem þarf að tengjast. Notaðu eftirfarandi snið:`https://{shop}.myshopify.com/`.
5. **Virkjaðu virkjunina** skipta, yfirfara og samþykkja skilmálana.
6. Ef beðið er, Skráðu þig inn á reikninginn þinn Shopify, Skoðaðu persónuverndarskilmálana og heimildina, þá skaltu velja **hnappinn setja upp App**.

Endurtakið skref 2-6 fyrir allar netverslanir sem þú vilt tengjast.

> [!NOTE]
> Gakktu úr skugga um að vafrinn blokki ekki pop-up gluggum. Þegar búið er að **Virkja virkjunina** skipta kerfið opnast **Biðin eftir svari-ekki loka þessari síðusíðu** sem bíður eftir aðgangsákefð frá Shopify, ef að síðan er lokað eða læst-ekki er hægt að Shopify tengjast. Frekari upplýsingar er að biðja um [aðgangssáfan](troubleshoot.md#request-the-access-token)

### <a name="next-steps"></a>Næstu skref

Nú er vefverslunin þín tengd [!INCLUDE[prod_short](../includes/prod_short.md)] /ur. Í næstu skrefum er skilgreint hvernig og hvað á að samstilla.

- [Samstilla vörur](synchronize-items.md)
- [Samstilla viðskiptavini](synchronize-customers.md)
- [Samstilla pantanir](synchronize-orders.md)

## <a name="see-also"></a>Sjá einnig .

[Próf-og þjálfunaráætlanir](/dynamics365/business-central/dev-itpro/administration/admin-shopify-connector).
