---
title: Aðgangur með  Microsoft 365  LEYFUM FAQ
description: Fáðu svör við algengum spurningum um aðgang rekstraraðila miðsvæðis með  Microsoft 365  leyfum.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: faq
ms.date: 09/28/2023
ms.custom: bap-template
---
# Aðgangur með  Microsoft 365  LEYFUM FAQ

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Notendur geta nálgast viðskiptaleg gögn miðlægt í  Microsoft Teams  með leyfi sínu Microsoft 365 . Í þessari grein svara Algengar spurningar frá stjórnendum, ráðgjafa og öðrum. Verktaki skal vísa í spurningar til hönnuða. Fyrir spurningar um samþættingu Viðskiptamiðanna við  Microsoft Teams er farið í  [TEYMUM FAQ](teams-faq.md).

## [Heimildir](#tab/permissions) 

### Get ég tekið þátt í að skilgreina mismunandi upphafsheimildir fyrir mismunandi flokka notenda?

Ekki á þessum tíma. Miðbær Business leyfir aðeins að samskipa einum flokki heimilda sem er úthlutað til allra  Microsoft 365  notenda þegar þeir skrá sig inn á viðskipti miðlægt í fyrsta sinn.

### Get ég tekið þátt í að skilgreina heimildir, forstillingar og stillingar fyrir einstaka notendur áður en þeir skrá sig inn?

Já. Hægt er að ná því í gegnum öryggishópa. Með því að nota öryggisflokk í umhverfi er heildarsafn notenda skilgreint sem hefur aðgang að því umhverfi. Þessi öryggiaflokkur getur innihaldið notendur með miðlægt leyfi og notendur með  Microsoft 365  leyfi. Þegar næst er að uppfæra notendur úr  Microsoft 365  í  **listanum**  notendur  Microsoft 365  verða notendafærslur stofnaðar. Síðan er hægt að úthluta notendaflokkum, heimildum, forstillingum og öðrum stillingum áður en þeir hafa skráð sig inn.

### Eftir að notandi skráir sig inn, get ég skipt um hvaða hluti þeir hafa aðgang að?

Já. Þegar notandi hefur skráð sig inn í fyrsta sinn og notendaskrá þeirra hefur verið úthlutaður hafa stjórnendur stjórnað þeim notendum rétt eins og allir aðrir notendur viðkomandi starfrækslu. Til dæmis geta þær bætt við eða fjarlægt heimildir fyrir mismunandi hluti. Ef þeim heimildabreyta  Microsoft 365  sem tengjast leyfinu er breytt á síðunni um leyfistilleytingu hefur breytingin aðeins áhrif á næstu notendur sem skrá sig inn í fyrsta sinn.

### Hvernig er best að hindra aðgang að viðkvæmum töflum?

Business Central býður upp á öflugt og sveigjanlegt heimildalíkan þar sem stjórnendur geta skilgreint heimildasöfn sem veita aðgang að tilteknum hlutum, viðskiptaferlum eða öllu því hlutverki. Til að hindra aðgang að viðkvæmum töflum er hægt að búa til sérsniðin heimildasöfn sem útiloka heimild til viðkvæmra hluta. Fyrir frekari upplýsingar um undanskildar heimildir, sjá  [Create a heimildamengi](ui-define-granular-permissions.md).  

### Í stað þess að sérsníða Leyfiskafbrigðið get ég sérsniðið notendaflokk?

Já. Ef leyfi er bætt við  Microsoft Teams  notendahóp innri notenda í aðalnotanda, hefur sömu nettóáhrif og bætt er við leyfið til  Microsoft 365  leyfisins, svo framarlega sem leyfið hefur  Microsoft 365  áfram verið kortsett fyrir þennan notendaflokk. Þessi nálgun hefur viðbættan ávinning sem heimildasöfn eru alltaf samstillt við meðlimi í hópnum þegar notendaflokksins er breytt.

### Þegar Seðlabanki í miðborg deilir færslu í teymum, veita þeir nýjar heimildir?

