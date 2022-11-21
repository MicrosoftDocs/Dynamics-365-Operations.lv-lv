---
title: Ar iepriekšēju datumu datētu čeku iestatīšana
description: Šajā rakstā ir paskaidrots, kā norādīt, vai grāmatot žurnāla ierakstus grāmatotām pārbaudēm un kurus grāmatošanas žurnālus izmantot ierakstu un kreditoru maksājumu dzēšanai.
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
ms.openlocfilehash: e7172dd56113de23d841fe59ed9785471e90ed1f
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779614"
---
# <a name="set-up-postdated-checks"></a>Ar iepriekšēju datumu datētu čeku iestatīšana

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir paskaidrots, kā norādīt, vai grāmatot žurnāla ierakstus grāmatotām pārbaudēm un kurus grāmatošanas žurnālus izmantot ierakstu un kreditoru maksājumu dzēšanai. Varat arī norādīt izsniegto čeku, saņemt čeku un ieturētā nodokļa klīringa kontus. Ar iepriekšēju datumu datēti čeki ir čeki, kas tiek izsniegti, lai veiktu vai saņemtu maksājumus nākotnes datumā. Varat norādīt, vai čekam ir jābūt atspoguļotam uzskaites grāmatās pirms tās dzēšanas termiņa.



Šīs procedūras izpildei nepieciešama loma Kasieris. Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.


## <a name="set-up-postdated-checks"></a>Ar iepriekšēju datumu datētu čeku iestatīšana
1. Pārejiet uz sadaļu **Skaidras naudas un bankas pārvaldība > Iestatīšana > Skaidras naudas un bankas pārvaldības parametri**.
2. Noklikšķiniet uz **cilnes Grāmatotās pārbaudes**.
3. Atzīmējiet vai notīriet izvēles rūtiņu **Iespējot izliktās pārbaudes**.
4. Atzīmējiet vai notīriet izvēles rūtiņu **Post journal ierakstus grāmatotām pārbaudēm**.
5. **Laukā Izsniegto čeku** klīringa konts norādiet vēlamās vērtības.
6. Laukā Klīringa **konts saņemtajiem čekiem** norādiet vēlamās vērtības.
7. **Laukā Vispārīgs žurnāls ierakstu** notīrīšanai ierakstiet vērtību.
8. **Laukā Pārsūtīt grāmatotās pārbaudes uz šo kreditoru maksājumu žurnālu** ierakstiet vērtību.
9. Laukā **Ieturējuma nodokļa klīringa konts** norādiet vēlamās vērtības.
10. Noklikšķiniet uz **Saglabāt**.
11. Aizvērt lapu.
12. Pārejiet uz sadaļu **Kreditoru parādi > Maksājumu iestatīšana > Apmaksas** veidi.
13. Klikšķiniet **Jauns**.
14. Laukā **Maksāšanas veids** ievadiet vērtību.
15. Atlasiet opciju Grāmatota čeku klīringa grāmatošana, lai norādītu, ka čeka summa ir grāmatota **klīringa** kontā.
16. Laukā **Konta tips** atlasiet **Banka**.
    * Maksājuma metodes korespondējošais konts būs banka.  
17. Laukā **Maksājumu konts** norādiet vēlamās vērtības.
    * Atlasiet bankas kontu, kas tiek izmantots, lai atskaitītu rēķina summu.  
18. Noklikšķiniet uz **Saglabāt**.
19. Aizvērt lapu.
> [!NOTE]
> Lai varētu bankas kontā grāmatot ar datumu dalāmu čeku, ja sesijas datums ir lielāks par vai vienāds ar samaksas beigu datumu, ir jāiespējo līdzeklis **Termiņa beigu datuma pārbaude maksājumu žurnāla grāmatošanai grāmatotiem čekiem bankas kontā**. Šī funkcija ļauj grāmatot maksājumu žurnālus kreditoriem vai debitoriem ar grāmatotiem čekiem, ja sesijas datums ir lielāks vai vienāds ar termiņa beigu datumu.
> 
> Iestatot **maksāšanas metodi (kreditoru parādi >** maksājumu iestatījumi > maksāšanas **metodes**), neaizpildiet **pagaidu kontu**. Šajā gadījumā korespondējošais konts tiek aizpildīts ar bankas kontu, kas iestatīts **Maksājuma metodē**.
>  
> Kad līdzeklis ir iespējots un sesijas datums ir mazāks par dzēšanas datumu, grāmatojot maksājumu žurnālu, tiek parādīts šāds kļūdas ziņojums: Dzēšanas datumam jābūt mazākam vai vienādam ar sesijas datumu, **ja korespondējošā konta tips ir Banka**. Ja šī funkcija nav aktivizēta, varat grāmatot maksājumu žurnālu ar vēlāku datumu, ja sesijas datums ir pirms termiņa beigu datuma.
> Šis līdzeklis ir pieejams versijā 10.0.21 vai jaunākās versijās.    

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
