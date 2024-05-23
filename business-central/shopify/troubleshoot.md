---
title: Úrræðaleit í Shopify samstillingu Business Central
description: Lærðu að gera ef eitthvað fer úrskeiðis þegar þú samstillir gögnin milli Shopify og Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 05/01/2024
ms.custom: bap-template
ms.search.form: '30118, 30119, 30120, 30101, 30102'
ms.service: dynamics-365-business-central
---

# Úrræðaleit í Shopify samstillingu Business Central

Hægt er að keyra í aðstæður þar sem leysa þarf úr vandamálum þegar gögn eru samstillt milli Shopify og [!INCLUDE[prod_short](../includes/prod_short.md)]. Þessi síða skilgreinir úrræðaleitarskref fyrir dæmigerðar aðstæður.

## Keyra verk í forgrunni

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, opna **Shopify Verslun** og veldu tengda tengilinn.
2. Velja skal verkstæðið sem ætlunin er að ræsa til að opna síðuna **Shopify Vinnusalarspjald** .
3. Slökkva á **samstillingarkeyrslum** bakgrunns.

Þegar samstillingaraðgerðin er sett af stað keyrir verkið í forgrunninum. Ef villa kemur upp birtast villusvargluggar með **tengil afritaupplýsinga** . Nota tengilinn til að afrita upplýsingar í textaritil til frekari greiningar.

## Skrár

Með skráningaraðgerðunum er auðveldara að greina hvers vegna villa kom upp. Á síðunni **Shopify Vinnusalarspjald**, í reitnum **Skráningarhamur**, er hægt að tilgreina nákvæmnisstigið sem ætlunin er að ná yfir villur. Í reitnum eru eftirfarandi valkostir:

