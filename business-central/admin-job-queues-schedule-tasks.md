---
title: Tímasetja verk til að keyrast sjálfvirkt
description: Tímasettum verkum er stjórnað af verkröðinni. Þessi verk keyra skýrslur og kóðaeiningar. Stilla má verk svo þau keyri einu sinni eða endurtekið.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '672, 673, 674, 671'
ms.date: 10/01/2021
ms.author: edupont
---
# Nota verkraðir til að tímaraða verkhlutum

Síða verkraðarfærslna gerir notendum kleift að tímasetja og keyra tilteknar skýrslur og kóðaeiningar. Stilla má verk svo þau keyri einu sinni eða endurtekið. Til dæmis gætirðu viljað keyra skýrsluna **Sölumaður * sölutölur** vikulega til að rekja sölu sölumanns í hverri viku eða keyra kóðaeininguna **Framselja samþykktarbeiðnir** daglega til að koma í veg fyrir að skjöl safnist upp.

Síðan **Verkraðarfærslur** birtir öll núverandi verk. Ef þú bætir við nýrri verkraðarfærslu sem á að tímasetja þarftu að gefa upp nokkrar upplýsingar. Dæmi:

* Gerð hlutarins sem á að keyra, t.d. skýrsla eða kóðaeining. Þú verður að vera með heimild til að keyra tiltekna skýrslu eða kóðaeiningu.
* Heiti og hlutarkenni hlutarins. 
* Færibreytur til að tilgreina virkni verkraðarfærslu. Til dæmis er hægt að bæta við færibreytu til að sent einungis bókaðar sölupantanir. 
* Hvenær og hversu oft keyra á verkraðarfærsluna.

> [!IMPORTANT]  
> Ef þér er úthlutað SUPER-heimildasamstæðunni sem fylgir með [!INCLUDE[prod_short](includes/prod_short.md)] hefurðu heimild til að keyra alla hluti sem eru innifaldir í leyfinu þínu. Ef þú ert með úthlutað stjórnandahlutverki geturðu búið til og tímasett verkraðarfærslur, en aðeins stjórnendur og notendur með leyfi geta keyrt þær. Notendur með tækjaleyfi geta ekki búið til eða keyrt verkraðarfærslur.

Eftir að verkraðir eru settar upp og í keyrslu getur staðan breyst eins og fylgir hér á eftir innan hvers endurtekins tímabils:

* **Bið**  
* **Tilbúið**  
* **Í vinnslu**  
* **Villa**  
* **Lokið**  

Eftir að verki lýkur er það fjarlægt af lista yfir verkraðarfærslur nema það sé endurtekið verk. Fyrir endurtekin verk er reiturinn **Fyrsti upphafstími** stilltur til að sýna næsta áætlaða keyrslutíma verksins.  

## Fylgjast með stöðu eða villum í verkröð

Gögn sem verkröðin býr til eru geymd í gagnagrunninum þannig að þú getur úrræðaleitað villur verkraðar.  

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

### Til að skoða stöðu fyrir hvaða verk sem er

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verkraðarfærslur** og velja síðan viðkomandi tengil.
2. Á síðunni **Verkraðarfærslur** skal velja færslu verkraðar og síðan velja aðgerðina **Skráarfærslur**.  

> [!TIP]
> Einnig er hægt að skoða stöðu verkraðarfærslna með því að nota Application Insights í Microsoft Azure fyrir dýpri greiningu sem byggir á fjarmælingum. Frekari upplýsingar er að finna í [Fylgjast með og greina fjarmælingar](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) og [Greining á líftíma fjarmælingarrakningar verkraðar](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace) í [!INCLUDE [prod_short](includes/prod_short.md)] þróunar- og stjórnunarefni.

## Skoða áætluð verk

Síðan **Áætluð verk** í [!INCLUDE [prod_short](includes/prod_short.md)] sýnir hvaða verk eru tilbúin fyrir keyrslu í verkröðinni. Á síðunni má einnig sjá upplýsingar um fyrirtækið sem hvert verk er sett upp til að keyra í. Hins vegar er aðeins hægt að keyra verk sem merkt eru að tilheyri núverandi umhverfi.  

