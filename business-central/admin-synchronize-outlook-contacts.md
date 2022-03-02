---
title: Deila tengiliðum milli Business Central og Outlook
description: Þessi þjónusta hefur djúpa samþættingu við Microsoft 365 svo þú getir samnýt tengiliði milli Outlook og Business Central.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, Microsoft 365
ms.search.form: 6700, 5320, 5300, 5301, 5302, 5303, 5304, 5305, 5306, 5307, 5308, 5309, 5310, 5311
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 12ce99a79f465543ecc314b5042e70b6802f86ec
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2022
ms.locfileid: "8142420"
---
# <a name="synchronize-contacts-in-business-central-with-contacts-in-microsoft-outlook"></a>Samstilla tengiliði í Business Central við tengiliði í Microsoft Outlook

Þú getur séð sömu tengiliði í [!INCLUDE[prod_short](includes/prod_short.md)] eins og þú sérð í Outlook ef þú setur upp samstillingu tengiliðar. Til dæmis, ef þú ert sölumaður gætir þú gert eitthvað af vinnunni þinni í Outlook og eitthvað af vinnu þinni í [!INCLUDE[prod_short](includes/prod_short.md)]. Ef tengiliðirnir eru þeir sömu á báðum stöðum er vinnan þín einfaldari.  

Sérstök mappa í Outlook gerir auðvelt um vik að finna tengiliði og þú getur stillt síu til að samstilla aðeins tengiliðina frá [!INCLUDE[prod_short](includes/prod_short.md)] sem þú vilt sjá í Outlook. Þegar samstilling samskipta er sett upp geturðu byrjað samstillingu handvirkt eða sett upp sjálfvirka samstillingu sem mun halda tengiliðunum í samstillingu með reglulegu millibili.  

## <a name="set-up-synchronization"></a>Uppsetning samstillingar
Þú setur upp hvernig þú vilt samstilla tengiliði með Outlook á síðunni **Uppsetning Exchange-samstillingar** í [!INCLUDE[prod_short](includes/prod_short.md)]. Sem forsenda verður notandaprófíllinn þinn í [!INCLUDE[prod_short](includes/prod_short.md)] að tilgreina tölvupóstreikninginn þinn Microsoft 365. Þú getur athugað þetta í hlutanum **Microsoft 365 Sannvottun** notendaforstillingarinnar á listanum **Notendur**.  

Síðan á síðunni **Uppsetning Exchange-samstillingar** getur þú sannprófað að tengingin við Exchange virki og síðan sett upp samstillingu samskipta. Opnaðu síðuna **Uppsetning samstillingar tengiliða** og byrjaðu samstillinguna. Valfrjálst er að stilla síu til að velja úr þá tengiliði sem á að samstilla milli [!INCLUDE[prod_short](includes/prod_short.md)] og Outlook. Til dæmis er hægt að stilla síu fyrir nafn, gerð, fyrirtæki eða álíka. Þú getur einnig breytt sjálfgefna heiti möppunnar sem tengiliðirnir munu samstillast í Outlook. Sjálfgefið heiti er *Business Central*.  

Þegar þessi samstilling hefur verið sett upp, eru allar breytingar sem þú gerir á tengiliðnum í annaðhvort Outlook eða í [!INCLUDE[prod_short](includes/prod_short.md)] samstilltast við hvort annað.  

Sérhver samstarfsfélagi þinn getur einnig sett upp eigin Exchange-samstillingu og sett sína eigin síu til að velja úr hvaða tengiliði skal samstilla.  

## <a name="synchronize-contacts"></a>Samstilla tengiliði
Ef þú ert vanur því að vinna með tengiliði í [!INCLUDE[prod_short](includes/prod_short.md)], þá mun þér finnast það auðvelt að hefja samstillinguna handvirkt hvenær sem það hentar þér úr listanum **Tengiliðir**. Veldu **einfaldlega Aðgerðina Samstilla við Microsoft 365** og ákveddu síðan hvort breyta eigi afmörkuninni sem þú hefur sett upp. Þegar þú velur hnappinn „Í lagi“ byrjar samstillingin strax og nýjustu breytingum er komið á tengiliðina þína í Outlook.  

Í listanum **Tengiliðir** geturðu samstillt tengiliði á tvo vegu:

* **Samstilla við Microsoft 365**

  Þessi aðgerð samstillir allar breytingar frá [!INCLUDE[prod_short](includes/prod_short.md)]Microsoft 365 frá fyrri samstillingu, byggt á síðustu breyttu dagsetningu. Allir nýir tengiliðir frá Microsoft 365 verða einnig samstilltir við [!INCLUDE[prod_short](includes/prod_short.md)]. Þetta er venjulega hraðar en að gera fulla samstillingu.  

* **Full sync með Microsoft 365**

  Þessi aðgerð samstillir alla tengiliði í báðar áttir óháð síðasta samstillingardegi og síðasta breytingardegi.  

Í báðum tilvikum eru tengiliðir aðeins samstilltir frá Outlook ef þeir hafa nauðsynlega reiti útfyllta. Nauðsynleg svæði sem á að samstilla við Microsoft 365 eru **Name**, **Netfang** og þau verða að vera af gerðinni Einstaklingur. [!INCLUDE[prod_short](includes/prod_short.md)] er aðalsniðmát tengslaupplýsinganna, þannig að [!INCLUDE[prod_short](includes/prod_short.md)] tengslaupplýsingarnar verða vistaðar ef tvítekningar eiga sér stað.  

Í Outlook eru tengiliðirnir frá [!INCLUDE[prod_short](includes/prod_short.md)] sýndir í möppu undir **Aðrir tengiliðir** í yfirlitinu **Einstaklingar**. Ef þú þekkir ekki einstaklingsyfirlitið í Outlook, þá geturðu farið í það frá leiðsagnavalkostunum neðst til vinstri í Outlook.  

## <a name="see-also"></a>Sjá einnig
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Fjármál](finance.md)  
[Sala](sales-manage-sales.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Nota tengiliði (einstaklinga) í Outlook á vefnum](https://support.office.com/article/Using-contacts-People-in-Outlook-on-the-web-1e3438c7-26b2-420c-87de-3cea9d31b5cb?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]