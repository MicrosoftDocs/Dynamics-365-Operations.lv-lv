---
title: "Ievadīt algu sākuma bilances"
description: "Šajā tēmā ir aprakstītas darbības sākuma bilanču ievadīšanai attiecībā uz ienākumu veida kodiem, ieturējumiem, atvieglojumiem un nodokļiem. Šī informācija ir vērtīga partneriem, lai datus jaunai algu ieviešanai migrētu vai pārsūtītu no citas sistēmas."
author: kherr75
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 736eedf270ac08b0bdf9364821f8a7bae981ade9
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="enter-payroll-beginning-balances"></a>Ievadīt algu sākuma bilances

[!include[banner](../../includes/banner.md)]

Šajā tēmā ir aprakstītas darbības sākuma bilanču ievadīšanai attiecībā uz ienākumu veida kodiem, ieturējumiem, atvieglojumiem un nodokļiem. Šī informācija ir vērtīga partneriem, kuri datus jaunai algu ieviešanai pārsūtīta no citas sistēmas. Lai sagatavotos ievadīt sākuma algu bilances, mēs pārbaudām tālāk norādīto informāciju.

> * Darbinieka ieraksti ir ievadīti un ir pieejami sistēmā
> * Darbiniekiem tiek iestatīti un tiek piešķirti tālāk norādītie dati.

> > * Apmaksas cikli un apmaksas periodi
> > * Ienākumu veida kodi
> > * Nodokļi
> > * Atvieglojumi un atvilkumi

> * Uzņēmumam ir jāizvēlas datums, kur var iestatīt algu sākuma bilances.

> * No mantojuma sistēmas tika vākta informācija par visiem ienākumiem, atvieglojumiem/atvilkumiem, atvieglojumu iemaksām, darbinieka nodokļiem un darba devēja nodokļiem, un to līdzšinējā gada (YTD) summām.

Kad plānojat ievadīt sākuma bilances, apsveriet, cik detalizētai šai informācijai ir jābūt. Vairums uzņēmumu ievada vienu, konsolidētu līdzšinējā gada summu. Taču, ja ir nepieciešama sīkāka informācija, bilances var ievadīt ar ceturkšņa pieaugumu. Lēmums par nepieciešamo detalizētības līmeni arī nosaka, cik manuālo algas pārskatu ir jāizveido katram nodarbinātajam. Vienai līdzšinējā gada summai katram darbiniekam ir nepieciešams tikai viens manuāls pārskats. Lai to izdarītu, kā jaunajā algu sistēmā ievadīto summu izmantojiet līdzšinējā gada summas no iepriekšējās sistēmas gala algas pārskata.

Nākamajā piemērā ir parādīts, kā varat ievadīt darbinieku algu sākuma bilances, tostarp ienākumu veida kodus, atvieglojumu/atvilkumus un nodokļus. Reālā piemērā jums būtu rindas krājums katram ienākumu veida kodam, atvieglojuma ieturējumam, atvieglojumu iemaksai, darbinieka nodoklim un darba devēja nodoklim, kuru ievadītā summa ir līdzšinējā gada summa. Izmantojot šo kodu un summu sarakstu, izpildiet norādījumus par manuāla ienākumu un algas pārskata izveidošanu ar atspējotu uzskaiti, lai pārceltu sākuma bilances algu nolūkiem.  Uzskaite ir jāatspējo, jo šo sākuma bilances algas pārskatu jūs nevēlaties grāmatot savā virsgrāmatā. Tas tika izdarīts mantojuma sistēmā un pārnāk uz jauno sistēmu, kad virsgrāmatā iestatāt sākuma bilances.

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a>A. Kā iestatīt ienākumu veida kodus, ko izmantot algu sākuma bilancēm
Kad ievadāt algu sākuma bilances, pārliecinieties, ka ienākumu veida kodi, kurus jūs izmantosiet, ir konfigurēti ar iespējotu opciju “Atļaut ienākumu pārskata likmju rediģēšanu”. Tas jums ļauj manuāli pielāgot summu no mantojuma sistēmas. 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a>B. Izveidot ienākumu izrakstu darbiniekam, kam nepieciešama sākuma bilance
Šī darbība manuāli izveido ienākumu izrakstu katram nodarbinātajam par mantojuma sistēmas pēdējo apmaksas periodu, tādējādi izveidojot ienākumu izraksta rindas jaunajā algu sistēmā. Ievadiet vienu rindu katram ienākumu veida kodam, kā arī līdzšinējā gada summu un stundu skaitu. Piemēra darbības ir šādas:

1. Atveriet lapu **Visu ienākumu izraksti** un noklikšķiniet uz **Jauns**.  

Ievadiet tālāk norādīto informāciju. 

| Lauks      | Vērtība                 |
|------------|-----------------------|
| Nodarbinātais     | Michael Redmond       |
| Apmaksas cikls  | sm                    |
| Apmaksas periods | 6/16/2017 - 6/30/2017 |

2. Cilnē **Ienākumu izraksta rinda** ievadiet tālāk norādīto informāciju.

1. rinda: cilne **Ienākumu izraksta rinda**

| Lauks            | Vērtība       |
|------------------|-------------|
| Ienākumu veida kods    | Regulārā samaksa |
| Daudzums         | 1,00        |
| Diapazons             | 30 000      |
| Cilne Detalizēta informācija par rindu |             |
| Manuālā           | (iezīmēts)    |

2. rinda: cilne **Ienākumu izraksta rinda**

| Lauks            | Vērtība    |
|------------------|----------|
| Ienākumu veida kods    | Bonuss    |
| Daudzums         | 1.0000   |
| Norma             | 4250.00  |
| Cilne Detalizēta informācija par rindu |          |
| Manuālā           | (iezīmēts) |

3. rinda: cilne **Ienākumu izraksta rinda**

| Lauks           | Vērtība      |
|-----------------|------------|
| Ienākumu veida kods   | Komisija |
| Daudzums        | 1.0000     |
| Norma            | !,299.00   |
| Norma            | 1,299.00   |
| Cilne Detalizēta informācija par rindu |            |
| Manuālā          | (iezīmēts)   |

> [!NOTE]
> Slīdņa **Manuāli** iestatīšana uz **Jā** cilnē **Detalizēta informācija par rindu** katrai ienākumu izraksta rindai ir veids, kā likt ievadīt algu sākuma bilances katram nodarbinātajam.

3. Rūtī **Darbība** noklikšķiniet uz **Izlaist ienākumu izrakstu** USA-FED-ER-FICA.

4. Rūtī **Darbība** noklikšķiniet uz **Algas pārskats**, lai atvērtu lapu **Ģenerēt algas pārskatus**, un iestatiet tālāk norādīto informāciju

| Lauks              | Vērtība     |
|--------------------|-----------|
| Maksājuma datums       | 6/30/2017 |
| Maksājuma izdošanas veids   | Manuālā    |
| Atspējot uzskaiti |   Jā     |

> [!NOTE] 
> Šī darbība ir pieejama tikai tad, ja maksājuma izpildes tips ir manuāls un ja lietotājs vēlaties atspējot uzskaiti par apmaksas izpildi.

Noklikšķiniet uz **Labi** un aizveriet žurnālu **Informācijas žurnāls**.

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a>Kādēļ slīdnis Atspējot uzskaiti ir jāiestata uz Jā, ģenerējot algu pārskatus?
Slīdni iestatot uz **Jā**, algas pārskatā netiek ļauta rindu izplatīšana virsgrāmatā. Virsgrāmatas summas tika atjauninātas iepriekš, kad tika ievadītas konta bilances no mantojuma sistēmas. Ievadot algu sākuma bilances, varat ģenerēt pārskatus, kuros ietverta informācija no iepriekšējiem gadiem, kā arī identificēt ierobežojumus atvieglojumu un nodokļu nolūkiem.   

