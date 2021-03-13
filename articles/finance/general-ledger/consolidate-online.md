---
title: Tiešsaistes finanšu konsolidācijas
description: Šajā tēmā ir aprakstītas tiešsaistes finanšu konsolidācijas Virsgrāmatā.
author: aprilolson
manager: AnnBe
ms.date: 07/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 91df786ed2298e21e7a3018b915c9bd5458efc32
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009247"
---
# <a name="online-financial-consolidations"></a>Tiešsaistes finanšu konsolidācijas

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstītas tiešsaistes finanšu konsolidācijas Virsgrāmatā. Pirms šīs tēmas lasīšanas noteikti jāizlasa tēma [Finanšu konsolidācijas un valūtas pārrēķināšanas pārskats](financial-consolidations-currency-translation.md).

Pēc tam, kad esat pabeidzis iestatīšanu, ievadiet konsolidācijas datus lapā **Konsolidēt [tiešsaistē]**. Kad esat beidzis, varat noklikšķināt uz **Labi** vai **Partija**, lai apstrādātu konsolidāciju.

## <a name="criteria"></a>Kritēriji
Cilnē **Kritēriji** lapā **Konsolidēt [tiešsaistē]** definējiet kontus, periodus un datu veidus, kas tiek konsolidēti.

![Cilne Kritēriji](./media/criteria-consolidate-online.png "Cilne Kritēriji")

Tālāk aprakstīts šīs cilnes dažādo lauku skaidrojums.

- **Apraksts** – ievadiet precīzu aprakstu par periodu, kas tiek konsolidēts.
- **Galvenais konts** – izmantojiet šīs sadaļas laukus, lai noteiktu galvenos kontus, kas tiks apstrādāti.

    - **No** un **līdz** – norādiet apstrādājamo kontu diapazonu. Atstājot šos laukus tukšus, visu uzņēmumu visi konti tiks pārvietoti uz konsolidācijas uzņēmumu. Tādēļ, ja konsolidējat četrus uzņēmumus un katram uzņēmumam ir cits kontu plāns, visu četru uzņēmumu visi konti tiks izveidoti konsolidācijas uzņēmumā.
    - **Konsolidācijas konta izmantošana** — ja šī opcija ir iestatīta kā **Jā**, lauks **Atlasīt konsolidācijas kontu no** kļūst pieejams. Šajā laukā atlasiet, vai visi konti ir jākonsolidē konsolidācijas kontā, kas ir iestatīts lapā **Galvenie konti**, vai arī, vai vēlaties atlasīt kontu no kādas konsolidācijas kontu grupas.
    - **Konsolidācijas kontu grupa** – atlasiet grupu, kuru izmantot galvenā konta kartēšanai konsolidācijai.

- **Konsolidācijas periods** – izmantojiet šīs sadaļas laukus, lai definētu konsolidācijas periodu.

    - **No** un **līdz** – norādiet konsolidācijas datumu diapazonu. Atstājot šo lauku tukšu, konsolidācija tiks veikta visiem periodiem, kas definēti uzņēmuma Virsgrāmatas kalendārā. Ieteicams neatstāt šos laukus tukšus.
    - **Ietvert faktiskās summas** – iestatiet šo opciju kā **Jā**, lai konsolidētu faktiskos datus.
    - **Ietvert budžeta summas** – iestatiet šo opciju kā **Jā**, lai konsolidētu budžeta reģistra datus.
    - **Atjaunot bilances konsolidācijas laikā** – nav ieteicams, ka šī opcija ir iestatīta kā **Jā**. Tā vietā atjaunojiet bilances kā atsevišķu pakešuzdevumu.

- **Budžeta modeļi** — ja esat atlasījis konsolidēšanai budžeta datus, izmantojiet šīs sadaļas laukus, lai definētu budžeta modeļus.

    - **No** un **līdz** – norādiet izmantojamo modeļu diapazonu.
    - **Budžeta kursa tips** – atlasiet budžeta kursa tipu, ko izmantot budžeta datu valūtas pārrēķināšanā.

## <a name="financial-dimensions"></a>Finanšu dimensijas
Cilnē **Finanšu dimensijas** varat definēt dimensijas, kuras jāiekļauj konsolidācijas uzņēmumā. Lai atlasītu dimensiju, iestatiet lauku **Specifikācija** pozīcijā **Dimensija**, un pēc tam nosakiet dimensijas secību konsolidētajā uzņēmumā.

