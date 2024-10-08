---
title: Samþætta við Microsoft Dynamics 365 Field Service
description: Samþætta Business Central við reitaþjónustu.
ms.date: 02/21/2024
ms.topic: article
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.custom: bap-template
---

# <a name="integrate-with-microsoft-dynamics-365-field-service"></a>Samþætta við Microsoft Dynamics 365 Field Service

Þjónustufyrirtæki krefjast framvirkrar jöfnunar þar sem fjárhagslegar birgðir og innkaup eru þétt hjónuð með þjónustuafhendingu. Þau búa til fjárhagsleg gögn með öllum færslum. Sérhver verkbeiðni táknar kostnað og tekjur og sérhver forði býr til hagnað og tap. Viðskiptamannasamskiptum er bætt við færslum í fjárhagur. Samþættingin milli [!INCLUDE [prod_short](includes/prod_short.md)] og [!INCLUDE [field-service-short](includes/field-service-short.md)] straumlínulaga ferlið til lokaaðgerða við stjórnun þjónustuaðgerða og tryggir slétt upplýsingaflæði milli kerfanna tveggja.  

Auðvelt er að stofna og stjórna vinnupöntunum í [!INCLUDE [field-service-short](includes/field-service-short.md)], rekja framvindu þjónustuverka, úthluta forða og safna upplýsingum um notkun. Þegar lokið er við verkbeiðni gerir [!INCLUDE [field-service-short](includes/field-service-short.md)] samþættingin mögulega slétta yfirfærslu gagna til frekari [!INCLUDE [prod_short](includes/prod_short.md)] vinnslu.  

Samþættingin auðveldar einnig reikningsfærslu og uppfyllingu vinnupantana [!INCLUDE [prod_short](includes/prod_short.md)]. Hægt er að búa til nákvæma reikninga á grundvelli þjónustuaðgerða og notkunarinnar sem skráð er í [!INCLUDE [field-service-short](includes/field-service-short.md)].  

Með því að samþætta [!INCLUDE [prod_short](includes/prod_short.md)] við [!INCLUDE [field-service-short](includes/field-service-short.md)] þarf ekki að færa inn gögn handvirkt eða tvítekin viðleitni. Samþætting býður einnig upp á yfirgripsmikið yfirlit yfir þjónustuaðgerðir og fjármál, sem gerir betri ákvarðanatöku og rekstrarskilvirkni.

## <a name="prerequisites"></a>Frumskilyrði

