---
title: Algengar spurningar um listayfirlit
description: Ítarlegar upplýsingar um hvernig á að vista síur sem listayfirlit.
author: mikebcMSFT
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: list, filter, pane, views
ms.date: 01/01/2019
ms.author: mikebc
ms.openlocfilehash: 6357a025c58df8e55bf7aaad5961190ad6ed3350
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/03/2019
ms.locfileid: "2881991"
---
# <a name="list-views-faq"></a>Algengar spurningar um listayfirlit
Þetta efnisatriði svarar spurningum sem reyndir notendur spyrja oft um vinnu með listayfirlit og vistun fyrir síur.  

### <a name="how-do-views-handle-expressions"></a>Hvernig meðhöndla yfirlit segðir?
Þegar verið er að vista yfirlit sem inniheldur síur með segðir, eins og dagsetningabil, virkja, leitarorð eða síumerki, er segðin og ekki gildi hennar sem eru vistuð. Til dæmis, vista yfirlit sem afmarkar á svæðinu **Stofnuð dagsetning** með segðinni **-1W..í dag** finnur alltaf færslur sem eru tengdar við núverandi dagsetningu, jafnvel þegar yfirlitið er opnað fyrir næsta mánuð.

### <a name="where-are-list-views-saved"></a>Hvar eru listayfirlit vistuð?
Listayfirlit eru hluti af sérstillingum notanda og eru geymd í gagnagrunninum á sama hátt og þegar reitur er falinn eða yfirlitsvalmynd endurraðað. Ef öll aðlögun á lista er hreinsuð verða sérstilltar birtingar einnig fjarlægðar og þær hreinsaðar til frekari sérstillingar, svo sem endurröðun á yfirlitum. Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md).

### <a name="why-dont-i-have-a-save-icon"></a>Hvers vegna sé ég ekki tákn til að vista?
Vistunartákn og valmyndir eru ekki birtar með öllum yfirlitum í síuglugganum ef sérstilling er gerð óvirk fyrir notandahlutverk. Notendur sem eru ekki með virka sérstillingu geta ekki fengið aðgang að kerfisyfirlitum sem eru staðlaður hluti síðunnar, breyta eða búa til fleiri síur.

### <a name="on-which-page-types-can-i-use-list-views"></a>Á hvaða síðugerðum get ég notað listayfirlit?
Yfirlit eru aðeins tiltæk á lista og vinnublaðssíðum.

### <a name="are-views-also-available-on-other-form-factors"></a>Eru yfirlit einnig tiltæk á öðrum formeiginleikum?
Já. Öll yfirlit sem þú vistar í tölvuvafra eða skjáborðsforrit eru einnig í boði í töflu eða snjallsíma. Ekki er hægt að breyta eða sérsníða yfirlit í fartækjum.

### <a name="are-my-personal-views-always-accessible"></a>Eru persónuleg yfirlit mín alltaf aðgengileg?
Sömu yfirlit eru tiltæk á listasíðu ef farið er inn í hana úr yfirlitsvalmyndinni, í gegnum gluggann **Viðmótsleit**, eða með vefslóð tengils á listasíðuna. Yfirlit eru ekki tiltæk í listahlutum, uppflettingum eða þegar listasíða birtist sem gluggi.

### <a name="how-do-i-return-a-view-to-its-original-filters-after-modifying-them"></a>Hvernig set ég yfirlit í upprunalegar síur eftir að þeim hefur verið breytt?
Neðst í síuglugganum skal velja **Endurstilla síur** aðgerðina til að hreinsa síunarbreytingar sem gerðar hafa verið á yfirlitinu og snúa aftur í upprunalegt afmarkað svæði og síuskilyrði.

### <a name="what-is-the-difference-between-hiding-and-removing-views"></a>Hver er munurinn á því að fela og fjarlægja yfirlit?
Yfirliti er eytt varanlega þegar það er fjarlægt. Með því að fela yfirlit er hægt að fela það tímabundið á afmörkunarsvæði, en hægt er að opna það aftur síðar með því að velja aðgerðina **Sýna**.

