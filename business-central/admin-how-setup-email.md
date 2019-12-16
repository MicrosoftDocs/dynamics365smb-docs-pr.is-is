---
title: Setja upp tölvupóst í Business Central | Microsoft Docs
description: Lýsir því hvernig á að nota STMP-þjón fyrirtækisins til að senda og taka við tölvupósti í Business Central, einnig hvernig á að nota þær stillingar þjónsins sem voru stofnaðar með Office 365 áskrift.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Office 365
ms.date: 11/15/2019
ms.author: sgroespe
ms.openlocfilehash: e1f24e6da71d32e162b107b0e0b9e01cb68cc302
ms.sourcegitcommit: 23577ae8ecaaf09b58716c2b9f65e39c188e3661
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/18/2019
ms.locfileid: "2810814"
---
# <a name="set-up-email"></a>Setja upp tölvupóst
Til að senda og taka á móti tölvupósti innan [!INCLUDE[d365fin](includes/d365fin_md.md)] verður þú að fylla út reitina á síðunni SMTP-póstuppsetning.

Í stað þess að slá inn upplýsingar um SMTP-þjón handvirkt geturðu notað aðgerðina **Nota Office 365 þjónsstillingar** til að slá þær inn með upplýsingum úr Office 365 áskriftinni þinni.

Þú getur annaðhvort sett upp tölvupóst handvirkt, eins og lýst er hér að neðan, eða þú getur fengið hjálp með því að nota **Uppsetning tölvupósts** leiðbeiningar um uppsetningu með hjálp. Nánari upplýsingar er að finna á [Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md).  

## <a name="to-set-up-email"></a>Til að setja upp tölvupóst
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **SMTP uppsetning tölvupósts** og veldu síðan tengda tengilinn.
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > Ef þú ert að nota reikning sem krefst tveggja þátta staðfestingar verður aðgangsorðið sem þú slærð inn í reitinn **Aðgangsorð** að vera það sama og þú notar fyrir Office 365 áskriftina þína og það verður að vera af gerðinni **Aðgangsorð fyrir forrit**. Frekari upplýsingar er að finna í [Stjórna aðgangsorðum forrita fyrir tvíþætta staðfestingu](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords). 
3. Þú getur einnig valið **Nota stillingar Office 365 Stillingar vefþjóns** aðgerðina til að setja inn upplýsingar sem eru þegar skilgreindar fyrir Office 365 áskriftina þína.
4. Þegar allir reitir eru fylltir út velurðu aðgerðina **Prófa tölvupóstuppsetningu**.
5. Þegar prófið hefur tekist skal loka síðunni.

## <a name="using-a-substitute-sender-address-on-outbound-email-messages"></a>Notkun staðgengilsnetfang sendanda fyrir send tölvupóstskeyti
Öll send tölvupóstskeyti úr [!INCLUDE[d365fin](includes/d365fin_md.md)] nota sjálfgefið netfang fyrir reikninginn sem var tilgreindur á SMTP-uppsetningarsíðu tölvupósts eins og lýst er hér að ofan. Þú getur hinsvegar notað möguleikana **Senda sem** eða **Senda fyrir hönd** á Exchange-þjóninum til að breyta netfangi sendanda fyrir skeyti á útleið. [!INCLUDE[d365fin](includes/d365fin_md.md)] notar sjálfgefinn reikning til að sannvotta fyrir Exchange, en mun annaðhvort skipta út netfangi sendanda með því sem þú tilgreinir eða breytir því með „fyrir hönd.“

Eftirfarandi eru dæmi um hvernig Senda sem og Senda fyrir hönd eru notuð í [!INCLUDE[d365fin](includes/d365fin_md.md)].:

 * Þegar þú sendir skjöl eins og innkaupa- eða sölupantanir til lánardrottna og viðskiptamanna viltu mögulega að það líti út fyrir að þeir hafi komið frá netfanginu _noreply@yourcompanyname.com_.
 * Þegar verkflæðið þitt sendir samþykktarbeiðni í tölvupósti með netfangi beiðanda.

