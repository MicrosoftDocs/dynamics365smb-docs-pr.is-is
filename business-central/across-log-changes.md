---
title: Endurskoðun breytinga| Microsoft docs
description: Hægt er að virkja breytingaskrá svo að þú hafir yfirlit yfir allar breytingar sem gerðar hafa verið á gögnum í röktum töflum. Þú getur einnig rakið aðgerðir með tilteknum gerðum aðgerðakladda.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 656def609801a85716a4afe57d603fe93eb7569c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5770964"
---
# <a name="auditing-changes-in-business-central"></a>Endurskoðunarbreytingar í Business Central
Sameiginleg áskorun margra viðskiptastjórnunarforrita er að forðast óæskilegar breytingar á gögnum. Þetta getur verið allt frá röngu símanúmeri viðskiptamanns til rangrar bókunar í fjárhag. Í þessu efnisatriði er lýst möguleikanum á því að finna út hvað breyttist, hver breytti því og hvenær breytingin var gerð.

## <a name="about-the-change-log"></a>Um breytingaskrá 
Með breytingaskránni er hægt að rekja allar beinar breytingar sem notendur gera á gögnum í gagnagrunninum. Tilgreina verður hverja töflu og reit sem kerfið á að skrá og síðan þarf að virkja breytingaskrána.  

Rakningarbreytingar geta haft áhrif á afköst, sem geta kostað tíma og aukið stærð gagnagrunnsins, sem gæti kostað peninga. Til að draga úr þessum kostnaði skal hafa eftirfarandi í huga:
- Íhuga skal vel notkun á töflum og aðgerðum.
- Ekki bæta við færslum og bókuðum skjölum. Í staðinn skal forgangsraða kerfisreitum á borð við „Stofnað af“ og „Dagsetning stofnunar“.
- Ekki nota rakningargerðina „Allir reitir“. Þess í stað skal velja nokkra reiti og rekja aðeins mikilvægustu reitina.

Breytingaskráin byggir á breytingum sem gerðar eru á gögnum í töflunum sem þú rekur. Á síðunni **Breytingaskrárfærslur** er færslum raðað í tímaröð og sýndar eru allar breytingar sem gerðar eru á gildum í reitum í töflunum sem eru tilgreindar.

> [!Important]
> Breytingar sjást aðeins í **Breytingaskrárfærslum** þegar lota notanda er endurræst, sem gerist á eftirfarandi hátt:
<br />
> * Lotan rann út og var endurnýjuð.
> * Notandinn valdi annað fyrirtæki eða hlutverkamiðstöð.
> * Notandinn skráði sig út og aftur inn.

### <a name="working-with-the-change-log"></a>Vinna með breytingaskrá
Síðan **Uppsetning breytingaskrár** er notaður til að gera breytingaskráningu virka eða óvirka. Þegar notandi kveikir eða slekkur á breytingaskrá er þessi verkþáttur skráður til að geta ævinlega séð hvaða notandi kveikti eða slökkti á breytingaskránni.

Á síðunni **Breytingaskrár Uppsetning** ef aðgerðin **Töflur** er valin, skal tilgreina hvaða töflur á að rekja breytingar fyrir og hvaða breytingar á að rekja. [!INCLUDE[prod_short](includes/prod_short.md)] rekur einnig númer kerfistaflna.