### <a name="how-can-i-share-my-views-with-others"></a>Hvernig deili ég yfirliti mínu með öðrum?
[!INCLUDE[d365fin](includes/d365fin_md.md)] býður ekki upp á að deila nákvæmu listayfirliti, en hægt er að deila núverandi síum þannig að aðrir notendur geti séð sams konar lista yfir færslur. Í tölvuvafra er vefslóðin einfaldlega afrituð og henni deilt með samstarfsmönnum. Ekki er tryggt að samnýting á síum gefi viðtakandanum sömu síur og þú sérð í vafranum þínum.

### <a name="can-i-search-for-views-in-the-tell-me-window"></a>Get ég leitað að yfirlitum í glugganum „Viðmótsleit“?
Fj. Glugginn **Viðmótsleit** sýnir aðeins leitarniðurstöður fyrir síðuna en er einu skrefi frá því að sækja í eftirlætisyfirlitið þegar farið er á síðuna.

### <a name="what-is-shared-layout"></a>Hvað er samnýtt útlit?
Öll yfirlit á listasíðu skiptast í sameiginlega dálkauppsetningu þar sem dálkar eru birtir, röð þeirra, breidd, fast svæði og stillingar flýtifærslu. Þegar hluti dálkaútlitsins er sérstillt hefur það einnig áhrif á önnur yfirlit sem samnýta sama útlit á listasíðunni.

Sum kerfisyfirlit geta haft einkvæm yfirlit á dálkum á listanum. Til dæmis var hægt að endurraða dálkum aftur til að birta aðeins þá dálka sem mest eiga við það yfirlit. Hægt er að greina hvaða yfirlit hafa einkvæmt útlit með því að velja ![Sýna fleiri valkosti](media/show-more-options-icon.png "Sýna fleiri valkosti") táknið og fylgjast með því að gátreiturinn **Samnýtt útlit** sé ekki valinn. Sem notandi er hægt að sérstilla dálkútlitið fyrir yfirlit með einkvæmu útliti án þess að það hafi áhrif á önnur yfirlit á listasíðunni. Aðeins þróunaraðilar geta skilgreint einkvæma dálkauppsetningu fyrir yfirlit sem er með samnýtt útlit í upphafi.

### <a name="what-does-the-show-system-filters-link-do"></a>Hvað gerir tengillinn Sýna kerfisafmarkanir?
Á sumum listasíðum birtir síusvæðið **Sýna kerfisafmarkanir** neðst á síusvæðinu þegar síðan inniheldur síur sem kerfið hefur tilgreint. Þessar sérstöku síur eru yfirleitt notaðar til að birta færslur sem eru byggðar á núverandi samhengi, svo sem þegar búið er að sía lista yfir pantanir fyrir tiltekinn viðskiptavin.

Kerfissíur eru stilltar af þróunaraðila og nota síuhóp 0. Tæknilegar upplýsingar um kerfissíur má finna í [Aðferð síuhópa](/dynamics365/business-central/dev-itpro/developer/methods-auto/record/record-filtergroup-method)

### <a name="i-see-multiple-views-on-my-page-but-i-did-not-create-them-where-did-they-come-from"></a>Ég sé mörg yfirlit á síðunni minni en ég bjó þau ekki til. Hvaðan komu þau?
Yfirlitin sem birtast á öllum listum eru samandregin persónuleg yfirlit þín ásamt kerfisskoðunum. Kerfisyfirlit kunna að koma úr viðskiptaforritinu, úr viðbótum eða kunna að vera sértæk ef listinn var sérsniðinn fyrir hlutverkið þitt.

### <a name="why-do-some-views-provide-fewer-options"></a>Hvers vegna eru sum yfirlit með færri valkosti?
Sum yfirlit bjóða aðeins upp á valkostinn að vista afrit af yfirlitinu, á meðan aðrir leyfa ekki að breytingar á yfirlitinu séu vistaðar. Það hvernig yfirlitið var búið til ákvarðar valmöguleikana sem eru tiltækir fyrir það yfirlit. Hægt er að búa til yfirlit á marga vegu:
- Persónuleg yfirlit sem þú vistaðir
- Kerfisyfirlit sem eru staðlaður hluti viðskiptaforrits, eða bætt við af viðbótum eða hlutverkatilgreindum yfirlitum. Ólíkt persónulegum yfirlitum er ekki hægt að vista breytingar á síum aftur í það kerfisyfirlit.
- Eldri kerfisyfirlit sem eru staðlaður hluti viðskiptaforrits en voru stofnuð með eldri útgáfum af [!INCLUDE[d365fin](includes/d365fin_md.md)]. Þessi yfirlit bjóða upp á mun færri valkosti. Aðeins er hægt að vista þau sem nýtt yfirlit og ekki er hægt að fela þau eða endurraða þeim. Athugið að ekki verður boðið upp á eldri kerfisyfirlit við uppfærslu í framtíðinni á [!INCLUDE[d365fin](includes/d365fin_md.md)].

