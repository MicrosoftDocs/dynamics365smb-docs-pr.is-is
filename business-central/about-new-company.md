---
title: Stofna ný fyrirtæki með notkun leiðbeininga um uppsetningu með stuðningi
description: 'Það er auðvelt að stofna nýtt, autt fyrirtæki í Business Central. Leiðsagnarforrit með hjálp hjálpar til við að fara í gegnum skrefin og flytja inn viðskiptagögnin.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 03/08/2024
ms.custom: bap-template
ms.search.keywords: 'company, setup wizard'
ms.search.form: '1803, 9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.service: dynamics-365-business-central
---
# <a name="create-new-companies-in-"></a>Stofna ný fyrirtæki í [!INCLUDE[prod_short](includes/prod_short.md)]

Í [!INCLUDE[prod_short](includes/prod_short.md)] er vísað til hólfanna fyrir viðskiptagögn, sem tilheyra fyrirtækjaeiningu eða lögaðila, sem *fyrirtæki*. Þegar þú skráir þig í [!INCLUDE[prod_short](includes/prod_short.md)], færðu sýnifyrirtæki og autt fyrirtæki, *Mitt fyrirtæki*. Auðvelt er að skipta á milli fyrirtækja, þú opnar einfaldlega **Mínar stillingar** og færir þig yfir í hitt fyrirtækið. En þú getur líka stofnað ný fyrirtæki í [!INCLUDE[prod_short](includes/prod_short.md)] allt eftir þörfum þíns fyrirtækis.  

> [!NOTE]
> Til að stofna nýtt fyrirtæki verður að úthluta þér á **yfirheimildasafnið** .

Þegar þú stofnar nýtt fyrirtæki, munu leiðbeiningar um uppsetningu með stuðningi hjálpa þér við grunnuppsetninguna. Síðan er hægt að flytja inn gögn úr eldra kerfi eða öðru fyrirtæki í [!INCLUDE[prod_short](includes/prod_short.md)].  

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## <a name="choose-the-right-template"></a>Val á réttu sniðmáti

Ef ákveðið er að bæta fyrirtæki við er hægt að [!INCLUDE[prod_short](includes/prod_short.md)] nota leiðsagnarforritið **Stofna nýtt fyrirtæki** með aðstoð til að hefjast handa. Uppsetningarleiðbeiningarnar eru aðgengilegar á síðunni **Fyrirtæki** og frá uppflettingu í reitnum **Fyrirtæki** á síðunni **Mínar** stillingar.  

Uppsetningarleiðbeiningarnar bjóða upp á þrjú sniðmát og auðan valkost:

- **Mat - Sýnigögn**  
    Stofna fyrirtæki sem er svipað og sýnifyrirtækið með sýnigögn og uppsetningargögn. Þessi tegund fyrirtækis er í boði án þess að skipta yfir í 30 daga prufuútgáfu, sem hinar tegundirnar gera.  
- **Advanced Evaluation - Complete Sýnigögn** Stofna fyrirtæki með ítarlegt virknisvið, sem hefur allt sem þú þarft til að meta vöruna fyrir fyrirtæki með háþróaða ferla. Þessi tegund fyrirtækis er í boði án þess að skipta yfir í 30 daga prufuútgáfu, sem hinar tegundirnar gera.
- **Framleiðsla - Aðeins uppsetningargögn**  
    Stofna fyrirtæki sem er svipað og Fyrirtæki notanda **, með uppsetningargögnum** eins og bókhaldslykli, greiðsluaðferðum og skilgreiningum fjárhagsskýrslu, en án sýnigagna. Hægt er að nota þetta fyrirtæki á 30 daga prufutímabili.
- **Stofna nýtt - Engin gögn**  
    Stofna autt fyrirtæki án uppsetningargagna. Hægt er að nota þetta fyrirtæki á 30 daga prufutímabili.  

Ef þú vilt byrja auðveldlega með nýtt fyrirtæki, skal velja **Framleiðsla - Aðeins uppsetningargögn** og síðan flytja inn þín eigin viðskiptagögn, eins og viðskiptamenn, vörur og lánardrottnar. Veldu sniðmátið **Nýtt** ef þú vilt setja allt upp frá grunni. Í því tilfelli, geturðu nýtt þér **Uppsetning fyrirtækis** leiðsagnarforrit með stuðningi til að stíga fyrstu skrefin með nauðsynleg uppsetningargögn.  