- **Óvirkt** - Skráir ekki upplýsingar um villur.
- **Villa aðeins** - Skrá aðeins villuboðin án beiðni-/svarpör. Þessi stilling er sjálfgefin fyrir nýjar verslanir.
- **Allt** - Skrá beiðni-/svarpör fyrir allar færslur, þ.m.t. þær sem tókst. Hægt er að hægja á öllum villum ef allar villur eru skráðar [!INCLUDE [prod_short](../includes/prod_short.md)]. Nota skal þessa stillingu þegar gagnaskipti leiða ekki af sér villu en fá á fleiri innsýn í gögnin sem voru send og móttekin. Athuga skal að sum gögn eru alltaf skráð, óháð því hvort skráningarfærsla er virk. Nánari upplýsingar eru [í Data handtaka](#data-capture).

### Til að skoða kladda

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, farðu í **Shopify Skráarfærslur** og veldu viðkomandi tengil.
2. Valin er tengd kladdafærsla og síðan Skrá færslu **Shopify opnað** .
3. Farðu yfir beiðnina, stöðukóðann og lýsinguna og svargildin.

> [!TIP]
> Ef tengiliðastuðningur þarf að Shopify fá aðstoð við úrræðaleit skal athuga upplýsingarnar í reitnum **Kenni** beiðni. Upplýsingarnar geta hjálpað til við að leysa málið hraðar.

Hægt er að sækja beiðni- og svargildi sem skrár á textasniði.

### Vinna með gögn um skráningarfærslu

Til að hjálpa til við að halda stærð gagnagrunnsins undir eftirliti eru skráningarfærslur innifaldar í varðveislureglum sem nefndar **eru Shpfy-skráningarfærsla**. Varðveitingarreglur gera kleift að tilgreina hversu lengi ætlunin er að geyma mismunandi gerðir gagna. Sjálfgefið er að skráningarfærslur séu geymdar Shopify  í einn mánuð. Nánari upplýsingar um varðveitingarstefnur eru notaðar til að [skilgreina varðveitingarstefnur](../admin-data-retention-policies.md).

Á síðunni **Shopify Skrá færslur** er einnig hægt að eyða öllum skráningarfærslum eða aðeins þeim færslum sem eru eldri en sjö daga.

## Gagnataka

Burtséð frá því hvort kveikt er á skráningu eru sum Shopify svör alltaf skráð. Hægt er að skoða eða sækja skrárnar á síðunni **Gagnatökulisti** .

Veldu aðgerðina **Sótti Shopify gögn** á einni af eftirfarandi síðum:

- **Shopify pöntun**
- **Shopify pöntunarlína**
- **Shopify uppfyllingar**
- **Sendingarkostnaður Shopify pöntunar**
- **Shopify pöntunarfærslur**
- **Shopify Skila**
- **Shopify skilalína**
- **Shopify Endurgreiðslu**
- **Shopify endurgreiðslulína**
- **Shopify útgreiðslur**
- **Shopify greiðslufærslur**
- **Shopify færslur**

## Endurstilla samstillingu

Til að ná sem bestum afköstum flytur tengið aðeins inn viðskiptamenn, vörur og pantanir sem voru stofnaðar eða breyttar eftir síðustu samstillingu. Á síðunni **Shopify Vinnusalarspjald** eru aðgerðir sem breyta dagsetningu/tíma síðustu samstillingar eða endurstilla hana að fullu. Þessi aðgerð tryggir að öll gögn samstillist frekar en aðeins breytingar frá síðustu samstillingu.

Þessi aðgerð á aðeins við um samstillingar úr Shopify í [!INCLUDE[prod_short](../includes/prod_short.md)]. Það getur verið gagnlegt ef þú þarft að endurheimta eydd gögn eins og vörur, viðskiptamenn eða eyddar pantanir.

## Biðja um aðgangslykilinn

Ef [!INCLUDE[prod_short](../includes/prod_short.md)] vill ekki tengjast Shopify reikningnum þínum skaltu prófa að biðja um aðgangslykilinn frá Shopify. Hugsanlega þarf að biðja um nýtt tákn ef öryggislyklarnir eða nauðsynlegar heimildir eru gerðar (forritatölur).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, opnaðu **Shopify verslanir** og veldu viðeigandi tengil.
2. Veldu verslunina sem þú vilt aðgangslykilinn fyrir til að opna síðuna **Shopify verslunarkort**.
3. Veldu aðgerðina **Biðja um aðgang**.
4. Skráðu þig inn á Shopify reikninginn þinn ef beðið er um það.

Kveikt **er á víxlnum Með AccessKey** .

## Sannprófa og leyfa heimildir til að gera HTTP-beiðnir í umhverfi sem ekki er framleiðsluhæft

Til að vinna rétt Shopify þarf Connector-viðbótin heimild til að gera HTTP-beiðnir. HTTP-beiðnir eru bannaðar fyrir allar viðbætur þegar prófanir eru keyrðar í sandkassaumhverfi.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **viðbótastjórnun** og velja síðan viðeigandi tengil.
2. Veldu viðbótina **Shopify tengill**.
3. Veldu aðgerðina **Grunnstilla** til að opna síðuna **Stilling viðbótar**.
4. Gakktu úr skugga um víxlhnappurinn **Leyfa HttpClient-beiðnir** sé virkur.

## Snúðu Shopify aðgangslyklinum

Eftirfarandi ferlar lýsa því hvernig á að snúa aðgangslyklinum sem Shopify tengillinn notar til að komast inn í Shopify netverslunina þína.

### Eftir Shopify

1. Úr **Shopify stjórnandi** skaltu fara í [Forrit](https://www.shopify.com/admin/apps).
2. Veldu **Eyða** í línunni með **Dynamics 365 Business Central** forritinu.
3. Veldu **Eyða** í skilaboðunum sem birtast.

### Eftir [!INCLUDE[prod_short](../includes/prod_short.md)]

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Shopify verslanir** og velja síðan viðeigandi tengil.
2. Veldu verslunina sem þú vilt snúa aðgangslyklinum fyrir til að opna síðuna **Shopify verslunarkort**.
3. Veldu aðgerðina **Biðja um aðgang**.
4. Ef beðið er um það skaltu skrá þig inn á Shopify reikninginn þinn, fara yfir persónuvernd og heimildir og velja svo hnappinn **Setja upp forrit**.

## Þekkt vandamál

### Villa: Söluhausinn er ekki til. Kennireitir og gildi: Skjalategund='Tilboð',Nr.='VERSLUNIN ÞÍN'

Til að reikna út verð Shopify stofnar Connector bráðabirgðasöluskjal (tilboð) fyrir bráðabirgðaviðskiptamann (verkstæðiskóta) og notar útreikningsgrunn staðlaðs verðs. Ef þriðji aðili gerist áskrifandi að atburðum í bráðabirgðasöluskjali getur verið að hausinn sé ekki tiltækur. Mælt er með því að hafa samband við viðaukaveituna. Biðja þá um að breyta kóta sínum til að leita að tímabundnum færslum. Í sumum tilfellum þurfa þeir bara að bæta aðferðinni `IsTemporary` við á réttum stað. Farðu í IsTemporary til að `IsTemporary` fræðast meira [um](/dynamics365/business-central/dev-itpro/developer/methods-auto/record/record-istemporary-method). 

Til að ganga úr skugga um að vandinn stafi af viðbót þriðja aðila skal nota **tengilinn Afrita upplýsingar til klippispjalds** í villuboðunum og afrita efnið í textaritil. Upplýsingarnar innihalda AL-símtalsstafla **þar** sem efsta línan er línan þar sem villan kom upp. Eftirfarandi dæmi sýnir AL-símtalsstafla.

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

Muna þarf að samnýta upplýsingar um AL-kallstafla með birgnum í viðbótinni.

### Villa: Alm. Viðsk.bókunarflokkur verður að hafa gildi í Viðskiptamaður: 'YOUR SHOPIFY STORE'. Það má ekki vera núll eða tómt

Á síðunni **Shopify Vinnusalarspjald**, í reitnum **Kóti** sniðmáts viðskiptamanns, er valið sniðmátið sem er **með Alm. viðsk.bókunarflokkur** útfylltur. Viðskiptamannssniðmátið er notað til að stofna viðskiptamenn og reikna söluverð á söluskjölum.

### Villa: Innflutningur gagna í Shopify verkstæðið er ekki virkur. Opnaðu verslunarkortið til að virkja hann

Á síðunni **Shopify Vinnusalarspjald** skal kveikja á **samstillingu leyfa gagna til að Shopify** vífæra. Þessi stilling hjálpar til við að verja netverslunina fyrir [!INCLUDE[prod_short](../includes/prod_short.md)] kynningu á gögnum.

### Villa: Oauth villa invalid_request: API-forritið fannst Shopify ekki með api_key

Þú gætir hafa notað Ívafið [app](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview), þar sem veffang biðlarans er með sniðinu: `https://[application name].bc.dynamics.com`. Tengillinn Shopify virkar ekki fyrir „Innleiða forrit“. Til að fá nánari upplýsingar er farið í [Hvaða vörur Microsoft vinna með Shopify Connector?](shopify-faq.md#which-microsoft-products-work-with-the-shopify-connector).

### Villa: Innri villa. Eitthvað virðist hafa farið úrskeiðis á endanum. Beiðnikenni: XXXXXXXX-XXXX-XXXX-XXXX-XXXX

Tengiliðastuðningur Shopify innan sjö daga frá villunni og beiðnikenni gefið upp. Nánari upplýsingar eru í [Stuðningur fyrir Shopify](shopify-faq.md#shopify).

### Villa: Oauth villa invalid_request: Reikningurinn þinn hefur ekki heimild til að veita umbeðinn aðgang að forritinu. 

Notandinn sem bað um aðgang hefur ekki réttindi til að stjórna forritum (getu til að stjórna og setja upp forrit og rásir, ásamt hugsanlega samþykkja gjöld forrita). Þú getur verið fær um að leysa þetta með því að setja forritið upp sem eiganda reikningsins. Einnig er hægt að athuga heimild forritsins **til notandans í notandanum** og heimildastillingar [**í stjórnandanum**](https://www.shopify.com/admin/settings/account)  **Shopify .**  

### [{"skilaboð":"Aðgangur hafnaður fyrir reitinn REITUR.","birgðageymslur":[{"lína":0,"dálkur":0}],"slóð":["slóð"],"viðbætur":{"kóti":"ACCESS_DENIED","heimild":https://shopify.dev/api/usage/access-scopes}}]

Biðja um nýtt tákn vegna þess að uppfærð útgáfa tengitækisins krefst meiri heimilda (forritatölur). Til að [fá nánari upplýsingar er farið í Aðgangstákn beiðna](#request-the-access-token).

### Það er allt í sófanum. Ógilt API-lykill eða aðgangstákn (óþekkt innskráning eða rangt aðgangsorð)

Biðja um nýtt tákn vegna þess að uppfærð útgáfa tengitækisins krefst meiri heimilda (forritatölur). Til að [fá nánari upplýsingar er farið í Aðgangstákn beiðna](#request-the-access-token).

## Sjá einnig .

[Hafist handa með tengilinn fyrir Shopify](get-started.md)
