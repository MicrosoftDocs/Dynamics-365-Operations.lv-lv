---
title: "Pārdošanas līgumi"
description: "Šajā rakstā ir sniegta informācija par pārdošanas līgumiem. Pārdošanas līgums ir līgums, ar kuru debitors piekrīt laika gaitā iegādāties noteiktu daudzumu preču vai iegādāties preces par noteiktu summu apmaiņā pret īpašām cenām un atlaidēm."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesAgreement, SalesAgreementGenerateReleaseOrder, SalesAgreementListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 9554
ms.assetid: c5d55c8d-99f2-44f9-a897-5b0dee85fc81
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 15e3f872e4ded027734ee73081ba7af68be5107d
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="sales-agreements"></a>Pārdošanas līgumi

[!include[banner](../includes/banner.md)]


Šajā rakstā ir sniegta informācija par pārdošanas līgumiem. Pārdošanas līgums ir līgums, ar kuru debitors piekrīt laika gaitā iegādāties noteiktu daudzumu preču vai iegādāties preces par noteiktu summu apmaiņā pret īpašām cenām un atlaidēm.

Pārdošanas līgums ir vienošanās, kas nosaka, ka laika gaitā klientam jāiegādājas preces noteiktā daudzumā vai par konkrētu summu apmaiņā pret īpašām cenām, īpašām atlaidēm un citiem īpašiem nosacījumiem, piemēram, maksājuma un piegādes nosacījumiem. Pārdošanas līguma cenām un atlaidēm ir prioritāte pār jebkādām cenām un atlaidēm, kas ir norādītas jebkuros jau pastāvošajos tirdzniecības līgumos.  

Pārdošanas līguma derīguma termiņu nosaka līguma laukā **Spēkā stāšanās datums** un **Beigu datums**. Klienta pārdošanas pasūtījums atbilst līguma nosacījumiem, ja pasūtījumā pieprasītais nosūtīšanas datums ir derīguma periodā. Visas pārdošanas pasūtījuma rindas, kas ir saistītas ar pārdošanas līgumu ir svarīgas šī pārdošanas līguma izpildei.  

Pārdošanas pasūtījumu var izveidot tieši no pārdošanas līguma, izmantojot darbību **Izveidot izpildpasūtījumu**. Vai arī varat atlasīt spēkā esošo pārdošanas līgumu, pieņemot pasūtījumus (skatiet šī raksta sadaļu “Pārdošanas līgumu lietošana pasūtīšanas procesā”).  

**Piezīme.** Iepriekšējās versijās pārdošanas līgumi tika saukti par padošanas pasūtījumu plāniem.

## <a name="commitment-types"></a>Saistību veidi
Katra pārdošanas līguma rinda norāda saistības kaut ko pārdot. Parasti ir divas saistību kategorijas:

-   **Uz vērtību attiecināmās saistības** — klients piekrīt iegādāties preces par konkrētu summu.
-   **Uz daudzumu attiecināmas saistības** — klients piekrīt iegādāties noteiktu daudzumu preču.

Turklāt līgums var uzlikt par pienākumu klientam iegādāties noteiktu preču kategorijas preci vai preces. Apvienojot šos divus faktorus (vērtība pret daudzumu un konkrētas preces pret preču kategorijām), iegūstam četru veidu saistības.

-   **Uz preču daudzumu attiecināmas saistības** — klients piekrīt iegādāties noteiktu daudzumu preču. Rindas, kas lieto šo saistību veidu, tiek definētas pēc krājuma koda un daudzuma un vienības, par ko tika panākta vienošanās. Lauks **Summa** nav pieejams.
-   **Uz preču vērtību attiecināmas saistības** — klients piekrīt iegādāties konkrētas preces par konkrētu summu. Rindas, kas lieto šo saistību veidu, tiek definētas pēc krājuma koda un summas, par ko tika panākta vienošanās. Lauks **Daudzums** un **Vienība** nav pieejams.
-   **Uz preces kategorijas vērtību attiecināmās saistības** — klients piekrīt iegādāties konkrētas pārdošanas kategorijas preces par konkrētu summu. Rindas, kas lieto šo saistību veidu, tiek definētas pēc pārdošanas kategorijas pārdošanas kategoriju hierarhijā un summas. Lauks **Daudzums** un **Vienība** nav pieejams.
-   **Uz vērtību attiecināmās saistības** — klients piekrīt iegādāties jebkuru preci vai preces jebkurā sagādes kategorijā par konkrētu summu. Lauks **Daudzums** un **Vienība** nav pieejams.

Tā pašas pārdošanas līguma rindām var būt dažāda veida saistības.

## <a name="pricing-terms-for-sales-agreements"></a>Cenu noteikšanas nosacījumi pārdošanas līgumiem
Cenu noteikšanas nosacījumi var atšķirties atkarībā no saistību veida. Pārdošanas pasūtījumā, kas piesaistīts pārdošanas līgumam, pārdošanas līguma cenu noteikšanas nosacījumiem ir prioritāte pār jebkuriem citiem cenu noteikšanas nosacījumiem, kas tiek lietoti, pamatojoties uz tirdzniecības līgumiem. Šajā tabulā ir aprakstīti ar cenu saistītie lauki, kurus ietekmē katrs saistību veids. “Jā” norāda, ka lauku var atjaunināt pasūtījuma rindā.

