---
title: Setja upp tölvupóstskjöl
description: Fræðast um hvernig eigi að setja upp tölvupóstskjöl.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice'
ms.search.form: '359, 360, 6103, 6133'
ms.date: 05/02/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="set-up-e-documents"></a>Setja upp tölvupóstskjöl

> [!IMPORTANT]
> Kjarnaeining tölvupóstskjala er rammi. Sjálfgefið er að ekki **sé reiturinn Þjónustuheildun** . Ef sjálfgefið **er að valkostir fylgiskjalssniðs** finnist skal hafa í huga að þeir eru boðin sem dæmi og staðfæringin verður að gefa nákvæmt snið. Þessar upplýsingar eru hluti af staðfæringarforritum því þau eru sértæk fyrir staðbundnar kröfur.

> [!NOTE]
> Frá og með útgáfu 23.2 er staðlaðu PEPPOL-skjalssniði bætt við sem altæku sniði í reitnum **Skjalasnið** . Hafið í huga að líklega er ekki hægt að nota þetta snið eins og það er. Það er W1-snið sem gefur til að sýna hvernig þessi eiginleiki er notaður. Mælt er með því að prófa PEPPOL-sniðið sem fyrir er áður en byrjað er að nota þetta snið.

Fyrsta skrefið í grunnstillingu rafrænna skjala (e-documents) er að setja upp E-Documents-þjónustuna þar sem hegðun kerfisins er grunnstillt þar sem það er tengt tölvupóstsamskiptum.

## <a name="set-up-the-e-document-service"></a>Setja upp tölvupóstþjónustu

Fylgið þessum skrefum til að setja upp E-Document Service.

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **E-Document Services** og velja síðan viðeigandi tengil.
2. Valið er **Nýtt** og á síðunni **Þjónusta í E-document Services** á flýtiflipanum **Almennt** skal grunnstilla reitina eins og lýst er í eftirfarandi töflu.

    | Svæði | Heimildasamstæða |
    |-------|-------------|
    | Kóði | Velja skal uppsetningarkóta rafræns útflutnings. |
    | Heimildasamstæða | Færa inn stutta lýsingu á rafrænu útflutningsuppsetningunni. |
    | Skjalasnið | <p>Útflutningssnið rafræns útflutningsuppsetningar.</p><p>Sjálfgefið er að tveir valkostir séu í þessum reit. Hægt er að velja **PEPPOL BIS 3** sem almennt kótasnið eða **Data Exchange** þegar setja þarf upp fyrirfram skjöl með tilteknum sniðum á flýtiflipanum **Skilgreining** gagnaskipta.</p> |
    | Samþætting þjónustu | Velja skal samþættingarkótann fyrir rafræna útflutningsuppsetningu. Í bylgju 1 er **eini valkosturinn Engin samþætting**. |
    | Nota runuvinnslu | Tilgreina hvort þjónustan notar runuvinnslu til útflutnings. |

3. Á flýtiflipanum **Innfluttar færibreytur** eru reitirnir skilgreindir eins og lýst er í eftirfarandi töflu.

    | Svæði | Heimildasamstæða |
    |-------|-------------|
    | Staðfesta móttökufyrirtæki | Tilgreina þarf hvort staðfesta þurfi upplýsingar fyrirtækisins við innflutning. |
    | Leysa mælieiningu | Tilgreina skal hvort leysa skuli mælieininguna við innflutning. |
    | Fletta upp tilvísun í atriði | Tilgreina skal hvort leita eigi vöru með vörutilvísun við innflutning. |
    | Fletta upp GTIN-númeri atriðis | Tilgreina skal hvort leita eigi vöru með Altæku vörunúmeri (GTIN) við innflutning. |
    | Fletta upp reikningsvörpun | Tilgreina hvort leita eigi reikning í **reikningsvörpun** með innsendum texta við innflutning. |
    | Staðfesta línuafslátt | Tilgreina skal hvort staðfesta skuli línuafslátt við innflutning. |
    | Nota reikningsafslátt | Tilgreina hvort nota skuli reikningsafslátt við innflutning. |
    | Staðfesta samtölur | Tilgreina hvort staðfesta skuli samtölu reikninga við innflutning. |
    | Uppfæra pöntun | Tilgreina þarf hvort uppfæra þurfi samsvarandi innkaupapöntun. |
    | Stofna færslubókarlínur | Tilgreina þarf hvort stofna þurfi færslubókarlínu í stað innkaupaskjals. Þessi kostur er valinn þegar nota á færslubækur sem áfangastaðar fyrir reikningana. |
    | Heiti sniðmáts færslubókar | Tilgreina heiti færslubókarsniðmátsins sem notað er við stofnun færslubókarlínu. Þessi reitur á við þegar nota á færslubækur sem áfangastaðar fyrir reikningana. |
    | Heiti færslubókarkeyrslu | Tilgreina heiti færslubókarkeyrslunnar sem er notuð við stofnun færslubókarlínu. Þessi reitur á við þegar nota á færslubækur sem áfangastaðar fyrir reikningana. |
    | Sjálfvirkur innflutningur | Tilgreina hvort flytja skuli skjöl sjálfvirkt inn úr þjónustunni. |
    | Upphafstími keyrslu | Tilgreina upphafstíma fyrir innflutning verka. |
    | Mínútur á milli keyrslna | Tilgreina fjölda mínútna milli keyrslu á innflutningi. |

