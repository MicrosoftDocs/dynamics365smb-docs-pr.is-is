---
title: Úrræðaleit fyrir samstillingu Shopify og Business Central
description: Lærðu hvað á að gera ef eitthvað fer úrskeiðis þegar gögn eru samstillt á milli  Shopify  og Viðskiptamiðst.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 04/24/2023
ms.custom: bap-template
ms.search.form: '30118, 30119, 30120, 30101, 30102'
---

# Úrræðaleit fyrir samstillingu Shopify og Business Central

Þú gætir keyrt inn í aðstæður þar sem þú þarft að leita úrræða þegar gögn eru samstillt á milli  Shopify  og [!INCLUDE[prod_short](../includes/prod_short.md)]. Þessi síða skilgreinir villuleitarskref fyrir nokkrar dæmigerðar aðstæður.

## Verk keyrð í forgrunni

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, opna **Shopify Verslun** og veldu tengda tengilinn.
2. Veljið verkstæðið sem á að leita að við úrræðaleit til að opna  **Shopify  Vinnukortasíðuna** .
3. Slökkva á  **samsetlun**  Allow bakgrunns.

Þegar samstillingaraðgerðin er ræst verður verkið keyrt í forgrunni. Ef villa kemur upp, færðu villusvarglugga með  **hlekknum afrita upplýsingar** . Notið tengilinn til að afrita upplýsingar í textaritli fyrir nánari greiningu.

## Skrár

Ef samstillingarverk mistekst er hægt að kveikja á  **kladda virkt**  skipta á  **Shopify  síðunni verkstæðisspjald**  til að virkja innskráningu. Þá geturðu handvirkt ræst samstillingarverkið og yfirfarið skrár.

### Til að gera innskráningu virka

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, opna **Shopify Verslun** og veldu tengda tengilinn.
2. Veljið verkstæðið sem á að leita að við úrræðaleit til að opna  **Shopify  Vinnukortasíðuna** .
3. Kveikja á  **kladdavirkjanum**  skipta.

### Að yfirfara kladda

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, farðu í **Shopify Skráarfærslur** og veldu viðkomandi tengil.
2. Valin er tengd kladdafærsla og síðan er  **Shopify  síðan opnuð kladdafærsla** .
3. Farðu yfir beiðnina, stöðukóðann og lýsinguna og svargildin. Hægt er að sækja beiðnina og svargildin sem skrár á textaformi.

Síðar þarf að muna að slökkva á innskráningu til að forðast neikvæð áhrif á afköst og aukningu í gagnagrunnsstærð.

 **Shopify Á síðunni kladdafærslur**  er hægt að kalla fram eyðingu allra kladdafærslna, eða færslna sem eru eldri en sjö daga.

## Gagnataka

Sum  **svör eru alltaf skráð án tillits til hvort**  Innskráning er virk Shopify . Hægt er að skoða eða sækja kladda af  **listasíðunni**  gagnatökun.

Veldu aðgerðina **Sótti Shopify gögn** á einni af eftirfarandi síðum:

- **Shopify pöntun**
- **Shopify pöntunarlínu**
- **Shopify uppfylltar**
- **Sendingarkostnaður Shopify pöntunar**
- **Shopify pöntunarfærslur**
- **Shopify skila**
- **Shopify Skilalína**
- **Shopify endurgreiðslu**
- **Shopify endurgreiðslulínu**
- **Shopify útgreiðslur**
- **Shopify greiðslufærslur**
- **Shopify færslur**

## Endurstilla samstillingu

Fyrir bestan árangur flytur Connector eingöngu viðskiptavini, vörur og pantanir sem voru stofnaðar eða breytt eftir síðustu samstillingu.  **Shopify Á Vinnukortssíðunni**  eru aðgerðir sem breyta dagsetningu/tíma síðustu samstillingar eða algjörlega endurstilla þær. Þessi aðgerð tryggir að öll gögn samstillir frekar en breytingarnar frá síðustu samstillingu.

Þessi aðgerð á aðeins við um samstillingar úr Shopify í [!INCLUDE[prod_short](../includes/prod_short.md)]. Það getur verið gagnlegt ef þú þarft að endurheimta eydd gögn eins og vörur, viðskiptamenn eða eyddar pantanir.

## Biðja um aðgangslykilinn

Ef [!INCLUDE[prod_short](../includes/prod_short.md)] vill ekki tengjast Shopify reikningnum þínum skaltu prófa að biðja um aðgangslykilinn frá Shopify. Það gæti þurft að biðja um nýtt tákn ef breytingar voru gerðar á öryggislyklum eða nauðsynlegum heimildum (Application umfang).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, opnaðu **Shopify verslanir** og veldu viðeigandi tengil.
2. Veldu verslunina sem þú vilt aðgangslykilinn fyrir til að opna síðuna **Shopify verslunarkort**.
3. Veldu aðgerðina **Biðja um aðgang**.
4. Skráðu þig inn á Shopify reikninginn þinn ef beðið er um það.

