---
title: Hönnunarupplýsingar - vörurakning í vöruhúsi
description: Vöruhúsaskjöl á innleið og útleið eru með staðlaða virkni fyrir úthlutun og val á vörurakningarnúmerum.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'design, item, tracking, serial number, lot number, outbound documents'
ms.date: 06/15/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
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


[!INCLUDE[footer-include](includes/footer-banner.md)]
