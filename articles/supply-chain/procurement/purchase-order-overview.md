---
title: Pirkšanas pasūtījuma apskats
description: Šajā rakstā ir sniegta vispārīga informācija par pirkšanas pasūtījumiem (PP) un saites uz papildu rakstiem, kas ir saistīti ar dažādajiem PP apstrādes posmiem.
author: FrankDahl
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 93083
ms.assetid: e9b7bc5b-1d7e-4ec2-97be-d655274b0613
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b86e934a0ac25b1fe77a3359b74e707fb372ae6b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549340"
---
# <a name="purchase-order-overview"></a>Pirkšanas pasūtījuma apskats

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

Šajā rakstā ir sniegta vispārīga informācija par pirkšanas pasūtījumiem (PP) un saites uz papildu rakstiem, kas ir saistīti ar dažādajiem PP apstrādes posmiem.

Pirkšanas pasūtījums (PP) ir dokuments, kas atspoguļo vienošanos ar kreditoru par preču vai pakalpojumu iegādi. Šis dokuments palīdz arī sekot līdzi informācijai par produktu ieejas plūsmu, kuras tiek veikta saistībā ar pasūtījumu, un vēlāk veikt uzskaiti kreditora rēķiniem, ko šis kreditors izraksta saistībā ar pasūtījumu.  

Lapā **Pirkšanas pasūtījumi** ir sniegts pārskats par pieejamajiem pasūtījumiem, un tā jums ļauj modificēt šos pasūtījumus. Kad atverat pārdošanas pasūtījumu, varat atlasīt skatu **Virsraksts**, kur ir sniegta informācija, kas katram PP ir norādīta tikai vienu reizi, piemēram, informācija par kreditoru. Varat arī atlasīt skatu **Rindas**, kur varat modificēt pasūtījuma rindas. Parasti šie skati tiek pārslēgti pirkšanas pasūtījumu modificēšanas laikā. Maksas nav tieši norādītas lapā **Pirkšanas pasūtījumi**, bet tām var piekļūt, izmantojot izvēlnes pasūtījuma virsrakstā un rindās.  

Pastāv daudzas atskaites, kur varat apskatīt informāciju par pirkšanas pasūtījumiem, produktu ieejas plūsmām un kreditoru rēķiniem. Šīs atskaites atrodas moduļos **Sagāde un avoti** un **Kreditori**.  

Darbvietas **Pirkšanas pasūtījumu sagatavošana** un **Pirkšanas pasūtījuma ieejas plūsma un papilddati** jums ļauj skatīt pirkšanas pasūtījumu sarakstus dažādajos to apstrādes stāvokļos. Tie sniedz arī kopsavilkumu par veicamajām darbībām. Darbvieta **Pirkšanas pasūtījumu sagatavošana** ir koncentrēta uz pirkšanas pasūtījumu izveidošanu un pārskatīšanu, pasūtījuma apstrādāšanu, izmantojot apstiprinājumu, kā arī ratificēšanu no kreditora. Darbvieta **Pirkšanas pasūtījuma ieejas plūsma un papilddati** ir saistīta ar pirkšanas pasūtījumiem atbilstošo preču vai pakalpojumu ieejas plūsmas apstrādi. Tajā ir ietverti saraksti, kas sniedz ieskatu par ieejas plūsmām, kuras ir nokavētas vai kuras drīz būs jāpiegādā piegādātājam. Šīs darbvietas netiek izmantots, lai veiktu saistītās ieejas plūsmu aktivitātes, kuras tiek izpildītas noliktavā. Šīs aktivitātes tiek veiktas, izmantojot lapas moduļos **Krājumu vadība** un **Noliktavas valdība**. Kreditoru rēķinu apstrādāšana ir jāveic, izmantojot darbvietu **Kreditora rēķina ieraksts**, un maksājumi ir jāizpilda, izmantojot darbvietu **Kreditoru maksājumi**.  

Tālāk norādītajos rakstos ir sniegts apskats par dažādajiem PP apstrādes posmiem.

-   [Pirkšanas pasūtījuma izveidošana](purchase-order-creation.md)
-   [Pirkšanas pasūtījumu apstiprināšana un ratificēšana](purchase-order-approval-confirmation.md)
-   [Produktu ieejas plūsma pret pirkšanas pasūtījumiem](product-receipt-against-purchase-orders.md)
-   [Apskats par kreditoru rēķiniem](../../financials/accounts-payable/vendor-invoices-overview.md)

## <a name="types-of-purchase-orders"></a>Pirkšanas pasūtījumu tipi
Ir pieejami trīs pirkšanas pasūtījumu veidi. Kad izveidojat pirkšanas pasūtījumu, ir jānorāda tā veids. Noklusējuma pasūtījuma tipu jauniem pasūtījumiem varat iestatīt lapā **Sagādes un avotu parametri**.

