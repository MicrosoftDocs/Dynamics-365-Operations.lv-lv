---
title: Starptautiskā bankas konta numura (IBAN) kontu pārbaudes pārvaldīšana
description: Šajā tēmā ir izskaidrots, kā pārvaldīt starptautiskā bankas konta numura (IBAN) kontu pārbaudi.
author: mikefalkner
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: e44b855165752baeb42d3c9952c35982ef24b0f5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815864"
---
# <a name="manage-international-bank-account-number-iban-account-validation"></a>Starptautiskā bankas konta numura (IBAN) kontu pārbaudes pārvaldīšana

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]