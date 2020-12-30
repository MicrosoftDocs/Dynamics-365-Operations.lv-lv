---
title: Kreditoru rēķinu salīdzināšanas pārskats
description: Parādu kreditoriem rēķinu salīdzināšana ir kreditoru rēķinu, pirkšanas pasūtījumu un produktu ieejas plūsmu informācijas salīdzināšanas process.
author: abruer
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoicePostingHistory
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 27361
ms.assetid: 9f3dace7-05d8-4974-8f85-aca2e224876c
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a8e283038a0cc1c9834a827c453f2951e9e87bcf
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445677"
---
# <a name="accounts-payable-invoice-matching-overview"></a>Kreditoru rēķinu salīdzināšanas pārskats

[!include [banner](../includes/banner.md)]

Parādu kreditoriem rēķinu salīdzināšana ir kreditoru rēķinu, pirkšanas pasūtījumu un produktu ieejas plūsmu informācijas salīdzināšanas process.

Kad salīdzināt dokumentus, atšķirības starp šiem dokumentiem tiek sauktas par salīdzināšanas neatbilstībām. Salīdzināšanas neatbilstības tiek salīdzinātas ar norādītajiem tolerances līmeņiem. Ja salīdzināšanas neatbilstība pārsniedz tolerances procentuālo daļu vai summu, kreditora rēķina lapā un rēķinu vēstures un salīdzināšanas informācijas lapā tiek rādītas salīdzināšanas neatbilstību ikonas. 

Piemēram, jūs ievadāt pirkšanas pasūtījumu ar vienu rindas krājumu ar 1000 baterijām, kur katras vienības cena ir 1,00. Pirkšanas pasūtījums tiek apstiprināts un iesniegts kreditoram. Kreditors nosūta 1000 baterijas un jūs ievadāt produktu ieejas plūsmu par 1000 baterijām, kur katras vienības cena ir 1,00. Bateriju krājumu izmaksas tiek atjauninātas ar šo cenu. 

Rēķins tiek saņemts par 1000 baterijām, kur katras vienības cena ir 1,10. Jūsu juridiskās personas politika šai krājuma kategorijai atļauj 5 procentu neto vienības cenas toleranci. Cena 1,05 ir pieņemama, bet 1,10 — nav. Kad ievadāt informāciju par rēķinu, tiek identificēts, ka pastāv cenu salīdzināšanas neatbilstība, un jūs varat saglabāt rēķinu, līdz neatbilstība ir atrisināta.

Kreditoru rēķinu salīdzināšanai varat lietot šādus tipus:

-   Rēķina kopsummas salīdzināšana — rēķina kopsummas salīdzināt ar kopsummām pirkšanas pasūtījumā. Šis rēķinu salīdzināšanas veids ietver vismazāko detalizētību, tāpēc šo opciju varat izmantot, lai iestatītu kontroles, kas samazina laiku, kurš darbiniekiem ir nepieciešams, lai pārskatītu rēķinu salīdzināšanas informāciju.
-   Divvirzienu salīdzināšana — cenas informāciju rēķinā salīdzzina ar cenas informāciju pirkšanas pasūtījumā.
-   Trīsvirzienu salīdzināšana — cenas informāciju rēķinā salīdzina ar cenas informāciju pirkšanas pasūtījumā. Turklāt arī salīdzina daudzuma informāciju rēķinā ar daudzuma informāciju produktu ieejas plūsmās, kas ir atlasītas šim rēķinam.
-   Maksu salīdzināšana — maksu informāciju (summas) rēķinā salīdzina ar maksu informāciju (summām) pirkšanas pasūtījumā.

> [!NOTE]
> Citu veidu rēķinu validēšanu var izpildīt, izmantojot kreditoru rēķinu ierobežojumus. 

