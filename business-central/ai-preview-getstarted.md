---
title: Hafist er handa með Business Central forskoðunarútgáfu fyrir Copilot
description: Útskýrir hvernig á að fá Business Central umhverfi með nýja AI getu til að búa til textatillögur að vöru-/vörulýsingum.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/16/2023
ms.custom: bap-template
---

# Hafist er handa með Business Central forskoðunarútgáfu fyrir Copilot

[!INCLUDE[ai-preview](includes/ai-preview.md)]

Þú getur prófað al-powered markaðssetningartexta með Copilot hvort sem þú ert núverandi Business Central viðskiptavinur eða hugsanlegur viðskiptamaður, það er, einhver sem hefur bara áhuga á að skoða Business Central og reyna nýja getu. Til að byrja þarftu aðgang að Business Central netútgáfu sem styður nýja getu. Fyllið út hlutann fyrir neðan sem á við um þig.

## Fyrirtækið þitt notar nú þegar Business Central

Sem núverandi viðskiptavinur eða samstarfsaðili þarftu að fá aðgang að stjórnunarmiðstöð Business Central til að setja upp umhverfi sem keyrir forskoðunarútgáfuna sem inniheldur Copilot. Þegar umhverfið er í gangi geta notendur prófað nýja eiginleikann.

Ef þú ert umhverfisstjórnun skal ljúka eftirfarandi skrefum:

1. Skráðu þig inn í stjórnunarmiðstöð Business Central.
2. Valið **er Umhverfi nýtt** > **·**.
3. Á svæðinu **Stofna umhverfi** er tilgreint heiti fyrir nýja umhverfið í reitnum **Heiti** umhverfis.
4. Stilla **tegund** umhverfis á **Sandkassi** eða **Framleiðsla**.
5. Stilla **land** á hvaða land/svæði sem er á listanum en hafa ber í huga að í forskoðuninni er AI-mynda markaðssetningartextinn frá Copilot aðeins á ensku.
6. Í reitnum **Útgáfa er valin útgáfa** 22 eða nýrri af listanum.

   <!--
   > [!IMPORTANT]
   > You must use **22.0.54157.54311 (Preview - Copilot edition)** to experience Copilot.
   -->
7. Velja **Stofna**.  

