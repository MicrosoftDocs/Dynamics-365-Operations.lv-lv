---
title: Starptautiskā bankas konta numura (IBAN) kontu pārbaudes pārvaldīšana
description: Šajā rakstā skaidrots, kā pārvaldīt starptautisko bankas konta numura (IBAN) konta apstiprināšanu.
author: angelad116
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 0e64c763cb74362503a3d6dfa184b26df77f30b3
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151796"
---
# <a name="manage-international-bank-account-number-iban-account-validation"></a>Starptautiskā bankas konta numura (IBAN) kontu pārbaudes pārvaldīšana

[!include [banner](../includes/banner.md)]

Starptautiskā bankas konta numura (IBAN) validēšana palielina apjomu validēšanai, kas tiek veikta, kad bankas kontam pievienojat IBAN.

Informācija par IBAN Microsoft Dynamics struktūru tiek glabāta 365 Finansēs un tiek automātiski ielādēta, kad pirmo reizi bankas kontos izmantojat IBAN. Šī informācija ietver IBAN garumu, bankas konta numura un maršrutēšanas numura sākuma pozīcijas, kā arī bankas konta numura un maršrutēšanas numura garumu.

## <a name="set-up-iban-structures"></a>IBAN struktūru iestatīšana

1. Dodieties uz **Kases un bankas vadība \> Iestatīšana \> IBAN struktūras**.
2. Ņemiet vērā, ka IBAN struktūras katrai valstij vai reģionam ir iestatītas automātiski.
3. Atlasiet pogu **Rediģēt**, ja ir jāatjaunina struktūra konkrētai valstij vai reģionam.
4. Struktūras definīcijas būs katra jauna laidiena daļa. Var izmantot izvēlni **Atiestatīt struktūras**, lai ielādētu jaunākās definīcijas pēc katra jauninājuma.

## <a name="validate-the-iban-structure-in-a-bank-account"></a>Bankas konta IBAN struktūras validēšana

1. Atveriet sadaļu **Kases un bankas vadība \> Banku konti \> Banku konti**.
2. Izveidojiet bankas kontu.
3. Kopsavilkuma cilnē **Papildinformācija** ievadiet IBAN numuru.

    Ja IBAN garums neatbilst garumam, kas ir definēts katrai valstij vai reģionam, jūs saņemat brīdinājuma ziņojumu. Nevar turpināt, ja IBAN garums neatbilst IBAN struktūrā noteiktajam garumam.

    Validācijā arī tiek pārbaudīts, vai bankas konta numurs atbilst bankas konta numuru pārstāvošajai IBAN numura daļai. Ja bankas konta numurs neatbilst, jūs saņemat brīdinājuma ziņojumu. Šis ziņojums ir tikai brīdinājums. Jūs varat turpināt arī tādā gadījumā, ja bankas konta numurs neatbilst.

    Validācijā tiek arī pārbaudīts, vai bankas maršrutēšanas numurs atbilst bankas maršrutēšanas numuru pārstāvošajai IBAN daļai. Maršrutēšanas numurā ir bankas numurs un bieži arī papildu bankas filiāle. Ja bankas maršrutēšanas numurs neatbilst, jūs saņemat brīdinājuma ziņojumu. Šis ziņojums ir tikai brīdinājums. Jūs varat turpināt arī tādā gadījumā, ja bankas maršrutēšanas numurs neatbilst.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
