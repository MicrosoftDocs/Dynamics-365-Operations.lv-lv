---
title: Līdzekļa nomas maksājumu grafiku apstiprināšana partijā
description: Šajā rakstā ir izskaidrots, kā apstiprināt vairākus maksājumu grafikus paketē.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePaymConfirmationDetails
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: bd75e22f6407d6bc25a78c1dfeacf70022238e94
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895056"
---
# <a name="confirm-asset-leasing-payment-schedules-in-a-batch"></a>Līdzekļa nomas maksājumu grafiku apstiprināšana partijā

[!include [banner](../includes/banner.md)]

Šajā rakstā ir izskaidrots, kā apstiprināt vairākus maksājumu grafikus paketē. Maksājumu grafiki tiek apstiprināti vai katrai nomai, vai izmantojot partijas apstiprināšanas procesu. Žurnāla ierakstu var grāmatot tikai nomai ar apstiprinātu maksājumu grafiku. Maksājumu grafika apstiprināšana kalpo kā nomas finanšu informācijas galīgais apstiprinājums. Visas turpmākās izmaiņas nomas finanšu informācijā, piemēram, maksājumos un nomas termiņā, veido nomas korekciju, un ir jāapstrādā tādā veidā.

Lai apstiprinātu vairākus maksājumu grafikus, veiciet tālāk norādītās darbības.

1. Doties uz **Līdzekļa noma \> Periodiskums \> Apstiprināšana partijā**.
2. Lapā **Apstiprināšana partijā** atlasiet **Apstiprināšana partijā**.
3. Parādītajā dialoglodziņā filtrējiet grāmatas, ko vēlaties apstiprināt.

    - Lai apstiprinātu visas konkrētās nomas grupas grāmatas, atlasiet grupu laukā **Nomas grupa**.
    - Lai apstiprinātu noteiktas grāmatas, atlasiet grāmatas laukā **Grāmatas ID**.
    - Lai apstiprinātu visas grāmatas, ieslēdziet parametru **Visām grāmatām**.

Informācija par nesen apstiprinātajām grāmatām tiek parādīta lapā **Apstiprinātās grāmatas**. Kad maksājumu grafiki ir apstiprināti, nomai var grāmatot sākotnējos atzīšanas žurnāla ierakstus.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
