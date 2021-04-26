---
title: Úrræðaleit vegna samstillingarvillna | Microsoft Docs
description: Veitir leiðbeiningar til að finna og leysa samstillingarvillur.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: bb3c0684d476fbba2a23a73dd821384d32afbbab
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777042"
---
# <a name="troubleshooting-synchronization-errors"></a>Úrræðaleit vegna samstillingarvillna
[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

Margir hreyfanlegir hlutir taka þátt í samþættingu [!INCLUDE[prod_short](includes/prod_short.md)] við [!INCLUDE[prod_short](includes/cds_long_md.md)] og stundum fer eitthvað úrskeiðis. Þetta efnisatriði bendir á nokkrar dæmigerðar villur sem koma upp og gefur ýmis ráð um hvernig á að laga þær.

Villur koma oft upp annaðhvort vegna þess að notandi hefur gert eitthvað við tengdar færslur eða eitthvað er að uppsetningu samþættingar. Notendur geta leyst úr villum sem tengjast tengdum færslum. Þessar villur stafa af aðgerðum eins og að eyðing á gögnum í öðru, en ekki báðum, viðskiptaforritunum og síðan samstilla. Frekari upplýsingar er að finna í [Skoða stöðu á samstillingu](admin-how-to-view-synchronization-status.md).

## <a name="example"></a>Dæmi
Þetta myndband sýnir dæmi um hvernig leita á úrræða út af villum sem komu upp við samstillingu við Sales. Ferlið verður það sama fyrir allar samþættingar. 

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]

Villur sem tengjast því hvernig samþættingin er sett upp þurfa venjulega á athygli stjórnanda að halda. Hægt er að skoða þessar villur á síðunni **Villur í samstillingu samþættingar**. Dæmigerð vandamál eru til að mynda:  
  
* Heimildum og hlutverkum sem notanda er úthlutað eru ekki rétt.  
* Reikningur stjórnanda var tilgreindur sem samþættingarnotandinn.  
* Aðgangsorð samþættingarnotanda er stillt þannig að þurfi að breyta því þegar notandi skráir sig inn.  
* Gengi gjaldmiðla er ekki tilgreint í öðru hvoru forritinu.  
  
Leysa þarf villurnar handvirkt, en til eru nokkrar leiðir sem síðan hjálpar þér með. Dæmi:  

* Reitirnir **Uppruni** og **Endastaður** kunna að innihalda tengla á línuna þar sem villan fannst. Smellið á tengilinn til að rannsaka villuna.  
* Aðgerðirnar **Eyða færslum eldri en sjö daga** og **Eyða öllum færslum** hreinsa listana. Venjulega eru þessar aðgerðir notaðar eftir að orsök villu sem hefur áhrif á margar færslur hefur verið löguð. Sýndu samt aðgát. Þessar aðgerðir gætu eytt villum sem skipta enn máli.

Stundum geta tímastimplarnir í færslum valdið árekstrum. Taflan „CDS-samþættingarfærsla“ heldur tímastimplunum „Síðustu samstillingu breytt þann“ og „Síðustu samstillingu CDS breytt þann“ fyrir síðustu samþættingu lokið í báðar áttir fyrir færslu. Þessir tímastimplar eru bornir saman við tímastimpla á færslum Business Central og sölu. Í Business Central er tímastimpillinn í töflunni „Samþættingarfærsla“.

Hægt er að afmarka færslur sem eiga að vera samstilltar með því að bera saman línustimpla í töflunni „Vörpun samþættingartöflu“, svæðunum „Samst. breytt á afmörkun“ og „Samst. innr. töfl. breyt. Á afmörkun“.

Árekstrarvilluboðin „Ekki er hægt að uppfæra viðskiptamannafærslu vegna þess að hún er með eldri breytingardagsetningu en reikningsfærslan“ eða „Ekki er hægt að uppfæra Lykilfærsluna vegna þess að hún er með eldri breytingardagsetningu en viðskiptamannafærslan“ geta birst ef línan er með tímastimpil sem er stærri en IntegrationTableMapping. „Samst. breytt á afmörkun“ en hún er ekki nýlegri en tímastimpill á Sölusamþættingarfærslu. Þetta þýðir að upprunalínan var samstillt handvirkt, ekki með verkraðarfærslu. 

Áreksturinn gerist vegna þess að viðtökulínunni var einnig breytt – Tímastimpill línunnar er nýlegri en tímastimpill Sölusamþættingarfærslu. Viðtökustaðarathugunin er aðeins framkvæmd fyrir tvístefnutöflur. 

Þessar færslur eru nú fluttar á síðuna „Samst.færslur sem var sleppt“ sem er opnuð er úr á tengingaruppsetningarsíðu Microsoft Dynamics í Business Central. Þar er hægt að tilgreina breytingarnar sem á að halda og samstilla síðan færslurnar aftur.

## <a name="remove-couplings-between-records"></a>Fjarlægja tengingu milli færslna
Þegar eitthvað fer úrskeiðis í samþættingunni og nauðsynlegt er að aftengja færslur til að stöðva samstillingu þeirra á milli, þá er hægt að gera slíkt fyrir eina eða fleiri færslur í einu. Hægt er að aftengja eina eða fleiri færslur af listasíðum eða síðunni **Samstillingarvillur í tengdum gögnum** með því að velja eina eða fleiri línu og velja **Eyða tengingu**. Einnig er hægt að fjarlægja allar tengingar fyrir eina eða fleiri töfluvörpun á síðunni **Vörpun samþættingartöflu**. 

## <a name="see-also"></a>Sjá einnig
[Samþætting við Microsoft Dataverse](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Uppsetning á notendareikningum fyrir samþættingu við Microsoft Dataverse](admin-setting-up-integration-with-dynamics-sales.md)  
[Uppsetning á tengingu við Microsoft Dataverse](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Tengja og samstilla færslur handvirkt](admin-how-to-couple-and-synchronize-records-manually.md)  
[Skoða stöðu á samstillingu](admin-how-to-view-synchronization-status.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]