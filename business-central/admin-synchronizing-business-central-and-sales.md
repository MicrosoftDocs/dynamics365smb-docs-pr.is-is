---
title: Samstilling og samþætting gagna
description: Samstillingin afritar gögn milli tafla Microsoft Dataverse og Business Central og heldur gögnunum í báðum kerfum uppfærðum.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 05/07/2024
ms.custom: bap-template
ms.search.keywords: 'Dataverse, integration, sync, synchronize, mapping'
ms.saerch.form: 5372_Primary
ms.service: dynamics-365-business-central
---

# Samstilling gagna í Business Central við Microsoft Dataverse

Við samþættingu [!INCLUDE[prod_short](includes/cds_long_md.md)] við [!INCLUDE[prod_short](includes/prod_short.md)] er hægt að ákveða hvort eigi að samstilla gögn á völdum svæðum [!INCLUDE[prod_short](includes/prod_short.md)] (t.d. viðskiptamenn, tengiliðir og sölumenn) við samsvarandi línur í [!INCLUDE[prod_short](includes/cds_long_md.md)] (s.s. reikningar, tengiliðir og notendur). Háð gerðar línu, er hægt að samstilla gögn úr [!INCLUDE[prod_short](includes/cds_long_md.md)] við [!INCLUDE[prod_short](includes/prod_short.md)] eða öfugt. Frekari upplýsingar er að finna í [Samþætting við Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).  

Samstilling notar eftirfarandi einingar:

* Vörpun samþættingartöflu
* Varpanir samþættingarreits
* Samstillingarreglur
* Tengdar færslur

Þegar samstilling er sett upp geturðu tengt færslur [!INCLUDE[prod_short](includes/prod_short.md)] við línur [!INCLUDE[prod_short](includes/cds_long_md.md)] til að samstilla gögn þeirra. Þú getur byrjað samstillingu handvirkt eða samkvæmt áætlun. Eftirfarandi tafla veitir yfirlit yfir leiðir til að samstilla.  

|  Tegund  |  Aðferð  |  Sjá  |  
|--------|----------|-------|  
|Handvirk samstilling|Samstilla línu fyrir línu.<br /><br /> Hægt er að samstilla einstakar færslur í [!INCLUDE[prod_short](includes/prod_short.md)], t.d. viðskiptamann, við samsvarandi línu [!INCLUDE[prod_short](includes/cds_long_md.md)], t.d. reikning. Svona koma notendur venjulega til með að vinna með [!INCLUDE[prod_short](includes/cds_long_md.md)]-gögn í [!INCLUDE[prod_short](includes/prod_short.md)].|[Tengja og samstilla færslur handvirkt](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
|  |Samstilla á grunni töfluvörpunar.<br /><br /> Hægt er að samstilla allar færslur í [!INCLUDE[prod_short](includes/prod_short.md)]-töflu með [!INCLUDE[prod_short](includes/cds_long_md.md)]-töflu.|[Samstilla einstakar töfluvarpanir](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
||Samstilla allar breyttar færslur fyrir allar töfluvarpanir.<br /><br /> Hægt er að samstilla allar færslur sem hefur verið breytt í [!INCLUDE[prod_short](includes/prod_short.md)]-töflum frá síðustu samstillingu.|[Samstilling á öllum breyttum færslum](admin-manual-synchronization-of-table-mappings.md#synchronizing-all-modified-records)|
||Full samstilling allra gagna fyrir allar töfluvarpanir.<br /><br /> Hægt er að samstilla öll gögn í [!INCLUDE[prod_short](includes/prod_short.md)]-töflum og [!INCLUDE[prod_short](includes/cds_long_md.md)]-töflum sem er varpað, og stofna nýjar færslur eða línur í lausn viðtökustaðar fyrir ótengdar færslur í lausn upprunastaðar.<br /><br /> Full samstilling samstillir öll gögn og hunsar tengingu. Venjulega er gerð full samstilling þegar samþætting er sett upp og aðeins ein lausnin inniheldur gögn. Full samstilling getur einnig verið gagnleg í sýniumhverfi.|[Keyra fulla samstillingu](admin-manual-synchronization-of-table-mappings.md#run-a-full-synchronization)|  
|Áætluð samstilling|Samstilla allar breytingar á gögnum fyrir allar töfluvarpanir.<br /><br /> Hægt er að samstilla [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)] með áætluðu millibili með því að setja upp verk í verkröðinni.|[Áætla samstillingu](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)|  

> [!NOTE]
> Samstillingin á milli [!INCLUDE[prod_short](includes/cds_long_md.md)] og [!INCLUDE[prod_short](includes/prod_short.md)] byggir á tímasettir keyrslu á verkraðarfærslum og tryggir ekki samræmi rauntímagagna milli þjónustanna tveggja. Fyrir samræmi í rauntímagögnum ættirðu að skoða [Sýndartöflur Business Central](/dynamics365/business-central/dev-itpro/powerplatform/powerplat-overview) eða Business Central API.   

## Staðlaður töfluvörpun fyrir samstillingu

Töflur í [!INCLUDE[prod_short](includes/cds_long_md.md)], t.d. reikningar, eru samþættar við jafngildar gerðir af töflum í [!INCLUDE[prod_short](includes/prod_short.md)], t.d. viðskiptavini. Til að vinna með [!INCLUDE[prod_short](includes/cds_long_md.md)]-gögn eru tenglar settir upp, kallast tengingar, milli tafla í [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)].

Eftirfarandi töflur birta staðlaða vörpun milli tafla í [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)].

> [!TIP]
> Hægt er að endurstilla breytingar á grunnstillingu sem gerðar voru á vörpunum samþættingartöflu og reita í sjálfgefnar stillingar með því að velja varpanirnar og velja síðan **Nota sjálfgefinn samstillingargrunn**.

| [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)] | Stefna samstillingar | Sjálfgefin sía |
|---------------------------------------------|----------------------------------------------|---------------------------|----------------|
| Sölumaður/innkaupaaðili | Notandi | [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)] tengiliðasía: **Staða** er **Nei**, **Notandi með leyfi** er **Já**, stilling samþættingarnotanda er **Nei** |
| Viðskiptamaður | Reikningur | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)] reikningssía: **Gerð vensla** er **Viðskiptavinur** og **Staða** er **Virkur**. [!INCLUDE[prod_short](includes/prod_short.md)] sía: **Lokað** er autt (viðskiptavinur er ekki útilokaður). |
| Lánardrottinn | Reikningur | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)] afmörkun á reikningi: **Venslagerð** er **Lánardrottinn** og **Staða** er **Virk**. [!INCLUDE[prod_short](includes/prod_short.md)] sía: **Lokað** er autt (lánardrottinn er ekki útilokaður). |
| Tengiliður | Tengiliður | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/prod_short.md)] tengiliðasía: **Gerð** er **Einstaklingur** og tengilið er úthlutað á fyrirtæki. [!INCLUDE[prod_short](includes/cds_long_md.md)] tengiliðasía: Tengiliðnum er úthlutað á fyrirtæki og yfireining viðskiptamannsgerðar er **Viðskiptamaður** |
| Gjaldmiðill | Gjaldmiðill færslu | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] |  |

