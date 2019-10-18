---
title: Starptautiskā bankas konta numura (IBAN) kontu pārbaudes pārvaldīšana
description: Šajā tēmā ir izskaidrots, kā pārvaldīt starptautiskā bankas konta numura (IBAN) kontu pārbaudi.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: a4f9bc2a22aabc7b83eb15665f37849d505e1b6b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178872"
---
# <a name="manage-international-bank-account-number-iban-validation"></a>Starptautiskā bankas konta numura (IBAN) validācijas pārvaldīšana

[!include [banner](../includes/banner.md)]

Starptautiskā bankas konta numura (IBAN) validēšana palielina apjomu validēšanai, kas tiek veikta, kad bankas kontam pievienojat IBAN.

Programmā Microsoft Dynamics 365 Finance tiek glabāta informācija par IBAN struktūru. Šī informācija tiek automātiski ielādēta, kad šo IBAN bankas kontiem lietojat pirmo reizi. Šī informācija ietver IBAN garumu, bankas konta numura un maršrutēšanas numura sākuma pozīcijas, kā arī bankas konta numura un maršrutēšanas numura garumu.

## <a name="set-up-iban-structures"></a>IBAN struktūru iestatīšana

1. Dodieties uz **Kases un bankas vadība \> Iestatīšana \> IBAN struktūras**.
2. Ņemiet vērā, ka IBAN struktūras katrai valstij vai reģionam ir iestatītas automātiski.
3. Ja vēlaties pielāgot struktūras kādai noteiktai valstij vai reģionam, varat tās rediģēt.
4. Struktūras definīcijas būs katra jauna laidiena daļa. Var izmantot izvēlni **Atiestatīt struktūras**, lai ielādētu jaunākās definīcijas pēc katra jauninājuma.

## <a name="validate-the-iban-structure-in-a-bank-account"></a>Bankas konta IBAN struktūras validēšana

1. Atveriet sadaļu **Kases un bankas vadība \> Banku konti \> Banku konti**.
2. Izveidojiet bankas kontu.
3. Kopsavilkuma cilnē **Papildinformācija** ievadiet IBAN numuru.

    Ja IBAN garums neatbilst garumam, kas ir definēts katrai valstij vai reģionam, jūs saņemat brīdinājuma ziņojumu. Nevar turpināt, ja IBAN garums neatbilst IBAN struktūrā noteiktajam garumam.

    Validācijā arī tiek pārbaudīts, vai bankas konta numurs atbilst bankas konta numuru pārstāvošajai IBAN numura daļai. Ja bankas konta numurs neatbilst, jūs saņemat brīdinājuma ziņojumu. Šis ziņojums ir tikai brīdinājums. Jūs varat turpināt arī tādā gadījumā, ja bankas konta numurs neatbilst.

    Validācijā tiek arī pārbaudīts, vai bankas maršrutēšanas numurs atbilst bankas maršrutēšanas numuru pārstāvošajai IBAN daļai. Maršrutēšanas numurā ir bankas numurs un bieži arī papildu bankas filiāle. Ja bankas maršrutēšanas numurs neatbilst, jūs saņemat brīdinājuma ziņojumu. Šis ziņojums ir tikai brīdinājums. Jūs varat turpināt arī tādā gadījumā, ja bankas maršrutēšanas numurs neatbilst.
