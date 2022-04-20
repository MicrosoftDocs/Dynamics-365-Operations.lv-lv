---
title: Iestatīt PVN kodus
description: Šajā tēmā skaidrots, kā iestatīt PVN kodus Dynamics 365 Finanses.
author: twheeloc
ms.date: 09/27/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 69e2cf9a16fe0e694154cccf9b49944b49c79b90
ms.sourcegitcommit: 23588e66e25c05e989f3212ac519d7016820430a
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2022
ms.locfileid: "8565858"
---
# <a name="set-up-sales-tax-codes"></a>Iestatīt PVN kodus

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

    Ja kopsavilkuma cilnes **Aprēķins** laukā **Izcelsme** ir atlasīta **Summa par vienu vienību**, PVN summas rēķināšanai vērtība tiks reizināta ar transakcijā norādīto daudzumu.  Ja nodokļa kods neatbilst uz vienībām balstītam nodoklim, PVN summas vērtība tiek aprēķināta kā procenti no šī nodokļu koda Izcelsmes.     

11. Atlasiet **Saglabāt**.
12. Aizvērt lapu.
13. Atlasiet **Saglabāt**.

Microsoft Dynamics No 365 Finanšu versijas 10.0.22, [ja](../../localizations/global-tax-calcuation-service-overview.md) izmantojat nodokļu pakalpojumu, [**·**](../../localizations/emea-multiple-vat-registration-numbers.md)**un** līdzekļu pārvaldības darbvietā ir iespējota vairāku PVN reģistrācijas numuru atbalsta funkcija, **nodokļu** koda tipa norādīšanai var izmantot nodokļu lauka tipu. Ir pieejamas šādas vērtības:

- Standarta PVN
- Samazināts PVN
- PVN 0%
- Akcīze
- Cits

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
