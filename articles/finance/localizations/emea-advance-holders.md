---
title: Avansa turētāju pārskats
description: Šajā rakstā ir sniegta informācija par avansa turētāja funkcionalitāti.
author: AdamTrukawka
ms.date: 09/15/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: atrukawk
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 262574,  ""intro-internal
ms.search.form: HcmWorkerAdvHolderTableListPage_RU
ms.openlocfilehash: 4b4c28c342f82ecd265bc70a51b3aa88dc0d7038
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285765"
---
# <a name="advance-holders-overview"></a>Avansa turētāju pārskats

[!include [banner](../includes/banner.md)]

*Avansa turētājs* ir uzņēmuma darbinieks, kurš atbild par organizācijas nodrošinātu izdevumu summu. Avansa turētājs var būt tikai uzņēmuma nodarbinātais. Kad notiek sagāde, avansa turētājs ziņo uzņēmumam par notikušajiem izdevumiem. Uzņēmums darbiniekam atlīdzina šo izdevumu summu. Uzņēmums kontrolē bilanci katram avansa turētājam. Lietotāji juridiskajās personās, kas atrodas Igaunijā, Latvijā, Lietuvā, Polijā, Čehijā, Ungārijā un Krievijā, var atainot specifiskas transakcijas, kuras pavada tādu uzņēmuma darbinieku operācijas, kuri ir atbildīgi par organizācijas nodrošinātu izdevumu summu.

## <a name="set-up-an-advance-holder"></a>Iestatīt avansa turētāju
Izpildiet tālāk aprakstītos avansa turētāja iestatīšanas uzdevumus. Šajā sadaļā aprakstītie uzdevumi ir jāizpilda tālāk norādītajā secībā.

1. Izveidojiet avansa turētāju grupas.
2. Iestatiet darbinieka grāmatošanas profilu.
3. Iestatiet kreditoru parametrus.
4. Izveidojiet avansa turētājam specifiskus maksājuma nosacījumus.
5. Izveidojiet avansa turētājam specifiskus maksājuma nosacījumus.
6. Izveidojiet avansa turētāju.


### <a name="advance-holder-groups"></a>Avansa turētāju grupas

Lai izveidotu avansa turētāju grupu, izmantojiet lapu **Avansa turētāju grupas**. Avansa turētāju grupai varat norādīt nosaukumu, aprakstu un korespondējošo kontu.
### <a name="employee-posting-profile"></a>Darbinieku grāmatošanas metode

Lai izveidotu metodi avansa turētāju transakcijām, izmantojiet lapu **Darbinieku grāmatošanas metodes**. Darbinieka grāmatošanas metodei varat norādīt tālāk aprakstīto informāciju.

|      Lauks      |                                            Apraksts                                            |
|-----------------|---------------------------------------------------------------------------------------------------|
| **Grāmatošanas metode** |  Ievadiet grāmatošanas metodes identifikācijas kodu avansa turētājam.               |
|   **Apraksts**   |  Ievadiet īsu grāmatošanas metodes aprakstu.                         |
|    **Derīgs**    |  Grāmatošanas metodes iestatīšanas nolūkos grupēšanas līmenim atlasiet kādu no tālāk norādītajām opcijām. <ul> <li>**Tabula** — šī opcija tiek izmantota, lai iestatītu grāmatošanas profilu vienam avansa turētājam. Laukā **Atsauce** ir jānorāda avansa turētāja kods.</li> <li>**Grupa** — šī opcija tiek izmantota, lai iestatītu grāmatošanas profilu avansa turētāju grupai. Laukā **Atsauce** ir jānorāda grupas kods.</li> <li>**Viss** — šī opcija tiek izmantota, lai iestatītu grāmatošanas profilu visiem avansa turētājiem.</li></ul> |
| **Atsauce** | Atlasiet avansa turētāja kodu, ja laukā **Derīgs** ir atlasīta **Tabula**, vai atlasiet avansa turētāju grupu, ja laukā **Derīgs** ir atlasīta **Grupa**. |
| **Summu konts** | Atlasiet kopsavilkuma kontu transakciju iegrāmatošanai. |



