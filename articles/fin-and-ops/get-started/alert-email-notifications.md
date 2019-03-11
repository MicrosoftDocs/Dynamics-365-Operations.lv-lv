---
title: Klienta brīdinājuma paziņojumi pa e-pastu
description: Šajā tēmā ir sniegta informācija par to, kā iestatīt nosacījumus, kas nodrošina e-pasta paziņojumu nosūtīšanu iepriekš definētu notikumu gadījumā.
author: tjvass
manager: AnnBe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: kfend
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 314f04eec04a75aed058c9c38066738e8758f653
ms.sourcegitcommit: 440ebe14ad26574ba227d23ee8370f6b6110645b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2019
ms.locfileid: "373798"
---
# <a name="client-alert-notifications-by-email"></a>Klienta brīdinājuma paziņojumi pa e-pastu

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Programmā Microsoft Dynamics 365 for Finance and Operations varat definēt pielāgotus brīdinājumu nosacījumus, kas nodrošina filtrēto datu skatu uzraudzību un e-pasta paziņojumu automātisku nosūtīšanu iepriekš definēta notikuma gadījumā. E-pasta paziņojuma nosūtīšanas opcija ir pieejama visiem atbalstītajiem brīdinājumu veidiem, un to var ieslēgt arī esošajiem brīdinājumu nosacījumiem.

Varat izmantot iebūvētās vadīklas, lai izveidotu brīdinājumu nosacījumus, kas nodrošina sistēmas pakešuzdevumu filtrēto skatu uzraudzību. Uzraugot lauka **Statuss** vērtību, varat arī konfigurēt brīdinājumu nosacījumus, kas nodrošina e-pasta ziņojuma nosūtīšanu gadījumā, ja neizdodas veikt pakešuzdevumu. Pēc šo brīdinājumu nosacījumu izveides jums vairs nav jāpārbauda, vai pārskatos ir veiktas biznesa datu izmaiņas. Tā vietā varat uzraudzībai izmantot Finance and Operations intelektisko izmaiņu noteikšanas pakalpojumu.

Klienta brīdinājumi ir atkarīgi no e-pasta apakšsistēmas, ko nodrošina integrācija ar Microsoft Office. Ir ieteicams izmantot vienkāršā pasta pārsūtīšanas protokola (SMTP) nodrošinātāju, lai e-pasta ziņojumu izplatīšanai nebūtu jāizmanto lokālais pasta klients.

Lai nosūtītu paziņojumus pa e-pastu, debitoriem ir jākonfigurē integrētie e-pasta pakalpojumi. E-pasta paziņojumi tiek nosūtīti adresātiem brīdinājuma īpašnieku vārdā.

Papildinformāciju par to, kā konfigurēt e-pasta ziņojumus programmā Finance and Operations, skatiet rakstā [E-pasta ziņojumu konfigurēšana un sūtīšana](../organization-administration/configure-email.md).

Tālāk esošajā attēlā ir redzams dialoglodziņš **Brīdinājuma nosacījumu izveide**, kurā tagad ir ietverta opcija **Sūtīt e-pasta ziņojumu**.

[![Dialoglodziņš Brīdinājuma nosacījuma izveide, kurā ir iestatīta opcijas Sūtīt e-pasta ziņojumu vērtība Jā](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)

> [!NOTE]
> Kad ir iestatīta opcijas **Sūtīt e-pasta ziņojumu** vērtība **Jā**, joprojām tiek piegādāti brīdinājumu paziņojumi no darbību centra.

## <a name="alert-notification-email-templates"></a>Brīdinājumu e-pasta paziņojumu veidnes

Pakalpojums nosūta e-pasta paziņojumus, izmantojot iepriekš definētas e-pasta ziņojumu veidnes, kas sniedz brīdinājuma paziņojuma pamatinformāciju. Šajā informācijā ir ietverta tieša saite uz lapu, kurā tika definēts brīdinājuma nosacījums.

Tālāk esošajā attēlā ir redzama pa e-pastu saņemto brīdinājumu paziņojumu struktūra.

[![Izmantojot veidni izveidotie brīdinājumu paziņojumi par ieraksta izveidi, lauka izmaiņām un veidnes dzēšanu](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)
