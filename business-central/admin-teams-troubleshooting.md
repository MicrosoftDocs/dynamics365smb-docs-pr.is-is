---
title: Úrræðaleit Microsoft Teams samþættingar
description: Frekari upplýsingar um hvað hægt er að gera sem stjórnandi til að stjórna Microsoft Teams-samþættingu.
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, troubleshooting, errors'
ms.date: 10/01/2021
ms.author: jswymer
---

# <a name="troubleshooting-microsoft-teams-integration-with-"></a><a name="troubleshooting-microsoft-teams-integration-with-"></a><a name="troubleshooting-microsoft-teams-integration-with-"></a>Úrræðaleit Microsoft Teams-samþættingar við [!INCLUDE [prod_short](includes/prod_short.md)]

[!INCLUDE [online_only](includes/online_only.md)]

Í þessari grein er að finna upplýsingar um hvernig á að finna og lagfæra vandamál sem geta komið upp þegar Microsoft Teams er notað með [!INCLUDE [prod_short](includes/prod_short.md)], sem dæmigerður notandi eða stjórnandi.

## <a name="the-sign-in-link-doesnt-work"></a><a name="the-sign-in-link-doesnt-work"></a><a name="the-sign-in-link-doesnt-work"></a>Innskráningartengillinn virkar ekki

Ef reynt er að skrá sig inn í [!INCLUDE [prod_short.md](includes/prod_short.md)]-forritið fyrir Teams strax eftir uppsetningu forritsins og innskráningartengillinn bregst ekki við, getur það verið vegna þess að forritið hefur ekki lokið uppsetningunni að fullu. Til að reyna að laga vandamálið skal skrá sig út úr Teams-biðlaranum og skrá sig inn aftur.

## <a name="the-settings-page-is-empty"></a><a name="the-settings-page-is-empty"></a><a name="the-settings-page-is-empty"></a>Stillingasíðan er tóm

Þú verður fyrst að skrá þig inn til að komast í stillingarnar þínar. Til að skrá sig inn í forritið skal annaðhvort líma tengil í [!INCLUDE [prod_short.md](includes/prod_short.md)]-færslu eða reyna að leita að tengiliðum. Báðar þessar aðgerðir munu leiða þig í gegnum skráningarviðmótið og þar á eftir geturðu notað síðuna **Stillingar**.

## <a name="i-changed-company-but-it-didnt-seem-to-work"></a><a name="i-changed-company-but-it-didnt-seem-to-work"></a><a name="i-changed-company-but-it-didnt-seem-to-work"></a>Ég skipti um fyrirtæki en það virtist ekki virka

Þegar skipt er um fyrirtæki á síðunni **Stillingar** gæti fellilisti skipanareitsins sýnt að þú sért enn að leita í fyrra fyrirtækinu. Þetta vandamál kemur upp þegar síðan **Stillingar** er opnuð beint úr skipanareitnum. Í þessu tilfelli tókst að skipta um fyrirtæki og leitað verður í fyrirtækinu sem þú skiptir yfir í. Vandamálið er að fellilisti skipanareitsins hefur ekki enn verið uppfærður. Til að fellilistinn endurspegli fyrirtækið sem þú ætlar að leita í skaltu loka eða losa [!INCLUDE [prod_short.md](includes/prod_short.md)] úr skipanareitnum og síðan opna forritið aftur.


<!--When you change company from the **Settings** page that you reach from the command box, returning to the command box drop-down continues to show the previous company even though the company was successfully changed. For the drop-down accurately reflect the company you'll search in, you must close or unpin [!INCLUDE [prod_short.md](includes/prod_short.md)] from the command box and then find it again.-->

## <a name="something-went-wrong-error-when-searching-for-contacts"></a><a name="something-went-wrong-error-when-searching-for-contacts"></a><a name="something-went-wrong-error-when-searching-for-contacts"></a>Villan „Eitthvað fór úrskeiðis“ þegar leitað var að tengiliðum

Þessi villa gæti komið upp þegar leitað er í fyrirtæki sem hefur ekki verið frumstillt eða svarar ekki. Til dæmis er ekki hægt að leita í nýju prufufyrirtæki sem hefur ekki enn samþykkt notkunarskilmálana. Til að leysa þetta vandamál skal reyna að skrá sig inn í vefbiðlara [!INCLUDE [prod_short.md](includes/prod_short.md)] og bregðast við eða hafna öllum svargluggum sem birtast í upphafi.

