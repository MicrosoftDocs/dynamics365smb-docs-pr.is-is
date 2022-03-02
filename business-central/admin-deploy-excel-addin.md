---
title: Innbót Business Central sótt fyrir Excel
description: Kynntu þér hvernig sækja á innbót Business Central fyrir Excel handa notendum.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Excel, add-in, centralized deployment, M365 admin center, individual acquisition, appsource
ms.date: 10/07/2021
ms.author: jswymer
ms.openlocfilehash: 29cfec8ea605209aed7e7005dfcfa1c10d54b7b6
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2022
ms.locfileid: "8141412"
---
# <a name="get-the-business-central-add-in-for-excel"></a>Sækja innbót Business Central fyrir Excel

[!INCLUDE[prod_short](includes/prod_short.md)] inniheldur innbót fyrir Excel sem gerir notendum kleift að velja aðgerðina **Breyta í Excel** á ákveðnum síðum til að opna gögnin í Excel-vinnublaði. Þessi aðgerð er öðruvísi en aðgerðin **Opna í Excel** vegna þess að hún gerir notendum kleift að gera breytingar í Excel og birta síðan breytingarnar aftur í[!INCLUDE[prod_short](includes/prod_short.md)]

## <a name="overview"></a>Yfirlit

### <a name="about-the-add-in"></a>Um innbótina

