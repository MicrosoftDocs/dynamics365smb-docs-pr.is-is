---
title: Úrræðaleit fyrir samstillingu Shopify og Business Central
description: Lærðu hvað á að gera ef eitthvað fer úrskeiðis þegar þú samstillir gögn á milli Shopify og Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 04/24/2023
ms.custom: bap-template
ms.search.form: '30118, 30119, 30120, 30101, 30102'
---

# <a name="troubleshooting-the-shopify-and-business-central-synchronization"></a>Úrræðaleit fyrir samstillingu Shopify og Business Central

Þú gætir lent í aðstæðum þar sem þú þarft að leysa vandamál þegar þú samstillir gögn á milli Shopify og [!INCLUDE[prod_short](../includes/prod_short.md)]. Þessi síða skilgreinir úrræðaleit fyrir nokkrar dæmigerðar aðstæður.

## <a name="run-tasks-in-the-foreground"></a>Keyra verkefni í forgrunni

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, opna **Shopify Verslun** og veldu tengda tengilinn.
2. Veldu búðina sem þú vilt leysa úr til að opna **Shopify Verslunarkort** síðuna.
3. Slökktu á **Leyfa bakgrunnssamstillingu** rofa.

Nú, þegar samstillingaraðgerðin er ræst, keyrir verkefnið í forgrunni. Ef villa kemur upp færðu villuglugga með **Afrita upplýsingar** tengli. Notaðu hlekkinn til að afrita upplýsingar í textaritil til frekari greiningar.

## <a name="logs"></a>Skrár

Skráningareiginleikarnir geta gert það auðveldara að bera kennsl á hvers vegna villa kom upp. Á síðunni **Shopify Verslunarkort**, í reitnum **Logging Mode**, geturðu tilgreint hversu nákvæmar upplýsingar þú vilt fanga um villur. Reiturinn býður upp á eftirfarandi valkosti:

