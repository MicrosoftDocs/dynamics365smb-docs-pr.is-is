---
title: Úrræðaleit vegna samstillingarvillna
description: 'Þetta efnisatriði veitir leiðbeiningar um greiningu á, úrræðaleit og úrlausn á samstillingarvillum.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/14/2021
ms.author: bholtorf
---
# <a name="troubleshooting-synchronization-errors"></a><a name="troubleshooting-synchronization-errors"></a><a name="troubleshooting-synchronization-errors"></a>Úrræðaleit vegna samstillingarvillna


Margir hreyfanlegir hlutir taka þátt í samþættingu [!INCLUDE[prod_short](includes/prod_short.md)] við [!INCLUDE[prod_short](includes/cds_long_md.md)] og stundum fer eitthvað úrskeiðis. Þetta efnisatriði bendir á nokkrar dæmigerðar villur sem koma upp og gefur ýmis ráð um hvernig á að laga þær.

Villur koma oft upp annaðhvort vegna þess að notandi hefur gert eitthvað við tengdar færslur eða eitthvað er að uppsetningu samþættingar. Notendur geta leyst úr villum sem tengjast tengdum færslum. Þessar villur stafa af aðgerðum eins og að eyðing á gögnum í öðru, en ekki báðum, viðskiptaforritunum og síðan samstilla. Frekari upplýsingar er að finna í [Skoða stöðu á samstillingu](admin-how-to-view-synchronization-status.md).

Villur sem tengjast því hvernig samþættingin er sett upp þurfa venjulega á athygli stjórnanda að halda. Hægt er að skoða þessar villur á síðunni **Villur í samstillingu samþættingar**. 

Eftirfarandi tafla sýnir dæmi um algeng vandamál:  

|Gefa út  |Upplausn  |
|---------|---------|
|Heimildir og hlutverk sem úthlutað er samþættingarnotanda eru ekki rétt. | Þessi villa kemur úr [!INCLUDE[prod_short](includes/cds_long_md.md)] og oft fylgir henni eftirfarandi texti: „Notanda (kenni=\<user id>, gerð=8) vantar \<privilegeName> réttindi“. Þessi villa kemur upp því að samþættingarnotanda vantar réttindi sem leyfa honum að fá aðgang að einingu. Yfirleitt kemur þessi villa upp ef sérstilltar einingar eru samstilltar eða ef forrit er uppsett í [!INCLUDE[prod_short](includes/cds_long_md.md)] og þarf heimild til að fá aðgang að öðrum [!INCLUDE[prod_short](includes/cds_long_md.md)] einingum. Til að leysa úr þessari villu skal úthluta samþættingarnotanda heimildina í [!INCLUDE[prod_short](includes/cds_long_md.md)].<br><br> Finna má nafn samþættingarnotanda á síðunni **Dataverse Uppsetning tengingar**. Villuboðin gefa upp heiti heimildarinnar sem getur hjálpað þér að finna eininguna sem þarf heimild fyrir. Til að bæta við réttindunum sem vantar skal skrá sig inn í [!INCLUDE[prod_short](includes/cds_long_md.md)] með stjórnandareikningi og breyta öryggishlutverkinu sem samþættingarnotanda er úthlutað. Frekari upplýsingar er að finna í [Búa til eða breyta öryggishlutverki til að stjórna aðgangi](/power-platform/admin/create-edit-security-role). |
|Þú ert að tengja færslu sem notar aðra færslu sem er ekki tengd. Til dæmis gjaldmiðill viðskiptavinar sem er ekki tengdur eða vöru þar sem mælieiningin er ekki tengd. | Fyrst þarf að tengja háða færslu, t.d. gjaldmiðil eða mælieiningu, og svo reyna tenginguna aftur. |

Eftirfarandi eru nokkur verkfæri á síðunni Samstillingarvillur samþættingar sem geta hjálpað þér að leysa úr þessum vandamálum handvirkt.  

* Reitirnir **Upprunastaður** og **Áfangastaður** geta innihaldið tengla á línuna þar sem villan fannst. Smellið á tengilinn til að rannsaka villuna.  
* Aðgerðirnar **Eyða færslum eldri en sjö daga** og **Eyða öllum færslum** hreinsa listana. Venjulega eru þessar aðgerðir notaðar eftir að orsök villu sem hefur áhrif á margar færslur hefur verið löguð. Sýndu samt aðgát. Þessar aðgerðir gætu eytt villum sem skipta enn máli.
* Aðgerðin **Sýna villu í kallstafla** sýnir upplýsingar sem geta hjálpað til við að skilja rót vandans. Ef ekki er hægt að leysa úr villunni á eigin spýtum og ákveðið er að senda inn þjónustubeiðni skal hafa upplýsingarnar með í þjónustubeiðninni.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Sjá einnig
[Samþætting við Microsoft Dataverse](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Uppsetning á notendareikningum fyrir samþættingu við Microsoft Dataverse](admin-setting-up-integration-with-dynamics-sales.md)  
[Uppsetning á tengingu við Microsoft Dataverse](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Tengja og samstilla færslur handvirkt](admin-how-to-couple-and-synchronize-records-manually.md)  
[Skoða stöðu á samstillingu](admin-how-to-view-synchronization-status.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
