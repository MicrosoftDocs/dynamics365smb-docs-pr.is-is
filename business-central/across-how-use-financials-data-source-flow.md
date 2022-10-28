---
title: Nota Power Automate flæði í Viðskiptamiðinu
description: Setja upp og nota Power Automate flæði til að stofna eða breyta aðalgögnum viðskipta.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: workflow, OData, Power App, SOAP, Power Automate,
ms.search.form: 1500,
ms.date: 10/10/2022
ms.custom: bap-template
ms.openlocfilehash: ce1af0b2a07aa570141f9d4684930e303cbca742
ms.sourcegitcommit: 902834e76460d751a345485c66fd2831066b396b
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/25/2022
ms.locfileid: "9716495"
---
# <a name="use-power-automate-flows-in-prod_short"></a>Nota Power Automate rennur í [!INCLUDE[prod_short](includes/prod_short.md)]

Með [!INCLUDE[prod_short](includes/prod_short.md)] er þér gefið leyfi til þess Microsoft Power Automate. Þetta leyfi leyfir notanda að nota [!INCLUDE[prod_short](includes/prod_short.md)] gögnin sem hluta verkflæðis í Microsoft Power Automate. Flæðigryfjur eru [!INCLUDE [prod_short](includes/prod_short.md)] stofnaðar og tengst gögnum frá innri og ytri aðilum í tengivirkinu.

Power Automate streymi er ræst eftir atburðum, eins og færsla var búin til, henni breytt eða eytt. Einnig er hægt að keyra þær á notandaskilgreinda áætlun eða í eftirspurn.

> [!NOTE]
> Kerfisstjórum er hægt að takmarka aðgang að Power Automate. Finnir þú fyrir því að þú hafir ekki aðgang að einhverjum eða öllum aðgerðum sem getið er um í þessari grein skaltu tala við admin. Ef þú vilt fræðast um hvernig þú getur stjórnað Power Automate aðgangi sem admin, sjá [Setja upp Power Automate samþættingu](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-setup).

<!-- You must have a valid account with both [!INCLUDE[prod_short](includes/prod_short.md)] and Power Automate. --> 

