---
title: Uppsetning prentara
description: Kynntu þér hvernig á að setja upp prentara sem hægt er að nota fyrir skýrslur og skjöl og mismunandi prenteiginleika sem eru í boði í Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online printing, email printing, cloud printing, Universal Print
ms.date: 06/24/2021
ms.author: jswymer
ms.openlocfilehash: e459c854bfba13689b5dc6213ed7e88347780483
ms.sourcegitcommit: 81a35248e6f1e8773339281b6f5c0ebd4942e05a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547049"
---
# <a name="set-up-printers"></a>Setja upp prentara

Að prenta skjöl og skýrslur úr [!INCLUDE[prod_short](includes/prod_short.md)] er mikilvægt verk fyrir fyrirtækjanotendur. Notendur vilja gjarnan senda prentverk beint í einn prentara fyrirtækisins&mdash;sama hvaða [!INCLUDE[prod_short](includes/prod_short.md)] biðlara eða forrit þeir eru að nota. Vegna þess að [!INCLUDE[prod_short](includes/prod_short.md)] á netinu er skýjaþjónusta getur það ekki náð beint til prentara á staðnum sem tengjast tækjum notendum, en það getur tengst við prentara í skýinu.

Til að styðja við prentþarfirnar býður [!INCLUDE[prod_short](includes/prod_short.md)] upp á eftirfarandi eiginleika:

|Sérkenni|Description|Vefbiðlari| Fartækjaforrit|Forrit fyrir Teams|
|-------|-----------|----------|-----------|--------------|
|Skýjaprentun|Skýjaprentun er prentstjórnunarlausn sem er í boði sem skýjaþjónusta frá Microsoft. Með þessum eiginleika er hægt að setja upp prentara í skýjaprentun, síðan skrá þá til að nota í [!INCLUDE[prod_short](includes/prod_short.md)]. Þessi eiginleiki krefst áskriftar að Skýjaprentun og viðbótarinnar **Samþætting skýjaprentunar**|![vinnur á netinu.](media/check.png)|![vinnur á netinu.](media/check.png)|![vinnur á netinu](media/check.png)|
|Tölvupóstprentun|Þessi eiginleiki gerir kleift að setja upp tölvupóstsprentara. [!INCLUDE[prod_short](includes/prod_short.md)] sendir þá prentverk til prentara með netfangi prentarans. Þessi eiginleiki krefst netfangaprentara og viðbótarinnar **Senda á tölvupóstsprentara**.|![vinnur á netinu.](media/check.png)|![vinnur á netinu](media/check.png)|![vinnur á netinu](media/check.png)|
|Prentun í vafra|Prentvirkni í vafra notandans sér um prentverk. Ef skýjaprentari er ekki uppsettur, eða ef uppsettur prentari mistekst, verða prentvalkostir vafrans sjálfgefið valdir. Reiturinn **Prentari** á síðu skýrslubeiðni sýnir *(Vafri sér um prentun)*.|![vinnur á netinu](media/check.png)|||

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] styður einnig sérstilltar prentaraviðbætur til að bæta við enn fleiri prenteiginleikum. Ef sérstilltar prentaraviðbætur eru settar upp gæti forritið verið með prenteiginleika sem ekki er lýst í þessari grein. 

## <a name="set-up-universal-print"></a>Setja upp skýjaprentun

Skýjaprentun er áskriftarþjónusta Microsoft 365 sem keyrir eingöngu á Microsoft Azure. Hún býður upp á miðstýrða prentstjórnun í gegnum gátt skýjaprentunar. [!INCLUDE[prod_short](includes/prod_short.md)] gerir uppsetningu prentara í skýjaprentun tiltæka biðlurum í gegnum viðbótina **Samþætting skýjaprentunar**.

![Uppsetning skýjaprentunar.](media/Universal-Print-arch.png)

