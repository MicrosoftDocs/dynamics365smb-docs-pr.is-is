---
title: Skrá sjálfbærnifærslur
description: Læra að skrá losun gróðurhúsalofttegunda (GHG).
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, journal'
ms.search.form: '6216, 6219, 6220'
ms.date: 05/07/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="record-sustainability-entries"></a>Skrá sjálfbærnifærslur

Eins og er er eina leiðin til að skrá losun gróðurhúsalofttegunda í sjálfbærnibók er að nota sjálfbærnibækur.

## <a name="sustainability-journals"></a>Sjálfbærnibækur

Sjálfbærnibækur eru hannaðar til að rekja og skrá sjálfbærnitengdar aðgerðir með því að nota sömu notendaupplifun og aðrar færslubækur í Business Central. Notendur sem hafa nauðsynlegar upplýsingar geta fært útblástur handvirkt í færslubók. Einnig er hægt að nota innbyggðar reiknireglur til að reikna út losun nákvæmlega samkvæmt þekktum færibreytum sem samsvara ýmsum tegundum uppruna og reikninga.

Upplýsingarnar sem færðar eru inn í færslubók eru til bráðabirgða og hægt er að breyta þeim í þeirri færslubók. Þegar færslubókin er bókuð eru upplýsingarnar fluttar í sjálfbærnibókarfærslur á einstökum sjálfbærnireikningum þar sem ekki er hægt að breyta þeim. Hins vegar er hægt að bóka bakfærslu eða leiðréttingu færslna.

### <a name="use-journal-templates-and-batches"></a>Nota bókarsniðmát og keyrslur

Sjálfgefið er að um tvö sjálfbærnibókarsniðmát sé að ræða: staðlaða sniðmátið og ítrekunarsniðmátið.

Fyrir hvert sniðmát færslubókar, geturðu sett upp þína eigin færslbók sem bókarkeyrsla. Til að gera það skal velja **keyrslur** á síðunni **Sniðmát** sjálfbærnibóka og stofna síðan nýja **sjálfbærnibókarkeyrslu** á nýju síðunni. Til dæmis er hægt að skilgreina eigin bókarkeyrslu fyrir hvert útblásturssvið með því að nota valkostinn **Útblásturssvið** og velja síðan á milli svæðanna þriggja sem fyrir eru. Fyrir hverja keyrslu er hægt að bæta við eða breyta gildunum **Upprunakóti** og **Ástæðukóti** .

> [!TIP]
> Ef um margar línur er að ræða er hægt að draga úr hættu á mistökum með því að hafa eina bókarkeyrslu fyrir hverja útblásturstegund. Einnig er hægt að nota sameiginlega keyrslu fyrir allar tegundir útblásturs.

### <a name="validate-sustainability-journals"></a>Staðfesta sjálfbærnibækur

Á síðunni **Sjálfbærniuppsetning** er hægt að kveikja á bakgrunnsprófun til að koma í veg fyrir bókunartafir. Ef einhver mistök sem verða á meðan unnið er í sjálfbærnibókinni tilkynnir staðfestingin þér og kemur í veg fyrir að bókin sé bókuð.

Þegar staðfestingin er gerð virk sýnir upplýsingakassinn **Færslubókarprófun** úthreyfingar í opnu línunni og allri keyrslunni. Villuleit gerist þegar færslubókarkeyrsla er hlaðin inn og þegar önnur færslubókarlína er valin. Reiturinn **Samtala** útgáfa í upplýsingakassanum sýnir heildarfjölda vandamála sem [!INCLUDE [prod_short](includes/prod_short.md)] fundust. Hægt er að velja spjaldið til að opna yfirlit yfir úthreyfingarnar.

### <a name="work-with-sustainability-journals"></a>Vinna með sjálfbærnibækur

Til að byrja að vinna með sjálfbærnibækur skal fylgja eftirfarandi skrefum:

1.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 3.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Sjálfbærnibók** og velja síðan viðeigandi tengil.
2. Á síðunni **Sjálfbærnibók** skal færa inn eins margar línur og ætlunin er að bóka í sömu keyrslu.
3. Reiturinn Tegund fylgiskjals **má hafa auðan eða velja** Reikningur eða **Kreditreikningur**  **.**
4. Í reitnum **Reikningur nr.** er aðeins hægt að velja sjálfbærnireikninga sem ekki eru lokaðir þar sem reiturinn **Bein bókun** er valinn og reiturinn **Tegund** bókhalds er stilltur á **Bókun**. Einnig þarf að grunnstilla reikningana með tegund og undirflokki.

    > [!NOTE]
    > Ef notuð er keyrsla þar sem útblásturssviðið er grunnstillt **verður gildi útblásturssviðsins** í sjálfbærnireikningnum **að vera jafnt gildi útblásturssviðsins** í keyrslunni.