Víxlhnappurinn **Er með aðgangslykil** verður gerður virkur.

## Sannreyna og virkja heimildir til að gera HTTP beiðnir í umhverfi sem er ekki í framleiðslu

Til að vinna rétt  Shopify  þarf tengivirkið leyfi til að gera HTTP beiðnir. Við prófun í sandkassa eru HTTP-beiðnir bannaðar fyrir öllum viðaukum.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn  **Framlengingarstjórnun** og velja síðan tengda tengilinn.
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

1. Veldu þá  ![ljósaperu sem opnast Segðu mér lögun 1.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn  **Shopify  verslanir** og veljið síðan tengda tengilinn.
2. Veldu verslunina sem þú vilt snúa aðgangslyklinum fyrir til að opna síðuna **Shopify verslunarkort**.
3. Veldu aðgerðina **Biðja um aðgang**.
4. Ef beðið er um það skaltu skrá þig inn á Shopify reikninginn þinn, fara yfir persónuvernd og heimildir og velja svo hnappinn **Setja upp forrit**.

## Þekkt vandamál

### Villa: söluhaus er ekki til. Auðkennissvæði og-gildi: skjalagerð = ' tilboð ', Nr. = ' SHOPIFY STORE ' '

Til að reikna út verð  Shopify  stofnar tengivirkið tímabundið söluskjal (tilboð) fyrir tímabundinn viðskiptavin (Vinnukóta) og notar stöðluðu reiknirökin fyrir verð. Ef um er að ræða framlengingu þriðja aðila á viðburðum í tímabundnu söluskjali gæti verið að hausinn sé tiltækur. Við mælum með því að hafa samband við framlengingarveitu. Biðja þá um að breyta kóðanum sínum til að leita að tímabundnum færslum. Í sumum tilfellum þurfa þeir bara að bæta við  `IsTemporary`  aðferðinni Ìn á réttum stað. Til að fræðast meira um  `IsTemporary` er farið í  [þykkvasafn](/dynamics365/business-central/dev-itpro/developer/methods-auto/record/record-istemporary-method). 

Til að sannreyna að vandinn sé vegna Framlengingar á þriðja aðila skal nota  **afritunarupplýsingarnar á klemmuspjaldi**  í villuboðum og afrita efnið í textaritli. Upplýsingarnar inniheldur  **Al Call bunka**, þar sem efsta línan er sú lína þar sem villan varð. Eftirfarandi dæmi sýnir AL kallabunka.

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

### Villa: gen. Strætisvagn. bókunarflokkur verður að hafa gildi í Customer: ' SHOPIFY STORE '. Það má ekki vera núll eða autt

 **Shopify Á vinnukortasíðunni**, í  **reitnum sniðmát sniðmáts**  viðskiptamanns, skal velja sniðmátið sem hefur  **gen. viðsk. bókunarflokks** . Sniðmát viðskiptamanns er notað til að stofna viðskiptamenn og reikna söluverð á söluskjölum.

### Villa: Innflutningur á gögnum til  Shopify  verkstæðis er ekki virkjaður. Opnaðu verslunarkortið til að virkja hann

 **Shopify Á Vinnukortasíðunni**  er kveikt á reitnum  **heimila samkeyrslu til að  Shopify**  skipta. Þessi stilling hjálpar til við að vernda vefverslunina með því að sækja sýnigögn [!INCLUDE[prod_short](../includes/prod_short.md)].

### Villa:  Oauth  villa invalid_request: Ekki tókst að finna  Shopify  API-forrit með api_key

Svo virðist sem þú notir [Innleiða forrit](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview) þar sem vefslóð biðlara er á sniðinu:`https://[application name].bc.dynamics.com`. Tengillinn Shopify virkar ekki fyrir „Innleiða forrit“. Til að fá frekari upplýsingar er farið í  [hvaða Microsoft-vörur eru tengivirkið sem er  Shopify  tiltækt?](shopify-faq.md#which-microsoft-products-are-the-shopify-connector-available-for).

### Villa: Innri villa. Svo virðist sem eitthvað hafi farið úrskeiðis á endanum. Óska eftir auðkenni: XXXXXXXX-XXXX-XXXX-XXXX-XXXX

Vinsamlegast hafðu samband  Shopify  við þig innan 7 daga frá því að upplifa þessa villu og Gefðu upp kenni beiðninnar. Til að fá frekari upplýsingar er farið í  [stuðningsvalkosti Shopify](shopify-faq.md#shopify).

## Sjá einnig .

[Hafist handa með tengilinn fyrir Shopify](get-started.md)
