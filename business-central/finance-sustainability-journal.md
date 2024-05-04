---
title: Hvernig á að skrá sjálfbærnifærslur
description: Læra að skrá losun gróðurhúsalofttegunda.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, journal'
ms.search.form: '6216, 6219, 6220'
ms.date: 04/02/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="how-to-record-sustainability-entries"></a>Hvernig á að skrá sjálfbærnifærslur

Á þessu augnabliki er eina leiðin til að skrá losun GHG í **sjálfbærnibókina** með **sjálfbærnibókunum**.   

## <a name="sustainability-journal"></a>Sjálfbærnibók

**Sjálfbærnibækur** eru hannaðar til að rekja og skrá sjálfbærnitengdar aðgerðir með sömu notendaupplifun og aðrar færslubækur í Business Central. Í bókinni eiga notendur kost á að nota losun handvirkt ef þeir hafa nauðsynlegar upplýsingar. Einnig er hægt að nota gögnin til að reikna út losun sem byggir á þekktum færibreytum sem samsvara ýmsum tegundum uppruna og reikninga. 

Upplýsingarnar sem færðar eru inn í færslubók eru til bráðabirgða og hægt er að breyta þeim í færslubókinni. Þegar færslubókin er bókuð eru upplýsingarnar fluttar **í Sjálfbærnibókarfærslur** á einstökum **sjálfbærnireikningum** þar sem ekki er hægt að breyta þeim. Hins vegar er hægt að bóka bakfærslu eða leiðrétta færslur.  

### <a name="use-journal-templates-and-batches"></a>Nota bókarsniðmát og keyrslur

Sjálfgefið er að tvö **sniðmát** sjálfbærnibóka séu stöðluð og ítrekunarbók. Fyrir hvert sniðmát færslubókar, geturðu sett upp þína eigin færslbók sem bókarkeyrsla. Til að gera það þarf að velja **keyrslur** á síðunni **Sniðmát** sjálfbærnibóka og stofna nýja **sjálfbærnibókarkeyrslu** á nýju síðunni. Til dæmis er hægt að skilgreina eigin bókarkeyrslu fyrir hvert útblásturssvið með því að nota valkostinn **Útblásturssvið** þar sem hægt er að velja milli þriggja svæða sem fyrir eru. Einnig er hægt að bæta við eða breyta **upprunakóta** og **ástæðukóta** fyrir hverja keyrslu. 

>[!TIP]
>Hægt er að hafa eina bókarkeyrslu fyrir hverja útblásturstegund ef um margar línur er að ræða en einnig er hægt að nota sameiginlega keyrslu fyrir allar tegundir útblásturs.   

### <a name="validating-sustainability-journals"></a>Prófun sjálfbærnibóka

Hægt er að kveikja á bakgrunnsathugun á síðunni **Sjálfbærniuppsetning** sem hjálpar til við að koma í veg fyrir tafir þegar bókað er. Í prófuninni er greint frá mistökum þegar unnið er í sjálfbærnibókinni **og það kemur í** veg fyrir að bókin sé bókuð.  

Þegar staðfestingin er gerð virk birtir upplýsingakassinn **færslubókarprófunarkassann** úthreyfingar í opnu línunni og í allri keyrslunni. Villuleit gerist þegar færslubókarkeyrsla er hlaðin inn og þegar önnur færslubókarlína er valin. Reiturinn **Samtala** útgáfa í upplýsingakassanum sýnir heildarfjölda vandamála sem [!INCLUDE [prod_short](includes/prod_short.md)] fundust og hægt er að velja það til að opna yfirlit yfir vandamálin. 

### <a name="work-with-sustainability-journals"></a>Vinna með sjálfbærnibækur

Til að hefja vinnu með **sjálfbærnibækur er skrefunum** fylgt:   

1.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 3.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Sjálfbærnibók** og velja síðan viðeigandi tengil. 
2. Á síðunni **Sjálfbærnibók** er hægt að færa inn eins margar línur og ætlunin er að bóka með sömu keyrslu.  
3.  **Sem tegund** fylgiskjals er hægt að hafa auðan valkost eða velja að nota **Reikningur eða** Kreditreikningur **·**.  
4. Í reitnum **Reikningur nr.** er eingöngu **hægt að velja Sjálfbærnireikninga** með reitinn **Bein bókun,Bókun**  **·**  sem tegund **bókhalds og reikningur sem** ekki er lokaður. Einnig verða reikningar að hafa verið grunnstilltir með tegund og undirflokki.  

>[!NOTE]
>Ef notuð er keyrslan þar sem útblásturssviðið er grunnstillt **verður útblásturssviðið** í sjálfbærnireikningnum **að** vera það sama og **útblásturssviðið** í notuðu keyrslunni.  

