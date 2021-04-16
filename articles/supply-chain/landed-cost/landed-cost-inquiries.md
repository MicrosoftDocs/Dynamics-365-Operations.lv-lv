---
title: Uzziņas par kopējām izmaksām
description: Šajā tēmā ir aprakstīts, kā atrast un izmantot dažādus pieprasījumu tipus, kas ir pieejami Kopējo izmaksu modulim.
author: sherry-zheng
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMLine, ITMItemTracking, ITMContainerActivityTracking, ITMContainerTracking
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-21
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 22a2e76780adb43b053b6cf7fd08411a4a60aeac
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823365"
---
# <a name="landed-cost-inquiries"></a>Uzziņas par kopējām izmaksām

[!include [banner](../../includes/banner.md)]

## <a name="voyage-line-inquiries"></a>Reisa rindas uzziņas

Vaicājumā par **Reisa rindām** ir parādītas visas reisa rindas, kuras attiecas uz krājumiem. Šo pieprasījumu var izmantot kā filtru, lai palīdzētu atrast krājumu, pirkšanas pasūtījumu vai citu noderīgu informācijas daļu. To var izmantot arī, lai identificētu paredzamo piegādes datumu krājumam, kas varētu būt uz viena vai vairākiem reisiem. Šādā veidā tas var palīdzēt pārvaldīt paredzamo krājumu saņemšanu.

Lai atvērtu šo vaicājumu, dodieties uz **Kopējās izmaksas \> Uzziņas \> Reisa rindas**.

### <a name="overview-tab"></a>cilne Pārskats

Uzziņu lapas **Reisa rindas** cilne **Pārskats** ietver režģi, kurā ir pamatinformācija par katru atbilstošo reisa rindu. Tālāk redzamajā tabulā ir sniegts dažādu kolonnu tipu apraksts.

| Kolonna | Apraksts |
|---|---|
| **Krājuma numurs** | Reisa rindas krājums. |
| **Atsauce** | Pasūtījuma tips (pirkšanas pasūtījums vai pārsūtīšanas pasūtījums). |
| **Skaits** | Pirkšanas pasūtījuma numurs vai pārsūtīšanas pasūtījuma numurs. |
| **Folio** | Folio, kas saistīts ar reisa rindu. |
| **Nosūtīšanas konteiners** | Nosūtīšanas konteiners, kas saistīts ar reisa rindu. |
| **Reiss** | Reiss, kas saistīts ar reisa rindu. |
| **Daudzums** | Riesa rindas krājuma daudzums. |
| (Citas dimensijas) | Ja nepieciešams, var rādīt papildu dimensiju kolonnas. Šīs dimensijas ietver partijas numuru, krājuma statusu un noliktavu. Darbību rūtī atlasiet **Krājumi \> Rādīt dimensijas**, lai atvērtu dialoglodziņu, kurā var atlasīt iekļaujamās dimensijas. |

### <a name="general-tab"></a>Cilne Vispārīgi

Atlasiet cilni **Vispārīgi**, lai skatītu papildinformāciju par rindu, kas pašreiz atlasīta cilnē **Pārskats**.

### <a name="dimensions-tab"></a>Cilne Dimensijas

Atlasiet cilni **Dimensijas**, lai skatītu cilnē **Pārskats** atlasītajai cilnei visu pieejamo krājumu dimensiju vērtības neatkarīgi no dimensijām, kuras esat izvēlējies tajā rādīt.

## <a name="cost-estimate-inquiries"></a>Uzziņas par izmaksu aprēķiniem

Katru reizi, kad ģenerējiet izmaksu novērtējumu, novērtējums tiek pievienots **Izmaksu novērtējumu** pieprasījuma lapai. Pilnu informāciju par to, kā ģenerēt, skatīt un strādāt ar izmaksu novērtējumiem (tajā skaitā aprēķinus uzziņu lapā), skatiet sadaļā [Novērtēt un pārvaldīt kopējās izmaksas](estimate-manage-landed-costs.md).

## <a name="item-tracking"></a>Krājuma izsekošana

Izmantojiet **Krājumu izsekošanas** lapu, lai apskatītu atvērtos pirkšanas pasūtījumu rindas un to pašreizējo statusu. Rindas nav jāsaista ar reisu, lai šeit parādās. Tomēr, ja krājums ir saistīts ar reisu, krājuma izsekošanas ieraksta rinda rāda reisa ID.

Lai atvērtu šo lapu, dodieties uz sadaļu **Kopējās izmaksas \> Uzziņas \> Izsekošana \> Krājumu izsekošana**.

