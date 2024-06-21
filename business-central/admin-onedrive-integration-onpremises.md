---
title: Grunnstilling OneDrive samþættingar við Business Central innanhúss
description: Fræðast um hvernig á að setja upp Business Central innanhúss til að samþætta sig við OneDrive fyrir vinnu eða skóla (áður þekkt sem OneDrive fyrir fyrirtæki).
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'OneDrive, share, browser'
ms.date: 06/13/2024
ms.author: jswymer
ms.service: dynamics-365-op
ms.reviewer: jswymer
---
# Grunnstilling OneDrive samþættingar við Business Central innanhúss

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Þessi grein útskýrir hvernig á að grunnstilla OneDrive fyrir vinnu eða skóla (áður þekkt sem OneDrive fyrir fyrirtæki) samþættingu við Business Central á staðnum. Ólíkt [!INCLUDE[prod_short](includes/prod_short.md)] netinu er tengingin milli Business Central og OneDrive ekki sett upp sjálfkrafa. Ef tengingin er ekki stillt geta notendur ekki notað eiginleikana fyrir OneDrive.

Gera þarf tvö verk til að grunnstilla OneDrive samþættinguna.

- Fyrsti verkhlutinn felur í sér að skrá forrit (forrit) vegna leigjanda áætlunarinnar Microsoft Entra  Microsoft 365 . Skráða forritið er notað til auðkenningar. Þetta verk er yfirleitt gert í Azure-gáttinni og vefbiðlara Business Central.
- Hitt verkið felur í sér að setja upp tenginguna við OneDrive vefslóðina og kveikja á OneDrive eiginleikunum í Business Central. Þetta verk er gert í vefbiðlara Business Central. Það er gert öðruvísi fyrir útgáfu 21 en fyrir útgáfu 19 og 20. Útgáfa 21 kynnir nýja **OneDrive uppsetningu** sem kemur í staðinn fyrir uppsetningu **SharePoint tengingar**.  

