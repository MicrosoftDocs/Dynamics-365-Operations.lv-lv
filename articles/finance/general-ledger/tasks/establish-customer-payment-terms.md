---
title: Debitoru maksājumu nosacījumu izveide
description: Šī procedūra definē termiņatlaides un apmaksas datuma iestatījumus.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PaymDay, PaymTerm, CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f641d75e06b11ca325d2624f836fc2a7c92d69e4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445495"
---
# <a name="establish-customer-payment-terms"></a>Debitoru maksājumu nosacījumu izveide

[!include [banner](../../includes/banner.md)]

Šī procedūra definē termiņatlaides un apmaksas datuma iestatījumus. Šis uzdevuma ceļvedis izmanto USMF demonstrācijas uzņēmumu.

1. Pārejiet uz sadaļu **Navigācijas rūts > Moduļi > Debitori > Maksājumu iestatīšana > Maksājumu dienas**. **Apmaksas nosacījumu** ir kopīgi **Debitoriem** un **Kreditoriem**. Ja tos definējat modulī, tie būs pieejami arī citā modulī. Šajā uzdevumu ceļvedī visi apmaksas nosacījumi izveidoti sadaļā **Debitori**.
2. Klikšķiniet **Jauns**. Izveidojiet maksāšanas dienu, ja apmaksas nosacījumos ir prasīta konkrēta nedēļas diena (pirmdiena, otrdiena u.c.) vai konkrēts mēneša datums (5., 10. u.c.). 
3. Ievadiet ID laukā **Maksājuma diena**.
4. Laukā **Apraksts** ievadiet maksājuma dienas īsu aprakstu.
5. Laukā **Nedēļa/Mēnesis** atlasiet 'Nedēļa' vai 'Mēnesis'. Ja vēlaties ievadīt nedēļas dienu, piemēram, pirmdiena, atlasiet Nedēļa. Ja vēlaties ievadīt mēneša datumu, piemēram, 10., atlasiet Mēnesis. Šim piemēram atlasiet Mēnesis. 
6. Ievadiet datumu laukā **Mēneša diena**. Datums ir jāievada kā skaitlis, piemēram, "10", nevis "10‑ais". 
7. Noklikšķiniet uz **Saglabāt**.
8. Aizvērt lapu.
9. Pārejiet uz sadaļu **Navigācijas rūts > Moduļi > Debitori > Maksājumu iestatīšana > Maksājumu nosacījumi**.
10. Klikšķiniet **Jauns**. Apmaksas noteikumi tiek izmantoti, lai definētu, kā tiks aprēķināti apmaksas termiņi. Termiņatlaides datuma iestatīšana ir definēta atsevišķā lapā. 
11. Ievadiet ID laukā **Maksājuma nosacījumi**.
12. Ievadiet aprakstu laukā **Apraksts**.
13. Atlasiet **Maksāšanas metodi**, piemēram, SPB, neto, pašreizējais mēnesis utt. Maksāšanas metode tiek izmantota, lai definētu sākuma veidu, kā tiks aprēķināta apmaksājamā summa. Piemēram, neto tiek izmantots, ja apmaksas datums vienmēr ir noteikts mēnešu vai dienu skaits pēc rēķina datuma. SPB var izmantot, ja maksājums ir nepieciešams, saņemot rēķinu, tāpēc apmaksas datums netiek rēķināts. Šim piemēram atlasiet 'Pašreizējais mēnesis'.  
14. Ja aprēķinā iekļauta noteikta nedēļas diena vai datums, atlasiet **Maksājuma diena**. Atkarībā no maksāšanas termiņa var ievadīt daudzumu, norādot mēnešu vai dienu skaitu. Vai var izmantot **Maksājumu grafiku** vai **Maksājumu dienu**, kas jāpievieno maksāšanas metodes beigās. Ja apmaksas datums vienmēr ir nākamā mēneša 10. datums, atlasiet **Maksājumu dienu** 10. datumu. 
15. Noklikšķiniet uz **Saglabāt**.
16. Aizvērt lapu.
17. Pārejiet uz sadaļu **Debitori > Maksājumu iestatījumi > Termiņatlaides**.
18. Klikšķiniet **Jauns**. Šajā lapā tiek definēts, kā tiks aprēķināts termiņatlaides datums. 
19. Ievadiet ID laukā **Termiņatlaide**.
20. Ievadiet aprakstu laukā **Apraksts**.
21. Ja ir pieejama pa pakāpēm sadalīta termiņatlaide, atlasiet **Nākamais atlaižu kods**, kas ir attiecināms pēc šīs jaunās termiņatlaides.
22. Laukā **Dienas** ievadiet dienu skaitu, kas tiek aprēķināts termiņatlaides datumu. Ja ir atlasīts princips **Neto**, termiņatlaides datuma aprēķināšanai rēķina datumam tiks pieskaitīts noteikts dienu skaits.  
23. Laukā **Atlaides procenti** ievadiet termiņatlaidi procentos.
24. **Debitora atlaižu galvenajā kontā** ievadiet galveno kontu, kurā tiks grāmatota termiņatlaide debitora rēķiniem.
25. Atlasiet opciju laukā **Atlaides korespondējošie konti**. Atlasot Konti rēķina rindās, termiņatlaide tiks iegrāmatota tajā pašā līdzekļu/izdevumu galvenajā kontā, kurā kreditora rēķina rindas. Atlasot Kreditoru rēķiniem izmantot galveno kontu, termiņatlaide tiks iegrāmatota galvenajā kontā, kurš definēts laukā Kreditoru rēķinu galvenais konts. Šim piemēram izvēlieties 'Kreditoru rēķiniem izmantot galveno kontu'. 
26. Laukā **Kreditora atlaižu galvenais konts** ievadiet galveno kontu, kurā tiks grāmatota termiņatlaide kreditora rēķiniem.
27. Noklikšķiniet uz **Saglabāt**.

