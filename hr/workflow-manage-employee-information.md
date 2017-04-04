---
title: "Izmantot darbplūsmas, lai pārvaldītu informāciju par darbiniekiem"
description: "Šajā tēmā ir paskaidrots, kā jūs varat izmantot darbplūsmu spēju cilvēkresursu, lai pārvaldītu informāciju par darbiniekiem. Piemēram, var saistīt ar amatu darbplūsmu un konfigurēt apstiprinājuma darbplūsmu, kas ir sākts, kad darbiniekiem mainīt savu ierakstu."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: a76ec0cd86bcc810b42ae3cd8efd8a584e6c4da3
ms.openlocfilehash: f286436aa4833babaeb3de875ee393d18e5f8eea
ms.lasthandoff: 03/31/2017


---

# <a name="use-workflows-to-manage-employee-information"></a>Izmantot darbplūsmas, lai pārvaldītu informāciju par darbiniekiem

Šajā tēmā ir paskaidrots, kā jūs varat izmantot darbplūsmu spēju cilvēkresursu, lai pārvaldītu informāciju par darbiniekiem. Piemēram, var saistīt ar amatu darbplūsmu un konfigurēt apstiprinājuma darbplūsmu, kas ir sākts, kad darbiniekiem mainīt savu ierakstu.

Spējas darbplūsmu cilvēkresursu nodrošina vairākas darbplūsmas cilvēkresursu darbību pārvaldībai. Turklāt daudzas opcijas ir pieejamas, lai varētu modificēt noteiktu darbplūsmas un saistīt tos ar ziņošanas hierarhiju. Darbplūsmas ir pieejamas, lai palīdzētu pārvaldīt izmaiņas standarta dažāda veida informācija par darbinieku. Darbplūsmu var saistīt ar amatu. Tad, ja darbinieki mainās viņu darbinieka ierakstu, darbplūsma ir sākts, kas prasa apstiprinājumu, pirms jaunā informācija tiek saglabāta. Šāda veida informāciju, kas palīdzēs jums efektīvi pārvaldīt izmaiņas un paturēt savu darbinieku dati precīzi definēts darbplūsmas:

-   Identifikācijas numuri
-   Kursi
-   Izglītība
-   Attēls
-   Patapinātie krājumi
-   Profesionālā pieredze
-   Projektu pieredze
-   Prasmes
-   Atbildīgie amati
-   Personāla vadības darbības
-   Kursu reģistrācija

Kad darbiniekiem ir spēkā, pārsūtīta vai pārtraukts, darbplūsmu var iekļaut pārskatīšanas procesā. Šādā veidā, var pārskatīt dokumentu vai darbības noteikumiem var definēt kā daļu no darbplūsmas. Pēc pārskatīšanas procesa pabeigšanas dokumentu vai darbību pabeigšanas un darbplūsmas pārvietojas galīgās apstiprināšanas solis.

## <a name="associate-a-workflow-with-a-position-hierarchy"></a>Saistītu darbplūsmu ar pozīciju hierarhijā
Darbplūsmu var saistīt ar hierarhija, kuras jūs konfigurējat. Piemēram, ja pozīcija ir saistīta ar ziņošanas hierarhijas matricu, var konfigurēt darbplūsmas, kas maršrutē izdevumus konkrētam projektam projekta izpildes vietā darbinieks, kurš ir saistīts ar šo pozīciju vadītāja. Izveidot jaunu darbplūsmu vai modificēt esošas darbplūsmas, par **cilvēkresursu darbplūsmas** lapu, noklikšķiniet uz **New**. Sarakstā sākt darbplūsmas noformētāju, atlasiet darbplūsmu. Varat izmantot izstrādes rīku, lai izveidotu jaunu darbplūsmu vai mainītu esošas darbplūsmas soļus. Mainot esošas darbplūsmas, izmaiņas tiek saglabātas kā jaunu versiju. Tādēļ, jūs vienmēr varat doties atpakaļ uz iepriekšējo versiju, ja jums ir.

## <a name="configure-a-human-resources-workflow"></a>Cilvēkresursu darbplūsmas konfigurēšana
Lai konfigurētu pamata darbplūsmas, kas ir sākts, kad darbinieki pieprasīt mainīt savu personīgo identifikācijas, rīkojieties šādi.

1.  Par **cilvēkresursu darbplūsmas** lapu, noklikšķiniet uz **New**.
2.  Pieejamo darbplūsmu sarakstā atlasiet **identifikācijas numurus**.
3.  Noklikšķiniet uz **palaist** sākt darbplūsmas noformētāju, un kad tiek parādīta uzvedne, ievadiet savu lietotāja vārdu un paroli.
4.  Vilkšanas **apstiprināt identifikācijas numuru** elementu no saraksta darbplūsmas elementu dizaineru audekls.
5.  Savienojumu elementu apstiprināšanas **sākt** un **pabeigt**.
6.  Veiciet dubultklikšķi uz **apstiprināt elementu**, un pēc tam noklikšķiniet ar peles labo pogu un izvēlieties **Properties**.
7.  Izpildiet šos soļus, kā pievienot darba vienumu instrukcijas:
    1.  Atlasiet **pielietojums**, un pēc tam atlasiet **hierarhijas** zem slodzes tips.
    2.  Zem **hierarhijas** atlase, atlasiet **konfigurējamas hierarhijas**.
    3.  Pievienojiet apturētas un aizveriet lappusi.

8.  Pabeigtu jebkuru papildu instrukcijas (bez papildu brīdinājumiem, ko vajadzētu pastāvēt).
9.  Noklikšķiniet uz **Saglabāt un aizvērt**. Aktivizēt jaunu darbplūsmu, ja dialoglodziņu atver un atlasiet **padarīt aktīvu**.
10. Dodieties uz **cilvēkresursu**&gt;**pozīcijas**&gt;**pozīciju hierarhijā tipi**.
11. Atlasiet **Matrix**.
12. Pievienot **darbinieka identifikācijas numurs** darbplūsmu sarakstam.