## <a name="cannot-find-the-contactcontact-summary-api-error-when-searching-for-contacts"></a><a name="cannot-find-the-contactcontact-summary-api-error-when-searching-for-contacts"></a><a name="cannot-find-the-contactcontact-summary-api-error-when-searching-for-contacts"></a>„API fyrir tengilið/samantekt tengiliða finnst ekki“ villa við leit að tengiliðum

Þetta vandamál getur stafað af sérsniðnum lausnum eða lausnum fyrir viðskiptalífið sem hafa áhrif á eða breyta [!INCLUDE [prod_short.md](includes/prod_short.md)], eða þau bjóða ekki upp á API fyrir samskipti eða samskiptayfirlit. Ef vandamálið lagast ekki skal hafa samband við kerfisstjóra eða stuðningsaðila.

## <a name="none-of-my-links-expand-into-a-card"></a><a name="none-of-my-links-expand-into-a-card"></a><a name="none-of-my-links-expand-into-a-card"></a>Enginn af tenglunum mínum stækkar í spjald

Ef þetta vandamál kemur upp, þá eru nokkrir hlutir hér sem þú getur prófað:

1. Fyrst skal ganga úr skugga um að [!INCLUDE [prod_short](includes/prod_short.md)] forritið fyrir Teams sé uppsett.

    Til að athuga það skal skrá sig inn í Teams-skjáborðsforritið eða Teams í vafranum. Síðan skal velja vinstra megin **Forrit** og leita að **[!INCLUDE [prod_short](includes/prod_short.md)]**. Þegar **[!INCLUDE [prod_short](includes/prod_short.md)]** forrritið finnst skal velja það til að opna upplýsingasíðu forritsins. Ef hnappurinn **Bæta við fyrir mig** birtist, þá er [!INCLUDE [prod_short](includes/prod_short.md)]-forritið ekki uppsett. Frekari upplýsingar um uppsetningu forritsins er að finna í [Setja upp [!INCLUDE [prod_short](includes/prod_short.md)]-forritið fyrir Microsoft Teams](across-install-app-for-teams.md).

    > [!NOTE]
    > Gestanotendur geta ekki strax sett upp forrit. Frekari upplýsingar um gestanotendur er að finna í algengum spurningum um samvinnu við gesti. 

2. Næst skaltu athuga hvort þú hafir skráð þig inn með réttum innskráningarupplýsingum.

    Í Teams skal fara í hvaða spjall sem er og undir skrifglugga skilaboða skal velja táknið [!INCLUDE [prod_short](includes/prod_short.md)] og síðan velja **Stillingar**. Þegar glugginn birtist skaltu athuga hvort notandinn sem stendur að sé tengdur sé sá sami og þú notar til að tengjast við [!INCLUDE [prod_short](includes/prod_short.md)].

3. Gangið úr skugga um að codeunit: **2718 Þjónustuaðili síðusamantektar** sé gefin út sem vefþjónusta.

    Teams tengist við [!INCLUDE [prod_short](includes/prod_short.md)] með endastöð að þessari Codeunit í [!INCLUDE [prod_short](includes/prod_short.md)]-þjónustunni. Upplýsingar um birtingu vefþjónustu er að finna í [Birta vefþjónustu](across-how-publish-web-service.md).

4. Fyrirtækið kann einnig að koma í veg fyrir að þú getir límt tengla sem verða að spjöldum. Hafa skal samband við stjórnanda til að skilja fyrirtækisreglur Teams sem kunna að eiga við.

## <a name="my-link-sometimes-doesnt-expand-into-a-card"></a><a name="my-link-sometimes-doesnt-expand-into-a-card"></a><a name="my-link-sometimes-doesnt-expand-into-a-card"></a>Tengillinn minn víkkar stundum ekki í spjald

Tengill verður ekki víkkaður í spjald við eftirfarandi aðstæður:

- Tengillinn vísar í síðu sem (á tæknilegu stigi) tengist ekki upprunatöflu í [!INCLUDE [prod_short](includes/prod_short.md)]. Hægt er að skoða hvort síða sé með upprunatöflu með því að nota síðueftirlitssvæðið í vefbiðlaranum í [!INCLUDE [prod_short](includes/prod_short.md)]. Frekari upplýsingar um síðueftirlit er að finna í [Síður skoðaðar](across-inspect-page.md).
- Teams styður ekki forskoðun tengla í sumum eiginleikum. Til dæmis þegar spjall er opnað í sérglugga, eða þú ert gestur í öðru fyrirtæki.
- Teams hættir að reyna að sýna spjaldið eftir 15 sekúndur, t.d. vegna netvandamála.
- Teams víkkar hugsanlega ekki tengilinn ef búið að líma tengil í sama skrifglugga skilaboða og eyða spjaldinu.

