---
title: "Sérsníða Dynamics 365 Business Central | Microsoft Docs"
description: "Settu saman, sýndu og kynntu forritin og viðbætur þínar fyrir Business Central."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: fc926afbf0c1442bb610531b28507fbb2c1b1cf4
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="extending-included365finlongincludesd365finlongmdmd"></a>Stækka [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]
Microsoft [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] er viðskiptahugbúnaður sem hjálpar fyrirtækjum að tengja fjármálin, sölur, þjónustu og aðgerðir sínar til að einfalda viðskiptaferla, bæta samskipti við viðskiptavini og taka betri ákvarðanir. [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] er fáanlegt í skýinu og handa notendum á alls kyns gerðum af tækjum, sem er alltaf uppfært. Með þessum nútíma viðskiptavettvangi getur þú auðveldlega og á fljótlegan hátt aðlagað, stækkað og smíðað forrit svo þau passi sérstaklega við þínar þarfir - með lítilli sem engri þróun á kóða.  

Það eru fjölmargir kostir við að nota [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] sem vettvang fyrir forritasmiði, sem eru t.a.m.:

* Byrjaðu af öryggi með óaðfinnanlega upplifun innleiðingar 
* Nota markaðssetningarþjónustu Microsoft
* Sérsníða listasíðu forritanna þinna 
* Tengstu beint við þá sem taka ákvarðanir og náðu til fleiri viðskiptavina
* Auktu virði viðskipta og auktu stærð samninga við núverandi og nýja viðskiptavini
* Afkastið meira á vettvangi sem tryggir nútímalega upplifun og býður upp á mikið umfang  
* Fáðu innsýn í frammistöðu skráninganna þinna sem hægt er að bregðast við í gegnum samstarfsgátt skýsins eða birtingarferli Office-forritsins
* Notið það samhliða snjallforritum fyrir rekstur, svo sem PowerApps, flæði, Power BI, Cortana Intelligence, og mörg fleiri  

Komdu með [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] þjónustu þína til Microsoft AppSource sem: 

**Stök forrit** - þar sem þú kemur með iðnþekkingu þína inn á markaðinn.  
**Ráðgjafarþjónustupakki** - þar sem þú kemur með tilbúna innleiðingarpakka á markaðinn.

Nýju þróunarverkfærin gera þér kleift að búa til viðbætur fyrir [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] notendur. Ef þú vilt kynna þér nýju verkfærin eða fræðast um viðbætur 2.0, skaltu kíkja á [aka.ms/GetStartedWithApps](https://aka.ms/GetStartedWithApps).  

Finndu upplýsingar um forrit og ráðgjafarþjónustur sem eru í boði á [Microsoft AppSource](https://appsource.microsoft.com/en-us/marketplace/consulting-services?country=US&page=1).

Til að hjálpa viðskiptanotendum að byrja á fljótlegan hátt hefur Microsoft bætt við vörulista af ráðgjafarþjónustum fyrir lausnir sem byggjast á [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)], Power BI og PowerApps til AppSource. Frekari upplýsingar um [Ráðgjafarþjónustur](/dynamics-nav/developer/readiness/readiness-consulting).

## <a name="choosing-which-services-to-offer-with-included365finlongincludesd365finlongmdmd"></a>Velja hvaða þjónustur til að bjóða með [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] 

### <a name="integrate-a-3rd-party-solution"></a>Samþætta lausnir þriðja aðila
[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] birtir marga API sem eru tilbúnir til notkunar fyrir [Tengja forrit](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-connect-apps) til að búa til hnökralausa samþættingu milli þjónustu þinnar og [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]. Þú getur sameinað þjónustur þínar með [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] og gefið viðskiptavinum þínum samþætta upplifun. Frekari upplýsingar um [Samþætta lausnir þriðja aðila](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-thirdparty-solution).

### <a name="development-of-a-vertical-solution"></a>Þróun á lóðréttri lausn
Búa til forrit sem sérhæfir sig í tiltekinni atvinnugrein. Með [Innleiða forrit](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-embed-apps) geturðu stækkað og sérstillt núverandi forritið [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] og auðgað upplifun notandans með sértækri virkni atvinnugreinar með því að nota ný nútímaverkfæri og viðbótaútgáfu 2.0. Frekari upplýsingar um [Þróun á lóðréttri lausn](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-develop-vertical).

### <a name="development-of-a-horizontal-solution"></a>Þróun á láréttri lausn
Víkkaðu út upplifunina og möguleikana á [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] með því að búa til [Viðbótarforrit](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-add-on-apps) sem samþættast við notendaupplifunina á [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]. Smíðaðu notandaviðmót sem byggir á því hvernig þú vilt að gögnin þín flæði á milli [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] og þjónustu þinnar. Frekari upplýsingar um [Þróun á láréttri lausn](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-develop-horizontal). 

### <a name="development-of-a-localization-solution"></a>Þróun á staðfærslulausn
Fylgdu staðbundnum eftirlitseiginleikum með því að þróa fyrir [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)], sem aðlagar virk svæði að kröfum staðbundins markaðar ásamt [Dynamics 365 þýðingarþjónustunni](/dynamics365/unified-operations/dev-itpro/lifecycle-services/translation-service-overview). Samstilltu kjarnastarfsemi staðbundinnar lagaskyldu og víkkaðu út núverandi virkni til að keppa á staðbundna markaðnum þínum með góðum árangri. Frekari upplýsingar um [Þróun á staðfærslulausn](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-develop-localization).

