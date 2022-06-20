---
title: Datuma un laika parametri, kas tiek izmantoti Plānošanas optimizācijai
description: Šajā rakstā ir sniegta informācija par datuma un laika parametriem, ko plānošanas optimizēšana izmanto tās operācijas laikā.
author: t-benebo
ms.date: 09/21/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-09-21
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 807834bf5cd062ed24e5e3f3512d8389717a2d39
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885904"
---
# <a name="date-and-time-parameters-used-by-planning-optimization"></a>Datuma un laika parametri, kas tiek izmantoti Plānošanas optimizācijai

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir sniegta informācija par datuma un laika parametriem, ko plānošanas optimizēšana izmanto tās operācijas laikā.

Turpretim iebūvētajā vispārējās plānošanas programmā tiek izmantoti darbību datumi visos aprēķinos, bet Plānošanas optimizācija darbojas ar datuma un laika vērtībām, kas tiek konvertētas uz datumiem. Šī atšķirības uzvedība var izraisīt situācijas, kad, piemēram, budžeta darbības, kas ir izveidotas pusnaktī tajā dienā, kad ir palaista vispārējā plānošana, nav iekļautas, jo Plānošanas optimizācija apsver, ka tās ir izveidotas pirms pašreizējā datuma.

## <a name="parameters-for-issue-and-demand-transactions"></a>Izejas plūsmas un pieprasījuma darbību parametri

Šajā tabulā uzskaitīti parametri, ko izmanto Plānošanas optimizācijai, kad tā apstrādā izejas plūsmas un pieprasījuma transakcijas.

| Parametrs | Parametri, kas netiek izmantoti Plānošanas optimizācijai | Apraksts | Ekvivalents lauks programmā Microsoft Dynamics 365 Supply Chain Management (tabulā ReqTrans) |
|---|---|---|---|
| Plānotais izsniegšanas laiks | `PlannedIssueTime` | Datums, kurā ir plānota izsniegšana. | **Uz datumu** (`FuturesDate`) un **Atlikts līdz laikam** (`FuturesTime`) |
| Pieprasītais izsniegšanas laiks | `RequestedIssueTime` | Datums, kad lietotājs pieprasīja un iestatīja Supply Chain Management. Šis parametrs ir izmantojams tikai nodotajiem vai apstiprinātajiem plānotajiem pasūtījumiem. Plānotiem pasūtījumiem tas pēc noklusējuma ir tukšs. | **Pieprasītais datums** (`ReqDateDlvOrig`) |
| Pieprasītais izsniegšanas laiks | `RequiredIssueTime` | Pieprasītais izsniegšanas datums, kas ir pielāgots, veicot Plānošanas optimizāciju. Ja pieprasītais izsniegšanas laiks ir pagātnē, kad ir palaista Plānošanas optimizācija, nepieciešamais izdošanas laiks tiks pielāgots pirmajai atvērtajai dienai, kas nav agrāka par šodienas datumu. Ja kalendārā pieprasītais izdošanas laiks ir atzīmēts kā bloķēts, nepieciešamais izdošanas laiks tiks pielāgots pirmajai atvērtai dienai pirms šī datuma. | **Vajadzības datums** (`ReqDate`) un **Vajadzības laiks** (`ReqTime`) |
| Izsniegšanas laika aizkave | `IssueTimeDelay` | Laika starpība starp plānoto izdošanas laiku un pieprasīto izdošanas laiku apstiprinātajiem un izpildei nodotajiem pasūtījumiem vai pieprasīto izdošanas laiku. | **Aizkave (dienās)** (`FuturesDays`) |

## <a name="parameters-for-receipt-and-supply-transactions"></a>Saņemšanas un piegādes darbību parametri

Šajā tabulā uzskaitīti parametri, ko izmanto Plānošanas optimizācijai, kad tā apstrādā izejas plūsmas un pieprasījuma transakcijas.

