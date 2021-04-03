---
title: Starpuzņēmumu plāna izveide
description: Šajā procedūrā ir aprakstīts, kā izveidot starpuzņēmuma plānu.
author: ShylaThompson
manager: tfehr
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5b64ababa618d58feb6095704e5978295060c96f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5261121"
---
# <a name="create-an-intercompany-plan"></a>Starpuzņēmumu plāna izveide

[!include [banner](../../includes/banner.md)]

Šajā procedūrā ir aprakstīts, kā izveidot starpuzņēmuma plānu. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.


## <a name="set-up-an-intercompany-planning-group"></a>Iestatīt starpuzņēmuma plānošanas grupu 
1. **Navigācijas rūtī** pārejiet uz sadaļu **Moduļi > Šablona plānošana > Iestatīšana > Starpuzņēmumu plānošanas grupas**. 
2. Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus. Piemēram, filtrējiet pēc lauka Nosaukums, izmantojot vērtību "10".
3. Sarakstā atzīmējiet atlasīto rindu.
4. Noklikšķiniet uz **Dzēst**. Šī darbība ir nepieciešama, lai saīsinātu starpuzņēmuma plānošanas izpildi.   Izmantojot starpuzņēmuma plānošanu, tiks izpildīta vispārējā plānošana plānošanas grupas visos uzņēmumos, sākot no zemākās plānošanas secības.  
5. Noklikšķiniet uz pogas **Jā**.
6. Aizvērt lapu.

## <a name="create-an-intercompany-plan"></a>Starpuzņēmumu plāna izveide
1. **Navigācijas rūtī** ejiet uz **Moduļi > Vispārējā plānošana > Darbvietas > Vispārējā plānošana**.
2. Klikšķiniet uz **Starpuzņēmumu vispārējā plānošana**.  
3. Laukā **Starpuzņēmumu plānošanas grupa** noklikšķiniet uz nolaižamās pogas uzmeklēšanas atvēršanai.
4. Sarakstā noklikšķiniet uz saites atlasītajā rindā. Atlasiet starpuzņēmuma plānošanas 10. grupu.  
5. Laukā **Starpuzņēmumu plānošanas atkārtojumi** ievadiet „2”. Starpuzņēmuma plānošanas 10. grupā ir divi dalībnieki. Lai ieviestu aizkaves, kas radušās no avota uzņēmuma (USMF) līdz klienta uzņēmumam (DEMF), ir jāizpilda starpuzņēmuma forma abos uzņēmumos divas reizes. Pirmās iterācijas ieviesīs pieprasījumu un identificēs aizkaves avota uzņēmumā (USMF). Otrā iterācija ieviesīs aizkaves no USMF līdz DEMF.  
6. Laukā **Pirmais atkārtojums** atlasiet „Reģenerācija”.
7. Laukā **Turpmākie atkārtojumi** atlasiet „Reģenerācija”.
8. Laukā **Pavedienu skaits** ievadiet skaitli. Tas norāda, cik paralēli pavedieni ir izmantoti plānošanā.  
9. Noklikšķiniet uz **Labi**.

## <a name="view-the-result-of-the-plan"></a>Skatīt plānošanas rezultātu
1. Laukā **Plāns** noklikšķiniet uz nolaižamās pogas uzmeklēšanas atvēršanai.
2. Sarakstā noklikšķiniet uz saites atlasītajā rindā. Noklikšķiniet uz StaticPlan saites. Jums jābūt uzņēmumā USMF.  
3. Klikšķiniet uz **Plānotie pasūtījumi**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]