Innbótin er kölluð **Microsoft Dynamics Office-innbót** og hún er í boði til uppsetningar í [Office-versluninni (AppSource)](https://appsource.microsoft.com/). Með innbótina uppsetta er aðgerðin **Breyta í Excel** í boði á flestum listasíðum og listahlutasíðum í **Deila** tákninu ![Deila síðu í öðru forriti.](media/share-icon.png). Frekari upplýsingar um hvernig nota á viðbótin er að finna í [Skoða og breyta í Excel úr Business Central](across-work-with-excel.md).

> [!NOTE]
> Innbótin virkar aðeins í Windows; ekki macOS.

### <a name="about-deployment-as-an-admin"></a>Um uppsetningu sem stjórnandi

Með [!INCLUDE[prod_short](includes/prod_short.md)] á netinu eru nokkrir uppsetningarmöguleikar til að fá innbótina fyrir notendur. Einn valkostur er *einstaklingsbundið* þar sem þú leyfir notendum að setja innbótina upp. Með þessum valkosti verða notendur að hafa aðgang að niðurhali skráa úr Office-versluninni. Annar valkostur er að setja upp *Miðlæga dreifingu* í Microsoft 365 stjórnendamiðstöðinni til að virkja sjálfkrafa viðbótina í allt fyrirtækið, hópana eða tiltekna notendur. Miðlæg innleiðing býður upp á leið til að ná í innbótina fyrir notendur ef fyrirtækið þitt veitir notendum ekki aðgang að Office-versluninni.

Fyrir notandann er uppsetningin öðruvísi fyrir uppsetningarleiðirnar tvær:

- Með einstaklingsbundinni uppsetningu velur nýr notandi aðgerðina **Breyta í Excel**, glugginn **Ný Office-innbót** opnast í Excel. Til að setja upp innbótina velur notandinn **Treysta þessari innbót** sem mun fyrir vikið setja upp innbótina beint úr Office-versluninni. Notendur skrá sig síðan inn í [!INCLUDE[prod_short](includes/prod_short.md)] með notandanafni og lykilorði.

- Með miðlægri innleiðingu velur nýr notandi aðgerðina **Breyta í Excel**, innbótin verður sjálfkrafa sett upp í Excel úr miðlægri innleiðingu; ekki Office-verslun. Það eina sem notendur þurfa að gera er að skrá sig inn til að[!INCLUDE[prod_short](includes/prod_short.md)]

Með báðum þessum virkjunarvalkostum er viðbótin sjálfkrafa skilgreind til að [!INCLUDE[prod_short](includes/prod_short.md)] tengjast . Þriðji dreifingarvalkosturinn er handvirk uppsetning á viðbótinni beint úr Excel. Með þessum valkosti þurfa notendur að stilla viðbótina til að tengjast[!INCLUDE[prod_short](includes/prod_short.md)]

### <a name="switching-from-individual-acquisition-to-centralized-deployment-or-the-other-way-around"></a><a name="switch"></a>Skipt úr einstaklingsbundinni uppsetningu í miðlæga innleiðingu eða öfugt

Þegar breytt er úr einstaklingsbundinni uppsetningu innbótar í miðlæga innleiðingu eða öfugt, verða Excel-skrár sem notendur bjuggu til á undan umbreytingunni fyrir áhrifum. Eftir umbreytinguna geta notendur enn opnað hvaða Excel-vinnublað sem er sem var áður búið til með því að nota aðgerðina **Breyta í Excel** eða búið til handvirkt með því að stilla Excel-innbótina. En þeir geta ekki uppfært gögnin í skránni úr Business Central eða ýtt á uppfærslur í Business Central

Þetta ástand stafar af því að hverri Excel-skrá er úthlutað auðkenni „innbótar“. Þegar skipt er yfir í eða úr miðstýrðri innleiðingu er úthlutað öðru auðkenni þannig að eldra auðkennið er útilokað.

## <a name="preparation-on-premises-only"></a>Undirbúningur (aðeins á staðnum)

[!INCLUDE[prod_short](includes/prod_short.md)] á staðnum krefst þess að umhverfið þitt sé stillt fyrir innbótina. Ef svo er ekki verður aðgerðin **Breyta í Excel** ekki tiltæk notendum. Frekari upplýsingar er að finna í [Uppsetning Excel-innbótar fyrir breytingu á gögnum Business Central](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin) í hjálparefni þróunaraðila og upplýsingatækni.

## <a name="deploy-the-add-in-by-using-centralized-deployment"></a>Setja upp innbótina með miðlægri innleiðingu

Miðlæg dreifing er eiginleiki í Microsoft 365 stjórnunarmiðstöð sem þú notar til að setja sjálfkrafa upp viðbætur í Office-forritum notenda, eins og Excel. Til að hjálpa þér með miðlæga innleiðingu inniheldur [!INCLUDE[prod_short](includes/prod_short.md)] hjálparuppsetninguna **Miðlæg innleiðing Excel-innbótar**.

### <a name="before-you-begin"></a>Áður en hafist er handa

- Frekari upplýsingar um að koma í veg fyrir að notendur sæki úr Office-versluninni er að finna í [Stjórna innbótum í stjórnendamiðstöðinni](/microsoft-365/admin/manage/manage-addins-in-the-admin-center).
- Gakktu úr skugga um að miðlæg innleiðing muni virka fyrir fyrirtækið þitt. Frekari upplýsingar er að finna í [Skera úr um hvort miðlæg innleiðing innbóta virki fyrir fyrirtækið þitt](/microsoft-365/admin/manage/centralized-deployment-of-add-ins)
- Ef þú ert að skipta úr einstaklingsbundinni uppsetningu skaltu skoða [Skipta úr einstaklingsbundinni uppsetningu í miðlæga innleiðingu](#switch)

> [!NOTE]
> Virkjun miðlægrar innleiðingar hefur áhrif á eiginleika sem nota Excel-innbótina, svo sem aðgerðina **Breyta í Excel**. Það hefur engin áhrif á aðra Excel-tengda eiginleika og eða heimildir sem notendum er úthlutað í[!INCLUDE[prod_short](includes/prod_short.md)]

### <a name="set-up-centralized-deployment-of-the-add-in"></a>Setja upp miðlæga innleiðingu innbótarinnar

Þú munt vinna bæði í [!INCLUDE[prod_short](includes/prod_short.md)] stjórnstöðinni Microsoft 365.

1. Í [!INCLUDE[prod_short](includes/prod_short.md)] skal velja ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") færa inn **Miðlæg innleiðing Excel-innbótar**, síðan velja viðkomandi tengil.
2. Lestu upplýsingarnar á síðunni **Uppsetning Excel-innbótar í Business Central** og veldu **Næsta**.
3. Skráðu þig inn í stjórnendamiðstöðina [Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2163967) og farðu **í Integrated Apps**<!--**Add-ins**-->.

    Ljúktu eftirfarandi skrefum til að skilgreina innbótina sem á að setja upp úr Office-verslun: 
    1. Veldu **Sækja forrit** til að opna Office-verslun (AppSource). <!--**Deploy Add-in** 5. In the **Deploy a new add-in**, select **Choose from the store**.-->
    2. Leitaðu að **Microsoft Dynamics Office-innbót** og veldu síðan **Sækja núna**. <!--On the **Select add-in** page, search for and select **Microsoft Dynamics Office Add-in** > **Add** > **Continue**.-->
    3. Á síðunni **Bæta við notendum** skal tilgreina notendurna sem ætlunin er að setja upp innbótina fyrir, veldu síðan **Næsta**.<!--On the **Configure add-in**, specify the users that you want to deploy the add-in for.-->
    4. Farðu yfir **Samþykkja heimildarbeiðnir**, veldu síðan **Næsta** > **Ljúka uppsetningu**.
    5. Bíddu eftir græna gátmerkið við hliðina á **Uppsett** birtist fyrir innbótina, veldu síðan **Lokið**. <!--Select **Deploy** and wait til successful, then **Next** > **Continue**.-->

       Innbótin birtist á síðunni **Innbætur**. Frekari upplýsingar um virkjun innbætur í Microsoft 365 admin center er að finna [í Dreifa viðbótum í admin center](/microsoft-365/admin/manage/manage-deployment-of-add-in).
4. Fara aftur **í Uppsetningu með hjálp** Excel-í miðstýrðri virkjun[!INCLUDE[prod_short](includes/prod_short.md)] og veldu **Next**.
5. Kveiktu á **Nota miðstýrða innleiðingu** og veldu **Ljúka**.

    Ef þú kveikir ekki á þessum rofa sækir [!INCLUDE[prod_short](includes/prod_short.md)] innbótina beint úr Office-versluninni.

Þegar því er lokið er alltaf hægt að breyta virkjuninni í Microsoft 365 stjórnendamiðstöð, eins og að úthluta fleiri notendum. Frekari upplýsingar um uppsetningu innbóta í stjórnendamiðstöðinni er að finna í [Setja upp innbætur í stjórnendamiðstöðinni](/microsoft-365/admin/manage/manage-deployment-of-add-in).

> [!IMPORTANT]
> Ef þú ert með fleiri en eitt umhverfi þarf að keyra hjálparuppsetninguna **Miðlæg innleiðing Excel-innbótar** í hverju umhverfi þar sem þú vilt nota miðlæga innleiðingu. Hins vegar þarftu ekki að samskipa Miðlægri virkjun aftur Microsoft 365. Það eina sem þú þarft að gera er að kveikja á rofanum **Nota miðstýrða innleiðingu** í uppsetningu með hjálp. 

> [!NOTE]
> Allt að sólarhringur getur liðið áður en innbótin er sett upp sjálfkrafa í Excel fyrir notendur.

## <a name="individual-acquisition-install-the-add-in-manually-for-your-own-use"></a><a name="install"></a>Einstaklingsbundin uppsetning: Setja upp innbótina handvirkt til eigin nota

Í flestum tilfellum þegar þú opnar Excel úr Business Central verður innbótin annaðhvort sett upp sjálfkrafa fyrir þig eða beðið verður um að þú setjir hana upp. Hinsvegar geta komið upp tilfelli þar sem þú þarft að setja innbótina upp handvirkt.

1. Opnaðu Excel og opnaðu svo hvaða Excel-vinnubók sem er.
2. Í valmyndinni **Setja inn** skal velja **Innbætur** > **Sækja innbætur**
3. Farðu í **Stýrt af stjórnanda** og leitaðu að **Microsoft Dynamics Office-innbót**. Ef þú sérð hana þar skaltu velja hana og síðan velja **Bæta við**. Ef þú sérð hana ekki skaltu fara í **Verslun** og leita að *Microsoft Dynamics Office-innbót* og fylgja leiðbeiningunum á skjánum til að bæta henni við.

Þegar innbótin er sett upp er hún sýnd sem gluggi í Excel. Næst skal stilla tenginguna.

### <a name="configure-the-business-central-connection"></a>Skilgreina tengingu Business Central

Ef notandi getur ekki tengst sjálfkrafa geturðu opnað fyrir hann með því að biðja hann um að fylgja þessum skrefum:

1. Í innbótasvæðinu **Microsoft Dynamics** í Excel skal velja **Bæta við upplýsingum um þjón**. Ef þú sérð það ekki skaltu velja ![Fleiri valhnappar í Excel.](media/cogwheel.png) táknið efst til að opna svarglugga valmöguleika. 
2. Fyrir [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum skal stilla **Vefslóð þjóns** á `https://exceladdinprovider.smb.dynamics.com`. Fyrir [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum skal stilla vefslóðina á vefslóð vefbiðlarans, t.d. `https://myBCserver/190`.
3. Veldu **Í lagi** og staðfestu síðan að forritið endurhlaðist.
4. Þegar beðið er um það skaltu skrá þig inn með notandanafni og aðgangsorði Business Central.
5. Þú mátt velja umhverfið og fyrirtækið sem þú vilt tengjast við.

Viðbótin er nú tengd við og hægt er að [!INCLUDE [prod_short](includes/prod_short.md)] breyta gögnum og birta breytingarnar [!INCLUDE [prod_short](includes/prod_short.md)] á.  

## <a name="prepare-devices-and-network-for-the-excel-add-in"></a>Undirbúa tæki og netkerfi fyrir Excel-innbótina

Netþjónustur eins og staðgenglar eða eldveggir verða að leyfa flutning milli tækja biðlara þar sem innbótin er sett upp í og margar endastöðvar þjónustu. Lista yfir endastöðvar er að finna í [Undirbúa netkerfið undir Excel-innbótina](/dynamics365/business-central/dev-itpro/administration/configuring-network-for-addins).

## <a name="troubleshooting"></a>Úrræðaleit

Stundum lenda notendur í vandræðum með Excel-innbótina. Þessi hluti gefur upp ábendingar um hvernig á að opna fyrir notendur við ákveðnar aðstæður.

|Gefa út  |Lausn eða hjáleið  |Athugasemdir  |
|---------|---------|---------|
|Viðbótin ræsist ekki|Athugaðu hvort innbótin sé sett upp miðlægt. Eða athugaðu hvort notandi er útilokaður frá því að setja hana upp á staðnum. | Stjórnandinn getur stillt Office þannig að notendur geti ekki sótt innbætur. Í þeim tilvikum verður stjórnandi að setja innbótina upp miðlægt. Frekari upplýsingar er að finna í [Setja upp innbætur í stjórnendamiðstöðinni](/microsoft-365/admin/manage/manage-deployment-of-add-ins?view=o365-worldwide&preserve-view=true).|
|Gögn hlaðast ekki inn í Excel|Prófaðu tenginguna með því að opna annan lista í Excel úr [!INCLUDE [prod_short](includes/prod_short.md)]. Eða opnaðu vinnubókina í Excel í vafra.|Ef notandinn hefur tilgreint heiti fyrirtækis sem inniheldur sérstafi getur innbótin ekki tengst. |
|Gögn geta ekki birt aftur í [!INCLUDE [prod_short](includes/prod_short.md)].|Prófaðu tenginguna með því að opna vinnubókina í Excel í vafra. |Stundum getur viðbótin lokað fyrir birtingarverk. Ef síðan er stækkuð eða sérstillt skal fjarlægja viðbæturnar og reyna síðan aftur.|
|Dagsetningarnar eru rangar  |Excel gæti sýnt tíma og dagsetningar með öðru sniði en [!INCLUDE [prod_short](includes/prod_short.md)]. Þetta ástand gerir þeim ekki rangt og gögnin í [!INCLUDE [prod_short](includes/prod_short.md)] verða ekki rugluð.|         |
|Fyrir sumar listasíður koma upp stöðugar villlur þegar mörgum línum er breytt í Excel. Þetta skilyrði getur komið upp ef OData-köll fela í sér Flowfield og reiti utan stýringar á endurtekningu.|Á síðunni **Vefþjónustur** skal velja gátreitina **Útiloka óbreytanlegt Flowfields** og **Útiloka reiti utan við endurtekningu** fyrir birta síðu. Með því að velja þessa gátreiti er óbreytanlegu Flowfields og reitnum úr eTag-útreikningnum útilokað. |Þessi gátreitir eru sjálfgefið faldir. Til að sýna síðuna **Vefþjónustur** skal nota [sérstillingu](/dynamics365/business-central/ui-personalization-user). |



<!--
## Deploy the Excel add-in for Business Central online

For [!INCLUDE [prod_short](includes/prod_short.md)] online, the administrator can deploy the add-in for all users. But users can also install the add-in themselves, provided they have permission to configure their Office experience.  

> [!TIP]
> In some organizations, administrators cannot deploy add-ins centrally. For more information, see [Determine if Centralized Deployment of add-ins works for your organization](/microsoft-365/admin/manage/centralized-deployment-of-add-ins?view=o365-worldwide&preserve-view=true).

### To deploy the Excel add-in for all users

1. As the administrator, sign in to the Microsoft commercial website and find the add-in at [https://appsource.microsoft.com/product/office/WA104379629](https://appsource.microsoft.com/product/office/WA104379629).
2. Choose the **Get it now** button.

    You'll be redirected to the Microsoft 365 admin center.
3. In the left panel, go to **Settings**, and then choose **Add-ins**.
4. In the **Configure add-in** pane, specify which users to grant access to the add-in.
5. Save your changes.


### To add the Excel add-in locally

1. Open Excel, and then open any Excel workbook.
2. On the **Insert** menu, choose **Office Add-ins**, and then choose **Admin managed** or **Store** as appropriate.
3. Search for *Dynamics Office Add-In*, and then install the add-in.

When the add-in is installed, it shows up as a panel in Excel. Next, you must configure the connection.

> [!TIP]
> If the workbook is not automatically saved to the user's OneDrive, then recommend them to save all workbooks that they export from [!INCLUDE [prod_short](includes/prod_short.md)].When they open the workbook again, the connection is still available, so they do not have to configure the connection again.

> [!NOTE]
> In certain deployments, the administrator must configure network access to unblock the Excel add-in. For more information, see [Preparing Your Network for the Excel Add-In](configuring-network-for-addins.md).-->

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig

[Greina fjárhagsskýrslur í Microsoft Excel](finance-analyze-excel.md)  
[Unnið með Business Central](ui-work-product.md)  
[Endurbætur á Excel-samþættingu í 2019 útgáfu 2](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]