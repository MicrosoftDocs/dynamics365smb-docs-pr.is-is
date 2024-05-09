---
title: Sérstilling síðna (myndskeið)
description: Kynntu þér hvernig á að sérstilla notendaviðmótið og aðlaga vinnusvæðið þitt til að henta því hvernig þú vinnur í Business Central.
author: jswymer
ms.topic: conceptual
ms.service: dynamics-365-business-central
ms.custom: bap-template
ms.reviewer: jswymer
ms.search.keywords: 'customize, personalize, personalization, hide columns, remove fields, move fields, resize column, change column width'
ms.search.form: '9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 01/15/2024
ms.author: jswymer
---
# Sérsníða vinnusvæðið

Þú getur sérstillt vinnusvæðið þitt þannig að það falli betur að vinnunni og óskum þínum. Breyta síðum þannig að þær birti einungis upplýsingarnar sem þú þarfnast þegar þú þarfnast þeirra. Sérstilling hefur aðeins áhrif á vinnusvæðið. Það breytir ekki vinnu annarra. Hægt er að sérstilla allar gerðir síðna, þar á meðal síðuna [Mitt hlutverk](ui-change-basic-settings.md#role-center) .

> [!NOTE]
> Vegna takmarkana á hönnunargetu í vefbiðlara er ekki hægt að sérstilla eða sérstilla eftirlit innan `grid` og `fixed` málskipan.
Það á við um allar hönnunarstillingar, ekki bara sérstillingu.

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

Hægt er að gera ýmsar breytingar, svo sem að færa eða fela reiti, dálka, aðgerðir og hluta í heild sinni og bæta nýjum reitum við. Mestan hluta sérstillingar þarf að gera með því að fyrst virkja borðann **Sérstilling**. Hægt er að gera einfaldar breytingar, svo sem dálkbreidd, strax á hvaða lista sem er.

> [!NOTE]
> Stjórnendur geta breytt sömu útliti og notendur með því að sérstilla forstillingu (hlutverk) sem mörgum notendum er úthlutað. Til að fá nánari upplýsingar um síður hlutverka er farið í [Sérstilla síður fyrir hlutverk](ui-personalization-manage.md)<br /><br />
Stjórnendur geta einnig hnekkt eða slökkt á sérstillingu notenda og hægt er að skilgreina hvaða eiginleikar eru tiltækir fyrir notendur til að sjá í öllum eða tilteknum fyrirtækjum. Frekari upplýsingar eru í [Sérstilling Business Central](ui-customizing-overview.md).

## Myndband

Eftirfarandi myndband sýnir nokkrar af þeim leiðum sem hægt er að sérsníða hlutverkamiðstöð notanda.

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4ArUB?rel=0]

## Breyta breidd á dálki

Þú getur auðveldlega breytt stærð dálka á hvaða lista sem er. Dragðu bara mörkin milli tveggja dálka til vinstri eða hægri.  

1. Í haus lista skal velja og draga mörkin á milli tveggja dálka.
2. Einnig er hægt að tvísmella á mörkin milli tveggja dálka til að gera breidd dálksins sjálfvirka. Breiddin lagast að kjörstærð fyrir læsileika.

Eins og fyrir aðrar sérstillingar eru breytingarnar sem gerðar eru á breidd dálks geymdar á reikningnum þínum og fylgja þér, sama hvaða tæki þú notar til að skrá þig inn.

## Hefja sérstillingu með því að nota sérstillingarstillinguna

1. Opna skal síðuna sem á að sérsníða.
1. Í efra hægra horninu skaltu velja táknið ![Stillingar.](media/ui-experience/settings_icon_small.png "Stillingatákn fyrir hlutverkamiðstöð") og síðan velja aðgerðina **Sérstilla**.

    Borðinn **Sérstillir** birtist efst til að tákna að hægt sé að byrja að gera breytingar.

    > [!NOTE]
    > Til að fletta í sérstillingunni er <kbd>Ctrl</kbd>+<kbd>Smellt á</kbd> í aðgerð ef örvarhausinn auðkenndir hana.

    Ef þú sérð ![Lás sérstillingar](media/personalization-lock-icon.png "Sérstilla lás") eða ![Sérstilling útilokuð](media/personalization-blocked-icon.png "Sérstilling útilokuð") á borðanum er ekki hægt að sérstilla síðuna. Frekari upplýsingar eru í [Af hverju er síða læst og því ekki hægt að sérsníða hana](ui-personalization-locked.md).

