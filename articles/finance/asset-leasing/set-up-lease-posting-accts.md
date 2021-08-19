---
title: Nomas grāmatošanas kontu iestatīšana
description: Šajā tēmā uzskaitīti grāmatošanas konti, kas ir nepieciešami līdzekļu nomas darījumiem, un skaidrots, kā definēt grāmatošanas kontus nomas grāmatošanas parametru lapā.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ac8dc59a19a489c6a7c4bf6621dd1a316de03ac3af4512d3ed7e55668af801b1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770645"
---
# <a name="set-up-lease-posting-accounts"></a>Nomas grāmatošanas kontu iestatīšana

[!include [banner](../includes/banner.md)]

Šajā tēmā uzskaitīti grāmatošanas konti, kas ir nepieciešami līdzekļu nomas darījumiem, un skaidrots, kā definēt grāmatošanas kontus **nomas grāmatošanas parametru** lapā.

Lai ievērotu uzskaites standartu kodifikācijas tēmu 842 (ASC 842) un starptautisko finanšu pārskatu standartu 16 (IFRS 16), jums, iespējams, būs jāizveido konti kontu plānā. Tomēr neviens konts, ko izveidojat, lai atbilstu ASC un IFRS standartiem, nav pamatlīdzekļu konts. Saskaņā ar ASC 842, līdzekļu lietošanas tiesības tiek ierakstītas gan finansēm, gan operatīvai nomai. Šīs nomas ir nodalītas no pamatlīdzekļiem. (Jūs joprojām varat uzturēt LLT, lietojot pamatlīdzekļus.)

Vairāk informācijas par to, kā izveidot konta struktūras, skatiet sadaļā [Konta struktūru izveide](../general-ledger/tasks/create-account-structures.md). Vairāk informācijas par to, kā izveidot galveno kontu, skatiet sadaļā [Galvenā konta izveide](../general-ledger/tasks/create-main-account.md).

Tabulā ir parādīti to kontu piemēri, kuri ir jāizveido iznomāto līdzekļu darījumiem, ja tie vēl nav izveidoti. Atbilstoši IFRS 16 operatīvās nomas attiecības joprojām tiek izmantotas zemas vērtības un īstermiņa nomai.

| Virsgrāmatas konta numurs | Konta veids  | Konta nosaukums                                          |
|-----------------------|---------------|-------------------------------------------------------|
| 180150                | Līdzeklis         | Transportlīdzekļa LLT                                     |
| 180160                | Līdzeklis         | Ēkas LLT                                    |
| 180250                | Līdzeklis         | Uzkrātais nolietojums — transportlīdzekļi                   |
| 180260                | Līdzeklis         | Uzkrātais nolietojums — ēkas                  |
| 222300                | Saistības     | Īstermiņa saistības — finanšu nomas                |
| 222310                | Bilance | Īstermiņa saistības — operatīvās nomas              |
| 250200                | Saistības     | Izsniegtie vekseļi                                         |
| 250601                | Bilance | Ilgtermiņa saistības — finanšu nomas                 |
| 250602                | Bilance | Ilgtermiņa saistības — operatīvās nomas               |
| 250606                | Bilance | Atliktā nomas maksa                                         |
| 300160                | Bilance | Nesadalītā peļņa                                     |
| 604500                | Expense       | Nomas izdevumi                                         |
| 604501                | Expense       | Transportlīdzekļa operatīvās nomas izdevumi — procentu pieaugums  |
| 604502                | Expense       | Transportlīdzekļa operatīvās nomas izdevumi — amortizācija        |
| 605200                | Expense       | Ēkas operatīvās nomas izdevumi — procentu pieaugums |
| 605201                | Expense       | Ēkas operatīvās nomas izdevumi — amortizācija       |
| 607101                | Expense       | Transportlīdzekļa nomas amortizācijas izdevumi                    |
| 607102                | Expense       | Ēkas nomas amortizācijas izdevumi                   |
| 607103                | Expense       | Vērtības samazinājuma izdevumi — finanšu nomas                   |
| 607104                | Expense       | Vērtības samazinājuma izdevumi — operatīvās nomas                 |
| 618910                | Expense       | Nomas izdevumi — finanšu nomas                        |
| 618920                | Expense       | Mainīgie maksājumi — finanšu nomas                    |
| 618930                | Expense       | Mainīgie maksājumi — operatīvās nomas                  |
| 800600                | Expense       | Transportlīdzekļa nomas procentu izdevumi                        |
| 800601                | Expense       | Ēkas nomas procentu izdevumi                       |
| 801201                | Bilance | Peļņa un zaudējumi — nomas modifikācija                      |

## <a name="configure-posting-accounts"></a>Grāmatošanas kontu konfigurēšana

Lai piešķirtu kontus nomas grāmatām un grupām, kas ir izveidotas, ir jākonfigurē parametri līdzekļu nomai.

1. Dodieties uz **Līdzekļu noma \> Iestatījumi \> Nomas grāmatošanas parametri**.
2. Cilnē **Konti** atveriet **nomas kontu** kopsavilkuma cilni. Nosakiet finanšu un operatīvās nomas galvenos pārskatus atbilstošajam **grāmatošanas tipam**. Iepriekšējā tabulā ir parādīti tie konti,, kas ir saistīti ar operatīvo un finanšu nomu.

    > [!NOTE]
    > Šajā darbībā ir jāiestata atsevišķi konti operatīvajām un finanšu nomām katram grāmatošanas tipam, izņemot **Nomas izdevumu nobīde** un **Nomas pieaugums/samazinājums**. Uzņēmumiem, kas ievēro IFRS 16 uzskaites struktūru, operatīvajai nomai ir jāpievieno galvenais konts. Taču sistēma neizmantos šo kontu, kaut arī tas ir obligāts lauks, jo visas nomas saskaņā ar IFRS 16 klasificē kā finanšu nomas.
    >[!NOTE]
    > **Nomas pieaugums/samazinājums** tiks izmantots kā grāmatošanas tips papildu līdzekļu apsvērumiem, ieskaitot **sākotnējās tiešās izmaksas, nomas stimulus, nomas priekšapmaksas un demontāžas izmaksas**, bet grāmatojiet LLT galvenajā kontā, kas pēc noklusējuma izmanto **nomas līdzekli**.        
    
3. Lai atlasītu īpašu nomas grupu, kas atbilst galvenajam kontam, laukā **Konta kods** atlasiet **Grupa**. Pēc tam laukā **Konta/grupas numurs** atlasiet nomas grupu, ko piešķirt galvenajam kontam.
4. Lai piešķirtu kontu kodus administratīvajām izmaksām, kas ir iestatītas sistēmā, kopsavilkuma cilnes **Izpildes izmaksas** laukā **Izdevumu veids** atlasiet izdevumus. Pēc tam piešķiriet finanšu un operatīvos kontus, ko izmantot katrai grāmatai.

    > [!NOTE]
    > Atlasītais finanšu vai operatīvais konts tiks debetēts, kad tiek iegrāmatots plānotais izdevumu rēķins.
    > **Nomas izdevumu nobīde** tiks izmantota kā izpildes izmaksu darījumu grāmatošanas tips, bet grāmatojiet noteiktā **korespondējošā kontā** **Izpildes izmaksu maksājumu grafika rindās** nomas informācijā vai nomas grāmatas veidlapā.   


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
