---
title: ISO20022 pārvietošanai kredītā konfigurācijas importēšana
description: Šī procedūra parāda, kā importēt kreditora maksājuma elektronisko pārskatu veidošanas konfigurāciju.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4a96827bc6e126a7f5de6d67338b5233a65d93c8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840917"
---
# <a name="import-iso20022-credit-transfer-configuration"></a>ISO20022 pārvietošanai kredītā konfigurācijas importēšana

[!include [banner](../../includes/banner.md)]

Šī procedūra parāda, kā importēt kreditora maksājuma elektronisko pārskatu veidošanas konfigurāciju. Vācijas ISO 20022 kredīta pārskaitījuma formāts tiek izmantots kā piemērs. Šo procedūru var izmantot citiem pieejamajiem elektronisko pārskatu veidošanas formātiem. 

Šis uzdevums tika izveidots, izmantojot demonstrācijas datu uzņēmumu DEMF, bet jūs varat izmantot jebkuru demonstrācijas datu uzņēmumu, lai pabeigtu šo uzdevumu.

Šis ir pirmais no pieciem uzdevumus, kas kopumā parāda kreditoru maksājumu process, izmantojot elektronisko pārskatu veidošanas konfigurācijas. Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.

1. Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.
2. Sarakstā pieejamās konfigurācijas nodrošinātāji, atlasiet Microsoft.
3. Noklikšķiniet uz Iestatīt aktīvu.
4. Noklikšķiniet uz Repozitoriji.
5. Noklikšķiniet uz Atvērt.
6. Noklikšķiniet uz Rādīt filtrus.
7. Lietojiet šādus filtrus: Ievadiet filtrēšanas vērtību “ISO20022 kredīta pārskaitījums (DE)” laukā “Konfigurācijas nosaukums”, izmantojot “sākas ar” filtra operatoru
    * Vai atrodiet konfigurāciju sarakstā, atlasiet to un pārvietojiet to uz importa uzdevumu.  
8. Noklikšķiniet uz Importēt.
    * Ja poga Importēt nav pieejama, tas nozīmē, ka šī konfigurācija jau ir importēta.  
9. Noklikšķiniet uz Jā.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]