---
title: Skrá útgjöld og tekjur beint í fjárhag
description: Hægt er að stofna færslur á síðunni Færslubók fyrir viðskiptaaðgerðir sem ekki koma við sögu í skjali.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'direct posting, general ledger'
ms.search.form: '39, 251'
ms.date: 08/06/2024
ms.service: dynamics-365-business-central
---

# <a name="post-transactions-directly-to-the-general-ledger"></a>Bóka færslur beint á fjárhagur

Nota færslubækur til bóka fjárhagsfærslur beint í fjárhagsreikninga og aðra reikninga, svo sem banka-, viðskiptamanna-, lánardrottna- og starfsmannareikninga.  

Dæmigerð notkun færslubókarinnar er að bóka útgjöld starfsmanna við viðskiptaaðgerðir vegna endurgreiðslu. Nánari upplýsingar eru [í Skrá og endurgreiða starfsmannakostnað](finance-how-record-reimburse-employee-expenses.md).

Færslubækur bóka fjárhagsfærslur beint í fjárhagsreikninga og aðra reikninga, svo sem banka-, viðskiptamanna-, lánardrottna- og starfsmannareikninga. Bókun á færslubók stofnar færslur á fjárhagur reikningum. Færslur eru stofnaðar jafnvel þegar færslubókarlína er bókuð á viðskiptamannareikning þar sem færsla er bókuð á fjárhagur útistandandi reikning með bókunarflokki. Hægt er að sérsníða þína útgáfu af færslubók með því að setja upp bókakeyrslu eða sniðmát. Frekari upplýsingar eru í [vinna með almenn færslubók](ui-work-general-journals.md).

Færslur sem bókaðar eru með fylgiskjölum þurfa kreditreikningsferli. Hins vegar er hægt að bakfæra færslur sem bókaðar eru með færslubókinni. Frekari upplýsingar er að finna í [Bakfæra bókanir í færslubók og afturkalla kvittanir/sendingar](finance-how-reverse-journal-posting.md).

## <a name="to-post-a-transaction-directly-to-a-general-ledger-account"></a>Að bóka færslu beint í fjárhagsreikning

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Færslubækur** og velja síðan viðkomandi tengil.
2. Færslubókarkeyrslan er opnuð. Frekari upplýsingar eru í [vinna með almenn færslubók](ui-work-general-journals.md).
3. Fyllið í reitina eftir þörfum í nýrri færslubókarlínu. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. Skref 3 er endurtekið fyrir allar færslur sem á að bóka.

    > [!TIP]  
    > Ef færa á inn margar færslulínur á undan efnahagsreikningslínu, til dæmis fyrir einn bankareikning, skal velja **gátreitinn Leggja til mótupphæð** í línunni fyrir keyrsluna á síðunni **Færslubókarkeyrslur** . Reiturinn **Upphæð** í efnahagsreikningslínunni er sjálfkrafa útfylltur með gildinu sem þarf til að jafna færslurnar.
5. Veljið **Bóka** aðgerðina til að skrá færslurnar á tilteknu fjárhagsreikningana.

## <a name="see-also"></a>Sjá einnig .

[Vinna í færslubókum](ui-work-general-journals.md)    
[Skrá og endurgreiða kostnað starfsmanns](finance-how-record-reimburse-employee-expenses.md)    
[Bakfæra bókanir í færslubók og afturkalla móttökur/afhendingar](finance-how-reverse-journal-posting.md)    
[Fjármál](finance.md)    
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
