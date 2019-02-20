---
title: "Vinna með viðskiptamenn með því nota Dynamics 365 for Sales| Microsoft Docs"
description: "Hægt er að nota Dynamics 365 for Sales innan Business Central til að varpa gögnum og hafa óaðfinnanlegur samþætting og samstillingu í heildarferlinu."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map, Sales
ms.date: 01/24/2019
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: c129dd63b3aabeeac15c6684f961e04bd2b08a2a
ms.openlocfilehash: bba9fb9a83856cea43e4f4215e7c148b713252a9
ms.contentlocale: is-is
ms.lasthandoff: 01/24/2019

---
# <a name="integrating-with-dynamics-365-for-sales"></a>Samþætting við Dynamics 365 for Sales
Ef þú notar Dynamics 365 for Sales til að taka þátt í viðskiptum, getur þú notað [!INCLUDE[d365fin](includes/d365fin_md.md)] til þess að panta vinnslu og fjármál og hafa óaðfinnanlegur samþættingu í framhaldi af peningum.

> [!NOTE]
> Þetta efnisatriði gerir ráð fyrir því að bæði [!INCLUDE[d365fin](includes/d365fin_md.md)] og samþætt Sales-lausn séu notuð í SaaS-umhverfi. Að blanda saman netútgáfu og staðbundinni útgáfu er mögulegt, en krefst ákveðinnar grunnstillingar. Nánari upplýsingar er að finna í [Undirbýr samþættingu við Dynamics 365 for Sales á staðnum](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

Þegar umsóknin þín er sett upp til að samþætta við Sales, hefur þú aðgang að gögnum Sales frá [!INCLUDE[d365fin](includes/d365fin_md.md)] og öfugt í sumum tilfellum. Þessi samþætting gerir þér kleift að vinna með og samstilla gagnategundir sem eru algengar fyrir bæði þjónustu, svo sem viðskiptavini, tengiliði og söluupplýsingar og halda gögnunum uppfærðar á báðum stöðum.  

Til dæmis getur sölumaðurinn í Sales notað verðlista frá [!INCLUDE[d365fin](includes/d365fin_md.md)] þegar sölupöntun er búin til. Þegar vörunni er bætt við sölupöntunarlínuna í Sales er hægt að sjá birgðastöðu (framboð) vörunnar frá [!INCLUDE[d365fin](includes/d365fin_md.md)].

Á móti kemur að pantanavinnslur í [!INCLUDE[d365fin](includes/d365fin_md.md)] geta afgreitt sérkenni sölupantana sem eru fluttar sjálfkrafa eða handvirkt úr Sales, eins og að stofna og bóka sjálfkrafa gildar sölupöntunarlínur fyrir vörur eða tilföng sem voru færð inn í Sales sem innskriftarvörur. Frekari upplýsingar er að finna í hlutanum „Afgreiðsla sérstakra sölupöntunargagna“.

> [!IMPORTANT]  
> [!INCLUDE[d365fin](includes/d365fin_md.md)] samþættir aðeins við Dynamics 365 for Sales. Önnur forrit eða lausnir innan Dynamics 365 sem breyta stöðluðu verkflæði eða gagnalíkani í Sales, til dæmis Project Service Automation, kunna að rjúfa samþættinguna milli [!INCLUDE[d365fin](includes/d365fin_md.md)] og Sales.

## <a name="standard-sales-entity-mapping-for-synchronization"></a>Stöðluð einingavörpun Sales fyrir samstillingu
Sölueiningar, á borð við lykla, eru samþættir við jafngildar [!INCLUDE[d365fin](includes/d365fin_md.md)] færslugerðir, svo sem viðskiptamenn. Til að vinna með gögn Sales setur þú upp varpanir, sem kallast tengingar, á milli [!INCLUDE[d365fin](includes/d365fin_md.md)] færslna og einingarfærslur Sales. T.d. mætti setja upp tengingu á milli tiltekins viðskiptamanns í [!INCLUDE[d365fin](includes/d365fin_md.md)] og samsvarandi lykils í Sales.

Í eftirfarandi töflu er skráð [!INCLUDE[d365fin](includes/d365fin_md.md)] færslugerðir (töflur) og samsvarandi einingar Sales sem hægt er að samstilla út-fyrir-kassann.

|[!INCLUDE[d365fin](includes/d365fin_md.md)]|Sala|Stefna samstillingar|Sjálfgefin sía|
|-------------------------------------------|-----|-------------------------|--------------|
|Sölumaður/innkaupaaðili|Notandi|Sales -> Business Central|Tengiliðasía Sales: **Staða** er **Nei**, **Notandi með leyfi** er **Já**, stilling samþættingarnotanda er **Nei**|
|Viðskiptavinur|Reikningur|Business Central -> Sales og Sales -> Business Central|Afmörkun á reikningi Sales: **Venslagerð** er **Viðskiptamaður** og **Staða** er **Virk**.|
|Tengiliður|Tengiliður|Business Central -> Sales og Sales -> Business Central|Tengiliðasía Business Central: **Gerð** er **Einstaklingur** og tengiliði er úthlutað á fyrirtæki. Tengiliðasía Sales: Tengiliðnum er úthlutað á fyrirtæki og yfireining viðskiptamannsgerðar er **Reikningur**|
|Gjaldmiðill|Gjaldmiðill færslu|Business Central -> Sales| |
|Mælieining|Einingarflokkur|Business Central -> Sales| |
|Atriði|Vara|Business Central -> Sales og Sales -> Business Central|Tengiliðasía Sales: **Gerð afurðar** er **Birgðir Sales**|
|Forði|Vara|Business Central -> Sales og Sales -> Business Central|Tengiliðasía Sales: **Gerð afurðar** er **Þjónusta**|
|Verðflokkur viðskiptamanna|Verðlisti|Business Central -> Sales| |
|Söluverð|Verðlisti vöru|Business Central -> Sales|Tengiliðasíða Business Central: **Sölukóði** er ekki auður, **Sölugerð** er **Verðflokkur viðskiptamanns**|
|Tækifæri|Tækifæri|Business Central -> Sales og Sales -> Business Central| |
|Sölureikningshaus|Reikningsfæra|Business Central -> Sales| |
|Sölureikningslína|Reikningsfæra vöru|Business Central -> Sales| |

Einingar Sales og [!INCLUDE[d365fin](includes/d365fin_md.md)] töflur sem eru samstilltar eru skilgreindar af töfluvörpunarfærslum í töflu 5335, **Vörpun samþættingartöflu**. Hægt er að sjá varpanir og setja upp síur á síðu 5335, **Vörpun samþættingartaflna**. Vörpun á milli reita í [!INCLUDE[d365fin](includes/d365fin_md.md)] færslum og reitirnir í Sales-einingum eru skilgreindir af reitavörpunarfærslum í töflu 5336, **Vörpun samþættingarreits** og með viðbótar vörpunarrökfræði.

### <a name="field-mapping-for-the-sales-account-option"></a>Reitarvörpun fyrir reikningsvalkost Sales
Þremur töflum í [!INCLUDE[d365fin](includes/d365fin_md.md)] er varpað á valreiti einingarinnar **Reikningur**.   

Færslunum í töflunni sem eru ekki tengdar við valkostina sem eru til staðar í Sales verður sleppt við samstillingu. Þetta þýðir að reiturinn **Valkostur** verður auður í Sales.

Eftirfarandi tafla sýnir varpanir frá Business Central töflum fyrir reitinn **Valkostur** í einingunni **Reikningur**.

|Tafla|Valreitur í lyklaeiningunni í Sales|
|----------------------|-------------------------------------------|
|Greiðsluskilmálar|Greiðsluskilmálar|
|Afhendingarmáti|Heimilisfang 1: Flutningsskilmálar|
|Flutningsaðili|Heimilisfang 1: Afhendingarmáti|

### <a name="synchronization-rules"></a>Samstillingarreglur
Í eftirfarandi töflu er lýst reglum sem stjórna samstilling á milli tafla Business Central og eininga Sales.

> [!NOTE]  
> Breytingar á gögnum í Sales sem eru framkvæmdar af tengingarreikningi Sales eru hunsaðar. Breytingarnar verða ekki samstilltar. Af þessum sökum er mælt með að gera ekki breytingar á gögnum með því að nota tengingarreikning Sales.

|Tafla|Regla|
|-----|----|
|Viðskiptavinum|Áður en hægt er að samstilla viðskiptamann við reikning verður sölumaðurinn sem er viðskiptamanni er úthlutaður að vera tengdur við notandi í Sales. Af þessum sökum skal, þegar samstillingarverkið VIÐSKIPTAMENN - Dynamics 365 for Sales er keyrt og þú setur það upp til að stofna nýjar færslur, skaltu ganga úr skugga um að samstilla sölumenn við notendur Sales áður en þú samstillir viðskiptamenn við reikninga Sales. <br /> <br />VIÐSKIPTAMENN - Samstillingarverk fyrir Dynamics 365 for Sales samstillir aðeins reikninga sem hafa venslagerðina viðskiptamaður.|
|Tengiliður|Aðeins tengiliðir í Sales sem eru tengdir við reikning verða stofnaðir í Business Central. Gildið á kóða sölumanns skilgreinir eiganda tengdu einingarinnar í Sales.|
|Gjaldmiðlar|Gjaldmiðlar tengjast við færslugjaldmiðla í Sales á grundvelli ISO-kóða. Aðeins gjaldmiðlar sem eru með staðlaður ISO-kóði verða tengdir og samstilltir við færslugjaldmiðla.|
|Mælieiningar|Mælieiningar eru samstillar við einingahópa í Sales. Aðeins er hægt að skilgreina eina mælieiningu í einingahópnum.|
|Birgðir|Þegar vörur eru samstilltar við vörur Sales mun Business Central sjálfkrafa stofna verðlista í Sales. Til að forðast samstillingarvillur ætti ekki að breyta þessum verðlisti handvirkt.|
|Sölumenn|Sölumenn eru tengdir kerfisnotendum í Sales. Notandinn verður að vera virkur og hafa leyfi og má ekki vera samþættingarnotandinn. Athugaðu að þetta er fyrsta taflan sem þarf að samstilla vegna þess að hún er notuð í viðskiptavinum, tengiliðum, tækifærum og sölureikningum.|
|Forði|Tilföng eru samstillt við vörur Sales sem hafa þjónustu sem vörugerðina.|
|Verðflokkar viðskm.|Verðflokkar viðskiptavinar eru samstilltir við verðlista Sales.|
|Söluverð|Söluverð sem eru með verðflokk viðskiptavinar sem sölugerð og eru með skilgreindan sölukóða eru samstillt við verðlistalínur Sales|
|Tækifæri|Tækifæri eru samstillt við tækifæri Sales. Gildið á kóða sölumanns skilgreinir eiganda tengdu einingarinnar í Sales.|
|Bókaðir sölureikningar|Bókaðir sölureikningar eru samstilltir við sölureikninga. Áður en hægt er að samstilla reikning er betra að samstilla allar aðrar einingar sem geta verið hluti af reikningnum, frá sölumanni til verðlista. Gildið á kóða sölumanns í fyrirsögn reiknings skilgreinir eiganda tengdu einingarinnar í Sales.|

## <a name="setting-up-the-connection"></a>Uppsetning tengingarinnar
Frá upphafssíðunni geturðu nálgast leiðbeiningar um uppsetningu með hjálp fyrir **Uppsetningu Microsoft Dynamics 365 tengingar** sem hjálpar þér að setja upp tengingu. Þegar því er lokið verður þú með hnökralausa tengingu á Sales-færslum við [!INCLUDE[d365fin](includes/d365fin_md.md)] skrár.  

> [!NOTE]  
>   Eftirfarandi útskýrir uppsetningu með aðstoð, en þú getur framkvæmt sömu verkin handvirkt á síðunni **Uppsetning Sales-tengingar**.

Í aðstoðarsamskipunarleiðbeiningunni geturðu valið hvaða gögn eru samstillt á milli tveggja þjónustunnar. Þú getur einnig tilgreint að þú viljir flytja inn núverandi Sales lausnina þína. Í því tilviki verður þú að tilgreina stjórnsýslu notendareikning.

### <a name="setting-up-the-user-account-for-importing-the-solution"></a>Setja upp notandareikninginn til að flytja inn lausnina
Til að flytja inn núverandi Sales lausn, notar uppsetningarhandbókin stjórnsýslureikning. Þessi reikningur verður að vera gildur notandi í Sales með eftirfarandi öryggishlutverki:

* Kerfisstjóri  
* Lausnastilling  

Nánari upplýsingar er að finna í [Búa til notendur í Microsoft Dynamics 365 (online) og úthluta öryggishlutverkum](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles) og [Vinna með notendur og heimildir](ui-how-users-permissions.md).  

Þessi reikningur er aðeins notaður meðan á uppsetningu stendur. Þegar lausnin er flutt inn í [!INCLUDE[d365fin](includes/d365fin_md.md)] er reikningurinn ekki lengur þörf.

### <a name="setting-up-the-user-account-for-synchronization"></a>Setja upp notandareikning fyrir samstillingu
Samþættingin byggist á sameiginlegum notendareikningi. Svo í Office 365 áskriftinni þinni verður þú að búa til hollur notandi sem verður notaður til samstillingar á milli tveggja þjónustunnar. Þessi reikningur verður þegar að vera gildur notandi í Sales, en þú þarft ekki að úthluta öryggishlutverkum til reikningsins vegna þess að uppsetningarhandbókin muni gera það fyrir þig. Þú verður að tilgreina þennan notandareikning einn eða fleiri sinnum í uppsetningarhandbókinni, háð því hversu mikið samstilling þú vilt virkja. Nánari upplýsingar er að finna í [Búa til notendur í Microsoft Dynamics 365 (á netinu) og úthluta öryggishlutverkum](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles).

Ef þú velur að virkja *hlutafyrirkomulag*, verður aðgangur að notendareikningurinn að vera með aðgangstakkann fyrir vefþjónustu. Þetta er tvíþættur hlutur á [!INCLUDE[d365fin](includes/d365fin_md.md)] síðunni fyrir þennan notandareikning. Þú verður að velja **Breyta lykli vefþjónustu** og í uppsetningarhandbók Sales-tengingarinnar verður þú að tilgreina þann notanda sem notanda OData vefþjónustunnar.

Ef þú velur að gera kleift að virkja *sölupöntunarsamþætting*, verður þú að tilgreina notanda sem getur séð þessa samstillingu - samþætting notandans eða annan notandareikning.

### <a name="coupling-records"></a>Tengja skrár
Í aðstoðarsamskipunarleiðbeiningunni geturðu valið að samstilla á milli tveggja þjónustunnar. En síðar getur þú einnig sett upp samstillingu tiltekinna gerða gagna. Þetta er kallað *tenging* og í þessum kafla er að finna tillögur um það sem þú verður að taka tillit til.

Til dæmis, ef þú vilt sjá Sales reikninga sem viðskiptavini í [!INCLUDE[d365fin](includes/d365fin_md.md)], verður þú að tengja tvær tegundir af skrám. Það er ekki mjög flókið - þú opnar síðuna **Viðskiptavinalisti** í [!INCLUDE[d365fin](includes/d365fin_md.md)] og það er aðgerð í borðanum til að tengja þessi gögn við Sales. Þá tilgreinir þú hvaða [!INCLUDE[d365fin](includes/d365fin_md.md)] viðskiptavinir passa við hvaða reikninga í Sales.

Á ákveðnum sviðum byggir virknin á að þú tengir ákveðnar gagnasettir fyrir aðrar gagnasettir eins og sýnt er í eftirfarandi lista:

* Viðskiptavinir og reikningar  
  * Tengja fyrst sölumenn við Sales notendur  
* Vörur og forði  
  * Tengja mælieiningar við einingahópa Sales fyrst  
* Vörur og forðaverð  
  * Tengja verðflokka viðskiptavina við Sales fyrst  

> [!NOTE]  
>   Ef þú ert að nota verð í erlendum gjaldmiðlum skaltu ganga úr skugga um að þú tengir gjaldmiðla við færslugjaldmiðil Sales.

Í Sales velta sölupantanir á viðbótarupplýsingum eins og viðskiptavinum, mælieiningum, gjaldmiðlum, verðflokkum viðskiptavina, vörum og/eða tilföngum. Til að samþættingin með sölupöntunum gangi hnökralaust fyrir sig verður þú að tengja viðskiptavini, mælieiningar, gjaldmiðla, verðflokka viðskiptavina, vörur og/eða auðlindir fyrst.

### <a name="synchronizing-records-fully"></a>Samstilla skrár að fullu
Í lok aðstoðaruppsetningarleiðbeiningarinnar geturðu valið aðgerðina **Keyra fulla samstillingu** til að byrja að samstilla allar [!INCLUDE[d365fin](includes/d365fin_md.md)] færslur við allar tengdar skrár í tengdu Sales lausninni. Á síðunni **CRM full samstilling tengslastjórnunar** skaltu velja aðgerðina **Ræsa**. Samstillingin byrjar síðan að framkvæma störf í samræmi við ósjálfstæði. Til dæmis eru gjaldeyrisskrár samstilltar fyrir viðskiptavinaskrár. Fullur samstilling getur tekið langan tíma og mun því birtast í bakgrunni þannig að þú getir haldið áfram að vinna í [!INCLUDE[d365fin](includes/d365fin_md.md)].

Til að kanna framvindu einstakra starfa í fullri samstillingu, skal fara á **Staða verkraðarfærslu**, **Í innri vinnslustöðu töflu**, eða **Úr innri vinnslustöðu töflu** á síðunni **CRM full samstilling tengslastjórnunar**.

Frá síðunni **Uppsetning Microsoft Dynamics 365 tengingar** er hægt að fá upplýsingar um fulla samstillingu hvenær sem er. Héðan er einnig hægt að opna síðuna **Vörpun samþættingartöflu** til að sjá upplýsingar um töflurnar í [!INCLUDE[d365fin](includes/d365fin_md.md)] og í Sales lausninni sem þarf að samstilla.

## <a name="handling-special-sales-order-data"></a>Afgreiðsla sérstakra sölupöntunargagna
Sölupantanir í Sales verða fluttar sjálfkrafa í [!INCLUDE[d365fin](includes/d365fin_md.md)] ef gátreiturinn **Stofna sölupantanir sjálfkrafa** á síðunni **Uppsetning Microsoft Dynamics 365-tengingar** er valinn. Á slíkum sölupöntunum er reiturinn **Heiti** í upprunalegu pöntuninni fluttur og honum varpað í reitinn **Utanaðkomandi fylgiskjalsnúmer** á sölupöntuninni í [!INCLUDE[d365fin](includes/d365fin_md.md)].

Þetta getur líka virkað ef upprunalega sölupöntunin inniheldur innskriftarvörur, þ.e.a.s. vörur eða forða sem er skráður í hvorugri vörunni. Í því tilviki verður þú að fylla út reitina **Gerð innskriftarvöru** og **Nr. innskriftarvöru** reitirnir á síðunni **Sölugrunnur**, til þess að slíkri óskráðri vörusölu sé varpað í tiltekið vöru-/forðanúmer fyrir fjárhagsgreiningu.

Ef vörulýsingin í upprunalegu sölupöntuninni er mjög löng er stofnuð ný sölupöntunarlína af gerðinni Athugasemd til þess að rúma allan texta sölupöntunarinnar í [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="see-also"></a>Sjá einnig
[Undirbýr samþættingu við Dynamics 365 for Sales á staðnum](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration)  
[Umsjón með venslum](marketing-relationship-management.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md)  
[Vinna með notendur og heimildir](ui-how-users-permissions.md)    
[Um borð stofnunina þína og notendur til Dynamics 365 (á netinu)](/dynamics365/customer-engagement/admin/onboard-your-organization-and-users-to-dynamics-365-online)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  

