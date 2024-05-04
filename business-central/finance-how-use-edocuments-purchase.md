---
title: Nota tölvupóstskjöl í innkaupaferlinu
description: Læra að nota tölvupóstskjöl sem tengjast innkaupareikningum og pöntunum.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, receive, purchase, matching, mapping, Copilot'
ms.search.form: '50, 51, 138, 6103, 6133, 6121, 6167, 9307, 9308'
ms.date: 04/03/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="use-e-documents-in-the-purchases-process"></a>Nota E-skjöl í innkaupaferlinu

Hægt er að nota grunnstillt rafræn skjöl (e-documents) með innkaupaskjölunum.

Hægt er að nota eftirfarandi innkaupaskjöl með virkni tölvupóstskjala:  

- Innkaupareikningar
- Innkaupapantanir (útgáfa 24.0)
- Innkaupakreditreikningar
- Almennar færslubækur

> [!NOTE]
> Úr [!INCLUDE[prod_short](includes/prod_short.md)] útgáfu 24.0 er hægt að tengja **innkaupapantanir** við móttekin **E-skjöl**.  

## <a name="e-documents-in-purchases"></a>E-skjöl í innkaupum

Hægt er að framkvæma móttöku rafrænna skjala í Dynamics 365 Business Central innkaupum sem keyrslu eða handvirkt.  

### <a name="how-to-set-up-vendors-to-work-with-different-purchase-documents"></a>Hvernig lánardrottnar eru settir upp til að vinna með mismunandi innkaupaskjöl

Fylgdu skrefunum til að grunnstilla lánardrottna til að vinna rétt með rafræna reikninga á innleið: 

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **lánardrottna** og velja síðan viðeigandi tengil. 
2. Velja skal lánardrottininn sem á að grunnstilla.   
3. Á flýtiflipanum **Móttaka** skal finna reitinn **Móttaka e-fylgiskjal til** til að tilgreina sjálfgefið innkaupaskjal sem á að mynda úr mótteknu E-fylgiskjali. 

> [!NOTE]
> Í reitnum **Taka á móti e-fylgiskjali til** geta notendur annaðhvort valið **Innkaupareikning** eða **Innkaupapöntun** eftir því hvað þeir vilja hafa stofnað úr mótteknum e-reikningi. Þetta val hefur ekki áhrif á stofnun leiðréttingarskjala; Í báðum tilvikum býr kerfið til **kreditreikning**.  

> [!NOTE]
> Ef notandinn velur kostinn **Innkaupapöntun** í reitnum **Taka á móti e-fylgiskjali til** reynir kerfið að uppfæra eina af innkaupapöntununum sem fyrir eru, en ef innkaupapöntunin fyrir lánardrottin í mótteknu **E-fylgiskjali** er ekki til [!INCLUDE[prod_short](includes/prod_short.md)] stofnar kerfið nýja **innkaupapöntun** með sömu aðferð og stofnun nýrra **innkaupareikninga** sem útskýrðir eru á þessari síðu síðar.  

4. Einn af kostunum sem nota á fyrir valinn lánardrottinn er valinn. 
5. Loka síðunni.   

### <a name="to-work-with-purchase-invoices"></a>Unnið með innkaupareikninga

#### <a name="run-the-batch-job"></a>Keyrslan er keyrð

> [!NOTE]
> Þessi keyrsla er fyrir sjálfvirka söfnun reikninga sem berast. Hún getur aðeins unnið í landi eða svæði þar sem virknin er til staðar.  

Í hvert sinn sem **verkröð** er valin til keyrslu, ef ytri þjónustan er með reikninga sem voru sendir frá lánardrottni notanda, safnar kerfið og flytur inn þá reikninga. Til að ljúka ferlinu skal fylgja þessum skrefum. 