Tengillinn þarf einnig að innihalda allar nauðsynlegar upplýsingar til að finna færsluna og birta samsvarandi spjald. Þessar upplýsingar fela í sér:

- Umhverfisheiti, með því að taka það með í vefslóð. Ef heiti umhverfis er ekki tilgreint gerir Teams ráð fyrir því að þú sért að reyna að ná í umhverfi sem heitir „Framleiðsla“.
- Nafn fyrirtækis með því að nota *company=* færibreytuna
- Auðkenni síðu með því að nota *page=* færibreytuna
- Bókamerkið í færslunni með því að nota *bookmark=* færibreytuna

Dæmi:

`https://businesscentral.dynamics.com/?environmentname=Production&company=CRONUS%20USA%2C%20Inc.&page=21&dc=0&bookmark=21%3bEgAAAAJ7BTEAMAAwADAAMA%3d%3d`

Tæknilegar upplýsingar um [!INCLUDE [prod_short](includes/prod_short.md)]-vefslóðir er að finna í [Vefslóð vefbiðlara](/dynamics365/business-central/dev-itpro/developer/devenv-web-client-urls) í [!INCLUDE [prod_short](includes/prod_short.md)]-þróunaraðila og IT Pro hjálp.

## <a name="the-details-window-opens-but-shows-an-error-before-details-are-shown"></a><a name="the-details-window-opens-but-shows-an-error-before-details-are-shown"></a><a name="the-details-window-opens-but-shows-an-error-before-details-are-shown"></a>Upplýsingaglugginn opnast en sýnir villu áður en upplýsingar eru sýndar

Tvær ástæður geta verið fyrir þessu vandamáli: ekki nægar heimildir í [!INCLUDE [prod_short](includes/prod_short.md)] eða vafrastillingar (þegar Teams er notað í vafranum).

1. Staðfestu heimildir þínar í [!INCLUDE [prod_short](includes/prod_short.md)].

    Til að skoða upplýsingar um kort, athugar [!INCLUDE [prod_short](includes/prod_short.md)] leyfið þitt og heimildirnar til að skoða þessa ákveðnu færslu og síðu í tilteknu fyrirtæki og umhverfi. Ef þú hefur ekki heimild fyrir einhverjum þessara þátta, þá birtast stöðluð [!INCLUDE [prod_short](includes/prod_short.md)] villuboð um heimildir í upplýsingaglugganum. 

    Nánari upplýsingar um heimildir má finna í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md)

