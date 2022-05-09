---
title: Sækja innbót Business Central fyrir Outlook
description: Kynntu þér hvernig á að setja upp innbót Business Central fyrir Outlook fyrir fyrirtækið þitt eða til eigin nota.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Microsoft 365, Outlook
ms.search.form: 1831, 1832
ms.date: 04/27/2022
ms.author: jswymer
ms.openlocfilehash: a2c0754aed38d80fc4a088ab7dccec81cb0141e0
ms.sourcegitcommit: f9143302b8271f5924a027cacdf29dc37c95f4c6
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2022
ms.locfileid: "8654915"
---
# <a name="get-the-business-central-add-in-for-outlook"></a>Sækja innbót Business Central fyrir Outlook

Með [!INCLUDE[prod_short](includes/prod_short.md)] er hægt að stjórna samskiptum fyrirtækisins við viðskiptamenn og lánardrottna beint í Microsoft Outlook. [!INCLUDE[prod_short](includes/prod_short.md)] Með Outlook viðbóunni Sérðu Fjárhagsleg gögn sem tengjast viðskiptavinum og lánardrottnum. Einnig er hægt að búa til og senda fjárhagsleg skjöl, t.d. verðtilboð og reikninga.  

Til eru tvær leiðir til að sækja innbót Business Central fyrir uppsett Outlook en það fer eftir hlutverki þínu í fyrirtækinu:

- Microsoft 365 Sem kerfisstjóri skal nota *miðlæga virkjun* til að setja upp viðbóta sjálfvirkt fyrir allt fyrirtækið, flokkana eða ákveðna notendur.

- Sem hvaða notandi sem er skaltu setja innbótina upp til eigin nota ef stjórnandi þinn hefur þegar innleitt hana fyrir þig.

## <a name="about-the-business-central-add-in-for-outlook"></a>Um innbót Business Central fyrir Outlook

Innbót Business Central fyrir Outlook samanstendur af tveimur minni innbótum:

- Talnagögn tengiliða

    Þessi innbót býður notendum upp á [!INCLUDE[prod_short](includes/prod_short.md)] viðskiptamanna- eða lánardrottnaupplýsingum í tölvupóstum og dagatalsfundum Outlook. Það gerir þér einnig kleift að búa til og senda [!INCLUDE[prod_short](includes/prod_short.md)] viðskiptaskjöl á borð við sölutilboð og reikninga til tengiliðar. <!--To support these task, the add-in adds actions to the Outlook ribbon, in the **Business Central** group. --> 

- Skjalayfirlit

    Þegar tölvupóstur vísar á númer viðskiptaskjals í meginmáli tölvupósts býður þessi innbót upp á beinan tengil í línu úr meginmáli tölvupóstsins í raunverulegt viðskiptaskjal í [!INCLUDE[prod_short](includes/prod_short.md)].

Frekari upplýsingar um það sem gert er við viðbóta er að finna [í notkun Viðskiptaseðla sem fyrirtækið innanborðs í Outlook](work-outlook-addin.md).

Boðið er upp á hverja innbót sem XML-skrá sem kallast *manifest* sem hver sá sem vill þess virkni þarf að setja upp í Outlook. Þessar skrár lýsa því hvernig á að virkja innbæturnar og tengjast Business Central þegar þær eru notaðar í Outlook. Yfirleitt vinnur stjórnandi með þessar skrár. Sem almennur notandi þarft þú í flestum tilfellum ekki að vinna með þessar skrár með beinum hætti. Annaðhvort mun stjórnandinn setja upp innbótina þannig að uppsetningin gerist sjálfkrafa fyrir þig eða þú munt nota innbyggða uppsetningu með hjálp til að fara í gegnum uppsetninguna.

> [!IMPORTANT]
> Að vinna með margfallt umhverfi? Viðskiptamiðað við Outlook er hannað til að vinna með eitt miðlægt umhverfi fyrirtækja. Þegar viðbótin er uppsett er nafn umhverfisins innifalið í farmskrá viðbóta. Þessi Skilgreining þýðir að viðbótin mun aðeins tengjast því umhverfi sem hún var uppsett frá. Til að nota viðbóta við annað umhverfi opnist þú umhverfið og setur upp viðbóta aftur.