> [!NOTE]
> **Dataverse** aðgerðirnar verða ekki tiltækar á síðum, til dæmis síðu viðskiptamannaspjalds, fyrir færslur sem virða ekki töflusíuna á vörpun samþættingartöflu.

### Ábending um stjórnendur: skoðun töfluvörpunar

Hægt er að skoða vörpunina milli tafla í [!INCLUDE[prod_short](includes/cds_long_md.md)] og í [!INCLUDE[prod_short](includes/prod_short.md)] á síðunni **Vörpun samþættingartöflu** þar sem einnig er hægt að nota afmarkanir. Skilgreining á vörpun milli reita í [!INCLUDE[prod_short](includes/prod_short.md)]-töflum og dálka í [!INCLUDE[prod_short](includes/cds_long_md.md)]-töflum á síðunni **Vörpun samþættingarreits** þar sem hægt er að bæta við viðbótarreglum fyrir vörpun. Þetta getur til dæmis verið gagnlegt ef nauðsynlegt er að úrræðaleita samstillingu.

## Nota sýndartöflur til að fá fleiri gögn

Þegar samþætting er sett upp er hægt að nota sýndartöflur til að gera fleiri gögn tiltæk í [!INCLUDE[prod_short](includes/cds_long_md.md)] án hjálpar frá hönnuði.

Sýndartafla er sérsniðin tafla með dálkum og línum sem innihalda gögn úr ytri gagnagjafa, t.d [!INCLUDE [prod_short](includes/prod_short.md)]. Dálkarnir og línur í sýndartafla líta út eins og venjuleg tafla en gögnin eru hins vegar ekki geymd í rauntöflu í gagnagrunninum [!INCLUDE[prod_short](includes/cds_long_md.md)] . Þess í stað eru gögnin sótt við keyrslutíma.

> [!NOTE]
> [!INCLUDE [prod_short](includes/prod_short.md)] inniheldur hluti sem einnig eru kallaðar sýndartöflur. Þessir töfluhlutir eru ekki tengdir sýndartöflunum sem notaðar eru með [!INCLUDE[prod_short](includes/cds_long_md.md)].

Til að fræðast meira um sýndartöflur er farið í eftirfarandi greinar:

