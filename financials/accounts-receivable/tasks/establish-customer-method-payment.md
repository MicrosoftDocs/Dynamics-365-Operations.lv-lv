--- 
title: "Debitoru maksājuma metodes izveide"
description: "Izveidojiet maksāšanas metodi debitoru maksājumiem."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: bfafcccb12112ca7cceefb65be3f942bfc307751
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="establish-customer-method-of-payment"></a>Debitoru maksājuma metodes izveide

[!include[task guide banner](../../includes/task-guide-banner.md)]

Izveidojiet maksāšanas metodi debitoru maksājumiem. Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.

1. Pārejiet uz sadaļu Debitori > Maksājumu iestatījumi > Maksāšanas metodes.
2. Noklikšķiniet uz Jauns.
3. Laukā Maksāšanas metode ievadiet maksāšanas metodes ID.
    * Maksājuma metodes ID tiek attēlots rēķinos un maksājumos, tāpēc pārliecinieties, ka tas ir pietiekami aprakstošs, lai saprastu, kāda veida maksājums tiek ierakstīts un kurā bankas kontā.  
4. Ievadiet aprakstu laukā Apraksts.
5. Atlasiet, kāds maksājuma statuss ir nepieciešams, lai iegrāmatotu maksājumus.
    * Veidojot debitora maksājumu, to var iegrāmatot tikai tad, ja maksājuma statuss atbilst šeit definētajam maksājuma statusam.  
6. Atlasiet, kā veidot debitoru maksājumus rēķiniem.
    * Šī opcija tiek izmantota tikai izpildot maksājuma priekšlikumu. Maksājuma priekšlikumu var izmantot debitoru maksājumiem, veicot tiešo debetu un velkot līdzekļus no klientu bankas kontiem.  
7. Atlasiet maksājuma tipu.
    * Pēc maksājuma tipa var noteikt, vai maksājumam tiks vai netiks veiktas dažādas pārbaudes.  
8. Atlasiet, uz kādu konta tipu maksājumi tiks grāmatoti.
    * Parasti šai opcijai jāatlasa Banka.  
9. Atlasiet bankas kontu, kurā šis maksājums tiks ierakstīts.
10. Ievadiet Bankas transakcijas tipu, lai identificētu jūsu bankas izmantoto maksājuma tipu.
    * Bankas saskaņošanas procesā tiek izmantots bankas transakcijas tips, kas var atvieglot saskaņošanu.  
11. Atlasiet, vai šis maksājums īslaicīgi tiks grāmatots pagaidu kontā.
    * Vai vēlaties pārbaudīt laiku, kurā maksājums tiek apstrādāts bankā, izmantojiet pagaidu funkcionalitāti. Maksājums tiks īslaicīgi iegrāmatots Virsgrāmatas kontā, līdz to apstrādās banka un maksājums tiks pārvietots uz šeit definēto bankas kontu.  
12. Ievadiet galveno kontu, kas tiks izmantots pagaidu grāmatošanai.
    * Šis ir galvenais konts, kurā maksājumu uz laiku iegrāmato, ja izmantojat pagaidu funkcionalitāti.  
13. Izmantojiet cilni Faila formāts, lai definētu elektronisko maksājumu iestatījumus.
14. Izmantojiet cilni Maksājumu kontrole, lai definētu obligātos laukus.
    * Piemēram, ja vēlaties, lai visi šīs maksāšanas metodes maksājumi tiktu deponēti, varat izvēlēties šo opciju šajā cilnē.  
15. Izmantojiet cilni Maksājumu atribūti, lai definētu maksājuma atribūtus, kurus vēlaties izmantot šai maksāšanas metodei.
16. Noklikšķiniet uz Saglabāt.


