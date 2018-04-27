--- 
title: "Debitoru maksājumu nosacījumu izveide"
description: "Šī procedūra definē termiņatlaides un apmaksas datuma iestatījumus."
author: aprilolson
manager: AnnBe
ms.date: 10/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ef3cad6538d9efbd1c1881f4b7d771382d9b1ba8
ms.openlocfilehash: 04b45508047d26ef7c08ede5862be75835783ef5
ms.contentlocale: lv-lv
ms.lasthandoff: 10/26/2017

---
# <a name="establish-customer-payment-terms"></a>Debitoru maksājumu nosacījumu izveide

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Šī procedūra definē termiņatlaides un apmaksas datuma iestatījumus. Šis uzdevuma ceļvedis izmanto USMF demonstrācijas uzņēmumu.

1. Pārejiet uz sadaļu Debitori > Maksājumu iestatījumi > Maksāšanas dienas.
    * Apmaksas nosacījumu iestatījumi ir kopīgi debitoru parādos un parādos kreditoriem. Ja tos definējat modulī, tie būs pieejami arī citā modulī. Šajā uzdevumu ceļvedī visi apmaksas nosacījumi izveidoti debitoru parādiem.  
2. Noklikšķiniet uz Jauns.
    * Izveidojiet maksāšanas dienu, ja apmaksas nosacījumos ir prasīta konkrēta nedēļas diena (pirmdiena, otrdiena u.c.) vai konkrēts mēneša datums (5., 10. u.c.).  
3. Laukā Maksājuma diena ievadiet maksājuma dienas ID.
4. Laukā Apraksts ievadiet maksājuma dienas īsu aprakstu.
5. Laukā Nedēļa/Mēnesis atlasiet Nedēļa vai Mēnesis.
    * Ja vēlaties ievadīt nedēļas dienu, piemēram, pirmdiena, atlasiet Nedēļa. Ja vēlaties ievadīt mēneša datumu, piemēram, 10., atlasiet Mēnesis. Šim piemēram atlasiet Mēnesis.  
6. Ievadiet datumu laukā Mēneša diena.
    * Datums ir jāievada kā skaitlis, piemēram, "10", nevis "10‑ais".  
7. Noklikšķiniet uz Saglabāt.
8. Aizvērt lapu.
9. Pārejiet uz sadaļu Debitori > Maksājumu iestatījumi > Apmaksas nosacījumi.
10. Noklikšķiniet uz Jauns.
    * Apmaksas noteikumi tiek izmantoti, lai definētu, kā tiks aprēķināti apmaksas termiņi. Termiņatlaides datuma iestatīšana ir definēta atsevišķā lapā.  
11. Laukā Apmaksas nosacījumi ievadiet ID.
12. Ievadiet aprakstu laukā Apraksts.
13. Atlasiet maksāšanas metodi, piemēram, COD, neto, pašreizējā mēnesī u.c.
    * Maksāšanas metode tiek izmantota, lai definētu, kā tiks aprēķināts apmaksas termiņa sākums.  Piemēram, neto tiek izmantots, ja apmaksas datums vienmēr ir noteikts mēnešu vai dienu skaits pēc rēķina datuma. SPB var izmantot, ja maksājums ir nepieciešams, saņemot rēķinu, tāpēc apmaksas datums netiek rēķināts. Šim piemēram atlasiet Pašreizējais mēnesis.  
14. Ja aprēķinā iekļauta noteikta nedēļas diena vai datums, atlasiet maksāšanas dienu.
    * Atkarībā no maksāšanas termiņa var ievadīt daudzumu, norādot mēnešu vai dienu skaitu. Vai var izmantot maksāšanas grafiku vai maksāšanas dienu, kas jāpievieno maksāšanas metodes beigās. Ja apmaksas datums vienmēr ir nākamā mēneša 10. datums, atlasiet maksāšanas dienu 10. datumu.  
15. Noklikšķiniet uz Saglabāt.
16. Aizvērt lapu.
17. Pārejiet uz sadaļu Debitori > Maksājumu iestatījumi > Termiņatlaides.
18. Noklikšķiniet uz Jauns.
    * Šajā lapā tiek definēts, kā tiks aprēķināts termiņatlaides datums.  
19. Laukā Termiņatlaide ievadiet ID.
20. Ievadiet aprakstu laukā Apraksts.
21. Ja ir pieejama pa pakāpēm sadalīta termiņatlaide, atlasiet nākamo atlaižu kodu, kas ir attiecināms pēc šīs jaunās termiņatlaides.
22. Ievadiet dienu skaitu, ko izmanto, lai aprēķinātu termiņatlaides datumu.
    * Ja ir atlasīts neto princips, termiņatlaides datuma aprēķināšanai rēķina datumam tiks pieskaitīts noteikts dienu skaits.  
23. Ievadiet termiņatlaides procentuālo daļu.
24. Ievadiet galveno kontu, kurā jāgrāmato debitoru rēķinu termiņatlaide.
25. Atlasiet opciju laukā Atlaides korespondējošie konti.
    * Atlasot Konti rēķina rindās, termiņatlaide tiks iegrāmatota tajā pašā līdzekļu/izdevumu galvenajā kontā, kurā kreditora rēķina rindas. Atlasot Kreditoru rēķiniem izmantot galveno kontu, termiņatlaide tiks iegrāmatota galvenajā kontā, kurš definēts laukā Kreditoru rēķinu galvenais konts. Šim piemēram izvēlieties Kreditoru rēķiniem izmantot galveno kontu.  
26. Ievadiet galveno kontu, kurā jāgrāmato kreditoru rēķinu termiņatlaide.
27. Noklikšķiniet uz Saglabāt.


