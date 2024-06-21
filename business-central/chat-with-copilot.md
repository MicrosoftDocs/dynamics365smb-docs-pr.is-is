---
title: Spjalla við Copilot (forskoðun)
description: Lærðu að nota spjall við Copilot til að finna gögn og fá hjálp í Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 06/13/2024
ms.custom: bap-template
ms.collection:
  - bap-ai-copilot
  - get-started
---

# <a name="chat-with-copilot-preview"></a>Spjalla við Copilot (forskoðun)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Þessi grein útskýrir hvernig á að spjalla við Copilot til að fá svör um gögn fyrirtækisins og aðstoð við verkefni og efni sem tengjast Business Central.

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## <a name="about-chat-with-copilot"></a>Um spjall við Copilot

Microsoft Copilot er AI-powered aðstoðarmaður sem hjálpar neista sköpunarkrafti, uppörva framleiðni og útrýma leiðinlegum verkefnum. Með því að spjalla við Copilot í Business Central er hægt að spyrja spurninga og finna viðskiptagögn á náttúrulegu tungumáli. Hér er það sem hægt er að gera:

- Finna viðskiptagögn fyrir fyrirtækið í Business Central. Nota spjall til að fletta upp (og opna) gögnum um einingar/færslur sem tengjast viðskiptaferlum, svo sem viðskiptamenn, lánardrottna, sölupantanir og vörur og fleira. Til dæmis má spyrja Copilot: "Sýna mér nýjustu sölupöntunina fyrir Adatum."
- Fáðu útskýringar eða skref fyrir skref leiðsagnar um ýmis verk. Til dæmis má spyrja "Hjálpa mér að skilja víddir" eða "Hvernig bóka ég sölupöntun."
- Skilja tilgang og dæmigerða notkun einstakra reita. Þegar Ask Copilot **er valið** í vísbendingu um reit opnast spjall með Útskýringarkvaðning um heiti reitarins og Copilot veitir upplýsingar um það. Copilot tengir við greinarnar sem vísað er í, svo auðvelt er að votta lýsinguna.

Heimildir Copilots svara frá opinberum upplýsingum sem fáanlegar eru á Microsoft Learn  [Dynamics 365 Business Central heimildum](/dynamics365/business-central/).
  
Notkun spjalls við Copilot straumlínur vinnuflæðis þíns með því að fara framhjá hefðbundnum yfirlits- og vöruhjálpum.
  
