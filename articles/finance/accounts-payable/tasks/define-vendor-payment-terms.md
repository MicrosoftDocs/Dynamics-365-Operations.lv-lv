---
title: Kreditora maksājumu nosacījumu definēšana
description: Šajā rakstā ir izskaidrots, kā iestatīt apmaksas nosacījumus kreditoru rēķiniem.
author: abruer
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a676856ed43bf1b78684eac0682e0fdef9c84083
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906476"
---
# <a name="define-vendor-payment-terms"></a>Kreditora maksājumu nosacījumu definēšana

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir izskaidrots, kā iestatīt apmaksas nosacījumus kreditoru rēķiniem. Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.

1. Pārejiet uz sadaļu **Navigācijas rūts > Moduļi > Kreditori > Maksājuma iestatīšana > Apmaksas nosacījumi**.
2. Atlasiet **Jauns**. Maksājuma **nosacījumu lapa tiek** izmantota, lai definētu, kā tiks aprēķināts izpildes datums. Tā netiek izmantota, lai definētu, kā tiks aprēķināts termiņatlaides datums.  
3. Ierakstiet vērtību laukā **Apmaksas nosacījumi**.
4. Laukā **Apraksts** ierakstiet vērtību.
5. Ievadiet skaitli laukā **Dienas**. Šeit ievadītais numurs tiks izmantots, lai pievienotu apmaksas datumam vai maksājuma metodē identificētā perioda **beigām**. Piemēram, ja atlasāt **Neto**, skaitlis tiks pieskaitīts apmaksas datumam. Ja atlasāt **Pašreizējais mēnesis**, aprēķinot apmaksas datumu, skaitlis tiks pieskaitīts pašreizējā mēneša pēdējai dienai.  
6. Atlasiet **Saglabāt**.
7. Aizvērt lapu.
8. Pārejiet uz sadaļu **Kreditori > Maksājuma iestatīšana > Termiņatlaides**.
9. Atlasiet **Jauns**.
10. Ievadiet ID laukā **Termiņatlaide**.
11. Laukā **Apraksts** ierakstiet kādu vērtību.
12. Ja kreditors piedāvā diferencētas atlaides, atlasiet nākamo termiņatlaidi, kas stājas spēkā, kad pašreizējā vairs nav spēkā.
13. Aizvērt lapu.
14. Ievadiet skaitli laukā **Dienas**. Laukā Dienas ievadītais **daudzums** tiks **izmantots**, lai aprēķinātu termiņatlaides datumu, pamatojoties uz to, kāda opcija tika atlasīta **laukā Neto/Pašreizējais**. Ja ir atlasīts **Neto**, termiņatlaides datuma aprēķināšanai dienu daudzums tiks pieskaitīts rēķina datumam. Ja ir atlasīts **Pašreizējais mēnesis**, termiņatlaides datuma aprēķināšanai dienu daudzums tiks pieskaitīts pašreizējā mēneša beigām.  
15. Laukā **Atlaide** ievadiet termiņatlaidi procentos. 
16. Ievadiet galveno kontu, kurā tiks iegrāmatota termiņatlaide debitoru rēķiniem, pēc tam ievadiet galveno kontu, kurā tiks iegrāmatota termiņatlaide kreditoru rēķiniem. Ja lauka **Atlaižu korespondējošie konti** vērtība ir **Kreditoru atlaidēm izmantot galveno kontu**, tiks izmantots galvenais konts. Ja ir izvēlēta opcija **Konti rēķina rindās**, termiņatlaide tiks iegrāmatota līdzekļu/izdevumu kontos, kuri izmantoti rēķina rindās.  
17. Atlasiet **Saglabāt**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
