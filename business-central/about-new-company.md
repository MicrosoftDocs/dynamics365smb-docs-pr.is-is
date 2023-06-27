---
title: Stofna ný fyrirtæki með notkun leiðbeininga um uppsetningu með stuðningi
description: 'Það er auðvelt að stofna nýtt, autt fyrirtæki í Business Central. Leiðbeiningar um uppsetningu aðstoðar hjálpa í gegnum verkliði og hægt er að flytja inn viðskipagögn.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 04/14/2023
ms.custom: bap-template
ms.search.keywords: 'company, setup wizard'
ms.search.form: '1803, 9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
---
# <a name="create-new-companies-in-" />Stofna ný fyrirtæki í [!INCLUDE[prod_short](includes/prod_short.md)]

Í [!INCLUDE[prod_short](includes/prod_short.md)] er vísað til hólfanna fyrir viðskiptagögn, sem tilheyra fyrirtækjaeiningu eða lögaðila, sem *fyrirtæki*. Þegar þú skráir þig í [!INCLUDE[prod_short](includes/prod_short.md)], færðu sýnifyrirtæki og autt fyrirtæki, *Mitt fyrirtæki*. Auðvelt er að skipta á milli fyrirtækja, þú opnar einfaldlega **Mínar stillingar** og færir þig yfir í hitt fyrirtækið. En þú getur líka stofnað ný fyrirtæki í [!INCLUDE[prod_short](includes/prod_short.md)] allt eftir þörfum þíns fyrirtækis.  

> [!NOTE]
> Til að stofna nýtt fyrirtæki þarf að vera úthlutað  **Super**  heimildasafni.

Þegar þú stofnar nýtt fyrirtæki, munu leiðbeiningar um uppsetningu með stuðningi hjálpa þér við grunnuppsetninguna. Þá geturðu flutt inn tilheyrandi gögn úr eldri kerfum eða öðrum fyrirtækjum í [!INCLUDE[prod_short](includes/prod_short.md)].  

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## <a name="choose-the-right-template" />Val á réttu sniðmáti

Ef ákveðið er að bæta fyrirtæki við  [!INCLUDE[prod_short](includes/prod_short.md)] er hægt að nota  **Uppsetningarleiðbeiningar stofnunar nýrra fyrirtækja**  til að byrja. Uppsetningarleiðbeiningarnar eru tiltækar frá  **síðunni fyrirtæki**  og úr uppflettingunni í  **reitnum fyrirtæki**  á  **síðunni mínar stillingar** .  

Uppsetningarhandbókin býður upp á tvö sniðmát og auðan valkost:

- **Mat - Sýnigögn**  
    Hér er stofnað fyrirtæki sem svipar til sýnifyrirtækisins hvað varðar sýnigögn og uppsetningargögn. Þessi tegund fyrirtækis er í boði án þess að skipta yfir í 30 daga prufuútgáfu, sem hinar tegundirnar gera.  
- **Framleiðsla - Aðeins uppsetningargögn**  
    Hér er stofnað fyrirtæki sem svipar til **Mitt fyrirtæki** hvað varðar uppsetningargögn, en er án sýnigagna. Hægt er að nota þetta fyrirtæki í 30 daga prufutíma.  
- **Stofna nýtt - Engin gögn**  
    Hér er stofnað autt fyrirtæki án uppsetningargagna. Hægt er að nota þetta fyrirtæki í 30 daga prufutíma.  

Ef þú vilt byrja auðveldlega með nýtt fyrirtæki, skal velja **Framleiðsla - Aðeins uppsetningargögn** og síðan flytja inn þín eigin viðskiptagögn, eins og viðskiptamenn, vörur og lánardrottnar. Veldu sniðmátið **Nýtt** ef þú vilt setja allt upp frá grunni. Í því tilfelli, geturðu nýtt þér **Uppsetning fyrirtækis** leiðsagnarforrit með stuðningi til að stíga fyrstu skrefin með nauðsynleg uppsetningargögn.  

> [!NOTE]  
> Þegar þú stofnar nýtt fyrirtæki, líða nokkrar mínútur áður en þú getur komist inn í það í [!INCLUDE[prod_short](includes/prod_short.md)]. Uppsetningarstaðan á síðunni **Fyrirtæki** sýnir hvenær nýja fyrirtækið er tilbúið fyrir þig. Þá geturðu skipt yfir í nýja fyrirtækið með því að nota **Mínar stillingar**.  

