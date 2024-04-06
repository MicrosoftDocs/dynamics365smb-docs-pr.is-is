---
author: brentholtorf
ms.topic: include
ms.date: 03/12/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
Hægt er að nota áminningar til að minna viðskiptamenn á gjaldfallnar upphæðir. Einnig er hægt að nota áminningar til að reikna út vexti og annan kostnað og hafa þær upplýsingar með í áminningunni.

> [!TIP]
> Upplýsingarnar í þessari grein eru nákvæmar en hún lýsir aðallega handvirku ferli. [!INCLUDE [prod_short](prod_short.md)] býður upp á verkfæri sem hægt er að nota til að gera ferli við stofnun, útgáfu og sendingu innheimtubréfa sjálfvirka. Með því að gera þessi skref sjálfvirkt er hægt að spara umtalsverðan tíma sem eytt er í söfn. Nánari upplýsingar eru notaðar til að [fara í Innheimtubréf sjálfvirkt í söfnum](../finance-automate-reminders.md).

Áður en hægt er að stofna áminningar þarf að setja upp skilmála áminninga og tengja þá við viðskiptamenn. Frekari upplýsingar eru í [Setja upp skilmála og stig innheimtubréfa](../finance-setup-reminders.md). [!INCLUDE [reminder-terms](reminder-terms.md)] Innihald síðunnar **Vaxtaskilmálar** ákveður hvort vextir eru reiknaðir í áminningunni.  

Hægt er að keyra reglulega keyrsluna **Stofna innheimtubréf** til að stofna áminningar fyrir alla viðskiptamenn með gjaldfallnar skuldir eða stofna áminningu handvirkt fyrir einstaka viðskiptamenn og láta reikna línurnar og fylla þær út sjálfvirkt.  

Þegar búið er að stofna áminningarnar er hægt að breyta þeim. Textinn sem birtist í upphafi og í lok áminningar ræðst af áminningarstiginu og hægt er að sjá hann í dálknum **Lýsing**. Ef reiknuð upphæð hefur verið sett inn sjálfvirkt í upphafs- eða lokatextann verður textinn ekki leiðréttur ef línunum er eytt. Þá verður að nota aðgerðina **Uppfæra áminningu**.  

Viðskiptamannsfærsla með reitinn **Bið** útfylltan leyfir ekki stofnun áminningar. En ef áminning er stofnuð á grunni annarrar færslu verður gjaldfallin færsla merkt í bið einnig höfð með í áminningunni. Vextir eru ekki reiknaðir á línur með þessum færslum.

Þegar búið er að stofna áminningar, og breyta þeim ef þarf, er hægt að prenta prufuskýrslur eða senda áminningarnar, vanalega sem tölvupóst.

### <a name="to-create-a-reminder-automatically"></a>Innheimtubréf búin til sjálfvirkt:

Innheimtubréf líkist reikningi. Þegar innheimtubréf er búið til þarf að fylla út innheimtuhaus ásamt einni eða fleiri innheimtulínum. Þú getur notað aðgerð til að stofna innheimtubréf fyrir alla viðskiptamenn sjálfvirkt.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 0.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innheimtubréf** og velja síðan viðkomandi tengil.
2. Á síðunni **Innheimtubréf**, skal velja aðgerðina **Stofna innheimtubréf**.
3. Á síðunni **Stofna innheimtubréf** fyllið út reitina til að skilgreina hvernig og til hvaða aðila innheimtubréfin skulu stofnuð.
4. Velja hnappinn **Í lagi**.

### <a name="to-create-a-reminder-manually"></a>Innheimtubréf búin til handvirkt:

Á síðunni **Innheimtubréf** geturðu fyllt í flýtiflipann **Almennt** handvirkt og svo látið fylla í línurnar sjálfvirkt.

