---
title: Iestatīt priekšnosacījumus neatbilstības pārvaldībai
description: Izmantojiet šo tēmu, lai iespējotu neatbilstības pārvaldības procesus.
author: perlynne
manager: AnnBe
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, SysUserManagement, SysUserSetup, InventTestDiagnosticType, InventTestMiscCharges, InventTestOperation, InventProblemType, InventProblemTypeSetup, InventQuarantineZone
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dfd0bc7edb3236d016e64bd08b1858fd7b12417f
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145736"
---
# <a name="set-up-prerequisites-for-nonconformance-management"></a>Iestatīt priekšnosacījumus neatbilstības pārvaldībai

[!include [banner](../../includes/banner.md)]

Izmantojiet šo tēmu, lai iespējotu neatbilstības pārvaldības procesus. Neatbilstība apraksta procedūru vai vienību, kam ir problēmas ar kvalitāti, kur aprakstošajā informācijā ietverts problēmas cēlonis un tips. Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati. Parasti šo procedūru veic kvalitātes pārvaldītājs.


## <a name="enable-quality-management-processes-within-the-company"></a>Iespējojiet uzņēmuma kvalitātes pārvaldības procesus
1. Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Noliktavas vadība > Iestatīšana > Krājumu un noliktavas pārvaldības parametri**.
2. Atlasiet cilmi **Kvalitātes pārvaldība**.
3. Atlasiet **Jā** laukā **Izmantot kvalitātes pārvaldību**, lai aktivizētu uzņēmuma kvalitātes pārvaldības procesus.
4. Laukā **Stundas likme** ievadiet skaitli vietējā valūtā. Stundas likme tiek lietota, lai aprēķinātu izmaksas par operācijām, kas saistītas ar neatbilstību. Stundas nomināls un aprēķinātās izmaksas sniedz atsauces informāciju par neatbilstību un tās nemijiedarbojas ar citām funkcijām.  
5. Atlasiet **Pārskata iestatīšana**, lai definētu kvalitātes pārskata piezīmju tipus, kas tiks izmantoti dažāda veida kvalitātes pārvaldības pārskatos.

## <a name="enable-user-for-nonconformance-processing"></a>Iespējojiet lietotājam neatbilstību apstrādi.
1. Navigācijas rūtī dodieties uz **Moduļi > Sistēmas administrēšana > Lietotāji > Lietotāji**. 
2. Izmantojiet ātro filtru, lai atrastu lietotāju, kurš apstiprinās vai noraidīs neatbilstības ierakstus. Piemēram, filtrējiet pēc lauka **Nosaukums**, izmantojot `Ricardo` vērtību. Lai apstrādātu neatbilstības apstiprinājumu, lietotājam, kurš apstiprina vai noraida neatbilstības, lapā **Lietotāji** ir jābūt piešķirtai vērtībai "Nosaukums". Lai lietotu dokumentu piezīmes, lietotājam jābūt aktivizētai Dokumentu apstrāde lietotāja opcijās.  
3. Atzīmējiet vēlamā ieraksta rindu.
4. Atlasiet **Lietotāja opcijas**.
5. Atlasiet cilni **Preferences**.
6. Laukā **Iespējot dokumenta apstrādi** atlasiet **Jā**.

## <a name="define-diagnostic-types-for-nonconformance-processing"></a>Definējiet diagnostikas tipus neatbilstības apstrādei
1. Navigācijas rūtī dodieties uz **Moduļi > Krājumu vadība > Iestatīšana > Kvalitātes vadība > Diagnostikas veidi**. Izmantojiet lapu **Diagnostikas tipi**, lai definētu diagnostikas darbību klasifikāciju. Izlabošana identificē, kāda tipa diagnostikas darbības jāizdara apstiprinātajā neatbilstībā, kuram tas jāizpilda un pieprasītās un plānotās izpildes datumu.  
2. Atlasiet **Jauns**.
3. Ierakstiet vērtību laukā **Diagnostika**.
4. Laukā **Apraksts** ierakstiet kādu vērtību.

## <a name="define-quality-charges-for-nonconformance-processing"></a>Definējiet kvalitātes maksas neatbilstības apstrādei
1. Navigācijas rūtī dodieties uz **Moduļi > Krājumu vadība > Iestatīšana > Kvalitātes vadība > Kvalitātes maksas**. Izmantojiet lapu **Kvalitātes maksas**, lai definētu maksu klasifikāciju, kas tiks izmantota darbībām, kas saistītas ar neatbilstībām.  
2. Atlasiet **Jauns**.
3. Laukā **Maksu kods** ierakstiet kādu vērtību.
4. Laukā **Apraksts** ierakstiet kādu vērtību.

## <a name="define-the-operations-for-nonconformance-processing"></a>Definējiet operācijas neatbilstības apstrādei
1. Navigācijas rūtī dodieties uz **Moduļi > Krājumu vadība > Iestatīšana > Kvalitātes vadība > Operācijas**. Izmantojiet lapu **Operācijas**, lai definētu klasifikāciju darbam, ko var veikt apstiprinātajai neatbilstībai. Ja piešķirat saistīto darbību neatbilstībai, varat definēt detalizētu informāciju par saistīto materiālu, darba stundām, un dažādām papildmaksām, kas nepieciešami operācijas izpildei. Šī informācija sniedz pamatu izvērtēto izmaksu aprēķināšanas operāciju veikšanai.  
2. Atlasiet **Jauns**.
3. Ierakstiet vērtību laukā **Operācijas**.
4. Laukā **Apraksts** ierakstiet kādu vērtību.

## <a name="define-problem-types-for-nonconformance-processing"></a>Definējiet problēmu tipus neatbilstības apstrādei
1. Navigācijas rūtī dodieties uz **Moduļi > Krājumu vadība > Iestatīšana > Kvalitātes vadība > Problēmu veidi**. Izmantojiet lapu **Problēmu veidi**, lai definētu to kvalitātes problēmu klasifikāciju, kas rodas dažādiem neatbilstības veidiem. Neatbilstības veidi: **Iekšējais**, **Klienta**, **Kreditora**, **Pakalpojuma pieprasījuma**, **Ražošanas** un **Līdzprodukta ražošanas**. Viens problēmas veids var būt saistīts ar vairākiem neatbilstības veidiem.  
2. Atlasiet **Jauns**.
3. Ierakstiet vērtību laukā **Problēmas veids**.
4. Laukā **Apraksts** ierakstiet kādu vērtību.
5. Atlasiet **Neatbilstības veidi**. Izmantojiet lapu **Neatbilstības veidi**, lai autorizētu problēmas veida, kas jāizmanto vienam vai vairākiem neatbilstības veidiem. Piemēram, problēmas veids, kas attiecas uz defekta kodu, var attiekties uz visiem neatbilstības veidiem, turpretī problēmas veids saistībā ar debitora sūdzībām var attiekties tikai uz debitora un pakalpojuma pieprasījuma neatbilstības veidiem.  
6. Atlasiet **Jauns**.
7. Jaunās rindas laukā **Neatbilstības veids** atlasiet opciju.

## <a name="define-quarantine-zones-for-nonconformance-processing"></a>Definējiet karantīnas zonas neatbilstības apstrādei
1. Navigācijas rūtī dodieties uz **Moduļi > Krājumu vadība > Iestatīšana > Kvalitātes vadība > Karantīnas zonas**.
2. Atlasiet **Jauns**.
3. Ierakstiet vērtību laukā **Karantīnas zona**.
4. Laukā **Apraksts** ierakstiet kādu vērtību.
5. Aizvērt lapu.

