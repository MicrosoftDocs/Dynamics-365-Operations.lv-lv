---
title: "Navigācijas meklēšana"
description: "Šajā rakstā ir paskaidrots, kā izmantot meklēšanas funkcionalitāti, lai naviģētu uz lapas Microsoft Dynamics 365 operācijām."
author: aneesmsft
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 25991
ms.assetid: eef0676f-c4b1-490e-a032-e9c8580f3fea
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 87fed576f8cf358520d94f5cd5b326ff9801913a
ms.lasthandoff: 03/31/2017


---

# <a name="navigation-search"></a>Navigācijas meklēšana

Šajā rakstā ir paskaidrots, kā izmantot meklēšanas funkcionalitāti, lai naviģētu uz lapas Microsoft Dynamics 365 operācijām.

Dynamics 365 operācijām nodrošina funkcionalitāti plašas un rūpniecības vertikālēs. Pieteikums ietver vairākas jomas un lapas, kas palīdz veikt dažādus uzdevumus. Lai ātri atrastu lapas, kas nepieciešams, lai pabeigtu savu uzdevumu, izmantot navigācijas meklēšanas funkciju. Lai izmantotu šo līdzekli, noklikšķiniet uz ikonas **Meklēšana**, lai parādītu lodziņu **Meklēšana**. Pēc tam varat ierakstīt lodziņā vienu vai vairākus vārdus. Sistēma uzreiz meklē attiecīgās lapas programmā, kuras atbilst ievadītajiem vārdiem. Piemēram, jūs varat ievadīt “kreditora rēķins”, un pēc tam sistēma parādīs rezultātus, kas atbilst ievadītajam tekstam. **Piezīme.** Lodziņš **Meklēšana** palīdz atrast lapas un pāriet uz tām. Tas nepalīdzēs jums atrast specifiskus datus vai darbības. 

[![meklēšanas lodziņa](./media/search-box.png)](./media/search-box.png) navigācijas meklēšanas līdzeklis, kas kalpo arī kā lielisks veids, lai jūs varētu ātri pārvietoties uz noteiktu lappusi. Piemēram, ja esat apgādes lietvede kurš bieži izmanto **maksājumu žurnāla** lapas, meklēšanas lodziņā var ievadīt "maksājumu žurnāla". Ievade ir precīza atbilsme page title, tāpēc lapas ir uzskaitītas meklēšanas rezultātu lapas augšdaļā, un var viegli naviģēt uz to. 

[![meklēšana pēc maksājumu žurnāls](./media/searching-for-payment-journal.png)](./media/searching-for-payment-journal.png) 

Meklēšanas rezultātu sarakstā tiek parādīts lapas nosaukumu, kā arī navigācijas ceļu. Tas palīdz informēt lietotāju par lapas atrašanās vietu programmā. Tas arī palīdz atšķirt divas vai vairāk līdzīgas lapas rezultātos. Meklējot lapu, ievadītais teksts tiek salīdzināts ar lapas nosaukumu, kā arī tās navigācijas ceļu. Piemēram, ja ievadāt "parāds" * * * * meklēšanas lodziņu, jūs redzēsiet rezultātus lapas pieejamas debitoru kontus rajonā - pat tad, ja lapu nosaukumiem nevar iekļaut vārdus "parāds". 

[![meklēt-uz--vārds-debitoru](./media/search-for-the-word-receivable.png)](./media/search-for-the-word-receivable.png) 

Administrācija un drošības viedokļa, navigācijas meklēšanas funkcionalitāti tikai virsmām:

-   Lapas, kas ir iespējotas pašreizējā konfigurācijā (izmantojot konfigurācijas atslēgas).
-   Lapas, kurām lietotājam ir piekļuve, pamatojoties uz lietotāja lomu.

Meklēšanas rezultātu sarakstā tiek parādīti ne vairāk kā 10 vienumi. Ja jums neizdodas atrast meklēto rezultātos, mēģiniet precizēt vai atjaunināt ievadīto informāciju. No izstrādes viedokļa navigācijas meklēšanas funkcionalitāte ir ļoti viegli izmantojama, jo izvēļņu vienumus ir iespējams parādīt meklēšanas rezultātos gandrīz uzreiz pēc to izvietošanas. Ja uz izvēļņu vienumiem ir izveidota saite no navigācijas rūts vai informācijas paneļa, tie automātiski kļūst meklējami. Navigācijas meklēšanas funkcionalitāte ietver arī pieprasītu līdzekli, kas paredzēts prasmīgiem lietotājiem: iespēju ātri pārvietoties uz lapu, pamatojoties uz tehnisko formas nosaukumu. Daudzi lietotāji ir tik labi pazīstami ar sistēmu, ka viņi zina precīzus to formu nosaukumus, ar kurām tie strādā. Ja esat viens no šiem lietotājiem, jūs varat ievadīt tekstu **forma:** un pēc tam norādīt meklējamās formas nosaukumu. Piemēram, ja ievadāt **forma: vendinvoice**, meklēšanas rezultāti parādīs visas lapas, kurās formas nosaukums sākas ar **vendinvoice**. 

[![meklēšana pēc formas vendinvoice](./media/search-for-form-vendinvoice.png)](./media/search-for-form-vendinvoice.png)


