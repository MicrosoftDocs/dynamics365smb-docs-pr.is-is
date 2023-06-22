---
title: Setja upp og nota  Shopify  tengibúnað
description: Ýmsar samþættingaráætlanir fyrir Sýna verkflæði á milli  Shopify  og rekstur seðla-
ms.date: 06/21/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30101, 30102, 30106, 30107, 30113, 30115, 30126'
ms.reviewer: solsen
author: AndreiPanko
ms.author: andreipa
---

# <a name="walkthrough-set-up-and-use-the-shopify-connector" />Walkthrough: setja upp og nota  Shopify  tengibúnað

Þessi hluti sýnir nokkrar dæmigerðar aðstæður og tekur þú í gegnum skrefin til að prófa eða þjálfa notendur í verkflæði samþættingar  [!INCLUDE[prod_short](../includes/prod_short.md)]  og  Shopify  verslunar.

## <a name="prerequisites" />Frumskilyrði

### <a name="shopify" />Shopify

Þú verður að vera með:

- Á  Shopify  reikning
- Í  Shopify  netverslun

Frekari upplýsingar um hvernig á að stofna  Shopify  rannsóknir og ráðlagðar stillingar við  [stofnun og uppsetningu  Shopify  lykils](shopify-account.md).

### <a name="business-central" />Business Central

Það þarf að vera  [!INCLUDE[prod_short](../includes/prod_short.md)]  með lykil. 

Til dæmis er hægt að stofna prufureikning eða hefja réttarhöld. Lærðu meira á  [að undirbúa Sýnisumhverfi af  Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/administration/demo-environment)  og  [skrá sig til prufu](../trial-signup.md). 

## <a name="connect-business-central-to-the-shopify-shop" />Tengja Viðskiptamiðað  Shopify  við verkstæðið

Í  [!INCLUDE[prod_short](../includes/prod_short.md)], gerið eftirfarandi skref:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn  **Shopify  verslanir** og veljið síðan tengda tengilinn.
2. Valið er aðgerðin **Nýtt**.
3.  **Í reitnum kóti**  er fært inn `DEMO1`.
4.  **Shopify Í reitinn URL**  er rituð slóðin að vefversluninni sem á að tengjast.
5.  **Virkjaðu virkjunina**  skipta, Skoðaðu og samþykktu skilmálana.

 Shopify Samskipa versluninni eins og lýst er í eftirfarandi skrefum:

1. Kveikja á  **kladdavirkjanum**  skipta.
2. Slökkva á  **samsetlun**  Allow bakgrunns.
3. Veljið  **til að  Shopify**  **keyra svæðið sync-vara** .
4. Valið er að velja  **í svæðinu samkeyrsluvöru  Shopify**  .  **·** 
5. Kveikja skal  **á eigindum**  Samkeyrandi vara.
6. Kveikja á birgðum sem  **rekja**  á víxlun.
7. Velja  **skal hafna**  í  **sjálfgefinni birgðastefnu** .
8. Kveikja á  **Auto Create Óþekkt Viðskiptamódel**  skipta.
9.  **Reiturinn sniðmát**  viðskiptamanns er fylltur út með viðeigandi sniðmáti.
10. Fylltur er út reikningur  **fyrir** sendingarkostnaði,  **ábendinguna**  með tekjumlykli. T.d. í Bandaríkjunum, use `40100`.
11. Kveikja á  **Sjálfvirk stofna pantanir**  skipta.

Samskipa vörpun staðsetningarlagningar:

1. Veljið aðgerðina **Staðsetningar** til að opna **Shopify Staðsetningar verslunar**.
2.  **Velja aðgerðina Sækja  Shopify  staðsetningar**  til að flytja inn alla staði sem skilgreindir eru  Shopify í.
3.  **Í Birgðageymsluafmörkuninni** er fært inn `''|EAST|MAIN`.
4. Slökkva á  **óvirka**  skipta til að virkja samstillingu birgða fyrir valda  Shopify  staðsetningu.

## <a name="walkthrough-start-selling-products-online" />Walkthrough: Byrjaðu að selja vörur á netinu

### <a name="scenario" />Aðstæður

Segjum sem svo að þú viljir reyna  Shopify  við netverslun án þess að eyða miklum tíma í að setja upp hluti, sérstaklega vegna þess að þú ert þegar að viðhalda vörunum þínum á  [!INCLUDE[prod_short](../includes/prod_short.md)]  réttan hátt. Eftir að þú hefur ræst  Shopify  vefverslunina færðu strax nýja viðskiptavini sem eru ánægðir með verkstæðin og þeirra kaupreynslu. Geta þeir þá ákveðið að fara eftir ábendingum hjá afgreiðslufólk.

