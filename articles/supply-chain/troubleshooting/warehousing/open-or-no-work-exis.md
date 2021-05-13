---
title: Sūtījumu nevar apstiprināt nepabeigta vai trūkstoša darba dēļ
description: Sūtījumu nevar apstiprināt nepabeigta vai trūkstoša darba dēļ
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: da6388d433d6021a99840ae9781c717db1b540a9
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938512"
---
# <a name="you-cant-confirm-a-shipment-because-of-incomplete-or-missing-work"></a>Sūtījumu nevar apstiprināt nepabeigta vai trūkstoša darba dēļ

Kļūdas kods: WAX515

## <a name="symptoms"></a>Simptomi

Mēģinot apstiprināt kravu, sistēma rāda šādu kļūdas ziņojumu:

> Kravas %1 nosūtīšanu nevarēja apstiprināt, jo bija jāpabeidz visi ar kravu saistītie darbi.

Tādēļ kravas nosūtīšanu nevar apstiprināt.

## <a name="cause"></a>Iemesls

Krava vai sūtījums pašlaik ir stāvoklī, kad sūtījuma apstiprināšana neizdodas. Pirms varat apstiprināt sūtījumu, kravai ir jāpastāv vismaz dažiem darbiem, un visiem darbiem ir jābūt statusam *Slēgts* vai *Atcelts*.

## <a name="resolution"></a>Novēršana

Pārbaudiet ar kravu vai sūtījumu saistītos pārdošanas pasūtījumus vai pārsūtīšanas pasūtījumus un pārliecinieties, ka viss saistītais darbs ir pabeigts vai atcelts.

Varat strādāt ar sūtījumiem un kravām vairākās lapās. Tālāk ir sniegti daži piemēri.

### <a name="all-loads-page"></a>Visu kravu lapa

1. Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.
1. Izvēlieties kravu, kam nevar apstiprināt nosūtījumu.
1. Darbību rūtī cilnē **Kravas** grupā **Saistīta informācija** atlasiet **Darbs**.
1. Pārbaudiet katra darba ID statusu. Sekojiet katram darba ID, kura statuss nav *Slēgts* vai *Atcelts*.
1. Kad katram darba ID statuss *Slēgts* vai *Atcelts*, mēģiniet vēlreiz apstiprināt sūtījumu.

### <a name="all-shipments-page"></a>Visu sūtījumu lapa

1. Dodieties uz **Noliktavas pārvaldība \> Sūtījumi\> Visi sūtījumi**.
1. Izvēlieties sūtījumu, ko nevar apstiprināt.
1. Darbību rūtī cilnē **Sūtījumi** grupā **Darbs** atlasiet **Detalizēta informācija par darbu**.
1. Pārbaudiet katra darba ID statusu. Sekojiet katram darba ID, kura statuss nav *Slēgts* vai *Atcelts*.
1. Kad katram darba ID statuss *Slēgts* vai *Atcelts*, mēģiniet vēlreiz apstiprināt sūtījumu.

### <a name="all-work-page"></a>Visa darba lapa

1. Dodieties uz **Noliktavas pārvaldība \> Darbs\> Viss darbs**.
1. Atlasiet darbu pasūtījuma numuram, kam nevar apstiprināt sūtījumu.
1. Darbību rūtī, cilnē **Sūtījums**, grupā **Sūtījums** atlasiet **Apstiprināt sūtījumu**.
1. Pārbaudiet katra darba ID statusu. Sekojiet katram darba ID, kura statuss nav *Slēgts* vai *Atcelts*.
1. Kad katram darba ID statuss *Slēgts* vai *Atcelts*, mēģiniet vēlreiz apstiprināt sūtījumu.
