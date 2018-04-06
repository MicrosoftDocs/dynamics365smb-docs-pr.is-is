---
title: "Safna uppsetningargildum viðskiptamanns | Microsoft Docs"
description: "Grunnstillingarspurningalisti er notaður til að draga úr álagi við innleiðingarferli með því að straumlínulaga uppsetningarferlið fyrir nýja fyrirtækið. Hægt er að útbúa uppsetningarspurningalista í Business Central og senda svo til viðskiptavinar sem Excel .xls eða XML skrá."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/07/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: a1333567069d24bc5eff48d668dca8b480b85914
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="gather-customer-setup-values"></a>Safna uppsetningargildum viðskiptamanns
Grunnstillingarspurningalisti er notaður til að draga úr álagi við innleiðingarferli með því að straumlínulaga uppsetningarferlið fyrir nýja fyrirtækið. Hægt er að útbúa grunnstillingarspurningalista í [!INCLUDE[d365fin](includes/d365fin_md.md)] og senda svo til viðskiptavinar sem Excel .xls-skrá eða XML-skrá.  

Hægt er að breyta öllum sjálfgildum í spurningalista í svo þau svari þörfum viðskiptavinar betur.  

> [!TIP]  
>  Nánari upplýsingar um skilgreiningu uppsetningargilda í reitum framboðsáætlunar eru í [.Setja upp bestu starfsvenjur: Framboðsáætlun](setup-best-practices-supply-planning.md)  

Þegar viðskiptavinur fyllir út spurningalista er skráin flutt inn í nýja [!INCLUDE[d365fin](includes/d365fin_md.md)] fyrirtæki viðskiptavinarins. Þú og viðskiptavinurinn staðfestið svörin við spurningalistanum áður en þau eru notuð fyrir fyrirtækið.

## <a name="to-create-a-configuration-questionnaire"></a>Til að búa til grunnstillingarspurningalista
Hægt er að nota spurningalista til að hjálpa til við ákvarða umfang og þarfir í skilgreiningu. Hægt er að stofna nýja spurningalista eða breyta fyrirliggjandi spurningalista með því að bæta við nýjum spurningum og spurningasvæðum.  

 Aðeins er hægt er að stofna spurningalista fyrir töflur af uppsetningargerð. Til dæmis má nota verkfærið til að veita upplýsingar í eftirtöldum gluggum:  

-   Stofngögn  
-   Eignagrunnur  
-   Uppsetning fjárhags  
-   Birgðagrunnur  
-   Uppsetning samsetningar
-   Framleiðslugrunnur  
-   Innkaupagrunnur  
-   Uppsetning markaðssetningar  
-   Þjónustukerfisgrunnur  
-   Sölugrunnur  
-   Vöruhúsagrunnur  

> [!NOTE]  
>  Til að sjá heildarlista uppsetningartaflna skal velja táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslutákni"), slá inn **Uppsetning** og velja svo viðeigandi tengil. Til að ákvarða svið flutnings færslugagna skal nota flutningsaðgerðir. Frekari upplýsingar eru í [Flutningur á gögnum viðskiptamanns](admin-migrate-customer-data.md).  

1. Velja skal táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslutákn"), slá inn **Grunnstillingarspurningalisti** og velja svo viðeigandi tengil.  
2. Valið er **Nýtt** aðgerð. Glugginn **Stilla Spurningalisti** opnast.  
3. Veljið aðgerðina **Spurningasvæði**. Glugginn **Spurningasvæði** opnast.  
4. Valið er **Nýtt** aðgerð. Glugginn **Stillingar spurningasvæðis** opnast.  
5. Í reitnum **Töflukenni** veljið auðkenni töflunnar sem á að safna upplýsingum. Reiturinn **Heiti töflu** útfyllist sjálfkrafa.  
6. Velja skal aðgerðina **Uppfæra spurningar**. Hverju svæði í töflunni er bætt við spurningalista með spurningarmerki á eftir merkinu.

Hægt er að endurorða merkið til að gera skýrt hvernig svara á spurningu. Til dæmis ef svæði er kallað „Heiti“ er hægt að breyta því í „Hvað heitir <data being collected>.“ Einnig er hægt að veita leiðsögn í reitnum **Tilvísun**, sem inniheldur vefslóð á síðu sem veitir frekari upplýsingar.  

Einnig er hægt að eyða spurningum sem á ekki að taka með í spurningalistann.  

> [!NOTE]  
>  **Svarmöguleiki** reiturinn lýsir tegund og sniði svars gagnanna sem við á. **Svar** reiturinn inniheldur upplýsingar frá notendum.  
>   
>  Eftir þörfum er einnig hægt að skilgreina sjálfgefin svör í reitnum **Svar**. Þessi gildi eru notuð að sjálfgefnu fyrir sérsniðna uppsetningu. Hins vegar getur aðeins sá sem fyllir út spurningalistinn breytt og uppfært svarið.  

## <a name="to-complete-the-configuration-questionnaire"></a>Ljúka við grunnstillingarspurningalista
Grunnstillingarspurningalistinn er notaður til að móta og skrá nákvæma umræðu um sérstakar þarfir viðskiptavinar. Hann er einnig notaður til að safna uppsetningargögnum frá viðskiptavini til að stilla viðeigandi [!INCLUDE[d365fin](includes/d365fin_md.md)] uppsetningartöflur, s.s.fjárhag, birgðir og viðskiptavini.  

> [!NOTE]  
>  Einnig er hægt að búa til nýjan grunnstillingarspurningarlista til að mæta þínum þörfum.  