### <a name="steps" />Skref

Í  [!INCLUDE[prod_short](../includes/prod_short.md)]  farið í gegnum eftirtalda liði:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Shopify Vörur** og veldu viðeigandi tengil.
2. Velja aðgerðina **Bæta við atriðum**.
3.  **Í reitnum verkstæðiskóti**  er fært inn  *DEMO1*.
4. Stillið afmörkunina  `CHAIR`  á  **reitinn tegundarkóti**  vöru (bæta við afmörkun ef þarf).
5. Veldu  **í lagi**  og Bíddu þar til fyrstu samstillingu vara og verðs er lokið.
6. Veldu aðgerðina **Samstilla myndir af vörum**.
7.  **Veljið Samstillingarbirgðaaðgerðina** .

Í  **Shopify  netverslun**
> [!Tip]  
> Opna  **Shopify  admin**, með því að FLETTA að vefslóð sem tilgreind er í  **reitnum URL**  á  **Shopify  síðu vinnukorts** . Þá er valið augsteikn við  **hlið sölurásar Vefverslunarinnar**, sem er staðsett í hliðarstikunni  **Shopify  admin**. 

Opnið vörulista. Fyrirvara

* Titlar vara, mynda og verðs.
* Ráðstöfunar-vísir (selt út fyrir vörur á lager).

Veldu hvaða afurð er hægt að selja, til dæmis `BERLIN Swivel Chair, yellow`. Takið eftir að lýsingin inniheldur vörueigindir.

 **Veldu að kaupa það núna**  hnappinn og Haltu áfram að útskrá.

1.  **Í reitinn email eða farsímanúmer**  er fært inn  `cl@contoso.com`  (eða tölvupóstur þar sem taka á á móti pöntunar-og sendingarstaðfestingum).
2.  **Í skírnarnafni**  og  **eftirnafni**, Enter `Claudia Lawson`.
3. Færa inn staðbundið aðsetur.
4. Velja að  **vista þessar upplýsingar fyrir gátreitinn næsta tíma** .
5. Velja skal  **hnappinn halda áfram** .
6. Haltu  `Standard`  eins sendingarmáta og veldu  **síðan continue til greiðsluhnappi** .
7. Velja  `10%`  Tip.
8.  **Í reitinn kreditkort**  er fært inn  `1`  Ef notað  *er (fyrir prófun) Bogus gátt* eða  `5555 5555 5555 4444`  ef greiðslur  *Shopify  eru notaðar*  í prófunarham.
9. Reiturinn heiti á spjaldi  **er**  fylltur út.
10.  **Í reitinn Lokadagsetning**  er færður inn gildandi mánuður/ár.
11.  **Færið inn** í öryggiskótann `111`.
12.  **Veldu hnappinn laun núna** .

Í  [!INCLUDE[prod_short](../includes/prod_short.md)], gerið næstu skrefum:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn  **Shopify  pantanir** og veljið síðan tengda tengilinn.
2. Veldu aðgerðina **Samstilla pantanir frá Shopify**.
3. Velja **Í lagi**.

Innflutt pöntun er tilbúin til vinnslu.

1. Veljið innflutti pöntunina til að opna  **Shopify  pöntunargluggann** .
2. Tilkynning um að nýr viðskiptamaður og sölupöntun verði stofnuð.
3.  **Kanna áhættu**  -og  **sendingarkostnaðaraðgerðir** .
4. Sölupöntunaraðgerðin er  **valin til að opna**  gluggann sölupöntun  **.**  Sölupöntun er krafa, að ef þörf krefur, er hægt að þekja hana með samsetningu, framleiðslu eða með því að kaupa með hjálp áætlunarvélarinnar. Einnig styðja ýmsir afgreiðsluferlar vöruhússins við algjöra aðgreiningu á skyldum.
5.  **Veljið opna opnar**  aðgerðina.
6.  **Í umboðsmanninum**  er sett inn `DHL`.
7. Í reitnum  **pakki mælingar nr.**, Enter `123456789`.
8.  **Veldu bóka**  aðgerð, Hafðu  **Sendist-og reikningslykingu**  og veldu svo hnappinn í  **lagi** .

Nú eru Efnisleg og fjárhagsleg gögn skráð í [!INCLUDE[prod_short](../includes/prod_short.md)]. Nú er tímabært að tilkynna  Shopify  um breytingarnar.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn  **samstillingu afhendingar við  Shopify** og veljið tengdan tengil.
2. Velja **Í lagi**.

