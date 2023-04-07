---
title: Úrræðaleit fyrir samstillingu Shopify og Business Central
description: Kynntu þér hvað á að gera ef eitthvað fer úrskeiðis í samstillingu gagna milli Shopify og Business Central
ms.date: 03/27/2023
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30118, 30119, 30120, 30101, 30102'
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
---

# Úrræðaleit fyrir samstillingu Shopify og Business Central

Þú gætir keyrt inn í aðstæður þar sem þú þarft að leita úrræða þegar gögn eru samstillt á milli  Shopify  og [!INCLUDE[prod_short](../includes/prod_short.md)]. Þessi síða skilgreinir villuleitarskref fyrir nokkrar dæmigerðar aðstæður.

## Verk keyrð í forgrunni

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, opna **Shopify Verslun** og veldu tengda tengilinn.
2. Veljið verkstæðið sem á að leita að við úrræðaleit til að opna  **Shopify  Vinnukortasíðuna** .
3. Slökkva á  **samsetlun**  Allow bakgrunns.

Þegar samstillingaraðgerðin er ræst verður verkið keyrt í forgrunni og ef villa verður birtist gluggi fyrir villumelding með  **hlekknum afrita upplýsingar** . Notið þennan tengil til að afrita viðbótarupplýsingar í textaritli fyrir nánari greiningu.

## Skrár

Ef samstillingarverk mistekst er hægt að kveikja á  **kladda virkt**  skipta á  **Shopify  síðunni verkstæðisspjald**  til að virkja innskráningu. Þá geturðu handvirkt ræst samstillingarverkið og yfirfarið skrár.

### Til að gera innskráningu virka

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, opna **Shopify Verslun** og veldu tengda tengilinn.
2. Veljið verkstæðið sem á að leita að við úrræðaleit til að opna  **Shopify  Vinnukortasíðuna** .
3. Kveikja á  **kladdavirkjanum**  skipta.

### Að yfirfara kladda

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, farðu í **Shopify Skráarfærslur** og veldu viðkomandi tengil.
2. Veldu tengda skráningarfærslu og opnaðu síðuna **Shopify skráningarfærsla**.
3. Farðu yfir beiðnina, stöðukóðann og lýsinguna og svargildin. Hægt er að sækja beiðnina og svargildin sem skrár á textaformi.

Síðar skaltu muna að slökkva á skráningu til að forðast neikvæð áhrif á afköst og aukna stærð gagnagrunns.

Á síðunni **Shopify skráarfærslur** geturðu ræst eyðingu á öllum skráarfærslum eða þeim sem eru eldri en sjö daga.

## Gagnataka

Burtséð frá stillingum fyrir **Skrá virkjuð**, eru sum Shopify viðbrögð alltaf skráð svo þú getir skoðað eða sótt þau með síðunni **Listi gagnatöku**.

Veldu aðgerðina **Sótti Shopify gögn** á einni af eftirfarandi síðum:

- **Shopify pöntun**
- **Shopify uppfylling pantana**
- **Sendingarkostnaður Shopify pöntunar**
- **Shopify pöntunarfærslur**
- **Shopify útgreiðslur**
- **Shopify greiðslufærslur**
- **Shopify færslur**

## Endurstilla samstillingu

Til að ná sem bestum árangri flytur tengillinn aðeins inn viðskiptamenn, vörur og pantanir sem búnar eru til eða breytt frá síðustu samstillingu. Á síðunni **Shopify verslunarkort** eru aðgerðir sem breyta dagsetningu/tíma síðustu samstillingar eða endurstilla hana alveg. Þessi aðgerð tryggir að þegar samstilling er keyrð eru öll gögn samstillt frekar en bara breytingarnar frá síðustu samstillingu.

Þessi aðgerð á aðeins við um samstillingar úr Shopify í [!INCLUDE[prod_short](../includes/prod_short.md)]. Það getur verið gagnlegt ef þú þarft að endurheimta eydd gögn eins og vörur, viðskiptamenn eða eyddar pantanir.

## Biðja um aðgangslykilinn

Ef [!INCLUDE[prod_short](../includes/prod_short.md)] vill ekki tengjast Shopify reikningnum þínum skaltu prófa að biðja um aðgangslykilinn frá Shopify. Þessi beiðni gæti verið nauðsynleg ef öryggislyklar eru valdir handahófskennt eða breytingar hafa verið gerðar á nauðsynlegum heimildum (umfangi).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, opnaðu **Shopify verslanir** og veldu viðeigandi tengil.
2. Veldu verslunina sem þú vilt aðgangslykilinn fyrir til að opna síðuna **Shopify verslunarkort**.
3. Veldu aðgerðina **Biðja um aðgang**.
4. Skráðu þig inn á Shopify reikninginn þinn ef beðið er um það.

