--- 
title: "Manuālas iepakošanas iestatīšana (tikai 2016. gada februāris un maijs)"
description: "Iepakošanas procesu ļauj jums pārbaudīt un iepakot preces konteineros."
author: BibiSp
manager: AnnBe
ms.date: 11/04/2016
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
ms.openlocfilehash: 7f992a6a1655cd868d79228c490d59b46bfae715
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-manual-packing-february--may-2016-only"></a>Manuālas iepakošanas iestatīšana (tikai 2016. gada februāris un maijs)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Iepakošanas procesu ļauj jums pārbaudīt un iepakot preces konteineros. Šajā procesā, noliktavas darbinieki izdod preces no uzglabāšanas vietām un pārvieto tās uz iepakojuma staciju, kur tie pārbauda krājumu daudzumus un veidus, un piešķir tiem atbilstošus konteinerus. Kad konteiners ir pilns, to var aizvērt un pārvietot to uz nosūtīšanas doku, un preces ir gatavas nosūtīšanai. Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.


## <a name="set-up-location-profiles"></a>Iestatīt novietojuma profilus
1. Dodieties uz Noliktavas vadība > Iestatīšana > Noliktava > Novietojumu profili.
2. Noklikšķiniet uz Jauns.
    * Atrašanās vietas profils tiek izmantots iepakošanas stacijās, un satur informāciju un noteikumus par atrašanās vietu.  
3. Laukā Novietojuma profila ID ierakstiet vērtību.
4. Laukā Nosaukums ierakstiet kādu vērtību.
5. Laukā Atrašanās vietas formāts ievadiet vai atlasiet kādu vērtību.
6. Laukā Atrašanās vietas tips ievadiet vai atlasiet kādu vērtību.
7. Laukā Atļaut jauktus krājumus atlasiet Jā.
8. Laukā Atļaut jauktus krājumu statusus atlasiet Jā.
9. Atlasiet Jā, laukā Ignorēt partijas dienu kārtulas.
10. Aizvērt lapu.

## <a name="set-up-warehouse-management-parameters"></a>Noliktavas vadības parametru iestatīšana 
1. Doties uz Noliktavas vadība > Iestatīšana > Noliktavas pārvaldības parametri.
2. Klikšķiniet cilni Iepakošana.
3. Laukā Iepakošanas atrašanās vietas profila ID ievadiet vai atlasiet vērtību.
    * Atlasiet atrašanās vietas profilu, kuru vēlaties izmantot iepakošanai.  
4. Aizvērt lapu.

## <a name="set-up-container-types"></a>Konteinera veidu iestatīšana
1. Dodieties uz Noliktavas vadība > Iestatīšana > Konteineri > Konteineru veidi.
2. Noklikšķiniet uz Jauns.
    * Jūs varat noteikt konteineru tipus izmantošanai. Var norādīt konteinera fiziskās dimensijas, ieskaitot taras svaru, maksimālo svaru, maksimālo tilpumu, garumu, platumu un svaru.  Atribūti ir pielāgoti lauki, kas ļauj jums pievienot papildu dimensijas konteinera tipam.     
3. Laukā Konteinera veida kods ierakstiet vērtību.
4. Apraksta laukā ierakstiet vērtību.
5. Laukā Taras svars ievadiet skaitli.
6. Ievadiet skaitli laukā Maksimālais svars.
7. Laukā Tilpums ievadiet skaitli.
8. Laukā Garums ievadiet skaitli.
9. Ievadiet skaitli laukā Platums.
10. Ievadiet skaitli laukā Augstums.
11. Noklikšķiniet uz Saglabāt.
12. Aizvērt lapu.

## <a name="set-up-packing-profiles"></a>Iepakošanas profilu iestatīšana
1. Dodieties uz Noliktavas vadība > Iestatīšana > Iepakošana > Iepakošanas profili.
2. Noklikšķiniet uz Jauns.
3. Ievadiet vērtību laukā Iepakošanas profila ID.
4. Apraksta laukā ierakstiet vērtību.
5. Laukā Iepakošanas slēgšanas profila ID ievadiet vai atlasiet vērtību.
    * Konteinera slēgšanas profila ID ir neobligāts, un ir noklusējuma konteinera slēgšanas profils šim iepakošanas profilam.  
6. Laukā Konteinera ID režīms atlasiet kādu opciju.
    * Šī opcija nosaka, vai konteinera ID tiks automātiski ģenerēts, kad tiek izveidots konteineris, vai arī konteinera ID tiks ģenerēts manuāli.  
7. Laukā Konteinera veids, ievadiet vai atlasiet kādu vērtību.
    * Konteinera veids tiks izmantots pēc noklusējuma, veidojot jaunu konteineru.  
8. Konteinera slēgšanas izvēles rūtiņā, atlasiet Automātiski izveidot konteineru.
9. Noklikšķiniet uz Saglabāt.
10. Aizvērt lapu.

## <a name="set-up-container-closing-profiles"></a>Konteinera slēgšanas profilu iestatīšana
1. Dodieties uz Noliktavas vadība > Iestatīšana > Konteineri > Konteineru slēgšanas profili.
    * Konteinera slēgšanas profili definē, kas notiek, ja konteiners tiek slēgts. Jūs varat iestatīt vairākus konteinera slēgšanas profilus.       
2. Noklikšķiniet uz Jauns.
3. Laukā Iepakošanas slēgšanas profila ID ievadiet vērtību.
4. Apraksta laukā ierakstiet vērtību.
5. Laukā Manifestācija, atlasiet opciju.
    * Norādiet, vai manifestācija parādās, slēdzot konteinerus, vai apstiprinot sūtījumu. Ņemiet vērā, ka manifestācijai nepieciešama transportēšanas pārvaldība. Manifestācijai jābūt ieviestai transportēšanas programmās, lai tā strādātu.  
6. Laukā Noliktava ievadiet vai atlasiet kādu vērtību.
7. Laukā Noklusējuma galīgā sūtījuma atrašanās vieta, ievadiet vai atlasiet vērtību.
    * Tas ir vieta, uz kuru preces tiks pārvietotas pēc konteineru slēgšanas. Šai vietai jābūt atrašanās vietas profilam, kas ir definēts Noliktavas parametros.  
8. Laukā Svara vienība, ievadiet vai atlasiet kādu vērtību.
9. Noklikšķiniet uz Saglabāt.

