---
title: Kopējo izmaksu sadalījuma metode
description: Šajā tēmā ir sniegti norādījumi par to, kā lietot kopējo izmaksu sadalījumu (TCA). Kopējo izmaksu sadalījums (Total cost allocation — TCA) ir tādu izmaksu aprēķināšanas metode, kas jāsadala starp partijas pasūtījuma galvenās formulas krājumu un formulā noteiktajiem līdzproduktiem.
author: AndersGirke
manager: tfehr
ms.date: 04/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConsistOf, PmfFormulaCoBy
audience: Application User
ms.reviewer: kamaybac
ms.custom: 83852
ms.assetid: 7c14c3e5-9476-4a79-a210-e77fc91cc7fc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a588819926ddd6cb118dd2c12e4cad29f96672df
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967537"
---
# <a name="total-cost-allocation-method"></a>Kopējo izmaksu sadalījuma metode

[!include [banner](../includes/banner.md)]

Kopējo izmaksu sadalījums (Total cost allocation — TCA) ir tādu izmaksu aprēķināšanas metode, kas jāsadala starp partijas pasūtījuma galvenās formulas krājumu un formulā noteiktajiem līdzproduktiem. Šī ir dinamiska metode. To izmantojot, tiek aprēķinātas izmaksas kā svērtā vidējā vērtība starp daudzumiem, kas formulas krājumā un līdzproduktiem reģistrēti kā pabeigti. Ja TCA metode tiek izmantota, nav jāpārskata katra partijas pasūtījuma izmaksu sadalījums. Ja TCA metode netiek izmantota, formulas aprēķinā tiek izmantota esošā funkcionalitāte.

## <a name="using-tca-for-coproducts"></a>TCA metodes izmantošana līdzproduktu aprēķinos
Tālāk ir sniegti daži norādījumi par TCA metodes izmantošanu līdzproduktu aprēķinos.

-   Ja tiek iestatīta formulas versijas slīdņa **Kopējo izmaksu sadalījums** opcija **Jā**, līdzproduktiem ir jānorāda izmaksu cena, kas ir lielāka par 0 (nulli). Vērtību formulai, kas nav saistīta ar vietu, var izgūt no tās pašas vietas vai no pirmās vietas aktīvo izmaksu versijas. Šis nosacījums tiek pārbaudīts, apstiprinot formulu.

    -   Jums nav nepieciešams manuāli ievadīt izmaksu sadalījuma procentus līdzproduktiem. Tā vietā sistēma izmaksu sadalījuma procentus izveido automātiski kā līdzproduktu aktīvo izmaksu cenu vidējo vērtību. 
    -   Jums nav nepieciešams ievadīt standarta izmaksas nestandarta izmaksu krājumiem, kas ir līdzprodukti. Sistēma ir pieejamas divu veidu izmaksu aprēķināšanas versijas: standarta izmaksas un plānotās izmaksas 
    -   Ja krājums netiek novērtēts pēc standarta izmaksu novērtēšanas metodes, ieteicams izmantot aktīvu izmaksu cenu plānoto izmaksu versijā. Šī cena tiek izmantota izmaksu novērtēšanai, piemēram, MK aprēķinos, ražošanas izmaksu novērtēšanā un regresa cenām krājumu novērtēšanas procesā. 

-   Ja tiek iestatīta formulas versijas slīdņa **Kopējo izmaksu sadalījums** opcija **Jā** un tālāk minētie nosacījumi ir patiesi, izmaksu sadalījuma metode ir **TCA** un izmaksu sadalījuma procentuālā vērtība nemainās.
    -   Tika pievienots līdzprodukts.
    -   Tika izmantota cita līdzproduktu izmaksu sadales metode.
-   Ja tiek iestatīta formulas versijas slīdņa **Kopējo izmaksu sadalījums** opcija **Nē** un tālāk minētie nosacījumi ir patiesi, tiek mainīta izmaksu sadalījuma metode **Manuāls** un izmaksu sadalījuma procentuālā vērtība nemainās.
    -   Tika pievienots līdzprodukts.
    -   Izmaksu sadalījuma procentuālā vērtība ir lielāka par 0 (nulli).
