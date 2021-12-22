---
title: Pārvērst asinhronos debitorus par sinhroniem klientiem
description: Šajā tēmā ir paskaidrots, kā asinhronos klientus pārvērst par sinhroniem klientiem programmā Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: d8a386299f2c67c870fe0b8f779c9155405c1f1a
ms.sourcegitcommit: eef5d9935ccd1e20e69a1d5b773956aeba4a46bc
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/11/2021
ms.locfileid: "7913776"
---
# <a name="convert-asynchronous-customers-to-synchronous-customers"></a>Pārvērst asinhronos debitorus par sinhroniem klientiem

[!include [banner](includes/banner.md)]

Šajā tēmā ir paskaidrots, kā asinhronos klientus pārvērst par sinhroniem klientiem programmā Microsoft Dynamics 365 Commerce.

Lai asinhronos klientus pārvērstu par sinhroniem klientiem, rīkojieties šādi.

1. Programmā Commerce Headquarters palaidiet **P-darbu,** lai nosūtītu asinhronos klientus uz galveno mītni Commerce.
1. Palaidiet **sinhronizēt debitorus un biznesa partnerus no asinhronā režīma** darba, lai izveidotu debitoru kontu ID. (Šis darbs agrāk tika nosaukts **Sinhronizēt debitorus un biznesa partnerus no asinhronā režīma** .)
1. Palaidiet **darbu 1010,** lai sinhronizētu jaunos klientu kontu KONTUs ar kanāliem.

Ja pasūtījums atsaucas uz asinhronu klientu vai adresi, kas vēl nav sinhronizēta ar Commerce galveno mītni, klients vai adrese tiks sinhronizēta **pakešuzdevuma Sinhronizēt pasūtījumus** ietvaros. Ja skaidras naudas un pārvadāšanas transakcija atsaucas uz asinhronu debitoru vai adresi, klients vai adrese tiks sinhronizēta pirms dienas beigu (EOD) grāmatošanas.

## <a name="additional-resources"></a>Papildu resursi

[Klientu pārvaldība veikalos](customer-mgmt-stores.md)

[Asinhronais debitora izveides režīms](async-customer-mode.md)

[Debitora atribūti](dev-itpro/customer-attributes.md)

[Datu izslēgšana bezsaistē](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
