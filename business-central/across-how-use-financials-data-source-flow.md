---
title: Notaðu Power Automate flæði í Business Central
description: Settu upp og notaðu Power Automate flæði til að stofna eða breyta gögnum Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.search.keywords: 'workflow, OData, Power App, SOAP, Power Automate,'
ms.search.form: '1500,'
ms.date: 08/31/2023
ms.custom: bap-template
---

<!-- Line 41 says there are three cloud flow types, but the table lists four. Should line 41 change? -->


# <a name="use-power-automate-flows-in-"></a>Nota Power Automate flæðir inn [!INCLUDE[prod_short](includes/prod_short.md)]

Með [!INCLUDE[prod_short](includes/prod_short.md)] færðu leyfi fyrir Microsoft Power Automate. Þetta leyfi gerir þér kleift að nota [!INCLUDE[prod_short](includes/prod_short.md)] gögnin þín sem hluta af verkflæði í Microsoft Power Automate. Þú býrð til flæði og tengist gögnunum þínum frá innri og ytri upprunum í gegnum [!INCLUDE [prod_short](includes/prod_short.md)] tengilinn.

Power Automate flæði koma af stað af atburðum, svo sem að skrá er búin til, breytt eða eytt. Einnig er hægt að keyra flæði samkvæmt notendaskilgreindri áætlun eða eftir beiðni.

> [!NOTE]
> Stjórnendur geta takmarkað aðgang að Power Automate. Ef þú kemst að því að þú hafir ekki aðgang að sumum eða öllum eiginleikunum sem lýst er í þessari grein skaltu tala við stjórnandann. Ef þú vilt kynna þér frekar hvernig þú getur stjórnað Power Automate aðgangi sem stjórnandi skaltu skoða [Setja upp Power Automate-samþættingu](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-setup).

<!-- You must have a valid account with both [!INCLUDE[prod_short](includes/prod_short.md)] and Power Automate. --> 

