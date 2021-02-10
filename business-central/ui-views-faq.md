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
ms.date: 10/01/2020
ms.author: mikebc
ms.openlocfilehash: f39e20a9b4dae7e84c491d6d28308133f4691c05
ms.sourcegitcommit: 32bfc2acaaf3693afc9aeb86feea505fd328caa1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/19/2021
ms.locfileid: "5024515"
---
# <a name="list-views-faq"></a>Algengar spurningar um listayfirlit
Þessi grein svarar spurningum sem reyndir notendur spyrja oft um vinnu með listayfirlit og vistun fyrir síur.  

### <a name="how-do-views-handle-expressions"></a>Hvernig meðhöndla yfirlit segðir?

Þegar yfirlit er vistað sem inniheldur síur með segðum (eins og dagsetningabili, virknitáknum, leitarorðum eða síutáknum) verður aðeins segðin vistuð&mdash;ekki gildin sem verða til. Til dæmis, vista yfirlit sem afmarkar á svæðinu **Stofnuð dagsetning** með segðinni `-1W..today` finnur alltaf færslur sem eru tengdar við núverandi dagsetningu, jafnvel þegar yfirlitið er opnað fyrir næsta mánuð.

### <a name="where-are-list-views-saved"></a>Hvar eru listayfirlit vistuð?

Listayfirlit eru hluti af sérstillingum notanda og eru geymd í gagnagrunninum á sama hátt og þegar reitur er falinn eða yfirlitsvalmynd endurraðað. Ef allar sérstillingar á lista eru hreinsaðar verða sérstilltar birtingar einnig fjarlægðar og aðrar sérstillingar hreinsaðar, svo sem endurröðun á yfirlitum. Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md).

### <a name="why-dont-i-have-a-save-icon"></a><a name="save"></a>Hvers vegna sé ég ekki tákn til að vista?

Nokkrar ástæður geta verið fyrir því að geta ekki séð táknið fyrir vistun og valmyndina ásamt yfirlitum á afmörkunarsvæðinu.

Ein ástæðan gæti verið sú að sérstilling er ekki virk fyrir notandahlutverkið þitt. Í slíku tilfelli ertu enn með aðgang að kerfisyfirlitum sem eru staðlaður hluti síðanna. Hægt er að breyta þessum yfirlitum, t.d. með því að breyta eða bæta við síum. Þú bara getur ekki vistað breytingarnar. Önnur ástæða gæti verið sú að síðan sem þú ert að skoða er síða af gerðinni *vinnublað* en &mdash;ekki listi.

### <a name="on-which-page-types-can-i-use-list-views"></a>Á hvaða síðugerðum get ég notað listayfirlit?

Yfirlit eru aðeins í boði á listasíðum.

### <a name="how-do-i-know-whether-im-on-list-type-page"></a>Hvernig veit ég hvort ég er á síðu sem er listasíða

Notaðu síðueftirlitið. Til að opna síðueftirlit skal ýta á Ctrl+Alt+F1. Því næst skal í reitnum **Síða** leita að orðinu **Listi** í sviganum í lokin.

### <a name="are-views-also-available-on-other-form-factors"></a>Eru yfirlit einnig tiltæk á öðrum formeiginleikum?

Já. Öll yfirlit sem þú vistar í tölvuvafra eða skjáborðsforrit eru einnig í boði í töflu eða snjallsíma. Ekki er hægt að breyta eða sérsníða yfirlit í fartækjum.

### <a name="are-my-personal-views-always-accessible"></a>Eru persónuleg yfirlit mín alltaf aðgengileg?

Yfirlitin þín eru tiltæk á listasíðu hvort sem þú ferð inn á hana í gegnum yfirlitsvalmyndina með því að nota glugga **Viðmótsleitar** eða í gegnum tengil vefslóðar. Yfirlit eru ekki tiltæk í listahlutum, uppflettingum eða þegar listasíða birtist sem gluggi.

### <a name="how-do-i-return-a-view-to-its-original-filters-after-modifying-them"></a>Hvernig set ég yfirlit í upprunalegar síur eftir að þeim hefur verið breytt?

Neðst í síuglugganum skal velja **Endurstilla síur** aðgerðina til að hreinsa síunarbreytingar sem gerðar hafa verið á yfirlitinu og snúa aftur í upprunalegt afmarkað svæði og síuskilyrði.

