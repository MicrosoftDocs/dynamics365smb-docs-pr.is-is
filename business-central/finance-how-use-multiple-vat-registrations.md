---
title: Mörg VSK-númer
description: Fræðast um aðgerðirnar fyrir mörg (önnur) virðisaukaskattsnúmer (VSK).
author: altotovi
ms.topic: conceptual
ms.reviewer: null
ms.search.keywords: 'VAT, multiple, alternative, customer, tax, value-added tax'
ms.search.form: '212, 301,'
ms.date: 08/21/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Mörg VSK-númer 

Fyrir fyrirtæki með vöruhús í mörgum ESB-löndum getur stjórnun VSK (Virðisaukaskattur) verið ögrandi þar sem hver vöruhúsastaður þarfnast annars VSK-númers til að fara eftir tilteknum reglum hvers lands. Í þessari grein eru upplýsingar um þessa þörf og hún skýrir virkni fyrir mörg virðisaukaskattsnúmer (VSK). Þessi aðgerð gerir notendum kleift að setja upp skattskráningarnúmer fyrir viðskiptamenn sína í mismunandi löndum/svæðum.  

> [!NOTE]
> Mörg *VSK-númer fyrir* viðskiptamenn eru aðeins fáanleg úr Business Central 2024 útgáfubylgju 2 (útgáfa 25).

## Hvernig setja á upp önnur VSK-númer  

Til að setja upp önnur VSK-númer fyrir mismunandi lönd/svæði skal fylgja eftirfarandi skrefum: 

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **aðra VSK-skráningu** viðskiptamanns og velja síðan tengda tengja. 
2. Viðskiptamanninum er bætt við í reitnum **Númer viðskiptamanns** og landi/svæði sem tengist þessari VSK-skráningu í **LANDs-/svæðiskóta VSK**.  
3. Vsk-númerið verður að bæta við í reitnum **VSK-númer.** akur. Halda verður á sniðinu þegar lands-/svæðiskóti er **notaður**. 
4. Ef nota á mismunandi VSK eða almenna bókunarflokka er hægt að bæta þeim við uppsetninguna í reitunum **VSK viðsk.bókunarflokkur** og **Alm. viðsk.bókunarflokkur** . 
5. Loka síðunni.   

Til að stofna annað aðsetur fyrir viðskiptamanninn er skrefunum fylgt:  

1.  **Opna skal Viðskiptamannaspjald** viðskiptamannsins sem bæta á við nýju **sendist-til aðsetri**. 
2. Velja skal **Viðskiptamaður** og velja aðgerðina **Sendist-til aðsetur** .   
3. Síðan **Sendist-til aðsetur - Listi opnast** og velur **Nýtt**. 
4. Upplýsingar um sendist-til áfangastaðar viðskiptamanns eru færðar inn.  
5. Réttur **lands-/svæðiskóti er** valinn.   
6. Hafi nýtt **VSK-númer þegar verið grunnstillt.** í **VSK-skráningu** annars viðskiptamanns í þessu landi eða svæði gerist ekkert. 
7. En ef VSK-númerið var ekki grunnstillt **.** áður á VSK-skráningu **annars viðskiptamanns í þessu landi eða svæði birtist eftirfarandi tilkynning:** Smellt er á Bæta við ef setja á **inn aðra VSK-skráningu fyrir þennan sendist-til landskóta.** 
8. Tilkynning birtist sem viðvörun um að bæta skuli við nýju VSK-númeri. Til að gera það þarf að velja Aðgerðina **Bæta við** á tilkynningunni **og síðan Vsk-skráning** annars viðskm. opnast. 
9. Þessi síða færir viðskiptamannsnúmer notanda í reitinn **Númer viðskiptamanns.**  **og lands-/svæðiskóta** VSK. Svo þarf bara að bæta við uppsetningu sem á að nota. 

## Vinna við söluskjöl   

Hægt er að stofna nýjan [sölureikning](sales-how-invoice-sales.md) eða [sölupöntun](sales-how-sell-products.md) í [!INCLUDE[prod_short](includes/prod_short.md)]. Ef nota þarf sendist-til aðsetur sem er frábrugðið aðsetri viðskiptamannsins og er staðsett í öðru landi er skrefunum fylgt:  

