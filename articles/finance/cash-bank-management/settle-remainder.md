---
title: Atlikuma nokārtošana
description: Jūs varat apmaksāt atlikušo no norēķinu darbības, ieskaitot šo summu virsgrāmatas kontā.
author: mikefalkner
manager: aolson
ms.date: 10/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 52b0b456a6d9879c480ac3f076a32e382426a89c
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3977795"
---
# <a name="settle-remainder"></a>Atlikuma nokārtošana

[!include [banner](../includes/banner.md)]

Jūs varat apmaksāt atlikušo no norēķinu darbības, ieskaitot šo summu virsgrāmatas kontā vai citam debitoram. Jūs varat nokārtot atlikumu, kad sedzat žurnālā ievadītās summas, vai kad tikai sedzat atvērtās transakcijas.

## <a name="setting-up-defaults"></a>Noklusējumu iestatīšana 
Pirms atlikuma nokārtošanas izmantošanas, ir jāiespējo atlikuma nokārtošanas līdzeklis un jāiestata noklusējuma iestatījumi.

1)  Noklikšķiniet uz **Debitoru parādi > Parametri > Norēķini** vai **Kreditoru parādi > Parametri > Norēķini**.
2)  Atlasiet cilni **Norēķini** un noklikšķiniet uz **Iespējot atlikuma nokārtošanu**.
3)  Laukā **Noklusējuma iemesla kods** atlasiet noklusējuma iemesla kodu. Iemeslu kodiem jau ir jābūt iestatītiem sadaļā **Debitoru parādi > Iestatījumi > Debitoru norakstīšanas iemesla kodi** vai **Kreditoru parādi > Iestatījumi > Debitoru norakstīšanas iemesla kodi**. **Noklusējuma atlikuma nokārtošanas konts** pēc noklusējuma būs konts, kas piešķirts norakstīšanas iemesla kodam.
3)  Atjauniniet parametra **Noklusējuma atlikuma nokārtošanas konts** informāciju pēc nepieciešamības.
4)  Laukā **Noklusējuma žurnāla nosaukums**, atlasiet maksājumu žurnālu, kas tiks izmantots, ja vēlaties izveidot maksājumu žurnālu, kad kārtojat tikai atvērtās transakcijas. Ja iespējojat atlikuma nokārtošanas līdzekli, ir jāpievieno noklusējuma žurnāla nosaukums.

## <a name="settle-remainder-from-a-journal"></a>Atlikuma nokārtošana no žurnāla
Ja neiespējojat līdzekli **Atlikuma nokārtošana**, jūs joprojām varat ievadīt transakciju žurnālā un pēc tam nokārtot transakcijas atbilstoši žurnālam, kā to darījāt iepriekš. Noklikšķinot uz pogas **OK**, atvērtā rēķina bilance tiek samazināta atbilstoši iemaksātajai summai. Ja iemaksātā summa pilnībā nenosedz rēķinu, rēķins paliek atvērts, un atlikumu var samaksāt vēlāk.

Kad līdzeklis līdzekli **Atlikuma nokārtošana** ir iespējots, varat segt atlikušo summu virsgrāmatas kontā. Tā vietā, lai atstātu atvērtus rēķinus, varat arī pārsūtīt atlikumu uz cita debitora kontu (debitoru transakcijām) vai cita kreditora kontu (kreditoru transakcijas). 

Lai nokārtotu atlikumu lapā **Norēķini**, veiciet šādas darbības:

