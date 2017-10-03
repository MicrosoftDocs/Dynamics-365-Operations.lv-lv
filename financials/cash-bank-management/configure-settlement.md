---
title: "Ssegšanas konfigurēšana"
description: "Transakciju segšanas veids un laiks var būt sarežģītas tēmas, tāpēc jums ir svarīgi saprast un pareizi definēt parametrus, lai tie atbilstu jūsu biznesa prasībām. Šajā rakstā ir aprakstīti parametri, kas tiek izmantoti segšanai gan modulim Parādi kreditoriem, gan modulim Debitoru parādi."
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans, CustParameters, VendOpenTrans, VendParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14601
ms.assetid: 6b61e08c-aa8b-40c0-b904-9bca4e8096e7
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 059513de66827aa3a839b9eb06973ec4c1549f73
ms.contentlocale: lv-lv
ms.lasthandoff: 06/13/2017

---

# <a name="configure-settlement"></a>Ssegšanas konfigurēšana

[!include[banner](../includes/banner.md)]


Transakciju segšanas veids un laiks var būt sarežģītas tēmas, tāpēc jums ir svarīgi saprast un pareizi definēt parametrus, lai tie atbilstu jūsu biznesa prasībām. Šajā rakstā ir aprakstīti parametri, kas tiek izmantoti segšanai gan modulim Parādi kreditoriem, gan modulim Debitoru parādi. 

Tālāk norādītie parametri ietekmē to, kā programmatūras Microsoft Dynamics 365 for Finance and Operations izdevumā Enterprise tiek apstrādātas segšanas. Segšana ir rēķina nosegšanas process saistībā ar maksājumu vai kredīta notu. Šie parametri atrodas lapas **Debitoru moduļa parametri** un **Kreditoru moduļa parametri** apgabalā **Segšana**.

-   **Automātiska segšana** — iestatiet šai opcijai **Jā**, ja transakcija ir jāsedz automātiski attiecībā pret citām atvērtajām transakcijām, kad tā tiek grāmatota. Ja šai opcijai tiek iestatīts **Nē**, lietotāji var manuāli nosegt transakcijas, kad tie ievada maksājumus, vai arī vēlāk, izmantojot lapu **Transakciju nosegšana**.
-   **Termiņatlaižu administrēšana** — norādiet, kā [termiņatlaide tiek apstrādāta, ja rēķins ir pārmaksāts](cash-discount-handling-overpayments.md). Pārmaksas gadījumā termiņatlaidi var samazināt, to var apstrādāt kā starpību vai atstāt kreditora vai debitora kontā.
    -   **Nespecifiska** — termiņatlaides summa tiek samazināta atbilstoši pārmaksātajai summai. Šādi vienmēr tiek darīts neatkarīgi no tā, vai pārmaksātā summa ir lielāka vai mazāka par summu, kas tiek ievadīta laukā **Maksimālā pārmaksa vai nepilna samaksa**.
    -   **Specifiska** — pārmaksas summa tiek grāmatota termiņatlaides starpības virsgrāmatas kontā vai paliek kā bilance debitora vai kreditora kontā. Specifiska uzvedība ir atkarīga no tā, vai pārmaksas summa ir starp 0,00 un summu, kas ievadīta laukā **Maksimālā pārmaksa vai nepilna samaksa**, vai arī pārmaksas summa ir lielāka nekā summa laukā **Maksimālā pārmaksa vai nepilna samaksa**.
-   **Maks. sīknaudas starpība** — ievadiet maksimālo atļauto sīknaudas starpību segtajām transakcijām. Ja sīknaudas starpība ir vienāda ar vai mazāka par sīknaudas starpību, kas ir norādīta šajā laukā, tad starpība tiks grāmatota sīknaudas starpības virsgrāmatas kontā, kurš ir norādīts lapā **Automātisko darījumu konti**.
-   **Maksimālā pārmaksa vai nepilna samaksa** — ievadiet pieļaujamo pārmaksas vai nepilnas samaksas summu. Lai aprēķinātu nodokli pārmaksām vai nepilnām samaksām, lapā **Virsgrāmatas parametri** noklikšķiniet uz **PVN** un pēc tam atlasiet opciju **PVN pārmaksa/nepilnai samaksa**.
    -   Ja pārmaksas vai nepilnas samaksas vērtība veido starpību, kas ir mazāka par starpību, kas tika definēta laukā **Maks. sīknaudas starpība**, sīknaudas starpības summa tiek grāmatota sīknaudas starpības kontā.
    -   Ja pārmaksas vai nepilnas samaksas vērtība veido starpību, kas ir lielāka par starpību, kas tika definēta laukā **Maks. sīknaudas starpība**, starpības summa tiek grāmatota starpības kontā, kas tika atlasīts grāmatošanas veidam **Debitora termiņatlaide** vai **Kreditora termiņatlaide** lapā **Automātisko darījumu konti**.