> [!TIP]
> Til viðbótar við Power Automate geturðu notað sniðmát samþykktarverkflæðis í [!INCLUDE[prod_short](includes/prod_short.md)]. Þótt þetta séu tvö aðskilin verkflæðisforrit, þá er öllum sniðmátum samþykktarverkflæðis sem þú stofnar með Power Automate bætt við listann yfir verkflæði í [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar eru í [Verkflæði](across-workflow.md).

## <a name="about-power-automate-flows"></a>Um Power Automate flæði

Power Automate er þjónusta sem hjálpar þér að búa til sjálfvirk verkflæði (eða flæði) á milli forrita og þjónustu, eins og [!INCLUDE[prod_short](includes/prod_short.md)]. Power Automate flæði krefjast lítillar eða engrar þekkingar á kóðun. Hægt er að tengja þau við ýmis tilvik og svör, eins og:

- Breytingar á færslum
- Uppfærslur á ytri skrám
- Bókuð fylgiskjöl
- Mismunandi þjónustur Microsoft og þriðja aðila, eins og Microsoft Outlook, Excel, Dataverse, Teams, SharePoint, Power Apps og fleiri.

Hægt er að vinna með þrjár mismunandi gerðir af skýjaflæði:

|Flæðisgerð|Heimildasamstæða|
|---------|-----------|
|Sjálfvirkt flæði|Þesi flæðisgerð keyrir sjálfkrafa eftir tilviki. Í [!INCLUDE[prod_short](includes/prod_short.md)] gæti atburður verið þegar skrá eða skjal er búið til, breytt eða eytt. Til dæmis getur nýr sölureikningur komið af stað flæði fyrir samþykktarbeiðni, sem getur verið mismunandi tilvik stillt eftir því hvernig samþykktaraðilinn svarar. Neikvætt svar sendir tilkynningu og tölvupóst til samþykktarbeiðanda. Jákvætt svar uppfærir Excel-töflureikni í SharePoint möppu og sendir uppfærslu á Teams-spjalli samtímis. Hægt er að ræsa sjálfvirkt flæði með bæði innri og ytri tilvikum í [!INCLUDE[prod_short](includes/prod_short.md)].|
|Samþykkisflæði|Samþykkisflæði eru líka sjálfvirk flæði í Power Automate, en þau eru sérstaklega hönnuð til að biðja um samþykki þegar breytingar eru gerðar á skrám og gögnum. Þú getur notað samþykkisflæði í Power Automate sem valkost við [samþykktarverkflæðiseiginleika](across-use-workflows.md) sem er hluti af [!INCLUDE[prod_short](includes/prod_short.md)]. |
|Áætlað flæði|Þessi gerð flæðis er einnig keyrð sjálfkrafa en hún keyrir reglubundið á áætluðum degi og tíma. |
|Augnablik flæði|Þessi gerð flæðis er keyrð eftir þörfum og krefst þess að notandinn keyri hana handvirkt frá hnappi eða aðgerð í öðru forriti eða tæki, í þessu tilfelli [!INCLUDE[prod_short](includes/prod_short.md)] biðlaranum. Skyndiflæði virka svipað og flýtileiðir runa, framkvæmir mörg löng skref með nokkrum hnöppum og eru ræst á tilteknum síðum eða töflum. Til dæmis getur flæði bætt hnappi við aðgerðavalmyndina á síðunni **Lánardrottnar** til að útiloka greiðslur til lánardrottins og á sama tíma sent sérstillanlega tölvupósta til tengil lánardrottins og innkaupaaðila fyrirtækisins sem og að uppfæra tengiliðinn í Outlook. |

## <a name="power-automate-features"></a>Power Automate eiginleikar

Þú getur skoðað öll Power Automate flæði sem stendur þér til boða með því að skrá þig inn á [Power Automate](https://powerautomate.com) og velja **Mitt flæði** í yfirlitsstikunni vinstra megin. Hér finnur þú öll flæði sem þú hefur þegar búið til sjálfur og flæði sem stjórnandi eða samstarfsmaður hefur deilt með þér.

- Augnabliksflæði eru einnig aðgengileg til að keyra beint frá flestum lista-, korta- og skjalasíðum í [!INCLUDE[prod_short](includes/prod_short.md)]. Þú finnur augnabliksflæðið í **Sjálfvirku** aðgerðahópnum á aðgerðastikunni á síðum. Til að keyra flæði skaltu velja það og fylgja leiðbeiningunum sem kynntar eru þér. Fáðu frekari upplýsingar í köflunum sem fylgja hér á eftir.

- Með sjálfvirku flæði í [!INCLUDE[prod_short](includes/prod_short.md)] er ekkert fyrir þig að gera nema þú viljir breyta þeim eða slökkva á þeim. Annars virka þeir bara þegar þeir eru ræstir. 
<!--

## <a name="automated-flows"></a>Automated flows

With Power Automate, you can create business flows directly in-house and rely on citizen developers. Automated workflows can be started by both internal and external events in [!INCLUDE[prod_short](includes/prod_short.md)], and also be set to run periodically. Learn more and get instructions on how to create flows in the [Set Up Automated Workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) article in the administration content.

-->

## <a name="run-instant-flows"></a>Keyra skyndiflæði

Augnabliksflæði opnast inni [!INCLUDE [prod_short](includes/prod_short.md)] á netinu svo að þú getir verið innan samhengis viðskiptaferlisins sem þú varst í miðjunni að gera. Hægt er að keyra skyndiflæði úr flestum listum, spjöldum eða skjölum.

1. Í aðgerðastikunni, veldu **Sjálfvirka**, veldu síðan flæði af listanum yfir tiltæk flæði undir aðgerðinni **Power Automate** .

    :::image type="content" source="media/power-automate-instant-menu.svg" alt-text="Sýnir sjálfvirka aðgerðina með skyndiflæðisaðgerðum.":::

    Á sumum síðum er **Automate** er hreiður undir **Fleiri valkostir (...)**. 
2. Á svæðinu **Keyra flæði** skal fylla út í áskilda reiti, síðan velja **Halda áfram** til að keyra flæðið.

> [!NOTE]
> Fyrsta skipti sem þú notar atriðið **Sjálfvirkni** gætirðu hugsanlega bara séð aðgerðina **Hefjast handa með Power Automate**. Þú sérð þessa aðgerð vegna þess að þú hefur ekki samþykkt persónuverndartilkynninguna fyrir Microsoft Power Automate. Til að halda áfram skaltu velja **Byrjaðu með Power Automate** og fylgja leiðbeiningunum til að vera sammála eða ósammála.  
>
> :::image type="content" source="media/power-automate-action.png" alt-text="Sýnir sjálfvirka atriðið á aðgerðarstikunni.":::

<!--

[!INCLUDE [prod_short](includes/prod_short.md)] can run a Power Automate flow from most list, card, and document pages. Once the admin has connected [!INCLUDE [prod_short](includes/prod_short.md)] with Power Automate, you'll see any flows your organization has added when you choose the **Automate** action on the relevant pages. Instant flows are run without leaving [!INCLUDE [prod_short](includes/prod_short.md)]. Learn more in the [Set Up Automated Workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) article in the administration content.

These instant flows open on a page inside [!INCLUDE [prod_short](includes/prod_short.md)] online so you can remain within the context of the business process you were in the middle of. Choose the **Automate** action—on some pages nested under the **More Options** menu—choose the **Power Automate** menu item, then choose the relevant link to trigger the workflow. The connection to Power Automate is already set up for you.

Most flows require you to fill in a field or two before you choose the **Run flow** action.

> [!TIP]
> If you don't see an **Automate** action, then your [!INCLUDE [prod_short](includes/prod_short.md)] probably hasn't yet been set up to use Power Automate. Learn more from your admin.-->

## <a name="create-edit-and-manage-flows"></a>Búa til, breyta og stjórna flæði

Að búa til ný flæði eða breyta og stjórna þeim sem fyrir eru (eins og að kveikja eða slökkva á þeim) er hægt að gera beint í Power Automate. En þú getur hafið sum þessara verkefna úr sjálfvirkri aðgerðavalmyndinni í  [!INCLUDE[prod_short](includes/prod_short.md)]:

:::image type="content" source="media/power-automate-menu.svg" alt-text="Sýnir sjálfvirka aðgerðina á aðgerðastikunni með stækkuðum aðgerðum.":::

- Til að búa til sjálfvirkt flæði af lista, spjaldi eða skjalasíðu skaltu velja **Sjálfvirka** > **Búa til sjálfvirkt flæði**.
- Til að búa til samþykkisverkflæði af korti eða skjalasíðu skaltu velja **Sjálfvirkja** > **Búa til samþykkisflæði**.

  > [!TIP]
  > Þessi aðgerð er aðeins tiltæk á síðum korta og skjalategunda; ekki listar.
- Til að búa til tafarlaust flæði af lista, spjaldi eða skjalasíðu skaltu velja **Sjálfvirka** > **Búa til aðgerð sem byggir á flæði**.
- Til að opna Power Automate af lista, spjaldi eða skjalasíðu skaltu velja **Sjálfvirkja** > **Stjórna flæði**.
<!--- To create new flows or manage existing flows from inside [!INCLUDE[prod_short](includes/prod_short.md)], got to the **Manage Power Automate Flows** page.-->

Stjórnandi eða yfirnotandi sér yfirleitt um þessi verk. Verkin krefjast víðtækari þekkingar á viðskiptaferlunum í [!INCLUDE[prod_short](includes/prod_short.md)]. Til að læra meira skaltu fara í eftirfarandi greinar í Business Central Dev and IT Pro hjálpinni:

- [Power Automate sameining](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-overview)
- [Búðu til sjálfvirk flæði](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows) (nær einnig samþykkisflæði)
- [Búðu til tafarlaus flæði](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)
- [Stjórna Power Automate flæði](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows)
<!-- 

## <a name="add-more-automated-flows-and-instant-flows"></a>Add more automated flows and instant flows

You can create flows through the [powerautomate.microsoft.com](https://powerautomate.microsoft.com) website. However, if your admin has switched on the capability to run Power Automate flows from inside [!INCLUDE [prod_short](includes/prod_short.md)] online, you can start the process of building a flow from the **Automate** action on the relevant pages, which can be found under the **More Options** menu depending on the page. Then choose the **Power Automate** menu item, and then choose the **Create a flow** action. Power Automate then opens in a new browser tab, and you're signed in automatically.

You can find sample templates to adapt to your company and all available trigger events, using both [!INCLUDE [prod_short](includes/prod_short.md)] and external tools, by choosing the **Connectors** menu on the Power Automate website. Learn more about available templates and triggers in the [Set Up Automated Workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) article in the administration content.

## <a name="create-and-manage-power-automate-flows"></a>Create and manage Power Automate flows

You can create new flows or manage existing Power Automate flows in [!INCLUDE [prod_short](includes/prod_short.md)] on the **Manage Power Automate Flows** page. Learn more in the [Manage Power Automate Flows](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows) article in the administration content.

<!--
You can also manage available Power Automate workflows on the **Workflows** page in [!INCLUDE[prod_short](includes/prod_short.md)]. The page lists both the built-in approval and Power Automate workflows, with options for the latter to enable/disable, delete, and view the workflow on the Power Automate website.-->

## <a name="see-also"></a>Sjá einnig .

[Úrræðaleitaðu sjálfvirku [!INCLUDE[prod_short](includes/prod_short.md)] verkflæðin þín](across-flow-troubleshoot.md)  
[Undirbúðu þig undir viðskiptin](ui-get-ready-business.md)  
[Verkflæði](across-workflow.md)  
[Flytja inn viðskiptagögn úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Úthluta leyfi til notenda og hópa](ui-define-granular-permissions.md)  
[Setja upp [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Fjármálastjórnun](finance.md)  
[Stjórna Power Automate flæði](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows)  
[Setja upp sjálfvirk verkfllæði](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  
[Kveikja á skyndiflæði](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
