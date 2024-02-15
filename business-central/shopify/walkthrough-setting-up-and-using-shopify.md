---
title: Setja upp og nota Shopify Connector
description: Ýmsar samþættingaraðstæður til að sýna vinnuflæði milli Shopify og Business Central
ms.date: 06/21/2022
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '30101, 30102, 30106, 30107, 30113, 30115, 30126'
ms.reviewer: solsen
author: brentholtorf
ms.author: bholtorf
---

# <a name="walkthrough-set-up-and-use-the-shopify-connector"></a>Kynning: Uppsetning og notkun Shopify Connector

Þessi hluti sýnir nokkur dæmigerð atburðarás og tekur notandann í gegnum skrefin til að prófa eða þjálfa notendur á vinnuflæði samþættra [!INCLUDE[prod_short](../includes/prod_short.md)] og verslunarinnar Shopify .

## <a name="prerequisites"></a>Frumskilyrði

### <a name="shopify"></a>Shopify

Þú verður að vera með:

- Reikningur Shopify 
- Netverslun Shopify 

Fræðast meira um hvernig á að búa til Shopify prufur og ráðlagðar stillingar í [Stofna og setja upp Shopify reikning](shopify-account.md).

### <a name="business-central"></a>Business Central

Þú verður að vera með [!INCLUDE[prod_short](../includes/prod_short.md)] reikning. 

Til dæmis er hægt að búa til prufureikning eða hefja prufu. Nánari upplýsingar um [útbúa sýningaumhverfi og Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/administration/demo-environment)  [skráðu þig fyrir réttarhöldunum](../trial-signup.md). 

## <a name="connect-business-central-to-the-shopify-shop"></a>Tengja Business Central við verkstæðið Shopify

Eftirfarandi [!INCLUDE[prod_short](../includes/prod_short.md)] er gert í:

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Shopify Verslanir** og velja síðan viðeigandi tengil.
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
8. Viðeigandi sniðmát er fært í reitinn **Kóti** viðskiptamannssniðmáts.
9.  **Fylla út reikning afhendingarkostnaðar**, **ábendingarreikningur** með tekjureikningnum. Til dæmis í Bandaríkjunum, notkun `40210`.
10. Kveikja á víflipinu **Stofna pantanir** sjálfvirkt.

Grunnstilla birgðageymsluvörpun:

1. Veljið aðgerðina **Birgðageymslur** til að opna **Shopify Birgðageymslur verkstæðis**.
2. Velja skal aðgerðina **Sækja Shopify birgðageymslur** til að flytja inn allar birgðageymslur sem skilgreindar eru í skjámyndinni Shopify. Sjálfgefin birgðageymsla er valin í Shopify.
3. Fært er inn **í** Birgðageymsluafmörkun `''|EAST|MAIN`.
4. Kveikja á sjálfgefnu **vífæribreytu vörustaðsetningar** .
5. Valið er *Áætluð staða til ráðstöfunar í dag* í reitnum **Birgðaútreikningur** til að virkja samstillingu birgða fyrir tiltekna Shopify birgðageymslu.

## <a name="walkthrough-start-selling-products-online"></a>Kynning: Byrjaðu að selja vörur á netinu

### <a name="scenario"></a>Aðstæður

Segjum að þú viljir reyna Shopify að netverslun án þess að eyða miklum tíma í [!INCLUDE[prod_short](../includes/prod_short.md)] uppsetningu, sérstaklega vegna þess að þú ert þegar með vörurnar þínar rétt. Eftir að þú opnar netverslun þína Shopify færðu strax nýja viðskiptavini sem eru ánægðir með verslunina þína og kaup reynslu sína. Þeir ákveða því að gefa ráð við skoðun.

### <a name="steps"></a>Skref

Í [!INCLUDE[prod_short](../includes/prod_short.md)] skal fylgja eftirfarandi skrefum:

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Shopify Vörur** og velja viðeigandi tengil.
2. Valið er **Bæta við vörum**.
3. Í reitinn **Vinnusalarkóti** er demo1 *slegið inn*.
4. Afmörkunin `CHAIR` er stillt á reitinn **Kóti** vöruflokks (bæta við afmörkunarreit ef þörf krefur).
5. Í lagi **er valið** og beðið þar til upphafssamstillingu á vörum og verði er lokið.
6. Velja **Samstilla vörumyndir**.
7. Samstilla birgðir **valdar**.

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
5. Valið er **Halda áfram í afhendingu**.
6. Halda skal `Standard` sem flutningsmáta og velja svo hnappinn **Halda áfram að greiðslu** .
7. Velja ábending `10%` .
8. Í reitinn **Kreditspjald** er fært inn ef (til prófunar) Bogus Gateway `1`  er fært *inn* eða fært inn `5555 5555 5555 4444` ef greiðslur eru notaðar *Shopify* í prófunarstillingu.
9. Fyllt er í reitinn **Heiti á spjaldi** .
10. Í reitinn **Fyrningardagsetning** er fært inn líðandi mánuður/ár.
11. Fært er inn **í** Öryggiskótann `111`.
12. Valið er **Borgun núna**.

