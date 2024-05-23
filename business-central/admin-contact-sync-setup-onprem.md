---
title: Setja upp tengiliðasamstillingu við Outlook fyrir Business Central innanhúss
description: Læra að grunnstilla Business Central umhverfi innanhúss til að samstilla tengiliði í Business Central og Outlook.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics-365-op
ms.topic: how-to
ms.date: 09/28/2023
ms.custom: bap-template
---

# <a name="set-up-contact-sync-with-outlook-for-business-central-on-premises"></a>Setja upp tengiliðasamstillingu við Outlook fyrir Business Central innanhúss

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Í þessari grein er lært hvernig á að setja upp [!INCLUDE[prod_short](includes/prod_short.md)] innanhúss til að samstilla tengiliði við [!INCLUDE[prod_short](includes/prod_short.md)] tengiliði í Outlook. Frekari upplýsingar er hægt að [fá í Samstilla tengiliði í Business Central við tengiliði í Microsoft Outlook](admin-synchronize-outlook-contacts.md).

## <a name="introduction"></a>Kynning

Samstilling tengiliða krefst þess að nota samskiptaregluna OAuth 2.0 til sannvottunar með Exchange Online. Áður var grunnsönnun einnig studd, en hún hefur verið afskrifuð og ekki lengur studd með Exchange Online. Nánari upplýsingar um afskriftir eru [í Afskrift einfaldrar sannvottunar í Exchange Online](/exchange/clients-and-mobile-in-exchange-online/deprecation-of-basic-authentication-exchange-online). Þessi breyting þýðir að tengiliðasamstilling í Business Central gæti hafa hætt að vinna við umhverfið á staðnum. Þessi grein mun útskýra hvernig á að fá hana til starfa aftur.

## <a name="prerequisites"></a>Frumskilyrði

- Exchange Online, annaðhvort standalone útgáfu eða með Microsoft 365 áætlun  
- Aðgangur að leigjandanum Microsoft Entra sem notaður er af Exchange Online
- [!INCLUDE[prod_short](includes/prod_short.md)] notendur hafa eða Microsoft 365  Exchange Online tölvupóstreikning, sem er úthlutað á reikninga þeirra í [!INCLUDE[prod_short](includes/prod_short.md)]. Hægt er að athuga þessa stillingu í hlutanum **Microsoft 365 Sannvottun** notendasniðs á listanum **Notendur** . 

## <a name="set-up-contact-sync"></a>Setja upp samstillingu tengiliða

Ljúka skal eftirfarandi skrefum til að setja upp samstillingu tengiliða. Ef þú keyrir [!INCLUDE[prod_short](includes/prod_short.md)] Vor 2019 (v.14) þarftu að gera aukaskref sem annaðhvort breytir forritskóta eða setur upp tengingu við Power BI.

1. <a name="registerapp"></a> Skráðu forrit fyrir Exchange Online API í leigjanda þínum Microsoft Entra .

   Í þessu skrefi bætir þú við skráðu forriti í Microsoft Entra leigjanda eða Microsoft 365  Exchange Online áætlun. Eins og önnur Azure þjónusta sem vinnur með Business Central krefst Exchange Online  skráðs forrits í Microsoft Entra auðkenni. Skráða forritið veitir sannvottun og heimildarþjónustu á milli Business Central og Exchange Online.

   Fylgdu nákvæmum leiðbeiningum í hjálp forritara og tæknimanns við [að skrá forrit í Microsoft Entra kenni](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory). Eftir því sem farið er í gegnum leiðbeiningarnar þarf að muna eftirfarandi atriði:

   - Ef þú hefur þegar skráð forrit sem hluta af samþættingu við aðra Microsoft-vöru, svo sem Power BI, þá endurnotaðu það skráða forrit. Í þessu tilfelli þarftu bara að setja upp forritið með þeim heimildum sem Office 365 Exchange Online lýst er í næstu kúlu.

   - Stilla skráða forritið með eftirfarandi framseldum heimildum á Office 365 Exchange Online API:

     - Tengiliðir.ReadWrite
     - EWS.AccessAsUser.All

2. Í [!INCLUDE[prod_short](includes/prod_short.md)] útgáfu 14 er eitt af eftirfarandi verkum gert:

   - Breyta bls. 6700 með því að `FALSE` breyta `TRUE` í eftirfarandi kótalínu í gikknum `OnPageOpen` :

     ```
     PasswordRequired := AzureADMgt.GetAccessToken(AzureADMgt.GetO365Resource,AzureADMgt.GetO365ResourceName,TRUE) = '';
     ```

   - Stofna nýja síðu með eftirfarandi kóða á OnPageOpen-kveikjunni:

     ```
     PasswordRequired := AzureADMgt.GetAccessToken(AzureADMgt.GetO365Resource,AzureADMgt.GetO365ResourceName,TRUE) = '';
     ```

   - Setja upp Power BI með því að fylgja leiðbeiningum á [Setja upp Business Central innanhúss fyrir Power BI samþættingu](across-working-with-business-central-in-powerbi.md).

   Þegar lausnin sem valin er er til staðar er beðið notendur um að keyra nýja/breyttu síðuna eða [tengjast Power BI](across-working-with-powerbi.md#connect). Þeir þurfa aðeins að gera þetta skref einu sinni.

## <a name="next-steps"></a>Næstu skref

[Samstilla tengiliði í Business Central við tengiliði í Microsoft Outlook](admin-synchronize-outlook-contacts.md)  
