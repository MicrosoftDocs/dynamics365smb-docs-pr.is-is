---
title: Hvernig á að Vinna með ábyrgðarstöðvar
description: Ábyrgðarmiðstöð sem stjórnstöð hjálpar fyrirtækjum að setja upp notendamiðuð yfirlit yfir sölu- og innkaupaskjöl sem tengjast eingöngu hverri stöð.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.forms: 5714, 5715
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: e966e5050cf16ce60e07983f129be318706fbbf3
ms.sourcegitcommit: 189bf08d7ddf6c8b7ef2c09058c6847aa6e590d3
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/31/2022
ms.locfileid: "8059335"
---
# <a name="work-with-responsibility-centers"></a>Vinna með ábyrgðarstöðvar

Ábyrgðarstöðvar bjóða upp á eiginleika sem felst í umsjón með stjórnunarmiðstöðvum. Ábyrgðarstöð getur verið kostnaðarstöð, framlegðarstöð, fjárfestingarstöð eða önnur stöð skilgreind út frá stjórnsýslu fyrirtækisins. Dæmi um ábyrgðarmiðstöðvar eru söluskrifstofur, innkaupadeild fyrir nokkrar birgðageymslur og verksmiðjuskipulagsdeild. Með því að nota þessa aðgerð, geta fyrirtæki t.d. sett upp notendasértæk birtingaform sölu- og innkaupaskjala sem varða eingöngu tiltekinnar ábyrgðastöðvar.  

Notkun margra birgðageymslur og ábyrgðarstöðvar býður upp á eiginleikann að stjórna viðskiptaaðgerðum sínum á eins sveigjanlegan og hagstæðan máta og kostur er.

Margar birgðageymslur gera fyrirtækjum kleift að stjórna birgðum sínum á mörgum stöðum í einum gagnagrunni. Tvö hugtök – birgðageymslur og birgðahaldseiningar – eru hornsteinar þessarar eindar. Birgðageymsla er skilgreind sem staður sem sér um raunstaðsetningu og magn vöru. Hugtakið er nægilega vítt til að taka til staðsetninga eins og verksmiðja eða framleiðslustaða sem og dreifingastöðva, vöruhúsa, sýningasala og þjónustubifreiða. Birgðahaldseining er skilgreind sem vara á tilteknum stað og/eða sem afbrigði. Með því að nota birgðahaldseiningar geta fyrirtæki með margar birgðageymslur bætt inn áfyllingarupplýsingar, aðsetur og upplýsingar um fjármálalegar bókanir á birgðageymslustiginu. Þar af leiðandi geta þau fyllt á afbrigði af sömu vöru í hverri birgðageymslu sem og pantað vörur fyrir hverja birgðageymslu á grundvelli staðbundinna birgðageymsluupplýsinga.  

## <a name="to-set-up-a-responsibility-center"></a>Uppsetning ábyrgðarstöðva

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Ábyrgðarstöðvar** og velja síðan viðkomandi tengil.  
2. Valið er **Nýtt** aðgerð.  
3. Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Ef ábyrgðarstöðvar eru notaðar til að sjá um fyrirtækið getur verið gott að hafa sjálfgefna ábyrgðarstöð fyrir fyrirtækið.
4. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Upplýsingar um fyrirtæki** og velja síðan viðkomandi tengil.
5. Í **Ábyrgðastöð** reitnum er kóði ábyrgðarstöðvar færður inn.

Kóðinn verður notuð í öllum innkaupa- sölu- og þjónustuskjölum ef notanda, viðskiptamanni eða lánardrottni hefur ekki sjálfgefna ábyrgðarstöð. Í öllum innkaupa- sölu- og þjónustuskjölum getur fært inn aðra ábyrgðastöð en þá sem er sjálfgefin.

> [!NOTE]  
> Þegar ábyrgðarstöðvarkóti er settur á fylgiskjal hefur það áhrif á aðsetur, víddir og verð á fylgiskjalinu.  

## <a name="to-assign-responsibility-centers-to-users"></a>Að úthluta ábyrgðarstöðvum til notenda:

Hægt er að setja upp notendur þannig að í daglegri keyrslu sæki forritið aðeins þau skjöl sem eiga við verksvið þeirra. Notendur eru venjulega tengdir einni ábyrgðarstöð og vinna aðeins með skjöl sem tengjast sértækum kerfishlutum í þeirri tilteknu ábyrgðarstöð.  

Til að setja þetta upp þarf að úthluta notendum ábyrgðarstöðvum á þremur grunnsvæðum: Innkaup, sala og þjónustustjórnun.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning notanda** og velja síðan viðkomandi tengil.  
2. Á síðunni **Uppsetning notanda** velur þú notandann sem á að úthluta ábyrgðarstöð til. Ef notandinn er ekki á listanum verður að slá inn notandakenni í reitnum **Notandakenni** .  
3. Í reitinn **Söluafmörkun ábyrgðarstöðvar** skal færa inn ábyrgðarstöðina þar sem notandi vinnur að sölumálum.  
4. Í reitinn **Innkaupaafmörkun ábyrgðarstöðvar** skal færa inn ábyrgðarstöðina þar sem notandi vinnur að innkaupamálum.  
5. Í reitinn **Þjónustuafmörkun ábyrgðarstöðvar** skal færa inn ábyrgðarstöðina þar sem notandi vinnur að þjónustustjórnun.  

> [!NOTE]  
> Notendur geta aðeins skoðað þessi bókuðu skjöl sem tengjast ábyrgðarstöð þeirra. Hins vegar er hægt að skoða allar fjárhagsfærslur og fletta að öðrum bókuðum skjölum úr fjárhagsfærslunum.

## <a name="see-also"></a>Sjá einnig

[Uppsetning birgða](inventory-setup-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]