### <a name="reseller-solution"></a>Lausn endursöluaðila
Þar sem hvert fyrirtæki er einstakt, með [Sérstillingar leigjanda](/dynamics-nav/developer/readiness/readiness-customizing-tenants), getur þú lagað þig að því hvernig þú vinnur með einföldum ferlum þínum, hugtökum þínum og hvernig starfsmenn eða deildir tengjast og vinna saman. Að auki getur þú valið að endurselja og stilla [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] að þörfum hvers viðskiptavinar með því að veita [Ráðgjafarþjónustu](/dynamics-nav/developer/readiness/readiness-consulting). Eða notaðu Microsoft Flow, Power Apps og Power BI til að búa til [Sérsniðin verkflæði](/dynamics-nav/developer/readiness/readiness-no-code), forrit og skýrslur um innsýn í viðskipti án þess að þurfa að skrifa kóða. Frekari upplýsingar um [Endursöluaðili Dynamics 365 (VAR)](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-reseller). 

## <a name="where-do-i-learn-more"></a>Hvar finn ég frekari upplýsingar?
Til að fá frekari upplýsingar um tilboð ráðgjafarþjónustu í Microsoft AppSource skal velja eftirfarandi tengla: 

[Ráðgjafartilboð AppSource](https://appsource.microsoft.com/en-us/marketplace/consulting-services?country=US&page=1)  
[Hæfi samstarfsaðila](https://smp-cdn-prod.azureedge.net/documents/Microsoft%20AppSource%20Partner%20Listing%20Guidelines.pdf)  
[Tilnefningareyðublað samstarfsaðila](https://appsource.microsoft.com/en-us/partners/list-consulting-service)  

## <a name="the-ready-to-go-program"></a>Forritið sem er tilbúið til notkunar
Forritið sem er tilbúið til notkunar er hannað til að styðja þig við að koma með Microsoft [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] tilboðin þín í Microsoft Appsource. Í forritinu eru: 

- [Netnámskeið](https://aka.ms/ReadyToGoOnlineLearning)
- [Þjálfun og vinnustofur](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-ready-to-go)
- [Samvinnuvettvangur Microsoft](https://aka.ms/Collaborate)

Lærðu meira um hvernig þú getur byggt upp [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] tilboð í upplýsingunum [Forrit tilbúið til notkunar](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-ready-to-go). Ef þú hefur spurningar eða athugasemdir um forritið **Tilbúið til notkunar** geturðu [haft samband við okkur](mailto:dyn365bep@microsoft.com). 

## <a name="see-also"></a>Sjá einnig
[Hafist handa](product-get-started.md)  
[Sérstilling [!INCLUDE[d365fin](includes/d365fin_md.md)] með viðbótum](ui-extensions.md)  
[https://appsource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365-for-financials&page=1)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 

