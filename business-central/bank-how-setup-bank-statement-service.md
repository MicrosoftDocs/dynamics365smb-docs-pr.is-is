---
title: Setja upp Yodlee bankastreymi
description: Hægt er að umreikna greiðsluupplýsingar í hvaða gagnasnið sem bankinn krefst og opna fyrir inn- og útflutning á bankaskrám.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Yodlee, feed, stream, payment process'
ms.search.form: '1280, 1290'
ms.date: 03/20/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="set-up-the-envestnet-yodlee-bank-feeds-service"></a>Setja upp Envestnet Yodlee bankastraumsþjónustuna

Hægt er að flytja inn rafræn bankayfirlit frá bankanum til að fylla fljótlega út síðuna **Greiðsluafstemmingarbók** þannig að hægt sé að jafna greiðslur og stemma af bankareikninginn. Nánari upplýsingar er að finna í [Jafna greiðslur sjálfkrafa og afstemma bankareikninga](receivables-apply-payments-auto-reconcile-bank-accounts.md).

> [!IMPORTANT]
> Vegna tilskipunar um greiðsluþjónustu í Evrópu (PSD2), eftir 14. september 2019, verður ekki hægt að flytja sjálfkrafa bankayfirlit frá bönkum í Bretlandi inn í [!INCLUDE[prod_short](includes/prod_short.md)]. Við bjóðum hugsanlega upp á þennan eiginleika aftur í framtíðinni.

> [!NOTE]
> Envestnet Yodlee Bank Feeds þjónustan er aðeins studd í netútgáfunni af Business Central. Þessi virkni er ekki studd fyrir útgáfur innanhúss af [!INCLUDE [prod_short](includes/prod_short.md)] eða fyrir [!INCLUDE [prod_short](includes/prod_short.md)] umhverfi sem hýst er í forritaþjónustu í Embed ISV. Ef nota á þessa aðgerð innanhúss þarf að fá samþættan reikning frá Envestnet og bæta þarf kóta við til að samþætta Yodlee API.
>
> Envestnet Yodlee Bank Feeds Þjónustan er aðeins studd í Bandaríkjunum og Kanada.
> Aðeins eru studdir bönkum sem búa í þessum löndum/svæðum þó að bankar frá öðrum löndum/svæðum kunni að birtast í Envestnet Yodlee Bank Feeds bankavalsglugganum í [!INCLUDE[prod_short](includes/prod_short.md)].

> [!IMPORTANT]
> Fyrir tæknilega aðstoð vegna virkni Envestnet Yodlee, hafðu samband við Microsoft Support. Ekki hafa samband við Envestnet Yodlee. Frekari upplýsingar eru í [Grunnstilling tæknilegrar aðstoðar Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/technical-support).

Þjónustan Envestnet Yodlee Bank Feeds er sett upp sem viðbót við [!INCLUDE[prod_short](includes/prod_short.md)] netið og er tilbúin til virkjunar í studdum löndum/svæðum. Frekari upplýsingar skoða [Sérstilla [!INCLUDE[prod_short](includes/prod_short.md)] Nota viðbætur](ui-extensions.md).

Þegar búið að virkja bankastreymisþjónustu, verður að tengja bankareikning við netbankareikning sem streymið kemur úr. Þú býrð til tengla frá bankareikningum í netbankareikninga í mismunandi eftirfarandi aðstæður:

* Bankareikningur er ekki til í [!INCLUDE[prod_short](includes/prod_short.md)] netbankareikningnum. Því er stofnarðu bankareikning með því að búa til tengil úr netbankareikningi.
* Bankareikningur er til staðar í [!INCLUDE[prod_short](includes/prod_short.md)], sem þú vilt tengja við netbankareikning.
* Tengdar bankareikning þarf að aftengja af því þú vilt hætta að nota bankastreymisþjónustuna fyrir reikninginn..
* Netbankareikningar hafa breyst og þú vilt uppfæra upplýsingarnar um bankareikninga í [!INCLUDE[prod_short](includes/prod_short.md)].

Þegar þjónusta bankastraums er virk má setja upp bankareikning til að flytja ný bankayfirlit sjálfkrafa inn á síðuna **Greiðsluafstemmingarbók** á tveggja tíma fresti. Færslur fyrir greiðslur sem þegar hafa verið bókaðar sem jafnaðar og/eða afstemmdar á síðunni **Greiðsluafstemmingarbók verða ekki fluttar** inn. Sjá frekari upplýsingar í “Til að virkja sjálfvirkan innflutning bankayfirlits” hlutann.

