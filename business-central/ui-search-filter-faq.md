---
title: Um leit og síun í Business Central
description: Svarar algengum spurningum um leit og síun.
author: mikebcMSFT
ms.service: dynamics365-business-central
ms.topic: article
ms.reviewer: edupont04
ms.search.keywords: keyboarding, productivity, how do i, filter pane
ms.date: 11/16/2020
ms.author: mikebc
ms.openlocfilehash: b993fd047db09b1dc412d9927168aa0233c057a6
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756718"
---
# <a name="searching-and-filtering-faq"></a>Algengar spurningar um leit og síun
Þessi grein svarar algengum spurningum sem þú gætir haft um leit og síun.

## <a name="is-there-a-difference-between-searching-and-filtering"></a>Er munur á leit og síun?
Já.
- Leitin er einföld og víðtæk: hún passar við skrár sem innihalda leitartexta yfir allar sýnilegar reiti á síðunni og gerður ekki er gerður greinarmunur á hástöfum og lágstöfum.
- Síun er mjög sveigjanleg og hægt að beita á tilteknum reitum, þar á meðal þær sem eru ekki sýnilegar á síðunni: Það sýnir færslur með nákvæmum samsvörum þar sem gerður er greinarmunur á hástöfum og lágstöfum, en hægt er að breyta með öflugu leitarmerkjum, táknum og formúlum. Nánari upplýsingar um hvernig á að nota þessar aðgerðir er að finna í [Flokkun, leit og síun](ui-enter-criteria-filters.md).

