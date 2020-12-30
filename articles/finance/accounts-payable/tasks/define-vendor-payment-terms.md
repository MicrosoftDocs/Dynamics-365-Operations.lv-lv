---
title: Kreditora maksājumu nosacījumu definēšana
description: Šajā tēmā ir izskaidrots, kā iestatīt kreditoru rēķinu apmaksas nosacījumus.
author: abruer
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7e6778f61a9367399e4b71d5b2bb2459c09ba508
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445428"
---
# <a name="define-vendor-payment-terms"></a>Kreditora maksājumu nosacījumu definēšana

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir izskaidrots, kā iestatīt kreditoru rēķinu apmaksas nosacījumus. Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.

1. Pārejiet uz sadaļu **Navigācijas rūts > Moduļi > Kreditori > Maksājuma iestatīšana > Apmaksas nosacījumi**.
2. Atlasiet **Jauns**. Lapa Apmaksas noteikumi tiek izmantota, lai definētu, kā tiks aprēķināts apmaksas termiņš. Tā netiek izmantota, lai definētu, kā tiks aprēķināts termiņatlaides datums.  
3. Ierakstiet vērtību laukā **Apmaksas nosacījumi**.
4. Laukā **Apraksts** ierakstiet vērtību.
5. Ievadiet skaitli laukā **Dienas**. Šeit ievadītais skaitlis tiks izmantots, lai to pieskaitītu apmaksas datumam vai maksāšanas metodē norādītā perioda beigām. Piemēram, ja atlasāt **Neto**, skaitlis tiks pieskaitīts apmaksas datumam. Ja atlasāt **Pašreizējais mēnesis**, aprēķinot apmaksas datumu, skaitlis tiks pieskaitīts pašreizējā mēneša pēdējai dienai.  
6. Atlasiet **Saglabāt**.
7. Aizvērt lapu.
8. Pārejiet uz sadaļu **Kreditori > Maksājuma iestatīšana > Termiņatlaides**.
9. Atlasiet **Jauns**.
10. Ievadiet ID laukā **Termiņatlaide**.
11. Laukā **Apraksts** ierakstiet kādu vērtību.
12. Ja kreditors piedāvā diferencētas atlaides, atlasiet nākamo termiņatlaidi, kas stājas spēkā, kad pašreizējā vairs nav spēkā.
13. Aizvērt lapu.
14. Ievadiet skaitli laukā **Dienas**. Daudzums, kas ievadīts laukā **Dienas**, tiks izmantots, lai aprēķinātu termiņatlaides datumu, pamatojoties uz opciju, kas atlasīta laukā **Neto/Pašreizējais**. Ja ir atlasīts **Neto**, termiņatlaides datuma aprēķināšanai dienu daudzums tiks pieskaitīts rēķina datumam. Ja ir atlasīts **Pašreizējais mēnesis**, termiņatlaides datuma aprēķināšanai dienu daudzums tiks pieskaitīts pašreizējā mēneša beigām.  
15. Laukā **Atlaide** ievadiet termiņatlaidi procentos. 
16. Ievadiet galveno kontu, kurā tiks iegrāmatota termiņatlaide debitoru rēķiniem, pēc tam ievadiet galveno kontu, kurā tiks iegrāmatota termiņatlaide kreditoru rēķiniem. Ja lauka **Atlaižu korespondējošie konti** vērtība ir **Kreditoru atlaidēm izmantot galveno kontu**, tiks izmantots galvenais konts. Ja ir izvēlēta opcija **Konti rēķina rindās**, termiņatlaide tiks iegrāmatota līdzekļu/izdevumu kontos, kuri izmantoti rēķina rindās.  
17. Atlasiet **Saglabāt**.

