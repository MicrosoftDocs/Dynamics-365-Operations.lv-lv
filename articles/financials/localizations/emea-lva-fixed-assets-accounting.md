---
title: " Pamatlīdzekļu uzskaite nodokļu aprēķinam"
description: Šajā tēmā ir sniegta informācija par nodokļu nolietojuma funkcionalitāti Latvijai.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, AssetDepreciationProfile, AssetTable, AssetTaxDepreciation
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 264374
ms.assetid: cbf94106-2c1b-45dd-8734-18a2a56a4682
ms.search.region: Latvia
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d66f1f02377429f0cf9cea48c0ed939e194ecbfb
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549066"
---
# <a name="fixed-assets-accounting-for-tax-purposes"></a> Pamatlīdzekļu uzskaite nodokļu aprēķinam

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegta informācija par nodokļu nolietojuma funkcionalitāti Latvijai, tostarp nodokļu nolietojuma iestatīšanu, ka arī nodokļu nolietojuma pārskata aprēķināšanu un drukāšanu. 
> [!NOTE]
> Nodokļu nolietojums strādā ar vērtības modeļiem. Vērtības modelis un nolietojuma grāmata ir sapludināti vienā jēdzienā ar nosaukumu *grāmata*. Papildinformāciju skatiet rakstā [Pamatlīdzekļu vērtības modeļa un nolietojuma grāmatas sapludināšana](../fixed-assets/fixed-asset-value-model-depreciation-book-merge.md).

## <a name="set-up-a-depreciation-profile"></a>Iestatīt nolietojuma tabulu
Iestatot nolietojuma tabulu, ņemiet vērā tālāk minēto.

|                       |                                                                                                                                                                                                                                                                                                                    |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nolietojuma apr. gads** | Atlasiet gada tipu, kuru lietojat nolietojuma aprēķināšanai. Nolietojuma aprēķina gads un perioda biežums ir saistīti. Tādēļ opciju lauks **Perioda biežums** ir atkarīgs no vērtības laukā **Nolietojuma apr. gads**.                                                                                 |
| **Perioda biežums**  | Atlasiet virsgrāmatas uzkrājumu biežumu kalendārā gada vai finanšu gada laikā. Šajā laukā rādītās opcijas ir atkarīgas no jūsu atlasītā nolietojuma gada. Ja kā nolietojuma aprēķināšanas gadu atlasījāt vērtību **Kalendārs**, tad opcijas ir **Reizi gadā**, **Reizi mēnesī**, **Reizi ceturksnī** un **Reizi pusgadā**. |
| **Pilns nolietojums** | Atzīmējiet šo opciju, lai pamatlīdzekli uzskatītu par pilnīgi nolietotu, kad atlikušais lietošanas ilgums ir 0 (nulle).                                                                                                                                                                                                             |

<!---To set up a depreciation profile, complete the following procedure, [Set up and create depreciation profiles](../fixed-assets/tasks/set-up-depreciation-profiles.md).-->

## <a name="set-up-books"></a>Iestatīt grāmatas
Izmantojiet lapu **Grāmatas**, lai definētu nodokļu kategoriju. Grāmatas tiek sauktas arī par nodokļu kategorijām. Lai izveidotu grāmatu, atlasiet nolietojuma tabulu, kurai lapas **Nolietojuma tabulas** laukā **Metode** ir atzīmēta vērtība **Degresīvā**. Lapa **Grāmatas** juridiskajām personām Latvijā ietver tālāk uzskaitītos laukus.

-   **Grāmatošanas līmenis** — šajā laukā atlasiet vērtību **Nodokļi**.
-   **Summēt par kategoriju** — atzīmējiet šo opciju, ja nodokļu nolietojums ir jāsummē un jāaprēķina visiem pamatlīdzekļiem, kam laukā **Kategorija** ir atlasīta vienāda grāmata.
-   **Nodokļu koeficienti** — varat iestatīt nodokļu koeficientus katram koeficientam, lai finanšu gadam koriģētu iegādes cenu.

Papildinformāciju par grāmatu iestatīšanu skatiet rakstā [Nolietojuma grāmatu iestatīšana](../fixed-assets/tasks/set-up-depreciation-books-2016-05.md)