Heildaruppsetningin krefst þess að unnið sé bæði í Microsoft Azure, með [Azure-gáttinni](https://portal.azure.com), og í [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="supported-printers"></a>Studdir prentarar

[!INCLUDE[prod_short](includes/prod_short.md)] styður sömu prentara og skýjaprentun sem geta verið samhæfir skýjaprentun eða ekki. Ósamhæfðir prentarar geta ekki átt samskipti við skýjaprentun með beinum hætti, þannig að þeir þurfa á aukahugbúnaði fyrir tenginguna sem skýjaprentunin býður upp á. Ekki er allir eldri prentarar studdir. 

<!-- TODO If not installed, go to AppSource -->

### <a name="prerequisites"></a>Frumskilyrði

**Fyrir [!INCLUDE[prod_short](includes/prod_short.md)]**

- [!INCLUDE[prod_short](includes/prod_short.md)] 2021 útgáfutímabil 1 eða nýrra
- Viðbót **Samþættingar skýjaprentunar** er uppsett

    Þessi viðbót er sjálfgefið gefin út og uppsett sem hluti af [!INCLUDE[prod_short](includes/prod_short.md)] á netinu og á staðnum.  Hægt er að staðfesta hvort hún er sett upp á síðunni **Viðbótastjórnun**. Frekari upplýsingar er að finna í [Uppsetning og fjarlæging viðbóta í Business Central](ui-extensions-install-uninstall.md).
- [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum:
  - Azure Active Directory (AD) eða NavUserPassword-sannvottun er skilgreind
  - Forrit fyrir Business Central er skráð í Azure AD-leigjandanum og [!INCLUDE[prod_short](includes/prod_short.md)]

      Eins og önnur Azure-þjónusta sem vinnur með [!INCLUDE[prod_short](includes/prod_short.md)], krefst Skýjaprentun skráningu forrits fyrir [!INCLUDE[prod_short](includes/prod_short.md)] í Azure Active Directory (Azure AD). Forritsskráningin býður upp á sannvottun og heimildarþjónusta milli [!INCLUDE[prod_short](includes/prod_short.md)] og Skýjaprentunar.

      Uppsetningin þín gæti nú þegar verið að nota forritsskráningu fyrir aðra Azure-þjónustu eins og Power BI. Ef svo er skal líka nota núverandi forritsskráningu fyrir skýjaprentun í stað þess að bæta nýrri við. Það eina sem þarf að gera í þessu tilfelli er að laga forritsskráninguna þannig að hún taki með tilheyrandi prentheimildir fyrir Microsoft Graph API.

      Til að skrá forrit og stilla viðeigandi heimildir skal fylgja skrefunum sem lýst er í [Skrá forrit í Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory).

**Fyrir skýjaprentun**

- Áskrift/leyfi skýjaprentunar fyrir fyrirtækið.

    Frekari upplýsingar er að finna í [Leyfi skýjaprentunar](/universal-print/fundamentals/universal-print-license).

- Þú ert með hlutverkin **Prentarastjórnun** og **Altækur stjórnandi** í Azure.

    Til að stjórna skýjaprentun verður reikningurinn þinn að vera með hlutverkin **Prentarastjórnun** og **Altækur stjórnandi** í Azure AD. Þessi hlutverk eru aðeins nauðsynleg til að stjórna skýjaprentun. Notendur þurfa ekki að nota prentarana úr [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="set-up-universal-print-and-add-printers-in-microsoft-azure"></a>Setja upp skýjaprentun og bæta við prenturum í Microsoft Azure

Áður en hægt er að stjórna prenturum skýjaprentunar í Business Central þarf að fara í gegnum nokkur verk til að koma skýjaprentun í gagnið í Azure með prenturnum sem ætlunin er að nota.

Ítarlegar leiðbeiningar um hvernig uppsetningin fer fram er að finna í [Hafist handa: Setja upp skýjaprentun](/universal-print/fundamentals/universal-print-getting-started) í fylgigögnum skýjaprentunar. Hér er yfirlit yfir skrefin sem þú þarft að ljúka. Flest þessara skrefa eru unnin í Azure-gáttinni.

1. Úthlutaðu leyfum skýjaprentunar á þig og aðra notendur.

    Hvernig leyfunum er úthlutað fer eftir því hvort verið er að samþætta við Business Central Online eða á staðnum.

    - Með [!INCLUDE[prod_short](includes/prod_short.md)] á netinu er leyfum úthlutað með því að nota stjórnendamiðstöð Microsoft 365.

      Frekari upplýsingar er að finna í [Hjálp stjórnendamiðstöðvar Microsoft - Úthluta leyfum á notendur](/microsoft-365/admin/manage/assign-licenses-to-users).

    - Með [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum er leyfum úthlutað í Azure-leigjandanum með Azure-gáttinni.

      Frekari upplýsingar er að finna í [Azure Directory - Úthluta eða fjarlægja leyfi í Azure Active Directory-gáttinni](/azure/active-directory/fundamentals/license-users-groups).

2. Setjið upp tengil skýjaprentunar til að skrá prentara sem geta ekki átt bein samskipti við skýjaprentun.

    Flestir prentarar á markaðnum geta ekki átt bein samskipti við skýjaprentun. Setja þarf upp tengil skýjaprentunar fyrir þessa prentara. Frekari upplýsingar er að finna í [Uppsetning skýjaprentunartengils](/universal-print/fundamentals/universal-print-connector-installation).

3. Skráið prentarana í skýjaprentun.

    Með því að skrá prentara veit skýjaprentun af prentaranum.

    - Fyrir prentara sem geta átt bein samskipti við skýjaprentun skal fylgja skrefunum sem framleiðandi prentarans gefur upp.

    - Fyrir aðra prentara skal skrá prentarana með því að nota tengil skýjaprentunar. 

      Nánari upplýsingar eru í [Skráning prentara](/universal-print/fundamentals/universal-print-connector-printer-registration).

4. Breyta eiginleikum prentara (valfrjálst)

    Þegar prentari hefur verið skráður er hægt að skoða og breyta prentaraeiginleikum á borð við sjálfgefnar kjörstillingar.

    Nánari upplýsingar eru í [Stjórna prentarastillingum með gátt skýjaprentunar](/universal-print/portal/configure-printer-settings).

5. Deilið prenturunum.

    Alla prentara sem á að nota í [!INCLUDE[prod_short](includes/prod_short.md)] verður að deila í skýjaprentun.

    <!--For more information, see [Share a Printer](/universal-print/fundamentals/universal-print-printer-permissions#share-a-printer). -->

    Frekari upplýsingar er að finna í [Deila prentara](/universal-print/portal/share-printers).

6. Veita notendum heimild fyrir samnýtta prentara.

    <!--For more information, see [Printer Permissions](/universal-print/fundamentals/universal-print-printer-permissions#printer-permissions).-->

    Frekari upplýsingar er að finna í [Prentaraheimildir](/universal-print/portal/share-printers#configure-user-permissions-for-a-printer-share).


7. Virkja umbreytingu skjals.

    Skýjaprentun breytir efni fyrir prentun yfir á XPS-snið. Sumir eldri prentarar á markaðnum styðja ekki breytingu yfir í XPS-efni&mdash;í mörgum tilfellum, aðeins PDF-snið. Prentun á þessum prenturum mistekst nema skýjaprentun sé sett upp til að umbreyta skjölum í snið sem prentari styður.

    Frekari upplýsingar er að finna í [Yfirlit skjalaumbreytinga](/universal-print/portal/document-conversion).

Nú er hægt að bæta prenturunum við [!INCLUDE[prod_short](includes/prod_short.md)], setja upp sjálfgefna prentara fyrir skýrslur og prenta.  

### <a name="add-universal-printer-printers-to-business-central"></a>Bæta prenturum skýjaprentunar við Business Central

Þegar prentarar hafa verið settir upp og þeim deilt í skýjaprentun verður hægt að bæta þeim við Business Central til að nota. Til eru tvær leiðir til að bæta við prenturum skýjaprentunar. Hægt er að bæta öllum prenturum við í einu eða einum í einu.

Með því að bæta við einum prentara í einu verður hægt að setja upp sama prentara skýjaprentunar í Business Central oftar en einu sinni. Því næst er hægt að breyta prentstillingum fyrir hvern viðbættan prentara, eins og pappírsbakki, stærð og stefnu. Á þennan hátt er hægt að setja upp prentara fyrir mismunandi skýrslur og skjöl sem eru með sérstakar kröfur um prentunina.
  
<!-- To Do Adding printers individually lets you duplicate printers with custom , like different paper trays and paper size and orientation.  To add printers individually, you'll need to know printer's share name in Universal Print. -->

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Prentarastjórnun** og velja síðan viðkomandi tengil.
2. Veljið **Skýjaprentun** og því næst skal velja einn af eftirfarandi valkostum:

    - **Bæta við öllum prenturum Skýjaprentunar** til að bæta við öllum prenturum sem ekki er búið að bæta við. Hægt er að nota þennan valkost þótt búið sé að bæta við prenturum. 

    - **Bæta við prentara Skýjaprentunar** til að bæta við sérstökum prentara.  
3. Fylgdu leiðbeiningunum á skjánum.

    - Ef valið var **Bæta við öllum prenturum Skýjaprentunar** hefst uppsetningin **Bæta við prenturum Skýjaprentunar**. <!--This setup leads you through the process of verifying your Azure AD setup (for on-premises), checking your Universal Print license, and then finally adding the printers.-->

    - Ef valið var að **Bæta við prentara Skýjaprentunar** birtist síðan **Stillingar skýjaprentunar**. Fyllið út reitinn **Heiti**, veljið því næst **...** við hliðina á reitnum **Samnýttur prentari í Skýjaprentun** til að velja prentara skýjaprentunar. Fyllið út eftirstandandi reiti eftir því sem þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
  
    Þessar aðgerðir staðfesta Azure AD uppsetninguna (fyrir á staðnum), athugar hvort þú sért leyfi skýjaprentunar og að lokum bætir við prenturum.

    > [!NOTE]
    > Fyrir á staðnum, ef þetta er fyrsta skipti sem tengst er við skýjaprentun, birtist síðan AZURE ACTIVE DIRECTORY SERVICE PERMISSIONS og óskað verður eftir samþykki fyrir Azure-þjónustunni. Þú þarft aðeins að gefa samþykki einu sinni.

Eftir að prentara hefur verið bætt við er hægt að skoða og breyta stillingum hans úr **Prentarastjórnun**. Veldu prentarann og veldu síðan **Breyta stillingum prentara**. 

<!--
### Troubleshooting

#### You don't see the a printer in the 

The printer is not shared in Universal Print.

### You get an error when tryong to add all or a single printer

You have'nt been assigned a Uincersla Print license.

There was an error fetching printers shared to you. You don't have access to the data. Make sure your account has been assigned a Universal Print license and you have the required permissions.
or 
You don't seem to have access to Universal Print. Make sure you have a Universal Print subscription, and that your account has been assigned a Universal Print license.

## Could not upload the document to print job 50.

There is a technical problem withe the printer. Unsupported document-format: application/pdf. Supported formats: Attribute document-format-supported: SimpleIppValue-Type:MimeMediaType-Value:application/oxps

## You don't have access to the printer

- You have not been assigned a Up license
- You have not been given access to the printer in UP.
- (On-prem) The app registration has been broken
-->
## <a name="set-up-email-print"></a>Setja upp tölvupóstsprentun

### <a name="prerequisites"></a>Frumskilyrði

- [!INCLUDE[prod_short](includes/prod_short.md)]2020 útgáfutímabil 1 eða nýrra
- Viðbótin **Senda á tölvupóstsprentara** er uppsett

    Þessi viðbót er uppsett sjálfgefið Upplýsingar um uppsetningu viðbóta er að finna í 
- Tölvupóstvirkni er sett upp.

   Frekari upplýsingar eru í [Setja upp tölvupóst](admin-how-setup-email.md).

### <a name="add-an-email-printer"></a>Bæta við tölvupóstprentara

Síðan **Prentarastjórnun** sýnir þér prentarana sem búið er að setja upp. Síðan veitir þér einnig aðgang að síðunni **Stillingar** fyrir hvern prentara fyrir sig til að breyta núverandi uppsetningu eða til að setja upp nýjan prentara.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Prentarastjórnun** og velja síðan viðkomandi tengil.
2. Veldu **Tölvupóstprentun** og veldu síðan **Bæta við tölvupóstprentara**.
3. Á síðunni **Stillingar tölvupóstsprentara** skal fylla út reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > Velja verður viðeigandi pappírsstærð handvirkt fyrir prentara þar sem enginn staðbundinn prentari eða notandastillingar geta verið geymdir.
    >
    > Hafið í huga að viðbót tölvupóstsprentara er sjálfgefið stillt á pappírsstærð **A4**, sem er til dæmis ekki hentugt í Norður-Ameríku.

### <a name="privacy-notice"></a>Persónuverndaryfirlýsing

Ef viðbót tölvupóstsprentara er notuð verða öll eða sum prentverk send á netfangið sem er skilgreint fyrir prentarann. Við mælum eindregið með því að einkvæmt tölvupóstskenni sé tengt við prenttæki með því að nota aðeins opinbera þjónustu sem framleiðandi vélbúnaðar veitir, svo sem HP ePrint, KonicaMinolta EveryonePrint eða Epson Email Print.

Nauðsynlegt er að gera allar nauðsynlegar persónuverndarráðstafanir, þar á meðal að tryggja að prentlausnin fyrir tölvupóst hafi rétt skilgreindar heimildir, persónuverndarstillingar og varðveislureglur. Það er á ábyrgð notanda að gefa upp rétt, staðfest og starfhæft netfang. Frekari upplýsingar er að finna í [Yfirlýsing Microsoft um persónuvernd](https://privacy.microsoft.com/privacystatement).


## <a name="set-up-default-printers"></a><a name="default"></a>Setja upp sjálfgefna prentara

Það eru nokkrar leiðir til að setja upp prentara sem verða sjálfgefið notaðar fyrir prentverk. Sjálfgefinn prentari er gagnlegur ef unnið er með mismunandi skýrslur sem krefjast mismunandi prentara vegna staðsetningar þeirra í fyrirtækinu eða útprentunarmöguleika.

### <a name="set-a-printer-as-a-default-printer-for-all-print-jobs"></a>Stilla prentara sem sjálfgefinn prentara fyrir öll prentverk

Síðan **Prentarastjórnun** gerir kleift að setja upp prentara sem sjálfgefinn prentara fyrir öll prentverk. Hægt er að tilgreina prentarann sem sjálfgefinn fyrir einn notanda eða alla notendur.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Prentarastjórnun** og velja síðan viðkomandi tengil.

    > [!TIP]
    > Einnig er hægt að opna síðuna **Prentarastjórnun** af síðunni **Prentaraval** með því að velja **Prentarastjórnun**.  
2. Á síðunni **Prentarastjórnun** skal velja prentara af listanum, velja **Stjórna**, því næsta velja **Stilla sem sjálfgefinn prentara fyrir mig** eða **Stilla sem sjálfgefinn prentara fyrir alla notendur**.

> [!NOTE]
> Ef sjálfgefnum prentari er stilltur í **Prentarastjórnun** verður færslu bætt við í **Prentaravalinu**.

### <a name="set-a-default-printer-for-specific-reports"></a>Stilla sjálfgefinn prentara fyrir tilteknar skýrslur

Síðan **Prentaraval** gerir kleift að tilgreina prentarann sem skýrsla notar að sjálfgefnu. Sjálfgefnir prentarar eru stilltir á grundvelli notandareiknings. Hægt er að stilla sjálfgefinn prentara fyrir eingöngu sjálfan sig, annan notanda eða alla notendur.

> [!IMPORTANT]
> Fyrir [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum getur síðan **Prentaraval** aðeins verið notuð fyrir prentara í skýinu sem prentaraviðbætur skilgreina, eins og tölvupóstsprentara og prentara skýjaprentunar. Ekki er hægt að nota hana fyrir staðbundna prentara.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Prentaraval** og velja síðan viðkomandi tengil. Í staðinn, á síðunni **Prentarastjórnun**, skal velja prentara og því næst velja aðgerðina **Prentaraval**.
2. Velja skal aðgerðina **Nýtt** til að bæta við prentaravali fyrir tiltekna skýrslu.
3. Fyllið inn reitina eftir þörfum.

Tilgreind skýrsla er nú uppsett til prentunar í völdum sjálfgefnum prentara.

> [!NOTE]
> Þegar skýrslan er prentuð er hægt að velja arða með því að nota reitinn **Prenta** á beiðnisíðunni.

> [!NOTE]
> Ef ekki er sett upp skýrsla fyrir tiltekinn prentara á síðunni **Prentaraval** verður hún prentuð á sjálfgefinn prentara fyrirtækisins, eins og það er skilgreint á síðunni **Prentarastjórnun**.

Þú eða stjórnandinn getur einnig notað síðuna **Prentaraval** til að skilgreina önnur afbrigði prentunar fyrir notendur og skýrslur. Eftirfarandi tafla lýsir samsetningu gilda til að tilgreina mismunandi prentunaruppsetningu fyrir skýrslu.

|Til að                                                 |Stilla eftirfarandi gildi:                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Prenta skýrslu í tilteknum prentara fyrir alla notendur |Tilgreinið gildi í reitunum **Kenni skýrslu** og **Prentaraheiti** og skiljið reitinn **Kenni notanda** eftir auðan.|
|Prenta allar skýrslur í tilteknum prentara fyrir tiltekinn notanda|Tilgreinið gildi í reitunum **Kenni notanda** og **Prentaraheiti** og skiljið reitinn **Kenni skýrslu** eftir auðan. Þessi færsla gerir það sama og aðgerðin **Stilla sem sjálfgefinn prentara fyrir mig** á síðunni **Prentstýring**.|
|Stilla sjálfgefinn prentara fyrir allar skýrslur fyrir alla notendur|Tilgreinið gildi í reitnum **Prentaraheiti** og skiljið reitina **Kenni notanda** og **Kenni skýrslu** eftir auða. Þessi færsla gerir það sama og aðgerðin **Stilla sem sjálfgefinn prentara fyrir alla notendur** á síðunni **Prentstýring**.|
|Prenta tiltekna skýrslu á sjálfgefnum prentara notanda|Tilgreinið gildi í reitnum **Kenni skýrslu** og skiljið reitina **Prentaraheiti** og **Kenni notanda** eftir auða.|
|Prenta tiltekna skýrslu í tilteknum prentara fyrir tiltekinn notanda|Tilgreinið gildi í öllum þremur reitunum.|

> [!NOTE]
> Sértækara prentaraval hefur forgang fram yfir almennara prentaraval. Prentaraval sem hefur til dæmis gildi í reitunum **Notandakenni**, **Skýrslukenni** og **Prentaraheiti** hefur forgang fram yfir prentaraval sem er með auðar færslur í reitunum **Notandakenni** eða **Skýrslukenni**.

### <a name="sizing-print-jobs"></a>Stærð prentverka stillt

Skýjaprentun er hönnuð fyrir skjöl af hæfilegri stærð. Flestar skýjaþjónustur, þ.m.t. PrintNode og HP ePrint, eru með 10 MB hámark fyrir hvert verk. Ef þú þarft að prenta stærri skýrslur gætirðu þurft að skipta þeim í margar útprentanir.

## <a name="see-also"></a>Sjá einnig

[Prenta skýrslu](ui-work-report.md#PrintReport)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Keyra runuvinnslur](ui-how-run-batch-jobs.md)  
[Senda skjöl í tölvupósti](ui-how-send-documents-email.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]