| Parametrs | Parametri, kas netiek izmantoti Plānošanas optimizācijai | Apraksts | Ekvivalents lauks Supply Chain Management (tabulā ReqTrans vai ReqPO) |
|---|---|---|---|
| Plānotais pieejamības laiks | `PlannedAvailabilityTime` | Datums, kad ieejas plūsma tiek plānota pieejama. | **Vajadzības datums** (`ReqDate`) un **Vajadzības laiks** (`ReqTime`) |
| Plānotais ieejas plūsmas laiks | `PlannedReceiptTime` | Datums, kad kvīts tiks saņemtā atrašanās vietā. | **Līdz datumam (**`FuturesDate`), **Atlikts līdz laikam** (`FuturesTime`) un **Piegādes datumam** (`ReqDateDlv`) vai **Pieprasītajam datumam** (`ReqDateDlvOrig`), ja pasūtījums vēl nav nodots izpildei. |
| Pieprasītais pieejamības laiks | `RequiredAvailabilityTime` | Pieprasītais izsniegšanas datums, kas ir pielāgots, veicot Plānošanas optimizāciju. | **Vajadzības datums** (`ReqDate`) un **Vajadzības laiks** (`ReqTime`) |
| Plānotais ieejas plūsmas laiks | `ExpectedReceiptTime` | Paredzamais izpildei nodotās ieejas plūsmas datums. Lietotājs ir iestatījis vērtību Supply Chain Management, un Plānošanas optimizācijā tā nav pielāgota. Šis parametrs attiecas tikai uz izdotajām ieejas plūsmām. | **Pieprasītais datums** (`ReqDateDlvOrig`) |
| Nepieciešamais saņemšanas laiks | `RequiredReceiptTime` | Pieprasītais ieejas plūsmas datums, kas ir pielāgots, veicot Plānošanas optimizāciju. | **Vajadzības datums** (`ReqDate`) un **Vajadzības laiks** (`ReqTime`) |
| Plānotais pasūtīšanas laiks | `PlannedOrderingTime` | Pasūtīšanas datums, kas ir aprēķināts, veicot Plānošanas optimizāciju. | **Pasūtījuma datums** (`ReqDateOrder`) un **Pasūtījuma laiks** (`ReqTimeOrder`) |
| Plānotais aktivitātes sākuma laiks | `PlannedActivityStartTime` | Datums, kad jāsākas šīs ieejas plūsmas aktivitātei. | **Sākuma datums** (`SchedFromDate`) |
| Ieejas plūsmas laika aizkave | `ReceiptTimeDelay` | Laika starpība starp plānoto ieejas plūsmas laiku un pieprasīto ieejas plūsmas laiku. | **Aizkave (dienas)** (`FuturesDays`) un **Aizkave līdz laikam** (`FuturesTime`) |

## <a name="examples-of-date-parameter-use-by-planning-optimization"></a>Datuma parametru piemēri, kas tiek izmantoti Plānošanas optimizācijai

Šajās ilustrācijās attēlotie plāni ir dienas līmenī, taču Plānošanas optimizācija tiek palaista detalizētāk. Piemēram, tāpēc, ka rezerves var būt stundās, plānošanas pasūtīšanas laiks var būt 2021. gada 22. janvāris, plkst. 11.35 un tā tālāk.

### <a name="example-1-simple-scenario"></a>1. piemērs: vienkāršs scenārijs

Vienu pārdošanas pasūtījumu, kura izdošanas laiks ir pieprasīts 22. janvārī, sedz viens pirkšanas pasūtījums. Tiek izmantoti šādi iestatījumi:

- Nav izpildes laika
- Nav kalendāra (Visas dienas ir atvērtas.)
- Nav uzcenojuma

Tālāk redzamajā attēlā parādīts šis piemērs. (Atlasiet ilustrāciju, lai atvērtu lielāku versiju.)

[![Vienkāršs scenārijs.](media/planning-service-dates-1-small.png)](media/planning-service-dates-1.png)

### <a name="example-2-lead-time-scenario"></a>2. piemērs: Izpildes laika scenārijs

Vienu pārdošanas pasūtījumu, kura izdošanas laiks ir pieprasīts 22. janvārī, sedz viens pirkšanas pasūtījums. Tiek izmantoti šādi iestatījumi:

- Trīs izpildes laika dienas
- Nav kalendāra (Visas dienas ir atvērtas.)
- Nav uzcenojuma

Tālāk redzamajā attēlā parādīts šis piemērs. (Atlasiet ilustrāciju, lai atvērtu lielāku versiju.)

[![2. piemērs: Izpildes laika scenārijs.](media/planning-service-dates-2-small.png)](media/planning-service-dates-2.png)

### <a name="example-3-margin-scenario"></a>3. piemērs: uzcenojuma scenārijs

Vienu pārdošanas pasūtījumu, kura izdošanas laiks ir pieprasīts 22. janvārī, sedz viens pirkšanas pasūtījums. Tiek izmantoti šādi iestatījumi:

- Trīs izpildes laika dienas
- Pasūtīšanas uzcenojums četras dienas
- Piecu dienu pieejamības uzcenojums
- Nav kalendāra (Visas dienas ir atvērtas.)

Tālāk redzamajā attēlā parādīts šis piemērs. (Atlasiet ilustrāciju, lai atvērtu lielāku versiju.)

[![Uzcenojuma scenārijs.](media/planning-service-dates-3-small.png)](media/planning-service-dates-3.png)

### <a name="example-4-delay-scenario"></a>4. piemērs: aizkaves scenārijs

Vienu pārdošanas pasūtījumu, kura izdošanas laiks ir pieprasīts 22. janvārī, sedz viens pirkšanas pasūtījums. Šis piemērs izmanto tos pašus iestatījumus kā 3. piemērā, bet plānošanas datums ir pārvietots uz 15. janvāri. Atpakaļejoša plānošana (sarkani marķieri) neizdodas, jo plānotajam pasūtīšanas laikam būtu jābūt pirms šodienas datuma. Tāpēc vispārējā plānošana ir jāplāno uz priekšu, un rodas aizkaves.

Tālāk redzamajā attēlā parādīts šis piemērs. (Atlasiet ilustrāciju, lai atvērtu lielāku versiju.)

[![Aizkaves scenārijs.](media/planning-service-dates-4-small.png)](media/planning-service-dates-4.png)

### <a name="example-5-transfer-scenario"></a>5. piemērs: Pārsūtīšanas scenārijs

Vienu pārdošanas pasūtījumu no 1. noliktavas, kuram 22. janvārī ir pieprasīts izdošanas laiks, nosedz viens pārsūtīšanas pasūtījums no 2. noliktavas, ko sedz plānotais pirkšanas pasūtījums. Tiek izmantoti šādi iestatījumi:

- Trīs pārsūtīšanas izpildes laika dienas (1. noliktava)
- Divas pirkšanas izpildes laika dienas (2. noliktava)
- Nav kalendāra (Visas dienas ir atvērtas.)

Tālāk redzamajā attēlā parādīts šis piemērs. (Atlasiet ilustrāciju, lai atvērtu lielāku versiju.)

[![Pārsūtīšanas scenārijs.](media/planning-service-dates-5-small.png)](media/planning-service-dates-5.png)

### <a name="example-6-lead-time-with-calendars-scenario"></a>6. piemērs: izpildes laiks ar kalendāru scenāriju

Vienu pārdošanas pasūtījumu, kura izdošanas laiks ir pieprasīts 22. janvārī, sedz viens pirkšanas pasūtījums. Tiek izmantoti šādi iestatījumi:

- Trīs izpildes laika dienas
- Izdošanas kalendārs (slēgts piektdienā)
- Pieejamības kalendārs (slēgts ceturtdienā un piektdienā)
- Saņemšanas kalendārs (slēgts otrdienā, trešdienā un svētdienā)
- Izpildes laika kalendārs (slēgts ceturtdienā un piektdienā)
- Pasūtījumu kalendārs (atvērts pirmdienā un sestdienā)

Tālāk redzamajā attēlā parādīts šis piemērs. (Atlasiet ilustrāciju, lai atvērtu lielāku versiju.)

[![Izpildes laiks ar kalendāru scenāriju.](media/planning-service-dates-6-small.png)](media/planning-service-dates-6.png)

### <a name="example-7-delay-with-calendars-scenario"></a>7. piemērs: aizkave ar kalendāru scenāriju

Vienu pārdošanas pasūtījumu, kura izdošanas laiks ir pieprasīts 22. janvārī, sedz viens pirkšanas pasūtījums. Šis piemērs izmanto tos pašus iestatījumus kā 6. piemērā, bet plānošanas datums ir pārvietots uz 13. janvāri. Atpakaļejoša plānošana (sarkani marķieri) neizdodas, jo plānotajam pasūtīšanas laikam būtu jābūt pirms šodienas datuma. Tāpēc vispārējā plānošana ir jāplāno uz priekšu, un rodas aizkaves.

Tālāk redzamajā attēlā parādīts šis piemērs. (Atlasiet ilustrāciju, lai atvērtu lielāku versiju.)

[![Aizkave ar kalendāru scenāriju.](media/planning-service-dates-7-small.png)](media/planning-service-dates-7.png)
