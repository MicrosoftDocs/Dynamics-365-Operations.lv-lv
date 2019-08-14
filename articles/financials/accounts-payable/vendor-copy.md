---
title: Kreditoru kopēšana, izmantojot koplietotas numuru sērijas
description: Šajā tēmā ir paskaidrots, kā izmantot koplietotas numuru sērijas, lai kreditoru kopētu uz citu juridisko personu, bet saglabātu to pašu kreditora ID.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: e777596e1bd752db438fc3591ce1125a301f4097
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836962"
---
# <a name="copy-vendors-by-using-shared-number-sequences"></a>Kreditoru kopēšana, izmantojot koplietotas numuru sērijas

[!include [banner](../includes/banner.md)]

Kreditoru ID piešķiršanai varat izmantot koplietotas numuru sērijas. Koplietotas numuru sērijas jums dod iespēju arī kopēt kreditorus no vienas juridiskās personas uz citu juridisko personu, bet abās juridiskajās personās izmantot tos pašus kreditoru ID.

## <a name="setup"></a>Iestatīšana

Šis līdzeklis tiek aktivizēts, kad kreditoru ID piešķiršanai izmantojat koplietotu numuru sēriju. Jums ir jāizmanto tā pati numuru sērija visās juridiskajās personās, kurās vēlaties kopēt šo kreditoru. Kreditoru numuru sēriju katrai juridiskajai personai varat mainīt lapā **Parādu kreditoriem parametri**. Atlasiet **Parādi kreditoriem** \> **Iestatīšana** \> **Parādu kreditoriem parametri** un pēc tam atlasiet cilni **Numuru sērijas**.

Kreditoru numuru sērijas varat iestatīt arī katrai kreditoru grupai. Arī šīm numuru sērijām ir jābūt koplietotām. Vispirms tiek lietota numuru sērija kreditoru grupai. Ja kreditoru grupai nav norādīta nekāda numuru sērija, tiek lietota tā numuru sērija, kas ir norādīta lapā **Parādu kreditoriem parametri**.

Kreditorus varat kopēt starp dažādām juridiskajām personām arī tad, ja izmantojat manuālus kreditoru ID. Taču, ja kādu kreditoru mēģināt kopēt uz juridisko personu, kur šāds kreditora ID jau pastāv, kopēšanas process nesākas.

## <a name="copy-a-vendor"></a>Kreditora kopēšana

Lai kopētu kādu kreditoru, saraksta lapā **Visi kreditori** atlasiet vienumu **Jauns**, lai atvērtu lapu **Visi kreditori, jauns ieraksts**. Ņemiet vērā, ka jaunais kreditora ID netiek piešķirts uzreiz. Šī uzvedība atšķiras no uzvedības iepriekšējās Microsoft Dynamics 365 for Finance and Operations versijās. Tā kā jūs vēl neesat atlasījis kreditoru grupu, sistēma nevar noteikt, kura numuru sērija ir jāizmanto. Turklāt tā nevar noteikt, vai jūs mēģināt izveidot jaunu kreditoru vai kopēt jau esošu kreditoru. Tādēļ kreditora ID tiek piešķirts tikai pēc tam, kad lapas apakšā atlasāt **Saglabāt**.

Ja veidojat jaunu kreditoru, varat turpināt ar visu lauku aizpildīšanu kā parasti. Kad esat beidzis un atlasāt **Saglabāt**, varat redzēt, ka kreditora ID tika piešķirts automātiski. Savukārt manuālām numuru sērijām varēsit redzēt, ka tika izmantots jūsu manuālais kreditora ID.

Lai kopētu kādu kreditoru, laukā **Nosaukums** ievadiet vienu vai vairākas rakstzīmes, kas atbilst jūsu meklētajam kreditoram. Meklēšanas dialoglodziņā tiek parādīts saraksts ar visām personām, kas varētu atbilst jūsu meklētajam kreditoram. Kad atlasāt vienu no personām, dialoglodziņa labajā pusē tiek parādīta tālāk aprakstītā papildinformācija.

- Cilnē **Vispārīgi** tiek rādīts personas tālruņa numurs un adrese.
- Cilnē **Lomas** tiek rādītas lomas, kādas atlasītajai personai var būt, kā arī juridiskā persona, kurā tai ir katra no šīm lomām.
- Cilnē **Nodokļa reģistrācijas ID** tiek rādīti nodokļa reģistrācijas identifikatori (ID), kas šai personai ir piešķirti.

Personu varat kopēt tikai tad, ja tai ir kreditora loma un ja tai šī loma ir tādā juridiskajā personā, kas nav pašreizējā juridiskā persona. Kad atrodat personu, kas atbilst šiem kritērijiem, izpildiet tālāk aprakstītos norādījumus.

1. Tiek parādīta opcija **Kopēt kreditoru**. Pēc noklusējuma šī opcija ir iestatīta uz **Nē**. Lai šo kreditoru kopētu uz pašreizējo juridisko personu, iestatiet šo opciju uz **Jā**. 
2. Tiek parādīts lauks **Juridiskā persona**. Atlasiet juridisko personu, no kuras kopēt šo kreditoru. Ja kreditors pastāv tikai vienā juridiskajā personā, šis lauks pēc noklusējuma tiek iestatīts uz attiecīgo juridisko personu.
3. Atlasiet **Atlasīt**. Jaunais kreditors ir izveidots.

## <a name="validation"></a>Validēšana

Kad kopējat kādu kreditoru, sistēma mēģina saglabāt jaunā kreditora informāciju. Tiek veikta validēšana, lai apstiprinātu, ka kopētie dati ir derīgi. Par katru nesekmīgo validēšanu tiek parādīts kļūdas ziņojums. Kļūdas ziņojumos ir paskaidrots, kāda informācija ir jāatjaunina. Kreditora datu kopiju var saglabāt tikai pēc tam, kad esat izlabojis visas validēšanas kļūdas.

## <a name="copy-a-vendor-by-using-the-tax-exempt-number-search-feature"></a>Kreditora kopēšana, izmantojot PVN reģistrācijas numura meklēšanas līdzekli

Kreditorus varat arī kopēt, izmantojot PVN reģistrācijas numura meklēšanas līdzekli, kas atrodas grupā **Reģistrācija**, cilnē **Kreditors**, lapas **Visi kreditori** darbību rūtī. Parādītajā dialoglodziņā **PVN reģistrācijas numura meklēšana** ir redzami PVN reģistrācijas numuri, kreditora ID, kreditora nosaukums un juridiskā persona, kur šis PVN reģistrācijas ID tiek izmantots. Kreditoru var kopēt tikai tad, ja tas atrodas kādā juridiskajā personā, kas nav pašreizējā juridiskā persona. Kad esat atlasījis kreditoru, kas atbilst šim kritērijam, izpildiet tālāk aprakstītos norādījumus.

1. Tiek parādīta opcija **Kopēt kreditoru**. Pēc noklusējuma šī opcija ir iestatīta uz **Nē**. Lai šo kreditoru kopētu uz pašreizējo juridisko personu, iestatiet šo opciju uz **Jā**.
2. Atlasiet **Atlasīt**. Jaunais kreditors ir izveidots.
