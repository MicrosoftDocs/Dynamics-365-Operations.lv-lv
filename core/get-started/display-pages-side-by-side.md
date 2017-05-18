---
title: "Parādīt lapas līdzās, izmantojot ikonu Atvērt jaunā logā"
description: "Šajā rakstā ir paskaidrots, kā programmatūrā Microsoft Dynamics 365 for Operations lapas parādīt vienu otrai līdzās."
author: aneesmsft
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: e29d436560590e844e92180a6d1e2ad53d019662
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="display-pages-side-by-side-using-the-open-in-new-window-icon"></a>Parādīt lapas līdzās, izmantojot ikonu Atvērt jaunā logā

[!include[banner](../includes/banner.md)]


Šajā rakstā ir paskaidrots, kā programmatūrā Microsoft Dynamics 365 for Operations lapas parādīt vienu otrai līdzās.

Microsoft Dynamics 365 for Operations jums palīdz uzdevumus izpildīt efektīvi. Dažos gadījumos, iespējams, vēlēsieties skatīt vairākas lappuses līdzās, lai ātri veiktu uzdevumus. Piemēram, iespējams, vēlēsieties apstiprināt vai ievadīt rindas vairāk nekā vienā žurnālā. Parasti, lai to izdarītu, ir jāpāriet atpakaļ un uz priekšu no lapas, kurā ir parādīts žurnālu saraksts, uz lapu, kurā ir parādītas attiecīgā žurnāla rindas. Tomēr līdzeklis **Atvērt jaunā logā** ļauj parādīt šīs lapas blakus, lai jūs varētu ātri veikt uzdevumus. Turpinot iepriekš minēto piemēru, skatot rindas, varat noklikšķināt uz ikonas **Atvērt jaunā logā**. [![open-in-new-window-icon](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png) Noklikšķinot uz ikonas **Atvērt jaunā logā**, rindu lapa tiek atvērta jaunā uznirstošā pārlūkprogrammā un pēc tam sākotnējā pārlūkprogramma pāriet atpakaļ vēsturē uz lapu, kurā tika rādīts žurnālu saraksts. Pēc tam var parādīt abas lapas līdzas. Kad esat pabeidzis žurnāla skatīšanu, žurnālu saraksta lapā varat mainīt atlasīto žurnālu un rindu lapa uznirstošajā logā automātiski parādīs jaunatlasītā žurnāla rindas. [![pages-show-side-by-side](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png) Dinamiskā saistīšana un atsvaidzināšana tiek veikta atbilstoši attiecībām, kas pastāv starp datiem, kuri ir šo lapu pamatā. Ja sistēmai nav informācijas par attiecībām starp datiem, uznirstošais logs netiks automātiski atsvaidzināts, reaģējot uz izmaiņām tā izcelsmes logā. Dažām lapām ir vairāki skati, piemēram, režģa skata, virsrakstu skats un detalizētas informācijas skats. Ikona **Atvērt jaunā logā** atver visu lapu jaunā pārlūkprogrammas logā. Tādēļ nav iespējams saglabāt vienas lapas divus skatus līdzās, izmantojot līdzekli **Atvērt jaunā logā**. Tomēr gandrīz visās šādās lapās ir navigācijas saraksts, ko varat izmantot, lai pārslēgtos starp ierakstiem un sasniegtu līdzīgu pieredzi. Pirms izmantojat līdzekli **Atvērt jaunā logā**, ir nepieciešams konfigurēt pārlūkprogrammas uznirstošo elementu bloķētāju, lai tas atļautu uznirstošos elementus no Dynamics 365 for Operations vietnes URL. Piemēram, varat atļaut uznirstošos elementus no “\*. dynamics.com”. Līdzeklis **Atvērt jaunā logā** ir pieejams tikai tad, ja logā ir atvērta vairāk nekā viena lapa. Turklāt uznirstošais logs automātiski aizveras, kad vairs nav atvērta neviena lapa (t. i., aizverot pēdējo lappusi attiecīgajā logā). Programmatūra Dynamics 365 for Operations arī aizver atvērtas lapas, kad pārejat uz citu apgabalu programmā. Tādēļ, ja ir atvērti uznirstošie logi un jūs pārejat uz citu apgabalu programmā, uznirstošie logi tiek automātiski aizvērti, jo sistēma aizvēra lapas attiecīgajos logos. Uznirstošo logu augšējā joslā ir parādīta informācija par uzņēmumu, kurā lapa tika atvērta, un tā ir tikai lasāma. Uznirstošie logi arī balstās uz galveno Dynamics 365 for Operations pārlūkprogrammas logu. Ja galvenais logs tiek aizvērts vai atsvaidzināts, visi atvērtie uznirstošie logi kļūst tikai lasāmi. Tas nozīmē, ka joprojām varat apskatīt informāciju šajos logos, bet nevarēsiet ar to mijiedarboties.




