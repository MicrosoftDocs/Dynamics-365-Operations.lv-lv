---
title: Laika logi
description: Laika logus varat izmantot, lai optimizētu pakalpojuma pasūtījumu rindu plānošanas.
author: ShylaThompson
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMATimeAgreement
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 29c43d5c21d435086bcc272e89b4c877f4057a44374e4d0005a842e10fe43a88
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741241"
---
# <a name="time-windows"></a>Laika logi  

[!include [banner](../includes/banner.md)]

Laika logus varat izmantot, lai optimizētu pakalpojuma pasūtījumu rindu plānošanas. Sistēmu var iestatīt tā, lai tajā automātiski tiktu izveidoti pakalpojumu pasūtījumi. Pamatojoties uz laika loga norādītajiem kritērijiem, vēlamo skaitu pakalpojumu pasūtījumu rindu varat savienot ar vēlamo skaitu pakalpojumu pasūtījumu.

Laika logi nosaka, cik tālu pakalpojuma pasūtījuma rinda var pārvietoties no sava aprēķinātā datuma. Aprēķinātais datums ir datums, kurā tika planota pakalpojuma pasūtījuma rindas parādīšanās. Šis datums ir atkarīgs no tā intervāla iestatījuma un pakalpojuma perioda, ko definējāt lapā **Pakalpojumu pasūtījumu izveide**. Jūs definējat laika logu, izmantojot vērtības šajā tabulā:

| Metode | apraksts                                                                                                                                                                                                                                                                                           |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nedēļa   | Datums, kad pakalpojuma pasūtījuma rindu var pārvietot uz jebkuru pieejamo dienu sākotnējā aprēķinātā datuma nedēļā.                                                                                                                                                                                    |
| Mēnesis  | Datums, kad pakalpojuma pasūtījuma rindu var pārvietot uz jebkuru pieejamo dienu sākotnējā aprēķinātā datuma mēnesī. Piemēram, pakalpojuma pasūtījuma rindas aprēķinātais datums ir 2017. gada 15. februāris. Pakalpojuma pasūtījuma rindu var ieplānot jebkurā nedēļas dienā no 2017. gada 1. februāra līdz 28. februārim. |
| Manuāli | Jūs nosakāt maksimālo dienu skaitu pirms vai pēc sākotnējā aprēķinātā datuma, uz kuru var pārvietot pakalpojuma pasūtījuma rindu.                                                                                                                                                                           |

Ja pakalpojumu līguma rindai nenorādāt laika logu, tad pakalpojuma pasūtījuma rinda, kas ir atvasināta no pakalpojumu līguma, ir jāizpilda tieši tajā datumā, kurā tā tika sākotnēji ieplānota.

## <a name="related-topics"></a>Saistītās tēmas

[Laika loga izveide](create-time-windows.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]