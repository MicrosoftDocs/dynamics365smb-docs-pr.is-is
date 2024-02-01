---
title: Tímasetja verk til að keyrast sjálfvirkt
description: Lærðu að nota vinnsluraðarfærslur til að keyra skýrslur og kódeseiningar.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: jswymer
ms.topic: conceptual
ms.date: 09/15/2023
ms.custom: bap-template
ms.search.form: '672, 673, 674, 671'
ms.service: dynamics-365-business-central
---
# <a name="use-job-queues-to-schedule-tasks"></a>Nota starfaraðir til að áætla verk

 **Notaðu síðuna Vinnsluraðarfærslur**  til að raða og keyra tilteknar skýrslur og kódeseiningar. Stilla má verk svo þau keyri einu sinni eða endurtekið. Til dæmis gætirðu viljað keyra skýrsluna **Sölumaður * sölutölur** vikulega til að rekja sölu sölumanns í hverri viku eða keyra kóðaeininguna **Framselja samþykktarbeiðnir** daglega til að koma í veg fyrir að skjöl safnist upp.

Síðan Verkraðarafærslur skráir öll tiltæk verk. Ef bætt er við nýrri verkraðarafærslu sem keyrir á áætlun verður að gefa upp einhverjar upplýsingar. Dæmi:

* Gerð hlutar sem keyra á, eins og skýrsla eða Codeunit. Þú verður að vera með heimild til að keyra tiltekna skýrslu eða kóðaeiningu.
* Heiti og hlutarkenni hlutarins.
* Færibreytur til að tilgreina virkni verkraðarfærslu. Til dæmis er hægt að bæta við færibreytu til að sent einungis bókaðar sölupantanir.
* Hvenær og hversu oft keyra á verkraðarfærsluna.

> [!IMPORTANT]  
> Ef þér er úthlutað SUPER-heimildasamstæðunni sem fylgir með [!INCLUDE[prod_short](includes/prod_short.md)] hefurðu heimild til að keyra alla hluti sem eru innifaldir í leyfinu þínu. Ef hlutverk fulltrúa er úthlutað er hægt að stofna og tímasetja verkraðarafærslur en aðeins kerfisstjórar og leyfir notendur geta keyrt þær.

Eftir að verkraðir eru settar upp og í keyrslu getur staðan breyst eins og fylgir hér á eftir innan hvers endurtekins tímabils:

* **Bið**  
* **Tilbúið**  
* **Í vinnslu**  
* **Villa**  
* **Lokið**  
* **Í bið vegna óvirkni**

