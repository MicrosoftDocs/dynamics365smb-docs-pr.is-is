---
title: Stjórnun OneDrive samþættingar við Business Central
description: Kynntu þér hvað þú getur gert til að stýra samþættingu milli Business Central og OneDrive for Business.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'OneDrive, share, browser'
ms.date: 02/28/2022
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# <a name="managing-onedrive-integration-with-business-central"></a>Stjórnun OneDrive samþættingar við Business Central

Í þessari grein er að finna yfirlit yfir það sem stjórnandi getur gert til að stýra samþættingu OneDrive for Business við [!INCLUDE[prod_short](includes/prod_short.md)]. [!INCLUDE[prod_short](includes/prod_short.md)] netviðskiptavinir njóta sjálfvirkrar samþættingar án viðbótaruppsetningar sem þarf til að nota opna og deila í OneDrive eiginleikum. Með uppsetningaleiðbeiningunum **OneDrive uppsetning** geturðu gefið notendum aðgang að jafnvel fleiri OneDrive eiginleikum, eins og að opna Excel-skrá í OneDrive&mdash;eða jafnvel slökkva á öllum eiginleikum.  

## <a name="configure-onedrive-for-integration-with-business-central"></a>Grunnstilla OneDrive fyrir samþættingu við Business Central

Í þessum hluta er rætt um kröfur sem þarf að uppfylla í OneDrive til að Business grunnstilli samþættinguna við Business Central og verk sem þú getur gert til að stjórna samþættingunni.

### <a name="minimum-requirements"></a>Lágmarkskröfur

* Hver notandi verður að hafa leyfi fyrir [!INCLUDE[prod_short](includes/prod_short.md)] og OneDrive sem hluta af áskriftarleið Microsoft 365.
* OneDrive verður að vera sett upp fyrir hvern notanda fyrir sig.

### <a name="managing-privacy"></a>Umsjón með persónuvernd

> [!IMPORTANT]
> Ef þú hefur valið að innleiða Business Central og OneDrive í mismunandi löndum og svæðum geta skrár sem Business Central býr til og eru settar í OneDrive farið yfir mörk gagnastaðsetningar. Gakktu úr skugga um að staðfesta reglur fyrirtækisins og kröfur yfirvalda um reglufylgni fyrir staðsetningu gagna áður en þú virkjar tenginguna við OneDrive.