5. Valkostirnir eru tveir: annaðhvort bóka upphæðirnar handvirkt eða nota reiknireglur.   

    1. Ef til eru nákvæmar upplýsingar um losunina þarf að bóka hann (þ.e. þær eru á mótteknum reikningi) þarf að velja **reitinn Handfært** ílag til að tilgreina að upphæðirnar verði ílag handvirkt. Í þessu tilfelli er ekki hægt að færa gögn í reitina **Eldsneyti/rafmagn**, **Fjarlægð**, **Sérsniðin upphæð**, **Margfaldari** uppsetningar og **Tímastuðull**, þar sem þeim er ekki hægt að breyta. En reitirnir **Emission CO2**, **Emission CH4** og **Emission N2O** verður hægt að breyta og þú getur fyllt gögnin beint þar. 
    2. Ef útblásturinn er ekki nákvæmlega þekktur þarf að reikna það og ekki þarf að velja **reitinn Handfært** ílag og í þessu tilviki **verða reitirnir Losun CO2**, **Emission CH4** og **Emission N2O** ekki hægt að breyta en hægt er að færa inn útreikningsupplýsingar út frá reiknireglunni sem er notuð. Hér er að finna nánari upplýsingar um notaðar reiknireglur og skilgreindar í flokknum **Sjálfbærnireikningur** hér í [bókhaldslykli og fjárhag](finance-sustainability-accounts-ledger.md#account-categories).
    
7. Til að bóka færslubókina er valið aðgerðin **bóka**. Við bókun í **sjálfbærnibók** myndast færslur í **sjálfbærnibókinni**. 

Ef reiknireglan er byggð á valkostinum **Reikna út úr fjárhag** í flokknum **Sjálfbærnireikningur** verður að nota aðgerðina **Innheimta upphæð úr fjárhagsfærslum** áður en færslubókin er bókuð til að reikna út losun byggða á þessum gagnagjafa. Ef nokkrar breytingar hafa verið gerðar á útblástursstuðlum eftir að færslubókarlínurnar hafa verið fylltar út þarf að velja aðgerðina **Endurreikna** til að fá rétta upphæð í færslubókinni.  

### <a name="recurring-journals"></a>Ítrekunarbækur

Ítrekunarbók er **Sjálfbærnibók** með sérstökum reitum til að stjórna færslum sem oft eru bókaðar með fáum eða ef einhverjar eru, breytist. Til dæmis sjálfbærniviðskipti eins og rafmagn, hiti eða önnur áþekk viðskipti. Með því að nota ítrekunarbækur er hægt að bóka fastar og breytilegar upphæðir. Með ítrekunarbók eru búnar til færslur sem verða bókaðar reglulega aðeins einu sinni. Til dæmis haldast reikningar, víddir, víddargildi og svo framvegis áfram í færslubókinni eftir bókun. Ef breytinga er þörf getur þú gert þær í hvert sinn sem þú bókar. 

Reiturinn **Ítrekunarmáti** skiptir máli. Það ákvarðar hvernig farið er með upphæðina í færslubókarlínunni eftir bókun. Ef sama upphæðin er til dæmis notuð í hvert sinn sem lína er bókuð er hægt að láta upphæðina standa og í því tilviki ætti að nota **Föst** sem valkost. Ef sömu reikningar og texti eru notaðir í línunni, en upphæðin verður breytileg í hvert sinn sem er bókað, er hægt að velja að eyða upphæðinni að lokinni bókun og í því tilviki verður valkosturinn **V-breytilegur** valinn. 

Einnig þarf að grunnstilla reitinn **Ítrekunartíðni** því þessi dagsetningarreikniregla ákvarðar hversu oft skuli bóka færsluna í færslubókarlínuna og fylla hana út. Frekari upplýsingar er að finna í [Nota dagsetningarformúlur](ui-enter-date-ranges.md#use-date-formulas).  

Reiturinn **Fyrningardagsetning** ákvarðar dagsetninguna þegar línan verður bókuð í síðasta sinn. Línan verður ekki bókuð eftir þessa dagsetningu. Kosturinn við að nota reitinn **Útrunnið, dags** . er sá að línunni verður ekki eytt strax úr færslubókinni. Þú getur slegið inn síðari dagsetningu þannig að þú getir notað línuna í framtíðinni. Ef reiturinn er auður verður línan bókuð í hvert skipti þar til henni er eytt úr færslubókinni.  

## <a name="see-also"></a>Sjá einnig .
[Fjármál](finance.md)    
[Yfirlit yfir sjálfbærnistjórnun](finance-manage-sustainability.md)   
[Sjálfbærniuppsetning](finance-sustainability-setup.md)   
[Bókhaldslykill sjálfbærnireikninga og fjárhagur](finance-sustainability-accounts-ledger.md)   
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)   

[!INCLUDE[footer-include](includes/footer-banner.md)]
