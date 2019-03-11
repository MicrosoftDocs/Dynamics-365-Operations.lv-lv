---
title: Kreditora maksājumu nosacījumu definēšana
description: Iestatiet kreditoru rēķinu apmaksas nosacījumus.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 68c69d5be5ccbdfb17fea7c61121cbf26fee48d4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "358558"
---
# <a name="define-vendor-payment-terms"></a>Kreditora maksājumu nosacījumu definēšana

[!include [task guide banner](../../includes/task-guide-banner.md)]

Iestatiet kreditoru rēķinu apmaksas nosacījumus. Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.

1. Pārejiet uz sadaļu Kreditori > Maksājuma iestatījumi > Apmaksas nosacījumi.
2. Noklikšķiniet uz Jauns.
    * Lapa Apmaksas noteikumi tiek izmantota, lai definētu, kā tiks aprēķināts apmaksas termiņš. Tā netiek izmantota, lai definētu, kā tiks aprēķināts termiņatlaides datums.  
3. Ierakstiet vērtību laukā Apmaksas nosacījumi.
4. Apraksta laukā ierakstiet vērtību.
5. Ievadiet skaitli laukā Dienas.
    * Šeit ievadītais skaitlis tiks izmantots, lai to pieskaitītu apmaksas datumam vai maksāšanas metodē norādītā perioda beigām. Piemēram, ja atlasāt neto, skaitlis tiks pieskaitīts apmaksas datumam. Ja atlasāt pašreizējo mēnesi, aprēķinot apmaksas datumu, skaitlis tiks pieskaitīts pašreizējā mēneša pēdējai dienai.  
6. Noklikšķiniet uz Saglabāt.
7. Aizvērt lapu.
8. Pārejiet uz sadaļu Kreditori > Maksājuma iestatījumi > Termiņatlaides.
9. Noklikšķiniet uz Jauns.
10. Ievadiet ID laukā Termiņatlaide.
11. Apraksta laukā ierakstiet vērtību.
12. Ja kreditors piedāvā diferencētas atlaides, atlasiet nākamo termiņatlaidi, kas stājas spēkā, kad pašreizējā vairs nav spēkā.
13. Aizvērt lapu.
14. Ievadiet skaitli laukā Dienas.
    * Daudzums, kas ievadīts laukā Dienas, tiks izmantots, lai aprēķinātu termiņatlaides datumu, pamatojoties uz opciju, kas atlasīta laukā Neto/Pašreizējais. Ja ir atlasīts neto, termiņatlaides datuma aprēķināšanai dienu daudzums tiks pieskaitīts rēķina datumam. Ja ir atlasīts pašreizējais mēnesis, termiņatlaides datuma aprēķināšanai dienu daudzums tiks pieskaitīts pašreizējā mēneša beigām.  
15. Laukā Atlaide ievadiet termiņatlaidi procentos. 
16. Ievadiet galveno kontu, kurā jāgrāmato debitoru rēķinu termiņatlaide.
17. Ievadiet galveno kontu, kurā jāgrāmato kreditora rēķinu termiņatlaide.
    * Ja lauka Atlaižu korespondējošie konti vērtība ir Kreditoru atlaidēm izmantot galveno kontu, tiks izmantots galvenais konts.  Ja ir izvēlēta opcija Konti rēķina rindās, termiņatlaide tiks iegrāmatota līdzekļu/izdevumu kontos, kuri izmantoti rēķina rindās.  
18. Noklikšķiniet uz Saglabāt.

