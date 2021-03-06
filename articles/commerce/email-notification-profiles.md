---
title: E-pasta paziņojumu iestatīšana
description: Šajā tēmā aprakstīts, kā izveidot e-pasta paziņojumu profilu programmā Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 03/01/2021
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
ms.openlocfilehash: 7504b2b36f6869f90de196bf32c09e7bdd51e7b5
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792661"
---
# <a name="set-up-an-email-notification-profile"></a>E-pasta paziņojumu profila iestatīšana

[!include [banner](includes/banner.md)]

Šajā tēmā aprakstīts, kā izveidot e-pasta paziņojumu profilu programmā Microsoft Dynamics 365 Commerce.

Veidojot kanālus, varat iestatīt e-pasta paziņojuma profilu. Šādā veidā e-pasta ziņojumi var tikt nosūtīti debitoriem par dažādiem darbību notikumiem, piemēram, pasūtījuma izveidi, pasūtījuma nosūtīšanas statusu un maksājuma kļūmi.

Papildinformāciju par e-pasta ziņojumu konfigurēšanu skatiet rakstā [E-pasta ziņojumu konfigurēšana un sūtīšana](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).

## <a name="create-an-email-notification-profile"></a>E-pasta paziņojumu profila izveide

Lai izveidotu e-pasta paziņojumu profilu, izpildiet tālāk norādītās darbības.

1. Navigācijas rūtī pārejiet uz sadaļu **Moduļi \> Mazumtirdzniecība un komercija \> Headquarters iestatīšana \> Komercijas e-pasta paziņojumu profils**.
1. Darbību rūtī noklikšķiniet uz **Jauns**.
1. Lai identificētu profilu, ievadiet nosaukumu laukā **E-pasta paziņojumu profils**.
1. Ievadiet atbilstošu aprakstu laukā **Apraksts**.
1. Iestatiet slēdzi **Aktīvs** uz **Jā**.

### <a name="create-an-email-template"></a>E-pasta veidnes izveidošana

Lai e-pasta paziņojuma tipu varētu iespējot, programmā Commerce Headquarters ir jāizveido organizācijas e-pasta veidne. Šī veidne definē e-pasta tēmu, sūtītāju, noklusējuma valodu un e-pasta pamattekstu katrai valodai, ko vēlaties atbalstīt.

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

![E-pasta veidņu iestatījumi](media/email-template.png)

### <a name="create-an-email-event"></a>E-pasta notikuma izveide

Lai izveidotu e-pasta notikumu, izpildiet tālāk norādītās darbības.

1. Navigācijas rūtī pārejiet uz sadaļu **Moduļi \> Mazumtirdzniecība un komercija \> Headquarters iestatīšana \> Komercijas e-pasta paziņojumu profils**.
1. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu. 
1. **E-pasta ID** nolaižamajā sarakstā atlasiet e-pasta veidni.
1. Nolaižamajā sarakstā atlasiet atbilstošu **E-pasta paziņojumu veidu**.
1. Atzīmējiet izvēles rūtiņu **Aktivizēt**.
1. Darbību rūtī atlasiet **Saglabāt**.

Tālāk redzamajā attēlā parādīti daži notikuma paziņojumu iestatījumi.

![Notikuma paziņojuma iestatījumi](media/email-notification-profile.png)

### <a name="next-steps"></a>Turpmākās darbības

Lai varētu nosūtīt e-pastus, ir jākonfigurē izejošais pasta pakalpojums un jāiestata pakešuzdevums. Papildinformāciju skatiet [E-pasta konfigurēšana un sūtīšana](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).


## <a name="additional-resources"></a>Papildu resursi

[E-pasta konfigurēšana un sūtīšana](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[Kanālu apskats](channels-overview.md)

[Kanālu iestatīšanas priekšnosacījumi](channels-prerequisites.md)

[Organizācijas un organizāciju hierarhiju pārskats](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
