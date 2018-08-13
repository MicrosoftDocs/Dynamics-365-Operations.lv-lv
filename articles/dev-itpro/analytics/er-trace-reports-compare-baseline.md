---
title: "Ģenerēto pārskatu rezultātu izsekošana un to salīdzināšana ar bāzlīnijas vērtībām"
description: "Šajā tēmā ir sniegta informācija par to, kā ģenerēto ER pārskatu rezultātus varat salīdzināt ar bāzlīnijas pārskata vērtībām."
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 2fc887668171175d436b9eb281a35c1c9d089591
ms.openlocfilehash: 1a598d0bd053c60c3f8df6b05ecb7ff15addfaa3
ms.contentlocale: lv-lv
ms.lasthandoff: 08/09/2018

---

# <a name="trace-generated-report-results-and-compare-them-with-baseline-values"></a>Ģenerēto pārskatu rezultātu izsekošana un to salīdzināšana ar bāzlīnijas vērtībām

[!include[banner](../includes/banner.md)]

Varat izsekot tādu ER formātu rezultātus, kas ģenerē izejošos elektroniskos dokumentus. Kad izsekošanas ģenerēšana ir ieslēgta (ER lietotāja parametrs **Palaist atkļūdošanas režīmā**), ER formāta izpildes žurnālā tiek ģenerēts jauns izsekošanas ieraksts katru reizi, kad tiek palaists ER pārskats. Katrā ģenerētajā izsekošanas reizē tiek saglabāta tālāk norādītā informācija.

- Visi brīdinājumi, ko ģenerēja validēšanas kārtulas
- Visas kļūdas, ko ģenerēja validēšanas kārtulas
- Visi ģenerētie faili, kas tiek saglabāti kā izsekošanas ieraksta pielikumi

Varat glabāt atsevišķus bāzlīnijas programmas failus jebkuram ER formātam. Faili tiek uzskatīti par bāzlīnijas failiem, ja tie apraksta palaisto pārskatu gaidītos rezultātus. Ja bāzlīnijas fails ir pieejams kādam ER formātam, kas tika palaists, kamēr bija ieslēgta izsekošanas ģenerēšana, tad papildus iepriekš minētajai informācijai izsekošana saglabā arī rezultātus no ģenerētā elektroniskā dokumenta salīdzinājuma ar bāzlīnijas failu. Ar vienu klikšķi šo ģenerēto elektronisko dokumentu un tā bāzlīnijas failu varat arī saņemt vienā zip failā. Pēc tam varat veikt detalizētu salīdzināšanu, izmantojot kādu ārēju rīku, piemēram, Windiff.

Varat novērtēt izsekošanu, lai analizētu, vai ģenerētajos elektroniskajos dokumentos ir gaidītais saturs. Šo novērtēšanu varat veikt lietotāju akcepttestēšanas (User Acceptance Testing — UAT) vidē, ja koda bāze ir mainīta (piemēram, ja veicāt migrēšanu uz jaunu programmas instanci, instalējāt labojumfailu pakotnes vai izvietojāt koda modifikācijas). Šādi varat pārliecināties, vai novērtējums neietekmē izmantoto ER pārskatu izpildi. Daudziem ER pārskatiem novērtēšanu var veikt neuzraudzītā režīmā.

Lai par šo līdzekli uzzinātu vairāk, noskatieties uzdevumu ceļvežus **ER Pārskatu ģenerēšana un rezultātu salīdzināšana (1. daļa)** un **ER Pārskatu ģenerēšana un rezultātu salīdzināšana (2. daļa)**, kas veido daļu no biznesa procesa **7.5.4.3 IT pakalpojumu/risinājumu testēšana (10679)** un ko var lejupielādēt no [Microsoft lejupielādes centra](https://go.microsoft.com/fwlink/?linkid=874684). Šajos uzdevumu ceļvežos ir izklāstīts ER struktūras konfigurēšanas process, lai izmantotu bāzlīnijas failus ģenerēto elektronisko dokumentu novērtēšanai.

