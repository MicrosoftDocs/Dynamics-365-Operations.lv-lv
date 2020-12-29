---
title: Numura zīmes uzlīmes drukāšanas iespējošana
description: Šajā tēmā parādīts, kā iespējot seriālā pārvadāšanas konteinera koda (SSCC) marķējuma drukāšanu pēc tam, kad pēdējais vienums ir izņemts no inventāra pārdošanas pavadzīmju darba procesā.
author: perlynne
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e548e5e5528733412d47478dd740b87217cdac2
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4433135"
---
# <a name="enable-license-plate-label-printing"></a>Numura zīmes uzlīmes drukāšanas iespējošana

[!include [banner](../../includes/banner.md)]

Šajā tēmā parādīts, kā iespējot seriālā pārvadāšanas konteinera koda (SSCC) marķējuma drukāšanu pēc tam, kad pēdējais vienums ir izņemts no inventāra pārdošanas pavadzīmju darba procesā. Šo procedūru varat palaist demonstrācijas datu uzņēmumā USMF. Ja to palaižat, izmantojot pats savus datus, jums numura zīmei ir nepieciešama iestatīta numuru sērija. Pirms sākat šo uzdevumu, ir jāiestata etiķešu printeris. Dodieties uz Organizācijas administrēšana > Iestatīšana > Tīkla printeri. Darbību rūtī noklikšķiniet uz Opcijas un pēc tam noklikšķiniet uz pogas Lejupielādēt dokumentu maršrutēšanas aģenta instalētāju. Pirms turpiniet šīs procedūras izpildi, palaidiet instalētāju un pārliecinieties, ka strādājošs tīkla printeris ir iestatīts kā Aktīvs.


## <a name="set-up-the-gs1-company-prefix"></a>Iestatīt GS1 uzņēmuma prefiksu
1. Dodieties uz **Navigācijas rūts > Moduļi > Noliktavas vadība > Iestatīšana> Noliktavas vadības parametri**.
2. Laukā **GS1 uzņēmuma prefikss** ievadiet sava GS1 uzņēmuma numura 7 ciparus.
3. Atlasiet **Saglabāt**.
4. Aizvērt lapu.

## <a name="setup-the-sscc-license-plate-number-sequence"></a>SPKK unikālā noliktavas vienības identifikatora virknes iestatīšana
1. Pārejiet uz **Navigācijas rūts > Moduļi > Organizācijas administrēšana > Numuru sērijas > Numuru sērijas**.
2. Laukā **Apgabals** atlasiet opciju.
3. Laukā **Atsauce** atlasiet opciju.
4. Laukā **Uzņēmums** ievadiet vērtību. 
5. Izvērsiet sadaļu **Segmenti**.
6. Atlasiet **Rediģēt**.
7. Tabulā **Segmenti** atlasiet pirmo rindu
8. Atlasiet **Noņemt**.
9. Atlasiet **Noņemt**.
10. Atlasiet **Saglabāt**.
11. Aizvērt lapu.

## <a name="create-the-document-route-layout"></a>Izveidot dokumentu maršruta izkārtojumu
1. Dodieties uz **Navigācijas rūts > Moduļi > Noliktavas vadība > Iestatīšana> Dokumentu maršrutēšana > Dokumentu maršrutēšanas izkārtojumi**. Iespējojiet SPKK izkārtojumu.  
2. Atlasiet **Jauns**.
3. Laukā **Izkārtojuma ID** ievadiet vērtību. 
4. Laukā **Apraksts** ierakstiet kādu vērtību.
5. Atlasiet **Ievadīt teksta beigās**.
6. Atlasiet **Saglabāt**.
7. Aizvērt lapu.

## <a name="set-up-the-document-routing"></a>Iestatīt dokumentu maršrutēšanu
1. Dodieties uz **Navigācijas rūts > Moduļi > Noliktavas vadība > Iestatīšana> Dokumentu maršrutēšana > Dokumentu maršrutēšana**.
2. Laukā **Darba pasūtījuma tips** atlasiet opciju.
3. Atlasiet **Jauns**.
4. Laukā **Noliktava** atlasiet vērtību.
5. Laukā **Nosaukums** ierakstiet kādu vērtību.
6. Atlasiet **Jauns**.
7. Laukā **Izkārtojuma ID** ievadiet vai atlasiet vērtību.
8. Laukā **Nosaukums** ievadiet tā printera nosaukumu, kuru vēlaties lietot.
9. Atlasiet **Saglabāt**.
10. Aizvērt lapu.

## <a name="create-mobile-device-menu"></a>Izveidot mobilās ierīces izvēlni
1. Dodieties uz **Navigācijas rūts > Moduļi > Noliktavas vadība > Iestatīšana > Mobilā ierīce > Mobilās ierīces izvēlne**.
2. Atlasiet **Jauns**.
3. Laukā **Izvēlnes vienuma nosaukums** ievadiet vērtību.
4. Laukā **Nosaukums** ievadiet vērtību. 
5. Laukā **Režīms** atlasiet opciju.
6. Atlasiet **Jā** laukā **Izmantot esošo darbu**.
7. Atlasiet **Jā** laukā **Ģenerēt licences numura zīmi**.
8. Izvērtiet sadaļu **Darba klases**.
9. Atlasiet **Jauns**.
10. Laukā **Darba klases ID** ievadiet vērtību.
11. Atlasiet **Saglabāt**.
12. Aizvērt lapu.
13. Dodieties uz **Navigācijas rūts > Moduļi > Noliktavas vadība > Iestatīšana > Mobilā ierīce > Mobilās ierīces izvēlne**.
14. Kokā atlasiet to izvēlnes vienumu, kuru izveidojāt iepriekš.
15. Atlasiet **Rediģēt**.
16. Atlasiet bultu, lai izvēlnei pievienotu izvēlnes vienumu.
17. Atlasiet **Saglabāt**.
18. Aizvērt lapu.

## <a name="update-a-work-template"></a>Atjaunināt darba veidni
1. Dodieties uz **Navigācijas rūts > Moduļi > Noliktavas vadība > Iestatīšana> Darbs > Darba veidnes**.
2. Atlasiet **Rediģēt**.
3. Atlasiet **Jauns**.
4. Laukā **Darba tips** atlasiet **Drukāt**.
5. Laukā **Darba klases ID** ievadiet vai atlasiet vērtību.
6. Atlasiet **Pārvietot uz augšu**.
7. Atlasiet **Saglabāt**.
8. Aizvērt lapu.

