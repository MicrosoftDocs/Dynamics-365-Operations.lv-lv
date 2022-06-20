---
title: Maksu kodu izveide
description: Šajā rakstā skaidrots, kā konfigurēt maksājumu kodus gan parādiem kreditoriem, gan debitoriem.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MarkupTable
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d65952cb989672e4eac2dd6101ee9c7c9424daed
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8866088"
---
# <a name="create-charges-codes"></a>Maksu kodu izveide

Šajā rakstā skaidrots, kā konfigurēt maksājumu kodus gan parādiem kreditoriem, gan debitoriem. Ja jūsu organizācijai nepieciešams, lai papildus rindas vienībām pārdošanas pasūtījumā vai pirkšanas pasūtījumā tiktu izsekotas pārdošanas summas vai pirkšanas summas, šim nolūkam var izmantot maksu kodus. Piemēram, jūs pirkšanas pasūtījumā maksājat kravas pārvadāšanai un apdrošināšanai un šīs summas pirkšanas pasūtījumā tiek atdalītas atsevišķi. Šajā gadījumā var norādīt, vai summas tiek grāmatotas izdevumu kontos vai pievienotas krājumu izmaksām.

## <a name="set-up-charges-codes-for-accounts-receivable"></a>Iestatīt izmaksu kodus debitoru parādiem

Lai izveidotu maksu kodus debitoru parādiem, sekojiet šiem soļiem.

1. Dodieties uz **debitoru maksu** &gt; **iestatījumu** &gt; **izmaksu kodu**.
2. Atlasiet **Jauna**.
3. **Laukā Maksu** kods ievadiet maksas kodu.
3. **Laukā** Apraksts ievadiet maksas aprakstu.
4. Nav obligāti **: laukā Krājumu** PVN grupa atlasiet PVN grupu.
5. Kopsavilkuma cilnē **Grāmatošana** norādiet, kā maksa ir automātiski jādebetē un kreditēta.
6. Ja jūs izvēlējāties **Virsgrāmatas** kontu kā debeta tipu vai kredīta tipu, **norādiet** grāmatošanas tipu iegrāmatošanas laukos un norādiet galveno kontu konta **laukos**.

### <a name="example"></a>Paraugs

Jūsu debitors apmaksā maksu. Tāpēc tā tiek pievienota pārdošanas pasūtījuma kopsummai. Var iestatīt šādu grāmatošanas informāciju:

- Sadaļas **Debets** **laukā** Tips atlasiet **Debitors/** Kreditors, lai pievienotu rēķina maksu debitora kontam.
- Laukā **Tips sadaļā Kredīts** **atlasiet** Virsgrāmatas **kontu**. Pēc tam laukā **Konts** atlasiet galveno kontu ieņēmumiem no rēķina papildmaksām.

> [!NOTE]
> Ja atlasītajam kodam **debeta** **vai** kredīta tips ir Virsgrāmatas konts vai krājums, maksas darbībai varat ievadīt citu valūtu.

Varat drukāt maksu tekstu debitoram piešķirtajā valodā. Lai norādītu izmaksu koda tekstu citās valodās, atlasiet **Tulkojumi**.

## <a name="set-up-charges-codes-for-accounts-payable"></a>Iestatīt maksājumu kodus parādiem kreditoriem

Lai izveidotu maksu kodus Parādiem kreditoriem, sekojiet šiem soļiem.

1. Izpildiet kādu no šīm darbībām:

    - Dodieties uz **sadaļu Parādu kreditoriem** &gt; **·** **maksu iestatījuma** &gt; **izmaksu kods.**
    - Dodieties uz **Sagādes un avotu Iestatījumu** &gt; **maksu** &gt; **·** &gt; **maksu kodu.**

2. Atlasiet **Jauna**.
3. **Laukā Maksu** kods ievadiet maksas kodu.
3. **Laukā** Apraksts ievadiet maksas aprakstu.
4. Nav obligāti **: laukā Krājumu** PVN grupa atlasiet PVN grupu.
5. Nav obligāti: **laukā** Maksimālā summa ievadiet maksimālo summu, kas ir atļauta maksas kodam.

    Šis lauks tiek izmantots, lai pārbaudītu kreditoru rēķinu maksas. Lai iespējotu maksu validāciju, atzīmējiet **·** **·** **izvēles rūtiņu Iespējot rēķinu salīdzināšanas pārbaudi lapas Kreditoru parametri cilnē Rēķina** apstiprināšana.

    > [!IMPORTANT]
    > Lai apstiprinātu rēķinu maksas, jāizveido arī ierobežojuma nosacījumu tipa instance, kas pamatojas uz noteiktu kreditora rēķinu ierobežojumu maksām.

6. Kopsavilkuma cilnē **Grāmatošana** norādiet, kā maksa ir automātiski jādebetē un kreditēta.
7. Ja atlasīts **Virsgrāmatas konts** kā debeta tips vai kredīta tips, **·** **norādiet** grāmatošanas tipu debeta grāmatošanas un kredīta grāmatošanas laukiem **un** **norādiet galveno kontu debeta konta un kredīta konta** laukos.
8. Lai iespējotu maksas vērtību salīdzināšanu rēķinam, kas ietver maksas no atbilstošā pirkšanas pasūtījuma virsraksta vai rindām, **atzīmējiet izvēles rūtiņu Salīdzināt pirkšanas pasūtījuma un** rēķina vērtības.

### <a name="example"></a>Paraugs

Maksu var ierakstīt kā izdevumu kā daļu no pirkšanas pasūtījuma vai kreditora rēķina kopsummas. Lai iestatītu grāmatošanas informāciju, sekojiet šiem soļiem. 

- Sadaļas **Kredīts** **laukā** Tips atlasiet **Debitors/** Kreditors, lai pievienotu rēķina maksu kreditora kontam.
- Laukā **Tips sadaļā Debets** **atlasiet** Virsgrāmatas **kontu**. Pēc tam **laukā** Konts atlasiet galveno kontu izdevumiem no rēķina maksām.

Izpildiet šīs darbības, lai iestatītu grāmatošanas informāciju tā, ka vienības maksa tiek pievienota krājuma izmaksām.

- Sadaļas **Kredīts** **laukā** Tips atlasiet **Debitors/** Kreditors, lai pievienotu rēķina maksu kreditora kontam.
- Sadaļas **Debets** **laukā** Tips atlasiet **Krājums**, kuru pievienot krājuma izmaksām.

> [!NOTE]
> Iespējams, vēlēsieties izmantot valūtu, kas atšķiras no valūtas, kas norādīta pirkšanas pasūtījumā vai rēķinā. Varat ievadīt citu valūtu, ja atlasītā koda debeta vai kredīta tips ir Virsgrāmatas **konts vai** **Krājums**.

Varat drukāt maksu tekstu debitoram piešķirtajā valodā. Lai norādītu izmaksu koda tekstu citās valodās, atlasiet **Tulkojumi**.
