---
title: Algas pozīcijas darbs
description: Šī tēma sniedz detalizētu informāciju un parauga vaicājumu algas pozīcijas darba elementam programmā Dynamics 365 Human Resources.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 62b9caf94f1c9aa8bb5758e62565fe57dfdd245a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055032"
---
# <a name="payroll-position-job"></a>Algas pozīcijas darbs

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šī tēma sniedz detalizētu informāciju un parauga vaicājumu algas pozīcijas darba attiecību elementam programmā Dynamics 365 Human Resources.

## <a name="properties"></a>Rekvizīti

| Rekvizīts<br>**Fiziskais nosaukums**<br>**_tips_** | Izmantot | Apraksts |
| --- | --- | --- |
| **Darba ID**<br>mshr_jobid<br>*Virkne* | Tikai lasāms<br>Obligāts |Darba ID. |
| **Derīgs no**<br>mshr_validto<br>*Datuma Laika Nobīde* | Tikai lasāms <br>Obligāts | Datums, no kurā ir spēkā posīcijas un darba attiecības. |
| **Derīgs līdz**<br>mshr_validto<br>*Datuma Laika Nobīde* | Tikai lasāms <br>Obligāts | Datums, līdz kuram ir spēkā posīcijas un darba attiecības.  |
| **Amata ID**<br>mshr_positionid<br>*Virkne* | Tikai lasāms<br>Obligāts | Pozīcijas ID. |
| **Primārais lauks**<br>mshr_primaryfield<br>*Virkne* | Obligāts<br>Sistēmas ģenerēts |  |
| **Pozīcijas darba ID vērtība**<br>_mshr_fk_positionjob_id_value<br>*GUID* | Tikai lasāms<br>Obligāts<br>Ārējā atslēga:mshr_PayrollPositionJobEntity no mshr_payrollpositionjobentity |Darba ID, kas saistīts ar amatu.|
| **Fiksētās atlīdzības plāna ID vērtība**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | Tikai lasāms<br>Obligāts<br>Ārējā atslēga: mshr_FixedCompPlan_id no mshr_payrollfixedcompensationplanentity  | Fiksētās atlīdzības plāna ID, kas saistīts ar amatu. |
| **Algas pozīcijas darba elementa ID**<br>mshr_payrollpositionjobentityid<br>*Guid* | Obligāts<br>Sistēmas ģenerēts. | Sistēmas ģenerēta GUID vērtība, lai unikāli identificētu darbu.  |

