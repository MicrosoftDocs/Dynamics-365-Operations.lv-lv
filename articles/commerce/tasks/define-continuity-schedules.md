---
title: Nepārtrauktības grafiku definēšana
description: Šajā tēmā aprakstīts, kā iestatīt nepārtrauktības programmu (zināma arī kā atkārtošanās pasūtījumi).
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRContinuitySchedule, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 06fd1e23ad84fdc5e94e309717d5a96fbff45035
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414095"
---
# <a name="define-continuity-schedules"></a>Nepārtrauktības grafiku definēšana

[!include [banner](../includes/banner.md)]

Šajā tēmā aprakstīts, kā iestatīt nepārtrauktības programmu (zināma arī kā atkārtošanās pasūtījumi). Šajā tēmā tiek izmantoti uzņēmuma USRT demonstrācijas dati.


## <a name="create-continuity-program"></a>Nepārtrauktības programmas izveide
1. Dodieties uz Mazumtirdzniecība un komercija > Nepārtrauktība > Nepārtrauktības programmas.
2. Klikšķiniet Jauns.
3. Grafika ID laukā ierakstiet Nepārtrauktības grafika ID.
4. Laukā Pasūtījuma sākums atlasiet "Pirmais notikums".
    * Ja debitors nepārtrauktības programmā veic jaunu pasūtījumu, ir divas preces nosūtīšanas opcijas: 1. Pirmais notikums: tiek nosūtīta pirmā prece nepārtrauktības programmā.  2. Pašreizējais notikums: tiek nosūtīta pašreizējā prece. Piemēram, trīs mēnešus esot programmā, klients saņems trešo programmu.  
5. Atlasiet 'Jā', lai uzvedinātu pasūtījuma sākuma datumu.
6. Noklikšķiniet uz Pievienot rindu.
7. Laukā Krājuma numurs ievadiet krājuma numuru pirmajai precei ('0013').
8. Ierakstiet 'CP'.
9. Ievadiet datumu, kad pirmā prece būs pieejama pasūtījumam.
10. Noklikšķiniet uz Pievienot rindu.
11. Laukā Krājuma kods ierakstiet 0014.
12. Laukā Datumu intervāla kods, notīriet vērtību, lai lauks ir tukšs.
    * Lai veiktu šo procedūru, notīriet datumu intervālu. Jūs varat iestatīt datumu kā inkrementālu no pirmā vienuma sākuma datuma.  
13. Šeit var ievadīt intervālu, kādā preces tiek izsūtītas. Ierakstiet '30'.
    * Mēneša programmai, jums būs jāievada 30 dienu intervālu.  
14. Noklikšķiniet uz Pievienot rindu.
15. Laukā Krājuma kods ierakstiet 0015.
16. Ierakstiet 'Beigas'.
17. Noklikšķiniet uz Saglabāt.

## <a name="assign-to-continuity-item"></a>Piešķirt nepārtrauktības krājumam
1. Pārejiet uz sadaļu Preču informācijas pārvaldība > Preces > Izlaistās preces.
2. Atlasiet vienumu '0016'.
    * Lai veiktu šo procedūru, jums būs jāatlasa krājuma numuru 0016. Parasti Jums būs izveidota izlaista prece, kurai ir pielietota papildu nepārtrauktības biznesa loģika, ja tā ir izvietota pārdošanas pasūtījumā zvanu centrā.  
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
4. Noklikšķiniet uz Rediģēt.
5. Izvērsiet vai sakļaujiet sadaļu Pārdot.
6. Šeit jums jāievada nepārtrauktība programma, kuru pārstāv šis krājums. Ierakstiet Grafika ID, ko izveidojāt iepriekš.
    * Ja šī prece tiek pārdota zvanu centrā, papildu biznesa loģika tiek pielietota no atlasītās nepārtrauktības programmas.  
7. Noklikšķiniet uz Saglabāt.

