---
title: Tímasetja verk til að keyrast sjálfvirkt
description: Fræðast um notkun verkraðarfærslna til að keyra skýrslur og codeunit.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 04/29/2024
ms.custom: bap-template
ms.search.form: '672, 673, 674, 671'
ms.service: dynamics-365-business-central
---
# <a name="use-job-queues-to-schedule-tasks"></a>Nota verkröð til að tímasetja verk

Nota síðuna **Verkraðarfærslur** til að tímasetja og keyra tilteknar skýrslur og codeunit. Stilla má verk svo þau keyri einu sinni eða endurtekið. Til dæmis gætirðu viljað keyra skýrsluna **Sölumaður * sölutölur** vikulega til að rekja sölu sölumanns í hverri viku eða keyra kóðaeininguna **Framselja samþykktarbeiðnir** daglega til að koma í veg fyrir að skjöl safnist upp.

Síðan **Verkraðarfærslur** birtir öll núverandi verk. Ef verkraðarfærslu sem keyrir í áætlun er bætt við verður að veita einhverjar upplýsingar. Dæmi:

* Gerð hlutar sem á að keyra, t.d. skýrsla eða kótaeining. Notandi verður að hafa heimild til að keyra skýrsluna eða kótasafnið.
* Heiti og hlutarkenni hlutarins.
* Færibreytur til að tilgreina virkni verkraðarfærslu. Til dæmis er hægt að bæta við færibreytu til að sent einungis bókaðar sölupantanir.
* Áætlunin fyrir hvenær og hversu oft verkraðarfærslan er keyrð.

> [!IMPORTANT]  
> Ef þér er úthlutað SUPER-heimildasamstæðunni sem fylgir með [!INCLUDE[prod_short](includes/prod_short.md)] hefurðu heimild til að keyra alla hluti sem eru innifaldir í leyfinu þínu. Ef um er að ræða hlutverkið Úthlutaður stjórnandi er hægt að stofna og tímasetja verkraðarfærslur en aðeins kerfisstjórar og leyfisskyldir notendur geta keyrt þær.

Þegar verki er lokið skal [!INCLUDE [prod_short](includes/prod_short.md)]  fjarlægja það af lista yfir verkraðarfærslur, nema um ítrekað verk sé að ræða. Ítrekunarverkum er reiturinn **Fyrsti upphafstími** leiðréttur þannig að hann sýni næst þegar verkið verður keyrt.

## <a name="important-for-scheduling-recurring-jobs"></a>Mikilvægt fyrir tímasetningu endurtekinna verka

> [!IMPORTANT]  
> Ítrekaðar verkraðir geta haft áhrif á afköst svo að ekki ætti að keyra þær of oft. Þegar sett er upp hversu oft eigi að keyra ítrekað verk er reynt að stilla stærsta tímabilið sem hægt er að nota. Ef til dæmis á að endurtaka fimm mínútur þarf að hafa í huga hvort það geti verið 15 mínútur eða jafnvel einu sinni á klukkustund í staðinn. Við áætlun ítrekaðra verkraða skal hafa í huga hvaða svæði forritið hefur áhrif á. Er það svæði þar sem margir notendur vinna og verða fyrir mikilli virkni? Íhuga skal lengd einnar verkkeyrslu og viðskiptahvöt fyrir keyrslu verka með tiltekinn náunga.

## <a name="the-earliest-start-date"></a>Fyrsta upphafsdagsetning

Gildið í reitnum **Fyrsta upphafsdagsetning/tími** á síðunni **Færsluspjald** verkraðar sýnir næst þegar verkið verður keyrt. Nokkrir þættir geta haft áhrif á það hvort verkraðarfærsla keyrir í raun á þeim tíma.

Algengustu þættirnir eru fjöldi verkraðarfærslna í umhverfi og heildarfjöldi áætlaðra verka. Til að verja afkastastig eru aðgerðarmörk. Ef um margar færslur er að ræða og önnur þeirra mistekst eða tekur lengri tíma en búist var við gæti næsta verk ekki hafist á áætluðum tíma. Ef til eru codeunit sem eru að búa til 100.000 eða fleiri áætluð verk ætti að athuga hvort í raun þurfi alla þessa verkhluta. Hægt er að nálgast lista yfir öll áætluð verk á síðunni **Tímasettir verkhlutar** .

