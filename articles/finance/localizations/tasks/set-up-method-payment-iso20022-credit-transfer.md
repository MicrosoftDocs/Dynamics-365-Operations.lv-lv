---
title: Maksājuma metodes iestatīšana ISO20022 pārvietošanai kredītā
description: Šajā procedūrā parādīts, kā iestatīt kreditoru maksājumu metodes ISO20022 kredīta pārsūtīšanai vai kādam citam maksāšanas veidam, izmantojot elektronisko pārskatu veidošanu, lai ģenerētu failu.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8bb54864c8d0a57510b4d47b00aed60c5be95512
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174954"
---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a>Maksājuma metodes iestatīšana ISO20022 pārvietošanai kredītā

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā parādīts, kā iestatīt kreditoru maksājumu metodes ISO20022 kredīta pārsūtīšanai vai kādam citam maksāšanas veidam, izmantojot elektronisko pārskatu veidošanu, lai ģenerētu failu. 

Pirms uzdevuma pabeigšanas, ir jāiestata eksporta formāta konfigurācijas un maksājumu konti.

Šajā uzdevumā izmantots demonstrācijas datu uzņēmums DEMF.

Šī ir trešā procedūra no piecām, kas parāda kreditoru maksājumu procesu, izmantojot elektronisko pārskatu veidošanas konfigurāciju. Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.

1. Pārejiet uz sadaļu Kreditori > Maksājuma iestatījumi > Maksāšanas metodes.
2. Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus. Piemēram, filtrējiet pēc lauka Maksāšanas metodes, izmantojot vērtību SEPA CT.
3. Noklikšķiniet uz Rediģēt.
4. Laukā Periods atlasiet vērtību Kopā.
5. Laukā Maksājuma veids atlasiet Elektronisks maksājums.
6. Izvērsiet sadaļu Failu formāti.
7. Laukā Vispārīga elektronisko pārskatu veidošana atlasiet Jā.
8. Ievadiet vai atlasiet vērtību laukā Eksporta formāta konfigurācija.
    * Sarakstā atlasiet vērtību ISO20022 pārvietošana kredītā (DE). Ja saraksts ir tukšs, tas nozīmē, ka nav importēta un aktīva kreditora maksājuma eksporta formāta konfigurācija.  
9. Laukā Konta tips atlasiet Banka.
10. Laukā Maksājumu konts norādiet vērtības DEMF OPER.
11. Noklikšķiniet uz Saglabāt.
