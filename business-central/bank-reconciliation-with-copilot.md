---
title: Stemma af bankareikninga við Afrita (forútgáfa)
description: Læra að nota Copilot til að stemma af bankareikninga í Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.collection:
  - get-started
  - bap-ai-copilot
ms.date: 06/13/2024
ms.custom: bap-template
---

# Stemma af bankareikninga við Afrita (forútgáfa)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Þessi grein útskýrir hvernig afstemming bankareikninga aðstoðar við afstemmingu bankafærslna og fjárhagsfærslna í Microsoft Dynamics 365 Business Central.

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## Aðstoð við afstemmingu bankareikninga

Aðstoð við afstemmingu bankareikninga er safn eiginleikanna Ónýtir eiginleikar sem hjálpa til við afstemmingu bankareikninga. Það býður upp á tvö aðgreind verk í gegnum Copilot:

- Bætt samsvörun færslna með fjárhagsfærslum

    Eins og kunnugt **er samsvörun sjálfkrafa** á síðunni **Afstemming** bankareikninga samsvarar sjálfkrafa flestum bankafærslum og fjárhagsfærslum. Við vísar í þessa aðgerð sem *sjálfvirka vinnsluaðgerð*. Þótt sjálfvirkni virkar vel geta reiknireglurnar sem hún notar stundum leitt til margra ósamræmdra færslna. Copilot notar AI-tækni til að skoða þessar ósamræmdu færslur og auðkenna fleiri samsvörun, byggt á dagsetningum, upphæðum og lýsingum. Ef viðskiptamaður greiddi til dæmis marga reikninga í einni moldarsamtölu stemmir Copilot af eina bankayfirlitslínu við margar reikningsfærslur.

    [Fræðast meira um þetta verk](#reconcile-bank-accounts-with-copilot).

- Tillögur um reikninga fjárhagur (fjárhags)

    Afrita ber færslulýsinguna saman við fjárhagsreikningsheitin og leggur síðan til líklegasta fjárhagsreikninginn sem bóka skal á fyrir afgöngum bankafærslna sem ekki er hægt að para við færslur. Til dæmis ef ósamræmdar færslur hafa frásagnareldsneyti Stöðvun *24* gæti Copilot lagt til að þær séu bókaðar á *flutningsreikninginn* .

    [Fræðast meira um þetta verk](#post-unmatched-bank-transaction-amounts-to-suggested-gl-accounts).

## Tiltæk tungumál

[!INCLUDE[bank-recon-assist-language-support](includes/bank-recon-assist-language-support.md)]

## Frumskilyrði

- Aðstoð við afstemmingu bankareikninga er gerð virk. Stjórnandi verður að ljúka þessu verki. [Fá nánari upplýsingar um hvernig á að stilla Copilot og AI getu](enable-ai.md).
- Bankareikningarnir í Business Central sem á að stemma af eru tengdir netbankareikningi eða þeir eru settir upp með innflutningssniði bankayfirlits.
- Þú kannast við afstemmingu bankareikninga í Business Central, eins og lýst er í [afstemmingu bankareikninga](bank-how-reconcile-bank-accounts-separately.md).

## Stemma af bankareikninga við Afrita

<!-- Similar to the **Match Automatically** capability on the **Bank Acc. Reconciliation** page, Bank account reconciliation assist can also automatically matches transactions in banks statements with bank entries. The difference is that **Match Automatically** uses a native rules-based algorithm, while Bank account reconciliation assist is based AI technology though Copilot. Bank account reconciliation assist is intended to supplement the **Match Automatically** capability. While **Match Automatically** is fairly successful at matching transactions, there are some instances where it can't&mdash;which is where Bank account reconciliation assist comes. By using the **Reconcile with Copilot** action on **Bank Acc. Reconciliation** page, you can find even more matches.-->

Stjórntæki í afstemmingu bankareiknings er ætlað að bæta sjálfvirkri vinnsluaðgerð við sjálfvirka vinnslu. Þess vegna keyrir sjálfvirka samsvörunin þegar Copilot er notað fyrst til að gera fyrstu samsvörunina. Þá keyrir Copilot til að reyna að passa við færslur sem sjálfvirka aðgerðin réð ekki við.

Hægt er að nota tvær aðferðir til að stemma af bankareikninga við Copilot:

- Nota Copilot til að hefja nýja afstemmingu á bankareikningi, beint af **listanum Afstemmingar bankareikninga** .
- Nota Afrita í nýrri eða eldri afstemmingu á afstemmingarspjaldi **bankareiknings** .

# [Úr listanum Afstemming bankareikninga](#tab/fromlist)

Með þessari aðferð má stofna og stemma af nýja afstemmingu bankareikninga frá grunni. Þessi nálgun krefst þess að bankareikningur sé valinn. Ef bankareikningurinn er ekki tengdur netreikningi þarf einnig að flytja inn bankayfirlitsskrána.

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teikn, færa inn **afstemmingar bankareikninga** og velja síðan viðeigandi tengja.
1. Valið er **Afstemming við stjórnborð** til að opna **gluggann Stemma af og stjórnborð** .
1. Stilla skal reitinn **Framkvæma afstemmingu fyrir þennan bankareikning** á bankareikninginn sem á að stemma af.

    ![Skjámynd sem sýnir gluggann Stemma af við Copilot til að stemma af frá grunni.](media/reconcile-bank-accounts-new-copilot.svg)

1. Ef valinn bankareikningur er ekki tengdur netbankareikningi verður að flytja inn bankayfirlitsskrána. Til að flytja skrána inn skal velja gildið í reitnum **Nota færslugögn úr** reitnum eða velja hnappinn Mynda pappír næst hnappnum **Mynda** . Síðan skal nota **Velja skrá til að flytja inn til að flytja** inn bankayfirlitsskrána með því annað hvort að draga hana úr tækinu eða vafra um tækið.
1. Til að stemma af við Copilot er Mynda **valið**.

    Copilot byrjar að búa til eldsnið sem lagt er til. Þegar því er lokið **sýnir glugginn Afstemming við Copilot** niðurstöður samsvarandi vinnslu.

1. Skoða eldsnið sem lagt er til eins og lýst er í næsta hluta.

# [Afstemmingarspjald bankareiknings afstemmingar](#tab/fromcard)

Nota má Copilot annaðhvort með nýrri afstemmingu bankareikninga sem búin er til handvirkt eða með því að breyta fyrirliggjandi afstemmingu.

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teikn, færa inn **afstemmingar bankareikninga** og velja síðan viðeigandi tengja.
1. Eftirfarandi skrefum er fylgt:

    - Valið er **Nýr** til að hefja nýja afstemmingu.
    - Velja og opna fyrirliggjandi afstemmingu í listanum.

1. Á afstemmingarspjaldi **Bankareikn.afstemmingar** er valið **Afstemming með afrita**.

    ![Skjámynd sem sýnir hnappinn Stemma af og afrita á afstemmingarspjaldi bankareiknings.](media/bank-reconciliation-copilot-card.svg)

    Copilot byrjar að búa til eldsnið sem lagt er til. Þegar því er lokið **sýnir glugginn Afstemming við Copilot** niðurstöður samsvarandi vinnslu.

1. Skoða eldsnið sem lagt er til eins og lýst er í næsta hluta.
---

### Skoða, vista eða fleygja eldsniðum sem lagt er til

Þegar Afrita hefur verið keyrt **sýnir glugginn Afstemming við copilot nákvæmar niðurstöður, þ.m.t. eldspýtur sem lagt** er til. Engin samsvörun sem Copilot lagt til hefur verið vistuð. Þess vegna er hægt að skoða tillögurnar og vista þær eða fleygja þeim eftir þörfum.

![Skjámynd sem sýnir fyrirhugaðar samsvörunir í glugganum Stemma af með glugganum Copilot.](media/bank-reconciliation-copilot-window.png)

Glugganum **Stemma af við copilot er skipt** í tvo hluta. Efri hlutinn veitir nokkrar almennar upplýsingar um niðurstöðurnar. Neðri hlutinn, **Samsvörunartillögur**, sýnir samsvörunina sem Copilot lagði til.

Eftirfarandi tafla lýsir reitunum í efri hlutanum.

| Svæði | Heimildasamstæða |
|---|---|
| Sjálfvirk samsvörun | Fjöldi bankayfirlitslína sem sjálfvirka aðgerðin samsvaraði. Velja skal gildið til að skoða afstemmingarspjaldið. |
| Copilot-pörun | Fjöldi bankayfirlitslína sem Afrita lagt er til samsvörun fyrir. Hægt er að skoða upplýsingar um samsvörun í hlutanum **Samsvörunartillögur** . |
| Lokastaða yfirlits | Lokastaðan sem kemur fram á bankayfirlitinu sem verið er að stemma af við. |
| Bóka ef jafnað að fullu | Kveikja skal á þessum valkosti til að bóka sjálfkrafa afstemmingu bankareiknings þegar allar línur (100 prósent) eru jafnaðar og Halda henni er **valið**. |

Í hlutanum **Samsvörunartillögur** skal fara yfir línuna sem lagt er til samsvörun fyrir línu. Síðan skal framkvæma viðeigandi aðgerð:

- Til að fleygja einni samsvörun sem lögð er til skal velja hana á listanum og velja **svo Eyða línu**.
- Til að fleygja öllum samsvörunum sem lagt er til og loka **glugganum Stemma af með Copilot** glugga skal velja hnappinn Fleygja (ruslpóst) hnappnum ![Fleygja.](media/copilot-delete-trash-can.png) Við hliðina á hnappnum **Halda honum** neðst í glugganum.
- Til að bóka sjálfkrafa fullkomlega samsvörun afstemmingarinnar þegar hún er vistuð skal kveikja á **Bóka ef valkosturinn Sem er að fullu er notaður** .
- Til að vista samsvörunirnar sem eru sýndar í **glugganum Stemma af við stjórnborð** skal velja **Halda honum**.

## Bóka ósamþykktar upphæðir bankafærslu á fjárhagsreikninga sem lagðir eru til

Í þessum hluta er útskýrt hvernig Afrita er notað til að bóka óafstemmdar línuupphæðir bankareikningsyfirlits (eins og tilgreint er í reitnum **Mismunur**) á fjárhagsreikning. Aðeins er hægt að framkvæma þennan verkhluta úr fyrirliggjandi afstemmingu.

1. Farið á listann **Afstemmingar bankareikninga** og opnið fyrirliggjandi afstemmingu sem inniheldur óafstemmdar línur.

    Þetta skref gefur skýra yfirsýn yfir allar óafstemmdar bankayfirlitslínur sem þarf að flytja í fjárhagsreikninginn.

1. Á svæðinu **Bankayfirlitslínur** skal auðkenna ósamræmdar bankayfirlitslínur og velja eina eða fleiri línur sem á að stemma af.

    Copilot einblínir á valdar línur til að bóka nýjar greiðslur í fjárhagsreikninginn.

1. Velja skal **Bóka mismun á fjárhagsreikning** til að hefja ferlið.

    ![Skjámynd sem sýnir hnappinn Bóka mismun á fjárhagsreikningi á afstemmingarspjaldi bankareiknings.](media/bank-reconciliation-transfer-gl-copilot-card.png)

    Copilot byrjar að búa til tillögur um bókun nýrra greiðslna.

1. Þegar Copilot hefur lokið við að búa til tillögur **birtist glugginn Afritatillögur fyrir bókunarmismun í fjárhagsreikninga** .

    Í hlutanum **Samsvörunartillögur** í þessum glugga eru tillögurnar. Reynslan er eins og reynslan af því að stemma af copilot.

    ![Skjámynd sem sýnir Afritatillögur um bókun mismunar í fjárhagsreikninga.](media/bank-reconciliation-gl-transfer-proposed-matches.png)

1. Skoða tillögulínu fyrir línu til að tryggja nákvæmni greiðslna sem lagðar eru til fyrir bókun.

    - Ef kafa niður í tillögunni með því að velja hana í listanum er farið á reikningalista. Þaðan er hægt að velja annan reikning. Aðeins er hægt að gera þessa tegund handvirkrar leiðréttingar þegar flæði **bóka mismunar er notað í fjárhagsreikningsflæði** en ekki samsvarandi flæði.
    - Ef Vista er valið **við** hliðina á tillögu er hægt að **bæta vörpun við vörpun**  síðuna Texti á reikning. Næst þegar þessi texti birtist við samsvörun er honum varpað á reikning sem lagt er til.

1. Fleygja eða vista tillögur.

    - Til að fleygja tiltekinni tillögu skal velja hana á listanum og velja **svo Eyða línu**. Til að fleygja öllum tillögum og loka Copilot skal velja hnappinn fleygja (ruslpóst) hnappinn ![Fleygja.](media/copilot-delete-trash-can.png) Við hliðina á hnappnum **Halda honum** neðst í glugganum.
    - Ef tillögurnar uppfylla kröfurnar og vista á þær skal velja **Halda henni**.

         Þetta skref staðfestir flutning valinna tillagna úr bankareikningsbókinni yfir í fjárhagsreikninginn. Hún bókar nýjar greiðslur á fjárhagsreikninga sem lagðar eru til og jafnar samsvarandi línur við bankareikningsfærslurnar sem leiða af.

## Næstu skref

[Staðfesta afstemmingu bankareiknings](bank-how-reconcile-bank-accounts-separately.md#validate-your-bank-reconciliation)

## Sjá einnig .

[Úrræðaleit fyrir Copilot- og AI-eiginleika](ai-copilot-troubleshooting.md)  
[Algengar spurningar um bankaafstemmingu](faqs-bank-reconciliation.md)  
[Uppsetning bankaþjónustu](bank-setup-banking.md)  
[Afstemma bankareikninga](bank-how-reconcile-bank-accounts-separately.md)  
[Jafna greiðslur sjálfkrafa og afstemma bankareikninga](receivables-apply-payments-auto-reconcile-bank-accounts.md)
