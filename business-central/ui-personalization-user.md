---
title: Persónusniðnar síður (inniheldur myndskeið)
description: Kynntu þér hvernig á að sérstilla notendaviðmótið og aðlaga vinnusvæðið þitt til að henta því hvernig þú vinnur í Business Central.
author: jswymer
ms.topic: conceptual
ms.service: dynamics365-business-central
ms.custom: bap-template
ms.reviewer: jswymer
ms.search.keywords: 'customize, personalize, personalization, hide columns, remove fields, move fields, resize column, change column width'
ms.search.form: '9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 09/14/2023
ms.author: jswymer
---
# Sérsníða vinnusvæðið

Þú getur sérstillt vinnusvæðið þitt þannig að það falli betur að vinnunni og óskum þínum. Breyta síðum þannig að þær birti einungis upplýsingarnar sem þú þarfnast þegar þú þarfnast þeirra. Sérstaða hefur eingöngu áhrif á vinnusvæðið. Það breytir því ekki hvernig aðrir vinna. Hægt er að sérsníða allar gerðir síðna, þar á meðal á  [hlutverkamiðstöðina](ui-change-basic-settings.md#role-center)  síðu. 

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

Hægt er að gera ýmsar breytingar, svo sem að færa eða fela reiti, dálka, aðgerðir og hluta í heild sinni og bæta nýjum reitum við. Mestan hluta sérstillingar þarf að gera með því að fyrst virkja borðann **Sérstilling**. Hægt er að gera einfaldar breytingar, svo sem dálkbreidd, strax á hvaða lista sem er.

> [!NOTE]
> Kerfisstjórar geta gert sömu útlitsbreytingar og notendur með því að sérsníða forstillingu (hlutverk) sem mörgum notendum er úthlutað. Frekari upplýsingar um hlutverk er að fá með því að fara í  [Sérsníða síður fyrir hlutverk](ui-personalization-manage.md)<br /><br />
Stjórnendur geta einnig hnekkt eða slökkt á sérstillingu notenda og hægt er að skilgreina hvaða eiginleikar eru tiltækir fyrir notendur til að sjá í öllum eða tilteknum fyrirtækjum. Frekari upplýsingar eru í [Sérstilling Business Central](ui-customizing-overview.md).

## Myndband

Eftirfarandi myndband sýnir nokkrar af þeim leiðum sem hægt er að sérsníða hlutverkamiðstöð notanda.

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4ArUB?rel=0]

## Breyta breidd á dálki

Þú getur auðveldlega breytt stærð dálka á hvaða lista sem er. Dragðu bara mörkin milli tveggja dálka til vinstri eða hægri.  

1. Í haus lista skal velja og draga mörkin á milli tveggja dálka.
2. Að öðrum kosti er tvísmellt á mörkin milli tveggja dálka til að laga breidd dálksins. Breiddin lagast að kjörstærð fyrir læsileika.

Eins og fyrir aðrar sérstillingar eru breytingarnar sem gerðar eru á breidd dálks geymdar á reikningnum þínum og fylgja þér, sama hvaða tæki þú notar til að skrá þig inn.

## Ræsa sérsnið með því að nota sérsniðsstillingu

1. Opna skal síðuna sem á að sérsníða.
1. Í efra hægra horninu skaltu velja táknið ![Stillingar.](media/ui-experience/settings_icon_small.png "Stillingatákn fyrir hlutverkamiðstöð") og síðan velja aðgerðina **Sérstilla**.

    Borðinn **Sérstillir** birtist efst til að tákna að hægt sé að byrja að gera breytingar.

    > [!NOTE]
    > Til að vafra á meðan á sérprentun stendur skal nota  <kbd>CTRL</kbd>+<kbd> smella <kbd>  á aðgerð ef hún er auðkennd með arrowhead.

    Ef þú sérð ![Lás sérstillingar](media/personalization-lock-icon.png "Sérstilla lás") eða ![Sérstilling útilokuð](media/personalization-blocked-icon.png "Sérstilling útilokuð") á borðanum er ekki hægt að sérstilla síðuna. Frekari upplýsingar eru í [Af hverju er síða læst og því ekki hægt að sérsníða hana](ui-personalization-locked.md).

