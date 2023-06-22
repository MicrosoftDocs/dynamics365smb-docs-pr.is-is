---
title: Hafist handa með tengli fyrir Shopify
description: Fyrstu skrefin við að grunnstilla tengingu milli Business Central og Shopify
ms.date: 03/27/2023
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
ms.search.form: '30100, 30101, 30102, 30103, 30104, 30135,'
author: AndreiPanko
ms.author: andreipa
---

# Hafist handa með Shopify tengli

Tengdu Shopify verslunina þína (eða verslanir) við [!INCLUDE [prod_short](../includes/prod_short.md)] og hámarkaðu afköst viðskiptanna. Stjórnaðu og skoðaðu innsýn í viðskiptin og Shopify verslunina þína í einni einingu.

Til að nota  Shopify  með  [!INCLUDE [prod_short](../includes/prod_short.md)] eru nokkur atriði sem þú átt að gera fyrst. Þessi grein þjónar hlutverki leiðsagnar til að samþætta Shopify verslun við [!INCLUDE [prod_short](../includes/prod_short.md)].

## Forkröfur fyrir Shopify

Þú verður að vera með:

- Á  Shopify  reikning
- Í  Shopify  netverslun

Til að fræðast nánar um hvernig á að búa  Shopify  til tríggjar og þær stillingar sem mælt er fyrir er farið í að  [Stofna og setja upp  Shopify  lykil](shopify-account.md).

## Skilyrði fyrir Business Central

