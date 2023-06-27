---
title: Breyta grunnstillingum fyrir núverandi notanda
description: 'Kynntu þér hvernig þú getur breytt sumum stillingum í Business Central, til dæmis hlutverkinu þínu og Mitt hlutverk, fyrirtæki, vinnudagsetningu og tímabelti.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'change Role Center, notification, change company, change work date, decimal separator'
ms.search.form: '9022, 9019, 9027, 9020, 9026, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 08/31/2022
ms.author: jswymer
---
# <a name="change-basic-settings"></a>Breyta grundvallarstillingum

Á síðunni **Stillingar mínar** er hægt að sjá og breyta grunnstillingum fyrir [!INCLUDE[prod_short](includes/prod_short.md)]. Breytingar sem þú gerir munu aðeins hafa áhrif á vinnusvæðið þitt, ekki vinnusvæði annarra notenda.  

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## <a name="role"></a><a name="role-center"></a>Hlutverk

Hlutverkið táknar heimasíðuna, upphafssíðu sem er hönnuð fyrir þarfir tiltekins hlutverks í fyrirtækinu. Það fer eftir hlutverki þínu, en heimasíðan þín eða Mitt hlutverk gefur þér yfirlit yfir fyrirtækið, deildina þína eða persónuleg verkefnin þín. Það hjálpar þér líka að komast í daglegu verkefnin þín og finna vinnu sem þér er úthlutað.

* Efst gerir yfirlitið þér kleift að skipta á milli viðskiptavina, lánardrottna, vara og annarra mikilvægra lista yfir upplýsingar. Á svipaðan hátt leyfa aðgerðir þér að hefja verkefni, svo sem að búa til nýjan sölureikning, beint af heimasíðunni.

* Fyrir miðju er að finna svæðið **Aðgerðir** sem sýnir núverandi gögn og má velja til að skoða nákvæmari upplýsingar. Afkastavísa má setja upp til að sýna valin myndrit svo fáist myndræn framsetning af, til dæmis, fjárstreymi´ og tekjum og útgjöldum. Þú getur einnig byggt upp lista af uppáhalds viðskiptavinum á heimasíðunni fyrir reikninga sem þú ert oft í viðskiptum við eða þarft að veita sérstaka athygli.

### <a name="change-the-role"></a>Breyta hlutverki

Sjálfgefið hlutverk þitt er **Viðskiptastjórnandi**, en hægt er að velja annað hlutverk sem uppfyllir þarfir þínar betur.  

1. Í efra hægra horninu skaltu velja **Stillingar** táknið ![Stillingar](media/ui-experience/settings_icon_small.png "Stillingatákn fyrir hlutverkamiðstöð") og velja síðan aðgerðina **Stillingar mínar**.
2. Á síðunni **Mínar stillingar** á svæðinu **Hlutverk**, skal velja hlutverkið sem á að nota sem sjálfgefið. Veljið til dæmis **Bókari**.
3. Velja **Í lagi**.

## <a name="company"></a><a name="company"></a>Fyrirtæki

Fyrirtæki virkar sem geymsluhólf fyrir gögn í [!INCLUDE[prod_short](includes/prod_short.md)]. Hægt er að hafa mörg fyrirtæki í gagnagrunni, en aðeins hægt að velja eitt í einu. Sjálfgefið fyrirtæki er kallað CRONUS og inniheldur aðeins kynningargögn.

Reiturinn **Fyrirtæki** sýnir fyrirtækið sem þú ert að vinna í og þú getur notað hann til að skipta yfir í annað fyrirtæki. Heiti fyrirtækisins er alltaf birt uppi í vinstra horninu og virkar sem aðgerð sem hægt er að velja til að fara til baka í Mitt hlutverk.

> [!TIP]
> Einnig er hægt að breyta fyrirtækinu með því að nota fyrirtækjaskiptinn (Crtl+O). Frekari upplýsingar um þennan eiginleika og aðrar leiðir til að breyta fyrirtæki eða umhverfi er að finna í [Skipta yfir í annað fyrirtæki eða umhverfi](ui-organization-switch.md).

Sjálfgefið fyrirtæki er kallað CRONUS og inniheldur aðeins kynningargögn. Þú getur stofnað nýtt fyrirtæki með sérstilltum gögnum. Nánari upplýsingar eru í [Stofna ný fyrirtæki](about-new-company.md).

<!--
### <a name="to-change-the-company-name"></a>To change the company name

The company name is always displayed at the top left corner and works as an action that you can choose to go back to the Role Center. You can change this name on the **Company Information** page.

1. Choose the ![Sprocket icon to open the Settings menu.](media/ui-experience/settings_icon_small.png) icon, and then choose the **Company Information** action.
2. In the **Name** field, enter the new company name.
3. Leave the page. The system restarts and displays the new company in the top-left corner.

### <a name="to-display-a-company-badge-for-quick-access-to-company-information"></a><a name="badge"></a>To display a company badge for quick access to company information