Nánari upplýsingar um eftirlit með stöðu verkraðarfærslna eru í Til að [skoða stöðu fyrir hvaða verk](#to-view-status-for-any-job) sem er. Farið í Ósamstillt verkmörk til að [fræðast meira um aðgerðamörk](/dynamics365/business-central/dev-itpro/administration/operational-limits-online#Task).

## <a name="monitor-status-or-errors-in-the-job-queue"></a>Fylgjast með stöðu eða villum í verkröð

Gögn sem verkröðin býr til eru geymd svo hægt sé að ræða villur.  

Fyrir hverja verkraðarfærslu er hægt að skoða og breyta stöðunni. Við stofnun verkraðarfærslu er staða hennar stillt á **Bið**. T.d. er hægt að setja stöðuna á **Tilbúið** og svo aftur í **Í bið**. Annars eru stöðuupplýsingar uppfærðar sjálfkrafa.

Eftirfarandi tafla lýsir gildum reitsins **Staða**.

| Staða | Lýsing |
|--|--|
| Tilbúið | Verkraðarfærslan er tilbúin til keyrslu. |
| Í vinnslu | Verkraðarfærslan er í vinnslu. Þessi reitur uppfærist á meðan verkröðin er í gangi. |
| Í bið | Sjálfgefin staða verkraðarfærslu þegar hún er stofnuð. Veljið aðgerðina **Stilla stöðu í tilbúið** til að breyta stöðunni í **Tilbúið**. Veldu aðgerðina **Setja í bið** til að snúa aftur í stöðuna **Í bið**. Til að fræðast meira er farið í [Um bið](#about-on-hold).|
| Í bið vegna aðgerðaleysis | Aðallega notað fyrir verkraðarfærslur sem tímasetja samstillingu milli [!INCLUDE [prod_short](includes/prod_short.md)] og annarrar kerfis, t.d [!INCLUDE [cds_long_md](includes/cds_long_md.md)]. Hægt er að fá nánari upplýsingar um þessa stöðu með því að [fara í Tímamörk](/dynamics365/business-central/admin-scheduled-synchronization-using-the-synchronization-job-queue-entries#about-inactivity-timeouts) óvirkni. |
|Í bið | Á aðeins við um verkraðarfærslur sem úthlutað er tegundarkóta. Gefur til kynna að verkið sé áætlað en undirliggjandi áætlað verk er ekki virkt. Eftir að verkraðarfærslunni sem er í keyrslu og er í sama flokki lýkur verður staða næsta verks í flokknum með stöðuna Bíða tilbúin. |
| Villa | Eitthvað fór úrskeiðis. Veldu **Sýna villu** til að sýna villuboðin. |
| Klárað | Verkraðarfærslunni er lokið. |

 > [!TIP]  
> Verkraðarfærslur hætta að keyra þegar villa kemur upp. Þetta getur til dæmis verið vandamál þegar færsla tengist utanaðkomandi þjónustu, til dæmis bankastraumi. Ef þjónustan er ekki í boði í augnablikinu og verkraðarfærslan getur ekki tengst mun færslan sýna villu og stöðva keyrslu. Þú þarft að endurræsa verkraðarfærsluna handvirkt. Reitirnir **Hámarksfjöldi tilrauna** og **Töf á endurtekinni keyrslu (sek.)** geta hins vegar hjálpað þér að koma í veg fyrir þessar aðstæður. Reiturinn **Hámarksfjöldi tilrauna** gerir þér kleift að tilgreina hversu oft verkraðarfærsla getur mistekist áður en hún hættir að reyna að keyra. Reiturinn **Töf á endurtekinni keyrslu (sek.)** gerir þér kleift að tilgreina tímann, í sekúndum, á milli tilrauna. Samsetning þessara tveggja reita gæti haldið verkraðarfærslunni gangandi þar til ytri þjónustan verður tiltæk.

### <a name="about-on-hold"></a>Um bið

Ef færsla verkraðar er stillt á Bið **hefur það ekki áhrif á verk sem þegar er verið að** keyra. Eftir að verk hefst heldur það áfram að keyra þar til verkinu er lokið, burtséð frá þeim breytingum sem síðar hafa verið gerðar á verkraðarfærslunni, svo sem að setja hana í bið.<br><br> **Staðan Bið** er gjarnan notuð til að koma í veg fyrir að verk byrji sjálfkrafa þegar það nær áætluðum upphafstíma. Það gerir notandanum kleift að gera hlé um stundarsakir verks áður en það hefst í vinnslu. <br><br>Ef stöðva þarf eða hætta við keyrslu verks er hægt að grípa inn handvirkt í ferlið. Til dæmis er hægt að stöðva samsvarandi lotu eða vinnslu.

### <a name="to-view-status-for-any-job"></a>Til að skoða stöðu fyrir hvaða verk sem er

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verkraðarfærslur** og velja síðan viðkomandi tengil.
2. Á síðunni **Verkraðarfærslur** skal velja færslu verkraðar og síðan velja aðgerðina **Skráarfærslur**.  

> [!TIP]
> Hægt er að nota Application Insights  Microsoft Azure í til að fara yfir stöðu verkraðarfærslna til að sjá stöðu verkraðarfærslna sem byggjast á fjarmælingum. Til að [fræðast meira um fjarmælingar er farið í Eftirlit og Greining fjarmælinga](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) og [greining á Vinnsluröð Rakningarsíma](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace).

## <a name="view-scheduled-tasks"></a>Skoða áætluð verk

Síðan **Áætluð verk** í [!INCLUDE [prod_short](includes/prod_short.md)] sýnir hvaða verk eru tilbúin fyrir keyrslu í verkröðinni. Á síðunni má einnig sjá upplýsingar um fyrirtækið sem hvert verk er sett upp til að keyra í. Hins vegar er aðeins hægt að keyra verk sem merkt eru að tilheyri núverandi umhverfi.  

Til dæmis hætta öll tímasett verk ef fyrirtækið er í umhverfi sem er afrit af öðru umhverfi. Notaðu síðuna **Áætluð verk** til að stilla verk sem tilbúin til keyrslu í verkröðinni.  

> [!NOTE]
> Innri stjórnendur og notendur með leyfi geta tímasett keyrslur á verkum. Úthlutaðir stjórnendur geta sett upp og tímasett verk til að keyra, en aðeins notendur með leyfi geta keyrt þau.

## <a name="the-my-job-queue-part"></a>Verkraðarhlutinn verkraðarhlutinn minn

Hlutinn **Verkröð** mín í Mínu hlutverki sýnir verkraðarfærslurnar sem hafist voru en er ekki lokið. Að sjálfgefnu er hlutinn ekki sýndur, en þú getur bætt honum við í hlutverkamiðstöðina. Nánari upplýsingar um sérstillingu fást með því að [fara í Sérstilla vinnusvæðið](ui-personalization-user.md).  

Eftirtaldir hlutur sýnir eftirfarandi upplýsingar:

* Hvaða skjöl með auðkenninu þínu í reitnum **Úthlutað notandakenni** verið er að vinna úr eða eru í biðröð, þ.m.t. skjöl sem eru að bókast í bakgrunni. 
* Villa kom upp við bókun skjals eða í verkraðarfærslu. 

Hlutinn „Mín verkröð“ gerir þér einnig kleift að hætta við bókun skjals.

### <a name="to-view-an-error-from-the-my-job-queue-part"></a>Til að skoða villu ú hlutanum Mín verkröð

1. Í færslu með stöðuna **Villa** skal velja aðgerðina **Sýna villu**.
2. Fara skal yfir villuboðin og leysa vandann.

## <a name="examples-of-what-you-can-schedule-using-job-queue-entries"></a>Dæmi um hvað er hægt að tímasetja með því að nota verkraðarfærslur

### <a name="schedule-reports"></a>Áætla skýrslur

Hægt er að tímasetja skýrslu eða runuvinnslu þannig að hún keyri á tilteknum degi og tíma. Tímasettar skýrslur og runuvinnslur eru færðar inn í verkröð og unnar á áætluðum tíma, eins og önnur verk. Valkosturinn **Tímasetning** er valinn eftir að aðgerðin **Senda er** valin og síðan eru færðar inn upplýsingar eins og prentari, tími, dagsetning og endurtekning.  

Til að fá nánari upplýsingar um tímasetningar er farið í [Tímasetning skýrslu í Keyra](ui-work-report.md#ScheduleReport)

### <a name="schedule-synchronization-between--and-includeprod_short"></a>Tímastilla samstillingu á milli [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)]

Ef samþætt [!INCLUDE[prod_short](includes/prod_short.md)] er við [!INCLUDE[prod_short](includes/cds_long_md.md)] gerir verkröð notanda kleift að tímasetja hvenær eigi að samstilla gögn. Eftir því hvaða stefna og reglur eru skilgreindar getur færsla verkraðar búið til færslur í einu forriti til að passa við færslur í hinu. Gott dæmi er þegar þú skráir tengilið í [!INCLUDE[crm_md](includes/crm_md.md)] getur verkraðarfærslan sett upp þann tengilið fyrir þig í [!INCLUDE[prod_short](includes/prod_short.md)]. Nánari upplýsingar um tímasetningar er farið í [Tímasetning samstillingu milli Business Central og Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md).

### <a name="schedule-when-to-post-sales-and-purchase-orders"></a>Tímasetja hvenær á að bóka sölu- og innkaupapantanir

Þú getur notað verkraðarfærslur til að tímasetja viðskiptaferla á að keyra í bakgrunni. Til dæmis eru bakgrunnsverk gagnleg þegar margir notendur bóka sölupantanir samtímis, en einungis er hægt að afgreiða eina pöntun í einu. Nánari upplýsingar um bakgrunnsbókun er farið í Til að [setja upp bakgrunnsbókun með verkröðunum](ui-batch-posting.md#to-set-up-background-posting-with-job-queues).

## <a name="handle-job-queue-entry-issues"></a>Vinna með vandamál í verkraðarfærslum

Ef villa kemur upp í verkraðarfærslu er fyrsti valkosturinn til að leysa málið er að endurræsa verkraðarfærsluna. Hægt er að stilla stöðu verkraðarfærslunnar **á Bið** og síðan **á Tilbúið** eða endurræsa hana bara.

Ef endurræsing hjálpar ekki gæti það verið í kótanum. Finna má eiganda (einnig kallaður *útgefandi*) kótans í AL-staflarakningunni í verkraðarkladdanum. Ef villan kemur úr forriti/viðbót skal hafa samband við Microsoft-samstarfsaðilann. Ef villan kemur úr Microsoft-forriti er stuðningsbeiðni opnuð með Microsoft.

Ef þú hefur samband við samstarfsaðila Microsoft eða Microsoft til að fá aðstoð gefur þú eftirfarandi upplýsingar:

* Kenni verkraðarfærslunnar sem villan kom upp
* Tímastimpill þess hvenær villan kom upp
* Tímabelti notanda

> [!TIP]
> Eftir því hvort útgáfa [!INCLUDE [prod_short](includes/prod_short.md)] 22.1 er safnað saman á eftirfarandi hátt:
>
> * Fyrir eldri útgáfur má sjá skjámynd af síðunni **Verkraðarskrárfærslur** .
> * Fyrir síðari útgáfur skal nota aðgerðina **Afrita upplýsingar** á síðunni Færslur í verkraðarkladda til að afrita upplýsingarnar (kenni verkraðar, tímastimpill og tímabelti notanda).

## <a name="monitor-the-job-queue-with-telemetry"></a>Fylgjast með verkröðinni með fjarmælingu

Stjórnendur geta notað [Azure Application Insights](/azure/azure-monitor/app/app-insights-overview) til að safna saman og greina fjarmælingar sem hjálpa til við að bera kennsl á vandamál. Til að [fræðast meira um fjarmælingar er farið í Eftirlit og Greining fjarmælinga](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) og [greining á Vinnsluröð Rakningarsíma](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace).

Fjarmælingar gera stjórnendum kleift að setja upp viðvaranir um málefni verkraðar sem senda textaskilaboð, tölvupóst eða skilaboð í Teams ef eitthvað er ekki rétt. Til að fræðast meira um þessar viðvaranir er farið í [Alert on Telemetry](/dynamics365/business-central/dev-itpro/administration/telemetry-alert).

## <a name="see-also"></a>Sjá einnig .

[Stjórnun](admin-setup-and-administration.md)  
[Uppsetning Business Central](setup.md)  
[Grunnstillingum breytt](ui-change-basic-settings.md)  
[Greining á líftíma fjarmælingarrakningar verkraðar](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace)  
[Viðvörun í fjarmælingum](/dynamics365/business-central/dev-itpro/administration/telemetry-alert)

[!INCLUDE[footer-include](includes/footer-banner.md)]
