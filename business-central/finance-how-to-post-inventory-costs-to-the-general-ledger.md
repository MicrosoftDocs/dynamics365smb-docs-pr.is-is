---
title: Stemma af birgðakostnað við fjárhagur
description: Við lok bókhaldstímabila þarf að framkvæma röð kostnaðarstjórnunar- og endurskoðunarverkhluta til að tilkynna rétt og jafnað birgðavirði.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'warehouse, stock'
ms.search.form: 9297
ms.date: 07/31/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Stemma af birgðakostnað við fjárhagur

Þegar birgðafærslur, til dæmis söluafhending, innkaupareikningur eða birgðaleiðrétting eru bókaðar eru breytingar á kostnaði hinnar leiðréttu vöru skráðar í virðisfærslum birgða. Til að endurspegla þessar breytingar á birgðavirði í ársreikningum, er birgðakostnaður bókaður sjálfkrafa á tengda birgðareikninga í fjárhag. Fyrir hverja birgðafærslu sem er bókuð er viðeigandi gildi bókað í birgðareikninginn, leiðréttingarreikninginn og KSV-reikninginn í fjárhagnum.

Sjálfvirk kostnaðarbókun er skilgreind í reitnum **Sjálfvirk kostnaðarbókun** á síðunni **Uppsetning birgða**.

Jafnvel þó birgðakostnaður sé sjálfkrafa bókaður í fjárhagur er samt nauðsynlegt að tryggja að kostnaður vara sé áframsendur til tengdra söluviðskipta á útleið, sérstaklega þegar vörur eru seldar áður en keyptar eru vörur. Í kerfinu er þetta kallað kostnaðarleiðrétting. Vörukostnaður er sjálfkrafa leiðréttur þegar vörufærslur eru bókaðar en einnig er hægt að leiðrétta vörukostnað handvirkt. Nánari upplýsingar eru í [Leiðrétta kostnað](inventory-how-adjust-item-costs.md).

## Handvirk bókun birgðakostnaðar

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, farðu í **Bóka birgðakostnað í fjárhag** og veldu síðan tengda tengilinn.
2. Birgðakostnaður er bókaður handvirkt í fjárhaginn með því að keyra runuvinnsluna. Þegar þessi keyrsla er keyrð eru fjárhagsfærslur stofnaðar á grundvelli virðisfærslna. Hægt er að bóka færslurnar svo að þær séu teknar saman eftir bókunarflokki.

> [!NOTE]  
> Þegar þessi keyrsla er keyrð gæti kerfið rekist á villur sem hafa með uppsetningu sem vantar að gera eða ósamhæfa víddaruppsetningu. Ef keyrslan rekst á villur í víddaruppsetningunni hefur hún þessar villur að engu og notar víddir virðisfærslunnar. Í tilfelli annarra villna hoppar runuvinnslan yfir bókun virðisfærslnanna og telur þær upp við lok skýrslunnar í hluta sem heitir “Færslur sem hoppað var yfir.” Til að bóka þessar færslur þarf að laga villurnar.

Hægt er að sjá lista af villum áður en bókunarrunuvinnslan er keyrð með því að keyra skýrsluna **Bóka birgðabreytingar - Prófun**. Prófunarskýrslan telur upp allar þær villur sem finnast meðan á bókuninni stendur. Þá er hægt að laga villurnar og keyra bókunarkeyrslu birgðakostnaðar án þess að sleppa neinum færslum.

Ef fá á yfirlit yfir það hvaða gildi væri hægt að bóka í fjárhagur án þess að framkvæma bókunina er hægt að keyra **keyrsluna Bóka birgðakostnað í fjárhag** án þess að bóka gildin í fjárhagur í raun. Hægt er að gera þetta með því að taka hakið úr reitnum **Bóka** á beiðnisíðunni. Þegar keyrslan er keyrð er skýrslan framleidd og sýnir gildin sem eru tilbúin til bókunar í fjárhagur en ekki bókuð.

## Endurskoða afstemmingu á milli birgðabókar og fjárhags.
Síðan **Birgðir - Fjárhagsafstemmingar** veitir eftirfarandi:

- Sýnir mun á afstemmingu með því að bera saman skráningar í fjárhag og birgðahöfuðbók (virðisfærslur).
- Birtir óafstemmdar kostnaðarupphæðir í virðisfærslum í birgðahöfuðbók eins og þeim væri varpað á samsvarandi birgðatengda reikninga í fjárhag og ber þær saman við samtölurnar sem skráðar eru í sömu reikninga í fjárhag.
- Sýnir uppbyggingu fjárhags með tvöföldum færslum með myndrænni uppsetningu gagna. KSV-færsla hefur t.d. samsvarandi birgðafærslu.
- Gerir notendum kleift að kafa niður og sjá færslur sem kostnaðarupphæð er samsett úr.
- Er með afmörkunum svo hægt sé að þrengja greiningu eftir dagsetningu, vöru og birgðageymslu.
- Skýrir ástæður fyrir frávikum í afstemmingu með skilaboðum með upplýsingum.


