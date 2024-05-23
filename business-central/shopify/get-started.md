---
title: Hafist er handa með tengi fyrir Shopify
description: Fyrstu skrefin þegar tenging er stillt milli Business Central og Shopify.
ms.date: 04/30/2024
ms.topic: article
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
ms.search.form: '30100, 30101, 30102, 30103, 30104, 30135,'
author: brentholtorf
ms.author: bholtorf
---

# <a name="get-started-with-the-shopify-connector"></a>Hafist handa Shopify með Connector

Tengdu Shopify verslanir við [!INCLUDE [prod_short](../includes/prod_short.md)] og stækkaðu framleiðni fyrirtækisins. Stjórnaðu og skoðaðu innsýn í viðskiptin og Shopify verslunina þína í einni einingu.

Til að nota Shopify með [!INCLUDE [prod_short](../includes/prod_short.md)] þarf fyrst að gera nokkra hluti. Þessi grein þjónar hlutverki leiðsagnar til að samþætta Shopify verslun við [!INCLUDE [prod_short](../includes/prod_short.md)].

## <a name="prerequisites-for-shopify"></a>Forkröfur fyrir Shopify

Þú verður að vera með:

- Reikningur Shopify 
- Netverslun Shopify 

Nánari upplýsingar um hvernig á að stofna Shopify prufur og stillingarnar sem mælt er með er farið í [Stofna og settur upp reikningur Shopify](shopify-account.md).

## <a name="prerequisites-for-business-central"></a>Skilyrði fyrir Business Central