| PP tips        | Apraksts                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Žurnāls        | Izmantojiet šo tipu, lai izveidotu melnraksta pasūtījumu. Šis tips neietekmē krājumu rezervju daudzumu un neģenerē krājumu transakcijas. Pirkšanas pasūtījumu žurnāla rindas netiek iekļautas vispārējā plānošanā.                                                                                                       |
| Pirkšanas pasūtījums | Izmantojiet šo tipu, lai izveidotu pirkšanas pasūtījumus, kad kreditors pasūtījumus ir ratificējis, un kad pasūtījumi tiek apstrādāti, izmantojot ieejas plūsmu un rēķinu izrakstīšanu, pirms kreditoram tiek veikts maksājums. Šī tipa pirkšanas pasūtījumi tiek izmantoti visbiežāk.                                                                          |
| Atgrieztais pasūtījums | Izmantojiet šo tipu, kad atgriežat preces kreditoram. Šī tipa pasūtījumam ir nepieciešams, lai jūs norādāt atgriezto krājumu autorizācijas (AKA) kodu, ko saņemat no kreditora. Šo AKA numuru jūs norādāt pirkšanas pasūtījuma cilnē **Vispārīgi**. Pasūtījuma rindām ir nepieciešami negatīvi daudzumi. |

## <a name="purchase-order-statuses"></a>Pirkšanas pasūtījumu statusi
Pirkšanas pasūtījumi ietver vairākus statusa laukus, kas norāda pasūtījuma izpildes gaitu. Visi šie lauki ir redzami pasūtījuma skatā **Virsraksts**, un daži no tiem ir redzami arī visu pasūtījumu režģa apskatā. Laukā **Statuss** tiek rādīts statuss pasūtījuma daudzumiem. Ir pieejamas šādas vērtības:

-   **Atvērts pasūtījums** — pasūtījumi ir izveidoti, un daudzumi ir ietverti pasūtījumā.
-   **Saņemts** — daži no daudzumiem ir saņemti, bet par tiem vēl nav izrakstīts rēķins.
-   **Iekļauts rēķinā** — ir izrakstīts rēķins par visu pasūtījumā iekļauto daudzumu. **Piezīme.** Ja pasūtījums rēķinā ir iekļauts *daļēji*, tad nav piemērots ne statuss **Saņemts**, ne statuss **Iekļauts rēķinā**. Tāpēc šāda pasūtījuma statuss joprojām ir **Atvērts pasūtījums**.
-   **Atcelts** — pasūtījums tika ratificēts, bet vēlāk tika atcelts. Tādēļ šis statuss norāda, ka pasūtījumam vairs nav neviena atvērta daudzuma.

Lauks **Dokumenta statuss** jums palīdz ātri pārskatīt pasūtījuma apstrādes gaitu attiecībā uz dokumentiem, kas ir apstrādāti. Tas rāda pēdējā šim dokumentam pabeigtā dokumenta statusu. Ir pieejamas šādas vērtības:

-   **Nav** — šim pasūtījumam vēl nav apstrādāts neviens dokuments.
-   **Pirkšanas pieprasījums** — ir ģenerēts pirkšanas pieprasījums, un pasūtījums gaida atbildi no kreditora.
-   **Pirkšanas pasūtījums** — šim pasūtījumam ir apstrādāta ratifikācija.
-   **Produktu ieejas plūsma** — šim pasūtījumam ir apstrādāta produktu ieejas plūsma.
-   **Rēķins** — šim pasūtījumam uzskaitē ir iekļauts rēķins.

Lauks **Apstiprinājuma statuss** tiek izmantots, kad pirkšanas pasūtījumam tiek veikts pārskatīšanas process vai darbplūsma. Ir pieejamas šādas vērtības:

-   **Melnraksts**, **Tiek pārskatīts** un **Noraidīts** — šie statusi tiek izmantoti tikai tad, ja pirkšanas pasūtījumam tiek lietota apstiprināšanas darbplūsma.
-   **Apstiprināts** — šis statuss tiek piešķirts pasūtījumiem, kam ir izpildīts darbplūsmas apstiprinājums. Pasūtījumiem, kas ir izveidoti, neizmantojot apstiprinājuma darbplūsmu, statuss **Apstiprināts** tiek piešķirts nekavējoties.
-   **Tiek pārskatīts ārēji** — šis statuss tiek lietots scenārijos, kur pirkšanas pieprasījums tiek nosūtīts kreditoram, lai kreditors varētu ratificēt pirkšanas pasūtījuma nosacījumus. Šis statuss tiek lietots arī procesā, ko uzsāk ar darbību **Ratifikācijas pieprasījums**. Šim procesam kreditoram tiek lūgts apstiprināt pirkšanas pasūtījuma nosacījumus, izveidojot savienojumu ar jūsu sistēmu un reģistrējot, vai kreditors šo pasūtījumu ratificē vai noraida.
-   **Ratificēts** — šis statuss tiek piešķirts pēc tam, kad pasūtījums ir ratificēts. Parasti šis statuss ir pēdējais apstiprinājuma statuss, kas pasūtījumam tiek piešķirts.


<a name="additional-resources"></a>Papildu resursi
--------

[Pirkšanas pasūtījuma izveidošana](purchase-order-creation.md)

[Pirkšanas pasūtījumu apstiprināšana un ratificēšana](purchase-order-approval-confirmation.md)

[Produktu ieejas plūsma pret pirkšanas pasūtījumiem](product-receipt-against-purchase-orders.md)

[Apskats par kreditoru rēķiniem](../../financials/accounts-payable/vendor-invoices-overview.md)