1. Til að breyta viðmótseiningu skal færa bendilinn á eininguna, eins og á aðgerð, reit eða hluta. Einingin er tafarlaust auðkennd með örvaroddi eða jaðri. Veldu eininguna og veldu annaðhvort **Færa**, **Fjarlægja**, **Fela**, **Sýna**, **Sýna undir „Sýna meira“**, **Sýna þegar fellt**, **Sýna alltaf**, **Stilla/hreinsa fast svæði** eða **Taka með/útiloka frá flýtifærslu**, allt eftir gerð og stöðu viðmótseiningarinnar.
1. Til að bæta við reit skal velja aðgerðina **+ Reitur**. Á svæðinu **Bæta reit við síðu** skal draga og sleppa reit í æskilega stöðu á síðunni.
1. Þegar lokið er við að breyta útliti **einnar eða fleiri síðna skal velja** hnappinn Gert á borðanum **Sérstilling** .

Frekari upplýsingar er að finna á [Hvað hægt er að sérstilla](#What).

## <a name="What"></a> Hvað er hægt að sérstilla

|Hvað viltu gera|Hvernig á að gera það|Athugasemdir|
|----|------------|-------|
|Færa eitthvað, eins og reit, dálk í lista, spjaldi, aðgerð eða hluta á annan stað á síðunni|Bentu hvar sem er á það sem þú vilt færa og dragðu það á nýja staðinn. Þykk lárétt lína gefur til kynna staðsetninguna.<br /><br />![Get ekki fært hingað tákn](media/personalization-cannot-move-here.png "Snið sérstillingar - Geta ekki fært hingað táknið") gefur til kynna að þú getir ekki fært eininguna yfir á valda staðsetningu.|Hlutar eru undirdeildir eða svæði á síðu sem innihalda hluti eins og marga reiti, aðra síðu, graf eða reiti.<br /><br />[Fá nánari upplýsingar um sérstillingu aðgerða](#Actions)<br>[Fræðast meira um sérstillingu hluta](#Parts)|
|Fela einingu sem birtist eins og reitur, dálkur í lista, spjaldi, aðgerð eða hluta.|Einingin er valin, örvarhaus valinn og fela <b>valið</b>.|Í sérstillingunni eru faldar aðgerðir gráar með skáletruðum texta og faldir hlutar skyggðir með skálínum. Faldir reitir og dálkar eru ekki tilgreindir beint á síðunni en hægt er að finna þá með því að nota <b>svæðið Bæta reit við síðu</b> ([fræðast um vinnureiti](#fields)).<br><br>Þegar sérstillingarstillingu er lokað hverfa allar einingar úr yfirliti. Ef reiturinn sem er feldur er einnig sýndur á haus flýtiflipa þegar flýtiflipinn er felldur saman birtist reiturinn ekki lengur þar.|
|Sýna aðgerð eða hluta sem er falinn núna|Til að skoða skyggða (falda) einingu skal velja örvaroddinn velja síðan <b>Sýna</b>.|Falinn hluti er aftur sýnilegur.|
|Bæta við reit sem er falinn núna|Á borðanum <b>Sérstilling</b> er aðgerðin <b>+ Reitur</b> valin.<br /></br>Svæðið <b>Bæta reit við síðu</b> opnast hægra megin á síðunni. Ef reitur er valinn á svæðinu birtist falin staðsetning á síðunni.<br /><br />Til að bæta við reit er hann dreginn af svæðinu eða frá faldri staðsetningu þess á staðinn sem hann á að fá. Staðsetningin er auðkennd annaðhvort með þykkri láréttri eða lóðréttri línu.<br><br> Önnur leið er að velja örvarhöfuð á faldri staðsetningu reitsins og velja **Sýna**. |Á hverri síðu eru fyrirfram skilgreindir reitir sem hægt er að velja að birta.<br /><br />[Fræðast meira um vinnusvæði](#fields) |
|Sýndu reit í haus flýtiflipa þegar hann er minnkaður.|Veldu örvaoddinn og veldu svo <b>Sýna þegar dregið saman</b>. <br /> <br />Ef þú sérð ekki þennan valkost er hann þegar stilltur. Í þessu tilfelli, til að hætta að sýna reitinn í haus flýtiflipans, skal velja <b>Sýna alltaf</b>.|*Flýtiflipi* er hugtakið sem er notað um flokk af reitum sem birtast undir sameiginlegri fyrirsögn. Notaðu valkostinn <b>Sýna þegar dregið saman</b> til að birta mikilvægustu reitina. Ef valinn er reitur í hausnum opnast flýtiflipinn og beinir sjónum að völdum reit.<br /><br />Þessi valkostur gildir aðeins ef síða er með fleiri en einn flýtiflipa. Ef aðeins einn flýtiflipi er í boði er ekki hægt að fella hann saman, þannig að valkosturinn <b>Sýna þegar fellt er</b> saman er ekki tiltækur.|
|Aðeins birta reit þegar þú velur **Sýna meira**.|Veldu örvaroddinn og <b>Sýna undir „Sýna meira“</b>.|Ef sýna er ekki <b>í "Sýna meira"</b> , þá er reiturinn þegar stilltur. Í þessu tilviki, til að láta reit alltaf sjást, ekki bara þegar þú velur **Sýna meira** skaltu velja <b>Sýna alltaf</b>.|
|Breyta því hvort hægt sé að breyta reit.|Velja skal reitinn, velja örvarhöfuð í reitnum og velja <b>svo Læsa breytingu</b> til að koma í veg fyrir að gildi reitsins sé breytt eða <b>Aflæsa</b> breytingum til að leyfa breytingar á gildi reitsins.|Aðeins er hægt að aflæsa reitum sem notandi hefur læst sjálfur. Sumir reitir eru sjálfgefið læstir, annaðhvort með hönnun eða með stjórnanda forstillingar sem hefur [sérsniðið síðuna](ui-personalization-manage.md). Ekki er hægt að aflæsa þessum reitum.|
|Breyta föstum svæði í lista í annan dálk. |Veldu örina í dálknum sem þú vilt nota sem síðasta dálk í festu svæði og veldu síðan <b>Stilla Fast svæði</b>.<br /><br/>Ef þú vilt stilla fasta svæðinu aftur á upphaflega staðsetningu skaltu velja örina fyrir fasta dálkinn og velja <b>Hreinsa Fast svæði</b>. Athugaðu: Ekki er hægt að fjarlægja þetta fasta svæði.|Frysta svæðið tilgreinir dálkana sem birtast alltaf vinstra megin á listanum, jafnvel þótt skrunað sé lárétt.|  
|Hoppa yfir reit þegar ýtt er á Enter.|Veldu örvaroddinn við hliðina á reitnum, eða dálkahaus í lista, og veldu **Útiloka frá flýtifærslu**.  | Ef ekki sést **Sleppa úr flýtifærslu** er reitnum þegar sleppt. Í þessu tilfelli, til að hætta að sleppa reitnum, skal velja **Hafa með í flýtifærslu**.<br><br>[Fræðast meira um flýtifærslu](ui-enter-data.md#QuickEntry)|
|Endurraða og fjarlægja yfirlit sem tákna síaða lista.|Veldu örvaoddinn við hliðina á yfirliti og veldu svo **Færa**, **Fjarlægja** eða **Fela**.|[Fá nánari upplýsingar um vistun og sérstillingu listayfirlita](ui-views.md)|  
|Bæta nýrri aðgerð við síðu eða skýrslu í Mitt hlutverk.|Af marksíðu, síður skýrslubeiðna eða glugga Viðmótsleitar skal velja bókamerkjatákn.|[Fræðast meira um bókamerkingarsíður og skýrslur](ui-bookmarks.md)|
|Byrja alltaf að birta listann sem stækkaðan eða dreginn saman|Veldu hnappinn **Stækka allt** eða **Draga allt saman** efst í vinstra horni listans. Einnig er hægt að velja aðgerðina **Stækka allt** eða **Draga allt saman** í valmynd fyrsta dálksins. |Á við um stiveldislista sem hægt er að fella saman|

## <a name="Actions"></a> Sérstilla aðgerðaslá og valmyndir

Sérstilling gerir þér kleift að ákveða hvaða aðgerðir á að sýna á yfirlits- og aðgerðarstikunni og í hlutverkamiðstöðvum og hvar á að sýna þær. Þú getur sýnt, falið eða fært stakar aðgerðir eða hóp aðgerða.

Eftirfarandi myndband sýnir hvernig hægt er að sérstilla aðgerðir á síðum og í „Mínu hlutverki“.

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE594m2]

Sérstilling yfirlits- og aðgerðarstika er einfaldlega gerð á sama hátt og á öðrum viðmótseiningum. Það sem þú hins vegar getur gert við aðgerð eða hóp aðgerða fer eftir því hvar aðgerðin eða hópur aðgerða er staðsettur. Besta leiðin til að komast að því er að fara í sérsnið og láta svo örvaoddinn leiðbeina þér.

Það eru nokkur hugtök sem þú ættir að kynna þér til að skilja betur sérstillingaraðgerðina: *aðgerðahópur* og *uppfærður flokkur*.  

*Aðgerðahópur* er eining sem víkkar út til að birta aðrar aðgerðir eða flokka. Til dæmis á síðunni **Sölupantanir** er einn aðgerðahópurinn aðgerðina **Virkni** sem birtist þegar þú velur aðgerðina **Aðgerðir**.

*Uppfærður flokkur* er aðgerðaflokkur sem birtist á undan lóðrétta línunni `|` á aðgerðastikunni. Flokkarnir innihalda yfirleitt algengustu aðgerðirnar sem eru notaðar, svo þú getir fundið þær fljótt. Til dæmis á síðunni **Sölupantanir** eru aðgerðirnar **Pöntun**, **Losun**, og **Bókun** uppfærðir flokkar.

> [!NOTE]  
> Til að hreinsa sérstillingu skal velja örvahausinn utan um hönnuðarvalmynd hlutans og velja **svo Hreinsa sérstillingu**.

### Fjarlægja, fela og sýna aðgerðir og aðgerðahópa

Þegar ætlunin er að sýna eða fela aðgerð skilgreina valkostirnir fyrir neðan örvaroddinn hvað sé hægt að gera miðað við ástand aðgerðarinnar. 

1. Veldu örvaoddinn fyrir aðgerð eða aðgerðahóp.
2. Einn af eftirfarandi valkostum er valinn:

|Valkostur|Það sem hann gerir|
|------|------------|
|**Fjarlægja**|Þessi valkostur birtist ef valin aðgerð er einnig sýnd einhvers staðar annars staðar í yfirlits- eða aðgerðarstikunni. Ef þessi valkostur er valinn eyðist aðgerðin úr valdri staðsetningu svo hún birtist ekki lengur. Aðgerðin eða aðgerðaflokkurinn er áfram í öðrum birgðageymslum. |
|**Fela**|Þessi valkostur birtist ef aðgerðin eða aðgerðahópurinn er ekki staðsettur á neinum öðrum stað í yfirlits- eða aðgerðarstikunni.  **Ef** þessi valkostur er valinn hverfa aðgerðin eða aðgerðahópurinn af yfirlitsstikunni eða aðgerðastikunni. Í sérstillingarstillingu er aðgerðin eða aðgerðaflokkurinn enn sýndur í núverandi stöðu, nema að hann birtist deyfður.|
|**Sýna**|Þessi valkostur birtist ef aðgerðin eða aðgerðaflokkurinn er falinn (deyfður). Ef þessi kostur er valinn birtist aðgerðin eða aðgerðahópurinn á yfirlitsstikunni eða aðgerðaslánni.|

### Færa aðgerðir og aðgerðahópa

Þar sem þú getur sleppt aðgerðum eða aðgerðahópum er það gefið í skyn með láréttri línu milli tveggja aðgerða eða ramma utan um aðgerðahóp. Eftirfarandi takmarkanir eru til staðar:

- Þú getur fært einstaka aðgerðir í uppfærða flokka, en þú getur ekki endurraðað röðuninni á aðgerðum í flokknum.
- Ekki er hægt að færa aðgerðahóp í uppfærðan flokk.

1. Til að færa aðgerð eða aðgerðahóp skaltu draga og sleppa honum á viðeigandi stað, rétt eins og með reiti og dálka.
2. Til að færa aðgerð eða aðgerðahóp í annan aðgerðahóp sem er tómur, dragðu aðgerðina eða aðgerðahópinn í nýja hópinn og slepptu honum í boxið **Sleppa aðgerð hér**.

### Um valmyndina Sjálfvirkt

- Ekki er hægt að fela eða færa **valmyndina Sjálfvirkt** eða **Power Automate** undirvalmynd og aðgerðir hennar.
- Þú getur flutt innifalin flæði undir atriðið **Sjálfvirkni**, en ekki er hægt að fela þau með sérstillingu. Ef flæðið er fært er flæðið afritað á áfangastaðarstað fjarlægir það það ekki úr vörunni **Sjálfvirkt** .

> [!TIP]
> Sem stjórnandi getur þú falið atriðið **Sjálfvirkni** fyrir notendum. Frekari upplýsingar er að finna á [Setja upp Power Automate samþættingu](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-setup).

## <a name="Parts"></a> Sérstilla hluta

Bent er á eða valið <kbd>Alt</kbd>+<kbd>Up Arrow</kbd> Varahlutir eru svæði á síðu sem eru yfirleitt settir saman úr mörgum reitum, myndritum eða öðru efni. Hluti sýnir litaðan ramma þegar þú fókusar á hlutann. Til dæmis er heimaskjár hlutverkamiðstöðvar með marga hluta. Vegna vel skilgreindra marka þeirra er hægt að sérsníða allan hlutann og innihald hans.

- Til að færa hluta skal draga og sleppa honum á æskilegan stað. Lituð lína gefur til kynna gildar stöður á skjánum. Til dæmis er aðeins hægt að færa FactBox við hlið annars FactBox á FactBox-svæðinu.
- Hægt er að fela hluta með því að velja valkostinn **Fela** undir örvaroddinum.
- Þegar byrjað er að sérstilla eða fletta að nýrri síðu birtast þeir hlutar sem eru faldir á síðunni með sérsniðnum sjónrænum hlutum sem gefa til kynna að þeir séu faldir. Hægt er að sýna þann hluta með því að velja valkostinn **Sýna** undir örvaroddinum.

Hægt er að hreinsa allar breytingar sérstillingar sem voru gerðar innan einstaks hlutar með því að velja valkostinn **Hreinsa sérstillingar** undir örvaroddi hlutans. Hreinsun sérstillinga á hluta hefur aðeins áhrif á breytingar á innihaldi þess hlutar, ekki staðsetningu eða sýnileika hlutans á síðunni.  

## <a name="fields"></a> Vinna með reiti og dálka

Þegar síða er sérstillt er reiturinn **Bæta við síðusvæði** notaður til að taka með reiti eða dálka á síðunni sem eru faldir úr yfirliti. Til að opna þetta svæði skal velja aðgerðina **+ Reitur**, efst á síðunni. Ólíkt öðrum falnum einingum eru faldir reitir ekki tilgreindir á síðunni sjálfri í sérstillingarstillingu. Hins vegar er hægt að auðkenna falda reiti með því að nota reitinn **Bæta við síðusvæðið** .

Hér eru nokkrar almennar leiðbeiningar sem fylgja skal þegar reiturinn **Bæta við síðusvæðið** er notaður:

- Sjálfgefið er að á svæðinu birtist listi yfir alla falda reiti. Faldir reitir eru merktir með tákninu ![Sýnir falda reitstáknið](media/hidden-icon.png "Sýnir falda reitstáknið") .
- Hægt er að afmarka listann til að sýna aðra reiti, til dæmis þá sem birtast á síðunni, með því að **velja hnappinn Ráðlagðir reitir** fyrir ofan listann og velja afmörkunarvalkost. Heiti hnappsins breytist eftir afmörkunarvalkostinum sem valinn er.
  
   :::image type="content" source="media/personlaization-filter.svg" alt-text="Sýnir afmörkunarhnappinn á svæðinu Bæta við reit í sérstillingarstillingunni.":::
- Ef reitur er valinn á listanum er staðsetningin á síðunni auðkenndari. Ef reiturinn er falinn núna er staðsetning hennar eftir hönnun sýnd í skyggðu ástandi. 
- Til að fá nánari upplýsingar um reit á listanum skal benda á það eða velja <kbd>Alt</kbd>+<kbd>Up Arrow</kbd> til að sýna ábendingu.
- Reitirnir sem tiltækir eru á **svæðinu Bæta við síðusvæði** ákvarðast af forritara síðunnar og upprunatöflu hennar eða stjórnanda forstillingar sem hefur [sérsniðið síðuna](ui-personalization-manage.md). Ekki er hægt að stofna nýjar.
- Sumar síður hafa marga síðureiti sem varpa á sömu upprunatöflu. Á svæðinu sjást hvoru tveggja síðureitirnir eru hvoru í sínu lagi. Það er einnig sjálfstætt að sýna/fela/hreyfa þá reiti er einnig óháð án þess að annar hefur áhrif á hinn.

### Bæta við reit svo að hann birtist á síðunni

Frá **Bæta við reit á síðusvæði** eru tvær leiðir til að taka með reit sem er falinn á síðunni:

- Reiturinn er dreginn á viðeigandi stað. Þykk lárétt lína gefur til kynna staðsetningu marksins.
- Reiturinn er valinn í listanum, farið í skyggða reitinn á síðunni og valkosturinn **Sýna** valinn.

> [!NOTE]
> Suma reiti sem bætt er við er ekki hægt að breyta á síðunni þegar sérstillingu er lokið. Þessir reitir eru annaðhvort hannaðir með þessum hætti eða stjórnandi [sérsniðið](ui-personalization-manage.md) síðuna til að koma í veg fyrir að hægt sé að breyta þeim.

## Hreinsa sérstillingar

Á einhverjum tímapunkti gætir þig langað til að afturkalla sumar eða allar breytingar sérstillinga sem þú gerðir á síðu í gegnum tíðina.

1. Á borðanum **Sérstilling** er aðgerðin **Hreinsa sérstillingu** valin.
2. Einn af eftirfarandi kostum er valinn:  

> [!CAUTION]
> Ekki er hægt að afturkalla hreinsun sérstillinga.

|Valkostur|Það sem hann gerir|
|------|------------
|**Aðeins yfirlitsvalmynd**|Hreinsar allar breytingar sérstillinga sem þú hefur gert á yfirlitsvalmyndinni sem er deilt í Mitt hlutverk og á öðrum síðum. Slíkar breytingar fela í sér allar nýjar aðgerðir sem var bætt við sem bókamerki, og allar breytingar á tenglum og flokkum í valmyndinni.|  
|**Aðeins aðgerðir**|Hreinsar allar sérstilltar breytingar sem þú hefur gert á yfirlits- eða aðgerðarstiku síðunnar.|
|**Aðeins reitir og dálkar**|Hreinsar allar sérstilltar breytingar sem þú hefur gert á síðunni nema þær sem eru á yfirlits- eða aðgerðarstikunni. Slíkar breytingar fela í sér breytingar á reitum, dálkum, hlutum og svæðum. |
|**Allt**|Hreinsa allar breytingar sérstillinga sem hafa verið gerðar á síðunni þannig að síðan líti út eins og hún gerði í upphafi. Slíkar breytingar fela í sér breytingar á yfirlits- og aðgerðarstikum, reitum, dálkum og pörtum.|

## Ábendingar og aðrir áhugaverðir punktar

Til að hjálpa þér að skilja sérstillingar eru hér nokkrar ábendingar.

- Þegar breytingar eru gerðar á spjaldsíðu sem er opnuð úr lista taka breytingarnar gildi á öllum færslum sem opnaðar eru á þeim lista. Segjum til dæmis að þú opnir tiltekinn viðskiptavin af listasíðunni Viðskiptavinir og sértillir svo síðuna með því að bæta við reit. Þegar aðrir viðskiptamenn eru opnaðir úr listanum birtist einnig reiturinn sem bætt var við.
- Breytingar sem hafa áhrif á öll hlutverk (Mitt hlutverk) Ef t.d. er breytt á viðskiptamannalistanum þegar Mitt hlutverk er stillt á Viðskiptastjóri sést einnig breytingin á síðunni Viðskiptamenn **þegar Mitt hlutverk er stillt á** Vinnsla sölupöntunar.
- Breytingar á síðu á svæði taka gildi á síðunni þar sem hún birtist alltaf.  
- Ekki er hægt að sérstilla síðu sem er í [greiningarstillingu](analysis-mode.md). Rofi **greiningar** er óvirkur. Ef skipt er í sérstillingarstillingu meðan síðan er í greiningarstillingu er slökkt á greiningarstillingu sjálfkrafa. 
- Sumar síður hafa marga síðureiti sem varpa á sömu upprunatöflu. Á svæðinu sjást hvoru tveggja síðureitirnir. Það er einnig sjálfstætt að sýna/fela/hreyfa þá reiti er einnig óháð án þess að annar hefur áhrif á hinn.
- Ef hluti eða hópur er falinn sýna draugareitir inni í honum en ekki er hægt að draga fellilistann eða bæta við/sýna þann reit fyrr en hópurinn/hlutinn birtist.

## Sjá einnig .

[Sérsníða síður fyrir forstillingar](ui-personalization-manage.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Grunnstillingum breytt](ui-change-basic-settings.md)  
[Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
