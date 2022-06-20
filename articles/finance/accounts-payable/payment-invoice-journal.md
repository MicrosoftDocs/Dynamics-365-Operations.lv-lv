---
title: Maksājumu grafika lietošana rēķinu žurnālā
description: Šajā rakstā ir aprakstīts, kā pievienot maksājumu kreditoru rēķinu žurnālam.
author: sunfzam
ms.date: 01/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: f3ae08ea46be66dd8bf26f7f91bd73f6c5b9192f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863135"
---
# <a name="apply-a-payment-schedule-to-the-invoice-journal"></a>Maksājumu grafika lietošana rēķinu žurnālā

[!include [banner](../includes/preview-banner.md)]

Microsoft Dynamics 365. finanšu laidienā 10.0.25 tagad tiek atbalstīts maksājumu **grafiks Kreditoru rēķinu žurnālā**.

Lai lietotu šo funkcionalitāti, līdzekļa Līdzekļa **pārvaldība iespējo iespēju** Lietot maksājumu grafiku rēķinu žurnālam.

Kad funkcija ir aktivizēta, rēķinu žurnāla **lapai** tiek pievienots jauns **maksājumu grafika** lauks. Veidojot rēķinu žurnāla rindu, ja apmaksas nosacījumi tiek uzturēti kreditoram un maksājuma nosacījumi ir atlasīti maksājumu grafikā, **·** **maksājumu grafika lauks tiek atjaunināts rēķinu žurnāla** lapā.

Varat mainīt maksājumu grafiku, kas tiek lietots atbilstīgi biznesa prasībām. Kreditora rēķinu žurnāla grāmatošanas laikā kreditora atvērtās darbības tiks izveidotas saskaņā ar maksājumu grafiku.

 - Lai pārskatītu vairākas kreditoru atvērtās **\> darbības, kas tika ģenerētas no maksājumu grafika, \>** dodieties uz Parādi kreditoriem - rēķini - atvērt kreditoru rēķini un ievadiet rēķina numuru vai kreditora kontu.
 - Lai pārskatītu vai konfigurētu maksājumu grafiku, dodieties uz sadaļu **Parādi kreditoriem \> maksājumu iestatīšanas \> maksājumu grafikam**.
 - Lai konfigurētu maksājuma nosacījumus un piešķirtu maksājumu grafiku, dodieties uz sadaļu **Kreditoru \> maksājumu \> iestatījumu apmaksas nosacījumi**.
 - Lai uzturētu kreditora apmaksas nosacījumus, **\>** dodieties uz Parādi kreditoriem visiem kreditoriem, **atlasiet** kreditora kontu un pēc tam cilnē Maksājums iestatiet **apmaksas** nosacījumus.

Maksājumu grafika funkcija ir pieejama arī Kreditoru **rēķinu reģistrēšanas** procesā. Ja maksājumu grafiks ir atlasīts rēķinu reģistrācijas žurnālā, vairākas kreditora maksājuma rindas **netiks** ģenerētas, kad tiek grāmatots rēķinu reģistrs. Kreditora maksājuma rindas tiks ģenerētas, kad rēķins būs apstiprināts.

## <a name="limitation"></a>Ierobežojums

Neizlemta kreditora rēķinam, ja maksājumu grafiks ir rēķina galvenē, ir papildu lapa, kas ļauj lietotājiem rediģēt maksājuma rindas. (Piemēram, lietotāji var labot apmaksas datumu un vērtību katrai maksājuma rindai.) No rēķinu žurnāla ģenerētajām maksājuma rindām būs vērtība no maksājumu grafika.

Šī funkcionalitāte būs pieejama kreditoru rēķinu žurnālam **un neizlemtajiem** **rēķiniem** nākamajā laidienā.
