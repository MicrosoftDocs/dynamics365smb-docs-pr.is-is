---
title: Hönnunarupplýsingar - Endurpöntunarstefnur | Microsoft Docs
description: Þetta efnisatriði gefur yfirlit yfir stefnur varðandi vöruáfyllingar.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 1212c6f2f7e9da03a15c7fb39496d85869ef3e73
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1238648"
---
# <a name="design-details-reordering-policies"></a>Hönnunarupplýsingar: Endurpöntunarstefnur
Endurpöntunarstefnur skilgreina hversu mikið þarf að panta þegar vara þarf að vera fyllt á. Fjórir mismunandi endurröðunarstefnur eru til.  

## <a name="fixed-reorder-qty"></a>Fast endurpöntunarmagn
Stefnan Fast endurpöntunarmagn tengist birgðaáætlanagerð á dæmigerðum C-vörum (lágur birgðakostnaður, lítil hætta á úreldingu og / eða mörgum vörum). Þessi stefna er yfirleitt notað í tengslum við pöntunarmark endurspeglar fyrirsjáanlegs eftirspurn meðan á afhendingartími vörunanr stendur.  

### <a name="calculated-per-time-bucket"></a>Reiknuð fyrir hvern tímaramma  
 Ef áætlanakerfið greinir að endurpöntunarmarkinu hafi verið náð eða farið yfir það innan tiltekins tímaramma (endurpöntunarferli) – yfir eða við endurpöntunarmarkið í upphafi tímabilsins og undir því eða við það í lokin – leggur það til stofnun nýrrar birgðapöntunar á tilgreinda endurpöntunarmagninu og áætlar það áfram frá fyrstu dagsetningunni eftir lok tímarammans.  

 Hugtakið um hólfað endurpöntunarmark dregur úr fjölda framboðstillaga. Þetta endurspeglar handvirkt ferli af því að fara oft inn á lager til að athuga raunverulegt innihald í hinum ýmsu hólfum.  

### <a name="creates-only-necessary-supply"></a>Stofanr aðeins nauðsynlegar birgðir  
 Áður en ný birgðapöntun er lögð til til að mæta endurpöntunarmarki, kannar áætlanakerfið hvort framboð hafi verið pantað eða móttekið innan afhendingartíma vörunnar. Ef núverandi birgðapöntun leysir vandamálið með því að færa áætlaðar birgðir að eða yfir endurpöntunarmarkið innan afhendingartímans leggur kerfið ekki til nýja birgðapöntun.  

 Birgðapantanri sem eru búnar til sérstaklega til að mæta pöntunarmark er útilokuð frá venjulegum framboðsjöfnun, og mun ekki á nokkurn hátt hægt að breyta eftirá. Þar af leiðandi, ef á að áfangaskipta út vöru með endurpöntunarmarki (ekki endurnýja) er ráðlegt að endurskoða útistandandi birgðapantanir handvirkt eða breyta endurpöntunarstefnu í Lotu fyrir lotu, þannig að kerfið dragi úr eða afturkalli umframbirgðir.  

### <a name="combines-with-order-modifiers"></a>Samsett við Breytingalykla  
 Pantanabreytingarnar, Lágmarksmagn pöntunar, Hámarksmagn pöntunar og Margföld pöntun, ættu ekki að gegna stóru hlutverki þegar notuð er stefnan um fast pöntunarmagn. Hins vegar reiknar áætlanakerfið enn með þessum breytingalyklum og minnkar magnið í tilgreint hámarkspöntunarmagn (og býr til tvær eða fleiri birgðir til að ná heildarpöntunarmagninu), eykur pöntunina í tilgreint lágmarkspöntunarmagn, eða námundar pöntunarmagnið upp til að ná tiltekinni margfaldri pöntun.  

### <a name="combines-with-calendars"></a>Sameinast dagbók  
 Áður en ný birgðapöntun er lögð til að mæta endurpöntunarmarki, kannar áætlanakerfið hvort pöntunin sé áætluð á frídegi, samkvæmt öllum dagatölum sem eru skilgreind í **Grunndagatalskóði** reitnum á síðunni **Fyrirtækjaupplýsingar** og **Birgðageymslukort**.  

 Ef fyrirhuguð dagsetning er frídagur, færir áætlanakerfið pöntunina áfram á næsta virka dag. Þetta getur orsakað pöntun sem uppfyllir endurpöntunarmark en uppfyllir ekki einhverja tiltekna eftirspurn. Fyrir svona ójafna eftirspurn, býr áætlanakerfið til auka framboð.  

