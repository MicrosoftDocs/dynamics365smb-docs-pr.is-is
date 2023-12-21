---
title: Samræma bankareikninga með því að nota afstemmingaraðstoð
description: Lærðu hvernig á að nota Copilot til að samræma bankareikninga í Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.collection: get-started
ms.date: 10/25/2023
ms.custom: bap-template
---

# Samræma bankareikninga með Copilot (sýnishorn)

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

Þessi grein útskýrir hvernig á að nota afstemmingaraðstoð bankareikninga til að hjálpa þér að samræma bankafærslur við fjárhagsfærslur í Business Central.

## Um aðstoð bankareikningsafstemmingar

Aðstoð við afstemmingu bankareikninga er safn af gervigreindaraðgerðum sem aðstoða þig við að samræma bankareikninga. Aðstoð við afstemmingu bankareikninga býður þér upp á tvö aðskilin verkefni í gegnum Copilot:

- Bætt samsvörun viðskipta við fjárhagsfærslur

   Þú gætir nú þegar kannast við **Passa sjálfkrafa** aðgerðina á **bankareikningi. Afstemmingar** síðu sem passar sjálfkrafa við flestar bankafærslur við fjárhagsfærslur. Við vísum til þessa aðgerð sem *automatch*. Þó að automatch virki vel geta reikniritin sem það notar stundum leitt til margra ósamþykktra viðskipta. Copilot notar gervigreindartækni til að skoða viðskipti sem eftir eru og bera kennsl á fleiri samsvörun, byggt á dagsetningum, upphæðum og lýsingum. Til dæmis, ef margir reikningar voru greiddir sem ein eingreiðsla af viðskiptamanni, samræmir Copilot eina bankayfirlitslínuna við margar reikningsfærslur.
   
   Farðu í [Samræma bankareikninga með Copilot](#reconcile-bank-accounts-with-copilot).

- Tillögur að aðalbókareikningum

  Fyrir afgangs bankafærslur sem ekki er hægt að samræma við neinar fjárhagsfærslur, ber Copilot færslulýsinguna saman við nöfn reikningsreikninga og gefur til kynna líklegasta reikninginn til að bóka á. Til dæmis gæti Copilot stungið upp á því að færslur með frásögninni "Fuel Stop 24" verði færðar inn á "Transportation" reikninginn.
  
   Farðu í [Flytja ósamræmdar bankafærslur á ráðlagða fjárhagsreikninga](#transfer-unmatched-bank-transactions-to-suggested-general-ledger-accounts).


   
## Frumskilyrði

- Afstemmingaraðstoð bankareikninga er virkjuð og virkjuð. Þetta verkefni er unnið af stjórnanda. [Lærðu meira um að virkja Copilot og gervigreindargetu](enable-ai.md).
- Bankareikningar í Business Central sem þú vilt samræma eru tengdir netbankareikningi eða settir upp með innflutningssniði bankayfirlits. 
- Þú þekkir afstemmingu bankareikninga í Business Central eins og lýst er í [Samræma bankareikninga](bank-how-reconcile-bank-accounts-separately.md). 

<!--H2s. Required. A how-to article explains how to do a task. The bulk of each H2 should be a procedure.-->
## Samræma bankareikninga við Copilot

<!-- Similar to the **Match Automatically** capability on the **Bank Acc. Reconciliation** page, Bank account reconciliation assist can also automatically matches transactions in banks statements with bank entries. The difference is that **Match Automatically** uses a native rules-based algorithm, while Bank account reconciliation assist is based AI technology though Copilot. Bank account reconciliation assist is intended to supplement the **Match Automatically** capability. While **Match Automatically** is fairly successful at matching transactions, there are some instances where it can't&mdash;which is where Bank account reconciliation assist comes. By using the **Reconcile with Copilot** action on **Bank Acc. Reconciliation** page, you can find even more matches.-->

Copilot í bankareikningsafstemmingu er ætlað að nota sem viðbót við sjálfvirka aðgerðina. Af þessum sökum, þegar þú notar Copilot, keyrir sjálfvirk aðgerð fyrst til að gera fyrstu samsvörun. Síðan keyrir Copilot til að reyna að passa við færslur sem sjálfvirka aðgerðin höndlaði ekki.   

Það eru tvær leiðir til að samræma bankareikninga við Copilot. Þú getur notað Copilot til að hefja nýja afstemmingu á bankareikningi, beint af **Bankareikningsafstemming** listanum, eða þú getur notað Copilot á nýrri eða núverandi afstemmingu á **Bankafrv. Afstemmingar** kort.

# [Af afstemmingarlista bankareikninga](#tab/fromlist) 

Með þessari nálgun býrðu til og samræmir nýja bankareikningsafstemmingu frá grunni. Þessi aðferð krefst þess að þú velur bankareikninginn og flytur inn bankayfirlitsskrána, ef bankareikningurinn er ekki tengdur við netreikning.

1. Veldu ![peru sem opnar Segðu mér eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, sláðu inn **Afstemmingar bankareikninga** og veldu síðan tengda hlekkinn. 
1. Veldu aðgerðina **Samræma við Copilot** til að opna **Sjána við Copilot** gluggann.
1. Stilltu **Framkvæma afstemmingu fyrir þennan bankareikning** reit á bankareikninginn sem þú vilt samræma.

   ![Sýnir afstemmingar við stýrimannsgluggann til að samræma frá grunni](media/reconcile-bank-accounts-new-copilot.svg) 
 
1. Ef valinn bankareikningur er ekki tengdur við netbankareikning verður þú að flytja inn bankayfirlitsskrána. Til að flytja skrána inn skaltu annað hvort velja gildið í reitnum **Nota færslugögn frá**  eða velja bréfaklemmuhnappinn við hliðina á **Búa til** hnappur. Notaðu síðan **Veldu skrána til að flytja inn** til að flytja inn bankayfirlitsskrána með því annað hvort að draga hana úr tækinu þínu eða vafra í tækinu þínu.
1. Til að sættast við Copilot skaltu velja **Generate**.

   Copilot byrjar að búa til fyrirhugaðar samsvörun. Þegar því er lokið opnar gluggann Samræma við stýrimann niðurstöður samsvörunarferlisins.

1. Skoðaðu fyrirhugaðar samsvörun eins og lýst er í eftirfarandi kafla.

# [Af afstemmingarkorti banka](#tab/fromcard) 

Með þessari nálgun notar þú Copilot annað hvort á nýja bankareikningsafstemmingu sem þú býrð til handvirkt eða með því að breyta núverandi afstemmingu. 


1. Veldu ![peru sem opnar Segðu mér eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, sláðu inn **Afstemmingar bankareikninga** og veldu síðan tengda hlekkinn. 
1. Framkvæmdu eitt af eftirfarandi skrefum:

   - Veldu **Nýtt** til að hefja nýja afstemmingu. 
   - Veldu og opnaðu núverandi afstemmingu af listanum.
1. Í **bankafrv. Afstemmingar** kort, veldu **Samræma með Copilot**

   ![Sýnir afstemmingu við aðstoðarflugmannsaðgerð á bankareikningnum. Samþykktarkort](media/bank-reconciliation-copilot-card.svg) 

   Copilot byrjar að búa til fyrirhugaðar samsvörun. Þegar því er lokið opnar glugginn **Sjást við Copilot**  niðurstöður samsvörunarferlisins. 

1. Skoðaðu fyrirhugaðar samsvörun eins og lýst er í eftirfarandi kafla. 
---

### Skoðaðu, vistaðu eða fargaðu fyrirhuguðum samsvörun

Eftir að þú keyrir Copilot, **Sættast við Copilot**  gluggi sýnir nákvæmar niðurstöður, þar á meðal allar fyrirhugaðar samsvörun. Á þessum tímapunkti hefur engin samsvörun verið vistuð af Copilot, svo það gefur þér tækifæri til að skoða tillögurnar og vista eða henda eins og þú vilt.

![Sýnir afstemmingargluggann með aukastjórnanda með fyrirhuguðum samsvörun](media/bank-reconciliation-copilot-window.png) 

Copilot glugginn er skipt í tvo hluta. Efri hlutinn gefur nokkrar almennar upplýsingar um niðurstöðu, eins og lýst er í eftirfarandi töflu.  Því lægra **Samsvörun tillaga**  kafla er listi yfir samsvörun sem Copilot lagði til.

|Svæði|Heimildasamstæða|
|-|-|
|Sjálfvirk samsvörun|Tilgreinir hversu margar línur á bankayfirlitinu passa við sjálfvirka aðgerðina. Veldu gildi til að skoða afstemmingarspjaldið.  |
|Copilot-pörun|Tilgreinir hversu margar línur í bankayfirlitinu hafa samsvörun sem Copilot hefur lagt til. Þú getur skoðað upplýsingar um leiki í **Leikir fyrirhugaðir**  kafla.|
|Lokastaða yfirlits|Tilgreinir lokastöðuna sem sýnd er á yfirliti bankans sem þú ert að samræma við|
|Bóka ef jafnað að fullu|Kveiktu á þessum rofa ef þú vilt bóka afstemmingu bankareiknings sjálfkrafa þegar allar línur (100%) passa saman og þú hefur valið **Eigðu það**.|

#### Vistaðu eða fargaðu fyrirhuguðum samsvörun

Í kaflanum **Samsvarandi tillögur**  skaltu fara yfir tillögurnar línu fyrir línu og grípa síðan til viðeigandi aðgerða:

- Til að henda einni fyrirhugaðri samsvörun skaltu velja hana á listanum og velja síðan aðgerðina **Eyða línu** .

- Til að fleygja öllum fyrirhuguðum samsvörunum og loka Copilot glugganum, veldu fleygjahnappinn (ruslafata) ![Sýnir ruslatunnutáknið til að eyða öllum Copilot tillögunum um afstemmingu bankareikninga](media/copilot-delete-trash-can.png) við hliðina á  **Haltu honum** hnappnum neðst í glugganum.

- Til að birta fullkomlega samsvarandi afstemmingu sjálfkrafa þegar þú vistar hana skaltu kveikja á **Færa ef fullkomlega er beitt** rofi.  
- Til að vista samsvörun sem sýndar eru í Copilot glugganum skaltu velja **Halda því**.


## Flytja ósamræmdar bankafærslur á ráðlagða fjárhagsreikninga

Í þessum hluta lærir þú hvernig á að nota Copilot til að flytja ósamræmd bankareikningsyfirlit úr bankareikningi yfir á aðalbók. Þetta verkefni er aðeins hægt að gera út frá fyrirliggjandi afstemmingu. 

1. Farðu í **Afstemmingar bankareikninga** listann og opnaðu núverandi afstemmingu sem inniheldur óafstilltu línurnar.

   Byrjaðu á því að opna núverandi afstemmingu bankareiknings. Þetta skref veitir þér skýra yfirsýn yfir allar ósamræmdar bankayfirlitslínur sem þarf að flytja yfir á fjárhagsreikning.

2. Í **Bankayfirlitslínum** rúðunni, auðkenndu ósamsettu bankayfirlitslínurúðuna og veldu eina eða fleiri línur sem þú vilt samræma.

   Þessar línur eru yfirlitslínurnar sem Copilot einbeitir sér að til flutnings yfir á fjárhagsreikning.

3. Veldu **Flytja á G/L Account** til að hefja ferlið.

   ![Sýnir millifærsluna í G/L með aukaflugmannsaðgerð á bankareikningnum. Samþykktarkort](media/bank-reconciliation-transfer-gl-copilot-card.svg) 

   Þetta skref hvetur Copilot til að byrja að búa til tillögur fyrir flutninginn.

4. Þegar Copilot hefur lokið við að búa til tillögur opnast glugginn **Copilot G/L Account Transfer Supplements** .

   Þessi gluggi sýnir tillögurnar í **Passaða tillögu** hlutanum. Reynslan er svipuð og samræmast Copilot.

   ![Sýnir millifærsluna í G/L með samsvörunarsíðu fyrirhugaðrar samsvörunarstjóra fyrir afstemmingu bankareiknings](media/bank-reconciliation-gl-transfer-proposed-matches.png) 

5. Farðu yfir hverja tillögu línu fyrir línu til að tryggja nákvæmni fyrirhugaðra flutninga.

   - Ef þú kafar niður á tillöguna með því að velja hana á listanum ertu færður á lista yfir reikninga. Héðan geturðu valið annan reikning. Handvirk leiðrétting af þessu tagi er aðeins möguleg þegar  **Flytja á G/L Account** flæði er notað, ekki í samsvarandi flæði. 
   - Ef þú velur **Vista...** við hlið tillögu geturðu bætt vörpuninni við **Texti-til-reikningsvörpun** síðu, þannig að næst þegar þessi texti birtist á meðan hann er samsvörun verður hann varpaður á fyrirhugaðan reikning.

6. Henda eða vista tillögur.

   - Ef þú vilt henda tiltekinni tillögu skaltu velja hana á listanum og velja síðan **Eyða línu**. Til að henda öllum tillögunum og hætta við Copilot, veldu fleygjahnappinn (ruslafötuna) ![Sýnir ruslatunnutáknið til að eyða öllum Copilot tillögunum fyrir afstemmingu bankareikninga](media/copilot-delete-trash-can.png) við hliðina á **Haltu honum** hnappnum neðst í glugganum.
   
   - Ef tillögurnar uppfylla kröfur þínar og þú vilt vista þær skaltu velja **Keep It**. 

      Þetta skref staðfestir flutning á tillögum sem nú eru valdar úr bankareikningi yfir á aðalbók. Það bóka nýjar greiðslur á fyrirhugaða fjárhagsreikninga og beitir samsvarandi línum á fjárhagsfærslur bankareiknings sem myndast.

## Næstu skref

[Staðfestu afstemmingu bankareiknings þíns](bank-how-reconcile-bank-accounts-separately.md#validate-your-bank-reconciliation)  

## Sjá einnig .
[Villuleita Copilot- og gervigreindarmöguleika](ai-copilot-troubleshooting.md)  
[Algengar spurningar um gervigreind á ábyrgð fyrir aðstoð við bankaafstemmingu](faqs-bank-reconciliation.md)  
[Uppsetning bankaþjónustu](bank-setup-banking.md)  
[Afstemma bankareikninga](bank-how-reconcile-bank-accounts-separately.md)  
[Jafna greiðslur sjálfkrafa og afstemma bankareikninga](receivables-apply-payments-auto-reconcile-bank-accounts.md) 
