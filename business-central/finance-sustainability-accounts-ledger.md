---
title: Bókhaldslykill sjálfbærnireikninga og fjárhagur
description: 'Læra að stýra bókhaldslykli sjálfbærnireikninga (CoSA), flokkum og undirflokkum og upplýsingum um sjálfbærnibókarfærslur.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, CoA, Chart, Account, Ledger'
ms.search.form: '6210, 6213, 6214, 6220'
ms.date: 05/07/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Bókhaldslykill sjálfbærnireikninga og fjárhagur

## Bókhaldslykill sjálfbærni

Bókhaldslykillinn sjálfbærnilyklar (CoSA) myndar grunnskipulagslistann sem er notaður til að skrá öll útblástursgögn. Hún er rammi sem flokkar og skipuleggur sjálfbærnireikninga eftir eigindum þeirra, t.d. umfangi eða öðrum flokkum. Hverjum reikningi er yfirleitt úthlutað einkvæmum kóta eða númeri til að auðvelda tilvísun og rakningu. Hún hefur sömu uppbyggingu og hefðbundinn bókhaldslykill en er sérsniðinn sérstaklega til að fylgjast með sjálfbærnitengdum gögnum og mælikvörðum innan fyrirtækis.

Notendur geta bætt við flokkum sjálfbærnireikninga og undirflokkum sjálfbærnireikninga til að skilgreina hvernig kerfið hagar sér. Á þennan hátt geta þeir valið sértækan útblástur til að rekja, losunarstuðla, reiknireglur og svipaðar grunnstillingar.

> [!NOTE]
> Samkvæmt staðli gróðurhúsalofttegunda eru þrjú útblásturskerfi:
>
> - **Svið 1 losun** felur í sér losun frá kyrrstæðri og farsímabifreið, og frá óvart flóttamannslosun.
> - **Losun** á sviði 2 felur í sér óbeinan losun frá stofnun orku sem keypt er frá veitendum.
> - **Losun** á 3. sviði felur í sér breiðskírteini losunar, frá keyptum vörum og þjónustu og fjármagnsvörum, eldsneyti og orku-tengdri starfsemi, til flutnings í uppistöðulásum og niðurflutningi, til að mynda úrgangs, fyrir ferðalög og vinnu starfsmanna, og svo framvegis.

Frá yfirmenn Rússlands er hægt að gera hluti eins og:

- Skoða skýrslur sem sýna sjálfbærnifærslur og stöðu.
- Opna sjálfbærnireikningsspjaldið til að bæta við eða breyta stillingum.
- Skoða tegund og undirflokk fyrir lykilinn. 
- Skoða sérstakar stöður fyrir hvern útblástur fyrir einn reikning.
- Bæta einni eða mörgum víddum við hvern reikning og stilla víddarafmarkanir.

Hægt er að bæta við, breyta eða eyða sjálfbærnireikningum. Til að koma í veg fyrir misræmi er ekki hægt að eyða sjálfbærnireikningi ef ein eða fleiri færslur tengjast honum.

### Bæta við eða breyta reikningum

1.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 3.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **bókhaldslykil sjálfbærnireikninga** og velja síðan viðeigandi tengil.
2. Á síðunni **Sjálfbærnireikningar bókhaldslykils** er hægt að opna hvern sjálfbærnireikning og bæta svo við eða breyta stillingum. Haltu bendlinum yfir reit til að lesa stutta lýsingu.

Fyrir reikninga af gerðinni **Samtals** þarf að stilla reitinn **Samantekt** .

Fyrir reikninga af gerðinni **Tiltala** stillir aðgerðin Inndráttur sjálfkrafa reitinn **Samantekt** . Þegar allir reikningarnir hafa verið settir upp skal velja aðgerðina **Inndráttur bókhaldslykils** til að keyra inndráttaraðgerðina og stilla reitinn **Samantekt** .

> [!IMPORTANT]
> Aðgerðin Inndráttur skrifar yfir gildi allra reita fyrir **til-tölureikninga** . Þess vegna, ef skilgreiningar voru færðar inn í **reitinn Samantekt** fyrir **til-tölureikninga** áður en aðgerðin Inndráttur var keyrð þarf að færa þær inn aftur eftir að hún hefur verið keyrð.

### Eyða reikningum

Hægt er að eyða sjálfbærnireikningi. Hins vegar verður fyrst að ganga úr skugga um að engar færslur séu tengdar henni. Business Central kemur í veg fyrir að notandi eyði sjálfbærnireikningi ef ein eða fleiri færslur tengjast honum.

