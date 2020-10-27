---
title: Meðhöndlun gilda sem vantar fyrir valkosti
description: Kynntu þér hvernig á að koma í veg fyrir að full samstilling misheppnist vegna þess að valkostir eru mismunandi í vörpuðum reitum.
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 10/01/2020
ms.openlocfilehash: 9148217400da88506e41b460157fe00be596a7c5
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911668"
---
# <a name="handling-missing-option-values"></a>Meðhöndlun gilda sem vantar fyrir valkosti
[!INCLUDE[d365fin](includes/cds_long_md.md)] inniheldur aðeins þrjá valkostarreiti sem innihalda valgildi sem hægt er að varpa í [!INCLUDE[d365fin](includes/d365fin_md.md)] reiti af gerð valkostar<!-- Option type, not enum? @Onat can you vertify this? --> fyrir sjálfvirka samstillingu. Við samstillingu eru óvarpaðir valkostir hunsaðir og valkostina sem vantar er komið fyrir í tengdri [!INCLUDE[d365fin](includes/d365fin_md.md)] töflu og bætt við kerfistöfluna **Vörpun CDS-valkosta** til að meðhöndla handvirkt seinna. Til dæmis með því að bæta við valkostunum sem vantar í aðrahvora vöruna og síðan uppfæra vörpunina. Í þessum hluta er því lýst hvernig það virkar.

Síðan **Vörpun samþættingartöflu** inniheldur þrjár varpanir fyrir reiti sem innihalda eitt eða fleiri varpað valgildi. Eftir fulla samstillingu inniheldur síðan **Vörpun CDS-valkosta** óvarpaða valkostina í þremur reitum.

|         Færsla             | Gildi valkosts | Yfirskrift valkostsgildis |
|----------------------------|--------------|----------------------|
| Greiðsluskilmálar: NET30       | 1            | Nettó 30               |
| Greiðsluskilmálar: 2%10NET30   | 2            | 2% 10; Nettó 30        |
| Greiðsluskilmálar: NET45       | 3            | Nettó 45               |
| Greiðsluskilmálar: NET60       | 4            | Nettó 60               |
| Afhendingarmáti: FOB       | 1            | FOB                  |
| Afhendingarmáti: NOCHARGE  | 2            | Gjaldfrjálst            |
| Flutningsaðili: AIRBORNE   | 1            | Á flugi             |
| Flutningsaðili: DHL        | 2            | DHL                  |
| Flutningsaðili: FEDEX      | 3            | FEDEX                |
| Flutningsaðili: UPS        | 4            | UPS                  |
| Flutningsaðili: POSTALMAIL | 5            | Póstur          |
| Flutningsaðili: FULLLOAD   | 6            | Fullt álag            |
| Flutningsaðili: WILLCALL   | 7            | Mun hringja            |

Efni síðunnar **Vörpun CDS-valkosta** byggist á fasttextagildum í töflunni **CDS-reikningur** . Í [!INCLUDE[d365fin](includes/cds_long_md.md)], er eftirfarandi reitum í reikningseiningunni varpað í reiti viðskiptavina- og lánardrottnafærslna:

- **Aðsetur 1: Flutningsskilmálar** af gagnagerðinni fasttexti, þar sem gildi eru skilgreind á eftirfarandi hátt:

```
enum 5335 "CDS Shipment Method Code"
{
    Extensible = true;
    value(0; " ") { Caption = ' '; }
    value(1; "FOB") { Caption = 'FOB'; }
    value(2; "NoCharge") { Caption = 'No Charge'; }
}
```

- **Aðsetur 1: Afhendingarmáti** af gagnagerðinni fasttexti, þar sem gildi eru skilgreind á eftirfarandi hátt:

```
enum 5336 "CDS Shipping Agent Code"
enum 5336 "CDS Shipping Agent Code"
{
    Extensible = true;
    value(0; " ") { Caption = ' '; }
    value(1; "Airborne") { Caption = 'Airborne'; }
    value(2; "DHL") { Caption = 'DHL'; }
    value(3; "FedEx") { Caption = 'FedEx'; }
    value(4; "UPS") { Caption = 'UPS'; }
    value(5; "PostalMail") { Caption = 'Postal Mail'; }
    value(6; "FullLoad") { Caption = 'Full Load'; }
    value(7; "WillCall") { Caption = 'Will Call'; }
}
```

- **Greiðsluskilmálar** af gagnagerðinni fasttexti, þar sem gildi eru skilgreind á eftirfarandi hátt:

```
enum 5334 "CDS Payment Terms Code"
{
    Extensible = true;
    value(0; " ") { Caption = ' '; }
    value(1; "Net30") { Caption = 'Net 30'; }
    value(2; "2%10Net30") { Caption = '2% 10; Net 30'; }
    value(3; "Net45") { Caption = 'Net 45'; }
    value(4; "Net60") { Caption = 'Net 60'; }
}
```

Öllum [!INCLUDE[d365fin](includes/d365fin_md.md)] fasttextunum að ofan er varpað í safn valkosta í [!INCLUDE[d365fin](includes/cds_long_md.md)].

### <a name="extending-option-sets-in-d365fin"></a>Viðbót við safn valkosta í [!INCLUDE[d365fin](includes/d365fin_md.md)]
1. Búa til nýja AL-viðbót.

