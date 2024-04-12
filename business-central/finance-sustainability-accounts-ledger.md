---
title: Bókhaldslykill sjálfbærnireikninga og fjárhagur
description: 'Læra um umsjón með bókhaldslykli, flokkum og undirflokkum og upplýsingum um sjálfbærnifærslur.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, CoA, Chart, Account, Ledger'
ms.search.form: '6210, 6213, 6214, 6220'
ms.date: 04/02/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Bókhaldslykill sjálfbærnireikninga og fjárhagur 

## Bókhaldslykill sjálfbærni  

Bókhaldslykillinn **Sjálfbærnireikningur**  (CoSA) myndar grunnskipulagða listann sem notaður er til að skrá öll útblástursgögn. Hún vinnur sem rammi sem flokkar og skipuleggur sjálfbærnireikninga út frá eigindum þeirra, t.d. umfangi eða öðrum flokkum. Hverjum reikningi er gjarnan úthlutað einkvæmum kóta eða númeri til að auðvelda tilvísun og rakningu, eftir sömu uppbyggingu og hefðbundinn **bókhaldslykill** en sérsniðinn sérstaklega til að fylgjast með sjálfbærnitengdum gögnum og mælikvörðum innan fyrirtækis. 
 
Notendur geta bætt við **reikningsflokkum** og **undirflokkum** til að skilgreina hvernig kerfið hagar sér, valið sérstakt losun fyrir rakningu, útblástursþætti, reiknireglur og svipaðar grunnstillingar.  

>[!NOTE]
>Til að vera kunnugt um scopes, byggt á staðlinum GHG (Gróðurhúsalofttegundir) eru þrjú útblásturskerfi:  
>- **Svið 1**: fela í sér losun sem losnar úr ritföngum og farsímabifreiðum og frá óvart flóttamannslosun. 
>- **Svið 2**: fela í sér óbeinan losun frá stofnun orku sem keypt er frá nýtingaraðilum. 
>- **Útblásturssvið** 3: felur í sér breiðskírteini um losun, aðkeyptar vörur og þjónustu og fjármagnsvörur, eldsneyti og orkutengda starfsemi, flutning í uppi og niður á við, mynda sóun, viðskiptaferðir og starfsmannasamskipti o.s.frv. 

Í bókhaldslyklinum **Sjálfbærnireikningur**  (CoSA) er hægt að gera hluti eins og:  

-   Skoða skýrslur sem sýna sjálfbærnifærslur og stöðu. 
-    **Opna spjald** sjálfbærnireiknings til að bæta við eða breyta stillingum.  
-   Sjá tegund og undirflokk fyrir þann reikning.   
-   Skoða sérstakar stöður fyrir hvern útblástur fyrir einn reikning. 
-   Einni eða mörgum **víddum** er bætt við hvern reikning og víddarafmörkun stillt. 
    
Hægt er að bæta við, breyta eða eyða **sjálfbærnireikningum**. Til að koma í veg fyrir misræmi er ekki hægt að eyða **sjálfbærnireikningi** ef ein eða fleiri færslur eru tengdar þessum reikningi.  

### Bæta við eða breyta reikningum  

1.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 3.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **bókhaldslykil sjálfbærnireikninga** og velja síðan viðeigandi tengil. 
2. Á síðunni **Sjálfbærnireikningar**  (CoSA) er hægt að opna hvern **sjálfbærnireikning** og bæta svo við eða breyta stillingum. Haltu bendlinum yfir reit til að lesa stutta lýsingu. 

Fylla þarf út reitinn **Samantekt** fyrir reikninga af reikningsgerðinni **Samtals**. Þessi reitur fyllist sjálfkrafa út með inndráttaraðgerðinni fyrir reikninga af gerðinni **Lokasamtala**. Þegar allir reikningarnir hafa verið settir upp skal velja aðgerðina Þrep **bókhaldslykill sjálfbærnireiknings** til þess.  

>[!IMPORTANT]
>Ef skilgreiningar hafa verið færðar í **Samtals**-reitina fyrir **Til-tölu**-reikningana áður en inndráttaraðgerðin er framkvæmd þarf að færa þær inn aftur því að aðgerðin skrifar yfir gildin í öllum **Til-tölu**-reitum.  

### Eyða reikningum  

Hægt er að eyða **sjálfbærnireikningi**. Áður en honum er eytt verður hins vegar að ganga úr skugga um að ein eða fleiri færslur séu tengdar þessum reikningi þar sem Business Central kemur í veg fyrir að sjálfbærnireikningi **sé eytt** í þessum aðstæðum.  

