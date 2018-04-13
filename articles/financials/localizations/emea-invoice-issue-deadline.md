---
title: "Rēķina izsniegšanas termiņš"
description: "Šajā rakstā ir izskaidrots, kā iestatīt parametrus, lai aprēķinātu izpildes termiņus kreditoru un debitori rēķinu izrakstīšanai Eiropas Savienībā (ES)."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustParameters, LedgerInvoiceIssueDueDateSetup_W
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 10923
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Iceland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 34dac634e09a8daa8a22b9f1efbc18ca44444e21
ms.contentlocale: lv-lv
ms.lasthandoff: 03/26/2018

---

# <a name="invoice-issue-deadline"></a>Rēķina izsniegšanas termiņš

[!INCLUDE [banner](../includes/banner.md)]

Šajā rakstā ir izskaidrots, kā iestatīt parametrus, lai aprēķinātu izpildes termiņus kreditoru un debitori rēķinu izrakstīšanai Eiropas Savienībā (ES).

Saskaņā ar Eiropas Savienības (ES) Direktīvu 45/2010 un citām direktīvām rēķinu par piegādēm Eiropas Savienībā (piegādes ES) izsniedz ne vēlāk kā tā mēneša piecpadsmitajā dienā, kas ir pēc mēneša, kurā tiek veikta piegāde. ES valstīs rēķinu izrakstīšanas termiņi iekšzemes piegādēm var atšķirties. Rēķina izrakstīšanas izpildes termiņa funkcionalitāte ļauj saskaņot datumu intervālu valsts/reģiona veidam. Pēc tam visām piegādēm uz noteikta veida valsti/reģionu un no tā rēķina izsniegšanas izpildes termiņš tiek aprēķināts, izmantojot kārtulas, kas tiek iestatītas norādītajā datumu intervālā. Varat arī saņemt visas pavadzīmes, kurām ir noteikts rēķina izrakstīšanas izpildes termiņš, filtrēt pēc rēķina izrakstīšanas izpildes termiņa periodisko pārdošanas rēķinu izrakstīšanas laikā, kā arī kontrolēt pārdošanas rēķina izrakstīšanas termiņu rēķina grāmatošanas laikā. Varat iestatīt datumu intervāla kodu un pēc tam iestatīt aprēķina kārtulu rēķina izrakstīšanas termiņam, piešķirot datumu intervāla kodu valsts/reģiona veidam. Aprēķināšanas nosacījums tiek izmantots, lai aprēķinātu izpildes datumu izrakstītajiem rēķiniem par šādām transakcijām:

-   Piegādes ES
-   Iekšzemes sūtījumi ES dalībvalsts ietvaros

Varat iestatīt arī datumu kontroles, lai nodrošinātu, ka debitoru rēķini un kredīta notas debitoru transakcijām tiek ģenerēti noteiktā periodā pēc piegādes veikšanas.

## <a name="prerequisites"></a>Priekšnosacījumi
Tālāk redzamajā tabulā ir ietverti priekšnosacījumi, kas jāievēro, lai izmantotu rēķina izrakstīšanas izpildes termiņa funkcionalitāti.

| Kategorija            | Priekšnosacījums                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Valsts/reģions      | Juridiskās personas primārajai adresei ir jāatrodas ES dalībvalstī.                                                                                                                                                                                                                                                                                                                    |
| Saistītie iestatīšanas uzdevumi | Lapā **Datumu intervāli** iestatiet datumu intervālu, ko izmanto rēķina izrakstīšanas izpildes termiņa aprēķināšanā. (Noklikšķiniet uz **Virsgrāmata** &gt; **Virsgrāmatas iestatīšana** &gt; **Datumu intervāli**.) Lapā **Ārējās tirdzniecības parametri** iestatiet ārējās tirdzniecības rekvizītus dažādām valstīm/reģioniem. (Noklikšķiniet uz **Nodokļi** &gt; **Iestatīšana** &gt; **Ārējā tirdzniecība** &gt; **Ārējās tirdzniecības parametri**.) |

## <a name="invoice-issue-due-date-calculation-rule"></a>Rēķina izrakstīšanas izpildes datuma aprēķināšanas nosacījums
Izmantojiet lapu **Iestatīt rēķina izrakstīšanas izpildes termiņa aprēķinu**, lai iestatītu rēķina izrakstīšanas izpildes termiņa aprēķina kārtulu, piešķirot datumu intervāla kodu valsts/reģiona veidam.

## <a name="date-control-parameters-for-customer-invoices-and-credit-notes"></a>Datumu kontroles parametri debitora rēķiniem un kredīta notām
Varat iestatīt arī datumu kontroles parametrus, lai nodrošinātu, ka debitoru rēķini un kredīta notas debitoru transakcijām tiek ģenerēti noteiktā periodā pēc piegādes veikšanas. Šie parametri ir pieejami lapas **Debitoru moduļa parametri** apgabalā **Rēķinu datumu kontrole**.

## <a name="example"></a>Paraugs
Lai programmā Microsoft Dynamics 365 for Finance and Operations iestatītu, ka sūtījumiem ES robežās rēķina izrakstīšanas izpildes termiņi tiek aprēķināti tā mēneša piecpadsmitajā dienā, kas ir pēc sūtījuma piegādāšanas, izveidojiet datumu intervāla kodu un aprēķina kārtulu ar tālāk sniegtajiem iestatījumiem.

### <a name="date-interval-code"></a>Datumu intervāla kods

| Lauks                                                           | Vērtība                           |
|-----------------------------------------------------------------|---------------------------------|
| Datumu intervāla kods                                              | 15-NM                           |
| Apraksts                                                     | Nākamā mēneša iecpadsmitā diena |
| Līdz (lauku grupā **Līdz datumam**)                         | Mēnesis                           |
| Sākums/Beigas (lauku grupā **Līdz datumam**)                      | Beigt                             |
| +/- (lauku grupā **Līdz datumam**)                            | 15.                              |
| Dienas, mēneši, gadi vai periodi (lauku grupā **Līdz datumam**) | Dienas                            |

