---
title: Skatīt kreditora rēķina automatizācijas rezultātus (priekšskatījums)
description: Šajā tēmā skaidrots, kā skatīt to kreditoru rēķinu statusu, kas ir iekļauti automatizētajā darbplūsmā iesniegšanas procesā.
author: abruer
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 872ec404da0cce41c4ea0f882a3fa8af56316ce3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837229"
---
# <a name="view-vendor-invoice-automation-results"></a>Kreditoru rēķinu automatizācijas rezultātu skatīšana

[!include [banner](../includes/banner.md)]

Šajā tēmā skaidrots, kā skatīt to kreditoru rēķinu statusu, kas ir iekļauti automatizētajā darbplūsmā iesniegšanas procesā. Detalizēta informācija par automatizācijas vēsturi tiek uzturēta katram importētajam kreditora rēķinam. Atkarībā no biznesa procesiem, ko esat automatizējuši, lapa **Gaidošie kreditoru rēķini** parāda vērtības **Automatizētās preču ieejas plūsmas atbilstības statuss** un **Automatizētās darbplūsmā iesniegšanas statuss**. Varat apskatīt detalizētu informāciju un izveidot plānu, lai koncentrētos uz rēķiniem, kam automatizēta darbība bijusi nesekmīga. Pēc tam, kad esat novērsis problēmu, varat atsākt importētā rēķina automatizēto procesu.

Pirms iesniegta rēķina rediģēšanas, ir jāpārtrauc automātiskā apstrāde. Ja automatizētajā darbplūsmā iesniegšanas procesā ir jāpārtrauc rēķins, iestatiet lauku **Iekļaut automatizētajā apstrādē** uz **Nē** lapā **Kreditoru rēķini**. Pēc tam automatizācija netiks palaista, kamēr lauks **Iekļaut automatizētajā apstrādē** netiks iestatīts uz **Jā**. Var pārtraukt rēķina turpmāku automatizāciju, ja rēķins vēl nav darbplūsmas sistēmā un netiek izmantots automatizētajā procesā.

Ja importētais rēķins ir pakļauts darbplūsmā iesniegšanas procesam, varat skatīt tā vērtību **Automatizācijas statuss** lapā **Kreditoru rēķini**. Tālāk minētie statusi tiek izsekoti:

- **Iekļauts** — automatizētie procesi, kas ir definēti lapā **Kreditoru parametri**, darbojas pareizi, bet vēl nav pabeigti.
- **Pārtraukts** — automatizētie procesi, kas ir definēti lapā **Kreditoru parametri**, ir palaisti, bet vismaz viena procesa darbība neizdevās. Arī statuss **Pārtraukts** tiek piemērots, ja lauks **Iekļaut automatizētajā apstrādē** ir iestatīts uz **Nē**. Varat apskatīt kļūmes, atlasot **Skatīt visjaunākos rezultātus**.
- **Darbplūsmā** — importētais rēķins ir iesniegts darbplūsmas sistēmā, vai nu automatizētā darbplūsmā iesniegšanas procesa rezultātā, vai manuāli.
- **Darbplūsma pabeigta** — darbplūsmas process importētajam rēķinam ir pabeigts.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]