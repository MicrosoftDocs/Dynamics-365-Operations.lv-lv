---
title: Iestatījums "Grāmatot, lai iekasētu no konta virsgrāmatā" netiek ieslēgts
description: Šī problēma parādās, kad pirkuma pasūtījumam tiek izrakstīts rēķins, ja lapas "Parādi kreditoriem" cilnē "Rēķins" tiek iespējota opcija "Grāmatot, lai iekasētu no konta grāmatā"
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 592444958dad4624fdc9098dc58df0a2e49e63de
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477004"
---
# <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a>Iestatījums "Grāmatot, lai iekasētu no konta virsgrāmatā" netiek ieslēgts

## <a name="symptoms"></a>Simptomi

Šī problēma rodas, izrakstot rēķinu pirkšanas pasūtījumam, ja opcija **Grāmatot Virsgrāmatas izmaksu kontā** ir iestatīta uz *Jā* cilnē **Rēķins**, kas atrodas lapā **Kreditoru parametri**.

## <a name="reproduce-the-issue"></a>Problēmas atveide

Nākamajā procedūrā ir parādīts viens šīs problēmas atveides veids.

1. Dodieties uz **Parādi kreditoriem \> Iestatīšana \> Kreditoru moduļa parametri**.
1. Cilnē **Rēķins** iestatiet opciju **Grāmatot Virsgrāmatas izmaksu kontā** uz *Jā*.
1. Doties uz **Krājumu vadība \> Iestatīšana \> Grāmatojums \> Grāmatošana**.
1. Cilnē **Pirkšanas pasūtījums** pārliecinieties, vai visas preces pirkšanas izdevumu rindas ir izdzēstas.
1. Dodieties uz **Kreditori \> Pirkšanas pasūtījumi \> Visi pirkšanas pasūtījumi**.
1. Izveidojiet pirkšanas pasūtījumu. Laukā **Kreditora konts** atlasiet *1001 Acme Office Supplies*.
1. Pievienojiet pirkšanas pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Krājuma kods:** *D0011 Laser Projector*
    - **Vieta:** *1*
    - **Noliktava:** *11*
    - **Daudzums:** *4*

1. Darbību rūts cilnē **Pirkšana**, grupā **Darbība** atlasiet **Apstiprināt**.
1. Darbību rūtī cilnes **Saņemt** grupā **Ģenerēt**, atlasiet **Produktu ieejas plūsma**.
1. Dialoglodziņā **Produktu ieejas plūsmas grāmatošana** laukā **Produktu ieejas plūsma**, ievadiet patvaļīgu numuru un pēc tam atlasiet **Labi**.
1. Darbību rūtī, cilnē **Rēķins**, grupā **Ģenerēt** atlasiet **Rēķins**.
1. Laukā **Numurs** ievadiet patvaļīgu numuru kā rēķina numuru.
1. Atjauniniet atbilstības statusu un grāmatojiet.
1. Ievērojiet, ka tagad, ģenerējot rēķinu no pirkšanas pasūtījuma, tiek parādīta šāda kļūda: “Konta numurs darbības veidam Preces pirkšanas izdevumi nepastāv.”

## <a name="resolution"></a>Novēršana

Tas ir atkarīgs no rēķinu un rēķinu grupu parametru iestatījumiem. Lai iegūtu papildinformāciju, skatiet šo emuāra ierakstu: [Pirkšanas izmaksu un krājumu izmaiņu uzskaite](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).