## <a name="deploy-the-add-in-by-using-centralized-deployment-as-an-admin"></a>Setja upp innbótina með miðlægri innleiðingu sem stjórnandi

Miðstýrð innleiðing er eiginleiki í Microsoft 365 Stjórnun sem notaður er til að setja sjálfvirkt upp viðbætur í Office apps notenda, líkt og Outlook. Þetta er ráðlagða leiðin fyrir stjórnendur til að setja upp Office-innbætur fyrir notendur og hópa innan fyrirtækisins.

> [!NOTE]
> Fyrir Business Central á staðnum skal skoða [Að setja upp innbót fyrir Outlook-samþættingu við Business Central á staðnum](/dynamics365/business-central/dev-itpro/administration/setting-up-office-add-ins-outlook-inbox) í efni fyrir stjórnendur (eingöngu á ensku).

### <a name="prerequisites"></a>Frumskilyrði

- Í Microsoft 365 áskrift  
- Notendum er úthlutað Microsoft 365 leyfi  
- Microsoft 365 Reikningurinn hefur alþjóðlegan stjórnanda *eða* skipti um *stjórnendahlutverk*

### <a name="deploy-the-add-in"></a>Setja upp innbótina

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") í Business Central. táknið, fara í **Uppsetning með hjálp** og velja síðan viðkomandi tengil.
2. Veldu **Miðlæg innleiðing Outlook-innbótar** til að hefja uppsetningu með hjálp.
3. Farðu yfir fyrstu síðuna og veldu **Næsta** til að opna síðuna til að sækja innbæturnar.
4. Í dálknum **Uppsetning** skal velja gátreitinn fyrir innbæturnar sem á að setja upp, síðan velja **Sækja og halda áfram**.

    Skrá sem heitir *OutlookAddins.zip* er hlaðið niður á tækið þitt.

5. Á þessum tímapunkti er vinnunni sem þarf að gera í Business Central lokið þannig að þú getur valið **Lokið**.

   >[!TIP]
   > Áður en þú velur **Next** skaltu velja **ferðinni Microsoft 365 í (opnast í nýjum glugga)** til að opna og skrá þig inn í Microsoft 365 admin Center í nýjum vafraglugga. Þú verður að fara Microsoft 365 í admin Center í seinna skrefi samt.

