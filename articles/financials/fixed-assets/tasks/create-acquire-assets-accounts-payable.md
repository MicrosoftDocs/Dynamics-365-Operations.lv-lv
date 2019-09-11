---
title: Līdzekļu izveide un iegūšana no kreditoriem
description: Šis uzdevuma ceļvedis apraksta pamatlīdzekļa izveidi un iegādi, izmantojot pirkšanas procesu.
author: saraschi2
manager: AnnBe
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, VendInvoiceWorkspace, VendEditInvoice, VendTableLookup, InventItemIdLookupSimple, AssetTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 025639e6e5bdc6b95e9c496f11f29ed8ec8d388c
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914680"
---
# <a name="create-and-acquire-assets-from-accounts-payable"></a>Līdzekļu izveide un iegūšana no kreditoriem

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šis uzdevuma ceļvedis apraksta pamatlīdzekļa izveidi un iegādi, izmantojot pirkšanas procesu.  Tas izmanto grāmatveža un kreditoriem maksājamo rēķinu darbinieka lomas, kā arī demonstrācijas uzņēmumu USMF.


## <a name="set-fixed-assets-parameters"></a>Pamatlīdzekļu parametru iestatīšana
1. **Navigācijas rūtī** ejiet uz **Moduļi > Pamatlīdzekļi > Iestatīšana> Pamatlīdzekļu parametri**.
2. Izvērsiet kopsavilkuma cilni **Pirkuma pasūtījumi**.
3. Atzīmējiet izvēles rūtiņu **Atļaut līdzekļu iegādi no pirkšanas**.
4. Atzīmējiet izvēles rūtiņu **Izveidot līdzekli produkta saņemšanas vai rēķina publicēšanas laikā**.

## <a name="create-a-new-vendor-invoice"></a>Jauna kreditora rēķina izveide
1. **Navigācijas rūtī** pārejiet uz sadaļu **Moduļi > Kreditori > Darbvietas > Piegādātāju rēķina ieraksts**.
2. Klikšķiniet uz **Jauns piegādātāja rēķins**.
3. Laukā **Rēķina konts** noklikšķiniet uz nolaižamās pogas uzmeklēšanas atvēršanai.
4. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
5. Laukā **Numurs** ierakstiet vērtību.
6. Laukā **Publicēšanas datums** ievadiet datumu.
7. Nokl. **Piev. r.**
8. Laukā **Krājuma kods** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu. Pamatlīdzekļu iegādei var tikt izmantoti vai nu noliktavā neesoši krājumi vai sagādes kategorijas.  
9. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
10. Laukā **Daudzums** ierakstiet kādu skaitli. Viena rēķina rinda izveidos tikai vienu pamatlīdzekli neatkarīgi no daudzuma. Rēķina daudzuma lauka vērtība tiks pārnesta uz pamatlīdzekļa daudzumu.  
11. Laukā **Vienības cena** ievadiet kādu skaitli.
12. Izvērsiet kopsavilkuma cilni **Detalizēta informācija par rindu**.
13. Noklikšķiniet uz cilnes **Pamatlīdzekļi**.
14. Atzīmējiet izvēles rūtiņu **Izveidot jaunu pamatlīdzekli**.
15. Laukā **Pamatlīdzekļu grupa** noklikšķiniet uz nolaižamās pogas uzmeklēšanas atvēršanai.
16. Sarakstā atlasiet pamatlīdzekļu grupu, kura tiks izmantota jauna pamatlīdzekļa izveidei.
17. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
18. Noklikšķiniet uz **Grāmatot**. Pamatlīdzeklis tiks izveidots un iegūts, iegrāmatojot rēķinu.  

