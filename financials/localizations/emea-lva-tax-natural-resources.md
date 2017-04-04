---
title: "Dabas resursu nodokļa pārskats"
description: "Šajā tēmā ir paskaidrots, kā iestatīt un radīt nodoklis par dabas resursiem (NR nodokļu) ziņojums."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LvNRTaxItemGroupLookup
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 270454
ms.assetid: ca5fb637-e01b-4499-9bc4-51da02b8c61a
ms.search.region: Latvia
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: 422d944d4d7ee2388017ba84a686fad4252e2012
ms.lasthandoff: 03/31/2017


---

# <a name="tax-on-natural-resources-report"></a>Dabas resursu nodokļa pārskats

Šajā tēmā ir paskaidrots, kā iestatīt un radīt nodoklis par dabas resursiem (NR nodokļu) ziņojums.

Latviešu uzņēmumi ir periodiski jāiesniedz **dabas resursu nodokli** (**NR nodokļu**) ziņojums. Šī darbība attiecas tikai uz juridiskām personām Latvija. Arī nodoklis jāaprēķina par importēto vai pašu ražotās preces, kas tiek izmantots iekšēji. Visbeidzot, iepakojuma materiāli, ko izmanto iepakojuma precēm, kas tiek pārdoti pārskata periodā ir jāaprēķina nodoklis par dabas resursiem.

## <a name="prerequisites"></a>Priekšnosacījumi
| Priekšnoteikumi                                                   | Papildinformācija                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Iestatīt PVN iestādi.                                        |    |
| Iestatiet Virsgrāmatas grāmatošanas grupas, par dabas resursu nodokli. |  |
| Iestatītu apmaksas periodu, par dabas resursu nodokli.      |  |
| Jāiestata PVN kodi par dabas resursu nodokli.          | |
| Iestatīt PVN grupas, par dabas resursu nodokli.         |  |
| Iestatīt PVN grupas, par dabas resursu nodokli.               | Lietošanas **dabas resursu nodokļu grupa** lapu, lai uzstādītu PVN grupām, kas nosaka pareizo PVN kodiem, kas pamatojas uz krustojuma nodokļu grupu un PVN grupu par dabas resursu nodokli.                                                                                                                                                                                                    |
| Iestatiet krājumu parametros.                                   | Par **krājumu un noliktavu pārvaldības parametri** lapa, kas **Aprēķiniet iepakojuma materiālu izmaksas** iespēju **Jā**. Šajā **PVN grupa** lauku, atlasiet PVN grupu, par dabas resursu nodokli. Pēc noklusējuma šī PVN grupa tiek lietota, lai atrastu PVN kodu, kas tiek lietots atskaitē aprēķiniem, ja darbība, kas tiek pārsūtīts ziņojums ir bez PVN grupu. |
| Norādiet vienuma dabas resursu nodokļu informāciju.         | Produkta informācijas pārvaldību, par **atbrīvo produktus** lapa par **pārvaldīt krājumu** cilni, jo **dabas resursu nodokļu grupas** lauku, norādiet vērtību, lai aprēķinātu dabas resursu nodokli pārdošanai vai krājumu darbības krājumam.                                                                                                                                              |

## <a name="report-setup"></a>Pārskatu izveidošana
Pirms varat ģenerēt **dabas resursu nodokļu** atskaitē iestatiet rindas par katru atskaites izkārtojumu. Atkārtot šīs darbības katrai rindai katrā atskaites izkārtojumu.

1.  Noklikšķiniet uz **nodokļu**&gt;**Setup**&gt;**PVN**&gt;**dabas resursu nodokļa pārskata iestatījumi**.
2.  Click **New**.
3.  Šajā **formas numurs** lauku, atlasiet formu, lai iestatītu:
    -   **Form 2** -šī forma parāda informāciju par izmantošanu dabas resursus un vides piesārņojumu, kas tiek ģenerēta pārskata periodā.
    -   **Veidlapa Nr. 3** -šī forma tiek parādīta informācija par dabas resursu nodokli, kas aprēķināts attiecībā uz precēm, kas ievesti vai uzņēmums ražo un pārdod Latvija pirmo reizi.

4.  Atlasiet sērijas numuru. Šis skaitlis norāda rindas pozīciju secībā no atskaites līnijas.
5.  Šajā **līnijas veidu** lauku, atlasiet atskaites rindas tips:
    -   **Galvenes** -rinda tiek drukāta kā galvenes rindas atskaites lapās.
    -   **Line**
    -   **Kopējais** -rinda rāda kopsavilkuma rindu vērtības.

