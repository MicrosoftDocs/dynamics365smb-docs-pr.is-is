---
title: Stofna hólf
description: 'Búa til hópa af svipuðum hólfum í vinnublaði fyrir stofnun hólfs, stofna stök hólf í staðsetningaspjaldinu eða sjálfkrafa í vinnublaði fyrir stofnun hólfs.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '7368, 7369, 7370, 7371, 7372, 7373'
ms.date: 12/13/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="create-bins"></a>Stofna hólf

Skilvirkasta leiðin til að stofna hólf í vöruhúsinu er að stofna flokka samskonar hólfa á vinnublaði hólfastofnunar, en einnig er hægt að stofna stök hólf frá birgðageymsluspjaldi. Einnig er hægt að nota virkni á síðunni **Hólfastofnunarvinnublaði** til að stofna hólfs sjálfvirkt.  

## <a name="to-create-a-bin-from-the-location-card"></a>Hólf stofnaða af birgðageymsluspjaldinu:

1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Staðsetningar** og velja viðkomandi tengil.  
2.  Veljið birgðageymsluna þaðan sem á að stofna hólfið og veljið síðan aðgerðina **Hólf**.  
3. Valið er aðgerðin **Nýtt**.
4. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="the-dedicated-field"></a>Sérsniðna reiturinn

Reiturinn **Sérnýttur** á síðunni **Hólf** tilgreinir að magn í hólfinu sé varið fyrir tínslu fyrir aðrar eftirspurnir. Hins vegar er enn hægt að taka frá magn í sérnýttum hólfum. Í samræmi við það er magnið í sérnýttum hólfum tekið með í reitnum **Heildarmagn tiltækt** á síðunni **Frátekning**.

Að búa til sérnýtt hólf leiðir til svipaðrar aðgerðar í grunnvöruhúsi eins og að nota hólfategundir, sem er eingöngu hægt í ítarlegu vöruhúsi. Frekari upplýsingar eru í [Setja upp hólfategundir](warehouse-how-to-set-up-bin-types.md).

### <a name="example"></a>Dæmi

Vinnustöð er sett upp með hólfakóða í reitnum **Hólfakóði framleiðslu á innleið**. Íhlutalínur framleiðslupöntunar með þann hólfakóta krefjast þess að framvirkir íhlutir séu settir þar. Hins vegar, þar til íhlutirnir eru notaðir úr því hólfi, gætu aðrir íhlutaeftirspurnir tínt eða notað úr því hólfi vegna þess að þeir eru enn taldir tiltækt hólfainnihald. Til að tryggja að hólfainnihald sé aðeins tiltækt fyrir eftirspurn íhlutar sem notar þetta hólf framleiðslu á innleið, þarf að velja reitinn **Sérnýtt** í línunni fyrir þann hólfakóða.

> [!Caution]
> Vörur í sérstökum hólfum eru ekki varðar þegar þær eru tíndar eða notaðar sem framleiðsla eða samsetningaríhlutir með síðunni **Birgðatínsla**. Frekari upplýsingar eru í [Taka til fyrir framleiðslu eða samsetningu í einföldum vöruhúsagrunnstillingum](warehouse-how-to-pick-for-production.md).

## <a name="to-create-bins-individually-in-the-bin-creation-worksheet"></a>Stök hólf stofnuð á Hólfastofnunarvinnublaði:

1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnublað fyrir stofnun hólfs** og velja viðkomandi tengil.  
2.  Reitirnir sem nauðsynlegir eru til að nefna eru fylltir út og hólfin sem verið er að stofna eru fylltir út.  
3.  Veldu aðgerðina **Stofna hólf**.  

## <a name="to-make-bins-automatically-in-the-bin-creation-worksheet"></a>Hólf stofnuð sjálfvirkt á vinnublaði hólfastofnunar

Áður en byrjað er að stofna hólf sjálfvirkt ætti að ákvarða hvaða tegund hólfa er nauðsynleg fyrir aðgerðirnar og hagkvæmasta vöruflæðið í gegnum raunskipulag vöruhússins.  

> [!NOTE]  
> Um leið og hólf hefur verið notað er ekki hægt að eyða því nema það sé tómt. En ef á að nota annað nafnakerfi fyrir hólf er hægt að nota endurflokkunarbókina til að færa í raun vörurnar í nýja hólfakerfið. Þetta ferli er handvirkt og tímafrekt þannig að best er að setja hólfin rétt upp í upphafi.  

Til að vinna með síðuna **Hólfastofnunarvinnublaði** þarftu að vera settur upp sem starfsmaður í vöruhúsi á staðsetningunni þar sem hólfin eru. Frekari upplýsingar eru í [Setja upp vöruhússtarfsmenn](warehouse-how-to-set-up-warehouse-employees.md).    

1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnublað fyrir stofnun hólfs** og velja viðkomandi tengil.  
2.  Veldu aðgerðina **Reikna út hólf**.
3. Á síðunni **Reikna hólf** í reitnum **Kóti** hólfasniðmáts er valið hólfasniðmátið sem á að nota sem líkan fyrir hólfin sem verið er að stofna.
4.  Rituð er lýsing á hólfunum sem verið er að stofna.  
5.  Hólfakóðarnir eru stofnaðir með því að fylla út reitina **Frá nr.** og **Til nr.** í flokkunum þrem sem sýndir eru á síðunni: **Rekki**, **Geiri** og **Stig**. Hólfakótinn getur haft allt að 20 stafi.  

    > [!NOTE]  
    >  Fjöldi stafa sem færðir eru inn í flokkunum þrem fyrir hvorn reit, til dæmis stafirnir sem færðir eru inn fyrir alla þrjá reitina **Frá nr.** ásamt reitaskiltáknum, ef einhver eru, verður að vera 20 eða minni.  

     Hægt er að nota bókstafi í kóðanum sem auðkennandi samsetningu, en bókstafurinn sem notaður er verður að vera sá sami í reitunum **Frá nr.** og **Til nr.** Reitir Til dæmis væri hægt að skilgreina rekkahluta kótans sem **Frá nr. A01** og **Til nr. A10**. Forritið er ekki sett upp til að búa til kóta með bókstafaraðir, til dæmis frá A01 til F05.  

6.  Eigi að nota tákn eins og bandstrik til að aðgreina flokkareitina sem skilgreindir hafa verið sem hluti af hólfakótanum er það tákn fært inn í reitinn **Reitaskiltákn**.  
7.  Ef forritið á ekki að stofna línu fyrir hólf ef það er þegar til skal velja reitinn **Kanna í hólfi sem til er**.  
8. Þegar lokið er við að fylla út reitina er hnappurinn **Í lagi** valinn.

    Forritið stofnar línu fyrir hvert hólf á vinnublaðinu. Nú er hægt að eyða sumum hólfunum, til dæmis ef til er rekki með gönguleið gegnum fyrstu tvö stigin í nokkrum geirum.  

9. Þegar öllum óþarfa hólfum er eytt skal velja aðgerðina **Stofna hólf** og jöfnunin stofnar hólf fyrir hverja línu á vinnublaðinu.  

Ferlið er endurtekið fyrir annað safn hólfa þar til öll hólf eru stofnuð í vöruhúsinu.  

## <a name="see-also"></a>Sjá einnig .

[Yfirlit yfir vöruhúsakerfi](design-details-warehouse-management.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsakerfi sett upp](warehouse-setup-warehouse.md)    
[Samsetningardeild](assembly-assemble-items.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