### <a name="should-not-be-used-with-forecast"></a>Ætti ekki að nota við spá  
 Þar sem væntalega eftirspurn er þegar lýst í endurpöntunarmarki er ekki nauðsynlegt að spá í að skipuleggja hlut með endurpöntunarmarki. Ef það er viðeigandi að byggja áætlun á spá skal nota stefnuna lotu-fyrir-lotu.  

### <a name="must-not-be-used-with-reservations"></a>Má ekki nota með frátekningu  
 Ef notandi hefur tekið frá magn, til dæmis magn í birgðum fyrir einhverja fjarlæga eftirspurn, truflar það forsendur áætlunarinnar. Jafnvel þótt áætlað birgðastig sé leyfilegt með tilliti til endurpöntunarmarks, má magnið ekki vera til staðar vegna frátekningarinnar. Kerfið kann að reyna að bæta það upp með því að stofna frávikspantanir. Þó er mælt með því að reiturinn Taka frá sé stilltur á Aldrei fyrir vörur sem eru planaðar með endurpöntunarmarki.

## <a name="maximum-qty"></a>Hámarksmagn
Reglan um hámarksmag er ein leið til að viðhalda birgðum með því að nota endurpöntunarmark.  

Allt sem gildir um stefnu endurpöntunarmagns gildir einnig um þessa stefnu. Eini munurinn er magnið sem lagt er til sem framboð. Þegar reglan um hámarksmagn rer notuð verður endurpöntunarmagnið skilgrein á virkan hátt samkvæmt ætluðu birgðastigi og verður því yfirleitt mismunandi eftir pöntunum.  

### <a name="calculated-per-time-bucket"></a>Reiknuð fyrir hvern tímaramma  
Endurpöntunarmarkið er ákvarðað á þeim tímapunkti (við lok tímaramma) þegar áætlanakerfið greinir að farið hefur verið yfir endurpöntunarmark. Á þessum tíma mælir kerfið bilið frá núverandi áætlaðar birgðum upp að tilteknum hámarksbirgðum. Þetta stendur fyrir magnið sem þarf að endurpanta. Kerfið kannar þá hvort birgðir hafi þegar verið pantaðar annars staðar þannig að þær berist innan afhendingartímans og, ef svo er, minnkar magn nýju birgðapöntunarinnar í samræmi við það magn sem þegar hefur verið pantað.  

Kerfið tryggir að áætlaðar birgðir nái a.m.k. endurpöntunarmarkinu - ef vera skyldi að notandinn hafi gleymt að tilgreina hámarksbirgðagildi.  

### <a name="combines-with-order-modifiers"></a>Samsett við Breytingalykla  
Það fer eftir uppsetningu, getur það verið best að sameina það hámarksmagn stefnu með breytingalyklum til að tryggja lágmarksupphæð þess magn eða sléttun innkaupaeiningar, eða kljúfa það í fleiri lotur samkvæmt skilgreiningu hámarksmagns.  

### <a name="combines-with-calendars"></a>Sameinast dagbók  
Áður en ný birgðapöntun er lögð til að mæta endurpöntunarmarki, kannar áætlanakerfið hvort pöntunin sé áætluð á frídegi, samkvæmt öllum dagatölum sem eru skilgreind í **Grunndagatalskóði** reitnum á síðunni **Fyrirtækjaupplýsingar** og **Birgðageymslukort**.  

Ef fyrirhuguð dagsetning er frídagur, færir áætlanakerfið pöntunina áfram á næsta virka dag. Þetta getur orsakað pöntun sem uppfyllir endurpöntunarmark en uppfyllir ekki einhverja tiltekna eftirspurn. Fyrir svona ójafna eftirspurn, býr áætlanakerfið til auka framboð.

## <a name="order"></a>Pöntun
Í framleiða eftir pöntun umhverfi, er vara keypt eða framleidd til eingöngu ná ákveðna eftirspurn. Venjulega tekur hún til A-vara og ástæða fyrir að velja Endurpöntunarstefnu pöntunar getur verið að eftirspurn er hverfandi, sem afhendingartími er óveruleg, eða nauðsynlegar eigindir mismunandi.  

