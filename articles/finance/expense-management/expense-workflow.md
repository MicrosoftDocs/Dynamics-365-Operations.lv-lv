---
title: Izdevumu darbplūsma
description: Šajā tēmā ir paskaidrots, kā varat izmantot darbplūsmu sistēmu programmā Microsoft Dynamics 365 Finance, lai modulī Izdevumu pārvaldība iestatītu izdevumu pārskatu pārbaudes procesu.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c52915860709e38013ec06204c52bb06de417eb1
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187594"
---
# <a name="expense-workflow"></a>Izdevumu darbplūsma

[!include [banner](../includes/banner.md)]

Varat izmantot darbplūsmu sistēmu, lai modulī Izdevumu pārvaldība iestatītu izdevumu pārskatu pārbaudes procesu. Varat iestatīt darbplūsmu, kas izmanto tālāk norādītos kritērijus, lai noteiktu, kurš apstiprina izdevumu pārskatus.

- Darbinieku pārskatu veidošanas hierarhija un sākotnēji definētu apstiprinājumu ierobežojumi
- Vairāku līmeņu apstiprinājums, kas atbalsta pagaidu apstiprinātājus un galīgo apstiprinātāju
- Finanšu dimensijas un projekta atbildība
- Piešķire noteiktiem lietotājiem vai lietotāju grupām

Darbplūsmu apstiprinājumus var izveidot izdevumu pārskatiem, komandējumu pieprasījumiem, skaidras naudas avansiem un pievienotās vērtības nodokļa (PVN) atgūšanai.

**Piemērs**

Nākamais process ir izdevumu pārskatam paredzētas izdevumu pārvaldības darbplūsmas piemērs.

1. Darbinieks izveido un saglabā izdevumu pārskatu.
2. Šis darbinieks izdevumu pārskatu iesniedz apstiprināšanai. Apstiprinātājs tiek identificēts, balstoties uz kārtulām, kuras tika definētas darbplūsmas iestatīšanas laikā.
3. Apstiprinātājs saņem paziņojumu par to, ka izdevumu pārskats ir gatavs apstiprināšanai. Apstiprinātājs pārskata izdevumu pārskatu un apstiprina, ka ir izpildīti tālāk norādītie nosacījumi.

    - Izdevumi nepārkāpj izdevumu politikas. Ja izdevumi pārkāpj politiku, tad apstiprinātājs apstiprina, ka izdevumu pārskats ietver derīgu darījuma pamatojumu.
    - Izdevumu pārskatam ir pievienotas elektroniskās kvītis.

4. Apstiprinātājs apstiprina izdevumu pārskatu.
5. Izdevumu pārskats tiek nodots parādu kreditoriem koordinatoram iegrāmatošanai.
6. Atkarībā no tā, vai ir konfigurēta automātiskā grāmatošana, notiek viena no tālāk norādītajām darbībām.

    - Ja automātiskā grāmatošana ir konfigurēta, tad izdevumu pārskats tiek apstrādāts maksājuma veikšanai un izdevumu pārskata statuss tiek atjaunināts.
    - Ja automātiskā grāmatošana nav konfigurēta, tad parādu kreditoriem koordinators pārbauda, vai ir iesniegtas visas sākotnējās kvītis un vai kvītis saskan ar izdevumu pārskatā norādītajiem izdevumiem. Ir arī jāpārbauda, vai ir pareizi visi izdevumu pārskatā ievadītie nodokļu kodi.

Kad atbilstība šīm prasībām ir pārbaudīta, izdevumu pārskats tiek grāmatots.

Kad izdevumu pārskats ir iegrāmatots, tiek autorizēts maksājums par šo izdevumu pārskatu un darbinieks saņem kompensāciju.
