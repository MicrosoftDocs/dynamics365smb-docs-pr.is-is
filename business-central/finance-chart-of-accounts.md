---
title: Að skilja bókhaldslykilinn
description: 'Lýsir bókhaldslyklinum, hvernig hann er settur upp og hvernig hann er notaður.'
author: kennienp
ms.topic: conceptual
ms.search.keywords: 'analysis, history, track'
ms.search.form: '18, 20, 37, 65, 99, 312, 314, 313, 395, 552, 569, 570, 634, 790, 791, 1158'
ms.date: 08/06/2024
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
---

# Að skilja bókhaldslykilinn

Bókhaldslykill (COA) er yfirgripsmikill skráasafn fjárhagsreikninga og samsvarandi tilvísunarnúmer. CoA hefur yfirleitt af tveimur aðalflokkum reikninga:

- Efnahagsreikningar: Þessir reikningar rekja eignir, skuldir fyrirtækisins og nettóvirði.
- Reikningar rekstrarreiknings: Þessir reikningar skrá tekjur frá ýmsum aðilum og rekja einnig kostnað.

Efnahagsreikningum er ennfremur flokkað í þrjá flokka:

1. Eign reikninga: Þessir reikningar rekja alla verðmæta forða í eigu fyrirtækisins.
1. Skuldareikningar: Þeir skrá skuldir fyrirtækisins.
1. Eiginfjárreikningar: Standa fyrir hrakvirði í viðskiptum eftir að skuldir eru dregnar frá eignum.

Tekjureikningum er skipt í tvo flokka:

1. Tekjureikningar: Þessir reikningar safna tekjum fyrirtækisins af ýmsum áttum.
1. Kostnaðarreikningar: Þessir reikningar safna öllum útgjöldum fyrirtækisins.

Nota coA til að skrá færslur í fjárhagur fyrirtækisins. Hver reikningur er yfirleitt með kenni (reikningsnúmer) og lýsandi texta eða haus og eru kerfisbundið kótaðir á grundvelli reikningstegundar þeirra.

[!INCLUDE[prod_short](includes/prod_short.md)] inniheldur staðlaðan bókhaldslykil sem er tilbúin til að styðja þitt fyrirtæki.

Samsetning bókhaldslykils fyrirtækisins er stjórnunarleg ákvörðun sem stjórnandi notar (eða eftir reglugerðum um landið). Það er breytilegt byggt á starfsgreinum fyrirtækisins, viðskiptalíkani og fjármálauppbyggingu. Til dæmis, eftir því hvaða iðnaður er, gæti verið tiltekinn eign reikningar sem eru sérsniðnir að einstökum rekstri og þörfum fyrirtækisins:

* Smásölufyrirtæki gæti lagt áherslu á útistandandi birgðir og kröfur.
* Tæknifyrirtæki gæti einbeitt sér að óáþreifanlegum eignum eins og einkaleyfi og hugbúnaði.
* Framleiðsluverksmiðja myndi rekja eignir og birgðir.

## Síðan Bókhaldslykill

Skýringin á reikningum sýnir allar almennar bókhaldsreikningar. Úr bókhaldslyklinum geturðu gert hluti eins og:  

* Skoða skýrslur sem sýna aðalbókaratriði og jafnvægi.  
* Lokaðu rekstrarreikningi þínum.  
* Opna skal fjárhagur reikningsspjald þar sem hægt er að bæta við eða breyta stillingum.  
* Skoða lista yfir bókunarflokka fyrir þann aðgang.
* Skoða debet- og kreditstöður fyrir einstakan fjárhagsreikning

