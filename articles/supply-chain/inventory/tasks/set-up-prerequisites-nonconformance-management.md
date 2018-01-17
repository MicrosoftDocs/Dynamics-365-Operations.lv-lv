---
title: "Pārvaldības priekšnosacījumu iestatīšana"
description: "Izmantojiet šo procedūru, lai iespējotu neatbilstības pārvaldības procesus."
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 4bb4af7cb7aff101a8b9e6162823515f63b12886
ms.openlocfilehash: 9b5b05a3c00f093066a2714964bb99146427c3bc
ms.contentlocale: lv-lv
ms.lasthandoff: 11/02/2017

---
# <a name="set-up-prerequisites-for-management"></a>Pārvaldības priekšnosacījumu iestatīšana

[!include[task guide banner](../../includes/task-guide-banner.md)]

Izmantojiet šo procedūru, lai iespējotu neatbilstības pārvaldības procesus. Neatbilstība apraksta procedūru vai vienību, kam ir problēmas ar kvalitāti, kur aprakstošajā informācijā ietverts problēmas cēlonis un tips. Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati. Parasti šo procedūru veic kvalitātes pārvaldītājs.


## <a name="enable-quality-management-processes-within-the-company"></a>Iespējojiet uzņēmuma kvalitātes pārvaldības procesus
1. Pārejiet uz sadaļu Krājumu pārvaldība > Iestatījumi > Krājumu un noliktavas pārvaldības parametri.
2. Noklikšķiniet uz cilnes Kvalitātes pārvaldība.
3. Laukā Izmantot kvalitātes pārvaldību atlasiet Jā.
    * Atlasiet šo parametru, lai uzņēmumam iespējotu kvalitātes pārvaldības procesus.  
4. Ievadiet vērtību laukā Stundas likme.
    * Laukā Stundas likme ievadiet darbaspēka stundas likmi vietējā valūtā. Stundas likme tiek lietota, lai aprēķinātu izmaksas par operācijām, kas saistītas ar neatbilstību. Stundas nomināls un aprēķinātās izmaksas sniedz atsauces informāciju par neatbilstību un tās nemijiedarbojas ar citām funkcijām.  
5. Noklikšķiniet uz Pārskatu iestatījums.
    * Šajā lapā varat definēt kvalitātes pārskata piezīmju veidus, kas tiks izmantoti dažāda veida kvalitātes pārvaldības pārskatos.  
6. Aizvērt lapu.
7. Aizvērt lapu.

## <a name="enable-user-for-nonconformance-processing"></a>Iespējojiet lietotājam neatbilstību apstrādi.
1. Pārejiet uz sadaļu Sistēmas administrēšana > Lietotāji > Lietotāji.
    * Lai apstrādātu neatbilstības apstiprinājumu, lietotājam, kurš apstiprina vai noraida neatbilstību, lapā Lietotāji jābūt piešķirtai vērtībai "Nosaukums". Lai lietotu dokumentu piezīmes, lietotājam jābūt aktivizētai Dokumentu apstrāde lietotāja opcijās.  
2. Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus. Piemēram, filtrējiet pēc lauka Nosaukums, izmantojot vērtību "Ricardo".
    * Izmantojiet filtru, lai atrastu lietotāju, kurš apstiprinās vai noraidīs neatbilstības ierakstus.  
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Lai apstrādātu neatbilstības apstiprinājumu, lietotājam, kurš apstiprina vai noraida neatbilstību, lapā Lietotāji jābūt piešķirtai vērtībai "Nosaukums".  
4. Noklikšķiniet uz Lietotāja opcijas.
5. Noklikšķiniet uz cilnes Preferences.
6. Laukā Iespējot dokumenta apstrādi atlasiet Jā.
    * Lai lietotu dokumentu piezīmes, lietotājam jābūt aktivizētai Dokumentu apstrāde lietotāja opcijās.  
7. Aizvērt lapu.
8. Aizvērt lapu.
9. Aizvērt lapu.