### <a name="account-payable-parameters"></a>Kreditoru moduļa parametri

Lai atainotu avansa turētāju transakcijas, lapas **Kreditoru moduļa parametri** sadaļā **Avansa turētāji** ir jāiestata tālāk aprakstītie lauki.

|  Lauks                                         | Apraksts       |
|------------------------------------------------|-------------------|
| **Grāmatošanas metode**                            | Atlasiet noklusējuma metodi avansa turētāju transakciju veikšanai.                                                                                                         |
| **Avansa turētāju kārtošana**                     | Ja šī opcija ir atzīmēta, tad avansa turētāji lapā **Avansa turētāji** tiek rādīti saraksta sākumā lapā.                                                                     |
| **Izsniegšana, kad bilance ir atvērta**                 | Ja šī opcija ir atzīmēta, tad tiek atļauta naudas avansa izsniegšana avansa turētājam, kuram ir atvērta pozitīva bilance.                                                                      |
| **Lauku grupa Bilances slēgšana no kases: Nosaukums** | Atlasiet kases orderu žurnāla kodu. Šis žurnāla kods tiek izmantots, lai ģenerētu kases izdevumu orderus un ieņēmumu orderus, kad avansa turētāju bilances tiek slēgtas caur kasi. |
| **Kase**                                       | Atlasiet kases kontu, lai noteiktu dokumentus, kas tiek izmantoti avansa turētāju bilanču slēgšanai.                                                                 |
| **Lauku grupa Bilances slēgšana no bankas: Nosaukums** | Atlasiet žurnāla kodu transakcijām, kas paredzētas bilanču slēgšanai caur banku.                                                                                                   |
| **Konta tips**                               | Atlasiet banku, kas paredzēta avansa turētāja bilanču slēgšanai caur banku.                                                                                                        |
| **Galvenais konts**                               | Atlasiet bankas konta kodu, kas paredzēts avansa turētāja bilanču slēgšanai caur banku.                                                                                           |

### <a name="terms-of-payment-for-advance-holder"></a>Avansa turētāja maksājuma nosacījumi

Lai pareizi reģistrētu un grāmatotu pirkšanas pasūtījumu, izmantojot avansa turētāju, ir jālieto maksājuma nosacījumi, kuriem opcija **No avansa turētāja** ir iestatīta uz **Patiess**.

### <a name="create-an-advance-holder"></a>Avansa turētāja izveide

Lai varētu izveidot avansa turētāju, nodarbinātajiem jau ir jābūt iestatītiem. Papildinformāciju skatiet rakstā [Ievadīt darbinieka informāciju (uzdevuma ceļvedis)](../../human-resources/hr-personnel-enter-worker-information.md). 

1. Dodieties uz **Kreditori** > **Avansa turētāji** >  **Avansa turētāji**.

    > [!NOTE]
    > Lapā **Avansa turētāji** darbiniekus nevar pievienot vai dzēst. Darbinieki vispirms ir jāpieņem darbā modulī **Cilvēkresursi**. Lapā **Darbinieku grāmatošanas metodes** var iestatīt darbinieku grāmatošanas metodi, kas tiek izmantota avansa turētāju bilances grāmatošanai.

2. Atlasiet darbinieku un pēc tam noklikšķiniet uz **Rediģēt**.
3. Lai norādītu, ka darbinieks ir avansa turētājs, kopsavilkuma cilnē **Vispārēji** iestatiet opcijas **Avansa turētājs** vērtību **Jā**.
4. Laukā **Grupa** atlasiet avansa turētāju grupu, kurai pieder darbinieks.
5. Laukā **Personas identifikācijas dokuments** norādiet detalizētu informāciju par personas identifikācijas dokumentu.
    - **Sērija** — ievadiet tā dokumenta sēriju, kurš tiek izmantots avansa turētāja identitātes verificēšanai.
    - **Numurs** — ievadiet tā dokumenta numuru, kurš tiek izmantots avansa turētāja identitātes verificēšanai.
    - **Izsniegšanas datums** — atlasiet vai ievadiet dokumenta izsniegšanas datumu.
    - **Izsniedza** — ievadiet detalizētu informāciju par iestādi vai personu, kas izsniedza šo dokumentu.
