---
title: Breytingar á endurskoðun
description: Hægt er að virkja breytingaskrá svo að þú hafir yfirlit yfir allar breytingar sem gerðar hafa verið á gögnum í röktum töflum. Þú getur einnig rakið aðgerðir með tilteknum gerðum aðgerðakladda.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'user log, user activity, tracking'
ms.search.form: '592, 593, 594, 595, 710, 1366, 1367, 1368, 1369'
ms.date: 05/03/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Breytingar á endurskoðun

Sameiginleg áskorun margra viðskiptastjórnunarforrita er að forðast óæskilegar breytingar á gögnum. Þetta getur verið allt frá röngu símanúmeri viðskiptamanns til rangrar bókunar í fjárhag. Þessi grein lýsir getu til að komast að því hvað breyttist, hver breytti henni og hvenær breytingin var gerð.

## Um breytingaskrá

Með breytingaskránni er hægt að rekja allar beinar breytingar sem notendur gera á gögnum í gagnagrunninum. Tilgreina skal hverja töflu og reit sem kerfið á að skrá og síðan virkja breytingaskrána. Breytingaskráin byggir á breytingum sem gerðar eru á gögnum í töflunum sem þú rekur. Á síðunni **Breytingaskrárfærslur** er færslum raðað í tímaröð og sýndar eru allar breytingar sem gerðar eru á gildum í reitum í töflunum sem eru tilgreindar.

Rakningarbreytingar geta haft áhrif á afköst, sem geta kostað tíma og aukið stærð gagnagrunnsins, sem gæti kostað peninga. Til að draga úr þessum kostnaði þarf að hafa eftirfarandi atriði í huga:

- Íhuga skal vel notkun á töflum og aðgerðum.
- Ekki bæta við færslum og bókuðum skjölum. Í staðinn skal forgangsraða kerfisreitum á borð við „Stofnað af“ og „Dagsetning stofnunar“.
- Ekki skal nota rakningartegund allra **reita** . Þess í stað skal velja **Sumir reitir** og rekja aðeins mikilvægustu reitina.

> [!NOTE]
> Breytingaskráin rekur ekki breytingar á reitum sem nota þennan reit `autoIncrement property`. Dæmi um reit sem notar eiginleikann er heiltölureitur í töflunum Villuboð og VSK-skýrslulína.

Einnig af afkastaástæðum er slökkt á breytingaskránni við uppfærslu á [!INCLUDE [prod_short](includes/prod_short.md)] í næstu útgáfu. Auk þess að flýta uppfærsluferlinu hjálpar það til við að draga úr vísbendingu í möguleikaskránni. Um leið og uppfærslu er lokið byrjar skráin að rekja breytingar á ný.

> [!Important]
> Breytingar sjást aðeins í **Breytingaskrárfærslum** þegar lota notanda er endurræst, sem gerist á eftirfarandi hátt:
>
> - Lotan rann út og var endurnýjuð.
> - Notandinn valdi annað fyrirtæki eða hlutverkamiðstöð.
> - Notandinn skráði sig út og aftur inn.

## Uppsetning breytingaskrárinnar

Á síðunni **Uppsetning** breytingaskrár er hægt að kveikja eða slökkva á breytingaskránni. Þegar það er gert er aðgerðin skráð og því alltaf hægt að sjá hver breytti því.

Á síðunni **Breytingaskrár Uppsetning** ef aðgerðin **Töflur** er valin, skal tilgreina hvaða töflur á að rekja breytingar fyrir og hvaða breytingar á að rekja. [!INCLUDE[prod_short](includes/prod_short.md)] rekur einnig nokkrar kerfistöflur.

