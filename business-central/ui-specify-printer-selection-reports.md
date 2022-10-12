---
title: Uppsetning prentara
description: Nánar um uppsetningu á prenturum fyrir skýrslur og skjöl og mismunandi prentmöguleika sem eru í boði miðsvæðis.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online printing, email printing, cloud printing, Universal Print
ms.search.form: 2650, 2750, 2752, 2753, 2754, 8900,
ms.date: 09/22/2022
ms.author: jswymer
ms.openlocfilehash: 07cda9c796a08436dc48d623f64fcc1252305a14
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9607743"
---
# <a name="set-up-printers"></a>Setja upp prentara

Að prenta skjöl og skýrslur úr [!INCLUDE[prod_short](includes/prod_short.md)] er mikilvægt verk fyrir fyrirtækjanotendur. Vanalega er ætlunin að senda prentverk beint í einn prentara &mdash; fyrirtækisins sama hvaða [!INCLUDE[prod_short](includes/prod_short.md)] biðlara eða forrit er verið að nota. Þar [!INCLUDE[prod_short](includes/prod_short.md)] sem á netinu er skýþjónusta getur hún ekki beint náð í staðbundna prentara sem tengdir eru við tæki notenda, en hægt er að tengja hann við skýrendar-prentara.

Til að styðja við prentþarfirnar býður [!INCLUDE[prod_short](includes/prod_short.md)] upp á eftirfarandi eiginleika:

|Sérkenni|Description|Vefbiðlari| Fartækjaforrit|Forrit fyrir Teams|
|-------|-----------|----------|-----------|--------------|
|Skýjaprentun|Skýjaprentun er prentstjórnunarlausn sem er í boði sem skýjaþjónusta frá Microsoft. Með þessum eiginleika er hægt að setja upp prentara í skýjaprentun, síðan skrá þá til að nota í [!INCLUDE[prod_short](includes/prod_short.md)]. Þessi eiginleiki krefst alhliða prentáskriftar og Framlengingar á **Universal PRINT Samþættingarlausnir**|![vinnur á netinu.](media/check.png)|![vinnur á netinu.](media/check.png)|![vinnur á netinu](media/check.png)|
|Tölvupóstprentun|Þessi eiginleiki gerir kleift að setja upp tölvupóstsprentara. [!INCLUDE[prod_short](includes/prod_short.md)] sendir þá prentverk til prentara með netfangi prentarans. Þessi eiginleiki krefst netfangaprentara og viðbótarinnar **Senda á tölvupóstsprentara**.|![vinnur á netinu.](media/check.png)|![vinnur á netinu](media/check.png)|![vinnur á netinu](media/check.png)|
|Prentun í vafra|Prentvirkni í vafra notandans sér um prentverk. Ef skýjaprentari er ekki uppsettur, eða ef uppsettur prentari mistekst, verða prentvalkostir vafrans sjálfgefið valdir. Reiturinn **Prentari** á síðu skýrslubeiðni sýnir *(Vafri sér um prentun)*.|![vinnur á netinu](media/check.png)|||

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] styður aðra sérsniðna prentaraviðbætur sem bæta við enn fleiri prenthlögun. Svo ef þú ert með einhverja sérsniðna prentaraviðbætur uppsetta getur beiting þín falið í sér prenteiginleika sem ekki er lýst í þessari grein. 

## <a name="set-up-universal-print"></a>Setja upp skýjaprentun

Universal PRINT er Microsoft 365 áskriftarþjónusta sem keyrir alfarið á Microsoft Azure. Hún býður upp á miðstýrða prentstjórnun í gegnum gátt skýjaprentunar. [!INCLUDE[prod_short](includes/prod_short.md)] gerir uppsetningu prentara í skýjaprentun tiltæka biðlurum í gegnum viðbótina **Samþætting skýjaprentunar**.

![Uppsetning skýjaprentunar.](media/Universal-Print-arch.png)

