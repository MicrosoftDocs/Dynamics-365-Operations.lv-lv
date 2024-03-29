---
title: Pārskatu ģenerēšana, pievienojot saturu kā neapstrādātu XML
description: Varat noformēt elektronisko pārskatu (Electronic Reporting — ER) formātus, kas izejošos dokumentus ģenerē XML formātā.
author: kfend
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.openlocfilehash: 87b70d5893d71e5022205a2f39f8263edf6d5280
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277548"
---
# <a name="generate-reports-by-adding-content-as-raw-xml"></a>Pārskatu ģenerēšana, pievienojot saturu kā neapstrādātu XML

[!include[banner](../includes/banner.md)]

Varat izmantot jauno **RAW XML** formāta elementu, lai noformētu elektronisko pārskatu (Electronic Reporting — ER) formātus, kas izejošos dokumentus ģenerē XML formātā. Reizēm jums var būt nepieciešams šiem pārskatiem pievienot neapstrādātus XML datus viena vai vairāku tālāk norādīto iemeslu dēļ.

- Neapstrādātos XML ir ērtāk izmantot pārskata sākotnējam noformējumam un turpmākai uzturēšanai, jo XML struktūru var ģenerēt automātiski, izpildot izpildlaika izteiksmi. Tādēļ noformēšanas laikā nav nepieciešams noteikt vairākus saistījumus vairākiem formāta elementiem. Tas ir iespējams, kad jūsu izmantotie datu avoti ietver informāciju, kuru var izmantot, lai izveidotu XML elementus, kamēr tiek ģenerēts pārskats.
- Nevar izmantot nevienu citu metodi, lai pārskatu aizpildītu ar XML saturu, kas sistēmā tika saņemts un saglabāts iepriekš. Piemēram, ģenerētajai XML atbildei, iespējams, ir jāietver saturs no kāda iepriekš sūtīta XML pieprasījuma.
- Nevienu citu metodi nevar izmantot, lai ģenerētajā dokumentā ievietotu rakstzīmes, pamatojoties uz to ciparu kodiem. Dažām valodām un rakstzīmēm šāda tipa kodi nepastāv. Kā piemēru varētu minēt grieķu alfabēta burtu ro (ρ) un tādus HTML entītijas kodus kā \&eacute; tādam burtam *e*, kam tiek izmantota diakritiskā zīme “akūts” (é).

> [!NOTE]
> Ņemiet vērā, ka šī struktūra nekontrolē to, vai XML saturs, kurš tiek ievietots ģenerētajā dokumentā, izmantojot **RAW XML** formāta elementu, ir pareizs.

Lai par šo līdzekli uzzinātu vairāk, noskatieties uzdevumu ceļvežus **ER Neapstrādātu XML datu izmantošana XML pārskatu ģenerēšanai (1. daļa. Datu modeļa noformēšana)** un **ER Neapstrādātu XML datu izmantošana XML pārskatu ģenerēšanai (2. daļa. Pārskata noformēšana un palaišana)**, kuri veido daļu no biznesa procesa **7.5.4.3 IT pakalpojumu/risinājumu komponentu iegāde/izstrāde (10677)** un kurus var lejupielādēt no [Microsoft lejupielādes centra](https://go.microsoft.com/fwlink/?linkid=874684). Šajos uzdevumu ceļvežos ir izklāstīts ER formāta konfigurēšanas process neapstrādātu XML datu ievietošanai ģenerētajos failos.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
