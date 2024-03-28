---
title: Selja hluti sem eru settir saman í pöntun
description: Lærðu að selja vöru sem er sett saman til að panta.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 11/23/2022
ms.search.keywords: 'kit, kitting, substitute items'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
ms.custom: bap-template
---
# <a name="sell-items-assembled-to-order"></a>Selja hluti sem eru settir saman í pöntun

Vörur sem settar eru upp fyrir samsetningum eru ekki væntanlegar í birgðum og verða settar saman þegar þær eru hafðar með í sölupöntun. Vara er sett upp fyrir saman til-pöntunar þegar  **reiturinn Samsetningarregla**  á birgðaspjaldinu  **er settur saman við pöntun**. Þegar varan er færð inn á sölupöntunarlínu er samsetningarpöntun stofnuð sjálfkrafa og hún tengd við sölupöntunina.  

> [!NOTE]  
> Ef vörur með samsetningum eru þegar til í birgðum er hægt að draga það magn úr samsetningarpöntuninni og taka þær frá birgðum. Lærðu meira á  [að selja birgðavörur í saman-til-panta flæði](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

Í þessu ferli er sala vöru sem verður sett saman samkvæmt óskum viðskiptamannsins meðhöndluð. Skrefin eru: 

* Sölupöntunarlína stofnuð.
* Samsetningaratriði sérsniðin með því að breyta íhlutum þess og forða.
* Kanna til ráðstöfunar til að koma á afhendingardagsetningu.
* Gefa út sölupöntunina sem á að setja saman og senda strax.  

> [!NOTE]  
> Í eftirfarandi ferli eru ekki skrefin til að stofna staðlaða sölupöntun sem gerist fyrir skrefið þar sem fært er inn sölupöntunarvöruna í sölupöntunarlínu. Frekari upplýsingar um stofnun sölupantana í  [selja vörur með sölupöntun viðskiptavinar](sales-how-sell-products.md).  

## <a name="to-sell-an-item-that-is-assembled-to-order"></a>Til að selja vöru sem er sett saman í pöntun

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.  
2. Stofnið sölupöntun. 
3. Í reitnum **númer** færið inn vöru sem stillt eru til að setja saman í pöntun.  
4. Í reitnum **Kóti birgðageymslu** er tilgreind sú birgðageymsla sem varan mun verða seld frá. Samsetningarferlið fer fram í þeirri birgðageymslu.  
5. Í reitnum **Magn** er fært inn hversu margar einingar á að selja.  

    > [!NOTE]  
    >  Ef einn eða fleiri íhlutir umbeðins samsetningarmagns eru ekki tiltækir, opnast viðvörunarsíða til ráðstöfunar. <!-- Check whether the field help would be useful. For more information, see Assembly Availability.  -->

    Samsetningarpöntun er stofnuð og tengd við sölupöntunarlínuna. Gjalddagi samsetningarpöntunar er afhendingardagsetning sölupöntunarlínunnar.  

    Magnið sem á að selja er afritað í  **Magn til að taka saman í röð**  sem gefur til kynna að vöruuppsetningin býst við að hægt sé að setja saman heildarmagnið í sölulínunni. Hægt er að minnka magnið til að setja saman, t.d. Ef vitað er að sumar vörur eru þegar tiltækar. Lærðu meira á  [að selja birgðavörur í saman-til-panta flæði](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

6. Ef viðskiptavinurinn vill fá viðbótarvöru í Raðhús, á  **fastflipanum línur**, veljið  **þá Línuaðgerð**, veljið  **setja saman við pantanaaðgerðina**  og veljið  **svo aðgerðina Setja saman við pöntunarlínur**  til að skoða og breyta stöðluðum samsetningaríhlutum. Að öðrum kosti skal velja reitinn **Magn til samsetningar til pöntunar**.  
7.  **Á síðunni setja saman pöntunarlínur**  til að stofna nýja línu af gerðinni  **Vara**  fyrir viðbótarsamsetningaríhlutinn.  

    Einnig er hægt að sérsníða pöntunina með því að auka magnið með einni staðlaðri vöru í settinu. Hægt er að gera þetta með því að auka gildið í reitnum **Magn á** á viðkomandi samsetningarpöntunarlínu.  

    > [!NOTE]  
    >  Á  **síðunni setja upp línur**  á milli lína eru grunnsvæðin til að sérsníða íhlutalilið, bæta við vörurakningarnúmerum eða leysa vandamál vegna ráðstöfunar íhluta. Til að bæta við fleiri upplýsingum um  **samsetningarpöntun, eins og upphafsdagsetningu samsetningarpöntunar, er aðgerðin Sýna skjöl**  valin. Þá opnast fullt yfirlit yfir samsetningarpöntunina sem er tengd við sölupöntunarlínuna. Ekki er hægt að breyta innihaldi flestra reita í samsetningarpöntunarhausnum og ekki er hægt að bóka úttak frá því. Bóka verður sendinguna í sölupöntunarlínuna.  
    >
    >  Í tengdum samsetningarpöntunum er einungis  **hægt að breyta upphafsdagsetningu** . Breytingar á upphafsdagsetningunni með því að starfsmenn samsetningarmenn tilgreina að þeir séu að hefja samsetningu á undan gjalddagann. Öllum reitum í línunum á tengdu samsetningarpöntuninni er hægt að breyta svo að vöruhússstarfsmenn geti fært inn notkunartölur við vinnsluna.  

8. Fara skal yfir eða bregðast við vandamálum með ráðstöfun íhluta. Veljið til dæmis staðgengilsvara.  
9. Loka síðunni **Setja saman í pöntunarlínur**. Tengda samsetningarpöntunin er tilbúin og geta starfsmenn byrjað að taka saman sérsniðnu vörurnar.  
10. Á sölupöntuninni skal velja **Losa** aðgerðina til að tilkynna samsetningardeildinni að sem samsetningarferlið geti hafist. Lærðu meira að  [setja saman vörur](assembly-how-to-assemble-items.md).  

> [!NOTE]  
> Staðgengur vöru skipta ekki sjálfkrafa um vöru með aðra vöru, til dæmis þegar sölupöntun er stofnuð eða í UPPSKRIFT. Þess í stað færðu viðvörun að því gefnu að staðgengilslíkur sé fyrir hendi.

## <a name="see-also"></a>Sjá einnig .

[Samsetningardeild](assembly-assemble-items.md)  
[Vinna með samsetningaruppskriftir](assembly-how-work-assembly-boms.md)  
[Skrá nýjar vörur](inventory-how-register-new-items.md)  
[Birgðir](inventory-manage-inventory.md)  
[Warehouse Management Overview](design-details-warehouse-management.md)
[Work with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
