---
title: "Cenas simulācija"
description: "Šajā rakstā ir sniegta informācija par cenu simulāciju piedāvājumiem. Cenu simulācija jums piedāvājuma procesa laikā palīdz novērtēt ieturējumu ietekmi uz turpmāku pārdošanas cenu, pirms piekrītat lietot noteiktu cenu."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesQuotationPriceSimulation
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 12254
ms.assetid: 92be7c85-73cf-4f77-833c-d37ce779a031
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 1db68ea5728cc417f0e70675d9074d5b054883da
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="price-simulation"></a>Cenas simulācija

[!include[banner](../includes/banner.md)]


Šajā rakstā ir sniegta informācija par cenu simulāciju piedāvājumiem. Cenu simulācija jums piedāvājuma procesa laikā palīdz novērtēt ieturējumu ietekmi uz turpmāku pārdošanas cenu, pirms piekrītat lietot noteiktu cenu.

Piedāvājuma cenas simulācija rāda jaunu kopsummu, balstoties uz ierosināto jauno cenu. Cenas simulācija var arī rādīt jaunas summas noteiktai rindai, kas ir izveidota esošā piedāvājumā. Cenas simulāciju varat ievadīt un to lietot vēlāk. Alternatīvi varat izmantot oriģinālo piedāvājumu bez cenas simulācijas un izdarīt papildu izmaiņas, kad veicat pārdošanas procesu kopā ar klientu.  

Cenas simulācija nemaina cenu piedāvājumā. Ja cenas simulācija tiek lietota visam piedāvājumam, tā tiek apstrādāta kā īpaša atlaide piedāvājuma virsrakstā. Ja cenas simulācija tiek lietota noteiktiem krājumiem, tā tiek apstrādāta kā īpaša atlaide piedāvājuma rindās. Kad tiek lietota cenas simulācija, jau izveidotā vienības pārdošanas cena piedāvājuma rindā nemainās. Tā vietā tiek pielietoti atlaides procenti, kas attiecas uz cenas samazinājumu kotācijas rindā. Kad tiek lietota cenas simulācija, vienības pārdošanas cena un atlaides procenti tiek pārsūtīti uz piedāvājuma rindu vai piedāvājuma virsrakstu.  

**Piezīme.** Kad palaižat cenas simulāciju, simulācijas izveidei tiek izmantota tikai pašreizējā pārdošanas valūta. Taču, kad apskatāt piedāvājuma kopsummas, redzat uzņēmuma valūtas un pārdošanas valūtas kombināciju.  

Papildu krājumi, kas tiek pievienoti piedāvājuma rindām, var izraisīt rindas atlaides vai vairākrindu atlaides. Tie var izraisīt arī kopējās atlaides, kas maina piedāvājuma rindu un visas atlaides seguma summas un seguma summas likmes.  

Varat palaist vairākas cenu simulācijas, lai izsekotu cenas korekciju ietekmi uz piedāvājuma mērķiem. Palaižot šīs simulācijas, varat regulēt piedāvājuma vispārējo cenu vai vienas vai vairāku specifisku piedāvājuma rindu cenu un pēc tam lietot to cenas simulāciju, kura ir visticamākā pārdošanas līguma noslēgšanai.  

Kad veidojat piedāvājumu, varat iestatīt brīdinājumu. Lūk, daži no brīdinājumu lietošanas veidiem:

-   Tie jūs var pastāvīgi informēt par piedāvājumu statusu organizācijā.
-   Tie var aktivēt specifiska piedāvājuma pārskatīšanu informēt jūs, ja tiek pārsniegti atlaižu ierobežojumi.

## <a name="price-simulation-and-discounts"></a>Cenas simulācija un atlaides
Lai nodrošinātu, ka atlaides un cenas tiek aprēķinātas pareizi, uzmanieties, kad cenu simulācijas palaižat tādos piedāvājumos, kur pastāv atlaides. Tā kā visas cenu simulācijas tiek apstrādātas kā īpašas atlaides aktīvajā piedāvājuma rindā vai visā piedāvājumā, jums ir nepieciešams izsekot atlaižu starpības.

### <a name="types-of-discounts-in-trade-agreements"></a>Atlaižu tipi tirdzniecības līgumos

Tirdzniecības līgumiem programmatūrā Microsoft Dynamics 365 for Finance and Operations var lietot četru veidu cenu atlaides. Šīs atlaides var iestatīt atšķirīgiem krājumiem, debitoriem vai cenu grupām, un tās var ierobežot datums. Lai nepieļautu nepareizus aprēķinus, cenu simulāciju palaišanas laikā jums ir jāņem vērā tirdzniecības līgumi. Lūk, četri atlaižu tipi tirdzniecības līgumos:

-   **Pārdošanas cena** — krājumiem var norādīt atsevišķas pārdošanas cenas. Kad tiek izveidotas piedāvājuma rindas, programma meklē pareizo pārdošanas cenu attiecībā uz krājumu un pārsūta to uz piedāvājuma rindām. Tāpēc tirdzniecības līgums, kam ir šāda veida atlaide, neietekmē cenas simulāciju. Pārdošanas cena, kas tiek izmantota piedāvājuma rindā, ataino tirdzniecības līgumu.
-   **Rindas atlaide** — krājumiem tiek norādītas īpašas atlaides, ņemot vērā pasūtīto daudzumu. Pirms cenu simulācijas sākšanas rindas summas parasti tiek samazinātas ar rindas atlaidi. Tāpēc tirdzniecības līgums, kam ir šāda veida atlaide, ietekmē cenas simulāciju.
-   **Daudzrindu atlaide** — ja apvienotie daudzumi pārsniedz jūsu definēto ierobežojumu, tad iepriekš definētās pasūtīto krājumu kombinācijas izraisa visa pasūtījuma atlaidi. Pirms cenu simulācijas sākšanas rindas summas parasti tiek samazinātas ar rindas atlaidi. Tāpēc tirdzniecības līgums, kam ir šāda veida atlaide, ietekmē cenas simulāciju.
-   **Kopējā atlaide** — ja apvienotās summas pārsniedz jūsu definēto ierobežojumu, tad iepriekš definētie pasūtītie krājumi izraisa atlaidi visam pasūtījumam. Kopējo atlaidi ģenerē piedāvājuma rindas. Taču, tā kā kopējā atlaide tiek lietota piedāvājuma kopsummai kā atlaide, tā samazina piedāvājuma kopsummu. Tāpēc tirdzniecības līgums, kam ir šāda veida atlaide, ietekmē cenas simulāciju.

### <a name="quotation-lines-and-trade-agreements"></a>Piedāvājuma rindas un tirdzniecības līgumi

Kad veidojat vai koriģējat piedāvājuma rindu, aprēķinātas tiek automātiski rindas atlaides. Saistītā pārdošanas cena krājumam tiek atrasta, pamatojoties uz tirdzniecības līgumu.

## <a name="price-simulation-examples"></a>Cenu simulācijas piemēri
Tālākajos piemēros piedāvājumu virsrakstiem un atsevišķiem rindas krājumiem tiek izmantota cenu simulācija.

### <a name="price-simulation-for-quotation-headers"></a>Piedāvājumu virsrakstu cenu simulācija

Izveidojiet piedāvājumu ar šādām rindām:

-   10 vienības krājuma BR-12 (izmaksu cena par vienību: 9,52 USD, pārdošanas cena par vienību: 15,32 USD)
-   12 vienības krājuma BR-14 (izmaksu cena par vienību: 7,48 USD, pārdošanas cena par vienību: 13,75 USD)

Nākamajā tabulā ir parādītas piedāvājuma rindas.

|                            | Aprēķins                          | Rezultāts   |
|----------------------------|--------------------------------------|----------|
| Pārdošanas daudzums             | 10 vienības + 12 vienības                  | 22 vienības |
| Pārdošanas vērtība USD         | (10 × 15,32) + (12 × 13,75)          | 318,20   |
| Izmaksu vērtība USD          | (10 × 9,52) + (12 × 7,48)            | 184,96   |
| Seguma summa USD | 318,20 – 184,96                      | 133,24   |
| Seguma summas norma         | (\[318,20 – 184,96\] ÷ 318,20) × 100 | 41,87%   |

Palaidiet cenu simulāciju un lietojiet 15 procentu kopējo atlaidi visam piedāvājumam vai piedāvājuma virsrakstam. Nākamajā tabulā ir redzamas jaunās piedāvājuma kopsummas pēc cenu simulācijas palaišanas.

|                                                      | Aprēķins                               | Rezultāts   |
|------------------------------------------------------|-------------------------------------------|----------|
| Pārdošanas daudzums                                       | 10 vienības + 12 vienības                       | 22 vienības |
| Vecā pārdošanas vērtība USD                               | (10 × 15,32) + (12 × 13,75)               | 318,20   |
| Vecā izmaksu vērtība USD                                | (10 × 9,52) + (12 × 7,48)                 | 184,96   |
| Vecā seguma summa USD                       | 318,20 – 184,96                           | 133,24   |
| Vecā seguma summas norma                               | (\[318,20 – (10 × 9,52)\] ÷ 318,20) × 100 | 41,87%   |
| Cenu simulācija ar 15 procentu kopējo atlaidi, USD | (15 × 318,2) ÷ 100                        | 47,73    |
| Jaunā pārdošanas vērtība USD                               | 318,20 – 47,73                            | 270,47   |
| Jaunā seguma summa USD                       | 270,47 – 184,96                           | 85,51    |
| Jauna seguma summas likme                               | \[(270,47 – 184,96) ÷ 270,47\] × 100      | 31,61%   |