- Gakktu úr skugga um að forritið **[Shopify tengill](https://go.microsoft.com/fwlink/?linkid=2196238)** sé uppsett.

  Forritið er foruppsett fyrir allar nýskráningar og prufuáskriftir. Frekari upplýsingar um uppsetningu forrit úr AppSource eru í [Uppsetning og fjarlæging viðbóta](../ui-extensions-install-uninstall.md#install). Fylgdu skrefunum sem talin eru upp hér að neðan ef þú ert ekki [!INCLUDE[prod_short](../includes/prod_short.md)].

- Gætið þess að notandinn hafi réttar heimildir. Shopify Connector er heimild fyrir  **Shopify  tengivirkið – stjórnun (SHPFY – admin)**  sett. Frekari upplýsingar eru í  [Stofna notendur samkvæmt leyfum](../ui-how-users-permissions.md)  og  [úthluta heimildum til notenda og hópa](../ui-define-granular-permissions.md).

## Settu Dynamics 365 Business Central forritið upp í Shopify netverslunina þína

Fyrir fyrirliggjandi tilvik af  [!INCLUDE[prod_short](../includes/prod_short.md)] er þetta skref valfrjálst og hægt er að sleppa því.

1. Finndu [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central) forritið í [Shopify AppStore](https://apps.shopify.com/)
2. Veldu hnappinn **Bæta við forriti**. Skráðu þig inn á Shopify reikninginn þinn ef beðið er um það. Veldu vefverslunina ef þú ert með fleiri en eina.
3. Þegar búið er að fara yfir persónuvernd og heimildir skaltu velja hnappinn **Setja upp forrit**.

   Þú getur fundið og opnað uppsett **Dynamics 365 Business Central** forrit í hlutanum **Forrit** á hliðarstikunni á síðunni **Shopify stjórnandi**.
4. Veldu  **skrá núna**  til að hefja  [!INCLUDE[prod_short](../includes/prod_short.md)]  réttarhöldin, eða  **Skráðu þig inn**  ef þú ert þegar með [!INCLUDE[prod_short](../includes/prod_short.md)]. Þér verður beint á síðuna [Business Central](https://businesscentral.dynamics.com).
5. Gera næstu skrefin í [!INCLUDE[prod_short](../includes/prod_short.md)].

## Tengja Business Central við Shopify netverslunina

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, opna **Shopify Verslun** og veldu tengda tengilinn.
2. Valið er aðgerðin **Nýtt**.  
3.  **Í reitinn Kóti**  er færður inn kóti sem auðvelt er að finna í [!INCLUDE[prod_short](../includes/prod_short.md)]. Nafnið gæti til dæmis endurspeglað það sem búð selur, svo sem "húsgögn" eða "kaffi", eða það land eða svæði sem það þjónar.
4.  **Shopify Í reitinn vefslóð**  er FÆRT inn veffang vefverslunar sem verið er að tengjast. Notaðu eftirfarandi snið: `https://{shop}.myshopify.com/`.
5. Kveiktu á  **virkjunni**  skipta og síðan er farið yfir og samþykkt skilmála.
6. Skráðu þig inn á Shopify reikninginn þinn ef beðið er um það. Farið yfir persónuverndarhugtökin og heimildir og veljið  **síðan hnappinn setja upp App** .

Endurtaktu skref 2-6 fyrir allar netverslanir sem þú vilt tengjast.

### Þekkt vandamál

- Vafrinn lokar sprettiglugganum. Þegar þú kveikir á virkjunni skipta opnar bið eftir svari-ekki loka þessari síðu  **á meðan hún bíður eftir aðgangstákn**  .  [!INCLUDE [prod_short](../includes/prod_short.md)]  **·**  Shopify Ef þessi síða er lokuð eða lokuð er ekki hægt að  Shopify tengjast. Frekari upplýsingar er að finna í [Biðja um aðgangslykilinn](troubleshoot.md#request-the-access-token).
- [Villa:  Oauth  villa invalid_request: Ekki tókst að finna  Shopify  API-forrit með api_key](troubleshoot.md#error-oauth-error-invalid_request-could-not-find-shopify-api-application-with-api_key)
- [Ekki hægt að tengja frá sandkassa](troubleshoot.md#verify-and-enable-permissions-to-make-http-requests-in-a-non-production-environment)

## Næstu skref

Nú er netverslunin þín tengd við [!INCLUDE[prod_short](../includes/prod_short.md)]. Í næstu skrefum skilgreinir þú hvernig og hvað á að samstilla.

- [Samstilla vörur](synchronize-items.md)
- [Samstilla viðskiptavini](synchronize-customers.md)
- [Samstilla pantanir](synchronize-orders.md)

## Aðferðir við prófanir

Það eru ólíkar nálganir til að prófa samþættingu og hver nálgun hefur sína prívat og galla.

Þú getur tengst  [!INCLUDE[prod_short](../includes/prod_short.md)]  og  Shopify  reikninga eins oft og þú vilt.  Shopify Tengivirki hefur áhrif eingöngu á umhverfið, eða verður nákvæmara, fyrirtækið þar sem það virkjast. Hægt er að tengjast sömu  Shopify  netverslun frá mörgum umhverfi eða fyrirtækjum. Hægt er að gera virkt og endurvirkja tengið.

Auðvelt er að endurkeyra samstillingarprófanir. Tengitengið gerir kleift að eyða innfluttum gögnum, til dæmis afurðum, viðskiptavinum og pöntunum og flytja þau síðan inn aftur. Endurstilla bara  [samstillingu](troubleshoot.md#reset-sync).

### Shopify Sandkassi og atvinnuhúsnæði Mið-sandkassann

Þetta er öruggasta leiðin til að prófa samþættingu. Í stað þess að nota  Shopify  sandkassa er einnig hægt að nota prufuáskrift eða Þróunargeyma. Í  [!INCLUDE[prod_short](../includes/prod_short.md)] er einnig hægt að nota prófunarfyrirtæki í vinnsluumhverfi.

Til að fræðast meira um  [!INCLUDE[prod_short](../includes/prod_short.md)]  sandreiti er farið í að búa til  [Nýtt umhverfi](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#create-a-new-environment).

### Shopify Sandkassi og rekstur Miðbæjarframleiðsla

Þetta er  *ekki*  Ráðlögð samskipan fyrir prófanir þar sem Connector er hægt að  Shopify  Stofna eða breyta vörum og viðskiptamönnum. Hann getur einnig stofnað söluskjöl eins og pantanir og reikninga. Þessi skjöl getur verið erfitt að afturkalla.
 
Ef nota þarf þessa skilgreiningu er mælt með því að endurskoða og líklega gera eftirfarandi stillingar óvirkar:

* **Stofna sjálfkrafa Óþekkt atriði**  til að stofna ekki vörur
* **Shopify hægt að uppfæra vörur**  til að ekki uppfæra vörpuð atriði
* **Stofna sjálfkrafa óþekkta viðskiptavini**  til að stofna ekki viðskiptavini og tengiliði
* **Shopify hægt að uppfæra viðskiptamenn**  til að uppfæra ekki fyrirliggjandi viðskiptavini
* **Stofna sölupöntun**  sjálfvirkt til að stofna sölupantanir og sölureikninga sjálfkrafa

Sjá  [endurheimt umhverfi](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-backup-restore) fyrir frekari upplýsingar.

### Shopify framleiðsla og rekstur Aðalbox sandkassan

Það gæti verið góð hugmynd að taka öryggisafrit af gögnunum. Til dæmis útflutning á vörum og viðskiptavinum. Frekari upplýsingar er að finna í using CSV skrár til að fá  [öryggisafrit af verslunarupplýsingum](https://help.shopify.com/en/manual/shopify-admin/duplicate-store#using-csv-files-to-back-up-store-information).

Slökkva á  **Allow gögnum samkeyrslu til að  Shopify**  skipta því sem  [!INCLUDE[prod_short](../includes/prod_short.md)]  ekki skrifar yfir á Shopify. Í þessu tilfelli er hægt að flytja inn vörur, myndir, viðskiptavini og pantanir frá Shopify. En það verður ekki hægt að senda vöru, verð, birgðastig, viðskiptamenn, upplýsingar um  Shopify uppfyllingu.

Ef Samkeyrsla leyfa er haldið  **til að  Shopify**  skipta á virkjum, þá eru viðbótarhlífðarráðstafanir:

*   Velja  **drög**  í  **stöðunni stofna afurðarsvæði**  til að tryggja að útfluttar afurðir séu ekki tiltækar fyrir kaupendur. Hægt er að sannreyna hvernig vörur líta út í netverslun, samstilla verð, valkosti og birgðastig. Gættu þess aðeins að nota afmarkanir á  **síðunni bæta við vöru  Shopify**  við til að takmarka fjölda útfluttra vara.
*  **Slökkva á Útflutningsviðskiptamanninum  Shopify**  sem á að skipta þannig að Viðskiptavinir séu ekki sendir til Shopify.

## Sjá tengda  [Microsoft-þjálfun](/training/paths/use-shopify-connector-dynamics-365-business-central/)

## Sjá einnig .

[Walkthrough: Uppsetning og notkun  Shopify  tengibúnaðar](walkthrough-setting-up-and-using-shopify.md)  

