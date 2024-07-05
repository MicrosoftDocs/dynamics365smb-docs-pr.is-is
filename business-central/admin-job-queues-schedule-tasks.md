---
title: Tímasetja verk til að keyrast sjálfvirkt
description: Fræðast um notkun verkraðarfærslna til að keyra skýrslur og codeunit.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 09/15/2023
ms.custom: bap-template
ms.search.form: '672, 673, 674, 671'
ms.service: dynamics-365-business-central
---
# Nota verkröð til að tímasetja verk

Nota síðuna **Verkraðarfærslur** til að tímasetja og keyra tilteknar skýrslur og codeunit. Stilla má verk svo þau keyri einu sinni eða endurtekið. Til dæmis gætirðu viljað keyra skýrsluna **Sölumaður * sölutölur** vikulega til að rekja sölu sölumanns í hverri viku eða keyra kóðaeininguna **Framselja samþykktarbeiðnir** daglega til að koma í veg fyrir að skjöl safnist upp.

Á síðunni Verkraðarfærslur er listi yfir öll fyrirliggjandi verk. Ef nýrri verkraðarfærslu er bætt við sem keyrð er í áætlun verður að veita einhverjar upplýsingar. Dæmi:

* Gerð hlutar sem á að keyra, t.d. skýrsla eða kótaeining. Þú verður að vera með heimild til að keyra tiltekna skýrslu eða kóðaeiningu.
* Heiti og hlutarkenni hlutarins.
* Færibreytur til að tilgreina virkni verkraðarfærslu. Til dæmis er hægt að bæta við færibreytu til að sent einungis bókaðar sölupantanir.
* Hvenær og hversu oft keyra á verkraðarfærsluna.

> [!IMPORTANT]  
> Ef þér er úthlutað SUPER-heimildasamstæðunni sem fylgir með [!INCLUDE[prod_short](includes/prod_short.md)] hefurðu heimild til að keyra alla hluti sem eru innifaldir í leyfinu þínu. Ef um er að ræða hlutverkið Úthlutaður stjórnandi er hægt að stofna og tímasetja verkraðarfærslur en aðeins kerfisstjórar og leyfisskyldir notendur geta keyrt þær.

Eftir að verkraðir eru settar upp og í keyrslu getur staðan breyst eins og fylgir hér á eftir innan hvers endurtekins tímabils:

* **Bið**  
* **Tilbúið**  
* **Í vinnslu**  
* **Villa**  
* **Lokið**  
* **Bið vegna óvirkni**

