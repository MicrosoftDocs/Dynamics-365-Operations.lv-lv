---
title: "Izdevumu darbplūsma"
description: "Šajā tēmā ir izskaidrots, kā programmā Microsoft Dynamics 365 for Finance and Operations var izmantot darbplūsmu sistēmu, lai modulī Izdevumu pārvaldība iestatītu izdevumu pārskatu pārskatīšanas procesu."
author: saraschi2
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 6ee607f723659a5b6ecd655ba4fdfca35a4c582d
ms.contentlocale: lv-lv
ms.lasthandoff: 03/26/2018

---

# <a name="expense-workflow"></a>Izdevumu darbplūsma

[!include [banner](../includes/banner.md)]

Programmā Microsoft Dynamics 365 for Finance and Operations var izmantot darbplūsmu sistēmu, lai modulī Izdevumu pārvaldība iestatītu izdevumu pārskatu pārskatīšanas procesu. Varat iestatīt darbplūsmu, kas izmanto tālāk norādītos kritērijus, lai noteiktu, kurš apstiprina izdevumu pārskatus.

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

