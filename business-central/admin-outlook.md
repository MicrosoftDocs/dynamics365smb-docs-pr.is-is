---
title: Sækja innbót Business Central fyrir Outlook
description: Kynntu þér hvernig á að setja upp innbót Business Central fyrir Outlook fyrir fyrirtækið þitt eða til eigin nota.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'SMTP, mail, Microsoft 365, Outlook'
ms.search.form: '1831, 1832'
ms.date: 06/14/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---
# Sækja Business Central innbót fyrir Outlook

Með [!INCLUDE[prod_short](includes/prod_short.md)] er hægt að stjórna samskiptum fyrirtækisins við viðskiptamenn og lánardrottna beint í Microsoft Outlook. Með [!INCLUDE[prod_short](includes/prod_short.md)] Outlook-innbótinni sérðu fjárhagsgögn sem tengjast viðskiptamönnum og lánardrottnum. Einnig er hægt að búa til og senda fjárhagsleg skjöl, t.d. verðtilboð og reikninga.  

Til eru tvær leiðir til að sækja innbót Business Central fyrir uppsett Outlook en það fer eftir hlutverki þínu í fyrirtækinu:

- Sem stjórnandi Microsoft 365 skal nota *Miðlæga innleiðingu* til að setja upp innbótina sjálfkrafa fyrir allt fyrirtækið, hópa eða tiltekna notendur.

- Sem hvaða notandi sem er skaltu setja innbótina upp til eigin nota ef stjórnandi þinn hefur þegar innleitt hana fyrir þig.

## Um innbót Business Central fyrir Outlook

Innbót Business Central fyrir Outlook samanstendur af tveimur minni innbótum:

- Talnagögn tengiliða

    Þessi innbót býður notendum upp á [!INCLUDE[prod_short](includes/prod_short.md)] viðskiptamanna- eða lánardrottnaupplýsingum í tölvupóstum og dagatalsfundum Outlook. Það gerir þér einnig kleift að búa til og senda [!INCLUDE[prod_short](includes/prod_short.md)] viðskiptaskjöl á borð við sölutilboð og reikninga til tengiliðar. <!--To support these task, the add-in adds actions to the Outlook ribbon, in the **Business Central** group. --> 

- Skjalayfirlit

    Þegar tölvupóstur vísar á númer viðskiptaskjals í meginmáli tölvupósts býður þessi innbót upp á beinan tengil í línu úr meginmáli tölvupóstsins í raunverulegt viðskiptaskjal í [!INCLUDE[prod_short](includes/prod_short.md)].

Frekar upplýsingar um hvað gert er við innbótina er að finna í [Nota Business Central sem fyrirtækjainnhólf í Outlook](work-outlook-addin.md).

Boðið er upp á hverja innbót sem XML-skrá sem kallast *manifest* sem hver sá sem vill þess virkni þarf að setja upp í Outlook. Þessar skrár lýsa því hvernig á að virkja innbæturnar og tengjast Business Central þegar þær eru notaðar í Outlook. Yfirleitt vinnur stjórnandi með þessar skrár. Sem almennur notandi þarft þú í flestum tilfellum ekki að vinna með þessar skrár með beinum hætti. Annaðhvort mun stjórnandinn setja upp innbótina þannig að uppsetningin gerist sjálfkrafa fyrir þig eða þú munt nota innbyggða uppsetningu með hjálp til að fara í gegnum uppsetninguna.

> [!IMPORTANT]
> Unnið með mörg umhverfi? Business Central-innbótin fyrir Outlook er hönnuð til að vinna með eitt Business Central-umhverfi. Þegar innbótin er sett upp er heiti umhverfisins haft með í skrá innbótarinnar. Þessi grunnstilling þýðir að innbótin mun aðeins tengjast við umhverfið þar sem hún var sett upp. Til að nota innbótina með öðru umhverfi opnarðu umhverfið og setur innbótina upp aftur.

## Setja upp innbótina með miðlægri innleiðingu sem stjórnandi

Miðlæg innleiðing er eiginleiki í Microsoft 365 stjórnendamiðstöð sem þú notar til setja sjálfkrafa upp innbætur í Office-forritum notanda eins og Outlook. Þetta er ráðlagða leiðin fyrir stjórnendur til að setja upp Office-innbætur fyrir notendur og hópa innan fyrirtækisins.

> [!NOTE]
> Fyrir Business Central á staðnum skal skoða [Að setja upp innbót fyrir Outlook-samþættingu við Business Central á staðnum](/dynamics365/business-central/dev-itpro/administration/setting-up-office-add-ins-outlook-inbox) í efni fyrir stjórnendur (eingöngu á ensku).

### Frumskilyrði

