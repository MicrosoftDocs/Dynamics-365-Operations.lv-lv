---
title: Sensor Data Intelligence parametri
description: Šajā rakstā ir sniegta informācija par konfigurācijas iestatījumiem, kas ir pieejami lapā Sensora datu informācijas parametri.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreServiceParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 5240537e3a6526ceb35253b9e68f46b1753c6a37
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689378"
---
# <a name="sensor-data-intelligence-parameters"></a>Sensor Data Intelligence parametri

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Sensora **datu informācijas parametru** lapa sniedz dažus iestatījumus, ko varat izmantot funkcijas konfigurēšanai. Šie iestatījumi ietver Azure savienojuma parametrus un parametru brīdinājuma ziņojumu darbmūžiem, kas tiek nosūtīti lietotājiem, atbildot uz sensora mērījumiem.

## <a name="read-and-change-connection-details-for-your-azure-iot-solution"></a>Lasīt un mainīt savienojuma detaļas jūsu Azure IoT risinājumam

Parasti iestatīsit risinājumu Azure IoT un savienosiet to ar pakalpojumu Microsoft Dynamics 365 Supply Chain Management **no lapas Izvietot un savienot Azure** resursus, kas palīdzēs veikt abas procedūras. (Plašāku informāciju skatiet [Izvietojiet IoT risinājumu Azure](sdi-deploy-iot-solution-on-azure.md).) Varat arī skatīt un rediģēt savienojuma detaļas jebkurā laikā Piegādes ķēžu pārvaldībā, sekojot šiem soļiem.

1. Dodieties uz sistēmas **administrēšanas iestatīšanas \>\> sensora datu inteliģences \> sensora datu inteliģences parametriem**.
1. Cilnē Laika **sērijas**, **kas atrodas laukā Redis metriskas** krātuves savienojuma virkne, ievadiet primārā savienojuma virknes (StackExchange.Redis) **vērtību Azure IoT risinājumam,** ar kuru vēlaties izveidot savienojumu. Papildinformāciju par to, kā atrast šo vērtību, skatiet [sadaļā IoT risinājuma izvietošana Azure](sdi-deploy-iot-solution-on-azure.md).
1. Cilnes Integrācijas **laukā** Programmas klienta ID ievadiet klienta ID **Azure AD** **vērtību Azure IoT risinājumam,** ar kuru vēlaties izveidot savienojumu. Papildinformāciju par to, kā atrast šo vērtību, skatiet [sadaļā IoT risinājuma izvietošana Azure](sdi-deploy-iot-solution-on-azure.md).

## <a name="set-the-lifetime-of-alert-messages"></a>Brīdinājuma ziņojumu darbmūžības iestatīšana

Katru reizi, kad sensora datu informācija nosaka situāciju, kurai ir nepieciešama lietotāja uzmanība, tā nosūta paziņojumu atbilstošam lietotājam. Lai novērstu šo paziņojumu saīsišanu sistēmā, tie jāuzstāda pēc dažām dienām.

1. Dodieties uz sistēmas **administrēšanas iestatīšanas \>\> sensora datu inteliģences \> sensora datu inteliģences parametriem**.
1. Cilnes Paziņojumi **laukā** Paziņojuma dienas **, kas** jāaizpilda, ievadiet dienu skaitu, cik ilgi paziņojums jāglabā. Kad norādītais laiks ir paiet, paziņojums tiks dzēsts.
