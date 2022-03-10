---
title: Veidojot jaunus debitorus, nav nosūtīts sveiciena e-pasts
description: Šajā tēmā ir sniegtas traucējummeklēšanas norādes, kas var palīdzēt, ja netiek nosūtīts sveiciena e-pasta paziņojums, izveidojot jaunu debitoru Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 1a4faf6cd189f69232e7f9ab8d0e79b320cfe2d9
ms.sourcegitcommit: d2e5d38ed1550287b12c90331fc4136ed546b14c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/25/2022
ms.locfileid: "8349930"
---
# <a name="welcome-email-is-not-sent-when-new-customers-are-created"></a>Veidojot jaunus debitorus, nav nosūtīts sveiciena e-pasts

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir sniegtas traucējummeklēšanas norādes, kas var palīdzēt, ja netiek nosūtīts sveiciena e-pasta paziņojums, izveidojot jaunu debitoru Microsoft Dynamics 365 Commerce.

## <a name="description"></a>Apraksts

Kad programmā Commerce headquarters tiek izveidots jauns debitors, debitoram netiek sūtīts sveiciena e-pasta ziņojums, **pat** ja debitora izveidotajā e-pasta paziņojuma veidam ir konfigurēts e-pasta paziņojums.

## <a name="resolution"></a>Novēršana

### <a name="set-the-correct-email-id-value-for-the-customer-created-email-notification-type"></a>Iestatīt pareizo e-pasta ID vērtību debitora izveidotam e-pasta paziņojuma veidam

Lai programmā galvenā birojā izveidoto **e-pasta** paziņojumu **veidam** iestatītu pareizu e-pasta ID vērtību, izpildiet šīs darbības.

1. Pārejiet uz **mazumtirdzniecības un Commerce \> Headquarters iestatīšanas \> Commerce e-pasta paziņojuma profilu**.
1. Kreisās puses navigācijas rūtī atlasiet e-pasta paziņojuma profilu.
1. Sadaļā **Mazumtirdzniecības notikumu paziņojumu iestatījumi**, debitora izveidoto **e-pasta** paziņojumu veidam iestatiet e-pasta **ID** lauka vērtību **NewCust**.

## <a name="additional-resources"></a>Papildu resursi

[E-pasta paziņojumu profila iestatīšana](../email-notification-profiles.md)
