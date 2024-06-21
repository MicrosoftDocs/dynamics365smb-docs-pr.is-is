---
title: Varpa e-skjölum í innkaupapöntunarlínur með Copilot
description: Fræðast um notkun Copilot til að varpa e-skjölum í innkaupapöntunarlínur.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.collection:
  - get-started
  - bap-ai-copilot
ms.date: 06/10/2024
ms.custom: bap-template
---

# Varpa e-skjölum í innkaupapöntunarlínur með Copilot (forskoðun)

Þegar innkaupaferli verða stafrænni gegnir e-skjöl aðgerðin Business Central lykilhlutverki í því að gera móttöku og vinnslu lánardrottins sjálfvirka. Copilot getur hjálpað þessu ferli með því að bæta vörpun og samsvörun reikninga lánardrottna á innkaupapantanir. Þessi aðstoð styttir tíma sem eytt er í verk sem fela venjulega í sér umfangsmikla leit, uppflettingu og gagnafærslu. Annar kostur er þegar lánardrottnareikningar tengjast ekki nákvæmlega innkaupapöntunum. Í því tilviki er Copilot vel staðsett til að auðkenna samsvarandi innkaupapantanir. Aukin samsvörunargeta gagnast sérstaklega litlum og miðstýrðum fyrirtækjum sem þurfa skilvirka rakningu skjala fyrir innkaupapantanalínur. Copilot er aðstoðarmaður sem eykur sköpunarkraft og bætir framleiðni Hjá Business Central notendum.

