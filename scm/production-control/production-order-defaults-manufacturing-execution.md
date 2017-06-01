---
title: "Ražošanas pasūtījuma noklusējuma vērtības ražošanas izpildes procesā"
description: 
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JmgProdParameters
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 70073
ms.assetid: 620944ae-3e20-444a-807e-65495f160904
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: af6e6db2523041dd8dbcef692c252c596802c22d
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="production-order-defaults-in-manufacturing-execution"></a>Ražošanas pasūtījuma noklusējuma vērtības ražošanas izpildes procesā

[!include[banner](../includes/banner.md)]




Pirms nodarbinātie sāk reģistrēt ražošanas darbus, nopietni apsveriet visus iestatījumus lapā **Ražošanas pasūtījuma noklusējuma vērtības**. Ja jūsu uzņēmums izmanto vairākvietu funkcijas, iespējams, vēlaties katrai vietai iestatīt atšķirīgas ražošanas pasūtījumu noklusējuma vērtības. Pasūtījuma noklusējuma vērtības integrācijai ar moduli Ražošanas kontrole tiek iestatītas tālāk norādītajās lapas **Ražošanas pasūtījuma noklusējuma vērtības** cilnēs.

-   **Vispārīgi** — vispārīgas pasūtījuma noklusējuma vērtības ražošanas darbiem modulī Ražošanas izpilde.
-   **Sākšana** — pasūtījuma noklusējuma vērtības, kas tiek izmantotas, kad tiek sākti ražošanas darbi vai operācijas.
-   **Operācijas** — pasūtījuma noklusējuma vērtības, kas tiek lietotas ražošanas darbiem vai operācijām un atsauksmēm par operācijām ražošanas procesa laikā.
-   **Reģistrēt pabeigšanu** — pasūtījuma noklusējuma vērtības, kas tiek lietotas, kad krājumi tiek reģistrēti kā pabeigti, veicot ražošanas pasūtījuma pēdējo operāciju.
-   **Daudzuma pārbaude** — pasūtījuma noklusējuma vērtības, kas ir paredzētas sākuma un atsauksmju daudzumu pārbaudei ražošanas pasūtījumos.

## <a name="types-of-production-jobs"></a>Ražošanas darbu tipi
Cilnē **Operācijas** varat atlasīt ražošanas darbu tipus, kuriem ir jāreģistrējas lapā **Darba reģistrācija**. Parasti darbinieki reģistrējas iestatīšanas darbiem un procesa darbiem. Taču, ja tiek izmantota darbu plānošana, varat atlasīt citus darbu tipus, piemēram, transportēšanas darbus, kam darbiniekiem ir jāreģistrējas, apstrādājot ražošanas pasūtījumu. **Svarīgi.** Pārliecinieties, ka ir atlasīti visi atbilstošie darbu tipi. Pretējā gadījumā darbi var nebūt pieejami reģistrācijai lapā **Darba reģistrācija**. Saskaņojiet atlasi ar atlasi, kas tika veikta kolonnā **Darbu vadība** lapā **Maršrutu grupas**. Ja lapā Maršrutu grupas ir atlasīta opcija **Darbu vadību**, šis darba tips tiek reģistrēts kā pabeigts ražošanas pasūtījumā. Šī reģistrēšana tiek veikta tad, kad darbs tiek reģistrēts kā pabeigts modulī Ražošanas izpilde. Kad visi operācijas darbu tipi, kam ir atlasīta opcija **Darbu vadība**, ir reģistrēti kā pabeigti, arī operācija tiek reģistrēta kā pabeigta modulī Ražošanas izpilde. **Piezīme.** Dažus darbu tipus var reģistrēt manuāli, izmantojot ražošanas žurnālus. Šādā gadījumā atlasiet darba tipam opciju **Darbu vadība**, taču neatlasiet darba tipu reģistrācijai cilnē **Operācijas** lapā **Ražošanas pasūtījuma noklusējuma vērtības**.

