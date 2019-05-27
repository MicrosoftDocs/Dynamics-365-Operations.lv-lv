---
title: Segšanas konfigurēšana
description: Transakciju segšanas veids un laiks var būt sarežģītas tēmas, tāpēc jums ir svarīgi saprast un pareizi definēt parametrus, lai tie atbilstu jūsu biznesa prasībām. Šajā tēmā ir aprakstīti parametri, kas tiek izmantoti segšanai gan modulim Parādi kreditoriem, gan modulim Debitoru parādi.
author: kweekley
manager: AnnBe
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, CustParameters, VendOpenTrans, VendParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14601
ms.assetid: 6b61e08c-aa8b-40c0-b904-9bca4e8096e7
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1361bce94f6542112cf29e369f2238f211d0647e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1561560"
---
# <a name="configure-settlement"></a>Segšanas konfigurēšana

[!include [banner](../includes/banner.md)]

Transakciju segšanas veids un laiks var būt sarežģītas tēmas, tāpēc jums ir svarīgi saprast un pareizi definēt parametrus, lai tie atbilstu jūsu biznesa prasībām. Šajā tēmā ir aprakstīti parametri, kas tiek izmantoti segšanai gan modulim Parādi kreditoriem, gan modulim Debitoru parādi. 

Segšanu apstrādi programmā Microsoft Dynamics 365 for Finance and Operations ietekmē tālāk norādītie parametri. Segšana ir rēķina nosegšanas process saistībā ar maksājumu vai kredīta notu. Šie parametri atrodas lapas **Debitoru moduļa parametri** un **Kreditoru moduļa parametri** apgabalā **Segšana**.

- **Automātiska segšana** — iestatiet šai opcijai **Jā**, ja transakcija ir jāsedz automātiski attiecībā pret citām atvērtajām transakcijām, kad tā tiek grāmatota. Ja šai opcijai tiek iestatīts **Nē**, lietotāji var manuāli nosegt transakcijas, kad tie ievada maksājumus, vai arī vēlāk, izmantojot lapu **Transakciju nosegšana**.
- **Termiņatlaižu administrēšana** — norādiet, kā [termiņatlaide tiek apstrādāta, ja rēķins ir pārmaksāts](cash-discount-handling-overpayments.md). Pārmaksas gadījumā termiņatlaidi var samazināt, to var apstrādāt kā starpību vai atstāt kreditora vai debitora kontā.
  -   **Nespecifiska** — termiņatlaides summa tiek samazināta atbilstoši pārmaksātajai summai. Šādi vienmēr tiek darīts neatkarīgi no tā, vai pārmaksātā summa ir lielāka vai mazāka par summu, kas tiek ievadīta laukā **Maksimālā pārmaksa vai nepilna samaksa**.
  -   **Specifiska** — pārmaksas summa tiek grāmatota termiņatlaides starpības virsgrāmatas kontā vai paliek kā bilance debitora vai kreditora kontā. Specifiska uzvedība ir atkarīga no tā, vai pārmaksas summa ir starp 0,00 un summu, kas ievadīta laukā **Maksimālā pārmaksa vai nepilna samaksa**, vai arī pārmaksas summa ir lielāka nekā summa laukā **Maksimālā pārmaksa vai nepilna samaksa**.
- **Maks. sīknaudas starpība** — ievadiet maksimālo atļauto sīknaudas starpību segtajām transakcijām. Ja sīknaudas starpība ir vienāda ar vai mazāka par sīknaudas starpību, kas ir norādīta šajā laukā, tad starpība tiks grāmatota sīknaudas starpības virsgrāmatas kontā, kurš ir norādīts lapā **Automātisko darījumu konti**.
- **Maksimālā pārmaksa vai nepilna samaksa** — ievadiet pieļaujamo pārmaksas vai nepilnas samaksas summu. Lai aprēķinātu nodokli pārmaksām vai nepilnām samaksām, lapā **Virsgrāmatas parametri** noklikšķiniet uz **PVN** un pēc tam atlasiet opciju **PVN pārmaksa/nepilnai samaksa**.
  -   Ja pārmaksas vai nepilnas samaksas vērtība veido starpību, kas ir mazāka par starpību, kas tika definēta laukā **Maks. sīknaudas starpība**, sīknaudas starpības summa tiek grāmatota sīknaudas starpības kontā.
  -   Ja pārmaksas vai nepilnas samaksas vērtība veido starpību, kas ir lielāka par starpību, kas tika definēta laukā **Maks. sīknaudas starpība**, starpības summa tiek grāmatota starpības kontā, kas tika atlasīts grāmatošanas veidam **Debitora termiņatlaide** vai **Kreditora termiņatlaide** lapā **Automātisko darījumu konti**.
