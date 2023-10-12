---
title: Grunnstilling OneDrive samþættingar við Business Central á staðnum
description: Kynntu þér hvernig setja á upp Business Central á staðnum til að samþætta við OneDrive for Business.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'OneDrive, share, browser'
ms.date: 09/28/2023
ms.author: jswymer
---
# <a name="configuring-onedrive-integration-with-business-central-on-premises"></a>Grunnstilling OneDrive samþættingar við Business Central á staðnum

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Í þessari grein er útskýrt hvernig á að grunnstilla OneDrive samþættingu við Business Central á staðnum. Ólíkt [!INCLUDE[prod_short](includes/prod_short.md)] á netinu er tengingin milli Business Central og OneDrive for Business ekki sett upp sjálfkrafa. Ef tengingin er ekki stillt geta notendur ekki notað eiginleikana fyrir OneDrive.

Gera þarf tvö verk til að grunnstilla OneDrive samþættinguna.

- Fyrsta verkefnið felst í því að skrá inn umsókn (App) um  Microsoft Entra  leigjanda þinn í áætlun þinni Microsoft 365 . Skráða forritið er notað til auðkenningar. Þetta verk er yfirleitt gert í Azure-gáttinni og vefbiðlara Business Central.
- Hitt verkið felur í sér að setja upp tenginguna við OneDrive vefslóðina og kveikja á OneDrive eiginleikunum í Business Central. Þetta verk er gert í vefbiðlara Business Central. Það er gert öðruvísi fyrir útgáfu 21 en fyrir útgáfu 19 og 20. Útgáfa 21 kynnir nýja **OneDrive uppsetningu** sem kemur í staðinn fyrir uppsetningu **SharePoint tengingar**.  