1. Þegar keyrslunni er lokið eru nýfluttir reikningar skráðir á **síðuna E-skjöl** ásamt grunnupplýsingum um þá. 
2. Til að skoða nánari upplýsingar er tiltekið tölvupóstskjal opnað.   
3. Ef engar villur eða vandamál eru í e-skjalinu varpar reiturinn **Færsla** fylgiskjalsnúmer innkaupareikningsins, ef það er grunnstillt á síðunni **Lánardrottinsspjald** (sem kerfið stofnaði sjálfkrafa). Velja skal tengilinn til að opna skjalið.
 
> [!NOTE]
> Þetta skjal sem stofnað er af kerfinu er ekki bókaða fylgiskjalið. 

1. Til að fara beint í innkaupaskjalið er reiturinn **Færsla** valinn. Þegar búið er að opna síðuna **Innkaupareikningur** er skjalið athugað. Ef allt er þá rétt er fylgiskjalið bókað.  
1. Þegar innkaupaskjal er bókað er reiturinn **Færsla** í **E-fylgiskjal** uppfærður úr **Reikningur** á **innkaupareikning** og númer bókaða innkaupaskjalsins er tiltækt. Hægt er að velja númer til að opna bókaða innkaupareikninginn. 

Upplýsingar um skráningar eru þær sömu og eru í söluferlinu fyrir tölvupóstskjöl.  

Þar sem villur í söluferlinu tengjast aðallega ráðstöfunarmagni þjónustunnar getur innsenda skjalið innihaldið margar ástæður. Algengasta ástæðan fyrir villu er að kerfið þekkir ekki línurnar í netfanginu sem birgir fékk. Því er ekki hægt að færa inn línur í innkaupareikninginn. 

Tvær algengar villur eru:  

- Ef nota á þessa tilteknu línu úr reikningi lánardrottins sem var bókaður beint í fjárhagsreikninginn verður að vera rétt að grunnstilla **Vörpunartextagildið** . Til að sniðganga þessa villu ef nota á fjárhagsreikninga skal velja Varpa texta á **reikning** til að búa til sérstaka vörpun á Vörpunartextagildinu **með** reitnum **Debetreikn.nr.** gildi sem á að nota. 
- Ef rekja á birgðirnar og nota línur af reikningi lánardrottins til að fylla út vörurnar í fylgiskjalslínunum verður að vera rétt að grunnstilla **tilvísunarnúmer vöru.** Gildi. Til að sniðganga villuna er ytri vörunni varpað á vörunúmerin með því að nota vörutilvísunarlistann. Nánari upplýsingar eru í [Nota vörutilvísanir](inventory-how-use-item-cross-refs.md). 

Þegar villur og viðvaranir hafa verið lagfærðar er hægt að tilgreina handvirkt hvenær kerfið eigi að stofna innkaupareikning út frá uppsetningunni með því að **velja Stofna skjal**.   

#### <a name="manually-import-invoices"></a>Flytja reikninga inn handvirkt

Til að flytja ytri tölvupóstskjöl inn handvirkt skal fylgja eftirfarandi skrefum:

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **E-Document Service** og velja síðan viðeigandi tengil. 
2. Á síðunni **Þjónusta** tölvupóstskjals er virka þjónustan valin.   
3. Velja skal **Móttaka** og hlaða upp e-skjalaskránni sem þú fékkst frá lánardrottninum. 
4. Ef villuboð koma upp er tölvupóstskjalið opnað til að lagfæra vandamálin. 
5. Þegar lokið er við að lagfæra vandamál er í hópnum **Flytja inn handvirkt** valið **Stofna skjal**.  
6. Þegar skjalið hefur verið stofnað í [!INCLUDE[prod_short](includes/prod_short.md)] breytist keyrsla ekki eins og það er skoðað. 

### <a name="e-documents-with-purchase-orders"></a>E-skjöl með innkaupapöntunum

#### <a name="to-link-purchase-orders-with-the-received-e-documents"></a>Innkaupapantanir tengdar við móttekin tölvupóstskjöl

 **Ef birgir** hefur grunnstillt reitinn **Taka á móti e-fylgiskjali til** til að vinna með **Innkaupapantanir**, þegar rafrænt skjal er stofnað í [!INCLUDE[prod_short](includes/prod_short.md)]  (handvirkt eða frá ytri endastað) [!INCLUDE[prod_short](includes/prod_short.md)]  gerir það eftirfarandi:  