> [!NOTE]  
> Ef þú notar uppsetningarleiðbeiningar með hjálp í Setja upp fyrirtæki, þá geta sum skrefin í ferlunum sem fylgja þar á eftir gerst sjálfvirkt þegar þú ert kominn í uppsetninguna fyrir bankareikning fyrirtækis. Nánari upplýsingar er að finna á [Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md).

## <a name="to-enable-the-bank-feed-service"></a>Til að virkja bankastreymisþjónustu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bankareikningar** og velja síðan viðkomandi tengil.
2. Opnaðu bankareikninginn sem þú munt nota fyrir bankastraumsþjónustuna.
3. Á síðunni **Bankareikningsspjald** í reitnum **Innflutningssnið** bankayfirlits er YODLEEBANKFEED valið.  

Bankastraumsþjónustan er virk þegar bankareikningur er tengdur við tengdan netbankareikning. Sjá næsta ferli..  

> [!NOTE]
> Ef þú notar uppsetningarleiðbeiningarnar **Uppsetning fyrirtækis** með hjálp, virkjar þú þjónustuna með því að velja gátreitinn **Nota bankastreymisþjónustu**. Frekari upplýsingar eru í [Stofna ný fyrirtæki í Business Central](about-new-company.md).

## <a name="to-create-a-new-linked-bank-account"></a>Stofna nýjan tengdan bankareikning

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bankareikningar** og velja síðan viðkomandi tengil.
2. Valinn er viðeigandi bankareikningur og síðan valið **stofna nýjan tengdan bankareikning**. **Stofnun tengla fyrir Bankareiknings** síðan opnast eftir smá stund.

    > [!NOTE]  
    > Þessi síða sýnir raunverulega vefsíðu fyrir Envestnet Yodlee Bank Feeds þjónustuna. Hugtök og virkni á síðunni mega ekki vera þau sömu og í þessu efnisatriði.  
3. Á síðunni **Stofnun tengla fyrir netbankareikninga** á flipanum **Tengja Reikning** skal nota leitaraðgerðina til að finna banka þar sem þú ert með einn eða fleiri netbankareikninga.
4. Veljið nafn banka. **Skrá inn** svæðinu opnast.
5. Færa skal inn notandanafn og aðgangsorð sem notað er til að skrá sig inn í netbanka og velja svo hnappinn **Áfram** .  
6. Bankastreymisþjónusta undirbýr að tengja fyrsta netbankareikning á tilgreindum banka í nýja bankareikninginn í [!INCLUDE[prod_short](includes/prod_short.md)].

    > [!NOTE]  
    > Ef þú ert með fleiri en einn netbankareikning í bankanum, verður að stofna fleiri bankareikninga í [!INCLUDE[prod_short](includes/prod_short.md)] fyrir þá. Sjá skref 8 til 10.  

    Þegar vinnslunni er lokið, birtist bankaheitið í **Mínir reikningar** svæðinu á **Tengt** flipanum. Númerið í svigunum gefur til kynna hversu margir netbankareikningar voru tengdir.  
7. Velja hnappinn **Í lagi**.

    Ef aðeins einn netbankareikningur **er tengdur opnast síðan Bankareikningsspjald** og birtir nafn netbankareikningsins. Í þessu tilfelli er tenging bankareiknings lokið. Allt sem er eftir er að setja upp bankareikninginn. Nánari upplýsingar um það eru í [Setja upp bankareikninga](bank-how-setup-bank-accounts.md).

    Ef fleiri en einn netbankareikningar **eru tengdir opnast síðan Tenging** bankareikninga og birtir lista yfir netbankareikninga sem ekki hafa enn verið tengdir bankareikningum í [!INCLUDE[prod_short](includes/prod_short.md)]. Í því tilviki, fylgið næsta skrefi.  
8. Á síðunni **Stofnun tengla fyrir bankareikning** skal velja línuna fyrir netbankareikning, og velja síðan **tengja í Nýr Bankareikningur** aðgerð.  

    Síðan **Bankareikningsspjald** fyrir nýjan bankareikning opnast og sýnir nafn netbankareikningsins.

    Ef bankareikningur er til í [!INCLUDE[prod_short](includes/prod_short.md)] sem á að tengja annan netbankareikning við, skal fylgja næsta skrefi.  
9. Á síðunni **Stofnun tengla fyrir bankareikning** skal velja línuna fyrir netbankareikning, og velja síðan **tengja í fyrirliggjandi Bankareikningur** aðgerð.
10. Á síðunni **Listi yfir bankareikninga** er valinn bankareikningur sem á að tengja við og smellt á **Í lagi**.

