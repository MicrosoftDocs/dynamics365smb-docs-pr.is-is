---
title: "Velja greiðslumáta rafrænna greiðslna | Microsoft Docs"
description: "Meðhöndla greiðslur til lánardrottna með því að flytja út skrá með greiðsluupplýsingum á færslubókarlínur."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 8b2e20e694279a8c06188e0e429ef3b4fb43aea2
ms.openlocfilehash: 20ae505bc76b8971c678de9e2664653aa5032d6e
ms.contentlocale: is-is
ms.lasthandoff: 09/27/2017

---
# <a name="make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer"></a>Greiða með umreikningsþjónustu bankagagna eða SEPA-kreditfærslu
Í **Greiðslubók** glugganum er hægt að meðhöndla greiðslur til lánardrottna með því að flytja út skrá með greiðsluupplýsingum á færslubókarlínur. Þá er hægt að hlaða upp skránni í netbanka til að meðhöndla tengdan peningaflutning. [!INCLUDE[d365fin](includes/d365fin_md.md)] styður SEPA-kreditfærslusniðið, en í heimalandi þínu / svæði geta önnur snið fyrir rafrænar greiðslur kunna að vera tiltækir.   

 Til að gera SEPA kredifærslur, verður þú fyrst að setja upp bankareikning, lánardrottin, og almenna bókarkeyrslurunu sem greiðslubók er byggt á. Greiðslur til lánardrottna eru því næst undirbúnar með því að fylla sjálfkrafa út gluggann **Greiðslubók** með gjaldföllnum greiðslum með tilgreindum bókunardagsetningum.  

> [!NOTE]  
>  Þegar þú hefur staðfest að greiðslurnar hafi verið framkvæmdar af bankanum getur þú bókað greiðslubókarlínurnar.  

 Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.   

|**Til að**|**Sjá**|  
|------------|-------------|  
|Virkjið eiginleikann UUmreikningsþjónusta fyrir bankagögn til að umbreyta hvers kyns bankayfirlitsskrá í snið sem hægt er að flytja inn eða til að umbreyta útfluttum greiðsluskrám í það snið sem bankinn krefst.|[Hvernig á að: Setja upp umreikningsþjónustu fyrir bankagögn](bank-how-setup-bank-statement-service.md)|  
|Setja upp bankareikning, lánardrottin og greiðslubók fyrir SEPA-millifærslur.|[Hvernig á að: Setja upp SEPA-kreditfærslur](finance-how-to-set-up-sepa-credit-transfer.md)|  
|Fyllið út greiðslubókina með línum fyrir greiðslu á gjalddaga til lánardrottna með möguleikanum á að setja inn bókunardagsetningar byggt á gjalddaga tengdra innkaupaskjala.|[Umsjón viðskiptaskulda](payables-manage-payables.md)|  
|Flytja út greiðslubókarlínur í skrá í SEPA lánsfjármillifærslusniði.|[Hvernig á að: Flytja út greiðslur í bankaskrá](payables-how-export-payments-bank-file.md)|  
|Endurskoða hvaða greiðslur hafa verið flutt út og inn í hvaða skrár.|Skráningar kreditmillifærslna|  
|Þegar rafræna greiðslan hefur verið unnin að fullu af bankanum skal bóka greiðslurnar.|[Vinna í færslubókum](ui-work-general-journals.md)|  

## <a name="see-also"></a>Sjá einnig  
[Hvernig á að: Setja upp umreikningsþjónustu fyrir bankagögn](bank-how-setup-bank-statement-service.md)  
[Hvernig á að: Setja upp SEPA-kreditfærslur](finance-how-to-set-up-sepa-credit-transfer.md)  
[Gjaldföllnu stjórnað](payables-manage-payables.md)   
[Vinna í færslubókum](ui-work-general-journals.md)  
[Innheimta greiðslur með SEPA-beingreiðslum](finance-collect-payments-with-sepa-direct-debit.md)   

