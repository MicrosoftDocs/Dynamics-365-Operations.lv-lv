---
title: Algu aprēķina integrācijas parametri
description: Šajā rakstā ir aprakstīti Dynamics 365 Human Resources algu integrācijas parametri.
author: marcelbf
ms.date: 06/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-17
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7d784909fc8c5fa05557566b62b19802cd2acece
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896107"
---
# <a name="payroll-integration-parameters"></a>Algu aprēķina integrācijas parametri


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Pirms algas Dynamics 365 Human Resources integrācijas izmantošanas ir jāiestata šajā rakstā aprakstītie parametri.

## <a name="enable-payroll-address"></a>Iespējot algas adresi

Lai varētu izmantot algas adresi, tā ir jāiespējo no [koplietojamu parametru formas](hr-setup-shared-parameters.md) cilnē Algu integrācija.

## <a name="define-the-identification-type"></a>Definējiet identifikācijas tipu

Lai [algas darbinieka entītijā](hr-admin-integration-payroll-api-payroll-employee.md) rādītu identifikācijas tipa ID, vajag [konfigurēt personāla vadības parametrus](hr-setup-shared-parameters.md) katram uzņēmumam.

1. Darbvietā **Kompensācijas pārvaldība**, saitēs atlasiet **Personāla vadības parametri**. 
2. Cilnē **Algu integrācija** norādiet vērtību šādiem laukiem.

| Lauks | Apraksts |
| --- | --- |
| Algas apstrādē izmantojiet identifikācijas veidus | Atlasot šo opciju, atlasītais tipa ID tiks pakļauts algas darbinieka elementam. |
| Identifikācijas veids | Identifikācijas tips, kas jāatsedz laukā **mshr_payrollemployeeentityid** sadaļā [algas darbinieka elements](hr-admin-integration-payroll-api-payroll-employee.md). |

## <a name="see-also"></a>Skatiet arī

[Payroll integrācijas API ieviešana](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