Þú getur bætt við, breytt eða eytt almennum bókhaldsreikningum. Til að koma í veg fyrir misræmi geturðu þó ekki eytt almennri aðalbókareikning ef gögnin eru notuð í töflureikningi. Einnig er hægt að loka reikningum sem eru óvart lokaðir á viðkvæmum tímabilum. Til að fræðast meira um eyðingu reikninga er farið í [Eyða reikningum](finance-setup-chart-accounts.md#delete-accounts).  

## Stigveldi kóta í fjárhagsreikningum

Fyrirtæki stofna yfirleitt stigveldisbyggingu í fjárhagsreikningskótum til að endurspegla hvar þau tilheyra bókhaldslyklinum. Til dæmis merkir það að fjárhagsreikningskótar sem byrja á **1** tákna eign reikninga, en fjárhagsreikningskótar sem byrja á 3 eiginfjárreikningum eru til dæmis þeir sem byrja á 3 eiginfjárreikningum. Í sumum svæðum eru reglugerðir um notkun staðlaðs bókhaldslykils. Til að hjálpa notendum að skilja þetta stigveldi án þess að þurfa að þekkja uppbyggingu innri kóta er hægt að skilgreina hausa og millisummur í bókhaldslyklinum sem opna þessar innri samsetningar.

## Hönnun bókhaldslykils

Hver lína í bókhaldslyklinum er fjárhagsreikningur einnar af tegundunum:

* Bókun (færslubækur geta bókað línur á þessa reikninga)
* Yfirskrift (skilgreinir yfirskriftina í bókhaldslyklinum)
* Samtals (skilgreinir reiknireglu fyrir millisamtölu í bókhaldslyklinum)
* Frá-tala (skilgreinir upphafshaus millisamtölu í bókhaldslyklinum. Allar línur sem á eftir fylgja þar til til til-tala er inndregin)
* Til-tala (skilgreinir lokahaus millisamtölu og reikniregluna fyrir hana í bókhaldslyklinum. Allar línur sem á eftir fara eftir þessa til-tölu eru dregnar út)

Í lágmarksbókhaldslykli geta aðeins verið línur bókunarreikninga. Hinar fjórar tegundirnar eru notaðar til að skilgreina hvernig bókhaldslykillinn sýnir einnig ársreikninga með hausum og millisamstæðum. Samantektarreikningar eru oft notaðir í fjárhagsskýrslugerð.

> [!TIP]
> Ef aðrar reikningstegundir en **Bókun** í bókhaldslyklinum eru notaðar er hægt að skilgreina mismunandi yfirlit til að sýna "hráa" bókunarreikningana án reikningstegunda skýrslugerðar fyrir samtölur og fyrirsagnir. Til dæmis, Sýna aðeins bókunarreikninga og fela reikninga sem lokað hefur verið á.

## Nota víddir til að einfalda bókhaldslykilinn

Víddir eru gildi sem flokka færslur svo þú getir fylgst með og greint þær í skjölum, t.d. sölupöntunum. Víddir geta til dæmis gefið í skyn verkið eða deildina sem færsla koma frá. Í stað þess að setja upp sérstaka aðalbókarreikninga fyrir hverja deild og verkefni, getur þú notað víddir sem grundvöll fyrir greiningu og forðast að þurfa að stofna flókna bókhaldslykla.

Hægt er að fræðast meira um víddir með því að fara í [Vinna með víddir](finance-dimensions.md).

## Fáðu snöggt yfirlit yfir fjármálin

Á síðu **bókhaldslykla** eru sýndir reikningar í stigveldislista sem býður upp á skjótan aðgang að helstu upplýsingum fyrir hvern reikning. Listinn er hins vegar fastur og ef þú ert með marga reikninga gætirðu þurft að fletta til að skoða mismunandi reikninga. Ef þú vilt aðeins fá fljótlegt yfirlit yfir grunnupplýsingar, t.d. nettóbreytingar og nettóstöður, er síðan **Yfirlit bókhaldslykils** gagnleg leið til þess. Dálkauppsetningin á síðunni er sú sama og á síðunni **Bókhaldslykill** (þó með færri dálkum) þannig að auðvelt er að skilja það. Hægt er að stækka eða fella saman stigveldisstigin. Til að auðvelda að fara á milli síðna er síðan **Yfirlit bókhaldslykils** aðgengileg á síðu **bókhaldslykils**.

## Aðgangur að því að búa til og breyta bókhaldslykli

Í litlu fyrirtæki eins og CRONUS sýnifyrirtækinu geta flestir notendur breytt bókhaldslyklum nema notendur með TEAM MEMBER-leyfi. Stærri fyrirtæki nota þó yfirleitt hlutverk og heimildir til að takmarka breytingaraðgang að bókhaldslyklum. Ef þú ert umsjónarmaður eða hefur hlutverk viðskiptastjóra eða endurskoðanda er hægt að stjórna notendaheimildum til að veita réttindi fólks aðgang að viðkomandi töflum. Nánari upplýsingar eru notaðar til að [fá yfirlit yfir heimildir](ui-define-granular-permissions.md#get-an-overview-of-a-users-permissions) notanda.  


<!-- ## Standard chart of accounts in different regions
Uncomment when we have more examples added to our localization documentation

Some regions have defined standards for the chart of accounts structure you should use in your company. 

Here are some examples of such standards that have been implemented in localized versions of [!INCLUDE[prod_short](includes/prod_short.md)]:

* [Standard chart of accounts in Denmark](localfunctionality/denmark/how-to-set-up-standard-coa.md)
-->

## Bestu venjur bókhaldslykils

Hér eru nokkrar bestu venjur sem notandi gæti íhugað þegar bókhaldslyklar eru þróaðir og viðhaldið:

* Semja bókhaldslykil fyrirtækisins til að styðja við fjárhagsskýrslugerð þarfir stjórnenda til að taka stjórnunarákvarðanir.
* Íhuga skal að byrja einfalt með færri fjárhagsreikningum. Alltaf er hægt að bæta við nákvæmari reikningum ef þörf krefur.
* Skilgreina hausa og millisamtölur í bókhaldslyklinum sem taka saman innri samsetningar í fjárhagsreikningum.
* Nota víddir til að einfaldra bókhaldslykilinn. Ekki hafa sérstaka fjárhagsreikninga fyrir hverja vöru eða deild.
* Bæta við nýjum fjárhagsreikningum eftir því sem þeir koma inn, en fjarlægja reikninga aðeins úr bókhaldslykli við lok tímabils.

## Sjá einnig .

[Setja upp eða breyta bókhaldslykli](finance-setup-chart-accounts.md)    
[Skilja fjárhag](finance-general-ledger.md)  
[Fjármálagreiningar](bi.md)    
[Yfirlit yfir Fjármál](finance.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
