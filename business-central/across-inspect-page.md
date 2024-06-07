---
title: Skoða síður í Viðskiptamiðinu
description: Notið eiginleika fyrir eftirlit með síðu til að skoða sérstaklega upplýsingar um síðuhönnun og gagnaveitu. Síðuskoðun hentar vel við úrræðaleit á vandamálum varðandi gögnin þín.
ms.topic: conceptual
author: jswymer
ms.author: jswymer
ms.date: 09/15/2023
ms.service: dynamics-365-business-central
---

# <a name="inspecting-pages-in-business-central"></a>Skoða síður í Viðskiptamiðinu

Eiginleiki fyrir eftirlit með síðu gerir þér kleift að ná í upplýsingar um síðu, veitir innsýn inn í síðuhönnun, mismunandi þætti sem síðan samanstendur af og uppruna gagnanna sem eru sýnd. Eftirlit með síðu er sérstaklega hönnuð fyrir stjórnendur, kraftnotendur, starfsfólk notendaþjónustu og þróunaraðila. Það er tilvalið að læra gagnalíkanið á bak við síðu og úrræðaleit. Ef þú ert til dæmis að upplifa vandamál á síðu getur þú notað síðuskoðun til að fá upplýsingar til að gefa kerfisstjóra eða þjónustuaðila.

> [!NOTE]  
> Með  [!INCLUDE [prod_short](includes/prod_short.md)]  2023 út bylgju 2, í gegnum síðuskoðun er hægt að ræsa  Visual Studio  kótann innan vefbiðlarann til að kanna frekar og kemba upprunakóta viðaukann. Frekari upplýsingar er að finna  [í úrræðaleit í  Visual Studio  Code beint af vefbiðlara](/dynamics365/business-central/dev-itpro/developer/devenv-troubleshoot-vscode-webclient)  í Business vefumsjónarkerfi og Pro Help.

[!INCLUDE [send-report-excel](includes/send-report-excel.md)]

## <a name="work-with-page-inspection"></a>Vinna með síðueftirlit

Þú byrjar síðueftirlit á **Hjálp og notendaþjónusta**. Veldu spurningamerkið efst í hægra horninu, svo **Hjálp og notendaþjónusta** og svo **Kanna síður og gögn**. Einnig er hægt að nota flýtivísunina  <kbd>CTRL</kbd>+<kbd>Alt</kbd>+<kbd>F1</kbd>.

Rúðan **Eftirlit með síðu** opnast á hliðinni. Þegar rúðan opnast fyrst, sýnir hún upplýsingar sem á við um hlut aðalsíðunnar.

Notaðu lyklaborðið eða benditækið til að færa fókusinn á aðrar einingar á síðunni. Þegar Upplýsingakassi er valinn eða hluti á aðalsíðunni verður afmarkaða svæðið auðkennt með ramma og rúðan **Eftirlit með síðu** birtir upplýsingar um valda einingu. Til dæmis sýnir skýringarmyndin hér á undan upplýsingar um listahlutann á síðunni **Sölupöntun**. Þar sem þú ferð yfir á aðrar síður í forritinu mun rúðan **Eftirlit með síðu** uppfærast sjálfkrafa með síðuupplýsingum um leið og þú ferð á milli.

Frekari upplýsingar um hvað er sýnt í síðueftirliti er að finna í [Síður eftirlits og úrræðaleitar](/dynamics365/business-central/dev-itpro/developer/devenv-inspecting-pages) í hjálpinni fyrir Business Central Developer og IT Pro.

Ef þú sérð ekki smáatriðin sem þú býst við að sjá í  **skoðunarrúðu**  síðunnar þá hefur þú líklega ekki tilskilin leyfi, eins og lýst er í næsta kafla.

## <a name="controlling-access-to-page-inspection-details"></a>Upplýsingar um stjórnun á aðgangi að síðueftirliti

Sem stjórnandi er hægt að stýra aðgangi að ítarlegum upplýsingum sem eru sýndar í rúðunni **Eftirlit með síðu** með því að stilla heimildir sem notendur eru með. Til að veita aðgangsheimild notanda að ítarlegum upplýsingum skal gefa notendum heimildina **Keyra** í **Kerfis** hlutanum **5330**. Hægt er að veita þessa heimild með því að nota heimildasamstæðu (t.d. **D365 úrræðaleit**) eða notendaflokk (t.d. **D365 úrræðaleit**). Nánari upplýsingar um heimildir má finna í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md).

Notendur sem ekki eru veittar heimildir fyrir  **hlut í kerfi 5330**  geta enn farið í  **skoðunarrúðu**  síðunnar, en þeir sjá  **aðeins síðuna**  og  **töflusvæðin**, sem sýna grunnupplýsingar sem þeir geta látið á stuðningshólið sitt.

## <a name="see-also"></a>Sjá einnig .

[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