1.  **Ef Innkaupapöntun** fyrir þennan tiltekna lánardrottinn er til og innkaupapöntunarnúmer er í móttöku-E-fylgiskjalsskránni **·**  [!INCLUDE[prod_short](includes/prod_short.md)]  tengir þetta **E-fylgiskjal** sjálfkrafa við umnefnda **innkaupapöntun** og **Staða** fylgiskjals þessa **e-fylgiskjals** er **Í vinnslu** og **staða** E-fylgiskjals á **undirsíðu þjónustustöðu** er **Pöntun tengd.** Þessi tengill sést í reitnum **Fylgiskjal** á þessu tiltekna **E-fylgiskjali**. Ef þörf er á að breyta innkaupapöntuninni **sem** tengist sjálfvirkt er hægt að gera það með því að nota aðgerðina **Uppfæra innkaupapöntunartengil** og velja handvirkt eina af fyrirliggjandi innkaupapöntunum fyrir þennan lánardrottin. Það er aðeins hægt að gera áður en línurnar eru samsvarandi milli **E-fylgiskjals** og **Innkaupapöntunar**.  
2. Ef Innkaupapöntun **fyrir þennan tiltekna lánardrottinn er til en ekkert innkaupapöntunarnúmer er í** móttöku-E-fylgiskjalsskránni **·**  býður upp á möguleika á að velja eina af fyrirliggjandi innkaupapöntunum þegar og ef skjalið er hlaðið upp handvirkt er listinn Innkaupapantanir [!INCLUDE[prod_short](includes/prod_short.md)] aðeins opnaður **með pöntunum fyrir lánardrottininn sem þú fékkst** E-Fylgiskjal **þar sem þú þarft að velja** Innkaupapöntun **sem þú vilt og velja** Í lagi **.** Ef rétt innkaupapöntun **var ekki valin eða E-skjalið** er **ekki valið** sjálfvirkt frá ytri lokapunkti með **Verkröð** verður nýtt **E-skjal** ekki tengt neinu **innkaupaskjali og Staða** fylgiskjals verður **Villa** og **staða** E-skjals í **undirsíðunni Þjónustustaða** verður **skjalavinnsluvilla**. Til að ljúka tengingu við **Innkaupapöntun** skal velja aðgerðina **Uppfæra innkaupapöntunartengil** og velja eina af fyrirliggjandi innkaupapöntunum fyrir þennan lánardrottin. 
3. Ef Innkaupapöntun **fyrir þennan tiltekna lánardrottinn er ekki til í augnablikinu þegar nýtt** E-fylgiskjal **er** stofnað stofnar ný [!INCLUDE[prod_short](includes/prod_short.md)] innkaupapöntun **, með því að nota sama líkan af stofnun og þegar er til fyrir nýja** innkaupareikninga **.** Skjalstaða **þessa** E-fylgiskjals **verður** unnin **og** staða **E-fylgiskjals á** undirsíðu þjónustustöðu **verður** stofnuð **.** Þessi tengill sést í reitnum **Fylgiskjal** á þessu tiltekna **E-fylgiskjali**.   

#### <a name="matching-lines-from-received-e-document-with-purchase-order"></a>Samsvarandi línur úr mótteknu e-skjali með innkaupapöntun

Þú getur passað við móttekin rafræn skjöl við línur innkaupapantana frá tveimur mismunandi stöðum, af **síðunni E-fylgiskjal** eða frá síðunni **Innkaupapöntun** . Auðveldasta leiðin til að finna innkaupapantanirnar sem þegar eru tengdar **er** að nota reitinn **Tengdar innkaupapantanir** sem hluta af aðgerðum e-skjala **·**. Öll fylgiskjöl sem ekki eru tengd má finna með því að nota reitinn **Biðinnkaupareikningar** þar sem notandi er með lista yfir **E-skjöl sem þú þarft að endurskoða** .  

