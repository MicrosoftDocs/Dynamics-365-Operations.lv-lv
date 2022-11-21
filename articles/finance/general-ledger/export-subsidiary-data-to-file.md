---
title: Filiāļu datu eksportēšana uz failiem
description: Šajā rakstā skaidrots, kā sagatavoties datu eksportēšanai no Microsoft Dynamics 365 Finanšu un pēc tam importēt tos konsolidētā juridiskajā persona.
author: jinniew
ms.date: 11/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 30d69f9a2813621df410a29568644f264392fb49
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779966"
---
# <a name="export-subsidiary-data-to-files"></a>Filiāļu datu eksportēšana uz failiem

[!include [banner](../includes/banner.md)]

Jūs izmantojat lapu **Eksportēt** (**Sistēmas administrēšana \> Darbvietas \> Importēt/eksportēt**), lai sagatavotu filiāli datu eksportēšanai uz failiem, kurus pēc tam var importēt konsolidētā juridiskajā personā. Papildinformāciju par importēšanas un eksportēšanas procesiem skatiet [Datu importēšanas un eksportēšanas darbu apskatā](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).

1. Juridiskas personas izveidošana konsolidācijas procesam. Informāciju par to, kā izveidot juridiskās personas, skatiet sadaļā [Juridiskas personas izveidošana](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md). Papildinformāciju skatiet sadaļās [Juridiskas personas sagatavošana izmantošanai konsolidācijas procesā](prepare-company-for-consolidation.md) un [Meitasuzņēmuma juridiskās personas konsolidācijas iestatīšana](set-up-subsidiary-company-for-consolidation.md). 

2. Dodieties uz **Konsolidācijas \> Eksportēt uzņēmuma bilances**. Lapas **Eksportēt uzņēmuma bilances** cilnē **Kritēriji** norādiet informāciju par konsolidāciju, iestatot tālāk esošos laukus.

    | Lauks                             | Apraksts |
    |-----------------------------------|-------|
    | **Galvenais konts**                      | Norādiet konsolidācijas kontus. Lai iekļautu visus kontus, atstājiet šo lauku tukšu. |
    | **Izmantot šādu konsolidācijas kontu**         | Ja esat norādījuši konsolidācijas kontus, iestatiet šo opciju uz **Jā**. |
    | **Atlasīt konsolidācijas kontu no** | Atlasiet **Galveno kontu** vai **Konsolidācijas kontu grupu**. |
    | **Konsolidācijas kontu grupa**       | Izvēlieties konsolidācijas kontu grupu izvēlētajam konsolidācijas kontam. |
    | **Konsolidācijas periods**              | Norādiet konsolidācijas "no" un "līdz" datumus. |
    | **Ietvert faktiskās summas**            | Iestatiet šo opciju uz **Jā**, lai iekļautu faktiskos kontus. |
    | **Ietvert budžeta summas**            | Iestatiet šo opciju uz **Jā**, lai ietvertu budžeta summas konsolidācijās. |
    | **Budžeta modeļi**                     | Norādiet iekļaujamā budžeta modeli. |

3. Cilnē **Finanšu dimensijas** norādiet konsolidācijas datus:

    - Norādiet finanšu dimensiju informāciju, kam jābūt pārsūtītai no meitasuzņēmuma kontu darījumiem uz darījumiem konsolidētajā juridiskajā personā.
    - Atlasiet finanšu dimensijas sarakstā.
    - Norādiet pareizu specifikāciju katrai konsolidētai finanšu dimensijai. Pieejamās opcijas ietver **Dimensiju**, **Grupas dimensiju**, **Uzņēmuma kontus** un **Kontu**.

        > [!NOTE]
        > **Grupas dimensijas** opcija ļauj definēt dimensijas vērtību, ko izmanto uzņēmumu grupa, kas tiek konsolidēta.

    - Norādiet konsolidējamo segmenta pasūtījumu.

4. Cilnē **Juridiskās personas** izpildiet šos soļus, lai norādītu juridisko personu, kuru eksportējat:

    1. Atlasiet **Jauns**.
    2. Laukā **Avota juridiskā persona** ievadiet juridisko personu.

        Ja vairākiem meitasuzņēmumiem, kas atrodas vienā datu bāzē, atbilst tie paši kritēriji, ir iespējams pārsūtīt datus no šiem meitasuzņēmumiem uz atsevišķiem eksporta failiem vienā transakcijā:

        1. Izveidojiet rindu katrai meitasuzņēmuma juridiskajai iestādei, kuras konti tiks eksportēti uz failiem. Šie faili vēlāk tiks importēti konsolidētajā juridiskajā uzņēmumā.
        2. Katrai filiālei ievadiet filiāles nosaukumu un eksporta faila nosaukumu, kurš tiks izveidots eksporta uzdevuma veikšanas laikā.

    3. Laukā **Konvertēšanas starpības konta tips** atlasiet **Peļņa un zaudējumi** vai **Bilance**.
    4. Ievadiet nosaukumu eksporta failam, kas tiks izveidots.

5. Atlasiet **Labi**, lai palaistu eksportu.

Kad eksports ir pabeigts, parādās ziņojums, kas uzskaita ierakstu daudzumu, kas tikuši saglabāti katrā failā. Pēc tam failus varat importēt konsolidētajā juridiskajā personā.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
