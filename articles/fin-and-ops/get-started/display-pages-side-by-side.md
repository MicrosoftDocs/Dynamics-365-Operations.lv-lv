---
title: Lapu parādīšana līdzās, izmantojot līdzekli Atvērt jaunā logā
description: Šajā rakstā ir paskaidrots, kā parādīt lapas līdzās programmā Microsoft Dynamics 365 for Finance and Operations.
author: aneesmsft
manager: AnnBe
ms.date: 09/07/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df9b091735a4971446c5b5d0e054076260040683
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "330176"
---
# <a name="show-pages-side-by-side-by-using-the-open-in-new-window-feature"></a>Parādīt lapas blakus, izmantojot līdzekli Atvērt jaunā logā

[!include [banner](../includes/banner.md)]

Šajā rakstā ir paskaidrots, kā parādīt lapas līdzās programmā Microsoft Dynamics 365 for Finance and Operations.

Microsoft Dynamics 365 for Finance and Operations palīdz efektīvi veikt uzdevumus. Dažos gadījumos, iespējams, vēlēsieties skatīt vairākas lappuses līdzās, lai ātri veiktu uzdevumus. Piemēram, iespējams, vēlēsieties apstiprināt vai ievadīt rindas vairāk nekā vienā žurnālā. Parasti, lai to izdarītu, ir jāpāriet atpakaļ un uz priekšu no lapas, kurā ir parādīts žurnālu saraksts, uz lapu, kurā ir parādītas attiecīgā žurnāla rindas. Tomēr līdzeklis **Atvērt jaunā logā** ļauj parādīt šīs lapas blakus, lai jūs varētu ātri veikt uzdevumus.

Turpinot iepriekš minēto piemēru, skatot rindas, varat noklikšķināt uz ikonas **Atvērt jaunā logā**.

[![open-in-new-window-icon](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)

Noklikšķinot uz ikonas **Atvērt jaunā logā**, rindu lapa tiek atvērta jaunā uznirstošā pārlūkprogrammā, un pēc tam sākotnējā pārlūkprogramma pāriet atpakaļ vēsturē uz lapu, kurā tika rādīts žurnālu saraksts. Pēc tam var parādīt abas lapas līdzas. Kad esat pabeidzis žurnāla skatīšanu, žurnālu saraksta lapā varat mainīt atlasīto žurnālu un rindu lapa uznirstošajā logā automātiski parādīs jaunatlasītā žurnāla rindas.

[![pages-show-side-by-side](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)

Dinamiskā saistīšana un atsvaidzināšana tiek veikta atbilstoši attiecībām, kas pastāv starp datiem, kuri ir šo lapu pamatā. Ja sistēmai nav informācijas par attiecībām starp datiem, uznirstošais logs netiks automātiski atsvaidzināts, reaģējot uz izmaiņām tā izcelsmes logā.

Dažām lapām ir vairāki skati, piemēram, režģa skata, virsrakstu skats un detalizētas informācijas skats. Ikona **Atvērt jaunā logā** atver visu lapu jaunā pārlūkprogrammas logā. Tādēļ nav iespējams saglabāt vienas lapas divus skatus līdzās, izmantojot līdzekli **Atvērt jaunā logā**. Tomēr gandrīz visās šādās lapās ir navigācijas saraksts, ko varat izmantot, lai pārslēgtos starp ierakstiem un sasniegtu līdzīgu pieredzi.

Pirms līdzekļa **Atvērt jaunā logā** lietošanas ir jākonfigurē pārlūkprogrammas uznirstošo elementu bloķētājs tā, lai atļautu uznirstošos elementus no Dynamics 365 for Finance and Operations vietnes URL. Piemēram, varat atļaut uznirstošos elementus no “\*. dynamics.com”.

Līdzeklis **Atvērt jaunā logā** ir pieejams tikai tad, ja logā ir atvērta vairāk nekā viena lapa. Turklāt uznirstošais logs automātiski aizveras, kad vairs nav atvērta neviena lapa (t. i., aizverot pēdējo lappusi attiecīgajā logā). Programmatūrā Dynamics 365 for Finance and Operations atvērtās lapas tiek aizvērtas arī tad, kad pārejat uz citu lietojumprogrammas apgabalu. Tādēļ, ja ir atvērti uznirstošie logi un jūs pārejat uz citu apgabalu programmā, uznirstošie logi tiek automātiski aizvērti, jo sistēma aizvēra lapas attiecīgajos logos.

Uznirstošo logu augšējā joslā ir parādīta informācija par uzņēmumu, kurā lapa tika atvērta, un tā ir tikai lasāma. Turklāt uznirstošie logi ir atkarīgi no galvenā Dynamics 365 for Finance and Operations pārlūkprogrammas loga. Ja galvenais logs tiek aizvērts vai atsvaidzināts, visi atvērtie uznirstošie logi kļūst tikai lasāmi. Tas nozīmē, ka joprojām varat apskatīt informāciju šajos logos, bet nevarēsiet ar to mijiedarboties.
