---
title: Setja upp og nota Shopify Connector
description: Ýmsar samþættingaraðstæður til að sýna vinnuflæði milli Shopify og Business Central
ms.date: 08/01/2024
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '30101, 30102, 30106, 30107, 30113, 30115, 30126, 30156, 30157'
ms.reviewer: bholtorf
author: brentholtorf
ms.author: bholtorf
---

# Kynning: Uppsetning og notkun Shopify Connector

Þessi hluti sýnir nokkur dæmigerð atburðarás og tekur notandann í gegnum skrefin til að prófa eða þjálfa notendur á vinnuflæði samþættra [!INCLUDE[prod_short](../includes/prod_short.md)] og verslunarinnar Shopify .

## Frumskilyrði 

### Shopify

Þú verður að vera með:

- Reikningur Shopify 
- Netverslun Shopify 

Fræðast meira um hvernig á að búa til Shopify prufur og ráðlagðar stillingar í [Stofna og setja upp Shopify reikning](shopify-account.md).

### Business Central

Þú verður að vera með [!INCLUDE[prod_short](../includes/prod_short.md)] reikning. 

Til dæmis er hægt að búa til prufureikning eða hefja prufu. Nánari upplýsingar um [útbúa sýningaumhverfi og Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/administration/demo-environment)  [skráðu þig fyrir réttarhöldunum](../trial-signup.md). 

## Tengja Business Central við verkstæðið Shopify 

Eftirfarandi [!INCLUDE[prod_short](../includes/prod_short.md)] er gert í:

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Shopify Verslanir** og velja síðan viðeigandi tengja.
2. Aðgerðin Ný er **valin** .
3. Fært er inn **í reitinn** Kóti `DEMO1`.
4. Í reitinn **Shopify URL er URL** fyrir vefverslunina sem á að tengjast fært inn.
5. Virkja virkt **vífæra** og fara yfir og samþykkja skilmála og skilyrði.

Til að grunnstilla verkstæðið Shopify skal fylgja eftirfarandi skrefum:

1. Slökkva á **samstillingarkeyrslum** bakgrunns.
2. Valið *er Til Shopify* í reitnum **Samstilla vöru** .
3.  *Valið Shopify* í reitnum **Samstilla vörumyndir** .
4. Kveikja á vífærslunni **Samstilla vörueigindir** .
5. Kveikja á víhlöðuna **Birgðir** raktar.
6.  *Hafna í reitnum* Sjálfgefin birgðaregla **er valið** .
7. Kveikja á vífærslu **óþekktra** viðskiptamanna sjálfvirkt.
8. Viðeigandi sniðmát er fært í reitinn **Sniðmát** viðskiptamanns/fyrirtækis.
9.  **Fylla út reikning afhendingarkostnaðar**, **ábendingarreikningur** með tekjureikningnum. Til dæmis í Bandaríkjunum, notkun `40210`.
10. Kveikja á víflipinu **Stofna pantanir** sjálfvirkt.
11. Slökkva á vífæringu sjálfvirkrar **útgáfu sölupantana** .

Grunnstilla staðsetningu vörpun:

1. Veljið aðgerðina **Birgðageymslur** til að opna **Shopify Birgðageymslur verkstæðis**.
2. Velja skal aðgerðina **Sækja Shopify birgðageymslur** til að flytja inn allar birgðageymslur sem skilgreindar eru í skjámyndinni Shopify. Valin er færsla með **Er aðalvífæra** hefur verið valin.
3. Fært er inn **í** Birgðageymsluafmörkun `''|EAST|MAIN`.
4. Valið er *Áætluð staða til ráðstöfunar í dag* í reitnum **Birgðaútreikningur** til að virkja samstillingu birgða fyrir tiltekna Shopify birgðageymslu.

## Kynning: Byrjaðu að selja vörur á netinu

### Aðstæður

Segjum að þú viljir reyna Shopify að netverslun án þess að eyða miklum tíma í [!INCLUDE[prod_short](../includes/prod_short.md)] uppsetningu, sérstaklega vegna þess að þú ert þegar með vörurnar þínar rétt. Eftir að þú opnar netverslun þína Shopify færðu strax nýja viðskiptavini sem eru ánægðir með verslunina þína og kaup reynslu sína. Þeir ákveða því að gefa ráð við skoðun.

### Skref