1. Til að breyta viðmótseiningu skal færa bendilinn á eininguna, eins og á aðgerð, reit eða hluta. Einingin er tafarlaust auðkennd með örvaroddi eða jaðri. Veldu eininguna og veldu annaðhvort **Færa**, **Fjarlægja**, **Fela**, **Sýna**, **Sýna undir „Sýna meira“**, **Sýna þegar fellt**, **Sýna alltaf**, **Stilla/hreinsa fast svæði** eða **Taka með/útiloka frá flýtifærslu**, allt eftir gerð og stöðu viðmótseiningarinnar.
1. Til að bæta við reit skal velja aðgerðina **+ Reitur**. Á svæðinu **Bæta reit við síðu** skal draga og sleppa reit í æskilega stöðu á síðunni.
1. Þegar lokið er við að breyta útliti á einni eða fleiri síðum, skal velja hnappinn **Lokið** á borðanum **Sérstilla**.

Frekari upplýsingar er að finna á [Hvað hægt er að sérstilla](#What).

## <a name="What"></a> Það sem hægt er að sérsníða

|Hvað viltu gera|Hvernig á að gera það|Athugasemdir|
|----|------------|-------|
|Flytja eitthvað, eins og reit, dálk í lista, Spjald, aðgerð eða hluta á annan stað á síðunni|Bentu hvar sem er á það sem þú vilt færa og dragðu það á nýja staðinn. Þykk lárétt eða lóðrétt lína segir til um stöðuna.<br /><br />![Get ekki fært hingað tákn](media/personalization-cannot-move-here.png "Snið sérstillingar - Geta ekki fært hingað táknið") gefur til kynna að þú getir ekki fært eininguna yfir á valda staðsetningu.|Hlutar eru undirdeildir eða svæði á síðu sem innihalda hluti eins og marga reiti, aðra síðu, graf eða reiti.<br /><br />[Frekari upplýsingar um aðgerðir sérsniðnar](#Actions)<br>[Frekari upplýsingar um sérsniðnum hluta](#Parts)|
|Fela einingu sem sést nú, eins og reit, dálk í lista, Spjald, aðgerð eða hluta.|Veljið atriðið, veljið arrowhead og veljið  <b>síðan fela</b>.|Í séreignarham eru huldar aðgerðir Gráir með skáletraðum texta og faldir hlutar eru Skyggðir með Diagonal línum. Faldir reitir og dálkar eru ekki tilgreind á síðunni. <!--The element is grayed when you are in personalizing mode.--> Þegar hætt er við séreignarstillingu hverfa allir þættir úr yfirliti. Ef svæðið sem þú felur er einnig sýnt á FastTab-fyrirsögninni þegar Fastflipinn er felldur inn birtist svæðið ekki lengur þar.|
|Sýna aðgerð eða hluta sem nú er falinn|Til að skoða skyggða (falda) einingu skal velja örvaroddinn velja síðan <b>Sýna</b>.|Falinn hluti er aftur sýnilegur.|
|Sýna svæði sem nú er hulið|Á borðanum <b>Sérstilling</b> er aðgerðin <b>+ Reitur</b> valin.<br /></br> <b>Reiturinn bæta við síðu</b>  opnast hægra megin á síðunni. Ef svæði í rúðunni er valið birtist falinn staður á síðunni.<br /><br />Ef sýna á svæði skal draga það frá rúðunni eða úr földum stað í stöðuna sem óskað er eftir. Staðsetningin er auðkennd annaðhvort með þykkri láréttri eða lóðréttri línu.<br><br> Önnur leið er að velja örhveið á Snilldar stað svæðisins og velja  **Show**. |Á hverri síðu eru fyrirfram ákveðin mengi reita sem hægt er að velja að birta.<br /><br />[Frekari upplýsingar um vinnusvæðin](#fields) |
|Sýndu reit í haus flýtiflipa þegar hann er minnkaður.|Veldu örvaoddinn og veldu svo <b>Sýna þegar dregið saman</b>. <br /> <br />Ef þú sérð ekki þennan valkost er hann þegar stilltur. Í þessu tilfelli, til að hætta að sýna reitinn í haus flýtiflipans, skal velja <b>Sýna alltaf</b>.|*Flýtiflipi* er hugtakið sem er notað um flokk af reitum sem birtast undir sameiginlegri fyrirsögn. Notaðu valkostinn <b>Sýna þegar dregið saman</b> til að birta mikilvægustu reitina. Ef svæði er valið í fyrirsögninni opnast Fastflipinn og einbeitir sér að völdu svæði.<br /><br />Þessi valkostur gildir aðeins ef síða er með fleiri en einn flýtiflipa. Ef það er aðeins ein Fastflipi þá er ekki hægt að fella hann niður svo  <b>Sýningin þegar ekki er felld úr gildi</b>  er ekki tiltæk.|
|Aðeins birta reit þegar þú velur **Sýna meira**.|Veldu örvaroddinn og <b>Sýna undir „Sýna meira“</b>.|Ef þú sérð  <b>ekki sýninguna undir "sýna meiri"</b>  valkost þá er svæðið þegar búið að stilla. Í þessu tilviki, til að láta reit alltaf sjást, ekki bara þegar þú velur **Sýna meira** skaltu velja <b>Sýna alltaf</b>.|
|Breyta hvort hægt sé að breyta svæði eða ekki.|Veljið svæðið, veljið örhvead á svæðinu og veljið  <b>svo breytingar</b>  á lás til að koma í veg fyrir að breyta gildi svæðisins eða  <b>aflæsa</b>  breytingum til að leyfa breytingu á gildi svæðis.|Aðeins er hægt að opna svæði sem notandi hefur læst áður sjálfur. Sum svæði eru sjálfkrafa læst, annaðhvort með því að hanna eða með forstillingaradmin sem hefur  [sérsniðið síðuna](ui-personalization-manage.md). Ekki er hægt að opna þessi svæði.|
|Breyta föstum svæði í lista í annan dálk. |Veldu örina í dálknum sem þú vilt nota sem síðasta dálk í festu svæði og veldu síðan <b>Stilla Fast svæði</b>.<br /><br/>Ef þú vilt stilla fasta svæðinu aftur á upphaflega staðsetningu skaltu velja örina fyrir fasta dálkinn og velja <b>Hreinsa Fast svæði</b>. Athugaðu: Ekki er hægt að fjarlægja þetta fasta svæði.|Frystirúðan Tilgreinir dálka sem alltaf birtast vinstra megin á listanum, jafnvel þar sem þú flettir lárétt.|  
|Hoppa yfir reit þegar ýtt er á Enter.|Veldu örvaroddinn við hliðina á reitnum, eða dálkahaus í lista, og veldu **Útiloka frá flýtifærslu**.  | Ef ekki  **er útilokað að Flýtifærsla** sé undanskilin er svæðinu þegar sleppt. Í þessu tilfelli, til að hætta að sleppa reitnum, skal velja **Hafa með í flýtifærslu**.<br><br>[Frekari upplýsingar um flýtifærslu](ui-enter-data.md#QuickEntry)|
|Endurraða og fjarlægja yfirlit sem tákna síaða lista.|Veldu örvaoddinn við hliðina á yfirliti og veldu svo **Færa**, **Fjarlægja** eða **Fela**.|[Nánari upplýsingar um listsýningar Vista og sérsníða](ui-views.md)|  
|Bæta nýrri aðgerð við síðu eða skýrslu í Mitt hlutverk.|Af marksíðu, síður skýrslubeiðna eða glugga Viðmótsleitar skal velja bókamerkjatákn.|[Frekari upplýsingar um bókamerkingar og skýrslur](ui-bookmarks.md)|
|Byrja alltaf að birta listann sem stækkaðan eða dreginn saman|Veldu hnappinn **Stækka allt** eða **Draga allt saman** efst í vinstra horni listans. Einnig er hægt að velja aðgerðina **Stækka allt** eða **Draga allt saman** í valmynd fyrsta dálksins. |Á við um stiveldislista sem hægt er að fella saman|

## <a name="Actions"></a> Sérsníða aðgerðrein og valmyndir

Sérstilling gerir þér kleift að ákveða hvaða aðgerðir á að sýna á yfirlits- og aðgerðarstikunni og í hlutverkamiðstöðvum og hvar á að sýna þær. Þú getur sýnt, falið eða fært stakar aðgerðir eða hóp aðgerða.

Eftirfarandi myndband sýnir hvernig hægt er að sérstilla aðgerðir á síðum og í „Mínu hlutverki“.

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE594m2]

Sérstilling yfirlits- og aðgerðarstika er einfaldlega gerð á sama hátt og á öðrum viðmótseiningum. Það sem þú hins vegar getur gert við aðgerð eða hóp aðgerða fer eftir því hvar aðgerðin eða hópur aðgerða er staðsettur. Besta leiðin til að komast að því er að fara í sérsnið og láta svo örvaoddinn leiðbeina þér.

Það eru nokkur hugtök sem þú ættir að kynna þér til að skilja betur sérstillingaraðgerðina: *aðgerðahópur* og *uppfærður flokkur*.  

*Aðgerðahópur* er eining sem víkkar út til að birta aðrar aðgerðir eða flokka. Til dæmis á síðunni **Sölupantanir** er einn aðgerðahópurinn aðgerðina **Virkni** sem birtist þegar þú velur aðgerðina **Aðgerðir**.

*Uppfærður flokkur* er aðgerðaflokkur sem birtist á undan lóðrétta línunni `|` á aðgerðastikunni. Flokkarnir innihalda yfirleitt algengustu aðgerðirnar sem eru notaðar, svo þú getir fundið þær fljótt. Til dæmis á síðunni **Sölupantanir** eru aðgerðirnar **Pöntun**, **Losun**, og **Bókun** uppfærðir flokkar.

> [!NOTE]  
> Til að hreinsa sérsnið er valið arrowhead kringum hönnuði valmyndina hluti og síðan er valið  **Hreinsa sérsnið**.

### Fjarlægja, fela og sýna aðgerðir og aðgerðaflokka

Þegar ætlunin er að sýna eða fela aðgerð skilgreina valkostirnir fyrir neðan örvaroddinn hvað sé hægt að gera miðað við ástand aðgerðarinnar. 

1. Veldu örvaoddinn fyrir aðgerð eða aðgerðahóp.
2. Einn af eftirfarandi valkostum er valinn:

|Valkostur|Það sem hann gerir|
|------|------------
|**Fjarlægja**|Þessi valkostur birtist ef valin aðgerð er einnig sýnd einhvers staðar annars staðar í yfirlits- eða aðgerðarstikunni. Ef þessi valkostur er valinn eyðist aðgerðin úr valdri staðsetningu svo hún birtist ekki lengur. Aðgerðin eða aðgerðahópurinn helst á öðrum stöðum. |
|**Fela**|Þessi valkostur birtist ef aðgerðin eða aðgerðahópurinn er ekki staðsettur á neinum öðrum stað í yfirlits- eða aðgerðarstikunni. Eins og  **Fjarlægja** skal velja gerir aðgerðin eða aðgerðahópurinn hverfa úr yfirlitsreininni eða aðgerðakreininni. Í aðlaga stillingu er aðgerðin eða aðgerðarflokkurinn þó enn sýndur í núverandi stöðu, nema að hann birtist deyfaður.|
|**Sýna**|Þessi valkostur birtist ef aðgerðin eða aðgerðahópurinn hefur verið falinn áður (skyggður). Ef þessi valkostur er valinn verður aðgerðin eða aðgerðarflokkurinn að birtast á yfirlitsreininni eða aðgerðarreininni.|

### Færa aðgerðir og aðgerðaflokka

Þar sem þú getur sleppt aðgerðum eða aðgerðahópum er það gefið í skyn með láréttri línu milli tveggja aðgerða eða ramma utan um aðgerðahóp. Eftirfarandi takmarkanir eru til staðar:

- Þú getur fært einstaka aðgerðir í uppfærða flokka, en þú getur ekki endurraðað röðuninni á aðgerðum í flokknum.
- Ekki er hægt að færa aðgerðahóp í uppfærðan flokk.

1. Til að færa aðgerð eða aðgerðahóp skaltu draga og sleppa honum á viðeigandi stað, rétt eins og með reiti og dálka.
2. Til að færa aðgerð eða aðgerðahóp í annan aðgerðahóp sem er tómur, dragðu aðgerðina eða aðgerðahópinn í nýja hópinn og slepptu honum í boxið **Sleppa aðgerð hér**.

### Um Valmyndin Automate

- Ekki er hægt að  **Fela eða færa valmyndina automate**  eða  **Power Automate**  undirvalmynd og aðgerðir.
- Þú getur flutt innifalin flæði undir atriðið **Sjálfvirkni**, en ekki er hægt að fela þau með sérstillingu. Það að flytja flæðið gerir afrit að áfangastað, það fjarlægir það ekki úr  **sjálfvirka**  atriðu.

> [!TIP]
> Sem stjórnandi getur þú falið atriðið **Sjálfvirkni** fyrir notendum. Frekari upplýsingar er að finna á [Setja upp Power Automate samþættingu](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-setup).

## <a name="Parts"></a> Sérsníða hluta

Benda á eða velja  <kbd>Alt</kbd>+<kbd>upp ör</kbd>  hlutar eru svæði á síðu sem gjarnan samanstanda af mörgum reitum, sjókortum eða öðru efni. Hluti sýnir litaðan ramma þegar þú fókusar á hlutann. Til dæmis er heimaskjár hlutverkamiðstöðvar með marga hluta. Vegna vel skilgreindra marka þeirra er hægt að sérsníða allan hlutann og innihald hans.

- Til að færa hluta skal draga og sleppa honum á æskilegan stað. Lituð lína gefur til kynna gildar stöður á skjánum. Til dæmis er aðeins hægt að færa FactBox við hlið annars FactBox á FactBox-svæðinu.
- Hægt er að fela hluta með því að velja valkostinn **Fela** undir örvaroddinum.
- Þegar þú byrjar að sérsníða eða vafra á nýja síðu birtast allir hlutir sem eru nú faldir á síðunni með sérstakri birtingu til að gefa til kynna að þeir séu faldir. Hægt er að sýna þann hluta með því að velja valkostinn **Sýna** undir örvaroddinum.

Hægt er að hreinsa allar breytingar sérstillingar sem voru gerðar innan einstaks hlutar með því að velja valkostinn **Hreinsa sérstillingar** undir örvaroddi hlutans. Hreinsun sérstillinga á hluta hefur aðeins áhrif á breytingar á innihaldi þess hlutar, ekki staðsetningu eða sýnileika hlutans á síðunni.  

## <a name="fields"></a> Vinna við reiti og dálka

Þegar síðu er sérsniðið er reiturinn bæta við síðu  **notaður**  til að sýna svæði sem eru falin á síðunni. Þessi rúða er opnuð með því að velja  **aðgerðina + reitur**  nálægt toppi síðunnar. Ólíkt öðrum þáttum eru falin svæði ekki tilgreind á síðunni sjálfri í séreignarstillingu. Hins vegar er hægt að auðkenna falin svæði með því að nota  **reitinn bæta við síðu** .

Til að gera vinnu með reiti auðvelda eru hér nokkrar almennar leiðbeiningar til að fylgja með þegar reiturinn bæta við svæði við síðurúðu  **er notaður** :

- Sjálfgefið er að rúðan sé listi yfir öll falin svæði sem eru merkt með  [teikninu á huldum reit](media/hidden-icon.png "Sýnir teiknið falin svæði") .
- Hægt er að afmarka listann Sýna aðra reiti, eins og þá sem eru sýndir á síðunni, með því að  **velja hnappinn reitir**  fyrir ofan listann og velja afmörkunarvalkost. Heiti hnappabreytinga á grundvelli afmörkunarvalkostsins sem valinn er.
  
   :::image type="content" source="media/personlaization-filter.svg" alt-text="Sýnir afmörkunarhnappinn í svæðinu Bæta við svæði í séreignarstillingu.":::
- Val á svæði í listanum auðkennir staðsetningu þess á síðunni. Ef svæðið er hulið er það hannað staðsetning er sýnt í skyggðu ástandi. 
- Til að fá frekari upplýsingar um svæði í listanum er bent á það eða valið  <kbd>Alt</kbd>+<kbd>upp ör</kbd>  til að birta ábendingu.
- Svæðin sem eru tiltæk í reitnum bæta við síðu eru ákvörðuð af hönnuði síðunnar og upprunatöflu hans eða með forstillingaradmin sem hefur  [sérsniðið síðuna](ui-personalization-manage.md). Ekki er hægt að stofna nýjar.
- Sumar síður eru með marga síðureiti sem varpa sömu upprunatöflu. Í rúðunni birtast bæði/allir þessir síðureitir sjálfstætt. Sýni/hulstur/hreyfanleg þau svæði er einnig sjálfstæð án þess að eitt hafi áhrif á hinn.


### Gera huldusvæði sýnilegt

Tvær leiðir eru til að sýna svæði sem nú eru falin á síðunni:

- Dragðu svæðið í æskilega stöðu. Þykk lárétt eða lóðrétt lína segir til um markstaðsetningu.
- Valið er svæðið á listanum og síðan er farið í skyggða svæðið á síðunni og valkosturinn Sýna  **valinn** .

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
|**Aðeins svæði og dálkar**|Hreinsar allar sérstilltar breytingar sem þú hefur gert á síðunni nema þær sem eru á yfirlits- eða aðgerðarstikunni. Slíkar breytingar fela í sér breytingar á reitum, dálkum, hlutum og svæðum. |
|**Allt**|Hreinsa allar breytingar sérstillinga sem hafa verið gerðar á síðunni þannig að síðan líti út eins og hún gerði í upphafi. Slíkar breytingar fela í sér breytingar á yfirlits- og aðgerðarstikum, reitum, dálkum og pörtum.|

## Ábendingar og annað sem bendir til vaxtar

Til að hjálpa þér að skilja sérstillingar eru hér nokkrar ábendingar.

- Þegar gerðar eru breytingar á kortasíðu sem opnaðar eru af lista taka breytingarnar gildi í öllum færslum sem opnaðar eru af þeim lista. Segjum til dæmis að þú opnir tiltekinn viðskiptavin af listasíðunni Viðskiptavinir og sértillir svo síðuna með því að bæta við reit. Þegar aðrir viðskiptamenn eru opnir af listanum er svæðinu sem bætt var við einnig sýnt.
- Breytingar sem þú hefur gert hafa áhrif á allar hlutverkamiðstöðvar þínar. Til dæmis, ef breyting er gerð á viðskiptamannalistanum þegar hlutverkamiðstöðin er stillt á Viðskiptastjóra, sést einnig breytingin á  **síðunni Viðskiptavinir**  þegar Gjörðabók hlutverkamiðstöðvarinnar er stillt á sölupöntun.
- Breytingar á síðu í rúðu taka gildi á síðunni þar sem alltaf er hún sýnd.  
- Ekki er hægt að sérsníða síðu sem er í  [greiningarham](analysis-mode.md).  **Rofinn greina**  er óvirkur. Ef skipt er um sérstillan ham á meðan síðan er í greiningarham er slökkt sjálfkrafa á greina stillingu. 
- Sumar síður eru með marga síðureiti sem varpa sömu upprunatöflu. Í rúðunni birtast bæði/allir þessir síðureitir sjálfstætt. Sýni/hulstur/hreyfanleg þau svæði er einnig sjálfstæð án þess að eitt hafi áhrif á hinn.
- Ef hluti eða flokkur er falinn munu ghóreiti birtast enn innan hans en ekki er hægt að draga-sleppa eða bæta við/Sýna því svæði fyrr en búið er að gera flokkinn/hlutann sýnilega.

## Sjá tengda [Microsoft þjálfun](/training/modules/personalize-ui-dynamics-365-business-central/index)

## Sjá einnig
[Sérsníða síður fyrir forstillingar](ui-personalization-manage.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Grunnstillingum breytt](ui-change-basic-settings.md)  
[Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