### <a name="how-do-i-convert-legacy-system-views"></a>Hvernig umbreyti ég eldri kerfisyfirlitum?
Eldri kerfisyfirlit eru listayfirlit sem þróunaraðilar hafa stofnað í eldri útgáfum af [!INCLUDE[d365fin](includes/d365fin_md.md)] með því að setja þær á síðuna Mitt hlutverk. Þessi yfirlit eru nú birt beint á listasíðunni en bjóða upp á færri sérstillingar og verulega færri valmöguleika. Hægt er að breyta eldra kerfisyfirliti í persónulegt yfirlit sem er fullkomlega sérstillanlegt, einfaldlega með því að vista það sem eldra yfirlit. Á sama hátt geta stjórnendur valið að umbreyta eldri kerfisyfirlitum sem bundin eru við tiltekin hlutverk með því að sérsníða notandahlutverkið og vista eldri yfirlitið sem nýtt yfirlit yfir hlutverkaleik.

Athugið að ekki verður boðið upp á eldri kerfisyfirlit við uppfærslu í framtíðinni á [!INCLUDE[d365fin](includes/d365fin_md.md)].

### <a name="others-in-my-organization-need-similar-list-views-as-standard-what-can-i-do"></a>Aðrir í fyrirtækinu mínu þurfa svipuð listayfirlit sem stöðluð yfirlit. Hvað get ég gert?
Vinna með persónuleg yfirlit eru fljótvirk og árangursrík en [!INCLUDE[d365fin](includes/d365fin_md.md)] býður upp á fleiri verkfæri til að skilgreina listayfirlit sem tiltekin notandahlutverk eða allir notendur í fyrirtækinu.
 - Forritarar geta sérstillt umhverfið og stofnað listayfirlit í viðbótum fyrir alla notendur í fyrirtækinu.
 - Þeir sem ekki kóða, á borð við stjórnendur eða deildarstjórnendur, hægt er að búa til lista yfir hlutverk sem eru sértækir þegar hlutverk er sérsniðið á síðunni **Forstillingar (hlutverk)**.

### <a name="i-work-with-multiple-languages-how-do-i-translate-the-name-of-the-view"></a>Ég vinn með mörg tungumál: Hvernig þýði ég heiti yfirlitsins?
Þegar nýtt yfirlit er vistað eða fyrirliggjandi yfirlit endurnefnt verður að færa inn þekkjanlegt og merkingarbært heiti fyrir það yfirlit. Heitið er vistað fyrir núverandi tungumál og birtist einnig þegar notandi eða aðrir notendur vinna með [!INCLUDE[d365fin](includes/d365fin_md.md)] á mismunandi tungumálum. Til að gefa upp þýdd heiti þarf að skipta um tungumál með því að nota síðuna **Mínar stillingar** og endurnefna síðan yfirlitið sem mun geyma þýtt heitið á nýja tungumálinu.

### <a name="do-views-with-expressions-work-in-all-languages"></a>Virka yfirlit með segðir á öllum tungumálum?
Segðir sem nota aðeins tákn, t.d. „**|**“ eða **..**, eru taldar öruggar fyrir notendur að opna á öllum tungumálum. Öll yfirlit með segðir sem innihalda bókstafi, leitarorð eða síumerki virka aðeins fyrir tungumálið þar sem þær voru heimilar.


### <a name="see-also"></a>Sjá einnig  
[Vista og sérsníða listayfirlit](ui-views.md)  
[Að finna eiginleika og upplýsingar](ui-search.md)    
[Röðun, leit og síun](ui-enter-criteria-filters.md)  