Divvirzienu salīdzināšana un trīsvirzienu salīdzināšana cenu informāciju vienmēr salīdzina ar vienības cenu. Varat arī konfigurēt šīs salīdzināšanas politikas, lai informāciju par cenu salīdzinātu pēc cenu kopsummas.
-   Vienības neto cenu salīdzināšana — cenas informāciju divvirzienu salīdzināšanai vai trīsvirzienu salīdzināšanai salīdzina, vienības neto cenu katrai rindai rēķinā salīdzinot ar atbilstošo vienības neto cenu pirkšanas pasūtījumā. Vienības neto cena tiek noteikta ar šādu formulu: Rindas neto summa/Rindas daudzums.
-   Cenu kopsummas salīdzināšana — cenas informāciju divvirzienu salīdzināšanai vai trīsvirzienu salīdzināšanai salīdzina, neto summu (cenas kopsummu) katrai rindai rēķinā salīdzinot ar atbilstošo neto summu pirkšanas pasūtījumā. Neto summa tiek noteikta ar šādu formulu: *(Vienības cena \* Rindas daudzums) + Rindas maksas - Rindas atlaides*. Nosakot cenas kopsummu atbilstību procentos, sistēma salīdzina vērtības, izmantojot darījuma valūtu. Nosakot cenas kopsummu atbilstību pēc summas, sistēma salīdzina vērtības, izmantojot uzskaites valūtu.

Parasti rēķinu salīdzināšanas aprēķini tiek veikti automātiski, kad lapā Kreditora rēķins rediģējat kreditoru rēķinus. Alternatīvi rēķinu salīdzināšanu var veikt pēc pieprasījuma, ja nepieciešams. Rēķinu salīdzināšanu pēc pieprasījuma juridiskajai personai kontrolē funkcija Automātiski atjaunināt rēķina virsraksta statusu uz, kas atrodas lapā Kreditoru moduļa parametri, cilnē Rēķinu validēšana. Rēķinu salīdzināšanu var veikt arī kā daļu no rēķinu pārskatīšanas procesa. Rēķinu salīdzināšanas rezultātus varat skatīt lapā Kreditora rēķins un saistītajās rēķinu salīdzināšanas lapās.

## <a name="invoice-totals-matching"></a>Rēķinu kopsummu salīdzināšana
Rēķinu kopsummu salīdzināšanu varat izmantot, lai pārliecinātos, ka rēķinu kopsummas neatšķiras no paredzētajām summām vairāk kā par pieņemamo novirzi. Sešas kopsummas tiek salīdzinātas lapā Detalizēta informācija par rēķinu kopsummu salīdzināšanu, kā parādīts nākamajā tabulā. Ja pieļaujamā tolerance rēķinu kopsummu salīdzināšanai ir 20%, tad 100% neatbilstības procentuālais daudzums attiecībā uz kopējo atlaides summu tiek uzskatīts par salīdzināšanas neatbilstību.

| Kopsummas lauks    | Faktiskā rēķina kopsumma | Prognozētā rēķina kopsumma | Novirze procentos | Atbilstības statuss |
|----------------|----------------------|------------------------|---------------------|--------------|
| Bilance        | 495,00               | 495,00                 | 0%                  | Izdevās       |
| Beigu atlaide | 0,00                 | 9,90                   | 100%                | Neizdevās.       |
| Izmaksas        | 64,90                | 64,90                  | 0%                  | Izdevās       |
| PVN      | 139,98               | 137,50                 | 2%                  | Izdevās       |
| Noapaļošana      | 0,00                 | 0,00                   | 0%                  | Izdevās       |
| Rēķina summa | 699,88               | 687,50                 | 2%                  | Izdevās       |

Rēķinu kopsummu salīdzināšanu juridiskajai personai kontrolē pārslēgs Salīdzināt rēķinu kopsummas, kurš atrodas lapā Kreditoru moduļa parametri. Salīdzināšana tiek veikta paredzamajām rēķinu kopsummām un faktiskajām rēķinu kopsummām. Paredzamās rēķinu kopsummas tiek aprēķinātas, ņemot vērā no cenas, papildmaksas un pārdošanas nodokļa informāciju no pirkšanas pasūtījuma un daudzumus no rēķina.

## <a name="two-way-price-totals-matching"></a>Divvirzienu cenu kopsummu salīdzināšana
Izmantojiet divvirzienu salīdzināšanu, lai palīdzētu pārliecināties, ka novirze starp cenas informāciju pirkšanas pasūtījumā un rēķinā atrodas pielaides robežās. Cenas informāciju par katras rēķina rindas neto summu un visām gaidošajām un iepriekš iegrāmatotajām rēķinu rindām varat salīdzināt ar atbilstošā pirkšanas pasūtījuma rindas neto summu. Tā tiek saukta arī par cenu kopsummu salīdzināšanu. 

