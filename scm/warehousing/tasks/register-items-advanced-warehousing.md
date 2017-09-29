--- 
title: "Krājumu reģistrēšana uzlabotā noliktavā aktivizētam krājumam, izmantojot krājumu saņemšanas žurnālu"
description: "Šajā procedūrā parādīts, kā reģistrēt krājumus, izmantojot krājumu saņemšanas žurnālu, ja izmantojat papildu noliktavas vadības procesus."
author: BibiSp
manager: AnnBe
ms.date: 02/12/2016
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
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 80f71f4ec5710ab257a45edbaee06d7c0e6a281e
ms.contentlocale: lv-lv
ms.lasthandoff: 07/28/2017

---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a>Krājumu reģistrēšana uzlabotā noliktavā aktivizētam krājumam, izmantojot krājumu saņemšanas žurnālu

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā parādīts, kā reģistrēt krājumus, izmantojot krājumu saņemšanas žurnālu, ja izmantojat papildu noliktavas vadības procesus. Tas parasti būtu jāveic saņemšanas darbiniekam. 

Šo procedūru varat izpildīt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus. Tad pirms šī ceļveža uzsākšanas pārliecinieties, ka jums ir apstiprināts pirkšanas pasūtījums ar atvērtu pirkšanas pasūtījuma rindu. Rindas vienībai ir jābūt esošai krājumā, tā nedrīkst lietot preču variantus, un tai nedrīkst būt izsekošanas dimensiju. Krājuma vienībai jābūt saistītai ar papildu noliktavas vadības procesu, kurš ir aktīvs noliktavas dimensijas grupai. Izmantojamajai noliktavai ir jābūt iespējotiem noliktavas vadības procesiem un saņemšanai izmantojamajam novietojumam jānotiek numuru zīmju pārbaudei. Ja jūs izmantojat USMF, varat izmantot uzņēmuma kontu 1001, noliktavu 51 un krājumu M9200, lai izveidotu savu PP. 

Pierakstiet izveidotā pirkšanas pasūtījuma numuru, un atzīmējiet arī krājuma kodu un vietu, kas izmantoti pirkšanas pasūtījuma rindai.


## <a name="create-an-item-arrival-journal-header"></a>Krājumu saņemšanas žurnāla virsraksta izveide
1. Dodieties uz Krājumu saņemšana.
2. Noklikšķiniet uz Jauns.
3. Laukā Nosaukums ierakstiet kādu vērtību.
    * Ja izmantojat USMF, varat ierakstīt WHS. Ja izmantojat citus datus, izvēlētajam žurnālam ir jābūt šādiem rekvizītiem: Pārbaudīt izdošanas vietu vērtībai ir jābūt Nē un Karantīnas pārraudzība vērtībai ir jābūt Nē.  
4. Laukā Numurs ierakstiet kādu vērtību.
5. Laukā Vieta ierakstiet kādu vērtību.
    * Atlasiet vietu, ko izmantojat pirkšanas pasūtījuma rindai. Tā kalpos kā noklusējuma vērtība, kas pēc noklusējuma tiks lietota visām žurnāla rindām. Ja izmantojāt USMF noliktavu 51, izvēlieties vietu 5.  
6. Laukā Noliktava ierakstiet kādu vērtību.
    * Atlasiet derīgu noliktavu atlasītajai vietai. Tā kalpos kā noklusējuma vērtība, kas pēc noklusējuma tiks lietota visām žurnāla rindām. Ja jūs izmantojat parauga vērtības no USMF, atlasiet 51.  
7. Ierakstiet vērtību laukā Vieta.
    * Atlasiet derīgu novietojumu atlasītajā noliktavā. Novietojums ir jāsasaista ar novietojuma profilu, ko kontrolē numura zīmes. Tā kalpos kā noklusējuma vērtība, kas pēc noklusējuma tiks lietota visām žurnāla rindām. Ja jūs izmantojat parauga vērtības no USMF, atlasiet Bulk-008.  
8. Ar peles labo pogu noklikšķiniet uz nolaižamās bultiņas laukā Numura zīme un pēc tam atlasiet Skatīt detalizētu informāciju.
9. Noklikšķiniet uz Jauns.
10. Laukā Numura zīme ierakstiet vērtību.
    * Pierakstiet vērtību.  
11. Noklikšķiniet uz Saglabāt.
12. Aizvērt lapu.
13. Laukā Numura zīme ierakstiet vērtību.
    * Ievadiet tikko izveidotās numura zīmes vērtību. Tā kalpos kā noklusējuma vērtība, kas pēc noklusējuma tiks lietota visām žurnāla rindām.  
14. Noklikšķiniet uz OK.

## <a name="add-a-line"></a>Rindas pievienošana
1. Noklikšķiniet uz Pievienot rindu.
2. Laukā Krājuma kods ierakstiet kādu vērtību.
    * Ievadiet krājuma kodu, kas tika izmantots pirkšanas pasūtījuma rindā.  
3. Laukā Daudzums ievadiet skaitli.
    * Ievadiet daudzumu, kuru vēlaties reģistrēt  
    * Lauks Datums nosaka datumu, kurā šī krājuma rīcībā esošais daudzums tiks reģistrēts krājumos.  
    * Laidiena ID ierakstīs sistēma, ja tā varēs to unikāli identificēt no sniegtās informācijas. Pretējā gadījumā jums būs tas jāpievieno manuāli. Tas ir obligāts lauks, kas savieno šo reģistrāciju ar noteiktu pirmdokumenta rindu.  

## <a name="complete-the-registration"></a>Reģistrācijas veikšana
1. Noklikšķiniet uz Pārbaudīt.
    * Šādi tiek pārbaudīts, vai žurnāls ir gatavs grāmatošanai. Ja pārbaude neizdodas, jums būs jāatrisina kļūdas pirms žurnālu varēs grāmatot.  
2. Noklikšķiniet uz OK.
    * Kad esat noklikšķinājis uz Labi, pārbaudiet ziņojumu. Tajā vajadzētu būt ziņojumam, kas ziņo, ka ar žurnālu ir viss kārtībā.  
3. Noklikšķiniet uz Grāmatot.
4. Noklikšķiniet uz OK.
    * Kad esat noklikšķinājis uz Labi, pārbaudiet ziņojumu joslu. Tajā vajadzētu būt ziņojumam par operācijas pabeigšanu.  
5. Aizvērt lapu.

