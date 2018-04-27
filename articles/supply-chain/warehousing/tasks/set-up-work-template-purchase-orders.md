--- 
title: "Pirkšanas pasūtījumu darba veidnes iestatīšana"
description: "Šajā procedūrā aprakstīta vienkāršas darba veidnes izveide, kuru paredzēts izmantot saņemto krājumu izvietošanai."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fbbe019bdca2d5182466a20370418a14032fe63d
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-a-work-template-for-purchase-orders"></a>Pirkšanas pasūtījumu darba veidnes iestatīšana

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā aprakstīta vienkāršas darba veidnes izveide, kuru paredzēts izmantot saņemto krājumu izvietošanai. Darba veidnes nosaka norādījumu kopu, kas noliktavas darbiniekam tiek sniegti mobilajā ierīcē, pārvietojot krājumus no saņemšanas zonas. Šo procedūru varat lietot, izmantojot datus, kas minēti demonstrācijas datu uzņēmumam USMF. Pirms sākat darbu ar šo ceļvedi, izveidojiet darbu kopas ID. Šajā piemērā tiek izmantots darbu kopas ID ar nosaukumu Ienākošs. Šī procedūra ir paredzēta noliktavas pārvaldniekam.

1. Doties uz Noliktavas vadība > Iestatīšana > Darbs > Darbu veidnes.
2. Laukā Darba pasūtījuma tips atlasiet “Pirkšanas pasūtījumi”.

## <a name="create-a-work-template-header"></a>Izveidojiet darba veidnes virsrakstu
1. Noklikšķiniet uz Jauns.
2. Ievadiet skaitli laukā Secības numurs.
    * Šī ir darba veidņu novērtēšanas secība. Ja nepieciešams, šo secību varat mainīt.  
3. Laukā Darba veidne ierakstiet kādu vērtību.
    * Tas ir šīs veidnes veidnes unikālais identifikators.  
4. Laukā Darba veidnes apraksts ierakstiet kādu vērtību.
    * Opcija Derīgs nebūs atzīmēta, kamēr nebūsiet aizpildījis visu veidnei nepieciešamo informāciju un noklikšķinājis uz Saglabāt.  
    * Darba pasūtījumu, kura veids ir Pirkšanas pasūtījums, nevar apstrādāt automātiski, tāpēc atstājiet opcijai Automātiski apstrādāt iestatījumu Nē.  
5. Laukā Darba kopas ID ierakstiet kādu vērtību.
    * Darbu kopu ID ļauj organizēt darbu grupās. Šeit iestatītā vērtība būs noklusējuma vērtība visiem darbiem, kas izveidoti, lietojot šo veidni.  
6. Laukā Darba prioritāte ievadiet skaitli "1".
    * Tas norāda darba svarīgumu, un šeit iestatītā vērtība būs noklusējuma vērtība visiem darbiem, kas izveidoti, lietojot šo veidni.  
7. Noklikšķiniet uz Saglabāt.
    * Pirms kļūst pieejama poga Rediģēt vaicājumu, vispirms jāsaglabā darba veidnes virsraksts.  

## <a name="set-up-the-query-for-the-work-template"></a>Darba veidnes vaicājuma iestatīšana
1. Noklikšķiniet uz Rediģēt vaicājumu.
    * Mēs noteiksim ierobežojumu, ka veidni var izmantot tikai noteiktā noliktavā.  
2. Noklikšķiniet uz Pievienot.
3. Sarakstā atzīmējiet atlasīto rindu.
4. Laukā Lauks ierakstiet "noliktava".
5. Laukā Kritēriji ierakstiet kādu vērtību.
6. Noklikšķiniet uz OK.
7. Noklikšķiniet uz Jā.

## <a name="set-work-template-details"></a>Detalizētas informācijas par darba veidni iestatīšana
1. Noklikšķiniet uz Jauns.
2. Laukā Darba tips atlasiet vienumu “Izdošana”.
3. Laukā Darba klases ID ierakstiet "pirkšana".
    * Šeit iestatītā darba klase būs noklusējuma klase visās darba rindās, kuru veids ir Izdošana un kuras izveidotas, lietojot šo veidni. Šo darba klasi nevar pārrakstīt no darba pasūtījuma rindām. Darba klases tiek izmantotas, lai virzītu un/vai ierobežotu darba pasūtījuma rindu veidu, ko noliktavas darbinieks var apstrādāt mobilajā ierīcē.  
4. Noklikšķiniet uz Jauns.
5. Laukā Darba tips atlasiet vienumu “Izvietošana”.
6. Laukā Darba klases ID ierakstiet kādu vērtību.
    * Izdošanas un izvietošanas instrukcijas ir kopa. Katrai izdošanas/izvietošanas kopai ir jābūt vienai un tai pašai darba klasei. Izmantojiet to pašu darba klasi, kuru norādījāt izdošanas instrukcijai.  
7. Noklikšķiniet uz Saglabāt.
    * Pievērsiet uzmanību, ka tagad ir atzīmēta izvēles rūtiņa Derīgs.  


