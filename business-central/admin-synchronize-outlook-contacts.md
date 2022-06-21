---
title: Samnýta tengiliði milli Viðskiptamiðis og Outlook
description: Þessi þjónusta er djúp Samþætting við Microsoft 365 svo hægt sé að samnýta tengiliði milli Outlook og Viðskiptamiðis.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, Microsoft 365
ms.search.form: 6700, 5320, 5300, 5301, 5302, 5303, 5304, 5305, 5306, 5307, 5308, 5309, 5310, 5311
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 571dce9d79532cb3659ec952a585764af78c5161
ms.sourcegitcommit: 93f30ce3349233cbcd03f300e74b654b49fa5518
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/24/2022
ms.locfileid: "8799879"
---
# <a name="synchronize-contacts-in-business-central-with-contacts-in-microsoft-outlook"></a>Samstilla tengiliði í Business Central við tengiliði í Microsoft Outlook

Hægt er að setja upp samstillingu tengiliða þannig að tengiliðirnir [!INCLUDE[prod_short](includes/prod_short.md)] þínir hafi sömu upplýsingar og Tengiliðirnir þínir í Microsoft Outlook. Ef þú ert til dæmis Sölumaður þá gætir þú unnið í Outlook og [!INCLUDE[prod_short](includes/prod_short.md)] á sama tíma. Ef tengiliðirnir eru þeir sömu á báðum stöðum er vinnan þín einfaldari.  

Sjálfgefið er að tengiliðirnir sem verið er að samtengjast séu geymdir **í aðalmöppu** í uppáhaldi í Möppurúðunni í Outlook. Mappan Aðalmappa getur auðveldað auðkenningu tengiliða sem verið er að sambúa. Hægt er að setja afmarkanir til að samstilla aðeins tiltekna tengiliði úr [!INCLUDE[prod_short](includes/prod_short.md)] í Outlook. Eftir að samstilling hefur verið sett upp er hægt að samstilla handvirkt eða gera ferlið að samstilla á áætluðum grunni.  

## <a name="set-up-synchronization"></a>Uppsetning samstillingar
Þú setur upp hvernig þú vilt samstilla tengiliði með Outlook á síðunni **Uppsetning Exchange-samstillingar** í [!INCLUDE[prod_short](includes/prod_short.md)]. Forstilling í því að hafa notandaforstillinguna í [!INCLUDE[prod_short](includes/prod_short.md)] verður að tilgreina Microsoft 365 tölvupóstreikning. Hægt er að haka í þessa stillingu í **Microsoft 365 hlutanum sannvottun** í notandaforstillingunni á **listanum yfir notendur**. 

**Á genginu samkv. Uppsetningarsíðu** er hægt að staðfesta að tengingin við Exchange sé að virka og setja síðan upp samstillingu tengiliða. **Frá eigendaskiptum samkv. Uppsetningarsíðu** er hægt að **Opna samkeyrslu tengiliðar. Uppsetningarsíðu** og ræsa samstillingu. Valfrjálst er að setja afmörkun til að tilgreina hvaða tengiliði skuli samstilla. Til dæmis er hægt að afmarka eftir nafni, tegund, fyrirtæki o. is. Einnig er hægt að breyta sjálfgefnu heiti möppunnar í Outlook sem tengiliðirnir samstilla við.  

Hver Samkeyrsla notanda getur einnig sett upp sína eigin Gengissamstillingu og sett sínar eigin afmarkanir á hvaða tengiliði á að samstilla.  

Eftir að samstilling hefur verið sett upp er hægt að samstilla breytingar á tengiliðinn handvirkt eða gera ferlið sjálfvirkt með því að setja upp færslu í Verkröð. Nánari upplýsingar um sjálfvirkni er að finna í næsta kafla í þessari grein.

### <a name="automate-synchronization"></a>Gera samstillingu sjálfvirkt
Hægt er að stofna færslu í vinnslu sem mun samstilla tengiliði samkvæmt áætlun sem skilgreind er. Frekari upplýsingar, sjá [Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md). 

Í eftirfarandi töflu er listi yfir stillingarnar á **Færsluspjaldssíðu Vinnslubiðkorts** sem eru til að samstilla tengiliði:

|Svæði|Stilling fyrir tengilið samkeyrslu|
|-----|-----|
|Gerð hlutar sem á að keyra|Codeunit|
|Auðkenni hlutar í keyrslu|6700|

## <a name="synchronize-contacts"></a>Samstilla tengiliði
Ef þú ert vanur að vinna með tengiliði í [!INCLUDE[prod_short](includes/prod_short.md)] finnst þér auðvelt að samstilla handvirkt **í tengiliðalistanum** hvenær sem það hentar þér. Hægt er að samstilla tengiliði á tvennan hátt:

* **Samkeyra við Microsoft 365**

  Samstilla allar breytingar frá [!INCLUDE[prod_short](includes/prod_short.md)] til Microsoft 365 sem voru gerðar eftir síðustu samstillingu, Byggt á síðustu Breyttu dagsetningu. Einnig verða nýir Tengiliðir Microsoft 365 samstilltir [!INCLUDE[prod_short](includes/prod_short.md)]. Yfirleitt er þessi aðgerð hraðari en Full samkeyrslu. 

* **Full Samkeyrsla við Microsoft 365**

  Samstilla skal alla tengiliði í báðar áttir, óháð síðustu samkeyrsludagsetningu og síðustu Breyttu dagsetningu.  

Í báðum tilvikum eru tengiliðir aðeins samstilltir frá Outlook ef þeir hafa nauðsynlega reiti útfyllta. Nauðsynlegir reitir til að samstilla við Microsoft 365 eru **Heiti**, **Netfang** og tengiliðurinn verður að vera af tegundinni **manneskja**. [!INCLUDE[prod_short](includes/prod_short.md)] er uppruni tengiliðarins og [!INCLUDE[prod_short](includes/prod_short.md)] því verða upplýsingar um tengiliði vistaðar ef um tvítekningar er að ræða.  

> [!NOTE]
> Ef tengilið er eytt í Outlook en henni [!INCLUDE[prod_short](includes/prod_short.md)] er haldið við skal tengiliðurinn afþakkaður í Outlook næst þegar hann er samstillinn. 

## <a name="see-also"></a>Sjá einnig
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Fjármál](finance.md)  
[Sala](sales-manage-sales.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Nota tengiliði (fólk) í Outlook á vefnum](https://support.office.com/article/Using-contacts-People-in-Outlook-on-the-web-1e3438c7-26b2-420c-87de-3cea9d31b5cb?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]