> [!NOTE]  
> Þegar þú stofnar nýtt fyrirtæki, líða nokkrar mínútur áður en þú getur komist inn í það í [!INCLUDE[prod_short](includes/prod_short.md)]. Uppsetningarstaðan á síðunni **Fyrirtæki** sýnir hvenær nýja fyrirtækið er tilbúið fyrir þig. Þá geturðu skipt yfir í nýja fyrirtækið með því að nota **Mínar stillingar**.  

Á 30 daga prufutíma þínum getur þú stofnað hvaða fjölda nýrra fyrirtækja sem eru, en þau eru aðeins í boði meðan á prufun stendur. Nánari upplýsingar má nálgast með því að hafa samband við [!INCLUDE[prod_short](includes/prod_short.md)] samstarfsaðila þinn. Sjá einnig greinina [Dynamics 365 Business Central Algengar spurningar um prufuútgáfu](trial-faq.md).  

Stjórnandi þinn getur fengið frekari upplýsingar um prufuútgáfur og áskriftir [hér](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions).  

## <a name="copy-a-company"></a>Afrita fyrirtæki

Á síðunni **Fyrirtæki** er hægt að nota aðgerðina **Afrita** til að stofna annað fyrirtæki út frá efni fyrirliggjandi fyrirtækis. Afritun fyrirtækis er til dæmis gagnleg þegar prófa á fyrirtæki án þess að trufla framleiðslugögn.

> [!Important]
> Ekki nota afritunaraðgerðina til að taka öryggisafrit af fyrirtæki. Ef taka á öryggisafrit er byrjað á því að flytja gagnagrunninn út sem .bacpac skrá. Frekari upplýsingar er að finna í [Flytja út gagnagrunna](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-database-export) í hjálp við þróun og stjórnun.

[!INCLUDE [email-copy-company](includes/email-copy-company.md)]

[!INCLUDE [dataverse-copy-company](includes/dataverse-copy-company.md)]

## <a name="set-up-the-company"></a>Setja upp fyrirtæki

Þegar skráð er inn í nýtt fyrirtæki hjálpar uppsetningarleiðsagnarforritið Uppsetning fyrirtækis **með** aðstoð við að hefjast handa. Leiðarvísirinn biður um upplýsingar um fyrirtækið, svo sem aðsetur, bankaupplýsingar og aðferð kostnaðarútreiknings birgða. Þessar upplýsingar eru grunnur margra svæða svo [!INCLUDE[prod_short](includes/prod_short.md)] ekki þurfi að setja þær upp handvirkt.  

Til dæmis inniheldur [!INCLUDE [prod_short](includes/prod_short.md)] heimilisfang fyrirtækisins á reikningum og öðrum skjölum og bankaupplýsingar þínar í greiðslum. Kostunaraðferðin er notuð til að reikna út verð og verðmat á birgðum.  

Þegar grunnatriðin eru til staðar er hægt að setja upp eftirstandandi kjarnasvæði. Þá er hægt að bæta inn viðskiptagögnum á borð við viðskiptamenn og lánardrottna. Nánari upplýsingar um það eru í [Setja upp [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md).  

## <a name="companies-and-environments"></a>Fyrirtæki og umhverfi

[!INCLUDE [company_environment](includes/company_environment.md)]

Frekari upplýsingar eru í [Skipta yfir í annað fyrirtæki eða umhverfi](ui-organization-switch.md). Frekari upplýsingar um umhverfi er að finna í [Að skilja tölvukerfi Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology) (eingöngu á ensku).  

## <a name="changing-a-companys-name"></a>Heiti fyrirtækis breytt

Þegar fyrirtæki hefur verið stofnað er ekki hægt að breyta heiti þess. Þó er hægt að breyta **heiti** þess Birtingar, sem er texti sem kemur fram í fyrirtækinu í öllu kerfinu.  

> [!TIP]
> Hægt er að endurnefna fyrirtæki ef [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum er notað.

## <a name="add-contoso-coffee"></a>Bæta við Contoso Coffee

Forrit Contoso Coffee býður upp á sýnigögn til að hjálpa þér að kanna ítarlega möguleika [!INCLUDE [prod_short](includes/prod_short.md)]. Finndu forritið í AppSource og settu það upp í tómu fyrirtæki, t.d. fyrirtæki í sandkassaumhverfi. Frekari upplýsingar er að finna í [Kynning á sýnigögnum Contoso Coffee](contoso-coffee/contoso-coffee-intro.md).  

## <a name="see-also"></a>Sjá einnig .

[Sérstilla Business Central](ui-customizing-overview.md)  
[Uppsetning [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Grunnstillingum breytt](ui-change-basic-settings.md)  
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Að skilja tölvukerfi Business Central Online (eingöngu á ensku)](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
