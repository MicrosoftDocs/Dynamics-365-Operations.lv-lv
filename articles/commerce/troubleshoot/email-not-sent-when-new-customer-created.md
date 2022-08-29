---
title: Veidojot jaunus debitorus, nav nosūtīts sveiciena e-pasta ziņojums
description: Šajā rakstā ir sniegti problēmu novēršanas norādījumi, kas var palīdzēt, ja netiek nosūtīts sveiciena e-pasta paziņojums, izveidojot jaunu debitoru Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 08/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 5aa7d864555f96194500989e2d7ad200d8892121
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219409"
---
# <a name="welcome-email-isnt-sent-when-new-customers-are-created"></a>Veidojot jaunus debitorus, nav nosūtīts sveiciena e-pasts

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir sniegti problēmu novēršanas norādījumi, kas var palīdzēt, ja netiek nosūtīts sveiciena e-pasta paziņojums, izveidojot jaunu debitoru Microsoft Dynamics 365 Commerce.

## <a name="description"></a>Apraksts

Kad programmā Commerce headquarters tiek izveidots jauns debitors, debitoram netiek sūtīts sveiciena e-pasta ziņojums, **pat** ja debitora izveidotajā e-pasta paziņojuma veidam ir konfigurēts e-pasta paziņojums.

## <a name="resolution"></a>Novēršana

### <a name="associate-an-email-notification-profile-under-commerce-parameters"></a>Saistīt e-pasta paziņojuma profilu zem Commerce parametriem

1. Galvenajā birojā dodieties uz sadaļu **Mazumtirdzniecības un Commerce \> Headquarters iestatīšanas \> parametri \> Commerce parametri \> Vispārīgi**.
2. E-pasta **paziņojumu profila** nolaižamajā sarakstā atlasiet e-pasta paziņojuma profilu, kas ietver kartējumu starp debitora izveidotā paziņojuma tipu un debitora izveidoto e-pasta veidni.  

> [!NOTE] 
> Kad iespējojat debitoru izveidotos paziņojumus, debitori, kas ir izveidoti visos juridiskās personas kanālos, saņems debitora izveidoto e-pastu. Pašlaik debitora izveidotos paziņojumus nevar ierobežot ar vienu kanālu.

Papildinformāciju skatiet sadaļā E-pasta [veidņu izveide transakciju notikumiem](../email-templates-transactions.md). 

## <a name="additional-resources"></a>Papildu resursi

[E-pasta paziņojumu profila iestatīšana](../email-notification-profiles.md)