1. Opnaðu fyrirtækið sem þú vilt klára spurningalista fyrir.
2. Velja skal táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslutákn"), slá inn **Grunnstillingarspurningalisti** og velja svo viðeigandi tengil.  
3. Veldu spurningalistann fyrir fyrirtækið og veldu síðan aðgerðina **Flytja út í Excel**, mögulega aðgerðina **Flytja út í XML**.
4. Fáðu viðskiptavininn til að ljúka við grunnstillingarspurningalistann með því að færa svörin inn í Excel-vinnubókina. Til eru vinnublöð fyrir hvert spurningasvæði sem búið var til fyrir spurningalistann.   
5. Veldu aðgerðina **Flytja inn úr Excel** og veldu .xlsx-skrána með svörum viðskiptavinarins.  
6. Veldu aðgerðina **Spurningasvæði** til að hefja ferli villuleitar og bæta svörunum við grunnstillingarspurningalistann.  

## <a name="to-complete-a-questionnaire-from-the-configuration-worksheet"></a>Til að ljúka spurningalista úr grunstillingarvinnublaðinu  
Næsta ferli býður upp á annars konar aðgang að grunnstillingarspurningalistum. Gert er ráð fyrir að grunnstillingarpakkinn sem veittur hefur verið innihaldi spurningalista.  

1. Þegar búið er að flytja inn grunnstillingarpakka, er grunnstillingarvinnublaðið opnað.  
2. Fyrir hverja töflu þar sem er að finna spurningasvæði skal velja aðgerðina **Spurningar**. Síða spurningalistans opnast.  
3. Svaraðu spurningunum og veldu svo aðgerðina **Nota svör**.  
4. Velja hnappinn **Í lagi** aftur til að loka spurningalistanum.

## <a name="to-validate-the-configuration-questionnaire"></a>Villuleita grunnstillingarspurningalistann
Mikilvægt er að villuleita grunnstillingarspurningalistann áður en hann er notaður á sniðið [!INCLUDE[d365fin](includes/d365fin_md.md)]. Það er líka leið til að tryggja að gagnasnið haldist við innflutning úr Excel.  

Algengt villuleitarverk er að tryggja að textastrengir séu ekki færðir inn í dagsetningareiti. Þetta endurskoðunarferli er nauðsynlegt þar sem snið svarsins í spurningalistanum er ekki sannvottað sjálfkrafa þegar aðgerðin **Nota svör** er keyrð.  

> [!NOTE]  
>  Villuleit grunnstillingarspurningalista er yfirleitt handvirkt ferli. Hins vegar er hægt að athuga ósamræmi í stillingum svæða. Auk þess munu villur koma upp ef skipulag [!INCLUDE[d365fin](includes/d365fin_md.md)] gagnagrunnsins passar ekki við skipulag innflutta gagnagrunnsins.  

1. Í glugganum **Grunnstillingarspurningalisti** skal velja spurningarnar sem eiga við og síðan velja aðgerðina **Spurningasvæði**.  
2. Opna viðeigandi spurningasvæðið.  
3. Fyrir hverja spurningu skal sannprófa að gildið í reitnum **Svar** samsvari sniðinu í reitnum **Svarmöguleiki**. Til dæmis skal tryggja að aðsetur fyrirtækis er á textasniði.  
4. Ef villur finnast er hægt að leita úrræða og gera leiðréttingar í Excel með því að flytja spurningalistann út og síðan aftur inn. Að öðrum kosti er einnig hægt að leiðrétta villur beint í [!INCLUDE[d365fin](includes/d365fin_md.md)] um leið og farið er yfir svörin í glugganum **Grunnstilling spurningasvæðis**.  
5. Endurtaka skal þessi skref fyrir hvert Spurningasvæði.  

Eftir að gengið hefur verið frá villuleit, eru gögn notanda tilbúin til notkunar í gagnagrunni.  

## <a name="to-apply-answers-from-the-configuration-questionnaire"></a>Nota svör úr spurningalista grunnstillingar
Þegar búið er að flytja inn og staðfesta upplýsingar úr grunnstillingarspurningalistanum, er hægt að flytja eða nota uppsetningargögnin í samsvarandi töflum í [!INCLUDE[d365fin](includes/d365fin_md.md)] gagnagrunninum.  

1. Velja skal táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslutákn"), slá inn **Grunnstillingarspurningalisti** og velja svo viðeigandi tengil. Glugginn **Stilla Spurningalisti** opnast.  
2. Veljið grunnstillingarspurningalista úr listanum og veljið síðan aðgerðina **Breyta lista**.  
3. Hægt er að nota svör á tvo vegu.  

- Til að nota allan spurningalistann skal velja aðgerðina **Nota svör**.  
- Til að nota svör aðeins fyrir tiltekið **Spurningasvæði** skal velja aðgerðina **Spurningasvæði**, velja **Spurningasvæði** í listanum og velja svo aðgerðina **Nota svör**.  

### <a name="to-verify-that-answers-have-been-applied-successfully"></a>Til að staðfesta að tekist hafi að nota svör  
1. Athuga uppsetningarglugga eftir ýmsum virkum svæðum af [!INCLUDE[d365fin](includes/d365fin_md.md)]. Til að finna gluggann skal velja táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslutákni"), slá inn heiti á uppsetningarglugganum og velja svo viðeigandi tengil.  
2. Staðfestu að reitirnir hafi verið fylltir út með réttum gögnum úr hinum ýmsu spurningasvæðum í grunnstillingarspurningalistanum.  

Nú hefur uppsetning með fyrirtækjaupplýsingum og reglum viðskiptavinar verið skilgreind.

## <a name="see-also"></a>Sjá einnig  
[Uppsetning fyrirtækis með RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Stjórnun](admin-setup-and-administration.md)