> [!Note]
> Aðeins er hægt að nota einn reikning sem staðgengil fyrir netföng sendanda. Þú getur sem sagt ekki haft eitt staðgengilsnetfang fyrir innkaupferli og annað fyrir söluferli.

### <a name="to-set-up-the-substitute-sender-address-for-all-outbound-email-messages"></a>Til að setja upp staðgengilsnetfang sendanda fyrir öll tölvupóstskeyti á útleið
1. Í **Stjórnandamiðstöð Exchange** fyrir Office 365-reikninginn þinn skaltu finna pósthólfið sem nota á sem staðgengilsnetfang og síðan skaltu afrita eða skrifa hjá þér netfangið. Ef þú þarft nýtt netfang skaltu fara í Stjórnendamiðstöð Microsoft 365 til að búa til nýjan notanda og setja upp pósthólfið hans.
2. Í [!INCLUDE[d365fin](includes/d365fin_md.md)] veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **SMTP uppsetning tölvupósts**, og veldu síðan tengda tengilinn.
3. Í reitnum **Senda sem** skal færa inn staðgengilsnetfangið.
4. Afritaðu eða skráðu netfangið niður í reitinn **Notandakennið**.
5. Í **Stjórnandamiðstöð Exchange** skaltu finna pósthólfið sem á að nota sem staðgengilsnetfang og færðu síðan inn netfangið úr reitnum **Notandakenni** í reitnum **Senda sem**. Frekari upplýsingar er að finna í [Stjórna heimildum fyrir viðtakendur](/Exchange/recipients/mailbox-permissions?view=exchserver-2019#use-the-eac-to-assign-permissions-to-individual-mailboxes).

### <a name="to-use-the-substitute-address-in-approval-workflows"></a>Til að nota staðgengilsnetfangið í samþykktarverkflæðum
1. Í [!INCLUDE[d365fin](includes/d365fin_md.md)] veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **SMTP uppsetning tölvupósts**, og veldu síðan tengda tengilinn.
2. Afritaðu eða skráðu netfangið niður í reitinn **Notandakennið**.
3. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Notandauppsetning samþykktar** og veldu síðan tengda tengilinn.
4. Í **Stjórnandamiðstöð Exchange** skaltu finna pósthólfin fyrir hvern notanda sem kemur fyrir á síðunni **Notandauppsetning samþykktar** og í reitinn **Senda sem** skal færa inn netfangið úr reitnum **Notandakenni** á síðunni **SMTP uppsetning tölvupósts** í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Frekari upplýsingar er að finna í [Stjórna heimildum fyrir viðtakendur](/Exchange/recipients/mailbox-permissions?view=exchserver-2019).
5. Í [!INCLUDE[d365fin](includes/d365fin_md.md)] veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið **SMTP uppsetning tölvupósts**, og veldu síðan tengda tengilinn.
6. Til að virkja skiptingu skal kveikja á víxlun **Leyfa að skipta um sendanda**.

> [!Note]
> [!INCLUDE[d365fin](includes/d365fin_md.md)] ákvarðar hvaða netfang eigi að birta í eftirfarandi röð: <br><br> 1. Netfang tilgreint í reitnum **Tölvupóstur** á síðunni **Notandauppsetning samþykktar** fyrir skeyti í verkflæði. <br> 2. Netfang tilgreint í reitnum **Senda sem** á síðunni **SMTP uppsetning tölvupósts**. <br> 3. Netfang tilgreint í reitnum **Notandakenni** á síðunni **SMTP uppsetning tölvupósts**.


## <a name="see-also"></a>Sjá einnig

[Samnýtt pósthólf í Exchange Online](/exchange/collaboration-exo/shared-mailboxes)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Senda skjöl í tölvupósti](ui-how-send-documents-email.md)  
[Sérstilling [!INCLUDE[d365fin](includes/d365fin_md.md)] með viðbótum](ui-extensions.md)  
[Nota [!INCLUDE[d365fin](includes/d365fin_md.md)] sem viðskiptainnhólf þitt í Outlook](admin-outlook.md)  
[Fáðu [!INCLUDE[d365fin](includes/d365fin_md.md)] í fartækið þinn](install-mobile-app.md)
