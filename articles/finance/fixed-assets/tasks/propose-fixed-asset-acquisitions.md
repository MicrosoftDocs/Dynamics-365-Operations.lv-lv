---
title: Pamatlīdzekļa iegādes priekšlikums
description: Šajā tēmā ir aprakstīts, kā iegūt pamatlīdzekli, izmantojot iegādes priekšlikumu Pamatlīdzekļu žurnālā.
author: saraschi2
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d529cd53b41827a78b282afd4d2c69d2f2db555e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817173"
---
# <a name="propose-fixed-asset-acquisitions"></a>Pamatlīdzekļa iegādes priekšlikums

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā iegūt pamatlīdzekli, izmantojot iegādes priekšlikumu Pamatlīdzekļu žurnālā. Tas izmanto grāmatveža lomu un demonstrācijas datus USMF juridiskajai personai. Lai iegūtu pamatlīdzekli, izmantojot pamatlīdzekļu priekšlikumu žurnālu, vispirms ir jāizveido pamatlīdzekļa ieraksts un pēc tam jādefinē iegādes cena pamatlīdzekļu grāmatā.

## <a name="create-an-asset-acquisition-proposal"></a>Līdzekļa iegādes priekšlikuma izveide

Lai izveidotu līdzekļa iegādes priekšlikumu, veiciet tālāk norādītās darbības. 

1. Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Pamatlīdzekļi > Žurnāla ieraksti > Pamatlīdzekļu žurnāls**.
2. Atlasiet **Jauns**.
3. Ievadiet vai atlasiet vērtību laukā **Nosaukums**.
4. Darbību rūtī atlasiet **Rindiņas**.
5. Atlasiet **Priekšlikumi**.
6. Atlasiet **Iegādes priekšlikums**.
7. Atlasiet **Filtrēt**. Atlasiet **Atiestatīt**, lai notīrītu iepriekšējās vērtības.
8. Atlasiet rindu **Pamatlīdzekļa numurs**.
9. Ievadiet vai atlasiet vērtību laukā **Kritēriji**. Iestatiet atlikušos kritērijus pamatlīdzekļiem, kurus vēlaties iegūt, izmantojot šo priekšlikumu.  
10. Atlasiet **Labi** divas reizes, lai izietu no rūts.
- Pārbaudiet vai ir izveidotās transakcijas rindas.  
- Tikai pamatlīdzekļi ar iegādes datumu un iegādes cenu, kas ir iestatīta grāmatā, tiks iekļauti iegādes priekšlikumā.  
11. Lapā atlasiet cilni **Grāmatas**.
12. Atlasiet **Grāmatot**.

## <a name="include-default-financial-dimensions-in-an-acquisition-proposal"></a>Pirkšanas priekšlikumā iekļaut noklusējuma finanšu dimensijas

Iegādes darījumu var izveidot, izmantojot Excel pievienojumprogrammas, noklikšķinot uz **Pamatlīdzekļi > Žurnāla ieraksti > Pamatlīdzekļu žurnāls**. Izveidojiet jaunu žurnālu un pārvietojieties uz lapas sadaļu **Rindas** un atlasiet Excel ikonu un pēc tam atlasiet pamatlīdzekļu žurnāla rindu. Sistēma izveidos un atvērs Excel veidni, kas atspoguļo žurnāla rindas. Varat pievienot datus žurnāla rindām, ko pievienojat veidnei, un pēc tam publicēt šo informāciju atpakaļ sistēmā. 

Ja atlasītajai līdzekļu grāmatai un atbilstošajiem pamatlīdzekļiem, kas tika ievadīti Excel veidnē, noklusējuma dimensijas tiks izsauktas no līdzekļu grāmatas pamatdatiem, kad žurnāls ir publicēts sistēmā Excel. Lai līdzekļu grāmatā automātiski iekļautu finanšu dimensijas, publicējot pamatlīdzekļu žurnālu no Excel pievienojumprogrammas, iepriekš jāiestata noklusējuma dimensijas.  


[!INCLUDE [footer-include](../../../includes/footer-banner.md)]
