---
title: Hvernig á að bóka mörg skjöl á sama tíma | Microsoft Docs
description: Í stað þess að bóka eitt skjal í einu er hægt að velja mörg óbókuð skjöl í lista fyrir fjöldabókun, annaðhvort fyrir bókun án tafar eða sem til að mynda er áætluð við lok dags.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e493aa1a965d4d3cb5a546e8671915ed19fce918
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5387075"
---
# <a name="post-multiple-documents-at-the-same-time"></a>Bóka mörg skjöl á sama tíma

Í stað þess að bóka eitt skjal í einu er hægt að velja mörg óbókuð skjöl í lista fyrir bókun án tafar eða fyrir fjöldabókun samkvæmt áætlun, svo sem við lok dags. Þetta getur komið sér vel ef aðeins yfirmaður getur bókað skjöl sem aðrir notendur hafa búið til eða til að koma í veg fyrir vandamál tengd afköstum þegar bókun er gerð á vinnutíma.

## <a name="to-post-multiple-purchase-orders-immediately"></a>Til að bóka margar innkaupapantanir strax

Eftirfarandi ferli útskýrir hvernig á að bóka margar innkaupapantanir strax. Skrefin eru svipuð fyrir öll innkaupa- og söluskjöl.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innkaupapantanir** og veldu síðan tengda tengilinn.
2. Á síðunni **Innkaupapantanir** skal velja allar pantanir sem á að bóka:
3. Í reitnum **númer** skal velja þrjá lóðrétta punkta til að opna efnisvalmynd og síðan velja aðgerðina **Velja fleira**.
4. Veldu gátreitinn fyrir allar línurnar sem tákna pantanir sem á að bóka á sama tíma.
5. Veldu **Bókun** aðgerðina og svo aðgerðina **Bóka**.
6. Velja hnappinn **Já** á staðfestingarskilaboðunum.

## <a name="to-batch-post-multiple-purchase-orders"></a>Til að runubóka marga innkaupapantanir

Eftirfarandi ferli útskýrir hvernig á að fjöldabóka innkaupapantanir. Skrefin eru svipuð fyrir öll innkaupa- og söluskjöl þar sem aðgerðin **Fjöldabóka** er í boði.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innkaupapantanir** og veldu síðan tengda tengilinn.  
2. Á síðunni **Innkaupapantanir** skal velja allar pantanir sem á að bóka:
3. Í reitnum **númer** skal velja þrjá lóðrétta punkta til að opna efnisvalmynd og síðan velja aðgerðina **Velja fleira**.
4. Veldu gátreitinn fyrir allar línurnar sem tákna pantanir sem á að bóka á sama tíma.
5. Veldu **Bókun** aðgerðina og svo aðgerðina **Fjöldabóka**.
6. Á síðunni **Innkaupapöntun fjöldabókunar** þarf að fylla reitina út eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Velja hnappinn **Í lagi**.
8. Til að skoða möguleg vandamál sem komu upp við fjöldabókun á skjölum skal opna síðuna **Skráning villuboða**.

> [!NOTE]
> Bókun margra fylgiskjala gæti tekið nokkurn tíma og lokað á aðra notendur. Íhugaðu að virkja bakgrunnsbókun. Frekari upplýsingar, sjá [Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md).

## <a name="to-set-up-background-posting-with-job-queues"></a>Að setja upp bókun í bakgrunni með verkraðir
Verkraðir eru áhrifaríkt verkfæri til að raða keyrslu viðskiptaferla í bakgrunni, t.d. þegar margir notendur reyna að bóka sölupantanir, en aðeins er hægt að vinna úr einni pöntun í einu.  

