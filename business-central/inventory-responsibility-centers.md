---
title: Hvernig á að vinna með ábyrgðarstöðvar
description: Ábyrgðarmiðstöð sem stjórnstöð hjálpar fyrirtækjum að setja upp notendamiðuð yfirlit yfir sölu- og innkaupaskjöl sem tengjast eingöngu hverri stöð.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.forms: '5714, 5715'
ms.date: 05/16/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Vinna við ábyrgðarstöðvar

Ábyrgðarstöðvar bjóða upp á eiginleika sem felst í umsjón með stjórnunarmiðstöðvum. Ábyrgðarstöð getur verið kostnaðarstöð, framlegðarstöð, fjárfestingarstöð eða önnur stöð skilgreind út frá stjórnsýslu fyrirtækisins. Dæmi um ábyrgðarmiðstöðvar eru söluskrifstofur, innkaupadeild fyrir nokkrar birgðageymslur og verksmiðjuskipulagsdeild. Til dæmis geta fyrirtæki sett upp notendasértæk yfirlit yfir sölu- og innkaupaskjöl sem tengjast tiltekinni ábyrgðarstöð.  

Með því að nota margar birgðageymslur ásamt ábyrgðarstöðvum er hægt að stjórna viðskiptaaðgerðum á sveigjanlegan og bestan hátt.

Margar birgðageymslur gera fyrirtækjum kleift að stýra birgðum sínum í mörgum birgðageymslum með einum gagnagrunni. Tvö hugtök – birgðageymslur og birgðahaldseiningar – eru hornsteinar þessarar eindar. Birgðageymsla er skilgreind sem staður sem sér um raunstaðsetningu og magn vöru. Hugtakið er nógu breiðt til að taka með staðsetningar eins og verksmiðjur eða framleiðsluaðstöðu og dreifingarmiðstöðvar, vöruhús, sýningarsali og þjónustubifreiðar. Birgðahaldseining er skilgreind sem vara á tilteknum stað og/eða sem afbrigði. Með því að nota birgðahaldseiningar geta fyrirtæki með margar birgðageymslur bætt við áfyllingarupplýsingum, aðsetrum og upplýsingum um fjárhagslegar bókanir á birgðageymslustiginu. Þar af leiðandi geta þau útfyllt afbrigði af sömu vöru fyrir hverja birgðageymslu og pantað vörur samkvæmt upplýsingum um birgðageymslutengdar áfyllingar.  

## Uppsetning ábyrgðarstöðva

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Ábyrgðarstöðvar** og velja síðan viðkomandi tengil.  
2. Valið er aðgerðin **Nýtt**.  
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Ef ábyrgðarstöðvar eru notaðar til að sjá um fyrirtækið getur verið gagnlegt að hafa sjálfgefna ábyrgðarstöð.
4. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Upplýsingar um fyrirtæki** og velja síðan viðkomandi tengil.
5. Á flýtiflipanum **Afhending** í reitnum **Ábyrgðarstöð** er færður inn kóti ábyrgðarstöðvar.

Þessi kóti er notaður fyrir öll innkaupa-, sölu- eða þjónustuskjöl ef notandi, viðskiptamaður eða lánardrottinn hefur enga sjálfgefna ábyrgðarstöð. Á sölu-, innkaupa- eða þjónustuskjölum er hægt að færa inn aðra ábyrgðarstöð en sjálfgildið.

> [!NOTE]  
> Þegar ábyrgðarstöðvarkóti er settur á fylgiskjal hefur það áhrif á aðsetur, víddir og verð á fylgiskjalinu.  

## Að úthluta ábyrgðarstöðvum til notenda:

Hægt er að setja upp notendur þannig að [!INCLUDE [prod_short](includes/prod_short.md)] þeir sæki aðeins skjöl sem eiga við tiltekin vinnusvæði þeirra. Notendur eru tengdir einni ábyrgðarstöð og vinna aðeins með skjöl sem tengjast tilteknum kerfishlutum í þeirri tilteknu stöð.  

Til að setja þetta upp þarf að úthluta notendum ábyrgðarstöðvum á þremur grunnsvæðum: Innkaup, sala og þjónustustjórnun.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning notanda** og velja síðan viðkomandi tengil.  
2. Á síðunni **Uppsetning notanda** velur þú notandann sem á að úthluta ábyrgðarstöð til. Ef notandinn er ekki á listanum verður að slá inn notandakenni í reitnum **Notandakenni** .  
3. Í reitinn **Söluafmörkun ábyrgðarstöðvar** skal færa inn ábyrgðarstöðina þar sem notandi vinnur að sölumálum.  
4. Í reitinn **Innkaupaafmörkun ábyrgðarstöðvar** skal færa inn ábyrgðarstöðina þar sem notandi vinnur að innkaupamálum.  
5. Í reitinn **Þjónustuafmörkun ábyrgðarstöðvar** skal færa inn ábyrgðarstöðina þar sem notandi vinnur að þjónustustjórnun.  

> [!NOTE]  
> Notendur geta aðeins skoðað þessi bókuðu skjöl sem tengjast ábyrgðarstöð þeirra. Hins vegar er hægt að skoða allar fjárhagsfærslur og fletta að öðrum bókuðum skjölum úr fjárhagsfærslunum.

## Sjá einnig .

[Uppsetning birgða](inventory-setup-inventory.md)    
[Vöruhúsakerfi sett upp](warehouse-setup-warehouse.md)    
[Birgðir](inventory-manage-inventory.md)    
[Yfirlit yfir vöruhúsakerfi](design-details-warehouse-management.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    
[Skilgreina bókunarreglu reiknings fyrir notendur](admin-setup-invoice-posting-policy.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
