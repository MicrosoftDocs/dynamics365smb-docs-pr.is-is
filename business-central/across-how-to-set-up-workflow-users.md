---
title: 'Hvernig á að: Setja upp notendur verkflæðis'
description: Áður en hægt er að stofna verkflæði verður að setja upp notendur sem taka þátt í þeim á síðu notendaflokks verkflæðis.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reject, delegate, request
ms.search.form: 1533
ms.date: 09/09/2022
ms.author: edupont
ms.openlocfilehash: 4dbe4217720ddd0bfe976560331329537577cfeb
ms.sourcegitcommit: 9049f75c86dea374e5bfe297304caa32f579f6e4
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/23/2022
ms.locfileid: "9585946"
---
# <a name="set-up-workflow-users"></a>Setja upp notendur verkflæðis

Áður en hægt er að stofna samþykktarverkflæði þarf að setja upp notendurna sem taka þátt í verkflæði. Þetta þarf nauðsynlega að gera til að geta tilgreint hverjir verða að fá tilkynningu sem bregðast þarf við í verkflæðisskrefi.  

**Á síðunni verkflæði notendaflokka** er hægt að setja upp notendur í verkflæði notendaflokka og tilgreina númer notanda í ferlaröð, eins og til dæmis samþykkjakeðju. 

Notendur verkflæðis sem samþykktarnotendur, þar á **meðal bæði samþykktaraðilar og samþykkjendur, verða einnig að setja upp á síðunni Samþykktarnotendauppsetning**. Frekari upplýsingar um [uppsetningu Samþykktarnotenda](across-how-to-set-up-approval-users.md).  

> [!NOTE]  
> Ef skilgreina á samþykktarbeiðni sem ekki samþykkt fyrr en margir notendur hafa samþykkt hana er sett samþykkjendur upp í stigveldi. Hvað varðar samþykkjendur af gerðinni **Samþykkjandi** skal setja þá upp á síðunni **Uppsetning Samþykkjandi notandi**. Notendaflokkur **verkflæðis fyrir samþykkjanda** er stilltur, stilla samþykkjendur á **síðunni verkflæði notendaflokka** og skilgreina stigveldið með því að úthluta stigvaxandi númerum á hvern samþykkjanda í reitnum **Raðnúmer nr.** . Frekari upplýsingar hér að neðan og í [uppsetningu Samþykktarnotenda](across-how-to-set-up-approval-users.md). 

## <a name="to-set-up-a-workflow-user"></a>Uppsetning verkflæðisnotenda

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **notendaflokka** verkflæðis og velja síðan tengda tengilinn.  
2. Valið er aðgerðin **Nýtt**. Síðan **Notendahópur verkflæðis** opnast.  
3. Í **Kóði** reitinn skal slá inn að hámarki 20 stafi til að auðkenna verkflæðið.  
4. Í **Lýsing** reitnum skal lýsa verkflæðinu.  
5. **Á fastflipa fyrir meðlimi** verkflæðis-notendaflokksins eru reitirnir í fyrstu línunni fylltir út eins og lýst er í eftirfarandi töflu.  

   |Svæði|Lýsing|
   |-----|-----------|
   |**Notandanafn**|Tilgreina notandann sem á að taka þátt í verkflæði.<br /><br /> Notandi verður að vera til á síðunni **Uppsetning notanda**. [Frekari upplýsingar um úthlutun heimilda til notenda og hópa](ui-define-granular-permissions.md).|
   |**Nr. raðar**|Tilgreina í hvaða röð notandi verkflæðis virkjast í verkflæði, út frá öðrum notendum. Þetta svæði getur til dæmis átt við þegar notandinn samþykkir að vera tengdur öðrum samþykkjendum með því að setja upp **valkostinn verkflæði notendaflokks** í **reitnum Tegund** samþykkjanda verkflæðis.| 

   > [!TIP]
   > Til að skilgreina að samþykktarbeiðni krefst þess að margir jafnsettir notendur samþykki hana óháð stigveldi skal setja upp notendaflokk fyrir flatt verkflæði með því að úthluta sama raðnúmeri á alla viðeigandi samþykkjendur.

6. Endurtaka skref 5 til að bæta fleiri verkflæðinotendum við notendaflokk verkflæðis.  
7. Endurtaka skref 2 til 6 til að bæta við fleiri notendaflokkum verkflæðis.  

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/create-workflows/)

## <a name="see-also"></a>Sjá einnig .

[Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md)  
[Uppsetning Samþykktarverkflæðis](across-set-up-workflows.md)  
[Nota samþykktarverkflæði](across-use-workflows.md)  
[Kynning: Uppsetning og notkun á samþykktarverkflæði innkaupa](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Verkflæði](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