2. Bæta við viðbót fasttexta fyrir valkostina sem auka á við. Gætið þess að sama gildi sé notað. 

```
enumextension 50100 "CDS Payment Terms Code Extension" extends "CDS Payment Terms Code"
{
    value(779800001; "Cash Payment") { Caption = 'Cash Payment'; }
    value(779800002; "Transfer") { Caption = 'Transfer'; }
}
```

> [!IMPORTANT]  
> Nota verður sömu auðkennisgildi valkostar úr [!INCLUDE[d365fin](includes/cds_long_md.md)] þegar bætt er við [!INCLUDE[d365fin](includes/d365fin_md.md)] fasttextann. Annars mistekst samstillingin.

> [!IMPORTANT]  
> Ekki skal nota stafinn "," í fasttextagildi og skjátexta. Þetta er sem stendur ekki stutt af [!INCLUDE[d365fin](includes/d365fin_md.md)] keyrslunni.

> [!NOTE]
> Fyrstu tíu stafirnir á nýjum heitum og myndatextum valgilda verða að vera einkvæmir. Til dæmis kemur upp villa ef tveir valkostir heita „Transfer 20 working days“ og „Transfer 20 calendar days“ vegna þess að báðir eru með fyrstu 10 stafina „Transfer 2“. Nefndu þá til dæmis „TRF20 WD“ og „TRF20 CD.“

### <a name="update-d365fin-option-mapping"></a>Uppfæra vörpun [!INCLUDE[d365fin](includes/cds_long_md.md)] valkostar
Nú er hægt að endurgera vörpunina milli [!INCLUDE[d365fin](includes/cds_long_md.md)] valkosta og [!INCLUDE[d365fin](includes/d365fin_md.md)] færslna.

Á síðunni **Vörpun samþættingartöflu** skal velja línuna fyrir vörpun **Greiðsluskilmálar** og síðan velja aðgerðina **Samstilla breyttar færslur** . Síðan **Vörpun CDS-valkosta** er uppfærð með viðbótarfærslunum hér að neðan.

|         Færsla                 | Gildi valkosts   | Yfirskrift valkostsgildis |
|--------------------------------|----------------|----------------------|
| Greiðsluskilmálar: NET30           | 1              | Nettó 30               |
| Greiðsluskilmálar: 2%10NET30       | 2              | 2% 10; Nettó 30        |
| Greiðsluskilmálar: NET45           | 3              | Nettó 45               |
| Greiðsluskilmálar: NET60           | 4              | Nettó 60               | 
| **Greiðsluskilmálar: STAÐGREIÐSLA**  | **779800001**  | **Staðgreiðsla**     |
| **Greiðsluskilmálar: MILLIFÆRSLA**    | **779800002**  | **Millifærsla**         |

Taflan **Greiðsluskilmálar** í [!INCLUDE[d365fin](includes/d365fin_md.md)] verður þá með nýjum færslum fyrir [!INCLUDE[d365fin](includes/cds_long_md.md)] valkostina. Í eftirfarandi töflu eru nýir valkostir feitletraðir. Skáletraðar línur tákna alla valkostina sem nú er hægt að samstilla. Eftirstandandi línur tákna valkosti sem eru ekki í notkun og verða hunsaðir við samstillingu. Hægt er að fjarlægja þær eða víkka út CDS-valkostina með sömu heitum.)

| Kóti       | Gjalddagaútreikningur | Tímabil afsláttar | Afsláttur % | Reikna greiðsluafsl. af kreditreikn. | Description       |
|------------|----------------------|---------------------------|------------|-------------------------------|-------------------|
| 10 DAGAR    | 10D                  |                           | 0.         | RANGT                         | Nettó 10 dagar       |
| 14 DAGAR    | 14D                  |                           | 0.         | RANGT                         | Nettó 14 dagar       |
| 15 DAGAR    | 15D                  |                           | 0.         | RANGT                         | Nettó 15 dagar       |
| 1M(8D)     | 1 milljón                   | 8D                        | 2.         | RANGT                         | 1 Mánuður/2% 8 dagar |
| 2 DAGAR     | 2D                   |                           | 0.         | RANGT                         | Nettó 2 dagar        |
| *2%10NET30* |                      |                           | 0.         | RANGT                         |                   |
| 21 DAGUR    | 21D                  |                           | 0.         | RANGT                         | Nettó 21 dagur       |
| 30 DAGAR    | 30 d.                  |                           | 0.         | RANGT                         | Nettó 30 dagar       |
| 60 DAGAR    | 60 d.                  |                           | 0.         | RANGT                         | Nettó 60 dagar       |
| 7 DAGAR     | 7D                   |                           | 0.         | RANGT                         | Nettó 7 dagar        |
| ***STAÐGREIÐSLA*** |                      |                           | 0.         | RANGT                         |                   |
| LM         | LM                   |                           | 0.         | RANGT                         | Gildandi mánuður     |
| Greiðslukrafa        | 0D                   |                           | 0.         | RANGT                         | Greiðslukrafa  |
| *NET30*      |                      |                           | 0.         | RANGT                         |                   |
| *NET45*      |                      |                           | 0.         | RANGT                         |                   |
| *NET60*      |                      |                           | 0.         | RANGT                         |                   |
| ***MILLIFÆRSLA*** |                      |                           | 0.         | RANGT                         |                   |

## <a name="see-also"></a>Sjá einnig
