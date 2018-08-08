---
title: "MK un formulas rindu izlaišana nosūtīšanai uz noliktavu"
description: "Šajā tēmā ir aprakstīts, kā izejmateriālus MK rindām un formulas rindām izlaist nosūtīšanai uz noliktavu."
author: johanhoffmann
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: johanho
ms.search.validfrom: 2017-12-31
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: 83648a93f367510d7b04bbd04a9f37689ecfaa59
ms.openlocfilehash: 2bccabb033f5ba142b145e69930ce516aad596f2
ms.contentlocale: lv-lv
ms.lasthandoff: 05/23/2018

---

# <a name="release-bom-and-formula-lines-to-the-warehouse"></a>MK un formulas rindu izlaišana nosūtīšanai uz noliktavu

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā izejmateriālus materiālu komplektu (MK) rindām un formulas rindām izlaist nosūtīšanai uz noliktavu. Kad MK vai formulas rindu izlaižat nosūtīšanai uz noliktavu, sistēma vispirms nosaka, vai attiecīgais materiāls ražotnē jau ir pieejams ražošanas ievades novietojumā, kur šis materiāls tiks patērēts ražošanas procesam.

- Ja materiāls ir pieejams ražošanas ievades novietojumā, tas tiek izdots no šī novietojuma uzreiz pēc tam, kad tiek dots signāls materiāla izlaišanai pārvietošanai uz noliktavu.
- Ja materiāls nav pieejams ražošanas ievades novietojumā, materiāla izlaišana norāda, ka no novietojumiem noliktavā šis materiāls ir jāpārvieto uz ražošanas ievades novietojumu. Materiāls tiek pārvietots, izmantojot noliktavas darbu izejmateriālu izdošanai. Tādēļ ir jābūt konfigurētiem noliktavas procesiem izejmateriālu izdošanai. Papildinformāciju skatiet šeit: [Papildināšana](../warehousing/replenishment.md) un [Noliktavas darba kontrolēšana, izmantojot darbu veidnes un novietojuma direktīvas](../warehousing/control-warehouse-location-directives.md).

## <a name="methods-for-releasing-bom-and-formula-lines"></a>Metodes MK un formulas rindu izlaišanai

MK un formulas rindu izlaišanu var konfigurēt tā, lai tā notiktu kā daļa no ražošanas pasūtījuma vai partijas pasūtījumu izlaišanas. Alternatīvi izlaišanu var kontrolēt ar pakešuzdevumu vai kā manuālu mijiedarbību.

MK un formulas rindu izlaišanai izmantotā metode tiek kontrolēta ar parametru **Ražošanas rindas izlaišana**. Šis parametrs ir atrodams sadaļā **Ražošanas kontrole** \> **Iestatīšana** \> **Ražošanas parametri**.

- **Izlaist MK un formulas rindas kā daļu no ražošanas vai partijas pasūtījuma izlaišanas** — ar šo metodi MK un formulas rindas ražošanas vai partijas pasūtījumam tiek izlaistas kā daļa no pasūtījuma izlaišanas procesa. Ražošanas vai partijas pasūtījuma izlaišanas laikā parasti ražošanas darbi tiek izlaisti nodošanai ražotnes darbiniekiem un tiek drukāta ražošanas dokumentācija. Šī procesa laikā pasūtījuma statuss tiek arī mainīts uz **Izlaists**.
- **Izlaist MK un formulas rindas ar pakešuzdevumu vai kā manuālu mijiedarbību** — izmantojot šo metodi, MK un formulas rindas var izlaist vienīgi ar pakešuzdevumu **Automātiska MK un formulas rindu izlaišana** vai kā manuālu mijiedarbību. Lai MK un formulas rindas izlaistu manuāli, ražošanas pasūtījuma saraksta lapas vai ražošanas pasūtījuma informācijas lapas darbību rūtī atlasiet **Izlaist pārvietošanai uz noliktavu**.

