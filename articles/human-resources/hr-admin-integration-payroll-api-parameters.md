---
title: Algu aprēķina integrācijas parametri
description: Šajā tēmā aprakstīts Dynamics 365 Human Resources Payroll integrācijas parametri.
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
ms.openlocfilehash: 5f76ce395d7f5a82ab622dd323aee52a39b09847
ms.sourcegitcommit: 89bb2a7f402deed32998eddc1e56e75250e3d15e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314442"
---
# <a name="payroll-integration-parameters"></a>Algu aprēķina integrācijas parametri

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Pirms Dynamics 365 Human Resources Algas integrācijas izmantošanas ir jāiestata šajā tēmā aprakstītie parametri.

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