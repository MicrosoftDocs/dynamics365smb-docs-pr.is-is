---
title: Kynning á sýnigögnum Contoso Coffee
description: Yfirlit yfir áætlanir um hvernig contoso kaffi sýnishorn gögn geta aðstoðað við að læra hvernig nýta má getu í viðskiptafræði miðlægt.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 4760
author: edupont04
ms.author: andreipa
---

# Kynning á sýnigögnum Contoso Coffee

Contoso Coffee er skáldað fyrirtæki sem framleiðir kaffivélar fyrir neytendur og fyrirtæki. The  **contoso Coffee**  apps fyrir Business Central bæta við sýnigögnum sem þú getur notað til að læra hvernig á að nota getu í viðskiptafræði Central.  


## Setja upp Contoso Coffee gögn

Til að nota sýnigögn Contoso Coffee þarftu að setja upp tvö forrit í viðeigandi fyrirtæki í [!INCLUDE [prod_short](../includes/prod_short.md)]:  

- **Gagnamengi Contoso Coffee**  

    Þetta forrit afhendir sýnigögn fyrir grunnforritið.  
- **Sýnigagnamengi Contoso Coffee (auðkenni lands)**  

    Þetta forrit bætir landsbundnu efni við efst í grunnforritið.

Bættu forritunum við autt fyrirtæki í greiddri áskrift eða sem hluti af prufuáskrift. Stofnaðu til dæmis nýtt fyrirtæki með engin sýnigögn úr uppsetningarleiðbeiningunni **Stofna nýtt fyrirtæki** sem hægt er að opna úr listanum **Fyrirtæki**. Bættu síðan við forritunum úr [markaðstorginu](../ui-extensions-install-uninstall.md#install) ef þau eru ekki þegar sýnd á síðunni **Viðbótastjórnun**.  

Þú skalt þá ljúka:
 -  [Uppsetning](manufacturing/contoso-coffee-manufacturing-intro.md)  framleiðslu til undirbúnings fyrir notkun á  [framleiðsluaðstæðum](#manufacturing-scenarios)
 -  [Uppsetning](warehousing/contoso-coffee-warehousing-intro.md)  vöruhúsa til undirbúnings fyrir notkun á  [vöruhúsaaðstæðum](#warehousing-scenarios)

## Framleiðsluaðstæður

Gögnin á contoso Coffee sem nú styður eftirfarandi framleiðsluáætlanir fyrir próf og þjálfun:

1. [Stofna nýja framl. UPPSKRIFT og UPPSKRIFTARÚTGÁFU](manufacturing/create-new-production-bom-version.md)  
2. [Stofna nýja leið](manufacturing/create-new-routing.md)  
3. [Stofna fastáætlaða framleiðslupöntun og breyta henni](manufacturing/create-firm-planned-production-order-change.md)  
4. [Sameina sjálfvirka og handvirka Flushing](manufacturing/combine-automatic-manual-flushing.md)  
5. [Nota Pantanáætlanagerð til að stofna og taka frá framboð](manufacturing/order-planning-create-reserve-supply.md)  
6. [Setja upp og vinna Úthýsingaraðgerð](manufacturing/set-up-process-subcontracting-operation.md)  
7. [Setja upp nýtt geymslurými](manufacturing/set-up-new-capacity.md)  
8. [Spáreftirspurn fyrir vöruafbrigði með mismunandi uppskriftum](manufacturing/variants.md)  

Lestu skrefin fyrir hverjar aðstæður í viðkomandi grein.  

> [!IMPORTANT]
> Framleiðsluferlar krefjast þess að notendaupplifun sé stillt á  *aukagjald*  á  **upplýsingasíðu**  félagsins.

## Vöruhúsaaðstæður

The contoso kaffi sýnikennsla styður nú við eftirtaldar vöruhúsáætlanir fyrir próf og þjálfun:

1.  Skilgreina sjálfgefin hólf, taka á móti og ganga frá með birgðafrágangi, velja og senda með birgðatínslu í pöntunar-eftir-pöntun tíska með  [walkmeð um inn-og úttengi í Grunnvöruafbrigði](warehousing/warehouse-basic-flow-putaway-pick.md)
2.  Móttaka og frágangur margar pantanir á innleið í einu með vöruhúsamóttöku, skipa mörgum pöntunum í einu með vöruhúsaafhendingu, tínslur með vöruhúsatiltekt með  [walkmeð-með inn-og útflæði í Blönduðum Vöruhúsafbrigðum](warehousing/warehouse-mixed-flow-receive-pick-ship.md)
3.  Skilgreinið föst hólf fyrir mælieiningu vörunnar, hjáskipun notanda til að draga úr flutningi á vörum, setja vörur með áfyllingu hólfs, magn stórra mælieininga niður í smærri, dreifa tiltekt á meðal vöruhúsaatvinnumenn með tiltektarvinnublaði með  [walkof af inn-og útbrennslu í ítarlegri samskipan vöruhúss með beinan frágang og tínslu](warehousing/warehouse-directed-flow.md)

Lestu skrefin fyrir hverjar aðstæður í viðkomandi grein.
   
## Sjá einnig .

[Framleiðsla](../production-manage-manufacturing.md)  
[Vöruhúsum](../warehouse-manage-warehouse.md)  