## <a name="define-diagnostic-types-for-nonconformance-processing"></a>Definējiet diagnostikas tipus neatbilstības apstrādei
1. Dodieties uz Krājumu vadība > Iestatīšana > Kvalitātes pārvaldība > Diagnostikas tipi.
    * Izmantojiet lapu Diagnostikas tipi, lai definētu diagnostikas darbību klasifikāciju. Izlabošana identificē, kāda tipa diagnostikas darbības jāizdara apstiprinātajā neatbilstībā, kuram tas jāizpilda un pieprasītās un plānotās izpildes datumu.  
2. Noklikšķiniet uz Jauns.
3. Ierakstiet vērtību Diagnostikas laukā.
4. Apraksta laukā ierakstiet vērtību.
5. Aizvērt lapu.

## <a name="define-quality-charges-for-nonconformance-processing"></a>Definējiet kvalitātes maksas neatbilstības apstrādei
1. Dodieties uz Krājumu vadība > Iestatīšana > Kvalitātes pārvaldība > Kvalitātes maksas.
    * Izmantojiet kvalitātes maksas lapu, lai definētu maksu klasifikāciju, kas tiks izmantota darbībām, kas saistītas ar neatbilstībām.  
2. Noklikšķiniet uz Jauns.
3. Laukā Maksu kods ierakstiet kādu vērtību.
4. Apraksta laukā ierakstiet vērtību.
5. Aizvērt lapu.

## <a name="define-the-operations-for-nonconformance-processing"></a>Definējiet operācijas neatbilstības apstrādei
1. Dodieties uz Krājumu vadība > Iestatīšana > Kvalitātes pārvaldība > Operācijas.
    * Izmantojiet lapu Operācijas, lai definētu klasifikāciju darbam, ko var veikt apstiprinātajai neatbilstībai. Ja piešķirat saistīto darbību neatbilstībai, varat definēt detalizētu informāciju par saistīto materiālu, darba stundām, un dažādām papildmaksām, kas nepieciešami operācijas izpildei. Šī informācija sniedz pamatu izvērtēto izmaksu aprēķināšanas operāciju veikšanai.  
2. Noklikšķiniet uz Jauns.
3. Ierakstiet vērtību laukā Operācijas.
4. Apraksta laukā ierakstiet vērtību.
5. Aizvērt lapu.

## <a name="define-problem-types-for-nonconformance-processing"></a>Definējiet problēmu tipus neatbilstības apstrādei
1. Dodieties uz Krājumu vadība > Iestatīšana > Kvalitātes pārvaldība > Problēmu tipi.
    * Izmantojiet lapu Problēmtipi, lai definētu to kvalitātes problēmu klasifikāciju, kas rodas dažādiem neatbilstības veidiem. Neatbilstības veidi: Iekšējais, Debitora, Kreditora, Pakalpojuma pieprasījuma, Ražošanas un Līdzprodukta ražošanas. Viens problēmas veids var būt saistīts ar vairākiem neatbilstības veidiem.  
2. Noklikšķiniet uz Jauns.
3. Ierakstiet vērtību laukā Problēmas tips.
4. Apraksta laukā ierakstiet vērtību.
5. Noklikšķiniet uz Neatbilstības tipi.
    * Izmantojiet lapu Neatbilstības tipi, lai autorizētu problēmas veida, kas jāizmanto vienam vai vairākiem neatbilstības veidiem. Piemēram, problēmas veids, kas attiecas uz defekta kodu, var attiekties uz visiem neatbilstības veidiem, turpretī problēmas veids saistībā ar debitora sūdzībām var attiekties tikai uz debitora un pakalpojuma pieprasījuma neatbilstības veidiem.  
6. Noklikšķiniet uz Jauns.
7. Sarakstā atzīmējiet atlasīto rindu.
8. Atlasiet opciju laukā Neatbilstības tips.
9. Aizvērt lapu.
10. Aizvērt lapu.

## <a name="define-quarantine-zones-for-nonconformance-processing"></a>Definējiet karantīnas zonas neatbilstības apstrādei
1. Dodieties uz Krājumu vadība > Iestatīšana > Kvalitātes pārvaldība > Karantīnas zonas.
2. Noklikšķiniet uz Jauns.
3. Ierakstiet vērtību laukā Karantīnas zona.
4. Apraksta laukā ierakstiet vērtību.
5. Aizvērt lapu.

