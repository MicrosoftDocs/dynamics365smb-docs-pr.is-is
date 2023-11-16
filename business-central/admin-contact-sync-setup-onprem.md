---
title: Setja upp tengilið samkeyrslu við Outlook sem er í Innanhússmiðstöð
description: Lærðu að skilgreina umhverfi innanhúss til að samstilla tengiliði í viðskiptamiðinu og Outlook.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 09/28/2023
ms.custom: bap-template
---

# <a name="set-up-contact-sync-with-outlook-for-business-central-on-premises"></a>Setja upp tengilið samkeyrslu við Outlook sem er í Innanhússmiðstöð

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Í þessari grein er hægt að læra hvernig setja á upp  [!INCLUDE[prod_short](includes/prod_short.md)]  innanhúss til að samstilla tengiliði í  [!INCLUDE[prod_short](includes/prod_short.md)]  við tengiliði í Outlook. Nánari upplýsingar um aðgerðina er að leita í til að  [Samstilla tengiliði í Viðskiptamiðinu við tengiliði í Microsoft Outlook](admin-synchronize-outlook-contacts.md).

## <a name="introduction"></a>Kynning

Samstilling tengiliða krefst þess að nota OAuth 2,0 samskiptareglurnar fyrir sannvottun með Exchange Online. Áður hafði grunnsannvottun einnig verið studd, en hún verið fyrst og ekki studd lengur Exchange Online. Hægt er að lesa nánar um afskráð hjá  [sviptingu grunnskírteinis í Exchange Online](/exchange/clients-and-mobile-in-exchange-online/deprecation-of-basic-authentication-exchange-online). Þessi breyting þýðir að Samstilling tengiliða í Viðskiptamiðinu getur hafa hætt að virka í umhverfi innanhúss. Í þessari grein verður útskýrt hvernig á að fá það að virka aftur.

## <a name="prerequisites"></a>Frumskilyrði

- Exchange Online, annað hvort með sjálfstæðri útgáfu eða með  Microsoft 365  áætlun  
- Aðgangur að  Microsoft Entra  leigjanda notaður af Exchange Online
- [!INCLUDE[prod_short](includes/prod_short.md)] notendur hafa með sér  Microsoft 365  eða  Exchange Online  email reikning, sem er úthlutað reikningum í [!INCLUDE[prod_short](includes/prod_short.md)]. Hægt er að haka í þessa stillingu í  **Microsoft 365  hlutanum sannvottun**  á notandaforstillingu á  **listanum yfir notendur** . 

## <a name="set-up-contact-sync"></a>Setja upp samkeyrslu tengiliðar

Ljúkið eftirfarandi skrefum til að setja upp tengiliðsamkeyrslu. Ef þú ert að keyra  [!INCLUDE[prod_short](includes/prod_short.md)]  vorið 2019 (v. 14) þá þarftu að gera aukaskref sem annað hvort breytir forritskóða eða setur upp tengingu við Power BI.

1. <a name="registerapp"></a> Skrá app fyrir  Exchange Online  API hjá  Microsoft Entra  leigjandanum.

   Í þessu skrefi bætist við skráð App hjá  Microsoft Entra  leigjanda  Microsoft 365  eða  Exchange Online  áætlun. Eins og aðrir Azure þjónustuaðilar sem vinna með Central Business,  Exchange Online  þurfa skráð App í  Microsoft Entra  auðkenni. Skrásett App veitir sannvottun og heimildaþjónustu á milli Viðskiptamiðis og Exchange Online.

   Fylgdu ítarlegum leiðbeiningum forritara og það Pro Help at  [skrá inn umsókn í  Microsoft Entra  ID](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory). Eftir því sem farið er eftir leiðbeiningunum skal minnt á eftirfarandi atriði:

   - Ef þú hefur þegar skráð inn umsókn sem hluta af samþættingu við aðra Microsoft vöru, eins og  Power BI, endurnýtir þú þá skráð App. Í þessu tilfelli þarftu bara að setja upp App með þeim  Office 365 Exchange Online  heimildum sem lýst er í næstu kúlu.

   - Skilgreinið skrásett App með eftirfarandi úthlutuðum heimildum til  Office 365 Exchange Online  API:

     - Tengiliðir. Lesiskrifa
     - EWS.AccessAsUser.All

2. Fyrir  [!INCLUDE[prod_short](includes/prod_short.md)]  útgáfu 14 skal gera eitt af eftirtöldum verkefnum:

   - Breyta síðu 6700 með því að  `FALSE`  Breyta  `TRUE`  í í eftirfarandi kóðalínu í  `OnPageOpen`  kveikjunni:

     ```
     PasswordRequired := AzureADMgt.GetAccessToken(AzureADMgt.GetO365Resource,AzureADMgt.GetO365ResourceName,TRUE) = '';
     ```

   - Stofna nýja síðu með eftirfarandi kóta á OnPageOpen gikkinu:

     ```
     PasswordRequired := AzureADMgt.GetAccessToken(AzureADMgt.GetO365Resource,AzureADMgt.GetO365ResourceName,TRUE) = '';
     ```

   - Setjið upp  Power BI  með því að fylgja leiðbeiningunum  [með því að setja upp viðskipti miðsvæðis innanhúss fyrir  Power BI  samþættingu](admin-powerbi-setup.md#setup).

   Eftir að lausnin sem þú velur er á sínum stað biðjum við notendur um annað hvort keyra nýju/Breyttu síðuna eða  [tengjast við Power BI](across-working-with-powerbi.md#connect). Þeir þurfa því aðeins að gera þetta skref einu sinni.

## <a name="next-steps"></a>Næstu skref

[Samstilla tengiliði í Aðalmiðinu við tengiliði í Microsoft Outlook](admin-synchronize-outlook-contacts.md)  
