---
title: Parādīt lapas blakus, izmantojot līdzekli Atvērt jaunā logā
description: Šajā rakstā ir paskaidrots, kā parādīt lapas līdzās.
author: jasongre
ms.date: 11/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.openlocfilehash: bfc2aa534da17529421af0a28d1c90ee3aeb40cb
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288637"
---
# <a name="show-pages-side-by-side-using-the-open-in-new-window-feature"></a>Parādīt lapas blakus, izmantojot līdzekli Atvērt jaunā logā

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Šajā rakstā ir paskaidrots, kā parādīt lapas līdzās.

Iespējams, vēlēsieties skatīt vairākas lappuses līdzās, lai ātri veiktu uzdevumus. Piemēram, iespējams, vēlēsieties apstiprināt vai ievadīt rindas vairāk nekā vienā žurnālā. Parasti, lai validētu vai ievadītu rindas vairāk kā vienā žurnāla, būtu jāpāriet uz priekšu un atpakaļ starp lapu, kurā ir parādīts žurnālu saraksts, un lapu, kurā ir parādītas attiecīgā žurnāla rindas. Tomēr līdzeklis **Atvērt jaunā logā** ļauj parādīt šīs lapas blakus, lai jūs varētu ātri veikt uzdevumus.

Turpinot iepriekš minēto piemēru, skatot rindas, varat noklikšķināt uz ikonas **Atvērt jaunā logā**.

[![Ikonas Atvērt jaunā logā noklikšķināšana.](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)

Noklikšķinot uz ikonas **Atvērt jaunā logā**, rindu lapa tiek atvērta jaunā uznirstošā pārlūkprogrammā, un pēc tam sākotnējā pārlūkprogramma pāriet atpakaļ vēsturē uz lapu, kurā tika rādīts žurnālu saraksts. Pēc tam var parādīt abas lapas līdzās. Kad esat pabeidzis žurnāla skatīšanu, žurnālu saraksta lapā varat mainīt atlasīto žurnālu un rindu lapa uznirstošajā logā automātiski parādīs jaunatlasītā žurnāla rindas.

[![Lapu parādīšana blakus.](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)

Dinamiskā saistīšana un atsvaidzināšana tiek veikta atbilstoši attiecībām, kas pastāv starp datiem, kuri ir šo lapu pamatā. Ja sistēmai nav informācijas par attiecībām starp datiem, uznirstošais logs netiks automātiski atsvaidzināts, reaģējot uz izmaiņām tā izcelsmes logā.

Dažām lapām ir vairāki skati, piemēram, režģa skata, virsrakstu skats un detalizētas informācijas skats. Ikona **Atvērt jaunā logā** atver visu lapu jaunā pārlūkprogrammas logā. Tādēļ nav iespējams saglabāt vienas lapas divus skatus līdzās, izmantojot līdzekli **Atvērt jaunā logā**. Tomēr gandrīz visās šādās lapās ir navigācijas saraksts, ko varat izmantot, lai pārslēgtos starp ierakstiem un sasniegtu līdzīgu pieredzi.

Pirms izmantojat līdzekli **Atvērt jaunā logā**, ir nepieciešams konfigurēt pārlūkprogrammas uznirstošo elementu bloķētāju, lai tas atļautu uznirstošos elementus no vietnes URL. Piemēram, varat atļaut uznirstošos elementus no “\*. dynamics.com”.

Līdzeklis **Atvērt jaunā logā** ir pieejams tikai tad, ja logā ir atvērta vairāk nekā viena lapa. Turklāt uznirstošais logs automātiski aizveras, kad vairs nav atvērta neviena lapa (t.i., aizverot pēdējo lappusi attiecīgajā logā). Sistēma arī aizver atvērtās lapas, kad pārejat uz citu programmas apgabalu. Tādēļ, ja ir atvērti uznirstošie logi un jūs pārejat uz citu apgabalu programmā, uznirstošie logi tiek automātiski aizvērti, jo sistēma aizvēra lapas attiecīgajos logos.

Uznirstošo logu augšējā joslā ir parādīta informācija par uzņēmumu, kurā lapa tika atvērta, un tā ir tikai lasāma. Uznirstošie logi ir atkarīgi arī no pārlūkprogrammas galvenā loga. Ja galvenais logs tiek aizvērts vai atsvaidzināts, visi atvērtie uznirstošie logi kļūst tikai lasāmi. Šādā situācijā joprojām varat apskatīt informāciju šajos logos, bet nevarēsiet ar to mijiedarboties.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