Vegna þess að [!INCLUDE [field-service-short](includes/field-service-short.md)] byggt er efst á Dynamics 365 Sala verður að [setja upp tengingu við Dataverse](/dynamics365/business-central/admin-how-to-set-up-a-dynamics-crm-connection#to-use-the-dataverse-connection-setup-assisted-setup-guide) og [virkja samþættingu við Dynamics 365 Sala](/dynamics365/business-central/admin-prepare-dynamics-365-for-sales-for-integration#connection-settings-in-the-setup-guide).

Sækja þarf forritið Þjónustuheildunarforrit reita og [AppSource](https://go.microsoft.com/fwlink/?linkid=2277917) setja það upp í [!INCLUDE [prod_short](includes/prod_short.md)].

### <a name="permissions-and-security-roles-for-user-accounts"></a>Heimildir og öryggishlutverk notendareikninga

Þegar samþættingarlausnin er sett upp eru heimildir fyrir notandareikning samþættingar grunnstilltar. Ef heimildirnar breytast gæti þurft að endurstilla þær. Til að gera það skal setja samþættingarlausnina upp aftur af síðunni **Uppsetning Dynamics 365 með** því að velja **Samþættingarlausnina** Endurvirkjun. Hér á eftir eru taldar upp heimildir og öryggishlutverk sem lausnin nýtir fyrir hvert forrit.

#### <a name="sales"></a>Sölur

* Dynamics 365 [!INCLUDE [prod_short](includes/prod_short.md)] samþættingarstjóri
* Dynamics 365 [!INCLUDE [prod_short](includes/prod_short.md)] samþættingarnotandi
* Notandi Dynamics 365 [!INCLUDE [prod_short](includes/prod_short.md)] til ráðstöfunar

#### <a name="business-central"></a>Business Central

Notendur sem bóka verkbækur verða að hafa eftirfarandi heimildasamstæða:

* Dynamics 365 Söluheildun

#### <a name="field-service"></a>Field Service

Ef nota á samþætt gögn verða notendur að hafa eftirfarandi öryggishlutverk:

* Þjónustuheildun Business Central reits

Notendur verða til dæmis að hafa þetta hlutverk til að tengja vinnupantanir við til [!INCLUDE [prod_short](includes/prod_short.md)] vinnslu.

> [!NOTE]
> Tryggja að notendum sé úthlutað á stöðluð öryggishlutverk og forstillingar í [!INCLUDE [field-service-short](includes/field-service-short.md)].  
>
> Nánari upplýsingar um öryggisforstillingar dálka eru í [!INCLUDE [field-service-short](includes/field-service-short.md)] [öryggishlutverkum](/dynamics365/field-service/users-licenses-permissions#field-service-security-roles) Field Service.
>
> Stjórnendur verða að bæta við viðeigandi dálkaöryggisforstillingum við notendur í Power Platform. Nánari upplýsingar eru opnaðar með því að fara í [Bæta við teymum eða notendum í dálkaöryggissnið til að stjórna aðgangi](/power-platform/admin/add-teams-users-field-security-profile).

> [!NOTE]
> Til að nota aðgerðina **Opið í Business Central** í Sölu þarf að hafa eftirfarandi heimildir fyrir eftirfarandi töflur:
>
> * Lesheimildir fyrir töfluna **Tenging**  (nav_connection) verða að vera **Dynamics 365 Business Central lesheimildir** .
> * Notandi verður að hafa **les**-, **skrif**- og **eyða** heimildum fyrir töfluna **Sjálfgefna Dynamics 365 Business Central tengingu**  (nav_defaultconnection).

### <a name="other-settings-in-field-service"></a>Aðrar stillingar í Reitaþjónusta

Á síðunni **Stilling** reitaþjónustu eru eftirfarandi breytingar gerðar:

*  **Á flipanum Innkaup** er reiturinn **Notkun vara úr birgðunum** hreinsaður. Annars er hægt að fá viðvörun um "úr birgðum" þegar valin er vara sem er ekki á lager í [!INCLUDE [field-service-short](includes/field-service-short.md)], en er á lager. [!INCLUDE [prod_short](includes/prod_short.md)]
*  **Á flipanum verkbeiðni / Bókun** skal slökkva á vífærslnunum **Reikna verð** og **Reikna kostnað** . Í reitnum **verkbeiðni Stofnreikningur** er Aldrei **valið**.

> [!NOTE]
> Uppsetning tenginga til að [!INCLUDE [field-service-short](includes/field-service-short.md)] fjarlægja tengingu milli forða og vara. Til að gera [!INCLUDE [prod_short](includes/prod_short.md)] vörur tiltækar þarf [!INCLUDE [field-service-short](includes/field-service-short.md)] að uppfæra reitinn Vörutegund reits **til samræmis við reitinn** Tegund **varanna** í [!INCLUDE [prod_short](includes/prod_short.md)]. Nánari upplýsingar eru notaðar til að [stofna vöru eða þjónustu](/dynamics365/field-service/create-product-or-service#create-a-product-or-service).

## <a name="set-up-the-integration-in-business-central"></a>Setja upp samþættingu í Business Central

Þegar sambandi við Dataverse og Sala hefur verið tengt við er hægt að setja upp samþættingu við [!INCLUDE [field-service-short](includes/field-service-short.md)].

* Sækja og setja upp forritið Þjónustuheildun reita úr [AppSource](https://go.microsoft.com/fwlink/?linkid=2277917). Á síðunni **Viðbótastjórnun** skal finna forritið Þjónustuheildun reita og velja **setja upp** aðgerð til að keyra leiðsagnarforritið leiðsagnarforrit fyrir aðstoð.
* Á síðunni **Aðstoðargrunnur** í [!INCLUDE [prod_short](includes/prod_short.md)] skal velja **Setja upp samþættingu til að Dynamics 365 Field Service** keyra leiðsagnarforritið með aðstoð.

Í þessum hluta er lýst lykilstillingum í handbókinni.

Til að láta fólk bóka notkun á vörum og þjónustu í [!INCLUDE [field-service-short](includes/field-service-short.md)] vinnupöntunum skal tilgreina **sniðmát** verkbókar og **Verkbókarkeyrslu til** að nota til að bóka notkun á vörum og þjónustu.

Þar sem þjónusta er sýnd í [!INCLUDE [field-service-short](includes/field-service-short.md)] tímalengd skal tilgreina **tímamælieininguna** sem á að nota til að breyta lengd í magn í [!INCLUDE [prod_short](includes/prod_short.md)].

Einnig er hægt að tilgreina hvenær verkbeiðni vörur og þjónustulínur samstilla við [!INCLUDE [prod_short](includes/prod_short.md)]. Til dæmis er hægt að samstilla hvenær verkbeiðni línur eru notaðar eða þegar einhver lýkur verkbeiðni. Velja skal viðeigandi valkost í reitnum **Samstilla verkbeiðni vörur/þjónustu** .

Þegar vörur og þjónusta verkbeiðni samstilla við verkbók í [!INCLUDE [prod_short](includes/prod_short.md)] er hægt að velja hvort bóka eigi verkbækur handvirkt. Velja skal viðeigandi valkost í reitnum **Bóka verkbókarlínur** sjálfvirkt:

* Þegar verkbeiðni er lokið.
* Þegar verkbeiðni vörur eða þjónusta eru notuð.

Þegar uppsetningunni hefur verið lokið er keyrð full samstilling á síðunni **Dynamics 365 Field Service Samþættingargrunnur** . Þessi aðgerð samstillir töfluvörpun fyrir hluti eins og:

* Verkhlutar verka með tengja **stilla Beita** notkun. Þessi samstilling gerir [!INCLUDE [prod_short](includes/prod_short.md)] verk tiltæk fyrir val í [!INCLUDE [field-service-short](includes/field-service-short.md)].
* Forði sem ekki er lokaður, hafa ekki **valið Nota vinnuskýrslu** og hafa **Klukkustundir** tilgreindar sem mælieiningu á síðunni **Dynamics 365 Field Service Uppsetning** samþættingar.
* Þjónustuvörur (krefst notkunar iðgjaldsupplifunarinnar [!INCLUDE [prod_short](includes/prod_short.md)]).

## <a name="standard-field-service-entity-mapping-for-synchronization"></a>Staðlaður reitaþjónustueining vörpun fyrir samstillingu

Grunnur samstillingargagna er vörpun töflum og reitum með [!INCLUDE [prod_short](includes/prod_short.md)] töflum og dálkum í Dataverse svo að þau geti skipst á gögnum. Vörpun gerist í samþættingartöflum. Nánari upplýsingar um töfluvörpun er farið [í vörpun Töflur og Reitir til að samstilla](/dynamics365/business-central/admin-how-to-modify-table-mappings-for-synchronization).

Samþætting við [!INCLUDE [field-service-short](includes/field-service-short.md)] kynnir eftirfarandi staðlaðar samþættingartafla vörpun:

* **PJLINE-WORDERPRODUCT** - Kort verkbeiðni vörur í í [!INCLUDE [field-service-short](includes/field-service-short.md)] verkbókarlínur í [!INCLUDE [prod_short](includes/prod_short.md)].
* **PJLINE-WORDERSERVICE** - Maps verkbeiðni þjónustu í í [!INCLUDE [field-service-short](includes/field-service-short.md)] verkbókarlínum í [!INCLUDE [prod_short](includes/prod_short.md)].
* **PROJECTTASK** - Varpar verkum og verkhlutum í [!INCLUDE [prod_short](includes/prod_short.md)] afurðir í ytri verkum í [!INCLUDE [field-service-short](includes/field-service-short.md)].
* **FORÐI-BÓKFÆRANLEGRSC** - Varpar forða í á [!INCLUDE [prod_short](includes/prod_short.md)] bókhæfan forða í [!INCLUDE [field-service-short](includes/field-service-short.md)].
* **SVCITEM-CUSTASSET** - (Aðeins premium Experience) Varpar þjónustuvörum í [!INCLUDE [prod_short](includes/prod_short.md)] á eignir viðskiptavina í [!INCLUDE [field-service-short](includes/field-service-short.md)].

## <a name="use-data-in-both-applications"></a>Nota gögn í báðum forritum

Eftirfarandi hlutar lýsa aðgerðunum þar sem hægt er að nota gögnin sem fylgja [!INCLUDE [prod_short](includes/prod_short.md)] og [!INCLUDE [field-service-short](includes/field-service-short.md)].

### <a name="field-service-1"></a>Field Service

Hægt er [að stofna vinnupantanir](/dynamics365/field-service/create-work-order) með því að nota **þjónustureikninginn** og **reikningsfærslureikninginn**  [!INCLUDE [prod_short](includes/prod_short.md)]. Á vinnupöntunum þarf að velja **Business Central Project Task** í reitnum **Utanaðkomandi verkefni** . Með því að velja verk er hægt að samstilla verkbeiðni vörur og þjónustu við viðeigandi verkhluta í [!INCLUDE [prod_short](includes/prod_short.md)].

Hægt er að bæta við birgðum og utanbirgðavörum eins og **verkbeiðni Vörur** á vinnupöntunum og fá tiltækt magn og kostnað og verð [!INCLUDE [prod_short](includes/prod_short.md)]. Til að fá nánari upplýsingar er farið í [Stofna verkbeiðni úr verkbeiðni skjámyndinni og færslulistanum](/dynamics365/field-service/create-work-order#create-a-work-order-from-the-work-order-form-and-record-list).

Hægt er að bæta við vörum af gerðinni þjónusta sem **verkbeiðni Þjónusta** og sækja kostnað og verð frá [!INCLUDE [prod_short](includes/prod_short.md)]. Farðu á flipann [Vörur og þjónustu til að](/dynamics365/field-service/work-order-experience#products-and-services-tab) fá nánari upplýsingar.

> [!NOTE]
> Þegar staða vöru eða þjónustu í verkbeiðni breytist úr **Áætlað**  **í Notað** í [!INCLUDE [field-service-short](includes/field-service-short.md)] samstilla þeir við verkbókarlínur í [!INCLUDE [prod_short](includes/prod_short.md)].

Þú getur bókað forða og tengt Bókanir **við verkbeiðni þjónustu með því að nota bókhæfan** forða **.**  [!INCLUDE [prod_short](includes/prod_short.md)]

### <a name="business-central-1"></a>Business Central

Það fer eftir stillingunum á síðunni **Samþættingargrunnur** reita, þegar vinnupantanir innihalda vörur og þjónustu, eru notkunarupplýsingar fluttar og bókaðar með **verkbók** í [!INCLUDE [prod_short](includes/prod_short.md)].

Gildin **Magn til reikningsfærslu** og **Tímalengd í reikningsfærslu** eru afrituð í reitinn **Magn til flutnings á reikning** . Á grundvelli þessara gilda er hægt að stofna og bóka sölureikninga á [!INCLUDE [prod_short](includes/prod_short.md)] til að reikningsfæra viðskiptavininn. Þegar reikningurinn hefur verið bókaður eða notkun er unnin í [!INCLUDE [prod_short](includes/prod_short.md)] birtast reikningsfært magn og notað magn á [!INCLUDE [prod_short](includes/prod_short.md)]  **flipanum verkbeiðni Vara** og **verkbeiðni Þjónustusíður** .  

Nota síðuna **Áætlunarlínur** verkefnis til að rekja bókun og reikningsfærslu notkunar á vinnupöntunum. Af síðunni **Áætlunarlínur** verkefnis er hægt að stofna og bóka sölureikninga í [!INCLUDE [prod_short](includes/prod_short.md)]. Síðan er hægt að samstilla þá við og fylgjast með [!INCLUDE [field-service-short](includes/field-service-short.md)] stöðu reikninganna.

> [!NOTE]
> Verkbeiðni þjónustu við bókun sem notar bókhæfan forða sem er paraður [!INCLUDE [prod_short](includes/prod_short.md)] við forða samstilla við tvær verkbókarlínur: ein lína af tegundinni **Áætlun** fyrir paraða forðann og önnur lína af tegundinni **Reikningshæft** fyrir vöruna sem verið er að þjónusta.
>
> Varan sem valin er á verkbeiðni þjónustu verður að vera paruð við vöru af tegundinni **Þjónusta** í [!INCLUDE [prod_short](includes/prod_short.md)]. Einnig þarf grunnmælieiningin fyrir vöruna að vera stillt á **tímamælieininguna** sem valin er á síðunni **Dynamics 365 Field Service Samþættingargrunnur** .
>
> Hægt er að stofna reikning fyrir vöru af tegundinni **Þjónusta** úr reikningshæfu verkáætlunarlína og nota áætlunina verkáætlunarlína til að skrá kostnað við forðann.

## <a name="see-also"></a>Sjá einnig .

[Samþætta við Microsoft Dataverse með samstillingu gagna](admin-common-data-service.md)  
[Vörpun á töflum og reitum fyrir samstillingu](admin-how-to-modify-table-mappings-for-synchronization.md)