1. Veldu ![Ljósapera sem opnar eiginleika viðmótsleitar aftur 2.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innheimtubréf** og velja síðan viðkomandi tengil.
2. Valið er aðgerðin **Nýtt**.
3. Fyllt er út í reiti eftir því sem er nauðsynlegt í flýtiflipanum **Almennt**.
4. Veljið aðgerðina **Leggja til innheimtubr.línur**.
5. Í runuvinnslunni **Leggja til innheimtubr.línur** skal fylla út reitina til að skilgreina hvernig og til hvaða aðila innheimtubréfin skulu stofnuð.
6. Veljið gátreiturinn **Taka færslur í bið með** ef á áminningum eiga að birtast opnar færslur gjaldfallnar í bið.
7. Veldu gátreitinn **Aðeins færslur með gjaldföllnum upphæðum** ef þú vilt að áminningarnar innihaldi aðeins opnar færslur sem eru komnar fram yfir á tíma. Aðeins reikningar og greiðslur verða sýndar þar sem þetta eru færslurnar þar sem greiðslur viðskiptamanna kunna að vera gjaldfallnar.

    > [!Important]
    > Opnar færslur sem eru á bið verða settar inn, þrátt fyrir stillingar í gátreitur **Aðeins færslur með gjaldföllnum upphæðum**.

8. Velja hnappinn **Í lagi**.

### <a name="to-replace-reminder-texts"></a>Texta innheimtubréfs skipt út.

Nokkrar leiðir eru í boði til að ákvarða hvaða texti birtist á prentuðu innheimtubréfi. Í einstaka tilvikum gæti þurft að skipta út byrjunar- og endatexta gildandi stigs með texta af öðru stigi.

1. Veldu ![Ljósapera sem opnar eiginleika viðmótsleitar í enn eitt skiptið 3.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innheimtubréf** og velja síðan viðkomandi tengil.
2. Opna skal viðeigandi innheimtubréf, og síðan velja **uppfæra innheimtubréf texti** aðgerðina.
3. Á síðunni **uppfæra innheimtubréf texti** er fært inn stigið sem óskað er eftir í reitnum **Stig innheimtubréfs**.
4. Velja hnappinn **Í lagi** til að uppfæra byrjunar- og endatexta.

### <a name="to-issue-a-reminder"></a>Gefa út innheimtubréf

Þegar búið er að stofna áminningar, og breyta þeim ef þarf, er hægt að prenta prufuskýrslur eða senda áminningarnar.

Þegar áminning er send eru gögnin flutt á sérstaka síðu fyrir sendar áminningar. Um leið eru áminningarfærslurnar bókaðar. Ef vextir eða viðbótarkostnaður hefur verið reiknaður eru færslur bókaðar í viðskiptamannabók og á fjárhag.

Þegar innheimtubréf er sent bókar kerfið færslur eftir því sem var tilgreint á síðunni **Skilmálar innheimtubréfa**. Þessi staðall ákvarðar hvort vextir og/eða viðbótargjöld séu bókuð á reikning viðskiptamanns og fjárhag. Uppsetning á síðunni **Bókunarflokkar viðskiptavinar** ákvarðar á hvaða reikninga er bókað.

Fyrir hverja fjárhagsfærslu viðskiptamanns á vaxtareikning, er stofnuð færsla á síðunni **Innheimtubréf/vaxtafærslur**.

Ef gátreitirnir **Bóka vexti** og **Bóka viðbótargjöld** eru valdir á síðunni **Skilmálar innheimtubréfs**, eru eftirfarandi færslur einnig stofnaðar:

- Ein færsla á síðunni **Fjárhagsfærslur viðskiptamanna**
- Ein útistandandi færsla í viðeigandi fjárhagsreikningi
- Ein vaxta- og/eða viðbótargjaldsfærsla í viðeigandi fjárhagsreikningi

Að auki getur sending innheimtubréfs leitt af sér VSK-færslur.

1. Veldu ![Ljósapera sem opnar eiginleika viðmótsleitar einnig hér 4.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innheimtubréf** og velja síðan viðkomandi tengil.
2. Velja skal viðeigandi innheimtubréf, og síðan velja **Senda út** aðgerðina.
3. Á síðunni **Senda út innheimtubréf** þarf að fylla reitina út eftir þörfum.
4. Velja hnappinn **Í lagi**.

Innheimtubréfið er annað hvort prentað út eða sent á tiltekið netfang sem PDF viðhengi.

### <a name="to-cancel-an-issued-reminder"></a>Hætta við útgefið innheimtubréf

Ef innheimtubréf voru gefin út fyrir mistök er hægt að hætta við þau áður en þau eru send út. Þetta er hægt að gera annaðhvort fyrir hvert bréf fyrir sig eða í lotu.

1. Á síðunni **Send innheimtubréf** skal velja eina eða fleiri línu fyrir send innheimtubréf sem á að hætta við og velja svo aðgerðina **Hætta við**.
2. Á síðunni **Hætta við útgefnar áminningar** skal fylla út reitina eftir þörfum og velja síðan hnappinn **Í lagi**.


