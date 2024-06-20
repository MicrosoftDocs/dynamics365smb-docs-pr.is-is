---
title: 'Hvernig á að: Setja upp notendur verkflæðis'
description: Áður en hægt er að stofna verkflæði verður að setja upp notendurna sem taka þátt í þeim á síðunni Notandauppsetning samþykktar.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'reject, delegate, request'
ms.search.form: '1533,'
ms.date: 04/04/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="set-up-a-sequence-of-workflow-users"></a>Setja upp runu verkflæðisnotenda

Áður en hægt er að stofna samþykktarverkflæði verður að setja upp notendur sem geta sent inn beiðnir og samþykkjendur þeirra. Til dæmis er hægt að tilgreina hver fær tilkynningu til að bregðast við verkflæðisskrefi. Þátttakendur samþykktarverkflæðis eru settir upp á síðunni **Notandauppsetning samþykktar** . Frekari upplýsingar má finna á [Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md).

Á síðunni **Notendaflokkar** verkflæðis er hægt að tilgreina hvar þátttakandi tekur þátt í samþykktarverkflæði með því að færa inn númer í reitinn **Raðnr.** . Til dæmis er hægt að tilgreina að notendur geti tekið þátt í röð, t.d. keðja samþykkjenda. Einnig er hægt að tilgreina flatan lista yfir samþykkjendur með því að færa inn sama númer. Í seinni tilfellinu verður aðeins einn samþykkjanda að samþykkja beiðni.

[!INCLUDE [workflow-requestor-approver](includes/workflow-requestor-approver.md)]

## <a name="to-set-up-a-workflow-user-group"></a>Til að setja upp notendaflokk verkflæðis

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara inn **Notendahópar verkflæðis**, velja síðan viðkomandi tengil.  
2. Valið er aðgerðin **Nýtt**. Síðan **Notendahópur verkflæðis** opnast.  
3. Í **Kóði** reitinn skal slá inn að hámarki 20 stafi til að auðkenna verkflæðið.  
4. Í **Lýsing** reitnum skal lýsa verkflæðinu.  
5. Á flýtiflipanum **Meðlimir verkflæðishóps** skal fylla út reitina í fyrstu línunni, eins og lýst er í eftirfarandi töflu.  

   |Svæði|Heimildasamstæða|
   |-----|-----------|
   |**Notandanafn**|Tilgreina notandann sem tekur þátt í verkflæði.<br /><br /> Notandi verður að vera til á síðunni **Uppsetning notanda**. Frekari upplýsingar eru í [Úthluta leyfi til notenda og hópa](ui-define-granular-permissions.md).|
   |**Nr. raðar**|Tilgreina í hvaða röð notandi verkflæðis virkjast í verkflæði, út frá öðrum notendum. Þessi reitur gefið upp t.d. hvenær notandi samþykkir í samhengi við aðra samþykktaraðila með því að setja upp valkostinn **Notendahópur verkflæðis** í reitnum **Gerð samþykktaraðila** í tengdu verkflæðissvari.|

   > [!NOTE]
   > Raðnúmer eru yfirleitt í röð notenda í notendaflokki verkflæðis. Hins vegar geta margir notendur haft sama raðnúmer. Þegar svo er þarf aðeins einn af notendunum að samþykkja beiðni áður en verkflæðið fer í næsta skref. Ef notandi A og notandi B eru t.d. bæði númer tvö í röðinni fer verkflæðið á þrep þriðja þrepið þegar annað hvort notandinn A eða notandi B samþykkir beiðnina.
6. Endurtaktu skref 5 til að bæta fleiri notendum verkflæðis við notendahópinn.  

## <a name="see-also"></a>Sjá einnig .

[Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md)  
[Setja upp Verkflæði samþykktar](across-set-up-workflows.md)  
[Nota Samþykktarverkflæði](across-use-workflows.md)  
[Kynning: Uppsetning og notkun á samþykktarverkflæði innkaupa](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Verkflæði](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
