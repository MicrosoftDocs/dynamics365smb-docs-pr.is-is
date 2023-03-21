---
title: Hafist handa með tengli fyrir Shopify
description: Fyrstu skrefin við að grunnstilla tengingu milli Business Central og Shopify
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
ms.search.form: '30100, 30101, 30102, 30103, 30104, 30135,'
author: AndreiPanko
ms.author: andreipa
---

# Hafist handa með Shopify tengli

Tengdu Shopify verslunina þína (eða verslanir) við [!INCLUDE [prod_short](../includes/prod_short.md)] og hámarkaðu afköst viðskiptanna. Stjórnaðu og skoðaðu innsýn í viðskiptin og Shopify verslunina þína í einni einingu.

Til að nota Shopify með [!INCLUDE [prod_short](../includes/prod_short.md)] þarft fyrst að gera nokkra hluti. Þessi grein þjónar hlutverki leiðsagnar til að samþætta Shopify verslun við [!INCLUDE [prod_short](../includes/prod_short.md)].

## Forkröfur fyrir Shopify

Þú verður að vera með:

- Á  Shopify  reikning
- Í  Shopify  netverslun

Nánari upplýsingar um það hvernig eigi að stofna  Shopify  rannsóknir og ráðlagðar stillingar eru í til að  [Stofna og setja upp  Shopify  lykil](shopify-account.md).

## Skilyrði fyrir Business Central

- Gakktu úr skugga um að forritið **[Shopify tengill](https://go.microsoft.com/fwlink/?linkid=2196238)** sé uppsett.

  Forritið er foruppsett fyrir allar nýskráningar og prufuáskriftir. Frekari upplýsingar um uppsetningu forrit úr AppSource eru í [Uppsetning og fjarlæging viðbóta](../ui-extensions-install-uninstall.md#install). Fylgdu skrefunum sem talin eru upp hér að neðan ef þú ert ekki [!INCLUDE[prod_short](../includes/prod_short.md)].

- Tryggja að notandi eigi nægar heimildir. Shopify Connector er heimild fyrir  *Shopify  tengivirkið – stjórnun (SHPFY – admin)*  sett. Frekari upplýsingar í  [Stofna notendur samkvæmt leyfum](../ui-how-users-permissions.md)  og  [úthluta heimildum til notenda og hópa](../ui-define-granular-permissions.md)


## Settu Dynamics 365 Business Central forritið upp í Shopify netverslunina þína

Fyrir núverandi [!INCLUDE[prod_short](../includes/prod_short.md)] er þetta skref valfrjálst og hægt er að sleppa því.

1. Finndu [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central) forritið í [Shopify AppStore](https://apps.shopify.com/)
2. Veldu hnappinn **Bæta við forriti**. Skráðu þig inn á Shopify reikninginn þinn ef beðið er um það. Veldu nauðsynlega netverslun ef þú ert með fleiri en eina.
3. Þegar búið er að fara yfir persónuvernd og heimildir skaltu velja hnappinn **Setja upp forrit**.

   Þú getur fundið og opnað uppsett **Dynamics 365 Business Central** forrit í hlutanum **Forrit** á hliðarstikunni á síðunni **Shopify stjórnandi**.
4. Veldu **Nýskrá núna** til að hefja [!INCLUDE[prod_short](../includes/prod_short.md)] prufuáskriftina eða **Skrá inn** ef þú ert þegar með [!INCLUDE[prod_short](../includes/prod_short.md)]. Þér verður beint á síðuna [Business Central](https://businesscentral.dynamics.com).
5. Næstu skref skal gera í [!INCLUDE[prod_short](../includes/prod_short.md)].

## Tengja Business Central við Shopify netverslunina

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, opna **Shopify Verslun** og veldu tengda tengilinn.
2. Valið er aðgerðin **Nýtt**.  
3. Í reitinn **Kóði** skal færa inn kóðann sem auðveldar þér að finna í [!INCLUDE[prod_short](../includes/prod_short.md)]. Til dæmis getur heiti endurspeglað það sem verslun selur, til dæmis „Húsgögn“ eða „Kaffi“, eða landið eða svæðið sem hún þjónustar.
4. Í reitinn **Shopify vefslóð** skal færa inn vefslóð netverslunar sem á að tengja. Notaðu eftirfarandi snið: `https://{shop}.myshopify.com/`.
5. Virkjaðu víxlhnappinn **Virkjað**, farðu yfir og samþykktu skilmálana.
6. Ef beðið er um það skaltu skrá þig inn á Shopify reikninginn þinn, fara yfir persónuverndarskilmálana og heimildirnar, síðan velja hnappinn **Setja upp forrit**.

Endurtaktu skref 2-6 fyrir allar netverslanir sem þú vilt tengjast.

### Þekkt vandamál

- Vafrinn lokar sprettiglugganum. Þegar búið er að  **Virkja virkjunina**  skipta kerfið opnast  **Biðin eftir svari-ekki loka þessari síðusíðu**  sem bíður eftir aðgangsákefð frá  Shopify, ef að síðan er lokað eða læst-ekki er hægt að  Shopify tengjast. Frekari upplýsingar er að finna í [Biðja um aðgangslykilinn](troubleshoot.md#request-the-access-token).
- [Oauth Villa invalid_request: Ekki tókst að finna  Shopify  API-forrit með api_key](troubleshoot.md#oauth-error-invalid_request-could-not-find-shopify-api-application-with-api_key)
- [Ekki hægt að tengja frá sandkassa](troubleshoot.md#verify-and-enable-permissions-to-make-http-requests-when-running-in-a-non-production-environment)


## Næstu skref

Nú er netverslunin þín tengd við [!INCLUDE[prod_short](../includes/prod_short.md)]. Í næstu skrefum skilgreinir þú hvernig og hvað á að samstilla.

- [Samstilla vörur](synchronize-items.md)
- [Samstilla viðskiptavini](synchronize-customers.md)
- [Samstilla pantanir](synchronize-orders.md)

## Sjá einnig .

[Walkthrough: Uppsetning og notkun  Shopify  tengibúnaðar](walkthrough-setting-up-and-using-shopify.md)  