Forritið stofnar pöntun-við-pöntun tengsl sem virka sem undirbúningstengsl milli framboðsins, birgðapöntunar eða birgða og eftirspurnarinnar sem henni er ætlað að mæta.  

Burtséð frá notkun pöntunarstefnu er hægt að nota tengil á milli pantana í áætlun með eftirfarandi hætti:  

* Þegar reglan framleiðsla eftir pöntun er notuð til að stofna margþrepa framleiðslupöntun eða framleiðslupöntun af gerðinni verk (nauðsynlegir íhlutir framleiddir samkv. sömu framleiðslupöntun).  
* Þegar búnaðurinn Sölupantanaáætlun er notaður til að stofna framleiðslupöntun úr sölupöntun.  

Jafnvel þótt framleiðslufyrirtæki álíti sig framleiða eftir pöntun geur verið best að nota endurpöntunarstefnuna lota fyrir lotu ef vörurnar eru staðlaðar án afbrigða í eigindum. Niðurstaðan er að kerfið mun nota óáætlaðar birgðir og safna aðeins sölupöntunum með sömu afhendingardagsetningu eða innan tilgreinds tímaramma.  

### <a name="order-to-order-links-and-past-due-dates"></a>Tenglar á milli pantana og liðnir skiladagar  
Ólíkt flestum framboð-eftirspurn settum eru tengdar pantanir með skiladag á undan upphafsdagsetningu áætlunar áætlaðar að fullu af kerfinu. Viðskiptaástæðan fyrir þessa undanþágu er að tiltekin pör eftirspurnar og framboðs þurfa að vera samstillt fram að framkvæmdinni. Nánari upplýsingar um frosna svæðið sem eiga við um flestar gerðir framboðs og eftirspurnar eru í [Hönnunarupplýsingar: Takast á við pantanir fyrir upphafsdagsetningu áætlunar](design-details-dealing-with-orders-before-the-planning-starting-date.md).

## <a name="lot-for-lot"></a>Lotu-fyrir-lotu
Lota-fyrir-lotu reglan er sveigjanlegust vegna þess að kerfið bregst bara við raunverulegri eftirspurn og bregst auk þess við væntanlegri eftirspurn samkvæmt spám og standandi pöntunum og ákvarðar svo magn pantanan á grundvelli eftirspurnarinnar. Lota-fyrir-lotu reglan beinist að A- og B-vörum þar sem hægt er að samþykkja birgðir en ætti helst að forðast það.  

Að sumu leyti er lota fyrir lotu stefnan eins og pantanastefnan en er með almenna nálgun á vörur; það getur samþykkt magn í birgðum, og það flokkareftirspurn og samsvarandi framboð í tímarömmum skilgreindum af notanda.  

Tímaramminn er skilgreindum í reitnum **Tímarammi**. Kerfið vinnur með lágmarks tímaramma upp á einn dag, þar sem það er minnsta tímamælieining fyrir birgðir og eftirspurn í kerfin (þó svo að í raun geti tímamælieining á framleiðslupöntunum og íhlutaþörfum verið sekúndur).  

Tímaramminn setur einnig takmörkun á það hvenær birgðapöntun er enduráætluð til að mæta tiltekinni eftirspurn. Ef framboð er innan tímarammans verður það enduráætlað inn eða út til að svara eftirspurninni. Annars, ef það liggur fyrr, mun það valda óþarfa uppsöfnun birgða og ætti að afturkalla. Ef það er síðar verður nýtt framboð stofnað í staðinn.  

Með þessari reglu er einnig mögulegt að skilgreina öryggisbirgðir til að bæta upp hugsanlegar sveiflur á birgðum eða til að mæta skyndilegri eftirspurn.  

Þar sem birgðapöntunarmagn byggir á raunveruleg eftirspurn getur það borgað sig að nota raðabreytur: slétta pöntunarmagn til að það passi við tiltekna pöntunarstuðul (eða innkaupamælieiningu), auka pöntuina upp í tiltekið magn, eða minnka magnið í hámarksmagn (og því búa til tvær eða fleiri birgðir til að uppfylla allt magnið).

## <a name="see-also"></a>Sjá einnig  
[Hönnunarupplýsingar: Áætlunarfæribreytur](design-details-planning-parameters.md)   
[Hönnunarupplýsingar: Meðhöndlun endurpöntunarstefna](design-details-handling-reordering-policies.md)   
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)
