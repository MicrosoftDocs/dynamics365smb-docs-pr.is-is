---
title: Breytingar á endurskoðun
description: Hægt er að virkja breytingaskrá svo að þú hafir yfirlit yfir allar breytingar sem gerðar hafa verið á gögnum í röktum töflum. Þú getur einnig rakið aðgerðir með tilteknum gerðum aðgerðakladda.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: null
ms.topic: conceptual
ms.search.keywords: 'user log, user activity, tracking'
ms.search.form: '592, 593, 594, 595, 710, 1366, 1367, 1368, 1369'
ms.date: 03/15/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="auditing-changes-in-business-central"></a>Endurskoðunarbreytingar í Business Central

Sameiginleg áskorun margra viðskiptastjórnunarforrita er að forðast óæskilegar breytingar á gögnum. Þetta getur verið allt frá röngu símanúmeri viðskiptamanns til rangrar bókunar í fjárhag. Þessi grein lýsir getu til að komast að því hvað breyttist, hver breytti henni og hvenær breytingin var gerð.

## <a name="about-the-change-log"></a>Um breytingaskrá

Með breytingaskránni er hægt að rekja allar beinar breytingar sem notendur gera á gögnum í gagnagrunninum. Tilgreina skal hverja töflu og reit sem kerfið á að skrá og síðan virkja breytingaskrána. Breytingaskráin byggir á breytingum sem gerðar eru á gögnum í töflunum sem þú rekur. Á síðunni **Breytingaskrárfærslur** er færslum raðað í tímaröð og sýndar eru allar breytingar sem gerðar eru á gildum í reitum í töflunum sem eru tilgreindar.

Rakningarbreytingar geta haft áhrif á afköst, sem geta kostað tíma og aukið stærð gagnagrunnsins, sem gæti kostað peninga. Hafðu eftirfarandi í huga til að draga úr þeim kostnaði:

- Íhuga skal vel notkun á töflum og aðgerðum.
- Ekki bæta við færslum og bókuðum skjölum. Í staðinn skal forgangsraða kerfisreitum á borð við „Stofnað af“ og „Dagsetning stofnunar“.
- Ekki skal nota rakningartegund allra **reita** . Þess í stað skal velja **Sumir reitir** og rekja aðeins mikilvægustu reitina.

> [!NOTE]
> Breytingaskráin rekur ekki breytingar á reitum sem nota þennan reit `autoIncrement property`. Dæmi um reit sem notar eiginleikann er heiltölureitur í töflunum Villuboð og VSK-skýrslulína.

Einnig af afkastaástæðum er slökkt á breytingaskránni við uppfærslu á [!INCLUDE [prod_short](includes/prod_short.md)] í næstu útgáfu. Auk þess að flýta uppfærsluferlinu dregur þetta einnig úr óþarfa óreiðu í breytingaskránni. Um leið og uppfærslu er lokið byrjar skráin að rekja breytingar á ný.

> [!Important]
> Breytingar sjást aðeins í **Breytingaskrárfærslum** þegar lota notanda er endurræst, sem gerist á eftirfarandi hátt:
>
> - Lotan rann út og var endurnýjuð.
> - Notandinn valdi annað fyrirtæki eða hlutverkamiðstöð.
> - Notandinn skráði sig út og aftur inn.

### <a name="work-with-the-change-log"></a>Vinna með breytingaskrá

Síðan **Uppsetning breytingaskrár** er notaður til að gera breytingaskráningu virka eða óvirka. Þegar notandi kveikir eða slekkur á breytingaskrá er þessi verkþáttur skráður til að geta ævinlega séð hvaða notandi kveikti eða slökkti á breytingaskránni.

Á síðunni **Breytingaskrár Uppsetning** ef aðgerðin **Töflur** er valin, skal tilgreina hvaða töflur á að rekja breytingar fyrir og hvaða breytingar á að rekja. [!INCLUDE[prod_short](includes/prod_short.md)] rekur einnig nokkrar kerfistöflur.