6. Atlasiet **Saglabāt** vai aizveriet lapu.

> [!NOTE]
> Ja lapā **Kreditoru moduļa parametri** ir iestatīta opcijas **Avansa turētāju kārtošana** vērtība **Jā**, lapas **Avansa turētāji** režģa augšpusē tiek parādīti avansa turētāji.


## <a name="advance-holder-inquiries-and-reports"></a>Avansa turētāju pieprasījumi un pārskati

### <a name="advance-holder-transactions-inquiry"></a>Avansa turētāju transakciju pieprasījums

Lai iegūtu sarakstu ar avansa turētāja transakcijām, lapā **Avansa turētāji** atlasiet **Transakcijas**. Lai redzētu transakcijas visiem avansa turētājiem vai lai izveidotu specifisku pieprasījumu, pamatojoties uz avansa turētāja transakcijām, noklikšķiniet uz **Kreditori** >  **Pieprasījumi un pārskati** >  **Avansa turētāju pieprasījumi un pārskati**  > **Transakcijas**. Atlasiet vienumu **Dokuments**, lai atvērtu lapu **Dokumentu transakcijas**.

### <a name="advance-holder-balance-inquiry"></a>Avansa turētāja bilances pieprasījums

Lai redzētu avansa turētāja bilanci, izmantojiet lapu **Avansa turētāji**. Lai redzētu bilanci visiem avansa turētājiem vai lai izveidotu specifisku pieprasījumu, pamatojoties uz avansa turētāju kontiem, noklikšķiniet uz **Parādi kreditoriem** &gt; **Pieprasījumi un pārskati** &gt; **Avansa turētāju pieprasījumi un pārskati** &gt; **Bilance**.
### <a name="advance-holder-balance-report"></a>Avansa turētāja bilances pārskats

Lai priekšskatītu un drukātu pārskatu, pamatojoties uz informāciju par avansa turētāja bilanci, noklikšķiniet uz **Parādi kreditoriem** &gt; **Pieprasījumi un pārskati** &gt; **Avansa turētāju pieprasījumi un pārskati** &gt; **Avansa turētāja bilances pārskats**.
### <a name="advance-holder-transactions-report"></a>Avansa turētāja transakciju pārskats

Lai priekšskatītu un drukātu pārskatu, pamatojoties uz avansa turētāju transakcijām, noklikšķiniet uz **Parādi kreditoriem** &gt; **Pieprasījumi un pārskati** &gt; **Avansa turētāju pieprasījumi un pārskati** &gt; **Avansa turētāja transakciju pārskats**.

## <a name="advance-holder-transactions"></a>Avansa turētāju darbības

Darbiniekiem, kuri ir avansa turētāji, transakcijas var grāmatot, izmantojot avansa turētāju kontus. Lai izsekotu visas avansa turētāja transakcijas, var izmantot katram avansa turētājam norādīto nodarbinātā ID. Šis numurs kā konta numurs avansa turētāju transakcijām tiek izgūts lapās **Virsgrāmatas žurnāli** un **Avansa turētāju transakcijas**.

### <a name="create-and-post-a-purchase-order-with-advance-holder-details"></a>Izveidot un grāmatot pirkšanas pasūtījumu ar avansa turētāja informāciju
Vispārīgāku informāciju par pirkšanas pasūtījumiem skatiet rakstā [Pirkšanas pasūtījuma apskats](../../supply-chain/procurement/purchase-order-overview.md). Ja tiek izveidots un grāmatots kreditora rēķins ar avansa turētāja informāciju, tad avansa turētāja bilances tiks grāmatotas darbinieka bilances kontā, nevis kreditora bilances kontā. Lai pirkšanas pasūtījumam pievienotu avansa turētāja informāciju, izpildiet tālāk sniegtos norādījumus.

1. Sadaļas **Cena un atlaide** laukā **Maksājuma nosacījumi** atlasiet maksājuma nosacījumu. Plašāku informāciju par **Maksājuma nosacījumiem** skatiet sadaļā [Definēt piegādātāja maksājuma nosacījumus](../accounts-payable/tasks/define-vendor-payment-terms.md). 
2. Atlasiet maksājumu termiņu, kuram lapā **Maksājuma nosacījumi** ir atzīmēta opcija **No avansa turētāja**. 
3. Kopsavilkuma cilnes **Cena un atlaide** laukā **Avansa turētājs** pirkšanas pasūtījumam atlasiet avansa turētāju.

