---
title: Debitoru maksājumu nosacījumu izveide
description: Šī procedūra definē termiņatlaides un apmaksas datuma iestatījumus.
author: aprilolson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PaymDay, PaymTerm, CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6069d28d84ab1705fd62a33cea7e0b923f0e0705
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065714"
---
# <a name="establish-customer-payment-terms"></a>Debitoru maksājumu nosacījumu izveide

[!include [banner](../../includes/banner.md)]

Šī procedūra definē termiņatlaides un apmaksas datuma iestatījumus. Šis uzdevuma ceļvedis izmanto USMF demonstrācijas uzņēmumu.

1. Pārejiet uz sadaļu **Navigācijas rūts > Moduļi > Debitori > Maksājumu iestatīšana > Maksājumu dienas**. **Apmaksas nosacījumu** ir kopīgi **Debitoriem** un **Kreditoriem**. Ja tos definējat modulī, tie būs pieejami arī citā modulī. Šajā uzdevumu ceļvedī ir iestatīti visi debitoru parādu **maksāšanas** termiņi.
2. Klikšķiniet **Jauns**. Izveidojiet maksāšanas dienu, ja apmaksas nosacījumos ir prasīta konkrēta nedēļas diena (pirmdiena, otrdiena u.c.) vai konkrēts mēneša datums (5., 10. u.c.). 
3. Ievadiet ID laukā **Maksājuma diena**.
4. Laukā **Apraksts** ievadiet maksājuma dienas īsu aprakstu.
5. Laukā **Nedēļa/Mēnesis** atlasiet 'Nedēļa' vai 'Mēnesis'. Ja vēlaties ievadīt nedēļas dienu, piemēram, pirmdiena, atlasiet Nedēļa. Ja vēlaties ievadīt mēneša datumu, piemēram, 10., atlasiet Mēnesis. Šim piemēram atlasiet Mēnesis. 
6. Ievadiet datumu laukā **Mēneša diena**. Datums ir jāievada kā skaitlis, piemēram, "10", nevis "10‑ais". 
7. Noklikšķiniet uz **Saglabāt**.
8. Aizvērt lapu.
9. Pārejiet uz sadaļu **Navigācijas rūts > Moduļi > Debitori > Maksājumu iestatīšana > Maksājumu nosacījumi**.
10. Klikšķiniet **Jauns**. **Maksāšanas termiņi tiek** izmantoti, lai definētu, kā tiks aprēķināti apmaksas datumi. Termiņatlaides datuma iestatīšana ir definēta atsevišķā lapā. 
11. Ievadiet ID laukā **Maksājuma nosacījumi**.
12. Ievadiet aprakstu laukā **Apraksts**.
13. Izvēlieties maksājuma **metodi,** piemēram, SPB **·**, **Neto**, Pašreizējais **mēnesis u.c**. Maksājuma **metode tiek** izmantota, lai definētu sākuma laiku, kādā maksājums tiks aprēķināts. Piemēram, Neto **tiek** izmantots, ja apmaksas datums vienmēr ir mēnešu vai dienu skaits pēc rēķina datuma. **SPB** var izmantot, kad maksājums tiek pieprasīts pēc rēķina, tādējādi apmaksas datums netiek aprēķināts. Izvēlieties **Šo uzdevumu** ceļvedi šo mēnesi.  
14. Ja aprēķinā iekļauta noteikta nedēļas diena vai datums, atlasiet **Maksājuma diena**. Atkarībā no maksāšanas termiņa var ievadīt daudzumu, norādot mēnešu vai dienu skaitu. Vai arī jūs varat izmantot **Maksājumu** grafiku **vai Maksājuma** dienu, lai "pievienot" maksājuma metodes **beigās**. Ja apmaksas datums vienmēr ir nākamā mēneša 10. datums, atlasiet **Maksājumu dienu** 10. datumu. Ja izmantojat Maksājumu **kalendāru**, varat definēt, kā tiek noteikts izpildes datums, kad aprēķinātais datums no zemes ir uz ārpus darba dienas. Sākotnējo izpildes datumu aprēķina, izmantojot kalendārās dienas. Ja aprēķinātais datums nomā brīvdienā, varat koriģēt aprēķināto apmaksas datumu uz nākamo darba datumu vai agrāko darba dienu.
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
25. Atlasiet opciju laukā **Atlaides korespondējošie konti**. Atlasot Konti rēķina rindās, termiņatlaide tiks iegrāmatota tajā pašā līdzekļu/izdevumu galvenajā kontā, kurā kreditora rēķina rindas. Ja kreditoru rēķiniem **atlasīsit** opciju Izmantot galveno kontu, **termiņatlaide tiks grāmatota galvenajā kontā, kas tiek definēts kreditora rēķinu galvenajā kontā**. Šim piemēram izvēlieties Izmantot **galveno kontu kreditora rēķiniem**. 
26. Laukā **Kreditora atlaižu galvenais konts** ievadiet galveno kontu, kurā tiks grāmatota termiņatlaide kreditora rēķiniem.
27. Noklikšķiniet uz **Saglabāt**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
