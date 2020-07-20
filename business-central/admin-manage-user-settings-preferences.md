---
title: Stjórna notendastillingum og kjörstillingum í Dynamics 365 Business Central
description: Stjórna notendastillingum og kjörstillingum í Dynamics 365 Business Central.
author: sorenfriisalexandersen
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user settings, preferences, language, region, time zone, regional settings
ms.date: 06/17/2020
ms.author: soalex
ms.openlocfilehash: 633a0872a878843f26d627dcd76e69d1c851ef8a
ms.sourcegitcommit: 3945f16d6d9c9853651e6291ce1465a44fd71fc8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/17/2020
ms.locfileid: "3460421"
---
# <a name="manage-user-settings-and-preferences"></a>Stjórna notendastillingum og kjörstillingum

Sem stjórnandi getur þú nýtt notandastillingar í [!INCLUDE[d365fin](includes/d365fin_md.md)], svipað því og einstakir notendur geta stjórnað eigin kjörstillingum á síðunni **Mínar stillingar**.  

## <a name="types-of-user-settings"></a>Gerðir notendastillinga

*Notandastillingar* eru ekki þær sömu og *Notandauppsetning*, sem er um notandann sem eining og aðgangur notanda í kerfinu. Notandastillingar hafa ennfremur ekkert að gera með sérstillingar notanda, t.d. minniháttar breytingum á notandaviðmóti. Notendastillingar tilgreina kjörstillingar notandans á ýmsan máta sem forritið birtist notandanum. Eftirfarandi málsgrein sýnir fimm gerðir notendastillinga og kjörstillingar sem einstakur notandi getur stillt eða stjórnandi stillir miðlægt:

- **Fyrirtæki**  

  Þessi stilling ákvarðar fyrirtækið sem er skráð inn í næstu innskráningu. Notandi getur haft aðgang að mörgum fyrirtækjum og getur verið virkur í nokkrum fyrirtækjum.

- **Forstillingar (hlutverk)**  

  Forstillingin lýsir hlutverki notanda í fyrirtækinu, t.d. *Sölustjóri*, *Bókari* eða *Innkaupafulltrúi*. Forstillingin ákvarðar síðan hlutverkamiðstöð notandans, heimasíðuna sem notendur sjá þegar hann skráir sig inn. Forstillingin hefur ekki áhrif á aðgangsheimild að virkni í [!INCLUDE[d365fin](includes/d365fin_md.md)].  

- **Auðkenni málstaðals (svæðisstillingar)**  

  Skilgreinir hvernig dagsetningar og tölustafir birtast í [!INCLUDE[d365fin](includes/d365fin_md.md)] -biðlaranum, svo sem hvort nota eigi evrópskar eða bandarískar dagsetningarsnið eða hvernig á að birta tugabrotin og þúsund skiltákn í upphæðum. Ef [!INCLUDE[d365fin](includes/d365fin_md.md)] notendur eru samstilltir frá Office 365 eru svæðisstillingarnar frá Office 365 notaðar, að því gefnu að notandinn vill nota sömu stillingar í Office-vörum og [!INCLUDE[d365fin](includes/d365fin_md.md)]. Stjórnandi eða notandi getur breytt þessum stillingum handvirkt í [!INCLUDE[d365fin](includes/d365fin_md.md)], en þær verða endurstilltar á gildið frá Office 365 þegar næsta samstilling er framkvæmd.

- **Tungumál**  

  Skilgreinir forritstungumál sem [!INCLUDE[d365fin](includes/d365fin_md.md)] birtir texta, textar og villuskilaboð á. Ef [!INCLUDE[d365fin](includes/d365fin_md.md)] notendur eru samstilltir frá Office 365 eru tungumálastillingar frá Office 365 notaðar, að því gefnu að notandinn vilji nota sömu stillingar í Office-vörum og [!INCLUDE[d365fin](includes/d365fin_md.md)]. Stjórnandi eða notandi getur breytt þessum stillingum handvirkt í [!INCLUDE[d365fin](includes/d365fin_md.md)], en þær verða endurstilltar á gildið frá Office 365 þegar næsta samstilling er framkvæmd.

  Ef tungumálastillingin úr Office 365 samsvarar studdu tungumáli í [!INCLUDE[d365fin](includes/d365fin_md.md)] verður slíkt tungumál valið fyrir notandann.  

  > [!NOTE]
  > Hugsanlega þarf að setja upp tungumálaforrit fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] til að birta tungumálið á réttan hátt. Þar af leiðandi er það góð venja að setja upp nauðsynleg tungumálaforrit áður en einhver notandi skráir sig inn í fyrsta skipti þannig að þeir fái góða upplifun frá byrjun. Frekari upplýsingar er að finna í listanum yfir [studd tungumál](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations).  
  
- **Tímabelti**  

  Skilgreinir tímabeltið þar sem notandinn er staðsettur. Sem stendur er þetta ekki samstillt af Office 365 og verður að stilla handvirkt.  

> [!NOTE]
> Ef samstilling Office 365 -notanda er gerð á meðan notendur eru skráðir inn í [!INCLUDE[d365fin](includes/d365fin_md.md)] verða slíkir notendur að uppfæra vafrann eða skrá sig út og aftur inn í [!INCLUDE[d365fin](includes/d365fin_md.md)] til að sjá þeir geti séð annað tungumál stillt með samstillingaraðgerðinni.

## <a name="overview-of-all-user-settings"></a>Yfirlit yfir allar notendastillingar

Stjórnendur hafa möguleika á því að stilla eða breyta þessum stillingum fyrir notendur í hverju fyrirtæki. Þetta er gert á síðunni **Sérstillingar notanda**. Færslurnar á þessari síðu sýna val tiltekins notanda á stillingunum hér á undan, eða eina færslu á hvern notanda. Þegar notendur gera breytingar á stillingum sínum á síðunni **Mínar stillingar** birtast slíkar breytingar á listanum **Sérstillingar notanda**. Stjórnendur geta einnig breytt þessum stillingum fyrir notendur áður en þeir skrá sig inn í fyrsta sinn, þannig að notendur þurfa ekki að gera það sjálfir og gefur þeim betri upplifun við að *hefjast handa*.

> [!NOTE]
> Sérstillingar notanda tengjast á engan hátt minniháttar *sérstillingum* sem notandi gerir á upplifun notanda.

## <a name="to-review-or-make-changes-to-user-settings"></a>Til að yfirfara eða gera breytingar á notandastillingum

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu tákn") slá inn **Sérstillingar notanda** og velja svo viðeigandi tengil.
2. Þetta sýnir lista yfir notendur og stillingar þeirra. Til að breyta stillingum notanda er smellt á **kenni notanda** eða á **stjórna** og síðan á **breyta**.
3. Spjaldið **Sérstilling notanda** fyrir stillingar tiltekins notanda er sýnt og hægt er að gera breytingar á stillingum sem óskað er eftir.  

## <a name="see-also"></a>Sjá einnig

[Hafist handa](product-get-started.md)  
[Lönd/svæði í boði og studd tungumál](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations)  
[Breyta tungumáli og landsstaðli](about-locale-language.md)  