Nr. Þessi aðgerð er ekki sú sama og að samnýta tengil í  SharePoint  skjali þar sem einstaklingurinn sem nýtir skjalið getur valið að veita heimild til annarra. Í miðborg Business geta aðeins kerfisstjórar samskipa og úthlutað heimildum. Þegar borið er saman við samnýtingu  SharePoint  skjala er það jafngildi þess að velja þann kost að "samnýta á fólk með fyrirliggjandi aðgangi".

### Styður þessi eiginleiki línustigið öryggi?

Já. Jafnvel þótt einstaklingur fái aðgang að skrá í teymum með sitt  Microsoft 365  leyfi geta þeir fengið réttar töflu-og síðuhlutaheimildir, aðgangsheimildum á línustigi verður framfylgt ef það ' hefur verið útfært fyrir þá töflu.  

### Ef ég Skilgreini heimildir sem fela í sér skrifaðgang geta notendur skrifað í teymum?

Ef Viðskiptamiðlæg er skilgreind til að úthluta heimildarmengi sem felur í sér innsetningu, breytingu eða eyðingu á einum eða fleiri hlutum er notanda samt ekki hægt að skrifa í teymum þegar þeir hafa  Microsoft 365  aðeins leyfi. Miðlæg þjónusta Viðskiptamiðinu framfylgir lesaðgangi sama hvað á að setja inn, breyta eða eyða heimild sem úthlutað er.  

Jafnvel þó að Viðskiptamiðlæg veiti þetta stig vernd mælum við samt eindregið með því að leyfi verði sett með skrifaðgangi. Standi svo í veg fyrir að mál komi niður á við þegar notendur breyta um hlutverk eða eignast ný leyfi.  

## [Uppsetning og samskipan](#tab/setup)

### Af hverju er stillingin til að virkja aðgang ekki tiltæka fyrir umhverfið mitt?

Aðgangur að virkjum með  Microsoft 365  leyfum er einungis til staðar fyrir Viðskiptamiðlumhverfi pallbíla útgáfa 21,1 eða nýrri. Þegar umhverfið er uppfært í þessa lágmarks útgáfu verður stillingin tiltæk sjálfkrafa. Til að athuga útgáfu á umhverfi þínu ferðu á síðuna umhverfisupplýsingar fyrir umhverfið í stjórnsýslumiðstöðinni okkar í Síðumúla. Eða skrá sig inn í umhverfið og fara  **á hjálp & stuðningssísíðu**  úr  **valmyndinni Hjálp** .

### Get ég nálgast atvinnuhúsnæði miðsvæðis á húsnæði með  Microsoft 365  leyfum?

Nei, það er ekki stutt. Miðbær fyrirtækja birtir villu þegar notendur reyna að fá aðgang að aðalskrám innanhúss í teymum.

### Hvað er Starfsmatsniðs?

Starfsmannasninið  **sem**  birtist í  **listasíðu forstillingar (hlutverk)**  var kynnt með uppfærslu 21,1. Það er sjálfgefna sniðið sem úthlutað er til notenda sem hafa aðgang að Viðskiptamiðinu með sínu  Microsoft 365  leyfi. Þessi forstilling er ætluð fólki innan stofnunar sem ekki hefur sértækt hlutverk í starfsemi miðbæjarins og þarf því aðeins að skoða gögn sem deilt var með þeim.

### Hvað er hópurinn notendaflokkur notenda?

 **Microsoft Teams Hópurinn notendur**  innanhúss sem birtist á  **síðunni notendaflokkar**  var kynntur með uppfærslu 21,1. Þessi flokkur er sjálfgefinn Notendaflokkur sem tengist notendum sem hafa aðgang að Viðskiptamiðinu með leyfi þeirra Microsoft 365 . Notendahópurinn er ætlaður fólki innan sömu stofnunar þar sem Miðbær Viðskiptamiðsins er hýst sem samvinna í Microsoft Teams.  

### Eru notendur sem aðeins hafa  Microsoft 365  leyfissvipingu í notendalistanum í Business miðlægu?