> [!NOTE]
> Hægt er að fylgjast með tilteknum reitum fyrir breytingar, t.d. reitum sem innihalda viðkvæm gögn, með því að setja upp eftirlit með reitum. Ef það er gert, til að forðast offramboð, verður taflan sem inniheldur reitinn ekki í boði fyrir uppsetningu breytingaskráar. Nánari upplýsingar eru [í Skjár viðkvæmir reitir](across-log-changes.md#monitor-sensitive-fields).

Þegar breytingaskráin hefur verið sett upp, virkjuð og gögn breytt er hægt að skoða og afmarka breytingarnar á síðunni **Breytingaskrárfærslur** . Ef eyða á færslum er sett upp varðveitt regla þar sem hægt er að setja afmarkanir byggðar á dagsetningum og tíma. Nánari upplýsingar um varðveitingarstefnur eru notaðar til að [skilgreina varðveitingarstefnur](admin-data-retention-policies.md).  

## Greining gagna í breytingaskránni

Hægt er að nota aðgerðina **Gagnagreining** til að greina gögn í breytingaskrá á síðunni [Breytingaskrárfærslur](https://businesscentral.dynamics.com/?page=595) . Ekki þarf að keyra skýrslu eða opna annað forrit, t.d. Excel. Eiginleikinn býður upp á gagnvirka og fjölhæfa leið til að reikna út, taka saman og skoða gögn. Í stað þess að keyra skýrslur með valkostum og afmörkunum er hægt að bæta við mörgum flipum sem tákna mismunandi verk eða yfirlit á gögnunum. Ákveðin dæmi eru "Hver breytti hvaða gögn, og hvenær" eða "Gögn breytast eftir töflu/reit" eða önnur sjónarmið er hægt að ímynda sér. Til að fræðast meira um notkun aðgerðarinnar **Gagnagreining** er farið í [Greiningarlista og fyrirspurnargögn með greiningarstillingu](analysis-mode.md).

### Breytingaskrá tilfalengd greiningardæmi

Eftirfarandi hlutar gefa dæmi um aðstæður þar sem greining breytingaskrár getur hjálpað til við að fylgjast með og endurskoða mikilvægar breytingar.

| Svæðarit | Til... | Opna þessa síðu í greiningarstillingu | Þessir reitir notaðir |
| ---- | ----- | ------------------------------- |------------------- |
| [Hver breytti hvaða gögnum, og hvenær](#example-who-changed-what-data-and-when) | Sjá hver breytti hvaða gögnum. | [Breytingaskrárfærslur](https://businesscentral.dynamics.com/?page=595) | **Notandakenni, Dagsetning og Tími**, **Texti** töflu,Texti **reits**,Aðallykilsgildi **2,Aðallykilgildi** **3**, **Gerð breytinga,Eldra** **gildi** og **Nýtt gildi.** **·** |
| [Gagnabreytingar eftir töflu/svæði](#example-data-changes-by-tablefield) | Sjá breytingar á gögnum eftir töflu/reit og hver gerði breytinguna. | [Breytingaskrárfærslur](https://businesscentral.dynamics.com/?page=595) | **Töflutitit**, Texti reits **,** Kenni notanda **,** Dagsetning og Tími **,** Aðallykilgildi 2,Aðallykilgildi **3** **,** Tegund breytinga,Eldra **gildi** **og** Nýtt gildi **.** |

### Dæmi: Hver breytti hvaða gögnum, og hvenær

Til að greina Hver breytti hvaða gögnum skal fylgja eftirfarandi skrefum:

1. Listinn [Breytingaskrárfærslur](https://businesscentral.dynamics.com/?page=595) er opnaður og smellt á :::image type="content" source="media/analysis-mode-icon.png" alt-text="Færa inn greiningarham."::: Tákn til að kveikja á greiningarstillingu.
1. Í valmyndinni **Dálkar** eru allir dálkar fjarlægðir (reiturinn við hliðina á leitarreitnum **til** hægri er valinn).
1. Reiturinn Kenni notanda er dreginn **(hver gerði það) yfir á** svæðið Línuflokkar **.** 
1. Velja skal eftirfarandi reiti:
   - Til að sýna hvenær það gerðist skal velja **Dagsetning og Tími**.
   - Til að sýna töfluna þar sem það gerðist skal velja **Texti** töflu. 
   - Til að sýna hvaða reit skal velja **Texti reits**.
   - Til að sýna reitskótann skal velja **Aðallykilgildi 2**. 
   - Til að sýna heiti fyrirtækis skal velja **Aðallykilgildi 3**.
   - Til að sýna hvort breytingin var sett inn, uppfærð eða eyða aðgerð skal velja **Tegund breytinga**.
   - Til að sýna breytinguna skal velja **Gamalt virði** og **Nýtt virði**.
1. Endurnefna greiningarflipann á **Hver breytti hvaða gögnum hvenær**, eða eitthvað sem lýsir þessari greiningu.

Eftirfarandi mynd sýnir niðurstöður þessara skrefa.

:::image type="content" source=" media/data-analysis-change-log-entries-Who-changed-What-data-When.png" alt-text="Dæmi um greiningu á gögnum á síðunni Breytingaskrárfærslur (Hver breytti hvaða gögnum Hvenær)." lightbox="media/data-analysis-change-log-entries-Who-changed-What-data-When.png":::

### Dæmi: gagnabreytingar eftir töflu/reit

Til að greina gagnabreytingar eftir töflu/reit er eftirfarandi skrefum fylgt:

1. Listinn [Breytingaskrárfærslur](https://businesscentral.dynamics.com/?page=595) er opnaður og smellt á :::image type="content" source="media/analysis-mode-icon.png" alt-text="Færa inn greiningarham."::: Tákn til að kveikja á greiningarstillingu.
1. Í valmyndinni **Dálkar** eru allir dálkar fjarlægðir (reiturinn við hliðina á leitarreitnum **til** hægri er valinn).
1. Dragðu **töflutexta**  (á hvaða töflu) og **Reitatexti**  (á hvaða reit) í **línuflokkasvæðið** .
1. Velja skal eftirfarandi reiti:
   - Til að sýna hvenær það gerðist skal velja **Dagsetning og Tími**
   - Til að sýna hver gerði breytinguna skal velja **Kenni** notanda.
   - Til að sýna kóta reitsins skal velja **Aðallykilgildi 2**.
   - Til að sýna heiti fyrirtækis skal velja **Aðallykilgildi 3**  (yfirleitt heiti fyrirtækis) 
   - Til að sýna hvort breytingin var sett inn, uppfærð eða eyða aðgerð skal velja **Tegund breytinga**.
   - Til að sýna breytinguna skal velja **Gamalt virði** og **Nýtt virði**.
1. Endurnefna greiningarflipa við **Gagnabreytingar eftir töflu + reit** eða einhverju sem lýsir þessari greiningu.

Eftirfarandi mynd sýnir niðurstöður þessara skrefa.

:::image type="content" source=" media/data-analysis-change-log-entries-data-changes-by-table-field.png" alt-text="Dæmi um hvernig á að gera gagnagreiningu á síðunni Breytingaskrárfærslur (gögn breytast eftir töflu/reit)." lightbox="media/data-analysis-change-log-entries-data-changes-by-table-field.png":::

## Um aðgerðaskrár

Á sumum síðum í [!INCLUDE [prod_short](includes/prod_short.md)] er hægt að skoða aðgerðarkladda sem sýnir stöðu og allar villur úr skrám sem þú flytur út úr eða flytur inn í [!INCLUDE [prod_short](includes/prod_short.md)].  

### Vinna með aðgerðaskrár

Upplýsingarnar birtast á síðunni **Aðgerðaskrá** samkvæmt samhenginu sem hún var opnuð úr. Til dæmis er hægt að opna síðuna á síðunum **Uppsetning skjalaskiptaþjónustu**, **Skjal á innleið**, **Bókaður sölureikningur** og **Bókaður sölukreditreikningur**. Hægt er að tæma listann yfir kladdafærslur eða hreinsa lista yfir færslur sem eru eldri en sjö daga.  

## Fylgjast með viðkvæmum reitum

Að halda viðkvæmum gögnum öruggum tryggja persónuvernd er mikilvægt flestum fyrirtækjum. Til að bæta við öryggislagi er hægt að fylgjast með mikilvægum reitum og fá tölvupóst þegar einhver breytir gildi. Til dæmis gætirðu viljað fá tilkynningu ef einhver breytir IBAN-númeri fyrirtækisins.

> [!NOTE]
> Að senda tilkynningu í tölvupósti krefst þess að eiginleiki tölvupósts verði settur upp í [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar eru í [Setja upp tölvupóst](admin-how-setup-email.md).

### Setja upp reitarvöktun

Hægt er að nota uppsetningarleiðbeiningar **Uppsetning á breytingavöktun reits** með hjálp til að tilgreina reitina sem á að fylgjast með samkvæmt síuskilyrði á borð við flokkun gagnatrúnaðar fyrir reitina. Nánari upplýsingar er að finna í [Flokkun á gagnatrúnaðar](admin-classifying-data-sensitivity.md). Leiðarvísirinn gerir einnig kleift að tilgreina þann sem fær tilkynningu í tölvupósti þegar breyting á sér stað og tölvupóstreikninginn sem sendir tilkynninguna. Tilgreinið bæði notandann sem fær tilkynningu og reikninginn sem tilkynningin verður send frá. Eftir að leiðarvísinum er lokið er hægt að vinna með stillingar fyrir reitavöktun á síðunni **Uppsetning reitavöktunar**.

> [!NOTE]
> Þegar þú tilgreinir tölvupóstsreikninginn sem á að senda tilkynningar frá verður þú annaðhvort að bæta við reikningsgerðunum **Microsoft 365** eða **SMTP**. Senda skal tilkynningar frá reikningi sem er ekki tengdur við raunverulegan notanda. Þú getur því ekki valið reikningsgerðina **Núverandi notandi**. Tilkynningar verða ekki sendar ef þú gerir það.

Með tímanum stækkar listinn yfir færslur á síðunni **Kladdafærslur reitavöktunar**. Til að draga úr fjölda færslna er hægt að stofna varðveislureglu sem eyðir færslum eftir tiltekinn tíma. Frekari upplýsingar er að finna í [Skilgreina varðveislureglur](admin-data-retention-policies.md).

Þegar settur er upp reitavöktun eða einhverju er breytt í uppsetningunni, eru færslur stofnaðar fyrir breytingarnar. Hægt er að tilgreina hvort birta eigi færslur sem tengjast uppsetningu vöktunar með því að sýna eða fela þær.

Hægt er að stjórna stillingum fyrir reitavöktun, t.d. hvort senda eigi tilkynningu í tölvupósti eða bara skrá breytinguna, fyrir hvern reit á síðunni **Vinnublað vaktaðra reita**. Á þessari síðunni er einnig hægt að bæta við eða fjarlægja vaktaða reiti.

> [!NOTE]
> Þegar búið er að skrá einn eða fleiri rieti og hefja vöktun þarf að skrá sig út úr [!INCLUDE[prod_short](includes/prod_short.md)] og skrá sig inn aftur til að stillingarnar taki gildi.

### Vinna við svæðavöktun

Færslur fyrir öll breytt gildi í vöktuðum reitum eru tiltækar á síðunni **Kladdafærslur vaktaðra reita**. Færslur innihalda til að mynda eftirfarandi upplýsingar:

- Reiturinn sem gildið breyttist í.
- Upphaflegu og nýju gildin.
- Hver gerði breytinguna og hvenær viðkomandi gerði hana.

Til að rannsaka breytingu frekar þarf að velja gildi til að opna síðuna þar sem hún var gerð. Til að skoða lista yfir allar færslur skal velja **Breytingafærslur reita**.

### Skoða fjarmælingar í reitum

Hægt er að setja upp [!INCLUDE[prod_short](includes/prod_short.md)] til að senda aðgerðir reitarvörpunar í Application Insights tilfang í Microsoft Azure. Síðan er hægt að nota Azure Monitor til að búa til skýrslur og setja upp viðvaranir í söfnuðum gögnum. Frekari upplýsingar eru í eftirfarandi greinum í [!INCLUDE[prod_short](includes/prod_short.md)] Developer og IT Pro Help:

- [Eftirlit og greining fjarmælinga - Virkjun Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-overview?toc=/dynamics365/business-central/toc.json#enable)
- [Greining fjarmælinga á reitum](/dynamics365/business-central/dev-itpro/administration/telemetry-field-monitoring-trace?toc=/dynamics365/business-central/toc.json)

## Skilgreina varðveitingarstefnu

Hægt er að búa til varðveislureglur til að eyða ónauðsynlegum gögnum í klöddum eftir tiltekinn tíma sem gefa skal upp. Til dæmis getur fjærslufjöldinn í kladda aukist með tímanum. Með því að hreinsa upp eldri færslur er auðveldara að setja athyglina á nýlegri og líklega meira viðeigandi færslur. Nánari upplýsingar um varðveitingarstefnur eru notaðar til að [skilgreina varðveitingarstefnur](admin-data-retention-policies.md).

## Sjá einnig

[Fylgjast með viðkvæmum reitum](across-log-changes.md#monitor-sensitive-fields)  
[Greining fjarmælinga á reitum](/dynamics365/business-central/dev-itpro/administration/telemetry-field-monitoring-trace?toc=/dynamics365/business-central/toc.json)  
[Skilgreina varðveislureglur](admin-data-retention-policies.md)  
[Grunnstillingum breytt](ui-change-basic-settings.md)  
[Röðun, leit, og síun](ui-enter-criteria-filters.md)  
[Finndu síður og upplýsingar með Viðmótsleit](ui-search.md)  
[Úthluta leyfi til notenda og hópa](ui-define-granular-permissions.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