4. Ef Gagnaskipti voru valin **í reitnum** Skjalasnið **á flýtiflipanum** Almennt **skal nota** flýtiflipann Skilgreining **gagnaskipta til að stilla eftirfarandi reiti.** 

    | Svæði | Heimildasamstæða |
    |-------|-------------|
    | Gerð fylgiskjals | Tilgreina skjalategundina sem notar gagnaskipti til að flytja inn og flytja út gögnin. Sem dæmi má nefna **Sölureikning**, **Sölukreditreikning** og **Innkaupareikning.** |
    | Skilgreiningarkóði gagnaskipta í innflutningi | Tilgreina gagnaskiptakóðann sem er notaður til að flytja inn gögnin. Þessi reitur er aðeins notaður til að taka á móti fylgiskjali í innkaupaferlinu. |
    | Skilgreiningarkóði gagnaskipta í útflutningi | Tilgreina gagnaskiptakóðann sem er notaður til að flytja út gögnin. Þessi reitur er aðeins notaður til að afhenda skjöl í söluferlinu. |

> [!NOTE]
> Til eru útbúnar gagnaskiptaskilgreiningar fyrir PEPPOL-snið sem tengjast stöðluðu sölu- og innkaupaskjali. Hins vegar er líklegt að ekki sé hægt að nota þessar skilgreiningar eins og er. Þau eru öll W1-snið sem fylgja til að sýna hvernig á að nota þessa aðgerð. Mælt er með því að þú prófir PEPPOL-sniðið sem fyrir er áður en byrjað er að nota það.

Ef skilgreiningarsnið **data** Exchange hefur verið grunnstillt í staðfæringu er hægt að bæta við línu fyrir hverja skjalategund sem þörf er á. Bæta við línum sem samsvara sjálfgefnu gagnaskiptunum fyrir W1 PEPPOL-sniðið. Fyrst er valkosturinn Tegund **fylgiskjals** valinn fyrir hverja línu sem þörf er á. Fyrir hverja gagnategund skal velja gildið **Flytja inn gagnaskiptaskilgreiningarkóta** eða **Flytja út eigindarkóta** gagnaskipta sem á að nota.

Ef skilgreiningarsnið gagnaskipta er ekki notað **er hægt að búa til og grunnstilla snið með því að nota viðmótið**  [.](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments) Stilla skal upplýsingarnar í **Útflutningsvörpun** og **Innflutningsvörpunarlínum** þar sem hægt er að finna töflur og reiti til að grunnstilla umbreytingarreglur. Í þessu tilviki verður að bæta við nýjum valkosti í reitnum **Skjalasnið** sem tengist sniðinu.  

### <a name="supported-document-types"></a>Studdar skjalategundir

Studdar skjalategundir eru byggðar á því skjalasniði **sem** valið var. Til að kanna hvaða skjalategundir eru studdar skal velja aðgerðina **Studdar skjalategundir á síðunni**  **Studdar skjalategundir** . Skjalaþjónustan **sem studd er við upprunaskjal** opnast og í dálknum **Tegund** upprunaskjals er hægt að velja mismunandi tegundir skjala til að gera þær sem studdar af því sniði sem ætlunin er að nota. Tryggja skal að skjalategundin noti ekki ef skjalið er ekki valið á þessari síðu.   

