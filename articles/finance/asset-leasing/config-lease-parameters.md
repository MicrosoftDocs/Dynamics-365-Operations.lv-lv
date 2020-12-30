---
title: Nomas parametru konfigurēšana (priekšskatījums)
description: Šajā tēmā ir aprakstīti konfigurācijas iestatījumi Līdzekļu nomai, piemēram, drošības informācija un uzskaites iestatījumi.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f71006570cd8f2bdc0385388eae0800cd29d3ec8
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4445791"
---
# <a name="configure-lease-parameters"></a>Nomas parametru konfigurēšana

[!include [banner](../includes/banner.md)]

Vairāki konfigurācijas iestatījumi ietekmē Līdzekļu nomas darbību. Šie iestatījumi ietver žurnālu nosaukumus, vispārīgos parametrus un grāmatošanas profila iestatījumus.

1. Dodieties uz **Līdzekļu noma \> Iestatījumi \> Līdzekļu nomas parametri**.
2. Cilnē **Nomas** atlasiet kopsavilkuma cilni **Vispārīgi**.

    Parametrs **Atļaut manuālās klasifikācijas pārlabošanu** nosaka, vai nomas klasifikāciju var pārlabot pirms maksājumu grafika apstiprināšanas.

    Parametrs **Partija no dažādiem elementiem** nosaka, vai varat grāmatot citās juridiskajās personās no esošās juridiskās personas. Ja šis parametrs ir ieslēgts, varat izveidot žurnāla ierakstus juridiskām personām, kurām jums ir piekļuve.

3. Iestatiet opciju **Atļaut dzēst apstiprinātās nomas** uz **Jā**, lai atļautu dzēst nomas, kam ir apstiprināti maksājumu grafiki. Nomu nevar dzēst, ja ar tām ir saistītas grāmatoti vai negrāmatoti darījumi, neatkarīgi no šīs opcijas iestatījuma. Nav iespējams atjaunot nomas ierakstu pēc tā dzēšanas. Ja augšupielādējiet jebkādus ierakstus par dzēstu nomu vai nu manuāli, vai izmantojot datu entītijas, augšupielādētā informācija tiek uzskatīta par jaunu, nevis esošas nomas atjauninājumu.

    Iestatot šo opciju kā **Jā** un grāmatas pārejas veidu kā **Kumulatīvās izlīdzināšanas opcija A vai B**, sistēma iestata lauku **Salīdzināmā aizņēmuma procentu likme** uz lauka **Salīdzināmā aizņēmuma procentu likme pārejas laikā** vērtību lapā **Grāmatas iestatījumi**. Ja šī opcija ir iestatīta uz **Nē**, neatkarīgi no grāmatas pārejas veida galvenās nomas likme ir iestatīta uz vērtību laukā **Salīdzināmā aizņēmuma procentu likme** lapā **Detalizēta informācija par grāmatu**.

4. Iestatiet opciju **Atļaut nolietojuma anulēšanu slēgtā grāmatas versijā** uz **Jā**, atļautu nolietojuma izdevumu darījumu anulēšanu. Izdevumu darījumus var anulēt pat tad, ja grāmatas versija ir slēgta.

    > [!NOTE]
    > Ieteicams saglabāt šo opciju iestatītu uz **Nē**. Šīs opcijas iestatījums tiek izmantots kā validācija un kontrole, lai novērstu, ka slēgtas grāmatas versijā nolietojums tiek piemērots nejauši. Saglabājot opciju iestatītu uz **Nē**, varat nodrošināt precīzu atlikušo vērtību un nākotnes nolietojuma aprēķinus.