Víxlhnappurinn **Er með aðgangslykil** verður gerður virkur.

### Staðfesta og virkja heimildir til að leggja fram http-beiðnir þegar keyrt er í öðru umhverfi en framleiðsluumhverfi

Til að allt virki rétt þarf viðbót Shopify tengilsins heimild til að leggja fram http-beiðnir. Þegar prófað er í sandkassa eru http-beiðnir bannaðar fyrir allar viðbætur.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, opnaðu **viðbótastjórnun** og veldu síðan viðkomandi tengil.
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

1. Veldu þá  ![ljósaperu sem opnast Segðu mér lögun 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, opnaðu **Shopify verslanir** og veldu viðeigandi tengil.
2. Veldu verslunina sem þú vilt snúa aðgangslyklinum fyrir til að opna síðuna **Shopify verslunarkort**.
3. Veldu aðgerðina **Biðja um aðgang**.
4. Ef beðið er um það skaltu skrá þig inn á Shopify reikninginn þinn, fara yfir persónuvernd og heimildir og velja svo hnappinn **Setja upp forrit**.

## Þekkt vandamál

### Villa: söluhaus er ekki til. Auðkennissvæði og-gildi: skjalagerð = ' tilboð ', No. = ' þú SHOPIFY STORE '

Til að reikna út verð  Shopify  býr Connector til tímabundið söluskjal (tilboð) fyrir tímabundinn viðskiptavin (Vinnukóta) og gerir staðlaðan verðreiknigrunn að verki. Það er dæmigerð atburðarás þegar þriðji aðili framlengir áskrift að atburðum í sölulínu en kannast ekki við að færslan sé tímabundin, svo að hausinn er hugsanlega ekki aðgengilegur. Viðmælandi okkar er að hafa samband við birgi í framlengingu og biðja þá um að breyta kóða þeirra til að athuga hvort skráningar séu tímabundnar. Í sumum tilvikum skal bæta við  `IsTemporary`  aðferð-Ìn rétti staðurinn er nægur. Nánari upplýsingar um IsTemporary er að fá á  [þykkvasafninu](/dynamics365/business-central/dev-itpro/developer/methods-auto/record/record-istemporary-method). 

Til að sannreyna að vandinn sé vegna Framlengingar á þriðja aðila skal nota  **afritunarupplýsingarnar á klemmuspjaldi**  í villuboðum og afrita efnið yfir í textaritun. Upplýsingarnar inniheldur  **Al Call bunka**, þar sem efsta línan er línan þar sem Villa kom upp. Eftirfarandi er dæmi um AL kalla bunka.

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

Munið að deila símtalinu með upplýsingum um birgi nafnaukann.

### Villa: gen. Bus. bókunarflokkur verður að hafa gildi í Customer: ' þú SHOPIFY STORE '. Það má ekki vera núll eða autt

Á síðunni **Shopify verslunarkort** skal fylla út í reitinn **Sniðmátskóði viðskiptamanns** með sniðmátinu sem er með **Almennur viðskiptabókunarflokkur** útfyllt. Sniðmát viðskiptamanns er notað ekki bara til þess að stofna viðskiptamenn heldur einnig fyrir útreikning á söluverðinu og við stofnun söluskjala.

### Villa: Innflutningur á gögnum til  Shopify  verkstæðis er ekki virkjaður. Opnaðu verslunarkortið til að virkja hann

Í glugganum **Shopify verslunarkort** skaltu kveikja á víxlhnappnum **Leyfa gagnasamstillingu í Shopify**. Þessi víxlhnappur á að vernda netverslunina frá því að fá sýnigögn úr [!INCLUDE[prod_short](../includes/prod_short.md)].

### Villa:  Oauth  villa invalid_request: Ekki tókst að finna  Shopify  API-forrit með api_key

Svo virðist sem þú notir [Innleiða forrit](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview) þar sem vefslóð biðlara er á sniðinu:`https://[application name].bc.dynamics.com`. Tengillinn Shopify virkar ekki fyrir „Innleiða forrit“. Sjá  [hvaða Microsoft-vörur eru með  Shopify  tengibúnað sem tiltækur er fyrir frekari upplýsingar?](shopify-faq.md#which-microsoft-products-are-the-shopify-connector-available-for)

## Sjá einnig .

[Hafist handa með tengilinn fyrir Shopify](get-started.md)
