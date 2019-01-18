---
title: "Meðhöndla notendur og hlutverk | Microsoft Docs"
description: "Lærið að meðhöndla notendur og Mitt hlutverk í Business Central."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: profiles, users
ms.date: 10/24/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 7ecd8a5ad2b321d4d1683047e70ede90c7ce229f
ms.contentlocale: is-is
ms.lasthandoff: 11/26/2018

---
# <a name="understanding-users-profiles-and-role-centers"></a>Að skilja notendur, forstillingar og Mitt hlutverk

Í [!INCLUDE[d365fin](includes/d365fin_md.md)], eru notendum bætt við af stjórnanda sem gefur einnig notendum aðgang að þeim svæðum [!INCLUDE[d365fin](includes/d365fin_md.md)] sem þeir þurfa í starfi sínu.  

Aðgangur að virkni er stjórnað með *notendahópum* og *notandasíðum*. Sem stjórnandi geturðu bætt við og fjarlægt notendur sem hluta af [!INCLUDE[d365fin](includes/d365fin_md.md)] áskrift þinni og þú getur úthlutað leyfum til notenda í gegnum notendaflokka.  

## <a name="adding-users"></a>Bæta við notendum

Til að bæta við notendum í [!INCLUDE[d365fin](includes/d365fin_md.md)] á netinu, verður stjórnandi Office 365 í fyrirtækinu fyrst að búa til notendur í Office 365 stjórnendamiðstöðinni. Frekari upplýsingar, sjá [Bæta notendum við Office 365 for business](https://aka.ms/CreateOffice365Users).

Síðan getur kerfisstjórinn úthlutað sérhverjum notanda og flokkum notenda leyfi. Frekari upplýsingar eru í [Stjórna notendum og heimildum](ui-how-users-permissions.md).  

Öflugustu heimildir sem notandi getur haft er SUPER-heimildasamstæðan. Hvert fyrirtæki verður að hafa að minnsta kosti einn notanda með þessa heimildasamstæðu, en það er best að gefa hverjum notanda heimildir sem samsvara vinnuþörfum hans í [!INCLUDE[prodshort](includes/prodshort.md)] og ekki meira en það. Þetta hjálpar til við að tryggja að notendur hafi aðeins aðgang að gögnum sem tengjast vinnu þeirra, til dæmis.  

> [!TIP]
> Það er best að ganga úr skugga um að Office 365 stjórnandinn hafi einnig SUPER-heimildasamstæðuna í [!INCLUDE[prodshort](includes/prodshort.md)] vegna þess að það auðveldar mörg stjórnunarverk, þar á meðal að setja upp samþættingu við önnur forrit.

### <a name="users-of-on-premises-deployments"></a>Notendur uppsetningar á staðnum

Fyrir uppsetningu á staðnum fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] getur stjórnandi valið á milli mismunandi auðkenningarbúnaðs skilríkja fyrir notendur. Þegar þú býrð til notanda gefur þú síðan mismunandi upplýsingar eftir því hvaða skilríki þú notar í tilteknu [!INCLUDE[server](includes/server.md)] tilviki. Nánari upplýsingar er að finna í [Gerðir auðkenningar og persónuskilríkja](/dynamics365/business-central/dev-itpro/administration/users-credential-types) í stjórnunarhluta þróunaraðila og ITPro efni fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="profiles"></a>Forstillingar

Fólkið í þínu fyrirtæki sem hefur aðgang að [!INCLUDE[d365fin](includes/d365fin_md.md)] er öllum úthlutað *Forstilling* sem veitir þeim aðgang að *Hlutverkamiðstöð*.

Forstillingar eru söfn [!INCLUDE[d365fin](includes/d365fin_md.md)] notenda sem hafa sömu hlutverkamiðstöð (Mitt hlutverk). Hlutverkamiðstöð er aðgangsstaður og heimasíða fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] sem gefur þér skjótan aðgang að mikilvægustu verkum þínum og birtir ýmsar innsýnir og afkastavísa um vinnu þína.  

> [!NOTE]  
>  Í núverandi útgáfu af [!INCLUDE[d365fin](includes/d365fin_md.md)] á netinu, er ekki hægt að bæta við, breyta eða eyða snið.  

