---
title: Afbrigði
description: Kynning á því hvernig þú uppfærir eftirspurnarspá fyrir hvert afbrigði af vöru í Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---

# Kynning: Afbrigði

Í þessari grein förum við í gegnum skrefin til að nota sýnigögn Contoso Coffee til að kynnast afbrigðum.

## Aðstæður

Þú ert framleiðslustjóri á Contoso Coffee. Þú verður að uppfæra eftirspurnarspá fyrir hvert afbrigði af vörunni SP-SCM1006, AutoDripLite. Þar sem þau eru með mismunandi liti þarf að ganga úr skugga um rétt framleiðsluuppskrift sé notuð fyrir hvert afbrigði. Keyrðu áætlanavinnublaðið til að reikna út framboðið.  

## Skref

1. Settu upp birgðahaldseiningar fyrir vöru SP-SCM1006 AutoDripLite. Úthlutaðu uppskrift fyrir BHE með afbrigðunum RAUTT og HVÍTT.

    1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í *Vörur* og velja síðan viðkomandi tengil.  

    2. Opnaðu vöruna **SP-SCM1006, AutoDripLite**.

    3. Valið er **Stofna birgðahaldseining** aðgerð.  

    4. Stilltu reitinn **Stofna á** á *Birgðageymsla og afbrigði*.

    5. Stilltu síu fyrir birgðageymslu á *Norður* og veldu síðan hnappinn **Í lagi**.

    6. Veldu aðgerðina **Birgðahaldseiningar**.  

    7. Uppfærðu framleiðsluuppskriftir fyrir eftirfarandi birgðahaldseiningar:

        1. RAUTT í NORÐUR, veldu SP-SCM1006-RED  

        2. HVÍTT í NORÐUR, veldu SP-SCM1006-WHITE  

        3. Halda númeri framleiðsluuppskriftar auðu fyrir SVART í NORÐUR  

2. Uppfærðu framleiðsluuppsetning og farðu eftir eftirspurnarspá í birgðageymslum og afbrigðum.  

    1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í *Uppsetning framleiðslu* og velja síðan viðkomandi tengil.  

    2. Kveiktu á reitnum **Nota spá á birgðageymslu**.

    3. Kveiktu á reitnum **Nota spá á afbrigði**.

    4. Lokaðu glugganum **Framleiðsluuppsetning**.

3. Búðu til mánaðarlega eftirspurnarspá, *AUTODRIP*. Síaðu eftir vörunni SP-SCM1006 og birgðageymslunni NORÐUR. Stilltu eftirspurn fyrir maí fyrir hvert afbrigði. 

    1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í *eftirspurnarspá* og velja síðan viðkomandi tengil.

    2. Búðu til nýja eftirspurnarspá með heitinu *AUTODRIP*.

    3. Veldu aðgerðina **Breyta eftirspurnarspá**.

    4. Í reitnum **Skoða eftir** skal velja *Mánuður*.

    5. Í reitnum **Vörusía** skal velja *SP-SCM1006*

    6. Kveiktu á reitnum **Nota spá á birgðageymslu**.

    7. Í reitnum **Birgðageymslusía** skal velja *NORÐUR*.

    8. Kveiktu á reitnum **Nota spá á afbrigði**.

    9. Fyrir hverja línu eru uppfærð gildi í maí dálkinum

        1. RAUTT í NORÐUR , velja 100

        2. HVÍTT í NORÐUR, velja 200

        3. SVART í NORÐUR, velja 300

    10. Loka gluggum eftirspurnarspáar

4. Keyrðu MPS-áætlun í maí fyrir stofnaðar eftirspurnarspár. Farðu yfir íhluti til að sjá hvort málning vöru samsvari afbrigði.

    1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í *Áætlunarvinnublað* og velja síðan viðkomandi tengil.

    2. Velja **Reikna áætlun endurgerðar** aðgerðina.

    3. Kveiktu á reitnum **MPS**.

    4. Slökktu á reitnum **MPS**.

    5. Í reitnum **Upphafsdagsetning** skal velja *1. maí*

    6. Í reitnum **Lokadagsetning** skal velja *31. maí*

    7. Í reitnum **Nota spá** skal velja *AUTODRIP*

    8. Velja aðgerðina **Í lagi**.

    9. Fyrir hverja stofnaða línu skal velja aðgerðina **Íhlutir** og fara yfir hvaða málning er notuð.  

## Sjá einnig .

[Kynning á sýnigögnum Contoso Coffee](contoso-coffee-intro.md)  
