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
ms.openlocfilehash: 0c489b99d5d05ddac46d222e701512288aeb10583a5e829212e0e1c924622f16
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712077"
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
