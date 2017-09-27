---
title: "Neatbilstības pārvaldība"
description: "Šajā rakstā ir aprakstīts pamata iestatīšana, kas ir nepieciešama, lai lietotu neatbilstības. Papildu iestatīšana ir nepieciešama, ja vēlaties izmantot kvalitātes pārbaudes pasūtījumus."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 28951
ms.assetid: a62d4ba8-eebc-4b14-b587-630be7298522
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 7a6f7c12ab5fe5e67ffb844c1dbc6cd688ecd4d5
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---

# <a name="nonconformance-management"></a>Neatbilstības pārvaldība

[!include[banner](../includes/banner.md)]


Šajā rakstā ir aprakstīts pamata iestatīšana, kas ir nepieciešama, lai lietotu neatbilstības. Papildu iestatīšana ir nepieciešama, ja vēlaties izmantot kvalitātes pārbaudes pasūtījumus.

Lai iespējotu neatbilstības pārvaldību, izpildiet tālāk aprakstītās darbības.

1.  Definējiet krājuma un noliktavas pārvaldības parametrus, kas ir saistīti ar neatbilstībām.
    -   Opcijai **Izmantot kvalitātes pārvaldību** iestatiet **Jā**.
    -   Laukā **Stundas likme** ievadiet darbaspēka stundas likmi vietējā valūtā. Stundas likme tiek lietota, lai aprēķinātu izmaksas operācijām, kas ir saistītas ar neatbilstību. Stundas likme un aprēķinātās izmaksas nodrošina atsauces informāciju par neatbilstību. Šie vienumi nemijiedarbojas ar citām funkcijām.
    -   Lai definētu drukājamā dokumenta tipu, izmantojiet cilni **Kvalitātes pārvaldība** lapā **Pārskatu iestatīšana**. Varat drukāt neatbilstības pārskatu, neatbilstības atzīmi vai labojumu pārskatu. Dažādu dokumenta tipu iedrukāšanai pārskatā var definēta vairāk nekā vienu ierakstu, vai iekšēju vai ārēju paziņojumu drukāšanai. Var būt lietderīgi izmantot lapu **Dokumenta veids**, lai neatbilstībām un labojumiem definētu unikālus dokumentu veidus. Piemēram, ievadiet piezīmes par neatbilstību, izmantojot unikālu neatbilstību dokumenta veidu. Šajā gadījumā unikālo dokumenta veidu norādiet pārskata opcijās.
    -   Iespējojiet neatbilstības un labošanas atsauču numuru sērijas.

2.  Iespējojiet neatbilstībām lietotāja apstiprināšanu. Izmantojiet lapas **Lietotāji** lauku **Nosaukums**, lai piešķirtu darbinieku katram lietotājam, kuram ir jāapstiprina neatbilstība. Sistēma izmanto darbiniekus, kuri maina neatbilstības statusu, lai izsekotu neatbilstības vēsturi. Lietotāji var apstiprināt neatbilstību tikai tad, ja viņiem ir piešķirts darbinieka identifikators.
3.  Definējiet problēmu veidus, kas tiks piešķirti neatbilstībām. Izmantojiet lapu **Problēmtipi**, lai definētu to kvalitātes problēmu klasifikāciju, kas rodas dažādiem neatbilstības veidiem. Varar iestatīt šādus neatbilstības veidus: **Iekšējais**, **Debitora**, **Kreditora**, **Pakalpojuma pieprasījuma**, **Ražošanas** un **Līdzprodukta ražošanas**. Izmantojiet lapu **Neatbilstības tipi**, lai autorizētu problēmas veidu, kas jāizmanto vienam vai vairākiem neatbilstības veidiem. Piemēram, problēmas veids, kas attiecas uz defekta kodu, var attiekties uz visiem neatbilstības veidiem, turpretī problēmas veids, kas attiecas uz debitora sūdzībām, var attiekties tikai uz neatbilstības veidu **Debitors** un **Pakalpojuma pieprasījums**.
4.  Definējiet karantīnas zonas, lai nodrošinātu norādījumus par rīcību ar defektīviem materiāliem. Izmantojiet lapu **Karantīnas zonas**, lai definētu zonas, ko var piešķirt neatbilstībai. Izdrukāta neatbilstības atzīme parādīs piešķirto karantīnas zonu un informāciju par lietojumu, lai sniegtu norādījumus par defektīvu materiālu apstrādi. Zonas var atbilst krājumu vietām vai operāciju resursiem.
5.  Definējiet diagnostikas veidus, kas tiks piešķirti labojumiem. Izmantojiet lapu **Diagnostikas tipi**, lai definētu diagnostikas darbību klasifikāciju. Labojumā norāda, kāda veida diagnostikas darbība jāveic attiecībā uz apstiprināto neatbilstību un kam tā ir jāveic. Tajā norāda arī pieprasīto un plānotais pabeigšanas datumu.
6.  Definējiet saistītās operācijas, kas tiks piešķirtas neatbilstībām. Izmantojiet lapu **Operācijas**, lai definētu klasifikāciju darbam, ko var veikt apstiprinātajai neatbilstībai. Ja neatbilstībai piešķirat saistīto operāciju, varat nodrošināt detalizētu informāciju, piemēram, par saistīto materiālu, darba stundām un dažādām papildmaksām, kas nepieciešamas operācijas izpildē. Šī informācija tiek izmantota, lai operācijai aprēķinātu novērtētās izmaksas. Detalizētā informācija un novērtētās izmaksas tiek nodrošinātas tikai atsauces nolūkā. Kvalitātes saistītās operācijas ir atšķirīgas no operācijām, ko var definēt ražošanas maršrutā.


<a name="see-also"></a>Skatiet arī
--------

[Neatbilstības izveide un apstrāde (uzdevuma ceļvedis)](/dynamics365/unified-operations/supply-chain/inventory/tasks/create-process-non-conformance)

[Kvalitātes pārvaldības procesi](quality-management-processes.md)

[Priekšnosacījumu iestatīšana neatbilstības pārvaldībai (uzdevuma ceļvedis)](/dynamics365/unified-operations/supply-chain/inventory/tasks/set-up-prerequisites-nonconformance-management)