Eftirfarandi ferli lýsir hvernig setja á upp bakgrunnsbókun fyrir sölupantanir. Skrefin eru svipuð fyrir Kaup í innkaup.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölugrunnur** og veldu síðan tengda tengilinn.
2. Á síðunni **Uppsetning sölu og útistandandi** skal velja gátreitinn **Bóka með verkröð**.
3. Veldu **Flokkakóði verkraðar** svæðið tilgreindu síðan **SALESPOST** koðann.

    > [!NOTE]
    > Sum verk breyta sömu gögnum og ekki ætti að keyra þau samtímis þar sem það getur valdið árekstrum. Til dæmis munu bakgrunnsvinnslur fyrir söluskjöl reyna að breyta sömu gögnum á sama tíma. Verkraðarflokkar koma í veg fyrir að þessar gerðir árekstrar með því að tryggja að þegar ein vinnsla er keyrð muni önnur vinnsla sem tilheyrir sömu verkraðarflokki ekki keyra fyrr en henni lýkur. Til dæmis mun vinnsla sem tilheyrir flokki söluverkraðar bíða þar til öll önnur sölutengd verk eru búin. Verkraðarflokkur er tilgreindur á flýtiflipanum **Bókun í bakgrunni** á síðunni **Sölugrunnur**.
    >
    > [!INCLUDE[prod_short](includes/prod_short.md)] bíður upp á verkraðarflokka fyrir sölu, innkaup og bókun í fjárhag. Mælt er með því að eitt þessara, eða eitt þess sem er búið til, sé alltaf tilgreint. Ef bilanir koma upp vegna árekstra skal íhuga að setja upp flokk fyrir allar sölur, innkaup og bakgrunnsbókun í fjárhag.

    Ef þú vilt einnig að söluskjöl verði prentuð þegar þau eru bókuð skal velja gátreitinn **Bóka & Prenta með verkröð** á síðunni **Uppsetning sölu og útistandandi**.  
    Ef valið er **PDF** í reitnum **Skýrslufrálagsgerð** verða bókaðar innkaupapantanir sem heppnuðust tiltækar í hlutanum **Skýrsluinnhólf** í hlutverkamiðstöðinni.

    > [!IMPORTANT]  
    > Ef þú setur upp verk sem mun bóka og prenta skjöl, og prentarinn sýnir svarglugga, svo sem beiðni um auðkennisupplýsingar eða viðvörun um að blek sé að klárast, bókast fylgiskjalið en prentast ekki út. Samsvarandi verkraðarfærsla rennur á endanum út á tíma og reiturinn **Staða** stillist á **Villa**. Ekki er mælt með notkun prentarauppsetningar sem krefst samskipta við svarglugga prentara samhliða bakgrunnsbókunar.

    Næst þegar söluskjöl eru bókuð þarf stofnar [!INCLUDE [prod_short](includes/prod_short.md)] sjálfkrafa verkraðarafærslu fyrir hvert fylgiskjal og keyrir vinnslurnar í bakgrunni, eina í einu.

4. Til að staðfesta að verkröðin vinni eins og búist er við skal bóka sölupöntun. Frekari upplýsingar eru í [Selja vörur](sales-how-sell-products.md).
    Sölupöntun verður nú bætt við valda verkraðarfærslu, sem skilgreinir hvenær skjölin eru bókuð. 

### <a name="to-view-status-from-a-sales-or-purchase-document"></a>Til að skoða stöðu úr sölu- eða innkaupaskjali
Ef verkröðin getur ekki bókað sölupöntunina breytist staðan í **Villa** og er sölupöntuninni þá bætt við lista yfir sölupantanir sem notandinn verður að meðhöndla handvirkt.
1. Úr skjalinu sem þú reyndir að bóka með verkröðinni skal velja bakgrunnsbókun **Staða verkraðar** sem mun innihalda **Villu**.
2. Fara skal yfir villuboðin og leysa vandann.