Í  **Shopify  tilkynningu stjórnun**  að pöntunin sé nú merkt sem  *uppfyllum*. Einnig er hægt að fara yfir sendingarupplýsingar og sjá Rakningarslóðina þar. Ef keyrðar  **eru Samstillingarpantanir frá  Shopify**  aftur verður pöntunin skjöluð í báðum kerfum.

## <a name="walkthrough-invite-your-customers-to-your-new-online-store" />Walkthrough: Bjóddu viðskiptavinum þínum upp á nýja netverslun

### <a name="scenario" />Aðstæður

Eftir árangursríka flýtiræsingu í nýju netversluninni er óskað eftir að núverandi viðskiptavinir þínir geti heimsótt hana og byrjað að setja inn pantanir.

### <a name="steps" />Skref

Í  [!INCLUDE[prod_short](../includes/prod_short.md)], gerið eftirfarandi skref:

1. Veldu þá  ![ljósaperu sem opnast Segðu mér aðgerðina.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Shopify Verslanir** og veldu viðeigandi tengil.
2.  **Veljið DEMO1**  -verslunina sem samstilla á viðskiptavinina við til að opna  **Shopify  vinnukortasíðuna** .
3. Veldu aðgerðina **Samstilla viðskiptamenn**.

Í  **Shopify  tilkynningu frá kerfisstjóra**  um að viðskiptavinirnir væru fluttir inn. Opnaðu einn viðskiptavinanna og Taktu eftir því að fyrsta og Síðasta heiti viðskiptamannsins kemur úr  **reitnum Heiti**  tengiliðar á  **viðskiptamannaspjaldinu**. Heiti fyrirtækisins má finna í sjálfgefna aðsetrinu sem tengt er viðskiptavininum. Velja  **skal senda reikning**  til að bjóða viðskiptavininum.

## <a name="walkthrough-fine-tuning-of-item-management" />Walkfrom: Fine Tuning the Item Management

### <a name="scenario" />Aðstæður

Þú vilt bæta meiri sveigjanleika og stýra ferlum í kringum vörustjórnun. Þú vilt bæta vörulýsingu og vilt bæta við endurskoðunarleiðbeiningum áður en afurðir verða tiltækar til að ljúka viðskiptavini.

### <a name="steps" />Skref

Í  [!INCLUDE[prod_short](../includes/prod_short.md)], gerið eftirfarandi skref:

Undirbúningur gagna.

1. Veldu þá  ![ljósaperu sem opnast Segðu mér aðgerðina.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn  **verðflokk** viðskiptamanns og velja tengdan tengil.
2. Bæta við nýjum verðflokki.  **Í reitnum kóti**  er fært inn `SHOPIFY`.
3. Glugganum Verðflokkur  **viðskiptamanns er**  lokað.
4. Veldu þá  ![ljósaperu sem opnast Segðu mér aðgerðina.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn  **atriði** og veljið tengdan tengil.

Velja vöru  **1896-S, Athens Skrifborðsstóll**  og keyra eftir leiðbeiningum.

1.  **Veldu afbrigðin**  aðgerð og bættu svo við tveimur vöruvíddasamsetningum  `PREMIUM, Athens Desk, Premium edition`  og `ESSENTIAL, Athens Desk, Essential edition`.
2. Velja  **lengda**  aðgerð aðgerðar, búa til nýjan lengdan texta sem gildir fyrir alla tungumálskóta.  **Í reitnum Lýsing**  er fært inn `Shopify`. 
3. Bæta við eftirfarandi texta við HTML-merki: `<b>Simple stylish design</b> blends with any ensemble. <i>Available in two editions.</i>`.
4. Veljið  **Söluverð**  aðgerðar og bætið við nýju verði eins og sýnt er í eftirfarandi töflu:

  |Lína|**Tegund sölu**|**Kóti sölu**|Tegund|Kóti|Afbrigðiskóði<br>(bæta svæðinu í gegnum sérstillingar)|Einingarverð|
  |------|------------|------------|------------|------------|------------|------------|
  |1|Verðflokkur viðskiptamanna|SHOPIFY|Vara|1896-S|ÓMISSANDI|700|
  |2|Verðflokkur viðskiptamanna|SHOPIFY|Vara|1896-S|IÐGJALD|1000|

5. Velja  **aðgerð söluafsláttar**  og bæta við nýjum afslætti:

* **Flokkur sölutegundar** *viðskiptavinar*
* **Sölukóði** *smásala*
* **Tegund** *vöru*
* **Kóði** *1896-S*
* **·** *Mælieining PCs*
* **Línuafsláttur%** *10*

6. Veldu  **Vörutilvísanaðgerðina**  og eftirfarandi bæta við línum:

  |Lína|**Gerð tilvísunar**|**Tilvísun nr.**|Afbrigðiskóði|
  |------|------------|------------|------------|
  |1|Strikamerki|77777777|ÓMISSANDI|
  |2|Strikamerki|11111111|IÐGJALD|


Velja skal Item  **1920-S, ANTWERP-Fundartöflu**  og keyra eftirfarandi skref.

1. Veldu  **leiðrétta birgðastöðu**  og í  **reitnum ný birgðastöð**  er fært inn  `100`  fyrir birgðageymslur  *Austur*  og  *Vestur*. 
2. Velja **Í lagi**.

Stilla samstillingarstillingarnar.

1. Veldu þá  ![ljósaperu sem opnast Segðu mér aðgerðina.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Shopify Verslanir** og veldu viðeigandi tengil.
2.  *Veljið verslunina DEMO1*  sem á að samstilla vörur til að opna  Shopify  spjald-síðu verkstæðis.
3. Velja  *shopify*  í  **reitnum Verðflokkur**  viðskiptamanna.
4. Veljið  *RETAIL*  í  **afsláttarflokki**  viðskiptavinaafsláttar.
5.  **Virkja lengdan textareit**  Samkeyrsluvöru.
6. Veljið  *Vörunr. + afbrigðiskóta*  í  **skr. vörpun**  svæði.
7. Velja  *drög*  í  **reitnum Staða fyrir stofnaðar afurðir** .
8. Veljið  *stöðu í skjalasafni*  **fyrir aðgerð fyrir fjarlægð afurðarsvæðis** .

Keyra samstillinguna.

1. Veldu þá  ![ljósaperu sem opnast Segðu mér aðgerðina.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Shopify Verslanir** og veldu viðeigandi tengil.
2.  *Veljið DEMO1*  -verslunina þar sem á að samstilla vörur til að opna  **Shopify  vinnukortasíðuna** .
3. Velja skal  **aðgerðina afurðir**  til að opna  **Shopify  vöruglugga** .
4. Velja aðgerðina **Bæta við atriðum**.
5. Stillið afmörkunartöfluna  *·*  á  **vörutegundarkótann** .
6. Veldu aðgerðina **Samstilla myndir af vörum**.
7.  **Veljið Samstillingarbirgðaaðgerðina** .

Afurðum bætt við. Takið eftir að staðan er stillt á  *uppkast* og því eru vörurnar ekki sýnilegar í  Shopify  vefversluninni.

1. Línan með Item  *1920-S, ANTWERP-Ráðstefnutöflu* er valin.  **Í SEO-titlinum** skal slá `Rectangular meeting table Antwerp, 10 seats, black`.
2. Velja  *skal*  virkt  **í reitnum Staða** .
3. Valin er línan með vörunni  *1906-S, ATHENS, Mobile Stallbakur*  og svo er  **valið DELETE**  aðgerðina.

Í  **Shopify  Stjórnun**  er tekið eftir að allar vörur hafa mismunandi stöðu.

* *Ráðstefnutafla*  ANTWERP er  *virk*  vegna þess að við breyttum stöðu í  **Shopify  vöruglugga** .
* *ATHENS Skrifborðsstóll*  er  *uppdragandi*  þar sem við skilgreindan sjálfgefna stöðu fyrir allar Viðbættur vörur til  *uppgerðar*.
* *ATHENS Mobile Stallbakur*  er  *Skjalasafn*  þar sem við skilgreindum versluninni sjálfkrafa að úthluta stöðuskjalasafni  *·*  fyrir eyddar afurðir.

Taka skal eftir að birgðaskrá fyrir Ráðstefnutöflu ANTWERP er 100, þar sem samskipað kerfi til að nota birgðir aðeins frá tveimur stöðum í AÐALSTAÐ og AUSTUR. Birgðir á öðrum stöðum (VESTURLANDI) eru hunsaðar.

* Opnið  *forskoðunartöflu* **Antwerp, Takið eftir** sérsniðnu gerð  **,** lánardrottni  **,** þyngd  **,**  kostnaði fyrir hverja vörureiti  **og**  leitarvélahluta í leit að lista.
* Opnaðu  *Athens Desk*, Skrunaðu niður í  **vöruvíddasamsetningar**  og Taktu eftir því hvernig  **·**  Skráning er útfyllt.
* Velja  **Breyta**  til að fara yfir strikamerki og verð.
* Breyttu stöðu  *Afgreiðsluborðs*  Athens í  *Active*  og veldu  **forskoðunaraðgerð** .

 **Shopify Í netverslun**  Opna vörulistans er að finna  *Athens Desk*   Product. Takið eftir að mismunandi valkostir eru í boði. Fyrir mismunandi valkosti eru mismunandi verð. Greiða skal athygli á afsláttarupplýsingum.

## <a name="walkthrough-import-items-from-shopify" />Walkthrough: flytja inn vörur úr Shopify

### <a name="scenario" />Aðstæður

Þú átt nú þegar vel heppnaða netverslun og langar að byrja að nota  [!INCLUDE[prod_short](../includes/prod_short.md)]  sem Business Management hugbúnað. Þú vilt flytja inn eins mikið af  Shopify  gögnum og hægt er. 

### <a name="steps" />Skref

Þetta er framhald af walkof  [: Byrjaðu að selja vörur á netinu](walkthrough-setting-up-and-using-shopify.md#walkthrough-start-selling-products-online). Þú getur líka prófað með þínum eigin gögnum, til dæmis þinni  Shopify  verslun eða sandkassa.

Í  [!INCLUDE[prod_short](../includes/prod_short.md)], gerið eftirfarandi skref:

#### <a name="prepare-data" />Undirbúa gögn

1. Skiptu yfir í ókeypis 30 daga prufutíma án sýnigagna. Frekari upplýsingar er að finna  [í bæta eigin gögnum við tóma prufu](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions#add-your-own-data-to-an-empty-trial-company).
2. Veldu þá  ![ljósaperu sem opnast Segðu mér aðgerðina.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn  **Shopify  verslanir** og veljið síðan tengda tengilinn.
3. Valið er aðgerðin **Nýtt**.
4.  **Í reitnum kóti**  er fært inn `DEMO2`.
5.  **Shopify Í reitinn URL**  er rituð slóðin að vefversluninni sem á að tengjast.
6.  **Virkjaðu virkjunina**  skipta, Skoðaðu og samþykktu skilmálana.

Skilgreinið  Shopify  verkstæðið eins og lýst er hér á eftir í næstu skrefum:

7. Virkja kladda sem virkjaður  **er**  skipta.
8.  **Gera Samcs**  -víxlun óvirka.
9. Veljið  **úr  Shopify**  í  **reitnum sync-vara** .
5. Gera Óþekkt atriði  **virka á**  sjálfvirka stofnun skipta.
11.  **Reiturinn Vörusniðmátskóti**  er fylltur út með viðeigandi sniðmáti.
12. Valið  **er úr  Shopify**  í  **reitnum Samkeyrslumynd**  vöru.
13. Velja  **alla viðskiptamenn**  sem  **flytja inn viðskiptavin úr Shopify**.
14. Gera sjálfvirka stofna Óþekkt viðskiptavini  **skipta út** .
15.  **Reiturinn sniðmát**  viðskiptamanns er fylltur út með viðeigandi sniðmáti.
16. Fyllt er inn í  **reikning** sendingargjalda,  **oddareikningur**  með tekjulykli. Til dæmis í Bandaríkjunum notkun `40100`.
17. Sjálfvirk stofnun pantana  **er gerð virk í**  skipta.

#### <a name="run-the-synchronization" />Keyra samstillingu

1. Veldu þá  ![ljósaperu sem opnast Segðu mér aðgerðina.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Shopify Verslanir** og veldu viðeigandi tengil.
2.  *DEMO2*  -verslunin sem samstilla á gögn fyrir er valin til að opna  **Shopify  síðu verkstæðiskortsins** .
3. Veldu aðgerðina **Samstilla vörur**.
4. Veldu aðgerðina **Samstilla myndir af vörum**.
5. Veldu aðgerðina **Samstilla viðskiptamenn**.

### <a name="results" />Niðurstöður

* Shopify Vörur eru fluttar inn. Til að sannprófa skaltu velja þá  ![ljósaperu sem opnar aðgerðina segja mér.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Shopify Vörur** og veldu viðeigandi tengil.
* Vörur með myndum eru búnar til. Til að sannprófa skaltu velja þá  ![ljósaperu sem opnar aðgerðina segja mér.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn  **atriði** og veljið tengdan tengil.
* Shopify Viðskiptavinir eru fluttir inn. Til að sannprófa skaltu velja þá  ![ljósaperu sem opnar aðgerðina segja mér.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn  **Shopify  viðskiptamenn** og veljið tengdan tengil.
* Viðskiptamenn eru stofnaðir. Til að sannprófa skaltu velja þá  ![ljósaperu sem opnar aðgerðina segja mér.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn  **viðskiptamenn** og veljið tengdan tengil.


## <a name="see-also" />Sjá einnig

[Byrjaðu með  Shopify  tengiflugi](get-started.md)  