Cenu kopsummu salīdzināšanas pamatā var būt procenti, summa vai procenti un summa. 

Ja ir norādīts pirkšanas cenas kopējās tolerances procentuālais daudzums, tiek salīdzināti pieci lauki, kā parādīts nākamajā tabulā. Tā kā pirkšanas cenas kopējās tolerances procentuālais daudzums ir 10%, cenas kopējās novirzes procentuālais daudzums 50% apzīmē salīdzināšanas neatbilstību.

| Atbilstības statuss | Pavadrēķina neto summa | Sagaidāmā neto summa | Nesaskaņota pirkšanas cenas kopsumma (novirzes summa) | Nesaskaņoti pirkšanas cenas kopsummas procenti (novirze procentos) | Pirkšanas cenas kopējās tolerances procents |
|--------------|--------------------|---------------------|--------------------------------------------------|-----------------------------------------------------------------|----------------------------------------|
| Izdevās       | 105,00             | 100,00              | 5,00                                             | 5%                                                              | 10%                                    |
| Neizdevās.       | 150,00             | 100,00              | 50,00                                            | 50%                                                             | 10%                                    |

Ja ir norādīta pirkšanas cenas kopējās tolerances summa, tiek salīdzināti pieci lauki, kā parādīts nākamajā tabulā. Tā kā pirkšanas cenas kopējās tolerances summa ir 100,00, cenas kopējās novirzes summa 105,00 apzīmē salīdzināšanas neatbilstību.

| Atbilstības statuss | Pavadrēķina neto summa | Sagaidāmā neto summa | Nesaskaņota pirkšanas cenas kopsumma (novirzes summa) | Nesaskaņota pirkšanas cenas kopsumma uzskaites valūtā (novirzes summa) | Pirkšanas cenas kopējā tolerance |
|--------------|--------------------|---------------------|--------------------------------------------------|-------------------------------------------------------------------------|--------------------------------|
| Izdevās       | 150,00             | 100,00              | 50,00                                            | 50,00                                                                   | 100,00                         |
| Neizdevās.       | 205,00             | 100,00              | 105,00                                           | 105,00                                                                  | 100,00                         |

Ja cenu kopsummu salīdzināšana ir iestatīta ar procentuālu toleranci un tolerances summu, ko reizēm sauc arī par nepārsniedzamo summu, tad tiek ņemtas vērā abas tolerances, kad tiek vērtēts, vai rindai ir salīdzināšanas neatbilstība. Ja procentuālais daudzums vai summa pārsniedz šo toleranci, kā nākamajā tabulā parādīts rindās 150,00 un 205,00, šai rindai ir salīdzināšanas neatbilstība.

| Atbilstības statuss | Pavadrēķina neto summa | Sagaidāmā neto summa | Nesaskaņoti pirkšanas cenas kopsummas procenti (novirze procentos) | Pirkšanas cenas kopējās tolerances procents | Nesaskaņota pirkšanas cenas kopsumma uzskaites valūtā (novirzes summa) | Pirkšanas cenas kopējā tolerance |
|--------------|--------------------|---------------------|-----------------------------------------------------------------|----------------------------------------|-------------------------------------------------------------------------|--------------------------------|
| Izdevās       | 105,00             | 100,00              | 5%                                                              | 10%                                    | 5,00                                                                    | 100,00                         |
| Neizdevās.       | 150,00             | 100,00              | 50%                                                             | 10%                                    | 50,00                                                                   | 100,00                         |
| Neizdevās.       | 205,00             | 100,00              | 105%                                                            | 10%                                    | 105,00                                                                  | 100,00                         |

Divvirzienu salīdzināšana juridiskajai personai tiek kontrolēta ar lauku Rindu atbilstības ierobežojumi, kas atrodas lapā Kreditoru moduļa parametri. Atkarībā no atlases laukā Atļaut atbilstības ierobežojumu ignorēšanu, varat atlasīt divvirzienu salīdzināšanu noteiktam kreditoram, krājumam vai krājuma un kreditora kombinācijai lapā Atbilstības ierobežojumi, un noteiktam pirkšanas pasūtījumam lapā Pirkšanas pasūtījums.

