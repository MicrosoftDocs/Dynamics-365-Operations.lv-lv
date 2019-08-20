---
title: Līdzekļu izveide un iegūšana no kreditoriem
description: Šis uzdevuma ceļvedis apraksta pamatlīdzekļa izveidi un iegādi, izmantojot pirkšanas procesu.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 2626877c907994d03cdae960c8501a858ca214bd
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840029"
---
# <a name="create-and-acquire-assets-from-accounts-payable"></a>Līdzekļu izveide un iegūšana no kreditoriem

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šis uzdevuma ceļvedis apraksta pamatlīdzekļa izveidi un iegādi, izmantojot pirkšanas procesu.  Tas izmanto grāmatveža un kreditoriem maksājamo rēķinu darbinieka lomas, kā arī demonstrācijas uzņēmumu USMF.


## <a name="set-fixed-assets-parameters"></a>Pamatlīdzekļu parametru iestatīšana
1. Pārejiet uz sadaļu Pamatlīdzekļi > Iestatījumi > Pamatlīdzekļu parametri.
2. Izvērsiet vai sakļaujiet sadaļu Pirkšanas pasūtījumi.
3. Atzīmējiet izvēles rūtiņu Atļaut līdzekļu iegādi no Pirkšanas.
4. Atzīmējiet izvēles rūtiņu Izveidot līdzekli produktu ieejas plūsmas vai rēķina grāmatošanas laikā.

## <a name="create-a-new-vendor-invoice"></a>Jauna kreditora rēķina izveide
1. Pārejiet uz sadaļu Kreditori > Darbvietas > Kreditora rēķina ieraksts.
2. Noklikšķiniet uz Jauns kreditora rēķins.
3. Laukā Rēķina konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
4. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
5. Laukā Numurs ierakstiet kādu vērtību.
6. Ievadiet datumu laukā Grāmatošanas datums.
7. Noklikšķiniet uz Pievienot rindu.
8. Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
    * Pamatlīdzekļu iegādei var tikt izmantoti vai nu noliktavā neesoši krājumi vai sagādes kategorijas.  
9. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
10. Laukā Daudzums ievadiet skaitli.
    * Viena rēķina rinda izveidos tikai vienu pamatlīdzekli neatkarīgi no daudzuma.  Rēķina daudzuma lauka vērtība tiks pārnesta uz pamatlīdzekļa daudzumu.  
11. Laukā Vienības cena ievadiet kādu skaitli.
12. Izvērsiet vai sakļaujiet sadaļu Detalizēta rindas informācija.
13. Noklikšķiniet uz cilnes Pamatlīdzekļi.
14. Atzīmējiet izvēles rūtiņu Izveidot jaunu pamatlīdzekli..
15. Laukā Pamatlīdzekļa grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
16. Sarakstā atlasiet pamatlīdzekļu grupu, kura tiks izmantota jauna pamatlīdzekļa izveidei.
17. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
18. Noklikšķiniet uz Grāmatot.
    * Pamatlīdzeklis tiks izveidots un iegūts, iegrāmatojot rēķinu.  

