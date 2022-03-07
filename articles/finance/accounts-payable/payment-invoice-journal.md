---
title: Piesakiet maksājumu grafiku rēķinu žurnālam
description: Šajā tēmā ir aprakstīts, kā pievienot maksājumu piegādātāja rēķinu žurnālam.
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
ms.openlocfilehash: bd288ac48ef59d8e2a4e0922aa652276dddb666d
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075738"
---
# <a name="apply-a-payment-schedule-to-the-invoice-journal"></a>Piesakiet maksājumu grafiku rēķinu žurnālam

[!include [banner](../includes/preview-banner.md)]

Programmā Microsoft Dynamics 365 Finance laidiens 10.0.25, maksājumu grafiks tagad tiek atbalstīts piegādātāja rēķinu žurnālā.

Lai izmantotu šo funkciju, ir jāiespējo **Pielietot maksājumu grafiku rēķinu žurnālam** funkciju pārvaldībā.

Kad funkcija ir iespējota, jauna **Maksājumu grafiks** lauks tiek pievienots **Rēķinu žurnāls** lappuse. Kad veidojat rēķina žurnāla rindu, ja maksāšanas noteikumi tiek uzturēti pie piegādātāja un maksājuma noteikumi ir atlasīti maksājumu grafikā, **Maksājumu grafiks** lauks ir atjaunināts **Rēķinu žurnāls** lappuse.

Varat mainīt izmantoto maksājumu grafiku atbilstoši jūsu uzņēmuma prasībām. Pārdevēja rēķinu žurnāla grāmatošanas laikā saskaņā ar maksājumu grafiku tiks izveidotas piegādātāja atvērtās transakcijas.

Lai pārskatītu vairākus piegādātāju atvērtos darījumus, kas tika ģenerēti no maksājumu grafika, dodieties uz **Kreditori \> Rēķini \> Atvērtie piegādātāja rēķini** un ievadiet rēķina numuru vai piegādātāja kontu.

Lai pārskatītu vai konfigurētu maksājumu grafiku, dodieties uz **Kreditori \> Maksājuma iestatīšana \> Maksājumu grafiks**.

Lai konfigurētu maksājumu noteikumus un piešķirtu maksājumu grafiku, dodieties uz **Kreditori \> Maksājuma iestatīšana \> Maksājuma nosacījumi**.

Lai saglabātu pārdevēja maksājumu noteikumus, dodieties uz **Kreditori \> Visi pārdevēji**, atlasiet piegādātāja kontu un pēc tam uz **Maksājums** cilnē iestatiet **Maksājuma nosacījumi** lauks.

Maksājumu grafika funkcija ir pieejama arī **Pārdevēja rēķinu reģistrs** process. Ja rēķinu reģistra žurnālā ir atlasīts maksājumu grafiks, tiks izmantotas vairākas piegādātāja maksājumu rindas **nē** jāģenerē, kad tiek reģistrēts rēķinu reģistrs. Pārdevēja maksājumu rindas tiks ģenerētas, kad tiks apstiprināts rēķins.

## <a name="limitation"></a>Ierobežojums

Ja rēķina galvenē ir norādīts neapstiprināta piegādātāja rēķina maksājumu grafiks, ir pieejama papildu lapa, kurā lietotāji var rediģēt maksājumu rindas. (Piemēram, lietotāji var rediģēt katras maksājuma rindas izpildes datumu un vērtību.) Maksājumu rindām, kas tiek ģenerētas no rēķinu žurnāla, būs vērtība no maksājumu grafika.

Šī funkcionalitāte būs pieejama piegādātāja rēķinu žurnālam un neapstiprinātajiem rēķiniem nākamajā laidienā.