- Microsoft 365 áskrift  
- Notendur fá úthlutað Microsoft 365 leyfi  
- Reikningurinn hefur Microsoft 365 að minnsta kosti hlutverkið [Exchange Administrator](/entra/identity/role-based-access-control/permissions-reference#exchange-administrator] hlutverk

### Setja upp innbótina

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") í Business Central. táknið, fara í **Uppsetning með hjálp** og velja síðan viðkomandi tengil.
1. Veldu **Miðlæg innleiðing Outlook-innbótar** til að hefja uppsetningu með hjálp.
1. Farðu yfir fyrstu síðuna og veldu **Næsta** til að opna síðuna til að sækja innbæturnar.
1. Í dálknum **Uppsetning** skal velja gátreitinn fyrir innbæturnar sem á að setja upp, síðan velja **Sækja og halda áfram**.

    Skrá sem heitir *OutlookAddins.zip* er hlaðið niður á tækið þitt.

1. Á þessum tímapunkti er vinnunni sem þarf að gera í Business Central lokið þannig að þú getur valið **Lokið**.

   >[!TIP]
   > Áður en þú velur **Næsta** skaltu velja tengilinn **Opna Microsoft 365 (opnast í nýjum glugga)** til að opna og skrá þig inn í stjórnendamiðstöð Microsoft 365 í nýjum vafraglugga. Þú verður hvort sem er að fara í stjórnendamiðstöð Microsoft 365 síðar.

1. Farðu í möppuna þar sem OutlookAddins.zip var sótt og dragðu út skrárnar **Contact Insights.xml** og **Document View.xml** úr zip-skránni yfir í möppu að eigin vali.

    Frekari upplýsingar er að finna í [Þjappa og afþjappa skrár](https://support.microsoft.com/en-us/windows/zip-and-unzip-files-8d28fa72-f2f9-712f-67df-f80cf89fd4e5).
1. Skráðu þig inn í stjórnendamiðstöð Microsoft 365 og farðu svo í [Samþætt forrit](https://go.microsoft.com/fwlink/?linkid=2163967).

1. Veldu **Hlaða upp sérsniðnum forritum**.
1.  **Á upphleðsluforritunum til að virkja** síðuna skal stilla **App gerð á**  **Office Innbót**.
1. Velja skal **Upphleðsluskrá (.xml) úr Tæki** > **Velja skrá**.
1. Velja skal eina af innbótarskránum **Samhengi Insights.xml** eða **Documents.xml** sem dregnar voru út á undan.
1. Fylgdu leiðbeiningunum til að úthluta notendum og setja upp innbótina.
1. Endurtaktu skref 9 til 11 fyrir hina innbótarskrána ef þú vilt.

> [!IMPORTANT]
> Grænt gátmerki birtist þegar innbótin er uppsett í stjórnendamiðstöðinni. Það getur þó liðið allt að sólarhringur áður en notendur sjá innbótina í Outlook-forritinu. Notendur gætu einnig þurft að endurræsa Outlook.

Þegar því er lokið er alltaf hægt að breyta uppsetningunni í stjórnendamiðstöð Microsoft 365 á borð við að úthluta fleiri notendum. Frekari upplýsingar um uppsetningu innbóta í stjórnendamiðstöðinni er að finna í [Setja upp innbætur í stjórnendamiðstöðinni](/microsoft-365/admin/manage/centralized-deployment-faq?view=o365-worldwide#how-do-you-target-add-in-user-assignments-with-centralized-deployment-&preserve-view=true).

## <a name="install"></a>Setja upp innbótina til eigin nota

Ef fyrirtækið þitt leyfir það getur þú sett upp innbót Business Central fyrir eingöngu þig. Ef þú ert ekki viss skaltu hafa samband við stjórnanda.

1. Í Business Central skal fara í ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") færa inn **Sækja Outlook-innbót**, síðan velja viðkomandi tengil.
2. Lestu síðuna og veldu síðan **Næsta**.
3. Ef þú vilt fá kynningartölvupóst frá Business Central með yfirliti um notkun innbótarinnar skaltu kveikja á **Senda dæmi um tölvupóst**.
4. Veldu **Ljúka** til að ljúka uppsetningunni.

Business Central mun tengjast tölvupóstþjóninum þínum og setja upp innbótina í Outlook. Þetta tekur ekki langan tíma. Nú geturðu byrjað að nota innbótina í Outlook.

### <a name="onprem"></a>Fyrir Business Central á staðnum

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

## Sjá einnig .

[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Sækja Business Central í fartækið mitt](install-mobile-app.md)  
[Senda skjöl í tölvupósti](ui-how-send-documents-email.md)  
[Fjármál](finance.md)  
[Sala](sales-manage-sales.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Lágmarkskröfur fyrir Outlook](product-requirements.md#outlook)  
[Nota innbætur í Outlook á vefnum](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