Cenu kopsummu salīdzināšanu juridiskajai personai kontrolē lauks Salīdzināt cenu kopsummas, kurš atrodas lapā Kreditoru modeļa parametri. Pirkšanas cenas kopsummas tolerances procentuālais daudzums un tolerances summa (nepārsniedzamā summa) ir norādīti arī tajā lapā.

## <a name="two-way-net-unit-price-matching"></a>Divvirzienu, neto vienības cenu salīdzināšana
Izmantojiet divvirzienu salīdzināšanu, lai palīdzētu pārliecināties, ka novirze starp cenas informāciju pirkšanas pasūtījumā un rēķinā atrodas pielaides robežās. Varat salīdzināt cenas informāciju katra rēķinā ietvertā krājuma vienības neto cenai. Šī tiek saukta par vienības neto cenas salīdzināšanu. 

Deviņas rindu summas tiek salīdzinātas lapā Detalizēta informācija par rēķinu salīdzināšanu, kā parādīts nākamajā tabulā. Ja pieļaujamā cenas tolerance attiecībā uz vienības neto cenu salīdzināšanu ir 10%, tad 22,61% novirze attiecībā uz vienības neto cenu tiek uzskatīta par salīdzināšanas neatbilstību.

| Rindas lauks                    | Rēķina vērtība | Pirkšanas pasūtījuma vērtība | Novirze procentos | Atbilstības statuss |
|-------------------------------|---------------|----------------------|---------------------|--------------|
| Vienības cena                    | 55,40         | 55,38                | 0%                  | Izdevās       |
| Cenas vienība                    | 1,00          | 1,00                 | 0%                  | Izdevās       |
| Pirkšanas papildmaksas          | 50,00         | 0,00                 | 100%                | Neizdevās.       |
| Atlaide                      | 0,00          | 0,00                 | 0%                  | Izdevās       |
| Atlaides procents              | 0,00          | 0,00                 | 0%                  | Izdevās       |
| Daudzrindu atlaide            | 0,00          | 0,00                 | 0%                  | Izdevās       |
| Daudzrindu atlaide procentos | 0,00          | 0,00                 | 0%                  | Izdevās       |
| Neto summa                    | 271,60        | 221,52               | 22,61%              | Neizdevās.       |
| Vienības neto cena                | 67,9000       | 55,3800              | 22,61%              | Neizdevās.       |

Divvirzienu salīdzināšana juridiskajai personai tiek kontrolēta ar lauku Rindu atbilstības ierobežojumi, kas atrodas lapā Kreditoru moduļa parametri. Atkarībā no atlases laukā Atļaut atbilstības ierobežojumu ignorēšanu, varat atlasīt divvirzienu salīdzināšanu noteiktam kreditoram, krājumam vai krājuma un kreditora kombinācijai lapā Atbilstības ierobežojumi, un noteiktam pirkšanas pasūtījumam lapā Pirkšanas pasūtījums. 

Vienības neto cenas salīdzināšanu juridiskajai personai kontrolē lauks Iespējot rēķinu salīdzināšanas pārbaudes, kurš atrodas lapā Kreditoru modeļa parametri. Vienības neto cenas tolerances procentuālo daudzumu var konfigurēt krājumiem, krājumu grupām, kreditoriem, kreditoru grupām, krājumu un kreditoru kombinācijām vai juridiskajai personai, izmantojot lapu Cenu tolerances.

## <a name="two-way-price-totals-matching-and-net-unit-price-matching"></a>Divvirzienu, cenu kopsummu salīdzināšana un vienības neto cenas salīdzināšana
Cenu kopsummu salīdzināšanu un vienības neto cenas salīdzināšanu varat lietot kopā. Šajā piemērā tiek pieņemts, ka tiek lietota šāda konfigurācija:

-   Vienības neto cenas tolerance attiecībā uz USB atmiņas krājumu ir 10%.
-   Cenu kopsummu salīdzināšanas tolerance juridiskajai personai ir 15% vai 500,00.

Pirkšanas pasūtījums satur tālāk norādīto rindu.

| Krājuma kods | Daudzums | Vienības cena | Neto summa |
|-------------|----------|------------|------------|
| USB atmiņā   | 1000    | 10,00      | 10 000,00  |

