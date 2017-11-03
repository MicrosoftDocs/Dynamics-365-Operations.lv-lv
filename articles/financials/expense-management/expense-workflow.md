---
title: "Izdevumu darbplūsma"
description: "Šajā tēmā ir skaidrots, kā programmatūrā Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition varat izmantot darbplūsmu sistēmu, lai modulī Izdevumu pārvaldība iestatītu pārskatīšanas procesu izdevumu pārskatiem."
author: saraschi2
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi2
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2c2e01d4da04cd24c2df1690e6e354e1c03cb50d
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="expense-workflow"></a>Izdevumu darbplūsma

[!include[banner](../includes/banner.md)]

Programmatūrā Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition varat izmantot darbplūsmu sistēmu, lai modulī Izdevumu pārvaldība iestatītu pārskatīšanas procesu izdevumu pārskatiem. Varat iestatīt darbplūsmu, kas izmanto tālāk norādītos kritērijus, lai noteiktu, kurš apstiprina izdevumu pārskatus.

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