> [!NOTE]
> Aðgerðir **í** e-fylgiskjali með þessum tveimur flísum er að finna í eftirfarandi **hlutverkum**: Mat viðskiptastjóra, viðskiptastjóra, endurskoðanda, birgðastjóra og afhendingu og móttöku.  

> [!NOTE]
> Ef VSK-prósentan er frábrugðin VSK-prósentunni milli innleiðarskjals og VSK-prósentu fyrirtækisins er ekki hægt að nota samsvarandi skjöl í umhverfi í mörgum löndum.  

##### <a name="matching-lines-from-purchase-order"></a>Samsvarandi línur úr innkaupapöntun

Hægt er að para línurnar af listanum **Innkaupapantanir** eða úr einni af opnu **innkaupapöntununum**. Til að byrja þetta skal nota eftirfarandi skref:  

1. Reiturinn **Tengdar innkaupapantanir** er valinn í Mínu hlutverki ef eitthvað er til af númeri. 
2. Þar sem tveir valkostir eru fyrir samsvörun skal velja annan þeirra: 

    1. Ef samsvara á línunum af listanum **Innkaupapantanir** skal velja         **Innkaupapöntunarlínuna** sem á að para og velja aðgerðina **Varpa e-fylgiskjalslínum** .  
    2. Ef fyrst á að opna **Innkaupapöntun** skal opna skjalið og velja svo aðgerðina **Varpa e-fylgiskjalalínum** . 

3. Þar sem báðir valkostir hafa sama ferli opnast síðan Samsvörun **innkaupapöntunar** með eftirfarandi innihaldi: 

    1. Í hausnum er að finna eftirfarandi upplýsingar sem auðvelda vörpun línanna: 

    |Heiti reits |Heimildasamstæða |
    |--------|-----------------|
    |Nafn lánardrottins |Tilgreinir nafn lánardrottins á rafrænu skjali. |
    |Nr. rafræns skjals |Tilgreinir númer tengda rafræna skjalsins. |
    |Dagsetning rafræns skjals |Tilgreinir dagsetningu rafræns skjals sem tengist.  |
    |Upphæð rafræns skjals |Tilgreinir tengda heildarupphæð tölvupóstskjalsins með VSK. |

    2. Í línunum er hægt að finna línurnar sem fluttar eru inn úr **E-skjalaskránni** vinstra megin og línurnar úr innkaupapöntun **sem til er** fyrir hægra megin.  
    3. Allar línur báðar hafa vörunúmer og lýsingar ásamt **innk.verði** og **Línuafsl.%**.  
    4.  **Á innfluttum línum** er einnig hægt að finna reitinn **Magn** sem heildarmagn úr tölvupóstreikningi og reitinn **Jafnað magn** sem tilgreinir magnið sem þegar hefur verið jafnað við innkaupapöntunarlínurnar. 
    5.  **Einnig** er hægt að finna **Tiltækt** magn sem magn sem hægt er að para við þessa línu (móttekið en ekki reikningsfært magn) og **Magn til reikningsf**. og magnið sem þegar hefur verið parað við þessa línu. 
    6. Til að passa við línur skal velja línurnar á báðum hliðum sem á að para og velja aðgerðina **Samsvörun handvirkt** . Samsvarandi línur verða merktar með græna litnum. 
    7. Hægt er að para saman einni og einni en einnig er hægt að para marga við einn eða einn fyrir marga og velja fleiri línur á hverri eða annarri áður en aðgerðin Samsvörun **er valin handvirkt** . 
    8. Einnig er hægt að velja aðgerðina Samsvörun sjálfvirkt **til að passa sjálfkrafa við allar línur með sömu** tegund **,** Nr., **Ein.verð** **,** Afsláttur og ** Mælieining **.** 
    9. Ef mistök eru gerð er hægt að velja aðgerðina **Fjarlægja samsvörun** til að fjarlægja samsvarandi línur á innkaupapöntunarhliðinni eða velja aðgerðina **Endurstilla samsvörun** til að endurstilla allt sem samsvarar. 
    10.  **Ef Tölvupóstskjalið** er með margar línur, í samsvarandi vinnslu, er hægt að velja aðgerðina **Sýna línur** í undirbúningi til að fjarlægja allar e-skjalslínur ef þær eru þegar alveg eins. Ef þörf er á að sjá allar línurnar er alltaf hægt að velja aðgerðina **Sýna allar línur** . 

