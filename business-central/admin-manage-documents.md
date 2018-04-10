---
title: "Meðhöndla, eyða eða þjappa skjöl | Microsoft Docs"
description: "Geyma söguleg gögn eða eyða þeim."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 696100bfbcc987b1d684e7987e7fd43979813282
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="manage-documents"></a>Umsjón með skjölum
Meginhlutverk, t.d. kerfisstjóri, þarf reglulega að sjá um þau gögn sem safnast upp, eyða þeim eða þjappa þau.  

## <a name="delete-documents"></a>Eyða skjölum
Í vissum tilvikum kann að þurfa að eyða reikningsfærðum innkaupapöntunum sem ekki hefur verið eytt. [!INCLUDE[d365fin](includes/d365fin_md.md)] kannar hvort eyddu innkaupapantanirnar hafa verið reikningsfærðar að fullu. Ekki er hægt að eyða pöntunum sem hafa ekki verið fullkomlega reikningsfærðar og mótteknar.  

Vöruskilapöntunum er yfirleitt eytt þegar þær hafa verið reikningsfærðar. Þegar reikningur er bókaður er hann fluttur í gluggann **Bókaður innkaupakreditreikningur**. Ef gátreiturinn **Vöruskilaafhending á kreditreikningi** hefur verið valinn í glugganum **Innkaupagrunnur** er reikningurinn fluttur í gluggann **Bókuð skilaafhending**. Hægt er að eyða skjölunum með því að nota keyrsluna **Eyða reiknf. innk.vöruskilapönt.**. Áður en eytt er, athugar runuvinnslan hvort innkaupaskilapantanirnar séu að fullu afhentar og reikningsfærðar.  

Standandi pöntunum er ekki eytt eftir að allar tengdar innkaupapantanir hafa verið unnar og reikningsfærðar. Hægt er að eyða standandi pöntunum með keyrslunni **Reikningsfærðum standandi innkaupapöntunum eytt**.  

Þjónustupöntunum er yfirleitt eytt sjálfkrafa þegar þær hafa verið reikningsfærðar til fulls. Þegar reikningur er bókaður er samsvarandi færsla stofnuð í glugganum  **Bókaðir þjónustureikningar** . Hægt er að skoða bókaða fylgiskjalið í glugganum **Bókaður þjónustureikningur**.  

Forritið eyðir þjónustupöntun ekki sjálfkrafa ef heildarmagn pöntunarinnar hefur verið bókað í glugganum **Þjónustureikningur** en ekki í þjónustupöntuninni sjálfri. Þá þarf að eyða bókuðum pöntunum sem ekki var búið að eyða. Hægt er að gera það með því að nota keyrsluna **Eyða reikningsfærðum þjónustupöntunum**.  

## <a name="see-also"></a>Sjá einnig  
[Stjórnun](admin-setup-and-administration.md)  