6. Farðu í möppuna þar sem OutlookAddins.zip var sótt og dragðu út skrárnar **Contact Insights.xml** og **Document View.xml** úr zip-skránni yfir í möppu að eigin vali.

    Frekari upplýsingar er að finna í [Þjappa og afþjappa skrár](https://support.microsoft.com/en-us/windows/zip-and-unzip-files-8d28fa72-f2f9-712f-67df-f80cf89fd4e5).
7. Skráðu þig inn Microsoft 365 á admin Center, farðu svo í [Integrated apps](https://go.microsoft.com/fwlink/?linkid=2163967).

8. Veldu **Hlaða upp sérsniðnum forritum**.
9. Á síðunni **Hlaða upp forritum til að setja upp** skal velja **Hlaða upp skrá (.xml) úr tækinu** > **Velja skrá**.
10. Veljið eina af þeim viðbótum sem unnar voru fyrr, til dæmis með því **að hafa samband við innsýn. XML**.
11. Fylgdu leiðbeiningunum til að úthluta notendum og setja upp innbótina.
12. Endurtaktu skref 9 til 11 fyrir hina innbótarskrána ef þú vilt.

> [!IMPORTANT]
> Grænt gátmerki birtist þegar innbótin er uppsett í stjórnendamiðstöðinni. Það getur þó liðið allt að sólarhringur áður en notendur sjá innbótina í Outlook-forritinu. Notendur gætu einnig þurft að endurræsa Outlook.

Þegar því er lokið er alltaf hægt að breyta virkjun í Microsoft 365 admin Center eins og að úthluta fleiri notendum. Frekari upplýsingar um viðbótarviðbætur í admin Center [fást í innleiða viðbætur í admin Center](/microsoft-365/admin/manage/centralized-deployment-faq?view=o365-worldwide#how-do-you-target-add-in-user-assignments-with-centralized-deployment-&preserve-view=true).

## <a name="install-the-add-in-for-your-own-use"></a><a name="install"></a>Setja upp innbótina til eigin nota

Ef fyrirtækið þitt leyfir það getur þú sett upp innbót Business Central fyrir eingöngu þig. Ef þú ert ekki viss skaltu hafa samband við stjórnanda.

1. Í Business Central skal fara í ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") færa inn **Sækja Outlook-innbót**, síðan velja viðkomandi tengil.
2. Lestu síðuna og veldu síðan **Næsta**.
3. Ef þú vilt fá kynningartölvupóst frá Business Central með yfirliti um notkun innbótarinnar skaltu kveikja á **Senda dæmi um tölvupóst**.
4. Veldu **Ljúka** til að ljúka uppsetningunni.

Business Central mun tengjast tölvupóstþjóninum þínum og setja upp innbótina í Outlook. Þetta tekur ekki langan tíma. Nú geturðu byrjað að nota innbótina í Outlook.

### <a name="for-business-central-on-premises"></a><a name="onprem"></a>Fyrir Business Central á staðnum

Ef þú notar Business Central á staðnum getur verið að uppsetning innbótarinnar sé aðeins öðruvísi.

1. Í Business Central skal fara í ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") færa inn **Sækja Outlook-innbót**, síðan velja viðkomandi tengil.
2. Lestu síðuna og veldu síðan **Næsta**.
3. Gerðu eitt af eftirfarandi eftir því hvaða síða kemur upp:

    - Ef þú sérð hnappinn **Setja upp í Outlook** skal velja hann og þá er þessu lokið.
    - Ef þú sérð hnappinn **Næsta** skaltu velja hann. Á næstu síðu, ef þú vilt fá kynningartölvupóst frá Business Central með yfirliti um notkun innbótarinnar, skaltu kveikja á **Senda dæmi um tölvupóst**. Veldu svo **Ljúka** og þá er þetta komið.
    - Ef þú sérð hnappinn **Sækja innbót** skaltu velja hann og fara svo í næsta skref.
4. Þegar þú velur **Sækja innbót** er skrá með heitinu *OutlookAddins.zip* sótt á tækið þitt. Þú ættir að sjá skrána efst í vafranum.

   Farðu í möppuna þar sem OutlookAddins.zip var sótt og dragðu út skrárnar **Contact Insights.xml** og **Document View.xml** úr zip-skránni yfir í möppu að eigin vali. Frekari upplýsingar um hvernig á að draga út skrár er að finna í [Þjappa og afþjappa skrár](https://support.microsoft.com/en-us/windows/zip-and-unzip-files-8d28fa72-f2f9-712f-67df-f80cf89fd4e5).

5. Opnaðu Outlook og veldu **Sækja innbætur** úr borðanum. Eða ef þú ert að nota Outlook á vefnum skaltu velja fellivalmyndina í einhverjum nýjum eða fyrirliggjandi tölvupósti, síðan velja **Sækja innbætur**.
6. Veldu **Mínar innbætur** > **Bæta við sérsniðinni innbót** > **Bæta við úr skrá**.
7. Veldu eina af xml-skránum sem þú dróst út, eins og **Contact Insights.xml**, veldu svo **Opna** > **Setja upp**.
8. Endurtaktu skref 6 og 7 fyrir hina xml-skrána ef þú sóttir hana.

Nú geturðu byrjað að nota innbótina í Outlook.

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/alternative-interfaces-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig

[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Sækja Business Central í fartækið mitt](install-mobile-app.md)  
[Senda skjöl í tölvupósti](ui-how-send-documents-email.md)  
[Fjármál](finance.md)  
[Sala](sales-manage-sales.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Lágmarkskröfur fyrir Outlook](product-requirements.md#outlook)  
[Nota viðbætur í Outlook á vefnum](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