> [!NOTE]
>  **Staðan Bið vegna óvirkni** er mest notuð fyrir verkraðarfærslur sem tímasetja samstillingu milli [!INCLUDE [prod_short](includes/prod_short.md)] og annarrar kerfis, svo sem [!INCLUDE [cds_long_md](includes/cds_long_md.md)]. Hægt er að fá nánari upplýsingar um þessa stöðu með því að [fara í Tímamörk](/dynamics365/business-central/admin-scheduled-synchronization-using-the-synchronization-job-queue-entries#about-inactivity-timeouts) óvirkni.

Eftir að verki lýkur er það fjarlægt af lista yfir verkraðarfærslur nema það sé endurtekið verk. Ítrekunarverkum er reiturinn **Fyrsti upphafstími** leiðréttur þannig að hann sýni næst þegar verkið verður keyrt. 

## Mikilvægt fyrir tímasetningu endurtekinna verka

> [!IMPORTANT]  
> Ítrekaðar verkraðir geta haft áhrif á afköst svo að ekki ætti að keyra þær of oft. Þegar sett er upp hversu oft eigi að keyra ítrekað verk er reynt að stilla stærsta tímabilið sem hægt er að nota. Ef til dæmis á að endurtaka fimm mínútur þarf að hafa í huga hvort það geti verið 15 mínútur eða jafnvel einu sinni á klukkustund í staðinn. Við áætlun ítrekaðra verkraða skal hafa í huga hvaða svæði forritið hefur áhrif á. Er það svæði þar sem margir notendur vinna og verða fyrir mikilli virkni? Íhuga skal lengd einnar verkkeyrslu og viðskiptahvöt fyrir keyrslu verka með tiltekinn náunga.

## Fyrsta upphafsdagsetning

Gildið í reitnum **Fyrsta upphafsdagsetning/tími** á síðunni **Færsluspjald** verkraðar sýnir næst þegar verkið verður keyrt. Nokkrir þættir geta haft áhrif á það hvort verkraðarfærsla keyrir í raun á þeim tíma.

Algengustu þættirnir eru fjöldi verkraðarfærslna í umhverfi og heildarfjöldi áætlaðra verka. Til að vernda afkastastig eru aðgerðamörk. Ef mikið af færslum er í röðinni og ein þeirra mistekst, til dæmis, eða færslurnar taka lengri tíma en búist var við, gæti næsta verk ekki hafist á áætluðum tíma. Ef til eru codeunit sem eru að búa til 100.000 eða fleiri áætluð verk ætti að athuga hvort í raun þurfi alla þessa verkhluta. Hægt er að nálgast lista yfir öll áætluð verk á síðunni **Tímasettir verkhlutar** .

Nánari upplýsingar um eftirlit með stöðu verkraðarfærslna eru í Til að [skoða stöðu fyrir hvaða verk](#to-view-status-for-any-job) sem er. Farið í Ósamstillt verkmörk til að [fræðast meira um aðgerðamörk](/dynamics365/business-central/dev-itpro/administration/operational-limits-online#Task).

## Fylgjast með stöðu eða villum í verkröð

Gögn sem verkröðin býr til eru geymd svo hægt sé að ræða villur.  

Fyrir hverja verkraðarfærslu er hægt að skoða og breyta stöðunni. Við stofnun verkraðarfærslu er staða hennar stillt á **Bið**. T.d. er hægt að setja stöðuna á **Tilbúið** og svo aftur í **Í bið**. Annars eru stöðuupplýsingar uppfærðar sjálfkrafa.

Eftirfarandi tafla lýsir gildum reitsins **Staða**.

| Staða | Lýsing |
|--|--|
| Tilbúið | Verkraðarfærslan er tilbúin til keyrslu. |
| Í vinnslu | Verkraðarfærslan er í vinnslu. Þessi reitur uppfærist á meðan verkröðin er í gangi. |
| Í bið | Sjálfgefin staða verkraðarfærslunnar þegar hún er búin til. Veljið aðgerðina **Stilla stöðu í tilbúið** til að breyta stöðunni í **Tilbúið**. Veldu aðgerðina **Setja í bið** til að snúa aftur í stöðuna **Í bið**. Nánari upplýsingar eru í [Um](#about-on-hold) bið.|
| Villa | Eitthvað fór úrskeiðis. Veldu **Sýna villu** til að sýna villuboðin. |
| Klárað | Verkraðarfærslunni er lokið. |

> [!TIP]  
> Verkraðarfærslur hætta að keyra þegar villa kemur upp. Þetta getur til dæmis verið vandamál þegar færsla tengist utanaðkomandi þjónustu, til dæmis bankastraumi. Ef þjónustan er ekki í boði í augnablikinu og verkraðarfærslan getur ekki tengst mun færslan sýna villu og stöðva keyrslu. Þú þarft að endurræsa verkraðarfærsluna handvirkt. Reitirnir **Hámarksfjöldi tilrauna** og **Töf á endurtekinni keyrslu (sek.)** geta hins vegar hjálpað þér að koma í veg fyrir þessar aðstæður. Reiturinn **Hámarksfjöldi tilrauna** gerir þér kleift að tilgreina hversu oft verkraðarfærsla getur mistekist áður en hún hættir að reyna að keyra. Reiturinn **Töf á endurtekinni keyrslu (sek.)** gerir þér kleift að tilgreina tímann, í sekúndum, á milli tilrauna. Samsetning þessara tveggja reita gæti haldið verkraðarfærslunni gangandi þar til ytri þjónustan verður tiltæk.

### Um bið

Ef færsla verkraðar er stillt á Bið **hefur það ekki áhrif á skokk sem þegar er verið að** keyra. Þegar verk hefur hafist í verkröðinni heldur hún áfram að keyra þar til henni er lokið, burtséð frá þeim breytingum sem gerðar hafa verið á verkraðarfærslunni, svo sem að setja hana í bið.<br><br> **Staðan Bið** er gjarnan notuð til að koma í veg fyrir að verk byrji sjálfkrafa þegar það nær áætluðum upphafstíma. Það gerir það mögulegt að gera tímabundið hlé á framkvæmd verks áður en það hefst í vinnslu. Þegar verk hefur þegar verið keyrt, breytist staðan í 'Bið' ekki rofin eða hefur áhrif á framkvæmd verksins.<br><br>Ef stöðva þarf eða hætta við keyrslu verks er hægt að gera það handvirkt með því að grípa inn í vinnsluna, t.d. að hætta við samsvarandi lotu eða vinnslu sem er ábyrgt fyrir framkvæmd verksins.
### Til að skoða stöðu fyrir hvaða verk sem er

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verkraðarfærslur** og velja síðan viðkomandi tengil.
2. Á síðunni **Verkraðarfærslur** skal velja færslu verkraðar og síðan velja aðgerðina **Skráarfærslur**.  

> [!TIP]
> Hægt er að nota Application Insights  Microsoft Azure í til að fara yfir stöðu verkraðarfærslna til að sjá stöðu verkraðarfærslna sem byggjast á fjarmælingum. Til að [fræðast meira um fjarmælingar er farið í Eftirlit og Greining fjarmælinga](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) og [greining á Vinnsluröð Rakningarsíma](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace).

## Skoða áætluð verk

Síðan **Áætluð verk** í [!INCLUDE [prod_short](includes/prod_short.md)] sýnir hvaða verk eru tilbúin fyrir keyrslu í verkröðinni. Á síðunni má einnig sjá upplýsingar um fyrirtækið sem hvert verk er sett upp til að keyra í. Hins vegar er aðeins hægt að keyra verk sem merkt eru að tilheyri núverandi umhverfi.  

Til dæmis hætta öll tímasett verk ef fyrirtækið er í umhverfi sem er afrit af öðru umhverfi. Notaðu síðuna **Áætluð verk** til að stilla verk sem tilbúin til keyrslu í verkröðinni.  

> [!NOTE]
> Innri stjórnendur og notendur með leyfi geta tímasett keyrslur á verkum. Úthlutaðir stjórnendur geta sett upp og tímasett verk til að keyra, en aðeins notendur með leyfi geta keyrt þau.

## Verkraðarhlutinn verkraðarhlutinn minn

Hlutinn **Mín verkröð** í hlutverkamiðstöðinni þinni sýnir verkraðarfærslur sem þú hefur byrjað á, en er enn ekki lokið. Að sjálfgefnu er hlutinn ekki sýndur, en þú getur bætt honum við í hlutverkamiðstöðina. Nánari upplýsingar um sérstillingu fást með því að [fara í Sérstilla vinnusvæðið](ui-personalization-user.md).  

Eftirtaldir hlutur sýnir eftirfarandi upplýsingar:

* Hvaða skjöl með auðkenninu þínu í reitnum **Úthlutað notandakenni** verið er að vinna úr eða eru í biðröð, þ.m.t. skjöl sem eru að bókast í bakgrunni. 
* Villa kom upp við bókun skjals eða í verkraðarfærslu. 

Hlutinn „Mín verkröð“ gerir þér einnig kleift að hætta við bókun skjals.

### Til að skoða villu ú hlutanum Mín verkröð

1. Í færslu með stöðuna **Villa** skal velja aðgerðina **Sýna villu**.
2. Fara skal yfir villuboðin og leysa vandann.

## Dæmi um hvað er hægt að tímasetja með því að nota verkraðarfærslur

### Áætla skýrslur

Hægt er að tímasetja skýrslu eða runuvinnslu þannig að hún keyri á tilteknum degi og tíma. Tímasettar skýrslur og runuvinnslur eru færðar inn í verkröð og unnar á áætluðum tíma, eins og önnur verk. Veldu valkostinn **Áætlun** eftir að hafa valið aðgerðina **Senda til** og færðu svo inn upplýsingar á borð við prentara, og tíma og dagsetningu, endurtekningu.  

Til að fá nánari upplýsingar um tímasetningar er farið í [Tímasetning skýrslu í Keyra](ui-work-report.md#ScheduleReport)

### Tímastilla samstillingu á milli [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)]

Ef þú hefur samþætt [!INCLUDE[prod_short](includes/prod_short.md)] við [!INCLUDE[prod_short](includes/cds_long_md.md)] gerir verkröðin þér kleift að tímasetja hvenær á að samstilla gögn. Verkraðarfærslan getur stofnað færslur í einu forriti til að samsvara færslum í öðrum eftir því hvaða stefna og reglur hafa verið skilgreindar. Gott dæmi er þegar þú skráir tengilið í [!INCLUDE[crm_md](includes/crm_md.md)] getur verkraðarfærslan sett upp þann tengilið fyrir þig í [!INCLUDE[prod_short](includes/prod_short.md)]. Nánari upplýsingar um tímasetningar er farið í [Tímasetning samstillingu milli Business Central og Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md).

### Tímasetja hvenær á að bóka sölu- og innkaupapantanir

Þú getur notað verkraðarfærslur til að tímasetja viðskiptaferla á að keyra í bakgrunni. Til dæmis eru bakgrunnsverk gagnleg þegar margir notendur bóka sölupantanir samtímis, en einungis er hægt að afgreiða eina pöntun í einu. Nánari upplýsingar um bakgrunnsbókun er farið í Til að [setja upp bakgrunnsbókun með verkröðunum](ui-batch-posting.md#to-set-up-background-posting-with-job-queues).

## Vinna með vandamál í verkraðarfærslum

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

## Fylgjast með verkröðinni með fjarmælingu

Stjórnendur geta notað [Azure Application Insights](/azure/azure-monitor/app/app-insights-overview) til að safna saman og greina fjarmælingar sem hjálpa til við að bera kennsl á vandamál. Til að [fræðast meira um fjarmælingar er farið í Eftirlit og Greining fjarmælinga](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) og [greining á Vinnsluröð Rakningarsíma](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace).

Fjarmælingar gera stjórnendum kleift að setja upp viðvaranir um málefni verkraðar sem senda textaskilaboð, tölvupóst eða skilaboð í Teams ef eitthvað er ekki rétt. Til að fræðast meira um þessar viðvaranir er farið í [Alert on Telemetry](/dynamics365/business-central/dev-itpro/administration/telemetry-alert).

## Sjá einnig .

[Stjórnun](admin-setup-and-administration.md)  
[Uppsetning Business Central](setup.md)  
[Grunnstillingum breytt](ui-change-basic-settings.md)  
[Greining á líftíma fjarmælingarrakningar verkraðar](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace)  
[Viðvörun í fjarmælingum](/dynamics365/business-central/dev-itpro/administration/telemetry-alert)

[!INCLUDE[footer-include](includes/footer-banner.md)]
