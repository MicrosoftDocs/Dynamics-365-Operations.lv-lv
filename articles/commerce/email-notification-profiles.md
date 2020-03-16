---
title: E-pasta paziņojumu iestatīšana
description: Šajā tēmā aprakstīts, kā izveidot e-pasta paziņojumu profilu programmā Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 320f21916a5f451ebf4f21e0075017a121ba6d6a
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057618"
---
# <a name="set-up-an-email-notification-profile"></a>E-pasta paziņojumu iestatīšana


[!include [banner](includes/banner.md)]

Šajā tēmā aprakstīts, kā izveidot e-pasta paziņojumu profilu programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Pirms kanālu izveides jums vajadzēs iestatīt profilu, lai nodrošinātu, ka dažādiem notikumiem, piemēram, pasūtījuma izveidei, pasūtījuma nosūtīšanas statusam un maksājuma kļūmei, var nosūtīt e-pasta paziņojumus.

Papildinformāciju par e-pasta ziņojumu konfigurēšanu skatiet rakstā [E-pasta ziņojumu konfigurēšana un sūtīšana](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-email).

## <a name="create-an-email-notification-profile"></a>E-pasta paziņojumu profila izveide

Lai izveidotu e-pasta paziņojumu profilu, izpildiet tālāk norādītās darbības.

1. Navigācijas rūtī pārejiet uz sadaļu **Moduļi \> Mazumtirdzniecība un komercija \> Headquarters iestatīšana \>Komercijas e-pasta paziņojumu profils**.
1. Darbību rūtī noklikšķiniet uz **Jauns**.
1. Lai identificētu profilu, ievadiet nosaukumu laukā **E-pasta paziņojumu profils**.
1. Ievadiet atbilstošu aprakstu laukā **Apraksts**.
1. Iestatiet slēdzi **Aktīvs** uz **Jā**.

### <a name="create-an-email-template"></a>E-pasta veidnes izveidošana

Lai varētu izveidot e-pasta paziņojumu, jāizveido organizācijas e-pasta veidne, kurā iekļauta sūtītāju e-pasta informācija un e-pasta veidne.

Lai izveidotu e-pasta veidni, izpildiet tālāk norādītās darbības.

1. Navigācijas rūtī pārejiet uz sadaļu **Moduļi \> Mazumtirdzniecība un komercija \> Headquarters iestatīšana \> Parametri \> Organizāciju e-pasta veidnes**.
1. Darbību rūtī atlasiet **Jauns**.
1. Laukā **E-pasta ID** ievadiet ID, lai palīdzētu identificēt šo veidni.
1. Laukā **Sūtītāja nosaukums** ievadiet sūtītāja nosaukumu.
1. Ievadiet jēgpilnu aprakstu laukā **Epasta apraksts**.
1. Laukā **Sūtītāja e-pasta adrese** ievadiet sūtītāju e-pasta adresi.
1. Sadaļā **Vispārīgi** aizpildiet visu izvēles informāciju (piemēram, e-pasta prioritāte).
1. Paplašiniet sadaļu **E-pasta ziņojuma saturs** un atlasiet **Jauns**, lai izveidotu veidnes saturu. Katram satura vienumam atlasiet valodu un norādiet e-pasta tēmas rindu. Ja e-pasta ziņojumā būs pamatteksts, pārliecinieties, ir atzīmēta izvēles rūtiņa **Ir pamatteksts**.
1. Darbības rūtī atlasiet **E-pasta ziņojums**, lai nodrošinātu e-pasta pamatteksta veidni.

Tālāk redzamajā attēlā parādīti daži e-pasta veidnes iestatījumi.

![E-pasta veidņu iestatījumi](media/email-template.png)

### <a name="create-an-email-event"></a>E-pasta notikuma izveide

Lai izveidotu e-pasta notikumu, izpildiet tālāk norādītās darbības.

1. Navigācijas rūtī pārejiet uz sadaļu **Moduļi \> Mazumtirdzniecība un komercija \> Headquarters iestatīšana \>Komercijas e-pasta paziņojumu profils**.
1. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu. 
1. **E-pasta ID** nolaižamajā sarakstā atlasiet e-pasta veidni.
1. Nolaižamajā sarakstā atlasiet atbilstošu **E-pasta paziņojumu veidu**.
1. Atzīmējiet izvēles rūtiņu **Aktivizēt**.
1. Darbību rūtī atlasiet **Saglabāt**.

Tālāk redzamajā attēlā parādīti daži notikuma paziņojumu iestatījumi.

![Notikuma paziņojuma iestatījumi](media/email-notification-profile.png)

## <a name="additional-resources"></a>Papildu resursi

[E-pasta konfigurēšana un sūtīšana](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-email)

[Kanālu apskats](channels-overview.md)

[Kanālu iestatīšanas priekšnosacījumi](channels-prerequisites.md)

[Organizācijas un organizāciju hierarhiju pārskats](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
