---
title: Starpuzņēmumu plāna izveide
description: Šajā procedūrā ir aprakstīts, kā izveidot starpuzņēmuma plānu.
author: ChristianRytt
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ef1484e6925427454f819a5effdc911f762b48b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578276"
---
# <a name="create-an-intercompany-plan"></a>Starpuzņēmumu plāna izveide

[!include [banner](../../includes/banner.md)]

Šajā procedūrā ir aprakstīts, kā izveidot starpuzņēmuma plānu. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.

## <a name="set-up-an-intercompany-planning-group"></a>Iestatīt starpuzņēmuma plānošanas grupu

1. **Navigācijas rūtī** pārejiet uz sadaļu **Moduļi > Šablona plānošana > Iestatīšana > Starpuzņēmumu plānošanas grupas**.
2. Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus. Piemēram, filtrējiet pēc lauka Nosaukums, izmantojot vērtību "10".
3. Sarakstā atzīmējiet atlasīto rindu.
4. Atlasiet **Dzēst**. Šī darbība ir nepieciešama, lai saīsinātu starpuzņēmuma plānošanas izpildi.   Izmantojot starpuzņēmuma plānošanu, tiks izpildīta vispārējā plānošana plānošanas grupas visos uzņēmumos, sākot no zemākās plānošanas secības.  
5. Atlasiet **Jā**.
6. Aizvērt lapu.

## <a name="create-an-intercompany-master-plan"></a>Starpuzņēmumu vispārējā plāna izveide

1. **Navigācijas rūtī** ejiet uz **Moduļi > Vispārējā plānošana > Darbvietas > Vispārējā plānošana**.
2. Atlasiet **Starpuzņēmumu vispārējā plānošana**.  
3. Laukā **Starpuzņēmumu plānošanas grupa** atlasiet nolaižamo pogu uzmeklēšanas atvēršanai.
4. Sarakstā atlasiet saiti atlasītajā rindā. Atlasiet starpuzņēmuma plānošanas 10. grupu.  
5. Laukā **Starpuzņēmumu plānošanas atkārtojumi** ievadiet „2”. Starpuzņēmuma plānošanas 10. grupā ir divi dalībnieki. Lai ieviestu aizkaves, kas radušās no avota uzņēmuma (USMF) līdz klienta uzņēmumam (DEMF), ir jāizpilda starpuzņēmuma forma abos uzņēmumos divas reizes. Pirmās iterācijas ieviesīs pieprasījumu un identificēs aizkaves avota uzņēmumā (USMF). Otrā iterācija ieviesīs aizkaves no USMF līdz DEMF.  
6. Laukā **Pirmais atkārtojums** atlasiet „Reģenerācija”.
7. Laukā **Turpmākie atkārtojumi** atlasiet „Reģenerācija”.
8. Laukā **Pavedienu skaits** ievadiet skaitli. Tas norāda, cik paralēli pavedieni ir izmantoti plānošanā.  
9. Atlasiet **Labi**.

## <a name="view-the-result-of-the-plan"></a>Skatīt plānošanas rezultātu

1. Laukā **Plāns** atlasiet nolaižamo pogu uzmeklēšanas atvēršanai.
2. Sarakstā atlasiet saiti atlasītajā rindā. Atlasiet StaticPlan saiti. Jums jābūt uzņēmumā USMF.  
3. Atlasiet **Plānotie pasūtījumi**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]