Þú getur einnig yfirfarið síðuna **Skrárfærslur verkraðar** ef tókst að bóka sölupöntun. Nánari upplýsingar eru í [Til að skoða stöðu eða villur í verkröð](admin-job-queues-schedule-tasks.md#to-view-status-or-errors-in-the-job-queue).

## <a name="to-create-a-job-queue-entry-for-batch-posting-of-sales-orders"></a>Til að stofna færslu verkraðar fyrir bókun runu á sölupöntunum

Einnig er hægt að fresta bókunum þar til það hentar fyrirtækinu. Til dæmis getur það verið gagnlegt í fyrirtæki að keyra tilteknar vinnslur þegar flestum gagnafærslum fyrir daginn er lokið. Þú getur náð þessu fram með því að láta verkröðina keyra mismunandi bókunarskrár í runu, eins og t.d. skrárnar **Bókunarsölupantanir í runu**, **Fjöldabóka sölureikninga**, og Bókunarsölukreditreikningar í runu. [!INCLUDE[prod_short](includes/prod_short.md)] styður bakgrunnsbókun fyrir öll sölu-, innkaupa- og þjónustuskjöl.

Eftirfarandi ferli sýnir hvernig á að setja upp skýrsluna **Fjöldabóka sölupantanir** til að bóka sjálfkrafa sölupantanir kl. 16:00 á virkum dögum.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verkraðarfærslur** og veldu síðan viðeigandi tengil.  
2. Valið er **Nýtt** aðgerð.  
3. Í reitnum **Gerð hlutar sem á að keyra** skal velja **Skýrsla**.  
4. Í reitnum **Kenni hlutar sem á að keyra**, skal velja 296, **Fjöldabóka sölupantanir**.

   Einnig er hægt að nota eftirfarandi skýrslur:
  
   * 900 **Fjölbóka samsetningarpantanir**
   * 497 **Fjöldabóka innkaupareikninga**
   * 496 **Fjöldabóka innkaupapantanir**
   * 498 **Fjöldabóka innk.kreditreikning**
   * 6665 **Fjöldabóka innkaupavöruskilapantanir**
   * 298 **Fjöldabóka sölukreditreikninga**
   * 297 **Fjöldabóka sölureikninga**
   * 296 **Fjöldabóka sölupantanir**
   * 6655 **Fjöldabóka söluvöruskilapantanir**
   * 6005 **Fjöldabóka kreditreikninga þjónustu**
   * 6004 **Fjöldabóka þjónustureikninga**
   * 6001 **Fjöldabóka þjónustupantanir**

5. Veldu gátreitinn **Beiðnisíða skýrslu**.
6. Á beiðnisíðunni **Fjöldabóka sölupantanir** skal skilgreina hvað er innifalið við sjálfvirka bókun á sölupöntunum og síðan velja hnappinn **Í lagi**.

    > [!IMPORTANT]
    > Munið að stilla strangar síur; annars bókar [!INCLUDE [prod_short](includes/prod_short.md)] öll skjöl, jafnvel þau sem ekki eru tilbúin. Íhugið að setja síu á svæðið **Staða** fyrir *Losað*, og síu á **Bókunardagsetning** fyrir gildið *.. í dag*. Nánari upplýsingar er að finna í [Flokkun, leit og síun](ui-enter-criteria-filters.md).
7. Veldu alla gátreitina frá **Keyra á mánudögum** til og með **Keyra á föstudögum**.
8. Í reitinn **Upphafstími** skal slá inn kl. 16:00.
9. Velja aðgerðina **Stilla stöðu á Tilbúin**.

Sölupantanir sem eru innan tilgreindra síu verða nú bókaðar í hverri viku kl. 16:00.


## <a name="see-also"></a>Sjá einnig

[Bókun skjala og færslubóka](ui-post-documents-journals.md)  
[Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md)  
[Breyta bókuðum skjölum](across-edit-posted-document.md)  
[Leiðrétta eða afturkalla ógreidda innkaupareikninga](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Finndu síður og upplýsingar með Viðmótsleit](ui-search.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]