### <a name="set-up-tax-depreciation-calculation"></a>Iestatīt nodokļu nolietojuma aprēķinu

Lai iestatītu nodokļu nolietojuma aprēķinu, lapā **Pamatlīdzekļi** atlasiet kādu pamatlīdzekli. Pēc tam kopsavilkuma cilnes **Vispārīgi** laukā **Kategorija** atlasiet vērtību **Grāmata**. Pašreizēja grāmatošanas līmenī ar pamatlīdzekli ir jābūt saistītai tikai vienai grāmatai. 
> [!NOTE]
> Šajā lauka tiek rādīts grāmatu ieraksts, un tā grāmatošanas līmeņa vērtība ir vienāda ar Tikai nodokļi.

## <a name="calculate-tax-depreciation"></a>Aprēķināt nodokļu nolietojumu
Lai aprēķinātu pamatlīdzekļa nodokļu nolietojumu, lapā **Nodokļu nolietojums** izveidojiet jaunu nodokļu periodu, kuru izmantot pārskatu veidošanai.

|                   |                                                                                                                                                                |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Lauka nosaukums**    | **Apraksts**                                                                                                                                                |
| **Sākuma datums**    | Atlasiet datumu, no kura periods ir derīgs.                                                                                                                |
| **Beigu datums**      | Atlasiet datumu, līdz kuram periods ir derīgs.                                                                                                               |
| **Perioda statuss** | Atlasiet perioda statusu (**Atvērts** vai **Slēgts**). Ja statuss ir **Slēgts**, tad **Kategorijas** kopsavilkuma cilnē **Detalizēta informācija par kategoriju** nevar pievienot vai dzēst. |

Kopsavilkuma cilnes **Detalizēta informācija par kategoriju** laukā **Kategorija** atlasiet grāmatu, kurai vēlaties aprēķināt nodokļu nolietojumu. Noklikšķiniet uz **Aprēķināt**, lai aprēķinātu nodokļu nolietojumu. Nodokļu nolietojums tiek aprēķināts vai nu atsevišķiem pamatlīdzekļiem, vai arī to aprēķina, pamatojoties uz kopsavilkuma informāciju par visiem pamatlīdzekļiem, kas piešķirti vienai pamatlīdzekļu nodokļu kategorijai. Aprēķins ir balstīts uz nodokļu koeficientu no atlasītās grāmatas un uzskaites datiem to pamatlīdzekļu grāmatās, kuri ir saistīti ar laukā **Kategorija** atlasīto grāmatu.

|                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------|
| **Aprēķina formulas**                                                                                         |
| Koriģētā vērtība = Sākuma bilance + Vērtību korekcijas - Norakstīšana + Iegādes cena \* Iegādes koeficients |
| Nodokļu nolietojuma summa = Koriģētā vērtība \* Pamata nolietojums \*2 /100 \* mēnešu skaits periodā / 12        |
| Beigu bilance = Koriģētā vērtība – Nodokļu nolietojuma summa                                                           |
| Sākuma bilance (pašreizējais nolietojuma periods) = Beigu bilance (iepriekšējais nolietojuma aprēķina periods)          |

Lai skatītu nodokļu nolietojuma informāciju, noklikšķiniet uz **Nodokļu nolietojuma detalizēta informācija**, lai atvērtu lapu **Nodokļu nolietojuma detalizēta informācija**.

## <a name="print-the-tax-depreciation-report"></a>Drukāt nodokļu nolietojuma pārskatu
Pārskats **Nodokļu nolietojums** lietotājiem Latvijā sniedz iespēju veidot nodokļu pārskatus, kas ir saistīti ar uzņēmuma pamatlīdzekļiem. Lai drukātu šo pārskatu, dodieties uz lapu **Nodokļu nolietojuma aprēķins**, atlasiet kādu konkrētu pārskatu, kuram veidot kopsavilkumu līmenī **Kategorija**. Noklikšķiniet uz **Nodokļu nolietojuma aprēķins** kategorijām, kam nav izveidots kopsavilkums, izmantojot pārskatu **Nodokļu nolietojums**.



