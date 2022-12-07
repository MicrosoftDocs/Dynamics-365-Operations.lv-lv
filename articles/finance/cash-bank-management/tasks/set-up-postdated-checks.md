---
title: Ar iepriekšēju datumu datētu čeku iestatīšana
description: Šajā rakstā ir izskaidrots, kā norādīt, vai grāmatot žurnāla ierakstus ar iepriekš noteiktu datumu veiktiem čekiem un kādus grāmatošanas žurnālus izmantot ierakstu un kreditoru maksājumu norēķiniem.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5ef9aa6b67eb630713dd1f15b2ae49c358edae9
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/23/2022
ms.locfileid: "9804187"
---
# <a name="set-up-postdated-checks"></a>Ar iepriekšēju datumu datētu čeku iestatīšana

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir izskaidrots, kā norādīt, vai grāmatot žurnāla ierakstus ar iepriekš noteiktu datumu veiktiem čekiem un kādus grāmatošanas žurnālus izmantot ierakstu un kreditoru maksājumu norēķiniem. Varat arī norādīt izsniegto čeku, saņemt čeku un ieturētā nodokļa klīringa kontus. Ar iepriekšēju datumu datēti čeki ir čeki, kas tiek izsniegti, lai veiktu vai saņemtu maksājumus nākotnes datumā. Varat norādīt, vai čekam ir jābūt atspoguļotam uzskaites grāmatās pirms tās dzēšanas termiņa.



Šīs procedūras izpildei nepieciešama loma Kasieris. Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.


## <a name="set-up-postdated-checks"></a>Ar iepriekšēju datumu datētu čeku iestatīšana
1. Pārejiet uz **sadaļu Kases un bankas > un > kases un bankas pārvaldības parametrus**.
2. Noklikšķiniet uz cilnes **Ar datumu čeki** .
3. Atzīmējiet vai notīriet izvēles **rūtiņu Iespējot ar datumu veiktas pārbaudes** .
4. Atzīmējiet vai notīriet izvēles **rūtiņu Grāmatot žurnāla ierakstus, kas ir jāveic, ja čeki** ir ar datumu.
5. Laukā **Klīringa konts izsniegtajiem** čekiem norādiet vēlamās vērtības.
6. Laukā **Klīringa konts saņemtajiem** čekiem norādiet vēlamās vērtības.
7. Virsgrāmatas žurnālā **ierakstu dzēšanas** laukam ierakstiet vērtību.
8. Laukā Pārsūtiet **čekus ar datumu, kas ir ar datumu, uz šo kreditoru** maksājumu žurnālu, ierakstiet vērtību.
9. Laukā Ieturētā **nodokļa tīrīšanas** konts norādiet vēlamās vērtības.
10. Noklikšķiniet uz **Saglabāt**.
11. Aizvērt lapu.
12. Pārejiet **uz sadaļu > kreditoriem, > maksājumu metodes**.
13. Klikšķiniet **Jauns**.
14. Laukā **Maksāšanas veids** ievadiet vērtību.
15. Atlasiet ar datumu **grāmatoto čeku klīringa grāmatošanas** opciju, lai norādītu, ka čeku summa ir grāmatota klīringa kontā.
16. Laukā **Konta** tips atlasiet **Banka**.
    * Maksājuma metodes korespondējošais konts būs banka.  
17. Laukā **Maksājumu konts** norādiet vēlamās vērtības.
    * Atlasiet bankas kontu, kas tiek izmantots, lai atskaitītu rēķina summu.  
18. Noklikšķiniet uz **Saglabāt**.
19. Aizvērt lapu.
> [!NOTE]
> Lai varētu bankas kontā grāmatot ar datumu dalāmu čeku, ja sesijas datums ir lielāks par vai vienāds ar samaksas beigu datumu, ir jāiespējo līdzeklis **Termiņa beigu datuma pārbaude maksājumu žurnāla grāmatošanai grāmatotiem čekiem bankas kontā**. Šī funkcija ļauj grāmatot maksājumu žurnālus kreditoriem vai debitoriem ar grāmatotiem čekiem, ja sesijas datums ir lielāks vai vienāds ar termiņa beigu datumu.
> 
> Iestatot maksājuma **metodi**  (**Parādi kreditoriem > iestatījumus > maksāšanas** metodēm), neie aizpildiet **Pagaidu kontu**. Šajā gadījumā korespondējošais konts tiek aizpildīts ar bankas kontu, kas iestatīts **Maksājuma metodē**.
>  
> Ja ir aktivizēta šī funkcija un sesijas datums ir pirms termiņa beigu datuma, kad tiek grāmatots maksājumu žurnāls, termiņa beigu datumam ir jābūt mazākam par sesijas datumu vai vienādam ar to, **ja korespondējošā konta tips ir Banka**. Ja šī funkcija nav aktivizēta, varat grāmatot maksājumu žurnālu ar vēlāku datumu, ja sesijas datums ir pirms termiņa beigu datuma.
> Šis līdzeklis ir pieejams versijā 10.0.21 vai jaunākās versijās.    

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