Í [!INCLUDE[prod_short](../includes/prod_short.md)] skal fylgja eftirfarandi skrefum:

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Shopify Vörur** og velja viðeigandi tengja.
2. Valið er **Bæta við vörum**.
3. Fært er inn **í reitinn** Vinnusalarkóti `DEMO1`.
4. Afmörkunin `CHAIR` er stillt á reitinn **Vöruflokkskóti** .
5. Kveikja á **vísbendingu um samstillingu vörumynda** .
6. Kveikja á **vífæringu samstilltra birgða** .
7. Í lagi **er valið** og beðið þar til upphaflegri samstillingu vara, verðs, mynda og birgða er lokið.

Í netverslun: **Shopify**
> [!Tip]  
> Stjórnandi er opnaður **Shopify með því að fletta að veffanginu sem tilgreint er í** reitnum URL **á síðunni** Vinnusalarspjald **Shopify .**  Veldu augntáknið við hliðina á **sölurás Online Store**, sem staðsett er á hliðarstikunni í **Shopify Admin**. 

Vörulistinn er opnaður. Tilkynning:

* Afurðatitlar, myndir og verð.
* Til ráðstöfunar vísir (seldur út fyrir vörur á lager).

Velja skal hvaða vöru sem hægt er að selja– til dæmis `BERLIN Swivel Chair, yellow`. Takið eftir að lýsingin inniheldur vörueigindir.

Valið er **Kaupa það núna** og haldið áfram að útrita.

1. Í reitinn **Tölvupóstur eða farsímanúmer** skal slá inn `cl@contoso.com`  (eða tölvupóst þar sem þú vilt fá pöntun og afhendingu staðfestingar).
2. Í reitina Fornafn **og** Eftirnafn **er fært inn** . `Claudia Lawson`
3. Færa skal inn staðbundið aðsetur.
4. Velja skal gátreitinn **Vista þessar upplýsingar fyrir næsta skipti** .
6. Halda *stöðluðum* sem flutningsmáta.
8. Í reitinn **Númer kreditkorts er fært inn ef (til prófunar) Bogus Gateway**  er fært `1`  *inn eða fært inn* ef greiðslur eru notaðar `5555 5555 5555 4444`  *Shopify í prófunarstillingu* .
9. Fyllt er í reitinn **Heiti á spjaldi** .
10. Í reitinn **Fyrningardagsetning** er fært inn líðandi mánuður/ár.
11. Fært er inn **í** Öryggiskótann `111`.
7. Valfrjálst: Velja skal `10%` ábending.
8. 12. Valið er **Borgun núna**.

Í [!INCLUDE[prod_short](../includes/prod_short.md)] skal gera næstu skref:

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Shopify Pantanir** og velja síðan viðeigandi tengja.
2. Veljið aðgerðina **Samstilla pantanir frá Shopify** .
3. Valið er **Í lagi**.

Innflutt pöntun er tilbúin til vinnslu.

1. Valin er innflutt pöntun til að opna **Shopify gluggann Pöntun** .
2. Takið eftir að nýr viðskiptamaður og sölupantanir eru stofnaðar.
3. Skoða aðgerðirnar **Áhætta** og **Flutningskostnaður** .
4.  **Sölupöntun er valin** til að opna **gluggann Sölupöntun** . Sölupöntun er eftirspurn sem hægt er að ná yfir samsetningu, framleiðslu eða með því að kaupa með hjálp áætlunarvélarinnar. Hann styður einnig ýmsa meðhöndlunarferli vöruhúsa með fullkomnum aðskilnaði á skyldum.
6. Fært er inn **í reitinn** Umboðsmaður `DHL`. Enduropna pöntun ef þörf krefur með því að **velja Enduropna** aðgerð.
7. Í reitinn **Leitarnr.** sendingar er fært inn `123456789`.
8. Velja skal **Bóka**, halda kostinum **Afhenda og reikningsfæra** og velja **síðan Í lagi**.

Nú eru efnisleg og fjárhagsleg gögn skráð inn [!INCLUDE[prod_short](../includes/prod_short.md)]. Tímabært að láta vita Shopify um breytingarnar.

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teikn, færa inn **Samstilla afhendingar við Shopify** og velja viðeigandi tengja.
2. Valið er **Í lagi**.

Í **Shopify Stjórnanda** er bent á að pöntunin er merkt sem *Uppfyllt*. Einnig er hægt að skoða afhendingarupplýsingar og skoða rakningarslóðina þar. Ef samstilltar pantanir eru keyrðar **aftur Shopify** verður pöntunin geymd í báðum kerfum.