Tiek ievadīti trīs rēķini, kā parādīts nākamajā tabulā. Pastāv rēķinu salīdzināšanas neatbilstība 3. rēķinam, jo 1880,00 novirze pārsniedz pirkšanas cenas kopsummas tolerances summu 500,00. Cenu kopsummu salīdzināšanai rēķina neto summa ietver visus iepriekš iegrāmatotos rēķinus papildus tam rēķinam, ar kuru strādājat pašlaik.

| Krājuma kods          | Daudzums | Vienības cena | Neto summa | Cenas salīdzināšana | Cenas kopsummas saskaņošana |
|----------------------|----------|------------|------------|-------------|-------------------|
| 1. rēķins: USB atmiņa | 800      | 10,80      | 8640,00   | Izdevās      | Izdevās            |
| 2. rēķins: USB atmiņa | 100      | 10,80      | 1080,00   | Izdevās      | Izdevās            |
| 3. rēķins: USB atmiņa | 200      | 10,80      | 2160,00   | Izdevās      | Neizdevās.            |
| KOPĀ                |          |            | 11 880,00  |             |                   |

## <a name="three-way-matching"></a>Trīsvirzienu atbilstība

Izmantojiet trīsvirzienu salīdzināšanu, lai palīdzētu pārliecināties, ka novirze starp cenas informāciju pirkšanas pasūtījumā un rēķinā ir pieņemamas pielaides robežās, un lai pārliecinātos, ka rēķina daudzums saskan ar daudzumu atbilstošajās produktu ieejas plūsmās.

Lapā Detalizēta informācija par rēķinu salīdzināšanu tiek salīdzinātas tās pašas rindu summas, kas tiek salīdzinātas divvirzienu salīdzināšanai. Turklāt daudzums rēķinā tiek salīdzināts ar produktu ieejas plūsmu daudzumu, kas ir saņemts. Ja rēķina daudzums atšķiras no salīdzinātā produktu ieejas plūsmas daudzuma, pastāv daudzuma salīdzināšanas kļūda.

| Rindas lauks                    | Rēķina vērtība | Pirkšanas pasūtījuma vērtība | Novirze procentos | Atbilstības statuss |
|-------------------------------|---------------|----------------------|---------------------|--------------|
| Vienības cena                    | 55,40         | 55,38                | 0%                  | Izdevās       |
| Cenas vienība                    | 1,00          | 1,00                 | 0%                  | Izdevās       |
| Pirkšanas papildmaksas          | 50,00         | 0,00                 | 100%                | Neizdevās.       |
| Atlaide                      | 0,00          | 0,00                 | 0%                  | Izdevās       |
| Atlaides procents              | 0,00          | 0,00                 | 0%                  | Izdevās       |
| Daudzrindu atlaide            | 0,00          | 0,00                 | 0%                  | Izdevās       |
| Daudzrindu atlaide procentos | 0,00          | 0,00                 | 0%                  | Izdevās       |
| Neto summa                    | 271,60        | 221,52               | 22,61%              | Neizdevās.       |
| Vienības neto cena                | 67,9000       | 55,3800              | 22,61%              | Neizdevās.       |

| Rindas lauks                     | Rēķina vērtība | Atbilstības statuss |
|--------------------------------|---------------|--------------|
| Rēķina daudzums               | 4,00          |              |
| Kopējās atbilstošās produktu ieejas plūsmas | 0,00          | Neizdevās.       |

Trīsvirzienu salīdzināšana juridiskajai personai tiek kontrolēta ar lauku Rindu atbilstības ierobežojumi, kas atrodas lapā Kreditoru moduļa parametri. Atkarībā no atlases laukā Atļaut atbilstības ierobežojumu ignorēšanu, varat atlasīt trīsvirzienu salīdzināšanu noteiktam kreditoram, krājumam vai krājuma un kreditora kombinācijai lapā Atbilstības ierobežojumi, un noteiktam pirkšanas pasūtījumam lapā Pirkšanas pasūtījums.

## <a name="charges-matching"></a>Maksu salīdzināšana
Maksu salīdzināšanu varat izmantot, lai pārliecinātos, ka maksu summas neatšķiras no paredzētajām summām vairāk kā par pieņemamo procentuālo novirzi. Kopsummas katram papildmaksu kodam, kas attiecas uz rēķinu un pirkšanas pasūtījumu, tiek salīdzinātas lapā Salīdzināt papildmaksu vērtības — Rēķins:, kā parādīts nākamajā tabulā. Ja pieļaujamā tolerance papildmaksu kodam ir 25%, tad 99 999 999 999,99% neatbilstības procentuālais daudzums attiecībā uz Licences papildmaksu kodu tiek uzskatīts par salīdzināšanas neatbilstību.

