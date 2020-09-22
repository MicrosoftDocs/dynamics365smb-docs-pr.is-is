---
title: Hönnunarupplýsingar - vörurakning í vöruhúsi | Microsoft Docs
description: Meðhöndlun á raðnúmeri eða lotunúmeri er aðallega vöruhúsaverkefni, og því eru öll vöruhúsaskjöl á innleið og útleið með staðlaða virkni fyrir úthlutun og val á vörurakningarnúmerum. Hins vegar, vegna þess að frátekningarkerfið er byggt á færslum í birgðahöfuðbók, eru skjöl um færslur í vöruhúsi sem skrá aðeins vöruhúsafærslur ekki studd að fullu.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item, tracking, serial number, lot number, outbound documents
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 6ffce5d73eabe8586ac682f6d1a549993b1b6d2a
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2020
ms.locfileid: "3787547"
---
# <a name="design-details-item-tracking-in-the-warehouse"></a>Hönnunarupplýsingar: vörurakning í vöruhúsi
Meðhöndlun á raðnúmeri eða lotunúmeri er aðallega vöruhúsaverkefni, og því eru öll vöruhúsaskjöl á innleið og útleið með staðlaða virkni fyrir úthlutun og val á vörurakningarnúmerum.  

Hins vegar, vegna þess að frátekningarkerfið er byggt á færslum í birgðahöfuðbók, eru skjöl um færslur í vöruhúsi sem skrá aðeins vöruhúsafærslur ekki studd að fullu. Vegna þess að frátekningar og vörurakningarnúmer geta aðeins verið meðhöndluð á staðsetningastigi, ekki á hólfa- og svæðisstigi er ekki hægt að opna síðuna **Vörurakningarlínur** úr virkniskjölum vöruhúss. Sama á við um síðuna **Frátekning**.  

Eftir að rað- eða lotunúmer hefur verið bætt við vöru í vöruhúsastaðsetningu er hægt að færa hana og endurflokka að vild í vöruhúsinu með því að nota sjálfstæða vörurakningaruppbyggingu sem er ótengd frátekningarkerfinu. **Raðnúmer** og **Lotunúmer** er farið inn í beint úr vöruhúsaskjalalínunum. Þegar rað- eða lotunúmer verður seinna hluti af bókun á útleið er það samstill við frátekningarkerfið sem hluti af venjulegri leiðréttingu hólfa. Nánari upplýsingar eru í [Upplýsingar um hönnun: Samþætting við birgðir](design-details-integration-with-inventory.md).  

Hins vegar tekur frátekningarkerfið tillit til vöruhúsaaðgerða þegar það reiknar út framboð. Til dæmis vörur sem úthlutað er til tínslu eða skráðar sem tíndar er ekki hægt að taka frá. Nánari upplýsingar eru í [Hönnunarupplýsingar: staða vöruhúss](design-details-availability-in-the-warehouse.md).

## <a name="see-also"></a>Sjá einnig  
[Hönnunarupplýsingar: vörurakning](design-details-item-tracking.md)  
[Hönnunarupplýsingar: Sameining með birgðum](design-details-integration-with-inventory.md)  
[Hönnunarupplýsingar: staða vöruhúss](design-details-availability-in-the-warehouse.md)  
[Hönnunarupplýsingarn: vörurakning hönnun](design-details-item-tracking-design.md)
