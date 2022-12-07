---
title: Periodu žurnālu grāmatošana
description: Periodiskos žurnālus reizēm sauc par cikliski atkārtotajiem žurnāliem, jo summa, teksts un cita informācija tiek atkārtoti katru reizi, kad šis periodiskais žurnāls tiek izgūts.
author: aprilolson
ms.date: 11/21/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransPeriodic, LedgerJournalTransDaily
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bdc1d9f67a515e3cdc45e173b88982feceb0ebfd
ms.sourcegitcommit: fb9b6969218f2b82f0a4c72bfad75387fe00395c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/22/2022
ms.locfileid: "9799391"
---
# <a name="post-periodic-journals"></a>Periodu žurnālu grāmatošana

[!include [banner](../../includes/banner.md)]

Periodiskos žurnālus reizēm sauc par cikliski atkārtotajiem žurnāliem, jo summa, teksts un cita informācija tiek atkārtoti katru reizi, kad šis periodiskais žurnāls tiek izgūts. Kad veidojat periodisko žurnālu, norādiet atkārtošanās perioda intervālu, piemēram, dienas vai mēnešus. Šajā uzdevuma ceļvedī tiks izveidots periodisks žurnāls ar atkārtošanos katru mēnesi.

1. Dodieties uz **Navigācijas rūts > Moduļi > Virsgrāmata > Periodiski uzdevumi > Periodiskie žurnāli**.
2. Klikšķiniet **Jauns**.
3. Ievadiet vai atlasiet vērtību laukā **Nosaukums**.
4. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
5. Laukā **Apraksts** ierakstiet kādu vērtību. Šis apraksts būs periodiskā žurnāla nosaukums, kad tas vēlāk tiks izgūts, tāpēc nodrošiniet, lai tam tiktu piešķirts piemērots nosaukums.
6. **Darbību rūtī** noklikšķiniet uz **Rindas**. Periodiskā žurnālā parasti ir ietvertas vairākas žurnāla rindas. Tomēr šī uzdevumu rokasgrāmata pievienos tikai vienu rindu.
7. Laukā **Datums** ievadiet datumu. Laukā **Datums** ir norādīts grāmatošanas datums nākamajai pārsūtīšanai uz ikdienas žurnālu. Žurnāliem, kas tiks izgūti katru mēnesi, ir ieteicams izmantot datumu mēnesī, kad tas tiks grāmatots. Parasti tas ir perioda pirmais vai pēdējais datums. Lauka Tukšs **datums** izmantošana var atstāt lauku **Datums** tukšu un norādīt datumu, kad žurnāls tiek izgūts. Lauks tiks atjaunināts uz nākamo periodisko datumu, kad darbības tiks izgūtas. 
8. Laukā **Konts** norādiet vēlamās vērtības.
9. Laukā **Apraksts** ievadiet vai atlasiet kādu vērtību.
10. Aizvērt lapu.
11. Laukā **Debets** ievadiet kādu skaitli.
12. Laukā **Korespondējošais konts** norādiet vēlamās vērtības.
13. Laukā **Vienība** atlasiet vērtību **Mēneši**.
14. Laukā **Vienību skaits** ievadiet **1**.
15. Laukā **Pēdējais datums** ievadiet kādu datumu. Ievadot iepriekšējā perioda pēdējo datumu, tiek novērsta iespēja, ka periodiskais žurnāls nejauši tiek izveidots nepareizajā sākuma periodā. Vēlāk pēdējais datums tiks atjaunināts katru reizi, kad periodiskais žurnāls tiek izgūts. 
16. Noklikšķiniet uz **Saglabāt**.
17. Ejiet uz **Navigācijas rūts > Moduļi > Virsgrāmata > Žurnāla ieraksti > Vispārējie žurnāli**.
18. Klikšķiniet **Jauns**.
19. Ievadiet vai atlasiet vērtību laukā **Nosaukums**.
20. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
21. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
22. Laukā **Apraksts** ierakstiet kādu vērtību.
23. **Darbību rūtī** noklikšķiniet uz **Rindas**.
24. **Darbību rūtī** noklikšķiniet uz **Periodisko darbību žurnāls**.
25. Noklikšķiniet uz **Izgūt žurnālu**.
26. Ievadiet datumu laukā **Līdz datumam**. Vienums **Līdz datumam** darbojas kā robeždatums attiecībā uz periodiskajām dokumentu rindām. Pamatojoties uz periodiskuma iestatījumu, **pēdējais datums un**  **datums Līdz** datumam to pašu rindu var iekļaut vairāk nekā vienu reizi iegūtajā žurnālā. Datums **Līdz tiek** automātiski atjaunināts, pamatojoties uz sesijas datumu pēdējai reizei, kad periodiskā rinda tika pārsūtīta uz žurnālu. 
27. Laukā **Periodiskāo darbību žurnāla numurs** ievadiet vai atlasiet kādu vērtību.
28. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
29. Noklikšķiniet uz **Labi**. Tagad periodisko darbību žurnālu var pārskatīt, apstiprināt vai grāmatot atkarībā no pieprasījuma un iestatījumiem.   


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
