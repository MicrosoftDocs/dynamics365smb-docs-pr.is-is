---
title: Deila tengiliðum milli Business Central og Outlook
description: Þessi þjónusta hefur mikla samþættingu við Microsoft 365 þannig að þú getur deilt tengiliðum milli Outlook og Business Central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'contacts, Microsoft 365'
ms.search.form: '6700, 5320, 5300, 5301, 5302, 5303, 5304, 5305, 5306, 5307, 5308, 5309, 5310, 5311'
ms.date: 03/17/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="synchronize-contacts-in-business-central-with-contacts-in-microsoft-outlook"></a>Samstilla tengiliði í Business Central við tengiliði í Microsoft Outlook

Hægt er að setja upp samstillingu tengiliðar þannig að tengiliðir þínir í [!INCLUDE[prod_short](includes/prod_short.md)] séu með sömu upplýsingar og tengiliðir þínir í Microsoft Outlook. Ef þú ert til dæmis sölumaður gætirðu unnið í Outlook og [!INCLUDE[prod_short](includes/prod_short.md)] á sama tíma. Ef tengiliðirnir eru þeir sömu á báðum stöðum er vinnan þín einfaldari.  

Tengiliðirnir sem verið er að samstilla eru sjálfgefið geymdir í möppu **Business Central** í eftirlæti á möppusvæðinu í Outlook. Mappa Business Central getur auðveldað þér að greina hvaða tengiliði þú ert að samstilla. Hægt er að stilla síur til að samstilla aðeins tiltekna tengiliði úr [!INCLUDE[prod_short](includes/prod_short.md)] í Outlook. Þegar þú hefur sett upp samstillingu er hægt að samstilla handvirkt eða gera ferlið sjálfvirkt til að samstilla samkvæmt áætlun.  

## <a name="prerequisites"></a>Frumskilyrði

- Þú notandasnið í [!INCLUDE[prod_short](includes/prod_short.md)] verður að tilgreina tölvupóstreikninginn þinn Microsoft 365 .

  Þú getur athugað þessa stillingu í hlutanum **Microsoft 365 Sannvottun** í notandaforstillingu þinni í listanum **Notendur**.
- Með [!INCLUDE[prod_short](includes/prod_short.md)] hefur verið sett upp samstilling tengiliða eins og lýst er í [Setja upp samstillingu tengiliða við Outlook fyrir Business Central innanhúss](admin-contact-sync-setup-onprem.md)

## <a name="set-up-synchronization"></a>Uppsetning samstillingar

Þú setur upp hvernig þú vilt samstilla tengiliði með Outlook á síðunni **Uppsetning Exchange-samstillingar** í [!INCLUDE[prod_short](includes/prod_short.md)]. 

Á síðunni **Uppsetning Exchange-samstillingar** getur þú sannprófað að tengingin við Exchange virki og síðan sett upp samstillingu samskipta. Á síðunni **Uppsetning Exchange-samstillingar** er hægt að opna síðuna **Uppsetning samstillingar tengiliða** og hefja samstillinguna. Valfrjálst er að stilla síu til að tilgreina hvaða tengiliði á að samstilla. Til dæmis er hægt að sía eftir nafni, tegund, fyrirtæki og svo framvegis. Þú getur einnig breytt sjálfgefna heiti möppunnar í Outlook sem tengiliðirnir munu samstillast við.  

Sérhver samstarfsfélagi þinn getur einnig sett upp eigin Exchange-samstillingu og sett sína eigin síur til að velja úr hvaða tengiliði skal samstilla.  

Eftir að samstilling hefur verið sett upp er hægt að samstilla breytingar á tengiliðnum handvirkt eða gera ferlið sjálfvirkt með því að setja upp verkraðarfærslu. Nánari upplýsingar um sjálfvirkni er að finna í næsta hluta í þessari grein.

### <a name="automate-synchronization"></a>Sjálfvirkni samstillingar

Hægt er að búa til verkraðarfærslu sem mun samstilla tengiliði samkvæmt tímaáætlun sem þú skilgreinir. Frekari upplýsingar, sjá [Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md). 

Eftirfarandi tafla sýnir stillingarnar á síðunni **Spjald verkraðarfærslu** sem eru fyrir samstillingu tengiliða:

|Svæði|Stilling fyrir samstillingu tengiliðar|
|-----|-----|
|Gerð hlutar sem á að keyra|Codeunit|
|Auðkenni hlutar í keyrslu|6700|

## <a name="synchronize-contacts"></a>Samstilla tengiliði

Ef þú hefur reynslu af því að vinna með tengiliði í [!INCLUDE[prod_short](includes/prod_short.md)] verður það lítið mál að samstilla handvirkt úr listanum **Tengiliðir** hvenær sem það hentar þér. Tengiliði er hægt að samstilla á tvo vegu:

* **Samstilla við Microsoft 365**

  Samstilltu allar breytingar úr [!INCLUDE[prod_short](includes/prod_short.md)] í Microsoft 365 sem voru gerðar eftir síðustu samstillingu út frá síðustu breytingardagsetningu. Nýir tengiliðir úr Microsoft 365 verða einnig samstilltir við [!INCLUDE[prod_short](includes/prod_short.md)]. Venjulega er þessi aðgerð hraðvirkari en full samstilling. 

* **Full samstilla við Microsoft 365**

  Samstilla alla tengiliði í báðar áttir óháð síðasta samstillingardegi og síðasta breytingardegi.  

Í báðum tilvikum eru tengiliðir aðeins samstilltir frá Outlook ef þeir hafa nauðsynlega reiti útfyllta. Áskildir reitir til að samstilla við Microsoft 365 eru **Nafn**, **Netfang** og tengiliðurinn verður að vera af gerðinni **Einstaklingur**. [!INCLUDE[prod_short](includes/prod_short.md)] er uppruni tengslaupplýsinganna, þannig að [!INCLUDE[prod_short](includes/prod_short.md)] tengslaupplýsingarnar verða vistaðar ef tvítekningar eru til staðar.  

> [!NOTE]
> Ef þú eyðir tengilið í Outlook, en en heldur honum í [!INCLUDE[prod_short](includes/prod_short.md)], verður tengiliðurinn búinn til aftur í Outlook í næsta skipti sem þú samstillir. 

## <a name="see-also"></a>Sjá einnig

[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Fjármál](finance.md)  
[Sala](sales-manage-sales.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Nota tengiliði (fólk) í Outlook á vefnum](https://support.office.com/article/Using-contacts-People-in-Outlook-on-the-web-1e3438c7-26b2-420c-87de-3cea9d31b5cb?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