## tegundir lykla

Notendur verða að bæta tegund sjálfbærnireiknings við hvern sjálfbærnireikning til að skilgreina hvernig kerfið hagar sér. Þeir geta valið útblástursspor, hollur útblástur til að fylgjast með, rekja reiknireglur og svipaðar grunnstillingar.

Til að fara yfir flokka sjálfbærnireikninga er skrefunum fylgt:

1.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 3.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **flokka** sjálfbærnireikninga og velja síðan viðeigandi tengil.
2. Á síðunni **Flokkar** sjálfbærnireikninga er hægt að breyta listanum sem fyrir er eða stofna nýjan flokk. Til að stofna nýja tegund skal velja aðgerðina **Nýtt** .
3. Reitirnir **Kóti** og **Lýsing** eru stilltir.
4. Í reitnum **Útblásturssvið** er valinn einn af kostunum fyrir umfangið.
5. Velja skal þá gaslosun sem á að rekja. Eins og er eru eftirfarandi valkostir tiltækir: **CO2,CH4** **og** **N2O.** Hægt er að velja hvaða samsetningu sem á að rekja, en velja þarf að minnsta kosti einn útblástur.
6. Í reitnum **Útreikningsstofn** má velja útreikningsgrunn (reiknireglu) sem nota á við útreikninga á losun ef ekki er vitað rétta losunarupphæðin. Hægt er að velja einn af eftirfarandi kostum: **Eldsneyti/rafmagn**, **Fjarlægð**, **Uppsetning** eða **Sérsnið**.

    > [!NOTE]
    > Ef tiltækar reiknireglur í reitnum **Útreikningsstofnun** duga ekki er hægt að lengja reitinn og bæta fleiri útreikningum við kerfið til notkunar í sjálfbærnibókum.

7. Ef Sérsniðið var valið **í reitnum** Útreikningsstofn **er hægt að grunnstilla sérsniðna lýsingu í reitnum** Sérsniðið virði **.** 

Ef reiturinn **Útreikningsstofn** er stilltur útskýrir eftirfarandi tafla hvernig kerfið reiknar útblástur samkvæmt valkostinum sem valinn var. (Í þessari töflu *EF* stendur fyrir gildi útblástursstuðulsins **sem** hægt er að grunnstilla á síðunni **Undirflokkar sjálfbærnireiknings** .)

| Tegund útblásturs | Grundvöllur útreiknings | Formúla | Athugasemd |
|---------------|------------------------|---------|---------|
| **Gildissvið 1** | | | |
| Kyrrsetning dreifingar | Eldsneyti / rafmagn | *Losunareldsneyti* = *·* &times; *EF* | *Eldsneyti* = Magn af eldsneyti sem er eytt fyrir ketill, hitara, hita oxidizers, og svo framvegis |
| Farsímabreiðslur | Eldsneyti / rafmagn | *Losunareldsneyti* = *·* &times; *EF* | *Eldsneyti* = Magn af eldsneyti sem er varið fyrir ökutæki á vegum eða ökutæki sem ekki eru á vegum, járnbrautum o.s.frv. |
| | | *Losunarfjarlægð* = *·* &times; *EF* | *Fjarlægð* = Kílómetri á vegum eða ökutækjum sem ekki eru á vegum, járnbraut, og svo framvegis |
| Flóttamannaútblástur | Uppsetning | *Margfaldari sérsniðin upphæð* = *útblástursuppsetningar* &times; *·* &divide; 100 &times; *Tímastuðull* | *Sérsniðin upphæð* = Samsetningartap, árlegur lekataxti o.s.frv. |
| **Gildissvið 2** | | | |
| Forritaveitur | Eldsneyti / rafmagn | *Losun* = *rafmagns* &times; *EF* | *Eldsneyti/rafmagn* = Rafmagn, gufumagn, hitaeining og svo fram vegar |
| | Sérsnið | *Sérsniðin losun* = *·* &times; *EF* | *Sérsniðin upphæð* = Hitaeining, tonntímar, og svo fram vegar |
| **Gildissvið 3** | | | |
| Keyptar vörur og þjónusta og fjármagnsvörur | Sérsnið | *Sérsniðin losun* = *·* &times; *EF* | *Sérsniðin upphæð* = Kostnaður (GL) og svo fram vegar |
| Spennandi flutningur og dreifing | Fjarlægð | *Losunarfjarlægð* = *·* &times; *EF* | |
| | Fjarlægð | *Margfaldarar* = *losunarvegalengdar EF* &times; *·* &times; *·* | *Margfaldari* = Tonn af farmum |
| Flutningur og dreifing niður | Fjarlægð | *Losunarfjarlægð* = *·* &times; *EF* | |
| | Fjarlægð | *Margfaldarar* = *losunarvegalengdar EF* &times; *·* &times; *·* | *Margfaldari* = Tonn af farmum |
| Úrgangur myndaður í aðgerðum og endingargóð meðhöndlun seldra vara | Sérsnið | *Sérsniðin losun* = *·* &times; *EF* | *Sérsniðin upphæð* = Úrgangur |
| Viðskiptaferðir og starfsmannaskipti | Fjarlægð | *Losunarfjarlægð* = *·* &times; *EF* | *Fjarlægð* = Kílómetri notaðs fyrirtækisbíls, bílaleigubíls, lestar, flugs og svo framvegis |
| | Sérsnið | *Sérsniðin losun* = *·* &times; *EF* | *Sérsniðin upphæð* = Hóteldvöl |
| | Eldsneyti / rafmagn | *Losunareldsneyti* = *·* &times; *EF* | *Eldsneyti* = Upphæð eldsneytis sem eytt er í bíl fyrirtækisins, bílaleigubíl, og svo fram vegar |

