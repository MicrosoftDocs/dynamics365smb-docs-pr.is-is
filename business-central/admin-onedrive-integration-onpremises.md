---
title: Skilgreining OneDrive samþættingar við fyrirtæki miðsvæðis innanhúss
description: Frekari upplýsingar um hvernig á að setja upp rekstur miðsvæðis innanhúss til að samþætta við OneDrive fyrir fyrirtæki.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OneDrive, share, browser
ms.date: 09/06/2022
ms.author: jswymer
ms.openlocfilehash: e1e3190ae61334042f1d4ff7aaf2026de2c2b4a5
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9608486"
---
# <a name="configuring-onedrive-integration-with-business-central-on-premises"></a>Skilgreining OneDrive samþættingar við fyrirtæki miðsvæðis innanhúss

Í greininni er útskýrt hvernig skilgreina OneDrive á samþættingu við rekstur miðsvæðis innanhúss. Ólíkt [!INCLUDE[prod_short](includes/prod_short.md)] á netinu er tengingin á milli Viðskiptamiðis og OneDrive fyrir viðskipti ekki sett upp sjálfkrafa. Ef tengingin er ekki stillt geta notendur ekki notað eiginleikana fyrir OneDrive.

Það eru tvö verkefni sem þarf að gera til að skilgreina OneDrive samþættingu.

- Fyrsta verkefnið felst í því að skrá inn umsókn (App) um Azure Active Directory leigjanda þinn í áætlun þinni Microsoft 365. Skráð App er notað í sannvottunarskyni. Þetta verk er vanalega gert í Azure gáttinni og í Aðalvefbiðlara Business Central.
- Annað verkefnið felst í því að setja upp tenginguna við OneDrive slóðina og kveikja á OneDrive aðgerðum í viðskiptamiðinu. Þetta verkefni í gert í vefbiðlara Business Central. Það er gert öðruvísi fyrir útgáfu 21 en fyrir útgáfur 19 og 20. Útgáfa 21 kynnir nýja **OneDrive uppsetningu sem kemur í** stað tengingar uppsetningar **SharePoint**.  

