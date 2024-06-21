---
title: Vinna með eignir
description: Skrá viðgerðir og þjónustu á eign til að varðveita verðmæti hennar.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'repair, service'
ms.search.form: '5642, 5625'
ms.date: 05/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="maintain-fixed-assets"></a>Vinna með eignir

Viðhaldskostnaður er rekstrarkostnaður vegna þess sem gert er til að varðveita skilyrði eignanna. Ólíkt endurbótum á fjármagni eykur viðhald ekki verðmæti eignanna.

Í hvert sinn sem eign er send til þjónustu skráir notandi upplýsingar eins og þjónustudagsetningu, lánardrottininn sem vann vinnuna og símanúmer þjónustufulltrúa. Viðhaldsupplýsingar eru færðar inn á nokkrar síður:

* Eignaspjald
* Innkaupapöntun
* Innkaupareikningur
* Eignafjárhagsbók

Endurmat er notað til að laga virði að almennum verðbreytingum. Nota aðgerðina **Endurmat eigna** til að endurreikna viðhaldskostnað.

## <a name="record-a-maintenance-cost-directly-on-a-fixed-asset"></a>Skrá viðhaldskostnað beint á eign

Í hvert sinn sem viðhald er gert fyrir eign, t.d. þjónustuheimsókn, er hægt að skrá það á síðuna **Skráning viðhalds** .  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eignir** og velja síðan viðkomandi tengil.  
2. Valin er eignin sem á að skrá viðhald fyrir og veldu síðan aðgerðina **skráning viðhalds**.
3. Fyllt er út í reiti eftir því sem á við á síðunni **Skráning viðhalds**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="post-maintenance-costs-from-a-fixed-asset-gl-journal"></a>Bóka viðhaldskostnað úr eignafjárhagsbók

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Afskriftabókarlisti** og velja síðan viðkomandi tengil.  
2. Veljið afskriftabókina sem er tengd eigninni og veljið síðan aðgerðina **breyta**.
3. Á síðunni **Afskriftabókarspjald** þarf að ganga úr skugga um að **gátreiturinn Viðhald** sé ekki valinn svo að viðhaldskostnaður sé ekki bókaður í fjárhag.
4. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eignafjárhagsbók** og velja síðan viðkomandi tengil.  
5. Stofnaður er upprunaleg Færslubókarlína og reitirnir fylltir út eftir þörfum.
6. Í reitnum **Eignabókunartegund** er valinn **viðhald**.
7. Valið er **Setja inn mótreikn. eigna** aðgerð. Seinni færslubókarlína er búin til fyrir mótreiknings sem er sett upp fyrir bókun viðhalds.

    > [!NOTE]  
    > Skref 7 virkar aðeins ef eftirfarandi er sett upp: Á **síðunni Eignabókunarflokksspjald** fyrir bókunarflokk eignar **er í reitnum Viðhaldsreikningur** debetreikningur fjárhags og í reitnum **Reikningur viðhalds mótreiknings er fjárhagsreikningurinn** sem á að bóka jöfnunarfærslur fyrir uppfærslu á. Frekari upplýsingar er að finna í [Að setja upp bókunarflokka eigna](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
8. Valið er **Bóka** aðgerðin.

## <a name="record-maintenance-cost-from-a-purchase-invoice"></a>Skrá viðhaldskostnað úr innkaupareikningi

Eftirfarandi skref útskýra hvernig á að skrá viðhaldskostnað eignar úr innkaupareikningi. Skrefin eru svipuð fyrir innkaupapöntun.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupareikningur** og velja síðan viðkomandi tengil.
2. Fyllt er út í reiti eftir því sem er nauðsynlegt í flýtiflipanum **Almennt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Á flýtiflipanum **Línur** í reitnum **Tegund** skal velja **Eign**.
4. Í reitnum **númer** Skal velja eignina og tilgreina síðan magn og kostnað.
5. Í reitnum **Eignabókunartegund** er valið **Viðhald**.
6. Innkaupareikningurinn er bókaður.

## <a name="follow-up-on-service-visits"></a>Fylgja eftir þjónustuheimsóknum

Hægt er að prenta skýrsluna **Viðhald - Næsta þjónusta** til að skrá eignirnar sem eru áætlaðar vegna þjónustu. Einnig má nota þessa skýrslu þegar uppfæra á reitinn **Næsta þjónustudags** . á eignaspjöldum.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðhald - Næsta þjónusta** og velja síðan viðkomandi tengil.  
2. Reitirnir **Upphafsdagsetning** og **Lokadagsetning** eru fylltir út.  
3. Veljið hnappinn **Prenta** eða **Forskoðun**.

## <a name="monitor-maintenance-costs"></a>Fylgjast með viðhaldskostnaði

Hægt er að skoða upplýsingar til að fylgjast með viðhaldskostnaði.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eignir** og velja síðan viðkomandi tengil.
2. Valin er eignin sem á að skoða viðhaldskostnað fyrir og veldu síðan aðgerðina **afskriftabækur**.
3. Á síðunni **Eignaafskriftabækur** er valin viðeigandi eignaafskriftabók og síðan er aðgerðin **Upplýsingar** valin.
4. Á síðunni **Eignaupplýsingar** er valið **viðhald** .

 **Síðan Viðhaldsfærslur** er notuð til að skoða færslurnar sem mynda upphæðina í reitnum **Viðhald** .

## <a name="view-or-print-maintenance-costs-for-multiple-fixed-assets"></a>Skoða eða prenta viðhaldskostnað fyrir margar eignir

Í skýrslunni **Viðhald - Greining** er hægt að velja að skoða viðhald samkvæmt einum, tveimur eða þremur viðhaldskótum á tiltekinni dagsetningu eða tímabili. Skýrslan getur sýnt samtölu allra valinna eigna eða samtölu hverrar eignar.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðhald - Greining** og velja síðan viðkomandi tengil.
2. Fyllið inn reitina eftir þörfum.
3. Veljið hnappinn **Prenta** eða **Forskoðun**.

## <a name="view-maintenance-ledger-entries"></a>Skoða viðhaldsfærslur

Einnig er hægt að skoða viðhaldskostnað með því að skoða viðhaldsfærslurnar.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eignir** og velja síðan viðkomandi tengil.
2. Valin er eignin sem á að skoða fjárhagsfærslur fyrir og veldu síðan aðgerðina **afskriftabækur**.
3. Á síðunni **Eignaafskriftabækur** er valin viðeigandi eignaafskriftabók og síðan er aðgerðin **Viðhaldsbókarfærslur** valin.

## <a name="view-or-print-maintenance-ledger-entries-for-multiple-fixed-assets"></a>Skoða eða prenta viðhaldsfærslur fyrir margar eignir

Í **Viðhald - Sundurliðun** skýrslu er hægt að skoða eða prenta viðhaldsbókarfærslur fyrir eina eða margar eignir.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðhaldsupplýsingar** og velja síðan viðkomandi tengil.
2. Fyllið inn reitina eftir þörfum.
3. Veljið hnappinn **Prenta** eða **Forskoðun**.

## <a name="see-also"></a>Sjá einnig .

[Eignir](fa-manage.md)  
[Uppsetning eigna](fa-setup.md)  
[Fjármál](finance.md)  
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