## tegundir lykla   

Notendur þurfa að bæta flokki **sjálfbærnireikninga** við hvern **sjálfbærnireikning**, til að skilgreina hvernig kerfið hagar sér, velja útblásturskerfi, sérstakt losun fyrir rakningu, reiknireglur og svipaðar grunnstillingar.  

Til að fara yfir **flokka** sjálfbærnireikninga skal fylgja skrefunum: 

1.   ![Veldu Lightbulb sem opnar Tell Me aðgerð 3.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **flokka** sjálfbærnireikninga og velja síðan viðeigandi tengil. 
2.  Á síðunni **Flokkar** sjálfbærnireikninga er hægt að breyta listanum sem fyrir er eða stofna nýjan flokk. Til að stofna nýja tegund skal velja aðgerðina **Nýtt** .  
3.  Fyllt er í reitina **Kóti** og **Lýsing**.   
4.  Reiturinn **Útblásturssvið** er settur upp og valinn einn af sviðskostum.  
5.  Velja skal þá gaslosun sem á að rekja. Eins og er er hægt að nota einn af kostunum: **CO2,CH4** **eða** **N2O**. Hægt er að velja hvaða samsetningu sem á að rekja, en að lágmarki þarf að vera einn útblástur til rakningar.  
6.  Í reitnum **Útreikningsstofn má** velja einhverja reiknireglu sem á að nota, ef ekki er vitað nákvæma losunarupphæð. Hér er hægt að tilgreina útreikningsgrunn (reiknireglu) fyrir útblástursútreikninga. Hægt er að velja einn af eftirfarandi kostum: **Eldsneyti/rafmagn**, **Fjarlægð**, **Uppsetning** eða **Sérsnið**. 
7.  Ef sérsniðin **reikniregla er valin** er hægt að grunnstilla sérsniðna lýsingu í reitnum **Sérsniðið virði** .  

>[!NOTE]
>Ef þessi reikniregla í reitnum **Útreikningsstofn** nægir ekki er hægt að lengja þennan reit og bæta fleiri útreikningum við kerfið sem á að nota í **sjálfbærnibókunum**.  

Ef útreikningsstofninn **(reiknireglurnar) er notaður** er útskýring á því hvernig kerfið reiknar út eftir valkostinum sem var valinn (**EF** er útblástursstuðullinn **sem hægt er** að grunnstilla á **síðunni Undirflokkar** sjálfbærnireiknings): 

|  Tegund útblásturs  |  Grundvöllur útreiknings  |  Formúla         | Athugasemd      |
|------------|--------------|------------------------------|---------------------------------|
| **SVIÐ 1**  |
| Kyrrsetning dreifingar | Eldsneyti / rafmagn | Losun = Eldsneyti * EF | _þ.e., Eldsneyti = Magn af eldsneyti sem eytt er fyrir katlar, Hitari, Hitastillir oxidizers ..._ |
| Farsímabreiðslur | Eldsneyti / rafmagn | Losun = Eldsneyti * EF | _þ.e., Eldsneyti = Magn eldsneytis sem eytt er fyrir ökutæki á vegum eða ökutæki sem ekki eru á vegum, járnbraut..._ |
|  |  |  Útblástur = Fjarlægð * EF | _þ.e., Fjarlægð = Milleage á vegum eða ökutæki utan vega, járnbraut..._ |
| Flóttamannaútblástur | Uppsetning | Útblástur = Uppsetning margfaldara * Sérsniðin upphæð / 100 * Tímastuðull | _þ.e., Sérsniðin upphæð = Samsetningartap, Árlegur lekataxti..._ |
| **SVIÐ 2**  |
| Utillity veitendur | Eldsneyti / rafmagn | Losun = Rafmagn * EF | _þ.e., Eldsneyti / Rafmagn = Rafmagn, gufumagn, hitaeining..._ |
|  | Sérsnið | Losun = Sérsniðin upphæð * EF | _þ.e., Sérsniðin upphæð = Hitaeining, Ton-klukkustund..._ |
| **SVIÐ 3**  |
| Keyptar vörur og þjónusta og fjármagnsvörur | Sérsnið | Losun = Sérsniðin upphæð * EF | _þ.e., Sérsniðin upphæð = Kostnaður (GL)..._ |
| Spennandi flutningur og dreifing | Fjarlægð | Útblástur = Fjarlægð * EF |  |
|  | Fjarlægð | Útblástur = Fjarlægð * Margfaldari * EF | _Margfaldari = Farmfarmar_ |
| Flutningur og dreifing niður | Fjarlægð | Útblástur = Fjarlægð * EF |  |
|  | Fjarlægð | Útblástur = Fjarlægð * Margfaldari * EF | _Margfaldari = Farmfarmar_ |
| Úrgangur myndaður í aðgerðum og endingargóð meðhöndlun seldra vara | Sérsnið | Losun = Sérsniðin upphæð * EF | _þ.e., Sérsniðin upphæð = Úrgangur_ |
| Viðskiptaferðir og starfsmannaskipti | Fjarlægð | Útblástur = Fjarlægð * EF | _þ.e., Fjarlægð = Milleage af notaða fyrirtæki bíla, bílaleigubíl, lest, flug..._ |
|  | Sérsnið | Losun = Sérsniðin upphæð * EF | _þ.e., Custom Amount = Hótel helst..._ |
|  | Eldsneyti / rafmagn | Losun = Eldsneyti * EF | _þ.e., Eldsneyti = Upphæð eldsneytis sem eytt er í bíl fyrirtækisins, bílaleigubíll..._ |

## Undirflokkar lykla  

Notendur þurfa að bæta undirflokknum **Sjálfbærnireikningur** við hvern **sjálfbærnireikning** til að skilgreina útblástursþætti sem notaðir verða í reiknireglunum, en það byggir á rakningarvali útblásturs í flokknum **Sjálfbærnireikningur**.  

Til að fara yfir **undirflokka** sjálfbærnireiknings er skrefunum fylgt:  

1.   ![Veldu Lightbulb sem opnar Tell Me aðgerð 3.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Tákn, slá inn **undirflokka sjálfbærnireiknings** og velja síðan viðeigandi tengil. 
2.  Á síðunni **Undirflokkar** sjálfbærnireiknings er hægt að breyta listanum sem fyrir er eða stofna nýjan flokk. Til að stofna nýja tegund skal velja aðgerðina **Nýtt** .  
3.  Fyllt er í reitina **Kóti** og **Lýsing**.   
4.  Á grundvelli þess gasútblásturs sem rekja á í flokknum **Sjálfbærnireikningur** og tengið undirflokkinn við er einnig hægt að útbúa einn eða fleiri útblástursþætti: 

   - **Losunarstuðull CO2** - Tilgreinir losunarstuðulinn fyrir CO2 losun.  
   - **Losunarstuðull CH4** - Tilgreinir útblástursstuðulinn fyrir CH4 losun. 
   - **Útblástursstuðull N2O** - Tilgreinir útblástursstuðulinn fyrir N2O útblástur.  

5.  Ef undirflokkurinn tengist endurnýjanlegri orku skal velja reitinn **Endurnýjanleg orka** .   

>[!NOTE]
>**Reitirnir Flytja inn gögn** og **Flytja inn úr** eru ætlaðir fyrir hugsanlega samþættingu við ytri kerfi sem eru notuð til að safna saman útblástursþáttum, en í **2024 er** ekki hægt að nota þá sem eiginleika sjálfgefið.  

## Fjárhagsfærslur fyrir sjálfbærni  

**Sjálfbærnibókin** geymir sögu allra bókaðra sjálfbærnifærslna og skipuleggur öll útblástursgögn samkvæmt bókhaldslykli **sjálfbærni**. Þegar notandi bókar **sjálfbærnibókina** verða öll mikilvæg gögn skráð þar. Allar virkar skýrslur eru búnar til samkvæmt **sjálfbærnibókarfærslunum**.   

Notandi getur opnað þennan fjárhagsreikning fyrir einn tiltekinn reikning með aðgerðinni **Færslur** af síðunni **Sjálfbærnireikningur** bókhalds eða valið ![Lightbulb sem opnar Tell Me aðgerð 3.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Sjálfbærnifærslur** og velja síðan viðeigandi tengil. Haltu bendlinum yfir reit til að lesa stutta lýsingu.  

>[!IMPORTANT]
>Þegar gögn hafa verið bókuð í sjálfbærnibókina er ekki hægt að eyða þeim. Ef mistök hafa verið gerð er hægt að bóka bakfærsluna með sömu upplýsingum en nota neikvætt merki fyrir upphæð.  

## Sjá einnig .  
[Fjármál](finance.md)    
[Sjálfbærnistjórnunaryfirlit](finance-manage-sustainability.md)
[Sjálfbærniuppsetning](finance-sustainability-setup.md)
[Hvernig á að skrá losun](finance-sustainability-journal.md)
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
