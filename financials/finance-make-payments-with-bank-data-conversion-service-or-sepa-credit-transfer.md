---
title: "Greiða með umreikningsþjónustu bankagagna eða SEPA-kreditfærslu | Microsoft Docs"
description: "Meðhöndla greiðslur til lánardrottna með því að flytja út skrá með greiðsluupplýsingum á færslubókarlínur."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/17/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: 0760b5480b3c2de9bc370526bd87da2c9a492d92
ms.contentlocale: is-is
ms.lasthandoff: 12/14/2017

---
# <a name="making-payments-with-bank-data-conversion-service-or-sepa-credit-transfer"></a>Greiða með umreikningsþjónustu bankagagna eða SEPA-kreditfærslu
Í **Greiðslubók** glugganum er hægt að meðhöndla greiðslur til lánardrottna með því að flytja út skrá með greiðsluupplýsingum á færslubókarlínur. Þá er hægt að hlaða upp skránni í netbanka til að meðhöndla tengdan peningaflutning. [!INCLUDE[d365fin](includes/d365fin_md.md)] styður SEPA-kreditfærslusniðið, en í heimalandi þínu / svæði geta önnur snið fyrir rafrænar greiðslur kunna að vera tiltækir.   

 Til að gera SEPA kredifærslur, verður þú fyrst að setja upp bankareikning, lánardrottin, og almenna bókarkeyrslurunu sem greiðslubók er byggt á. Greiðslur til lánardrottna eru því næst undirbúnar með því að fylla sjálfkrafa út gluggann **Greiðslubók** með gjaldföllnum greiðslum með tilgreindum bókunardagsetningum.  

> [!NOTE]  
>  Þegar þú hefur staðfest að greiðslurnar hafi verið framkvæmdar af bankanum getur þú bókað greiðslubókarlínurnar.  

 Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.   

|**Til að**|**Sjá**|  
|------------|-------------|  
|Virkjið eiginleikann UUmreikningsþjónusta fyrir bankagögn til að umbreyta hvers kyns bankayfirlitsskrá í snið sem hægt er að flytja inn eða til að umbreyta útfluttum greiðsluskrám í það snið sem bankinn krefst.|[Hvernig á að: Setja upp umreikningsþjónustu fyrir bankagögn](bank-how-setup-bank-statement-service.md)|  
|Setja upp bankareikning, lánardrottin og greiðslubók fyrir SEPA-millifærslur.|[Hvernig á að: Setja upp SEPA-kreditfærslur](finance-how-to-set-up-sepa-credit-transfer.md)|  
|Fyllið út greiðslubókina með línum fyrir greiðslu á gjalddaga til lánardrottna með möguleikanum á að setja inn bókunardagsetningar byggt á gjalddaga tengdra innkaupaskjala.|[Stjórna skuldum](payables-manage-payables.md)|  
|Flytja út greiðslubókarlínur í skrá í SEPA lánsfjármillifærslusniði.|[Hvernig á að: Flytja út greiðslur í bankaskrá](payables-how-export-payments-bank-file.md)|  
|Þegar rafræna greiðslan hefur verið unnin að fullu af bankanum skal bóka greiðslurnar.|[Vinna í færslubókum](ui-work-general-journals.md)|  

## <a name="see-also"></a>Sjá einnig  
[Hvernig á að: Setja upp umreikningsþjónustu fyrir bankagögn](bank-how-setup-bank-statement-service.md)  
[Hvernig á að: Setja upp SEPA-beingreiðslur](finance-how-to-set-up-sepa-credit-transfer.md)  
[Stjórna skuldum](payables-manage-payables.md)   
[Vinna í færslubókum](ui-work-general-journals.md)  
[Innheimta greiðslur með SEPA-beingreiðslum](finance-collect-payments-with-sepa-direct-debit.md)   

