---
title: Skýrsluval í Business Central
description: Kynntu þér hvernig á að setja upp skýrslurnar sem þú notar til að prenta ýmsar tegundir skjala í Business Central.
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'setup, reporting'
ms.search.form: '306, 307, 347, 385, 524, 865, 5932, 7401, 7355, 99000917'
ms.date: 06/09/2022
ms.author: bholtorf
---
# <a name="report-selection-for-documents-in-business-central"></a><a name="report-selection-for-documents-in-business-central"></a><a name="report-selection-for-documents-in-business-central"></a>Skýrsluval fyrir skjöl í Business Central

Hægt er að setja upp sjálfgefnar skýrslur til að prenta sölu-, innkaupa- og þjónustuskjöl, t.d. pantanir, verðtilboð og reikninga. Ef til dæmis um er að ræða tiltekið útlit fyrir sölureikninga er hægt að tilgreina þá skýrslu á síðunni **Skýrsluval - Sala** þannig að hún verði notuð til að senda eða prenta sölureikninga.  

## <a name="available-report-selections"></a><a name="available-report-selections"></a><a name="available-report-selections"></a>Skýrsluval í boði

Síðurnar **Skýrsluval** tilgreina hvaða skýrsla verður prentuð við mismunandi aðstæður. [!INCLUDE [prod_short](includes/prod_short.md)] býður upp á sjálfgefnar grunnstillingar, en hægt er að breyta þeim ef þörf krefur. Einnig er hægt að bæta skýrslum við síðurnar **Skýrsluval** ef á að prenta fleiri en eina skýrslu fyrir hverja skjalagerð sem dæmi. 

Eftirfarandi tafla útskýrir hvar hægt er að finna upplýsingar um mismunandi síður.  

|Svæði eða verkefni  |Frekari upplýsingar|
|--------------|----------|
|Dæmi um hvernig skýrsluval virkar (sala)|[Skýrsluval fyrir söluskjöl](#example-report-selection-for-sales-documents) fundust hér að neðan|
|Sjálfgefið útlit fyrir tölvupósta með sölu- og innkaupaskjölum  |[Setja upp endurnýtanlega texta og útlit tölvupósts fyrir sölu- og innkaupaskjöl](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts) |
|Skilgreina útlit ávísana     |[Velja útlit ávísunar](finance-how-define-check-layouts.md) |
|Skilgreina skýrslur fyrir VSK-skýrslu (Þýskaland)|[Setja upp skýrslur fyrir VSK og Intrastat](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md) |

> [!TIP]
> Sem dæmi getur [!INCLUDE [prod_short](includes/prod_short.md)] innihaldið fleiri síður **Skýrsluvals**, en það fer eftir staðsetningu þinni og atvinnugrein. Til að athuga uppsetningu skaltu velja ![Ljósapera sem opnar viðmótsleitina.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Skýrsluval**, velja síðan viðkomandi tengil.

Sjálfgefna útgáfan af [!INCLUDE [prod_short](includes/prod_short.md)] inniheldur eftirfarandi síður **Skýrsluvals**:

* **Skýrsluval - Sala**  
* **Skýrsluval - innkaup**  
* **Skýrsluval - Birgðir**  
* **Skýrsluval - Sjóðstreymi**  
* **Skýrsluval – vöruhús**  
* **Skýrsluval - Bankareikningur**  
* **Skýrsluval – verk**  
* **Skýrsluval - Þjónusta**

## <a name="example-report-selection-for-sales-documents"></a><a name="example-report-selection-for-sales-documents"></a><a name="example-report-selection-for-sales-documents"></a>Dæmi: Skýrsluval fyrir söluskjöl

Síðan **Skýrsluval - Sala** býður upp á sjálfgefnar skýrslur til að nota í mismunandi aðstæðum fyrir hverja skjalagerð sem á við. Veldu gerð skjals í reitnum **Notkun** og bættu síðan við eða farðu yfir skýrsluvalið. Hægt er að setja upp fleiri en eina skýrslu og tilgreina röðina sem á að senda eða prenta skýrslurnar eftir.  

[!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

Þú getur ekki sent allar skjalagerðir sem tölvupóstviðhengi. Fyrir þær sem þú getur inniheldur síðan **Skýrsluval** aukareiti.  

Til dæmis á síðunum **Skýrsluval - Sala** og **Skýrsluval - innkaup** hjálpa eftirfarandi reitir þér við að setja upp tölvupóst:

|Heiti reits |Lýsing  |
|-----------|-------------|
|**Nota fyrir meginmál tölvupósts**| Settu samanteknar upplýsingar eins og reikningsnúmer, gjalddaga eða tengil á greiðsluþjónustu í tölvupóst.        |
|**Nota fyrir tölvupóstsviðhengi**| Hengdu tengda skjalið við tölvupóstinn.|
|**Lýsing á útliti meginmáls tölvupósts**|Tilgreindu útlit á meginmáli tölvupósts sem á að nota. Venjulega er þetta sérsniðið skýrsluútlit. |

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Sjá einnig .

[Setja upp endurnýtanlega texta og útlit tölvupósts](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts)  
[Velja útlit ávísunar](finance-how-define-check-layouts.md)  
[Setja upp skýrslur fyrir VSK og Intrastat (Þýskaland)](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md)  
[Stjórna útliti skýrslna og skjala](ui-manage-report-layouts.md)  
[Skilgreina útlit skjala fyrir viðskiptamenn og lánardrottna](ui-define-customer-vendor-document-layouts.md)  
[Setja upp prentara](ui-specify-printer-selection-reports.md)  
[Fjárhagsskýrslur og greiningar í Business Central](finance-reports.md)  
[Skýrslur og greiningar viðskiptakrafna í Business Central](receivables-reports.md)  
[Skýrslur og greiningar viðskiptaskulda í Business Central](payables-reports.md)  
[Skýrslur og greiningar eigna í Business Central](fa-reports.md)  
[Verkskýrslur og greiningar í Business Central](project-reports.md)  
[Söluskýrslur og greiningar í Business Central](sales-reports.md)  
[Innkaupaskýrslur og greiningar í Business Central](purchase-reports.md)  
[Birgða- og vöruhúsaskýrslur og Analytics í Business Central](inventory-WMS-reports.md)  
[Samsetningarskýrslur og greiningar í Business Central](assembly-reports.md)  
[Framleiðsluskýrslur og greiningar í Business Central](production-reports.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