> [!TIP]
> Auk þess er hægt að Power Automate nota sniðmát samþykktarverkflæðis í [!INCLUDE[prod_short](includes/prod_short.md)]. Þó að þau séu tvö aðskilin verkflæðiskerfi er einhverju samþykktarverksniðmáti sem stofnað Power Automate er til bætt við listann yfir verkflæði að innan [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar um [verkflæði](across-workflow.md).

## <a name="about-power-automate-flows"></a>Um Power Automate streymi

Power Automate er þjónusta sem hjálpar þér að búa til sjálfvirk verkflæði (eða flæði) á milli apps og þjónustu, eins [!INCLUDE[prod_short](includes/prod_short.md)] og. Power Automate flæði krefst litla eða enga vitræa þekkingu. Þau geta tengst margs konar atburðum og viðbrögðum, svo sem:
- Taka upp breytingar
- Uppfærslur ytri skráa
- Bókuð skjöl
- Mismunandi þjónustur Microsoft og þriðja aðila, eins Microsoft Outlook, Excel, Dataverse, teygt, SharePoint Power Apps, og fleira.

Til eru þrjár mismunandi skýflæðagerðir sem hægt er að vinna með:

|Gerð flæðis|Lýsing|
|---------|-----------|
|Sjálfvirkum|Þessi flæðigerð er keyrð sjálfvirkt eftir atviki. Í [!INCLUDE[prod_short](includes/prod_short.md)], tilvik gæti verið þegar færsla eða skjal er stofnað, því breytt eytt. Þannig að t.d. nýr sölureikningur getur kallað fram rennsli fyrir samþykkisbeiðni, sem getur haft mismunandi atburði stillt eftir svari samþykkjanda. Neikvætt svar sendir tilkynningu og tölvupóst til samþykktarumsækjanda. Jákvætt svar uppfærir samtímis Excel-töflu sem er SharePoint staðsett í möppu og sendir uppfærslu á teymum spjalla. Hægt er að ræsa sjálfvirkt flæði með sjálfvirkum og ytri atvikum [!INCLUDE[prod_short](includes/prod_short.md)].|
|Tímasett|Þessi gerð flæðis er einnig keyrð sjálfvirkt en keyrir hana reglulega á áætlaða dagsetningu og tíma. |
|Skyndihjálp |Þessi flæðigerð er keyrð á eftirspurn, sem krefst þess að notandinn keyri hann handvirkt af hnapp eða aðgerð í öðru forriti eða tæki, í þessu tilviki [!INCLUDE[prod_short](includes/prod_short.md)]. Verk á augabragði eru notuð á sama hátt og í runustúðum, framkvæmd mörgum skrefum með nokkrum hnappabrennum og hleypt er frá tilteknum síðum eða töflum. Til dæmis getur áklæði bætt við hnapp í aðgerðavalmyndinni á **síðunni Lánardrottnar** til að loka fyrir greiðslur til lánardrottins og á sama tíma er hægt að senda sérhannaðan tölvupóst til tengiliðs lánardrottins og kaupanda fyrirtækisins sem og uppfæra tengilið í Outlook. |

## <a name="power-automate-features-in-prod_short"></a>Power Automate aðgerðir í [!INCLUDE[prod_short](includes/prod_short.md)]

Þú getur kannað allt Power Automate flæði sem nú er aðgengilegt þér með því að [Power Automate](https://powerautomate.com) skrá þig inn í og velja **mitt streymi** úr yfirlitsstikunni vinstra megin. Hér finnur þú eitthvað streymi sem þú hefur þegar stofnað sjálfur og streymir samdeilt með þér af admin eða coverke. Þessi streymi er einnig gert aðgengilegt frá innu [!INCLUDE [prod_short](includes/prod_short.md)] frá ýmsum síðum. Með sjálfvirkum flæðum [!INCLUDE[prod_short](includes/prod_short.md)] er ekkert fyrir þig að gera, nema að vilja breyta þeim eða snúa þeim við. Annars virka þær bara þegar af stað. Þegar um er að ræða skyndiupplýsingar [!INCLUDE[prod_short](includes/prod_short.md)] er hægt að keyra þær af flestum lista, spjald-og fylgiskjalssíðum með því að velja þær úr **automate** atridi í aðgerðinni. Lærðu meira á köflum sem fylgja.

<!--

## Automated flows

With Power Automate, you can create business flows directly in-house and rely on citizen developers. Automated workflows can be started by both internal and external events in [!INCLUDE[prod_short](includes/prod_short.md)], and also be set to run periodically. Learn more and get instructions on how to create flows in the [Set Up Automated Workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) article in the administration content.

-->

## <a name="run-instant-flows"></a>Keyra skyndiflæði

Augnablik streyma opið inni [!INCLUDE [prod_short](includes/prod_short.md)] á netinu þannig að þú getur haldið áfram innan samhengis viðskiptaferlisins sem þú varst í miðri. Hægt er að keyra skyndiflæði frá flestum listum, kortum eða skjölum.

1. Í aðgerðrein velurðu **automate**, síðan velur flæði úr lista yfir tiltæka flæði undir **Power Automate** aðgerðinni

    :::image type="content" source="media/power-automate-action-intro.png" alt-text="Sýnir aðgerðina Automate í aðgerðstiku með útvíkkuðum aðgerðum.":::

    Á einhverri síðu **er sjálfvirkt** hreiður undir **fleiri valkostum (...)**. 
2. **Í reitunum keyra flæðistreymissrúðu** eru reitirnir nauðsynlegir og síðan valið **halda áfram** til að keyra flæðið.

> [!NOTE]
> Í fyrsta sinn sem automate **-varan er notuð** gæti notandi aðeins **séð aðgerðina byrja með Power Automate** aðgerð. Þú sérð þessa aðgerð þar sem við höfum ekki samþykkt friðlýsingu fyrir Microsoft Power Automate. Til að halda áfram er valið **byrja með Power Automate** og fylgið leiðbeiningum til að samþykkja eða afnema.  
>
> :::image type="content" source="media/power-automate-action.png" alt-text="Sýnir Automate atriðið í aðgerðreininni.":::

<!--

[!INCLUDE [prod_short](includes/prod_short.md)] can run a Power Automate flow from most list, card, and document pages. Once the admin has connected [!INCLUDE [prod_short](includes/prod_short.md)] with Power Automate, you'll see any flows your organization has added when you choose the **Automate** action on the relevant pages. Instant flows are run without leaving [!INCLUDE [prod_short](includes/prod_short.md)]. Learn more in the [Set Up Automated Workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) article in the administration content.

These instant flows open on a page inside [!INCLUDE [prod_short](includes/prod_short.md)] online so you can remain within the context of the business process you were in the middle of. Choose the **Automate** action—on some pages nested under the **More Options** menu—choose the **Power Automate** menu item, then choose the relevant link to trigger the workflow. The connection to Power Automate is already set up for you.

Most flows require you to fill in a field or two before you choose the **Run flow** action.

> [!TIP]
> If you don't see an **Automate** action, then your [!INCLUDE [prod_short](includes/prod_short.md)] probably hasn't yet been set up to use Power Automate. Learn more from your admin.-->

## <a name="create-edit-and-manage-flows"></a>Stofna, breyta og stjórna streymi

Búa til nýjar rennur, breyta og stjórna þeim sem fyrir eru (eins og að kveikja eða slökkva á þeim) geta gert það beint Power Automate. En hægt er að hefja sum þessara verkefna út frá inni [!INCLUDE[prod_short](includes/prod_short.md)]:

- Ef búa á til skyndiflæði af lista, spjaldi eða síðu skjals skal velja **gera automate** > **Stofna flæði**.
- Til að opna Power Automate af lista, Spjald eða skjalssíður skal velja **gera automate** > **Manage streyma**.
- Til að búa til nýtt flæði eða stjórna flæðunum sem [!INCLUDE[prod_short](includes/prod_short.md)] fyrir eru innan **, er búið að sjá síðuna stjórna Power Automate flæði**.

Þessi verk eru vanalega gerð af admin eða Ofur notanda. Verkefnin krefjast víðari þekkingar á viðskiptaferlinum í [!INCLUDE[prod_short](includes/prod_short.md)]. Til að fræðast meira, sjá [Setja upp sjálfvirka streyta](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows), [Setja upp skyndilausnir](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) og [stjórna Power Automate flæði](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows).
<!-- 

## Add more automated flows and instant flows

You can create flows through the [powerautomate.microsoft.com](https://powerautomate.microsoft.com) website. However, if your admin has switched on the capability to run Power Automate flows from inside [!INCLUDE [prod_short](includes/prod_short.md)] online, you can start the process of building a flow from the **Automate** action on the relevant pages, which can be found under the **More Options** menu depending on the page. Then choose the **Power Automate** menu item, and then choose the **Create a flow** action. Power Automate then opens in a new browser tab, and you're signed in automatically.

You can find sample templates to adapt to your company and all available trigger events, using both [!INCLUDE [prod_short](includes/prod_short.md)] and external tools, by choosing the **Connectors** menu on the Power Automate website. Learn more about available templates and triggers in the [Set Up Automated Workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) article in the administration content.

## Create and manage Power Automate flows

You can create new flows or manage existing Power Automate flows in [!INCLUDE [prod_short](includes/prod_short.md)] on the **Manage Power Automate Flows** page. Learn more in the [Manage Power Automate Flows](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows) article in the administration content.

<!--
You can also manage available Power Automate workflows on the **Workflows** page in [!INCLUDE[prod_short](includes/prod_short.md)]. The page lists both the built-in approval and Power Automate workflows, with options for the latter to enable/disable, delete, and view the workflow on the Power Automate website.-->

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/use-power-automate/)

## <a name="see-also"></a>Sjá einnig .

[[!INCLUDE[prod_short](includes/prod_short.md)] Úrræðaleit vegna sjálfvirkra verkflæða](across-flow-troubleshoot.md)  
[Vertu klár í rekstur fyrirtækja](ui-get-ready-business.md)  
[Verkflæði](across-workflow.md)  
[Flytja inn viðskiptagögn úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Úthluta leyfi til notenda og hópa](ui-define-granular-permissions.md)  
[Setja upp[!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Fjármál](finance.md)  
[Stjórna Power Automate streymi](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows)  
[Setja upp sjálfvirk verkflæði](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  
[Rofi á Skyndistreymi](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
á