### <a name="price-simulation-for-single-line-items"></a>Atsevišķas rindas krājumu cenu simulācija

Izveidojiet piedāvājumu ar šādām rindām:

-   10 vienības krājuma BR-12 (izmaksu cena par vienību: 9,52 USD, pārdošanas cena par vienību: 15,32 USD)
-   12 vienības krājuma BR-14 (izmaksu cena par vienību: 7,48 USD, pārdošanas cena par vienību: 13,75 USD)

Nākamajā tabulā ir parādītas piedāvājuma rindas.

|                                      | Aprēķins                          | Rezultāts   |
|--------------------------------------|--------------------------------------|----------|
| Pārdošanas daudzums                       | 10 vienības + 12 vienības                  | 22 vienības |
| Pārdošanas vērtība USD BR-12         | 10 × 15,32                           | 153,20   |
| Pārdošanas vērtība USD BR-14         | 12 × 13,75                           | 165,00   |
| Izmaksu vērtība USD BR-12          | 10 × 9,52                            | 95,20    |
| Izmaksu vērtība USD BR-14          | 12 × 7,48                            | 89,76    |
| Seguma summa USD BR-12 | 153,20 – 95,20                       | 58,00    |
| Seguma summa USD BR-14 | 165,00 – 89,76                       | 75,24    |
| Seguma summas norma USD BR-12  | \[(153,20 – 95,20) ÷ 153,20\] × 100  | 37,86    |
| Seguma summas norma USD BR-14  | \[(165,00 – 89,76) ÷ 165,00\] × 100  | 45,60    |
| Kopējā pārdošanas vērtība USD             | (10 × 15,32) + (12 × 13,75)          | 318,20   |
| Kopējā izmaksu vērtība USD              | (10 × 9,52) + (12 × 7,48)            | 184,96   |
| Kopējā seguma summa USD     | 318,20 – 184,96                      | 133,24   |
| Kopējā seguma summas norma             | \[(318,20 – 184,96) ÷ 318,20\] × 100 | 41,87%   |

Palaidiet cenas simulāciju un lietojiet 10 procentu kopējo atlaidi BR-12 vienībām. Nākamajā tabulā ir redzamas jaunās piedāvājuma kopsummas pēc cenu simulācijas palaišanas vienas rindas krājumam.

|                                                   | Aprēķins                             | Rezultāts   |
|---------------------------------------------------|-----------------------------------------|----------|
| Pārdošanas daudzums                                    | 10 vienības + 12 vienības                     | 22 vienības |
| Vecā pārdošanas vērtība USD BR-12                  | 10 × 15,32                              | 153,20   |
| Cenu simulācija ar 10 procentu atlaidi krājumam BR-12 | (10 × 153,2) ÷ 100                      | 15,32    |
| Jaunā pārdošanas vērtība USD BR-12                  | (10 × 15,32) – 15,32                    | 137,88   |
| Pārdošanas vērtība USD BR-14                      | 12 × 13,75                              | 165,00   |
| Izmaksu vērtība USD BR-12                       | 10 × 9,52                               | 95,20    |
| Izmaksu vērtība USD BR-14                       | 12 × 7,48                               | 89,76    |
| Jaunā seguma summa USD BR-12          | 137,88 – 95,20                          | 42,68    |
| Seguma summa USD BR-14              | 165,00 – 89,76                          | 75,24    |
| Jaunā seguma summas norma USD BR-12           | \[(137,88 – 95,20) ÷ 137,88\] × 100     | 30,95    |
| Seguma summas norma USD BR-14               | \[(165,00 – 89,76) ÷ 165,00\] × 100     | 45,60    |
| Jaunā kopējā pārdošanas vērtība USD                      | \[(10 × 15,32) – 15,32\] + (12 × 13,75) | 302,88   |
| Kopējā izmaksu vērtība USD                           | (10 × 9,52) + (12 × 7,48)               | 184,96   |
| Jaunā kopējā seguma summa USD              | 302,88 – 184,96                         | 117,92   |
| Jauns kopējā ieguldījuma koeficients                      | \[(302,88 – 184,96) ÷ 302,88\] × 100    | 38,93%   |

Cenu simulācija ietekmē tikai to rindu, kurai tā tiek izmantota, un samazina šīs rindas kopsummu.




