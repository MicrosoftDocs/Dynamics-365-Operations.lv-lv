---
title: IoT informācijas pievienojumprogrammas instalēšana LCS
description: Šajā rakstā ir izskaidrots, kā instalēt Iot Intelligence pievienojumprogrammu Microsoft Dynamics Lifecycle Services (LCS).
author: johanhoffmann
ms.date: 08/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e18b05be1f2ba78c71515e4e76f180355d044b98
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2022
ms.locfileid: "9227840"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a>IoT informācijas pievienojumprogrammas instalēšana LCS

[!include [banner](../../includes/banner.md)]
[!INCLUDE [iot-sdi-announcement](../../includes/iot-sdi-announcement.md)]

Šajā rakstā ir izskaidrots, kā instalēt Iot Intelligence pievienojumprogrammu Microsoft Dynamics Lifecycle Services (LCS). Ņemiet vērā, ka pievienojumprogrammas nevar instalēt demonstrācijas/izmēģinājuma vidē. Pirms varat instalēt pievienojumprogrammu, jums ir [jāizveido Azure resursi](iot-azure-setup.md).

Varat iestatīt un konfigurēt Lietiskā interneta informāciju, nerakstot nekādus kodus. Šeit ir pamata soļi.

1. [Iestatīt Azure resursus](iot-azure-setup.md) - izveidojiet IoT pārkraušanas punktu, Redis kešatmiņu un atslēgas kešatmiņu, kam var piekļūt no Supply Chain Management.
2. [Ziņojumu shēmas formāti IoT hub](iot-schema-format.md) - konfigurējiet ierīces, lai sūtītu ziņojumus uz Iot Hub, un definējiet JavaScript Object Notation (JSON) ziņojuma formātu.
3. Līdzekļu pārvaldībā iespējojiet IoT Informācijas funkcionalitātes karodziņu.
4. Instalējiet Iot Intelligence Microsoft Dynamics pievienojumprogrammu Lifecycle Services (LCS) — instalējiet pievienojumprogrammu LCS un konfigurējiet Azure noslēpumus (kā aprakstīts šajā rakstā).
5. [Iestatīt rādījumus](iot-metrics-setup.md) – iestatiet rādījumus Supply Chain Management.
6. [Scenāriju iestatīšana](iot-scenario-setup.md) – iestatīt scenārijus Supply Chain Management.

## <a name="set-up-the-lcs-environment"></a>Iestatīt LCS vidi

1. Atveriet LCS un dodieties uz savu Microsoft Dynamics 365 Supply Chain Management vidi.
2. Ritiniet līdz sadaļai **Vides pievienojumprogrammas**.
3. Atlasiet **Instalēt jaunu pievienojumprogrammu**, lai skatītu videi iespējoto pievienojumprogrammu sarakstu.
4. Dialoglodziņā **Atlasīt instalējamo pievienojumprogrammu** atlasiet **IoT informācija**.
5. Dialoglodziņā **Iestatīt pievienojumprogrammu** norādiet detalizētu informāciju par savu IoT centrmezglu un Redis kešatmiņu. Nepieciešamās vērtības varat atrast atslēgas akreditācijas datu komplektā, ko izveidojāt [Azure resursu izveidošana](iot-azure-setup.md).

    + **Nomnieka ID** – Azure portālā dodieties uz atslēgas akreditācijas datu komplektu un pēc tam kreisās puses navigācijas rūtī atlasiet **Pārskats** un kopējiet **Direktorija ID** vērtību. Ielīmējiet šo vērtību dialoglodziņā **Iestatīt pievienojumprogrammu**.
    + **IoT Event Hub-saderīgs galapunkta atslēgas akreditācijas datu komplekta URI** – dodieties uz atslēgas akreditācijas datu komplektu un pēc tam kreisās puses navigācijas rūtī atlasiet **Pārskats** un kopējiet **DNS nosaukums** vērtību. Ielīmējiet šo vērtību dialoglodziņā **Iestatīt pievienojumprogrammu**.
    + **IoT Event Hub-saderīgā galapunkta noslēpumu nosaukums** – dodieties uz atslēgas akreditācijas datu komplektu un pēc tam kreisās puses navigācijas rūtī atlasiet **Noslēpumi** un kopējiet noslēpuma nosaukumu, kur tiek glabāta notikuma centrmezgla savienojuma virkne IoT centrmezglam. Ielīmējiet šo vērtību dialoglodziņā **Iestatīt pievienojumprogrammu**.
    + **Redis kešatmiņas atslēgas akreditācijas datu komplekta URI** – dodieties uz atslēgas akreditācijas datu komplektu un pēc tam kreisās puses navigācijas rūtī atlasiet **Pārskats** un kopējiet **DNS nosaukums** vērtību. Ielīmējiet šo vērtību dialoglodziņā **Iestatīt pievienojumprogrammu**.
    + **Redis kešatmiņas galapunkta noslēpumu nosaukums** – dodieties uz atslēgas akreditācijas datu komplektu un pēc tam kreisās puses navigācijas rūtī atlasiet **Noslēpumi** un kopējiet noslēpuma nosaukumu, kur tiek glabāta savienojuma virkne Redis kešatmiņai. Ielīmējiet šo vērtību dialoglodziņā **Iestatīt pievienojumprogrammu**.

6. Atzīmējiet izvēles rūtiņu, lai piekristu noteikumiem un nosacījumiem.
7. Atlasiet **Instalēt**.
8. Tiek parādīts ziņojuma lodziņš ar tekstu "Pievienojumprogramma ir sekmīgi aktivizēta instalēšanai." Atlasiet **Labi**.

LCS iestatīšana tagad ir pabeigta. Nākamā darbība ir [Scenāriju iestatīšana](iot-scenario-setup.md).

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a>Pievienojumprogrammas atinstalēšana

1. Supply Chain Management [scenāriju atspējošana](iot-scenario-setup.md#disable-a-scenario).
2. LCS dodieties uz savas Supply Chain Management vides informāciju.
3. Ritiniet līdz sadaļai **Vides pievienojumprogrammas**.
4. Atlasiet **Atinstalēt** IoT informācijas pievienojumprogrammai.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]