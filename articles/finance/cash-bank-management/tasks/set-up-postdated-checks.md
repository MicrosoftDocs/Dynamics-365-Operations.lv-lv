---
title: Ar iepriekšēju datumu datētu čeku iestatīšana
description: Šajā tēmā izskaidrots, kā norādīt, vai grāmatot ar iepriekšēju datumu datētu čeku žurnāla ierakstus, ko izmantot ierakstu dzēšanai un kreditoru maksājumiem.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d0d4afd74f9a0f9018629fa92ab6595bfa94f973
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026209"
---
# <a name="set-up-postdated-checks"></a>Ar iepriekšēju datumu datētu čeku iestatīšana

[!include [banner](../../includes/banner.md)]

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
18. Noklikšķiniet uz Saglabāt.
19. Aizvērt lapu.
> [!NOTE]
> Lai varētu bankas kontā grāmatot ar datumu dalāmu čeku, ja sesijas datums ir lielāks par vai vienāds ar samaksas beigu datumu, ir jāiespējo līdzeklis **Termiņa beigu datuma pārbaude maksājumu žurnāla grāmatošanai grāmatotiem čekiem bankas kontā**. Šī funkcija ļauj grāmatot maksājumu žurnālus kreditoriem vai debitoriem ar grāmatotiem čekiem, ja sesijas datums ir lielāks vai vienāds ar termiņa beigu datumu.
> 
> Iestatot **Maksāšanas metodi** (**Kreditori > Maksājumu iestatījumi > Maksājuma metodes**), neaizpildiet **Pagaidu kontu**. Šajā gadījumā korespondējošais konts tiek aizpildīts ar bankas kontu, kas iestatīts **Maksājuma metodē**.
>  
> Ja ir aktivizēta šī funkcija un sesijas datums ir pirms termiņa beigu datuma, grāmatojot maksājumu žurnālu, tiek parādīts šāds kļūdas ziņojums: "Termiņa beigu datumam ir jābūt mazākam par sesijas datumu vai vienādam ar to, ja korespondējošā konta tips ir Banka". Ja šī funkcija nav aktivizēta, varat grāmatot maksājumu žurnālu ar vēlāku datumu, ja sesijas datums ir pirms termiņa beigu datuma.    

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
