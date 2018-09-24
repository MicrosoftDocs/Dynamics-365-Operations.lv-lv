---
title: "Starptautiskā bankas konta numura (IBAN) kontu pārbaudes pārvaldīšana"
description: "Šajā tēmā ir izskaidrots, kā pārvaldīt starptautiskā bankas konta numura (IBAN) kontu pārbaudi."
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: e091aab70a98e0f4b96c41c1ee48926947539105
ms.contentlocale: lv-lv
ms.lasthandoff: 09/22/2018

---

# <a name="manage-international-bank-account-number-iban-account-validation"></a>Starptautiskā bankas konta numura (IBAN) kontu pārbaudes pārvaldīšana

[!include [banner](../includes/banner.md)]

Starptautiskā bankas konta numura (IBAN) kontu pārbaude palielina pārbaudes apjomu, kas tiek veikts, kad jūs pievienojat IBAN bankas kontu.

IBAN struktūra tiek glabāta sistēmā Microsoft Dynamics 365 for Finance and Operation un tiek automātiski ielādēta, kad pirmoreiz izmantojat IBAN bankas kontos. Bankas konta numurs ir daļa no IBAN numura definētās struktūras. Pamatojoties uz šo struktūru, ja IBAN izvietojums un konta numura garums neatbilst izvietojumam, kas ir definēts struktūrā katrai valstij vai reģionam, jūs saņemsiet brīdinājuma ziņojumu.

## <a name="set-up-iban-structures"></a>IBAN struktūru iestatīšana

1. Dodieties uz **Kases un bankas vadība \> Iestatīšana \> IBAN struktūras**.
2. Ņemiet vērā, ka IBAN struktūras katrai valstij vai reģionam ir iestatītas automātiski.
3. Ja kādai noteiktai valstij vai reģionam struktūras ir jāpielāgo, varat tās rediģēt.
4. Struktūras definīcijas būs katra jauna laidiena daļa. Var izmantot izvēlni **Atiestatīt struktūras**, lai ielādētu jaunākās definīcijas pēc katra jauninājuma.

## <a name="validate-the-iban-structure-in-a-bank-account"></a>Bankas konta IBAN struktūras validēšana

1. Atveriet sadaļu **Kases un bankas vadība\> Banku konti \> Banku konti**.
2. Izveidojiet bankas kontu.
3. Kopsavilkuma cilnē **Papildinformācija** ievadiet IBAN numuru.

    Ja IBAN izvietojums un konta numura garums neatbilst izvietojumam, kas ir definēts struktūrā katrai valstij vai reģionam, jūs saņemat ziņojumu. Nevar turpināt, ja IBAN numura garums neatbilst garumam IBAN struktūrā.

    Validācijā arī tiek pārbaudīts, vai bankas konta numurs atbilst bankas konta numuru pārstāvošajai IBAN numura daļai. Ja bankas konta numurs neatbilst, jūs saņemsiet brīdinājuma ziņojumu. Šis ziņojums ir tikai brīdinājums. Jūs varat turpināt arī tādā gadījumā, ja bankas konta numurs neatbilst.