## <a name="set-up-a-document-sending-profile"></a>Setja upp skjalasendingarsnið

Hægt er að setja upp kjöraðferð til að senda söluskjöl fyrir hvern viðskiptamann. Á þennan hátt þarf ekki að velja sendingarkost í hvert skipti þegar aðgerðin **Bóka og senda** er valin. Á síðunni **Sendingarforstillingar skjala** er hægt að setja upp mismunandi sendingarforstillingar og velja síðan þær í reitnum **Sending forstillingar** skjala á viðskiptamannaspjaldi. Hægt er að velja gátreitinn **Sjálfgefið** til að tilgreina að skjalasendingarforstilling sé sjálfgefin forstilling fyrir alla viðskiptamenn, nema viðskiptamenn þar sem reiturinn **Skjalasendingarforstilling** er stilltur á aðra sendingarforstillingu.

Þessi aðgerð er notuð til að setja upp sjálfvirkni rafrænna reikningsfærslu. Þegar valið er **Bóka og senda** í söluskjali sýnir svarglugginn **Bóka og senda staðfestingu** þá forstillingu sem er notuð: annaðhvort forstillingin sem er sett upp fyrir viðskiptamanninn eða sjálfgefna forstillingu fyrir alla viðskiptamenn.

Fylgið þessum skrefum til að setja upp skjalasendingarforstillingu.

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Skjalasendingarforstillingu** og velja síðan viðeigandi tengil.
2. Á síðunni **Sending forstillinga skjala** skal velja **Nýtt**.
3. Á flýtiflipanum **Almennt** eru færðar inn allar nauðsynlegar reitaupplýsingar.
4. Á flýtiflipanum **Sendingarvalkostir** eru reitirnir skilgreindir eins og lýst er í eftirfarandi töflu.

    | Svæði | Heimildasamstæða |
    |-------|-------------|
    | Rafrænt skjal | Tilgreina skal hvort skjalið sé sent sem tölvupóstskjal sem viðskiptamaður getur flutt inn í kerfi sitt þegar valið er **Bóka og senda**. Ef nota á þennan valkost þarf einnig að stilla reitinn **Snið** eða **Þjónustuflæðiskóti** rafrænna skjala. Einnig er hægt að vista skrána á disk. |
    | Snið | Tilgreina sniðið sem á að nota til að senda e-skjal. Þessi reitur er nauðsynlegur ef valið er **Gegnum skjalaskipti** í reitnum **Rafrænt skjal** . |
    | Kóði þjónustuflæðis fyrir rafræn skjöl | Tilgreina rafrænt þjónustuflæði sem er notað til að senda skjöl. Þessi reitur er nauðsynlegur ef valið er **Aukið þjónustuflæði** í reitnum **Rafrænt skjal** . |

    > [!NOTE]
    > Ef valið er **Aukið þjónustuflæði** í rafrænu skjali **verður** þegar að vera grunnstillt verkflæði fyrir tölvupóstskjölin.

## <a name="set-up-the-workflow"></a>Setja upp verkflæðið

Fylgið þessum skrefum til að setja upp verkflæðið sem er notað í e-skjalaaðgerðum.

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Verkflæðissniðmát** og velja síðan viðeigandi tengil.
2. Ef ekki er hægt að finna **sniðmát verkflæðis fyrir** E-skjal á síðunni **Sniðmát** verkflæðis skal velja **Endurstilla Microsoft-sniðmát**. **Sniðmát verkflæðis í E-skjali** ættu þá að birtast. Loka síðunni.
3.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Verkflæði** og velja síðan viðeigandi tengil.
4. Veljið aðgerðina **Nýtt verkflæði úr sniðmáti** til að velja sniðmát fyrir ferli tölvupóstskjala. Tiltæk sniðmát eru **Senda til einnar þjónustu** og **Senda til margra þjónustu**.
5. Velja skal **Í lagi** til að ljúka uppsetningu verkflæðis.
6. Í reitnum **Síðan svar** skal velja **Senda E-skjal með uppsetningunni** til að grunnstilla verkflæðissvörin.
7. Valin er e-Document þjónustan sem stofnuð var sem valkostur, Í lagi **valið** og verkflæðið virkjað.