![Cilne Finanšu dimensijas](./media/financial-dimensions-cons.png "Cilne Finanšu dimensijas")

Neatkarīgi no jūsu definētās secības **Galvenais konts** vienmēr būs pirmais segments.

## <a name="legal-entities"></a>Juridiskas personas
Cilnē **Juridiskās personas** varat definēt uzņēmumus, kuri jāiekļauj konsolidācijas uzņēmumā. Jūs arī nosakāt šo uzņēmumu īpašumtiesību procentu. Ja norādāt mazāk nekā 100 procentu īpašumtiesības, norādītā procentuālā vērtību tiks apkopota konsolidācijas uzņēmumā. Atšķirīgu pārrēķināšanu gadījumā lauks **Konta veids konvertācijas atšķirībām** tiek izmantots, lai atlasītu galveno kontu no iestatījuma lapā **Konti automātiskām transakcijām**.

![Cilne Juridiskās personas](./media/legal-entities-cons.png "Cilne Juridiskās personas")

![Lapa Automātisko darījumu konti](./media/accounts-for-automatic-cons.png "Lapa Automātisko darījumu konti")

## <a name="elimination"></a>Korekcijas
Cilnē **Eliminācija** ir trīs tālāk aprakstītās iespējas elimināciju apstrādei.

- Atlasiet eliminācijas kārtulu un pēc tam laukā **Piedāvājumu opcijas** atlasiet **Tikai piedāvājums**. Šī opcija apstrādā elimināciju konsolidācijas procesa laikā, bet negrāmato visu vienā darbībā. Žurnālu var grāmatot vēlāk.
- Atlasiet eliminācijas kārtulu un pēc tam laukā **Piedāvājumu opcijas** atlasiet **Tikai grāmatot**. Šī opcija apstrādā elimināciju konsolidācijas procesa laikā un visu grāmato vienā darbībā.
- Apstrādājiet eliminācijas piedāvājumu atsevišķi no konsolidācijas procesa, izmantojot eliminācijas žurnālu.

![Cilne Korekcijas](./media/elimination-cons-onl.png "Cilne Korekcijas")

Plašāku informāciju par eliminācijām skatiet sadaļā [Eliminācijas kārtulas](./elimination-rules.md).

## <a name="currency-translation"></a>Valūtas pārrēķināšana
Cilnē **Valūtas pārrēķināšana** varat noteikt juridisko personu kontu un maiņas kursa tipu un kursu. Laukā **Lietot maiņas kursu no** ir pieejamas trīs tālāk minētās opcijas.

- **Konsolidācijas datums** – konsolidācijas datums tiks izmantots, lai iegūtu maiņas kursu. Šis kurss ir līdzvērtīgs tābrīža vai mēneša beigu kursam. Kursa priekšskatījumu varēs redzēt, bet nevarēs rediģēt.
- **Transakcijas datums** – katras transakcijas datums tiks izmantots, lai atlasītu maiņas kursu. Šī opcija visbiežāk tiek izmantota pamatlīdzekļiem, un to bieži sauc par vēsturisko kursu. Kursa priekšskatījumu nevarēs redzēt, jo būs daudz dažādu transakciju kursu konta diapazonā.
- **Lietotāja noteiktais kursa** – pēc tam, kad ir atlasīta šī opcija, var ievadīt vēlamo maiņas kursu. Šī opcija var būt noderīga vidējiem maiņas kursiem vai veicot konsolidēšanu ar fiksētu valūtas kursu.

![Cilne Valūtas pārrēķināšana](./media/currency-translation-cons-online.png "Cilne Valūtas pārrēķināšana")

## <a name="additional-resources"></a>Papildu resursi

Lai iegūtu papildu informāciju par konsolidāciju un valūtas pārrēķiniem, skatiet šīs tēmas pamata tēmu [Finanšu konsolidācijas un valūtas pārrēķināšanas pārskats](./financial-consolidations-currency-translation.md).

Informāciju par scenārijiem, kuros varētu veidot konsolidētos finanšu pārskatus, skatiet sadaļu[Konsolidēto finanšu pārskatu veidošana](./generating-consolidated-financial-statements.md).
