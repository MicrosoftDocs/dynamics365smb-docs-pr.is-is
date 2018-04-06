---
title: "Hvernig á að setja upp notendur verkflæðis | Microsoft Docs"
description: "Áður en hægt er að stofna verkflæði verður að setja upp notendur sem taka þátt í verkflæðum. Þetta þarf nauðsynlega að gera til að geta tilgreint hverjir verða að fá tilkynningu sem bregðast þarf við í verkflæðisskrefi."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reject, delegate, request
ms.date: 08/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 0fe05d44acd7fb163996e8a663adb309d229b203
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-workflow-users"></a>Setja upp notendur verkflæðis
Áður en hægt er að stofna verkflæði verður að setja upp notendur sem taka þátt í verkflæðum. Þetta þarf nauðsynlega að gera til að geta tilgreint hverjir verða að fá tilkynningu sem bregðast þarf við í verkflæðisskrefi.  

Í **Verkflæðinotandahópur** glugganum eru settir upp notendur undir verkflæðisnotandahópi, og tilgreint númer notanda í ferliröð , svo sem samþykkiskeðja.  

Verkflæðisnotendur sem virka sem samþykktarnotendur, bæði samþykkjendur beiðni og samþykkjendur, verða að vera settir upp í **Uppsetning samþykkisnotanda** glugganum. Frekari upplýsingar eru í [Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md).  

> [!NOTE]  
>  Til að skilgreina að samþykktarbeiðni sé ekki samþykkt fyrr en margar samþykkjendur í samþykktarkeðju hafa samþykkt skal setja upp samþykkjendur í stigveldi. Hvað varðar samþykkjendur af gerðinni **Samþykkjandi** skal setja þá upp í glugganum **Uppsetning Samþykkjandi notandi**. Hvað varðar samþykkjendur af gerðinni **Notendaflokkur verkflæðis** skal setja þá upp í glugganum **Notendaflokkar verkflæðis** og skilgreina stigveldið með því að úthluta stighækkandi númerum á hvern samþykkjanda í reitnum **röð nr.**. . Nánari upplýsingar eru í [Setja upp notendur sem samþykkjendur](across-how-to-set-up-approval-users.md) og þessi efnisatriði.  
>   
>  Til að skilgreina að samþykktarbeiðni sé ekki samþykkt fyrr en margar jafn samþykkjendur hafa samþykkt, án tillits til stigveldi, skal setja upp flatan notendahóp verkflæðis. Hvað varðar samþykkjendur af gerðinni **Notendaflokkur verkflæðis** skal setja þá upp í glugganum **Notendaflokkar verkflæðis** og úthluta sama númeri á hvern samþykkjanda í reitnum **Röð nr.**. . Nánari upplýsingar er að finna í þessari grein.  

### <a name="to-set-up-a-workflow-user"></a>Uppsetning verkflæðisnotenda  

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Notandaflokkar Verkflæðis** og velja svo viðeigandi tengil.  
2. Valið er **Nýtt** aðgerð. Glugginn **notendaflokkur verkflæðis** opnast.  
3. Í **Kóði** reitinn skal slá inn að hámarki 20 stafi til að auðkenna verkflæðið.  
4. Í **Lýsing** reitnum skal lýsa verkflæðinu.  
5. Í flýtiflipanum **Aðilar í flokki verkflæðisnotenda** skal fylla inn í reitina í fyrstlu línu eins og lýst er í eftirfarandi töflu.  

    |Svæði|Description|  
    |---------------------------------|---------------------------------------|  
    |**Notandanafn**|Tilgreina notanda sem mun taka þátt í verkflæði.<br /><br /> Notandi verður að vera til í glugganum **Uppsetning notanda**. Frekari upplýsingar eru í [Stjórna notendum og heimildum](ui-how-users-permissions.md).|  
    |**Nr. raðar**|Tilgreina í hvaða röð notandi verkflæðis virkjast í verkflæði, út frá öðrum notendum. Þennan reit er t.d. hægt að nota til að tilgreina hvenær notandi samþykkir í samsvörun við aðra samþykkjendur þegar notaður er valkostur **Notandahópur verkflæðis** í reitnum **Gerð samþykkjanda** á tengdu verkflæðissvari. **Ábending:** Til að skilgreina að samþykktarbeiðni sé ekki samþykkt fyrr en margar jafn samþykkjendur hafa samþykkt, án tillits til stigveldi, skal setja upp flatan notendahóp verkflæðis með því að úthluta sömu númeraröð til viðeigandi samþykkjanda.|  
6. Endurtaka skref 5 til að bæta við fleiri notendum verkflæðis við notendaflokkinn.  
7. Endurtaka skref 2 til 6 til að bæta við fleiri notendaflokkum verkflæðis.  

## <a name="see-also"></a>Sjá einnig  
[Setja upp notendur samþykktar](across-how-to-set-up-approval-users.md)   
[Uppsetning verkflæðis](across-set-up-workflows.md)   
[Nota verkflæði](across-use-workflows.md)   
[Kynning: Uppsetning og notkun verkflæði innkaupasamþykktar](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
[Verkflæði](across-workflow.md)   