> [!IMPORTANT]
> [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum er aðeins hægt að tengja við OneDrive sem Microsoft hýsir í skýinu. Að tengja [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum við gagnageymslu minna svæða á SharePoint Server er ekki stutt.

## <a name="register-an-app-in-microsoft-entra-id-for-onedrive-integration"></a><a name="registerapp"></a>Skrá app í  Microsoft Entra  auðkenni fyrir  OneDrive  samþættingu

Í þessu verkefni er bætt við skráðu App fyrir viðskipti miðsvæðis í  Microsoft Entra  tjarnarbíói á  Microsoft 365  áætlun. Eins og aðrir Azure þjónustuaðilar sem vinna með Central Business,  OneDrive  þurfa skráð App í  Microsoft Entra  auðkenni. Skráða forritið býður upp á sannvottun og sannvottunarþjónustu milli Business Central og SharePoint, sem OneDrive notar.

Ítarlegar leiðbeiningar um útfyllingu þessa skrefs er að finna  [í skrá umsókn í  Microsoft Entra  auðkenni](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory)  hjá hönnuði og það Pro Help.

Þegar þú skráir forritið skaltu hafa eftirfarandi punkta í huga:

- Ef forrit hefur þegar verið skráð sem hluti af samþættingu við aðra vöru Microsoft á borð við Power BI, þá getur þú notað þetta skráða forrit aftur. Í þessu tilviki þarftu bara að stilla SharePoint heimildirnar fyrir fyrirliggjandi skráð forrit.

- Gættu þess að grunnstilla skráða forritið með eftirfarandi úthlutuðum heimildum í SharePoint API:

    - AllSites.FullControl
    - User.ReadWrite.All
    
    Fyrir Business Central 2021 útgáfutímabil 2 (útgáfa 19) skaltu velja þessar heimildir í staðinn:
    
    - AllSites.Write
    - MyFiles.Write
    - User.Read.All 

- Ef þú notar Business Central-útgáfu 19 eða 20 skaltu afrita **Auðkenni forrits (biðlara)** og **leynilykil biðlara** sem skráða forritið notar. Þú þarft þessar upplýsingar fyrir næsta verki.

## <a name="get-your-onedrive-url"></a><a name="url"></a>Fá OneDrive vefslóðina

[!INCLUDE[onedrive-url](includes/onedrive-url.md)]

## <a name="set-up-the-onedrive-connection-in-version-21-and-later"></a>Setja upp OneDrive tengingu í útgáfu 21 og nýrri

Notaðu þetta ferli ef notað er Business Central útgáfutímabil 2022 (útgáfa 21) eða nýrra.

### <a name="prerequisites"></a>Frumskilyrði

- Óbein breytingar- og eyðingarheimild í töflu **Aðstæður skjalaþjónustu** sem lágmark

### <a name="run-onedrive-setup"></a>Keyra OneDrive uppsetningu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **OneDrive Uppsetning** og velja síðan viðkomandi tengil.
2. Í fyrsta sinn sem þú opnar aðstoðina sérðu **Persónuvernd**. Lestu upplýsingarnar á síðunni og ef þú samþykkir skilmálana skaltu velja **Samþykkja** til að halda áfram.
3. Á síðunni **Stilla meðhöndlun skráa** ertu með eftirfarandi valkosti til að velja úr:

   [!INCLUDE[onedrive-feature-options](includes/onedrive-feature-options.md)]

4. Á síðunni **Grunnstilla Business Central** skal slá inn vefslóð OneDrive í reitinn **OneDrive vefslóð**.

   [Hvernig finn ég OneDrive vefslóðina?](#url)
5. Veldu **Prófa tengingu** og bíddu eftir niðurstöðunum.
   - Ef prófið tekst er valið **Lokið** og þá er allt klárt.
   - Ef prófið stenst ekki færðu skilaboð sem lýsa vandamálinu. Vandamálið tengist yfirleitt vefslóðinni sem þú gafst upp. Veldu **Í lagi** til að fara aftur á síðuna **Grunnstilla Business Central**, staðfestu vefslóðina og reyndu aftur.
   - Ef þú hefur ekki þegar sett upp kennið fyrir  Microsoft Entra  skrásett forrit, opnast leiðbeiningar um kenni  **fyrir  Microsoft Entra**  uppsetningu.
6. Þegar þessu er lokið er persónuverndaryfirlýsingin fyrir OneDrive samþættingu samþykkt fyrir alla notendur. Ef þú vilt breyta henni þannig að notendur verði sjálfir að samþykkja eða hafna, þá skal fara á síðuna **Staða persónuverndaryfirlýsingar** og velja **Leyfa notanda að ákveða** fyrir OneDrive samþættinguna. Notendur verða þá beðnir um að samþykkja eða hafna persónuverndaryfirlýsingunni í fyrsta skipti sem þeir nota OneDrive eiginleikana. Frekari upplýsingar er að finna í [Persónuverndaryfirlýsingar](privacy-notices-status.md).

## <a name="set-up-the-connection-in--version-19-and-20"></a>Setja upp tenginguna í [!INCLUDE[prod_short](includes/prod_short.md)] útgáfu 19 og 20

Notaðu þetta ferli ef notað er Business Central 2022 útgáfutímabil 1 (útgáfa 20) eða 2021 útgáfutímabil 2 (útgáfa 19).
> [!IMPORTANT]
> Með því að stilla þennan eiginleika virkjar þú einnig eldri eiginleika sem senda skrár til OneDrive.  
>
>* Eiginleikinn Opna í Excel mun sjálfkrafa afrita Excel-skrána í OneDrive, síðan opna hana í Excel Online. 
>* Að flytja út skýrslu í skrá mun sjálfkrafa afrita skrána í OneDrive, síðan opna hana í Excel Online, Word Online eða OneDrive. 
>* Aðrir eiginleikar gætu einnig opnast sjálfkrafa í OneDrive.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning Microsoft SharePoint-tengingar** og velja síðan viðkomandi tengil.
2. Í reitinn **Lýsing** skal færa inn lýsingu fyrir tenginguna, á borð við **OneDrive**.
3. Í reitinn **Mappa** skal færa inn **Business Central**.
4. Í reitinn **Staðsetning** skal færa inn vefslóðina fyrir OneDrive.

   [Hvernig finn ég OneDrive vefslóðina?](#url)
5. Í reitinn **Auðkenni biðlara** skal færa inn biðlarakennið úr skráða forritinu.
6. Í reitinn **Leynilykill biðlara** skal færa inn leynilykilinn úr skráða forritinu. 

> [!IMPORTANT]
> **SharePointUppsetningarsíða tengingar** er notuð til að stilla marga eldri eiginleika. Í **Almenna** hlutanum er tengingin við OneDrive stillt og hlutinn **Samnýtt skjöl** framsendir skrár í SharePoint í staðinn. **Uppsetning SharePoint tengingar** hefur verið úrelt og verður fjarlægð í næstu útgáfu. Við mælum með að þú stillir ekki hlutann **Samnýtt skjöl**. Frekari upplýsingar er að finna í [Úreltir eiginleikar í grunnforritinu ](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#microsoft-sharepoint-connection-setup).

## <a name="after-upgrade-to-version-21"></a>Eftir uppfærslu í útgáfu 21

Þegar þú uppfærir í útgáfu 21 eða nýrri mun núverandi tenging við OneDrive sem grunnstillt er á síðunni **Uppsetning SharePoint tengingar** enn virka. En vegna þess að síðan **Uppsetning SharePoint tengingar** verður fjarlægð í útgáfu 23 mælum við með því að þú skiptir yfir í nýju OneDrive samþættinguna eins og lýst er í næsta hluta. Að skipta yfir núna auðveldar hlutina þegar **Uppsetning SharePoint tengingar** verður að lokum fjarlægð. Auk þess gerir það þér kleift að nota uppsetningarleiðbeininguna **OneDrive uppsetning** til að stjórna OneDrive eiginleikum sem þú getur nálgast.

## <a name="switching-from-legacy-sharepoint-to-new-onedrive-integration"></a>Skipt úr eldra SharePoint yfir í nýja OneDrive samþættingu

Til að skipta yfir í nýju OneDrive samþættinguna keyrir þú uppsetningarleiðbeiningarnar **OneDrive uppsetning** með hjálp, sem hægt er að opna beint eða af eldri síðu **Uppsetningar SharePoint tengingar**. Uppsetning **OneDrive uppsetningar** með hjálp leiðir þig í gegnum umbreytinguna og veitir upplýsingar um breytingarnar sem verið er að gera.

Áður en þú hefst handa með umbreytinguna, eða meðan á henni stendur, skaltu skoða næsta hluta til að kynna þér nokkra þætti um ferlið. 

### <a name="about-switching-to-the-new-onedrive-integration"></a><a name="onedrivesetupmigration"></a>Um skiptingu yfir í nýju OneDrive samþættinguna

Til viðbótar við OneDrive samþættingu getur Business Central einnig samþæst við aðra þjónustu eins og Power BI og Universal print. Samþætting við þessa aðra þjónustu krefst einnig skráar  Microsoft Entra  app til auðkenningar.  Microsoft Entra App sem þessi önnur þjónusta er skilgreind fyrir  **er stillt  Microsoft Entra  í uppsetningu viðskiptaaðstoðar** . Þegar skipt er úr eldri  SharePoint  tengingum í uppsetningu mun  **OneDrive  ný**  Uppsetning aðstoða uppsetningu á uppsetningarforritinu  OneDrive  til að nota kerfið  **Setja upp  Microsoft Entra  uppsetningu**  fyrir aðstoðar lánardrottna &mdash; svo allir samþættingar noti sama  Microsoft Entra  App.

Þessi breyting hefur þýðingu þegar skipt er yfir í nýja  OneDrive  samþættingu eftir því hvort Microsoft-forrit sem  **er búið að skilgreina í uppsetningu viðskiptaaðstoðar  Microsoft Entra  setur upp** . 

> [!IMPORTANT]
> Þegar þú hefur skipt yfir í nýju OneDrive uppsetninguna geturðu ekki lengur notað síðuna **Uppsetning SharePoint tengingar** til að grunnstilla OneDrive samþættingu.

#### <a name="how-the-changes-affect-the-integration"></a>Hvernig breytingarnar hafa áhrif á samþættinguna

 **OneDrive** Uppsetningarforritið aðstoðar notar alltaf App sem er samskipað í  **Microsoft Entra  uppsetningu viðskiptaaðstoðar**, ef einhver er. Þegar keyrð  **OneDrive**  er Uppsetning aðstoðar-forrits er það borið saman við App sem samskipað er í  **Microsoft Entra  uppsetningu lykla**  með núverandi forriti sem samskipað er í  **SharePoint  Uppsetning** tengingar.

> [!TIP]
>  **SharePoint Í uppsetningarforritinu tenging**  og  **Setja upp  Microsoft Entra  uppsetningu**  VIÐSKIPTAAÐSTOÐAR  Microsoft Entra  er forritið auðkennt með  **Kenni** biðlara.

- Ef App í  **Microsoft Entra  Uppsetning lykla**  er annað en App í  **SharePoint  tengingaruppsetningu** OneDrive  breytist sameining til að nota App í  **Microsoft Entra  uppsetningu reikninga**.

   Í **OneDrive uppsetning** á meðan skipt er yfir færðu skilaboð svipuð og eftirfarandi texti: 

  `The Microsoft Entra application used for authentication will be configured for all Business Central integrations. This means the client id will change to NNNNNNNNN-NNNN-NNNN-NNNN-NNNNNNNNNNNN, you may want to test it has the correct permissions.`

  `NNNNNNNNN-NNNN-NNNN-NNNN-NNNNNNNNNNNN` táknar KENNI biðlara forritsins í  **uppsetningu  Microsoft Entra  reikninga**  sem  OneDrive  samþættingu hefur verið skipt við. 

  > [!IMPORTANT]
  > Til að ný OneDrive samþætting virki eftir að skipt er um, þarftu að veita forritinu heimild að SharePoint API í Azure-gáttinni. Þú getur gert þetta áður eða eftir að þú skiptir yfir í nýju OneDrive uppsetninguna. Frekari upplýsingar er að finna í kaflanum  [skrá app í  Microsoft Entra  Kenni  OneDrive  samþættingar](#registerapp).

- Ef App í  **Microsoft Entra  Uppsetning lykla**  er það sama og App í  **SharePoint  uppsetningu** OneDrive  tengingar notar Samþætting sama App og áður, nema frá samskipun í  **Microsoft Entra  uppsetningu lykla**  uppsetningar.

   Í **OneDrive uppsetning** á meðan skipt er yfir færðu skilaboð svipuð og eftirfarandi texti:

    `The Microsoft Entra application used for authentication will be configured for all Business Central integrations. This has already been configured with the same client id (5F78CADE-19C0-49BF-AF84-306D0579B50E).`

- Ef ekkert forrit er skilgreint í  **Microsoft Entra  uppsetningu lykla**  uppsetningar  OneDrive  mun Samþætting nota sama App og áður.

    **OneDrive** Uppsetningarforritið aðstoðar afritar forritið samskipan  **Microsoft Entra  uppsetningar lykla**  uppsetningar þannig að það verður notað fyrir aðra samþættingu í sem gæti verið sett upp síðar.

   Í **OneDrive uppsetning** á meðan skipt er yfir færðu skilaboð svipuð og eftirfarandi texti:

   `The Microsoft Entra application used for authentication will be configured for all Business Central integrations`.

### <a name="run-onedrive-setup-to-switch-to-the-new-onedrive-integration"></a>Keyrðu OneDrive uppsetningu til að skipta yfir í nýju OneDrive samþættinguna

1. Opna annaðhvort síðuna **OneDrive uppsetning** eða síðuna **Uppsetning SharePoint tengingar**.
2. Ef notuð er síðan **Uppsetning SharePoint tengingar** skal velja **Fara í nýju OneDrive uppsetninguna** í tilkynningunni efst á síðunni.
3. Fylgdu leiðbeiningu um **OneDrive uppsetningu** með hjálp.
4. Þegar þú ferð á síðuna **Grunnstilla skráarmeðhöndlun** skaltu velja einn af eftirfarandi valkostum til að kveikja á eiginleikum:

   [!INCLUDE[onedrive-feature-options](includes/onedrive-feature-options.md)]

5. Síðan **Grunnstilla Business Central** sýnir sömu vefslóðina og er notuð af fyrirliggjandi OneDrive samþættingu. Hægt er að breyta vefslóðinni eins og þarf.
6. Veldu **Prófa tengingu** og fylgdu leiðbeiningunum.

   Ef prófið heppnast skaltu velja **lokið** og þá er allt til reiðu. Notaðu annars skilaboðin á síðunni til að hjálpa þér að leysa vandamálið.

## <a name="see-also"></a>Sjá einnig
[Business Central og OneDrive fyrir Business Integration](across-onedrive-overview.md)  
[Opna Business Central Files í OneDrive](across-share-onedrive.md)  
[OneDrive ALGENGAR SPURNINGAR](admin-onedrive-faq.md)

