---
title: E-pasta paziņojumu iestatīšana
description: Šajā tēmā aprakstīts, kā izveidot e-pasta paziņojumu profilu programmā Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 02/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 7a7d796a173a6f9dfcd62e1f73e078cac614145e
ms.sourcegitcommit: 2aca3a95d42403c7f5d80dcd5e3ee958dca5c894
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2022
ms.locfileid: "8087871"
---
# <a name="set-up-an-email-notification-profile"></a>E-pasta paziņojumu profila iestatīšana

[!include [banner](includes/banner.md)]

Šajā tēmā aprakstīts, kā izveidot e-pasta paziņojumu profilu programmā Microsoft Dynamics 365 Commerce.

Veidojot kanālus, varat iestatīt e-pasta paziņojuma profilu. E-pasta paziņojumu profils definē pārdošanas darījuma notikumus (piemēram, pasūtījuma izveides, pasūtījuma iesaiņošanas un pasūtījuma rēķina notikumi), par kuriem jūs nosūtīsit paziņojumus saviem klientiem. 

Papildinformāciju par e-pasta ziņojumu konfigurēšanu skatiet rakstā [E-pasta ziņojumu konfigurēšana un sūtīšana](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).

## <a name="create-an-email-notification-profile"></a>E-pasta paziņojumu profila izveide

Lai izveidotu e-pasta paziņojumu profilu, izpildiet tālāk norādītās darbības.

1. Navigācijas rūtī pārejiet uz sadaļu **Moduļi \> Mazumtirdzniecība un komercija \> Headquarters iestatīšana \> Komercijas e-pasta paziņojumu profils**.
1. Darbību rūtī noklikšķiniet uz **Jauns**.
1. Lai identificētu profilu, ievadiet nosaukumu laukā **E-pasta paziņojumu profils**.
1. Ievadiet atbilstošu aprakstu laukā **Apraksts**.
1. Iestatiet slēdzi **Aktīvs** uz **Jā**.

### <a name="create-an-email-template"></a>E-pasta veidnes izveidošana

Lai varētu iespējot e-pasta paziņojumu veidu, jums ir jāizveido organizācijas e-pasta veidne Commerce galvenajā mītnē katram paziņojumu veidam, kuru vēlaties atbalstīt. Šī veidne katrai atbalstītajai valodai nosaka e-pasta tēmu, sūtītāju, noklusējuma valodu un e-pasta pamattekstu.

Lai izveidotu e-pasta veidni, izpildiet tālāk norādītās darbības.

1. Navigācijas rūtī pārejiet uz sadaļu **Moduļi \> Mazumtirdzniecība un komercija \> Headquarters iestatīšana \> Parametri \> Organizāciju e-pasta veidnes**.
1. Darbību rūtī atlasiet **Jauns**.
1. Laukā **E-pasta ID** ievadiet ID, lai palīdzētu identificēt šo veidni.
1. Laukā **Sūtītāja nosaukums** ievadiet sūtītāja nosaukumu.
1. Ievadiet jēgpilnu aprakstu laukā **Epasta apraksts**.
1. Laukā **Sūtītāja e-pasta adrese** ievadiet sūtītāju e-pasta adresi.
1. Sadaļā **Vispārīgi** atlasiet noklusējuma valodu e-pasta veidnei. Noklusējuma valoda tiks lietota, ja norādītajai valodai nav lokalizētas veidnes.
1. Paplašiniet sadaļu **E-pasta ziņojuma saturs** un atlasiet **Jauns**, lai izveidotu veidnes saturu. Katram satura vienumam atlasiet valodu un norādiet e-pasta tēmas rindu. Ja e-pasta ziņojumā būs pamatteksts, pārliecinieties, ir atzīmēta izvēles rūtiņa **Ir pamatteksts**.
1. Darbības rūtī atlasiet **E-pasta ziņojums**, lai nodrošinātu e-pasta pamatteksta veidni.

Tālāk redzamajā attēlā parādīti daži e-pasta veidnes iestatījumi.

![E-pasta veidņu iestatījumi.](media/email-template.png)

Papildinformāciju par e-pasta veidņu izveidi skatiet rakstā [Izveidojiet e-pasta veidnes darījumu notikumiem](email-templates-transactions.md). 

### <a name="create-an-email-event"></a>E-pasta notikuma izveide

Lai izveidotu e-pasta notikumu, izpildiet tālāk norādītās darbības.

1. Navigācijas rūtī pārejiet uz sadaļu **Moduļi \> Mazumtirdzniecība un komercija \> Headquarters iestatīšana \> Komercijas e-pasta paziņojumu profils**.
1. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu. 
1. **E-pasta ID** nolaižamajā sarakstā atlasiet e-pasta veidni.
1. Nolaižamajā sarakstā atlasiet atbilstošu **E-pasta paziņojumu veidu**.
1. Atzīmējiet izvēles rūtiņu **Aktivizēt**.
1. Darbību rūtī atlasiet **Saglabāt**.

Tālāk redzamajā attēlā parādīti daži notikuma paziņojumu iestatījumi.

![Notikuma paziņojuma iestatījumi.](media/email-notification-profile.png)

> [!NOTE]
> Lai varētu nosūtīt e-pasta paziņojumu, klienta izveidotajam paziņojuma veidam ir jāievieš pielāgošana.

### <a name="next-steps"></a>Turpmākās darbības

Lai varētu nosūtīt e-pastus, ir jākonfigurē izejošais pasta pakalpojums un jāiestata pakešuzdevums. Papildinformāciju skatiet [E-pasta konfigurēšana un sūtīšana](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).

## <a name="additional-resources"></a>Papildu resursi

[E-pasta konfigurēšana un sūtīšana](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[Kanālu apskats](channels-overview.md)

[Kanālu iestatīšanas priekšnosacījumi](channels-prerequisites.md)

[Organizācijas un organizāciju hierarhiju pārskats](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