> [!IMPORTANT]
> - Þetta er eiginleikinn Forskoðun framleiðslu tilbúið fyrir framleiðslu- og sandkassaumhverfi í hvaða landi sem er.<!-- with the exception of Canada -->.
> - Forskoðun framleiðslu tilbúnar er háð viðbótarnotkunarskilmálum. Nánari upplýsingar: [Viðbótarnotkunarskilmálar fyrir Dynamics 365 forskoðun](https://go.microsoft.com/fwlink/?linkid=2105274)
> - Ónýtt efni getur verið rangt.

Í upphaflegri útgáfu forritsins **e-skjals** kynntum við grundvallaratvik fyrir tölvupóstskjöl fyrir allt söluferlið. Hins vegar er þörf á viðbótum og sjálfvirkni við að meðhöndla móttekin skjöl, sérstaklega í samhengi við innkaupaferli. Copilot skilgreinir hvernig stjórnað er tölvupóstskjölum í innkaupaferlinu, sérstaklega hvað varðar innkaupapantanir. Með ramma tölvupóstskjala er hægt að tilgreina tegund innkaupaskjals sem stofna skal fyrir hvern lánardrottinn þegar tölvupóstur berst frá þeim. Áður var eini valkosturinn að stofna innkaupareikning, annaðhvort sem fylgiskjal eða fjárhagsbók.

Nú er hægt að uppfæra fyrirliggjandi innkaupapöntun í Business Central með þeim upplýsingum sem berast í tölvupósti.

## Tiltæk tungumál

[!INCLUDE[e-docs-matching-language-support](includes/e-docs-matching-language-support.md)]

## Virkja stjórnklefa  

Ef afritað var fyrir samsvörunarútgáfu **e-skjals var ekki virkt** þarf að gera það handvirkt. Til að virkja **aðstoð við samsvörun** tölvupóstskjala skal fylgja eftirfarandi skrefum: 

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Copilot & AI Getu** og velja síðan viðeigandi tengil. 
2. Í listanum yfir getu skal velja **aðstoð við samsvörun** tölvupósts og breyta stöðunni **í Virk**.  

Hægt er að byrja að nota Copilot um leið og hann er virkjaður. 

## Auðkenna innkaupapantanir

Fyrst er hægt að auðkenna innkaupapantanirnar sem hægt er að jafna sjálfkrafa.  **Ef lánardrottininn** grunnstillti reitinn **Taka á móti e-fylgiskjali til** til að vinna með **Innkaupapantanir**, þegar rafræna skjalið er stofnað í [!INCLUDE[prod_short](includes/prod_short.md)]  (handvirkt eða frá ytri endastöð) [!INCLUDE[prod_short](includes/prod_short.md)]  er eftirfarandi:

1.  **Ef Innkaupapöntun** fyrir þennan tiltekna lánardrottinn *er til og innkaupapöntunarnúmer* er í móttekinni **E-fylgiskjalsskrá**  tengir þetta [!INCLUDE[prod_short](includes/prod_short.md)] E-fylgiskjal **sjálfkrafa** við tilgreinda **innkaupapöntun**. Staða **skjals þessa** E-skjals **er** í vinnslu **og Staða** tölvupóstskjalsins **á** undirsíðu þjónustustöðu **er** Pöntun tengd **.**  
Þessi tengill sést í reitnum **Fylgiskjal** á þessu tiltekna **E-fylgiskjali**. Ef þörf er á að breyta innkaupapöntuninni **sem** tengd er sjálfvirkt er hægt að gera það með því að nota aðgerðina **Uppfæra innkaupapöntunartengil** og velja síðan eina af fyrirliggjandi innkaupapöntunum fyrir þennan lánardrottin handvirkt. Það er aðeins hægt að gera áður en þær samsvara línunum milli **E-fylgiskjals** og **Innkaupapöntunar**.  
2. Ef Innkaupapöntun **fyrir þennan tiltekna lánardrottinn** er til en ekkert innkaupapöntunarnúmer *er í skjalinu sem var móttekið* E-fylgiskjal **, ef skjalið var hlaðið upp handvirkt,**  gerir það mögulegt að velja úr einni af þeim innkaupapöntunum sem fyrir eru, með því að opna [!INCLUDE[prod_short](includes/prod_short.md)] listann Innkaupapantanir **úr pöntununum sem þú komst frá lánardrottnum sem innihalda aðeins** E-fylgiskjal **, þar sem þú þarft að velja** Innkaupapöntun **sem þú vilt og velja** Í lagi **.** Ef rétt **innkaupapöntun er ekki valin eða E-skjalið** er **sjálfkrafa valið frá ytri endastöð með** Verkröð **er nýja** E-skjalið **ekki tengt innkaupaskjalinu og Staða** skjals birtist sem **Villa** og **staða** **E-skjals á** undirsíðunni Þjónustustaða **er** Flutt inn **skjalavinnsluvilla**. Til að ljúka við að **tengja Innkaupapöntun** skal velja aðgerðina **Uppfæra innkaupapöntunartengil** og velja síðan eina af fyrirliggjandi innkaupapöntunum fyrir þennan lánardrottin.  

## Varpa línum

Copilot auðveldar samsvörun e-reikningslína sjálfvirkt við innkaupapantanalínur og býður upp á auka samsvörunarupplýsingar til að bæta samsvörunina.

Eftir að þær hafa verið jafnaðar og varpaðar [!INCLUDE [prod_short](includes/prod_short.md)]  uppfærir samsvarandi innkaupapöntun með viðeigandi móttökuupplýsingum til að tryggja að rétt magn berist í pöntunarlínurnar.

Þú getur passað við móttekin rafræn skjöl við línur innkaupapantananna frá tveimur mismunandi stöðum, af **síðunni E-skjöl** eða af síðunni **Innkaupapöntun** . Auðveldasta leiðin til að finna innkaupapantanirnar sem þegar eru tengdar **er** að nota reitinn **Tengdar innkaupapantanir** sem hluta af **aðgerðum** E-skjala. Öll ótengd skjöl er að finna með reitnum **Biðinnkaupareikningar** þar sem listi yfir **E-skjöl** þarf að skoða.  

> [!NOTE]
> Aðgerðir **í** E-fylgiskjali með þessum tveimur flísum er að finna í eftirfarandi hlutverkum (Mitt hlutverk): **Mat** viðskiptastjóra, **viðskiptastjóra**, endurskoðanda **,** **birgðastjóra** og **afhendingar og móttöku**.

Þegar keyra á samsvörun frá innkaupapöntuninni skal velja **Varpa e-fylgiskjalalínum**, sem er til á listasíðum innkaupapöntunar og innkaupapöntunar. En, ef þú vilt keyra samsvörun frá síðunni **E-skjöl**, veldu þá aðgerðina **Samsvörun innkaupapöntunar** á þessari síðu. Til að vinna með samsvörun skal fylgja eftirfarandi skrefum:

1.  **Veljið Varpa E-fylgiskjalslínum** eða **Samsvörun innkaupapöntunar** fyrir fylgiskjöl sem þegar eru tengd.  
2. Hægt er að taka eftir að **kvaðning** um samsvörun tölvupóstskjala með afritunarkvaðningu **er virk og** síðan Samsvörun innkaupapöntunar er í bakgrunni. Það þýðir að sama ferlið er að gerast, en með sjálfvirkum stuðningi **Copilot**, sem keyrir samsvörunarferlið í staðinn fyrir þig. 
3. Eftir nokkrar sekúndur munu samsvörunarpöntunarlínur e-skjals **með afritalot** stinga upp á línum til samræmis við nokkrar nánari upplýsingar: 

    1. Í kvaðningarhausnum er að finna eftirfarandi upplýsingar:   

    |Heiti reits |Heimildasamstæða |
    |--------|-----------------|
    |Sjálfvirk samsvörun | Tilgreinir þann fjölda samsvörunar sem lagt er til sjálfvirkt. Þetta númer er byggt á strengjasamanburði og ef 80% eða fleiri lýsingar skarast passar kerfið sjálfkrafa við þessar lýsingar án þess að nota Copilot getu. |
    |Copilot-pörun | Tilgreinir þann fjölda samsvöruna sem copilot leggur til með bæði strengja- og merkingarsamanburði. |
    |Nr. rafræns skjals | Tilgreinir númer tengda tölvupóstskjalsins. |
    |Heildarupphæð reiknings án VSK | Tilgreinir heildarupphæð reiknings án VSK. |
    |Heildarupphæð með VSK | Tilgreinir samsvarandi upphæð án VSK. |
    
    2. Ef allar línur eru jafnaðar sést græni textinn uppi í hægra horninu: **Allar línur (100%) eru samsvöruð. Fara yfir samsvörunartillögur**.  
    3. Í samsvarandi **tillögulínum** eru eftirfarandi upplýsingar:  

    |Heiti reits |Heimildasamstæða |
    |--------|-----------------|
    |Línunr. rafræns skjals | Tilgreinir línunúmer tölvupóstskjalsins (sem kemur úr upphaflegu e-skjalaskránni). |
    |Lýsing á rafrænni skjalalínu | Tilgreinir lýsingu e-skjalslínunnar (sem kemur úr upphaflegu e-skjalaskránni). |
    |Samsvarað magn | Tilgreinir magnið sem notað er á innkaupapöntunarlínuna. |
    |Tillaga | Tilgreinir aðgerðina sem AI leggur til og þessar aðgerðir sem lagðar eru til tengjast samsvarandi innkaupapöntunarlínum. |

    4. Allar tillögur og samsvarandi línur eru merktar með grænum lit. Ef um er að ræða úthreyfingu, til dæmis annað verð en innan leyfilegs verðbils er þessi lína merkt með gulum lit. Ef einhver líkindi eru milli lýsingarreitanna en verðmunurinn er hærri en leyfður er þessi lína merkt með rauðum lit.
    5. Ef einhverjar tillögur eru ekki fullnægjandi er hægt að eyða þeim með aðgerðinni **Eyða línu** .  
    6. Ef þú vilt sjá tillögusamsvörun er hægt að velja tengilinn í dálknum **Tillaga** til að opna síðuna Samsvörun **e-skjals** . 
    7. Á síðunni **Samsvörunarupplýsingar e-skjals** er hægt að bera saman upplýsingar úr **E-skjölunum** og **innkaupapöntuninni** til að ganga úr skugga um samsvörunina sem lögð er til áður en hún er staðfest. 
    8. Síðunni er lokað eftir yfirfarir.   

4. Ef þú ert ekki ánægður með flestar tillögurnar, eða í tilfelli viltu ekki nota **eiginleikann Pantanalínur fyrir samsvörun e-skjals með Stjórnborði**, veldu **Henda honum** og þú getur haldið áfram með [handvirka samsvörun](finance-how-use-edocuments-purchase.md).  
5. Ef halda á tillögum skal velja hnappinn **Halda honum** og kerfið vistar allar tillögur sem Copilot **gerir**.  
6. [!INCLUDE[prod_short](includes/prod_short.md)] lokar afritakvaðningunni og línur á síðunni **Samsvörun** innkaupapöntunar eru merktar sem grænar, þar sem þær hafa þegar verið jafnaðar.  
7. Héðan í frá er hægt að halda áfram að vinna eins og verið er að gera handvirka samsvörun og það þýðir að hægt er að fjarlægja samsvörun, handvirkar samsvörunir, endurstilla samsvörun eða ef engar breytingar eru til staðar, veldu þá aðgerðina **Jafna innkaupapöntun** og haltu áfram að vinna með **innkaupapöntunina**. 

> [!NOTE]
> Einnig er hægt að velja aðgerðina **Samsvörun með afritalot** af **síðunni Samsvörun** innkaupapöntunar aftur, en í þessu tilviki er notandinn spurður hvort skrifa eigi yfir eldri samsvörun, þar sem allar línur hafa þegar verið jafnaðar.  

> [!NOTE]
> Greining verðs/kostnaðar og tiltæk athugun á magni er hluti af forvinnsluaðgerð. 

## Sjá einnig .

[Yfirlit yfir tölvupóstskjöl](finance-edocuments-overview.md)    
[Nota tölvupóstskjöl í sölu](finance-how-use-edocuments.md)    
[Nota tölvupóstskjöl í innkaupum](finance-how-use-edocuments-purchase.md)   
[Úrræðaleit vegna stjórnunargetu og ÓM](ai-copilot-troubleshooting.md)    
[Algengar spurningar um bankaafstemmingu](faqs-bank-reconciliation.md)    
