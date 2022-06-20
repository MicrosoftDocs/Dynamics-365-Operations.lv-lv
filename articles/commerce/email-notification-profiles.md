---
title: E-pasta paziņojumu profila iestatīšana
description: Šajā rakstā ir aprakstīts, kā izveidot e-pasta paziņojuma profilu Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 02/11/2022
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
ms.openlocfilehash: 109adcc4e8b49c665bd14ecab2b7cc56cebd2291
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878490"
---
# <a name="set-up-an-email-notification-profile"></a>E-pasta paziņojumu profila iestatīšana

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā izveidot e-pasta paziņojuma profilu Microsoft Dynamics 365 Commerce.

Veidojot kanālus, varat iestatīt e-pasta paziņojuma profilu. E-pasta paziņojuma profils nosaka pārdošanas darbības notikumus (piemēram, izveidotais pasūtījums, iepakotais pasūtījums un pasūtījuma rēķinos iekļautais notikums), par kuru jums tiks sūtīti paziņojumi saviem debitoriem. 

Papildinformāciju par e-pasta ziņojumu konfigurēšanu skatiet rakstā [E-pasta ziņojumu konfigurēšana un sūtīšana](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).

## <a name="create-an-email-notification-profile"></a>E-pasta paziņojumu profila izveide

Lai izveidotu e-pasta paziņojumu profilu, izpildiet tālāk norādītās darbības.

1. Navigācijas rūtī pārejiet uz sadaļu **Moduļi \> Mazumtirdzniecība un komercija \> Headquarters iestatīšana \> Komercijas e-pasta paziņojumu profils**.
1. Darbību rūtī noklikšķiniet uz **Jauns**.
1. Lai identificētu profilu, ievadiet nosaukumu laukā **E-pasta paziņojumu profils**.
1. Ievadiet atbilstošu aprakstu laukā **Apraksts**.
1. Iestatiet slēdzi **Aktīvs** uz **Jā**.

### <a name="create-an-email-template"></a>E-pasta veidnes izveidošana

Lai iespējotu e-pasta paziņojuma veidu, programmā Commerce headquarters ir jāizveido organizācijas e-pasta veidne katram paziņojuma veidam, kuru vēlaties atbalstīt. Šī veidne definē e-pasta tēmu, sūtītāju, noklusējuma valodu un e-pasta pamattekstu katrai atbalstītajā valodā.

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

Papildinformāciju par e-pasta veidņu izveidi skatiet sadaļā [E-pasta veidņu izveide darbību notikumiem](email-templates-transactions.md). 

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
> Debitora izveidotā paziņojuma veidam ir nepieciešams pielāgot, lai varētu nosūtīt e-pasta paziņojumu.

### <a name="schedule-a-recurring-email-notification-process-job"></a>Plānot periodisku e-pasta paziņojumu apstrādes darbu

Lai sūtītu e-pasta paziņojumus, ir jādarbojas mazumtirdzniecības **pasūtījuma e-pasta paziņojumu procesa** darbam.

Lai programmā **Commerce Headquarters iestatītu procesu mazumtirdzniecības pasūtījuma e-pasta** paziņojuma darbu, ja tas vēl nav izdarīts, izpildiet šīs darbības.

1. E-pasta ziņojumu un paziņojumu sūtīšana uz e-pasta ziņojumu sūtīt e-pasta **ziņojumu, pārejiet \> uz Retail un Commerce \> Retail un Commerce IT \>**.
1. **Procesa mazumtirdzniecības pasūtījuma e-pasta** paziņojuma dialoglodziņā atlasiet **Periodiskums**.
1. Dialoglodziņā Definēt **atkārtošanos** atlasiet Bez **beigu datuma**.
1. Sadaļā **Periodiskuma** modelis atlasiet **Minūtes** un pēc tam lauku Skaits **iestatiet** uz **1**. Šie iestatījumi nodrošina to, ka e-pasta paziņojumi tiek apstrādāti pēc iespējas ātrāk.
1. Atlasiet Labi **,** lai atgrieztos mazumtirdzniecības **pasūtījuma e-pasta paziņojuma dialoglodziņā** Apstrādāt.
1. Atlasiet **Labi,** lai pabeigtu darba iestatīšanu.

### <a name="next-steps"></a>Turpmākās darbības

Lai varētu nosūtīt e-pastus, ir jākonfigurē izejošais pasta pakalpojums un jāiestata pakešuzdevums. Papildinformāciju skatiet [E-pasta konfigurēšana un sūtīšana](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).

## <a name="additional-resources"></a>Papildu resursi

[E-pasta konfigurēšana un sūtīšana](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[Kanālu apskats](channels-overview.md)

[Kanālu iestatīšanas priekšnosacījumi](channels-prerequisites.md)

[Organizācijas un organizāciju hierarhiju pārskats](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
