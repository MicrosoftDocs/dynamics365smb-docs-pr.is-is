---
title: Safna uppsetningargildum viðskiptamanns | Microsoft Docs
description: Grunnstillingarspurningalisti er notaður til að draga úr álagi við innleiðingarferli með því að straumlínulaga uppsetningarferlið fyrir nýja fyrirtækið. Hægt er að útbúa grunnstillingarspurningalista í Business Central og senda svo til viðskiptavinar sem Excel (.xlsx) eða XML-skrá.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: af8d2bb31b5f76912d69b123803243cfce1445bd
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783975"
---
# <a name="gather-customer-setup-values"></a>Safna uppsetningargildum viðskiptamanns
Grunnstillingarspurningalisti er notaður til að draga úr álagi við innleiðingarferli með því að straumlínulaga uppsetningarferlið fyrir nýja fyrirtækið. Hægt er að útbúa grunnstillingarspurningalista í [!INCLUDE[prod_short](includes/prod_short.md)] og senda svo til viðskiptavinar sem Excel .xls-skrá eða XML-skrá.  

Hægt er að breyta öllum sjálfgildum í spurningalista í svo þau svari þörfum viðskiptavinar betur.  

> [!TIP]  
>  Nánari upplýsingar um skilgreiningu uppsetningargilda í reitum framboðsáætlunar eru í [.Setja upp bestu starfsvenjur: Framboðsáætlun](setup-best-practices-supply-planning.md)  

Þegar viðskiptavinur fyllir út spurningalista er skráin flutt inn í nýja [!INCLUDE[prod_short](includes/prod_short.md)] fyrirtæki viðskiptavinarins. Þú og viðskiptavinurinn staðfestið svörin við spurningalistanum áður en þau eru notuð fyrir fyrirtækið.

## <a name="to-create-a-configuration-questionnaire"></a>Til að búa til grunnstillingarspurningalista
Hægt er að nota spurningalista til að hjálpa til við ákvarða umfang og þarfir í skilgreiningu. Hægt er að stofna nýja spurningalista eða breyta fyrirliggjandi spurningalista með því að bæta við nýjum spurningum og spurningasvæðum.  

<!-- A configuration questionnaire has the following structure
* The name of the questionnaire itself
* Question Areas that group questions about a similar subject. For example, you might create a question area that focuses on entering company informtion. Typically, configuration questionnaires have many question groups
* Questions that are closed ended, meaning that the customer must choose an answer, and can choose only one. -->

 Aðeins er hægt er að stofna spurningalista fyrir töflur af uppsetningargerð. Til dæmis má nota verkfærið til að veita upplýsingar á eftirtöldum síðum:  

-   Fyrirtækjaupplýsingar  
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
>  Til að sjá heildarlista yfir uppsetningartöflur skaltu velja ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Handvirk uppsetning** og veldu síðan tengda tengilinn. Til að ákvarða svið flutnings færslugagna skal nota flutningsaðgerðir. Frekari upplýsingar eru í [Flutningur á gögnum viðskiptamanns](admin-migrate-customer-data.md).  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Spurningalisti grunnstillingar** og veldu tengda tengilinn.  
2. Valið er aðgerðin **Nýtt**.   
3. Á síðunni **Spurningalisti grunnstillingar**, í reitnum **Kóði** skal slá inn ... 
<!--4. In the **Name** field, enter...
5. Choose the **Question Areas** action. .
6. On the **Config. Question Areas** page, in the **Code** field, enter...
  
    > [!Note]  
    > The code is alphanumeric, and must start with a letter of the alphabet.
7. In the Table ID field, choose the table to which to apply the answer to the question. Your selection will determine the fields that are available for the questions, and thereby the answer selections.
  
    > [!Tip]
    > The list of table objects is long. If you know the name of the table, use **Search** in the upper left to find it in the list.
8. In the **Description** field, enter text that indicates the subject of the question group.
9. In the **No.** field, enter a number to define where the question appears in the sequence of questions.
10. In the **Field ID** field, choose the field the the customer's answer will be applied to. You can choose from the fields on the table you chose in the **Table ID** field.
  
    When you choose a field, [!INCLUDE[prod_short](includes/prod_short.md)] provides a suggestion in the **Question** field. You can edit the question if needed.
