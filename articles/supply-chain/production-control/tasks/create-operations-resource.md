--- 
title: "Operācijas resursu izveide"
description: "Operācijas resurss izpilda projekta vai ražošanas procesa aktivitātes."
author: sorenva
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: aa80e4b22d116c8f580c9aefe7c114cfe1d19cc8
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---
# <a name="create-an-operations-resource"></a>Operācijas resursu izveide

[!include[task guide banner](../../includes/task-guide-banner.md)]

Operācijas resurss izpilda projekta vai ražošanas procesa aktivitātes. Šajā procedūras aprakstā ir paskaidrots, kā definēt operācijas resursu. Šo procedūru var izmēģināt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.

1. Dodieties uz Resursi.
2. Noklikšķiniet uz Jauns.
3. Laukā Resursi ierakstiet kādu vērtību.
4. Apraksta laukā ierakstiet vērtību.

## <a name="define-capacity-and-consumption-parameters"></a>Definēt noslodzes un patēriņa parametrus
1. Izvērsiet sadaļu Operācija.
2. Laukā Brāķis procentos ievadiet kādu skaitli.
3. Laukā Iestatīšanas kategorija ievadiet vai atlasiet kādu vērtību.
    * Norādiet izmaksu kategoriju, kas nosaka, kā uzskaitīt iestatīšanas izmaksas.  
4. Laukā Izpildlaiks ievadiet vai atlasiet kādu vērtību.
    * Norādiet izmaksu kategoriju, kas nosaka, kā uzskaitīt izpildes laika izmaksas.  
5. Laukā Daudzuma kategorija ievadiet vai atlasiet kādu vērtību.
    * Norādiet izmaksu kategoriju, kas nosaka, kā uzskaitīt resursu izmaksas, pamatojoties uz izstrādes daudzumu.  
6. Laukā Noslodzes vienība atlasiet kādu opciju.
    * Norādiet vienību, kādā izteikt operācijas resursa noslodzi.  
7. Laukā Noslodze ievadiet kādu skaitli.
8. Laukā Efektivitātes procenti ievadiet kādu skaitli.
    * Norādiet efektivitāti, kādu sagaidāt no šī operācijas resursa. Efektivitātes procentuālais daudzums pielāgo operācijas resursa caurlaidi un ietekmē resursam rezervēto laiku.  
9. Laukā Operāciju plānošanas procenti ievadiet kādu skaitli.
    * Norādiet maksimālo noslodzes procentuālo daudzumu tam operācijas resursam, kuru vēlaties izmantot operāciju plānošanā.  
10. Laukā Ierobežota noslodze atlasiet Jā.
    * Iestatiet šo opciju kā Jā, ja operācijas resurss ir jāplāno, pamatojoties uz faktiski pieejamo noslodzi, un ja ir jāņem vērā esošās noslodzes rezervācijas. Ja šī opcija ir iestatīta uz Nē, tad tiek pieņemts, ka operācijas resursam ir neierobežotā noslodze un resursam var tikt pārsniegta rezervācija.  
11. Laukā Deficīta resurss atlasiet Jā.

## <a name="define-working-times"></a>Definēt darba laikus
1. Izvērsiet sadaļu Kalendāri.
2. Noklikšķiniet uz Pievienot.
3. Laukā Kalendārs ievadiet vai atlasiet kādu vērtību.
    * Norādiet darba laika kalendāru, kas nosaka resursa noslodzi (stundās).  
4. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.

## <a name="define-resource-capabilities"></a>Resursu iespēju definēšana
1. Izvērsiet sadaļu Iespējas.
2. Noklikšķiniet uz Pievienot.
    * Iespēja ir operācijas resursu pieejamība konkrētas aktivitātes izpildīšanai. Plānošanas programma resursus piešķir, katras aktivitātes resursu pieprasījumus saskaņojot ar pieejamo operāciju resursu iespējām.  
3. Laukā Iespēja ievadiet vai atlasiet kādu vērtību.
4. Laukā Līmenis ievadiet kādu skaitli.
    * Norādiet prasmes līmeni, ar kādu šis resurss apstrādā iespēju.  
5. Laukā Prioritāte ievadiet kādu skaitli.
    * Norādiet operācijas resursa prioritāti attiecībā uz iespēju. Kad plānojat pēc prioritātes, vispirms tiek atlasīti operācijas resursi ar augstāko prioritāti (zemāko skaitlisko vērtību).  

## <a name="assign-resource-to-resource-group"></a>Piešķirt resursu kādai resursu grupai
1. Izvērsiet sadaļu Resursu grupas.
2. Noklikšķiniet uz Pievienot.
    * Resursu grupa operācijas resursiem nosaka vietu, ražošanas vienību un noliktavas kontekstu. Operācijas resursu var plānot tikai tad, ja tas ir piešķirts kādai resursu grupai, un tikai tajā vietā, kur šī resursu grupa atrodas.  
3. Laukā Resursu grupa ievadiet vai atlasiet kādu vērtību.
4. Laukā Ievades novietojums ievadiet vai atlasiet kādu vērtību.
    * Norādiet noliktavas novietojumu, no kura operācijas resurss patērē materiālus.  