> [!NOTE] 
> Novirzes procentuālais daudzums 99 999 999 999,99% nozīmē, ka paredzamā summa, pamatojoties uz pirkšanas pasūtījumu, ir nulle, un faktiskā summa rēķinā ir pozitīva vērtība. 

| Maksu salīdzināšanas statuss | Rēķinu izmaksu kods | Faktiskā aprēķinātā kopējā vērtība | Prognozētā aprēķinātā kopējā vērtība | Novirzes summa | Novirze procentos | Tolerances procenti |
|----------------------|----------------------|-------------------------------|---------------------------------|-----------------|---------------------|----------------------|
| Neizdevās.               | Licence              | 25                            | 0                               | 25              | 99 999 999 999,99%  | 25%                  |
| Izdevās               | Kravas pārvadāšana              | 200                           | 200                             | 0               | 0%                  | 25%                  |
| Neizdevās.               | Paātrināt izpildi             | 4.                             | 2                               | 2               | 100%                | 25%                  |

Maksu salīdzināšanu juridiskajai personai kontrolē pārslēgs Salīdzināt maksas, kurš atrodas lapā Kreditoru moduļa parametri. Novirzes tolerances procentuālo daudzumu maksām varat iestatīt lapā Maksu tolerances.

> [!NOTE]
> Maksu salīdzināšana tiek veikta tikai maksu kodiem, kam ir atlasīts pārslēgs Salīdzināt pirkuma pasūtījuma un rēķina vērtības lapā Maksas kods.

## <a name="related-functionality"></a>Saistītā funkcionalitāte
Kreditoru rēķinu pamatā bieži ir produktu ieejas plūsmas, kas parāda faktiskos sūtījumus, nevis pirkšanas pasūtījumus. Dažkārt rēķinos iekļautās summas nesakrīt ar pirkšanas pasūtījuma summām, un dažkārt nosūtītie daudzumi nesakrīt ar rēķinos iekļautajiem daudzumiem. Šo informāciju varat palīdzēt pārvaldīt šādos veidos:
-   Izveidot kreditora rēķinu, pamatojoties uz produktu ieejas plūsmām. Rēķiniem tiek automātiski ieteiktas produktu ieejas plūsmas, un varat atlasīt, kuras produktu ieejas plūsmas lietot. Varat arī atlasīt konkrētus produktu ieejas plūsmas rindu krājumus no vairākiem pirkšanas pasūtījumiem, ja tas nepieciešams.
-   Skatīt un apstiprināt rēķinā norādītā daudzuma un produktu ieejas plūsmā norādītā saņemtā daudzuma starpību. Ja pastāv atšķirība, varat saglabāt rēķinu un vēlāk to salīdzināt to ar citu produktu ieejas plūsmu vai mainīt rēķinā norādīto daudzumu, lai tas atbilstu saņemtajam daudzumam.
-   Ievadīt rēķinu summas, kas netika iekļautas oriģinālajā pirkšanas pasūtījumā, lai informācija rēķinā sakristu ar rēķinu, kuru saņēmāt no kreditora. Pirkšanas pasūtījumu maksas varat salīdzināt ar rēķinu maksām. Ja nepieciešams, varat pievienot maksas rēķiniem un sadalīt tās pa rēķinu rindām.
-   Skatīt un apstiprināt cenu salīdzināšanas neatbilstības rēķinā norādītās vienības neto cenā un pirkšanas pasūtījuma vienības neto cenā. Varat iestatīt cenas tolerances procentuālos daudzumus juridiskajām personām, kreditoriem un krājumiem. Ja kreditora rēķina rindu cena neietilpst pieņemamajās cenas tolerances robežās, varat rēķinu saglabāt, līdz tas ir apstiprināts grāmatošanai vai līdz saņemat labojumu no kreditora.

Plašāku informāciju skatiet sadaļā [Trīsvirzienu atbilstības ierobežojumi](three-way-matching-policies.md) un [Kreditoru rēķinu salīdzināšanas pārbaudes iestatīšana](tasks/set-up-accounts-payable-invoice-matching-validation.md). 




