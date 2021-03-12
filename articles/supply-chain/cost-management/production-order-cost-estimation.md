---
title: Ražošanas pasūtījuma izmaksu novērtējums
description: Šajā rakstā ir sniegta informācija par ražošanas izmaksu novērtējumu. Ražošanas izmaksu novērtējums sniedz plānotajam ražošanas pasūtījuma daudzumam paredzētās krājuma ražošanas materiālu un veiktspējas patēriņa izmaksas.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMCalcTrans, InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 80633
ms.assetid: b4625d10-c852-4fda-b718-79df458de0d4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 53f54c64b1c78e7385f0fde5ad1023c5b4e0af4f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967312"
---
# <a name="production-order-cost-estimation"></a>Ražošanas pasūtījuma izmaksu novērtējums

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegta informācija par ražošanas izmaksu novērtējumu. Ražošanas izmaksu novērtējums sniedz plānotajam ražošanas pasūtījuma daudzumam paredzētās krājuma ražošanas materiālu un veiktspējas patēriņa izmaksas. 

Kad ir izveidots ražošanas pasūtījums, jums ir jānovērtē ražošanas izmaksas. Nolūks ir novērtēt krājumu un maršruta patēriņu attiecīgajam ražošanas procesam, jo šie novērtējumi tiek izmantoti turpmāko plānošanas un ražošanas procesu pamatā.

## <a name="production-cost-estimation"></a>Ražošanas izmaksu novērtējums
Ražošanas izmaksu novērtējumi ir balstīti uz tālāk uzskaitīto informāciju.

-   Ražošanas pasūtījuma daudzums
-   Ražošanas materiālu komplektu (MK) komponenti
-   Ražošanas maršrutā iekļautās maršrutēšanas operācijas
-   Netiešās izmaksas, kas attiecas uz komponentiem un operācijām
-   Aktīvo izmaksu dati aprēķina datumā

Ja ražošanas materiālu komplektos (MK) pastāv fantoma rindas krājums, tad aprēķini atspoguļo fantoma komponentus un maršruta operācijas. Novērtēšanas uzdevumu varat izmantot novērtēto izmaksu pārrēķināšanai, lai tās atspoguļotu atjaunināto informāciju. Piemēram, atjauninātā informācija varētu būt izmaiņas ražošanas pasūtījuma daudzumā, ražošanas MK komponentos, maršrutēšanas operācijās ražošanas maršrutā, uz šiem komponentiem un operācijām attiecinātajās netiešajās izmaksās, vai aktīvajiem izmaksu datiem pārrēķina datumā. Novērtēto izmaksu aprēķini var tikt izmantoti arī ražotā krājuma ieteicamās pārdošanas cenas noteikšanai, izmantojot metodi izmaksas-plus-uzcenojums. Novērtēto izmaksu aprēķinus pēc izvēles var izmantot, lai atsauktos uz pasūtījumiem, kas atspoguļo citus ar šo ražošanas pasūtījumu saistītos ražošanas pasūtījumus.

## <a name="view-the-estimated-costs"></a>Skatīt novērtētās izmaksas
Kad ir izpildīta novērtēšana, rezultātus varat skatīt lapā **Cenas aprēķins**. Novērtēšanā tiek aprēķinātas tālāk uzskaitītās vērtības.

-   **Ražošanas izmaksas** — ražošanas izmaksas ir novērtējuma augšējā rinda. Tā parāda kopējās ražošanas pasūtījuma realizācijas izmaksas un kopējo ražojuma pārdošanas cenu. Tā ir visu novērtējuma izmaksu rindu kopsumma.
-   **Maršruta vai resursu izmaksas** — maršruta vai resursu izmaksas ir izmaksas par ražošanas operācijām. Tās ietver izmaksas par tādiem elementiem kā uzstādīšanas laiks, izpildlaiks un pieskaitāmās izmaksas.
-   **Materiālu izmaksas** — materiālu izmaksas ir krājuma ražošanai nepieciešamā materiālu komplekta (MK) komponentu izmaksas un cenas. Šīs izmaksas ir noteiktas un sistēmā ievadītas jau iepriekš.

## <a name="other-uses-of-cost-estimation"></a>Citi izmaksu novērtējuma lietojumi
Izmaksu novērtējums sniedz arī tālāk uzskaitīto informāciju.

-   Jēgpilni cenu piedāvājumi
-   Pasūtījuma rentabilitātes novērtējumi
-   Izejmateriālu lietojuma novērtējumi
-   Cenu informācijas salīdzinājumu no iepriekšējās ražošanas
-   Budžeta un prognozēšanas informācija
-   Noteiktas cenas uzturēšanai nepieciešamo ražošanas apmēru novērtējumi




