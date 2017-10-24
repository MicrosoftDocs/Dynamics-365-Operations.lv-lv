--- 
title: "Starpuzņēmumu plāna izveide"
description: "Šajā procedūrā ir aprakstīts, kā izveidot starpuzņēmuma plānu."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: da186f7ad74bb607fd6e7220d77c2f414789f29c
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="create-an-intercompany-plan"></a>Starpuzņēmumu plāna izveide

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir aprakstīts, kā izveidot starpuzņēmuma plānu. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.


## <a name="set-up-an-intercompany-planning-group"></a>Iestatīt starpuzņēmuma plānošanas grupu 
1. Dodieties uz sadaļu Starpuzņēmuma plānošanas grupas.
    * Vispārējā plānošana > Iestatīšana > Starpuzņēmumu plānošanas grupas  
2. Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus. Piemēram, filtrējiet pēc lauka Nosaukums, izmantojot vērtību "10".
3. Sarakstā atzīmējiet atlasīto rindu.
4. Noklikšķiniet uz Dzēst.
    * Šī darbība ir nepieciešama, lai saīsinātu starpuzņēmuma plānošanas izpildi.   Izmantojot starpuzņēmuma plānošanu, tiks izpildīta vispārējā plānošana plānošanas grupas visos uzņēmumos, sākot no zemākās plānošanas secības.  
5. Noklikšķiniet uz Jā.
6. Aizvērt lapu.

## <a name="create-an-intercompany-plan"></a>Starpuzņēmumu plāna izveide
1. Noklikšķiniet uz Starpuzņēmuma vispārējā plānošana.
    * Tas attiecas uz vispārējās plānošanas darbvietu.  
2. Laukā Starpuzņēmuma plānošanas grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas tabulu.
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Atlasiet starpuzņēmuma plānošanas 10. grupu.  
4. Laukā Starpuzņēmuma plānoto iterāciju skaits ievadiet skaitli 2.
    * Starpuzņēmuma plānošanas 10. grupā ir divi dalībnieki. Lai ieviestu aizkaves, kas radušās no avota uzņēmuma (USMF) līdz klienta uzņēmumam DEMF), ir jāizpilda starpuzņēmuma forma abos uzņēmumos divas reizes. Pirmās iterācijas ieviesīs pieprasījumu un identificēs aizkaves avota uzņēmumā (USMF). Otrā iterācija ieviesīs aizkaves no USMF līdz DEMF.  
5. Atlasiet opciju laukā Pirmā iterācija.
6. Laukā Pirmā iterācija atlasiet opciju Reģenerācija.
7. Laukā Turpmākās iterācijas atlasiet opciju Reģenerācija.
8. Laukā Pavedienu skaits ierakstiet kādu skaitli.
    * Tas norāda, cik paralēli pavedieni ir izmantoti plānošanā.  
9. Noklikšķiniet uz OK.

## <a name="view-the-result-of-the-plan"></a>Skatīt plānošanas rezultātu
1. Laukā Plāns noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
2. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Noklikšķiniet uz StaticPlan saites. Jums jābūt uzņēmumā USMF.  
3. Noklikšķiniet uz Plānotie pasūtījumi.