> [!NOTE]
> Hægt er að fylgjast með tilteknum reitum fyrir breytingar, t.d. reitum sem innihalda viðkvæm gögn, með því að setja upp eftirlit með reitum. Ef það er gert, til að forðast offramboð, verður taflan sem inniheldur reitinn ekki í boði fyrir uppsetningu breytingaskráar. Frekari upplýsingar er að finna í [Fylgjast með viðkvæmum reitum](across-log-changes.md#monitoring-sensitive-fields).

Þegar breytingaskrá hefur verið sett upp, virkjuð og einhver hefur breytt gögnum skráir forritið breytinguna í breytingaskrárfærslu. Hægt er að skoða og afmarka breytingarnar á síðunni **Breytingaskrárfærslur**. Ef á að eyða færslum er hægt að gera það á síðunni **Eyða breytingaskrárfærslum** þar sem hægt er að stilla afmarkanir eftir dagsetningu og tíma.  

## <a name="about-activity-logs"></a>Um aðgerðakladda
Á sumum síðum í [!INCLUDE [prod_short](includes/prod_short.md)] er hægt að skoða aðgerðarkladda sem sýnir stöðu og allar villur úr skrám sem þú flytur út úr eða flytur inn í [!INCLUDE [prod_short](includes/prod_short.md)].  

### <a name="working-with-activity-logs"></a>Vinna með aðgerðakladda
Upplýsingarnar eru birtar á síðunni **Aðgerðarkladdi** í samræmi við samhengið sem þær eru opnaðar úr. Til dæmis er hægt að opna síðuna á síðunum **Uppsetning skjalaskiptaþjónustu**, **Skjal á innleið**, **Bókaður sölureikningur** og **Bókaður sölukreditreikningur**. Hægt er að tæma listann yfir kladdafærslur eða hreinsa lista yfir færslur sem eru eldri en sjö daga.  

## <a name="monitoring-sensitive-fields"></a>Fylgst með viðkvæmum reitum
Að halda viðkvæmum gögnum öruggum tryggja persónuvernd er mikilvægt flestum fyrirtækjum. Til að bæta við öryggisstigi er hægt að fylgjast með mikilvægum reitum og verið látin vita í tölvupósti þegar einhver breytir gildi. Til dæmis gætirðu viljað fá tilkynningu ef einhver breytir IBAN-númeri fyrirtækisins.

> [!NOTE]
> Að senda tilkynningu í tölvupósti krefst þess að eiginleiki tölvupósts verði settur upp í [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar eru í [Setja upp tölvupóst](admin-how-setup-email.md).

### <a name="setting-up-field-monitoring"></a>Uppsetning reitarvöktunar
Hægt er að nota uppsetningarleiðbeiningar **Uppsetning á breytingavöktun reits** með hjálp til að tilgreina reitina sem á að fylgjast með samkvæmt síuskilyrði á borð við flokkun gagnatrúnaðar fyrir reitina. Nánari upplýsingar er að finna í [Flokkun á gagnatrúnaðar](admin-classifying-data-sensitivity.md). Leiðarvísirinn gerir einnig kleift að tilgreina þann sem fær tölvupóststilkynningu þegar breyting á sér stað, og tölvupóstsreikninginn sem sendir tilkynninguna í tölvupósti. Tilgreina verður bæði notandann sem fær tilkynningu og reikninginn sem tilkynningin verður send frá. Eftir að leiðarvísinum er lokið er hægt að vinna með stillingar fyrir reitavöktun á síðunni **Uppsetning reitavöktunar**. 

Með tímanum stækkar listinn yfir færslur á síðunni **Kladdafærslur reitavöktunar**. Til að draga úr fjölda færslna er hægt að stofna varðveislureglu sem eyðir færslum eftir tiltekinn tíma. Frekari upplýsingar er að finna í [Skilgreina varðveislureglur](admin-data-retention-policies.md).

Þegar settur er upp reitavöktun eða einhverju er breytt í uppsetningunni, eru færslur stofnaðar fyrir breytingarnar. Hægt er að tilgreina hvort birta eigi færslur sem tengjast uppsetningu vöktunar með því að sýna eða fela þær. 

Hægt er að stjórna stillingum fyrir reitavöktun, t.d. hvort senda eigi tilkynningu í tölvupósti eða bara skrá breytinguna, fyrir hvern reit á síðunni **Vinnublað vaktaðra reita**. Á þessari síðunni er einnig hægt að bæta við eða fjarlægja vaktaða reiti.

> [!NOTE]
> Þegar búið er að skrá einn eða fleiri rieti og hefja vöktun þarf að skrá sig út úr [!INCLUDE[prod_short](includes/prod_short.md)] og skrá sig inn aftur til að stillingarnar taki gildi.

### <a name="working-with-field-monitoring"></a>Vinna með reitarvöktun

Færslur fyrir öll breytt gildi í vöktuðum reitum eru tiltækar á síðunni **Kladdafærslur vaktaðra reita**. Til dæmis, færslur innihalda upplýsingar á borð við reitinn þar sem gildinu var breytt, upphaflega og nýja gildið, og hver gerði breytinguna og hvenær hún var gerð. Til að rannsaka breytingu frekar þarf að velja gildi til að opna síðuna þar sem hún var gerð. Til að skoða lista yfir allar færslur skal velja **Breytingafærslur reita**.

### <a name="viewing-field-monitoring-telemetry"></a>Skoða fjarmælingu reitarvöktunar 

Hægt er að setja upp [!INCLUDE[prod_short](includes/prod_short.md)] til að senda aðgerðir reitarvörpunar í Application Insights tilfang í Microsoft Azure. Síðan er hægt að nota Azure Monitor til að búa til skýrslur og setja upp viðvaranir í söfnuðum gögnum. Frekari upplýsingar eru í eftirfarandi greinum í [!INCLUDE[prod_short](includes/prod_short.md)] Developer og IT Pro Help:

- [Fylgjast með og greina fjarmælingar - Virkja Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-overview#enable)
- [Greining fjarmælinga reitarvöktunar](/dynamics365/business-central/dev-itpro/administration/telemetry-field-monitoring-trace)

## <a name="defining-retention-policies"></a>Varðveislureglur skilgreindar

Hægt er að búa til varðveislureglur til að eyða ónauðsynlegum gögnum í klöddum eftir tiltekinn tíma sem gefa skal upp. Til dæmis getur fjærslufjöldinn í kladda aukist með tímanum. Með því að hreinsa upp eldri færslur er auðveldara að setja athyglina á nýlegri og líklega meira viðeigandi færslur. Frekari upplýsingar er að finna í [Skilgreina varðveislureglur](admin-data-retention-policies.md).

## <a name="see-also"></a>Sjá einnig
[Grunnstillingum breytt](ui-change-basic-settings.md)  
[Röðun, leit, og síun](ui-enter-criteria-filters.md)  
[Finndu síður og upplýsingar með Viðmótsleit](ui-search.md)  
[Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md)    
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Skilgreina varðveislureglur](admin-data-retention-policies.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