| Saistību veids                   | Vienības cena | Cenas vienība | Atlaides procents | Termiņatlaides summa |
|-----------------------------------|------------|------------|------------------|----------------------|
| Uz preču daudzumu attiecināmas saistības       | Jā        | Jā        | Jā              | Jā                  |
| Uz preču vērtību attiecināmas saistības          |            |            | Jā              |                      |
| Uz preces kategorijas vērtību attiecināmās saistības |            |            | Jā              |                      |
| Uz vērtību attiecināmās saistības                  |            |            | Jā              |                      |

## <a name="policies-for-sales-agreements"></a>Pārdošanas līgumu ierobežojumi
Šādi ierobežojumi ietekmē veidu, kā darbojas saistība starp pirkšanas līguma saistībām un atbilstošajām pirkšanas pasūtījuma rindām.

-   **Sasniegts maksimums** — kopējais daudzums vai summa visās pasūtījuma rindās nevar pārsniegt to daudzumu vai summu, kas ir norādīti piesaistītajās saistībās.
-   **Cena un atlaide ir fiksēta** — cenai pasūtījuma rindā ir jābūt vienādai ar cenu piesaistītajās saistībās. Ja pasūtījuma rindā tiek mainīta cena, saikne ar saistībām tiek bojāta. Ja saikne ir bojāta, pasūtījuma rinda netiek izmantota saistību pildīšanai.
-   **Minimālā izlaišanas summa** un **Maksimālā izlaišanas summa** — ja ir norādīta summa, jūs saņemat ziņojumu gadījumā, ja kādā pasūtījuma rindā veicat jebkādas izmaiņas, kuru dēļ pasūtījuma rinda atšķiras no piesaistītajām saistībām.

## <a name="fulfillment-calculations-for-sales-agreements"></a>Pārdošanas līgumu izpildes aprēķini
Izpildes daudzumi un summas tiek rādīti cilnē **Izpilde**, kopsavilkuma cilnē **Detalizēta informācija par rindu**, kas atrodas lapā **Pirkšanas līgumi**.  

Apgabalā **Izpilde** varat skatīt kopējos daudzumus un summas visām pasūtījuma rindām, kas ir piesaistītas norādītajam pārdošanas līgumam. Varat arī skatīt atlikušo summu vai daudzumu, kas ir nepieciešams, lai izpildītu saistības.  

Apgabalā **Līgums** varat skatīt norādītā pārdošanas līguma daudzumus un summas. Šie daudzumi un summas ir kopējie daudzumi un summas, kas ir noteikti saistībās.

## <a name="confirmations-and-version-history-for-sales-agreements"></a>Pārdošanas līgumu apstiprinājumi un versiju vēsture
Apstiprinot pārdošanas līgumu, tā pašreizējā versija tiek saglabāta vēstures tabulā un tai tiek piešķirts versijas numurs. Ja maināt pārdošanas līgumu, varat apstiprināt to vēlreiz, lai vēsturē saglabātu citu pārdošanas līguma versiju.  

Ja neapstiprināt pārdošanas līgumu, joprojām to varat izmantot, lai izveidotu pārdošanas pasūtījumus. Tomēr pārdošanas līguma vēstures informācija netiek saglabāta.  

Varat priekšskatīt vai drukāt visus apstiprinājumu pārskatījumus. Pēc tam pārskatījumus varat koplietot ar debitoru, lai saņemtu apstiprinājumu.

## <a name="applying-sales-agreements-during-the-ordering-process"></a>Pārdošanas līgumu lietošana pasūtīšanas procesā
Ja pārdošanas pasūtījumi netiek nodoti izpildei tieši pārdošanas līgumiem, pārdošanas līgumu joprojām var piesaistīt pasūtījumam pasūtījuma izveides procesa laikā. Veidojot jaunu pārdošanas pasūtījumu un atlasot pārdošanas līgumu, pasūtījuma virsrakstā lieto līguma nosacījumus, piemēram, maksājuma nosacījumus, piegādes nosacījumus un piegādes adresi, un tiek izveidota saite starp līgumu un pasūtījumu. Pēc tam, kad ir iespējams atlasīt preces un kategorijas, pasūtījuma rindās, kas norādītas pārdošanas līgumā, tiek iekopētas cenas un atlaides no attiecīgā līguma. Vienā pārdošanas pasūtījumā var iekļaut gan rindas, kas nav saistītas ar pārdošanas līgumu, gan rindas, kas ir saistītas ar pārdošanas līgumu.

## <a name="modifying-sales-orders-that-are-linked-to-sales-agreements"></a>Ar pārdošanas līgumiem saistītu pārdošanas pasūtījumu modificēšana
Ja esat izveidojis (izsniedzis) pārdošanas pasūtījumu atbilstoši pārdošanas līgumam, dažus laukus šajās pārdošanas pasūtījumu rindās var modificēt tikai tad, ja noņemsit saiti uz saistītajām pārdošanas līguma rindām. Šajā tabulā ir uzskaitīti daži no šiem laukiem.