> [!IMPORTANT]
> [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum er aðeins hægt að tengja við OneDrive sem Microsoft hýsir í skýinu. Að tengja [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum við gagnageymslu minna svæða á SharePoint Server er ekki stutt.

## <a name="registerapp"></a> Skrá forrit í Microsoft Entra auðkenni til OneDrive samþættingar

Í þessu verki bætir þú við skráðu forriti fyrir Business Central í Microsoft Entra leigjanda áætlunarinnar Microsoft 365 . Eins og önnur Azure þjónusta sem vinnur með Business Central krefst OneDrive  skráðs forrits í Microsoft Entra auðkenni. Skráða forritið býður upp á sannvottun og sannvottunarþjónustu milli Business Central og SharePoint, sem OneDrive notar.

Nánari skref til að ljúka þessu skrefi [er að finna í Skrá forrit í Microsoft Entra kenni](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory) í hjálp forritara og tæknimanns.

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

## <a name="url"></a>Fá OneDrive vefslóðina

[!INCLUDE[onedrive-url](includes/onedrive-url.md)]

## Setja upp OneDrive tengingu í útgáfu 21 og nýrri

Notaðu þetta ferli ef notað er Business Central útgáfutímabil 2022 (útgáfa 21) eða nýrra.

### Frumskilyrði

- Óbein breytingar- og eyðingarheimild í töflu **Aðstæður skjalaþjónustu** sem lágmark

### Keyra OneDrive uppsetningu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **OneDrive Uppsetning** og velja síðan viðkomandi tengil.
2. Í fyrsta skipti sem aðstoðaruppsetningin er keyrð sést **persónuvernd** þín. Lestu upplýsingarnar á síðunni og ef þú samþykkir skilmálana skaltu velja **Samþykkja** til að halda áfram.
3. Á síðunni **Stilla meðhöndlun skráa** ertu með eftirfarandi valkosti til að velja úr:

   [!INCLUDE[onedrive-feature-options](includes/onedrive-feature-options.md)]

4. Á síðunni **Grunnstilla Business Central** skal slá inn vefslóð OneDrive í reitinn **OneDrive vefslóð**.

   [Hvernig finn ég OneDrive vefslóðina?](#url)
5. Veldu **Prófa tengingu** og bíddu eftir niðurstöðunum.
   - Ef prófið tekst er valið **Lokið** og þá er allt klárt.
   - Ef prófunin mistakist fást skilaboð sem lýsa vandamálinu. Vandamálið tengist yfirleitt vefslóðinni sem þú gafst upp. Veldu **Í lagi** til að fara aftur á síðuna **Grunnstilla Business Central**, staðfestu vefslóðina og reyndu aftur.
   - Ef þú hefur ekki þegar sett upp skráða forritið Microsoft Entra opnast leiðsagnarforritið **Setja upp Microsoft Entra kenni** .
6. Þegar þessu er lokið er persónuverndaryfirlýsingin fyrir OneDrive samþættingu samþykkt fyrir alla notendur. Ef þú vilt breyta henni þannig að notendur verði sjálfir að samþykkja eða hafna, þá skal fara á síðuna **Staða persónuverndaryfirlýsingar** og velja **Leyfa notanda að ákveða** fyrir OneDrive samþættinguna. Notendur verða þá beðnir um að samþykkja eða hafna persónuverndaryfirlýsingunni í fyrsta skipti sem þeir nota OneDrive eiginleikana. Frekari upplýsingar er að finna í [Persónuverndaryfirlýsingar](privacy-notices-status.md).

## Setja upp tenginguna í [!INCLUDE[prod_short](includes/prod_short.md)] útgáfu 19 og 20

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

## Eftir uppfærslu í útgáfu 21

Þegar þú uppfærir í útgáfu 21 eða nýrri mun núverandi tenging við OneDrive sem grunnstillt er á síðunni **Uppsetning SharePoint tengingar** enn virka. En vegna þess að síðan **Uppsetning SharePoint tengingar** verður fjarlægð í útgáfu 23 mælum við með því að þú skiptir yfir í nýju OneDrive samþættinguna eins og lýst er í næsta hluta. Þessi rofi er gerður auðveldari þegar **SharePoint uppsetning** tengingar er fjarlægð að lokum. Auk þess gerir það notandanum kleift að nota **OneDrive uppsetningarleiðbeiningar** með hjálp til að stjórna eiginleikum OneDrive notenda sem eru aðgengilegir notendum.

## Skipt úr eldra SharePoint yfir í nýja OneDrive samþættingu 

Til að skipta yfir í nýju OneDrive samþættinguna keyrir þú uppsetningarleiðbeiningarnar **OneDrive uppsetning** með hjálp, sem hægt er að opna beint eða af eldri síðu **Uppsetningar SharePoint tengingar**. Uppsetningin **OneDrive** sem aðstoðar leiðir notandann í gegnum breytinguna og veitir upplýsingar um breytingarnar sem gerðar eru á leiðinni.

Áður en þú hefst handa með umbreytinguna, eða meðan á henni stendur, skaltu skoða næsta hluta til að kynna þér nokkra þætti um ferlið. 

### <a name="onedrivesetupmigration"></a>Um skiptingu yfir í nýju OneDrive samþættinguna

Til viðbótar við OneDrive samþættingu getur Business Central einnig samþæst við aðra þjónustu eins og Power BI og Universal print. Samþætting við þessa þjónustu krefst einnig skráðs Microsoft Entra forrits til sannvottunar. Forritið Microsoft Entra sem þessi önnur þjónusta notar er grunnstillt í **Setja upp reikninga Microsoft Entra með** aðstoðaruppsetningu. Þegar skipt er úr uppsetningu eldri SharePoint tengingar breytir **OneDrive nýja** uppsetningaruppsetningin OneDrive með aðstoð við að samþættingu við að nota **einnig uppsetninguna Microsoft Entra Setja upp** reikninga&mdash; með aðstoð svo að allar samþættingar noti sama Microsoft Entra forritið.

Þessi breyting hefur þýðingu þegar skipt er yfir í nýju OneDrive samþættinguna eftir því hvort Microsoft-forrit er þegar grunnstillt í **uppsetningu reikninganna sem Microsoft Entra aðstoðar við** að setja upp. 

> [!IMPORTANT]
> Þegar þú hefur skipt yfir í nýju OneDrive uppsetninguna geturðu ekki lengur notað síðuna **Uppsetning SharePoint tengingar** til að grunnstilla OneDrive samþættingu.

#### Hvernig breytingarnar hafa áhrif á samþættinguna

Uppsetningaruppsetningin **OneDrive** með hjálp uppsetningarinnar notar alltaf forritið sem er grunnstillt í **uppsetningu reikninganna Microsoft Entra ,** ef einhver er. Þegar uppsetningin aðstoðar við uppsetningu er **OneDrive keyrð ber það forritið sem grunnstillt var í** Setja upp **reikninga Microsoft Entra við gildandi forrit sem grunnstillt er í** uppsetningu tenginga **SharePoint .**

> [!TIP]
> Á síðunni **SharePoint Uppsetning** tengingar og **Setja upp reikninga Microsoft Entra með** aðstoðaruppsetningu er forritið Microsoft Entra auðkennt með kenni **biðlarans**.

- Ef forritið í **Setja upp Microsoft Entra reikninga** er annað en forritið í **SharePoint uppsetningu** OneDrive  tengingar breytist samþættingin til að nota forritið í **Setja upp Microsoft Entra reikninga**.

   Í **OneDrive Uppsetning** á meðan rofinn er gerður fást boð svipuð eftirfarandi texta: 

  `The Microsoft Entra application used for authentication will be configured for all Business Central integrations. This means the client id will change to NNNNNNNNN-NNNN-NNNN-NNNN-NNNNNNNNNNNN, you may want to test it has the correct permissions.`

  `NNNNNNNNN-NNNN-NNNN-NNNN-NNNNNNNNNNNN` táknar kenni biðlara forritsins í **Setja upp Microsoft Entra reikninga** sem OneDrive samþætting hefur verið breytt í. 

  > [!IMPORTANT]
  > Til að ný OneDrive samþætting virki eftir að skipt er um, þarftu að veita forritinu heimild að SharePoint API í Azure-gáttinni. Þú getur gert þetta áður eða eftir að þú skiptir yfir í nýju OneDrive uppsetninguna. Nánari upplýsingar eru í hlutanum [Skrá forrit í Microsoft Entra kenni til OneDrive samþættingar](#registerapp).

- Ef forritið í **Setja upp reikningana Microsoft Entra þína** er það sama og forritið í **SharePoint uppsetningu** OneDrive  tenginga notar samþættingin sama forrit og áður, nema frá grunnstillingunni **í uppsetningu reikninga Microsoft Entra .** 

   Í **OneDrive Uppsetning** á meðan rofinn er gerður fást boð svipuð eftirfarandi texta:

    `The Microsoft Entra application used for authentication will be configured for all Business Central integrations. This has already been configured with the same client id (5F78CADE-19C0-49BF-AF84-306D0579B50E).`

- Ef ekkert forrit er grunnstillt í **uppsetningu Microsoft Entra reikninga** notar OneDrive samþættingin sama forrit og áður.

   Uppsetningaruppsetningin **OneDrive** sem aðstoðar við að afrita grunnstillingu forrits **í uppsetningu Microsoft Entra reikninga** þannig að hún er notuð í öðrum samþættingum sem gætu verið settar upp síðar.

   Í **OneDrive Uppsetning** á meðan rofinn er gerður fást boð svipuð eftirfarandi texta:

   `The Microsoft Entra application used for authentication will be configured for all Business Central integrations`.

### Keyrðu OneDrive uppsetningu til að skipta yfir í nýju OneDrive samþættinguna

1. Opna annaðhvort síðuna **OneDrive uppsetning** eða síðuna **Uppsetning SharePoint tengingar**.
2. Ef notuð er síðan **Uppsetning SharePoint tengingar** skal velja **Fara í nýju OneDrive uppsetninguna** í tilkynningunni efst á síðunni.
3. Fylgdu leiðbeiningu um **OneDrive uppsetningu** með hjálp.
4. Þegar þú ferð á síðuna **Grunnstilla skráarmeðhöndlun** skaltu velja einn af eftirfarandi valkostum til að kveikja á eiginleikum:

   [!INCLUDE[onedrive-feature-options](includes/onedrive-feature-options.md)]

5. Síðan **Grunnstilla Business Central** sýnir sömu vefslóðina og er notuð af fyrirliggjandi OneDrive samþættingu. Hægt er að breyta vefslóðinni eins og þarf.
6. Veldu **Prófa tengingu** og fylgdu leiðbeiningunum.

   Ef prófið heppnast skaltu velja **lokið** og þá er allt til reiðu. Notaðu annars skilaboðin á síðunni til að hjálpa þér að leysa vandamálið.

## Sjá einnig .
[Business Central og OneDrive samþætting](across-onedrive-overview.md)  
[Opna Business Central Files í OneDrive](across-share-onedrive.md)  
[OneDrive ALGENGAR SPURNINGAR](admin-onedrive-faq.md)