- **Óvirkt** - Ekki skrá upplýsingar um villur.
- **Aðeins villa** - Skráðu aðeins villuboðin, án beiðni/svarpöranna. Þessi stilling er sjálfgefin fyrir nýjar verslanir.
- **All** - Skráðu beiðni/svar pörin fyrir allar færslur, þar með talið þær sem heppnuðust. Að skrá allar villur stöðugt getur hægt á [!INCLUDE [prod_short](../includes/prod_short.md)]. Notaðu þessa stillingu þegar gagnaskiptin leiða ekki til villu en þú vilt fá meiri innsýn í gögnin sem voru raunverulega send og móttekin. Athugaðu að sum gögn eru alltaf skráð, óháð því hvort kveikt er á skráningu. Nánari upplýsingar er að finna í [Gagnasöfnun](#data-capture).

### <a name="to-review-logs"></a>Til að skoða logs

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, farðu í **Shopify Skráarfærslur** og veldu viðkomandi tengil.
2. Veldu tengda annálsfærslu og opnaðu síðan  **Shopify Logfærsla** síðuna.
3. Farðu yfir beiðnina, stöðukóðann og lýsinguna og svargildin.

> [!TIP]
> Ef þú verður að hafa samband við Shopify aðstoð til að fá aðstoð við úrræðaleit skaltu athuga upplýsingarnar í reitnum **Auðkenni beiðni** . Þessar upplýsingar geta hjálpað aðstoð við að leysa málið hraðar.

Þú getur halað niður beiðni- og svargildunum sem skrár á textasniði.

### <a name="manage-log-entry-data"></a>Hafa umsjón með gögnum um færsluskráningu

Til að hjálpa til við að halda stærð gagnagrunnsins í skefjum eru annálarfærslur innifaldar í gagnageymslustefnu sem heitir **Shpfy Log Entry**. Varðveislureglur gera þér kleift að tilgreina hversu lengi þú vilt geyma mismunandi tegundir gagna. Sjálfgefið er að Shopify skrárfærslur eru geymdar í einn mánuð. Til að læra meira um varðveislustefnur skaltu fara á [Skilgreina varðveislustefnur](../admin-data-retention-policies.md).

Einnig, á  **Shopify Logfærslum** síðunni geturðu eytt öllum annálsfærslum, eða bara þeim færslum sem eru eldri en sjö dagar.

## <a name="data-capture"></a>Gagnataka

Óháð því hvort kveikt er á skráningu eru sum Shopify svör alltaf skráð. Þú getur skoðað eða hlaðið niður annálunum af  **Data Capture List** síðunni.

Veldu aðgerðina **Sótti Shopify gögn** á einni af eftirfarandi síðum:

- **Shopify pöntun**
- **Shopify pöntunarlínu**
- **Shopify uppfyllingar**
- **Sendingarkostnaður Shopify pöntunar**
- **Shopify pöntunarfærslur**
- **Shopify skila**
- **Shopify afturlína**
- **Shopify endurgreiðslu**
- **Shopify endurgreiðslulína**
- **Shopify útgreiðslur**
- **Shopify greiðslufærslur**
- **Shopify færslur**

## <a name="reset-sync"></a>Endurstilla samstillingu

Til að ná sem bestum árangri flytur tengið aðeins inn viðskiptavini, vörur og pantanir sem voru búnar til eða breytt eftir síðustu samstillingu. Á **Shopify Shop Card** síðunni eru aðgerðir sem breyta dagsetningu/tíma síðustu samstillingar eða endurstilla hana alveg. Þessi aðgerð tryggir að öll gögn samstillast, frekar en bara breytingarnar frá síðustu samstillingu.

Þessi aðgerð á aðeins við um samstillingar úr Shopify í [!INCLUDE[prod_short](../includes/prod_short.md)]. Það getur verið gagnlegt ef þú þarft að endurheimta eydd gögn eins og vörur, viðskiptamenn eða eyddar pantanir.

## <a name="request-the-access-token"></a>Biðja um aðgangslykilinn

Ef [!INCLUDE[prod_short](../includes/prod_short.md)] vill ekki tengjast Shopify reikningnum þínum skaltu prófa að biðja um aðgangslykilinn frá Shopify. Þú gætir þurft að biðja um nýjan tákn ef breytingar urðu á öryggislyklum eða nauðsynlegum heimildum (umfang umsókna).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, opnaðu **Shopify verslanir** og veldu viðeigandi tengil.
2. Veldu verslunina sem þú vilt aðgangslykilinn fyrir til að opna síðuna **Shopify verslunarkort**.
3. Veldu aðgerðina **Biðja um aðgang**.
4. Skráðu þig inn á Shopify reikninginn þinn ef beðið er um það.

Kveikt er á **Hefur AccessKey** rofi.

## <a name="verify-and-enable-permissions-to-make-http-requests-in-a-non-production-environment"></a>Staðfestu og virkjaðu heimildir til að gera HTTP beiðnir í umhverfi sem ekki er framleiðslu

Til að virka rétt þarf Shopify Tengiviðbót leyfis til að gera HTTP beiðnir. HTTP beiðnir eru bannaðar fyrir allar viðbætur þegar þú keyrir próf í sandkassaumhverfi.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, sláðu inn **Extension Management** og veldu síðan tengda hlekkinn.
2. Veldu viðbótina **Shopify tengill**.
3. Veldu aðgerðina **Grunnstilla** til að opna síðuna **Stilling viðbótar**.
4. Gakktu úr skugga um víxlhnappurinn **Leyfa HttpClient-beiðnir** sé virkur.

## <a name="rotate-the-shopify-access-token"></a>Snúðu Shopify aðgangslyklinum

Eftirfarandi ferlar lýsa því hvernig á að snúa aðgangslyklinum sem Shopify tengillinn notar til að komast inn í Shopify netverslunina þína.

### <a name="in-shopify"></a>Eftir Shopify

1. Úr **Shopify stjórnandi** skaltu fara í [Forrit](https://www.shopify.com/admin/apps).
2. Veldu **Eyða** í línunni með **Dynamics 365 Business Central** forritinu.
3. Veldu **Eyða** í skilaboðunum sem birtast.

### <a name="in-"></a>Eftir [!INCLUDE[prod_short](../includes/prod_short.md)]

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, sláðu inn **Shopify verslanir** og veldu svo tengda hlekkinn.
2. Veldu verslunina sem þú vilt snúa aðgangslyklinum fyrir til að opna síðuna **Shopify verslunarkort**.
3. Veldu aðgerðina **Biðja um aðgang**.
4. Ef beðið er um það skaltu skrá þig inn á Shopify reikninginn þinn, fara yfir persónuvernd og heimildir og velja svo hnappinn **Setja upp forrit**.

## <a name="known-issues"></a>Þekkt vandamál

### <a name="error-the-sales-header-does-not-exist-identification-fields-and-values-document-typequotenoyour-shopify-store"></a>Villa: Söluhausinn er ekki til. Auðkennisreitir og gildi: Document Type='Quote',No.='YOUR SHOPIFY STORE'

Til að reikna út verð, býr Shopify Tengið til tímabundið söluskjal (tilboð) fyrir tímabundinn viðskiptavin (verslunarkóði) og notar staðlaða verðútreikningsrökfræði. Ef viðbót frá þriðja aðila gerist áskrifandi að atburðum á tímabundnu söluskjali gæti hausinn ekki verið tiltækur. Við mælum með að þú hafir samband við framlengingarveituna. Biddu þá um að breyta kóðanum sínum til að leita að tímabundnum gögnum. Í sumum tilfellum þurfa þeir bara að bæta `IsTemporary` aðferðinni við á réttum stað. Til að læra meira um `IsTemporary` skaltu fara á [IsTemporary](/dynamics365/business-central/dev-itpro/developer/methods-auto/record/record-istemporary-method). 

Til að staðfesta að vandamálið sé af völdum þriðja aðila viðbót, notaðu  **Afrita upplýsingar á klemmuspjald** tengilinn í villuskilaboðunum og afritaðu efnið í textaritli. Upplýsingarnar innihalda **AL kallastafla**, þar sem efsta línan er línan þar sem villan kom upp. Eftirfarandi dæmi sýnir AL kalla stafla.

AL-kallstafli:

```AL
[Object Name]([Object type] [Object Id]).[Function Name] line [XX] - [Extension Name] by [Publisher] 
...
"Sales Line"(Table 37)."No. - OnValidate"(Trigger) line 98 - Base Application by Microsoft
"Shpfy Product Price Calc."(CodeUnit 30182).CalcPrice line 20 - Shopify Connector by Microsoft
"Shpfy Create Product"(CodeUnit 30174).CreateTempProduct line 137 - Shopify Connector by Microsoft
"Shpfy Create Product"(CodeUnit 30174).CreateProduct line 5 - Shopify Connector by Microsoft
"Shpfy Create Product"(CodeUnit 30174).OnRun(Trigger) line 12 - Shopify Connector by Microsoft
"Shpfy Add Item to Shopify"(Report 30106)."Item - OnAfterGetRecord"(Trigger) line 2 - Shopify Connector by Microsoft
"Shpfy Products"(Page 30126)."AddItems - OnAction"(Trigger) line 5 - Shopify Connector by Microsoft
```

Mundu að deila AL-símtalstaflaupplýsingum með birgi viðbyggingarinnar.

### <a name="error-gen-bus-posting-group-must-have-a-value-in-customer-your-shopify-store-it-cannot-be-zero-or-empty"></a>Villa: Gen. Strætó. Bókunarhópur verður að hafa gildi í Viðskiptavinur: 'YOUR SHOPIFY STORE'. Það getur ekki verið núll eða tómt

Á síðunni **Shopify Verslunarkort**, í reitnum **Kóði viðskiptavinasniðmáts**, veljið sniðmátið sem hefur **Gen. Strætó. Birtingarhópur** fylltur. Viðskiptavinasniðmátið er notað til að stofna viðskiptavini og til að reikna út söluverð á söluskjölum.

### <a name="error-importing-data-to-your-shopify-shop-isnt-enabled-go-to-the-shop-card-to-enable-it"></a>Villa: Ekki er virkt að flytja inn gögn í Shopify verslunina þína. Opnaðu verslunarkortið til að virkja hann

Á  **Shopify Shop Card** síðunni skaltu kveikja á **Leyfa gagnasamstillingu að Shopify** skipta. Þessi stilling hjálpar til við að vernda netverslunina frá því að fá kynningargögn frá [!INCLUDE[prod_short](../includes/prod_short.md)].

### <a name="error-oauth-error-invalid_request-could-not-find-shopify-api-application-with-api_key"></a>Villa: Oauth villa invalid_request: Gat ekki fundið Shopify API forrit með api_key

Svo virðist sem þú notir [Innleiða forrit](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview) þar sem vefslóð biðlara er á sniðinu:`https://[application name].bc.dynamics.com`. Tengillinn Shopify virkar ekki fyrir „Innleiða forrit“. Til að fá frekari upplýsingar, farðu í [Hvaða Microsoft vörur eru Shopify tengið í boði fyrir?](shopify-faq.md#which-microsoft-products-are-the-shopify-connector-available-for).

### <a name="error-internal-error-looks-like-something-went-wrong-on-our-end-request-id-xxxxxxxx-xxxx-xxxx-xxxx-xxxx"></a>Villa: Innri villa. Það lítur út fyrir að eitthvað hafi farið úrskeiðis á endanum okkar. Auðkenni beiðni: XXXXXXX-XXXX-XXXX-XXXX-XXXX

Hafðu samband við Shopify stuðning innan sjö daga frá því að þessi villa kom upp og gefðu upp beiðniauðkenni. Til að læra meira skaltu fara í [Stuðningsvalkostir fyrir Shopify](shopify-faq.md#shopify).

### <a name="error-oauth-error-invalid_request-your-account-does-not-have-permission-to-grant-the-requested-access-for-this-app"></a>Villa: Oauth villa invalid_request: Reikningurinn þinn hefur ekki leyfi til að veita umbeðinn aðgang fyrir þetta forrit.

Svo virðist sem notandi sem biður um aðgang hafi ekki réttindi til að stjórna forritum (getu til að stjórna og setja upp forrit og rásir, sem og hugsanlega samþykkja appgjöld). Þú gætir hugsanlega leyst þetta vandamál með því að setja upp forritið sem reikningseigandi. Að öðrum kosti geturðu athugað **App heimildir** fyrir notandann í [**Notanda og heimildum**](https://www.shopify.com/admin/settings/account) stillingunum í **Shopify stjórnandi**.  

### <a name="messageaccess-denied-for-field-fieldlocationsline0column0pathpathextensionscodeaccess_denieddocumentationhttpsshopifydevapiusageaccess-scopes"></a>[{"message":"Aðgangi hafnað fyrir FIELD reit.","locations":[{"line":0,"column":0}],"path":["path"],"extensions":{"code":"ACCESS_DENIED","documentation":https://shopify.dev/api/usage/access-scopes}}]

Biddu um nýtt tákn vegna þess að uppfærð útgáfa af tenginu krefst fleiri heimilda (umfang forrita). Til að fá frekari upplýsingar skaltu fara á [Biðja um aðgangslykil](#request-the-access-token).

## <a name="see-also"></a>Sjá einnig .

[Hafist handa með tengilinn fyrir Shopify](get-started.md)
