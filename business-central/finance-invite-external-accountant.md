---
title: "Bæta ytri endurskoðanda við þitt Business Central | Microsoft Docs"
description: "Kynntu þér hvernig hægt er að bjóða ytri endurskoðanda í þitt Business Central."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting
ms.date: 01/14/2019
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 79729b42b660399893aebe1116c80ef3b3209042
ms.openlocfilehash: aff05be6ade45224a57f57c92c2d52fcf9e6eb13
ms.contentlocale: is-is
ms.lasthandoff: 01/15/2019

---
# <a name="inviting-your-external-accountant-to-your-included365finincludesd365finmdmd"></a>Bjóða ytri endurskoðanda í þitt [!INCLUDE[d365fin](includes/d365fin_md.md)]
Ef þú notar ytri endurskoðanda til að hafa umsjón með bókhaldinu og fjárhagsskýrslugerð, geturðu boðið þeim í þitt [!INCLUDE[d365fin](includes/d365fin_md.md)] svo þeir geti unnið með þín fjárhagsgögn.

Þegar endurskoðandi hefur fengið aðgang að þínu [!INCLUDE[d365fin](includes/d365fin_md.md)], getur hann notað **Endurskoðandi** Mitt hlutverk, sem veitir auðveldan aðgang að þeim síðum sem vinna þarf með.  

## <a name="invite-your-accountant-to-your-included365finincludesd365finmdmd"></a>Bjóða ytri endurskoðanda í þitt [!INCLUDE[d365fin](includes/d365fin_md.md)]

Við höfum auðveldað þér að bjóða ytri endurskoðanda. Einfaldlega opnið síðuna **Notendur** og veljið síðan **Bjóða ytri endurskoðanda** aðgerðina í borðanum. Tölvupósturinn er tilbúinn fyrir þig, bættu vinnunetfangi endurskoðandans inn og sendu boðið.  

![Bjóðið endurskoðanda](./media/finance-invite-accountant/invite-accountant.png)

> [!TIP]  
>  SMTP tölvupósts verður að vera uppsettur. Þetta geturðu gert sjálf(ur) eða spurt þinn [!INCLUDE[d365fin](includes/d365fin_md.md)] félaga. Þú verður að vera skráður inn í [!INCLUDE[d365fin](includes/d365fin_md.md)] sem notandi með stjórnunarheimild, ekki sem fyrirtækjaeigandi eða aðrir notendur. Að lokum verður þú að hafa yfirgefið prufufyrirtækið þannig að þú hafir Azure Active Directory stjórnanda.  

> [!IMPORTANT]  
> Netfang endurskoðanda verður að vera vinnunetfang sem er byggt á Azure Active Directory. Ef endurskoðandinn notar aðra gerð netfangs er ekki hægt að sena boðið.  

### <a name="separate-license"></a>Aðskilin leyfi
Endurskoðandanum er bætt við Active Directory leigjanda þinn á bak við tjöldin. Stjórnandi þinn getur staðfest að endurskoðandinn þiggi boðið og að honum sé úthlutað réttri heimild. Liðirnir í þessu ferli fara eftir þeirri tegund aðgangs sem þú notaðir þegar þú skráðir þig í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Þetta efnisatriði byggir á notkun á Office 365 aðgangi, sem notast við Microsoft Azure Active Directory.  

Ef þú hefur virkjað áskrift þína að [!INCLUDE[d365fin](includes/d365fin_md.md)] og notar ekki lengur matsfyrirtækið, ertu komin(n) með Azure Active Directory leigjanda. Stjórnandi eða [!INCLUDE[d365fin](includes/d365fin_md.md)] tengiliður hefur umsjón með þessum leigjanda í [Azure gáttinni](https://portal.azure.com). Hér er nýjum notendum bætt við og leyfi eru gefin og afturkölluð. Frekari upplýsingar, sjá [Microsoft Azure gátt yfirlit](https://docs.microsoft.com/en-us/azure/azure-portal-overview).  

Ein af leyfistegundunum fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] er *Ytri endurskoðandi* leyfið. Þessi leyfistegund er ætluð notendum á borð við ytri endurskoðanda. Þetta þýðir að þú þarft ekki að kaupa auka sæti í núgildandi Active Directory eða nota einn af [!INCLUDE[d365fin](includes/d365fin_md.md)] notandaaðgangi fyrir ytri endurskoðanda. Ef til dæmis núverandi Office 365 áskrift þín er með 10 notendur fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] og þú ert að nota 10 *Fullur notandi* leyfi, getur kerfisstjóri þinn einfaldlega bætt ytri endurskoðanda þínum við sem gestanotanda í Azure gáttinni og úthlutað þessum notanda *Ytri endurskoðandi* leyfi án nokkurs aukakostnaðar. Þú hefur hins vegar aðeins einn notanda með *Ytri endurskoðandi* leyfið. Ef þú vilt bæta við fleiri notendum þarf að uppfæra áskriftina að Office 365 í samræmi við það.  

## <a name="see-also"></a>Sjá einnig
[Fjármál](finance.md)  
[Setja upp tölvupóst handvirkt eða með því að nota Uppsetningu með aðstoð](admin-how-setup-email.md)  
[Upplifun endurskoðanda í Business Central ](finance-accounting.md)  
[Business Central fyrir endurskoðendur á Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants)  

