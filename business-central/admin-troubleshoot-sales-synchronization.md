---
title: Úrræðaleit vegna samstillingarvillna
description: 'Þessi grein veitir leiðbeiningar um auðkenningu, úrræðaleit og úrlausn samstillingarvillna.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 04/04/2024
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Úrræðaleit vegna samstillingarvillna

Margir hreyfanlegir hlutir taka þátt í samþættingu [!INCLUDE[prod_short](includes/prod_short.md)] við [!INCLUDE[prod_short](includes/cds_long_md.md)] og stundum fer eitthvað úrskeiðis. Í þessari grein er bent á nokkrar af dæmigerðum villum sem upp koma og gefur nokkra punkta fyrir hvernig á að lagfæra þær.

Villur koma oft upp annaðhvort vegna einhvers sem notandi gerði í ásamt færslum, eða eitthvað er að því hvernig samþættingin er sett upp. Fyrir villur sem tengjast paraðri færslu geta notendur leyst sjálfir. Orsakir þessara villna eru oft aðgerðir, svo sem eyðing gagna í einu, en ekki bæði, viðskiptaforrit og síðan samstillt. Frekari upplýsingar er að finna í [Skoða stöðu á samstillingu](admin-how-to-view-synchronization-status.md).

Villur sem tengjast því hvernig samþættingin er sett upp þurfa venjulega á athygli stjórnanda að halda. Hægt er að skoða þessar villur á síðunni **Villur í samstillingu samþættingar**. 

Eftirfarandi tafla sýnir dæmi um algeng vandamál:  

|Gefa út  |Upplausn  |
|---------|---------|
|Heimildirnar og hlutverkin sem tengd eru samþættingarnotandanum eru ekki rétt. | Þessi villa kemur [!INCLUDE[prod_short](includes/cds_long_md.md)] og hann inniheldur oft eftirfarandi texta,Aðalnotandi **(Id=\<user id>, tegund=8) vantar \<privilegeName> heimildir**. Þessi villa kemur upp því að samþættingarnotanda vantar réttindi sem leyfa honum að fá aðgang að einingu. Þessi villa gerist yfirleitt ef sérsniðnar einingar eru samstilltar eða ef forrit er uppsett í [!INCLUDE[prod_short](includes/cds_long_md.md)] þeim krefst heimildar til að fá aðgang að öðrum [!INCLUDE[prod_short](includes/cds_long_md.md)] einingum. Til að leysa úr þessari villu skal úthluta samþættingarnotanda heimildina í [!INCLUDE[prod_short](includes/cds_long_md.md)].<br><br> Finna má nafn samþættingarnotanda á síðunni **Dataverse Uppsetning tengingar**. Villuboðin gefa heiti heimildarinnar sem hjálpa til við að auðkenna einingu sem notandi þarfnast heimildar. Til að bæta við réttindunum sem vantar skal skrá sig inn í [!INCLUDE[prod_short](includes/cds_long_md.md)] með stjórnandareikningi og breyta öryggishlutverkinu sem samþættingarnotanda er úthlutað. Frekari upplýsingar er að finna í [Búa til eða breyta öryggishlutverki til að stjórna aðgangi](/power-platform/admin/create-edit-security-role). |
|Ūú sættir ūig viđ ađ nota ađra færslu sem er ekki parađur. Til dæmis ef viðskiptamaður er ekki paraður eða vara sem mælieiningin er ekki tekin fyrir. | Fyrst þarf að tengja háða færslu, t.d. gjaldmiðil eða mælieiningu, og svo reyna tenginguna aftur. |
|Hlé er á tengingunni Dataverse við samstillingu. Til dæmis vegna þess að lotan var útrunnin. Þegar það gerist birtast eftirfarandi villa þegar lotan er haldið áfram: _Skrá verður töflutengingu fyrir töflutegundina CRM með Því að nota RegisterTableConnection eða cmdlet New-NAVTableConnection áður en hægt er að nota hana._|* Endurnýjaðu síðuna til að tengjast aftur til að Dataverse fá tímamörk lotunnar. Villuboðin hverfur.<br><br>* Ef þú notar sérsniðna síðu til að birta gögn frá Dataverse einingu skaltu hafa samband við samstarfsaðila Microsoft eða stuðning. Þegar það er gert er aðgerðin **Afrita upplýsingar** notuð til að deila upplýsingum um villuna. |

Eftirfarandi eru nokkur verkfæri á síðunni Samstillingarvillur samþættingar sem geta hjálpað þér að leysa úr þessum vandamálum handvirkt.  

* Reitirnir **Upprunastaður** og **Áfangastaður** geta innihaldið tengla á línuna þar sem villan fannst. Velja tengilinn til að rannsaka villuna.  
* Aðgerðin **Eyða færslum eldri en 7 daga** og **Eyða öllum færslum** hreinsa listann. Þessar aðgerðir eru yfirleitt notaðar eftir að leyst hefur verið úr orsök villu sem hefur áhrif á margar færslur. Sýndu samt aðgát. Þessar aðgerðir gætu eytt villum sem skipta enn máli.
* Aðgerðin **Sýna villu í kallstafla** sýnir upplýsingar sem geta hjálpað til við að skilja rót vandans. Ef ekki er hægt að leysa úr villunni á eigin spýtum og ákveðið er að senda inn þjónustubeiðni skal hafa upplýsingarnar með í þjónustubeiðninni.

## Sjá einnig .

[Samþætting við Microsoft Dataverse](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Uppsetning á notendareikningum fyrir samþættingu við Microsoft Dataverse](admin-setting-up-integration-with-dynamics-sales.md)  
[Uppsetning á tengingu við Microsoft Dataverse](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Tengja og samstilla færslur handvirkt](admin-how-to-couple-and-synchronize-records-manually.md)  
[Skoða stöðu á samstillingu](admin-how-to-view-synchronization-status.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
