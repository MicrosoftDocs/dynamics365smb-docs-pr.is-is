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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/23/2022
ms.locfileid: "9585946"
---
# <a name="set-up-workflow-users"></a>Setja upp notendur verkflæðis

Áður en hægt er að stofna samþykktarverkflæði verður að setja upp notendur sem taka þátt í verkflæðum. Þetta þarf nauðsynlega að gera til að geta tilgreint hverjir verða að fá tilkynningu sem bregðast þarf við í verkflæðisskrefi.  

Á síðunni **Notendahópar verkflæðis** er hægt að setja upp notendur í notendahópum verkflæðis og tilgreina númer notanda í röð ferlisins, t.d. keðju samþykktaraðila. 

Verkflæðisnotendur sem virka eins og samþykktarnotendur, þ.m.t. bæði samþykktarbeiðendur og samþykktaraðilar, þarf einnig að setja upp á síðunni **Uppsetning samþykktarnotanda**. Frekari upplýsingar má finna á [Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md).  

> [!NOTE]  
> Til að skilgreina að samþykktarbeiðni sé ekki samþykkt fyrr en margir notendur hafa samþykkt hana skal setja upp samþykktaraðila í stigveldi. Hvað varðar samþykkjendur af gerðinni **Samþykkjandi** skal setja þá upp á síðunni **Uppsetning Samþykkjandi notandi**. Hvað varðar samþykkjendur af gerðinni **Notendaflokkur verkflæðis** skal setja þá upp á síðunni **Notendaflokkar verkflæðis** og skilgreina stigveldið með því að úthluta stighækkandi númerum á hvern samþykkjanda í reitnum **röð nr.**. . Frekari upplýsingar má finna hér að neðan og í [Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md). 

## <a name="to-set-up-a-workflow-user"></a>Uppsetning verkflæðisnotenda

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara inn **Notendahópar verkflæðis**, velja síðan viðkomandi tengil.  
2. Valið er aðgerðin **Nýtt**. Síðan **Notendahópur verkflæðis** opnast.  
3. Í **Kóði** reitinn skal slá inn að hámarki 20 stafi til að auðkenna verkflæðið.  
4. Í **Lýsing** reitnum skal lýsa verkflæðinu.  
5. Í flýtiflipanum **Aðilar í flokki verkflæðisnotenda** skal fylla inn í reitina í fyrstu línu eins og lýst er í eftirfarandi töflu.  

   |Svæði|Lýsing|
   |-----|-----------|
   |**Notandanafn**|Tilgreindu notandann sem á að taka þátt í verkflæðum.<br /><br /> Notandi verður að vera til á síðunni **Uppsetning notanda**. Frekari upplýsingar eru í [Úthluta leyfi til notenda og hópa](ui-define-granular-permissions.md).|
   |**Nr. raðar**|Tilgreina í hvaða röð notandi verkflæðis virkjast í verkflæði, út frá öðrum notendum. Þessi reitur gefið upp t.d. hvenær notandi samþykkir í samhengi við aðra samþykktaraðila með því að setja upp valkostinn **Notendahópur verkflæðis** í reitnum **Gerð samþykktaraðila** í tengdu verkflæðissvari.| 

   > [!TIP]
   > Til að skilgreina að samþykktarbeiðni þurfi marga jafna notendur til að samþykkja hana, án tillits til stigveldis, skal setja upp flatan notendahóp verkflæðis með því að úthluta sömu númeraröð til viðeigandi samþykktaraðila.

6. Endurtaktu skref 5 til að bæta fleiri notendum verkflæðis við notendahópinn.  
7. Endurtaka skref 2 til 6 til að bæta við fleiri notendaflokkum verkflæðis.  

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft þjálfun](/training/modules/create-workflows/)

## <a name="see-also"></a>Sjá einnig .

[Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md)  
[Setja upp Verkflæði samþykktar](across-set-up-workflows.md)  
[Nota Samþykktarverkflæði](across-use-workflows.md)  
[Kynning: Uppsetning og notkun á samþykktarverkflæði innkaupa](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Verkflæði](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