## Kynning: Bæta viðskiptamönnum við nýja netverslun

### Aðstæður

Eftir árangursríka gangsetningu á nýju netversluninni þinni, viltu að núverandi viðskiptavinir heimsækja hana og byrja að setja pantanir. Allt eftir Shopify áætlun og vinnslu er hægt að prófa B2B og DTC flæði.

### DTC-þrep

Eftirfarandi [!INCLUDE[prod_short](../includes/prod_short.md)] er gert í:

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **Shopify Viðskiptamenn** og velja viðeigandi tengja.
2. Velja skal **Bæta við viðskiptamönnum**.
3. Fært er inn **í reitinn** Vinnusalarkóti `DEMO1`.
4. Afmörkunin `20000` er stillt á reitinn **Nr.** .
5. Í lagi **er valið** og beðið þar til upphaflegri samstillingu viðskiptavina er lokið.

Í **Shopify Admin** er bent á að viðskiptavinurinn var fluttur inn. Viðskiptamennirnir eru opnaðir og takið eftir að fyrstu og eftirheiti viðskiptamannsins koma úr reitnum **Nafn** tengiliðar í spjaldi **viðskiptamanns**. Heiti fyrirtækisins má finna á sjálfgefnu aðsetri sem tengt er viðskiptamanninum. Ef hefðbundnir viðskiptamannareikningar eru notaðir *er* hægt að velja **Senda reikningaboð** til að bjóða viðskiptamanninum. Með *nýjum viðskiptavinareikningum* er lykilorð ekki krafist fyrir viðskiptamenn til að skrá sig inn, þess í stað Shopify gerir viðskiptavinum þínum kleift að skrá sig inn með 6 stafa sannprófunarkóða sem sendur er með tölvupósti. 

### B2B þrep

[!INCLUDE [shopify-preview](../includes/shopify-preview.md)]

Eftirfarandi [!INCLUDE[prod_short](../includes/prod_short.md)] er gert í:

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Shopify Fyrirtæki** og velja viðeigandi tengja.
2. Valið er **Bæta við fyrirtæki**.
3. Fært er inn **í reitinn Vinnusalarkóti.**  `DEMO1`
4. Afmörkunin `30000` er stillt á reitinn **Nr.** .
5. Í lagi **er valið** og beðið þar til upphaflegri samstillingu viðskiptavina er lokið.

Í **Shopify Admin** er bent á að bæði fyrirtækið og viðskiptamaðurinn voru flutt inn. Opnið viðskiptamennina og takið eftir staðreyndareitnum fyrirtæki með tengja fyrirtæki, staðsetningu og úthlutuðum heimildum. Velja **[...]** í staðreyndareitnum ** Fyrirtæki skal velja **síðan Senda B2B-aðgangspóst** til að bjóða viðskiptamanninum.

## Kynning: Fínjöfnun vörustjórnunar

### Aðstæður 

Notandi vill bæta við sveigjanleika og stjórna ferlinu í kringum stjórnun vara. Bæta á vörulýsingar og bæta við fleiri skrefum áður en vörur verða tiltækar öllum viðskiptavinum.

### Skref

Eftirfarandi [!INCLUDE[prod_short](../includes/prod_short.md)] er gert í:

Undirbúa gögn.

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **verðflokk viðskiptamanns** og velja viðeigandi tengja.
2. Nýjum verðflokki er bætt við. Fært er inn **í reitinn** Kóti `SHOPIFY`.
3.  **Glugganum Verðflokkur viðskiptamanna** er lokað.
4.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **Vörur** og velja viðeigandi tengja.
5. Vara *1896-S, Aþena skrifborð* er valin og eftirfarandi skrefum fylgt:

6. Veljið aðgerðina **Afbrigði** og bætið síðan við tveimur afbrigðum: `PREMIUM, Athens Desk, Premium edition` og `ESSENTIAL, Athens Desk, Essential edition`.
7. Veljið aðgerðina **Markaðssetningartexti** og notaðu **Uppkast með Copilot**  til að fá skapandi og þátttökutexta. Ef tillaga um markaðssetningartexta er ekki virk skal slá inn: '**Einfalt stílhrein hönnun** blandar saman við nokkurn ensemble. *Fáanlegt í tveimur útgáfum.*'. 
8. Aðgerðin **Söluverð er** valin og nýju verði bætt við eins og sýnt er í eftirfarandi töflu:

   |Línurit|Tegund sölu|Kóði sölu|Gerð|Kóði|Afbrigðiskóði<br>(reitnum bætt við með sérstillingu)|Einingarverð|
   |------|------------|------------|------------|----------------|------------|------------|
   |1|Verðflokkur viðskiptamanns|SHOPIFY|Atriði|1896-S|MIKILVÆGUR|700|
   |2|Verðflokkur viðskiptamanns|SHOPIFY|Atriði|1896-S|IÐGJALD|1000|

9. Velja skal aðgerðina **Söluafsláttur og bæta við nýjum afslætti** :

   * **Afsl.flokkur sölutegundar** *viðskm.*
   * **Smásölukóti** *SMÁSALa*
   * **Vara er slegin inn** *·*
   * **Kóti** *1896-S*
   * **Stk. mælieiningarkóta** *·*
   * **Línuafsláttur %** *10*

10. Veljið aðgerðina **Vörutilvísun** og eftirfarandi viðbótarlínur:

   |Línurit|Tegund tilvísunar|Tilvísunarnr.|Afbrigðiskóði|
   |------|------------|------------|------------|
   |1|Strikamerki|77777777|MIKILVÆGUR|
   |2|Strikamerki|11111111|IÐGJALD|

11. Velja skal vöruna *1920-S, ANTWERP Conference Table* og fylgja síðan eftirfarandi skrefum:
12. Valið er Leiðrétta birgðir **og í reitnum** Ný birgðir **er fært inn** fyrir birgðageymslurnar `100` Austur og *VESTUR* *.* 
13. Valið er **Í lagi**.

Stilla stillingar samstillingar.

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Shopify Verslanir** og velja viðeigandi tengja.
2.  `DEMO1` Velja skal verkstæðið sem á að samstilla vörur fyrir til að opna síðuna **Shopify Verkstæðisspjald** .
3. Reiturinn **Samstilla markaðssetningartexta** er virkjaður.
4. Vörunr.+ afbrigðiskóti er *valinn* í **vörpun**  reiti birgðahaldseiningar.
5. Valið er *Halda áfram* í reitnum **Sjálfgefin birgðaregla** .
6. Drög eru valin *í reitnum* Staða stofnaðra afurða **.** 
7. Staða er valin *í Geymd* í **aðgerð fyrir fjarlægðar vörur** .
8. Veljið *SHOPIFY* í reitnum **Verðflokkur viðskiptamanna** .
9. Veljið *RETAIL* í **svæðinu Afsláttarflokkur** viðskiptavinar.
 
Keyra samstillinguna.

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Shopify Verslanir** og velja viðeigandi tengja.
2.  `DEMO1` Velja skal verkstæðið sem á að samstilla vörur fyrir til að opna síðuna **Shopify Verkstæðisspjald** .
3. Vörur eru valdar **til** að opna **Shopify gluggann Vörur** .
4. Aðgerðin Bæta við vörum **er** valin.
5. Stilla afmörkunarTÖFLU *|SKRIFBORÐ* í reitnum **Vöruflokkskóti** .
6. Kveikja á **vísbendingu um samstillingu vörumynda** .
7. Kveikja á **vífæringu samstilltra birgða** .
8. Í lagi **er valið** og beðið þar til upphaflegri samstillingu vara, verðs, mynda og birgða er lokið.

Vörum er bætt við. Takið eftir að staðan er stillt á *Drög* og því eru vörur ekki sýnilegar í Shopify netversluninni.

1. Línan með vöru *1920-S, ANTWERP conference Table* er valin. Færið **inn** í SEO-titilinn `Rectangular meeting table Antwerp, 10 seats, black`.
2. Valið er *Virkt* í reitnum **Staða** .
3. Línan með vöru *1906-S, ATHENS, Mobile Stedestal* er valin og Eyða valið. **·**

Í **Shopify Admin** skal athuga að allar vörur hafa mismunandi stöðu.

* *ANTWERP ráðstefnutaflan* er *Virk* vegna þess að við breyttum stöðu hennar í **Shopify glugganum Vara** .
* *ATHENS skrifborð* er *Drög* vegna þess að við stilltum sjálfgefna stöðu fyrir allar viðbættar vörur sem á að vera *Drög*.
* *ATHENS Mobile Stedestal* er *geymt* vegna þess að við stilltum verkstæðið til að úthluta sjálfkrafa stöðu *í skjalasafn* fyrir eyddar vörur.

