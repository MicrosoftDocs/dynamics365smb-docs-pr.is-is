---
title: Setja upp Universal PRINT prentarar
description: Lærðu hvernig þú getur notað Universal PRINT til að gefa Cloud prentun í Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/26/2023
ms.custom: bap-template
---

# Setja upp Universal PRINT prentarar

Skýjaprentun er áskriftarþjónusta Microsoft 365 sem keyrir eingöngu á Microsoft Azure. Hún býður upp á miðstýrða prentstjórnun í gegnum gátt skýjaprentunar. [!INCLUDE[prod_short](includes/prod_short.md)] gerir uppsetningu prentara í skýjaprentun tiltæka biðlurum í gegnum viðbótina **Samþætting skýjaprentunar**.

![Uppsetning skýjaprentunar.](media/Universal-Print-arch.png)

Heildaruppsetningin krefst þess að unnið sé bæði í Microsoft Azure, með [Azure-gáttinni](https://portal.azure.com), og í [!INCLUDE[prod_short](includes/prod_short.md)]. Uppsetningin skiptist milli tveggja meginverkefna eins og lýst er í þessari grein:

1. Í  Microsoft Azure er sett upp Universal PRINT og bætt við þeim prenturum sem á að nota í viðskiptafræði miðlægt í prentmiðla. Fara í  [þennan kafla](#set-up-universal-print-and-printers-in-microsoft-azure).
2. Inn  [!INCLUDE[prod_short](includes/prod_short.md)], Bættu prenturum úr prenthluta í Universal print. Fara á  [þennan hluta](#add-printers-in-business-central-online)  fyrir á neti eða  [hér](#add-printers-in-business-central-on-premises)  til innanhúss.

## Frumskilyrði

- Studdir prentarar

  [!INCLUDE[prod_short](includes/prod_short.md)] styður sömu prentara og skýjaprentun sem geta verið samhæfir skýjaprentun eða ekki. Ósamhæfðir prentarar geta ekki átt samskipti við skýjaprentun með beinum hætti, þannig að þeir þurfa á aukahugbúnaði fyrir tenginguna sem skýjaprentunin býður upp á. Ekki er allir eldri prentarar studdir. 

- Universal PRINT:

  - Áskrift/leyfi skýjaprentunar fyrir fyrirtækið.

    Frekari upplýsingar er að finna í [Skýjaprentunarleyfi](/universal-print/fundamentals/universal-print-license).

  - Þú átt  **prentarastjórann**  (eða prentarastjórann) og  **alþjóðlegt Hlutverk kerfisstjóra**  í Azure.

    Til að stjórna Universal PRINT verður reikningurinn þinn að hafa  **prentarastjóra**  (eða prentstjórahlutverk  **) og**  altækan stjórnanda Azure AD. Þessi hlutverk eru aðeins nauðsynleg til að stjórna skýjaprentun. Þeir eru ekki nauðsynlegir þeim sem fólk setur upp og prenturum frá [!INCLUDE[prod_short](includes/prod_short.md)].

- [!INCLUDE[prod_short](includes/prod_short.md)] á netinu og innanhúss:

  - [!INCLUDE[prod_short](includes/prod_short.md)] 2021 útgáfutímabil 1 eða nýrra.
  - Viðbót **Samþættingar skýjaprentunar** er uppsett

    Þessi viðbót er sjálfgefið gefin út og uppsett sem hluti af [!INCLUDE[prod_short](includes/prod_short.md)] á netinu og á staðnum. Hægt er að staðfesta hvort hún er sett upp á síðunni **Viðbótastjórnun**. Frekari upplýsingar eru í [Uppsetning og fjarlæging viðbóta í Business Central](ui-extensions-install-uninstall.md).
- [!INCLUDE[prod_short](includes/prod_short.md)] aðeins til innanhúss:
  - Azure Active Directory (AD) eða NavUserPassword-sannvottun er skilgreind.
    > [!NOTE]
    >  Universal PRINT Extension styður ekki sannvottun þjónustuveitu þjónustu (S2S). Það þarf undirritaðan notanda til að senda prentverk í alhliða prentþjónustu í gegnum API.
  - Forrit fyrir Business Central er skráð í Azure AD-leigjandanum og [!INCLUDE[prod_short](includes/prod_short.md)].

    Eins og önnur Azure-þjónusta sem vinnur með [!INCLUDE[prod_short](includes/prod_short.md)], krefst Skýjaprentun skráningu forrits fyrir [!INCLUDE[prod_short](includes/prod_short.md)] í Azure AD. Forritsskráningin býður upp á sannvottun og heimildarþjónusta milli [!INCLUDE[prod_short](includes/prod_short.md)] og Skýjaprentunar.

    Uppsetningin þín gæti nú þegar verið að nota forritsskráningu fyrir aðra Azure-þjónustu eins og Power BI. Ef svo er skal líka nota núverandi forritsskráningu fyrir skýjaprentun í stað þess að bæta nýrri við. Það eina sem þú þarft að gera, í þessu tilfelli, er að breyta App-skráningunni til að taka með viðeigandi prentheimildir fyrir Microsoft graph API:  **printershare. Lesibasic. allar**,  **Printjob. stofna** -og  **prentverk. lesibasic.** 

    Til að skrá forrit og stilla viðeigandi heimildir skal fylgja skrefunum sem lýst er í [Skrá forrit í Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory).

## Setja upp Universal PRINT og prentarar í Microsoft Azure

Áður en hægt er að hefja umsjón með alhliða prentprenturum á Viðskiptamiðstað eru nokkur verkefni til að fá alhliða Prentmet og keyrslu í Azure með þeim prenturum sem á að nota.

Ítarlegar leiðbeiningar um hvernig uppsetningin fer fram er að finna í [Hafist handa: Setja upp skýjaprentun](/universal-print/fundamentals/universal-print-getting-started) í fylgigögnum skýjaprentunar. Hér er yfirlit yfir skrefin sem þú þarft að ljúka. Flest þessara skrefa eru unnin í Azure-gáttinni.

1. Úthlutaðu leyfum skýjaprentunar á þig og aðra notendur.

    Hvernig leyfunum er úthlutað fer eftir því hvort verið er að samþætta við Business Central Online eða á staðnum.

    - Með [!INCLUDE[prod_short](includes/prod_short.md)] á netinu úthlutar þú leyfum með Microsoft 365 stjórnendamiðstöðinni.

      Frekari upplýsingar er að finna í [Hjálp í stjórnendamiðstöð Microsoft - Úthluta notendum leyfum](/microsoft-365/admin/manage/assign-licenses-to-users).

    - Með [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum er leyfum úthlutað í Azure-leigjandanum með Azure-gáttinni.

      Frekari upplýsingar eru í [Azure Directory - Úthluta eða fjarlægja leyfi í Azure Active Directory-gáttinni](/azure/active-directory/fundamentals/license-users-groups).

2. Setjið upp tengil skýjaprentunar til að skrá prentara sem geta ekki átt bein samskipti við skýjaprentun.

    Flestir prentarar á markaðnum geta ekki átt bein samskipti við skýjaprentun og því þarftu að setja upp tengil skýjaprentunar. Frekari upplýsingar er að finna í [Uppsetning á tengli skýjaprentunar](/universal-print/fundamentals/universal-print-connector-installation).

3. Skráið prentarana í skýjaprentun.

    Með því að skrá prentara veit skýjaprentun af prentaranum.

    - Fyrir prentara sem geta átt bein samskipti við skýjaprentun skal fylgja skrefunum sem framleiðandi prentarans gefur upp.

    - Fyrir aðra prentara skal skrá prentarana með því að nota tengil skýjaprentunar. 

      Frekari upplýsingar má finna á [Skráning prentara](/universal-print/fundamentals/universal-print-connector-printer-registration).

4. Breyta eiginleikum prentara (valfrjálst)

    Þegar prentari hefur verið skráður er hægt að skoða og breyta prentaraeiginleikum á borð við sjálfgefnar kjörstillingar.

    Frekari upplýsingar er að finna í [Umsjón með prentarastillingum með því að nota gátt skýjaprentunar](/universal-print/portal/configure-printer-settings).

5. Samnýta prentara með notendum.

    Alla prentara sem á að nota í  [!INCLUDE[prod_short](includes/prod_short.md)]  mun þarf að bæta við  *Samnýting*  prentara í Universal print. Öllum notendum sem þurfa aðgang að prentaranum verður að bæta við hluta prentarans. Frekari upplýsingar má finna á [Deila prentara](/universal-print/portal/share-printers).

    > [!TIP]
    > Það er alltaf hægt að bæta við eða fjarlæleggja notendur síðar. Frekari upplýsingar eru í [Prentheimildir](/universal-print/portal/share-printers#configure-user-permissions-for-a-printer-share).

6. Virkja umbreytingu skjals.

    Skýjaprentun breytir efni fyrir prentun yfir á XPS-snið. Sumir eldri prentarar á markaðnum styðja ekki breytingu yfir í XPS-efni&mdash;í mörgum tilfellum, aðeins PDF-snið. Prentun á þessum prenturum mistekst nema skýjaprentun sé sett upp til að umbreyta skjölum í snið sem prentari styður.

    Frekari upplýsingar er að finna í [Yfirlit yfir skjalaumbreytingu](/universal-print/portal/document-conversion).

Nú er hægt að bæta prenturunum við [!INCLUDE[prod_short](includes/prod_short.md)], setja upp sjálfgefna prentara fyrir skýrslur og prenta.  

## Bæta við prenturum í viðskiptum miðsvæðis á netinu

Eftir að prentarar eru settir upp og miðlað í Universal PRINT Ertu tilbúinn að bæta þeim  [!INCLUDE[prod_short](includes/prod_short.md)]  við fyrir notkun. Til eru tvær leiðir til að bæta við prenturum skýjaprentunar. Hægt er að bæta öllum prenturum við í einu eða einum í einu.

Bæta við prenturum sérstaklega við skulum setja upp sama Universal prenprentarann í  [!INCLUDE[prod_short](includes/prod_short.md)]  oftar en einu sinni. Því næst er hægt að breyta prentstillingum fyrir hvern viðbættan prentara, eins og pappírsbakki, stærð og stefnu. Á þennan hátt er hægt að setja upp prentara fyrir mismunandi skýrslur og skjöl sem eru með sérstakar kröfur um prentunina.

> [!NOTE]
> Ertu að nota  [!INCLUDE[prod_short](includes/prod_short.md)]  innanhúss? Ef svo er þá er farið í  [næsta kafla](#add-printers-in-business-central-on-premises), fyrsta Uppsetning er aðeins öðruvísi.  
<!-- To Do Adding printers individually lets you duplicate printers with custom , like different paper trays and paper size and orientation.  To add printers individually, you'll need to know printer's share name in Universal Print. -->

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Prentarastjórnun** og velja síðan viðkomandi tengil.
2. Veldu **Skýjaprentun**, því næst skal velja einn af eftirfarandi valkostum:

   - **Bæta við öllum prenturum skýjaprentunar** til að bæta við öllum prenturum sem ekki er búið að bæta við. Hægt er að nota þennan valkost þótt búið sé að bæta við prenturum.
   - **Bæta við prentara Skýjaprentunar** til að bæta við sérstökum prentara.  
3. Fylgdu leiðbeiningunum á skjánum.

    - Ef valið var **Bæta við öllum prenturum Skýjaprentunar** hefst uppsetningin **Bæta við prenturum Skýjaprentunar**. 

    - Ef valið var að **Bæta við prentara Skýjaprentunar** birtist síðan **Stillingar skýjaprentunar**. Fyllt er í  **reitinn Heiti**  og síðan er valið  **...**  **við hliðina á prenthlut í Universal PRINT**  Field til að velja þann prentarahlut sem er í Universal PRINT prentari. Fyllið út eftirstandandi reiti eftir því sem þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

Eftir að prentara hefur verið bætt við er hægt að skoða og breyta stillingum hans úr síðunni **Prentarastjórnun**. Veldu prentarann og veldu síðan **Breyta stillingum prentara**.

## Bæta við prenturum í atvinnuhúsnæði miðsvæðis innanhúss

<!--With [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, unlike online, users aren't automatically authenticated with the registered app in Azure used for the Universal Print service. So, before any Business Central user (including admins) can add or even use Universal Print printers, they'll have to authenticate with the Azure app and grant access to the Universal Print service. The following procedure describes how to initiate this authentication flow. Each user typically only has to do this task once.-->

Áður en notandi getur bætt við eða notað Universal PRINT prentarar Business Central hafa þeir heimild til aðgangs að Azure þjónustu sem Universal PRINT notar og veita henni heimild til að fá gögn og aðgerðir eins og:

- Innskráning og lestur notendaforlýsingar
- Les helstu upplýsingar um prentverk
- Stofnun prentverka

Þetta er gjarnan gert í fyrsta sinn sem þeir tengjast Azure skráðu forritinu sem notað er fyrir Universal print. Þessi heimildarflæði er gert óaðfinnanlega í viðskiptum miðsvæðis á netinu, án notendasamskipta. En rekstur miðsvæðis innanhúss starfar á annan hátt. Það krefst þess að þú, eða aðrir notendur sem vilja nota Universal PRINT prentarar, hafi aðeins auðkenningarflæðið &mdash;, aðeins einu sinni. Beinustu leið er lýst á eftirfarandi hátt. Minna bein leið er með því að tengjast annarri samþættri þjónustu sem notar sama Azure skrásett app, eins og  Power BI  or OneDrive. Hver notandi þarf yfirleitt aðeins að gera þetta verk einu sinni.

> [!NOTE]
> Ef þú ert admin mælum við með því að þú kláir þetta verkefni fyrir aðra notendur. Síðan skal upplýsa notendur sem þurfa að nota Universal PRINT prentarar hvernig á að gera það. Ef Azure skráð App fyrir Universal PRINT þarfnast admin samþykkis fyrir API heimildir, það er auðveldara ef samþykkis er veitt fyrir hönd fyrirtækisins. Hægt er að veita samþykki admin frá Azure gáttinni eða þegar keyrð eru skrefin sem fylgja. 

<!-- To Do Adding printers individually lets you duplicate printers with custom , like different paper trays and paper size and orientation.  To add printers individually, you'll need to know printer's share name in Universal Print. -->
### Tengjast alhliða prentun í fyrsta sinn

Ljúkið þessum skrefum til að tengjast alhliða prentþjónustu í fyrsta sinn.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Prentarastjórnun** og velja síðan viðkomandi tengil.
2. Veldu  **Universal PRINT** > **Bæta við öllum Universal PRINT prenturum**  til að ræsa Uppsetningarleiðbeiningar fyrir  **Universal PRINT prentarar**  (leiðsagnarforrit).
3. Leiðbeiningum á skjá er fylgt þar til farið er inn á AZURE ACTIVE DIRECTORY HEIMILSÞJÓNUSTUSÍÐUNA.

    <!--The AZURE ACTIVE DIRECTORY SERVICE PERMISSIONS page appears. You'll be prompted to give consent to Azure Services. You'll be lead through the process of verifying your Azure AD setup, checking your Universal Print license, and then adding the printers.-->

   ![Sýnir þá HEIMILDASÍÐU í AZURE ACTIVE DIRECTORY](media/azure-ad-services-permissions.png "Sýnir þá HEIMILDASÍÐU í AZURE ACTIVE DIRECTORY")

4. Velja skal  **tengilinn Azure Services** .

   1.  **Ef Umbeðin**  síða heimilda birtist skaltu lesa hana vandlega og velja  **Samþykkja**  til að samþykkja og halda áfram. Ef verið er að keyra sem admin er hægt að velja  **samþykki fyrir hönd fyrirtækis**  ef óskað er samþykkis fyrir alla notendur.

      ![Sýnir heimildasíðuna](media/azure-ad-permissions-requested.png "Azure heimildasíða um") Azure Request.

   2. Ef þú ert beðinn um að skrá þig inn með nafni og lykilorði þínu.

5. Þegar heimild er lokið er þér skilað á  **síðuna bæta við Universal PRINT prentarar** . Velja  **Næsta** > **Ljúka**  til að ljúka uppsetningunni.

Eftir að prentara hefur verið bætt við er hægt að skoða og breyta stillingum hans úr síðunni **Prentarastjórnun**. Veldu prentarann og veldu síðan **Breyta stillingum prentara**.

Þegar búið er að ljúka við upphafsstaf er hægt að nota Universal PRINT prentarar til að prenta skýrslur og önnur prentverk. Til að fá frekari upplýsingar er farið í  [prentun skýrslu](ui-work-report.md#PrintReport). Ef þú vilt bæta við, fjarlægja eða breyta einhverjum prenturum, ferðu bara aftur á  **Prentstjórnunarsíðuna**  og velur  **Universal print**.

## Algeng vandamál og úrlausnir

Í þessum hluta muntu fræðast um algeng vandamál sem notendur kunna að upplifa þegar reynt er að setja upp eða nota Universal PRINT prentarar.

### Þú hefur ekki aðgang að prentaranum \<your-printer\>.

Ef notandi fær þessi skilaboð þegar reynt er að prenta skjal til alhliða prentprentara getur það stafað af einu eftirtalinna skilyrða:

- Notandinn hefur ekki Universal PRINT leyfi sem úthlutað hefur verið til þeirra  Microsoft 365  eða Azure ACTIVE auglýsingareikninginn. 
- Notandinn er ekki tengdur við samnýtt prentarahluta í Universal print.
- (Innanhúss) Azure App skráningin sem notuð er fyrir Universal PRINT er ekki virka eða hefur nýlega verið breytt frá því síðast þegar notandinn skráði sig inn.
- (Innanhúss) Notandinn hefur ekki enn skráð sig inn á Azure skráð App fyrir Universal prentari App og samþykkt í fyrsta sinn.

## Villa varð við að sækja prentara sem voru samnýtt.

Ef notandi fær þessi skilaboð þegar reynt er að bæta við Universal PRINT prentara af  **síðunni prentarastjórnun**  er það vanalega vegna þess að þeir hafa ekki enn skráð sig inn á Azure skrásett App fyrir Universal prentari App og samþykkt í fyrsta sinn. 
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




-->

## Næstu skref
[Setja upp sjálfgefna prentara](ui-specify-printer-selection-reports.md).

## Sjá einnig .

[Yfirlit prentara](admin-printer-setup-overview.md)  
[Setja upp tölvupóstprenturum](admin-printer-setup-email.md)
[til að prenta skýrslu](ui-work-report.md#PrintReport)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Keyra runuvinnslur](ui-how-run-batch-jobs.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]