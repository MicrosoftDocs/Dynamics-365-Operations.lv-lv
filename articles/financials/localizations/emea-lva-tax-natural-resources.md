---
title: Dabas resursu nodokļa pārskats
description: Šajā tēmā ir paskaidrots, kā iestatīt un ģenerēt pārskatu Dabas resursu nodoklis (DRN).
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LvNRTaxItemGroupLookup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 270454
ms.search.region: Latvia
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 93486e137b9ae8b9acf52a22230dec348bc56307
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/02/2019
ms.locfileid: "1852462"
---
# <a name="tax-on-natural-resources-report"></a>Dabas resursu nodokļa pārskats

[!include [banner](../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā iestatīt un ģenerēt pārskatu Dabas resursu nodoklis (DRN).

Uzņēmumiem Latvijā ir periodiski jāiesniedz pārskats **Dabas resursu nodoklis** (**DRN**). Šī funkcionalitāte attiecas tikai uz juridiskajām personām Latvijā. Nodoklis ir jāaprēķina arī par importētajām vai pašu ražotajām precēm, kuras tiek lietotas iekšēji. Visbeidzot — dabas resursu nodoklis ir jāaprēķina par pārskata perioda laikā pārdoto iepakoto preču iepakojuma materiāliem.

## <a name="prerequisites"></a>Priekšnosacījumi

| Priekšnosacījums                                                   | Papildinformācija                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Iestatiet nodokļu iestādi.                                        |    |
| Iestatiet virsgrāmatas grāmatošanas grupu dabas resursu nodoklim. |  |
| Iestatiet nosegšanas periodu dabas resursu nodoklim.      |  |
| Iestatiet PVN kodus dabas resursu nodoklim.          | |
| Iestatiet PVN grupas dabas resursu nodoklim.         |  |
| Iestatiet nodokļu grupas dabas resursu nodoklim.               | Izmantojiet lapu **Dabas resursu nodokļu grupa**, lai iestatītu nodokļu grupas, kurās ir definēti pareizie PVN kodi, ņemot vērā nodokļu grupas un PVN grupas krustpunktu dabas resursu nodoklim.                                                                                                                                                                                                    |
| Iestatiet krājumu parametrus.                                   | Lapā **Krājumu un noliktavas vadības parametri** opcijai **Aprēķināt iepakojuma materiālu maksas** iestatiet vērtību **Jā**. Laukā **PVN grupa** atlasiet PVN grupu dabas resursu nodoklim. Pēc noklusējuma šī PVN grupa tiek lietota, lai atrastu PVN kodu, kurš tiek lietots pārskata aprēķinos, ja uz pārskatu pārsūtītajai transakcijai nav PVN grupas. |
| Norādiet dabas resursu nodokļa informāciju kādam krājumam.         | Preču informācijas pārvaldības lapā **Izlaistās preces**, cilnē **Pārvaldīt krājumus**, laukā **Dabas resursu nodokļa grupa** norādiet kādu vērtību, lai dabas resursu nodokli aprēķinātu kādam krājumam pārdošanas vai krājumu transakcijās.                                                                                                                                              |

## <a name="report-setup"></a>Pārskatu iestatīšana
Lai varētu ģenerēt pārskatu **Dabas resursu nodoklis**, ir jāiestata rindas katram pārskata izkārtojumam. Katrā pārskata izkārtojumā katrai rindai izpildiet tālāk aprakstītās darbības.

1.  Noklikšķiniet uz **Nodokļi** &gt; **Iestatīšana** &gt; **PVN** &gt; **Dabas resursu nodokļa pārskata iestatīšana**.
2.  Noklikšķiniet uz **Jauns**.
3.  Laukā **Formas numurs** atlasiet iestatāmo formu no tālāk uzskaitītajām.
    -   **2. forma** — šajā formā tiek rādīta informācija par dabas resursu lietojumu un visu vides piesārņojumu, kas ir ģenerēts pārskata periodā.
    -   **3. forma** — šajā formā tiek rādīta informācija par dabas resursu nodokli, kas ir aprēķināts precēm, kuras uzņēmums importēja vai saražoja un pārdeva Latvijā pirmo reizi.

4.  Atlasiet sērijas numuru. Šis numurs norāda rindas pozīciju pārskatā iekļauto rindu virknē.
5.  Laukā **Rindas tips** atlasiet pārskata rindas tipu no tālāk uzskaitītajiem.
    -   **Galvene** — šī rinda pārskatu lapās tiek drukāta kā galvenes rindas.
    -   **Rinda**
    -   **Kopsumma** — rindā tiek rādīta rindu vērtību kopsumma.

6.  Ja 5. darbībā atlasījāt **Rinda**, ievadiet rindas kodu pārskata rindai **Dabas resursu nodoklis**.
7.  Laukā **Apraksts** ievadiet īsu transakcijas aprakstu.
8.  Laukā the **Kopsummas rindas kods** ievadiet kopsummas rindas kodu. Ja 5. darbībā atlasījāt **Rinda**, laukā **Noliktava** tiek rādīts noliktavas kods.
9.  Laukā **PVN kods** atlasiet PVN kodu, kurš tika izveidots dabas resursu nodokļa aprēķinam.
10. Laukā **Iepakojuma materiālu kods** atlasiet iepakojuma materiālu kodu, kurš tika izveidots dabas resursu nodoklim. Šis lauks nav pieejams, ja laukā **PVN kods** ir atlasīts kāds PVN kods. Vienlaicīgi ir pieejams tikai viens no šiem diviem laukiem.

### <a name="example-form-2-layout"></a>Piemērs. 2. formas izkārtojums

Šajā piemērā izkārtojumā ietilpst tālāk uzskaitītie informācijas elementi.

-   Galvene, kas sniedz ievadu par pārskata saturu
-   Rindas, kurās ir redzams apraksts un atsevišķas pārskata vērtības
-   Rindu vērtību kopsummas

| Formas numurs | Rindas tips | Sērijas numurs | Rindas kods | Apraksts                                | Kopsummas rindas kods | Novietojuma ID | Dabas resursu nodokļa kods | Iepakojuma materiāla kods |
|-------------|-----------|-----------------|-----------|--------------------------------------------|-----------------|-------------|----------------------------|-----------------------|
| 2. forma      | Galvene    | 1               |           | I. Nodoklis par dabas resursu lietojumu |                 |             |                            |                       |
| 2. forma      | Summa     | 2               | 1         | Dabas resursu lietojums (kopsumma)   | 3               |             |                            |                       |
| 2. forma      | Rinda      | 3               | 1.1       | Contoso Manufacturing Co                   | 1               | 785200      | NR-water                   |                       |
| 2. forma      | Rinda      | 4               | 1.2       | Smilšu karjers nr. 1                                | 1               | 600900      | NR-sand                    |                       |
| 2. forma      | Summa     | 5               | 2         | Vides piesārņojums (kopsumma)              | 3               |             |                            |                       |
| 2. forma      | Rinda      | 6               | 2.1       | Contoso Manufacturing Co                   | 2               | 785200      | NR-CO2                     |                       |
| 2. forma      | Rinda      | 7               | 2.1       | Pārskata rinda                             | 2               |             |                            |                       |
| 2. forma      | Kopsumma     | 8               | 3         | Kopsummas rinda (1. rinda + 2. rinda)                  |                 |             |                            |                       |
| 2. forma      | Rinda      | 9               | 4         | Pārskata rinda                             |                 |             |                            |                       |

### <a name="example-form-3-layout"></a>Piemērs. 3. formas izkārtojums

Šajā piemērā izkārtojumā ietilpst tālāk uzskaitītie elementi.

-   Galvene, kas sniedz ievadu par pārskata saturu
-   Rindas, kurās ir redzams apraksts un atsevišķas pārskata vērtības
-   Rindu vērtību kopsummas

| Formas numurs | Rindas tips | Sērijas numurs | Rindas kods | Apraksts                                                       | Kopsummas rindas kods | Novietojuma ID | Dabas resursu nodokļa kods | Iepakojuma materiāla kods |
|-------------|-----------|-----------------|-----------|-------------------------------------------------------------------|-----------------|-------------|----------------------------|-----------------------|
| 3. forma      | Galvene    | 1               |           | I. Nodoklis par bīstamām precēm, iepakojuma materiāliem un vienreizlietojamajiem traukiem |                 |             |                            |                       |
| 3. forma      | Kopsumma     | 2               | 1         | Bīstamas preces - Kopsumma:                                          | 4               |             |                            |                       |
| 3. forma      | Rinda      | 3               | 1.1       | Alumīnija folija                                                     | 1               |             | NR-GAlum                   |                       |
| 3. forma      | Rinda      | 4               | 1.2       |                                                                   | 1               |             |                            |                       |
| 3. forma      | Kopsumma     | 5               | 2         | Iepakojuma materiāli - Kopsumma:                                        | 4               |             |                            |                       |
| 3. forma      | Rinda      | 6               | 2.1       | Iepakojums: stikls                                                    | 2               |             |                            | PM-Glass              |
| 3. forma      | Rinda      | 7               | 2.2       | Iepakojums: plastmasa                                                 | 2               |             |                            | PM-Plastic            |
| 3. forma      | Rinda      | 8               | 2.3       | Iepakojums: metāla folija                                               | 2               |             |                            | PM-MetalF             |
| 3. forma      | Rinda      | 9               | 2.4       | Iepakojums: koks, papīrs, kartons                                     | 2               |             |                            | PM-WPC                |
| 3. forma      | Summa     | 10              | 3         | Vienreizlietojamie trauki - Kopsumma:                                         | 4               |             |                            |                       |
| 3. forma      | Rinda      | 11              | 3.1       | plastmasa                                                          | 3               |             |                            | T-Plast               |
| 3. forma      | Rinda      | 12              | 3.2       | Metāla folija                                                        | 3               |             |                            | T-MetalF              |
| 3. forma      | Rinda      | 13              | 3.3       | Koks, papīrs, kartons                                              | 3               |             |                            | T-WPC                 |
| 3. forma      | Summa     | 14              | 4         | Kopsummas rinda (1. rinda + 2. rinda + 3. rinda)                                 |                 |             |                            |                       |

## <a name="generate-the-natural-resources-tax-report"></a>Ģenerēt dabas resursu nodokļa pārskatu
Dabas resursu nodokļi tiek rēķināti krājumu žurnālu transakciju laikā un gadījumos, kad Latvijas debitoriem tiek izveidoti pārdošanas vai projektu rēķini, ja transakcijās ir iesaistīti krājumi, uz kuriem attiecas dabas resursu nodoklis. Šajā sadaļā ir aprakstīts, kā iegūt sarakstu ar dabas resursu nodokļa transakcijām, kas ir saistītas ar iepakojuma materiāliem, un kā izdrukāt dabas resursu nodokļa deklarāciju.

1. Noklikšķiniet uz **Nodokļi** &gt; **Deklarācijas** &gt; **PVN** &gt; **Dabas resursu nodoklis**.
2. Noklikšķiniet uz **Izveidot** &gt; **Izveidot dabas resursu nodokļa rindas iepakojumam**.
3. Ievadiet attiecīgā pārskatu perioda ceturksni un gadu.
4. Noklikšķiniet uz **Labi**, lai pārsūtītu informāciju, kura tiks izmantota, lai ģenerētu pārskatu par iepakojuma materiāliem šajā pārskata periodā.
5. Noklikšķiniet uz **Izveidot** &gt; **Izveidot dabas resursu nodokļa rindas krājumiem**.
6. Ievadiet attiecīgā pārskatu perioda ceturksni un gadu.
7. Noklikšķiniet uz **Labi**, lai pārsūtītu informāciju, kura tiks izmantota, lai ģenerētu pārskatu par bīstamu materiālu nodokli.
8. Kad dabas resursu nodokļa rindas ir izveidotas, katrā rindā informāciju varat manuāli pievienot vai modificēt.

   | Lauks                      | Apraksts                                                                                                                                                                                                                              |
   |----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   | Dokuments                    | Dokumenta numurs Virsgrāmatā.                                                                                                                                                                                                        |
   | Datums                       | Dabas resursu nodokļa transakcijas datums.                                                                                                                                                                                       |
   | Rēķins                    | Rēķina identifikators.                                                                                                                                                                                                           |
   | Transakcijas tips           | Dabas resursu nodokļa transakcijas tips. Pieejamās opcijas ir **Bīstamu krājumu nodoklis** un **Iepakojuma materiālu nodoklis**.                                                                                                |
   | Dabas resursu nodokļu grupa | Dabas resursu nodokļu grupa. Šis lauks nav pieejams, ja laukā **Transakcijas tips** ir atlasīta vērtība **Iepakojuma materiālu nodoklis**.                                                                                         |
   | PVN grupa            | Pārdošanas vai pirkšanas transakcijas laikā aprēķinātajiem dabas resursu nodokļiem izveidotā PVN grupa. Šis lauks nav pieejams, ja laukā **Transakcijas tips** ir atlasīta vērtība **Iepakojuma materiālu nodoklis**. |
   | PVN kods             | Kods, kas identificē PVN.                                                                                                                                                                                                  |
   | Nodokļa bāzes summa            | Sākotnējā summa, no kuras tiek rēķināts PVN. Šis lauks nav pieejams, ja laukā **Transakcijas tips** ir atlasīta vērtība **Iepakojuma materiālu nodoklis**.                                                                   |
   | PVN summa                 | Aprēķinātā PVN summa.                                                                                                                                                                                                         |
   | MK rinda                   | Atzīmējiet šo opciju, ja transakcija ir MK (materuālu komplekta) rinda.                                                                                                                                                                 |
   | Atsauce                  | Modulis, kas ģenerē šo transakciju.                                                                                                                                                                                               |
   | Numurs                     | Numurs, piemēram, pasūtījuma numurs, projekta numurs vai ražošanas numurs.                                                                                                                                                                  |
   | Atsauces tabulas ID         | Transakcijas avota tabula.                                                                                                                                                                                                    |
   | Atsauce                  | Avota atsauces lauks citā tabulā.                                                                                                                                                                                         |

   **Piezīme.** Lauku grupā **Iepakojuma materiāli** lauki ir pieejami tikai tad, ja laukā **Transakcijas tips** ir atlasīta opcija **Iepakojuma materiālu nodoklis**.
9. Noklikšķiniet uz **Datu validēšana**, lai validētu dabas resursu nodokļa transakciju rindas.
10. Izlabojiet visas kļūdas, rindas rediģējot manuāli.
11. Noklikšķiniet uz **Drukāt**.
12. Ievadiet pārskata gadu.
13. Atlasiet rīkotājdirektoru.
14. Atlasiet par pārskatu atbildīgo personu.
15. Atlasiet nodokļu iestādi.
16. Noklikšķiniet uz **Labi**, lai drukātu deklarāciju par dabas resursu nodokli.




