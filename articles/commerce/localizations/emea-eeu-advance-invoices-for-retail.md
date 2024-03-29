---
title: Avansa rēķini programmai Commerce Austrumeiropā
description: Šajā rakstā skaidrots, kā iestatīt avansa paziņojumus Komercijai Austrumeiropā.
author: EvgenyPopovMBS
ms.date: 10/23/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: josaw
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: 8.0999999999999996
ms.search.industry: Retail
ms.openlocfilehash: 9f82d5316c4b3d6ce5fd34b94f71689be77a6e4b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286557"
---
# <a name="advance-invoices-for-commerce-for-eastern-europe"></a>Avansa rēķini programmai Commerce Austrumeiropā

[!include [banner](../includes/banner.md)]

Informācija šajā rakstā attiecas uz Austrumeiropas lokalizāciju un ir raksturīga tirdzniecības nozarei.

Polijā, Ungārijā un Čehijas Republikā, saņemot priekšapmaksu no debitora caur pārdošanas punktu (Point of Sale — POS), priekšapmaksa ir jāreģistrē nodokļu aprēķinam, un ir nepieciešams izveidot un drukāt avansa rēķina dokumentu, kurā norādīta priekšapmaksas summa. Turklāt Polijā avansa rēķinu transakcijas ir jāgrāmato virsgrāmatā.

Kad tiek veikts galīgais pārdošanas pasūtījuma rēķina grāmatojums, galīgajā dokumentā jāietver avansa rēķins un ir jānorāda visas priekšapmaksas.

Ja pārdošanas pasūtījumi tiek izveidoti no debitoru parādiem, ir manuāli jāizveido avansa rēķini, izmantojot procedūru, kas aprakstīta tēmā [Avansa rēķini Austrumeiropas valstīm](/dynamics365/unified-operations/financials/localizations/emea-advance-invoice). Ja pārdošanas pasūtījumi tiek izveidoti ar POS starpniecību, sistēma izveido un grāmato avansa rēķinus jūsu vietā.

## <a name="supported-scenarios"></a>Atbalstītie scenāriji

Tālāk ir norādīti atbalstītie scenāriji.

- Izveidojiet un grāmatojiet avansa rēķinu.
- Modificējiet depozīta summu. Ja debitors izlemj palielināt depozīta summu, tiek izsniegts papildu avansa rēķins. Visu pārējo depozīta summas izmaiņu gadījumā (piemēram, ja debitora pasūtījums ir labots) tiek izveidota kredīta nota avansa rēķinam, kas tika izveidots iepriekš, un tiek izveidots un grāmatots jauns avansa rēķins par laboto summu.
- Atceliet pārdošanas pasūtījumu, kuram ir saistīti avansa rēķini. Šādā gadījumā avansa rēķinam tiek izveidota kredīta nota.
- Grāmatojiet pārdošanas pasūtījuma rēķinu, kuram ir saistīti avansa rēķini. Avansa rēķins, kas ir saistīts ar pārdošanas pasūtījumu, tiek atsaukts par pārdošanas rēķina summu. Avansa rēķina transakcijas tiek nosegtas ar avansa rēķina atsaukšanas transakcijām.

## <a name="set-up-advance-invoices"></a>Avansa rēķinu iestatīšana

### <a name="turn-on-the-functionality-for-creating-advance-invoices"></a>Ieslēgt avansa rēķinu veidošanas funkcionalitāti

1. Pārejiet uz sadaļu **Mazumtirdzniecība un komercija \> Headquarters iestatīšana \> Parametri \> Komercijas parametri**.
2. Cilnes **Debitoru pasūtījumi** kopsavilkuma cilnē **Pasūtījums** iestatiet opcijai **Izveidot avansa rēķinu depozītam** vienumu **Jā**.

### <a name="define-the-parameters-for-posting-advance-invoices"></a>Parametru definēšana avansa rēķinu grāmatošanai

1. Dodieties uz sadaļu **Debitoru parādi \> Iestatīšana \> Debitoru moduļa parametri**.
2. Cilnes **Atjauninājumi** kopsavilkuma cilnē **Avansa rēķins** iestatiet vērtības laukos **Grāmatošanas metode**, **PVN grupa** un **Krājumu PVN grupa**. Ja šie lauki ir iestatīti pareizi, avansa rēķins tiks grāmatots. Ja šie lauki nav iestatīti, avansa rēķini netiks grāmatoti.

### <a name="turn-off-posting-of-the-sales-tax-on-prepayment-journal-voucher"></a>PVN priekšapmaksas žurnāla dokumenta summā grāmatošanas izslēgšana

PVN priekšapmaksas žurnāla dokumenta summā nedrīkst grāmatot, ja ir ieslēgta avansa rēķina grāmatošana. Lai pārbaudītu, vai šī prasība ir izpildīta, veiciet šādas darbības.

1. Dodieties uz sadaļu **Debitoru parādi \> Iestatīšana \> Debitoru moduļa parametri**.
2. Cilnes **Virsgrāmata un PVN** kopsavilkuma cilnē **Maksājums** pārliecinieties, ka tālāk minētie lauki ir tukši vai tajos ir iestatīts vienums **Nē**.

    - PVN priekšapmaksas žurnāla dokumenta summā
    - Grāmatošanas profils priekšapmaksas žurnāla dokumenta summā
    - Nodokļu grupa priekšapmaksai
    - Krājumu PVN grupa

## <a name="print-advance-invoices"></a>Avansa rēķinu drukāšana

Varat drukāt avansa rēķinus no POS, izmantojot Microsoft Windows printeri, kas ir pievienots aparatūras stacijai. Pastāv divas opcijas avansa rēķina drukāšanai no POS.

- **Drukāt avansa rēķinu pēc transakcijas noslēgšanas POS.** Šī opcija tiek izpildīta automātiski, ja avansa rēķins tika izveidots un Windows printeris tika pareizi iestatīts. Šādā gadījumā tiek drukāts tikai pēdējais avansa rēķinu, kas saistīts ar debitora pasūtījumu.
- **Atkārtoti drukāt avansa rēķinu no transakciju žurnālā.** Atlasiet **Rādīt žurnālu**, lai atvērtu transakciju žurnālu, atrodiet debitora pasūtījumu un pēc tam atlasiet **Drukāt avansa rēķinu**. Šādā gadījumā tiek drukāti visi avansa rēķini, kas saistīti ar debitora pasūtījumu.

### <a name="set-up-a-windows-printer"></a>Windows printera iestatīšana

Veiciet šādas darbības, lai iespējotu dokumentu drukāšanu no POS, izmantojot Windows printeri, kas ir savienots ar aparatūras stacija.

1. Pārejiet uz sadaļu **Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> POS iestatīšana \> POS profili \> Aparatūras profili**.
2. Atlasiet aparatūras profilu, kas attiecas uz veikalu, kurā tiek izmantots printeris.
3. Sadaļā **Printeris** vai **2. printeris** atjauniniet iestatījumus.

    - Laukā **Printeris** atlasiet **Windows draiveris**.
    - Laukā **Ierīces nosaukums** ievadiet printera nosaukumu.

4. Pārejiet uz **Mazumtirdzniecība un komercija \> Mazumtirdzniecības un komercijas IT \> Sadales grafiks**.
5. Atlasiet darbu **1090** un pēc tam atlasiet **Izpildīt tūlīt**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
