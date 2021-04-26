---
title: Hvernig skal Vinna með ábyrgðarstöðvar | Microsoft Docs
description: Ábyrgðarstöðvar bjóða upp á umsjón með stjórnunarmiðstöðvum. Ábyrgðamiðstöð getur verið kostnaðarmiðstöð, hagnaðarmiðstöð, fjárfestingamiðstöð eða önnur fyrirtækisskilgreind stjórnunarmiðstöð.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e552378625325710b50989c513d303acd9c480af
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5774790"
---
# <a name="work-with-responsibility-centers"></a>Vinna með ábyrgðarstöðvar

Ábyrgðarstöðvar bjóða upp á eiginleika sem felst í umsjón með stjórnunarmiðstöðvum. Ábyrgðarstöð getur verið kostnaðarstöð, framlegðarstöð, fjárfestingarstöð eða önnur stöð skilgreind út frá stjórnsýslu fyrirtækisins. Dæmi um ábyrgðarmiðstöðvar eru söluskrifstofur, innkaupadeild fyrir nokkrar birgðageymslur og verksmiðjuskipulagsdeild. Með því að nota þessa aðgerð, geta fyrirtæki t.d. sett upp notendasértæk birtingaform sölu- og innkaupaskjala sem varða eingöngu tiltekinnar ábyrgðastöðvar.  

Notkun margra birgðageymslur og ábyrgðarstöðvar býður upp á eiginleikann að stjórna viðskiptaaðgerðum sínum á eins sveigjanlegan og hagstæðan máta og kostur er.

Margar birgðageymslur gera fyrirtækjum kleift að stjórna birgðum sínum á mörgum stöðum í einum gagnagrunni. Tvö hugtök – birgðageymslur og birgðahaldseiningar – eru hornsteinar þessarar eindar. Birgðageymsla er skilgreind sem staður sem sér um raunstaðsetningu og magn vöru. Hugtakið er nægilega vítt til að taka til staðsetninga eins og verksmiðja eða framleiðslustaða sem og dreifingastöðva, vöruhúsa, sýningasala og þjónustubifreiða. Birgðahaldseining er skilgreind sem vara á tilteknum stað og/eða sem afbrigði. Með því að nota birgðahaldseiningar geta fyrirtæki með margar birgðageymslur bætt inn áfyllingarupplýsingar, aðsetur og upplýsingar um fjármálalegar bókanir á birgðageymslustiginu. Þar af leiðandi geta þau fyllt á afbrigði af sömu vöru í hverri birgðageymslu sem og pantað vörur fyrir hverja birgðageymslu á grundvelli staðbundinna birgðageymsluupplýsinga.  

## <a name="to-set-up-a-responsibility-center"></a>Uppsetning ábyrgðarstöðva

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Ábyrgðarstöðvar** og veldu síðan tengda tengilinn.  
2. Valið er **Nýtt** aðgerð.  
3. Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Ef ábyrgðarstöðvar eru notaðar til að sjá um fyrirtækið getur verið gott að hafa sjálfgefna ábyrgðarstöð fyrir fyrirtækið.
4. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Stofngögn** og veldu síðan tengda tengilinn.
5. Í **Ábyrgðastöð** reitnum er kóði ábyrgðarstöðvar færður inn.

Kóðinn verður notuð í öllum innkaupa- sölu- og þjónustuskjölum ef notanda, viðskiptamanni eða lánardrottni hefur ekki sjálfgefna ábyrgðarstöð. Í öllum innkaupa- sölu- og þjónustuskjölum getur fært inn aðra ábyrgðastöð en þá sem er sjálfgefin.

> [!NOTE]  
> Þegar ábyrgðarstöðvarkóti er settur á fylgiskjal hefur það áhrif á aðsetur, víddir og verð á fylgiskjalinu.  

## <a name="to-assign-responsibility-centers-to-users"></a>Að úthluta ábyrgðarstöðvum til notenda:

Hægt er að setja upp notendur þannig að í daglegri keyrslu sæki forritið aðeins þau skjöl sem eiga við verksvið þeirra. Notendur eru venjulega tengdir einni ábyrgðarstöð og vinna aðeins með skjöl sem tengjast sértækum kerfishlutum í þeirri tilteknu ábyrgðarstöð.  

Til að setja þetta upp þarf að úthluta notendum ábyrgðarstöðvum á þremur grunnsvæðum: Innkaup, sala og þjónustustjórnun.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Notandauppsetning** og veldu síðan tengda tengilinn.  
2. Á síðunni **Uppsetning notanda** velur þú notandann sem á að úthluta ábyrgðarstöð til. Ef notandinn er ekki á listanum verður að slá inn notandakenni í reitnum **Notandakenni** .  
3. Í reitinn **Söluafmörkun ábyrgðarstöðvar** skal færa inn ábyrgðarstöðina þar sem notandi vinnur að sölumálum.  
4. Í reitinn **Innkaupaafmörkun ábyrgðarstöðvar** skal færa inn ábyrgðarstöðina þar sem notandi vinnur að innkaupamálum.  
5. Í reitinn **Þjónustuafmörkun ábyrgðarstöðvar** skal færa inn ábyrgðarstöðina þar sem notandi vinnur að þjónustustjórnun.  

> [!NOTE]  
> Notendur geta aðeins skoðað þessi bókuðu skjöl sem tengjast ábyrgðarstöð þeirra. Hins vegar er hægt að skoða allar fjárhagsfærslur og fletta að öðrum bókuðum skjölum úr fjárhagsfærslunum.

## <a name="see-also"></a>Sjá einnig

[Uppsetning birgða](inventory-setup-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)
[Birgðir](inventory-manage-inventory.md)[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]