4. Þegar samsvöruninni er lokið þarf að velja aðgerðina **Jafna innkaupapöntun** .   
5. Þegar samsvörunin hefur verið jöfnuð við **innkaupapöntun** [!INCLUDE[prod_short](includes/prod_short.md)]  uppfærist eftirfarandi reitir:

    1. **Reikningsnr. lánardr.** og **Dagsetning** fylgiskjals í fylgiskjalshausnum verður uppfærð með gildum úr rafrænu skjali sem tekið var á móti og tengt. 
    2. **Magn til reikningsf** . í línum verður uppfært með gildunum úr dálknum **Magn til reikningsf** . á **síðunni Samsvörun** innkaupapöntunar byggt á samsvörun sem gerð var. 
    3. Nú er hægt að bóka fylgiskjalið með því að velja Aðgerðin **Bóka** .  
    4. Þegar fylgiskjalið **hefur verið bókað breytist gildið** í reitnum Fylgiskjal **á E-fylgiskjali** og það tengist bókaða **innkaupareikningnum**. 
    5. Loka síðunni.  

> [!IMPORTANT]
> Sjálfgefið er að hægt sé að passa aðeins við línurnar sem hafa sömu heildarupphæð í báðum fylgiskjölum. Það þýðir **að innk.verð** ásamt jafnaðri línuafsl **.%** verður að vera það sama og í einu fylgiskjali er hægt að hafa upphæð án afsláttar og annars með afslætti.  

Ef bæta á við einhverjum vikmörkum og leyfa mismuninn á línum í **E-reikningi** og **Innkaupapöntun** er skrefunum fylgt:   

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Innkaupagrunnur** og velja síðan viðeigandi tengil.  
2. Leyfa á vikmörk í reitnum Samsvörunarmismunur í E-skjali % **og tilgreina hámarks heimila prósentu kostnaðarmismunar þegar það samsvarar E-fylgiskjalslínunni** í **innkaupapöntunarlínunni** **.**  
3. Þessi uppsetning á við um allar samsvarandi línur, en aftur með tilliti til vikmarka fyrir heildarupphæðina, eins og fyrir **innk.verð** ásamt jöfnuðu Línuafsl **.%**.  
4. Loka síðunni.   

##### <a name="matching-lines-from-e-document"></a>Samsvörun lína úr e-skjali

Hægt er að passa við línurnar á síðunni **E-fylgiskjal** . Til að byrja með skal nota eftirfarandi skref:  

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **E-skjöl** og velja síðan viðeigandi tengil. 
2. E-fylgiskjalið **sem** á að passa er valið.   
3. Veldu aðgerðina Samsvörun **innkaupapöntunar** til að opna síðuna **Samsvörun** innkaupapöntunar.  
4. Endurtaka þarf sömu skref og notuð voru þegar samsvörun úr innkaupapöntunum var hafin.

### <a name="e-document-matching-assistance-copilot"></a>Samsvarandi aðstoðarútgáfa tölvupóstskjals

> [!NOTE]
>  **Eins og er yfirfærsla samsvörunar** í E-Skjali í forskoðunarstöðu framleiðslunnar og hann er tiltækur á heimsvísu nema í Kanada. En ūađ virkar bara á ensku. 

> [!NOTE]
> Copilot er AI-knúinn aðstoðarmaður sem hjálpar einstaklingum hjá fyrirtækinu að virkja sköpunargáfuna og gera leiðinlegri verkefni sjálfvirk.  **Aðstoð við samsvörun** tölvupóstskjala auðveldar notendum að passa við móttekna rafræna reikninga sína með fyrirliggjandi innkaupapöntunarlínum með því að nota LLM-líkan fyrir samsvarandi línur milli tveggja ólíkra skjala. 