### <a name="CreateProfile"></a>Stofna forstillingu

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Forstillingalisti** og velja svo viðeigandi tengil.  

2.  Á síðunni **Forstillingalisti** skal velja aðgerðina **Nýtt** til að opna síðuna **Nýtt forstillingarspjald**.  

3.  Í reitnum **Kenni forstillingar** færið inn nafn sem lýsir ætluðum hlutverk notenda.  

4.  Í reitinn **Lýsing** er slegin inn lýsing á kenni forstillingar, t.d. **Pantanavinnsla**.  

5.  Stilltu **Kenni fyrir Mitt hlutverk** reitinn á Mitt hlutverk sem þú vilt tengja við forstillinguna.  

Ferlið til þess að breyta fyrirliggjandi forstillingu er hið sama, nema að valin er eldri forstilling á síðunni **Forstillingalisti** í stað þess að velja aðgerðina **Nýtt**.  


### <a name="copy-a-profile"></a>Afrita forstillingu
Afritun forstillingar getur sparað tíma ef nota á sambærilegar stillingar á forstillingu og eingöngu á að breyta nokkrum stillingum.

1.  Opnaðu forstillinguna sem þú vilt afrita og veldu svo **Afrita forstillingu** aðgerðina.

2.  Í reitnum **Nýtt kenni forstillingar** er slegið inn nafn á forstillingunni sem á að afrita.

3.  Stilltu **Nýtt umfang forstillingar** reitinn á eitt af eftirfarandi:

    - **Kerfi** til að gera nýja forstillingu aðgengilega fyrir alla gagnagrunna leigjenda sem nota forritið.
    - **Leigjandi** til að gera nýja forstillingu aðgengilega aðeins fyrir núverandi gagnagrunn leigjenda.
4. Velja hnappinn **Í lagi** að því loknu.

### <a name="ExportImportProfile"></a>Útflutningur og innflutningur forstillinga

Hægt er að flytja forstillingu inn og út sem XML-skrár til og frá [!INCLUDE[d365fin](includes/d365fin_md.md)] gagnagrunninum. Inn- og útflutningur forstillingar getur sparað þér tíma þegar þú stillir notendaviðmótið þar sem þú endurnýjar núverandi uppsetningu stillingar í stað þess að þurfa að stilla forstillingu frá grunni. Ef þú ert með forstillingu sem er stillt í [!INCLUDE[d365fin](includes/d365fin_md.md)] gagnagrunni og vilt endurnýta allar eða nokkrar uppsetningarstillingar í öðrum gagnagrunni getur þú flutt sniðið út í XML-skrá. Þá er hægt að flytja inn XML-skrá forstillingarinnar í hinn gagnagrunninn.

-   Til að flytja út forstillingu er annaðhvort hægt að velja aðgerðina **Flytja út forstillingar** frá síðunni **Forstillingalisti** eða **Forstillingarspjald** eða leita að og opna síðuna **Flytja út forstillingar**. Vistið XML-skrána á stað í tölvu eða á neti.

-   Til að flytja inn forstillingu er annaðhvort hægt að velja aðgerðina **Flytja inn forstillingar** frá síðunni **Forstillingalisti** eða leita að og opna síðuna **Flytja inn forstillingar**. 

    > [!NOTE]  
    >  Ekki er hægt að flytja inn forstillingu sem þegar er til í gagnagrunninum, jafnvel þótt XML-skráin hafi annað heiti eða annað innihald. Eyða verður forstillingumsem fyrir eru áður en hægt er að flytja inn nýju forstillinguna.


## <a name="configuration-and-personalization"></a>Grunnstilling og sérstillingar
<!--The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:  

-   Configuration, performed by the administrator  

-   Personalization, performed by users  

The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.  -->

Notendur sérsníða notendaviðmót sinnar útgáfu með því að sérsníða notendaviðmót undir eigin notandinafni. Stjórnandinn getur eytt þessari aðlögun. Frekari upplýsingar eru í [Sérstilling vinnusvæðisins þíns](ui-personalization-user.md).  

## <a name="see-also"></a>Sjá einnig  
[Vinna með notendur og heimildir](ui-how-users-permissions.md)  
[Stjórnun sérstillinga sem stjórnandi](ui-personalization-manage.md)  
[Sérstillingar verksvæðis](ui-personalization-user.md)  