### Annað afhendingaraðsetur  

1. Flýtiflipinn **Afhending og Reikningsfæra** er stækkaður.   
2. Í reitnum Sendist-til skal velja valkostinn **Annað afhendingaraðsetur** . 
3. Síðan **Sendist-til aðsetur - Listi** með tiltækum aðsetrum birtist. 
4. Eitt af aðsetrunum með mismunandi **lands-/svæðiskóta** er valið. 
5. Þá birtist svarglugginn **Staðfesta VSK-skráningu** annars viðskiptamanns með lista yfir reiti sem hefur verið breytt vegna breytinga á **VSK-uppsetningu** annars viðskiptamanns. 
6. Valið er **Í lagi** til staðfestingar.   

> [!NOTE]
> Ef ekki á að staðfesta slíkt lengur er hægt að velja reitinn **Sýna ekki aftur** og í framtíðinni sjást ekki svona tilkynningar um breytingar. En ef gera á hana virka aftur er hægt að gera það með því að gera reitinn **Staðfesta aðra VSK-skráningu** í VSK-uppsetningunni **virkan**.  
   
7. Þegar staðfest hefur verið er skrifað yfir gildin úr **UPPSETNINGU VSK-viðskiptamanns** . Hægt er að kanna alla VSK-tengda reiti sem eru á flýtiflipanum **Sundurl. reikningur** .  
8. Skjalið bókað.  

### Sérsniðið aðsetur  

Ef ekki er búið að grunnstilla sendist-til aðsetrið en nota á annað aðsetur fyrir afhendingu er hægt að nota þennan valkost.  

1. Flýtiflipinn **Afhending og Reikningsfæra** er stækkaður.   
2. Í reitnum Sendist-til er valkosturinn Sérsniðið **aðsetur** valinn.  
3. Breyta skal landi í reitnum **Land/svæði** .  
4. Þegar lands-/svæðiskótanum hefur verið breytt til samræmis við **VSK-lands-/svæðiskóta**  **vsk-kóta** annars viðskiptamanns birtist svarglugginn **Staðfesta VSK-skráningu** annars viðskm. með lista yfir reiti sem hefur verið breytt. 
5. [!INCLUDE[prod_short](includes/prod_short.md)] einnig verður öllum VSK-tengdum reitum sem eru í flýtiflipanum **Sundurl** . reikningur breytt.  

### Vinna án sendingar 

Ef engin afhending er til sem vinnsla er samt hægt að breyta úr **uppsetningu VSK-viðskiptamanns** .

Í sölupöntuninni eða reikningnum **má finna lands-/svæðiskóta** VSK á flýtiflipanum **Sundurl** . reikningur og tilgreina gildið sem samsvarar **uppsetningu VSK-viðskiptamanns** . Og þú ættir að sjá sömu staðfestingarsvarglugga og hér að ofan. 

Í slíkum tilvikum er hægt að bóka sölureikning með réttu **VSK-númeri.** viðskiptamanni þó að vörur séu ekki afhendar með þessu fylgiskjali. 

### Vinna við sölukreditreikninginn  

Þegar reikningurinn er bókaður með **sendist-til aðsetri** eða **LANDs-/svæðiskóta** VSK sem hefur mismunandi bókunargögn tekur leiðrétta **sölukreditreikningurinn** gildin úr **bókaða sölureikningshausnum** þar sem þessi gildi eru tekin úr **VSK-skráningu** annars viðskiptamanns, svo ekki sé þörf á öðrum aðgerðum. 

## Sjá einnig .

[Yfirlit VSK-stjórnunar](finance-manage-vat.md)    
[Setja upp virðisaukaskatt](finance-setup-vat.md)    
[Unnið með VSK í sölu og innkaupum](finance-work-with-vat.md)    
[Tilkynna VSK til skattyfirvalda](finance-how-report-vat.md)    
[Staðbundin virkni í Business Central](about-localization.md)    


[!INCLUDE[footer-include](includes/footer-banner.md)]
