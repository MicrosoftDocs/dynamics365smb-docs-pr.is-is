---
title: 'Hvernig á að: Setja upp notendur verkflæðis'
description: Áður en hægt er að stofna verkflæði þarf að setja upp notendurna sem taka þátt í þeim á síðunni Samþykktarnotendauppsetning.
author: brentholtorf
ms.topic: how-to
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'reject, delegate, request'
ms.search.form: '1533,'
ms.date: 05/31/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Setja upp röð notenda verkflæðis

Áður en hægt er að stofna samþykktarverkflæði þarf að setja upp notendurna sem munu Senda beiðnir og samþykkjendur þeirra. Til dæmis er hægt að tilgreina hver fær tilkynningu til að vinna í verkflæðisskrefi. Þátttakendur samþykktarverkflæðis eru  **settir upp á síðunni samþykktarnotandasíða** . Frekari upplýsingar má finna á [Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md).

 **Á síðunni Verkflæðisnotendaflokkar**  er hægt að tilgreina hvar þátttakandi á í samþykktarverkflæði með því að færa númer inn í  **númeraröð númeraraðarinnar.** . Til dæmis er hægt að tilgreina að notendur taki þátt í réttri röð, t.d. keðju samþykkjendur. Einnig er hægt að tilgreina flatarlista samþykkjendur með því að færa inn sama númer. Í síðara tilfellinu þarf aðeins einn samþykkjendum að samþykkja beiðni.

[!INCLUDE [workflow-requestor-approver](includes/workflow-requestor-approver.md)]

## Notendaflokkur verkflæðis settur upp

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara inn **Notendahópar verkflæðis**, velja síðan viðkomandi tengil.  
2. Valið er aðgerðin **Nýtt**. Síðan **Notendahópur verkflæðis** opnast.  
3. Í **Kóði** reitinn skal slá inn að hámarki 20 stafi til að auðkenna verkflæðið.  
4. Í **Lýsing** reitnum skal lýsa verkflæðinu.  
5. Í flýtiflipanum **Aðilar í flokki verkflæðisnotenda** skal fylla inn í reitina í fyrstu línu eins og lýst er í eftirfarandi töflu.  

   |Svæði|Heimildasamstæða|
   |-----|-----------|
   |**Notandanafn**|Tilgreina notandann sem tekur þátt í verkflæði.<br /><br /> Notandi verður að vera til á síðunni **Uppsetning notanda**. Frekari upplýsingar eru í [Úthluta leyfi til notenda og hópa](ui-define-granular-permissions.md).|
   |**Nr. raðar**|Tilgreina í hvaða röð notandi verkflæðis virkjast í verkflæði, út frá öðrum notendum. Þessi reitur gefið upp t.d. hvenær notandi samþykkir í samhengi við aðra samþykktaraðila með því að setja upp valkostinn **Notendahópur verkflæðis** í reitnum **Gerð samþykktaraðila** í tengdu verkflæðissvari.| 

6. Endurtaktu skref 5 til að bæta fleiri notendum verkflæðis við notendahópinn.  

## Sjá einnig .

[Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md)  
[Setja upp Verkflæði samþykktar](across-set-up-workflows.md)  
[Nota Samþykktarverkflæði](across-use-workflows.md)  
[Kynning: Uppsetning og notkun á samþykktarverkflæði innkaupa](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Verkflæði](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