Pirkšanas pasūtījuma grāmatošanas process izveido divas kreditora transakcijas ar pretējām summām un vienu avansa turētāja transakciju. Bez avansa turētāja informācijas tiek izveidota tikai viena kreditora transakcija.

### <a name="settle-advance-holder-balances-by-using-the-bank"></a>Nosegt avansa turētāja bilances, izmantojot banku
Kad avansa turētāja bilances nosedzat, izmantojot banku, avansa turētāja bilanču slēgšanas žurnāla ieraksti tiek izveidoti virsgrāmatas žurnālā. Žurnāla un bankas kodu varat iestatīt lapas **Kreditoru moduļa parametri** sadaļā **Avansa turētāji**. 

1. Lai slēgtu avansa turētāja bilanci, izmantojot banku, atveriet sadaļu **Kreditori** >  **Avansa turētāji** > **Avansa turētāji**. 
2. Darbību rūtī atlasiet **Bilance** > **Slēgt ar banku**. 
3. Lapā **Slēgt no bankas** ievadiet tālāk minēto informāciju.

    | Lauks                    | Apraksts |
    |------------------------------|-------------------|
    | **Maksājuma datums**          | Ievadiet datumu, kad maksājums ir jāgrāmato.|
    | **Summa pārskaitīšanai** | Ievadiet bilances summu slēgšanas laikā. Laukā **Summa** norādītā summa lapā **Bilance** tiek rādīta pēc noklusējuma. |
    | **Automātiski**                | Atzīmējiet izvēles rūtiņu **Automātiski**, lai automātiski izveidotu un grāmatotu žurnālu, kurš ir sākotnēji iestatīts lapā **Kreditoru moduļa parametri**.|

### <a name="settle-advance-holder-balances-by-using-cash"></a>Nosegt avansa turētāja bilances, izmantojot skaidru naudu
Kad nosedzat avansa turētāja bilances, izmantojot skaidru naudu, avansa turētāja bilanču slēgšanas žurnāla ieraksti tiek izveidoti pavadzīmju žurnālā. Žurnāla un skaidras naudas kodu varat iestatīt lapas **Kreditoru moduļa parametri** cilnē **Avansa turētāji**. 

1. Lai slēgtu avansa turētāja bilanci, izmantojot skaidru naudu, atveriet sadaļu **Kreditori** >  **Avansa turētāji** > **Avansa turētāji**. 
2. Darbību rūtī atlasiet **Bilance** > **Slēgt ar skaidru naudu**. 
3. Lapā **Slēgt no kases** ievadiet tālāk minēto informāciju.

    | Lauks                    | Apraksts
    |------------------------------|-----------------|
    | **Maksājuma datums**          | Ievadiet datumu, kad maksājums ir jāgrāmato.|
    | **Summa pārskaitīšanai** | Ievadiet bilances summu slēgšanas laikā. Laukā **Summa** norādītā summa lapā **Bilance** tiek rādīta pēc noklusējuma. |
    | **Automātiski**                | Atzīmējiet izvēles rūtiņu **Automātiski**, lai automātiski izveidotu un grāmatotu žurnālu, kurš ir sākotnēji iestatīts lapā **Kreditoru moduļa parametri**.     |

Pēc pavadzīmju žurnāla apstrādāšanas, ja laukā **Summa pārskaitīšanai** summa bija negatīva, tad avansa turētājam tiek ģenerēts izdevumu orderis, kad bilances tiek slēgtas. Ja laukā **Summa pārskaitīšanai** summa bija pozitīva, tad tiek ģenerēts ieņēmumu orderis.

## <a name="additional-resources"></a>Papildu resursi

- [Avansa maksājums darbiniekam (Austrumeiropa)](tasks/advance-payment-employee.md)
- [Krievijas avansa turētāju pārskats](rus-advance-holders.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
