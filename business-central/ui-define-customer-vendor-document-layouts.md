---
title: Úthluta útliti skjala á viðskiptamenn eða lánardrottna
description: Notaðu skjalaútlit til að stjórna framsetningu og sniði skjala á borð við reikninga og pantana sem þú sendir á viðskiptamenn og lánardrottna.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '21, 9650'
ms.date: 07/05/2024
ms.service: dynamics-365-business-central
---
# <a name="define-document-layouts-for-customers-and-vendors"></a>Skilgreina útlit skjala fyrir viðskiptamenn og lánardrottna

Skjalaútlit notar skýrsluútlit til að skilgreina útlit og yfirbragð skjala sem þú sendir á viðskiptamenn og lánardrottna. Business Central býður upp á staðlað útlit, en þú getur aðlagað sérsniðið útlit fyrir hvern viðskiptafélaga fyrir sig. Nánari upplýsingar er að finna í [Búa til og breyta sérsniðnum skýrsluútlitum](ui-how-create-custom-report-layout.md). Þú getur valið staðlað og sérsniðið skjalaútlit fyrir viðskiptamanna- og lánardrottnaspjald með því að velja aðgerðina **Skjalaútlit**. Gildið í reitnum **Notkun** skilgreinir ferlið þar sem skjalaútlitið er notað. Fyrir viðskiptamenn sem dæmi gætirðu notað gerðirnar **Áminning**, **Sending** og **Staðfesting** fyrir skjalaútlit.

Skjalaútlit getur líka sparað þér tíma þegar þú sendir skjöl á tengilið viðskiptamanns eða lánardrottins með tölvupósti. Fyrir hvert útlit sem þú úthlutar á viðskiptamann eða tengilið geturðu tilgreint eitt eða fleiri netföng tengiliða. Til dæmis er hægt að senda reikning til tengiliða innkaupa- og vöruhúss viðskiptamanns. Það er auðvelt að bæta við netföngum. Á síðunni **Útlit skjala** er aðgerðin **Velja tölvupóst úr tengiliðum** valin úr lista yfir netföng tengiliða sem þú skráðir fyrir viðskiptamanni eða lánardrottni. Einnig er hægt að bæta við netföngum handvirkt. Ef þú slærð inn mörg netföng skaltu aðskilja þau með semíkommu og ekki bæta við bilum á milli netfanga.

Áður en hægt er að skilgreina hvaða skjalaútlit á að nota fyrir hvaða ferli, og til hvaða tengiliðar á að senda skjalið, verður að hlaða öllum tiltækum skýrslum (skjölum) af síðunni **Skýrsluval** . Hægt er að hlaða skjölunum inn á fljótlegan hátt með því að nota aðgerðina **Afrita úr skýrsluvali** á síðunni **Skjalaútlit**.

Skrefin í næstu hlutum lýsa því hvernig á að skilgreina útlit söluskjala á síðunni **Viðskiptamannaspjald**. Fyrir lánardrottna eru skrefin þau sömu á síðunni **Lánardrottnaspjald**.

## <a name="to-load-the-standard-document-layouts-for-sales-documents-for-a-customer"></a>Að hlaða stöðluðu skjalaútliti fyrir söluskjöl fyrir viðskiptamann

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptavinir** og velja síðan viðkomandi tengil.
2. Opnaðu síðuna **Viðskiptamannaspjald** fyrir viðskiptamanninn og veldu síðan aðgerðina **Skjalaútlit**.
3. Á síðunni **Útlit fylgiskjals** skal velja aðgerðina **Afrita úr skýrsluvali**.

Síðan **Skjalaútlit** sýnir öll útlit sem eru í boði fyrir söluskjöl. 

## <a name="to-select-a-custom-report-layout-to-use-for-the-sales-document-layout"></a>Til að velja sérsniðið skýrsluútlit sem á að nota fyrir útlit söluskjals

Eftirfarandi skref gera ráð fyrir því að sérsniðin skýrsluútlit sé fyrir tegund fylgiskjalsins. Ef sérsniðin skýrsluútlit er ekki þegar til þarf að búa til það fyrst. Nánari upplýsingar er að finna í [Búa til og breyta sérsniðnum skýrsluútlitum](ui-how-create-custom-report-layout.md).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptavinir** og velja síðan viðkomandi tengil.
2. Opnaðu síðuna **Viðskiptamannaspjald** fyrir viðskiptamanninn og veldu síðan aðgerðina **Skjalaútlit**.
3. Á síðunni **Útlit fylgiskjals**, á línunni fyrir skýrsluútlit sem á að nota skal nota sérsniðið útlit fyrir skal velja reitinn **Lýsing á sérstilltu útliti**.

   > [!TIP]
   > Sjálfgefið er að reiturinn Lýsing sérsniðins uppsetningar sé falinn. Ef reiturinn er ekki tiltækur er hægt að sérsníða síðuna til að bæta honum við. Til að sérsníða síðuna skal velja táknið :::image type="content" source="media/ui-experience/settings_icon_small.png" alt-text="Stillingar."::: Táknmynd og velja **svo Sérstilla**. Nánari upplýsingar um sérstillingu síðna fást með því að [fara í Sérstilla vinnusvæðið](ui-personalization-user.md).

1. Á síðunni **Sérsniðið skýrsluútlit** skal velja skjalaútlitið sem á að nota fyrir gerð söluskjalsins. Nánari upplýsingar er að finna í [Búa til og breyta sérsniðnum skýrsluútlitum](ui-how-create-custom-report-layout.md).

## <a name="to-specify-which-contact-receives-which-document-layout-for-a-customer"></a>Til að tilgreina hvaða tengiliður fær hvaða fylgiskjalauppsetning viðskiptamanns

Til að spara tíma þegar þú sendir skjöl til tengiliða viðskiptamanns og lánardrottins með tölvupósti skaltu tilgreina netföng þeirra í skjalaútliti. Til dæmis geturðu alltaf sent yfirlit viðskiptamanns á tengiliði endurskoðanda eða sölupantanir á innkaupaaðila eða innkaupapantanir á sölufólk lánardrottins.

1. Á síðunni **Útlit fylgiskjals**, á línunni fyrir skýrsluútlit sem á að senda á tiltekinn tengilið fyrir viðskiptamanninn skal velja aðgerðina **Velja netfang úr tengiliðum**.
2. Á síðunni **Tengiliðir** skaltu velja einn eða fleiri tengiliði og velja síðan **Í lagi**.

## <a name="see-also"></a>Sjá einnig

[Uppfæra sérsniðið skýrsluútlit](ui-update-report-layouts.md)  
[Búa til og breyta sérsniðnum skýrsluútlitum](ui-how-create-custom-report-layout.md)  
[Flytja inn og út sérsniðið skýrsluútlit eða skjalaútlit](ui-how-import-and-export-report-layout.md)  
[Senda skjöl í tölvupósti](ui-how-send-documents-email.md)  
[Stjórnun skýrsluútlita](ui-manage-report-layouts.md)  
[Vinna með skýrslur, runuvinnslur og XMLports](ui-work-report.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
