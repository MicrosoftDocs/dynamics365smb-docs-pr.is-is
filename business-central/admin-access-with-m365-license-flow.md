---
title: Aðgangsflæði notanda fyrir Microsoft 365 leyfi
description: Fáðu yfirlit yfir það sem gerist þegar notandi fær aðgang að gögnum Business Central með því að nota Microsoft 365 leyfið í fyrsta sinn.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 11/03/2022
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
---
# <a name="user-access-flow-for-microsoft--licenses" />Aðgangsflæði notanda fyrir Microsoft 365 leyfi

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Þessi grein lýsir því sem gerist þegar notandi fær aðgang að gögnum Business Central með því að nota Microsoft 365 leyfið í fyrsta sinn. Skilningur á þessu flæði gerir stjórnendum kleift að skipuleggja nálgun sína og stilla Business Central þannig að það passi við viðskiptaþarfirnar.

1. Fyrst er auðkenni notandans sannvottað 
2. Business Central staðfestir að allar [lágmarkskröfur](admin-access-with-m365-license.md#minimum-requirements) séu uppfylltar.
3. Business Central staðfestir að þessi notandi hefur ekki stærra leyfi, eins og Business Centra-leyfi eða stjórnunarhlutverk eins og úthlutað stjórnandahlutverk. 
4. Business Central staðfestir hvort notandinn hafi aðgang að gögnum sem tilheyra umhverfi sem hefur virkjað aðgang með Microsoft 365 leyfum. 
5. Færsla notanda er sett upp í Business Central, þar sem notendahópi, notandasíðu og heimildasamstæðum er úthlutað eins og skilgreint er á grunnstillingarsíðu Microsoft 365 leyfisins. Notendahópi Teams-notenda er sjálfgefið úthlutað, notandasíðu starfsmanns er úthlutað og aðeins heimildasamstæðu innskráningar er úthlutuð. Allar aðrar sjálfgefnar stillingar notenda eru einnig settar á, rétt eins og notandi með Business Central-leyfi. 
6. Heildstætt öryggislíkan Business Central er notað til að ákvarða hvort notandinn eigi að fá aðgang að færslu, síðu í tilteknu fyrirtæki og tilteknu umhverfi. 

Ef öll skref heppnast getur notandinn nú skoðað þessi Business Central-gögn í Teams. Þjónusta Business Central tryggir sjálfkrafa skrifvarinn aðgang og einfaldar notendaviðmótið. 

Notandareikningurinn er nú skráður í Business Central og er hægt að stjórna honum eins og öllum notendum Business Central.

> [!NOTE]
> Skref gætu verið breytileg eftir því hvort hafa verið tilgreindar einhverjar öryggisstillingar í Microsoft 365 eða Business Central.

## <a name="see-also" />Sjá einnig .

[Aðgangur að Business Central með Microsoft 365 leyfum](admin-access-with-m365-license.md#minimum-requirements)  
[Setja upp aðgang með Microsoft 365 leyfum](admin-access-with-m365-license-setup.md)  