Til dæmis hætta öll tímasett verk ef fyrirtækið er í umhverfi sem er afrit af öðru umhverfi. Notaðu síðuna **Áætluð verk** til að stilla verk sem tilbúin til keyrslu í verkröðinni.  

> [!NOTE]
> Innri stjórnendur og notendur með leyfi geta tímasett keyrslur á verkum. Úthlutaðir stjórnendur geta sett upp og tímasett verk til að keyra, en aðeins notendur með leyfi geta keyrt þau.

## Hlutinn fyrir Mína verkröð

Hlutinn **Mín verkröð** í hlutverkamiðstöðinni þinni sýnir verkraðarfærslur sem þú hefur byrjað á, en er enn ekki lokið. Að sjálfgefnu er hlutinn ekki sýndur, en þú getur bætt honum við í hlutverkamiðstöðina. Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md).  

Eftirtaldir hlutur sýnir eftirfarandi upplýsingar:

* Hvaða skjöl með auðkenninu þínu í reitnum **Úthlutað notandakenni** verið er að vinna úr eða eru í biðröð, þ.m.t. skjöl sem eru að bókast í bakgrunni. 
* Villa kom upp við bókun skjals eða í verkraðarfærslu. 

Hlutinn „Mín verkröð“ gerir þér einnig kleift að hætta við bókun skjals.

### Til að skoða villu ú hlutanum Mín verkröð

1. Í færslu með stöðuna **Villa** skal velja aðgerðina **Sýna villu**.
2. Fara skal yfir villuboðin og leysa vandann.

## Dæmi um það sem hægt er að áætla með því að nota verkröð

### Áætla skýrslur

Hægt er að tímasetja skýrslu eða runuvinnslu þannig að hún keyri á tilteknum degi og tíma. Tímasettar skýrslur og runuvinnslur eru færðar inn í verkröð og unnar á áætluðum tíma, eins og önnur verk. Veldu valkostinn **Áætlun** eftir að hafa valið aðgerðina **Senda til** og færðu svo inn upplýsingar á borð við prentara, og tíma og dagsetningu, endurtekningu.  

Frekari upplýsingar eru í [Tímasetja keyrslu skýrslu](ui-work-report.md#ScheduleReport)

### Tímastilla samstillingu á milli [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)]

Ef þú hefur samþætt [!INCLUDE[prod_short](includes/prod_short.md)] við [!INCLUDE[prod_short](includes/cds_long_md.md)] gerir verkröðin þér kleift að tímasetja hvenær á að samstilla gögn. Verkraðarfærslan getur stofnað færslur í einu forriti til að samsvara færslum í öðrum eftir því hvaða stefna og reglur hafa verið skilgreindar. Gott dæmi er þegar þú skráir tengilið í [!INCLUDE[crm_md](includes/crm_md.md)] getur verkraðarfærslan sett upp þann tengilið fyrir þig í [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar eru í [Áætla samstillingu milli Business Central og Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md).

### Áætla bókun sölu- og innkaupapantana

Þú getur notað verkraðarfærslur til að tímasetja viðskiptaferla á að keyra í bakgrunni. Til dæmis eru bakgrunnsverk gagnleg þegar margir notendur bóka sölupantanir samtímis, en einungis er hægt að afgreiða eina pöntun í einu. Frekari upplýsingar eru í [Að setja upp bókun í bakgrunni með verkraðir](ui-batch-posting.md#to-set-up-background-posting-with-job-queues)

## Fylgjast með verkröðinni með fjarmælingu

Sem stjórnandi getur þú notað [Application Insights](/azure/azure-monitor/app/app-insights-overview) til að safna saman og greina fjarmælingar sem þú getur notað til að greina vandamál. Frekari upplýsingar er að finna í [Fylgjast með og greina fjarmælingar](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) í þróunar- og stjórnunarefni.  

## Sjá einnig

[Stjórnun](admin-setup-and-administration.md)  
[Uppsetning Business Central](setup.md)  
[Grunnstillingum breytt](ui-change-basic-settings.md)  
[Greining á líftíma fjarmælingarrakningar verkraðar](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace)  


[!INCLUDE[footer-include](includes/footer-banner.md)]