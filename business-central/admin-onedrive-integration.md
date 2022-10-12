---
title: Stjórnun OneDrive samþættingar við Business Central
description: Kynntu þér hvað þú getur gert til að stýra samþættingu milli Business Central og OneDrive for Business.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OneDrive, share, browser
ms.date: 02/28/2022
ms.author: jswymer
ms.openlocfilehash: cb9f91caa06ed1b5bf579bf4be477c906a588faf
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9606306"
---
# <a name="managing-onedrive-integration-with-business-central"></a>Stjórnun OneDrive samþættingar við Business Central

Í þessari grein er að finna yfirlit yfir það sem stjórnandi getur gert til að stýra samþættingu OneDrive for Business við [!INCLUDE[prod_short](includes/prod_short.md)]. [!INCLUDE[prod_short](includes/prod_short.md)] Viðskiptavinir á netinu njóta sjálfvirkrar samþættingar án auka uppsetningar sem þarf til að nota opna og samnýta í OneDrive aðgerðum. Með uppsetningarleiðbeiningum fyrir **OneDrive** uppsetningu aðstoðar er hægt að veita notendum aðgang að enn fleiri OneDrive eiginleikum, eins og að opna Excel-skrá eða slökkva jafnvel á OneDrive&mdash; öllum eiginleikum.  

## <a name="configure-onedrive-for-integration-with-business-central"></a>Skilgreining OneDrive á samþættingu við rekstur miðsvæðis

Í þessum kafla er fjallað um kröfur sem þarf að uppfylla í OneDrive til að skilgreina samþættingu við rekstur miðsvæðis og verkefni hægt að gera til að stýra samþættingu.

### <a name="minimum-requirements"></a>Lágmarkskröfur

* Hver notandi verður að hafa leyfi fyrir [!INCLUDE[prod_short](includes/prod_short.md)] og OneDrive sem hluta af Microsoft 365 áætlun.
* OneDrive verður að vera sett upp fyrir hvern notanda fyrir sig.

### <a name="managing-privacy"></a>Umsjón með friðlýsingu

> [!IMPORTANT]
> Ef þú hefur valið að nota Seðlabanka og OneDrive til mismunandi landa eða svæða eru skrárnar sem myndaðar voru af viðskiptamiðunum og settar í OneDrive maí milli landamæra gagnaresita. Tryggja skal að staðfestar reglur um fyrirtækið og stjórnvöld samræmi skilyrði fyrir gagnabúskröfur áður en tengingin OneDrive er gerð virk.