## Undirflokkar lykla

Notendur verða að bæta undirflokki sjálfbærnireiknings við hvern sjálfbærnireikning. Undirflokkurinn skilgreinir útblástursþættina sem eru notaðir í reiknireglunum, byggðir á vali á losunarrakningu í flokki sjálfbærnireiknings.

Til að fara yfir undirflokka sjálfbærnireiknings er skrefunum fylgt:

1.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 3.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Tákn, slá inn **undirflokka sjálfbærnireiknings** og velja síðan viðeigandi tengil. 
2. Á síðunni **Undirflokkar** sjálfbærnireiknings er hægt að breyta listanum sem fyrir er eða stofna nýjan flokk. Til að stofna nýja tegund skal velja aðgerðina **Nýtt** .
3. Reitirnir **Kóti** og **Lýsing** eru stilltir.
4. Á grundvelli þess gasútblásturs sem rekja á í flokki sjálfbærnireiknings og tengið undirflokkinn við er einnig hægt að stilla einn eða fleiri útblástursþætti: 

    - **Losunarstuðull CO2**  – Útblástursstuðull fyrir losun koldíoxíðs (CO<sub>2</sub>).
    - **Útblástursstuðull CH4** – Útblástursstuðull fyrir metan (CH<sub>4</sub>) útblástur.
    - **Útblástursstuðull N2O** – Útblástursstuðull fyrir tvínituroxíð (N<sub>2</sub> O).

5. Ef undirflokkurinn tengist endurnýjanlegri orku skal velja reitinn **Endurnýjanleg orka** .

> [!NOTE]
> Reitirnir **Flytja inn gögn** og **Flytja inn frá** eru fyrir hugsanlega samþættingu við ytri kerfi sem eru notuð til að safna saman útblástursþáttum. Í 2024 útgáfubylgju 1 **er ekki** hægt að nota þessa reiti sjálfgefið sem eiginleika.

## Sjálfbærnibókarfærslur

Sjálfbærnibókin geymir sögu allra bókaðra sjálfbærniviðskipta og skipuleggur öll útblástursgögn samkvæmt CoSA. Þegar notandi bókar sjálfbærnibókina eru öll mikilvæg gögn skráð þar. Allar virkar skýrslur eru búnar til á grundvelli sjálfbærnibókarfærslna.

Til að opna þennan fjárhag fyrir einn tiltekinn reikning skal nota aðgerðina **Færslur** á síðunni **Bókhaldslykill** um sjálfbærni. Til að opna allar færslur skal velja ![Lightbulb sem opnar Tell Me aðgerð 3.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Sjálfbærnifærslur** og velja síðan viðeigandi tengil. Haltu bendlinum yfir reit til að lesa stutta lýsingu.

> [!IMPORTANT]
> Þegar gögn hafa verið bókuð í sjálfbærnibókina er ekki hægt að eyða þeim. Ef mistök hafa verið gerð er hægt að bóka bakfærslu með sömu upplýsingum en notar neikvæða formerkið fyrir upphæðina.

## Sjá einnig .

[Fjármál](finance.md)  
[Sjálfbærnistjórnunaryfirlit](finance-manage-sustainability.md)  
[Sjálfbærniuppsetning](finance-sustainability-setup.md)  
[Hvernig á að skrá losun](finance-sustainability-journal.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
