---
title: Flokkun gagnanæmis
description: Þú verður að tilgreina hvaða gerð af gögnum þú geymir um fólk svo að þú getir svarað beiðnum frá viðföngum gagnanna.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.form: '1752,'
ms.date: 04/19/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="classifying-data-sensitivity-fields"></a>Flokkun gagnanæmisreita

Til að flokka reiti sem innihalda viðkvæm eða persónuleg gögn getur Microsoft samstarfsaðili stillt eiginleikann ```DataClassification``` á reitum. Þetta krefst aðgangs að gagnagrunnstöflum, annaðhvort í gegnum þróunarumhverfið eða með því að keyra Windows PowerShell forskrift. Nánari upplýsingar eru í [Flokkun gagna](/dynamics365/business-central/dev-itpro/developer/devenv-classifying-data).  

Sem viðskiptavinur getur þú bætt við öðru stigi flokkunar með því að tilgreina trúnaðarstig gagnanna sem þú geymir í stöðluðum og sérsniðnum reitum. Flokkun gagnatrúnaðar hjálpar til við að tryggja að þú veist hvar þú geymir persónuleg gögn í kerfinu þínu og auðveldar þér að svara beiðnum frá viðföngum gagnanna. Til dæmis, ef tengiliður eða viðskiptavinur biður þig um að flytja út persónuupplýsingar hans. Nánari upplýsingar eru í [Svara beiðnum um persónuleg gögn](admin-responding-to-requests-about-personal-data.md).

> [!Important]  
> Microsoft útvegar þessa flokkunaraðgerð á gagnatrúnaði eingöngu til hægðarauka. Það er á þína ábyrgð að flokka gögnin á viðeigandi hátt og fara eftir lögum og reglugerðum sem eiga við. Microsoft afsalar sér allri ábyrgð gagnvart kröfum sem tengjast flokkun þinni á gögnunum.  

Eftirfarandi tafla lýsir stigum gagnatrúnaðar sem þú getur úthlutað.

|Viðkvæmni|Description|
|----|----|
|Viðkvæmt | Gagnaupplýsingar um kynþátt eða þjóðernisuppruna einstaklings, pólitískar skoðanir, trúarbrögð, þátttaka í stéttarfélögum, líkamlega eða andlega heilsu, kynhneigð eða upplýsingar um lögbrot. |
|Persónulegt | Upplýsingar sem hægt er að nota til að bera kennsl á viðfang gagnanna, annaðhvort beint eða í sambandi við önnur gögn eða upplýsingar.|
|Trúnaðarmál | Viðskiptagögn sem þú notar fyrir bókhald eða í öðrum viðskiptatilgangi og ekki eru ætluð öðrum aðilum. Til dæmis gæti þetta átt við um fjárhagsfærslur.|
|Venjul. | Almenn gögn sem heyra ekki undir aðra flokka.|

## <a name="how-do-i-classify-my-data"></a>Hvernig flokka ég gögnin mín?

Að flokka viðkvæmni á miklu magni reita, einn reit í einu, tekur langan tíma. Til að hjálpa til við að flýta því ferli bjóðum við upp á verkfæri sem hægt er að nota til að magnflokka viðkvæmni reita og síðan fínstilla flokkanir fyrir tiltekna reiti. Finna má verkfæri á síðunni Vinnublað gagnaflokkunar sem er að finna í Stjórnun notenda, notendaflokka og hlutverkamiðstöðvar heimilda. Þú verður að vera kerfisstjóri til að nota vinnublaðið.
 
> [!Important]  
> Þegar síðan Vinnublað gagnaflokkunar er opnað í fyrsta skipti verður hún tóm. Þú verður að keyra leiðbeiningar gagnaflokkunar til að búa til lista yfir reiti. Til að byrja leiðbeiningarnar skal velja aðgerðina **Setja upp gagnaflokkanir**.

Til dæmis gerir síðan Vinnublað gagnaflokkunar kleift að gera hluti eins og:  

* Notaðu leiðbeiningar gagnaflokkunar til að flytja út reitina þína í Excel vinnublað þar sem þú getur magnflokkað þá. Notkun á Excel vinnublaðinu er sérstaklega gagnleg ef þú ert að vinna með Microsoft samstarfsaðila. Eftir að þú hefur uppfært vinnublaðið getur þú notað leiðbeiningarnar til að flytja inn og beita flokkunum. Einnig er hægt að nota leiðbeiningarnar til að flokka reiti handvirkt.  
* Veldu reit og síaðu síðan listann til að finna svipaða reiti sem líklegt er að tilheyra sömu flokkuninni og reiturinn sem þú byggðir leitina á.  
* Rannsakaðu reit með því að skoða innihald hans.  

> [!Tip]  
> Við höfum skilgreint dæmi um flokkun á viðkvæmni fyrir töflur og reiti í sýnifyrirtækinu Cronus. Þú getur notað þessar flokkanir til að fá hugmyndir um eigin flokkun á töflum og reitum.

## <a name="see-also"></a>Sjá einnig .

<!-- [Classifying Data](/dynamics365/business-central/dev-itpro/developer/devenv-classifying-data) -->
[!INCLUDE[footer-include](includes/footer-banner.md)]