11. To add more questions to the questionnaire, repeat steps seven through 10.

> [!Tip]
> If at some point you change a question, or add a new one, choose the **Update Questions** action to update the list.

-->

3. Veljið aðgerðina **Spurningasvæði**. Síðan **Spurningasvæði** opnast.  
4. Valið er **Nýtt** aðgerð. Síðan **Stillingar spurningasvæðis** opnast.  
5. Í reitnum **Töflukenni** veljið auðkenni töflunnar sem á að safna upplýsingum. Reiturinn **Heiti töflu** útfyllist sjálfkrafa.  
6. Velja skal aðgerðina **Uppfæra spurningar**. Hverju svæði í töflunni er bætt við spurningalista með spurningarmerki á eftir merkinu.

Hægt er að endurorða merkið til að gera skýrt hvernig svara á spurningu. Til dæmis ef svæði er kallað „Heiti“ er hægt að breyta því í „Hvað heitir <data being collected>.“ Einnig er hægt að veita leiðsögn í reitnum **Tilvísun**, sem inniheldur vefslóð á síðu sem veitir frekari upplýsingar.  

Einnig er hægt að eyða spurningum sem á ekki að taka með í spurningalistann.  

> [!NOTE]  
>  **Svarmöguleiki** reiturinn lýsir tegund og sniði svars gagnanna sem við á. **Svar** reiturinn inniheldur upplýsingar frá notendum.  
>   
>  Eftir þörfum er einnig hægt að skilgreina sjálfgefin svör í reitnum **Svar**. Þessi gildi eru notuð að sjálfgefnu fyrir sérsniðna uppsetningu. Hins vegar getur aðeins sá sem fyllir út spurningalistinn breytt og uppfært svarið.  

## <a name="to-complete-the-configuration-questionnaire"></a>Ljúka við grunnstillingarspurningalista
Grunnstillingarspurningalistinn er notaður til að móta og skrá nákvæma umræðu um sérstakar þarfir viðskiptavinar. Hann er einnig notaður til að safna uppsetningargögnum frá viðskiptavini til að stilla viðeigandi [!INCLUDE[prod_short](includes/prod_short.md)] uppsetningartöflur, s.s.fjárhag, birgðir og viðskiptavini.  

> [!NOTE]  
>  Einnig er hægt að búa til nýjan grunnstillingarspurningarlista til að mæta þínum þörfum.  

1. Opnaðu fyrirtækið sem þú vilt klára spurningalista fyrir.
2. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Spurningalisti grunnstillingar** og veldu síðan tengda tengilinn.  
3. Veldu spurningalistann fyrir fyrirtækið og veldu síðan aðgerðina **Flytja út í Excel**, mögulega aðgerðina **Flytja út í XML**.
4. Fáðu viðskiptavininn til að ljúka við grunnstillingarspurningalistann með því að færa svörin inn í Excel-vinnubókina. Til eru vinnublöð fyrir hvert spurningasvæði sem búið var til fyrir spurningalistann.   
5. Vistaðu Excel-vinnubókina sem *XML Data*. Veldu aðgerðina **Flytja inn úr XML** og veldu .xml-skrána með svörum viðskiptavinarins.
6. Veldu aðgerðina **Spurningasvæði** til að hefja ferli villuleitar og bæta svörunum við grunnstillingarspurningalistann.  

## <a name="to-complete-a-questionnaire-from-the-configuration-worksheet"></a>Til að ljúka spurningalista úr grunstillingarvinnublaðinu  
Næsta ferli býður upp á annars konar aðgang að grunnstillingarspurningalistum. Gert er ráð fyrir að grunnstillingarpakkinn sem veittur hefur verið innihaldi spurningalista.  

1. Þegar búið er að flytja inn grunnstillingarpakka, er grunnstillingarvinnublaðið opnað.  
2. Fyrir hverja töflu þar sem er að finna spurningasvæði skal velja aðgerðina **Spurningar**. Síða spurningalistans opnast.  
3. Svaraðu spurningunum og veldu svo aðgerðina **Nota svör**.  
4. Velja hnappinn **Í lagi** aftur til að loka spurningalistanum.