> [!NOTE]
> Í  **bið vegna óvirkni**  Staða er notuð fyrst og fremst fyrir vinnsluraðarfærslur sem raða samstillingu milli  [!INCLUDE [prod_short](includes/prod_short.md)]  og annars forrits, svo sem [!INCLUDE [cds_long_md](includes/cds_long_md.md)]. Til að fræðast meira um þessa stöðu er farið í  [tímafrekari](/dynamics365/business-central/admin-scheduled-synchronization-using-the-synchronization-job-queue-entries#about-inactivity-timeouts) upplýsingar um óvirkni.

Eftir að verki lýkur er það fjarlægt af lista yfir verkraðarfærslur nema það sé endurtekið verk. Fyrir endurteknar vinnslur  **er reiturinn fyrsti Upphafstími**  leiðréttur til að sýna næst þegar vinnslan verður keyrð. 

## <a name="important-for-scheduling-recurring-jobs"></a>Mikilvægt að raða endurteknum vinnslum

> [!IMPORTANT]  
> Endurteknar verkbiðraðir geta haft áhrif á afköst svo þú ættir ekki að keyra þær of oft. Þegar sett er upp hversu oft á að keyra endurtekna vinnslu er reynt að setja inn stærsta tímabilið sem hægt er að. Til dæmis ef þú ert að fara að stilla endurtekningu á fimm mínútum, Íhugaðu hvort það geti verið 15 mínútur, eða jafnvel einu sinni á klukkustund í staðinn. Þegar skipuleggja á endurteknar verkbiðraðir skal íhuga hvaða svæði í umsókninni vinnslan hefur áhrif á. Er það svæði þar sem margir notendur vinna og verða þau áhrif mikil virkni? Taka skal tillit til lengingar á einni keyrslu og fyrirtæki hvetja til keyrslu verka með tiltekinni cadence.

## <a name="the-earliest-start-date"></a>Fyrsti Upphafsdagur

Gildið í  **reitnum fyrsta upphafsdagsetning/tími**  á  **spjaldinu færsluspjald**  birtist næst þegar vinnslan verður keyrð. Það eru nokkrir þættir sem geta haft áhrif á hvort verkraðarafærsla keyrir í raun á þeim tíma.

Algengustu þættirnir eru fjöldi verkraðarafærslna í umhverfi og heildarfjölda áætlaaðra verkhluta. Til að verja afkastastig eru rekstrarmörk. Ef þú ert með mikið af færslum í biðröðinni og t.d. annað þeirra bregst eða færslurnar taka bara lengri tíma en búist var við, gæti næsta vinnsla ekki hafist í væntanlegu skipti. Ef þú ert með kótaeiningarnar sem myndar 100.000 eða fleiri áætluð verk, ættirðu að rannsaka hvort þú þurfir í raun öll þau verkefni. Hægt er að opna lista yfir öll áætluð verk á  **síðunni áætluð verk** .

Frekari upplýsingar um stöðu vinnsluraðarafærslna er  [að fá með því að skoða stöðu fyrir hvaða starf](#to-view-status-for-any-job) sem er. Til að fræðast meira um rekstrarmörk er farið í  [ósamstillt verkefnamörk](/dynamics365/business-central/dev-itpro/administration/operational-limits-online#Task).

## <a name="monitor-status-or-errors-in-the-job-queue"></a>Fylgjast með stöðu eða villum í verkröð

Gögn sem vinnslubiðröðin myndar er geymd þannig að hægt sé að leita að villum.  

Fyrir hverja verkraðarfærslu er hægt að skoða og breyta stöðunni. Við stofnun verkraðarfærslu er staða hennar stillt á **Bið**. T.d. er hægt að setja stöðuna á **Tilbúið** og svo aftur í **Í bið**. Annars eru stöðuupplýsingar uppfærðar sjálfkrafa.

Eftirfarandi tafla lýsir gildum reitsins **Staða**.

| Staða | Lýsing |
|--|--|
| Tilbúið | Verkraðarfærslan er tilbúin til keyrslu. |
| Í vinnslu | Verkraðarfærslan er í vinnslu. Þessi reitur uppfærist á meðan verkröðin er í gangi. |
| Í bið | Sjálfgefin staða verkraðarfærslunnar þegar hún er búin til. Veljið aðgerðina **Stilla stöðu í tilbúið** til að breyta stöðunni í **Tilbúið**. Veldu aðgerðina **Setja í bið** til að snúa aftur í stöðuna **Í bið**. |
| Villa | Eitthvað fór úrskeiðis. Veldu **Sýna villu** til að sýna villuboðin. |
| Klárað | Verkraðarfærslunni er lokið. |

> [!Tip]  
> Verkraðarfærslur hætta að keyra þegar villa kemur upp. Þetta getur til dæmis verið vandamál þegar færsla tengist utanaðkomandi þjónustu, til dæmis bankastraumi. Ef þjónustan er ekki í boði í augnablikinu og verkraðarfærslan getur ekki tengst mun færslan sýna villu og stöðva keyrslu. Þú þarft að endurræsa verkraðarfærsluna handvirkt. Reitirnir **Hámarksfjöldi tilrauna** og **Töf á endurtekinni keyrslu (sek.)** geta hins vegar hjálpað þér að koma í veg fyrir þessar aðstæður. Reiturinn **Hámarksfjöldi tilrauna** gerir þér kleift að tilgreina hversu oft verkraðarfærsla getur mistekist áður en hún hættir að reyna að keyra. Reiturinn **Töf á endurtekinni keyrslu (sek.)** gerir þér kleift að tilgreina tímann, í sekúndum, á milli tilrauna. Samsetning þessara tveggja reita gæti haldið verkraðarfærslunni gangandi þar til ytri þjónustan verður tiltæk.

### <a name="to-view-status-for-any-job"></a>Til að skoða stöðu fyrir hvaða verk sem er

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verkraðarfærslur** og velja síðan viðkomandi tengil.
2. Á síðunni **Verkraðarfærslur** skal velja færslu verkraðar og síðan velja aðgerðina **Skráarfærslur**.  

> [!TIP]
> Fyrir greiningu í dýpri byggð á Telemetry er hægt að nota  Application Insights  í  Microsoft Azure  til að fara yfir stöðu færslna í vinnsluröð. Til að fræðast meira um Telemetry er farið í að  [fylgjast með og greina Telemetry](/dynamics365/business-central/dev-itpro/administration/telemetry-overview)  og  [greina vinnslubiðröð Lífeyrisauka rakamæling Telemetry](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace).

## <a name="view-scheduled-tasks"></a>Skoða áætluð verk

Síðan **Áætluð verk** í [!INCLUDE [prod_short](includes/prod_short.md)] sýnir hvaða verk eru tilbúin fyrir keyrslu í verkröðinni. Á síðunni má einnig sjá upplýsingar um fyrirtækið sem hvert verk er sett upp til að keyra í. Hins vegar er aðeins hægt að keyra verk sem merkt eru að tilheyri núverandi umhverfi.  

Til dæmis hætta öll tímasett verk ef fyrirtækið er í umhverfi sem er afrit af öðru umhverfi. Notaðu síðuna **Áætluð verk** til að stilla verk sem tilbúin til keyrslu í verkröðinni.  

> [!NOTE]
> Innri stjórnendur og notendur með leyfi geta tímasett keyrslur á verkum. Úthlutaðir stjórnendur geta sett upp og tímasett verk til að keyra, en aðeins notendur með leyfi geta keyrt þau.

## <a name="the-my-job-queue-part"></a>Hluti Starfraðarhlutans

Hlutinn **Mín verkröð** í hlutverkamiðstöðinni þinni sýnir verkraðarfærslur sem þú hefur byrjað á, en er enn ekki lokið. Að sjálfgefnu er hlutinn ekki sýndur, en þú getur bætt honum við í hlutverkamiðstöðina. Frekari upplýsingar um sérsnið er að fá með því að  [Sérsníða vinnusvæðið](ui-personalization-user.md).  

Eftirtaldir hlutur sýnir eftirfarandi upplýsingar:

* Hvaða skjöl með auðkenninu þínu í reitnum **Úthlutað notandakenni** verið er að vinna úr eða eru í biðröð, þ.m.t. skjöl sem eru að bókast í bakgrunni. 
* Villa kom upp við bókun skjals eða í verkraðarfærslu. 

Hlutinn „Mín verkröð“ gerir þér einnig kleift að hætta við bókun skjals.

### <a name="to-view-an-error-from-the-my-job-queue-part"></a>Til að skoða villu ú hlutanum Mín verkröð

1. Í færslu með stöðuna **Villa** skal velja aðgerðina **Sýna villu**.
2. Fara skal yfir villuboðin og leysa vandann.

## <a name="examples-of-what-you-can-schedule-using-job-queue-entries"></a>Dæmi um það sem hægt er að áætla með notkun vinnsluraðarfærslna

### <a name="schedule-reports"></a>Áætla skýrslur

Hægt er að tímasetja skýrslu eða runuvinnslu þannig að hún keyri á tilteknum degi og tíma. Tímasettar skýrslur og runuvinnslur eru færðar inn í verkröð og unnar á áætluðum tíma, eins og önnur verk. Veldu valkostinn **Áætlun** eftir að hafa valið aðgerðina **Senda til** og færðu svo inn upplýsingar á borð við prentara, og tíma og dagsetningu, endurtekningu.  

Frekari upplýsingar um röðun er að fá með því að fara í  [röðun skýrslu í keyrslu.](ui-work-report.md#ScheduleReport)

### <a name="schedule-synchronization-between--and-includeprod_short"></a>Tímastilla samstillingu á milli [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)]

Ef þú hefur samþætt [!INCLUDE[prod_short](includes/prod_short.md)] við [!INCLUDE[prod_short](includes/cds_long_md.md)] gerir verkröðin þér kleift að tímasetja hvenær á að samstilla gögn. Verkraðarfærslan getur stofnað færslur í einu forriti til að samsvara færslum í öðrum eftir því hvaða stefna og reglur hafa verið skilgreindar. Gott dæmi er þegar þú skráir tengilið í [!INCLUDE[crm_md](includes/crm_md.md)] getur verkraðarfærslan sett upp þann tengilið fyrir þig í [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar um röðun er að fá með því að  [raða samstillingu milli Viðskiptamiðseðla og Dynamics 365 sölu](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md).

### <a name="schedule-when-to-post-sales-and-purchase-orders"></a>Áætla hvenær bóka á sölu-og innkaupapantanir

Þú getur notað verkraðarfærslur til að tímasetja viðskiptaferla á að keyra í bakgrunni. Til dæmis eru bakgrunnsverk gagnleg þegar margir notendur bóka sölupantanir samtímis, en einungis er hægt að afgreiða eina pöntun í einu. Ef fræðast á um bakgrunnabókun er farið í  [til að setja upp bakgrunnabókun með starfbiðröðum](ui-batch-posting.md#to-set-up-background-posting-with-job-queues).

## <a name="handle-job-queue-entry-issues"></a>Afgreiðsla úthreyfingar vinnslustöðvar færslu

Ef verkraðarafærsla sýnir villu er fyrsti kosturinn til að leysa málið að endurræsa verkraðarafærslu. Hægt er að stilla stöðu verkraðarafærslu  **á í bið**  og síðan að  **undirbúa** eða endurræsa hana.

Ef Endurræsing hjálpar ekki gæti málið verið í kóðanum. Eigandann má finna (einnig kallað  *útgefandann*) KÓTANUM í Al stafabraddakeppninni í Log-raðarskrá. Ef villan kemur úr App/framlengingu skaltu hafa samband við samstarfsaðila Microsoft. Ef villan kemur úr Microsoft Application skal opna stuðningsbeiðni við Microsoft.

Vinsamlegast Gefðu upp eftirfarandi upplýsingar ef þú hefur samband við Microsoft Partner eða Microsoft samstarfsaðila fyrir stuðning.

* KENNI færslunnar í verkraðarafærslu þar sem villan varð
* Tímastimpill þegar villan kom upp
* Tímabeltið þitt

> [!TIP]
> Eftir því hvort þú ert fyrr eða síðar en útgáfa 22,1, safnar þú  [!INCLUDE [prod_short](includes/prod_short.md)]  upplýsingunum á eftirfarandi hátt:
>
> * Fyrir eldri útgáfur er gefið Skjáskot af  **síðunni Skráningarfærslur**  vinnslustöðvar.
> * Nota  **skal aðgerðina afrita upplýsingar**  á síðunni Skráningarfærslur vinnslu til að afrita upplýsingarnar (VINNSLUBIÐRAÐARKENNI, stimpilklukku og tímabeltið).

## <a name="monitor-the-job-queue-with-telemetry"></a>Fylgjast með verkröðinni með fjarmælingu

Stjórnendur geta notað  [Azure  Application Insights](/azure/azure-monitor/app/app-insights-overview)  til að safna og greina Telemetry sem hjálpar til við að auðkenna vandamál. Til að fræðast meira um Telemetry er farið í að  [fylgjast með og greina Telemetry](/dynamics365/business-central/dev-itpro/administration/telemetry-overview)  og  [greina vinnslubiðröð Lífeyrisauka rakamæling Telemetry](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace).

Telemetri gerir stjórnendum kleift að setja upp viðvaranir um úthreyfingar vinnslu sem senda textaskilaboð, tölvupóst eða skilaboð í teymum ef eitthvað er ekki rétt. Til að fræðast meira um þessar viðvaranir er farið í  [viðvörun í Telemetry](/dynamics365/business-central/dev-itpro/administration/telemetry-alert).

## <a name="see-also"></a>Sjá einnig .

[Stjórnun](admin-setup-and-administration.md)  
[Uppsetning Business Central](setup.md)  
[Grunnstillingum breytt](ui-change-basic-settings.md)  
[Greining á líftíma fjarmælingarrakningar verkraðar](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace)  
[Viðvörun um Telemetramæling](/dynamics365/business-central/dev-itpro/administration/telemetry-alert)

[!INCLUDE[footer-include](includes/footer-banner.md)]