- **Aprēķināt termiņatlaides daļējiem maksājumiem** — iestatiet šai opcijai **Jā**, lai ļautu automātiski aprēķināt atlaides daļējiem maksājumiem.
  -   Šīs opcijas darbība ir atkarīga no vērtības lapas **Transakciju nosegšana** laukā **Izmantot termiņatlaidi**. Ja šai opcijai ir iestatīts **Jā**, atlaide tiek lietota tad, ja laukam **Izmantot termiņatlaidi** ir iestatīts **Parasts**. Ja laukam **Izmantot termiņatlaidi** ir iestatīts **Vienmēr**, termiņatlaide tiek izmantota vienmēr neatkarīgi no šī lauka iestatījuma. Ja laukam **Izmantot termiņatlaidi** ir iestatīts **Vienmēr**, termiņatlaide tiek izmantota vienmēr neatkarīgi no šī lauka iestatījuma.
  -   Ja šai opcijai ir iestatīts **Jā**, un lietotājs maina vērtību lapas **Transakciju nosegšana** laukā **Nosedzamā summa**, atlaide tiek automātiski aprēķināta un parādīta kā noklusējuma ieraksts laukā **Ņemamā termiņatlaides summa**.
  -   Ja šai opcijai ir iestatīts **Nē**, un lietotājs maina vērtību lapas **Transakciju nosegšana** laukā **Nosedzamā summa** page, laukā **Ņemamā termiņatlaides summa** noklusējuma ieraksts ir **0** (nulle).
- **Aprēķināt termiņatlaides kredīta notām** — iestatiet šai opcijai **Jā**, lai automātiski aprēķinātu termiņatlaides kredīta notām. Sadaļā Debitori kredīta notas transakcija ir negatīva transakcija, kurai ir vērtība lapas **Brīva teksta rēķins** laukā **Rēķins** vai atgriešana lapā **Pārdošanas pasūtījums**.
  - Šīs opcijas darbība ir atkarīga no vērtības lapas <strong>Transakciju nosegšana</strong> laukā <strong>Izmantot termiņatlaidi</strong>. Ja šai opcijai ir iestatīts <strong>Jā</strong>, atlaide tiek lietota tad, ja laukam *<strong><em>Izmantot termiņatlaidi</em></strong>* ir iestatīts <strong>Parasts</strong>. Ja laukam *<strong><em>Izmantot termiņatlaidi</em></strong>* ir norādīta vērtība <strong>Vienmēr</strong>, tad termiņatlaide tiek izmantota vienmēr neatkarīgi no šī lauka iestatījuma. Ja laukam *<strong><em>Izmantot termiņatlaidi</em></strong>* ir norādīta vērtība <strong>Nekad</strong>, tad termiņatlaide nekad netiek izmantota neatkarīgi no šī lauka iestatījuma.
  - Ja šai opcijai ir iestatīts **Jā**, un kredīta nota ir atzīmēta lapā **Transakciju nosegšana**, tad atlaide tiek automātiski aprēķināta un parādīta kā noklusējuma ieraksts laukā **Ņemamā termiņatlaides summa**.
  - Ja šai opcijai ir iestatīts **Nē**, un kredīta nota ir atzīmēta lapā **Transakciju nosegšana**, noklusējuma ieraksts laukā **Ņemamā termiņatlaides summa** ir **0** (nulle).

- **Atlaižu korespondējošie konti (tikai kreditoriem)** — definējiet noklusējuma termiņatlaides virsgrāmatas kontu, kas ir jāizmanto termiņatlaižu uzskaites ierakstiem.
  -   **Izmantot galveno kontu kreditoru atlaidēm** — termiņatlaide tiek grāmatota galvenajā kontā, kas ir definēts lapā **Termiņatlaides iestatījumi**.
  -   **Konti rēķina rindās** — termiņatlaide tiek grāmatota Virsgrāmatas kontos sākotnējā rēķinā.
- **Atzīmēt līnijas brīva teksta rēķinos un procentu paziņojumos (tikai kreditoriem)** — iestatiet šai opcijai **Jā**, lai iespējotu pogu **Atzīmēt rēķina rindas** lapā **Ievadīt debitora maksājumus**, **Maksājumu žurnāla dokuments** un **Transakciju nosegšana**. Šī poga ļauj lietotājiem atzīmēt atsevišķas rindas nosegšanai.
- **Noteikt segšanai prioritāti (tikai kreditoriem)** — iestatiet šai opcijai **Jā**, lai iespējotu pogu **Atzīmēt pēc prioritātes** lapā **Ievadīt debitora maksājumus** un **Transakciju nosegšana**. Šī poga lietotājiem ļauj piešķirt iepriekš definētu transakciju segšanas kārtību.  Ja transakcijai tika izmantota segšanas kārtība, tad pirms grāmatošanas šo kārtību un maksājuma sadalījumu var modificēt.
- **Izmantot prioritāti automātiskai segšanai** — šīs opcijas vērtību iestatiet uz **Jā**, lai transakciju automātiskās segšanas laikā izmantotu definēto prioritāšu secību. Šis lauks ir pieejams tikai tad, ja opcijai **Noteikt segšanai prioritāti** un **Automātiska segšana** ir norādīta vērtība **Jā**.

