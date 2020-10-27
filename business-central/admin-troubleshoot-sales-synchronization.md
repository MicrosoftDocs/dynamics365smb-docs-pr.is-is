---
title: Úrræðaleit vegna samstillingarvillna | Microsoft Docs
description: Veitir leiðbeiningar til að finna og leysa samstillingarvillur.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: db8b05aa74583d8ba74fcfeb8fae1d3c28893fac
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922393"
---
# <a name="troubleshooting-synchronization-errors"></a>Úrræðaleit vegna samstillingarvillna
Margir hreyfanlegir hlutir taka þátt í samþættingu [!INCLUDE[d365fin](includes/d365fin_md.md)] við Common Data Service og stundum fer eitthvað úrskeiðis. Þetta efnisatriði bendir á nokkrar dæmigerðar villur sem koma upp og gefur ýmis ráð um hvernig á að laga þær.

Villur koma oft upp annaðhvort vegna þess að notandi hefur gert eitthvað við tengdar færslur eða eitthvað er að uppsetningu samþættingar. Notendur geta leyst úr villum sem tengjast tengdum færslum. Þessar villur stafa af aðgerðum eins og að eyðing á færslu í öðru, en ekki báðum, viðskiptaforritunum og síðan samstilla. Frekari upplýsingar er að finna í [Skoða stöðu á samstillingu](admin-how-to-view-synchronization-status.md).

## <a name="example"></a>Dæmi
Þetta myndband sýnir dæmi um hvernig leita á úrræða út af villum sem komu upp við samstillingu við Sales. Ferlið verður það sama fyrir allar samþættingar. 

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]

Villur sem tengjast því hvernig samþættingin er sett upp þurfa venjulega á athygli stjórnanda að halda. Hægt er að skoða þessar villur á síðunni **Villur í samstillingu samþættingar** . Dæmigerð vandamál eru til að mynda:  
  
* Heimildum og hlutverkum sem notanda er úthlutað eru ekki rétt.  
* Reikningur stjórnanda var tilgreindur sem samþættingarnotandinn.  
* Aðgangsorð samþættingarnotanda er stillt þannig að þurfi að breyta því þegar notandi skráir sig inn.  
* Gengi gjaldmiðla er ekki tilgreint í öðru hvoru forritinu.  
  
Leysa þarf villurnar handvirkt, en til eru nokkrar leiðir sem síðan hjálpar þér með. Dæmi:  

* Reitirnir **Uppruni** og **Endastaður** kunna að innihalda tengla á færsluna þar sem villan fannst. Smelltu á tengilinn til að opna færsluna og skoða villuna.  
* Aðgerðirnar **Eyða færslum eldri en sjö daga** og **Eyða öllum færslum** hreinsa listana. Venjulega eru þessar aðgerðir notaðar eftir að orsök villu sem hefur áhrif á margar færslur hefur verið löguð. Sýndu samt aðgát. Þessar aðgerðir gætu eytt villum sem skipta enn máli.

Stundum geta tímastimplarnir í færslum valdið árekstrum. Taflan „CDS-samþættingarfærsla“ heldur tímastimplunum „Síðustu samstillingu breytt þann“ og „Síðustu samstillingu CDS breytt þann“ fyrir síðustu samþættingu lokið í báðar áttir fyrir færslu. Þessir tímastimplar eru bornir saman við tímastimpla á færslum Business Central og sölu. Í Business Central er tímastimpillinn í töflunni „Samþættingarfærsla“.

Hægt er að afmarka færslur sem eiga að vera samstilltar með því að bera saman færslutímastimpla í töflunni „Vörpun samþættingartöflu“, svæðunum „Samst. breytt á afmörkun“ og „Samst. innr. töfl. breyt. Á afmörkun“.

Árekstrarvilluboðin „Ekki er hægt að uppfæra viðskiptamannafærslu vegna þess að hún er með eldri breytingardagsetningu en reikningsfærslan“ eða „Ekki er hægt að uppfæra Lykilfærsluna vegna þess að hún er með eldri breytingardagsetningu en viðskiptamannafærslan“ geta birst ef færsla er með tímastimpil sem er stærri en IntegrationTableMapping. „Samst. breytt á afmörkun“ en hún er ekki nýlegri en tímastimpill á Sölusamþættingarfærslu. Þetta þýðir að upprunafærslan var samstillt handvirkt, ekki með verkraðarfærslu. 

Áreksturinn gerist vegna þess að viðtökufærslunni var einnig breytt – Tímastimpill færslunnar er nýlegri en tímastimpill Sölusamþættingarfærslu. Viðtökustaðarathugunin er aðeins framkvæmd fyrir tvístefnutöflur. 

Þessar færslur eru nú fluttar á síðuna „Samst.færslur sem var sleppt“ sem er opnuð er úr á tengingaruppsetningarsíðu Microsoft Dynamics í Business Central. Þar er hægt að tilgreina breytingarnar sem á að halda og samstilla síðan færslurnar aftur.

## <a name="remove-couplings-between-records"></a>Fjarlægja tengingu milli færslna
Þegar eitthvað fer úrskeiðis í samþættingunni og nauðsynlegt er að aftengja færslur til að stöðva samstillingu þeirra á milli, þá er hægt að gera slíkt fyrir eina eða fleiri færslur í einu. Á síðunni **Vörpun samþættingartöflu** er hægt að velja **Aftengja** og síðan **Eyða tengingu** . Einnig er hægt á síðunni **Samstillingarvillur í tengdum gögnum** að velja villurnar og síðan velja **Fjarlægja tengingar** . 

## <a name="see-also"></a>Sjá einnig
[Samþætting við Common Data Service](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Uppsetning á notendareikningum fyrir samþættingu við Common Data Service](admin-setting-up-integration-with-dynamics-sales.md)  
[Uppsetning á tengingu við Common Data Service](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Tengja og samstilla færslur handvirkt](admin-how-to-couple-and-synchronize-records-manually.md)  
[Skoða stöðu á samstillingu](admin-how-to-view-synchronization-status.md)  