#### <a name="to-activate-the-copilot"></a>Til að virkja stjórnklefann

Ef afritað var fyrir aðstoð **við samsvörun í E-skjali ekki virka** þarf að gera það handvirkt. Til að virkja **aðstoðarútgáfu fyrir samsvörun** tölvupóstskjala er skrefunum fylgt: 

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Copilot & AI Getu** og velja síðan viðeigandi tengil. 
2. Í listanum yfir getu skal velja **aðstoð við samsvörun** tölvupósts og breyta stöðunni **í Virk**.  

Þegar Copilot-vélin hefur verið virk er hægt að byrja að nota hana.

#### <a name="use-the-e-document-matching-assistance-copilot"></a>Nota aðstoðarútgáfu fyrir tölvupóstskjal

Ef Afritað er virkjað fá fyrirliggjandi aðgerðir **Varpa E-fylgiskjalalínum** á keyptum pöntunum og **samsvörun innkaupapöntunar** á **síðunni E-skjal** mismunandi táknmyndir sem tákna AI- getu. Hægt er að keyra þessar aðgerðir (algerlega þær sömu og í fyrri dæmum af lista yfir innkaupapantanir), úr einni af **innkaupapöntununum** eða úr **E-fylgiskjali**. Öll þrep til keyrslu eru þau sömu en þegar þessi aðgerð er keyrð verður útkoman mismunandi og fylgja þarf skrefunum:  

1.  **Veljið Varpa E-fylgiskjalslínum** eða **Samsvörun innkaupapöntunar** fyrir fylgiskjöl sem þegar eru tengd.  
2. Hægt er að taka eftir að **kvaðning** um samsvörun tölvupóstskjala með afritunarkvaðningu **er virk og** síðan Samsvörun innkaupapöntunar er í bakgrunni. Það þýðir að sama ferlið er að gerast en með sjálfvirkum stuðningi **Copilot**, sem keyrir ferlið passa í staðinn fyrir þig. 
3. Eftir nokkrar sekúndur munu samsvörunarpöntunarlínur e-skjals **með afritalot** stinga upp á línum sem samsvara nokkrum viðbótarupplýsingum: 

    1. Í kvaðningarhausnum er að finna eftirfarandi upplýsingar: 

    |Heiti reits |Heimildasamstæða |
    |--------|-----------------|
    |Sjálfvirk samsvörun | Tilgreinir þann fjölda samsvörunar sem lagt er til sjálfvirkt. Þetta er byggt á strengjasamanburði og ef 80% eða fleiri lýsingar skarast passar kerfið sjálfkrafa við þessar lýsingar án þess að nota GPT getu. |
    |Copilot-pörun | Tilgreinir þann fjölda samsvöruna sem copilot leggur til með bæði streng og semantískum samanburði. |
    |Nr. rafræns skjals | Tilgreinir númer tengda E-fylgiskjalsins. |
    |Heildarupphæð reiknings án VSK | Tilgreinir heildarupphæð reiknings án VSK. |
    |Heildarupphæð með VSK | Tilgreinir samsvarandi upphæð án VSK. |
    
    2. Ef allar línur eru jafnaðar sést græni textinn uppi í hægra horninu: **Allar línur (100%) eru samsvöruð. Fara yfir samsvörunartillögur**.  
    3.  **Í samsvarandi tillögulínum** er að finna eftirfarandi upplýsingar:  

    |Heiti reits |Heimildasamstæða |
    |--------|-----------------|
    |Línunr. rafræns skjals | Tilgreinir línunúmer E-skjals (sem kemur úr upphaflegu skjalaskránni). |
    |Lýsing á rafrænni skjalalínu | Tilgreinir lýsingu á línu e-skjals (sem kemur úr upphaflegu e-skjalaskránni). |
    |Samsvarað magn | Tilgreinir magnið sem á að jafna við innkaupapöntunarlínuna. |
    |Tillaga | Tilgreinir aðgerðina sem AI leggur til og þessar aðgerðir sem lagðar eru til tengjast samsvarandi innkaupapöntunarlínum. |

    4. Allar tillögur og samsvarandi línur eru merktar með grænum lit. Ef eitthvað er um að ræða, t.d. mismunandi verð, en á leyfilegu verðbili er línan merkt sem gul og ef einhver líkt er á milli lýsingarreitanna en verðmunur er meiri en leyfður er þessi lína merkt sem rauð. 
    5. Ef einhverjar tillögur eru ekki fullnægjandi er hægt að eyða þeim með aðgerðinni **Eyða línu** .  
    6. Ef þú vilt sjá tillögusamsvörun er hægt að velja tengilinn í dálknum **Tillaga** til að opna síðuna Samsvörun **e-skjals** . 
    7. Á síðunni **Samsvörunarupplýsingar e-skjals** er hægt að bera saman upplýsingar úr tölvupóstskjalinu **og** **innkaupapöntuninni** til að ganga úr skugga um samsvörunina sem lögð er til áður en hún er staðfest. 
    8. Síðunni er lokað eftir yfirfarir.   

