---
title: Nodarbinātā konfigurēšana, izmantojot mobilo darba ierīci
description: Šajā rakstā skaidrots, kā piešķirt pareizās lomas darbinieka lietotāja kontam un pēc tam iespējot darbinieku veikt ražotnes reģistrācijas.
author: johanhoffmann
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3f6f51a66d49cafd172ba123bf883fb41cdcb5c3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844310"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a>Nodarbinātā konfigurēšana, izmantojot mobilo darba ierīci

[!include [banner](../../includes/banner.md)]

Šajā rakstā skaidrots, kā piešķirt pareizās lomas darbinieka lietotāja kontam un pēc tam iespējot darbinieku veikt ražotnes reģistrācijas.

## <a name="verify-that-a-worker-is-assigned-a-certain-role"></a>Pārbaudiet, vai darbiniekam ir piešķirta noteikta loma

Šajā piemērā, pirms konfigurējat darbinieka kontu, pārbaudiet, vai lietotājam "SHANNON" ir piešķirta mašīnas operatora loma.

1. Dodieties uz **Navigācijas rūts > Moduļi > Sistēmas administrēšana > Lietotāji > Lietotāji**.
2. Meklējiet lietotāju ātrajā filtrā. Šim piemēram ievadiet `shannon`.
3. Atlasiet saiti parādītajā lietotāja konta kolonnā **Lietotāja ID**.
4. Kokā **Lietotāja lomas** atlasiet **Lomas > Mašīnas operators**.
5. Aizveriet lapas **Lietotāja informācija** un **Lietotāji**, lai atgrieztos sākumlapā.

## <a name="configure-worker-account"></a>Darbinieka konta konfigurēšana
1. Dodieties uz **Navigācijas rūts > Moduļi > Cilvēkresursi > Darbinieki > Darbinieki**.
2. Meklējiet lietotāju ātrajā filtrā. Šim piemēram ievadiet `shannon`.
3. Atlasiet saiti parādītajā lietotāja konta kolonnā **Nosaukums**.
4. Atlasiet cilni **Laika reģistrācija**.
5. Atlasiet **Aktivizēt reģistrācijas terminālos**.
6. Ievadiet vai atlasiet vērtības šādos laukos:  

    - **Aprēķinu grupa**  
    - **Noklusējuma aprēķinu grupa**  
    - **Apstiprinājumu grupa**  
    - **Standarta profils**  
    - **Profilu grupa**  

7. Atlasiet **Labi**.
8. Noklikšķiniet uz **Rediģēt**, lai ievadītu jauna laika reģistrācijas darbinieka žetona numuru. Ievadiet vērtību laukā **Žetona ID**.
9. Atlasiet **Saglabāt**.
10. Aizveriet lapas **Nodarbinātā papildinformācija** un **Nodarbinātie**.

## <a name="assign-worker-to-device-group"></a>Nodarbinātā piešķiršana ierīču grupai
1. Pārejiet uz sadaļu **Ražošanas kontrole > Iestatīšana > Ražošanas izpilde > Konfigurēt ierīču darba karti**.
2. Atlasiet **Pievienot**.
3. Sarakstā atlasiet vēlamo nodarbināto. Šajā piemērā atlasiet **SHANNON**.
4. Atlasiet **Labi**.
5. Atlasiet **Rediģēt**.
6. Laukā **Ražošanas vienība** var iestatīt noklusējuma filtru nodarbinātajam. Tas nodrošinās, ka, darbiniekam piesakoties ierīcē, tiek rādīti tikai ražošanas darbi atlasītajai ražošanas vienībai. Ievadiet vēlamo vērtību.
7. Aizvērt lapu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]