## <a name="exactly-which-fields-are-matched-when-searching"></a>Hvaða reitir eru samsvaraðir við leit?
[!INCLUDE[prod_short](includes/prod_short.md)] notar leitarskilyrði fyrir alla reiti sem eru sýnilegir á síðunni. Ef reitur hefur verið falinn, t.d. með því að nota sérstillingu, þá tekur leitin hann ekki til greina. Leitarskilyrði eru aðeins notuð á reitum ef gagnagerð þeirra passar við leitarskilyrðið. Til dæmis ef leitað er að textanum *í dag* verður leitað bókstaflega í öllum texta- og kóðareitum að gildinu „í dag“ og líka öllum dagsetningareitum þar sem *í dag* er metið sem segð fyrir daginn í dag, en leitar ekki í númerareitum. Frekari upplýsingar um síuskilyrði er að finna í [Flokkun, leit og síun](ui-enter-criteria-filters.md#-filter-criteria-and-operators).

## <a name="is-there-a-keyboard-experience-for-search-and-filter"></a>Er hljómborð reynsla fyrir leit og síun?
Leit og síun hafa verið mjög fínstillt fyrir notendur sem kjósa mús-frjáls samskipti til að vinna á skilvirkan hátt með gögnum þeirra. Það eru margs konar flýtilyklar sem hægt er að nota í röð til að vinna í miklum hraða. Frekari upplýsingar er að finna í [Flýtilyklar](keyboard-shortcuts.md#KeyboardFilter).

## <a name="is-the-filter-pane-available-on-all-lists"></a>Er síunarsvæðið í boði á öllum listum?
Síunarsvæði er tiltæk á síðum þar sem listinn er aðal innihald síðunnar, svo sem vinnublað og listasíður, þar með talin listar sem hægt er að nálgast á yfirlitsstikunni. Síunarsvæðið er ekki enn í boði fyrir lista sem birtast sem hlutar, t.d. upplýsingareitir eða hlutverkamiðstöð eða fyrir lista sem birtast sem svargluggi, til dæmis í leit. Þegar listi er felldur inn á síðu, t.d. sölulínur á sölupöntun, er síunarsvæðið í boði þegar áherslan er sett á þann lista með hnappi áherslustillingar. Frekari upplýsingar er að finna í [Fókus á vörulínur](ui-enter-data.md#Focus).

## <a name="how-can-i-save-my-filters"></a>Hvernig get ég vistað síurnar mínar?
Síurnar þínar og breytingar á fyrirfram skilgreindum síum eru vistaðar í gegnum lotuna (meðan þú ert ennþá innskráður), jafnvel þótt þú ferð í burtu frá síðunni. Hægt er að vista afmarkanir varanlega sem nafngreint yfirlit á listanum með því að velja ![Vista yfirlit](media/save_view_icon.png "Vista yfirlit") táknið á afmörkunarsvæðinu. Frekari upplýsingar er að finna í [Algengar spurningar um listayfirlit](ui-views-faq.md). Athugið að ólíkt síum er ekki hægt að muna leitartexta þegar þú vafrar í burtu frá síðu og hann er ekki vistaður þegar þú vistar yfirlit.

Á síðum skýrslubeiðna er einnig hægt að vista síur eða nota fyrirframskilgreindar síur. Frekari upplýsingar eru í [Nota vistaðar stillingar](ui-work-report.md#SavedSettings).

## <a name="is-this-the-same-as-advanced-filters-and-limit-totals-in-microsoft-dynamics-nav"></a>Er þetta það sama og ítarlegar síur og takmarka heildarstærðir í Microsoft Dynamics NAV?
[!INCLUDE[prod_short](includes/prod_short.md)] byggir á þessum vinsælustu eiginleikum og skilar nútíma og mjög nothæfi reynslu til að finna og greina gögnin þín. Með fleiri flýtilyklum og kynningu á leit, [!INCLUDE[prod_short](includes/prod_short.md)] yfirfærir virkni sem er að finna í Dynamics NAV.  

## <a name="can-i-search-and-filter-using-the-companion-apps-and-add-ins-for-microsoft-365"></a>Get ég leitað og síað með því að nota viðbótarforrit og innbætur fyrir Microsoft 365?
Á mismunandi birtingastöðum, eins og fartækjum eða Outlook, getur þú leitað í listum en getur ekki síað á einstökum reitum í flestum tilfellum. Í [!INCLUDE[prod_short](includes/prod_short.md)]-forritinu fyrir Microsoft Teams er bæði hægt að leita og sía í listum.

## <a name="how-do-i-view-how-my-search-terms-have-been-applied-to-fields-in-the-list"></a>Hvernig skoða ég hvernig leitarorðin mín hafa verið notuð í reitum í listunum?
Þegar leitarorð hafa verið slegin inn í leitarreitinn er hægt að skoða nákvæmt leitarskilyrði og hvaða reiti það hefur verið notað í með því að opna síðueftirlitsgluggann (**Ctrl+Alt+F1**) og velja flipann **Afmarkanir síðu**.

## <a name="can-i-do-anything-about-the-searching-for-rows-is-taking-too-long-message"></a>Get ég gert eitthvað við "leita að röðum tekur of lengi" skilaboð?

Það eru tímamörk um hversu langur leitaraðgerð getur tekið. Fyrst skaltu reyna að breyta leitarskilyrðum og leita aftur. Ef þú ert að nota [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum skaltu hafa samband við kerfisstjóra þína, því stjórnandi getur aukið tímamörk fyrir leit.

Sem stjórnandi á staðnum, eykur þú tímamörkin í leitum með því að breyta **tímamörk leitar** stillingunni á [!INCLUDE[prod_short](includes/prod_short.md)] þjóni. Nánari upplýsingar er að finna í [Stilling á Business Central Server](/dynamics365/business-central/dev-itpro/administration/configure-server-instance?#Database) í Business Central Developer og IT Pro hjálp.

## <a name="will-microsoft-extend-the-filter-pane-experience"></a>Mun Microsoft lengja reynslu síunarsvæðisins?
Við hjá Microsoft erum stöðugt að hlusta á viðbrögð frá fjölbreyttu samfélagi notenda okkar og starfa á efstu tillögum samfélagsins. Ef þú hefur áhuga á að lengja síunarsvæðið til fleiri myndaþátta og fleiri tegundir lista eða hafa góðan hugmynd um hvernig á að bæta það, bæta við hugmynd eða kjósa um núverandi hugmyndir á [aka.ms/BusinessCentralIdeas](https://aka.ms/businesscentralideas).

## <a name="see-also"></a>Sjá einnig .
[Röðun, leit, og síun](ui-enter-criteria-filters.md)  
[Finndu síður og upplýsingar með Viðmótsleit](ui-search.md)  
[Að finna síður með hlutverkaleit](ui-role-explorer.md)  
[Hafist handa](product-get-started.md)  
