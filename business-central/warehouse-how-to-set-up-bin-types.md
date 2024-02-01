---
title: Setja upp hólfategundir
description: Úthlutaðu gerðum og einföldum flæðisaðgerðum á hólf og skilgreindu hvernig hólf eru notuð fyrir ákveðnar vöruhúsaaðgerðir.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: 7367
ms.date: 06/25/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="set-up-bin-types"></a>Setja upp hólfategundir

Hægt er að beina vöruflæðinu gegnum hólf sem skilgreind hafa verið fyrir tilteknar vöruhúsaaðgerðir. Notandinn úthlutar hverju hólfi grunnflæðisaðgerðir, og skilgreinir þannig hvernig hólfið verður notað í kerfinu, með því að úthluta því hólfategund.  

Til eru sex tegundir. Hægt er að reka vöruhúsið með öllum sex hólfategundunum sem mögulegar eru, eða nota aðeins hólfategundirnar RECEIVE, PUTPICK, SHIP og QC. Þessar fjórar hólfategundir gera kleift að gera tillögur um vöruflæði og gera notandanum kleift að skrá misræmi í birgðum.  

## <a name="to-set-up-the-bin-types-you-want-to-use"></a>Hólfategundir sem á að nota settar upp

1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Hólfategundir** og velja síðan viðkomandi tengil.  
2.  Á síðunni **Hólfategundir** er 10 stafa kóði fyrir hólfategund stofnaður.  
3.  Veljið aðgerðir sem hægt er að framkvæma með hverri tegund hólfa.  

> [!NOTE]  
>  Hólfategundir eiga einungis við ef notaður er beinn frágangur og tínsla fyrir birgðageymsluna.  

Tegund hólfsins ákvarðar aðeins hvernig ákveðið hólf er notað í úrvinnslu vöruflæðis um vöruhúsið. Alltaf er hægt að hnekkja tillögum úr kerfinu fyrir hvaða vöruhúsaskjal sem er og hægt er að færa vörur milli hvaða hólfs sem er sem er með vöruhúsahreyfingu.  

Hólfategundirnar sem hægt er að stofna eru taldar upp hér á eftir.  

|Tegund hólfs|Description|  
|------------------|---------------------------------------|  
|MÓTTAKA|Vörur sem skráðar eru sem bókaðar móttökur en sem ekki hefur verið gengið frá.|  
|SHIP|Vörur sem tíndar hafa verið fyrir vöruhúsaafhendingarlínur en ekki verið bókaðar sem afhendar.|  
|PUT AWAY|Yfirleitt vörur sem geyma á í stórum einingum en sem kerfið á ekki að hafa aðgang að vegna tínslu. Þar sem hólfin eru ekki notuð til tínslu, hvort sem um er að ræða framleiðslupantanir eða afhendingar, getur notkun frágangshólfa verið takmörkuð en þau geta komið sér vel ef keypt hefur verið inn mikið af vörum. Hólf af þessari tegund ætti alltaf að flokka lágt þannig að þegar gengið er frá mótteknum vörum sé fyrst gengið frá öðrum hærra flokkuðum PUTPICK-hólfum sem fest eru við vöruna. Ef þessi tegund hólfs er notuð þarf að enduráfylla hólf reglulega svo að vörur sem þar eru geymdar séu einnig tiltækar í PUTPICK- og PICK-hólfum.|  
|PICK|Vörur sem aðeins á að nota við tínslu, til dæmis vörur sem eru farnar að nálgast síðasta söludag og fluttar hafa verið í hólf af þessari tegund. Há hólfaflokkun ætti að vera sett á þessi hólf til að stungið sé upp á að þau séu tínd fyrst.|  
|PUTPICK|Vörur í hólfum sem eru lagðar til fyrir bæði frágang og tínsluaðgerðir. Hólf af þessari tegund eru líklega með mismunandi hólfaflokkun. Hægt er að setja upp magngeymsluhólf með þessa hólfategund með lága hólfaflokkun samanborið við venjuleg tínsluhólf eða framtíðartínslusvæðishólf.|  
|QC|Þetta hólf er notað fyrir birgðaleiðréttingar ef þetta hólf er tilgreind á birgðageymsluspjaldinu í reitnum **Leiðréttingahólfskóði**. Einnig er hægt að setja upp hólf af þessari tegund fyrir gallaðar vörur og vörur sem teknar eru til skoðunar. Hægt er að flytja vörur í hólf af þessari tegund ef þær eiga ekki að vera tiltækar í venjulegu vöruflæði.<br /><br /> **Athugið:** Ólíkt öllum öðrum gerðum hólfa hefur hólfategundin **GE** enga vörumeðhöndlunargátreiti valda að sjálfgefnu. Þetta tilgreinir að allt innihald sem sett er í QC-hólf er ekki haft með í vöruflæði.|  

## <a name="see-also"></a>Sjá einnig .

[Warehouse Management Overview](design-details-warehouse-management.md)
[Inventory](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Samsetningardeild](assembly-assemble-items.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