### <a name="what-is-the-difference-between-hiding-and-removing-views"></a>Hver er munurinn á því að fela og fjarlægja yfirlit?

Yfirliti er eytt varanlega þegar það er fjarlægt. Með því að fela yfirlit er hægt að fela það tímabundið á afmörkunarsvæði, en hægt er að opna það aftur síðar með því að velja aðgerðina **Sýna**.

### <a name="how-can-i-share-my-views-with-others"></a>Hvernig deili ég yfirliti mínu með öðrum?

[!INCLUDE[prod_short](includes/prod_short.md)] býður ekki upp á að deila nákvæmu listayfirliti. En hægt er að deila núverandi síum þannig að aðrir notendur geti séð sams konar lista yfir færslur. Í vafra tölvunnar skal einfaldlega afrita vefslóðina og deila henni með samstarfsmönnum. Ekki er tryggt að samnýting á síum gefi viðtakandanum sömu síur og þú sérð í vafranum þínum.

### <a name="can-i-search-for-views-in-the-tell-me-window"></a>Get ég leitað að yfirlitum í glugganum „Viðmótsleit“?

Fj. Glugginn **Viðmótsleit** sýnir aðeins leitarniðurstöður fyrir síðuna en er einu skrefi frá því að sækja í eftirlætisyfirlitið þegar farið er á síðuna.

### <a name="what-is-shared-layout"></a>Hvað er samnýtt útlit?

Öll yfirlit á listasíðu deila sameiginlegri dálkauppsetningu. Útlitið felur í sér hvaða dálkar eru sýndir, röð þeirra, breidd, fast svæði og stillingar flýtifærslu. Þegar hluti dálkaútlitsins er sérstillt hefur það einnig áhrif á önnur yfirlit sem samnýta sama útlit á listasíðunni.

Sum kerfisyfirlit geta haft einkvæm yfirlit á dálkum á listanum. Til dæmis var hægt að endurraða dálkum aftur til að birta aðeins þá dálka sem mest eiga við það yfirlit. Hægt er að greina hvaða yfirlit hafa einkvæmt útlit með því að velja ![Sýna fleiri valkosti](media/show-more-options-icon.png "Sýna fleiri valkosti") táknið og fylgjast með því að gátreiturinn **Samnýtt útlit** sé ekki valinn. Sem notandi er hægt að sérstilla dálkútlitið fyrir yfirlit með einkvæmu útliti án þess að það hafi áhrif á önnur yfirlit á listasíðunni. Aðeins þróunaraðilar geta skilgreint einkvæma dálkauppsetningu fyrir yfirlit sem er með samnýtt útlit í upphafi.

### <a name="what-does-the-show-system-filters-link-do"></a>Hvað gerir tengillinn Sýna kerfisafmarkanir?

Á sumum listasíðum birtir síusvæðið **Sýna kerfisafmarkanir** neðst, sérstaklega þegar síðan inniheldur síur sem kerfið hefur tilgreint. Þessar sérstöku síur eru yfirleitt notaðar til að birta færslur sem eru byggðar á núverandi samhengi. Dæmi um þetta er þegar sía þarf pantanalista fyrir tiltekinn viðskiptamann.

Kerfissíur eru stilltar af þróunaraðila sem þeir gera með því að nota síuflokkinn 0. Frekari upplýsingar um kerfissíur er að finna í [Aðferð FilterGroup](/dynamics365/business-central/dev-itpro/developer/methods-auto/record/record-filtergroup-method).

### <a name="i-see-multiple-views-on-my-page-but-i-didnt-create-them-where-did-they-come-from"></a>Ég sé mörg yfirlit á síðunni minni, en ég bjó þau ekki til. Hvaðan komu þau?

Yfirlitin sem birtast á öllum listum eru samandregin persónuleg yfirlit þín ásamt kerfisskoðunum. Kerfisyfirlit kunna að koma úr viðskiptaforritinu, úr viðbótum eða kunna að vera sértæk ef listinn var sérsniðinn fyrir hlutverkið þitt.

### <a name="why-do-some-views-provide-fewer-options"></a>Hvers vegna eru sum yfirlit með færri valkosti?

Sum yfirlit bjóða aðeins upp á valkostinn að vista afrit af yfirlitinu, á meðan aðrir leyfa ekki að breytingar á yfirlitinu séu vistaðar. Það hvernig yfirlitið var búið til ákvarðar valmöguleikana sem eru tiltækir fyrir það yfirlit. Hægt er að búa til yfirlit á marga vegu:

- Persónuleg yfirlit sem þú vistaðir
- Kerfisyfirlit sem eru staðlaður hluti viðskiptaforrits, eða bætt við af viðbótum eða hlutverkatilgreindum yfirlitum. Ólíkt persónulegum yfirlitum er ekki hægt að vista breytingar á síum aftur í það kerfisyfirlit.
- Eldri kerfisyfirlit sem eru staðlaður hluti viðskiptaforrits en voru stofnuð með eldri útgáfum af [!INCLUDE[prod_short](includes/prod_short.md)]. Þessi yfirlit bjóða upp á færri valkosti. Aðeins er hægt að vista þau sem nýtt yfirlit og ekki er hægt að fela þau eða endurraða þeim. Ekki verður boðið upp á eldri kerfisyfirlit við uppfærslu í framtíðinni á [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="how-do-i-convert-legacy-system-views"></a>Hvernig umbreyti ég eldri kerfisyfirlitum?

Eldri kerfisyfirlit eru listayfirlit sem þróunaraðilar hafa stofnað í eldri útgáfum af [!INCLUDE[prod_short](includes/prod_short.md)] með því að setja þær á síðuna Mitt hlutverk. Þessi yfirlit eru nú birt beint á listasíðunni en bjóða upp á færri sérstillingar og færri valmöguleika. Hægt er að breyta eldra kerfisyfirliti í persónulegt yfirlit sem er fullkomlega sérstillanlegt, einfaldlega með því að vista það sem eldra yfirlit. Á sama hátt geta stjórnendur valið að umbreyta eldri kerfisyfirlitum sem bundin eru við tiltekin hlutverk með því að sérsníða notandahlutverkið og vista eldri yfirlitið sem nýtt yfirlit yfir hlutverkaleik.

Ekki verður boðið upp á eldri kerfisyfirlit við uppfærslu í framtíðinni á [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="others-in-my-organization-need-similar-list-views-as-standard-what-can-i-do"></a>Aðrir í fyrirtækinu mínu þurfa svipuð listayfirlit sem stöðluð yfirlit. Hvað get ég gert?

Vinna með persónuleg yfirlit eru fljótvirk og árangursrík en [!INCLUDE[prod_short](includes/prod_short.md)] býður upp á viðbótarverkfæri til að skilgreina listayfirlit sem tiltekin notandahlutverk eða allir notendur í fyrirtækinu.
 - Forritarar geta sérstillt umhverfið og stofnað listayfirlit í viðbótum fyrir alla notendur í fyrirtækinu.
 - Þeir sem ekki kóða, á borð við stjórnendur eða deildarstjórnendur, hægt er að búa til lista yfir hlutverk sem eru sértækir þegar hlutverk er sérsniðið á síðunni **Forstillingar (hlutverk)**.

### <a name="i-work-with-multiple-languages-how-do-i-translate-the-name-of-the-view"></a>Ég vinn með mörg tungumál: Hvernig þýði ég heiti yfirlitsins?

Þegar nýtt yfirlit er vistað eða fyrirliggjandi yfirlit endurnefnt verður að færa inn þekkjanlegt og merkingarbært heiti fyrir það yfirlit. Heitið er vistað fyrir núverandi tungumál og birtist einnig þegar notandi eða aðrir notendur vinna með [!INCLUDE[prod_short](includes/prod_short.md)] á mismunandi tungumálum. Til gefa upp þýdd heiti skal skipta um tungumál með því að nota síðuna **Mínar stillingar**. Því næst skal endurnefna yfirlitið sem geymir þýtt heiti á nýja tungumálinu.

### <a name="do-views-with-expressions-work-in-all-languages"></a>Virka yfirlit með segðir á öllum tungumálum?

Segðir sem nota aðeins tákn, t.d. `|` eða `..` eru taldar öruggar fyrir notendur að opna á öllum tungumálum. Öll yfirlit með segðir sem innihalda bókstafi, leitarorð eða síumerki virka aðeins fyrir tungumálið þar sem þær voru heimilar.

### <a name="see-also"></a>Sjá einnig

[Vista og sérsníða listayfirlit](ui-views.md)  
[Að finna eiginleika og upplýsingar](ui-search.md)  
[Röðun, leit, og síun](ui-enter-criteria-filters.md)  
