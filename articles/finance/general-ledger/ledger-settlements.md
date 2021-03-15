---
title: Virsgrāmatas darbību sasaistīšana
description: Šajā tēmā ir paskaidrots, kā izmantot virsgrāmatas darbību sasaistīšanas lapu, lai segtu virsgrāmatas transakcijas un anulētu nosegšanu.
author: mikefalkner
manager: aolson
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransSettlement
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-11-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 185a95cfebef0e9d6e7914f3102aa5ecb40a877a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988704"
---
# <a name="ledger-settlements"></a>Virsgrāmatas darbību sasaistīšana

[!include [banner](../includes/banner.md)]

Virsgrāmatas darbību sasaistīšana ļauj jums virsgrāmatā noteikt debeta un kredīta transakciju atbilstību un atzīmēt šīs transakcijas kā nosegtas. Šādi varat pārliecināties, vai saistītās transakcijas ir nokārtotas. Varat arī anulēt nosegšanu, ja tā tika veikta kļūdaini.

## <a name="enable-advanced-ledger-settlements"></a>Uzlabotās virsgrāmatas darbību sasaistīšanas iespējošana

Uzlabotās virsgrāmatas darbību sasaistīšanas lapa piedāvā papildu iespējas transakciju filtrēšanai un atlasīšanai. Lai iespējotu uzlabotās virsgrāmatas darbību sasaistīšanas lapu, izpildiet tālāk aprakstītos norādījumus.

1. Atlasiet **Virsgrāmata** \> **Virsgrāmatas iestatīšana** \> **Virsgrāmatas parametri**. 
2. Cilnē **Virsgrāmatas darbību sasaistīšana** opciju **Uzlabotā virsgrāmatas darbību sasaistīšana** iestatiet uz **Jā**, lai ieslēgtu uzlabotās virsgrāmatas darbību sasaistīšanas funkcionalitāti. Uzlabotā **Virsgrāmatas darbību sasaistīšanas** lapa tiek izmantota, kad atlasāt opciju **Virsgrāmatas darbību sasaistīšana** sadaļā **Periodiskie uzdevumi**. 
3. Jums ir jāievada saraksts ar kontiem, kurus izmantot virsgrāmatas darbību sasaistīšanai katram kontu plānam. Šis saraksts tiek izmantots, lai filtrētu lapā **Virsgrāmatas darbību sasaistīšana** redzamo transakciju sarakstu. Sarakstā **Kontu plāns** atlasiet kādu kontu plānu un pēc tam atlasiet **Jauns**, lai šim sarakstam pievienotu jaunus kontus.

## <a name="settle-transactions-by-using-the-advanced-ledger-settlements-page"></a>Transakciju segšana, izmantojot uzlabotās virsgrāmatas darbību sasaistīšanas lapu

Lai segtu virsgrāmatas transakcijas, izpildiet tālāk aprakstītos norādījumus.

1. Atlasiet **Virsgrāmata** \> **Periodiskie uzdevumi** \> **Virsgrāmatas darbību sasaistīšana**.
2. Iestatiet filtrus šīs lapas augšpusē, izpildot tālāk aprakstītos norādījumus.

    - Atlasiet kādu datu diapazonu vai atlasiet **Datumu intervāla kods**, lai datumu diapazonu aizpildītu automātiski.
    - Pēc nepieciešamības mainiet grāmatošanas līmeni.
    - Lai virsgrāmatas kontu un dimensijas rādītu atsevišķi, atlasiet kādu finanšu dimensiju kopu.

3. Atlasiet **Rādīt transakcijas**, lai rādītu visas transakcijas, kas atbilst jūsu iestatītajiem filtriem un kontu sarakstam, kuru norādījāt, kad iestatījāt kontu plānu sarakstu iepriekšējā sadaļā. Ka maināt kādu no filtriem vai dimensiju kopām, vienums **Rādīt transakcijas** ir jāatlasa vēlreiz.
4. Atlasiet vienu vai vairākas rindas, kuras apsverat nosegšanai. Lauka **Atlasītā summa** vērtība lapas augšpusē palielinās vai samazinās par jūsu atlasīto rindu kopsummu.
5. Kad esat beidzis atlasīt transakcijas, atlasiet **Atzīmēt atlasīto**. Katrai jūsu atlasītajai transakcijai kolonnā **Atzīmēts** tiek parādīta kontrolatzīme. Turklāt lauka **Atzīmētā summa** vērtība virs režģa palielinās vai samazinās par jūsu atzīmēto rindu kopsummu.
6. Kad lauka **Atzīmētā summa** vērtība ir **0** (nulle), atlasiet **Nosegt atzīmētās transakcijas**. Atzīmēto transakciju statuss tiek atjaunināts uz **Nosegts**.

## <a name="make-transactions-easier-to-find"></a>Transakciju atrašanas atvieglošana

Lapā **Virsgrāmatas darbību sasaistīšana** ir iespējas, kas ļauj vienkāršāk ieraudzīt nosegšanai nepieciešamās transakcijas.

- Izmantojot pogu **Noņemt atzīmētā atzīmi**, tiek notīrīts lauks **Atzīmēts** visām atlasītajām rindām.
- Izmantojot filtru **Atzīmēts**, transakcijas varat filtrēt atkarībā no tā, vai tām ir atzīmēts lauks **Atzīmēts**.
- Izmantojot filtru **Statuss**, transakcijas varat filtrēt atkarībā no tā, vai to statuss ir **Nosegts** vai **Nav nosegts**.
- Izmantojot pogu **Kārtot pēc absolūtās summas**, varat kārtot summas pēc absolūtās vērtības, tādēļ varat grupēt debeta un kredīta maksājumus, kam ir vienāda summa.

## <a name="reverse-a-settlement"></a>Nosegšanas anulēšana

Var anulēt nosegšanu, kas tika veikta kļūdaini.

1. No sadaļā “Transakciju segšana, izmantojot uzlabotās virsgrāmatas darbību sasaistīšanas lapu” aprakstītajām darbībām izpildiet 1. līdz 3. darbību, lai parādītu transakcijas, ko meklējat.
2. Filtrā **Statuss** atlasiet **Nosegts**.
3. Atlasiet vienu vai vairākas rindas, kuras apsverat anulēšanai. Lauka **Atlasītā summa** vērtība lapas augšpusē palielinās vai samazinās par jūsu atlasīto rindu kopsummu.
4. Kad esat beidzis atlasīt transakcijas, atlasiet **Atzīmēt atlasīto**. Katrai jūsu atlasītajai transakcijai kolonnā **Atzīmēts** tiek parādīta kontrolatzīme. Turklāt lauka **Atzīmētā summa** vērtība lapas augšpusē palielinās vai samazinās par jūsu atzīmēto rindu kopsummu.
5. Kad lauka **Atzīmētā summa** vērtība ir **0** (nulle), atlasiet **Anulēt atzīmētās transakcijas**. Atzīmēto transakciju statuss tiek atjaunināts uz **Nav nosegts**.

## <a name="update-the-list-of-accounts-that-are-included-in-the-list-of-transactions"></a>Transakciju sarakstā ietvertā kontu saraksta atjaunināšana

Atlasiet **Virsgrāmatas nosegšanas konti**, lai atvērtu dialoglodziņu, kur varat rediģēt transakciju sarakstā ietvertos kontus. Atlasiet **Jauns**, lai šim sarakstam pievienotu jaunus kontus. Šis saraksts tiek izmantots, lai filtrētu lapā **Virsgrāmatas darbību sasaistīšana** redzamo transakciju sarakstu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]