5. Annaðhvort er hægt að bóka upphæðirnar handvirkt eða nota reiknireglur.

    - Ef notandi er með réttar upplýsingar um losunina og vill bóka hann (það er, ef þú ert með upplýsingarnar á mótteknum reikningi) er reiturinn Handfært **ílag valið** til að gefa til kynna að þú munir færa upphæðirnar handvirkt inn. Í þessu tilfelli er ekki hægt að færa gögnin beint inn í reitina **Eldsneyti/rafmagn**, **Fjarlægð**, **Sérsniðin upphæð**, **Margfaldari** uppsetningar og **Tímastuðull** vegna þess að þeir verða óvirkir. Hins vegar **er hægt að breyta reitunum Útblástur CO2**, **Emission CH4** og **Emission N2O** og hægt er að færa gögnin beint inn í þá.
    - Ef ekki er til nákvæm þekking á útblæstrinum og þarf að reikna það út er reiturinn **Handfært** ílag ekki valinn. Í þessu tilviki verða reitirnir **Losun CO2**, **Emission CH4** og **Emission N2O** óbreytanlegir. Hins vegar er hægt að færa inn upplýsingar um útreikning út frá reiknireglunni sem er notuð. Fræðast meira um reiknireglur sem eru og skilgreindar í flokki **sjálfbærnireikninga** í [bókhaldslykli og fjárhag](finance-sustainability-accounts-ledger.md#account-categories).

6. Til að bóka færslubókina skal velja aðgerðina **Bóka** . Þegar bókað er í sjálfbærnibók myndast færslur í sjálfbærnibókinni.

Ef reiknireglan er byggð á valkostinum **Reikna út úr fjárhag** í flokknum Sjálfbærnireikningur verður að nota aðgerðina **Innheimta upphæð úr fjárhagsfærslum** áður en færslubókin er bókuð, til að reikna út losun á grundvelli þessarar gagnagjafa. Ef breytingar hafa verið gerðar á útblástursstuðlum eftir að færslubókarlínurnar voru útfylltar þarf að velja aðgerðina **Endurreikna** til að fá rétta upphæð í færslubókinni.

### <a name="recurring-journals"></a>Ítrekunarbækur

Ítrekunarbók er sjálfbærnibók sem hefur sérstaka reiti til að stjórna færslum sem oft eru bókaðar með fáum, ef einhverjar eru, breytist. Sem dæmi má nefna sjálfbærnihreyfingar eins og rafmagn eða hita eða aðrar áþekkar færslur. Hægt er að nota ítrekunarbækur til að bóka fastar og breytilegar upphæðir.

Þegar ítrekunarbók er notuð verður aðeins einu sinni að stofna færslur sem bókaðar eru reglulega. Upplýsingar á borð við reikninga, víddir og víddargildi haldast í færslubókinni að lokinni bókun. Í hvert sinn sem bókað er er hægt að gera þær breytingar sem þörf er á.

Reiturinn **Ítrekunarmáti** skiptir máli. Það ákvarðar hvernig upphæðin í færslubókarlínunni er meðhöndluð eftir bókun. Ef sama upphæðin er til dæmis notuð í hvert sinn sem línan er bókuð er hægt að velja valkostinn **Föst** til að láta upphæðina standa eftir bókun. Ef sömu reikningar og texti eru notaðir í línunni, en upphæðin er breytileg í hvert skipti sem er bókað, er hægt að velja kostinn **V breytilegt** til að eyða upphæðinni eftir bókun.

Reiturinn **Ítrekunartíðni** skiptir einnig máli og þarf að stilla hann. Það er dagsetningarreikniregla sem ákvarðar hversu oft færsla í færslubókarlínu er bókuð. Nánari upplýsingar í [Notkunarreiknireglur](ui-enter-date-ranges.md#use-date-formulas).

Reiturinn **Fyrningardagsetning** ákvarðar dagsetninguna þegar línan verður bókuð í síðasta sinn. Ekki er hægt að bóka línuna eftir þá dagsetningu. Kosturinn við að nota reitinn **Útrunnið, dags** . er sá að línunni er ekki eytt strax úr færslubókinni. Þú getur slegið inn síðari dagsetningu þannig að þú getir notað línuna í framtíðinni. Ef reiturinn er auður bókast línan í hvert sinn, þar til henni er eytt úr færslubókinni.

## <a name="see-also"></a>Sjá einnig .

[Fjármál](finance.md)  
[Sjálfbærnistjórnunaryfirlit](finance-manage-sustainability.md)  
[Sjálfbærniuppsetning](finance-sustainability-setup.md)  
[Bókhaldslykill sjálfbærnireikninga og fjárhagur](finance-sustainability-accounts-ledger.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