- Gakktu úr skugga um að forritið **[Shopify tengill](https://go.microsoft.com/fwlink/?linkid=2196238)** sé uppsett.

  Forritið er foruppsett fyrir allar nýjar innskráningar og rannsóknir. Frekari upplýsingar um uppsetningu forrit úr AppSource eru í [Uppsetning og fjarlæging viðbóta](../ui-extensions-install-uninstall.md#install). Fylgdu skrefunum hér að neðan ef þú ert ekki með [!INCLUDE[prod_short](../includes/prod_short.md)].

- Tryggja skal að notandinn hafi réttar heimildir. Shopify Tengill nær yfir **Shopify  – Admin (SHPFY – ADMIN)** permission set. Nánari upplýsingar um [stofnun notenda í samræmi við leyfi](../ui-how-users-permissions.md) og [úthluta heimildum til notenda og hópa](../ui-define-granular-permissions.md).

## <a name="install-the-dynamics-365-business-central-app-to-your-shopify-online-store"></a>Settu Dynamics 365 Business Central forritið upp í Shopify netverslunina þína

Fyrirliggjandi tilvik af [!INCLUDE[prod_short](../includes/prod_short.md)] er þetta skref valfrjálst og hægt er að sleppa því.

1. Finnið appið [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central) í [Shopify AppStore](https://apps.shopify.com/).
2. Veldu hnappinn **Bæta við forriti**. Skráðu þig inn á Shopify reikninginn þinn ef beðið er um það. Vefverslun er valin ef um fleiri en eitt er að ræða.
3. Þegar búið er að fara yfir persónuvernd og heimildir skaltu velja hnappinn **Setja upp forrit**.

   Þú getur fundið og opnað uppsett **Dynamics 365 Business Central** forrit í hlutanum **Forrit** á hliðarstikunni á síðunni **Shopify stjórnandi**.
4. Veldu Skráðu **þig núna** til að hefja réttarhöldin [!INCLUDE[prod_short](../includes/prod_short.md)] eða **skráðu þig inn** ef þú ert þegar með [!INCLUDE[prod_short](../includes/prod_short.md)]. Þér verður beint á síðuna [Business Central](https://businesscentral.dynamics.com).
5. Gerið næstu skref inn [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="connect-business-central-to-the-shopify-online-store"></a>Tengja Business Central við Shopify netverslunina

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, opna **Shopify Verslun** og veldu tengda tengilinn.
2. Valið er aðgerðin **Nýtt**.  
3. Í reitinn **Kóti** er færður inn kóti sem auðvelt er að finna í [!INCLUDE[prod_short](../includes/prod_short.md)]. Heitið gæti til dæmis endurspeglað það sem búð selur, t.d. "Húsgögn" eða "Kaffi" eða landið eða svæðið sem það þjónar.
4. Í reitinn **Shopify URL** er færð inn URL vefverslunarinnar sem þú ert að tengja. Notaðu eftirfarandi snið: `https://{shop}.myshopify.com/`.

   > [!TIP]
   > Hægt er að afrita veffangið úr Shopify Admin, eins `https://admin.shopify.com/store/{shop}` og, og tengillinn breytir því í það snið sem þarf.

5. Kveikja á virku **vífærslunni** og endurskoða og samþykkja skilmálana og skilyrðin.
6. Skráðu þig inn á Shopify reikninginn þinn ef beðið er um það. Skoðaðu persónuverndarskilmálana og heimildir og veldu svo hnappinn **Setja upp forrit** .

Endurtaktu skref 2-6 fyrir allar netverslanir sem þú vilt tengjast.

### <a name="known-issues"></a>Þekkt vandamál

- Vafrinn lokar sprettiglugga. Þegar kveikt er **á virku** vísbendingunni [!INCLUDE [prod_short](../includes/prod_short.md)]  **opnast Beðið eftir svari - ekki loka síðunni** meðan beðið er eftir aðgangstákni frá Shopify. Ef síðunni er lokað eða lokað er ekki hægt að Shopify tengjast. Læra meira á [Request the access tákn](troubleshoot.md#request-the-access-token).
- Gott gæti verið að hafa stjórnandann Shopify opna í sama vafranum og [!INCLUDE [prod_short](../includes/prod_short.md)] hann.
- [Villa: Oauth villa invalid_request: API-forritið fannst Shopify ekki með api_key.](troubleshoot.md#error-oauth-error-invalid_request-could-not-find-shopify-api-application-with-api_key)
- [Villa: Oauth villa invalid_request: Reikningurinn þinn hefur ekki heimild til að veita umbeðinn aðgang að forritinu.](troubleshoot.md#error-oauth-error-invalid_request-your-account-does-not-have-permission-to-grant-the-requested-access-for-this-app)
- [Ekki er hægt að tengjast úr sandkassa](troubleshoot.md#verify-and-enable-permissions-to-make-http-requests-in-a-non-production-environment)
- Ganga þarf úr skugga um að rétt URL sé fært inn í **Shopify reitinn URL** . Hægt er að búa til veffangið með því að sameina verslunarkennið úr stjórnunarslóðinni. Til dæmis, `admin.shopify.com/store/{shop}`  og `.myshopify.com` til að fá `https://{shop}.myshopify.com/`.

## <a name="next-steps"></a>Næstu skref

Nú er netverslunin þín tengd við [!INCLUDE[prod_short](../includes/prod_short.md)]. Í næstu skrefum skilgreinir þú hvernig og hvað á að samstilla.

- [Samstilla vörur og birgðir](synchronize-items.md)
- [Samstilla viðskiptavini](synchronize-customers.md)
- [Samstilla pantanir](synchronize-orders.md)

## <a name="testing-strategies"></a>Prófun aðferðir

Það eru mismunandi aðferðir til að prófa samþættingu, og hver nálgun hefur sína kosti og galla.

Hægt er að tengja [!INCLUDE[prod_short](../includes/prod_short.md)] og reikninga eins oft og Shopify óskað er.  Shopify Tengið hefur aðeins áhrif á umhverfið eða til að vera nákvæmari, fyrirtækið þar sem það er virkjað. Hægt er að tengjast sömu Shopify netverslun frá mörgum umhverfi eða fyrirtækjum. Hægt er að gera tengið óvirkt og gert það aftur virkt.

Auðvelt er að endurkeyra samstillingarpróf. Tengillinn gerir kleift að eyða innfluttum gögnum, t.d. vörum, viðskiptamönnum og pöntunum og flytja þau síðan inn aftur. Endurstillaðu bara [samstillingu](troubleshoot.md#reset-sync).

### <a name="shopify-sandbox-and-business-central-sandbox"></a>Shopify sandkassi og Business Central sandkassi

Þetta er líklega öruggasta leiðin til að prófa samþættingu. Í stað þess að nota Shopify sandkassa er hægt að nota prufuáskrift eða Þróunarverslun. Einnig [!INCLUDE[prod_short](../includes/prod_short.md)] er hægt að nota prófunarfyrirtæki í framleiðsluumhverfi.

Til að fræðast meira um [!INCLUDE[prod_short](../includes/prod_short.md)] sandkassa er farið í [Stofna nýtt umhverfi](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#create-a-new-environment).

### <a name="shopify-sandbox-and-business-central-production"></a>Shopify sandkassa og Business Central framleiðsla

Ekki er *mælt* með samstillingu við prófun vegna þess að Shopify Connector getur stofnað eða breytt vörum og viðskiptamönnum. Einnig er hægt að búa til söluskjöl eins og pantanir og reikninga. Það getur verið erfitt að afturkalla þessi skjöl.

Ef nota þarf þessa grunnstillingu er mælt með því að þú skoðir og gerir líklega eftirfarandi stillingar óvirkar:

- **Stofna óþekkta vöru** sjálfvirkt til að stofna ekki vörur.
- **Shopify getur uppfært vörur** til að uppfæra ekki varpaðar vörur.
- **Stofna óþekkta viðskiptamann sjálfvirkt** til að stofna ekki viðskiptamenn og tengiliði.
- **Shopify geta uppfært viðskiptamenn** til að uppfæra ekki núverandi viðskiptamenn.
- **Stofna sölupöntun** sjálfvirkt til að stofna ekki sölupantanir og sölureikninga.

Nánari upplýsingar eru [í Endurheimt umhverfis](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-backup-restore).

### <a name="shopify-production-and-business-central-sandbox"></a>Shopify framleiðslu og Business Central sandkassa

Það gæti verið góð hugmynd að taka öryggisafrit af gögnunum. Til dæmis má flytja út vörur og viðskiptamenn. Nánari upplýsingar eru í [Notkun CSV-skráa til að taka öryggisafrit af verslunarupplýsingum](https://help.shopify.com/en/manual/shopify-admin/duplicate-store#using-csv-files-to-back-up-store-information).

Slökkva á samstillingu **gagna til að Shopify** vífæra svo að ekki sé [!INCLUDE[prod_short](../includes/prod_short.md)] skrifað í Shopify. Í þessu tilviki verður þú að vera fær um að flytja inn vörur, myndir, viðskiptamenn og pantanir frá Shopify. En ekki verður hægt að senda vöru, verð, birgðastig, viðskiptamenn og upplýsingar um Shopify uppfyllingu.

Ef þú heldur samstillingu **gagna áfram til að Shopify** vífæra virka eru viðbótarhlífar:

- Valið er **Drög** í reitnum **Staða fyrir stofnun vöru** til að tryggja að útfluttar vörur séu ekki tiltækar kaupendum. Hægt er að sannprófa hvernig vörur líta út í netverslun og samstilla verð, valkosti og birgðastig. Passaðu bara að nota afmarkanir á síðunni **Bæta vöru við til að Shopify** takmarka fjölda útfluttra vara.
- Slökkva á útflutningsviðskiptamönnum **til að Shopify** vífæra svo að ekki séu sendir viðskiptamenn. Shopify

## <a name="see-also"></a>Sjá einnig .

[Kynning: Uppsetning og notkun Shopify tengis](walkthrough-setting-up-and-using-shopify.md)  