> [Horfa á myndskeið](https://go.microsoft.com/fwlink/?linkid=2250609)

## <a name="prerequisites"></a>Frumskilyrði

- Tryggja að spjall með Copilot getu sé virkjað af stjórnanda. [Fræðast meira um grunnstillingu stjórnunargetu og afkastagetu Stjórnunargetu](enable-ai.md).
- Stilltu skjátungumálið á Business Central á eitt eftirfarandi enska heimamanna: en-AU, en-CA, en-GB, en-IE, en-Í-NZ, en-PH, en-SG, en-US, en-ZA. [Fræðast meira um að breyta tungumálinu](ui-change-basic-settings.md#language).
- Tryggja að Business Central umhverfi þitt sé í neinu landi/svæði nema Kanada (þessi eiginleiki er ekki enn tiltækur í Kanada).

## <a name="get-started-using-chat-with-copilot"></a>Byrjaðu að nota spjall við Copilot

1. Uppi í hægra horni skjásins skal velja ![Sýna táknið Sýnir táknið fyrir spjall við Copilot Copilot](media/chat-copilot-icon.png) **táknið** ![Sýnir cllour númer 1](media/callout-number-1.svg).

   Copilot-svæðið **birtist** eins og sýnt er á myndinni:
   
    ![Sýnir táknið fyrir spjall við Copilot svæðið við útkall](media/chat-with-copilot-pane.svg)

1. Í spurningareitinn **Spurt** er neðst ![Sýnir útkallsnúmer 2](media/callout-number-2.svg), rita skal spurninguna og velja svo örvahnappinn eða ýta á <kbd>Færslulykilinn</kbd> til að fá svar.

   Ílag notandans, kallað *kvaðning*, getur verið spurning, yfirlýsing eða skipun.

   > [!TIP]
   > Copilot inniheldur nokkrar aðgerðir sem geta hjálpað þér að skrifa spurningar:
   > - Til að hjálpa við að móta spurningar er ein af kvaðningarleiðbeiningunum&mdash;**Finna,Útskýra** **eða** **Leiðbeiningar**&mdash; tiltækar efst á svæðinu ![Sýnir útkallsnúmer 3](media/callout-number-3.svg) eða úr tákninu ![Sýna kvaðningarleiðbeiningar táknið](media/prompt-guide-icon.png) **Skoða kvaðningu**  hér að ofan **Spyrja spurningareit**  ![Sýnir útkallsnúmer 4.](media/callout-number-4.svg) Leiðbeiningar um kvaðningu eru fyrirfram skilgreind stutt orðasamband sem hefja spurningu eða kvaðningu. Þeir spara þér tíma, leiðbeina svörum Copilot í átt að flokki svara og hjálpa þér að læra að orðalagsspurningar til að fá bestu svörin.
   > - Velja kvaðningartillögur fyrir ofan hnappinn **Skoða** kvaðningu ![Sýnir útkallsnúmer 5](media/callout-number-5.svg) til að spyrja sjálfkrafa fyrirfram skilgreinda spurningu til að sjá hvernig spurningarnar og svörin virka. Kvaðningartillögur eru aðeins tiltækar þegar sýnifyrirtækið er notað CRONUS .

1. Skoða svörin sem birtast á rúðunni Copilot ![Sýnir útkallsnúmer 6](media/callout-number-6.svg).

   Svarið getur innihaldið texta, tengla á færslur eða síður í Business Central og tengla á business Central hjálpargreinar á Microsoft Learn.

1. Spyrja aðra spurningu til að fínpússa svarið.

   Spjall man samhengið, sem þýðir að þú þarft ekki að endurtaka lykilatriði úr upphaflegu spurningunni.

## <a name="clear-chat-to-start-over"></a>Hreinsa spjall til að byrja upp á

Ef þú vilt skipta yfir í annað efnisatriði í samtali við Copilot, veldu ![Þá Sýnir táknið táknið hreinsa spjall](media/clear-chat-icon.png) **byrja á nýju spjallþráðartákni**  Copilot neðst á Copilot svæðinu fyrir ofan spurningareitinn. Þessi aðgerð hreinsar minni Copilot af síðustu skilaboðum. Það er oft gagnlegt að byrja upp á nýtt eftir lengra samtal með mörgum skilaboðum og það getur hjálpað Copilot að skila nákvæmari svörum.

Spjallið hreinsar einnig ef þú lokar eða skráir þig út úr Business Central.

## <a name="tips-for-better-questions"></a>Ábendingar um betri spurningar

Hér eru nokkrar leiðir til að bæta svörin sem þú færð frá Copilot:

- Spyrjið skýrra og sértækra spurninga.
- Vertu nákvæmur og forðastu langar setningar eða margar setningar.
- Spyrðu einnar spurningar í einu. <!--Avoid asking about multiple questions in one message.-->
- Nota náttúrumál, tjá spurningarnar á vinalegan og samræðulegan hátt.
- Notaðu leitarorð, orðasamband og hugtök sem þú þekkir eru notuð í Business Central, annaðhvort í forritinu eða í heimildaskránni.
- Ef upphaflega svarið svarar ekki fullkomlega spurningum skal spyrja eftirfylgnispurninga eða endurorða síðustu spurningu.
- Ef þú spyrð spurninga á öðru efni en fyrri spurningu skaltu hreinsa spjallþráðinn sem er í gangi.

## <a name="example-prompts"></a>Dæmi um kvaðningar

Spurningar þínar um Copilot eru mismunandi eftir hlutverki þínu, núverandi verki, ferlum sem fyrirtækið fylgir og hvernig notandi tjáir sig með orðum. Eftirfarandi eru dæmi sem sýna mismunandi leiðir til að spyrja spurninga á spjallsvæðinu sem getur bætt þér í það að skrifa eigin spurningar út frá aðstæðum þínum.

Hvetja: `Find the Item with Description 'ATHENS Desk'`

Í þessu dæmi gefur notandi skýrar leiðbeiningar fyrir Copilot um að finna eina færslu. Til dæmis er gefið í skyn að færslan sé á listanum Vara. Reiturinn 'Lýsing' verður að vera tiltekinn texti sem hefur verið sleginn inn með tilboðum og með réttri eignfærslu. Copilot svarar yfirleitt nákvæmlega þegar gefnar eru nokkrar nákvæmar vísbendingar, en einnig er hægt að nota meira frjálslegt tungumál eins og í næsta dæmi.

Hvetja: `Give me the latest invoice for adatum`

Í þessu dæmi er Copilot beðið um að finna færslu en spurningin er ekki nákvæm og gæti leitt til minna nákvæms svars. Copilot getur oft skilið, eða giskað á, að reikningurinn sem verið er að leita að sé ekki innkaupareikningur heldur sölureikningur af listanum Bókaðir sölureikningar. Copilot þarf einnig að passa `adatum` við `Adatum Corporation` það er fullt og nákvæmt nafn þess viðskiptamanns sem selt er til við reikninginn.

Hvetja: `Show me customer ledger entries for Adatum from about three weeks ago`

Í þessu dæmi er afritað beðið um að leysa sameiginlega dagsetningaþraut sem yfirleitt krefst þess að opna dagatal til viðmiðunar eða nota ítarlegar afmarkanir dagsetningabila. Copilot skilur yfirleitt algengar tjáningar og viðskiptaskilmála.

Hvetja: `How does I save my filterrings for later?`

Í þessu dæmi er copilot beðið um leiðbeiningar um hvernig eigi að framkvæma einhver verk í Business Central. Copilot getur yfirleitt skilið ásetning spurningar þinnar, jafnvel þótt til séu nokkrar málfræðilegar villur, stafsetningarvillur eða skammstafanir.

## <a name="provide-feedback-on-answers"></a>Birta svörun á svörum

Hægt er að meta svörin sem þú færð frá Copilot með því að nota like (þumalputta upp) hnapp fyrir góða flokkun eða ólíkt (þumalputtum niður) hnapp fyrir lélega flokkun. Þegar mislíkindahnappurinn er valinn er hægt að velja ástæðu, þ.m.t. ónákvæman, óviðeigandi eða annan. Þessar upplýsingar geta hjálpað okkur að bæta tillögur.

<!--
1. If you want help getting you're question started, select the prompts either from the **Find**, **Explain**, or **Guide** buttons at the top of the Coplit pane or use the **View Prompts** menu above **Ask a question** box at the bottom.

   Prompts are predefined short phrases that start a question. Apart from saving you time, they're designed to target responses to specific categories. They also help you undestand how you can phrase questions to get the responses.-->
   
## <a name="see-also"></a>Sjá einnig .

- [Úrræðaleit fyrir Copilot- og AI-eiginleika](ai-copilot-troubleshooting.md)  
- [Grunnstilla Copilot- og gervigreindarmöguleika](enable-ai.md)  
- [Ábyrg algengar spurningar fyrir spjall við Copilot](faqs-chat-with-copilot.md)  
- [Forði til hjálpar í Business Central](product-help-and-support.md)  