### <a name="invoice-issue-due-date-calculation-rule"></a>Rēķina izrakstīšanas izpildes datuma aprēķināšanas nosacījums

| Lauks               | Vērtība                                                     |
|---------------------|-----------------------------------------------------------|
| Valsts/reģiona veids | **ES**                                                    |
| Sākuma datums          | Ievadiet datumu, kad pašreizējā iestatījumu rinda stājas spēkā. |
| Datumu intervāla kods  | **15 NM**                                                 |

## <a name="next-steps"></a>Turpmākās darbības
Pēc tam, kad esat beidzis iestatīt parametrus, lai aprēķinātu rēķina izrakstīšanas izpildes termiņus, varat izveidot un grāmatot tālāk norādītās transakcijas, lai automātiski aprēķinātu un atjauninātu izpildes termiņus rēķinu izrakstīšanai.

-   **Pārdošanas pasūtījumi** — kad jūs izveidojat pārdošanas pasūtījumu un grāmatojat pavadzīmi, tajā tiek aprēķināts un atjaunināts izpildes datums rēķina izrakstīšanai. Izpildes datums tiek aprēķināts, pamatojoties uz datumu intervālu, kurš ir saistīts ar pārdošanas pasūtījuma piegādes adresē norādīto valsti/reģionu. Pēc pavadzīmes iegrāmatošanas varat pārbaudīt rēķina izrakstīšanas izpildes termiņu lapas **Pavadzīmju žurnāls** laukā **Rēķina izrakstīšanas izpildes termiņš**. (Noklikšķiniet uz **Pārdošana un mārketings** &gt; **Pārdošanas pasūtījums** &gt; **Pasūtījuma nosūtīšana** &gt; **Pavadzīme**.) Visas pavadzīmes, kuras nav iekļautas rēķinā, un to rēķinu izrakstīšanas izpildes termiņus varat apskatīt lapā **Pavadzīmes nav iekļautas rēķinā**. (Noklikšķiniet uz **Pārdošana un mārketings** &gt; **Pārdošanas pasūtījums** &gt; **Pasūtījuma piegāde** &gt; **Pavadzīmes nav iekļautas rēķinā**.)
-   **Pirkšanas pasūtījumi** — kad jūs izveidojat pirkšanas pasūtījumu un grāmatojat preces kvīti, tajā tiek aprēķināts un atjaunināts izpildes datums rēķina izrakstīšanai. Izpildes termiņš tiek aprēķināts, pamatojoties uz datumu intervālu, kas ir saistīts ar valsti/reģionu, kas ir norādīts kreditora primārajā adresē. Pēc produktu ieejas plūsmas grāmatošanas varat pārbaudīt rēķina izrakstīšanas izpildes termiņu lapas **Produktu ieejas plūsmas žurnāls** laukā **Rēķina izrakstīšanas izpildes termiņš**. (Noklikšķiniet uz **Sagāde un avoti** &gt; **Pirkšanas pasūtījumi** &gt; **Preču saņemšana** &gt; **Produktu ieejas plūsma**.) Visas produktu ieejas plūsmas, kuras nav iekļautas rēķinā, un to rēķinu izrakstīšanas izpildes termiņus varat apskatīt lapā **Produktu ieejas plūsmas nav iekļautas rēķinā**. (Noklikšķiniet uz **Sagāde un avoti** &gt; **Pirkšanas pasūtījumi** &gt; **Preču saņemšana** &gt; **Preču ieejas plūsmas nav iekļautas rēķinā**.)

## <a name="technical-information-for-system-administrators"></a>Tehniskā informācija sistēmas administratoriem
Ja nevarat piekļūt lapām, kas tiek izmantotas šajā rakstā minēto uzdevumu izpildīšanai, sazinieties ar sistēmas administratoru un sniedziet nākamajā tabulā redzamo informāciju.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Kategorija</th>
<th>Priekšnoteikumi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Configuration Keys</td>
<td>Noklikšķiniet uz <strong>Sistēmas administrēšana</strong> &gt; <strong>Iestatīšana</strong> &gt; <strong>Licencēšana</strong> &gt; <strong>Licences konfigurācija</strong>. Noklikšķiniet uz konfigurācijas atslēgas <strong>Virsgrāmatas</strong>.</td>
</tr>
<tr class="even">
<td>Drošības lomas un pienākumi</td>
<td>Lai veiktu šo uzdevumu, jums ir jābūt piešķirtai drošības lomai, kurā ietilpst šādi pienākumi:
<ul>
<li><strong>CustInvoiceInvoiceAndCashProcessEnable</strong> (Iespējot rēķinu un skaidras naudas procesu)</li>
<li><strong>VendInvoiceInvoicePaymentProcessEnable</strong> (Iespējot rēķinu un maksājuma procesu)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Drošības lomas un privilēģijas</td>
<td>Lai veiktu šo uzdevumu, jums ir jābūt piešķirtai drošības lomai, kurā ietilpst šādas privilēģijas:
<ul>
<li><strong>CustPackingSlipJournalView</strong> (Skatīt pārdošanas pavadzīmes)</li>
<li><strong>VendPackingSlipJournalView</strong> (Skatīt pirkšanas pasūtījuma preču kvīšu žurnālu)</li>
<li><strong>LedgerInvoiceIssueDueDateSetupMaintain_W</strong> (Aprēķināt rēķina izrakstīšanas izpildes termiņus)</li>
</ul></td>
</tr>
</tbody>
</table>