Stjórnendur og notendur stjórna efninu sem geymt er í OneDrive og þessi gögn eru eingöngu í eigu fyrirtækisins þíns. Frekari upplýsingar er að finna í [Hvernig SharePoint og OneDrive tryggja öryggi gagna þinna í skýinu](/sharepoint/safeguarding-your-data). Þú getur einnig farið í [Persónuverndaryfirlýsingu Microsoft](https://privacy.microsoft.com/en-us/privacystatement) sem útskýrir gögnin sem Microsoft vinnur úr, hvernig Microsoft vinnur úr þeim og í hvaða tilgangi.

Virkjun þessarar þjónustutengingar samþykkir:

(a) til að deila gögnum úr Dynamics 365 Business Central með þjónustuveitunni, sem mun nota þau samkvæmt skilmálum hennar og persónuverndarstefnu; (b) reglufylgnistig þjónustuveitunnar getur verið annað enDynamics 365 Business Central; og (c) Microsoft kann að deila samskiptaupplýsingum þínum með þessari þjónustuveitu ef þess er þörf til að hægt sé að nota og úrræðaleita þjónustuna.

## <a name="configure-business-central"></a>Grunnstilla Business Central

Með Business Central Online er tengingin á milli Business Central og OneDrive sjálfkrafa stillt fyrir þig og OneDrive eiginleikarnir eru sjálfgefið tiltækir fyrir notendur. Ef þú vilt slökkva á sumum eða öllum eiginleikunum getur þú notað uppsetningarleiðbeiningarnar **OneDrive uppsetning** í biðlara Business Central.

Að grunnstilla Business Central á staðnum er öðruvísi vegna þess að tengingin milli Business Central og OneDrive er ekki grunnstillt fyrir þig. Þú verður að gera þetta handvirkt. Frekari upplýsingar er að finna í [Grunnstilling OneDrive samþættingar við Business Central á staðnum](admin-onedrive-integration-onpremises.md).

### <a name="about-multiple-environments"></a>Um mörg umhverfi

OneDrive samþætting er stillt í hverju umhverfi. Þ.e. stillingarnar þínar munu gildi í öllum fyrirtækjum í því umhverfi. Ef fyrirtækið þitt er með fleiri en eitt umhverfi þarftu að stilla OneDrive samþættingu fyrir hvert og eitt.

### <a name="prerequisites"></a>Frumskilyrði

- Óbein breytingar- og eyðingarheimild í töflu **Aðstæður skjalaþjónustu** sem lágmark

### <a name="configure-onedrive-using-onedrive-setup"></a>Stilla OneDrive með OneDrive uppsetningu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **OneDrive Uppsetning** og velja síðan viðkomandi tengil. 
2. Í fyrsta sinn sem þú opnar aðstoðina sérðu **Persónuvernd**. Lestu upplýsingarnar á síðunni og ef þú samþykkir skilmálana skaltu velja **Samþykkja** til að halda áfram.
3. Á síðunni **Stilla meðhöndlun skráa** ertu með eftirfarandi valkosti til að velja úr:

   [!INCLUDE[onedrive-feature-options](includes/onedrive-feature-options.md)]
4. Veldu **Áfram**>**Lokið**.

### <a name="switching-to-new-onedrive-integration-after-upgrade"></a>Skipt yfir í nýja OneDrive samþættingu eftir uppfærslu

Hjálparuppsetningin **OneDrive uppsetning** var kynnt árið 2022 á útgáfutímabili 2, útgáfu 21.0. Áður notaði OneDrive samþættingin **Uppsetning SharePoint tengingar**, sem hefur verið úrelt og verður fjarlægð í 2023 útgáfutímabili 2, útgáfu 23.0. Þegar þú hefur uppfært í útgáfu 21 mun OneDrive enn virka eins og áður. En við mælum með því að þú skiptir yfir í nýju OneDrive samþættinguna. Að skipta yfir núna auðveldar hlutina þegar **Uppsetning SharePoint tengingar** verður að lokum fjarlægð. Auk þess gerir það þér kleift að nota uppsetningarleiðbeininguna **OneDrive uppsetning** til að stjórna OneDrive eiginleikum sem þú getur nálgast. Uppsetningarleiðbeiningin **OneDrive uppsetning** auðveldar og einfaldar færslu úr eldri SharePoint uppsetning.

Til að skipta skal bara opna og keyra uppsetningarleiðbeininguna **OneDrive uppsetning** eða opna síðuna **Uppsetning SharePoint tengingar** og velja **Fara í OneDrive uppsetningu** í tilkynningunni efst á síðunni. Fylgdu uppsetningarleiðbeiningunum eins og lýst er í hlutanum á undan.

## <a name="restoring-onedrive-and-"></a>Að endurheimta OneDrive og [!INCLUDE[prod_short](includes/prod_short.md)]

Sem hluti af æfingu til að endurheimta eftir áfall gætu stjórnendur þurft að endurheimta [!INCLUDE[prod_short](includes/prod_short.md)] netumhverfi í öryggisafriti aftur í tíma og samstilla OneDrive geymslu til þess tíma. OneDrive veitir ýmis verkfæri fyrir endurheimt, t.d. endurheimt á OneDrive notanda aftur í tíma, endurheimta eldri útgáfu einstakrar skráar eða endurheimta eyddar skrár. Frekari upplýsingar er að finna í eftirfarandi greinum:

* Fyrir [!INCLUDE[prod_short](includes/prod_short.md)] skal skoða [Að endurheimta umhverfi í stjórnendamiðstöðinni](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-backup-restore).
* Fyrir OneDrive skal skoða [Endurheimta OneDrive](https://support.microsoft.com/en-us/office/restore-your-onedrive-fa231298-759d-41cf-bcd0-25ac53eb8a15?ui=en-us&rs=en-us&ad=us)

## <a name="governance"></a>Stjórnunarhættir

Stjórnendamiðstöð SharePoint veitir víðtæka stjórn á reglum sem gilda um notkun á OneDrive í öllu fyrirtækinu. Altækir stjórnendur eða notendur sem eru með SharePoint stjórnandahlutverkið geta sett upp reglur sem skera úr um hver fær aðgang að OneDrive þar sem gögn eru geymd, líftími efnis og margt fleira. Eftirfarandi tenglar veita upplýsingar um oft notaða eiginleika og stillingar sem geta aukið samþættingu þína við [!INCLUDE[prod_short](includes/prod_short.md)]. 

* [Stjórna samnýtingarstillingum](/sharepoint/turn-external-sharing-on-or-off)
* [Nota upplýsingatálma með SharePoint](/sharepoint/information-barriers)
* [Kynntu þér gagnatapsvörn](/microsoft-365/compliance/dlp-learn-about-dlp)
* [Stilla sjálfgefið geymslupláss fyrir OneDrive notendur](/onedrive/set-default-storage-space)
* [Bæta við og fjarlægja stjórnendur fyrir OneDrive notanda](/sharepoint/manage-user-profiles#add-and-remove-admins-for-a-users-onedrive)
* [Gera stofnun OneDrive óvirka fyrir suma notendur](/sharepoint/manage-user-profiles#disable-onedrive-creation-for-some-users)
* [Fjölbreyttir landfræðilegir eiginleikar í OneDrive og SharePoint á netinu](/microsoft-365/enterprise/multi-geo-capabilities-in-onedrive-and-sharepoint-online-in-microsoft-365)

> [!NOTE]
> Sumir eiginleikar eru hugsanlega aðeins í boði fyrir tilteknar áskriftarleiðir.

## <a name="see-also"></a>Sjá einnig .

[Business Central og OneDrive fyrir Business Integration](across-onedrive-overview.md)  
[Opna Business Central Files í OneDrive](across-share-onedrive.md)  
[OneDrive ALGENGAR SPURNINGAR](admin-onedrive-faq.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
