---
title: Business Central og OneDrive fyrir Business Integration
description: Þú getur notað OneDrive fyrir Business til að geyma, hafa umsjón með og deila skrám á borð við skýrslur eða skráarviðhengi. Einnig ef þú stafar hana One Drive.
author: jswymer
ms.topic: overview
ms.workload: na
ms.search.keywords: ''
ms.date: 02/28/2022
ms.author: jswymer
ms.openlocfilehash: 5968cd8d2348b0fac7c81c4b588dfd89388a27f5
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9606468"
---
# <a name="business-central-and-onedrive-for-business-integration"></a>Business Central og OneDrive fyrir Business Integration

OneDrive fyrir Business er skýjageymsluþjónusta sem er hluti af Microsoft 365. [!INCLUDE[prod_short](includes/prod_short.md)] auðveldar geymslu, umsjón og deilingu skráa með öðrum í gegnum OneDrive. Þegar skrá er í OneDrive getur þú notið ríkulegs samstarfs úr netútgáfum af vörum Microsoft, t.d. Word, Excel og PowerPoint. Til dæmis er hægt að deila Word-skjali og þá getur þú og samstarfsfólk þitt breytt því saman í rauntíma. OneDrive gerir þér líka kleift að opna aðrar gerðir skráa, t.d. PDF. 

## <a name="get-started-with-onedrive-features"></a>Hafist handa með OneDrive eiginleika

Ef þú notar [!INCLUDE[prod_short](includes/prod_short.md)] á netinu höfum við þegar búið til tenginguna á milli [!INCLUDE[prod_short](includes/prod_short.md)] á netinu og OneDrive þannig að auðvelt er að hefjast handa. Eina krafan er sú að notendur hafi opnað OneDrive að minnsta kosti einu sinni. Með [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum þarf stjórnandi að grunnstilla tenginguna áður en þú getur hafist handa. Frekari upplýsingar eru í [Stjórnun OneDrive samþættingar við Business Central](admin-onedrive-integration.md).

<!-- We've created the connection between [!INCLUDE[prod_short](includes/prod_short.md)] online and OneDrive, so it's easy to get started. The only requirement is that users have opened OneDrive at least one time. -->

### <a name="open-and-share-in-onedrive"></a>Opna og deila í OneDrive

Á flestum síðum þar sem skrár eru tiltækar, svo sem í innhólfi skýrslunnar eða skrám sem hengdar eru við færslur, finnur þú aðgerðirnar **Opna í OneDrive** og **Deila**.

:::image type="content" source="media/onedrive-overview-report-inbox-w-outline.png" alt-text="Opna í OneDrive og deilingaraðgerðirnar fyrir skýrslur":::


:::image type="content" source="media/one-drive-attachments-w-outline.png" alt-text="Opna í OneDrive og deilingaraðgerðirnar fyrir fylgiskjöl":::

|skal velja...|Til...|Sjá meiri upplýsingar...|
|---------|-----|----------------|
|Opna í OneDrive|Afritaðu skrána í möppu Business Central í OneDrive og opnaðu skrána.|[Opna í OneDrive](across-share-onedrive.md#open-in-onedrive) |
|Deila|Afritaðu skrána í OneDrive og deildu henni með öðrum.|[Deila í OneDrive](across-share-onedrive.md#share) |

### <a name="save-excel-workbooks-and-report-files-in-onedrive"></a>Vista vinnubækur og skýrsluskrár Excel í OneDrive

Með uppsetningu OneDrive samþættingar munu nokkrir aðrir kunnuglegir eiginleikar sjálfkrafa nota OneDrive til að vista skrár í stað þess að vista skrár í tækinu þínu:

- Aðgerðirnar **Opna í Excel** og **Breyta í Excel** á listasíðum munu afrita Excel-skrána sjálfkrafa í OneDrive, síðan opna hana í Excel Online. Frekari upplýsingar er að finna í [Skoða og breyta í Excel](across-work-with-excel.md).
- Að senda skýrslu í Excel- eða Word-skrá mun afrita skrána sjálfkrafa í OneDrive, síðan opna hana í Excel eða Word á netinu. Frekari upplýsingar er að finna í [Skýrsla vistuð í skrá](ui-work-report.md#saving-a-report-to-a-file).

Ekki er kveikt á þessum eiginleikum að sjálfgefnu. En sem stjórnandi getur þú auðveldlega kveikt á þeim með því að nota uppsetningarleiðbeininguna **OneDrive uppsetning**.

<!--
When you use the **Open in OneDrive** action for the first time, [!INCLUDE[prod_short](includes/prod_short.md)] does the following in your OneDrive:

1. Creates a folder named [!INCLUDE[prod_short](includes/prod_short.md)]. 
2. In the [!INCLUDE[prod_short](includes/prod_short.md)] folder, it creates another folder with the same name as the company you're working in. If you work in more than one company, it will create a folder for the company you're working in when you use the **Open in OneDrive** action. 
3. Puts a copy of the file you selected in the folder, and then opens the file. The next time you use the action, it only copies and opens the file. 

The folder and its content are private until you decide to share them with others. For example, you might decide to share content with one or more of your coworkers, or even people outside of your organization. For more information, see [Share OneDrive files and folders](https://support.microsoft.com/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07) in the content for OneDrive.
-->

> [!NOTE]
> Einnig er hægt að tengja [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum við OneDrive. Nokkur atriði þarf hinsvegar að hafa í huga til að það gangi upp. Frekari upplýsingar er að finna í [Skilgreining Business Central-þjóns innanhúss](admin-onedrive-integration-onpremises.md).

## <a name="see-also"></a>Sjá einnig .

[Stjórnun OneDrive samþættingar við Business Central](admin-onedrive-integration.md)  
[Opna Business Central Files í OneDrive](across-share-onedrive.md)  
[OneDrive ALGENGAR SPURNINGAR](admin-onedrive-faq.md)  