6.  Ja esat atlasījis **Line** 5. solī ievadiet rindas kods **dabas resursu nodokļa** atskaites līniju.
7.  Šajā **aprakstu** laukā, ievadiet īsu darbības aprakstu.
8.  Šajā **Total rindas kods** ievadiet kopējo līniju kodu. Ja esat atlasījis **Line** solis 5, **noliktava** laukā ir norādīts noliktavas kods.
9.  Šajā **PVN kods** lauku, atlasiet PVN kodu, kas tika izveidota dabas resursu nodokļa aprēķināšanai.
10. Šajā **iepakojuma materiālu kodam** lauku, atlasiet iepakojuma materiāla kodu, kas tika izveidota, par dabas resursu nodokli. Šis lauks nav pieejams, atlasot PVN kodu laukā **PVN kods** lauks. Tikai viens no šiem diviem laukiem ir pieejama laikā.

### <a name="example-form-2-layout"></a>Piemērs: 2 formas izkārtojumu

Šis piemērs izkārtojums satur šādus informācijas elementus:

-   Galvenes, kas iepazīstina ar pārskata saturu
-   Rindas, kas parāda apraksti un atsevišķas atskaites vērtības
-   Kopsummas rindas vērtības

| Formas numurs | Rindas tips | Sērijas numurs | Rindas kods | apraksts                                | Kopsummas rindas kods | Atrašanās vietas Id | Dabas resursu nodokļa kods | Iepakojuma materiāla kods |
|-------------|-----------|-----------------|-----------|--------------------------------------------|-----------------|-------------|----------------------------|-----------------------|
| 2. forma      | Virsraksts    | 1.               |           | Es. Nodoklis par dabas resursu izmantošanu |                 |             |                            |                       |
| 2. forma      | Summa     | 2.               | 1.         | Dabas resursu (kopā) izmantošanu   | 3.               |             |                            |                       |
| 2. forma      | Līnija      | 3.               | 1,1       | "Contoso" ražošanas Co                   | 1.               | 785200      | NR-ūdens                   |                       |
| 2. forma      | Līnija      | 4.               | 1,2       | Smilšu kaste Nr1                                | 1.               | 600900      | NR-smilšu                    |                       |
| 2. forma      | Summa     | 5.               | 2.         | Vides piesārņojums (kopā)              | 3.               |             |                            |                       |
| 2. forma      | Līnija      | 6.               | 2,1       | "Contoso" ražošanas Co                   | 2.               | 785200      | NR CO2                     |                       |
| 2. forma      | Līnija      | 7.               | 2,1       | Pārskata rindas                             | 2.               |             |                            |                       |
| 2. forma      | Summa     | 8.               | 3.         | Kopsummas rindā (1 + 2)                  |                 |             |                            |                       |
| 2. forma      | Līnija      | 9.               | 4.         | Pārskata rindas                             |                 |             |                            |                       |

### <a name="example-form-3-layout"></a>Piemērs: 3 formas izkārtojumu

Šajā piemērā izkārtojuma ir šādi elementi:

-   Galvenes, kas iepazīstina ar pārskata saturu
-   Rindas, kas parāda apraksti un atsevišķas atskaites vērtības
-   Kopsummas rindas vērtības

| Formas numurs | Rindas tips | Sērijas numurs | Rindas kods | apraksts                                                       | Kopsummas rindas kods | Atrašanās vietas Id | Dabas resursu nodokļa kods | Iepakojuma materiāla kods |
|-------------|-----------|-----------------|-----------|-------------------------------------------------------------------|-----------------|-------------|----------------------------|-----------------------|
| 3. forma      | Virsraksts    | 1.               |           | Es. Nodoklis par bīstamām precēm, iepakojuma materiālus un reklamācija ēdieni |                 |             |                            |                       |
| 3. forma      | Summa     | 2.               | 1.         | Bīstamās preces - pavisam:                                          | 4.               |             |                            |                       |
| 3. forma      | Līnija      | 3.               | 1,1       | Alumīnija foliju                                                     | 1.               |             | NR GAlum                   |                       |
| 3. forma      | Līnija      | 4.               | 1,2       |                                                                   | 1.               |             |                            |                       |
| 3. forma      | Summa     | 5.               | 2.         | Iepakošanas materiāli - pavisam:                                        | 4.               |             |                            |                       |
| 3. forma      | Līnija      | 6.               | 2,1       | Iepakošana: stikla                                                    | 2.               |             |                            | PM-stikla              |
| 3. forma      | Līnija      | 7.               | 2.2       | Iepakošana: plastmasa                                                 | 2.               |             |                            | PM-plastmasas            |
| 3. forma      | Līnija      | 8.               | 2.3       | Iepakojums: metāla folija                                               | 2.               |             |                            | PM-MetalF             |
| 3. forma      | Līnija      | 9.               | 2.4       | Iepakojums: koka, papīra, kartona kārbās                                     | 2.               |             |                            | PM-WPC                |
| 3. forma      | Summa     | 10.              | 3.         | Reklamācija ēdieni - pavisam:                                         | 4.               |             |                            |                       |
| 3. forma      | Līnija      | 11.              | 3.1       | plastmasa                                                          | 3.               |             |                            | T-Plast               |
| 3. forma      | Līnija      | 12.              | 3.2       | Metāla folija                                                        | 3.               |             |                            | T MetalF              |
| 3. forma      | Līnija      | 13.              | 3.3       | Koksne, papīrs, kartons                                              | 3.               |             |                            | T-WPC                 |
| 3. forma      | Summa     | 14.              | 4.         | Kopsummas rindā (1 + 2 + line3)                                 |                 |             |                            |                       |