Takið eftir að Birgðir fyrir ANTWERP-ráðstefnutöfluna eru 100 því við grunnstilltum kerfið þannig að kerfið noti aðeins birgðir frá tveimur birgðageymslum, AÐAL- og Austurlandi. Birgðir í annarri birgðageymslu (WEST) eru hunsaðar.

* Opnið *ANTWERP-ráðstefnutöfluna*, takið eftir reitunum Sérsniðin **tegund**, **Lánardrottinn**, **Þyngd** og **Kostnaður á vöru** og **forútgáfa skráningu leitarvéla** .
* Skrifborð *Aþenu er opnað*, flett niður að hlutanum **Afbrigði** og bent á útfyllingu **birgðahaldseininga** .
* Velja Breyta **til** að fara yfir strikamerki og verð.
* Breyta stöðu *Aþenu-skrifborðs*  *í Virk* og velja **forútgáfa**.

Í netversluninni **Shopify** er vörulistinn opnaður og varan á ATHENS-skrifborðinu *fundin* . Takið eftir að mismunandi valkostir eru tiltækir. Verð eru mismunandi fyrir mismunandi valkosti. Veita afsláttarupplýsingar.

### Viðbótarskref fyrir B2B

[!INCLUDE [shopify-preview](../includes/shopify-preview.md)]

Hægt er að grunnstilla tengilinn til að stofna og úthluta vörulista fyrir útflutt fyrirtæki sjálfvirkt. Skrefin hér að neðan eru gagnleg ef óskað er eftir nákvæmari stjórn á því hvað er í boði fyrir viðskiptamenn B2B.

Í **Shopify Admin** ccreate og úthluta vörulista.

1. Vörur eru valdar **og** síðan **vörulistar** á hliðarstikunni í stjórnunarstikunni **Shopify**.
2. Búa til vörulista fyrir tilteknar vörur. Gefa í titilinn 'B2B'. 
3. Veldu **Stjórna** og stjórnaðu vörum **og verðlagningu**.
4. Velja skal *Útilokaða* afmörkun, finna *ATHERN-skrifborð* og velja **Taka með í vörulista**.
5. Viðskiptamenn eru valdir **og** síðan **Fyrirtæki á hliðarstikunni í stjórnunarstikunni**  **Shopify .**
6. Veldu *School of Fine Art* og veldu **[...]** og bæta síðan **við vörulistum** og bæta við *B2B-vörulista* sem stofnaður var fyrr.

Eftirfarandi [!INCLUDE[prod_short](../includes/prod_short.md)] er gert í:

Undirbúa gögn.

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **Vörur** og velja viðeigandi tengja.

2. Vara **1896-S, Aþena skrifborð** er valin og eftirfarandi skrefum fylgt:

3. Velja skal aðgerðina **Söluafsláttur og bæta við nýjum afslætti** :

   * **Afsl.flokkur sölutegundar** *viðskm.*
   * **Stóri kóti sölukóta** *·*
   * **Vara er slegin inn** *·*
   * **Kóti** *1896-S*
   * **Stk. mælieiningarkóta** *·*
   * **Línuafsláttur %** *25*

4.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Shopify vörulista** og velja viðeigandi tengja.
5. Velja skal **Sækja vörulista**.
6. Fært er inn **í reitinn** Vinnusalarkóti `DEMO1`.
7. Velja skal færslu með heitinu *B2B-vörulisti* sem samstilla á verð fyrir.
8.  **Gera vífæringu á samstilltu verði** virka.
9. Veljið *SHOPIFY* í reitnum **Verðflokkur viðskiptamanna** .
10. Stór reikn. er valið *í reitnum* Afsláttarflokkur viðskiptamanns **.** 
11. Velja skal **Samstilla** verð og bíða þar til samstillingu verðs er lokið.

Í **Shopify Admin** skal skoða verð fyrir *B2B-vörulista* .

Í netversluninni **Shopify** er vörulistinn opnaður og varan á ATHENS-skrifborðinu *fundin* . Athugasemdaverð eru upplýsingar um afslátt.

