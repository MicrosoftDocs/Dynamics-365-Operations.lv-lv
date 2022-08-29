---
title: Asinhrono debitoru pārvēršana par sinhroniem debitoriem
description: Šajā rakstā skaidrots, kā asinhronu debitoru pārvēršana par sinhroniem debitoriem Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: b442bfc0685706359771e4d9e2729565d3652a60
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278197"
---
# <a name="convert-asynchronous-customers-to-synchronous-customers"></a>Asinhrono debitoru pārvēršana par sinhroniem debitoriem

[!include [banner](includes/banner.md)]

Šajā rakstā skaidrots, kā asinhronu debitoru pārvēršana par sinhroniem debitoriem Microsoft Dynamics 365 Commerce.

Lai asinhronus debitorus pārveidotu par sinhroniem debitoriem, veiciet šos soļus.

1. Programmā Commerce Headquarters izpildiet **P darbu, lai** asinhronos debitorus nosūtītu uz programmu Commerce Headquarters.
1. Palaidiet sinhronizēt **debitorus un biznesa partnerus no asinhronā** režīma darba, lai izveidotu debitoru kontu KODUs. (Šis darbs bija agrāk nosaukts **Sinhronizēt debitorus un biznesa partnerus no async režīma**.)
1. Izpildiet **1010** darbu, lai sinhronizētu jaunos debitora kontu sinhronizēšanu kanālos.

Ja pasūtījumam ir atsauce uz asinhronu debitoru vai adresi, kas vēl nav sinhronizēta ar programmu Commerce Headquarters, **debitors vai adrese tiks sinhronizēta kā daļa no pakešuzdevuma Sinhronizēt** pasūtījumus. Ja darbībai, kas ir jāveic, ir atsauce uz asinhronu debitoru vai adresi, pirms dienas beigu (EOD) grāmatošanas debitors vai adrese tiks sinhronizēti.

## <a name="additional-resources"></a>Papildu resursi

[Klientu pārvaldība veikalos](customer-mgmt-stores.md)

[Asinhronā debitora izveides režīms](async-customer-mode.md)

[Debitora atribūti](dev-itpro/customer-attributes.md)

[Datu izslēgšana bezsaistē](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
