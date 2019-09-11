---
title: Līdzekļa KPI
description: Šajā tēmā ir paskaidroti līdzekļu izpildes pamatrādītāji (IP) programmā Asset Management.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4fc32d337be1f71932555fcb062a8d05c9ca9bda
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918422"
---
# <a name="asset-kpis"></a>Līdzekļa KPI

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Programmā Asset Management varat aprēķināt dažādus izpildes pamatrādītājus līdzekļiem un līdzekļu veidiem. Varat izmantot IP, lai iegūtu pārskatu par līdzekļu izpildi attiecībā, piemēram, uz darbības laiku, dīkstāvi, remontu un vidējo laiku starp atteicēm.

1. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Pieprasījumi** > **Līdzekļi** > **Līdzekļu IP**.

2. Dialogā **Aprēķināt līdzekļa IP** atlasiet **Laika skala** ko izmantot aprēķinam un periodu laukos **Datums no** un **Datums līdz**. 

3. Ja vajadzīgs, kopsavilkuma cilnē **Iekļaujamie ieraksti** varat atlasīt konkrētus līdzekļus un līdzekļu veidus, ko iekļaut aprēķinā.

4. Noklikšķiniet uz **Labi**, lai sāktu aprēķināšanu.

5. Kopsavilkuma cilnē **Pārskats** aprēķina rezultāti tiek parādīti režģa skatā. Katru līdzekli rāda atsevišķā rindā.

6. Kopsavilkuma cilnē **IP atlasītajai rindai** redzami aprēķini līdzeklim, kas izvēlēts kopsavilkuma cilnē **Pārskats**. IP vērtības tiek kategorizētas attiecībā uz **Laiks**, **Pieejamība**, **Darba pasūtījumi**, **Apkope**, **Kļūmes**, **Dīkstāve uzturēšanas dēļ** un **Izmaksas**.

Šajā tabulā atradīsiet aprakstu par laukiem lapā **Līdzekļu IP**.

