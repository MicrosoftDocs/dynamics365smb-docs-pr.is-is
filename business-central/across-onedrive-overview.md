---
title: Business Central og OneDrive fyrir Business Integration
description: Þú getur notað OneDrive fyrir Business til að geyma, hafa umsjón með og deila skrám á borð við skýrslur eða skráarviðhengi.
author: jswymer
ms.topic: overview
ms.workload: na
ms.search.keywords: ''
ms.date: 02/28/2022
ms.author: jswymer
ms.openlocfilehash: 371c090e321992ec2fdc0ee7cb218feaa6b16d9a
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8521229"
---
# <a name="business-central-and-onedrive-for-business-integration"></a>Business Central og OneDrive fyrir Business Integration

OneDrive til viðskipta er skýgeymsluþjónusta sem er innifalin í Microsoft 365. [!INCLUDE[prod_short](includes/prod_short.md)] auðveldar geymslu, umsjón og deilingu skráa með öðrum í gegnum OneDrive. Þegar skrá er í OneDrive getur þú notið ríkulegs samstarfs úr netútgáfum af vörum Microsoft, t.d. Word, Excel og PowerPoint. Til dæmis er hægt að deila Word-skjali og þá getur þú og samstarfsfólk þitt breytt því saman í rauntíma. OneDrive gerir þér líka kleift að opna aðrar gerðir skráa, t.d. PDF. 

## <a name="getting-started"></a>Hafist handa

Við höfum búið til tenginguna milli [!INCLUDE[prod_short](includes/prod_short.md)] á netinu og OneDrive og því er auðvelt að hefjast handa. Eina krafan er sú að notendur hafi opnað OneDrive að minnsta kosti einu sinni. 

Á flestum síðum þar sem skrár eru tiltækar, svo sem í Skýrsluinnhólfinu eða skrám sem tengdar eru færslum, er hægt að finna **opnar inn OneDrive** og **samnýta** Aðgerðir.

:::image type="content" source="media/onedrive-overview-report-inbox-w-outline.png" alt-text="Glugginn opna í OneDrive og samnýta aðgerðir fyrir skýrslur":::


:::image type="content" source="media/one-drive-attachments-w-outline.png" alt-text="Glugginn opna í OneDrive og samnýta aðgerðir fyrir viðhengi":::

|Veldu...|Að...|Sjá frekari uppl...|
|---------|-----|----------------|
|Opnar í OneDrive|Afritið skrána í Aðalmöppu notanda OneDrive og opnið hana.|[Opnar í OneDrive](across-share-onedrive.md#open-in-onedrive) |
|Hlutdeild|Afritaðu skrána yfir á þína OneDrive og Deildu henni með öðrum.|[Hlut í OneDrive](across-share-onedrive.md#share) |

<!--
When you use the **Open in OneDrive** action for the first time, [!INCLUDE[prod_short](includes/prod_short.md)] does the following in your OneDrive:

1. Creates a folder named [!INCLUDE[prod_short](includes/prod_short.md)]. 
2. In the [!INCLUDE[prod_short](includes/prod_short.md)] folder, it creates another folder with the same name as the company you're working in. If you work in more than one company, it will create a folder for the company you're working in when you use the **Open in OneDrive** action. 
3. Puts a copy of the file you selected in the folder, and then opens the file. The next time you use the action, it only copies and opens the file. 

The folder and its content are private until you decide to share them with others. For example, you might decide to share content with one or more of your coworkers, or even people outside of your organization. For more information, see [Share OneDrive files and folders](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).
-->

> [!NOTE]
> Einnig er hægt að tengja [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum við OneDrive. Nokkur atriði þarf hinsvegar að hafa í huga til að það gangi upp. Frekari upplýsingar er að finna í [Skilgreining Business Central-þjóns innanhúss](admin-onedrive-integration.md#configuring-business-central-on-premises).

## <a name="see-also"></a>Sjá einnig
[Stjórnun OneDrive samþættingar við Business Central](admin-onedrive-integration.md)  
[Opna Business Central Files í OneDrive](across-share-onedrive.md)  
[OneDrive ALGENGAR SPURNINGAR](admin-onedrive-faq.md)