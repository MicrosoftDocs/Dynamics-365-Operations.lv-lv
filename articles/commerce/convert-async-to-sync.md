---
title: Asinhrono debitoru pārvēršana par sinhroniem debitoriem
description: Šajā tēmā skaidrots, kā asinhronos debitorus pārveidot par sinhroniem debitoriem Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: fc1690ff6068317c748bda0d767a10f306f3debe
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691448"
---
# <a name="convert-asynchronous-customers-to-synchronous-customers"></a>Asinhrono debitoru pārvēršana par sinhroniem debitoriem

[!include [banner](includes/banner.md)]

Šajā tēmā skaidrots, kā asinhronos debitorus pārveidot par sinhroniem debitoriem Microsoft Dynamics 365 Commerce.

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