Í [!INCLUDE[prod_short](../includes/prod_short.md)] skal gera næstu skref:

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Shopify Pantanir** og velja síðan viðeigandi tengil.
2. Veljið aðgerðina **Samstilla pantanir frá Shopify** .
3. Valið er **Í lagi**.

Innflutt pöntun er tilbúin til vinnslu.

1. Valin er innflutt pöntun til að opna **Shopify gluggann Pöntun** .
2. Takið eftir að nýr viðskiptamaður og sölupantanir eru stofnaðar.
3. Skoða aðgerðirnar **Áhætta** og **Flutningskostnaður** .
4.  **Sölupöntun er valin** til að opna **gluggann Sölupöntun** . Sölupöntun er eftirspurn sem hægt er að ná yfir samsetningu, framleiðslu eða með því að kaupa með hjálp áætlunarvélarinnar. Hann styður einnig ýmsa meðhöndlunarferli vöruhúsa með fullkomnum aðskilnaði á skyldum.
5. Veljið aðgerðina **Enduropna** .
6. Fært er inn **í reitinn** Umboðsmaður `DHL`.
7. Í reitinn **Leitarnr.** sendingar er fært inn `123456789`.
8. Velja skal **Bóka**, halda kostinum **Afhenda og reikningsfæra** og velja **síðan Í lagi**.

Nú eru efnisleg og fjárhagsleg gögn skráð inn [!INCLUDE[prod_short](../includes/prod_short.md)]. Tímabært að láta vita Shopify um breytingarnar.

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Samstilla afhendingar við Shopify** og velja viðeigandi tengil.
2. Valið er **Í lagi**.

Í **Shopify Stjórnanda** er bent á að pöntunin er merkt sem *Uppfyllt*. Einnig er hægt að skoða afhendingarupplýsingar og skoða rakningarslóðina þar. Ef samstilltar pantanir eru keyrðar **aftur Shopify** verður pöntunin geymd í báðum kerfum.

## <a name="walkthrough-invite-your-customers-to-your-new-online-store"></a>Kynning: Bjóddu viðskiptavinum þínum í nýju netverslunina þína

### <a name="scenario-1"></a>Aðstæður

Eftir árangursríka gangsetningu á nýju netversluninni þinni, viltu að núverandi viðskiptavinir heimsækja hana og byrja að setja pantanir.

### <a name="steps-1"></a>Skref

Eftirfarandi [!INCLUDE[prod_short](../includes/prod_short.md)] er gert í:

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Shopify Verslanir** og velja viðeigandi tengil.
2.  **Velja skal DEMO1-verkstæðið** sem á að samstilla viðskiptamenn við til að opna **Shopify síðuna Verkstæðisspjald** .
3. Samstilla viðskiptamenn **er valið**.

Í **Shopify Admin** er bent á að viðskiptamennirnir voru fluttir inn. Opna skal einn af viðskiptamönnum og takið eftir að fyrstu og eftirnafn viðskiptamannsins koma úr reitnum **Heiti** tengiliðar í spjaldi **viðskiptamanns**. Heiti fyrirtækisins má finna á sjálfgefnu aðsetri sem tengt er viðskiptamanninum. Velja skal **Senda reikningaboð** til að bjóða viðskiptavininum.

## <a name="walkthrough-fine-tuning-of-item-management"></a>Kynning: Fínjöfnun vörustjórnunar

### <a name="scenario-2"></a>Aðstæður

Notandi vill bæta við sveigjanleika og stjórna ferlinu í kringum stjórnun vara. Bæta á vörulýsingar og bæta við fleiri skrefum áður en vörur verða tiltækar viðskiptavinum.

### <a name="steps-2"></a>Skref

Eftirfarandi [!INCLUDE[prod_short](../includes/prod_short.md)] er gert í:

Undirbúa gögn.

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **verðflokk viðskiptamanns** og velja viðeigandi tengil.
2. Nýjum verðflokki er bætt við. Fært er inn **í reitinn** Kóti `SHOPIFY`.
3.  **Glugganum Verðflokkur viðskiptamanna** er lokað.
4.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **Vörur** og velja viðeigandi tengil.

Vara **1896-S, Aþena skrifborð** er valin og eftirfarandi skrefum fylgt:

1. Veljið aðgerðina **Afbrigði** og bætið síðan við tveimur afbrigðum: `PREMIUM, Athens Desk, Premium edition` og `ESSENTIAL, Athens Desk, Essential edition`.
2. Velja skal aðgerðina **Lengdur texti** og stofna síðan nýjan lengdan texta sem gildir fyrir alla tungumálakóta. Fært er inn **í reitinn** Lýsing `Shopify`. 
3. Eftirfarandi texta er bætt við með HTML-merkjum: `<b>Simple stylish design</b> blends with any ensemble. <i>Available in two editions.</i>`. Loka síðunni **Lengdur texti** og fara aftur í birgðaspjaldið.
4. Aðgerðin **Söluverð er** valin og nýju verði bætt við eins og sýnt er í eftirfarandi töflu:

   |Línurit|Tegund sölu|Kóti sölu|Gerð|Kóði|Afbrigðiskóði<br>(reitnum bætt við með sérstillingu)|Einingarverð|
   |------|------------|------------|------------|------------|------------|------------|
   |1|Verðflokkur viðskiptamanns|SHOPIFY|Atriði|1896-S|NAUÐSYNLEGT|700|
   |2|Verðflokkur viðskiptamanns|SHOPIFY|Atriði|1896-S|AUKAGJALD|1000|

5. Velja skal aðgerðina **Söluafsláttur og bæta við nýjum afslætti** :

   * **Afsl.flokkur sölutegundar** *viðskm.*
   * **Smásölukóti** *SMÁSALa*
   * **Vara er slegin inn** *·*
   * **Kóti** *1896-S*
   * **Stk. mælieiningarkóta** *·*
   * **Línuafsláttur %** *10*

6. Veljið aðgerðina **Vörutilvísun** og eftirfarandi viðbótarlínur:

   |Línurit|Tegund tilvísunar|Tilvísunarnr.|Afbrigðiskóði|
   |------|------------|------------|------------|
   |1|Strikamerki|77777777|NAUÐSYNLEGT|
   |2|Strikamerki|11111111|AUKAGJALD|


Velja skal vöruna **1920-S, ANTWERP Conference Table** og fylgja síðan eftirfarandi skrefum:

1. Valið er Leiðrétta birgðir **og í reitnum** Ný birgðir **er fært inn** fyrir birgðageymslurnar `100` Austur og *VESTUR* *.* 
2. Valið er **Í lagi**.

Stilla stillingar samstillingar.

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Shopify Verslanir** og velja viðeigandi tengil.
2.  *Velja skal deMO1-verkstæðið* sem á að samstilla vörur fyrir til að opna **Shopify síðuna Verkstæðisspjald** .
3. Veljið *SHOPIFY* í reitnum **Verðflokkur viðskiptamanna** .
4. Veljið *RETAIL* í **svæðinu Afsláttarflokkur** viðskiptavinar.
5. Gera reitinn **Samstilla vöru lengdan texta** virkan.
6. Vörunr.+ afbrigðiskóti er *valinn* í reitnum **Birgðahaldseiningarvörpun** .
7. Drög eru valin *í reitnum* Staða stofnaðra afurða **.** 
8. Staða er valin *í Geymd* í **aðgerð fyrir fjarlægðar vörur** .

Keyra samstillinguna.

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Shopify Verslanir** og velja viðeigandi tengil.
2.  *Velja skal deMO1-verkstæðið* sem á að samstilla vörur fyrir til að opna **Shopify síðuna Verkstæðisspjald** .
3. Vörur eru valdar **til** að opna **Shopify gluggann Vörur** .
4. Aðgerðin Bæta við vörum **er** valin.
5. Stilla afmörkunarTÖFLU *|SKRIFBORÐ* í reitnum **Vöruflokkskóti** .
6. Velja **Samstilla vörumyndir**.
7. Samstilla birgðir **valdar**.

Vörum er bætt við. Takið eftir að staðan er stillt á *Drög* og því eru vörur ekki sýnilegar í Shopify netversluninni.

1. Línan með vöru *1920-S, ANTWERP conference Table* er valin. Færið **inn** í SEO-titilinn `Rectangular meeting table Antwerp, 10 seats, black`.
2. Valið er *Virkt* í reitnum **Staða** .
3. Línan með vöru *1906-S, ATHENS, Mobile Stedestal* er valin og Eyða valið. **·**

Í **Shopify Admin** skal athuga að allar vörur hafa mismunandi stöðu.

* *ANTWERP ráðstefnutaflan* er *Virk* vegna þess að við breyttum stöðu hennar í **Shopify glugganum Vara** .
* *ATHENS skrifborð* er Drög *vegna þess að við stilltum sjálfgefna stöðu fyrir allar viðbættar vörur sem á að vera* Drög *·*.
* *ATHENS Mobile Stedestal* er *geymt* vegna þess að við stilltum verkstæðið til að úthluta sjálfkrafa stöðu *í skjalasafn* fyrir eyddar vörur.