## Kynning: Skoða og panta samstillingu fyrir einstaka kaupanda og fulltrúa fyrirtækisins
Þetta er framhald kynningarinnar [: Byrjaðu að selja vörur á netinu](walkthrough-setting-up-and-using-shopify.md#walkthrough-start-selling-products-online). Einnig er hægt að reyna með eigin gögnum – til dæmis í verslun eða Shopify sandkassa.

Einstakur kaupandi

1.  **Shopify Í netversluninni**. Velja **reikningstákn** . Sláðu inn tölvupóst sem þú hefur aðgang að.
2. Skráðu þig inn með því að nota 6 stafa sannprófunarkóða sem sendur var með tölvupósti sem þú færðir inn.
3. Skoða vörulista ætti að vera hægt að sjá allar vörur með smásöluverði.
4. Veljið nauðsynlegt afbrigði og veljið **Kaupa það núna** og haldið áfram að útrita.
5. Fyllt er í reitina **Fornafn** og **Eftirnafn** .
6. Færa skal inn staðbundið aðsetur.
7. Halda *stöðluðum* sem flutningsmáta.
8. Í reitinn **Númer** kreditkorts er fært inn `1` ef notað *er (til prófunar) Bogus Gateway* eða fært inn `5555 5555 5555 4444` ef greiðslur eru notaðar *Shopify* í prófunarstillingu.
9. Í reitinn **Fyrningardagsetning** er fært inn líðandi mánuður/ár.
10. Fært er inn **í** Öryggiskótann `111`.
11. Fyllt er í reitinn **Heiti á spjaldi** .
12. Valið er **Borgun núna**.
 
Fulltrúi fyrirtækis

[!INCLUDE [shopify-preview](../includes/shopify-preview.md)]

1. Í **Shopify Stjórnunarklasa**
2. Viðskiptamenn eru valdir **og** síðan **Fyrirtæki á hliðarstikunni í stjórnunarstikunni**  **Shopify .**
3. Opnunarskóli *fínnar listafærslu* .
4. Velja **[...]** í staðreyndareitnum **Skóla fínnar listar** og svo **Breyta greiðsluskilmálum** og velja *Gjaldfallið að uppfylltum*.
5. Velja **[...]** í staðreyndareitnum **viðskiptamenn** og bæta svo **við viðskiptavini** og bæta við einum með tölvupósti sem þú skráðir þig inn í verslunina áðan.
6.  **Shopify Í netversluninni**. Velja **reikningstákn** . Sláðu inn tölvupóst sem þú hefur aðgang að.
7. Skráðu þig inn með því að nota 6 stafa sannprófunarkóða sem sendur var með tölvupósti sem þú færðir inn.
8. Skoða vörulista ætti að vera hægt að sjá aðeins vöru sem bætt er *við B2B-vörulistann* með sérstöku verði í smásölu.
9. Veljið nauðsynlegt afbrigði og veljið **Kaupa það núna** og haldið áfram að útrita.
10. Takið eftir að reikningur, Afhenda, greiðsluháttur er útfylltur.
11. Reiturinn Innkaupapöntunarnúmer **er** fylltur út með `PO-12345`.
12. Veljið **Senda pöntun**.
 
Í [!INCLUDE[prod_short](../includes/prod_short.md)] skal gera næstu skref:

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Shopify Pantanir** og velja síðan viðeigandi tengja.
2. Veljið aðgerðina **Samstilla pantanir frá Shopify** .
3. Valið er **Í lagi**.

Innflutt pöntun er tilbúin til vinnslu.

1. Valin er innflutt pöntun til að opna **Shopify gluggann Pöntun** .
2. Bent er á að báðar pantanirnar voru sendar inn af sama einstaklingi og þær tengjast tveimur mismunandi viðskiptamönnum. 
3. Í pöntuninni sem lögð er fram fyrir hönd fyrirtækis er hægt að **sjá gildi í** reitnum Númer **innkaupapöntunar sem einnig er flutt í númer utanaðkomandi skjals.** reitur stofnaðs söluskjals.
4. Vegna þess að við grunnstilltum B2B Fyrirtæki til að sjá um Shopify  **greiðslur utan fjárhagsstöðu** er stillt á *Í undirbúningi*. Þegar greiðslan hefur borist skal velja **Mark sem greidda** aðgerð. Fjárhagsstaðan verður uppfærð í Shopify. 

## Kynning: Flytja inn vörur, viðskiptamenn, fyrirtæki frá Shopify

### Aðstæður 

Netverslun hefur þegar heppnast og ætlunin er að byrja að nota [!INCLUDE[prod_short](../includes/prod_short.md)] viðskiptastjórnunarhugbúnað. Flytja á inn eins mikið af gögnum og Shopify mögulegt er. 

### Skref

Þetta er framhald kynningarinnar [: Byrjaðu að selja vörur á netinu](walkthrough-setting-up-and-using-shopify.md#walkthrough-start-selling-products-online) og [Kynning: Bættu viðskiptavinum þínum við nýju netverslunina](walkthrough-setting-up-and-using-shopify.md#walkthrough-add-your-customers-to-your-new-online-store) þína. Einnig er hægt að reyna með eigin gögnum – til dæmis í verslun eða Shopify sandkassa.

Í [!INCLUDE[prod_short](../includes/prod_short.md)] skal fylgja skrefunum sem skráð eru næst.

#### Undirbúa gögn

1. Skipta yfir í ókeypis 30 daga prufu án sýnigagna. Nánari upplýsingar eru [í Bæta eigin gögnum við tóma réttarhöld](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions#add-your-own-data-to-an-empty-trial-company).
2.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Shopify Verslanir** og velja síðan viðeigandi tengja.
3. Valið er **Nýtt**.
4. Fært er inn **í reitinn** Kóti `DEMO2`.
5. Í reitinn **Shopify URL er URL** fært inn í vefverslunina sem á að tengjast.
6. Virkja virkt **vífæra** og fara yfir og samþykkja skilmála og skilyrði.

Grunnstilla verkstæðið Shopify eins og lýst er hér:

1. Gera vífæringu á Leyfa samstillingu bakgrunns **óvirka** .
2. Valið er *Frá Shopify* í reitnum **Samstilla vöru** .
3. Gera vífærslu á **óþekktum vörum** virka sjálfvirkt.
4. Viðeigandi sniðmát er fært í reitinn **Kóti** vörusniðmáts.
5. Valið *er Frá Shopify* í reitnum **Samstilla vörumyndir** .
6. Vörunr.+ afbrigðiskóti er *valinn* í **vörpun**  reiti birgðahaldseiningar.
7. Allir viðskiptamenn *í innflutningi* viðskiptamanns eru valdir **úr Shopify**.
8.  **Gera vífæringu á Sjálfvirk stofnun óþekktra viðskiptamanna** virka.
9. Viðeigandi sniðmát er fært í reitinn **Sniðmát** viðskiptamanns/fyrirtækis.
10. Allir viðskiptamenn *í* fyrirtækjainnflutningi eru valdir **úr Shopify**.
11.  **Gera vífæringu fyrirtækja sjálfvirkt stofnað óþekkt fyrirtæki** .

#### Keyra samstillingu

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Shopify Verslanir** og velja viðeigandi tengja.
2.  *Velja skal DEMO2-verkstæðið* sem samstilla á gögn fyrir til að opna **Shopify síðuna Verkstæðisspjald** .
3. Samstilla vörur er **valið**.
4. Velja **Samstilla vörumyndir**.
5. Samstilla viðskiptamenn er **valið**.
6. Velja **Samstilla fyrirtæki**

### Niðurstöður

* Shopify Vörur eru fluttar inn. Til að staðfesta skal velja Ljósálgina ![sem opnar Tell Me eiginleikann.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Shopify Vörur** og velja viðeigandi tengja.
* Vörur með myndum eru búnar til. Til að staðfesta skal velja Ljósálgina ![sem opnar Tell Me eiginleikann.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **Vöru** og velja viðeigandi tengja.
* Shopify Viðskiptamenn eru fluttir inn. Til að staðfesta skal velja Ljósálgina ![sem opnar Tell Me eiginleikann.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **Shopify Viðskiptamenn** og velja viðeigandi tengja.
* Shopify Fyrirtæki eru flutt inn. Til að staðfesta skal velja Ljósálgina ![sem opnar Tell Me eiginleikann.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Shopify Fyrirtæki** og velja viðeigandi tengja.
* Viðskiptamenn eru stofnaðir. Til að staðfesta skal velja Ljósálgina ![sem opnar Tell Me eiginleikann.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **Viðskiptamenn** og velja viðeigandi tengja.


## Sjá einnig .

[Hafist handa í tengilinu Shopify](get-started.md)  