You can add a customized badge in the top-right corner, which you can choose to quickly view company name and tenant information in a pop-up box. The company badge is also useful when [!INCLUDE[prod_short](includes/prod_short.md)] is embedded in another application, like Microsoft Teams or in some other web application. In these cases, because the [!INCLUDE[web_client](includes/web_client.md)] displays less surrounding contextual information, the company badge serves as the only way to determine which company or environment a record belongs to.

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Company Information**, and then choose the related link.
2. On the **Company Badge** FastTab, fill in the fields as necessary. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

> [!NOTE]
> If a company badge is defined, then you cannot change the company name as described in [To change the company name](ui-change-basic-settings.md#to-change-the-company-name)-->

## <a name="work-date"></a><a name="work-date"></a>Vinnudagur

Dagsetningin sem er algengust er dagurinn í dag. Þú gætir þurft að breyta tímabundið vinnudagsetningu til að framkvæma verk, eins og að klára færslur fyrir dagsetningu sem er ekki núverandi dagsetning.

> [!TIP]  
> Í öllum dagsetningarreitum skal slá inn **t** til að færa aftur inn daginn í dag og slá inn **w** til að færa fljótt inn vinnudagsetninguna sem er gildið í reitnum **Vinnudagsetning** á síðunni **Mínar stillingar**.

> [!IMPORTANT]  
> Eftir að vinnudagsetningu er breytt, ef þú skráir þig út eða skiptir yfir í annað fyrirtæki, mun vinnudagsetningin fara aftur á sjálfgefna vinnudagsetningu. Svo næst þegar þú skráir þig inn eða skiptir aftur í upprunalega fyrirtækið gætir þú þurft að stilla vinnudagsetninguna aftur.

### <a name="work-date-indication"></a>Ábending um vinnudagsetningu

Vinnudagsetningin er mikilvæg á síðum sem hægt er að breyta. Hvenær sem vinnudagsetningin er ekki stillt á daginn í dag á breytanlegri síðu birtast tvær gerðir af vísum á síðunni:

* Áminning birtist efst á síðunni sem segir til um hvað vinnudagsetningin er stillt á. Áminningin býður upp á beina tengingu við verkdagsetningarstillingu á síðuna **Mínar stillingar** svo þú breytir dagsetningunni ef þú vilt. Í innheimtubréfinu er einnig hægt að velja að sleppa áminningu fyrir restina af lotunni. Ef vinnudagsetningunni er breytt í „í dag“ birtist áminning næst þegar þú skráir þig inn.

* Ef áminningu er lokað birtist vinnudagsetningin í titli síðunnar.  

Ef vinnudagsetning er ekki stillt á núverandi dag (daginn í dag), þá á öllum síðum þar sem hægt er að breyta gögnum, er núverandi vinnudagsetning sýnd efst í vinstra horninu.

## <a name="region"></a><a name="region"></a> Svæði

**Svæði** stillingin ákvarðar hvernig dagsetningar, tímasetningar, númer og gjaldmiðlar eru sýndir eða forsniðnir. Hún ákvarðar líka hvaða stafur er notaður sem skiltákn tugabrots þegar talnalyklaborð er notað til að slá inn gögn. Frekari upplýsingar eru í [Gagnainnfærsla](ui-enter-data.md#decimal).

## <a name="language"></a><a name="language"></a> Tungumál

Breyta birtingartungumáli. Þessi reitur birtist aðeins þegar það er meira en eitt tungumál til að velja úr.

Upphafstungumálið er annaðhvort ákveðið af kerfisstjóra eða stillingum vafrans þegar þú skráir þig fyrir [!INCLUDE[prod_short](includes/prod_short.md)]. Tungumálið sem þú setur verður notað á öllum tækjum sem þú skráir þig inn í, svo sem síma eða spjaldtölvu.

Fleiri tungumál fyrir [!INCLUDE[prod_short](includes/prod_short.md)] er hægt að setja upp úr AppSource. Þótt öll studd tungumál viðmóts séu sýnd á listanum verður stjórnandi að setja upp viðeigandi tungumálaforrit í leigjandann áður en notendur geta skipt yfir í nýja tungumálið í [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="time-zone"></a>Tímabelti

Tilgreinir tímabeltið þar sem þú ert. Við fyrstu innskráningu á [!INCLUDE [prod_short](includes/prod_short.md)] er tímabeltið stillt út frá aðsetri fyrirtækisins. Breytið þessu ef það passar ekki við raunverulega staðsetningu.  

## <a name="notifications"></a>Tilkynningar

Veljið *Breyta þegar ég fæ tilkynningar* til að skoða eða breyta tilkynningum um tiltekin tilvik eða breytingar á stöðu, líkt og þegar þú ert að fara að reikningsfæra viðskiptamann sem er með gjaldfallna stöðu, eða þegar tiltækar birgðir eru lægri en magnið sem þú ert að fara að selja. Frekari upplýsingar er að finna á [Stjórnun tilkynninga](ui-smart-notifications.md).

## <a name="teaching-tips"></a>Kennsluábendingar

[!INCLUDE [ua-teachingtips](includes/ua-teachingtips.md)]

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft þjálfun](/training/modules/personalize-ui-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig .

[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md)  
[Stofna ný fyrirtæki](about-new-company.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
