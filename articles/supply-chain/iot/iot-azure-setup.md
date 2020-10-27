---
title: Azure resursu iestatīšana IoT informācijai
description: Šajā tēmā ir paskaidrots, kā izveidot un konfigurēt Microsoft Azure resursus, kas nepieciešami IoT informācijai.
author: ''
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bbac1676d28c7285c19ed48f77426a37ce123a29
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982898"
---
# <a name="set-up-azure-resources-for-iot-intelligence"></a>Azure resursu iestatīšana IoT informācijai

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā izveidot un konfigurēt Microsoft Azure resursus, kas nepieciešami IoT informācijai.

## <a name="create-azure-resources"></a>Azure resursu izveidošana

Veiciet šīs darbības, lai izveidotu IoT centrmezglu, Redis kešatmiņu un atslēgu akreditācijas datu komplektu, kam var piekļūt korporācija Microsoft Dynamics 365 Supply Chain Management.

### <a name="verify-that-the-microsoft-dynamics-erp-microservices-first-party-app-id-is-in-your-tenant"></a>Pārbaudīt, vai Microsoft Dynamics ERP apakšpakalpojumu pirmās puses programmas ID ir jūsu nomniekā

Lai pārbaudītu, vai programmas ID Microsoft Dynamics ERP apakšpakalpojuma pirmās puses programmai ir jūsu nomniekā, rīkojieties šādi.

1. Pierakstieties Azure portālā vietnē <https://portal.azure.com>.
2. Dodieties uz **Azure Active Directory**.
3. Dodieties uz **Uzņēmuma lietojumprogrammas**.
4. Laukā **Lietojumprogrammas veids** atlasiet **Microsoft lietojumprogrammas**.
5. Meklēšanas laukā ievadiet **Microsoft Dynamics ERP apakšpakalpojumi**.
6. Pārbaudiet, vai **Microsoft Dynamics ERP apakšpakalpojumi** ir sarakstā. Citām lietojumprogrammām ir līdzīgi nosaukumi. Tāpēc pārliecinieties, vai tiek atrastas pareizās lietojumprogrammas. Programmas ID ir **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.

    Ja lietojumprogramma nav sarakstā, tā ir jāpievieno nomniekam:

    1. Azure portāla rīkjoslā atlasiet pogu, lai atvērtu Azure Cloud Shell.
    2. Izpildiet komandu **Install-Module AzureAD**. Ievadiet **Y**, lai instalētu moduli.
    3. Izpildiet komandu **Get-InstalledModule -Name "AzureAD"**, lai pārbaudītu, vai modulis ir instalēts.
    4. Izpildiet komandu **Connect-AzureAD -Confirm**, lai palaistu autentifikāciju.
    5. Izpildiet komandu **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**.

    Tagad varat atkārtot 1. līdz 6. darbību, lai pārbaudītu, vai programmas ID ir jūsu nomniekā.

### <a name="create-a-key-vault-resource"></a>Atslēgas akreditācijas datu komplekta resursa veidošana

Lai izveidotu atslēgas akreditācijas datu komplekta resursu, rīkojieties šādi.

1. Azure portālā izveidojiet vai dodieties uz resursu grupu.
2. Atlasiet **Pievienot**.
3. Lapā **Jauns** meklēšanas laukā ievadiet **Atslēgas akreditācijas datu komplekts**. Pēc tam atlasiet **Izveidot**.
4. Lapas **Atslēgas akreditācijas datu komplekta izveide**, laukā **Atslēgas akreditācijas datu komplekta nosaukums** ievadiet nosaukumu.
5. Pārskatiet noklusējuma vērtības un pēc tam atlasiet **Pārskatīt + izveidot**.
6. Atlasiet **Izveidot**.

Atslēgas akreditācijas datu komplekts tiek veidots fonā.

### <a name="create-an-iot-hub-resource"></a>IoT centrmezgla resursa izveidošana

Lai izveidotu IoT centrmezgla resursu, rīkojieties šādi.

1. Izveidojiet vai dodieties uz resursu grupu.
2. Atlasiet **Pievienot**.
3. Lapā **Jauns** meklēšanas laukā ievadiet **IoT centrmezgls**. Pēc tam atlasiet **Izveidot**.
4. Laukā **IoT centrmezgla nosaukums** ievadiet nosaukumu.
5. Pārskatiet noklusējuma vērtības un pēc tam atlasiet **Pārskatīt + izveidot**.
6. Atlasiet **Izveidot**.

IoT centrmezgls tiek veidots fonā.

> [!NOTE]
> Ieteicams izveidot tikai vienu IoT centrmezgla resursu katrai videi.

### <a name="create-a-redis-cache-resource"></a>Redis kešatmiņas resursa izveidošana

