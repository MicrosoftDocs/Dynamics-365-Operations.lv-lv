---
title: Nevar apstiprināt sūtījumu, jo kalendārā radās problēma
description: Nevar apstiprināt sūtījumu, jo kalendārā radās problēma
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
ms.openlocfilehash: f1fccd10d8867252f32b37c77f9a3bad54157bdd
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938513"
---
# <a name="you-cant-confirm-a-shipment-because-of-an-issue-with-the-calendar"></a>Nevar apstiprināt sūtījumu, jo kalendārā radās problēma

Kļūdas kods: TRX2716

## <a name="symptoms"></a>Simptomi

Mēģinot apstiprināt kravu, sistēma rāda šādu kļūdas ziņojumu:

> Kalendāra tipam %1 ir nepieciešams paņemt un atdot norīkojumu %2.

Tādēļ kravas nosūtīšanu nevar apstiprināt.

## <a name="cause"></a>Iemesls

Kravai pastāv aktīvie norīkojumi. Piemēram, pastāv kārtula, saskaņā ar kuru ir pieprasīta autovadītāja atdošana. Tādēļ noslodze pašlaik ir stāvoklī, kad sūtījuma apstiprināšana neizdodas.

## <a name="resolution"></a>Novēršana

Jums ir jāizpēta un jāizlabo problēmas ar aktīvajiem norīkojumi, kas ir saistītas ar krāvu.

1. Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.
1. Izvēlieties kravu, kam nevar apstiprināt nosūtījumu.
1. Darbību rūts cilnes **Transportācija** grupā **Norīkojumi** atlasiet **Norīkojumu plānošana**.
1. Izpildiet kādu no šīm darbībām:

    - Pārliecinieties, vai norīkojuma laikā ir pabeigta autovadītāja atdošana/paņemšana.
    - Pabeidziet vai atceliet norīkojumu.
    - Atspējot opciju **Pieprasītā autovadītāja atdošana** saistītajā norīkojuma kārtulā.