Stjórnendur og notendur stjórna efninu sem geymt er í OneDrive og þessi gögn eru eingöngu í eigu fyrirtækisins þíns. Frekari upplýsingar er að finna í [Hvernig SharePoint og OneDrive tryggja öryggi gagna þinna í skýinu](/sharepoint/safeguarding-your-data). Þú getur einnig farið í [Persónuverndaryfirlýsingu Microsoft](https://privacy.microsoft.com/en-us/privacystatement) sem útskýrir gögnin sem Microsoft vinnur úr, hvernig Microsoft vinnur úr þeim og í hvaða tilgangi.

Með því að gera þessa þjónustutengingu samþykka:

(a) að deila gögnum frá Dynamics 365 Business Central með þjónustuaðila, sem mun nota hann í samræmi við skilmála þess og persónuverndarstefnu; (b) samræmismagn þjónustuveitunnar getur verið annað en Dynamics 365 Business Central ; og (c) Microsoft kann að samnýta tengiliðaupplýsingar notanda með þessum þjónustuaðila ef þörf er á því til að vinna og leysa þjónustuna af.

## <a name="configure-business-central"></a>Grunnstilla Business Central

Með Viðskiptamiðinu miðlægt er tengingin á milli viðskiptamiðanna OneDrive sjálfkrafa skilgreind fyrir þig og OneDrive aðgerðirnar eru fúslega tiltækar notendum. Ef slökkva á einhverjum eða öllum aðgerðum burt er hægt að nota Uppsetningarleiðbeiningar fyrir **OneDrive** uppsetningu aðstoðar í aðalbiðlara viðskiptavinar.

Skilgreining viðskiptamiðis innanhúss er ólík því tengingin á milli viðskiptamiðis OneDrive er ekki skilgreind fyrir þig. Þú verður að gera það handvirkt. Nánari upplýsingar fást með því að samskipa [samþættingu við Viðskiptamiðsjá OneDrive innanhúss](admin-onedrive-integration-onpremises.md).

### <a name="about-multiple-environments"></a>Um fjölum umhverfi

OneDrive Samþætting er skilgreind fyrir hvert umhverfi, þ.e. stillingarnar eiga við öll fyrirtæki í því umhverfi. Ef fyrirtækið hefur fleiri en eitt umhverfi þarf að skilgreina OneDrive samþættingu fyrir hverja.

### <a name="prerequisites"></a>Frumskilyrði

- Óbein, breyta og eyða (IMD) heimild um Þjónustuaðstæður **í töfluskjali** sem lágmarks

### <a name="configure-onedrive-using-onedrive-setup"></a>Samskipa OneDrive með OneDrive uppsetningarforriti

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **OneDrive uppsetningu** og veljið síðan tengda tengilinn. 
2. Í fyrsta sinn sem þú keyrir uppsetningarforritið hjálpar þú í **næði**. Lestu upplýsingarnar á síðunni og ef þú samþykkir skilmálana velur **þú að samþykkja** að halda áfram.
3. **Á síðunni Skilgreina skrármeðhöndlun** eru Eftirtaldir valkostir til að velja úr:

   [!INCLUDE[onedrive-feature-options](includes/onedrive-feature-options.md)]
4. Veldu **næst**>**Done**.

### <a name="switching-to-new-onedrive-integration-after-upgrade"></a>Skipta yfir í nýja OneDrive samþættingu eftir uppfærslu

**OneDrive** Uppsetning aðstoðar-hjálparinnar var kynnt í 2022 útgáfu Wave 2, útgáfu 21,0. OneDrive Áður fyrr var Samþætting notuð **SharePoint Uppsetning** tengingar, sem hefur verið afskrifaðar og verður fjarlægð í 2023 út Wave 2, útgáfa 23,0. Eftir að þú hefur uppfært í útgáfu 21, OneDrive munt þú vinna enn eins og áður. En við mælum með því að skipt sé yfir í nýja OneDrive samþættingu. Ef þessi rofi er gerður mun það verða auðveldara þegar Uppsetning **SharePoint tengingar er á** endanum fjarlægð. Auk þess sem það gerir kleift að nota leiðbeiningar um **OneDrive** uppsetningu uppsetningarhjálpar til að stjórna OneDrive aðgerðunum sem eru aðgengilegar fyrir notendur. **OneDrive** Uppsetningarforritið aðstoðar við umskiptin úr eldri SharePoint uppsetningu auðveld og óaðfinnalaus.

Til að skipta, bara opna og keyra **OneDrive uppsetningarforritið aðstoð til uppsetningar** beint eða opna **SharePoint uppsetningarsíðu** tengingar og velja **fara í nýja OneDrive uppsetningu** í tilkynningunni efst á síðunni. Fylgja skal uppsetningarleiðbeiningum eins og lýst er í fyrri hlutanum.

## <a name="restoring-onedrive-and-prod_short"></a>Að endurheimta OneDrive og [!INCLUDE[prod_short](includes/prod_short.md)]

Sem hluti af hörmulegu bataferli gætu Kerfisstjórar þurft að endurheimta [!INCLUDE[prod_short](includes/prod_short.md)] netumhverfi til að taka öryggisafrit frá einu í tímann og samstilla OneDrive geymslu við sama punkt í tíma. OneDrive Veitir endurheimt ýmis verkfæri eins og að endurheimta OneDrive fyrri tíma, endurheimta fyrri útgáfu af einstakri skrá eða endurheimta eyddar skrár. Frekari upplýsingar er að finna í eftirfarandi greinum:

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
