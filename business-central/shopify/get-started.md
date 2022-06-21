---
title: Hafist handa með tengibúnað fyrir Shopify
description: Fyrstu skrefin þegar tenging milli Viðskiptamiðseðla og Shopify
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
author: AndreiPanko
ms.author: andreipa
ms.openlocfilehash: 64fae9efdda832f14593564b9a19101d120c9712
ms.sourcegitcommit: fb43bc843be4ea9c0c674a14945df727974d9bb9
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/27/2022
ms.locfileid: "8808934"
---
# <a name="get-started-with-the-shopify-connector"></a>Byrjaðu með Shopify tengiflugi

Tengdu þína Shopify verslun (eða verslanir) við [!INCLUDE [prod_short](../includes/prod_short.md)] og hámarkar framleiðni fyrirtækisins. Stjórnaðu og Skoðaðu innsýn frá þínu fyrirtæki og þinni Shopify verslun sem eina einingu. 

Í Shopify tengivirkinu felst eftirfarandi hæfileiki:

- Aðstaða fyrir fleiri en eina Shopify búð  

  - Hver búð hefur sitt skipulag, þar á meðal safn vara, birgðageymslur sem eru notaðar til að reikna út birgðir og verðlista.  
- Samkeyrsla á bi-stefnumarkandi atriðum eða afurðum  

  - Í Connector eru samkeyrðar myndir, vöruafbrigði, strikamerki, vörunúmer lánardrottins, lengdir textar og seðlar.  
  - Flytja út eigindi vöru í Shopify.  
  - Nota valda verðflokka viðskiptamanna og afslætti til að skilgreina verð sem fluttur er út í Shopify.  
  - Ákveða hvort vörur megi stofna sjálfvirkt eða leyfa ekki uppfærslur á fyrirliggjandi afurðum.  
- Samstilling birgðastita  

  - Velja skal nokkra eða alla tiltæka staði í [!INCLUDE [prod_short](../includes/prod_short.md)].  
  - Uppfæra birgðastig á mörgum stöðum í Shopify.  
- Bi-stefnumiðuð samstilling viðskiptavina  

  - Snjallkort viðskiptavina með síma og tölvupósti.  
  - Nota skal landssniðmát þegar Viðskiptavinir eru stofnaðir, sem hjálpar til að tryggja að skattastillingar séu réttar.  
- Innflutningur á pöntunum frá Shopify  

  - Við innflutninginn er hægt að stofna viðskiptamenn sjálfkrafa í [!INCLUDE [prod_short](../includes/prod_short.md)] eða ákveða að stjórna viðskiptavinunum í Shopify.  
  - Taka með pantanir sem Shopify stofnaðar eru á öðrum leiðum, til dæmis POS eða Amazon.  
  - Sendingarkostnaður, gjafakort, ábendingar, siglinga-og greiðsluaðferðir, tilfærslur og hætta á svikum.  
  - Fá upplýsingar um útborgun úr Shopify greiðslum.  
- Auðveldar mælingar á uppfyllingu upplýsinga  

  - Valfrjálst er að skrifa vörurakningarupplýsingar frá [!INCLUDE [prod_short](../includes/prod_short.md)] í Shopify.  

Til að nota Shopify með [!INCLUDE [prod_short](../includes/prod_short.md)] hefur þú nokkra hluti til að gera fyrst. Þessi grein þjónar sem leiðarvísir til að ljúka samþættingu verslunar þinnar Shopify við [!INCLUDE [prod_short](../includes/prod_short.md)].

## <a name="prerequisites-for-shopify"></a>Forsendur fyrir Shopify

Heimilt verður að:

- Á Shopify reikning
- Í Shopify netverslun

Til að stofna nýjan Shopify reikning eða undirritað fyrir ókeypis 14 daga prufutíma, vafra til [Shopify](https://www.shopify.com/). Nánari upplýsingar um það hvernig eigi að stofna og sérsníða netverslun er að finna [Shopify í hjálparmiðstöðinni](https://help.shopify.com/).
  
Aðrar sölurásir eru t.d. Shopify studdar sölurásum.

### <a name="recommended-settings"></a>Ráðleggingar um stillingar

- Afvirkja **sjálfvirkt** í **hlutanum**[**pöntunarvinnsla**](https://www.shopify.com/admin/settings/checkout) í útskráningarstillingum **Shopify í admin**.

Til að vita meira um Shopify stillingar fyrir kynningu og prufuáætlanir, sjá [próf-og þjálfunaráætlanir](/dynamics365/business-central/dev-itpro/administration/admin-shopify-connector#preparation).

## <a name="prerequisites-for-business-central"></a>Forsendur fyrir starfrækslu miðlægu

- Gakktu úr skugga um að **[Shopify forritið tengi](https://go.microsoft.com/fwlink/?linkid=2196238)** uppsett.

Forritið er fyrirfram uppsett fyrir allar nýjar skrápur og rannsóknir. Frekari upplýsingar um uppsetningu á apps er sett upp af Markaðstaunum við uppsetningu og uppsetningu [á](../ui-extensions-install-uninstall.md#install) Óskránum. Fylgdu skrefunum sem talin eru upp hér á eftir ef þú ert ekki með [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="installing-the-dynamics-365-business-central-app-to-your-shopify-online-store"></a>**Dynamics 365 Business Central** Uppsetning á forritinu í Shopify netverslun

Fyrir fyrirliggjandi [!INCLUDE[prod_short](../includes/prod_short.md)] er þetta þrep valfrjálst og því má sleppa.

1. [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central) Finndu App [Shopify í AppStore](https://apps.shopify.com/)
2. **Veldu hnappinn Bæta við forriti**. Skráðu þig inn á reikninginn þinn Shopify ef beðið er um. Veldu nauðsynlega vefbúð ef þú ert með fleiri en einn.
3. Eftir að **hafa áfrýjað persónuvernd og heimildum skal velja hnappinn setja upp App**.
  Hægt er að finna og opna uppsett **Dynamics 365 Business Central** App í **apps** -hlutanum á hliðarstikunni **Shopify admin**.
4. Veldu **skrá núna** til að byrja [!INCLUDE[prod_short](../includes/prod_short.md)] að prufa eða **skrá þig inn** ef þú ert þegar með [!INCLUDE[prod_short](../includes/prod_short.md)]. Þú munt framvísa þér á [!INCLUDE[prod_short](../includes/prod_short.md)] Viðskiptamiðinu. [...](https://businesscentral.dynamics.com)
5. Næstu skref ættu að vera höfð í [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="connecting-business-central-to-the-shopify-online-store"></a>Tenging Viðskiptamiðlana við Shopify netverslunina

1. Farðu í Search ![ljósapera sem opnar aðgerðina Segðu mér.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **Shopify búð** og veljið tengdan tengil.
2. Valið er aðgerðin **Nýtt**.  
3. **Í reitinn Kóti** er viðeigandi kóti færður inn.  
4. Í **Shopify svæðinu URL** skal slá inn vefslóð vefverslunar, sem þarf að tengjast. Notaðu eftirfarandi snið:`https://{shop}.myshopify.com/`.
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