* [Stofna og breyta sýndartöflum sem innihalda gögn frá ytri gagnagjafa](/power-apps/maker/data-platform/create-edit-virtual-entities)  (Power Apps fylgiskjöl)
* [Business Central sýndartafla fyrir Microsoft Dataverse Admin Reference](/dynamics365/business-central/dev-itpro/powerplatform/powerplat-admin-reference) ([!INCLUDE [prod_short](includes/prod_short.md)] documentation)

Til að nota sýndartöflur verður að setja forritið **Business Central sýndareining** upp úr [AppSource](https://appsource.microsoft.com/en-US/product/dynamics-365/microsoftdynsmb.businesscentral_virtualentity). 

Þegar forritið hefur verið sett upp getur þú gert sýndartöflur virkar á einni af eftirfarandi síðum í [!INCLUDE [prod_short](includes/prod_short.md)]:

* Þegar uppsetningarleiðbeiningar með aðstoð við tengingu **eru keyrðar Dataverse** er hægt að nota **Dataverse síðuna Tiltækar sýndartöflur** til að velja margar sýndartöflur. Síðan eru töflurnar tiltækar í [!INCLUDE[prod_short](includes/cds_long_md.md)] og PowerApps Maker Portal. 
* Frá síðunum **Dataverse Uppsetning** tengingar, **Sýndartöflum** og **Tiltækum** sýndartöflum.  
* Frá Power App Maker Portal.

## Samstilla gögn frá mörgum fyrirtækjum eða umhverfi

Hægt er að samstilla gögn frá mörgum [!INCLUDE [prod_short](includes/prod_short.md)] fyrirtækjum eða umhverfi við [!INCLUDE[prod_short](includes/cds_long_md.md)] umhverfi. Í samstillingaraðstæðum í mörgum fyrirtækjum er ýmislegt sem þarf að íhuga.

### Stilla kenni fyrirtækis

Þegar færslur eru samstilltar setjum við kenni fyrirtækis á eininguna [!INCLUDE[prod_short](includes/cds_long_md.md)] til að útskýra fyrirtækið [!INCLUDE [prod_short](includes/prod_short.md)] sem færslurnar komu frá. Samþættingartafla vörpun hefur samþættingartafla afmörkunarreiti sem taka fyrirtækiskennið með í reikninginn. Til að hafa töfluvörpun með í uppsetningu margra fyrirtækja skal **velja** gátreitinn Samstilling **með mörgum fyrirtækjum á samþættingartafla vörpun**  síðunni. Stillingin bestar hvernig samþættingartafla afmarka reiti afmarka kenni fyrirtækis í uppsetningu margra fyrirtækja.

Fyrir samþættingartafla vörpun sem samstilla skjöl, t.d. pantanir, tilboð og tækifæri, ef gátreiturinn Samstilling **með mörgum fyrirtækjum er valinn** tekur samþættingin aðeins tillit til eininga sem eru með fyrirtækiskenni gildandi [!INCLUDE [prod_short](includes/prod_short.md)] fyrirtækis. Til að samstilla skjöl, t.d. milli Business Central og Sales, verða notendur í Sölu að tilgreina kenni fyrirtækis á skjölunum. Annars samstillast skjölin ekki.  

Ef um allar aðrar samþættingartafla vörpun er að velja **gátreitinn Samstilling** með mörgum fyrirtækjum virk fjarlægir afmörkunina á kenni fyrirtækis. Samstillingin tekur tillit til tengdra eininga, óháð kenni fyrirtækis þeirra.

### Tilgreina stefnu samstillingar

Ef stuðningur við mörg fyrirtæki er virkjaður í samþættingartafla vörpun er mælt með því að stefna vörpun á **FromIntegration**. Ef stefnan er stillt á **ToIntegration** eða **Bidirectional** er gott hugmynd að nota **töfluafmörkun og**  samþættingartafla afmörkun **til** að stjórna því hvaða einingar samstilla við hvaða fyrirtæki. Það er einnig gott hugmynd að nota samsvörunargrundvöll til að koma í veg fyrir að tvíteknar færslur séu búnar til. Nánari upplýsingar um samsvörun er að [finna í Sérstilla samsvörunarmiðaða jöfnun](/dynamics365/business-central/admin-how-to-set-up-a-dynamics-crm-connection#customize-the-match-based-coupling).

### Nota einkvæm númer

Ef númeraröðin tryggir ekki að aðallykilgildi séu einstök hverju fyrirtæki er mælt með því að forskeyti séu notuð. Til að hefja notkun forskeyta skal stofna umbreytingarreglu í vörpun samþættingarreitnum. Hægt er að fá nánari upplýsingar um breytingareglur með því að [fara í Afgreiða mismun í reitagildum](admin-how-to-modify-table-mappings-for-synchronization.md#handle-differences-in-field-values).

## Sjá einnig .  

[Tengja og samstilla færslur handvirkt](admin-how-to-couple-and-synchronize-records-manually.md)   
[Áætla samstillingu](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[Samþætting við Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