> [!IMPORTANT]
> [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum er aðeins hægt að tengja við OneDrive sem Microsoft hýsir í skýinu. Að tengja [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum við gagnageymslu minna svæða á SharePoint Server er ekki stutt.

## <a name="register-an-app-in-azure-ad-for-onedrive-integration"></a><a name="registerapp"></a> Skrá app í Azure AD fyrir OneDrive samþættingu

Í þessu verkefni er bætt við skráðu App fyrir viðskipti miðsvæðis í Azure AD tjarnarbíói á Microsoft 365 áætlun. Eins og aðrar Azure þjónustur sem vinna hjá Aðalstarfsemi fyrirtækja, OneDrive þarf skráð App í Azure Active Directory (Azure AD). Með skráðu App er til að finna sannvottun og heimildaþjónustu á milli Viðskiptamiðis og SharePoint þess sem notast er við OneDrive.

Ítarlegar leiðbeiningar við útfyllingu þessa skrefs er að finna [í skrá umsókn í Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory) hjá HÖNNUÐI og það Pro Help.

Eftir því sem umsóknin er skráð þarf að huga að eftirfarandi punktum:

- Ef þú hefur þegar skráð inn umsókn sem hluta af samþættingu við aðra Microsoft vöru, eins og Power BI, þá endurnýtú það skrásett forrit. Í þessu tilfelli þarftu bara að stilla SharePoint heimildirnar fyrir það skráða sem fyrir er á skráðu forritinu.

- Gætið þess að samskipa skráðu App með eftirtöldum heimildum SharePoint í API:

    - Alletur. Fulleftirlit
    - User. Lesiwrite. allar
    
    Fyrir viðskipti Mið 2021 út Wave 2 (útgáfa 19), setjið þessar heimildir í staðinn:
    
    - AllSites.Write
    - MyFiles.Write
    - User.Read.All 

- Ef þú ert að **nota viðskiptablaðið 19 eða 20 skaltu AFRITA auðkenni** forritsins (biðlara) og **leyniorð** biðlara sem skráð App notar. Þú þarft þessar upplýsingar fyrir næsta verki.

## <a name="get-your-onedrive-url"></a><a name="url"></a> Sæktu slóðina þína OneDrive

[!INCLUDE[onedrive-url](includes/onedrive-url.md)]

## <a name="set-up-the-onedrive-connection-in-version-21-and-later"></a>Tengingin var OneDrive sett upp í útgáfu 21 og síðar

Notaðu þetta ferli ef þú ert að nota Central 2022 Release Wave 2 (útgáfa 21) eða síðar.

### <a name="prerequisites"></a>Frumskilyrði

- Óbein, breyta og eyða (IMD) heimild um Þjónustuaðstæður **í töfluskjali** sem lágmarks

### <a name="run-onedrive-setup"></a>Keyra OneDrive uppsetningu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **OneDrive uppsetningu** og veljið síðan tengda tengilinn.
2. Í fyrsta sinn sem þú keyrir uppsetningarforritið hjálpar þú í **næði**. Lestu upplýsingarnar á síðunni og ef þú samþykkir skilmálana velur **þú að samþykkja** að halda áfram.
3. **Á síðunni Skilgreina skrármeðhöndlun** eru Eftirtaldir valkostir til að velja úr:

   [!INCLUDE[onedrive-feature-options](includes/onedrive-feature-options.md)]

4. **Vefslóð á vefsvæðið samskipa** er færð inn OneDrive í **OneDrive reitinn URL**.

   [Hvernig finn ég slóðina mína OneDrive ?](#url)
5. Veldu **Prufutengingu** og Bíddu eftir niðurstöðunum.
   - Ef prófun heppnast skaltu velja **Done**, þá ertu tilbúin (NUM) til að fara.
   - Ef prófið mistekst færðu skilaboð sem lýsa vandamálinu. Yfirleitt er vandamálið að gera með SLÓÐINA sem þú gafst upp. Veldu **í lagi** til að fara aftur **í aðalsíðu** samskipa, staðfesta vefslóðina og reyna aftur.
   - Ef þú hefur ekki þegar sett upp Azure AD skrásett App þá opnast leiðbeiningar með **Azure Active Directory** uppsetningu.
6. Að því loknu tekur persónuvernd til OneDrive samþættingar fyrir alla notendur. Ef þú vilt breyta því þannig að notendur verða að vera sammála eða ósammála sjálfum sér, þá skaltu fara í **Privacy tilkynningar stöðusíðu** og velja **Let notandi ákveða** fyrir OneDrive samþættingu. Notendur verða þá Vinsamlega beðnir um að vera sammála eða ósammála tilkynningu persónuverndar í fyrsta sinn sem þeir nota OneDrive aðgerðirnar. Sjá [Privacy tilkynningar](privacy-notices-status.md) til frekari upplýsinga.

## <a name="set-up-the-connection-in-prod_short-version-19-and-20"></a>Tenginguna sett upp í [!INCLUDE[prod_short](includes/prod_short.md)] útgáfum 19 og 20

Notaðu þetta ferli ef þú ert að nota 2022 út bylgju 1 (útgáfa 20) eða 2021 út bylgju 2 (útgáfa 19).
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

   [Hvernig finn ég slóðina mína OneDrive ?](#url)
5. **Í REITINN kenni** biðlara er FÆRT inn kenni biðlara í skráð App.
6. **Sláðu inn leyninúmer í reitinn leyndarmál** í biðlara skráðu forritsins. 

> [!IMPORTANT]
> **SharePoint Síðan Tengingaruppsetningarsíða** er notuð til að skilgreina marga eldri eiginleika. Í **Almenna** hlutanum er tengingin við OneDrive stillt og hlutinn **Samnýtt skjöl** framsendir skrár í SharePoint í staðinn. **SharePoint Uppsetning** tengingar hefur verið afskrifaðar og verður fjarlægð í næstu útgáfu. Við mælum með að þú stillir ekki hlutann **Samnýtt skjöl**. Sjá [afskrifaðar aðgerðir í Grunnforritinu](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#microsoft-sharepoint-connection-setup) til að fá nánari upplýsingar.

## <a name="after-upgrade-to-version-21"></a>Eftir uppfærslu í útgáfu 21

Þegar uppfært er í útgáfu 21 eða nýrra verka er tiltæk Tengingin við OneDrive það skilgreind á **SharePoint uppsetningarsíðu** tengingarinnar. En vegna þess **SharePoint að Uppsetningarsíða** tengingarinnar verður fjarlægð í útgáfu 23, er mælt með því að skipta yfir í nýja OneDrive samþættingu, eins og lýst er í næsta kafla. Ef þessi rofi er gerður mun það verða auðveldara þegar Uppsetning **SharePoint tengingar er á** endanum fjarlægð. Auk þess sem það gerir kleift að nota leiðbeiningar um **OneDrive** uppsetningu uppsetningarhjálpar til að stjórna OneDrive aðgerðunum sem eru aðgengilegar fyrir notendur.

## <a name="switching-from-legacy-sharepoint-to-new-onedrive-integration"></a>Skipt úr Legacy SharePoint í nýjar OneDrive samþættingar 

Ef skipta á um nýja OneDrive samþættingu er uppsetningarhandbók uppsetningarhjálpar **OneDrive keyrð**, sem hægt er að opna beint eða á uppsetningarsíðu **SharePoint eldri** tenginga. **OneDrive** Uppsetningarforritið aðstoðar mun leiða þig í gegnum umskiptin, veita upplýsingar um breytingar sem eru gerðar eftir leiðinni.

Áður en hafist er handa við skiptinguna eða eins og verið er að gera hana skal vísa í næsta kafla til að fræðast um nokkra þætti og sjónarmið um ferlið. 

### <a name="about-switching-to-the-new-onedrive-integration"></a><a name="onedrivesetupmigration"></a> Um að skipta yfir í nýja OneDrive samþættingu

Auk OneDrive samþættingar getur rekstur miðsvæðis einnig samþætt aðra þjónustu, líkt Power BI og Universal print. Samþætting við þessa aðra þjónustu krefst einnig skráar Azure AD app til auðkenningar. Azure AD App sem þessi önnur þjónusta er skilgreind fyrir **er stillt Azure Active Directory í uppsetningu viðskiptaaðstoðar**. Þegar skipt er úr eldri SharePoint tengingum í uppsetningu mun **OneDrive ný** Uppsetning aðstoða uppsetningu á uppsetningarforritinu OneDrive til að nota kerfið **Setja upp Azure Active Directory uppsetningu** fyrir aðstoðar lánardrottna &mdash; svo allir samþættingar noti sama Azure AD App.

Þessi breyting hefur þýðingu þegar skipt er yfir í nýja OneDrive samþættingu eftir því hvort um er að ræða Azure AD App sem er samskipað í **Azure Active Directory uppsetningu viðskiptaaðstoðar**. 

> [!IMPORTANT]
> Þegar skipt hefur verið yfir í nýja OneDrive uppsetningu er ekki lengur hægt að nota **SharePoint síðuna Uppsetning** tengingar til að skilgreina OneDrive samþættingu.

#### <a name="how-the-changes-affect-the-integration"></a>Hvernig breytingarnar hafa áhrif á samþættingu

**OneDrive** Uppsetningarforritið aðstoðar notar alltaf App sem er samskipað í **Azure Active Directory uppsetningu viðskiptaaðstoðar**, ef einhver er. Þegar keyrð **OneDrive** er Uppsetning aðstoðar-forrits er það borið saman við App sem samskipað er í **Azure Active Directory uppsetningu lykla** með núverandi forriti sem samskipað er í **SharePoint Uppsetning** tengingar.

> [!TIP]
> **SharePoint Í uppsetningarforritinu tenging** og **Setja upp Azure Active Directory uppsetningu** VIÐSKIPTAAÐSTOÐAR Azure AD er forritið auðkennt með **Kenni** biðlara.

- Ef App í **Azure Active Directory Uppsetning lykla** er annað en App í **SharePoint tengingaruppsetningu** OneDrive breytist sameining til að nota App í **Azure Active Directory uppsetningu reikninga**.

   Í uppsetningarforritinu **OneDrive á** meðan Skiptingin er gerð færðu skilaboð á svipaðan eftirfarandi texta: 

  `The Azure Active Directory Application used for authentication will be configured for all Business Central integrations. This means the client id will change to NNNNNNNNN-NNNN-NNNN-NNNN-NNNNNNNNNNNN, you may want to test it has the correct permissions.`

  `NNNNNNNNN-NNNN-NNNN-NNNN-NNNNNNNNNNNN` táknar KENNI biðlara forritsins í **uppsetningu Azure Active Directory reikninga** sem OneDrive samþættingu hefur verið skipt við. 

  > [!IMPORTANT]
  > Fyrir nýja OneDrive samþættingu til að vinna eftir að Skiptingin hefur verið gerð þarf að veita App heimild SharePoint fyrir API í Azure gáttinni. Hægt er að gera þetta skrefinu á undan eða eftir að skipt var yfir í nýja OneDrive uppsetninguna. Frekari upplýsingar er að finna í kaflanum [skrá app í Azure AD til OneDrive samþættingar](#registerapp).

- Ef App í **Azure Active Directory Uppsetning lykla** er það sama og App í **SharePoint uppsetningu** OneDrive tengingar notar Samþætting sama App og áður, nema frá samskipun í **Azure Active Directory uppsetningu lykla** uppsetningar.

   Í Setup **OneDrive á** meðan Skiptingin er gerð,, færðu skilaboð á svipaðan eftirfarandi texta:

    `The Azure Active Directory Application used for authentication will be configured for all Business Central integrations. This has already been configured with the same client id (5F78CADE-19C0-49BF-AF84-306D0579B50E).`

- Ef ekkert forrit er skilgreint í **Azure Active Directory uppsetningu lykla** uppsetningar OneDrive mun Samþætting nota sama App og áður.

   **OneDrive** Uppsetningarforritið aðstoðar afritar forritið samskipan **Azure Active Directory uppsetningar lykla** uppsetningar þannig að það verður notað fyrir aðra samþættingu í sem gæti verið sett upp síðar.

   Í uppsetningarforritinu **OneDrive á** meðan Skiptingin er gerð færðu skilaboð á svipaðan eftirfarandi texta:

   `The Azure Active Directory Application used for authentication will be configured for all Business Central integrations`.

### <a name="run-onedrive-setup-to-switch-to-the-new-onedrive-integration"></a>Keyra OneDrive uppsetningu til að skipta yfir í nýja OneDrive samþættingu

1. Opnið annað hvort **OneDrive uppsetningarsíðuna** eða **SharePoint síðu tengingaruppsetningarsíðunnar**.
2. Ef þú ert að nota **SharePoint síðuna Tengingarskipulag**, Veldu **fara í nýja OneDrive uppsetningu** í tilkynningunni efst á síðunni.
3. Fylgja skal leiðbeiningum um **OneDrive** uppsetningu aðstoðar.
4. Þegar farið er á **síðuna skilgreina skrármeðhöndlun** skal velja einn af eftirtöldum valkostum fyrir að kveikja á aðgerðum:

   [!INCLUDE[onedrive-feature-options](includes/onedrive-feature-options.md)]

5. **Á vefsíðu samskipa fyrirtækja** BIRTIST sama vefslóð og notuð er fyrir samþættingu sem til OneDrive er. Hægt er að breyta VEFSLÓÐINNI eftir þörfum.
6. Veldu **Prufutengingu** og fylgdu leiðbeiningunum.

   Ef prófun heppnast skaltu velja **Done** og þú ert tilbúinn að fara. Annars skaltu nota skilaboðin á síðunni til að hjálpa þér að leysa vandann.

## <a name="see-also"></a>Sjá einnig
[Business Central og OneDrive fyrir Business Integration](across-onedrive-overview.md)  
[Opna Business Central Files í OneDrive](across-share-onedrive.md)  
[OneDrive ALGENGAR SPURNINGAR](admin-onedrive-faq.md)