Í dálkinum **Heiti** lengst til vinstri í grindinni sjást ýmsar tegundir fjárhagsreikninga sem tengjast birgðunum.

Dálkarnir **Birgðir**, **Birgðir (Bráðabirgða)**, og **VÍV birgðir** sýna reikningsfært, óreikningsfært, og samtölu VÍV fyrir hverja tegund fjárhagsreiknings. Þær eru reiknaðar út frá virðisfærslum, það er, þær eru áætlaðar á fjárhagsreikningstegundirnar þar sem þeim lýkur þegar þær eru að lokum bókaðar í fjárhag.

Dálkurinn **Samtala** sýnir summu (feitletraða) virðisfærsluupphæða í þremur birgðadálkum.

**Samtala fjárhags** sýnir upphæðirnar (feitletraðar) fyrir hverja tegund fjárhagsreiknings í fjárhag. Þær eru reiknaðar með fjárhagsfærslum, það er tákna birgðakostnað sem þegar hefur verið bókaður í Fjárhag.

Dálkurinn **Mismunur** sýnir muninn á gildinu í reitunum **Samtala fjárhags** og **Samtala**.

Efst á síðunni **Birgðir - Afstemming fjárhags** er hægt að færa inn afmarkanir til að afmarka t.d. tímabil sem sækja á upplýsingar fyrir.

Ef gátmerki er sett í reitinn **Sýna viðvörun** og misræmi er á milli birgðasamtala og fjárhagssamtala birtir forritið skilaboð í **Viðvörun** reit grindarinnar þar sem misræmið er útskýrt. Ef viðvörunarreiturinn er valinn birtir forritið meiri upplýsingar um merkingu viðvörunarinnar.

Þegar þú hefur fært inn allar viðeigandi afmarkanir, skal velja **Sýna fylki** aðgerðina. Gögnin eru reiknuð og fylkjasíðan opnast.

Í dálkinum lengst til vinstri í grindinni sjást ýmsar tegundir fjárhagsreikninga sem tengjast birgðunum. Grindin sýnir því næst reikningsfærðar, óreikningsfærðar og VÍV birgðasamtölur fyrir hverja reikningstegund. Þessar samtölur eru reiknaðar út frá virðisfærslum.

Næstu dálkar sýna samtölur sömu reikningstegunda sem reiknaðar voru úr fjárhagsfærslunum.

Veldu upphæðina í hvaða samtölureit sem er til að sjá birgðaskýrslufærslurnar sem voru notaðar við útreikninginn. Fyrir birgðasamtölur eru birgðaskýrslufærslurnar summur virðisfærslna fyrir vörurnar. Fyrir fjárhagssamtölur eru birgðaskýrslufærslurnar summur úr fjárhagsfærslum.

## Tilkynna kostnað og afstemma við fjárhag
Aðrar skýrslur, rakningaraðgerðir og sérstakt afstemmingarverkfæri eru í boði til endurskoðanda eða fjármálastjóra sem ber ábyrgð á því að tilkynna um rétt og samhæft birgðavirði til fjármáladeildar.

Eftirfarandi tafla lýsir þeim.    

|**Til að**|**Sjá**|  
|------------|-------------|  
|Skoða birgðavirði valinna vara, þ.m.t. upplýsingar um magn og gildi hækkana og lækkana í birgðum á tilteknu tímabili.|**Birgðavirðis** skýrsla|  
|Skoða birgðamat tiltekinna framleiðslupantana í VÍV-birgðum (verk í vinnslu), eins og magn og virði notkunar, nýtingu afkastagetu og frálag framleiðslupantana sem eru í vinnslu.|**Birgðavirði - VÍV** skýrsla|  
|Skoða birgðamat valinna vara, þ.m.t. raunkostnað og væntanlegan kostnað þeirra á valinni dagsetningu.|**Verðm. birgða - Lýsing kostn.** skýrsla|  
|Nota skýrslu til að finna ástæður fyrir kostnaðarfrávikum eða fá innsýn í kostnaðarhlut seldra vara.|**Sundurliðun kostnaðarhlutdeild** skýrsla|  

## Sjá einnig .  
[Birgðakostnaði stjórnað](finance-manage-inventory-costs.md)    
[Innkaup](purchasing-manage-purchasing.md)    
[Sala](sales-manage-sales.md)    
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    
[Almenn viðskiptavirkni](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]