## <a name="to-link-a-bank-account-to-an-online-bank-account"></a>Til að tengja bankareikning í netbankareikning

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bankareikningar** og velja síðan viðkomandi tengil.
2. Velja skal línuna fyrir bankareikning sem ekki er tengdur netbankareikningi og velja svo aðgerðina **Tengja við netbankareikning** . Síðan **Stofnun tengla fyrir netbankareikning** opnast með heiti bankans sem var forútfylltur í svæðinu **Tengja reikning**.
3. Veljið nafn banka. **Skrá inn** svæðinu opnast.
4. Færa skal inn notandanafn og aðgangsorð sem notað er til að skrá sig inn í netbanka og velja svo hnappinn **Áfram** .  

    Bankastreymisþjónusta undirbýr að tengja bankareikning í [!INCLUDE[prod_short](includes/prod_short.md)] við viðkomandi netbankareikning.  

    Þegar vinnslunni er lokið á árangursríkan hátt, birtist bankaheiti á **Mínar Reikninga** svæðinu í á **Tengt** flipanum. Ef bankinn er með fleiri en einn bankareikning, er aðeins bankareikningurinn sem þú valdir í skrefi 2 tengdur.  
5. Velja hnappinn **Í lagi**.

Á síðunni **Bankareikningayfirlit** er valinn **tengt** gátreiturinn .

## <a name="to-edit-the-credentials-for-an-online-bank-account"></a>Að breyta innskráningarupplýsingum fyrir netbankareikning

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Bankareikningar** og veldu síðan tengda tengilinn.  
2. Veldu línuna fyrir bankareikning sem er tengdur við netbankareikning og veldu síðan aðgerðina **Breyta upplýsingum netbankareiknings**.
3. Uppfærið skilríki.

## <a name="to-unlink-a-bank-account"></a>Að Aftengja bankareikningi

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bankareikningar** og velja síðan viðkomandi tengil.  
2. Velja línuna fyrir tengdar bankareikning sem á að aftengja frá sínum tengda netbankareikningi, og velja síðan **aftengja frá netbankareikning** aðgerð.

> [!NOTE]  
> Ef þú velur **Já** í staðfestingarglugganum, er tengillinn í netbankareikninginn fjarlægður, og innskráningarupplýsingar eru þurrkaðar út. Til að tengja bankareikning við netbankareikning aftur verðurðu að skrá þig inn í bankann aftur. Nánari upplýsingar er að finna í “Til að tengja bankareikning í netbankareikning“ hlutanum.

## <a name="to-update-bank-account-linking"></a>Uppfæra tengla bankareikninga

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bankareikningar** og velja síðan viðkomandi tengil.
2. Valinn er viðeigandi bankareikningur og síðan valið **uppfæra tengla bankareiknings** aðgerðina.

Ef vandamál eru til staðar fyrir tengdu bankareikninga á síðunni **Bankareikningayfirlit** opnast **Stofnun tengla fyrir bankareikninga** og tilgreinir hvaða bankareikningar hafa verið vandamál. Vandamál má besta leyst með því að aftengja netbankareikninginn og síðan endurstofna tengilinn. Nánari upplýsingar er að finna í “Til að tengja bankareikning í netbankareikning“ hlutanum.

## <a name="to-enable-automatic-import-of-bank-statements"></a>Til að virkja sjálfvirkan innflutning bankayfirlits

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bankareikningar** og velja síðan viðkomandi tengil.
2. Veldu línuna fyrir tengdu bankareikningur og síðan valið **uppsetning sjálfvirks innflutnings bankayfirlits** aðgerð.
3. Á síðunni **uppsetning sjálfvirks innflutnings bankayfirlits** glugga í á **Fjöldi daga innifalið** reitnum, er tilgreint hversu langt aftur í tíma á að fá nýjar bankafærslur fyrir.

    > [!NOTE]  
    > Mælt er með því að setja þetta gildi á 7 daga eða fleiri.  
4. Veldu **virkjað** gátreitinn.  

Á hverri klukkustund mun síðan **Greiðsluafstemmingarbók** sýna nýjar greiðslur sem eru framkvæmdar á netbankareikningi.

> [!NOTE]  
> Færslur fyrir greiðslur sem þegar hafa verið bókaðar sem jöfnuð og/eða stemmt af á síðunni **Greiðsluafstemmingarbók** verða ekki fluttar inn.

## <a name="see-also"></a>Sjá einnig .

[Uppsetning bankaþjónustu](bank-setup-banking.md)  
[Afstemming bankareikninga](bank-manage-bank-accounts.md)  
[Jafna greiðslur sjálfkrafa og afstemma bankareikninga](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Sérstilling [!INCLUDE[prod_short](includes/prod_short.md)] með viðbótum](ui-extensions.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