Īsu demonstrāciju par to, kā izlaist MK un formulas rindas nosūtīšanai uz ražošanu, izmantojot pakešuzdevumu, noskatieties šo īso YouTube video: [Ražošanas izdošanas izlaišana uz noliktavu pakešveidā](https://www.youtube.com/watch?v=8urAJn50dQ8).

## <a name="releasing-the-bom-and-formula-lines-by-using-a-batch-job"></a>MK un formulas rindu izlaišana, izmantojot pakešuzdevumu

Pakešuzdevums **Automātiska MK un formulas rindu izlaišana** apstrādā atlasītās MK un formulas rindas, kam ir atlikušais izlaižamais daudzums. Darbs ņem vērā tikai pasūtījumus ar statusu **Izlaists**, **Sākts** vai **Ziņots kā pabeigts**. Ja MK vai formulas rindā ir daudzums, kas vēl ir jāizlaiž, darbs izlaiž ne vairāk kā daudzumu, ko var segt ar fiziski jau rezervēto daudzumu un fiziski pieejamo daudzumu.

### <a name="example-of-a-batch-job-release"></a>Pakešuzdevuma izlaišanas piemērs

| Scenārijs | Atlikušais izlaižamais daudzums | Fiziski rezervētais daudzums | Fiziski pieejamais daudzums | Daudzums, kas izlaists ar pakešuzdevumu |
|----------|-------------------------------|------------------------------|-------------------------------|------------------------------------|
| 1        | 100                           | 20                           | 90                            | 100                                |
| 2        | 100                           | 20                           | 70                            | 90                                 |
| 3        | 100                           | 0                            | 90                            | 90                                 |
| 4        | 100                           | 0                            | 110                           | 100                                |
| 5        | 100                           | 20                           | 0                             | 20                                 |

### <a name="batch-job-setup"></a>Pakešuzdevuma iestatīšana

Pakešuzdevuma **Automātiska MK un formulas rindu izlaišana** vaicājumā varat iestatīt filtra kritēriju, lai norādītu, cik dienas uz priekšu darbam ir jāmeklē rindas, kurās ir neizlaists daudzums. Darba vaicājuma laukā **Izejmateriālu reģistrēšanas datums** kā filtra kritēriju izmantojiet funkciju **(LessThanDate())**.

Nākamajā attēlā ir parādīts ražošanas pasūtījums, kurā ir divi darbi — 10 un 20 —, kuri aptver ražošanas pasūtījumam paredzēto montēšanu un iepakošanu. Katram darbam ir iestatīts patērēt noteiktu materiālu daudzumu. Šajā attēlā izlaišanas periods, kas ir norādīts ar zaļo bultu zem laika līnijas, ir vienāds ar dienu skaitu, kas ir norādīts ar kritēriju **(LessThanDate())**. Piemēram, **(LessThanDate(2))** norāda, ka darbam ir jāmeklē neizlaistais daudzums tikai divu dienu periodā.

![Ražošanas pasūtījuma piemērs ar diviem pakešuzdevumiem](media/bach-job-setup.PNG)

## <a name="releasing-material-per-operation-number-or-in-proportion-to-the-amount-of-finished-goods"></a>Materiāla izlaišana katram operācijas numuram vai proporcionāli pabeigto preču daudzumam

Ja materiālus izlaižat, izmantojot parametra **Veicot ražošanas pasūtījuma izlaišanu** iestatījumu, kad veicat manuālu izlaišanu, materiālu izlaišanas kontrolei jums ir divas tālāk aprakstītās opcijas.

- Izlaist materiālu katram operācijas numuram.
- Izlaist materiālu proporcionāli pabeigto preču daudzumam.

### <a name="release-material-per-operation-number"></a>Materiāla izlaišana katram operācijas numuram

Lai kontrolētu operācijas, uz kurām ir jāizlaiž materiāls, izmantojiet lapu **Izlaist pārvietošanai uz noliktavu**.

- Atlasiet **Ražošanas kontrole** \> **Ražošanas pasūtījumi** \> **Visi ražošanas pasūtījumi**, atlasiet kādu ražošanas pasūtījumu un pēc tam cilnē **Noliktava** atlasiet **Izlaist pārvietošanai uz noliktavu**. Pēc tam izmantojiet lauku **No operācijas Nr.** un **Līdz operācijai Nr.**, lai norādītu operācijas numuru diapazonu.

Nākamajā attēlā ir parādīts ražošanas pasūtījums, kurā ir divas operācijas — 10 un 20. Ja šajā piemērā ierobežojat izlaišanu uz operāciju 10, tiek izlaists tikai materiāls M9203.

![Piemērs par materiāla izlaišanu katram operācijas numuram](media/two-operations.PNG)

Īsu demonstrāciju par to, kā izlaist materiālu proporcionāli pabeigto preču daudzumam, varat skatīties šajā YouTube videoklipā: [Ražošanas pasūtījuma izlaišanas procesa uzlabojumi programmā Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=Rm3ojAz6Zu0)

### <a name="release-material-in-proportion-to-the-amount-of-finished-goods"></a>Materiāla izlaišana proporcionāli pabeigto preču daudzumam

Izejmateriālu varat izlaist daļējam gatavo preču daudzumam vai noteiktā vienībā.

- Lai izejmateriālu izlaistu daļējam gatavo preču daudzumam, atlasiet **Ražošanas kontrole** \> **Ražošanas pasūtījumi** \> **Visi ražošanas pasūtījumi**, atlasiet kādu ražošanas pasūtījumu un pēc tam cilnē **Noliktava** atlasiet **Izlaist pārvietošanai uz noliktavu**. Pēc tam ievadiet daudzumu laukā **Daudzums**.

    Piemēram, tiek izveidots ražošanas pasūtījums, kurš ir plānots 1000 gabaliem (gab.). Ražotnes vadītājs plāno 100 gab. ražošanu nākamajai maiņai un vēlas izlaist materiālus tikai šai maiņai. Šajā gadījumā vadītājs var izmantot lauku **Daudzums**, lai izlaistu materiālus tiem 100 gab., kuri tiek plānoti nākamajai maiņai.

- Lai izejmateriālu izlaistu noteiktā vienībā, atlasiet **Ražošanas kontrole** \> **Ražošanas pasūtījumi** \> **Visi ražošanas pasūtījumi**, atlasiet kādu ražošanas pasūtījumu un pēc tam cilnē **Noliktava** atlasiet **Izlaist pārvietošanai uz noliktavu**. Pēc tam izmantojiet lauku **Vienība**, lai atlasītu pabeigto preču mērvienību, kādā izlaist materiālu.

    Pieejamās mērvienības ir definētas ar pabeigto preču vienību secību grupas ID.

    Piemēram, pabeigtai precei ir šāda mērvienību konvertēšana starp mārciņām (mārc.) un paletēm (PL): 1 PL = 100 mārc. Lai izveidotu ražošanas pasūtījumu 10 000 mārc. pabeigto preču, varat izlaist izejmateriālus tādam palešu skaitam, kādu plānojat saražot. Kā vienību atlasiet **PL** un pēc tam atlasiet atbilstošu skaitu laukā **Daudzums**.