## <a name="bom-consumption-and-picking-list-journals"></a>MK patēriņš un izdošanas sarakstu žurnāli
Materiālus var iestatīt tā, lai tie ražošanas laikā tiktu patērēti automātiski vai manuāli. Automātiskais patēriņš tiek kontrolēts, izmantojot norakstīšanas principu, kas ir iestatīts uz materiālu komplekta (MK) rindās, un lauka **Automātisks MK patēriņš** iestatījumu lapā Ražošanas pasūtījuma noklusējuma vērtības. Automātisko patēriņu var iestatīt tā, lai tas notiktu tad, kad ražošanas pasūtījums tiek sākts vai reģistrēts kā pabeigts. Tas var notikt arī darba līmenī, kad darbs tiek sākts vai pabeigts.

### <a name="controlling-material-consumption-when-a-production-order-is-started"></a>Materiālu patēriņa kontrolēšana, kad tiek sākts ražošanas pasūtījums

Materiālu patēriņš ražošanas pasūtījuma sākšanas laikā tiek kontrolēts, izmantojot lauku **Automātisks MK patēriņš** cilnē **Sākšana**. Ir pieejamas šādas vērtības:

-   **Norakstīšanas princips** — kad tiek sākts ražošanas pasūtījums, materiālu daudzumi tiek patērēti atbilstoši norakstīšanas principam, kas ir iestatīts ražošanas MK rindās. Ražošanas sākšanas laikā tiek patērētas tikai tās materiālu rindas, kurās ir iestatīts norakstīšanas princips **Sākt**.
-   **Vienmēr** — vienmēr tiek patērēti materiālu daudzumi, kas ir proporcionāli sākšanas daudzumam.
-   **Nekad** — materiālu daudzumi nekad netiek patērēti.

### <a name="controlling-material-consumption-when-a-production-job-is-started-or-completed"></a>Materiālu patēriņa kontrolēšana, kad tiek sākts vai pabeigts ražošanas darbs

Materiālu patēriņš ražošanas darba sākšanas vai pabeigšanas laikā tiek kontrolēts, izmantojot lauku **Automātisks MK patēriņš** cilnē **Operācijas**. Ir pieejamas šādas vērtības:

-   **Norakstīšanas princips** — kad tiek sākts vai pabeigts ražošanas darba daudzums, materiālu daudzumi tiek patērēti atbilstoši norakstīšanas principam, kas ir iestatīts ražošanas MK rindās. Tiek patērētas tikai tās materiālu rindas, kurās ir iestatīts norakstīšanas princips **Sākt** vai **Pabeigt**.
-   **Vienmēr** — vienmēr tiek patērēti materiālu daudzumi, kas ir proporcionāli darba sākšanas daudzumam.
-   **Nekad** — materiālu daudzumi nekad netiek patērēti.

### <a name="controlling-material-consumption-when-a-production-order-is-reported-as-finished"></a>Materiālu patēriņa kontrolēšana, kad ražošanas pasūtījums tiek reģistrēts kā pabeigts

Materiālu patēriņš pabeigšanas reģistrēšanas procesa laikā tiek kontrolēts, izmantojot lauku **Automātisks MK patēriņš** cilnē **Reģistrēt pabeigšanu**. Ir pieejamas šādas vērtības:

-   **Norakstīšanas princips** — kad ražošanas pasūtījums tiek reģistrēts kā pabeigts, materiālu daudzumi tiek patērēti atbilstoši norakstīšanas principam, kas ir iestatīts ražošanas MK rindās. Tiek patērētas tikai tās materiālu rindas, kurās ir iestatīts norakstīšanas princips **Pabeigt**.
-   **Vienmēr** — vienmēr tiek patērēti materiālu daudzumi, kas ir proporcionāli daudzumam, kas ir reģistrēts kā pabeigts.
-   **Nekad** — materiālu daudzumi nekad netiek patērēti.





