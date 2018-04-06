---
title: "Hvernig skal Vinna með ábyrgðarstöðvar | Microsoft Docs"
description: "Ábyrgðarstöðvar bjóða upp á umsjón með stjórnunarmiðstöðvum. Ábyrgðamiðstöð getur verið kostnaðarmiðstöð, hagnaðarmiðstöð, fjárfestingamiðstöð eða önnur fyrirtækisskilgreind stjórnunarmiðstöð."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b1a8eb26783b7e93e9afe04b13298972af83175d
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-responsibility-centers"></a>Vinna með ábyrgðarstöðvar
Ábyrgðarstöðvar bjóða upp á eiginleika sem felst í umsjón með stjórnunarmiðstöðvum. Ábyrgðarstöð getur verið kostnaðarstöð, framlegðarstöð, fjárfestingarstöð eða önnur stöð skilgreind út frá stjórnsýslu fyrirtækisins. Dæmi um ábyrgðarmiðstöðvar eru söluskrifstofur, innkaupadeild fyrir nokkrar birgðageymslur og verksmiðjuskipulagsdeild. Með því að nota þessa aðgerð, geta fyrirtæki t.d. sett upp notendasértæk birtingaform sölu- og innkaupaskjala sem varða eingöngu tiltekinnar ábyrgðastöðvar.  

Notkun margra birgðageymslur og ábyrgðarstöðvar býður upp á eiginleikann að stjórna viðskiptaaðgerðum sínum á eins sveigjanlegan og hagstæðan máta og kostur er.

Margar birgðageymslur gera fyrirtækjum kleift að stjórna birgðum sínum á mörgum stöðum í einum gagnagrunni. Tvö hugtök – birgðageymslur og birgðahaldseiningar – eru hornsteinar þessarar eindar. Birgðageymsla er skilgreind sem staður sem sér um raunstaðsetningu og magn vöru. Hugtakið er nægilega vítt til að taka til staðsetninga eins og verksmiðja eða framleiðslustaða sem og dreifingastöðva, vöruhúsa, sýningasala og þjónustubifreiða. Birgðahaldseining er skilgreind sem vara á tilteknum stað og/eða sem afbrigði. Með því að nota birgðahaldseiningar geta fyrirtæki með margar birgðageymslur bætt inn áfyllingarupplýsingar, aðsetur og upplýsingar um fjármálalegar bókanir á birgðageymslustiginu. Þar af leiðandi geta þau fyllt á afbrigði af sömu vöru í hverri birgðageymslu sem og pantað vörur fyrir hverja birgðageymslu á grundvelli staðbundinna birgðageymsluupplýsinga.  

Ábyrgðastöðvar útvíkka margar birgðageymslur með því að gera notendum kleift að stjórna stjórnunarmiðstöðvum. Ábyrgðamiðstöð getur verið kostnaðarmiðstöð, hagnaðarmiðstöð, fjárfestingamiðstöð eða önnur fyrirtækisskilgreind stjórnunarmiðstöð. Dæmi um ábyrgðarmiðstöðvar eru söluskrifstofur, innkaupadeild fyrir nokkrar birgðageymslur og verksmiðjuskipulagsdeild. Með þessari virkni, geta fyrirtæki til dæmis sett upp fyrir notendur sértæk yfirlit yfir sölu- og innkaupaskjöl sem tengjast vissum ábyrgðarstöðvum.

## <a name="to-set-up-a-responsibility-center"></a>Uppsetning ábyrgðarstöðva  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Ábyrgðastöðvar** og velja svo viðeigandi tengil.  
2.  Valið er **Nýtt** aðgerð.  
3.  Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Ef ábyrgðarstöðvar eru notaðar til að sjá um fyrirtækið getur verið gott að hafa sjálfgefna ábyrgðarstöð fyrir fyrirtækið.
4. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Fyrirtækjaupplýsingar** og velja svo viðeigandi tengil.
5. Í **Ábyrgðastöð** reitnum er kóði ábyrgðarstöðvar færður inn.

Kóðinn verður notuð í öllum innkaupa- sölu- og þjónustuskjölum ef notanda, viðskiptamanni eða lánardrottni hefur ekki sjálfgefna ábyrgðarstöð. Í öllum innkaupa- sölu- og þjónustuskjölum getur fært inn aðra ábyrgðastöð en þá sem er sjálfgefin.

> [!NOTE]  
>  Þegar ábyrgðarstöðvarkóti er settur á fylgiskjal hefur það áhrif á aðsetur, víddir og verð á fylgiskjalinu.  

## <a name="to-assign-responsibility-centers-to-users"></a>Að úthluta ábyrgðarstöðvum til notenda:  
Hægt er að setja upp notendur þannig að í daglegri keyrslu sæki forritið aðeins þau skjöl sem eiga við verksvið þeirra. Notendur eru venjulega tengdir einni ábyrgðarstöð og vinna aðeins með skjöl sem tengjast sértækum kerfishlutum í þeirri tilteknu ábyrgðarstöð.  

Til að setja þetta upp þarf að úthluta notendum ábyrgðarstöðvum á þremur grunnsvæðum: Innkaup, sala og þjónustustjórnun.  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Notandauppsetning** og velja svo viðeigandi tengil.  
2.  Í glugganum **Uppsetning notanda** velur þú notandann sem á að úthluta ábyrgðarstöð til. Ef notandinn er ekki á listanum verður að slá inn notandakenni í reitnum **Notandakenni** .  
3.  Í reitinn **Söluafmörkun ábyrgðarstöðvar** skal færa inn ábyrgðarstöðina þar sem notandi vinnur að sölumálum.  
4.  Í reitinn **Innkaupaafmörkun ábyrgðarstöðvar** skal færa inn ábyrgðarstöðina þar sem notandi vinnur að innkaupamálum.  
5.  Í reitinn **Þjónustuafmörkun ábyrgðarstöðvar** skal færa inn ábyrgðarstöðina þar sem notandi vinnur að þjónustustjórnun.  

> [!NOTE]  
>  Notendur geta enn skoðað öll bókuð skjöl og bókfærslur, ekki aðeins þau sem tengjast ábyrgðarstöð þeirra.

## <a name="see-also"></a>Sjá einnig  
[Uppsetning birgða](inventory-setup-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)
[Birgðir](inventory-manage-inventory.md)[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Vöruhúsastjórnun](warehouse-manage-warehouse.md)    
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