Nánari upplýsingar um hvernig á að stofna umhverfi eru í [Stofna umhverfi](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#create-a-new-environment).

> [!IMPORTANT]
> Ef þú ert með forskoðunarsandkassa sem keyra á **22.0.54157.54311 (Forskoðun - Copilot útgáfa)**, hafðu í huga að þessi umhverfi eru aðeins tiltæk til 01. maí 2023. Eftir þessa dagsetningu þarftu að ráðstafa nýju umhverfi eða uppfæra eitthvað af öðru umhverfi þínu í útgáfu 22.0 eða nýrri til að halda áfram að reyna forskoðun á markaðssetningartexta AI-knúinna vöru.

## Fyrirtækið þitt notar ekki Business Central

Ef þú ert ekki Business Central viðskiptavinur skaltu skrá þig fyrir ókeypis prufu til að prófa nýja AI getu. Einfalt er að skrá sig í réttarhöldin. Þú munt hafa leiðsögn í nokkrum skrefum þar sem þú þarft að veita nokkrar upplýsingar, eins og netfangið þitt, símanúmer og nafn. Til að fá réttarhöldin skal ljúka eftirfarandi skrefum:

1. Farðu á [þessa prufusíðu](https://go.microsoft.com/fwlink/?linkid=2227167) til að byrja með skráningarferlið.
2. Leiðbeiningunum á skjánum er fylgt.

   Þú ert beðin(n) um að veita upplýsingar eins og netfang, nafn og símanúmer. Nákvæm upplifun getur verið mismunandi eftir upplýsingunum sem notandi veitir. <!--But here are a couple important points to be aware of as you run through the sign-up process:--> Notaðu vinnu- eða skólapóstfangið þitt fyrir netfangið þitt. Viđ stofnum réttarhöldin á reikningi fyrirtækisins. Þú getur ekki notað netföng sem veitt eru af neytendum með tölvupóstþjónustu eða fjarskiptaþjónustu, svo sem outlook.com, hotmail.com, gmail.com, og öðrum.
   
   <!-- When you get to the option for **Country or region** be sure to set this **United States**.

      > [!IMPORTANT]
      > You must set **Country or region** to **United States**; otherwise the AI-powered item marketing text with Copilot won't be available in Business Central.  -->
3. Þegar þú ferð í **upplýsingaskref staðfestingar** er þú tilbúinn að hefja réttarhöldin.

   - Til að fara beint í Business Central skal velja **Sleppa & fara til Að Dynamics 365 Business Central** > **byrja**.
   - Þú hefur einnig kost á að bjóða öðrum í fyrirtæki þínu til ókeypis prufu einnig. Sláðu bara inn, netföng hvers einstaklings og veldu **svo Senda fundarboð**. Veljið **Hafist handa** við að fara í Business Central.  

   Farið verður með þig í prufuútgáfuna á [https://businesscentral.dynamics.com/](https://businesscentral.dynamics.com/). Það getur tekið nokkrar mínútur að fá prufutímann tilbúna í fyrsta skipti sem þú skráir þig inn.

<!--
1. On the **Let's get you started** step, enter your work or school email address, then select **Next**.

   Use your work or school email address. We'll establish your trial on your organization's account. You can't use email addresses provided by consumer email services or telecommunication providers, such as outlook.com, hotmail.com, gmail.com, and others.
3. When asked what kind of email you have, select **I got it from my organization** > **Next**.
4. On the **Create your account** step, you provide information that will help use set up a trial version of Business Central that you can sign in to.

   1. Provide a telephone number that we can use to send you a verification code. Enter a country code and number that isn't VoIP or toll free.
   2. Choose how you want us to send the verification code:
      - Select **Text me** to get the verification code in a text message.
      - Select **Call me** to get the code in a voice message.
   3. Select **Send verification code**. 
   4. When you get the code, type it in the **Enter your verification code** box, then select **Verify**.

      Once you're verified, we'll send you an email with another verification code that you'll use in the next step to complete creating your account.
   5. Fill in your first and last name.
   6. Set **Country or region** to **United States**.

      > [!IMPORTANT]
      > You must set **Country or region** to **United States**; otherwise the AI-powered item marketing text with Copilot won't be available in Business Central.  

   7. Enter a valid phone umber in the **Business telephone number** box.
   8. In the **Create password** and **Confirm password** boxes, enter a password that you want to use to sign in to Business Central. The password must at least eight characters and include at least one number, an uppercase letter, and a lower case letter.
   9. In the **Verification code** box, enter the verification code we sent you in an email, then select **Next**.
   10. When you get a prompt that your account is successfully created, select **Sign in**.
-->

4. Þegar þú hefur verið skráð(ur) inn sérðu heimasíðu Business Central sem nefnist mitt hlutverk, sem lítur svipað út og eftirfarandi mynd:

   [![Sýnir mitt hlutverk Business Central og gátlistann fyrir Copilot](media/copilot-checklist.png)](media/copilot-checklist.png#lightbox)

5. Til að fá kynningu með leiðsögn um að búa til AI-powered markaðssetningartexta með Copilot, undir **Gátlistinn þinn næst efst** á síðunni, veldu **Create with Copilot** > **Start tour**. Leiðbeiningunum er síðan fylgt.

   > [!TIP]
   > Ef þú sérð **ekki Gátlistann** þinn skaltu velja hnappinn **Sýna kynningarferðir** fyrst.

## Næstu skref

Eiginleikar Copilot bjóða upp á verða að vera virkir áður en þú eða einhver annar getur notað Copilot. Til að gera ÓB-möguleikana virka þarf stjórnandi að hafa samþykki á skilmálum og skilyrðum forskoðunarinnar [og](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/) [yfirlýsingu](https://go.microsoft.com/fwlink/?LinkId=521839) Microsoft um persónuvernd fyrir hönd fyrirtækisins.

> [!NOTE]
> Ef þú notar réttarhöld þá ert þú stjórnandinn. Ef þú hefur boðið öðrum í samtökunum að réttarhöldin við skráningu munu þeir ekki geta notað Copilot fyrr en þú samþykkir skilmálana.

Tvær leiðir eru til að samþykkja sem stjórnandi:

- Auðveldast er að nota Copilot. Í fyrsta skipti sem Copilot er notað sem stjórnandi er beðið um að fara yfir skilmálana og skilyrðin, eru síðan sammála eða ósammála. Til að læra hvernig á að nota Copilot er farið í [Bæta markaðstexta við vörur](item-marketing-text.md).  

- Hin leiðin er að nota síðuna **Staða** persónuverndartilkynninga í Business Central og samþykkja **Azure OpenAI** samþættingu allra notenda. Til að fræðast meira er farið í [Samþykki samkvæmt skilmálum og skilyrðum](enable-ai.md#consent-to-or-reject-preview-and-privacy-terms-and-conditions-for-all-users).

## Sjá einnig .

[Yfirlit yfir AI-powered markaðssetningartexta vöru með Copilot](ai-overview.md)  
[Grunnstilla AI-knúinn markaðssetningartexta vöru með Copilot sem admin](enable-ai.md)  
[Búa til markaðssetningartexta fyrir vörur með Copilot](item-marketing-text.md)  
[AI-knúinn markaðssetningartexti vöru (forskoðun) með eignaútgáfu copilot](ai-faq.md)  