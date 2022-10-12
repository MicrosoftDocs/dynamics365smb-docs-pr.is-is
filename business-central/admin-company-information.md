---
title: Yfirlit yfir Fyrirtækjaupplýsingar
description: Síðan upplýsingar um fyrirtæki tilgreina grunnupplýsingar fyrir rekstrareiningu, s.s. nafn, aðsetur og upplýsingar um sendingu.
author: edupont04
ms.topic: conceptual
ms.search.form: 1
ms.date: 08/31/2022
ms.author: edupont
ms.openlocfilehash: 158a3717de6c3f205a66258fed47d68318592b67
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9607392"
---
# <a name="company-information-overview"></a>Yfirlit yfir Fyrirtækjaupplýsingar

[!INCLUDE[prod_short](includes/prod_short.md)] skipuleggur rekstur fyrirtækja í *fyrirtækjum*. Fyrir hvert fyrirtæki þarf að fylla út í sumar upplýsingar um Grunnfyrirtækið og viðeigandi upplýsingar á **upplýsingasíðu** félagsins. Upplýsingarnar á [**síðunni upplýsingar**](https://businesscentral.dynamics.com/?page=1) um fyrirtæki eru notaðar í fylgiskjölum, svo sem reikningshahausum. Hægt er að setja upp fleiri en eitt fyrirtæki, t.d. móðurfyrirtæki og dótturfyrirtæki.  

Ef birgðavöruhús fyrirtækisins er staðsett á öðru aðsetri en í höfuðstöðvum fyrirtækisins er hægt að fylla út mismunandi sendingarreiti fyrir sendist-til og **birgðageymslukóta** á **flipanum afhendingarfesting**. Upplýsingarnar í þessum reitum eru síðan prentaðar í innkaupapöntunum, til dæmis þannig að Lánardrottnar leggi vörur á réttan stað.  

Fyrir hvert fyrirtæki sem sett er upp þarf að fylla út **síðuna upplýsingar** um félagið ásamt **uppsetningarsíðu** fjárhags. Einnig þarf að setja upp hvert svæði í [!INCLUDE [prod_short](includes/prod_short.md)], svo sem **& uppsetningarsíðu** sölu, fyrir hvert fyrirtæki. Frekari upplýsingar á [Yfirlit yfir verkefni sem setja á upp [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md).  

Á **upplýsingasíðu** fyrirtækisins eru mismunandi reitir og fastflipar, allt eftir þínu landi. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] Eftirfarandi tafla lýsir algengum Festiflipum.

[!INCLUDE [admin-company-info-fasttabs](includes/admin-company-info-fasttabs.md)]

Þegar þú hefur lokið við að fylla út upplýsingarnar getur þú lokað síðunni.  

## <a name="working-with-multiple-companies"></a>Unnið með mörgum fyrirtækjum

[!INCLUDE [prod_short](includes/prod_short.md)] Ef mörg fyrirtæki eru notuð gætu notendur viljað nota *fyrirtækjamerkin* til að auðvelda þeim að finna þau fljótt og fylgjast með því hvaða fyrirtæki þau eru að vinna í. Nánari upplýsingar er að finna [í Display fyrirtækjamerkis](#badge).

Það eru örfáir Eiginleikar sem þú getur notað til að skipta á milli fyrirtækja eftir því hvernig þú vinnur, eins og fyrirtækið skiptir (Ctrl + O). [Frekari upplýsingar er að skipta í annað fyrirtæki eða umhverfi](ui-organization-switch.md).

## <a name="display-a-company-badge"></a><a name="badge"></a> Birta merki fyrirtækis

Þegar það eru fleiri en eitt fyrirtæki eða umhverfi þá Sjáið þið fyrirtækið skipari efst hægra megin á App Bar, nálægt leitartákninu í App Bar. Sjálfgefið er að fyrirtækið rofi noti Staðlað teikn fyrirtækis, eins og ![kynnirinn tákn fyrir fyrirtæki.](media/ui-experience/company-icon.png "Birtir sundurtákn fyrirtækisins sem notað er þegar eitt umhverfi er til staðar") Og ![fyrirtæki teikni-mult-Env](media/ui-experience/company-icon-multi-env.png "Birtir sundurtákn fyrirtækisins sem notað er þegar mörg umhverfi eru til staðar").

:::image type="content" source="media/ui-experience/company-switch-2.png" alt-text="Sýnir tákn fyrirtækisins í fyrirsögn Viðskiptamiðis viðskiptavinar.":::  

Með því **að nota síðuna Fyrirtækjaupplýsingar** er hægt að skipta út stöðluðu teikn fyrirtækisins með sérsniðnum skjölun á grundvelli fyrirtækis ef merki fyrirtækisins gerir auðveldara fyrir notendur að auðkenna fyrirtækið sem það vinnur í.

1. Fyllt er út í reiti eftir því sem við á í flýtiflipanum **Fyrirtækismerki**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
2. Þegar þetta er gert skal endurnýja vafrann (ýta á CTRL + F5) til að uppfæra skjölin í biðlaranum.  

> [!NOTE]
> Fyrirtækið skipari kynnti árið 2022 losun Wave 2, útgáfa 21. Í fyrri útgáfum er merki fyrirtækisins ekki notað við að skipta um fyrirtæki. Það er sýnt efst í hægra horninu á flestum síðum, jafnvel þegar það er aðeins eitt fyrirtæki. Með því að velja það sýnir fullt nafn fyrirtækis og heiti umhverfi.

## <a name="change-company-display-name"></a>Breyta Birtingarheiti fyrirtækis

Heiti fyrirtækisins er alltaf birt efst í vinstra horninu og virkar sem aðgerð sem hægt er að velja til að fara til baka í Mitt hlutverk. Þú getur breytt þessu heiti á síðunni **Upplýsingar um fyrirtækið**.

1. Veldu táknið ![Sprocket til að opna stillingavalmyndina.](media/ui-experience/settings_icon_small.png) táknið og veldu síðan aðgerðina **Upplýsingar um fyrirtæki**.
2. Heiti nýja fyrirtækisins er ritað í reitinn **Heiti**.
3. Fara af síðunni. Kerfið endurræsir og sýnir heitið á nýja fyrirtækinu í horninu efst til vinstri.

## <a name="experience"></a>Upplifun

Sjálfgefin notendaupplifun í [!INCLUDE [prod_short](includes/prod_short.md)] rannsókn gefur ekki leitt til allrar getu. Hægt er að skipta á fullri reynslu á **upplýsingasíðu** fyrirtækisins. Frekari upplýsingar er að finna í [Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md).  

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/create-new-companies-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig .

[Yfirlit yfir verkefni sem setja skal upp[!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Upplýsingar um fyrirtæki Flýtistart](quick-start-company-information.md)  
[Setja upp Fyrirtækjaupplýsingar á Ítalíu](LocalFunctionality/Italy/how-to-set-up-company-information.md)  
[Grunnstillingum breytt](ui-change-basic-settings.md)  
[Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md)  
[Stofna ný fyrirtæki](about-new-company.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