| Lauks                   | Apraksts                                                                                                                                                                                                                                                                                           |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Līdzeklis                   | Līdzekļa ID.                                                                                                                                                                                                                                                                                             |
| Kopējais laiks              | Kopējais laiks, kas iestatīts aprēķinā lietotajam kalendāram. Ja līdzeklis saistīts ar resursu, tiek lietots saistītais resursu kalendārs. Ja līdzeklis nav saistīts ar resursu, tiek izmantots kalendārs, kas atlasīts laukā **Standarta kalendārs** **Līdzekļu pārvaldības parametros**. |
| Darbspēja                  | Kopējais laiks, atskaitot dīkstāvi.                                                                                                                                                                                                                                                                            |
| Darbības pārtraukums                | Dīkstāves uzturēšanas dēļ reģistrācijas līdzeklim atlasītajā periodā.                                                                                                                                                                                                                              |
| Labošanas laiks             | Kopējais darba stundu skaits, kas patērēts remonta darbu pasūtījumiem.                                                                                                                                                                                                                                            |
| Pieejamība %          | Darbspējas laiks, kas dalīts ar kopējo laiku un reizināts ar 100.                                                                                                                                                                                                                                                   |
| Kļūmju skaits        | Kļūmju iemeslu skaits, kas reģistrēts līdzekļa kļūmju simptomiem atlasītajā periodā.                                                                                                                                                                                                             |
| Vidējais laiks starp atteicēm                    | Vidējais laiks starp kļūmēm, kas ir kopējais laiks, kas dalīts ar kļūmju skaitu, kas reģistrēts līdzeklim atlasītajā periodā. Ja kļūmju skaits ir nulle, vidējais laiks starp atteicēm tiek iestatīts kā kopējais laiks.                                                                                                                   |
| Kļūmju koeficients               | 1 dalīts ar vidējo laiku starp atteicēm.                                                                                                                                                                                                                                                                                    |
| Vidējais remonta laiks                     | Vidējais remonta laiks, kas ir remontu laiks, kas dalīts ar kļūmju skaitu, kas reģistrēts līdzeklim atlasītajā periodā. Ja kļūmju skaits ir nulle, vidējais remontu laiks tiek iestatīts kā remontu laiks.                                                                                                                           |
| Darbības apturēšanas reižu skaits         | Līdzeklim izveidotās dīkstāves uzturēšanas dēļ reģistrācijas.                                                                                                                                                                                                                                     |
| Vidējais laiks starp apturēšanām                    | Vidējais laiks starp apturēšanām, kas ir kopējais laiks, kas dalīts ar dīkstāves uzturēšanas dēļ reģistrācijām. Ja dīkstāves uzturēšanas dēļ reģistrāciju skaits atlasītajā periodā ir nulle, vidējais laiks starp apturēšanām tiek iestatīts kā kopējais laiks.                                                                                      |
| Preventīvās izmaksas         | Izmaksas, kas reģistrētas līdzeklim saistībā ar izmaksu veidu „Profilaktiski” atlasītajā periodā. Izmaksu veidi tiek iestatīti darba pasūtījumu veidiem.                                                                                                                                                                       |
| Korekcijas izmaksas         | Izmaksas, kas reģistrētas līdzeklim saistībā ar izmaksu veidu „Labojoši” atlasītajā periodā. Izmaksu veidi tiek iestatīti darba pasūtījumu veidiem.                                                                                                                                                                       |
| Aizstāšanas vērtība       | Līdzeklim noteiktā vērtība kā aizvietošanas izmaksas.                                                                                                                                                                                                                                                  |
| Līdzekļa tips             | Līdzeklim izvēlētā līdzekļa veida identifikācija.                                                                                                                                                                                                                                             |
| Ražotājs           | Līdzeklim izvēlētā ražotāja identifikācija.                                                                                                                                                                                                                                                 |
| Modelis                   | Līdzeklim izvēlētā ražotāja modeļa identifikācija.                                                                                                                                                                                                                                           |
| No datuma               | IP aprēķina sākuma datums. Ja līdzeklis izveidots pēc aprēķina sākuma datuma, šajā laukā tiek rādīts līdzekļa sākuma datums.                                                                                                                                  |
| Līdz datumam                 | IP aprēķina beigu datums. Ja līdzeklis reģistrēts kā neaktīvs pirms aprēķinam noteiktā beigu datuma, šajā laukā tiek rādīts datums, no kura līdzeklis vairs nebija aktīvs.                                                                                               |
| Laika skala              | Aprēķinot IP, jūs atlasāt izmantojamo laika skalu: stundas, dienas, nedēļas.                                                                                                                                                                                                            |
| Pieejamība            | Darbspējas laiks, kas dalīts ar kopējo laiku.                                                                                                                                                                                                                                                                         |
| Darba pasūtījumi             | Kopējais darba stundu skaits, kas iekļauts IP aprēķinā.                                                                                                                                                                                                                                          |
| Darba pasūtījuma ilgums         | Kopējais darba stundu skaits, kas patērēts darbu pasūtījumiem.                                                                                                                                                                                                                                               |
| Primārie darba pasūtījumi     | Primāro darba pasūtījumu skaits, kas iekļauts IP aprēķinā.                                                                                                                                                                                                                                        |
| Sekundārie darba pasūtījumi   | Sekundāro darba pasūtījumu skaits, kas iekļauts IP aprēķinā.                                                                                                                                                                                                                                      |
| Uzturēšanas darbu pasūtījumi | Uzturēšanas darba pasūtījumu skaits, kas iekļauts IP aprēķinā. Uzturēšanas darba pasūtījums ir darba pasūtījums, kas nav saistīts ar kļūmes iemesliem.                                                                                                                                                             |
| Uzturēšanas ilgums        | Kopējais darba stundu skaits, kas patērēts uzturēšanas darba pasūtījumiem.                                                                                                                                                                                                                                       |
| Remonta darbu pasūtījumi      | Remonta darba pasūtījumu skaits, kas iekļauts IP aprēķinā. Remonta darba pasūtījums ir darba pasūtījums, kas ir saistīts ar kļūmes iemesliem.                                                                                                                                                                        |
| Uzticamība %           | Aprēķins balstīts uz paredzamo eksponenciālo attīstību līdzekļa kļūmju reģistrācijā, tas ir, laika gaita līdzeklis kļūst mazāk uzticams saistībā ar nolietošanos. Šī IP aprēķins ir balstīts uz vidējo laiku starp atteicēm un kopējo laiku.                                                            |
| Ražošanas apstāšanās vidējais laiks                    | Ražošanas apstāšanās vidējais laiks, kas ir kopējais dīkstāves uzturēšanas dēļ laiks, kas dalīts ar dīkstāves uzturēšanas dēļ reģistrācijām. Ja dīkstāves uzturēšanas dēļ reģistrāciju skaits atlasītajā periodā ir nulle, vidējais laiks starp apturēšanām tiek iestatīts kā kopējais laiks.                                                                               |
| Kopējās izmaksas              | Kopējās izmaksas, kas reģistrētas līdzeklim atlasītajā periodā.                                                                                                                                                                                                                                              |
| Investīciju izmaksas         | Izmaksas, kas reģistrētas līdzeklim saistībā ar izmaksu veidu „Ieguldījumi” atlasītajā periodā. Izmaksu veidi tiek iestatīti darba pasūtījumu veidiem.                                                                                                                                                                       |

Zemāk esošajā attēlā ir parādīts četru līdzekļu IP aprēķina ekrānuzņēmums.

![1. attēls](media/11-controlling-and-reporting.png)

- Varat vienlaicīgi atlasīt vairākus līdzekļus **Visi līdzekļi**, tad klikšķiniet uz pogas **Līdzekļa IP** cilnē **Vispārīgi**. Tad klikšķiniet uz **Labi** dialogā **Aprēķinā līdzekļa IP**, lai aprēķinātu IP atlasītajiem līdzekļiem.  
- IP aprēķina rezultāti var saturēt vai nesaturēt [uzturēšanas dīkstāves reģistrācijas](../work-orders/maintenance-downtime.md) atkarībā no iestatījumiem un uzturēšanas dīkstāves iemeslu kodu izmantošanas. 

