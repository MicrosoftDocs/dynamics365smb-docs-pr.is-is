---
title: Setja upp tengilið samkeyrslu við Outlook sem er í Innanhússmiðstöð
description: Lærðu að skilgreina umhverfi innanhúss til að samstilla tengiliði í viðskiptamiðinu og Outlook.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 04/04/2023
ms.custom: bap-template
---

# Setja upp tengilið samkeyrslu við Outlook sem er í Innanhússmiðstöð

Í þessari grein er hægt að læra hvernig setja á upp  [!INCLUDE[prod_short](includes/prod_short.md)]  innanhúss til að samstilla tengiliði í  [!INCLUDE[prod_short](includes/prod_short.md)]  við tengiliði í Outlook. Nánari upplýsingar um aðgerðina er að leita í til að  [Samstilla tengiliði í Viðskiptamiðinu við tengiliði í Microsoft Outlook](admin-synchronize-outlook-contacts.md).

## Kynning

Samstilling tengiliða krefst þess að nota OAuth 2,0 samskiptareglurnar fyrir sannvottun með Exchange Online. Áður hafði grunnsannvottun einnig verið studd, en hún verið fyrst og ekki studd lengur Exchange Online. Hægt er að lesa nánar um afskráð hjá  [sviptingu grunnskírteinis í Exchange Online](/exchange/clients-and-mobile-in-exchange-online/deprecation-of-basic-authentication-exchange-online). Þessi breyting þýðir að Samstilling tengiliða í Viðskiptamiðinu getur hafa hætt að virka í umhverfi innanhúss. Í þessari grein verður útskýrt hvernig á að fá það að virka aftur.

## Frumskilyrði

- Exchange Online, annað hvort með sjálfstæðri útgáfu eða með  Microsoft 365  áætlun  
- Aðgang að  Azure Active Directory  (Azure AD) leigjandi notaði Exchange Online
- [!INCLUDE[prod_short](includes/prod_short.md)] notendur hafa með sér  Microsoft 365  eða  Exchange Online  email reikning, sem er úthlutað reikningum í [!INCLUDE[prod_short](includes/prod_short.md)]. Hægt er að haka í þessa stillingu í  **Microsoft 365  hlutanum sannvottun**  á notandaforstillingu á  **listanum yfir notendur** . 

## Setja upp samkeyrslu tengiliðar

Ljúkið eftirfarandi skrefum til að setja upp tengiliðsamkeyrslu. Ef þú ert að keyra  [!INCLUDE[prod_short](includes/prod_short.md)]  vorið 2019 (v. 14) þá þarftu að gera aukaskref sem annað hvort breytir forritskóða eða setur upp tengingu við Power BI.

1. <a name="registerapp"></a> Skrá app fyrir  Exchange Online  API hjá  Azure AD  leigjandanum.

   Í þessu skrefi bætist við skráð App hjá  Azure AD  leigjanda  Microsoft 365  eða  Exchange Online  áætlun. Eins og aðrar Azure þjónustur sem vinna hjá Aðalviðskiptum,  Exchange Online  þarf skráð App í Azure AD. Skrásett App veitir sannvottun og heimildaþjónustu á milli Viðskiptamiðis og Exchange Online.

   Fylgdu nánari leiðbeiningum forritara og það Pro Help at  [skrá umsókn inn Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory). Eftir því sem farið er eftir leiðbeiningunum skal minnt á eftirfarandi atriði:

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

## Næstu skref

[Samstilla tengiliði í Aðalmiðinu við tengiliði í Microsoft Outlook](admin-synchronize-outlook-contacts.md)  