## <a name="generate-the-natural-resources-tax-report"></a>Dabas resursu nodokļu atskaites ģenerēšanai
Dabas resursu nodokļi tiek aprēķināti krājumu žurnāla darbību laikā, un, kad pārdošanas vai projekta rēķini tiek izveidoti latviešu patērētājus, ja darījumi ietver krājumus, kas tiek apliktas ar dabas resursu nodokli. Šajā sadaļā aprakstīts, saņemt sarakstu ar dabas resursu nodokļu darbībām, kas saistītas ar iepakojuma materiāliem un izdrukāt dabas resursu nodokļa deklarācija.

1.  Noklikšķiniet uz **nodokļu**&gt;**deklarācijas**&gt;**PVN**&gt;**dabas resursu nodokli**.
2.  Noklikšķiniet uz **veidot**&gt;**izveidot dabas resursu nodokļu rindas iepakojuma**.
3.  Ievadiet ceturkšņa un gada pārskata perioda.
4.  Noklikšķiniet uz **OK** nodot informāciju, kas tiek lietota, lai ģenerētu pārskatu par iepakojuma materiāliem par pārskata perioda nodokli.
5.  Noklikšķiniet uz **veidot**&gt;**izveidot dabas resursu nodokļu rindas krājumos,**.
6.  Ievadiet ceturkšņa un gada pārskata perioda.
7.  Noklikšķiniet uz **OK** nodot informāciju, kas tiek lietota, lai ģenerētu atskaiti par nodokli par bīstamiem materiāliem.
8.  Pēc dabas resursu nodokļu rindas izveidošanas, var manuāli pievienot vai modificēt norādīto informāciju, katrā rindā.
    | Lauks                      | apraksts                                                                                                                                                                                                                              |
    |----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Dokuments                    | Dokumenta numurs Virsgrāmatā.                                                                                                                                                                                                        |
    | Datums                       | Datumu no dabas resursu nodokļa darbību.                                                                                                                                                                                       |
    | Rēķins                    | Rēķina identifikators.                                                                                                                                                                                                           |
    | Darbības veids           | Veida dabas resursu nodokļa darbību. Pieejamās opcijas ir **par bīstamām precēm nodokli** un **nodokli par iepakojuma materiāliem**.                                                                                                |
    | Dabas resursu nodokļu grupa | Dabas resursu nodokļu grupu. Šis lauks nav pieejams **nodokli par iepakojuma materiāliem** atlasīta **transakcijas tipu** lauks.                                                                                         |
    | PVN grupa            | PVN grupa, kas izveidota dabas resursu nodokļi, kas tiek aprēķināts pārdošanas vai pirkšanas darbību laikā. Šis lauks nav pieejams **nodokli par iepakojuma materiāliem** atlasīta **transakcijas tipu** lauks. |
    | PVN kods             | Kods, kurš identificē PVN.                                                                                                                                                                                                  |
    | PVN bāzes summa            | PVN tiek aprēķināts no sākotnējās summas. Šis lauks nav pieejams **nodokli par iepakojuma materiāliem** atlasīta **transakcijas tipu** lauks.                                                                   |
    | PVN summa                 | Aprēķinātā PVN summa.                                                                                                                                                                                                         |
    | MK rinda                   | Atlasiet šo opciju, ja darbība ir MK (materiālu komplekta) līnija.                                                                                                                                                                 |
    | Atsauce                  | Moduli, kas ģenerē darbības.                                                                                                                                                                                               |
    | Skaits                     | Skaitli, piemēram, pasūtījuma numuru, projekta numuru vai ražošanas uzdevuma numurs.                                                                                                                                                                  |
    | Atsauces tabulas ID         | Avota tabulas darbības.                                                                                                                                                                                                    |
    | Atsauce                  | Atsauces avota laukā citā tabulā.                                                                                                                                                                                         |

    **Piezīme:** laukos **iepakojuma materiālu** lauka grupa ir pieejama tikai tad, ja atlasāt **nodokli par iepakojuma materiāliem**, **transakcijas tipu** lauks.
9.  Noklikšķiniet uz **datu validācijas** apstiprināt dabas resursu nodokļa darbību rindas.
10. Izlabojiet kļūdas manuāli rediģējot līnijas.
11. Click **Print**.
12. Ievadiet atskaites gadu.
13. Atlasiet rīkotājdirektors.
14. Atlasiet personu, kura ir atbildīga par ziņojumu.
15. Atlasiet PVN iestādi.
16. Noklikšķiniet uz **OK** drukāt pārskatu par dabas resursu nodokli.