Lai izveidotu Redis kešatmiņas resursu, rīkojieties šādi.

1. Izveidojiet vai dodieties uz resursu grupu.
2. Atlasiet **Pievienot**.
3. Lapā **Jauns** meklēšanas laukā ievadiet **Azure kešatmiņa Redis**. Pēc tam atlasiet **Izveidot**.
4. Laukā **DNS nosaukums** ievadiet nosaukumu.
5. Pārskatiet noklusējuma vērtības un pēc tam atlasiet **Izveidot**.

Redis kešatmiņa tiek veidota fonā.

> [!NOTE]
> Ieteicams izveidot tikai vienu Redis kešatmiņu katrai videi.

Visi resursi tagad ir izveidoti.

## <a name="configure-the-azure-resources"></a>Azure resursu konfigurēšana

### <a name="configure-the-iot-hub"></a>IoT centrmezgla konfigurēšana

Lai konfigurētu IoT centrmezglu, rīkojieties šādi.

1. Savos resursos atlasiet IoT centrmezgla resursu.
2. Kreisās puses navigācijas rūtī atlasiet **Iebūvētie galapunkti**.
3. Sadaļā **Patērētāju grupas** ielīmējiet šādas patērētāju grupas. Šīs patērētāju grupas atbilst standarta komplektācijā iekļautajiem scenārijiem.

    + microsoft.dynamics.iotintelligence-1
    + microsoft.dynamics.iotintelligence-2
    + microsoft.dynamics.iotintelligence-3

### <a name="configure-the-key-vault"></a>Atslēgas akreditācijas datu komplekta konfigurēšana

Lai konfigurētu atslēgas akreditācijas datu komplektu, rīkojieties šādi.

1. Savos resursos atlasiet atslēgas akreditācijas datu komplekta resursu.
2. Kreisās puses navigācijas rūtī atlasiet **Piekļuves politikas**.
3. Atlasiet **Pievienot piekļuves politiku**.
4. Lapas **Pievienot piekļuves politiku** laukā **Slepenās atļaujas** atlasiet **Iegūt** un **Saraksts**.
5. Noklikšķiniet uz **Atlasīt vadītāju**.
6. Dialoglodziņā **Vadītājs** meklējiet un atlasiet **Microsoft Dynamics ERP apakšpakalpojumi**. Pēc tam atlasiet **Atlasīt**.
7. Atlasiet **Pievienot**.
8. Atlasiet **Saglabāt**.

Programmai tagad ir piekļuve atslēgas akreditācijas datu komplekta noslēpumiem.

### <a name="save-the-iot-hub-connection-string-secret"></a>Saglabāt IoT centrmezgla savienojuma virknes noslēpumu

Lai saglabātu IoT centrmezgla savienojuma virknes noslēpumu, rīkojieties šādi.

1. Savos resursos atlasiet IoT centrmezgla resursu.
2. Kreisās puses navigācijas rūtī atlasiet **Iebūvētie galapunkti**.
3. Kopējiet lauka **Event Hub-saderīgs galapunkts** vērtību.
4. Dodieties uz atslēgas akreditācijas datu komplekta resursu.
5. Kreisās puses navigācijas rūtī atlasiet **Noslēpumi**.
6. Atlasiet **Ģenerēt/Importēt**.
7. Laukā **Nosaukums** ievadiet nosaukumu.
8. Laukā **Vērtība** ielīmējiet iepriekš nokopēto galapunkta vērtību.
9. Atlasiet **Izveidot**.

### <a name="save-the-redis-cache-connection-string-secret"></a>Saglabāt Redis kešatmiņas savienojuma virknes noslēpumu

Lai saglabātu Redis kešatmiņas savienojuma virknes noslēpumu, rīkojieties šādi.

1. Savos resursos atlasiet Redis kešatmiņas resursu.
2. Atlasiet **Piekļuves atslēgas**.
3. Kopējiet vērtību **Primārā savienojuma virkne** laukā.
4. Dodieties uz atslēgas akreditācijas datu komplekta resursu.
5. Kreisās puses navigācijas rūtī atlasiet **Noslēpumi**.
6. Atlasiet **Ģenerēt/Importēt**.
7. Laukā **Nosaukums** ievadiet nosaukumu.
8. Laukā **Vērtība** ielīmējiet iepriekš nokopēto savienojuma virkni.
9. Atlasiet **Izveidot**.

> [!NOTE]
> Atjauninot vienu no savienojuma virknēm, ir jāatjaunina arī slepenās vērtības.

Tagad ir pabeigta nepieciešamo Azure resursu nodrošināšana. Nākamā darbība ir [instalēt IoT informācijas pievienojumprogrammu Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).
