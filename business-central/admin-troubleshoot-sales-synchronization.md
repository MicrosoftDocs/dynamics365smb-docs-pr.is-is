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
ms.date: 06/11/2019
ms.author: bholtorf
ms.openlocfilehash: bb6d0837f91240eb31abc7c02895cf2da420bf7d
ms.sourcegitcommit: 8fe694b7bbe7fc0456ed5a9e42291218d2251b05
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/04/2019
ms.locfileid: "1726791"
---
# <a name="troubleshooting-synchronization-errors"></a>Úrræðaleit vegna samstillingarvillna
Margir hreyfanlegir hlutir taka þátt í samþættingu [!INCLUDE[d365fin](includes/d365fin_md.md)] við [!INCLUDE[crm_md](includes/crm_md.md)] og stundum fer eitthvað úrskeiðis. Þetta efnisatriði bendir á nokkrar dæmigerðar villur sem koma upp og gefur ýmis ráð um hvernig á að laga þær.

Villur koma oft upp annaðhvort vegna þess að notandi hefur gert eitthvað við tengdar færslur eða eitthvað er að uppsetningu samþættingar. Notendur geta leyst úr villum sem tengjast tengdum færslum. Þessar villur stafa af aðgerðum eins og að eyðing á færslu í öðru, en ekki báðum, viðskiptaforritunum og síðan samstilla. Frekari upplýsingar er að finna í [Skoða stöðu á samstillingu](admin-how-to-view-synchronization-status.md).

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]

Villur sem tengjast því hvernig samþættingin er sett upp þurfa venjulega á athygli stjórnanda að halda. Hægt er að skoða þessar villur á síðunni **Villur í samstillingu samþættingar**. Dæmigerð vandamál eru til að mynda:  
  
* Heimildum og hlutverkum sem notanda er úthlutað eru ekki rétt.  
* Reikningur stjórnanda var tilgreindur sem samþættingarnotandinn.  
* Aðgangsorð samþættingarnotanda er stillt þannig að þurfi að breyta því þegar notandi skráir sig inn.  
* Gengi gjaldmiðla er ekki tilgreint í öðru hvoru forritinu.  
  
Leysa þarf villurnar handvirkt, en til eru nokkrar leiðir sem síðan hjálpar þér með. Dæmi:  

* Reitirnir **Uppruni** og **Endastaður** kunna að innihalda tengla á færsluna þar sem villan fannst. Smelltu á tengilinn til að opna færsluna og skoða villuna.  
* Aðgerðirnar **Eyða færslum eldri en sjö daga** og **Eyða öllum færslum** hreinsa listana. Venjulega eru þessar aðgerðir notaðar eftir að orsök villu sem hefur áhrif á margar færslur hefur verið löguð. Sýndu samt aðgát. Þessar aðgerðir gætu eytt villum sem skipta enn máli.

## <a name="see-also"></a>Sjá einnig
[Samþætting við [!INCLUDE[crm_md](includes/crm_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Uppsetning á notendareikningum fyrir samþættingu við [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)  
[Uppsetning á tengingu við [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Tengja og samstilla færslur handvirkt](admin-how-to-couple-and-synchronize-records-manually.md)  
[Skoða stöðu á samstillingu](admin-how-to-view-synchronization-status.md)  