| Lauks                                                             | Apraksts                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pieprasītais nosūtīšanas datums                                               | Ja maināt pieprasīto nosūtīšanas datumu uz datumu, kas ir agrāks par **spēkā stāšanās datuma** vērtību pārdošanas līguma rindā, ir jānoņem saite uz pārdošanas līguma rindu pirms mainītā nosūtīšanas datuma saglabāšanas. Ja maināt pieprasīto nosūtīšanas datumu uz datumu, kas ir vēlāks par **beigu datuma** vērtību pārdošanas līguma rindā, ir jānoņem saite uz pārdošanas līguma rindu pirms mainītā nosūtīšanas datuma saglabāšanas. |
| CurrencyDiscount, percentDiscountUnit, pricePrice, unitNet summa | Ja maināt vērtību jebkurā no šiem laukiem un saistītā pārdošanas līguma rindā ir atzīmēta izvēles rūtiņa **Cena un atlaide ir fiksēta**, ziņojuma lodziņš piedāvā saglabāt izmaiņas. Noklikšķiniet uz **Jā**, lai noņemtu saiti uz pārdošanas līguma rindu un pārrēķinātu cenu. Noklikšķiniet uz **Nē**, lai noņemtu saiti uz pārdošanas līguma rindu, nepārrēķinot cenu.                                                                   |
| Neto summa                                                        | Ja norādāt summu, kas pārsniedz to, kas norādīta pārdošanas līguma rindā, kur ir atzīmēta izvēles rūtiņa **Sasniegts maksimums**, ziņojuma lodziņš piedāvā saglabāt mainīto summu. Noklikšķiniet uz **Jā**, lai noņemtu saiti uz pārdošanas līguma rindu un pārrēķinātu cenu. Noklikšķiniet uz **Nē**, lai noņemtu saiti uz pārdošanas līguma rindu, nepārrēķinot cenu.                                                                 |
| Daudzums                                                          | Ja norādāt daudzumu, kas pārsniedz to, kas norādīts pārdošanas līguma rindā, kur ir atzīmēta izvēles rūtiņa **Sasniegts maksimums**, ziņojuma lodziņš piedāvā saglabāt mainīto daudzumu. Noklikšķiniet uz **Jā**, lai noņemtu saiti uz pārdošanas līguma rindu un pārrēķinātu cenu. Noklikšķiniet uz **Nē**, lai noņemtu saiti uz pārdošanas līguma rindu, nepārrēķinot cenu.                                                            |

## <a name="returning-an-item-that-was-ordered-from-a-sales-agreement"></a>Krājuma, kas tika pasūtīts pārdošanas līgumā, nodošana atpakaļ
Kad klients atgriež preci, kas tika pasūtīta no pārdošanas līguma, programmatūrā Microsoft Dynamics 365 for Finance and Operations var tikt atrastas un automātiski atjauninātas saistītās pārdošanas līguma saistības, lai atainotu daudzuma vai summas izmaiņas. Ja izveidojat atgriešanas pasūtījumu, pamatojoties uz sākotnējo pārdošanas pasūtījumu, kas ir piesaistīts pārdošanas līgumam, tiek izveidota relācija starp pārdošanas līguma saistību, pārdošanas pasūtījuma rindu un atgriešanas pasūtījuma rēķinu.  

Ja nevēlaties, lai atgriezto krājumu daudzumu ieturētu no pārdošanas līguma saistībām, var izmantot vadīklu **Noņemt saiti** lapā **Atgriezt pasūtījumu**, lai noņemtu saiti starp pasūtījumu un pārdošanas līguma saistībām. Ja jums ir vēlāk atkārtoti jāizveido saite, noklikšķinot uz **Izveidot saiti**.  

**Piezīme.** Atgriešanas pasūtījumu var saistīt tikai ar vienu pārdošanas līgumu.. Ja klients atgriež vairākas preces, kas tika pasūtītas no vairākiem pārdošanas līgumiem, ir jāizveido jauns atgriešanas pasūtījums katrai precei un jāizveido saite uz atbilstošo pārdošanas līgumu.

## <a name="automatic-search-for-sales-agreements"></a>Pārdošanas līgumu automātiskā meklēšana
Dažās situācijās, kad pārdošanas pasūtījumi tiek izveidoti netiešā veidā, piemēram, izveidojot kredīta notu vai starpuzņēmumu pārdošanas pasūtījumus, varat kontrolēt, vai programmatūrā Microsoft Dynamics 365 for Finance and Operations tiek automātiski meklēti lietojamie pārdošanas līgumi.

## <a name="financial-dimensions-on-sales-agreements"></a>Pārdošanas līgumu finanšu dimensijas
Finanšu dimensijas varat kopēt pārdošanas līguma dokumentu galvenēs vai atsevišķās rindās. Dimensijas uz līguma virsraksta vai līguma rindā var mainīt jebkurā laikā. Šajā gadījumā dimensijas tiek automātiski iekopētas izpildei nodoto pasūtījumu izpildpasūtījuma galvenē vai rindā.




