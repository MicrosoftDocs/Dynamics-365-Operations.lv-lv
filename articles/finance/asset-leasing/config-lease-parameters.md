---
title: Nomas parametru konfigurēšana (priekšskatījums)
description: Šajā tēmā ir aprakstīti konfigurācijas iestatījumi Līdzekļu nomai, piemēram, drošības informācija un uzskaites iestatījumi.
author: moaamer
ms.date: 01/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: twheeloc
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2a644b3c9d9ed4fc86a816af1ab338b96b1aa7ad
ms.sourcegitcommit: 7adf9ad53b4e6d1c4d5d612ce0977b76c61ec173
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968081"
---
# <a name="configure-lease-parameters"></a>Nomas parametru konfigurēšana

[!include [banner](../includes/banner.md)]

Vairāki konfigurācijas iestatījumi ietekmē Līdzekļu nomas darbību. Šie iestatījumi ietver žurnālu nosaukumus, vispārīgos parametrus un grāmatošanas profila iestatījumus.

1. Dodieties uz **Līdzekļu noma \> Iestatījumi \> Līdzekļu nomas parametri**.
2. Cilnē **Nomas** atlasiet kopsavilkuma cilni **Vispārīgi**.

    Parametrs **Atļaut manuālās klasifikācijas pārlabošanu** nosaka, vai nomas klasifikāciju var pārlabot pirms maksājumu grafika apstiprināšanas.

    Starpuzņēmumu **partijas** parametrs nosaka, vai varat grāmatot citām juridiskām personām no pašreizējās juridiskās personas. Ja šis parametrs ir ieslēgts, varat izveidot žurnāla ierakstus juridiskām personām, kurām jums ir piekļuve.

3. Iestatiet opciju Atļaut dzēst apstiprināto nomas maksu uz Jā, lai atļautu dzēst nomas **maksājumu** **grafikus**, kas ir apstiprinājuši maksājumu grafikus. Nomu nevar dzēst, ja ar tām ir saistītas grāmatoti vai negrāmatoti darījumi, neatkarīgi no šīs opcijas iestatījuma. Nav iespējams atjaunot nomas ierakstu pēc tā dzēšanas. Ja augšupielādējiet jebkādus ierakstus par dzēstu nomu vai nu manuāli, vai izmantojot datu entītijas, augšupielādētā informācija tiek uzskatīta par jaunu, nevis esošas nomas atjauninājumu.

    Iestatot šo opciju kā **Jā** un grāmatas pārejas veidu kā **Kumulatīvās izlīdzināšanas opcija A vai B**, sistēma iestata lauku **Salīdzināmā aizņēmuma procentu likme** uz lauka **Salīdzināmā aizņēmuma procentu likme pārejas laikā** vērtību lapā **Grāmatas iestatījumi**. Ja šī opcija ir iestatīta uz **Nē**, neatkarīgi no grāmatas pārejas veida galvenās nomas likme ir iestatīta uz vērtību laukā **Salīdzināmā aizņēmuma procentu likme** lapā **Detalizēta informācija par grāmatu**.

4. Lai atļautu nolietojuma izdevumu darbību atgriešanu, iestatiet opciju Atļaut nolietojuma **atgriešanu** **slēgtajā** grāmatā kā Jā. Izdevumu darījumus var anulēt pat tad, ja grāmatas versija ir slēgta.

    > [!NOTE]
    > Ieteicams saglabāt šo opciju iestatītu uz **Nē**. Šīs opcijas iestatījums tiek izmantots kā validācija un kontrole, lai novērstu, ka slēgtas grāmatas versijā nolietojums tiek piemērots nejauši. Saglabājot opciju iestatītu uz **Nē**, varat nodrošināt precīzu atlikušo vērtību un nākotnes nolietojuma aprēķinus.

5. Lai atļautu maksājumu summu sadalījumu lapas Maksājumu grafika rindu kopsavilkuma cilnē, iestatiet opciju Atļaut maksājuma summas sadalījumu **kā** **·** **·** **Jā**. Maksājuma sadalījuma tipi ir noteikti zem **Iestatījuma** lapā **Maksājumu summu** tipi. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
