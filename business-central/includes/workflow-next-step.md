---
author: brentholtorf
ms.topic: include
ms.date: 03/27/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

> [!IMPORTANT]
> Þegar tilviki verkflæðisskrefs er breytt breytist svörunin einnig. Stundum vísa svör annarra þegar atburðir vísa til þessara svara sem næsta skref í verkflæðinu. Þegar atburði hefur verið breytt er staðfest að næstu þrep fyrir atburði þess séu rétt.  
>
> Til dæmis **er verkflæðissniðmát** samþykktar lánardrottna aðalatriði þegar **beðið er um samþykki lánardrottins**. Ef tilvikið er með **beiðnina Senda samþykki fyrir færslunni og stofna tilkynningu** þá svar, sem annað en svar vísar til. Ef aðalsamþykkt **lánardrottins er beðið** um það, til dæmis, **færsla lánardrottins breytist**, þá er svarið hreinsað ásamt tilvísununum.
>
> Þá er svörum við samþykktarbeiðninni **úthlutað** og **samþykktarbeiðni er samþykkt**  (með **ástandi**  **bíður samþykktar >0**) þegar atvik eru dæmi um það hvar aðalatriði er breytt þegar atburður getur valdið vandræðum. Þá hafa svör þeirra næsta skref sem vísar til **beiðninnar Senda samþykktarbeiðni fyrir færsluna og stofna síðan tilkynningu** um samþykki **lánardrottins þegar atvikið fer** fram. Þar sem svar við samþykkt **lánardrottins er beðið** um það hvenær atburður er ekki lengur tiltækur er inndregið þegar atburðir virka ekki eins og búist er við.
>
> Tilgreina þarf næstu skref fyrir svör við þeim atburðum sem vísað er til breytta atburðarins.