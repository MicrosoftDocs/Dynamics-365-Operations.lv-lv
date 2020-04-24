---
title: Piegādātāja pieprasījuma konfigurācijas
description: Šajā tēmā ir aprakstīti lauki, kuri jaunā piegādātāja pieprasījumā ir jāaizpilda obligāti.
author: mkirknel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationConfig
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: d78aa7c14ed2a2a5097f6f80c946c6ae4ed8bb94
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208090"
---
# <a name="vendor-request-configurations"></a>Piegādātāja pieprasījuma konfigurācijas
[!include [banner](../includes/banner.md)]

Lai izpildītu piegādātāja pieprasījumu, piegādātāja kontaktpersonai ir jāizpilda potenciālā piegādātāja reģistrēšanas vednis.

Formā **Piegādātāja pieprasījuma konfigurācijas** varat izveidot profilus, kas potenciālā piegādātāja reģistrācijas vednī norāda obligātos laukus un redzamos laukus.

Kreditora reģistrācijas vednis sākas, jautājot potenciālā piegādātāja lietotājam par valsti/reģionu, kurā piegādātājs darbojas. Šī informācija nosaka piemērojamo konfigurāciju. Ja kādai valstij/reģionam nav definēta īpaša konfigurācija, tiek izmantota noklusējuma konfigurācija.

### <a name="set-up-a-vendor-request-configuration"></a>Piegādātāja pieprasījuma konfigurācijas iestatīšana

Kreditora konfigurācija pēc noklusējuma ir pieejama formā “Kreditora pieprasījuma konfigurācija”.

Noklusējuma konfigurācijai nav iespējams atlasīt valsti/reģionus, tādēļ sadaļu **Valstis/reģioni** nevar mainīt.

1. Noklikšķiniet uz **Sagāde un avoti** > **Iestatīšana** > **Kreditori** un pēc tam noklikšķiniet uz **Piegādātāja pieprasījuma konfigurācijas**.
2. Noklikšķiniet uz cilnes **Lauki**, lai iestatītu uzskaitīto lauku statusu.
3. Slēpts (nav redzams)
4. Parādīts (redzams, bet nav obligāts)
5. Obligāts (redzams un obligāts)
6. Noklikšķiniet uz cilnes **Saturs**, lai norādītu, vai teksts būs redzams vednī un vai ir nepieciešams apliecinājums, ka potenciālā piegādātāja lietotājam ir jāsniedz piekrišana par šo, pirms notiek pāriešana uz nākamo vedņa posmu. Apstiprinājums tiks pieprasīts par visiem noteikumiem un nosacījumiem, kas lietotājam ir jāpieņem, lai varētu turpināt.

Varat arī ievadīt apstiprinājuma ziņojumu, kas tiek parādīts, kad vednis ir pabeigts, un varat pievienot vienu vai vairākas anketas.

### <a name="create-a-vendor-configuration-for-a-specific-countryregion"></a>Piegādātāja konfigurācijas izveidošana noteiktai valstij/reģionam
1.  Noklikšķiniet uz **Sagāde un avoti** > **Iestatīšana** > **Kreditori** un pēc tam noklikšķiniet uz **Piegādātāja pieprasījuma konfigurācijas**.
2.  Noklikšķiniet uz **Jauns**, lai izveidotu jaunu konfigurāciju, un norādiet šīs konfigurācijas nosaukumu.
3.  Noklikšķiniet uz **Saglabāt**.
4.  Atveriet cilni **Valsts/reģioni**, lai atlasītu valsti/reģionu, kuriem šī konfigurācija ir jāizmanto.
5.  Pabeidziet konfigurēšanu, ievērojot vadlīnijas par noklusējuma konfigurāciju.