-   Lai varētu sekmīgi veikt formulas aprēķinus, vispirms ir jānovērtē izmaksu sadalījuma procentuālās vērtības. Šo darbību var izpildīt vai nu manuāli, vai izmantojot opciju **Novērtēt izmaksas** lapā **Līdzprodukti**. **Piezīme.** Opcija **Novērtēt izmaksas** ir pieejama tikai tad, ja ir iestatīta formulas versijas slīdņa **Kopējo izmaksu sadalījums** opcija **Jā**. Paredzamo sadalījumu var skatīt tad, ja partijas pasūtījuma daudzumi, kas reģistrēti kā pabeigti, atbilst daudzumiem, kas tiek norādīti formulā.
-   Ja partijas pasūtījums tiek izveidots manuāli vai tiek apstiprināts plānotais partijas pasūtījums, formulas versijas slīdņa **Kopējo izmaksu sadalījums** vērtība tiek iekopēta partijas pasūtījumā. Tomēr šo iestatījumu partijas pasūtījumā var mainīt. Ja ir iestatīta formulas versijas slīdņa **Kopējo izmaksu sadalījums** opcija **Nē** un pēc tam partijas pasūtījumam tiek mainīta opcija **Jā**, iestatītā katras rindas izmaksu sadalījuma metodes opcija **Manuāla** tiek mainīta uz **TCA**. Izmaksu sadalījuma opcija **Nav** netiek mainīta. Ja ir iestatīta formulas versijas slīdņa **Kopējo izmaksu sadalījums** opcija **Jā** un pēc tam tiek mainīta partijas pasūtījuma opcija **Nē**, iestatītā katra tipa **Produkcija** līdzprodukta izmaksu sadalījuma metode tiek mainīta uz **Manuāla**. Neviena novērtētā izmaksu sadalījuma procentuālā vērtība netiek mainīta.
-   Lapā **Līdzproduktu izmaksu sadalījums** ir redzama aprēķinātā izmaksu sadalījuma procentuālā vērtība. Šo lapu varat atvērt, izmantojot lapu **Partijas pasūtījums**. Šī informācija ir noderīga, ja reģistrētie produkti un daudzums atšķiras no plānotā vai ražot uzsāktā partijas pasūtījuma daudzuma. Kad izmaksu aprēķināšana ir pabeigta, jaunie procentuālie sadalījumi, kas iegūti, izmantojot TCA metodi, ir redzami lapā **Līdzproduktu izmaksu sadalījums**.

## <a name="calculating-the-burden-for-byproducts"></a>Blakusproduktu sloga aprēķināšana
Lauks **Blakusproduktu izmaksu sadalījums** lapā **Līdzprodukti** ir skaitītāja lauks, kas tiek izmantots tikai blakusproduktu transakcijās. Līdzproduktu transakcijās šī lauka vērtība vienmēr ir **Nav**. Blakusproduktu rindās šis lauks nosaka, kā blakusproduktu rindas izmaksu summa tiek pievienota kopējām ražošanas izmaksām. Pieejamas šādas opcijas

-   **Nav** ─ šajā blakusproduktu rindā ražošanas kopējām izmaksām netiek pievienota neviena summa.
-   **Procentuālā vērtība** ─ izmaksu summa tiek aprēķināta kā ražošanā patērēto izejmateriālu kopējo izmaksu procentuālā vērtība. Laukā tiek ievadīta aprēķinos izmantotā procentuālā vērtība.
-   **Uz vienu sēriju** ─ izmaksu summa tiek aprēķināta kā summa uz vienu ražošanas pasūtījuma standarta partijas lielumu. Šī summa ir atkarīga no ražošanā izmantotā reģistrētā daudzuma. Laukā tiek ievadīta aprēķinos izmantotā summa.
-   **Uz daudzuma vienības** ─ izmaksu summa tiek aprēķināta kā summa uz vienu reģistrēto ražošanā izmantoto formulas krājuma daudzuma vienību. Laukā tiek ievadīta aprēķinos izmantotā summa.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]