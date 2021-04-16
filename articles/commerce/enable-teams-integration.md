---
title: Iespējot Dynamics 365 Commerce un Microsoft Teams integrāciju
description: Šajā tēmā ir aprakstīts, kā aktivizēt Microsoft Dynamics 365 Commerce un Microsoft Teams integrāciju.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c0dbf7a3c7fa3532e35cac240c1abb8adbdbe489
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842703"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a>Iespējot Dynamics 365 Commerce un Microsoft Teams integrāciju

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šajā tēmā ir aprakstīts, kā aktivizēt Microsoft Dynamics 365 Commerce un Microsoft Teams integrāciju.

Lai nodrošinātu Teams ar informāciju no Dynamics 365 Commerce un sinhronizētu uzdevumu pārvaldības līdzekļus starp Teams un pārdošanas punkta (POS) programmu, ir jāiespējo integrācijas līdzekļi programmā Commerce Headquarters.

> [!NOTE]
> Iespējojot Teams integrāciju, jūs atļaujat koplietot datus ar brigādes grupām. Dati, kas tiek koplietoti ar Teams, var atrasties citā valstī, nevis jūsu Commerce datos, un uz tiem var būt attiecas atšķirīgi saskaņotības standarti. Papildinformāciju par šīm izmaiņām skatiet sadaļā [Microsoft drošības kontroles centrs](https://www.microsoft.com/trust-center). Papildinformāciju par Microsoft konfidencialitātes politikām skatiet [Microsoft Konfidencialitātes paziņojums](https://aka.ms/privacy).

## <a name="enable-teams-integration"></a>Iespējot Teams integrāciju

Lai iespējotu Microsoft Teams integrāciju ar commerce, jums Azure portālā ir jāreģistrē programma Teams ar savu nomnieku.

Lai reģistrētu programmu Teams savam nomniekam Azure portālā, veiciet tālāk norādītās darbības.

1. Veiciet norādītās darbības sadaļā [Ātrais starts: reģistrējiet programmu Microsoft identitātes platformā](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app), lai reģistrētu programmu Teams kopā ar nomnieku Azure portālā.
1. Kopējiet **Programmas (klienta) ID** vērtību no reģistrētās programmas **Pārskata** lapas. Šī vērtība tiks izmantota, lai iespējotu Teams integrāciju programmā Commerce Headquarters.
1. Kopējiet sertifikāta vērtību, kas tika ievadīta, kad [pievienojāt sertifikātu](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#add-a-certificate) 1. solī. Sertifikāts tiek saukts arī par publisko atslēgu vai programmas atslēgu. Šī vērtība tiks izmantota, lai iespējotu Teams integrāciju programmā Commerce Headquarters.

Lai iespējotu Teams integrāciju Commerce Headquarters, veiciet tālāk norādītās darbības.

1. Dodieties uz **Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> Microsoft Teams integrācijas konfigurēšana**.
1. Darbību rūtī atlasiet **Rediģēt**.
1. Iestatiet opciju **Iespējot Microsoft Teams integrāciju** uz **Jā**.
1. Laukos **Programmas ID** un **Programmas atslēga** ievadiet vērtības, ko ieguvāt, kad Azure portālā reģistrējāt programmu Teams.
1. Darbību rūtī atlasiet **Saglabāt**.

Šajā attēlā parādīts Teams integration konfigurācijas piemērs Commerce Headquarters.

![Grupu integrācijas konfigurācija programmā Commerce Headquarters](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

## <a name="disable-teams-integration"></a>Atspējot Teams integrāciju

Lai atspējotu Microsoft Teams integrāciju Commerce Headquarters, veiciet tālāk norādītās darbības.

1. Dodieties uz **Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> Microsoft Teams integrācijas konfigurēšana**.
1. Darbību rūtī atlasiet **Rediģēt**.
3. Iestatiet opciju **Iespējot Microsoft Teams integrāciju** uz **Nē**.
4. Notīriet vērtības no laukiem **Programmas ID** un **Programmas atslēga**.
1. Darbību rūtī atlasiet **Saglabāt**.

> [!NOTE]
> Pēc brigādes integrācijas programmas Commerce deaktivizēšanas POS termināļi vairs nerādīs uzdevumus, kas publicēti no programmas Teams.

## <a name="additional-resources"></a>Papildu resursi

[Dynamics 365 Commerce un Microsoft Teams integrācijas pārskats](commerce-teams-integration.md)

[Nodrošināt Microsoft Teams no Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Sinhronizēt uzdevumu pārvaldību starp Microsoft Teams un Dynamics 365 Commerce POS](synchronize-tasks-teams-pos.md)

[Lietotāju lomu pārvaldība Microsoft Teams](manage-user-roles-teams.md)

[Kartējiet veikalus un grupas, ja programmā ir iepriekšējas darba grupas Microsoft Teams](map-stores-existing-teams.md)

[Dynamics 365 Commerce un Microsoft Teams integrācijas BUJ](teams-integration-faq.md)
