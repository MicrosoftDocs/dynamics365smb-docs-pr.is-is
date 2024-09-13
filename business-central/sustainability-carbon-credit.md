---
title: Vinna með kolefnisskuldir
description: Læra hvernig á að setja upp og kaupa kolefnisskuld.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, carbon, credit, CO2'
ms.search.form: null
ms.date: 08/20/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: solsen
---

# Vinna við kolefnisskuld  

Þegar fyrirtæki geta ekki dregið úr losun sinni af ýmsum ástæðum geta þau keypt kolefnisskuldir til að mótfæra losun sína. Með því að kaupa kolefnisskuldir getur fyrirtæki enn gefið frá sér jafngilt magn af gastegundum en það sem eftir er af kolefnishlutlaust. Þessar kreditfærslur eru keyptar af sérhæfðum veitendum og hvatir til þess að draga úr losun.  

Almennt eru kolefnisskuldir leyfi sem gera eiganda kleift að gefa frá sér ákveðið magn af koltvísýringi (CO₂) eða öðrum gróðurhúsalofttegundum (GHGs). Ein kolefnisskuld gefur gjarnan til kynna rétt til að gefa frá sér einn mælikvarða af CO₂ eða jafngilt magn af öðru GHG, svo mikilvægt er að gera þennan valkost virkan fyrir sum fyrirtæki.  

## Setja upp kolefnisskuld  

Hægt er að stilla kolefnisskuldina [!INCLUDE[prod_short](includes/prod_short.md)]  **sem vöru**. Til að setja vöruna **upp** sem kolefnisskuld er skrefunum fylgt:
  
1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **Vörur** og velja síðan viðeigandi tengja. 
2. [Stofna nýja vöru eins og útskýrt er](inventory-how-register-new-items.md).   
3. Þegar varan hefur verið stofnuð er reiturinn GHG-kredit valinn **á flýtiflipanum** Sjálfbærni **og virði kolefnisskuldarinnar bætt við með reitnum** Kolefnisskuld á UOM **.** 

> [!NOTE]
> **Kolefnisskuld á UOM** stendur fyrir magn CO₂ í mælieiningunni sem stillt er í **mælieiningarkóta losunarmælieiningarinnar** í **sjálfbærniuppsetningunni**. Þannig þýðir þetta heildarvirði kolefnisskuldar sem upphæð kreditfærðs CO₂ á eina **grunnmælieiningu** notaðrar vöru.  

> [!NOTE]
> Hægt er að setja upp hvaða tegund af vöru sem er, hvort sem það er birgðir, þjónusta eða ekki í birgðum, sem kolefnisskuld.  

## Til að kaupa kolefnisskuld 

### Innkaupaskjöl 

Til að vinna með öll fylgiskjöl sem tengjast innkaupum skal fylgja skrefunum:

1.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 3.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd og:  
   1. Innkaupareikningar eru færðir **inn** ef reikningsfæra á sem **tegund** fylgiskjals og síðan valin tengd tengja.  
   2. Innkaupapantanir eru færðar **inn** ef ætlunin er **að panta sem tegund** fylgiskjals og síðan valdar tengdar tengja.   
2. Haus fylgiskjals er fylltur út frá eftirfarandi leiðbeiningum [um hvernig á að vinna með innkaupareikninga og pantanir](purchasing-how-record-purchases.md). 
3. Velja vöruna sem kolefnisskuld í reitnum **Nr.** í innkaupaskjalslínunum og viðeigandi **Magn** og **Innk.verð** bætt við. 
4. Reitnum **Sjálfbærnireikningur nr.** þú myndi nota til að minnka koltvísýringsgildið (CO₂). Kerfið færir sjálfkrafa inn gildið í reitnum Losun CO2 **samkvæmt gildinu sem hefur verið grunnstillt í reitnum** Kolefnisskuld á UOM **á** birgðaspjaldinu **.** 
5. Skjalið bókað.

> [!NOTE]
> Þótt kolefnisskuldin muni minnka virði færslna sést jákvætt virði í **losun CO2**. En þegar skjalið er bókað sést gildi með neikvæða skráningu í **Sjálfbærnibókarfærslunni** með **GHG-kredit** sem **tegund** fylgiskjals.  

### Sjálfbærnibækur 

Til að vinna með **sjálfbærnibók** skal fylgja skrefunum:  

1.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 3.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **Sjálfbærnibók** og velja síðan viðeigandi tengja. 
2. Á síðunni **Sjálfbærnibók** skal færa inn eins margar línur og ætlunin er að bóka í sömu keyrslu.  
3. GHG-kredit **er** valið í reitnum **Tegund** fylgiskjals.    
4. Í reitnum **Reikningur nr.** er aðeins hægt að velja sjálfbærnireikninga sem ekki eru lokaðir þar sem **bein bókun**  svæðið er valið og reiturinn **Tegund** bókhalds er stilltur á **Bókun**. Einnig þarf að grunnstilla reikningana með tegund og undirflokki. Velja skal viðeigandi reikning til að bóka kolefnisskuldir.
5. Handvirk ílag er valið **og gildið sem á að bóka sem kolefnisskuld fært** inn í reitinn **Losun CO2** .  
6. Bóka skal færslubókina.   

## Sjá einnig .

[Fjármál](finance.md)    
[Skrá sjálfbærnifærslur](finance-sustainability-journal.md)    
[Yfirlit yfir sjálfbærnistjórnun](finance-manage-sustainability.md)    
[Sjálfbærniuppsetning](finance-sustainability-setup.md)   
[Bókhaldslykill sjálfbærnireikninga og fjárhagur](finance-sustainability-accounts-ledger.md)  
[Tilfallukkagreining á sjálfbærnigögnum](ad-hoc-analysis-sustainability.md)    
[Sjálfbærniskýrslur og greiningar í [!INCLUDE[prod_short](includes/prod_short.md)]](sustainability-reports.md)   
[API sjálfbærni](/dynamics365/business-central/dev-itpro/api-sustainability/sustainability-api?toc=/dynamics365/business-central/toc.json)    
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
