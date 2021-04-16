---
title: Pasūtījumu izveides termiņi
description: Šajā rakstā ir sniegta informācija par pasūtījuma izveides termiņiem. Pasūtījuma izveides termiņš ir pēdējais laiks, kas nosaka, vai debitora pasūtījums tiek apstrādāts (un izpildīts) tā, it kā tas būtu jāsaņem šodien vai nākamajā dienā.
author: omulvad
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventOrderEntryDeadlineGroup, InventOrderEntryDeadlineParameters, InventOrderEntryDeadlineTable, MCRAutoTaxRules
audience: Application User
ms.reviewer: kamaybac
ms.custom: 7151
ms.assetid: bbc4f9a2-df4b-4d92-9f18-25282a85541f
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cf2780edc75891d565a184135d6a915a0e6f8504
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839081"
---
# <a name="order-entry-deadlines"></a>Pasūtījumu izveides termiņi

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegta informācija par pasūtījuma izveides termiņiem. Pasūtījuma izveides termiņš ir pēdējais laiks, kas nosaka, vai debitora pasūtījums tiek apstrādāts (un izpildīts) tā, it kā tas būtu jāsaņem šodien vai nākamajā dienā.

Daudzos uzņēmumos attiecīgajā dienā tiek apstrādāti tikai tie pārdošanas pasūtījumi, kas saņemti pirms noteikta dienas laika. Visi pasūtījumi, kas tiek saņemti pēc šī laika, tiek apstrādāti kā nākamajā darba dienā saņemti pasūtījumi. Šis pēdējais laiks pasūtījumiem tiek dēvēts par pasūtījuma izveides termiņu.  

Pasūtījuma izveides termiņi tiek izmantoti kā ievades dati pasūtījumu solīšanai. Šie termiņi ir noderīgi klientu informēšanai par pasūtījumu piegādes laiku. Piemēram, klienti var redzēt, ka, veicot pasūtījumu pie jums pirms noteikta laika, jūs apņematies veikt preču piegādi tajā pašā dienā. Taču, ja viņi nokavē šo termiņu, viņi saņems sūtījumu tikai nākamajā darba dienā. Pasūtījumu izveides termiņi ir jāiestata, pamatojoties uz noliktavas iespējām un sūtījumu pārvadātāja grafikiem.  

Lapā **Pasūtījumu izveides termiņi** iestatiet pasūtījumu izveides beigu termiņa laikus visām nedēļas dienām. Ja pasūtījumi tiek saņemti pēc šiem norādītajiem laikiem, tie tiks apstrādāti kā nākamajā darba dienā saņemti pasūtījumi. Pēc noklusējuma šie laiki ir iestatīti uz 23.59, proti, vienu minūti pirms pusnakts attiecīgās dienas beigās. Noklusētos laikus var mainīt, lai tie atbilstu faktiskajiem nosūtīšanas vai saņemšanas beigu termiņa laikiem.  

Jūs varat noteikt pasūtījumu izveides termiņus noteiktai debitoru grupai. Piemēram, iespējams, ka vēlēsities, lai noteiktai klientu grupai pasūtījumu izveides beigu termiņi ir vēlāk nekā citiem klientiem. Šajā gadījumā lapā **Pasūtījumu izveides termiņu grupas** vispirms jādefinē pasūtījumu izveides termiņu grupas. Pēc tam grupas var piešķirt klientiem lapā **Klienti**.  

Ja jūsu uzņēmums darbojas vairākās vietās, katrai no tām varat iestatīt savu pasūtījuma izveides beigu termiņu. Ja vietas atrodas dažādās laika joslās, pasūtījumu izveides termiņi tiek iestatīti katras vietas atbilstošajā laika joslā. Tomēr, strādājot ar pārdošanas pasūtījumiem un pārdošanas piedāvājumiem, pasūtījumu izveides beigu termiņš tiks mainīts atbilstoši jūsu laika joslai lapā **Pieejamie nosūtīšanas un saņemšanas datumi**.  

Lapā **Aktivizēt pasūtījumu izveides termiņu kombinācijas** definējiet atļautās vietu un pasūtījumu izveides termiņu grupu kombinācijas.