Á 30 daga reynslutímabilinu geturðu stofnað eins mörg fyrirtæki og þú vilt, en þau verða aðeins aðgengileg á meðan reynslutímabilinu stendur. Nánari upplýsingar má nálgast með því að hafa samband við [!INCLUDE[prod_short](includes/prod_short.md)] samstarfsaðila þinn. Sjá einnig greinina [Dynamics 365 Business Central Algengar spurningar um prufuútgáfu](trial-faq.md).  

Stjórnandi þinn getur fengið frekari upplýsingar um prufuútgáfur og áskriftir [hér](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions).  

## <a name="copy-a-company" />Afrita fyrirtæki

Á síðunni **Fyrirtæki** er hægt að nota aðgerðina **Afrita** til að stofna annað fyrirtæki út frá efni fyrirliggjandi fyrirtækis. Þetta er til dæmis gagnlegt þegar þú vilt prófa fyrirtæki án þess að það hafi áhrif á framleiðslugögn.

> [!Important]
> Ekki nota afritunaraðgerð til að taka öryggisafrit af fyrirtæki. Til að taka öryggisafrit er byrjað á því að flytja út gagnagrunninn sem. bacpac File. Frekari upplýsingar er að finna í [Flytja út gagnagrunna](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-database-export) í hjálp við þróun og stjórnun.

[!INCLUDE [email-copy-company](includes/email-copy-company.md)]

## <a name="set-up-the-company" />Setja upp fyrirtæki

Þegar þú skráir þig inn í nýtt fyrirtæki, mun **Uppsetning fyrirtækis** leiðsagnarforritið opnast sjálfvirkt og aðstoða þig við að komast af stað. Spurt verður um upplýsingar um fyrirtækið, eins og t.d. aðsetur, bankaupplýsingar, og aðferð kostnaðarútreiknings birgða. Við spyrjum um þessar upplýsingar þar sem þær eru notaðar sem grunnur á mörgum sviðum í [!INCLUDE[prod_short](includes/prod_short.md)], sem þú þarft þá ekki að setja handvirkt upp síðar.  

Til dæmis inniheldur [!INCLUDE [prod_short](includes/prod_short.md)] heimilisfang fyrirtækisins á reikningum og öðrum skjölum og bankaupplýsingar þínar í greiðslum. Kostunaraðferðin er notuð til að reikna út verð og verðmat á birgðum.  

Þegar grunnatriðin eru komin á sinn stað, geturðu sett upp þau grunnsvæði sem eftir eru. Þá er hægt að bæta inn viðskiptagögnum á borð við viðskiptamenn og lánardrottna. Nánari upplýsingar um það eru í [Setja upp [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md).  

## <a name="companies-and-environments" />Fyrirtæki og umhverfi

[!INCLUDE [company_environment](includes/company_environment.md)]

Frekari upplýsingar eru í [Skipta yfir í annað fyrirtæki eða umhverfi](ui-organization-switch.md). Frekari upplýsingar um umhverfi er að finna í [Að skilja tölvukerfi Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology) (eingöngu á ensku).  

## <a name="changing-a-companys-name" />Heiti fyrirtækis breytt

Þegar fyrirtæki hefur verið stofnað er ekki hægt að breyta heiti þess. En hægt er að breyta **Birtingarheiti** sem er texti sem verður sýndur fyrir fyrirtækið í gegnum forritið.  

> [!TIP]
> Hægt er að endurnefna fyrirtæki ef [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum er notað.

## <a name="add-contoso-coffee" />Bæta við Contoso Coffee

Forrit Contoso Coffee býður upp á sýnigögn til að hjálpa þér að kanna ítarlega möguleika [!INCLUDE [prod_short](includes/prod_short.md)]. Finndu forritið í AppSource og settu það upp í tómu fyrirtæki, t.d. fyrirtæki í sandkassaumhverfi. Frekari upplýsingar er að finna í [Kynning á sýnigögnum Contoso Coffee](contoso-coffee/contoso-coffee-intro.md).  

## <a name="see-related-microsoft-training" />Sjá tengda [Microsoft þjálfun](/training/modules/create-new-companies-dynamics-365-business-central/)

## <a name="see-also" />Sjá einnig .

[Sérstilla Business Central](ui-customizing-overview.md)  
[Uppsetning [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Grunnstillingum breytt](ui-change-basic-settings.md)  
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Að skilja tölvukerfi Business Central Online (eingöngu á ensku)](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