### <a name="c-create-pay-statements-for-employees"></a>C. Izveidot algas pārskatus darbiniekiem
Kad ir izveidoti algas pārskati, kuriem ir sākuma bilances, ir jāpārbauda, vai šie algas pārskati precīzi atspoguļo algu datus. Tāpat jums ir manuāli jāatjaunina atvieglojumu un nodokļu informācija, lai tā atbilstu vērtībām iepriekšējā algu sistēmā. Kad esat pārbaudījis, vai summas no iepriekšējās algu sistēmas atbilst summām pašreizējos algas pārskatos, šie algas pārskati ir jāfinalizē.

1. Atveriet lapu **Visi algas pārskati**.

2. Iezīmējiet pēdējo ģenerēto algas pārskatu darbiniekam Michael Redmond

3. Noklikšķiniet uz **Rediģēt**, lai atvērtu lapu **Algas pārskats**.

4. Atveriet cilni **Atvieglojumu ieturējumi** un ievadiet tālāk norādīto informāciju.

| Lauks                           | Vērtība            |
|---------------------------------|------------------|
| Atvieglojumi                         | Ieturējuma summa |
| 401K | Piedalīties              | 3000.00          |
| Zobārstniecība | SubSp                  | 495,00           |
| Apg. aprūpes izdevumi | Piedalīties | 2500.00          |
| Redze | SupSp                  | 500,00           |

5. Cilnē **Atvieglojumu iemaksas** ievadiet tālāk norādīto informāciju.

| Lauks              | Vērtība               |
|--------------------|---------------------|
| Atvieglojumi            | Seguma summa |
| 401K | Piedalīties | 3000,00             |
| Zobārstniecība | SubSp     | 495,00              |
| Redze | SubSp     | 500,00              |

6. Cilnē **Nodokļu ieturējumi** ievadiet tālāk norādīto informāciju.

| Lauks           | Vērtība            |
|-----------------|------------------|
| Nodokļa kods        | Ieturējuma summa |
| USA-FED-ER-FICA | 1600.00          |
| USA-FED-ER-MEDI | 825.75           |

7. Cilnē **Nodokļu iemaksas** ievadiet tālāk norādīto informāciju.

8. Noklikšķiniet uz **Aprēķināt**.
> [!IMPORTANT] 
> Pārliecinieties, ka algas pārskata kopsummas atbilst mantojuma sistēmas šī nodarbinātā līdzšinējā gada kopsummām. Iespējams, finalizēšana ir jāatliek uz nākamo darbību, lai veiktu visu algas pārskatu vispārēju validēšanu kopumā. Pēc validēšanas izejiet cauri visiem algas pārskatiem un finalizējiet tos.

Šo pašu procedūru var veikt ar ceturkšņa intervāliem, ja nepieciešams, visiem iepriekšējiem ceturkšņiem katru gadu. Tas ir jādara tikai tad, ja klientam ir nepieciešams datus redzēt pa ceturksnim, neatgriežoties mantojuma sistēmā.

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a>Ja pieļaujat kļūdu, ievadot darbinieka sākuma bilances
Transakcijas ir iespējams atsaukt un ievadīt no jauna. Lai transakciju atsauktu, jums ir tikai jāizpilda tālāk norādītās darbības lapā **Visi algas pārskati**.

1. Noklikšķiniet uz **Atsaukt**.

2. Noklikšķiniet uz **Jā**, kad tiek parādīts ziņojums “Kad anulējat šo algas pārskatu, tiek izveidots anulēšanas algas pārskats, lai kompensētu šo algas pārskatu. Nevienu no algas pārskatiem nevar rediģēt. Vai vēlaties anulēt šo samaksas pārskatu?” 

Pēc algas pārskata anulēšanas varat ģenerēt jaunu nodarbinātā algas pārskatu no iepriekš izveidotā ienākumu izraksta. Pirms ģenerējat jauno algas pārskatu, noteikti labojiet visas nepareizās ienākumu izraksta rindas, un pēc tam ģenerējiet jauno algas pārskatu ar pareizajām summām. 

