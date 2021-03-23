---
author: edupont04
ms.service: dynamics365-accountant
ms.topic: include
ms.date: 10/02/2020
ms.author: edupont
ms.openlocfilehash: d58d8d628577f163d36199b8fc5785982aac830a
ms.sourcegitcommit: a9d48272ce61e5d512a30417412b5363e56abf30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/04/2021
ms.locfileid: "5493001"
---
Áður en hægt er að setja upp tölvupóstsskráningu þarf að undirbúa Exchange Online með [opnum möppum](/exchange/collaboration/public-folders/public-folders?view=exchserver-2019&preserve-view=true ). Hægt er að gera þetta í [Exchange stjórnendamiðstöðinni](/Exchange/architecture/client-access/exchange-admin-center?view=exchserver-2019&preserve-view=true ) eða nota [Exchange Management Shell](/powershell/exchange/exchange-management-shell?view=exchange-ps&preserve-view=true ).  

> [!TIP]
> Ef þú vilt nota [Exchange Management Shell](/powershell/exchange/exchange-management-shell?view=exchange-ps&preserve-view=true ) getur þú fengið innblástur hvernig á að setja upp forskrift í sýnisforskrift sem við birtum í [BCTech-geymslunni](https://github.com/microsoft/BCTech/tree/master/samples/EmailLogging).

Eftirfarandi listi lýsir helstu skrefum til að fá frekari upplýsingar um tengla.  

- Stofna stjórnandahlutverk fyrir almenningsmöppur á grunni upplýsinganna í eftirfarandi töflu:

  |Eiginleiki        |Gildi:                     |
  |----------------|--------------------------|
  |Name            |Stjórnun almenningsmappa |
  |Valin hlutverk  |Opnar möppur            |
  |Valdir meðlimir|Tölvupóstur notandareiknings sem Business Central mun nota til að keyra verk tölvupóstsskráningar|

  Frekari upplýsingar eru í [Stjórna hlutverkahópum](/exchange/permissions/role-groups?view=exchserver-2019&preserve-view=true).

- Stofnið nýtt pósthólf með opna möppu á grundvelli upplýsinganna í eftirfarandi töflu:

  |Eiginleiki        |Gildi:                     |
  |----------------|--------------------------|
  |Name            |Opið pósthólf            |

  Frekari upplýsingar er að finna á [Búa til pósthólf með opinni möppu í Exchange Server](/exchange/collaboration/public-folders/create-public-folder-mailboxes).  

- Stofna nýjar almenningsmöppur

  - Stofnið nýja opna möppu með heitinu *Tölvupóstsskráning* í rótinni þannig að slóðin á möppuna verði ```\Email Logging\```
  - Búa til tvær undirmöppur þannig að útkoman sé eftirfarandi heilar slóðir í möppurnar:
    - ```\Email Logging\Queue\```
    - ```\Email Logging\Storage\```

  Nánari upplýsingar má finna í [Búa til opna möppu](/exchange/collaboration/public-folders/create-public-folders?view=exchserver-2019&preserve-view=true).

- Virkja tölvupóst fyrir *biðröð* opinnar möppu

  Frekari upplýsingar er að finna á [Kveika eða slökkva á tölvupósti fyrir opna möppu](/exchange/collaboration/public-folders/mail-enable-or-disable?view=exchserver-2019&preserve-view=true)

- Þegar tölvupóstur er virkjaður er hægt að senda tölvupóst á *biðröð* opnu möppunnar með Outlook eða Exchange Management Shell

  Frekari upplýsingar er að finna á [Heimila ónafngreindum notendum að senda tölvupóst í opna möppu þar sem búið er að virkja tölvupóst](/exchange/collaboration/public-folders/mail-enable-or-disable#allow-anonymous-users-to-send-email-to-a-mail-enabled-public-folder?view=exchserver-2019&preserve-view=true)

- Stillið notanda tölvupóstsskráningar sem eiganda að báðum opnu möppunum, opnu möppunum *Biðröð* og *Geymsla* með Outlook eða Exchange Management Shell á grundvelli upplýsinganna sem birtast í eftirfarandi töflu:

  |Eiginleiki        |Gildi:                     |
  |----------------|--------------------------|
  |Notandi            |Tölvupóstur notandareiknings sem Business Central mun nota til að keyra verk tölvupóstsskráningar|
  |Heimildarstig|Eigandi                     |

  Frekari upplýsingar er að finna í [Úthluta heimildum fyrir opnu möppuna](/exchange/collaboration-exo/public-folders/set-up-public-folders#step-3-assign-permissions-to-the-public-folder).

- Búa til tvær reglur um póstflæði út frá upplýsingunum í eftirfarandi töflu

  |Tilgangur  |Name |Skilyrði                        |Aðgerð                                       |
  |---------|-----|----------------------------------|---------------------------------------------|
  |Regla fyrir móttekinn tölvupóst |Skrá tölvupóst sem sendur er til þessa fyrirtækis|*Sendandi* er staðsettur *utan fyrirtækis* og *viðtakandinn* er staðsettur *innan fyrirtækis*|Sendu falið afrit til netfangsins sem tilgreint er fyrir *biðröð* opnu möppurnar|
  |Regla fyrir sendan tölvupóst | Skrá tölvupóst sem sendur er frá þessu fyrirtæki |*Sendandi* er staðsettur *innan fyrirtækisins* og *viðtakandinn* er staðsettur *utan fyrirtækis*|Sendu falið afrit til netfangsins sem tilgreint er fyrir *biðröð* opnu möppurnar|
  
  Frekari upplýsingar er að finna á [Reglum um póstflæði í Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules) og [Aðgerðum reglu um póstflæði í Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions).

> [!NOTE]
> Ef gerðar eru breytingar á Exchange Management Shell verða breytingarnar sýnilegar í stjórnunarmiðstöð Exchange eftir nokkra töf. Einnig verða breytingar sem gerðar hafa verið í Exchange í boði í [!INCLUDE[prod_short](prod_short.md)] eftir seinkun. Seinkunin gæti verið margar klukkustundir.
