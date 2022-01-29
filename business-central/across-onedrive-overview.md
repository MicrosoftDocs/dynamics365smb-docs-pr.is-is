---
title: Business Central og OneDrive fyrir Business Integration
description: Þú getur notað OneDrive fyrir Business til að geyma, hafa umsjón með og deila skrám á borð við skýrslur eða skráarviðhengi.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: overview
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: bholtorf
ms.openlocfilehash: 8965fe1c0f04c3b12fef984e71b7f2643f7f11c2
ms.sourcegitcommit: 8464b37c4f1e5819aed81d9cfdc382fc3d0762fc
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/19/2022
ms.locfileid: "8012576"
---
# <a name="business-central-and-onedrive-for-business-integration"></a>Business Central og OneDrive fyrir Business Integration
OneDrive til viðskipta er skýgeymsluþjónusta sem er innifalin í Microsoft 365. [!INCLUDE[prod_short](includes/prod_short.md)] auðveldar geymslu, umsjón og deilingu skráa með öðrum í gegnum OneDrive. Þegar skrá er í OneDrive getur þú notið ríkulegs samstarfs úr netútgáfum af vörum Microsoft, t.d. Word, Excel og PowerPoint. Til dæmis er hægt að deila Word-skjali og þá getur þú og samstarfsfólk þitt breytt því saman í rauntíma. OneDrive gerir þér líka kleift að opna aðrar gerðir skráa, t.d. PDF. 

## <a name="getting-started"></a>Hafist handa
Við höfum búið til tenginguna milli [!INCLUDE[prod_short](includes/prod_short.md)] á netinu og OneDrive og því er auðvelt að hefjast handa. Eina krafan er sú að notendur hafi opnað OneDrive að minnsta kosti einu sinni. 

Á flestum síðum þar sem skrár eru tiltækar, svo sem í innhólfi skýrslunnar eða skrám sem hengar eru við færslur, finnur þú aðgerðina **Opna í OneDrive**.

:::image type="content" source="media/Open in OneDrive.PNG" alt-text="Opna í OneDrive aðgerðin":::

 
:::image type="content" source="media/OneDrive attachment.PNG" alt-text="Deila skrá í viðhengjum í OneDrive":::

Þegar þú notar aðgerðina **Opna í OneDrive** í fyrsta skipti gerir [!INCLUDE[prod_short](includes/prod_short.md)] eftirfarandi í OneDrive þínu:

1. Stofnar möppu sem heitir [!INCLUDE[prod_short](includes/prod_short.md)]. 
2. Í [!INCLUDE[prod_short](includes/prod_short.md)] möppunni býr það til aðra möppu með sama heiti og fyrirtækið sem þú ert að vinna í. Ef unnið er í fleiri en einu fyrirtæki mun það búa til möppu fyrir fyrirtækið sem unnið er í þegar aðgerðin **Opna í OneDrive** er notuð. 
3. Setur afrit af skránni sem þú valdir í möppuna og opnar svo skrána. Næst þegar þú notar aðgerðina afritar það aðeins og opnar skrána. 

Mappan og efni hennar eru lokuð þar til þú ákveður að deila því með öðrum. Til dæmis gætir þú ákveðið að deila efni með einum eða fleiri samstarfsmönnum þínum eða jafnvel fólki utan fyrirtækisins. Frekari upplýsingar er að finna í [Deila OneDrive skrám og möppum](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).

> [!NOTE]
> Einnig er hægt að tengja [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum við OneDrive. Nokkur atriði þarf hinsvegar að hafa í huga til að það gangi upp. Frekari upplýsingar er að finna í [Skilgreining Business Central-þjóns innanhúss](admin-onedrive-integration.md#configuring-business-central-on-premises).

## <a name="see-also"></a>Sjá einnig
[Stjórnun OneDrive samþættingar við Business Central](admin-onedrive-integration.md)  
[Opna Business Central Files í OneDrive](across-share-onedrive.md)  
[OneDrive ALGENGAR SPURNINGAR](admin-onedrive-faq.md)