1)  Lapā **Norēķini** atzīmējiet rēķinus vai transakcijas, kuras vēlaties nosegt.
2)  Noklikšķiniet uz pogas **Nokārtot atlikumu**.
3)  Parādīsies dialoglodziņš, kurā būs norādīta summa, kas tiks segta virsgrāmatas kontā, datums, kas tiks izmantots, lai nokārtotu atlikumu, noklusējuma iemesla kods no parametriem un noklusējuma konts no parametriem. 
4)  Atlasiet jaunu norēķinu iemeslu, ja vēlaties mainīt noklusējuma iemeslu. Norēķinu konts tiks mainīts uz kontu, kas saistīts ar iemesla kodu.
5)  Labojiet norēķinu kontu, ja vēlaties to mainīt.
6)  Ja sedzat debitora transakcijas un vēlaties pārvietot atlikumu uz cita debitora kontu, pēc tam atlasiet debitoru laukā **Nokārtot atlikumu debitora kontā**. Ja sedzat kreditora transakcijas un vēlaties pārvietot atlikumu uz cita kreditora kontu, pēc tam atlasiet kreditoru laukā **Nokārtot atlikumu kreditora kontā**.
6)  Noklikšķiniet uz **Nokārtot atlikumu**.
7)  Tiks parādīta lapa **Žurnāls**. Žurnālam tiks pievienotas papildu žurnāla rindas ar atlikuma norēķinu summu kā summu un ar atlikuma norēķinu kontu kā korespondējošo kontu. Ja pievienojāt debitoru vai kreditoru, lai varētu pārvietot norēķinu summu uz citu debitora vai kreditora kontu, žurnālam tiks pievienota papildu rinda, lai pārvietotu norēķinu summu uz attiecīgo debitora vai kreditora kontu.

Grāmatojot žurnālu, atvērtā transakcija būs pilnībā nosegta. 

## <a name="settle-remainder-when-you-are-only-settling-open-transactions"></a>Atlikuma nokārtošana, sedzot tikai atvērtās transakcijas
Jūs varat nokārtot atlikumu, arī sedzot atvērtās transakcijas bez žurnāla.

Lai nokārtotu atlikumu, veiciet tālāk norādītās darbības.

1)  Lapā **Norēķini** atzīmējiet rēķinus vai transakcijas, kuras vēlaties nosegt.
2)  Noklikšķiniet uz **Nokārtot atlikumu**.
3)  Parādīsies dialoglodziņš, kurā būs norādīta summa, kas tiks segta virsgrāmatas kontā, datums, kas tiks izmantots, lai nokārtotu atlikumu, noklusējuma iemesla kods no parametriem un noklusējuma konts no parametriem. 
4)  Atlasiet jaunu norēķinu iemeslu, ja vēlaties mainīt noklusējuma iemeslu. Norēķinu konts tiks mainīts uz kontu, kas saistīts ar iemesla kodu.
5)  Labojiet **norēķinu kontu**, ja vēlaties to mainīt.
6)  Ja sedzat debitora transakcijas un vēlaties pārvietot atlikumu uz cita debitora kontu, pēc tam atlasiet debitoru laukā **Nokārtot atlikumu debitora kontā**. Ja sedzat kreditora transakcijas un vēlaties pārvietot atlikumu uz cita kreditora kontu, pēc tam atlasiet kreditoru laukā **Nokārtot atlikumu kreditora kontā**.
7)  Jūs varat arī izvēlēties, vai līdz ar atlikuma nokārtošanu izveidot maksājumu žurnālu, vai tikai grāmatot bez žurnāla. Lai izveidotu maksājumu žurnālu, opcijai **Labot žurnālā** atlasiet **Jā**. Varēsiet labot maksājumu žurnālu, ko veidojat.
8)  Noklikšķiniet uz **Nokārtot atlikumu**. Ja izvēlējāties izveidot žurnālu, poga mainīsies uz **Izveidot žurnālu**. Noklikšķiniet uz **Izveidot žurnālu**.
9)  Ja esat izveidojis maksājumu žurnālu, žurnāla lapa atvērsies pēc noklikšķināšanas uz **Nokārtot atlikumu**. Žurnālam tiks pievienota papildu žurnāla rinda ar atlikuma norēķinu summu kā summu un ar atlikuma norēķinu kontu kā korespondējošo kontu. Ja pievienojāt debitoru vai kreditoru, lai varētu pārvietot norēķinu summu uz citu debitora vai kreditora kontu, žurnālam tiks pievienota papildu rinda, lai pārvietotu norēķinu summu uz attiecīgo debitora vai kreditora kontu.
