---
title: Veidojot jaunus debitorus, nav nosūtīts sveiciena e-pasta ziņojums
description: Šajā rakstā ir sniegti problēmu novēršanas norādījumi, kas var palīdzēt, ja netiek nosūtīts sveiciena e-pasta paziņojums, izveidojot jaunu debitoru Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 8e95b33d4b8a9af13c613ab89dd33de6b4934694
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853687"
---
# <a name="welcome-email-is-not-sent-when-new-customers-are-created"></a>Veidojot jaunus debitorus, nav nosūtīts sveiciena e-pasta ziņojums

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir sniegti problēmu novēršanas norādījumi, kas var palīdzēt, ja netiek nosūtīts sveiciena e-pasta paziņojums, izveidojot jaunu debitoru Microsoft Dynamics 365 Commerce.

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