## <a name="example-order-entry-deadline"></a>Piemērs. Pasūtījumu izveides termiņš
Pasūtījumu izveides termiņš otrdienās noteikts uz 16.00. Konkrētā otrdienā plkst. 17.00 mēģiniet iestatīt pašreizējo datumu kā nosūtīšanas datumu. (Ņemiet vērā, ka šī piemēra ietvaros nav izpildes laika.) Ja ir atzīmēta izvēles rūtiņa **Piegādes datuma kontrole**, saņemat brīdinājumu par to, ka datums nav derīgs. Šis brīdinājums tiks parādīts lapā **Pieejamie nosūtīšanas un saņemšanas datumi**, kur pēc tam varēsit izvēlēties citus datumus.

## <a name="example-different-order-entry-deadlines-per-site"></a>Piemērs. Katrā vietā citi pasūtījumu izveides termiņi
Jūsu uzņēmumam ir divas atrašanās vietas. Vietas atrodas dažādās laika joslās, kā parādīts turpmākajā tabulā.

| Vieta A                      | Vieta B                      |
|-----------------------------|-----------------------------|
| Kalifornija                  | Florida                     |
| PST (Klusā okeāna standarta laiks) | EST (Austrumu standarta laiks) |

A un B vieta ir definējusi šādus pasūtījumu izveides termiņus.

| Nedēļas diena             | A: pasūtījumu izveides termiņi (PST) | B: pasūtījumu izveides termiņi (EST) |
|-----------------------------|--------------------------------|--------------------------------|
| Pirmdiena                      | 13.00                          | 14.00                          |
| Otrdiena                     | 13.00                          | 14.00                          |
| Trešdiena                   | 13.00                          | 14.00                          |
| Ceturtdiena                    | 13.00                          | 14.00                          |
| Piektdiena                      | 13.00                          | 14.00                          |

Jūs esat pasūtījumu operators Jutā, kur laika josla ir MST (Kalnu standarta laiks). Tādēļ, pieņemot, ka veicat pasūtījumus A vietā pirms 14.00 MST un izdarāt pasūtījumus B vieta pirms 12.00 MST, ievērosit abu vietu pasūtījumu izveides termiņus.  

Tabulā parādīts, kā pasūtījumu izveides termiņi A un B vietā tiek pārveidoti uz MST laiku.

| A vieta: PST         | A vieta: MST        | B vieta: EST           | B vieta: MST        |
|---------------------|--------------------|-----------------------|--------------------|
| 13.00               | 14.00              | 14.00                 | 12.00              |

**Piezīme.** Ja ir spēkā pāreja uz vasaras laiku, pasūtījuma izveides beigu termiņi tiek atbilstoši pielāgoti

## <a name="example-same-order-entry-deadline-per-site"></a>Piemērs. Visās vietās vienāds pasūtījumu izveides beigu termiņš
Jūsu uzņēmumam ir divas atrašanās vietas. Vietas atrodas dažādās laika joslās, kā parādīts turpmākajā tabulā.

| Vieta A                      | Vieta B                      |
|-----------------------------|-----------------------------|
| Kalifornija                  | Florida                     |
| PST (Klusā okeāna standarta laiks) | EST (Austrumu standarta laiks) |

A un B vieta ir definējusi šādus pasūtījumu izveides termiņus.

| Nedēļas diena | PST un EST |
|-----------------|-------------|
| Pirmdiena          | 13.00       |
| Otrdiena         | 13.00       |
| Trešdiena       | 13.00       |
| Ceturtdiena        | 13.00       |
| Piektdiena          | 13.00       |

Jūs esat pasūtījumu operators Jūtā, kur laika josla ir MST. Tādēļ, pieņemot, ka veicat pasūtījumus A vietā pirms 14.00 MST un izdarāt pasūtījumus B vieta pirms 11.00 MST, ievērosit abu vietu pasūtījumu izveides termiņus. 

Tabulā parādīts, kā pasūtījumu izveides termiņi A un B vietā tiek pārveidoti uz MST laiku.

| A vieta: PST         | A vieta: MST        | B vieta: EST           | B vieta: MST        |
|---------------------|--------------------|-----------------------|--------------------|
| 13.00               | 14.00              | 13.00                 | 11.00              |

**Piezīme.** Ja ir spēkā pāreja uz vasaras laiku, pasūtījuma izveides beigu termiņi tiek atbilstoši pielāgoti

<a name="additional-resources"></a>Papildu resursi
--------

[Piegādes grafiki](delivery-schedules.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]