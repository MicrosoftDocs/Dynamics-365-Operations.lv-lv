---
title: PVN kodu iestatīšana
description: Šajā tēmā paskaidrots, kā iestatīt pasūtījumu aizturēšanas kodus programmā Dynamics 365 Finance.
author: twheeloc
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6c7208fa65905fcc902d9c08b5b90178745e76d4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815048"
---
# <a name="set-up-sales-tax-codes"></a>PVN kodu iestatīšana

[!include [banner](../../includes/banner.md)]

Šajā tēmā paskaidrots, kā iestatīt pasūtījumu aizturēšanas kodus. PVN kodi tiek veidoti katram netiešajam nodoklim vai nodevai, kas juridiskajai personai obligāti jāaprēķina, jāapkopo un jāmaksā PVN iestādēm.

Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.

1. Pārejiet uz **Navigācijas rūts > Nodokļi > Netiešie nodokļi > PVN > PVN kodi**.
2. Atlasiet **Jauns**.
3. Ierakstiet vērtību laukā **PVN kods**.
4. Laukā **Nosaukums** ierakstiet kādu vērtību.
5. Atlasiet **Maksājumu periodu**, atverot nolaižamo sarakstu, lai norādītu, kurai PVN iestādei un kādos laika intervālos par šo PVN jāziņo un tas jānomaksā.
6. Lai norādītu galveno kontu PVN grāmatošanai Virsgrāmatā, atlasiet **Virsgrāmatas grāmatošanas grupu**.
7. Izvērsiet kopsavilkuma cilni **Aprēķins**. Tas ietver vairākus laukus, kas kontrolē, kā tiks aprēķinātas PVN summas. Aizpildiet šos laukus pēc vajadzības.  
8. **Darbību rūtī**, kas atrodas interfeisa augšdaļā, atlasiet **PVN kods**.
9. Atlasiet **Vērtības**.
10. Ievadiet šī nodokļa koda vērtību kolonnā **Vērtība**.
    - Kopsavilkuma cilnes **Aprēķins** laukā Izcelsme ir atlasīta Summa uz vienu vienību, PVN summas rēķināšanai vērtība tiks reizināta ar transakcijā norādīto daudzumu.  Ja nodokļa kods neatbilst uz vienībām balstītam nodoklim, PVN summas vērtība tiek aprēķināta kā procenti no šī nodokļu koda Izcelsmes.     
11. Atlasiet **Saglabāt**.
12. Aizvērt lapu.
13. Atlasiet **Saglabāt**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]