> [!NOTE]
> Hægt er að stofna eigið verkflæði fyrir tölvupóstskjöl án þess að nota fyrirfram skilgreind verkflæðissniðmát. Ef notandi er með meiri þjónustu er hægt að nota mismunandi verkflæði.

Til að nota fleiri verkflæði skal grunnstilla þau í gegnum skjalasendingarsnið fyrir mismunandi viðskiptamenn. Þegar verkflæðið er sett upp skal tilgreina skjalasendingarsniðið í dálknum **Á skilyrði** á flýtiflipanum **Verkflæðisskref** því ekki er hægt að hafa tvær þjónustur sem nota sömu skjalasendingarsnið í verkflæðum.

Þegar verkflæði er grunnstillt á síðunni **Verkflæði** skal benda **á reitinn Á skilyrði** á flýtiflipanum **Verkflæðisskref** . Á síðunni **Skilyrði tilviks** í reitnum **Afmörkun** skal velja skjalasendingarsniðið sem á að nota.

## <a name="set-up-a-retention-policy-for-e-documents"></a>Setja upp varðveitingarstefnu fyrir tölvupóstskjöl

Tölvupóstskjöl geta verið efni ólíkra staðbundinna löggjafa sem tengjast því tímabili sem tölvupóstskjölin eru geymd fyrir. Því höfum við bætt við uppsetningu varðveitingarstefnu fyrir allar mikilvægar upplýsingar sem tengjast tölvupóstskjölum. Stjórnendur geta skilgreint varðveitingarreglur sem tilgreina hversu oft Dynamics 365 Business Central eyðir úreltum færslum sem tengjast tölvupóstskjölum. Nánari upplýsingar um varðveitingarstefnur [eru í Skilgreina varðveitingarreglur](admin-data-retention-policies.md).

Til að setja upp varðveitingarstefnur sem tengjast e-skjali skal fylgja þessum skrefum.

1. Á síðunni **Þjónusta** tölvupóstskjala skal velja aðgerðina **Varðveita stefnu** .
2. Þegar aðgerðinni er lokið skal velja eina af eftirfarandi varðveitingarreglum til að setja upp:

    - Skrá rafræns skjals
    - Samþættingarskrá rafrænna skjala
    - Vörpunarskrá rafræns skjals
    - Gagnageymsla tölvupóstskjala

## <a name="e-documents-demo-data"></a>Sýnigögn e-skjala

> [!NOTE]
> Úr Business Central útgáfu 24.0 er hægt að setja upp sýnigögn fyrir E-skjöl.

Microsoft bjó til nýja kynningu á rafrænum skjölum **til að veita auðveldari leiðir til að prófa og sýna getu E-skjala**. Til að virkja þessa einingu skal fylgja skrefunum:  

1.   ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, sláðu inn **Contoso Demo Tool** og veldu svo viðeigandi tengil.  
2.  Áður en eining E-skjalasamsetningar er gerð **virk verður að vera hægt að virkja eftirfarandi einingar:** Almenn eining **og** Vöruhúsaeining **.** 
3.  Þegar þessar einingar hafa verið gerðar virkar skal velja **E-Documents Contoso Eining** og velja svo aðgerðina **Búa til** . 
4.  Fylgdu skrefunum.  
5.  Loka síðunni.   

Þegar þú hefur virka einingu hefði verið búin til ný kynningarvara, flutt inn sex rafræn skjöl (byggt á Peppol BIS 3) og þegar grunnstillt **E-Document Services** með stofnuðum verkflæðum.  

## <a name="see-also"></a>Sjá einnig .

[Hvernig á að nota tölvupóstskjöl í sölu](finance-how-use-edocuments.md)    
[Hvernig nota á tölvupóstskjöl við innkaup](finance-how-use-edocuments-purchase.md)  
[Hvernig á að framlengja tölvupóstskjöl í Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)    
[Fjármálastjórnun](finance.md)    
[Reikningsfæra sölu](sales-how-invoice-sales.md)    
[Skrá innkaup með innkaupareikningum og pöntunum](purchasing-how-record-purchases.md)    
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