Takið eftir að Birgðir fyrir ANTWERP-ráðstefnutöfluna eru 100 því við grunnstilltum kerfið þannig að kerfið noti aðeins birgðir frá tveimur birgðageymslum, AÐAL- og Austurlandi. Birgðir í annarri birgðageymslu (WEST) eru hunsaðar.

* Glugginn ANTWERP-ráðstefnutafla *er opnaður*, sérsniðin **tegund**, **lánardrottinn**, **þyngd** og **Kostnaður á hverja vöru** og forskoðunarhluti **fyrir** lista yfir leitarvélar.
* Skrifborð *Aþenu er opnað*, flett niður að hlutanum **Afbrigði** og bent á útfyllingu **birgðahaldseininga** .
* Velja Breyta **til** að fara yfir strikamerki og verð.
* Breyta stöðu *Aþenu-skrifborðs* í *Virk* og velja **Forskoðun**.

Í netversluninni **Shopify** er vörulistinn opnaður og varan á ATHENS-skrifborðinu *fundin* . Takið eftir að mismunandi valkostir eru tiltækir. Verð eru mismunandi fyrir mismunandi valkosti. Veita afsláttarupplýsingar.

## <a name="walkthrough-import-items-from-shopify"></a>Kynning: Flytja inn vörur úr Shopify

### <a name="scenario-3"></a>Aðstæður

Netverslun hefur þegar heppnast og ætlunin er að byrja að nota [!INCLUDE[prod_short](../includes/prod_short.md)] viðskiptastjórnunarhugbúnað. Flytja á inn eins mikið af gögnum og Shopify mögulegt er. 

### <a name="steps-3"></a>Skref

Þetta er framhald kynningarinnar [: Byrjaðu að selja vörur á netinu](walkthrough-setting-up-and-using-shopify.md#walkthrough-start-selling-products-online). Einnig er hægt að reyna með eigin gögnum – til dæmis í verslun eða Shopify sandkassa.

Í [!INCLUDE[prod_short](../includes/prod_short.md)] skal fylgja skrefunum sem skráð eru næst.

#### <a name="prepare-data"></a>Undirbúa gögn

1. Skipta yfir í ókeypis 30 daga prufu án sýnigagna. Nánari upplýsingar eru [í Bæta eigin gögnum við tóma réttarhöld](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions#add-your-own-data-to-an-empty-trial-company).
2.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Shopify Verslanir** og velja síðan viðeigandi tengil.
3. Valið er **Nýtt**.
4. Fært er inn **í reitinn** Kóti `DEMO2`.
5. Í reitinn **Shopify URL er URL** fært inn í vefverslunina sem á að tengjast.
6. Virkja virkt **vífæra** og fara yfir og samþykkja skilmála og skilyrði.

Grunnstilla verkstæðið Shopify eins og lýst er hér:

1. Gera vífæringu á Leyfa samstillingu bakgrunns **óvirka** .
1. Valið er *Frá Shopify* í reitnum **Samstilla vöru** .
1. Gera vífærslu á **óþekktum vörum** virka sjálfvirkt.
1. Viðeigandi sniðmát er fært í reitinn **Kóti** vörusniðmáts.
1. Valið *er Frá Shopify* í reitnum **Samstilla vörumyndir** .
1. Allir viðskiptamenn *í innflutningi* viðskiptamanns eru valdir **úr Shopify**.
1.  **Gera vífæringu á Sjálfvirk stofnun óþekktra viðskiptamanna** virka.

#### <a name="run-the-synchronization"></a>Keyra samstillingu

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Shopify Verslanir** og velja viðeigandi tengil.
2.  *Velja skal DEMO2-verkstæðið* sem samstilla á gögn fyrir til að opna **Shopify síðuna Verkstæðisspjald** .
3. Samstilla vörur er **valið**.
4. Velja **Samstilla vörumyndir**.
5. Samstilla viðskiptamenn er **valið**.

### <a name="results"></a>Niðurstöður

* Shopify Vörur eru fluttar inn. Til að staðfesta skal velja Ljósálgina ![sem opnar Tell Me eiginleikann.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Shopify Vörur** og velja viðeigandi tengil.
* Vörur með myndum eru búnar til. Til að staðfesta skal velja Ljósálgina ![sem opnar Tell Me eiginleikann.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **Vöru** og velja viðeigandi tengil.
* Shopify Viðskiptamenn eru fluttir inn. Til að staðfesta skal velja Ljósálgina ![sem opnar Tell Me eiginleikann.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **Shopify viðskiptamenn** og velja viðeigandi tengil.
* Viðskiptamenn eru stofnaðir. Til að staðfesta skal velja Ljósálgina ![sem opnar Tell Me eiginleikann.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **viðskiptamenn** og velja viðeigandi tengil.


## <a name="see-also"></a>Sjá einnig .

[Hafist handa í tengilinu Shopify](get-started.md)  
