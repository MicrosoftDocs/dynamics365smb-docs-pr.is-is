---
title: Stofna nýja framleiðsluuppskrift og uppskriftarútgáfu
description: Kynning til að komast að því hvernig á að bæta annarri kaffivél við vörulínu Contoso Coffee í Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---
# <a name="walkthrough-create-a-new-production-bom-and-bom-version" />Kynning: Stofna nýja framleiðsluuppskrift og uppskriftarútgáfu

Í þessari grein förum við í gegnum skrefin til að nota sýnigögn Contoso Coffee til að vinna með uppskriftir í framleiðsluferlunum.  

## <a name="scenario" />Aðstæður

Contoso Coffee hefur ákveðið að bæta við annarri kaffivél við vörulínuna: **SP-SCM1008 Airpot Lite**. Þessi kaffivél er eins og núverandi vara **SP-SCM1009 Airpot**, nema að hún inniheldur ekki hitaplötuna, **SP-BOM1104**. Í aðskildu skrefi er ljósrofinn **SP-BOM1106** fjarlægður fyrir útgáfu af uppskrift Airpot Lite.

Oscar, ferlahönnuður hjá Contoso Coffee, verður að setja upp nýja framleiðsluuppskrift til að skilgreina upphaflegar þarfir íhluta fyrir Airpot Lite. Oscar verður þá að setja upp nýja UPPSKRIFTARÚTGÁFU, með upphafsdegi 01. júlí, til að samræma við frekari áætlanir um að gefa út aðra útgáfu.

## <a name="steps" />Skref

1. Stofnaðu nýja framleiðsluuppskrift fyrir Airpot Lite.

    1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Framleiðsluuppskrift** og velja síðan viðkomandi tengil.  

    2. Veldu aðgerðina **Nýtt** og fylltu svo út reitina eins og lýst er í eftirfarandi töflu.  

        |Svæði  |Virði  |
        |---------|---------|
        |**Nr.** |SP-SCM1008|
        |**Lýsing** |Airpot lite|
        |**Mælieiningarkóði**|PCH  |

2. Afritaðu íhluti uppskriftar úr framleiðsluuppskriftinni **SP-SCM1009**.

    1. Veldu aðgerðina **Afrita uppskrift**.

    2. Á síðunni **Framleiðsluuppskriftir** skal velja línuna fyrir **SP-SCM1009 Airpot** og síðan velja hnappinn **Í lagi**.

3. Breyttu íhlutunum fyrir nýju framleiðsluuppskriftina eins og lýst er í sviðsmyndinni.

    1. Í flýtiflipanum **Línur** skal velja línuna fyrir vöruna **SP-BOM1104** og síðan velja aðgerðina **Eyða línu**.  

4. Vottaðu nýju uppskriftina.  

    1. Í reitnum **Staða** skal velja *Vottað*.  

5. Stofnaðu útgáfu framleiðsluuppskriftar fyrir Airpot Lite.

    1. Veldu aðgerðina **Útgáfur**.

    2. Á síðunni **Útgáfulisti framl.uppskr** skal velja aðgerðina **Ný** og síðan fylla út reitina eins og lýst er í eftirfarandi töflu.  

        |Svæði  |Virði  |
        |---------|---------|
        |**Útgáfukóði** |02|
        |**Lýsing** |Airpot Lite, v2|
        |**Mælieiningarkóði**|PCH  |  
        |**Upphafsdagsetning**|01. júlí  |  

6. Afritaðu íhlutalínurnar úr framleiðsluuppskriftinni í nýju uppskriftarútgáfuna.

    1. Veldu aðgerðina **Afrita uppskrift** veldu síðan hnappinn **Já** til að afrita íhlutina úr upprunalegri framleiðsluuppskrift.

7. Fjarlægðu vöruna **SP-BOM1106, Ljósrofi** úr íhlutum útgáfunnar.

8. Vottaðu nýju uppskriftarútgáfuna.

    1. Í reitnum **Staða** skal velja *Vottað*.  

    2. Lokaðu uppskriftarútgáfunni

Nýja kaffivélin er nú sett upp sem framleiðsluuppskrift með einni útgáfu.  

## <a name="see-also" />Sjá einnig .

[Kynning á contoso kaffi sýnigögnum](../contoso-coffee-intro.md)  