2. Athugaðu vafrastillingarnar ef Teams er notað í vafranum.

    - Annaðhvort verður að vera slökkt á sprettigluggavörn vafrans eða stillt þannig að leyfa sprettiglugga frá lénum *businesscentral.dynamics.com* eða *bc.dynamics.com*. Upplýsingar um hvernig á að leyfa sprettiglugga fyrir [!INCLUDE [prod_short](includes/prod_short.md)] er að finna í [Vafrinn settur upp](across-browser-settings.md#popup).
    - Vafrinn verður að hafa aðgang að staðbundinni vafrageymslu fyrir kökur og kjörstillingar á meðan þú vinnur.
    - Forðastu að nota gesta- eða einkavefskoðun nema það sé nauðsynlegt, því að það fleygir eða lokar fyrir ákveðið efni í sumum vöfrum.

    Frekari upplýsingar um lágmarkskröfur vafrans er að finna í [Lágmarkskröfur fyrir notkun [!INCLUDE [prod_short](includes/prod_short.md)]](product-requirements.md#browsers) 

## <a name="im-having-problems-with-the-camera-or-location-in-teams"></a><a name="im-having-problems-with-the-camera-or-location-in-teams"></a><a name="im-having-problems-with-the-camera-or-location-in-teams"></a>Vandamál kom upp með myndavélina eða staðsetningar í Teams

Þegar eiginleikar [!INCLUDE [prod_short](includes/prod_short.md)] eru notaðir í upplýsingaglugganum sem þarf aðgang að staðsetningu þinni eða myndavél tækis, þarf fyrst að veita Teams samþykki fyrir því að fá aðgang að þessum möguleikum tækisins.  

- Fyrir Teams í vafranum skal ganga úr skugga um að vafrastillingar þínar leyfi aðgang að myndavél og staðsetningu fyrir https://teams.microsoft.com. 

- Til að teyma fyrir  iOS  eða  Android þarf að tryggja að stillingar tækisins veita aðgang að myndavél og staðsetningu fyrir hópana Mobile App. 

Til að fá aðstoð við að breyta þessum stillingum skal sjá [Myndavélin mín virkar ekki í Teams](https://support.microsoft.com/office/my-camera-isn-t-working-in-teams-9581983b-c6f9-40e3-b0d8-122857972ade?ns=msftteams&version=16&ui=en-us&rs=en-us&ad=us) í notendaþjónustu Microsoft.

[!INCLUDE [prod_short](includes/prod_short.md)]-forritið styður ekki staðsetningu í skjáborðsforriti Teams. Frekari upplýsingar um staðsetningu er að finna í [Teams - Algengar spurningar](teams-faq.md#location).

Sumir vafrar, eins og nýi Microsoft Edge, gera þér kleift að velja hvaða myndavél tækis á að nota þegar tækið styður margar myndavélar. 

## <a name="teams-displays-mixed-languages-for-my-cards-and-card-details"></a><a name="teams-displays-mixed-languages-for-my-cards-and-card-details"></a><a name="teams-displays-mixed-languages-for-my-cards-and-card-details"></a>Teams sýnir ýmis tungumál fyrir mín spjöld og upplýsingar spjalds

Til þess að spjöld og upplýsingar spjalds birti alltaf á sama tungumálinu í Teams verður tungumál Teams-biðlarans og tungumálið sem er notað í [!INCLUDE [prod_short](includes/prod_short.md)]-vefbiðlaranum að passa.

- Til að finna út úr því hvernig á að breyta tungumálinu í Teams skal skoða [Breyta stillingum í Teams](https://support.microsoft.com/en-us/office/change-settings-in-teams-b506e8f1-1a96-4cf1-8c6b-b6ed4f424bc7) í notendaþjónustu Microsoft. 

- Frekar upplýsingar um hvernig skuli breyta tungumálinu í [!INCLUDE [prod_short](includes/prod_short.md)] er að finna í [Breyta grunnstillingum - Tungumál](ui-change-basic-settings.md#language).

Frekari upplýsingar um hvernig tungumál virka á milli Teams og [!INCLUDE [prod_short](includes/prod_short.md)] er að finna í [Teams - Algengar spurningar](teams-faq.md#language).

## <a name="i-edited-a-field-in-the-details-window-but-my-change-wasnt-saved"></a><a name="i-edited-a-field-in-the-details-window-but-my-change-wasnt-saved"></a><a name="i-edited-a-field-in-the-details-window-but-my-change-wasnt-saved"></a>Ég breytti reit í upplýsingaglugganum, en breytingin vistaðist ekki

Breytingar sem gerðar eru á reit í upplýsingagluggum eru sjálfkrafa vistaðar þegar farið er úr reitnum. Áður en glugganum er lokað eftir að svæði er breytt þarf að gæta þess að velja  <kbd>TAB</kbd>  takkann eða smella á/tappa utan við svæðið.

## <a name="a-new-tile-appeared-in-the-app-launcher-how-do-i-remove-it"></a><a name="a-new-tile-appeared-in-the-app-launcher-how-do-i-remove-it"></a><a name="a-new-tile-appeared-in-the-app-launcher-how-do-i-remove-it"></a>Nýr reitur birtist í forritavalmyndinni. Hvernig fjarlægi ég þetta?

Þegar þú skoðar forritin þín á heimasíðu Office 365 (https://home.office.com) eða í forritavalmyndinni mun nýr reitur sem heitir „Business Central Teams Integration Service Connector“ birtast eftir að [!INCLUDE [prod_short](includes/prod_short.md)]-forritið hefur verið uppsett fyrir Teams. Þessi reitur gefur ekkert gildi og er hægt að fela hann á öruggan hátt.

Sem kerfisstjóri, eru með Azure Active Directory stjórnandaheimildir, og getur falið reitinn með eftirfarandi skrefum:

1. Skráðu þig inn í [Azure Active Directory stjórnendamiðstöð](https://aad.portal.azure.com/).
2. Veljið **Fyrirtækjaforrit** og veljið síðan **Business Central Teams Integration Service Connector**.
3. Veljið **Eiginleikar** og stillið síðan rofann **Sýnilegt notendum** á **Nei**.
4. Veljið **Vista**.

> [!NOTE]
> Það mun líða töluverður tími áður en þessi breyting tekur gildi.

## <a name="duplicate-text-in-the-share-to-teams-window"></a><a name="duplicate-text-in-the-share-to-teams-window"></a><a name="duplicate-text-in-the-share-to-teams-window"></a>Afrita texta í glugganum Deila með Teams

Þegar þú límir texta í skilaboðagluggann í glugganum **Deila með Teams** er textinn afritaður. Þetta vandamál er þekkt hjá Microsoft og verður tekið á því í síðari uppfærslu. 

## <a name="unable-to-sign-into-the-share-to-teams-window"></a><a name="unable-to-sign-into-the-share-to-teams-window"></a><a name="unable-to-sign-into-the-share-to-teams-window"></a>Get ekki skráð mig inn í gluggann Deila með Teams

Þetta vandamál getur komið upp af ýmsum ástæðum. Til dæmis þarf auðkennið sem þú notar til að skrá þig inn að hafa aðgang að Microsoft Teams, svo sem í gegnum Microsoft 365 áskrift.

## <a name="my-cards-no-longer-have-a-popout-button"></a><a name="my-cards-no-longer-have-a-popout-button"></a><a name="my-cards-no-longer-have-a-popout-button"></a>Spjöldin mín eru ekki lengur með sprettihnapp

Frá og með apríl 2022 munu tenglar sem sýndir eru í samandregnu spjaldi í Teams ekki lengur innihalda hnappinn **Sprettimynd**. Til að opna spjaldið í eigin glugga skal velja **Upplýsingar**, síðan velja **Opna í vafra** úr fellivalmyndinni (**...**) efst í hægra horni gluggans.

## <a name="cant-pin-a-card-to-tab"></a><a name="cant-pin-a-card-to-tab"></a><a name="cant-pin-a-card-to-tab"></a>Ekki er hægt að festa spjald á flipa

Nokkrar ástæður eru fyrir þessu vandamáli.

- Ef spjaldinu var deilt úr „Leita í mér“, þá er ekki hægt að festa það á flipann. 

- Ekki er hægt festa fyrr en fyrsta Business Central-flipanum er bætt við. Þetta er þekkt vandamál í Teams. 

## <a name="someone-added-a-tab-but-the-tab-doesnt-show-up-for-me"></a><a name="someone-added-a-tab-but-the-tab-doesnt-show-up-for-me"></a><a name="someone-added-a-tab-but-the-tab-doesnt-show-up-for-me"></a>Einhver bætti við flipa en flipinn birtist ekki hjá mér

Þetta vandamál er vegna þess að þú ert ekki með BC-forritið fyrir Teams uppsett. Aðeins þeir sem eru með forritið uppsett sjá Business Central-flipana.

## <a name="others-see-different-sorting-or-column-layout-than-what-the-tab-author-sees"></a><a name="others-see-different-sorting-or-column-layout-than-what-the-tab-author-sees"></a><a name="others-see-different-sorting-or-column-layout-than-what-the-tab-author-sees"></a>Aðrir sjá aðra röðun eða dálkaútlit en það sem höfundur flipans sér

Þetta vandamál er líklega vegna þess að þú deildir listayfirliti sem er eigið yfirlit. Í þessu tilviki skaltu vinna með stjórnanda þínum til að búa til annaðhvort hlutverkamiðað listayfirlit sem nær yfir mismunandi hlutverk í rásinni/spjallinu eða búa til þetta yfirlit fyrir allt fyrirtækið þannig að allir geti fengið samræmt yfirlit.


## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Sjá einnig

[[!INCLUDE [prod_short](includes/prod_short.md)] og Microsoft Teams samþættingaryfirlit](across-teams-overview.md)  
[Setja upp [!INCLUDE [prod_short](includes/prod_short.md)]-forritið fyrir Microsoft Teams](across-install-app-for-teams.md)  
[Leitar að viðskiptavinum, lánardrottnum og öðrum tengiliðum úr Microsoft Teams](across-search-contacts-teams.md)  
[Deila færslum í Microsoft Teams](across-working-with-teams.md)  
[Teams - Algengar spurningar](teams-faq.md)  
[Breyta fyrirtæki og aðrar stillingar í Teams](across-teams-settings.md)  
[Þróun fyrir samþættingu Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