-   **Aprēķināt termiņatlaides daļējiem maksājumiem** — iestatiet šai opcijai **Jā**, lai ļautu automātiski aprēķināt atlaides daļējiem maksājumiem.
    -   Šīs opcijas darbība ir atkarīga no vērtības lapas **Transakciju nosegšana** laukā **Izmantot termiņatlaidi**. Ja šai opcijai ir iestatīts **Jā**, atlaide tiek lietota tad, ja laukam **Izmantot termiņatlaidi** ir iestatīts **Parasts**. Ja laukam **Izmantot termiņatlaidi** ir iestatīts **Vienmēr**, termiņatlaide tiek izmantota vienmēr neatkarīgi no šī lauka iestatījuma. Ja laukam **Izmantot termiņatlaidi** ir iestatīts **Vienmēr**, termiņatlaide tiek izmantota vienmēr neatkarīgi no šī lauka iestatījuma.
    -   Ja šai opcijai ir iestatīts **Jā**, un lietotājs maina vērtību lapas **Transakciju nosegšana** laukā **Nosedzamā summa**, atlaide tiek automātiski aprēķināta un parādīta kā noklusējuma ieraksts laukā **Ņemamā termiņatlaides summa**.
    -   Ja šai opcijai ir iestatīts **Nē**, un lietotājs maina vērtību lapas **Transakciju nosegšana** laukā **Nosedzamā summa** page, laukā **Ņemamā termiņatlaides summa** noklusējuma ieraksts ir **0** (nulle).
-   **Aprēķināt termiņatlaides kredīta notām** — iestatiet šai opcijai **Jā**, lai automātiski aprēķinātu termiņatlaides kredīta notām. Sadaļā Debitori kredīta notas transakcija ir negatīva transakcija, kurai ir vērtība lapas **Brīva teksta rēķins** laukā **Rēķins** vai atgriešana lapā **Pārdošanas pasūtījums**.
    -   Šīs opcijas darbība ir atkarīga no vērtības lapas **Transakciju nosegšana** laukā **Izmantot termiņatlaidi**. Ja šai opcijai ir norādīta vērtība **Jā**, tad atlaide tiek lietota tad, ja laukam ****Izmantot termiņatlaidi**** ir iestatīts **Parasts**. Ja laukam ****Izmantot termiņatlaidi**** ir norādīta vērtība **Vienmēr**, tad termiņatlaide tiek izmantota vienmēr neatkarīgi no šī lauka iestatījuma. Ja laukam ****Izmantot termiņatlaidi**** ir norādīta vērtība **Nekad**, tad termiņatlaide nekad netiek izmantota neatkarīgi no šī lauka iestatījuma.
    -   Ja šai opcijai ir iestatīts **Jā**, un kredīta nota ir atzīmēta lapā **Transakciju nosegšana**, tad atlaide tiek automātiski aprēķināta un parādīta kā noklusējuma ieraksts laukā **Ņemamā termiņatlaides summa**.
    -   Ja šai opcijai ir iestatīts **Nē**, un kredīta nota ir atzīmēta lapā **Transakciju nosegšana**, noklusējuma ieraksts laukā **Ņemamā termiņatlaides summa** ir **0** (nulle).
-   **Atlaižu korespondējošie konti (tikai kreditoriem)** — definējiet noklusējuma termiņatlaides virsgrāmatas kontu, kas ir jāizmanto termiņatlaižu uzskaites ierakstiem.
    -   **Izmantot galveno kontu kreditoru atlaidēm** — termiņatlaide tiek grāmatota galvenajā kontā, kas ir definēts lapā **Termiņatlaides iestatījumi**.
    -   **Konti rēķina rindās** — termiņatlaide tiek grāmatota Virsgrāmatas kontos sākotnējā rēķinā.
-   **Atzīmēt līnijas brīva teksta rēķinos un procentu paziņojumos (tikai kreditoriem)** — iestatiet šai opcijai **Jā**, lai iespējotu pogu **Atzīmēt rēķina rindas** lapā **Ievadīt debitora maksājumus**, **Maksājumu žurnāla dokuments** un **Transakciju nosegšana**. Šī poga ļauj lietotājiem atzīmēt atsevišķas rindas nosegšanai.
-   **Noteikt segšanai prioritāti (tikai kreditoriem)** — iestatiet šai opcijai **Jā**, lai iespējotu pogu **Atzīmēt pēc prioritātes** lapā **Ievadīt debitora maksājumus** un **Transakciju nosegšana**. Šī poga lietotājiem ļauj piešķirt iepriekš definētu transakciju segšanas kārtību.  Ja transakcijai tika izmantota segšanas kārtība, tad pirms grāmatošanas šo kārtību un maksājuma sadalījumu var modificēt.
-   **Izmantot prioritāti automātiskai segšanai** — šīs opcijas vērtību iestatiet uz **Jā**, lai transakciju automātiskās segšanas laikā izmantotu definēto prioritāšu secību. Šis lauks ir pieejams tikai tad, ja opcijai **Noteikt segšanai prioritāti** un **Automātiska segšana** ir norādīta vērtība **Jā**.





