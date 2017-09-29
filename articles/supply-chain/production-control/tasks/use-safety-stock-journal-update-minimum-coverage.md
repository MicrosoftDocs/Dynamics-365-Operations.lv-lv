--- 
title: "Drošības krājumu žurnāla lietošana, lai atjauninātu minimālo segumu"
description: "Šajā procedūrā ir parādīts, kā aprēķināt minimālā seguma priekšlikumus, pamatojoties uz vēsturiskām transakcijām, un pēc tam atjaunināt krājumu segumu, izmantojot priekšlikumus."
author: ChristianRytt
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 72b873faaee7bc86bd98f90ca2fb12a216d2f06b
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# Drošības krājumu žurnāla lietošana, lai atjauninātu minimālo segumu

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir parādīts, kā aprēķināt minimālā seguma priekšlikumus, pamatojoties uz vēsturiskām transakcijām, un pēc tam atjaunināt krājumu segumu, izmantojot priekšlikumus. Tas tiek darīts, izmantojot drošības krājumu žurnālu. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF. Šis uzdevums ir paredzēts ražošanas plānotājam, lai palīdzētu uzturēt minimālo segumu.


## Izveidot jaunu drošības krājumu žurnāla nosaukumu
1. Dodieties uz Drošības krājumu žurnālu nosaukumiem.
2. Noklikšķiniet uz Jauns.
3. Laukā Nosaukums ierakstiet “Materiāls”.
4. Laukā Apraksts ierakstiet “Materiāls”.
5. Aizvērt lapu.

## Izveidot drošības krājumu žurnālu
1. Dodieties uz Drošības krājumu aprēķins.
2. Noklikšķiniet uz Jauns.
3. Laukā Nosaukums ievadiet vai atlasiet kādu vērtību.
    * Atlasiet drošības krājumu žurnāla nosaukumu, kurus jūs izveidojāt, piemēram, Materiāls.  
4. Noklikšķiniet uz Izveidot rindas.
5. Ievadiet datumu laukā No datuma.
    * Iestatiet datumu uz “2015.01.02”.  
6. Laukā Līdz datumam ievadiet datumu.
    * Iestatiet datumu uz “2015.12.30”.  
7. Noklikšķiniet uz OK.
    * Šādi tiks izveidotas rindas tām dimensijām, kurām ir krājumu transakcijas.  

## Aprēķināt priekšlikumu
1. Noklikšķiniet uz Aprēķināt priekšlikumu.
2. Atlasiet opciju Izmantot vidējo izejas plūsmu izpildes laikā.
3. Vienumu Reizināšanas koeficients iestatiet uz “10”.
    * Reizināšanas koeficients tiek lietots, lai koriģētu priekšlikumu. Tā kā demonstrācijas datiem tikai dažas transakcijas, jums ir jāiestata šis koeficients, lai iegūtu reālistisku priekšlikumu.  
4. Noklikšķiniet uz OK.
    * Ritiniet uz leju, lai atrastu M0002 un M0003. Skatiet kolonnu Aprēķinātais minimālais daudzums.   

## Atjaunināt minimālo daudzumu
1. Laukā Jaunais minimālais daudzums ievadiet kādu skaitli.
    * Atjauniniet vērtību Jaunais minimālais daudzums, lai tā atbilstu vienuma Aprēķinātais minimālais daudzums vērtībai. Ja Aprēķinātais minimums ir nulle, varat ievadīt vēlamo nākotnes vērtību. Piemēram, šajā laukā varat ievadīt vērtību Aprēķinātais minimālais daudzums tādam M0002, kam ir noliktava 12.  
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Piemēram, varat atlasīt M0002, kam ir noliktava 12.  
3. Laukā Jaunais minimālais daudzums ievadiet kādu skaitli.
    * Atjauniniet vērtību Jaunais minimālais daudzums, lai tā atbilstu vienuma Aprēķinātais minimālais daudzums vērtībai. Ja Aprēķinātais minimums ir nulle, varat ievadīt vēlamo nākotnes vērtību.  

## Grāmatot jauno minimālo daudzumu un validēt rezultātu
1. Noklikšķiniet uz Grāmatot.
2. Noklikšķiniet uz OK.
3. Noklikšķiniet, lai sekotu saitei laukā Krājuma kods.
4. Noklikšķiniet, lai sekotu saitei laukā Krājuma kods.
5. Darbību rūtī noklikšķiniet uz Plānot.
6. Noklikšķiniet uz Krājumu vajadzība.
    * Ņemiet vērā, ka Minimālais daudzums ir atjaunināts ar jaunu minimālo daudzumu no drošības krājumu žurnāla.  

