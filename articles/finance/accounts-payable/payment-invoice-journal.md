---
title: Maksājumu grafika lietošana rēķinu žurnālā
description: Šajā tēmā aprakstīts, kā pievienot maksājumu kreditoru rēķinu žurnālam.
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
ms.openlocfilehash: f6481c3fc033acf4bb563bf1716789216646b60b
ms.sourcegitcommit: 9cbff8a2cdeaf606488fb0044b3de4ab4409c9dc
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/26/2022
ms.locfileid: "8358343"
---
# <a name="apply-a-payment-schedule-to-the-invoice-journal"></a>Maksājumu grafika lietošana rēķinu žurnālā

[!include [banner](../includes/preview-banner.md)]

Microsoft Dynamics 365 Finance laidienā 10.0.25 maksājumu grafiks tagad tiek atbalstīts **kreditoru rēķinu žurnālā**.

Lai izmantotu šo funkcionalitāti, līdzekļu pārvaldībā ir jāiespējo **līdzeklis Lietot maksājumu grafiku rēķinu žurnālam**.

Kad līdzeklis ir iespējots, rēķinu žurnāla **lapai tiek pievienots** jauns **maksājumu grafika** lauks. Veidojot rēķinu žurnāla rindu, ja kreditoram tiek saglabāti apmaksas nosacījumi un maksājumu grafikā ir atlasīti apmaksas nosacījumi, **lauks Maksājumu grafiks** tiek atjaunināts **lapā Rēķinu žurnāls**.

Jūs varat mainīt izmantoto maksājumu grafiku atbilstoši uzņēmuma prasībām. Grāmatojot kreditoru rēķinu žurnālu, kreditoru atvērtās darbības tiks izveidotas saskaņā ar maksājumu grafiku.

 - Lai pārskatītu vairākas kreditora atvērtās darbības, kas ģenerētas no maksājumu grafika, dodieties uz **Kreditoru \> rēķini \> Atvērtie kreditoru rēķini** un ievadiet rēķina numuru vai kreditora kontu.
 - Lai pārskatītu vai konfigurētu maksājumu grafiku, dodieties uz **Kreditoru maksājumu uzstādījumi \> Maksājumu grafiks \>**.
 - Lai konfigurētu apmaksas nosacījumus un piešķirtu maksājumu grafiku, dodieties uz **Kreditoru \> maksājumu iestatīšanas \> maksāšanas** noteikumi.
 - Lai saglabātu kreditora apmaksas nosacījumus, dodieties uz Parādi kreditoriem **\> Visi kreditori**, atlasiet kreditora kontu un pēc tam **cilnē Maksājums** iestatiet **lauku Apmaksas** nosacījumi.

Maksājumu grafika līdzeklis ir pieejams **arī kreditoru rēķinu reģistra** procesā. Ja rēķinu reģistra žurnālā ir atlasīts maksājumu grafiks, grāmatojot rēķinu reģistru, vairākas kreditoru maksājumu rindas **netiks** ģenerētas. Kreditora maksājuma rindas tiks ģenerētas, kad rēķins tiks apstiprināts.

## <a name="limitation"></a>Ierobežojums

Nenolemētam kreditora rēķinam, ja maksājumu grafiks ir rēķina virsrakstā, ir papildu lapa, kas ļauj lietotājiem rediģēt maksājumu rindas. (Piemēram, lietotāji var rediģēt izpildes datumu un vērtību katrai maksājuma rindai.) Maksājumu rindām, kas ģenerētas no rēķinu žurnāla, būs maksājumu grafika vērtība.

Šī funkcionalitāte būs pieejama kreditoru rēķinu žurnālam **un** **Gaidošajiem rēķiniem** nākamajā laidienā.
