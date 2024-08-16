---
title: Setja upp alhliða prentara
description: Lærðu hvernig þú getur notað Universal Print til að útvega skýprentun í Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 06/14/2024
ms.custom: bap-template
---

# Setja upp alhliða prentara

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Skýjaprentun er áskriftarþjónusta Microsoft 365 sem keyrir eingöngu á Microsoft Azure. Hún býður upp á miðstýrða prentstjórnun í gegnum gátt skýjaprentunar. [!INCLUDE[prod_short](includes/prod_short.md)] gerir uppsetningu prentara í skýjaprentun tiltæka biðlurum í gegnum viðbótina **Samþætting skýjaprentunar**.

![Uppsetning skýjaprentunar.](media/Universal-Print-arch.png)

Heildaruppsetningin krefst þess að unnið sé bæði í Microsoft Azure, með [Azure-gáttinni](https://portal.azure.com), og í [!INCLUDE[prod_short](includes/prod_short.md)]. Uppsetningunni er skipt milli tveggja meginverkhluta eins og lýst er í þessari grein:

1. Í Microsoft Azure skal setja upp Universal Prenta og bæta við prenturunum sem á að nota í Business Central í prenthlut. Farið í [þennan hluta](#set-up-universal-print-and-printers-in-microsoft-azure).
2. Bæta [!INCLUDE[prod_short](includes/prod_short.md)] skal við prenturum úr prenthlutum í Alhliða prentun.  [Farðu í þennan hluta](#add-printers-in-business-central-online) fyrir netið eða [hér](#add-printers-in-business-central-on-premises) á staðnum.

## Frumskilyrði

- Studdir prentarar

  [!INCLUDE[prod_short](includes/prod_short.md)] styður sömu prentara og skýjaprentun sem geta verið samhæfir skýjaprentun eða ekki. Ósamhæfðir prentarar geta ekki átt samskipti við skýjaprentun með beinum hætti, þannig að þeir þurfa á aukahugbúnaði fyrir tenginguna sem skýjaprentunin býður upp á. Ekki er allir eldri prentarar studdir. 

- Alhliða prentun:

  - Áskrift/leyfi skýjaprentunar fyrir fyrirtækið.

    Frekari upplýsingar er að finna í [Skýjaprentunarleyfi](/universal-print/fundamentals/universal-print-license).

  - Notandi hefur að minnsta kosti [hlutverk prentarastjóra](/entra/identity/role-based-access-control/permissions-reference#printer-administrator) í Microsoft Entra kenni.

    Ef stjórna á Alhliða prentun verður að vera að minnsta kosti [hlutverk prentarastjóra](/entra/identity/role-based-access-control/permissions-reference#printer-administrator) í Microsoft Entra auðkenni. Þessi hlutverk eru aðeins nauðsynleg til að stjórna skýjaprentun. Ekki er krafist þeirra af fólki sem settur er upp og prentararnir komnir úr [!INCLUDE[prod_short](includes/prod_short.md)].

- [!INCLUDE[prod_short](includes/prod_short.md)] á netinu og á staðnum:

  - [!INCLUDE[prod_short](includes/prod_short.md)] 2021 útgáfutímabil 1 eða nýrra.
  - Viðbót **Samþættingar skýjaprentunar** er uppsett

    Þessi viðbót er sjálfgefið gefin út og uppsett sem hluti af [!INCLUDE[prod_short](includes/prod_short.md)] á netinu og á staðnum. Hægt er að staðfesta hvort hún er sett upp á síðunni **Viðbótastjórnun**. Frekari upplýsingar eru í [Uppsetning og fjarlæging viðbóta í Business Central](ui-extensions-install-uninstall.md).
- [!INCLUDE[prod_short](includes/prod_short.md)] Aðeins innanhúss:
  - Microsoft Entra Auðkenni eða NavUserPassword sannvottun er grunnstillt.
    > [!NOTE]
    >  Alhliða prentunarviðbót styður ekki sannvottun á þjónustu (S2S). Það krefst þess að undirritaður notandi sendi prentverk til alhliða prentunarþjónustunnar í gegnum API-línurit.
  - Umsókn um Business Central er skráð í leigjanda þinn Microsoft Entra og [!INCLUDE[prod_short](includes/prod_short.md)].

    Eins og önnur Azure þjónusta sem vinnur með [!INCLUDE[prod_short](includes/prod_short.md)] krefst Universal Print forritaskráningar í [!INCLUDE[prod_short](includes/prod_short.md)]  Microsoft Entra auðkenni. Forritsskráningin býður upp á sannvottun og heimildarþjónusta milli [!INCLUDE[prod_short](includes/prod_short.md)] og Skýjaprentunar.

    Uppsetningin þín gæti nú þegar verið að nota forritsskráningu fyrir aðra Azure-þjónustu eins og Power BI. Ef svo er skal líka nota núverandi forritsskráningu fyrir skýjaprentun í stað þess að bæta nýrri við. Í þessu tilviki er skráningu forritsins breytt þannig að hún innihaldi viðeigandi prentheimildir fyrir Microsoft Graph API: **PrinterShare.ReadBasic.All,PrintJob.Create** **og** **PrintJob.ReadBasic.** 

    Til að skrá forrit og stilla réttar heimildir skal fylgja þeim skrefum sem lýst er í [Skrá forrit í Microsoft Entra kenni](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory).

## Setja upp alhliða prentun og prentara í Microsoft Azure

Áður en hægt er að hefja umsjón með Universal Prenta prentara í Business Central eru nokkur verk til að fá Universal Prenta upp og keyra í Azure með þeim prenturum sem á að nota.

Ítarlegar leiðbeiningar um hvernig uppsetningin fer fram er að finna í [Hafist handa: Setja upp skýjaprentun](/universal-print/fundamentals/universal-print-getting-started) í fylgigögnum skýjaprentunar. Hér er yfirlit yfir skrefin sem þú þarft að ljúka. Flest þessara skrefa eru unnin í Azure-gáttinni.

1. Úthlutaðu leyfum skýjaprentunar á þig og aðra notendur.

    Hvernig leyfunum er úthlutað fer eftir því hvort verið er að samþætta við Business Central Online eða á staðnum.

    - Með [!INCLUDE[prod_short](includes/prod_short.md)] á netinu úthlutar þú leyfum með Microsoft 365 stjórnendamiðstöðinni.

      Frekari upplýsingar er að finna í [Hjálp í stjórnendamiðstöð Microsoft - Úthluta notendum leyfum](/microsoft-365/admin/manage/assign-licenses-to-users).

    - Með [!INCLUDE[prod_short](includes/prod_short.md)] húsnæði er hægt að úthluta leyfi í leigjandanum með Azure-gáttinni.

      Læra meira við [Úthluta eða fjarlægja leyfi í Azure portal](/azure/active-directory/fundamentals/license-users-groups).

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

5. Samnýta prentarana með notendum.

    Þeim prentara sem á að nota í [!INCLUDE[prod_short](includes/prod_short.md)] þarf að bæta við *prentarahlutdeild* í Alhliða prentun. Öllum notendum sem þurfa aðgang að prentaranum verður að bæta við sem meðlimur prentarans. Frekari upplýsingar má finna á [Deila prentara](/universal-print/portal/share-printers).

    > [!TIP]
    > Alltaf er hægt að bæta við eða fjarlægja notendur síðar. Nánari upplýsingar eru í [Grunnstilling notendasáætlana fyrir samnýtingu](/universal-print/reference/portal/share-printers#configure-user-permissions-for-a-printer-share) prentara.

6. Virkja umbreytingu skjals.

    Skýjaprentun breytir efni fyrir prentun yfir á XPS-snið. Sumir eldri prentarar á markaði styðja ekki XPS innihald myndgerð&mdashin mörg tilfelli, aðeins PDF snið. Prentun á þessum prenturum mistekst nema skýjaprentun sé sett upp til að umbreyta skjölum í snið sem prentari styður.

    Nánari upplýsingar í [umbreytingaryfirliti](/universal-print/reference/portal/settings#2-document-conversion) skjala.

Nú er hægt að bæta prenturunum við [!INCLUDE[prod_short](includes/prod_short.md)], setja upp sjálfgefna prentara fyrir skýrslur og prenta.  

## Bæta við prenturum í Business Central á netinu

Þegar prentarar hafa verið settir upp og samnýttir í Alhliða prentun er hægt að bæta þeim við til [!INCLUDE[prod_short](includes/prod_short.md)] notkunar. Til eru tvær leiðir til að bæta við prenturum skýjaprentunar. Hægt er að bæta öllum prenturum við í einu eða einum í einu.

Með því að bæta við prenturum fyrir sig er sami alhliða prentari settur upp í [!INCLUDE[prod_short](includes/prod_short.md)] oftar en einu sinni. Því næst er hægt að breyta prentstillingum fyrir hvern viðbættan prentara, eins og pappírsbakki, stærð og stefnu. Á þennan hátt er hægt að setja upp prentara fyrir mismunandi skýrslur og skjöl sem eru með sérstakar kröfur um prentunina.

> [!NOTE]
> Ertu að nota [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum? Ef svo er er farið í [næsta hluta](#add-printers-in-business-central-on-premises) er uppsetningin aðeins önnur í fyrsta skipti.  
<!-- To Do Adding printers individually lets you duplicate printers with custom , like different paper trays and paper size and orientation.  To add printers individually, you'll need to know printer's share name in Universal Print. -->

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Prentarastjórnun** og velja síðan viðkomandi tengil.
2. Veldu **Skýjaprentun**, því næst skal velja einn af eftirfarandi valkostum:

   - **Bæta við öllum prenturum skýjaprentunar** til að bæta við öllum prenturum sem ekki er búið að bæta við. Hægt er að nota þennan valkost þótt búið sé að bæta við prenturum.
   - **Bæta við prentara Skýjaprentunar** til að bæta við sérstökum prentara.  
3. Fylgdu leiðbeiningunum á skjánum.

    - Ef valið var **Bæta við öllum prenturum Skýjaprentunar** hefst uppsetningin **Bæta við prenturum Skýjaprentunar**. 

    - Ef valið var að **Bæta við prentara Skýjaprentunar** birtist síðan **Stillingar skýjaprentunar**. Fyllt er í reitinn **Heiti** og síðan valið **...** við hlið reitsins **Prenta samnýtingu í Alhliða prentun** til að velja þann prentarahlut sem inniheldur alhliða prentara. Fyllið út eftirstandandi reiti eftir því sem þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

Eftir að prentara hefur verið bætt við er hægt að skoða og breyta stillingum hans úr síðunni **Prentarastjórnun**. Veldu prentarann og veldu síðan **Breyta stillingum prentara**.

## Bæta við prenturum í Business Central innanhúss

<!--With [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, unlike online, users aren't automatically authenticated with the registered app in Azure used for the Universal Print service. So, before any Business Central user (including admins) can add or even use Universal Print printers, they'll have to authenticate with the Azure app and grant access to the Universal Print service. The following procedure describes how to initiate this authentication flow. Each user typically only has to do this task once.-->

Áður en notandi getur bætt við eða notað Universal Prenta prentara Business Central, verða þeir að heimila aðgang að Azure-þjónustunni sem Universal Print notar og veita honum heimild til gagna og aðgerða eins og:

- Innskráning og lestur notandasniðs
- Les grundvallarupplýsingar um prentun
- Prentverk stofnuð

Þetta er yfirleitt gert í fyrsta skipti sem þeir tengjast Azure skráða forritinu sem notað er fyrir alhliða prentun. Í Business Central á netinu gerir þetta leyfisflæði óaðfinnanlega, án notendasamskipta. En Business Central á staðnum starfar öðruvísi. Það krefst þess að notandi eða allir aðrir notendur sem vilja nota Alhliða prentara hefji auðkenningarflæðið&mdash; yfirleitt, aðeins einu sinni. Beinu leiðinni er lýst í eftirfarandi skrefum. A minna bein leið er með því að tengjast annarri samþættri þjónustu sem notar sama Azure skráð forrit, eins Power BI og eða OneDrive. Hver notandi þarf yfirleitt aðeins að vinna þetta verk einu sinni.

> [!NOTE]
> Ef um er að ræða stjórnanda er mælt með því að þessu verki ljúki á undan öðrum notendum. Síðan skal láta notendur vita sem þurfa að nota Universal Prenta prentara hvernig á að gera það. Ef Azure skráða forritið fyrir Universal Print krefst stjórnunarsamþykktar fyrir API-heimildir er auðveldara að veita samþykki fyrir hönd fyrirtækisins. Hægt er að veita stjórna samþykki frá Azure Portal eða þegar keyrð eru skrefin sem fylgja. 

<!-- To Do Adding printers individually lets you duplicate printers with custom , like different paper trays and paper size and orientation.  To add printers individually, you'll need to know printer's share name in Universal Print. -->
### Tengjast alhliða prentun í fyrsta skipti

Ljúka skal þessum skrefum til að tengjast alhliða prentþjónustu í fyrsta skipti.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Prentarastjórnun** og velja síðan viðkomandi tengil.
2. Velja **Alhliða prentun** > **Bæta við öllum alhliða prenturum** til að ræsa uppsetningarleiðbeiningar með alhliða **prentprentara** (leiðsagnarforriti).
3. Leiðbeiningunum á skjánum er fylgt þar til þú kemur á síðuna **MICROSOFT ENTRA SERVICE PERMISSIONS** .

    <!--The MICROSOFT ENTRA SERVICE PERMISSIONS page appears. You'll be prompted to give consent to Azure Services. You'll be lead through the process of verifying your Microsoft Entra ID setup, checking your Universal Print license, and then adding the printers.-->

   ![Sýnir síðuna Microsoft ENTRA ÞJÓNUSTUheimildir](media/azure-ad-services-permissions.png "Sýnir síðuna Microsoft ENTRA ÞJÓNUSTUheimildir")

4.  **Velja skal Heimila Azure-þjónustu**  tengja.

   1.  **Ef síðan Umbeðin** heimild birtist skal lesa hana vandlega og velja **Samþykkja** til að samþykkja og halda áfram. Ef notandi er starfandi sem stjórnandi er hægt að velja **Samþykki fyrir hönd fyrirtækis** ef óskað er eftir samþykki fyrir öllum notendum.

      ![Sýnir síðuna](media/azure-ad-permissions-requested.png "Síðuna Azure beiðnaheimildir") Azure beiðnaheimildir.

   2. Skráðu þig inn með því að nota nafn þitt og aðgangsorð ef beðið er um það.

5. Þegar heimild lýkur er þér skilað á **síðuna Bæta við altækum prenturum** . Velja skal **Næsta** > **klára** til að ljúka uppsetningunni.

Eftir að prentara hefur verið bætt við er hægt að skoða og breyta stillingum hans úr síðunni **Prentarastjórnun**. Veldu prentarann og veldu síðan **Breyta stillingum prentara**.

Þegar innskráningu er lokið er hægt að nota alhliða prentara til að prenta skýrslur og önnur prentverk. Nánari upplýsingar eru í [Prentun skýrslu](ui-work-report.md#PrintReport). Ef bæta á við, fjarlægja eða breyta prenturum er farið aftur á **síðuna Prentstjórnun** og Alhliða prentun **valin**.

## Algeng vandamál og úrlausnir

Í þessum hluta fræðast um algeng vandamál sem notendur geta upplifað þegar reynt er að setja upp eða nota Alhliða prentara.

### Notandi hefur ekki aðgang að prentaranum \<your-printer\>.

Ef notandi fær þessi skilaboð þegar hann reynir að prenta skjal á altækan prentara stafar það hugsanlega af eftirfarandi:

- Notandinn hefur ekki leyfi til að úthluta alhliða prentun á reikning eða Microsoft 365 Azure Active AD. 
- Notandinn hefur ekki verið tengdur prentarahlutdeildinni í Altækri prentun.
- (Á staðnum) Azure-forritaskráningin sem notuð er fyrir Universal Print virkar ekki eða hefur nýlega breyst síðan síðast var notandinn skráður inn.
- (Á staðnum) Notandinn hefur ekki enn skráð sig inn í Azure skráð forrit fyrir universal Prentaraforrit og samþykki í fyrsta skipti.

## Villa varð við að sækja prentara sem samnýttir voru.

Ef notandi fær þessi skilaboð þegar hann reynir að bæta við alhliða prentara á **síðunni Prentarastjórnun** er það yfirleitt vegna þess að hann hefur ekki enn skráð sig inn í Azure skráð forrit fyrir universal Prentaraforrit og samþykki í fyrsta skipti. 
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
[Setja upp tölvupóstprentara](admin-printer-setup-email.md)
[prentun skýrslu](ui-work-report.md#PrintReport)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Keyra runuvinnslur](ui-how-run-batch-jobs.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
