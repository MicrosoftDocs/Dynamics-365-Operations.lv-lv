---
title: Starpuzņēmumu plāna izveide
description: Šajā procedūrā ir aprakstīts, kā izveidot starpuzņēmuma plānu.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d378a89bbb4de6d67db0019dc72a27945d50c4e9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555981"
---
# <a name="create-an-intercompany-plan"></a>Starpuzņēmumu plāna izveide

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

