---
title: Skatīt kreditora rēķina automatizācijas rezultātus (priekšskatījums)
description: Šajā rakstā ir skaidrots, kā skatīt piegādātāja rēķinu statusu, kas ir automatizētā iesniegšanas darbplūsmas procesā.
author: abruer
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: dd9b74d2ed34399aff455563504c296a5a25a874
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895172"
---
# <a name="view-vendor-invoice-automation-results"></a>Kreditoru rēķinu automatizācijas rezultātu skatīšana

[!include [banner](../includes/banner.md)]

Šajā rakstā ir skaidrots, kā skatīt piegādātāja rēķinu statusu, kas ir automatizētā iesniegšanas darbplūsmas procesā. Detalizēta informācija par automatizācijas vēsturi tiek uzturēta katram importētajam kreditora rēķinam. Atkarībā no biznesa procesiem, ko esat automatizējuši, lapa **Gaidošie kreditoru rēķini** parāda vērtības **Automatizētās preču ieejas plūsmas atbilstības statuss** un **Automatizētās darbplūsmā iesniegšanas statuss**. Varat apskatīt detalizētu informāciju un izveidot plānu, lai koncentrētos uz rēķiniem, kam automatizēta darbība bijusi nesekmīga. Pēc tam, kad esat novērsis problēmu, varat atsākt importētā rēķina automatizēto procesu.

Pirms iesniegta rēķina rediģēšanas, ir jāpārtrauc automātiskā apstrāde. Ja automatizētajā darbplūsmā iesniegšanas procesā ir jāpārtrauc rēķins, iestatiet lauku **Iekļaut automatizētajā apstrādē** uz **Nē** lapā **Kreditoru rēķini**. Pēc tam automatizācija netiks palaista, kamēr lauks **Iekļaut automatizētajā apstrādē** netiks iestatīts uz **Jā**. Var pārtraukt rēķina turpmāku automatizāciju, ja rēķins vēl nav darbplūsmas sistēmā un netiek izmantots automatizētajā procesā.

Ja importētais rēķins ir pakļauts darbplūsmā iesniegšanas procesam, varat skatīt tā vērtību **Automatizācijas statuss** lapā **Kreditoru rēķini**. Tālāk minētie statusi tiek izsekoti:

- **Iekļauts** — automatizētie procesi, kas ir definēti lapā **Kreditoru parametri**, darbojas pareizi, bet vēl nav pabeigti.
- **Pārtraukts** — automatizētie procesi, kas ir definēti lapā **Kreditoru parametri**, ir palaisti, bet vismaz viena procesa darbība neizdevās. Arī statuss **Pārtraukts** tiek piemērots, ja lauks **Iekļaut automatizētajā apstrādē** ir iestatīts uz **Nē**. Varat apskatīt kļūmes, atlasot **Skatīt visjaunākos rezultātus**.
- **Darbplūsmā** — importētais rēķins ir iesniegts darbplūsmas sistēmā, vai nu automatizētā darbplūsmā iesniegšanas procesa rezultātā, vai manuāli.
- **Darbplūsma pabeigta** — darbplūsmas process importētajam rēķinam ir pabeigts.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