Já. Ef öryggishópar eru notaðir í umhverfi munu þeir notendur birtast í listanum notendur eftir að Uppfærslunotendur  Microsoft 365  hafa notað aðgerðina  **úr listanum notendur** . Ef ekki er sótt um öryggishópa birtast notendafærslur á listanum notendur eftir fyrsta tímann sem þeir fá aðgang að aðalfærslu í starfsemi.

### Virkar þessi eiginleiki fyrir innstýringu á ÓHS lausnum?

Já. Notendur með aðeins  Microsoft 365  leyfi geta einnig nálgast færslur í umhverfi sem keyra undir *. bc.dynamics.com léni.

## [Leyfi](#tab/license)

### Getur viðskiptavinur notað þennan eiginleika ef þeir eru ekki miðsvæðis í viðskiptum?

Aðgangur að Viðskiptamiðinu með  Microsoft 365  leyfi er ætlaður fyrir stofnanir sem nú þegar gerast áskrifandi að viðskiptamiðinu og reka eitt eða fleiri viðskiptaleg umhverfi með leyfi rekstraraðila miðlægu þjónustunotenda. Það veitir enga nýja virkni eða nýtir sér réttindi til  Microsoft 365  viðskiptavina sem ekki hafa aðaláætlun fyrirtækja.

### Hvernig hjálpar þetta mér að stjórna áskriftarkostnaði í fyrirtækinu mínu?

Til að hámarka framleiðni og straumlínurekstur sinn, SMBs oft innkaup  Dynamics 365 Business Central  saman við Microsoft 365. Í hvaða tilvikum fá flestir úthlutað  Microsoft 365  leyfi, en aðeins tiltekin hlutverk eða fólk fær miðlægt leyfi rekstraraðila. Viðskiptamiðlæg veitir leyfishafa sveigjanleika þannig að Viðskiptavinir borgi aðeins fyrir það sem þeir þurfa:

