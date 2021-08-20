---
title: Debitoru kopēšana, izmantojot koplietotas numuru sērijas
description: Šajā tēmā ir paskaidrots, kā izmantot koplietotas numuru sērijas, lai debitoru kopētu uz citu juridisko personu, bet saglabātu to pašu debitora ID.
author: mikefalkner
ms.date: 08/31/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: d906ed3cb7af0af9e0137f878c39d5ad47616a783688ad70b1465bd0b2d470aa
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763338"
---
# <a name="copy-customers-by-using-shared-number-sequences"></a>Debitoru kopēšana, izmantojot koplietotas numuru sērijas

[!include [banner](../includes/banner.md)]

Debitoru ID piešķiršanai varat izmantot koplietotas numuru sērijas. Koplietotas numuru sērijas jums dod iespēju arī kopēt debitorus no vienas juridiskās personas uz citu juridisko personu, bet abās juridiskajās personās izmantot tos pašus debitoru ID.

## <a name="setup"></a>Iestatīšana

Šis līdzeklis tiek aktivizēts, kad debitoru ID piešķiršanai izmantojat koplietotu numuru sēriju. Jums ir jāizmanto tā pati numuru sērija visās juridiskajās personās, kurās vēlaties kopēt šo debitoru. Debitoru numuru sēriju katrai juridiskajai personai varat mainīt lapā **Debitoru parādu parametri**. Atlasiet **Debitoru parādi** \> **Parametri** un pēc tam atlasiet cilni **Numuru sērijas**.

Debitoru numuru sērijas varat iestatīt arī katrai debitoru grupai. Arī šīm numuru sērijām ir jābūt koplietotām. Vispirms tiek lietota numuru sērija debitoru grupai. Ja debitoru grupai nav norādīta nekāda numuru sērija, tiek lietota tā numuru sērija, kas ir norādīta lapā **Debitoru parādu parametri**.

Debitorus varat kopēt starp dažādām juridiskajām personām arī tad, ja izmantojat manuālus debitoru ID. Taču, ja kādu debitoru mēģināt kopēt uz juridisko personu, kur šāds debitora ID jau pastāv, kopēšanas process nesākas.

## <a name="copy-a-customer"></a>Debitora kopija

Lai kopētu debitoru, atlasiet **Jauns** saraksta lapā **Visi debitori**, tādējādi atverot dialoglodziņu **Izveidot debitoru**. Ņemiet vērā, ka jaunais debitora ID netiek piešķirts nekavējoties. Šī uzvedība atšķiras no uzvedības iepriekšējās versijās. Tā kā jūs vēl neesat atlasījis debitoru grupu, sistēma nevar noteikt, kura numuru sērija ir jāizmanto. Turklāt tā nevar noteikt, vai jūs mēģināt izveidot jaunu debitoru vai kopēt jau esošu debitoru. Tādēļ debitora ID tiek piešķirts tikai pēc tam, kad dialoglodziņa apakšā atlasāt **Saglabāt**.

Ja veidojat jaunu debitoru, varat turpināt ar visu lauku aizpildīšanu kā parasti. Kad esat beidzis un atlasāt **Saglabāt**, varat redzēt, ka debitora ID tika piešķirts automātiski. Savukārt manuālām numuru sērijām varēsit redzēt, ka tika izmantots jūsu manuālais debitora ID.

Lai kopētu kādu debitoru, laukā **Nosaukums** ievadiet vienu vai vairākas rakstzīmes, kas atbilst jūsu meklētajam debitoram. Meklēšanas dialoglodziņā tiek parādīts saraksts ar visām personām, kas varētu atbilst jūsu meklētajam debitoram. Kad atlasāt vienu no personām, dialoglodziņa labajā pusē tiek parādīta tālāk aprakstītā papildinformācija.

- Cilnē **Vispārīgi** tiek rādīts personas tālruņa numurs un adrese.
- Cilnē **Lomas** tiek rādītas lomas, kādas atlasītajai personai var būt, kā arī juridiskā persona, kurā tai ir katra no šīm lomām.
- Cilnē **Nodokļa reģistrācijas ID** tiek rādīti nodokļa reģistrācijas identifikatori (ID), kas šai personai ir piešķirti.

Personu varat kopēt tikai tad, ja tai ir debitora loma un ja tai šī loma ir tādā juridiskajā personā, kas nav pašreizējā juridiskā persona. Kad atrodat personu, kas atbilst šiem kritērijiem, izpildiet tālāk aprakstītos norādījumus.

1. Tiek parādīta opcija **Kopēt debitoru**. Pēc noklusējuma šī opcija ir iestatīta uz **Nē**. Lai šo debitoru kopētu uz pašreizējo juridisko personu, iestatiet šo opciju uz **Jā**. 
2. Tiek parādīts lauks **Juridiskā persona**. Atlasiet juridisko personu, no kuras kopēt šo debitoru. Ja debitors pastāv tikai vienā juridiskajā personā, šis lauks pēc noklusējuma tiek iestatīts uz attiecīgo juridisko personu.
3. Atlasiet **Atlasīt**. Jaunais debitors ir izveidots.

## <a name="validation"></a>Validēšana

Kad kopējat kādu debitoru, sistēma mēģina saglabāt jaunā debitora informāciju. Tiek veikta validēšana, lai apstiprinātu, ka kopētie dati ir derīgi. Par katru nesekmīgo validēšanu tiek parādīts kļūdas ziņojums. Kļūdas ziņojumos ir paskaidrots, kāda informācija ir jāatjaunina. Debitora datu kopiju var saglabāt tikai pēc tam, kad esat izlabojis visas validēšanas kļūdas.

## <a name="copy-a-customer-by-using-tax-exempt-number-search-feature"></a>Debitora kopēšana, izmantojot PVN reģistrācijas numura meklēšanas līdzekli

Debitorus varat arī kopēt, izmantojot PVN reģistrācijas numura meklēšanas līdzekli, kas atrodas cilnes **Debitors** grupā **Reģistrācija**, kura ir pieejama lapas **Visi debitori** darbību rūtī. Parādītajā dialoglodziņā **PVN reģistrācijas numura meklēšana** ir redzami PVN reģistrācijas numuri, debitora ID, debitora nosaukums un juridiskā persona, kur šis PVN reģistrācijas ID tiek izmantots. Debitoru var kopēt tikai tad, ja tas atrodas kādā juridiskajā personā, kas nav pašreizējā juridiskā persona. Kad esat atlasījis debitoru, kas atbilst šim kritērijam, izpildiet tālāk aprakstītos norādījumus.

1. Tiek parādīta opcija **Kopēt debitoru**. Pēc noklusējuma šī opcija ir iestatīta uz **Nē**. Lai šo debitoru kopētu uz pašreizējo juridisko personu, iestatiet šo opciju uz **Jā**. 
2. Atlasiet **Atlasīt**. Jaunais debitors ir izveidots.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]