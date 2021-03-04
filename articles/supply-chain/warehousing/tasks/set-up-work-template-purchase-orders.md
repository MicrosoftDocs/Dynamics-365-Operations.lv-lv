---
title: Pirkšanas pasūtījumu darba veidnes iestatīšana
description: Šajā tēmā aprakstīta vienkāršas darba veidnes izveide, kuru paredzēts izmantot saņemto krājumu izvietošanai.
author: ShylaThompson
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6628936a56619de255ca7dc7b332b5819918c310
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432989"
---
# <a name="set-up-a-work-template-for-purchase-orders"></a>Pirkšanas pasūtījumu darba veidnes iestatīšana

[!include [banner](../../includes/banner.md)]

Šajā tēmā aprakstīta vienkāršas darba veidnes izveide, kuru paredzēts izmantot saņemto krājumu izvietošanai. Darba veidnes nosaka norādījumu kopu, kas noliktavas darbiniekam tiek sniegti mobilajā ierīcē, pārvietojot krājumus no saņemšanas zonas. Šo procedūru varat lietot, izmantojot datus, kas minēti demonstrācijas datu uzņēmumam USMF. Pirms sākat darbu ar šo ceļvedi, izveidojiet darbu kopas ID. Šajā piemērā tiek izmantots darbu kopas ID ar nosaukumu Ienākošs. Šī procedūra ir paredzēta noliktavas pārvaldniekam.

1. Navigācijas rūtī dodieties uz **Moduļi > Noliktavas pārvaldība > Iestatīšana > Darba > Darba veidnes**.
2. Laukā **Darba pasūtījuma veids** atlasiet **Pirkuma pasūtījumi**.

## <a name="create-a-work-template-header"></a>Izveidojiet darba veidnes virsrakstu
1. Atlasiet **Jauns**.
2. Ievadiet skaitli laukā **Secības numurs**. Šī ir darba veidņu novērtēšanas secība. Ja nepieciešams, šo secību varat mainīt.  
3. Laukā **Darba veidne** ierakstiet kādu vērtību. Tas ir šīs veidnes veidnes unikālais identifikators.  
4. Laukā **Darba veidnes apraksts** ierakstiet kādu vērtību.
    - Opcija **Derīgs** nebūs atzīmēta, kamēr nebūsiet aizpildījis visu veidnei nepieciešamo informāciju un atlasījis **Saglabāt**.  
    - Darba pasūtījumu, kura tips ir **Pirkšanas pasūtījums**, nevar apstrādāt automātiski, tāpēc opcijai **Automātiski apstrādāt** atstājiet iestatījumu **Nē**.  
5. Laukā **Darba kopas ID** ierakstiet kādu vērtību. Darbu kopu ID ļauj organizēt darbu grupās. Šeit iestatītā vērtība būs noklusējuma vērtība visiem darbiem, kas izveidoti, lietojot šo veidni.  
6. Laukā **Darba prioritāte** ievadiet skaitli `1`. Tas norāda darba svarīgumu, un šeit iestatītā vērtība būs noklusējuma vērtība visiem darbiem, kas izveidoti, lietojot šo veidni.  
7. Atlasiet **Saglabāt**. Pirms kļūst pieejama poga **Rediģēt vaicājumu**, vispirms jāsaglabā darba veidnes virsraksts.  

## <a name="set-up-the-query-for-the-work-template"></a>Darba veidnes vaicājuma iestatīšana
1. Atlasiet **Rediģēt vaicājumu**. Mēs noteiksim ierobežojumu, ka veidni var izmantot tikai noteiktā noliktavā.  
2. Atlasiet **Pievienot**.
3. Jaunās rindas laukā **Lauks** ierakstiet vērtību `warehouse`.
4. Laukā **Kritēriji** ierakstiet kādu vērtību.
5. Atlasiet **Labi**.
6. Atlasiet **Jā**.

## <a name="set-work-template-details"></a>Detalizētas informācijas par darba veidni iestatīšana
1. Atlasiet **Jauns**.
2. Laukā **Darba tips atlasiet** vienumu **Izdošana**.
3. Laukā **Darba klases ID** ierakstiet vērtību `purchase`. Šeit iestatītā darba klase būs noklusējuma klase visās darba rindās, kuru veids ir Izdošana un kuras izveidotas, lietojot šo veidni. Šo darba klasi nevar pārrakstīt no darba pasūtījuma rindām. Darba klases tiek izmantotas, lai virzītu un/vai ierobežotu darba pasūtījuma rindu veidu, ko noliktavas darbinieks var apstrādāt mobilajā ierīcē.  
4. Atlasiet **Jauns**.
5. Laukā **Darba veids** atlasiet **Ievietot**.
6. Laukā **Darba klases ID** ievadiet vērtību. Izdošanas un izvietošanas instrukcijas ir kopa. Katrai izdošanas/izvietošanas kopai ir jābūt vienai un tai pašai darba klasei. Izmantojiet to pašu darba klasi, kuru norādījāt izdošanas instrukcijai.  
7. Atlasiet **Saglabāt**. Pievērsiet uzmanību, ka tagad ir atzīmēta izvēles rūtiņa **Derīgs**.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]