> [!NOTE]
> Hægt er að fylgjast með tilteknum reitum fyrir breytingar, t.d. reitum sem innihalda viðkvæm gögn, með því að setja upp eftirlit með reitum. Ef það er gert, til að forðast offramboð, verður taflan sem inniheldur reitinn ekki í boði fyrir uppsetningu breytingaskráar. Nánari upplýsingar eru [í Skjár viðkvæmir reitir](across-log-changes.md#monitor-sensitive-fields).

Þegar breytingaskrá hefur verið sett upp, virkjuð og einhver hefur breytt gögnum skráir forritið breytinguna í breytingaskrárfærslu. Hægt er að skoða og afmarka breytingarnar á síðunni **Breytingaskrárfærslur**. Ef eyða á færslum er sett upp varðveitt regla þar sem hægt er að setja afmarkanir byggðar á dagsetningum og tíma. Nánari upplýsingar um varðveitingarstefnur eru notaðar til að [skilgreina varðveitingarstefnur](admin-data-retention-policies.md).  

## <a name="about-activity-logs"></a>Um aðgerðaskrár

Á sumum síðum í [!INCLUDE [prod_short](includes/prod_short.md)] er hægt að skoða aðgerðarkladda sem sýnir stöðu og allar villur úr skrám sem þú flytur út úr eða flytur inn í [!INCLUDE [prod_short](includes/prod_short.md)].  

### <a name="work-with-activity-logs"></a>Vinna með aðgerðaskrár

Upplýsingarnar eru birtar á síðunni **Aðgerðarkladdi** í samræmi við samhengið sem þær eru opnaðar úr. Til dæmis er hægt að opna síðuna á síðunum **Uppsetning skjalaskiptaþjónustu**, **Skjal á innleið**, **Bókaður sölureikningur** og **Bókaður sölukreditreikningur**. Hægt er að tæma listann yfir kladdafærslur eða hreinsa lista yfir færslur sem eru eldri en sjö daga.  

## <a name="monitor-sensitive-fields"></a>Fylgjast með viðkvæmum reitum

Að halda viðkvæmum gögnum öruggum tryggja persónuvernd er mikilvægt flestum fyrirtækjum. Til að bæta við öryggisstigi er hægt að fylgjast með mikilvægum reitum og verið látin vita í tölvupósti þegar einhver breytir gildi. Til dæmis gætirðu viljað fá tilkynningu ef einhver breytir IBAN-númeri fyrirtækisins.

> [!NOTE]
> Að senda tilkynningu í tölvupósti krefst þess að eiginleiki tölvupósts verði settur upp í [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar eru í [Setja upp tölvupóst](admin-how-setup-email.md).

### <a name="set-up-field-monitoring"></a>Setja upp reitarvöktun

Hægt er að nota uppsetningarleiðbeiningar **Uppsetning á breytingavöktun reits** með hjálp til að tilgreina reitina sem á að fylgjast með samkvæmt síuskilyrði á borð við flokkun gagnatrúnaðar fyrir reitina. Nánari upplýsingar er að finna í [Flokkun á gagnatrúnaðar](admin-classifying-data-sensitivity.md). Leiðarvísirinn gerir einnig kleift að tilgreina þann sem fær tölvupóststilkynningu þegar breyting á sér stað, og tölvupóstsreikninginn sem sendir tilkynninguna í tölvupósti. Tilgreinið bæði notandann sem fær tilkynningu og reikninginn sem tilkynningin verður send frá. Eftir að leiðarvísinum er lokið er hægt að vinna með stillingar fyrir reitavöktun á síðunni **Uppsetning reitavöktunar**. 

> [!NOTE]
> Þegar þú tilgreinir tölvupóstsreikninginn sem á að senda tilkynningar frá verður þú annaðhvort að bæta við reikningsgerðunum **Microsoft 365** eða **SMTP**. Senda skal tilkynningar frá reikningi sem er ekki tengdur við raunverulegan notanda. Þú getur því ekki valið reikningsgerðina **Núverandi notandi**. Tilkynningar verða ekki sendar ef þú gerir það. 

Með tímanum stækkar listinn yfir færslur á síðunni **Kladdafærslur reitavöktunar**. Til að draga úr fjölda færslna er hægt að stofna varðveislureglu sem eyðir færslum eftir tiltekinn tíma. Frekari upplýsingar er að finna í [Skilgreina varðveislureglur](admin-data-retention-policies.md).

Þegar settur er upp reitavöktun eða einhverju er breytt í uppsetningunni, eru færslur stofnaðar fyrir breytingarnar. Hægt er að tilgreina hvort birta eigi færslur sem tengjast uppsetningu vöktunar með því að sýna eða fela þær. 

Hægt er að stjórna stillingum fyrir reitavöktun, t.d. hvort senda eigi tilkynningu í tölvupósti eða bara skrá breytinguna, fyrir hvern reit á síðunni **Vinnublað vaktaðra reita**. Á þessari síðunni er einnig hægt að bæta við eða fjarlægja vaktaða reiti.

> [!NOTE]
> Þegar búið er að skrá einn eða fleiri rieti og hefja vöktun þarf að skrá sig út úr [!INCLUDE[prod_short](includes/prod_short.md)] og skrá sig inn aftur til að stillingarnar taki gildi.

### <a name="work-with-field-monitoring"></a>Vinna við svæðavöktun

Færslur fyrir öll breytt gildi í vöktuðum reitum eru tiltækar á síðunni **Kladdafærslur vaktaðra reita**. Færslur innihalda til að mynda eftirfarandi upplýsingar:

- Reiturinn þar sem gildinu var breytt.
- Upphaflegu og nýju gildin.
- Hver gerði breytinguna og hvenær viðkomandi gerði hana.

Til að rannsaka breytingu frekar þarf að velja gildi til að opna síðuna þar sem hún var gerð. Til að skoða lista yfir allar færslur skal velja **Breytingafærslur reita**.

### <a name="view-field-monitoring-telemetry"></a>Skoða fjarmælingar í reitum

Hægt er að setja upp [!INCLUDE[prod_short](includes/prod_short.md)] til að senda aðgerðir reitarvörpunar í Application Insights tilfang í Microsoft Azure. Síðan er hægt að nota Azure Monitor til að búa til skýrslur og setja upp viðvaranir í söfnuðum gögnum. Frekari upplýsingar eru í eftirfarandi greinum í [!INCLUDE[prod_short](includes/prod_short.md)] Developer og IT Pro Help:

- [Fylgjast með og greina fjarmælingar - Virkja Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-overview#enable)
- [Greining fjarmælinga reitarvöktunar](/dynamics365/business-central/dev-itpro/administration/telemetry-field-monitoring-trace)

## <a name="define-retention-policies"></a>Skilgreina varðveitingarstefnu

Hægt er að búa til varðveislureglur til að eyða ónauðsynlegum gögnum í klöddum eftir tiltekinn tíma sem gefa skal upp. Til dæmis getur fjærslufjöldinn í kladda aukist með tímanum. Með því að hreinsa upp eldri færslur er auðveldara að setja athyglina á nýlegri og líklega meira viðeigandi færslur. Nánari upplýsingar um varðveitingarstefnur eru notaðar til að [skilgreina varðveitingarstefnur](admin-data-retention-policies.md).

## <a name="see-also"></a>Sjá einnig

[Grunnstillingum breytt](ui-change-basic-settings.md)  
[Röðun, leit, og síun](ui-enter-criteria-filters.md)  
[Finndu síður og upplýsingar með Viðmótsleit](ui-search.md)  
[Úthluta leyfi til notenda og hópa](ui-define-granular-permissions.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Skilgreina varðveislureglur](admin-data-retention-policies.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
