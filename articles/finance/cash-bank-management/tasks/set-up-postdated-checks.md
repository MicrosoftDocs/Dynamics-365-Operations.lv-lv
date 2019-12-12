---
title: Ar iepriekšēju datumu datētu čeku iestatīšana
description: Šajā tēmā izskaidrots, kā norādīt, vai grāmatot ar iepriekšēju datumu datētu čeku žurnāla ierakstus, ko izmantot ierakstu dzēšanai un kreditoru maksājumiem.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 035f6e3b0268f8ee4c9006ca5f0527133cf2771c
ms.sourcegitcommit: 69f8233e86b32347474a25d83b4ac5920f60407d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/02/2019
ms.locfileid: "2538482"
---
# <a name="set-up-postdated-checks"></a>Ar iepriekšēju datumu datētu čeku iestatīšana

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā tēmā izskaidrots, kā norādīt, vai grāmatot ar iepriekšēju datumu datētu čeku žurnāla ierakstus, ko izmantot ierakstu dzēšanai un kreditoru maksājumiem. Varat arī norādīt izsniegto čeku, saņemt čeku un ieturētā nodokļa klīringa kontus. Ar iepriekšēju datumu datēti čeki ir čeki, kas tiek izsniegti, lai veiktu vai saņemtu maksājumus nākotnes datumā. Varat norādīt, vai čekam ir jābūt atspoguļotam uzskaites grāmatās pirms tās dzēšanas termiņa.



Šīs procedūras izpildei nepieciešama loma Kasieris. Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.


## <a name="set-up-postdated-checks"></a>Ar iepriekšēju datumu datētu čeku iestatīšana
1. Pārejiet uz sadaļu Kases un bankas pārvaldība > Iestatījumi > Kases un bankas pārvaldības parametri.
2. Noklikšķiniet uz cilnes Ar iepriekšēju datumu datēti čeki.
3. Atzīmējiet vai notīriet izvēles rūtiņu Iespējot čekus, kas datēti ar iepriekšēju datumu.
4. Atzīmējiet vai notīriet izvēles rūtiņu Grāmatot žurnāla ierakstus, kas atbilst čekiem, kas datēti ar iepriekšēju datumu.
5. Laukā Klīringa konts izsniegtajiem čekiem norādiet vēlamās vērtības.
6. Laukā Klīringa konts saņemtajiem čekiem norādiet vēlamās vērtības.
7. Laukā Virsgrāmatas žurnāls ierakstu dzēšanai ievadiet vērtību.
8. Laukā Pārsūtīt ar iepriekšēju datumu datētus čekus uz šo kreditoru maksājumu žurnālu ierakstiet vērtību.
9. Laukā Ieturētā nodokļa tīrīšanas konts norādiet vēlamās vērtības.
10. Noklikšķiniet uz Saglabāt.
11. Aizvērt lapu.
12. Pārejiet uz sadaļu Kreditori > Maksājuma iestatījumi > Maksāšanas metodes.
13. Noklikšķiniet uz Jauns.
14. Ierakstiet vērtību laukā Maksāšanas metode.
15. Atlasiet opciju Ar iepriekšēju datumu datētu čeku klīringa grāmatošana, lai norādītu, ka čeka summa ir iegrāmatota klīringa kontā.
16. Laukā Konta tips atlasiet Banka.
    * Maksājuma metodes korespondējošais konts būs banka.  
17. Laukā Maksājumu konts norādiet vēlamās vērtības.
    * Atlasiet bankas kontu, kas tiek izmantots, lai atskaitītu rēķina summu.  
18. Klikšķiniet Saglabāt.
19. Aizvērt lapu.