Iespējams, sistēmā ir ļoti daudz pirkšanas pasūtījumu rindu, tāpēc lapā **Krājumu izsekošana** sākotnēji nav ierakstu. Sāciet, lietojot filtra laukus lapas augšpusē, lai definētu meklējamā pirkšanas pasūtījuma rindu kopu. Pēc tam darbību rūtī atlasiet **Atjaunināt**, lai ģenerētu sarakstu. Varat izmantot zvaigznīti (\*) kā aizstājējzīmi jebkurā filtra laukā. Piemēram, lai atrastu visas pirkšanas pasūtījuma rindas krājumiem, kuru nosaukumā ir iekļauts vārds "DVD", iestatiet lauka **Tips** vērtību uz **Preces nosaukums** un ievadiet *\*DVD\** laukā **Lauka vērtība**.

> [!NOTE]
> Pašlaik neizpildītie pasūtījumi ietver tikai pārdošanas pasūtījumus. Pārdošanas piedāvājumi nav rādīti vai tiek uzskatīti par neizpildītiem pasūtījumiem.

Tabulā ir aprakstītas kolonnas **Krājumu izsekošanas** lapas režģī.

| Kolonna | Apraksts |
|---|---|
| **Uz ostu** | Galamērķis. |
| **Apstiprināts** | Pirkšanas pasūtījuma rindas apstiprinātais datums. |
| **Piegādes datums** | Pirkšanas pasūtījuma rindas piegādes datums. |
| **Reiss** | Ja rinda ir saistīta ar reisu, reisa ID. |
| **Nosūtīšanas konteiners** | Ja rinda ir pievienota nosūtīšanas konteineram, konteinera ID. |
| **Nosūtīšanas osta** | Pašreizējā osta, balstoties uz pirmo izsekošanas formas daļu, kad ar pirkšanas pasūtījuma rindu saistītajam kravas konteineram nav iestatīts faktiskais datums. |
| **Aktivitāte** | Pašreizējā osta, balstoties uz pirmo izsekošanas formas daļu, kur ar pirkšanas pasūtījuma rindu saistītajam kravas konteineram nav iestatīts faktiskais datums. |
| **Plānotais beigu datums** | Datums, kad paredzams, ka reiss tiks saņemts mērķa noliktavā. |
| **Vārds, uzvārds** | Kreditora nosaukums. |
| **Reisa statuss** | Nosūtīšanas statuss, kas ir saistīts ar pirkšanas pasūtījuma rindu. |
| **Krājuma numurs** | Skatiet dotās pirkšanas pasūtījuma rindas krājuma numuru. |
| **Ārējie** | Kreditora krājuma nosaukums. |
| **Preces nosaukums** | Krājuma nosaukums pirkšanas pasūtījuma rindai. |
| **Daudzums** | Pirkšanas pasūtījuma rindas daudzums pirkšanas pasūtījuma rindai. |
| **Vienība** | Mērvienība pirkšanas pasūtījuma rindai. |
| **Atsauce** | Pasūtījuma tips (pirkšanas pasūtījums vai pārsūtīšanas pasūtījums) |
| **Atsauces numurs** | Pirkšanas pasūtījuma numurs vai pārsūtīšanas pasūtījuma numurs. |
| **Neizpildīts pasūtījums** | Simbols norāda, ka krājumam ir neizpildti pārdošanas pasūtījumi. |
| (Citas dimensijas) | Ja nepieciešams, var rādīt papildu dimensiju kolonnas. Šīs dimensijas ietver partijas numuru, krājuma statusu un noliktavu. Darbību rūtī atlasiet **Rādīt dimensijas**, lai atvērtu dialoglodziņu, kurā var atlasīt iekļaujamās dimensijas. |

### <a name="related-information-about-backorders"></a>Saistītā informācija par neizpildītajiem pasūtījumiem

Lai skatītu papildu informāciju par neizpildītajiem pasūtījumiem, atlasiet cilni **Saistītā informācija** lapas labajā pusē un pēc tam atlasiet **Neizpildītie pasūtījumi**. Lai skatītu vēl vairāk informācijas par noteiktu neizpildīto pasūtījumu, atlasiet tā rindu un pēc tam atlasiet saiti **Vairāk**.

## <a name="individual-shipping-container-tracking"></a>Individuāli nosūtīta konteinera izsekošana

**Atsevišķa nosūtīšanas konteinera izsekošanas** pieprasījums nodrošina filtru, kas ļauj atrast pārvadāšanas konteineru un pēc tam identificēt visas reisa rindas šajā konteinerā.

Lai atvērtu šo lapu, dodieties uz sadaļu **Kopējās izmaksas \> Uzziņas \> Izsekošana \> Atsevišķa nosūtīšanas konteinera izsekošana**.

## <a name="multiple-shipping-container-tracking"></a>Vairāku nosūtīšanas konteineru izsekošana

**Atsevišķa nosūtīšanas konteinera izsekošanas** pieprasījums nodrošina filtru, kas ļauj atrast pārvadāšanas konteineru un pēc tam identificēt visas reisa rindas šajā konteinerā.

Lai atvērtu šo lapu, dodieties uz sadaļu **Kopējās izmaksas \> Uzziņas \> Izsekošana \> Atsevišķa nosūtīšanas konteinera izsekošana**.