4. Ef þú ert ekki ánægður með flestar tillögurnar, eða í tilfelli viltu ekki nota **eiginleikann Pantanalínur fyrir samsvörun e-skjals með Copilot, veldu** Fleygðu **henni** og haltu áfram með handvirka samsvörun eins og áður hefur verið útskýrt.  
5. Ef halda á tillögum skal velja hnappinn **Halda honum** og kerfið vistar allar tillögur sem **Copilot** gerir.  
6. [!INCLUDE[prod_short](includes/prod_short.md)] lokar afritakvaðningunni og línur á síðunni **Samsvörun** innkaupapöntunar verða merktar sem grænar, þar sem þær hafa þegar verið jafnaðar.  
7. Frá þessari stundu er hægt að halda áfram að vinna eins og verið er að gera handvirka samsvörun og það þýðir að hægt er að fjarlægja samsvörun, handvirkar samsvörunir, endurstilla samsvörun eða ef engar breytingar eru til staðar, velja bara aðgerðina **Jafna innkaupapöntun** og halda áfram að vinna með **innkaupapöntunina**. 

> [!NOTE]
> Ef þú vilt velja aðgerðina **Samsvörun með Copilot** fon á síðunni Samsvörun **innkaupapöntunar** aftur, en í þessu tilfelli verður notandinn spurður hvort skrifa eigi yfir eldsniðin, þar sem allar línur hafa þegar verið paraðar.  

> [!NOTE]
> Greining verðs/kostnaðar og tiltæk athugun á magni er hluti af forvinnsluaðgerð.   

## <a name="overview-of-e-document-statuses"></a>Yfirlit yfir stöður tölvupóstskjala

Til að fá betra yfirlit yfir öll tölvupóstskjöl í fyrirtækinu er hægt að velja mitt hlutverk í endurskoðendahlutverkinu **þar** sem staða e-skjala er til. Þar er hægt að finna aðgerðir í tölvupósti sem hafa eftirfarandi stöðu:

- **E-skjöl á innleið:**

    - Meðhöndlað
    - Í vinnslu
    - Villa


## <a name="see-also"></a>Sjá einnig .

[Hvernig tölvupóstskjöl eru sett upp í [!INCLUDE[prod_short](includes/prod_short.md)]](finance-how-setup-edocuments.md)    
[Hvernig á að nota e-skjal í söluferlinu](finance-how-use-edocuments.md)   
[Hvernig á að lengja tölvupóstskjöl í [!INCLUDE[prod_short](includes/prod_short.md)]](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)    
[Fjármálastjórnun](finance.md)    
[Reikningsfæra sölu](sales-how-invoice-sales.md)    
[Skrá innkaup með innkaupareikningum og pöntunum](purchasing-how-record-purchases.md)    
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

