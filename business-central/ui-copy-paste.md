---
title: Afrita og líma gögn
description: Afritaðu reiti og raðir úr Business Central síðum og límdu einhvers staðar annars staðar.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accessibility, shortcuts, keyboarding
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 8c8714bc1f12b6fd4bf68124cf1797bfa89ece6b
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/03/2019
ms.locfileid: "2882255"
---
# <a name="copy-and-paste-faq"></a>Algengar spurningar um að afrita og líma
Þú getur afritað eina eða fleiri raðir (færslur) úr lista eða einum reit á síðu og síðan líma það sem þú afritaðir á sömu síðu, aðra síðu eða ytri skjal (eins og Microsoft Excel og Outlook tölvupóst). Í stuttu máli, til að afrita, ýtirðu á CTRL+C (cmd+C í macOS) á lyklaborðinu þínu. Til að líma er stutt á CTRL+V (cmd+V í macOS).

Það eru nokkrir aðrir flýtilyklar til að afrita og líma sem hjálpa þér að spara tíma þegar þú slærð inn gögn. Nánari upplýsingar um þetta er að finna í [Flýtilykla](keyboard-shortcuts.md#CopyRows).

Þessi grein svarar algengum spurningum sem þú gætir haft um að afrita og líma.  

## <a name="what-can-i-copy-and-paste"></a>Hvað get ég afritað og líma?
- Afritaðu eina eða fleiri raðir í [!INCLUDE[d365fin](includes/d365fin_md.md)] á sama lista eða í hvaða lista sem er með sömu dálka.
- Afritaðu eina eða fleiri raðir í [!INCLUDE[d365fin](includes/d365fin_md.md)] og líma inn í Excel eða önnur forrit.
- Afritaðu eina eða fleiri raðir í Excel og líma inn í [!INCLUDE[d365fin](includes/d365fin_md.md)] lista.
- Afritaðu gildi einstakra reita í [!INCLUDE[d365fin](includes/d365fin_md.md)] og límdu það hvar sem er.

## <a name="does-copy-and-paste-work-with-tiles"></a>Virkar afrit og líma með flísar?
Já, en aðeins fyrir einn valinn reit.

## <a name="how-do-i-copy-a-row"></a>Hvernig afrita ég línu?
Til að afrita eina röð, veldu hana og ýttu á Ctrl+C.

Ef þú vilt afrita fleiri línur, geturðu:
- Ýttu á Ctrl+Smelltu á aðra röð eða ýttu á Shift+Smelltu til að velja röðina og allar raðir á milli. Sjá [Flýtilykla](keyboard-shortcuts.md#CopyRows) fyrir fleiri músar- og lyklaborðs samsetningar til að velja raðir.
- Veldu ![Sýna fleiri valkosti](media/show-more-options-icon.png "Sýna tákn fyrir fleiri valkosti") í fyrsta dálki í röð, veldu **Veldu Meira**, veldu gátreitinn við hliðina á hverri röð sem þú vilt afrita og ýttu síðan á Ctrl+C.

## <a name="how-do-i-paste-rows"></a>Hvernig líma ég raðir?
Veljið auða línu, með bendilinn í hvaða hólfi sem er, og ýtið svo á Crtl+V.

Ef þú vilt skipta um núverandi raðir skaltu velja raðirnar og ýta á Crtl+V. Í þessu tilfelli er aðeins hægt að líma eins mörg raðir og þú valdir.

> [!NOTE]
> Listinn sem verið er að líma í verður að vera breytanlegur.

<!-- Rows are pasted directly where your cursor is located. If you paste into an empty line, any existing subsequent lines will be moved after the pasted lines. If you paste into an existing line or lines, this will be overwritten.-->

## <a name="can-i-paste-rows-into-an-outlook-email"></a>Get ég límt raðir inn í Outlook tölvupóst?
Já. Þetta er límt sem snjallaformað borð sem varðveitir inndrátt, tölulegar stillingar og litun, eins og þú myndir sjá í [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="in-which-lists-can-i-copy-and-paste-rows"></a>Í hvaða listum get ég afritað og líma raðir?
Þú getur afritað raðir í hvers konar lista, þar á meðal vinnublaði, Upplýsingakössum, eða lista sem er innfelldur á síðu (eins og línur sölupöntunar). Hins vegar, til að líma raðir, verður listinn að vera breytanlegur.

Á sumum síðum getur forritshönnunin komið í veg fyrir að þú getir límt raðir. Hafðu samband við stjórnanda þinn eða þróunaraðila forritsins til að breyta [Breytileg eign](/dynamics365/business-central/dev-itpro/developer/properties/devenv-editable-property) á síðunni eða [PasteIsValid eign](/dynamics365/business-central/dev-itpro/developer/properties/devenv-pasteisvalid-property) á upprunatöflunni.

## <a name="on-which-clients-is-copy-and-paste-available"></a>Á hvaða biðlurum er afrit og líma í boði?
Afrita og líma er í boði í vafranum eða [!INCLUDE[d365fin](includes/d365fin_md.md)] forritinu fyrir Windows 10.

## <a name="what-is-the-maximum-number-of-rows-that-can-be-copied"></a>Hver er hámarksfjöldi raða sem hægt er að afrita?
Þú getur afritað eins mörg raðir og þú hefur flett inn í yfirlit. Til að afrita t.d. allar 1000 raðir á síðu verður þú fyrst að fletta neðst á síðuna og bíða eftir að raðirnar birtast áður en þú afritar þær. Hámarksfjöldi raða sem þú getur afritað takmarkast aðeins af minni tækisins.

## <a name="must-i-have-the-exact-same-number-of-columns-when-pasting-rows"></a>Verður ég að hafa nákvæmlega sömu fjölda dálka þegar ég líma raðir?
Já. Hvort sem þú ert að afrita frá [!INCLUDE[d365fin](includes/d365fin_md.md)], frá Excel eða frá einhverjum öðrum töfluuppruna, verða línurnar sem þú límir í [!INCLUDE[d365fin](includes/d365fin_md.md)] að hafa nákvæmlega samsvarandi dálka - hvorki fleiri né færri.

## <a name="why-do-i-get-errors-when-pasting-rows"></a>Af hverju fæ ég villuboð þegar ég líma raðir?
Þegar líma inn í [!INCLUDE[d365fin](includes/d365fin_md.md)] er hver röð skoðuð til að ganga úr skugga um að gildi í hverjum dálki séu gild. Ef dálkur inniheldur gildi sem er ógilt er líming stöðvað og villuboð birtist. Til að forðast þetta skaltu ganga úr skugga um að dálkarnir hafi gild gildi áður en þú límir þá.


## <a name="see-also"></a>Sjá einnig .
[Aðstoðareiginleikar](ui-accessibility.md)  
[Hafist handa](product-get-started.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Algengar spurningar](across-faq.md)  