## <a name="fixed-dimensions-on-accounts-receivableaccounts-payable-main-accounts"></a>Fiksētas dimensijas debitoru parādu/parādu kreditoriem galvenajos kontos

Kad fiksētas dimensijas tiek lietotas debitoru parādu/parādu kreditoriem galvenajā kontā, ar segšanas procesu tiek grāmatoti papildu uzskaites ieraksti un divas papildu kreditoru transakcijas. Segšana salīdzina debitoru parādu/parādu kreditoriem virsgrāmatas kontu no rēķina un maksājuma.  Kad maksājums un segšana tiek pabeigti kopā — kā tas notiek parasti —, maksājuma uzskaites ieraksts virsgrāmatā tiek grāmatots tikai pēc tam, kad ir pabeigts arī šis segšanas process. Notikumu apstrādes secības dēļ segšana no maksājuma uzskaites ieraksta nespēj noteikt faktisko debitoru parādu/parādu kreditoriem virsgrāmatas kontu. Segšana rekonstruē to, kas būs virsgrāmatas konts šim maksājumam. Tas izraisa problēmu, ja debitoru parādu/parādu kreditoriem galvenajam kontam tiek izmantota fiksēta dimensija.

Lai rekonstruētu virsgrāmatas kontu, debitoru parādu/parādu kreditoriem galvenais konts tiek izgūts no grāmatošanas metodes un finanšu dimensijas tiek izgūtas no kreditora transakcijas ieraksta šim maksājumam, kā definēts maksājumu žurnālā. Fiksētās dimensijas netiek pēc noklusējuma lietotas maksājumu žurnāliem, tā vietā tās tiek piemērotas galvenajam kontam kā grāmatošanas procesa pēdējais posms. Līdz ar to fiksētās dimensijas vērtība, visticamāk, nav ietverta kreditora transakcijā, izņemot gadījumus, kad tā pēc noklusējuma tiek izmantota no cita avota, piemēram, kreditora. Rekonstruētajā kontā nav ietverta fiksētā dimensija. Segšanas apstrāde konstatē, ka ir jāizveido pielāgošanas ieraksts, jo rēķins tika iegrāmatots ar fiksētu dimensijas vērtību, bet rekonstruētais maksājumu konts netika.  Segšanai turpinoties ar pielāgošanas ieraksta grāmatošanu, grāmatošanas pēdējais posms ir paredzēts fiksētajai dimensijai, kas tiks lietota. Pielāgošanas ierakstam pievienojot fiksēto dimensiju, tas tiek iegrāmatots ar debetu un kredītu tajā pašā virsgrāmatas kontā. Segšana nevar veikt uzskaites ieraksta atriti.

Lai izvairītos no papildu uzskaites ierakstiem, debetu un kredītu tajā pašā virsgrāmatas kontā, ir jāapsver iespēja izmantot tālāk aprakstītās metodes, ņemot vērā jūsu uzņēmuma vajadzības. 

-   Bieži vien organizācijas izmanto fiksētas dimensijas, lai nullētu finanšu dimensiju, kas nav nepieciešama. Parasti tas attiecas uz bilances kontiem, piemēram, debitoru parādiem/parādiem kreditoriem. Kontu struktūras var izmantot, lai neizsekotu finanšu dimensijas, kas parasti tiek nullētas.  Varat noņemt finanšu dimensiju bilances kontiem, likvidējot nepieciešamību izmantot fiksētas dimensijas.
-   Ja jūsu organizācijai ir nepieciešamas fiksētas dimensijas debitoru parādu/parādu kreditoriem galvenajā kontā, atrodiet veidu, kā fiksētās dimensijas pēc noklusējuma lietot maksājumam, lai fiksētās dimensijas vērtība tiktu glabāta kreditora transakcijā šim maksājumam. Tādējādi sistēma var rekonstruēt debitoru parādu/parādu kreditoriem galveno kontu, lai ietvertu fiksētās dimensijas vērtības. Fiksētās dimensijas vērtību var definēt kā noklusējuma vērtību kreditoriem vai žurnāla nosaukumam maksājumu žurnālā.
