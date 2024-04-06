---
title: Stemma af bankareikninga með aðstoð afstemmingar
description: Fræðast um hvernig á að nota Copilot til að stemma af bankareikninga í Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.collection:
  - get-started
  - bap-ai-copilot
ms.date: 03/27/2024
ms.custom: bap-template
---

# <a name="reconcile-bank-accounts-with-copilot-preview"></a>Stemma af bankareikninga við Afrita (forskoðun)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Þessi grein útskýrir hvernig nota á afstemmingu bankareikninga til að aðstoða við afstemmingu bankafærslna og fjárhagsfærslna í Business Central.

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## <a name="about-bank-account-reconciliation-assist"></a>Aðstoð við afstemmingu bankareikninga

Aðstoð við afstemmingu bankareikninga er safn afléttra eiginleika sem aðstoða við afstemmingu bankareikninga. Aðstoð við afstemmingu bankareiknings býður upp á tvo aðgreinda verkhluta með Copilot:

- Bætt samsvörun færslna með fjárhagsfærslum

   Notandi kannast hugsanlega við aðgerðina **Samsvörun sjálfvirkt** á **síðunni Afstemming** bankareikninga sem samsvarar sjálfkrafa flestum bankafærslum og fjárhagsfærslum. Við vísar í þessa aðgerð sem *sjálfvirka vinnsluaðgerð*. Þótt sjálfvirkni virkar vel geta reiknireglurnar sem hún notar stundum leitt til margra ósamræmdra færslna. Copilot notar tækni viðmóts til að skoða eftirstandandi færslur og auðkenna fleiri samsvörun, byggt á dagsetningum, upphæðum og lýsingum. Ef til dæmis margir reikningar voru greiddir sem ein moldarsamtala af viðskiptamanni stemmir Copilot af eina bankayfirlitslínu við margar reikningsfærslur.

   Fara á [Afstemmingu bankareikninga við Copilot](#reconcile-bank-accounts-with-copilot).

- Tillögur um fjárhagsreikninga

  Afritið ber færslulýsinguna saman við heiti fjárhagsreikninga og leggur til líklegustu fjárhagsreikningana til að bóka á fyrir afviknar bankafærslur sem ekki er hægt að para við færslur. Til dæmis gæti Copilot lagt til að færslur með frásögninni "Eldsneytisstöð 24" verði bókaðar á "flutningsreikninginn".
  
   Fara í [Millifærslu ósamræmdra bankafærslna í tillögur um fjárhagsreikninga](#transfer-unmatched-bank-transactions-to-suggested-general-ledger-accounts).

## <a name="prerequisites"></a>Frumskilyrði

- Aðstoð við afstemmingu bankareikninga er gerð virk. Stjórnandi sinnir þessu verki. [Fræðast meira um grunnstillingu stjórnunargetu og afkastagetu](enable-ai.md) Stjórnunargetu.
- Bankareikningar í Business Central sem á að stemma af eru tengdir netbankareikningi eða settir upp með innflutningssniði bankayfirlita. 
- Þú kannast við afstemmingu bankareikninga í Business Central eins og lýst er í [afstemmingu bankareikninga](bank-how-reconcile-bank-accounts-separately.md). 

<!--H2s. Required. A how-to article explains how to do a task. The bulk of each H2 should be a procedure.-->
## <a name="reconcile-bank-accounts-with-copilot"></a>Stemma af bankareikninga við Afrita

<!-- Similar to the **Match Automatically** capability on the **Bank Acc. Reconciliation** page, Bank account reconciliation assist can also automatically matches transactions in banks statements with bank entries. The difference is that **Match Automatically** uses a native rules-based algorithm, while Bank account reconciliation assist is based AI technology though Copilot. Bank account reconciliation assist is intended to supplement the **Match Automatically** capability. While **Match Automatically** is fairly successful at matching transactions, there are some instances where it can't&mdash;which is where Bank account reconciliation assist comes. By using the **Reconcile with Copilot** action on **Bank Acc. Reconciliation** page, you can find even more matches.-->

Stjórntæki í afstemmingu bankareiknings er ætlað að nota sem viðbót við sjálfvirka vinnsluaðgerð. Af þessum sökum keyrir sjálfvirkniaðgerðin fyrst til að gera fyrstu samsvörunina. Síðan keyrir Copilot til að reyna að passa við færslur sem sjálfvirka aðgerðin réð ekki við.   

Tvær aðferðir eru til að stemma af bankareikninga við Copilot. Hægt er að nota Afrita til að hefja nýja afstemmingu á bankareikningi, beint af **afstemmingarlista** bankareikninga eða nota Afrita í nýrri eða eldri afstemmingu á **afstemmingarspjaldi** bankareiknings.

# [Úr afstemmingarlista bankareiknings](#tab/fromlist) 

Með þessari aðferð er búin til og stemmd af ný afstemming bankareikninga frá grunni. Þessi nálgun krefst þess að hægt sé að velja bankareikning og flytja bankayfirlitsskrána inn ef bankareikningurinn er ekki tengdur netreikningi.

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teikn, færa inn **afstemmingar bankareikninga** og velja síðan viðeigandi tengil. 
1. Velja skal aðgerðina **Stemma af við stjórnborð** til að opna **gluggann Stemma af við stjórnborð** .
1. Setja **afstemmingu vegna þessa bankareikningsreits** á þann bankareikning sem á að stemma af.

   ![Sýnir afstemmingu afstemmingarglugga afrita til að stemma af frá grunni](media/reconcile-bank-accounts-new-copilot.svg) 
 
1. Ef valinn bankareikningur er ekki tengdur netbankareikningi verður að flytja inn bankayfirlitsskrána. Til að flytja skrána inn skal velja annaðhvort gildið í reitnum **Nota færslugögn úr** reitnum eða velja hnappinn Mynda pappír næst hnappnum **Mynda** . Síðan skal nota Skrána **Velja til að flytja inn til að flytja** inn bankayfirlitsskrána með því annað hvort að draga hana úr tækinu eða vafra um tækið.
1. Til að stemma af við Copilot er Mynda **valið**.

   Copilot byrjar að búa til eldspýtur sem lagt er til. Þegar því er lokið opnast niðurstöður samsvörunarferlisins í glugganum Stemma af við Copilot.

1. Skoða eldsnið sem lagt er til eins og lýst er í eftirfarandi hluta.

# [Afstemmingarspjald bankareiknings](#tab/fromcard) 

Með þessari aðferð er Afrita annaðhvort notað í nýrri afstemmingu bankareikninga sem búin er til handvirkt eða með því að breyta fyrirliggjandi afstemmingu. 


1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teikn, færa inn **afstemmingar bankareikninga** og velja síðan viðeigandi tengil. 
1. Framkvæmdu eitt af eftirfarandi skrefum:

   - Valið er **Nýr** til að hefja nýja afstemmingu. 
   - Velja og opna fyrirliggjandi afstemmingu af listanum.
1. Á afstemmingarspjaldi **bankareikn.afstemmingar** skal velja **Afstemming með afrita**

   ![Sýnir afstemmingu afritunaraðgerðar á afstemmingarspjaldi bankareiknings](media/bank-reconciliation-copilot-card.svg) 

   Copilot byrjar að búa til eldspýtur sem lagt er til. Þegar því er lokið **opnast niðurstöður samsvörunarferlisins í glugganum Stemma af við Copilot** . 

1. Skoða eldsnið sem lagt er til eins og lýst er í eftirfarandi hluta. 
---

### <a name="review-save-or-discard-proposed-matches"></a>Skoða, vista eða fleygja eldsniðum sem lagt er til

Þegar Afrita hefur verið keyrt **sýnir glugginn Afstemming við copilot nákvæmar niðurstöður, þ.m.t. eldspýtur sem lagt** er til. Á þessum tímapunkti hafa engar samsvörunir lagðar til af Copilot verið vistaðar, þannig að það veitir þér tækifæri til að skoða tillögurnar og vista eða fleygja eins og þú vilt.

![Sýnir afstemmingu afstemmingarglugga stjórnborðs við áætluð samsvörun](media/bank-reconciliation-copilot-window.png) 

Copilot-glugganum er skipt í tvo hluta. Efri hlutinn veitir nokkrar almennar upplýsingar um niðurstöður, eins og lýst er í eftirfarandi töflu.  Neðri **samsvörunartillagan** sýnir samsvörunina sem lögð er til af Copilot.

|Svæði|Heimildasamstæða|
|-|-|
|Sjálfvirk samsvörun|Tilgreinir hversu margar línur á bankayfirlitinu passa við sjálfvirku aðgerðina. Velja skal gildið til að skoða afstemmingarspjaldið.  |
|Copilot-pörun|Tilgreinir hversu margar línur í bankayfirlitinu hafa samsvörun lagt til í Stjórnunarklefanum. Hægt er að skoða upplýsingar um samsvörun í hlutanum **Samsvörun sem lögð er til** .|
|Lokastaða yfirlits|Tilgreinir lokastöðuna á bankayfirlitinu sem verið er að stemma af við|
|Bóka ef jafnað að fullu|Kveikja skal á þessum rofa ef óskað er eftir að bóka sjálfkrafa afstemmingu bankareiknings þegar allar línur (100%) eru samsvöruð og haldið henni **áfram**.|

#### <a name="save-or-discard-proposed-matches"></a>Vista eða fleygja eldsniðum sem lagt er til

Í hlutanum **Samsvaraðar tillögur** skal fara yfir línuna sem lagt er til fyrir línu og framkvæma síðan viðeigandi aðgerð:

- Til að fleygja einni samsvörun sem lögð er til skal velja hana á listanum og velja svo aðgerðina **Eyða línu** .

- Til að fleygja öllum eldsniðunum sem lagt er til og loka glugganum Copilot skal velja hnappinn fleygja (ruslið getur) ![Sýnir ruslið getur táknið til að eyða öllum Copilot tillögum um afstemmingu](media/copilot-delete-trash-can.png) bankareikninga við hliðina á hnappnum **Halda honum** neðst í glugganum.

- Til að bóka sjálfkrafa fullkomlega samsvarandi afstemmingu þegar hún er vistuð skal kveikja á **Færslubók ef rofi að fullu er beitt** .  
- Til að vista samsvörunirnar sem birtast í glugganum Copilot skal velja **Halda henni**.


## <a name="transfer-unmatched-bank-transactions-to-suggested-general-ledger-accounts"></a>Flytja ósamræmdar bankafærslur í tillögur að fjárhagsreikningum

Í þessum hluta er fræðst um notkun Copilot til að færa óafstemmd bankareikningsyfirlit úr bankareikningshöfuðbók yfir á fjárhagsreikning. Aðeins er hægt að framkvæma þennan verkhluta úr fyrirliggjandi afstemmingu. 

1. Farið á listann **Afstemmingar bankareikninga** og opnið fyrirliggjandi afstemmingu sem inniheldur óafstemmdar línur.

   Byrjað er á því að opna fyrirliggjandi afstemmingu bankareiknings. Þetta skref veitir skýra yfirsýn yfir allar óafstemmdar bankayfirlitslínur sem þarf að færa í fjárhagsreikninginn.

2.  **Á svæðinu Bankayfirlitslínur** skal auðkenna svæðið ósamræmdar bankayfirlitslínur og velja eina eða fleiri línur sem á að stemma af.

   Þessar línur eru yfirlitslínurnar sem Afrita einblína á til að flytja í fjárhagsreikninginn.

3. Valið er **Millifærsla í fjárhagsreikning** til að hefja ferlið.

   ![Sýnir millifærslu í fjárhag með afritaaðgerð á afstemmingarspjaldi bankareiknings](media/bank-reconciliation-transfer-gl-copilot-card.svg) 

   Þetta skref biður Copilot um að hefja tillögur fyrir millifærsluna.

4. Þegar Copilot hefur lokið við að búa til tillögur **opnast glugginn Millifærslutillögur** afritalotu.

   Þessi gluggi birtir tillögurnar í hlutanum **Samsvarandi tillaga** . Reynslan er svipuð og að stemma af copilot.

   ![Sýnir millifærsluna í fjárhag með samsvörunarsíðu fyrir afritaða samsvörun fyrir afstemmingu bankareikninga](media/bank-reconciliation-gl-transfer-proposed-matches.png) 

5. Farið er yfir hverja tillögulínu fyrir línu til að tryggja nákvæmni millifærslna sem lagðar eru til.

   - Ef kafað er niður í tillöguna með því að velja hana í listanum er farið á reikningalista. Héðan er hægt að velja annan reikning. Þess háttar handvirk leiðrétting er aðeins möguleg þegar flæði **millifærslna í fjárhagsreikning** er notað, ekki í samsvarandi flæði. 
   - Ef valið er **Vista...** við hliðina á tillögu er hægt að bæta vörpuninni **á síðuna Vörpun** texta á reikning svo næst þegar þessi texti birtist á meðan hann verður samsvörun verður honum varpað á reikninginn sem lagt er til.

6. Fleygja eða vista tillögur.

   - Ef henda á tiltekinni tillögu er hún valin á listanum og Eyða línu **valið**. Til að fleygja öllum tillögum og hætta í Copilot skal velja fleyghnappinn (ruslið) ![Sýnir ruslið getur táknið til að eyða öllum Copilot-tillögum fyrir afstemmingu](media/copilot-delete-trash-can.png) bankareikninga við hliðina **á hnappinum Halda honum** neðst í glugganum.
   
   - Ef tillögurnar uppfylla kröfurnar og vista á þær skal velja **Halda henni**. 

      Þetta skref staðfestir flutning valinna tillagna úr bankareikningshöfuðbók yfir í fjárhagsreikninginn. Hún bókar nýjar greiðslur á fjárhagsreikninga sem lagðar voru til og jafnar samsvarandi línur við bankareikningsfærslurnar sem leiða af.

## <a name="next-steps"></a>Næstu skref

[Staðfesta afstemmingu bankareiknings](bank-how-reconcile-bank-accounts-separately.md#validate-your-bank-reconciliation)  

## <a name="see-also"></a>Sjá einnig .
[Villuleita Copilot- og gervigreindarmöguleika](ai-copilot-troubleshooting.md)  
[Algengar spurningar um bankaafstemmingu](faqs-bank-reconciliation.md)  
[Uppsetning bankaþjónustu](bank-setup-banking.md)  
[Afstemma bankareikninga](bank-how-reconcile-bank-accounts-separately.md)  
[Jafna greiðslur sjálfkrafa og afstemma bankareikninga](receivables-apply-payments-auto-reconcile-bank-accounts.md) 
