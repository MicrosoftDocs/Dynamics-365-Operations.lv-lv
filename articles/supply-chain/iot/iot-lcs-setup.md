---
title: IoT informācijas pievienojumprogrammas instalēšana LCS
description: Šajā tēmā ir paskaidrots, kā instalēt IoT informācijas pievienojumprogrammu Microsoft Dynamics Lifecycle Services (LCS).
author: robinarh
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2d1cc9a7535be05a3e466c27e53047d694cf0160
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826447"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a>IoT informācijas pievienojumprogrammas instalēšana LCS

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā instalēt IoT informācijas pievienojumprogrammu Microsoft Dynamics Lifecycle Services (LCS). Ņemiet vērā, ka pievienojumprogrammas nevar instalēt demonstrācijas/izmēģinājuma vidē. Pirms varat instalēt pievienojumprogrammu, jums ir [jāizveido Azure resursi](iot-azure-setup.md).

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