- Notendur sem þurfa fullan aðgang að Viðskiptamiðinu eru gjarnan með úthlutaðan Aðalfrumnot viðskipta eða miðlægu Premium starfsleyfi. 
- Notendum sem þurfa á takmörkuðum skrifaðgangi að skipa er yfirleitt úthlutað miðlæg starfsleyfi miðlægu teymis.
- Allir aðrir starfsmenn yfir skipulaginu sem aðeins þurfa að stundum lesa viðskipdata sem er miðlað með þeim, geta gert það ef þeir eru  Microsoft 365  með leyfi. Þeir þurfa ekki að fá úthlutað Hópaðildaleyfi. Aðrir leyfisveitingarmöguleikar eru fyrir hendi. Nánari upplýsingar má sækja og lesa leiðbeiningar  [um](https://go.microsoft.com/fwlink/?LinkId=866544) leyfisveitingu fyrir Dynamics 365.

### Er þetta 100% án endurgjalds?
 
Nr. Aðgangur að Viðskiptamiðlægum gögnum í  Microsoft Teams  krefst þess að hver notandi hafi annaðhvort aðalleyfi eða  Microsoft 365  leyfi frá lista yfir studd áform.

### Virkar þetta með  Microsoft 365  rannsóknum og Aðalrannsóknum fyrirtækja?

Já. Ef notandi hefur fengið  Microsoft 365  leyfi frá prufuútgáfu af studdu áætlun, geta þeir einnig haft aðgang að miðlægum færslum fyrirtækja í teymum. Það er síðan mögulegt fyrir viðskiptavini að reyna framleiðsölur og viðskiptaforrit sem vinna saman og leyfa söluaðilum og ráðgjafarfyrirtækjum að sýna þessa eiginleika auðveldlega. Til dæmis geta samstarfsaðilar ráðstafað eigin  Microsoft Entra  leigjendum út frá  [https://aka.ms/CDX](https://aka.ms/CDX)  því hafa  Microsoft 365  rannsóknir og rekstur miðlægu rannsóknir fyrir því að sýna viðskiptamiðað.

### Listi yfir leyfi í starfsemi miðsvæðis sýnir  Microsoft 365  leyfi. Hvað er það?

 **Síðan Leyfisskilgreiningar**  í viðskiptamiðinu eru birtar mismunandi tegundir leyfa sem geta veitt aðgang að þjónustu miðsvæðis í viðskiptum. Í útgáfu 21 bætist  Microsoft 365  Microsoft við þennan lista sem nýr farvegur til aðgangs að Viðskiptamiðinu. Þessi listi yfir leyfi gefur ekki til að fyrirtækið hafi keypt áskriftir að neinu af þessum leyfum eða fyrirtækið hefur virkjað aðgang í gegnum þessi leyfi.

### Þarf ég að öðlast nýja tegund  Microsoft 365  leyfis fyrir þennan eiginleika til að virka?  

Microsoft hefur ekki stofnað ný leyfi eða nýjar áætlanir hafa vald á þessum eiginleika. Þessi eiginleiki treystir alfarið á fyrirliggjandi  Microsoft 365  áætlanir og leyfi. Ef þú ert þegar áskrifandi að einum af þeim sem studdu  Microsoft 365  áætlanirnar þá hefur þú nú þegar þessa nýju notkun rétt. Að öðrum kosti, ef áskrifandi er ekki í dag er hægt að  Microsoft 365  skrá sig fyrir  Microsoft 365  viðskiptakaupauka eða svipuðum áætlunum hér. 

### Hvernig finn ég út hvaða notendur hafa aðeins  Microsoft 365  leyfi?

Til eru margar leiðir.  Microsoft 365 Í stjórnendamiðstöð er farið  **í lista virk notenda**  og vísað  **í dálkinn leyfi** . Í Business Central er farið  **í notendalistann**, valið hvaða notendur sem er og skoðað  **upplýsingakassa leyfis** .  

### Hvernig sía ég notendalistann í viðskiptafræði miðlægt til að sjá notendur sem aðeins eru  Microsoft 365  með leyfi?

Þetta verk er eins og er ekki hægt að nota við afmörkun eða Yfirlit. Hins vegar er hægt að velja notanda á listanum og skoða upplýsingakassa sem verður aðeins  Microsoft 365 með ef notandinn er  Microsoft 365  aðeins með leyfi.

### Hvað með notendur sem hafa bæði  Microsoft 365  leyfi og miðlægt leyfi fyrirtækja?

Þegar mörgum leyfum er úthlutað til notanda, vinnur leyfishafi yfir leyfi til að nota aðgang að aðalfyrirtæki. Í þessu tilfelli nefnir Seðlabanki fyrirtæki notandann rétt til fleiri notendaleyfis. Þannig að notendur geta lesið og skrifað aðalfærslur í teymum og fengið aðgang að vefsíðu aðalvefbiðlara í vafra, rétt eins og hver önnur starfsemi aðalleyfisveitanda. Ef tilteknum skilgreindum heimildum hefur verið samskipað fyrir  Microsoft 365  leyfið fær notandinn skilgreinda heimildina sem sett er saman við það leyfi sem sett er frá Aðalleyfi rekstraraðila eða sem þegar hefur verið úthlutað til notandans.

### Er leyfisveiting tengd starfsemi miðlægu teymis starfsleyfi?

Það eru engin tengsl á milli meðlim Miðlæguteymis og aðgangs að viðskiptamiðinu í  Microsoft Teams  notkun  Microsoft 365  leyfa. Þó svo  Microsoft Teams  og fylgigögn hennar vísa fólki í lið sem  *hópmeðlimum* þá er það sameiginlega hugtak fyrir hóp  Microsoft Teams  notenda. Það vísar því ekki til Aðalleyfis rekstraraðila.

### Hefur seðlabankinn framfylgt einhverju af hömlunum?

Já, allar vettvangskorðingar og lágmarkskröfur, þ.m.t. leyfisveitingar, eru knúnir inn á Aðalvettvang fyrirtækja. Þetta fylgja notendum með tiltekin villuskilaboð til að auðvelda þeim að leysa uppsetningu þeirra og koma í veg fyrir misnotkun. Til dæmis, ef notandi sem aðeins er  Microsoft 365  með leyfistilraunir til að fá aðgang að aðalvefbiðlara Viðskiptamiðis í vafranum verður aðgangi hafnað og villuskilaboð birt. 

## [Notkun](#tab/usage)
 
### Get ég nálgast færslur á teymum fyrir  iOS  og teyma Android? 

Eins og er þá er ekki hægt að nálgast viðskipti miðlægt í teymum farsíma með því að nota einungis  Microsoft 365  leyfi. Microsoft vinnur að því að virkja þessa getu bráðlega. 

### Hvernig breyta notendur persónulegum stillingum sínum í stillingum mínum? 

Þegar notandi sækir viðskipti miðlægt í fyrsta sinn með því að nota aðeins leyfið sitt  Microsoft 365 , eru notandastillingar þeirra eins og tungumál, tímabelti og svæðisstillingar sjálfkrafa settar á grundvelli stýrikerfis-eða vafrastillinga. Kerfisstjórar geta breytt þessum stillingum miðlægt fyrir hvern notanda. 

### Hvað ákvarðar val tungumálsins við innskráningu í fyrsta sinn? 

Tungumálið þar sem þú upplifir Viðskiptamiðað er stilltur út frá ýmsum þáttum, þar á meðal teymum biðlara þar sem þú hefur aðgang að Aðalsafni í fyrsta sinn. Fyrir teyma skjáborðs-app, teyma  iOS  og teyma fyrir  Android er stýrikerfi notað. Fyrir teyma fyrir vefinn er vafamál vafrans beitt. Í öllum tilfellum er teymisvinna ekki talin með. 

### Hvers vegna get ég ekki virkjað einhverja litaða tengla í flipum og kortaupplýsingum?

Actionable tenglar á miðlægu síður fyrirtækja eru oft sýndir sem Feitletraðir Tenglar sem hægt er að virkja til að fara annars staðar eða keyra einhvern rekstur. Á tæknilegu stigi eru þessir tenglar yfirleitt útfærðir sem gildi svæðis án texta sem kveikja einhverja kóða og þar sem val á stíl endurspeglar oft ástand. Þegar notendur fá aðgang að vefsíðum fyrirtækja með leyfi þeirra  Microsoft 365  eru Tenglarnir stílfærir eins og ef þeir eru actionanlegir. En þau er ekki hægt að virkja þar sem slíkt leyfi býður ekki upp á notkun réttinda til að keyra aðgerðir.  

### Af hverju er ekki hægt að virkja síðutilkynningaraðgerðir?

Contextual-tilkynningar sem sýndar eru á síðum fylgja oft Gantt tenglar. Þegar notendur fá aðgang að Aðalsíðum fyrirtækja með leyfi sínu  Microsoft 365  eru þessir tenglar birtir en ekki er hægt að virkja þá því þetta leyfi býður ekki upp á að nota réttindi til að keyra aðgerðir. Á tæknistigi eru þessir tenglar útfærðir sem aðgerðir.

### Geta  Microsoft 365  notendur fjarlægt flipa?

Já. Hver sem er á spjallinu eða rás getur fjarlægt flipa sem aðrir búa yfir. Ef flipi er fjarlægður skal ekki fjarlægja eða hafa áhrif á gögn í Aðalviðskiptum en Flipinn verður fjarlægður fyrir alla notendur Spjalls eða rása.

### Ef ég get ekki afmarkað, mun ég enn sjá afmarkaðan lista sem var búinn til af öðrum?

Notendur sem fá aðgang að miðborg með leyfi sínu  Microsoft 365  hafa ekki notkunina réttindi til að sía með afmörkunarúðanum eða nota yfirlitslista. En, ef annar notandi hefur búið til flipa með síaða listasíðu,  Microsoft 365  munu notendur einnig skoða þær síur sem beitt er á flipanum.

---

## Sjá einnig .

[Yfirlit yfir miðlægu aðgengi fyrirtækja með  Microsoft 365  leyfum](admin-access-with-m365-license.md#minimum-requirements)  
[Setja upp aðgang með Microsoft 365-leyfum](admin-access-with-m365-license-setup.md)  