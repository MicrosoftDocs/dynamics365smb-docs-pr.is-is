---
title: Áætla vinnslur fyrir leiðréttingu og afstemmingu birgðakostnaðar
description: Kynntu þér hvernig þú getur notað verkröðina til að færa verkin til að leiðrétta birgðakostnað eða afstemma hann við fjárhag í bakgrunni. Til dæmis ef fyrirtækið keyrir mörg verk eða vinnur úr mörgum færslum.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.form: 461
ms.date: 09/23/2021
ms.author: andreipa
ms.openlocfilehash: 85fec80ca9b7f2184e67da58f9d05a86534e90ac
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/14/2022
ms.locfileid: "7973545"
---
# <a name="schedule-jobs-for-adjusting-and-reconciling-inventory-cost-with-the-general-ledger"></a>Áætla vinnslur fyrir leiðréttingu og afstemmingu birgðakostnaðar með fjárhag

Til að hámarka upplifunina er sjálfkrafa kveikt á sjálfvirkri kostnaðarleiðréttingu og bókun í fjárhag. Það gæti þó haft áhrif á afköstin því gögn safnast upp með tímanum. Til að draga úr álagi í forritinu er oft gagnlegt að nota verkraðarfærslur til að flytja verk í bakgrunnskeyrslu.

## <a name="move-the-task-of-adjusting-item-costs-to-the-background-with-the-help-of-assisted-setup"></a>Færa verk vegna leiðréttingar á kostnaði vöru í bakgrunninn með aðstoð hjálparuppsetningar

Það getur verið snúið að stofna færslur verkraðar, jafnvel fyrir vanan ráðgjafa, og erum við því með uppsetning með hjálp til að auðvelda ferlið við að leiðrétta kostnað vöru.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Birgðauppsetning** og veldu síðan tengda tengilinn.  
2. Á síðunni **Birgðauppsetning** skal smella á víxlhnappinn **Sjálfvirk kostnaðarbókun** eða tilgreina **Aldrei** í reitnum **Sjálfvirk kostnaðarleiðrétting**.  
3. Í tilkynningunni sem nú birtist efst á síðunni velur þú tengilinn **Tímasetja færslu verkraðar**. Þetta opnar hjálparuppsetninguna **Tímasetja kostnaðarleiðréttingu og bókanir**.  
4. Tilgreindu verkið sem á að tímasetja.  

  > [!NOTE]
  > Ekki er hægt að búa til nýja verkraðarfærslu ef verkraðarfærsla fyrir tilgreint verk er þegar til.

5. Veldu reitinn **Skoða færslur verkraðar þegar þeim er lokið** til að fara yfir og leiðrétta stillingar. Frekari upplýsingar, sjá [Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md).  

## <a name="to-create-a-job-queue-entry-for-adjusting-and-reconciling-inventory-cost-manually"></a>Að stofna færslu verkraðar til að leiðrétta og afstemma birgðakostnað handvirkt

Einnig er hægt að stofna færslur verkraðar handvirkt. Eftirfarandi ferli sýnir hvernig á að stilla runuvinnsluna **Leiðrétta kostnað - Birgðafærslur** til að hún keyri daglega, en sömu skrefin gilda um runuvinnsluna **Bóka birgðakostnað í fjárhag**.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verkraðarfærslur** og veldu síðan viðeigandi tengil.  
2. Valið er aðgerðin **Nýtt**.  
3. Í reitnum **Gerð hlutar sem á að keyra** skal velja *Skýrsla*.  
4. Í **Auðkenni hlutar sem á að keyra** skal velja *795*, **Leiðr. kostnað – Birgðafærslur**.  
5. Í reitinn **Reikniregla næstu keyrsludagsetningar** skal færa inn *1D*.
6. Í reitinn **Upphafstími** skal slá inn *2 AM*.
7. Velja aðgerðina **Stilla stöðu á Tilbúin**.

Nú verður birgðakostnaður uppfærður á hverju kvöldi.  

Til að tímasetja verk fyrir afstemmingu birgða í fjárhag skal velja kóðaeininguna 2846 **Bóka birgðakostnað í fjárhag**.

> [!TIP]
> Til að koma í veg fyrir læsingu skaltu ekki setja upp verk fyrir runuvinnsluna **Leiðrétta kostnað - Birgðafærslur**, codeunit **Bóka birgðakostnað í fjárhag** og verk vegna sölu- og innkaupabókunar á sama tíma. Einnig þarf að ganga úr skugga um að sami flokkur verkraðar sé notaður.

## <a name="see-also"></a>Sjá einnig

[Leiðr. kostnað vara](inventory-how-adjust-item-costs.md)  
[Afstemma birgðakostnað í fjárhag](finance-how-to-post-inventory-costs-to-the-general-ledger.md)  
[Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md)  
[Finndu síður og upplýsingar með Viðmótsleit](ui-search.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