## <a name="to-validate-the-configuration-questionnaire"></a>Villuleita grunnstillingarspurningalistann
Mikilvægt er að villuleita grunnstillingarspurningalistann áður en hann er notaður á sniðið [!INCLUDE[prod_short](includes/prod_short.md)]. Það er líka leið til að tryggja að gagnasnið haldist við innflutning úr Excel.  

Algengt villuleitarverk er að tryggja að textastrengir séu ekki færðir inn í dagsetningareiti. Þetta endurskoðunarferli er nauðsynlegt þar sem snið svarsins í spurningalistanum er ekki sannvottað sjálfkrafa þegar aðgerðin **Nota svör** er keyrð.  

> [!NOTE]  
>  Villuleit grunnstillingarspurningalista er yfirleitt handvirkt ferli. Hins vegar er hægt að athuga ósamræmi í stillingum svæða. Auk þess munu villur koma upp ef skipulag [!INCLUDE[prod_short](includes/prod_short.md)] gagnagrunnsins passar ekki við skipulag innflutta gagnagrunnsins.  

1. Á síðunni **Grunnstillingarspurningalisti** skal velja spurningarnar sem eiga við og síðan velja aðgerðina **Spurningasvæði**.  
2. Opna viðeigandi spurningasvæðið.  
3. Fyrir hverja spurningu skal sannprófa að gildið í reitnum **Svar** samsvari sniðinu í reitnum **Svarmöguleiki**. Til dæmis skal tryggja að aðsetur fyrirtækis er á textasniði.  
4. Ef villur finnast er hægt að leita úrræða og gera leiðréttingar í Excel með því að flytja spurningalistann út og síðan aftur inn. Að öðrum kosti er hægt að leiðrétta villur beint í [!INCLUDE[prod_short](includes/prod_short.md)] um leið og farið er yfir svörin á síðunni **Grunnstillingar spurningasvæðis**.  
5. Endurtaka skal þessi skref fyrir hvert Spurningasvæði.  

Eftir að gengið hefur verið frá villuleit, eru gögn notanda tilbúin til notkunar í gagnagrunni.  

## <a name="to-apply-answers-from-the-configuration-questionnaire"></a>Nota svör úr spurningalista grunnstillingar
Þegar búið er að flytja inn og staðfesta upplýsingar úr grunnstillingarspurningalistanum, er hægt að flytja eða nota uppsetningargögnin í samsvarandi töflum í [!INCLUDE[prod_short](includes/prod_short.md)] gagnagrunninum.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Spurningalisti grunnstillingar** og veldu síðan tengda tengilinn. Síðan **Stilla spurningalista** opnast.  
2. Veljið grunnstillingarspurningalista úr listanum og veljið síðan aðgerðina **Breyta lista**.  
3. Hægt er að nota svör á tvo vegu.  

- Til að nota allan spurningalistann skal velja aðgerðina **Nota svör**.  
- Til að nota svör aðeins fyrir tiltekið **Spurningasvæði** skal velja aðgerðina **Spurningasvæði**, velja **Spurningasvæði** í listanum og velja svo aðgerðina **Nota svör**.  

### <a name="to-verify-that-answers-have-been-applied-successfully"></a>Til að staðfesta að tekist hafi að nota svör  
1. Athuga uppsetningarsíður eftir ýmsum virkum svæðum af [!INCLUDE[prod_short](includes/prod_short.md)]. Til að staðsetja síðuna velurðu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, slærð inn heiti uppsetningarsíðunnar og velur síðan tengda tengilinn.  
2. Staðfestu að reitirnir hafi verið fylltir út með réttum gögnum úr hinum ýmsu spurningasvæðum í grunnstillingarspurningalistanum.  

Nú hefur uppsetning með fyrirtækjaupplýsingum og reglum viðskiptavinar verið skilgreind.

## <a name="see-also"></a>Sjá einnig  
[Uppsetning fyrirtækis með RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Stjórnun](admin-setup-and-administration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]