Heildaruppsetningin krefst þess að unnið sé bæði í Microsoft Azure, með [Azure-gáttinni](https://portal.azure.com), og í [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="supported-printers"></a>Studdir prentarar

[!INCLUDE[prod_short](includes/prod_short.md)] styður sömu prentara og skýjaprentun sem geta verið samhæfir skýjaprentun eða ekki. Ósamhæfðir prentarar geta ekki átt samskipti við skýjaprentun með beinum hætti, þannig að þeir þurfa á aukahugbúnaði fyrir tenginguna sem skýjaprentunin býður upp á. Ekki er allir eldri prentarar studdir. 

<!-- TODO If not installed, go to AppSource -->

### <a name="prerequisites"></a>Frumskilyrði

**Fyrir [!INCLUDE[prod_short](includes/prod_short.md)]**

- [!INCLUDE[prod_short](includes/prod_short.md)] 2021 losun bylgjupappa 1 eða nýrri.
- **Universal PRINT Integration** framlenging er uppsett.

    Þessi viðbót er sjálfgefið gefin út og uppsett sem hluti af [!INCLUDE[prod_short](includes/prod_short.md)] á netinu og á staðnum. Hægt er að staðfesta hvort hún er sett upp á síðunni **Viðbótastjórnun**. Frekari upplýsingar er að [Setja upp og fjarlægja viðauka í Viðskiptamiðinu](ui-extensions-install-uninstall.md).

- [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum:
  - Azure Active Directory(AD) eða Navuserlykilsannvottun er samskipað.
  - Umsókn um rekstur miðsvæðis er skráð í þinn Azure AD leigjandi og [!INCLUDE[prod_short](includes/prod_short.md)].

      Eins og aðrar Azure þjónustur sem vinna með [!INCLUDE[prod_short](includes/prod_short.md)], Universal PRINT þarf App skráningu fyrir [!INCLUDE[prod_short](includes/prod_short.md)] inn Azure AD. Forritsskráningin býður upp á sannvottun og heimildarþjónusta milli [!INCLUDE[prod_short](includes/prod_short.md)] og Skýjaprentunar.

      Innleiðing þín getur þegar notað App skráning fyrir aðra Azure þjónustu eins og Power BI. Ef svo er skal líka nota núverandi forritsskráningu fyrir skýjaprentun í stað þess að bæta nýrri við. Það eina sem þarf að gera í þessu tilfelli er að laga forritsskráninguna þannig að hún taki með tilheyrandi prentheimildir fyrir Microsoft Graph API.

      Til að skrá app og setja inn réttar heimildir skaltu fylgja skrefunum sem lýst er í [skrá umsókn í Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory).

**Fyrir skýjaprentun**

- Áskrift/leyfi skýjaprentunar fyrir fyrirtækið.

    Frekari upplýsingar í [leyfi Universal PRINT](/universal-print/fundamentals/universal-print-license).

- Þú ert með hlutverkin **Prentarastjórnun** og **Altækur stjórnandi** í Azure.

    Til að stjórna skýjaprentun verður reikningurinn þinn að vera með hlutverkin **Prentarastjórnun** og **Altækur stjórnandi** í Azure AD. Þessi hlutverk eru aðeins nauðsynleg til að stjórna skýjaprentun. Þeir eru ekki nauðsynlegir þeim sem nota prentarana frá [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="set-up-universal-print-and-add-printers-in-microsoft-azure"></a>Setja upp skýjaprentun og bæta við prenturum í Microsoft Azure

Áður en þú getur byrjað að stjórna Universal PRINT prentarar í Business Central, eru nokkur verkefni sem þú þarft að fara í gegnum til að fá Universal PRINT upp og keyra í Azure með þeim prenturum sem þú vilt nota.

Ítarlegar leiðbeiningar um hvernig uppsetningin fer fram er að finna í [Hafist handa: Setja upp skýjaprentun](/universal-print/fundamentals/universal-print-getting-started) í fylgigögnum skýjaprentunar. Hér er yfirlit yfir skrefin sem þú þarft að ljúka. Flest þessara skrefa eru unnin í Azure-gáttinni.

1. Úthlutaðu leyfum skýjaprentunar á þig og aðra notendur.

    Hvernig leyfunum er úthlutað fer eftir því hvort verið er að samþætta við Business Central Online eða á staðnum.

    - Með [!INCLUDE[prod_short](includes/prod_short.md)] netinu er leyfum Microsoft 365 úthlutað með admin Center.

      Frekari upplýsingar er að fá í Hjálp í [Microsoft admin Center-úthluta leyfum til notenda](/microsoft-365/admin/manage/assign-licenses-to-users).

    - Með [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum er leyfum úthlutað í Azure-leigjandanum með Azure-gáttinni.

      [Frekari upplýsingar er Azure Active Directory að fá í Azure Directory-úthluta eða fjarlægja leyfi í gáttinni](/azure/active-directory/fundamentals/license-users-groups).

2. Setjið upp tengil skýjaprentunar til að skrá prentara sem geta ekki átt bein samskipti við skýjaprentun.

    Flestir í markuprenturum geta ekki haft samskipti við Universal PRINT beint, þannig að þú munt þurfa að setja upp Universal PRINT Connector. Frekari upplýsingar við [uppsetningu á Universal PRINT Connector](/universal-print/fundamentals/universal-print-connector-installation).

3. Skráið prentarana í skýjaprentun.

    Ef prentari er skráður gerir Universal prentari grein fyrir prentaranum.

    - Fyrir prentara sem geta átt bein samskipti við skýjaprentun skal fylgja skrefunum sem framleiðandi prentarans gefur upp.

    - Fyrir aðra prentara skal skrá prentarana með því að nota tengil skýjaprentunar. 

      Frekari upplýsingar við [skráningu](/universal-print/fundamentals/universal-print-connector-printer-registration) prentara.

4. Breyta eiginleikum prentara (valfrjálst)

    Þegar prentari er skráður er hægt að skoða og breyta eiginleikum prentara, svo sem sjálfgefnum stillingum.

    Frekari upplýsingar í [Umsjón með prentarastillingum með Universal PRINT Portal](/universal-print/portal/configure-printer-settings).

5. Deilið prenturunum.

    Alla prentara sem nota á í [!INCLUDE[prod_short](includes/prod_short.md)] mun þarf að samnýta í Universal print.

    <!--Learn more at [Share a Printer](/universal-print/fundamentals/universal-print-printer-permissions#share-a-printer). -->

    [Frekari upplýsingar er að samnýta með prentara](/universal-print/portal/share-printers).

6. Veita notendum heimild fyrir samnýtta prentara.

    <!--Learn more at [Printer Permissions](/universal-print/fundamentals/universal-print-printer-permissions#printer-permissions).-->

    Frekari upplýsingar í [prentrekilsheimildum](/universal-print/portal/share-printers#configure-user-permissions-for-a-printer-share).


7. Virkja umbreytingu skjals.

    Skýjaprentun breytir efni fyrir prentun yfir á XPS-snið. Sumir eldri prentarar á markaðnum styðja ekki breytingu yfir í XPS-efni&mdash;í mörgum tilfellum, aðeins PDF-snið. Prentun á þessum prenturum mistekst nema skýjaprentun sé sett upp til að umbreyta skjölum í snið sem prentari styður.

    Frekari upplýsingar á yfirliti [um breytingu á](/universal-print/portal/document-conversion) skjali.

Nú er verið að undirbúa að bæta prenturum við [!INCLUDE[prod_short](includes/prod_short.md)], setja upp sjálfgefna prentara fyrir skýrslur og prenta.  

### <a name="add-universal-print-printers-to-business-central"></a>Bæta við Universal PRINT prenturum yfir í Business Central

Eftir að prentarar eru settir upp og miðlað í Universal PRINT Ertu tilbúinn að bæta þeim við miðsvæðis í viðskiptum fyrir notkun. Til eru tvær leiðir til að bæta við prenturum skýjaprentunar. Hægt er að bæta öllum prenturum við í einu eða einum í einu.

Þegar bæta á við prenturum sérstaklega skulum við setja upp sama Universal PRINT prentarann í Business Central oftar en einu sinni. Því næst er hægt að breyta prentstillingum fyrir hvern viðbættan prentara, eins og pappírsbakki, stærð og stefnu. Þannig er hægt að setja upp prentara fyrir mismunandi skýrslur og skjöl með sérstökum frálagsþörfum.
  
<!-- To Do Adding printers individually lets you duplicate printers with custom , like different paper trays and paper size and orientation.  To add printers individually, you'll need to know printer's share name in Universal Print. -->

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **prentarastjórnun** og velja síðan tengda tengilinn.
2. Veldu **Universal PRINT** og veldu svo einn af eftirfarandi valkostum:

    - **Bæta öllum Universal prenturum** við til að bæta öllum prenturum ekki þegar við. Hægt er að nota þennan valkost jafnvel þótt búið sé að bæta prentara við. 

    - **Bæta við prentara Skýjaprentunar** til að bæta við sérstökum prentara.  
3. Fylgdu leiðbeiningunum á skjánum.

    - Ef valið var **Bæta við öllum prenturum Skýjaprentunar** hefst uppsetningin **Bæta við prenturum Skýjaprentunar**. <!--This setup leads you through the process of verifying your Azure AD setup (for on-premises), checking your Universal Print license, and then finally adding the printers.-->

    - Ef valið var að **Bæta við prentara Skýjaprentunar** birtist síðan **Stillingar skýjaprentunar**. **Reiturinn Name** er fylltur út og síðan er valið **...** við hliðina **á prenthluta í Universal PRINT** Field til að velja Universal PRINT prentarann. Fyllið út eftirstandandi reiti eftir því sem þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
  
    Þessar aðgerðir sannprófa Azure AD uppsetninguna (fyrir innanhúss), Kannaðu alhliða prentleyfi og bættu svo loks við prentarunum.

    > [!NOTE]
    > Fyrir á staðnum, ef þetta er fyrsta skipti sem tengst er við skýjaprentun, birtist síðan AZURE ACTIVE DIRECTORY SERVICE PERMISSIONS og óskað verður eftir samþykki fyrir Azure-þjónustunni. Þú þarft aðeins að gefa samþykki einu sinni.

Eftir að prentara hefur verið bætt við er hægt að skoða og breyta stillingum hennar af **síðunni prentarastjórnun**. Veldu prentarann og veldu síðan **Breyta stillingum prentara**. 

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

- You have not been assigned an UP license
- You have not been given access to the printer in UP.
- (On-premises) The app registration has been broken.
-->
## <a name="set-up-email-print"></a>Setja upp tölvupóstsprentun

### <a name="prerequisites"></a>Frumskilyrði

- [!INCLUDE[prod_short](includes/prod_short.md)]2020 útgáfutímabil 1 eða nýrra
- Viðbótin **Senda á tölvupóstsprentara** er uppsett

    Þessi viðbót er uppsett sjálfgefið Frekari upplýsingar um uppsetningu viðauka er að finna í<!--see what?--> 
- Tölvupóstvirkni er sett upp.

   Frekari upplýsingar er að setja upp í [tölvupósti](admin-how-setup-email.md).

### <a name="add-an-email-printer"></a>Bæta við tölvupóstprentara

Á **síðunni prentarastjórnun** birtast prentararnir sem nú eru settir upp. Síðan gerir þér einnig kleift að komast á **síðuna stillingar** fyrir hvern prentara til að breyta fyrirliggjandi uppsetningu eða setja upp nýjan prentara.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **prentarastjórnun** og velja síðan tengda tengilinn.
2. Veldu **email PRINT**, Veldu svo **Add tölvupóst prentara**.
3. Á síðunni **Stillingar tölvupóstsprentara** skal fylla út reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > Velja verður viðeigandi pappírsstærð handvirkt fyrir prentara þar sem enginn staðbundinn prentari eða notandastillingar geta verið geymdir.
    >
    > Hafið í huga að viðbót tölvupóstsprentara er sjálfgefið stillt á pappírsstærð **A4**, sem er til dæmis ekki hentugt í Norður-Ameríku.

### <a name="privacy-notice"></a>Tilkynning um persónuvernd

Ef notaður er prentaraframlenging eru öll eða einhver prentverk send á netfangið sem samskipað er fyrir prentarann. Við mælum eindregið með því að einkvæmt tölvupóstskenni sé tengt við prenttæki með því að nota aðeins opinbera þjónustu sem framleiðandi vélbúnaðar veitir, svo sem HP ePrint, KonicaMinolta EveryonePrint eða Epson Email Print.

Nauðsynlegt er að gera allar nauðsynlegar persónuverndarráðstafanir, þar á meðal að tryggja að prentlausnin fyrir tölvupóst hafi rétt skilgreindar heimildir, persónuverndarstillingar og varðveislureglur. Það er á ábyrgð notanda að gefa upp rétt, staðfest og starfhæft netfang. Frekari upplýsingar í yfirlýsingu [Microsoft um](https://privacy.microsoft.com/privacystatement) persónuvernd.

## <a name="set-up-default-printers"></a><a name="default"></a>Setja upp sjálfgefna prentara

Það eru tvær leiðir til að setja prentara upp til að nota sjálfgefið fyrir prentverk. Sjálfgefinn prentari er gagnlegur ef unnið er með mismunandi skýrslur sem krefjast mismunandi prentara vegna staðsetningar þeirra í fyrirtækinu eða útprentunarmöguleika.

### <a name="set-a-printer-as-a-default-printer-for-all-print-jobs"></a>Stilla prentara sem sjálfgefinn prentara fyrir öll prentverk

**Í gegnum prentarastjórnunarsíðuna** er Prentari settur upp sem sjálfgefinn prentari fyrir öll prentverk. Hægt er að tilgreina prentarann sem sjálfgefinn fyrir einn notanda eða alla notendur.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **prentarastjórnun** og velja síðan tengda tengilinn.

    > [!TIP]
    > Einnig er hægt að opna síðuna **Prentarastjórnun** af síðunni **Prentaraval** með því að velja **Prentarastjórnun**.  
2. Á síðunni **Prentarastjórnun** skal velja prentara af listanum, velja **Stjórna**, því næsta velja **Stilla sem sjálfgefinn prentara fyrir mig** eða **Stilla sem sjálfgefinn prentara fyrir alla notendur**.

> [!NOTE]
> Stilling sjálfgefins prentara frá **prentarastjórnun** bætir færslu í **Prentaraval**.

### <a name="set-a-default-printer-for-specific-reports"></a>Stilla sjálfgefinn prentara fyrir tilteknar skýrslur

**Síðan Prentaraval** leyfir að tilgreina prentarann verður að nota sjálfgefið í skýrslunni. Sjálfgefnir prentarar eru stilltir á grundvelli notandareiknings. Hægt er að stilla sjálfgefinn prentara fyrir eingöngu sjálfan sig, annan notanda eða alla notendur.

> [!IMPORTANT]
> Fyrir [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum getur síðan **Prentaraval** aðeins verið notuð fyrir prentara í skýinu sem prentaraviðbætur skilgreina, eins og tölvupóstsprentara og prentara skýjaprentunar. Ekki er hægt að nota hana fyrir staðbundna prentara.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teikn, færa inn **Prentaraval** og velja síðan tengda tengilinn. Einnig er hægt að velja prentara á síðunni prentarastjórnun **og velja** síðan aðgerðina Prentaraval **.**
2. Velja skal aðgerðina **Nýtt** til að bæta við prentaravali fyrir tiltekna skýrslu.
3. Fyllið inn reitina eftir þörfum.

Tilgreind skýrsla er nú uppsett til prentunar í völdum sjálfgefnum prentara.

> [!NOTE]
> Þegar skýrslan er prentuð út sem spurning er hægt að velja aðra með því að **nota reitinn prenta** á síðunni skýrslubeiðni.

> [!NOTE]
> Ef ekki er sett skýrsla upp fyrir ákveðinn prentara á **síðunni Prentaraval** er hún prentuð á sjálfgefinn prentara fyrirtækisins, eins og það er skilgreint á **síðunni prentarastjórnun**.

Þú eða stjórnandinn getur einnig notað síðuna **Prentaraval** til að skilgreina önnur afbrigði prentunar fyrir notendur og skýrslur. Í eftirfarandi töflu er samsetning gildanna lýst til að tilgreina mismunandi uppsetningar fyrir skýrslu.

|Til                                                 |Stilla eftirfarandi gildi:                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Prenta skýrslu í tilteknum prentara fyrir alla notendur |Tilgreinið gildi í reitunum **Kenni skýrslu** og **Prentaraheiti** og skiljið reitinn **Kenni notanda** eftir auðan.|
|Prenta allar skýrslur í tilteknum prentara fyrir tiltekinn notanda|Tilgreinið gildi í reitunum **Kenni notanda** og **Prentaraheiti** og skiljið reitinn **Kenni skýrslu** eftir auðan. Þessi færsla gerir það sama og aðgerðin **Stilla sem sjálfgefinn prentara fyrir mig** á síðunni **Prentstýring**.|
|Stilla sjálfgefinn prentara fyrir allar skýrslur fyrir alla notendur|Tilgreinið gildi í reitnum **Prentaraheiti** og skiljið reitina **Kenni notanda** og **Kenni skýrslu** eftir auða. Þessi færsla gerir það sama og aðgerðin **Stilla sem sjálfgefinn prentara fyrir alla notendur** á síðunni **Prentstýring**.|
|Prenta tiltekna skýrslu á sjálfgefnum prentara notanda|Tilgreinið gildi í reitnum **Kenni skýrslu** og skiljið reitina **Prentaraheiti** og **Kenni notanda** eftir auða.|
|Prenta tiltekna skýrslu í tilteknum prentara fyrir tiltekinn notanda|Tilgreinið gildi í öllum þremur reitunum.|

> [!NOTE]
> Fleiri tiltekin Prentaraval taka forgang yfir fleiri almenn Prentaraval. Prentaraval sem hefur til dæmis gildi í reitunum **Notandakenni**, **Skýrslukenni** og **Prentaraheiti** hefur forgang fram yfir prentaraval sem er með auðar færslur í reitunum **Notandakenni** eða **Skýrslukenni**.

### <a name="choosing-the-printer-when-running-a-report"></a>Prentari að velja þegar skýrsla er keyrð

Í stað þess að nota sjálfgefinn prentara þegar skýrsla er keyrð er hægt að hnekkja þessari stillingu af beiðingarsíðunni. Einfaldlega er hægt að velja prentarann sem nota á fyrir þessa Skýrslumyndun í **fellivalmyndinni prentara**.

### <a name="sizing-print-jobs"></a>Vefverk í stærð prentunar

Skýjaprentun er hönnuð fyrir skjöl af hæfilegri stærð. Flestar skýjaþjónustur, þ.m.t. PrintNode og HP ePrint, eru með 10 MB hámark fyrir hvert verk. Ef þú þarft að prenta stærri skýrslur gætirðu þurft að skipta þeim í margar útprentanir.

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/change-documents-dynamics-365-business-central/).

## <a name="see-also"></a>Sjá einnig .

[Prenta skýrslu](ui-work-report.md#PrintReport)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Keyra runuvinnslur](ui-how-run-batch-jobs.md)  
[Senda skjöl í tölvupósti](ui-how-send-documents-email.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
