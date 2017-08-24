--- 
title: "Numura zīmes uzlīmes drukāšanas iespējošana"
description: "Šī procedūra ļauj veikt seriālā pārvadāšanas konteinera koda (SPKK) etiķetes automātisko drukāšanu, kad pārdošanas izdošanas darba procesā pēdējais krājums ir izdots no krājumiem."
author: perlynne
manager: AnnBe
ms.date: 11/03/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: c4ca3cd02a43692cfa9510847b460a318855fd24
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="enable-license-plate-label-printing"></a>Numura zīmes uzlīmes drukāšanas iespējošana

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šī procedūra ļauj veikt seriālā pārvadāšanas konteinera koda (SPKK) etiķetes automātisko drukāšanu, kad pārdošanas izdošanas darba procesā pēdējais krājums ir izdots no krājumiem. Šo procedūru varat palaist demonstrācijas datu uzņēmumā USMF. Ja to palaižat, izmantojot pats savus datus, jums numura zīmei ir nepieciešama iestatīta numuru sērija. Pirms sākat šo uzdevumu, ir jāiestata etiķešu printeris. Dodieties uz Organizācijas administrēšana > Iestatīšana > Tīkla printeri. Darbību rūtī noklikšķiniet uz Opcijas un pēc tam noklikšķiniet uz pogas Lejupielādēt dokumentu maršrutēšanas aģenta instalētāju. Pirms turpiniet šīs procedūras izpildi, palaidiet instalētāju un pārliecinieties, ka strādājošs tīkla printeris ir iestatīts kā Aktīvs.


## <a name="set-up-the-gs1-company-prefix"></a>Iestatīt GS1 uzņēmuma prefiksu
1. Doties uz Noliktavas vadība > Iestatīšana > Noliktavas pārvaldības parametri.
2. Laukā GS1 uzņēmuma prefikss ievadiet 7 skaitļus savam GS1 uzņēmuma numuram.
3. Noklikšķiniet uz Saglabāt.
4. Aizvērt lapu.

## <a name="setup-the-sscc-license-plate-number-sequence"></a>SPKK unikālā noliktavas vienības identifikatora virknes iestatīšana
1. Pārejiet uz sadaļu Organizācijas administrēšana > Numuru secība > Numuru secība.
2. Laukā Apgabals atlasiet kādu opciju.
3. Laukā Atsauce atlasiet kādu opciju.
4. Laukā Uzņēmums ierakstiet kādu vērtību.
5. Sarakstā atzīmējiet atlasīto rindu.
6. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
7. Izvērsiet sadaļu Segmenti.
8. Noklikšķiniet uz Rediģēt.
9. Tabulā Segmenti atlasiet pirmo rindu
10. Noklikšķiniet uz Noņemt.
11. Noklikšķiniet uz Noņemt.
12. Noklikšķiniet uz Saglabāt.
13. Aizvērt lapu.

## <a name="create-the-document-route-layout"></a>Izveidot dokumentu maršruta izkārtojumu
1. Doties uz Noliktavas vadība > Iestatīšana > Dokumentu maršrutēšana > Dokumentu maršrutēšanas izkārtojumi.
    * Iespējojiet SPKK izkārtojumu.  
2. Noklikšķiniet uz Jauns.
3. Laukā Izkārtojuma ID ierakstiet kādu vērtību.
4. Apraksta laukā ierakstiet vērtību.
5. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
6. Noklikšķiniet uz Ievietot teksta beigās.
7. Noklikšķiniet uz Saglabāt.
8. Aizvērt lapu.

## <a name="set-up-the-document-routing"></a>Iestatīt dokumentu maršrutēšanu
1. Doties uz Noliktavas vadība > Iestatīšana > Dokumentu maršrutēšana > Dokumentu maršrutēšana.
2. Laukā Darba pasūtījuma tips atlasiet kādu opciju.
3. Klikšķiniet Jauns.
4. Laukā Noliktava ierakstiet kādu vērtību.
5. Laukā Nosaukums ierakstiet kādu vērtību.
6. Klikšķiniet Jauns.
7. Laukā Izkārtojuma ID ievadiet vai atlasiet kādu vērtību.
8. Laukā Nosaukums ievadiet tā printera nosaukumu, kuru vēlaties izmantot.
9. Noklikšķiniet uz Saglabāt.
10. Aizvērt lapu.

## <a name="create-mobile-device-menu"></a>Izveidot mobilās ierīces izvēlni
1. Dodieties uz Noliktavas vadība > Iestatīšana > Mobilā ierīce > Mobilās ierīces izvēlnes vienumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Izvēlnes vienuma nosaukums ierakstiet kādu vērtību.
4. Laukā Virsraksts ierakstiet kādu vērtību.
5. Laukā Režīms atlasiet kādu opciju.
6. Laukā Izmantot esošo darbu atlasiet Jā.
7. Laukā Ģenerēt numura zīmi atlasiet Jā.
8. Izvērsiet sadaļu Darba klases.
9. Noklikšķiniet uz Jauns.
10. Laukā Darba klases ID ierakstiet kādu vērtību.
11. Noklikšķiniet uz Saglabāt.
12. Aizvērt lapu.
13. Dodieties uz Noliktavas vadība > Iestatīšana > Mobilā ierīce > Mobilās ierīces izvēlne.
14. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
15. Koka struktūrā atlasiet “Koka struktūrā atlasiet iepriekš izveidoto izvēlnes vienumu.”.
16. Noklikšķiniet uz Rediģēt.
17. Noklikšķiniet uz bultiņas, lai šo izvēlnes vienumu pievienotu izvēlnei.
18. Noklikšķiniet uz Saglabāt.
19. Aizvērt lapu.

## <a name="update-a-work-template"></a>Atjaunināt darba veidni
1. Doties uz Noliktavas vadība > Iestatīšana > Darbs > Darbu veidnes.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
3. Noklikšķiniet uz Rediģēt.
4. Klikšķiniet Jauns.
5. Sarakstā atzīmējiet atlasīto rindu.
6. Laukā Darba tips atlasiet vienumu “Drukāt”.
7. Laukā Darba klases ID ievadiet vai atlasiet kādu vērtību.
8. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
9. Noklikšķiniet uz Pārvietot uz augšu.
10. Noklikšķiniet uz Saglabāt.
11. Aizvērt lapu.


