---
title: Problēmu novēršana saistībā ar izdošanu un iepakošanu
description: Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, izdodot un iepakojot programmā Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 2cce1038ed393fc8a7bb489a37fc0921b0ac755e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993938"
---
# <a name="troubleshoot-picking-and-packing"></a>Problēmu novēršana saistībā ar izdošanu un iepakošanu

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, izdodot un iepakojot programmā Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-dimension-location-cant-be-left-blank-if-dimension-serial-number-is-set"></a>Tiek parādīts šāds kļūdas ziņojums: "Dimensijas novietojumu nevar atstāt tukšu, ja ir iestatīts dimensijas sērijas numurs."

### <a name="issue-description"></a>Problēmas apraksts

Šis kļūdas ziņojums tiek parādīts, ja izveidojat pārsūtīšanas pasūtījumu sērijas krājumam, izmantojot noliktavu, kas ir aktivizēta papildu noliktavas pārvaldībai (WMS), un pēc tam, kad darbs ir pabeigts, jūs mēģināt apstiprināt kravu.

### <a name="issue-resolution"></a>Problēmas risinājums

**Noklusējuma kvīts novietojuma** lauks ir tukšs noliktavas "no" tranzīta noliktavai. Lai labotu šo problēmu, norādiet noklusēto ieejas plūsmas vietu tranzīta noliktavā. Pārliecinieties, vai šī atrašanās vieta ir numura zīmes kontrolēta.

## <a name="i-receive-the-following-error-message-invalid-license-plate"></a>Tiek parādīts šāds kļūdas ziņojums: "Nederīga numura zīme."

### <a name="issue-description"></a>Problēmas apraksts

Šis kļūdas ziņojums tiek parādīts noliktavas programmā, skenējot numura zīmes ID.

### <a name="issue-resolution"></a>Problēmas risinājums

Pārliecinieties, vai numura zīmes ID atrodas numura zīmju tabulā, un ka krājumi un daudzumi numura zīmē ir pieejami (citiem vārdiem sakot, tie nav bloķēti).

## <a name="i-receive-the-following-error-message-field-load-weight-1-can-only-contain-positive-numbers-update-has-been-canceled"></a>Tiek parādīts šāds kļūdas ziņojums: "Lauks 'Kravas svars' (=-%1) var saturēt tikai pozitīvus skaitļus. Labojumi ir atcelti."

### <a name="issue-description"></a>Problēmas apraksts

Šis kļūdas ziņojums tiek parādīts, ja, apstrādājot darbu no iepakošanas vietām uz sagatavošanas posmiem vai no sagatavošanas vietām uz doka vietām.

### <a name="issue-resolution"></a>Problēmas risinājums

Lai labotu šo problēmu, dodieties uz **Sistēmas administrēšana \> Periodiskie uzdevumi \> Datu bāzes \> Konsekvences pārbaude** un palaidiet procesu **Noliktavas kravas svara konsekvences pārbaudei**.

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a>Tiek parādīts šāds kļūdas ziņojums: "Daudzums nav derīgs %1 vienībai."

### <a name="issue-description"></a>Problēmas apraksts

Šis kļūdas ziņojums tiek parādīts, mēģinot veikt *sadalītu izdošanu* vairākās partijās.

### <a name="issue-resolution"></a>Problēmas risinājums

Noliktavas darbiniekam jāizmanto *Īsā izdošanas* procedūra noliktavas programmā. Ja mēģināt izvēlēties vairākas partijas no vienas un tās pašas vietas, varat arī izmantot **Pilno** opciju noliktavas programmā.

## <a name="i-cant-move-inventory-to-a-location-that-is-license-platecontrolled"></a>Nevar pārvietot krājumu uz atrašanās vietu, ko kontrolē numura zīme.

### <a name="issue-description"></a>Problēmas apraksts

Kravai nevar samazināt izdotos daudzumus.

### <a name="issue-resolution"></a>Problēmas risinājums

Agrākās versijās kravai nevar samazināt izdotos daudzumus. Tomēr tagad varat neizdot uz novietojumu, ko kontrolē numura zīme. Lapā **Samazināt izdoto daudzumu** ir jānorāda gan **Novietojuma** vērtība, gan **Numura zīmes** vērtība.

## <a name="can-i-print-a-delivery-note-or-packing-content-by-warehouse"></a>Vai var drukāt piegādes pavadzīmi vai iepakojuma saturu pēc noliktavas?

### <a name="issue-description"></a>Problēmas apraksts

Jūs vēlaties drukāt piegādes pavadzīmi vai iepakojuma saturu pēc noliktavas vai vietnes lapā **Darba audita veidnes rindas atjaunināšana**.

### <a name="issue-resolution"></a>Problēmas risinājums

Kad drukājat dokumentu, izmantojot drukas pārvaldības iestatījumus, ierobežojiet tvērumu (vietne/noliktava), izmantojot Drukas pārvaldību, nevis atlasot **Rediģēt drukas iestatījumus** lapā **Darba audita veidnes rindas atjaunināšana**.

## <a name="i-cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a>Nevar atcelt pavadzīmi pēc tās grāmatošanas no pārdošanas pasūtījuma.

### <a name="issue-description"></a>Problēmas apraksts

Kad izdošanas un nosūtīšanas procesi ir iespējoti WMS, pavadzīmi nevar atcelt pēc tās grāmatošanas no pārdošanas pasūtījuma.

### <a name="issue-resolution"></a>Problēmas risinājums

Lai labotu grāmatotās pavadzīmes krājumiem, kas ir iespējoti WMS, grāmatošana ir jāveic no kravas, nevis tieši no pasūtījuma. Korporācija Microsoft ir izvērtējusi šo problēmu un ir noteikusi, ka tas ir līdzekļa ierobežojums. Parasti pārdošanas pasūtījums, kas ir izdots un nosūtīts ar noliktavas pārvaldības procesu starpniecību, var būt pavadzīmē atjaunināts no kravas vai sūtījuma un paša pārdošanas pasūtījuma dokumenta. Tomēr, ja pavadzīmē atjauniniet pārdošanas pasūtījumu no pārdošanas pasūtījuma dokumenta, pavadzīmes atgriešana joprojām nevar tikt veikta no kravas vai pārdošanas pasūtījuma. Tāpēc ieteicams izmantot pavadzīmes grāmatošanu no kravas. Šādā gadījumā tiks aktivizēta atgriešana, kas ir jāveic no kravas.

## <a name="i-receive-the-following-error-message-not-enough-work-can-be-found-for-cluster"></a>Es saņemu sekojošu kļūdas ziņojumu: "Klasterim nav atrasts pietiekami darba."

### <a name="issue-description"></a>Problēmas apraksts

Ja izmantojat *Sistēmas virzītu klastera izdošanas* procesu, konfigurējot klastera profilu, kur, piemēram, var izdot 10 pozīcijas, process darbojas kā plānots, kad ir pietiekami daudz darba, lai izdotu 10 pozīcijas. Tomēr, ja izdošanai ir tikai astoņas pozīcijas, tiek parādīts šis kļūdas ziņojums, jo vienā klasterī nav pietiekami daudz darba.

### <a name="issue-resolution"></a>Problēmas risinājums

Lai labotu šo problēmu, rediģējiet klastera profilu un iestatiet opciju **Aktivizēt pozīcijas** uz *Nē*.
