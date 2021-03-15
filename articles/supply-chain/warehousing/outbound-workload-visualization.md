---
title: Izejošās darba slodzes vizualizācija
description: Šajā tēmā ir sniegta informācija par izejošo darba slodzes vizualizāciju. Šī funkcionalitāte ļauj noliktavas pārvaldniekiem un uzraugiem izveidot pielāgotas darba slodzes diagrammas, ko var izmantot, lai pārraudzītu pašreizējā darba norisi un atlikušo daudzumu. Noliktavas pārvaldnieki var izveidot vairākus skatījumus un iestatīt automātisko atsvaidzināšanu pēc to nepieciešamības.
author: Mirzaab
manager: tfehr
ms.date: 08/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-08-28
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 2515a71297df7213f93a4c619f7eebf1c2411b39
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965556"
---
# <a name="outbound-workload-visualization"></a>Izejošās darba slodzes vizualizācija

[!include [banner](../includes/banner.md)]

Papildu iestatīšanas iespējas, kas pieejamas lapā **Izejošā darba slodzes vizualizācija**, ļauj noliktavas pārvaldniekiem un uzraugiem izveidot pielāgotas darba slodzes diagrammas, ko var izmantot, lai pārraudzītu pašreizējā darba norisi un atlikušo daudzumu. Noliktavas pārvaldnieki var izveidot vairākus skatījumus un iestatīt automātisko atsvaidzināšanu pēc to nepieciešamības. Izejošās darba slodzes vizualizācija ir piemērotas rādīšanai noliktavas veiktspējas lapās.

Šo funkcionalitāti var izmantot, lai izsekotu izdošanas darba norisi. Šis līdzeklis ir integrēts ar darba pārvaldību, un, ja darba pārvaldība ir iestatīta, izejošās darba slodzes vizualizācijas var rādīt stundu skaita aprēķinu, kas paliek parādītajam izdošanas darbam (filtrēts).

## <a name="turn-on-the-outbound-workload-visualization-feature"></a>Ieslēgt līdzekli Izejošās darba slodzes vizualizācija

Lai varētu izmantot šo līdzekli, tas vispirms ir jāiespējo jūsu sistēmā. Administratori var izmantot [Funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Noliktavas pārvaldība*
- **Līdzekļa nosaukums:** *Ieslēgt līdzekli Izejošās darba slodzes vizualizācija*

## <a name="set-up-outbound-workload-visualizations"></a>Iestatīt izejošās darba slodzes vizualizācijas

Lai iestatītu vizualizācijas, izveidojiet filtru (skatus) un katra filtra noformējumu, lai tas uzrādītu citu analīzes tipu. Lai izstrādātu filtrus, izmantojiet lapu **Konfigurēt filtrus**.

Lai iestatītu izejošās darba slodzes vizualizāciju, veiciet šīs darbības.

1. Doties uz **Noliktavas pārvaldība \> Noliktavas pārraudzības pārskati \> Izejošās darba slodzes vizualizācija**.

    Tiek parādīta lapa **Izejošās darba slodzes vizualizācija**. Kad ir izveidoti daži filtri, šī lapa parādīs jūsu vizualizāciju. Filtru skaits nav ierobežots. Visi izveidotie filtri tiek saglabāti jūsu lietotāja kontā, lai tos varētu izmantot vēlāk. Citiem vārdiem sakot, katram lietotājam būs sava izveidoto filtru kopa. Šie filtri netiks koplietoti ar citiem lietotājiem.

1. Lapā **Izejošās darba slodzes vizualizācija** darbību rūtī cilnē **Filtri** atlasiet **Konfigurēt filtrus**.
1. Lapā **Konfigurēt filtrus**, kas atrodas darbības rūtī, atlasiet **Jauns**, lai pievienotu filtru, un pēc tam iestatiet tālāk norādītos laukus.

    - **X ass grupas tabula** - atlasiet tabulu, kas satur lauku, kas jāizmanto, lai grupētu x ass vērtības.
    - **X ass grupas lauks** – no tabulas laukiem, kas atlasīti laukā **X ass grupas tabula**, atlasiet lauku, kas jāizmanto x ass vērtību grupēšanai.
    - **X ass vērtību tabula** - atlasiet tabulu, kas satur lauku, kas jāizmanto, lai tālāk analizētu grupas.
    - **X ass vērtību lauks** – no tabulas laukiem, kas atlasīti laukā **X ass vērtību tabula**, atlasiet lauku, kas nodrošina vērtības, kas ir jāanalizē katrai grupai.
    - **Automātiskā atsvaidzināšana** – atlasiet, vai vizualizācija ir automātiski jāatsvaidzina.
    - **Atsvaidzināšanas intervāls (minūtēs)** - ievadiet minūšu skaitu no automātiskās atsvaidzināšanas.
    - **Displeja līmenis** – atlasiet, vai diagrammai jārāda atvērtās rindas vai atvērto virsrakstu skaits.
    - **Izdošanas veids** - ja iestatāt lauku **Displeja līmenis** uz _Atvērtajām rindām_, izvēlieties, vai diagrammā atvērto darba rindu skaitam ir jāietver sākuma izdošana, pakāpeniskā izdošana vai gan sākotnējā, gan pakāpeniskā izdošana.
    - **Vietne** — atlasiet vietni, kur ielādēt diagrammu.
    - **Noliktava** — atlasiet noliktavu, kur ielādēt diagrammu.
    - **Dienas, kuras iekļaut** - ievadiet to dienu skaitu pagātnē, kurām ir jāģenerē diagramma.
    - **Darba pasūtījuma veids** - atlasiet izejošās darba slodzes tipus, ko filtrēt.

    ![Konfigurēt filtru lapu](media/work-viz-filters-1.png "Konfigurēt filtru lapu")

1. Aizveriet lapu **Konfigurēt filtrus**, lai atgrieztos lapā **Izejošās darba slodzes vizualizācijas**.

    Lapa **Izejošās darba slodzes vizualizācijas** tagad rāda datus, pamatojoties uz jaunajiem filtra iestatījumiem. Jaunais filtrs tagad ir pieejams, un tas ir atlasīts **Filtra** laukā. Tālāk norādītie lauki ir pieejami diagrammas augšā:

    - **Filtrs** – šajā laukā ir ietverti visi līdz šim izveidotie filtri. Atlasiet filtru, lai skatītu tā datus diagrammā.
    - **Pēdējoreiz atsvaidzināts** – šis lauks rāda datumu un laiku, kad informācija diagrammā tika pēdējoreiz atjaunināta.
    - **Novērtētais/faktiskais laiks** - ja sistēmā ir iestatīti darbaspēka standarti, iestatiet šo opciju uz *Jā*, lai parādītu uzkrātos paredzamos izdošanas laikus katras diagrammas kolonnas sākumā. Ja neizmantojat darba standartus, šī opcija nav pieejama.

    ![Vizualizācijas piemērs](media/work-viz-chart.png "Vizualizācijas piemērs")

1. Atlasiet jebkuru stabiņu diagrammā, lai skatītu saistīto informāciju par darbu rindu.

    ![Detalizēta darba rindas informācija](media/work-viz-work-details.png "Detalizēta darba rindas informācija")

## <a name="example-outbound-workload-visualization-for-zones"></a>Piemērs: Izejošās darba slodzes vizualizācija zonām

Šim piemēram jūs vēlaties iestatīt vizualizāciju, kas rāda darba rindas katrai zonai, un katras darba rindas statusu (_Atvērts_, _Slēgts_ vai _Atcelts_). Šādā gadījumā varat iestatīt filtru, kam ir sekojoši iestatījumi:

- **Filtra nosaukums** - ievadiet šī filtra nosaukumu (piemēram, _Zona pret darba statusu_).
- **Apraksts** - ievadiet šī filtra īsu aprakstu (piemēram, _Zona pret darba statusu_).
- **X ass grupas tabula** - atlasiet _Atrašanās vietas._
- **X ass grupa** - atlasiet _Zonas ID_.
- **X ass vērtību tabula** - atlasiet _Darbu_, jo vēlaties skatīt darbu pa zonām.
- **X ass vērtību lauks** - atlasiet _Darba statusu_, jo vēlaties skatīt darba statusu.
- **Automātiskā atsvaidzināšana** – atlasiet, vai vizualizācija ir automātiski jāatsvaidzina.
- **Izdošanas veids** - atlasiet _Sākotnējā izdošana un pakāpeniskā izdošana_, jo jūs vēlaties ietvert gan sākotnējās savākšanas, gan savākšanas vietas. Citiem vārdiem sakot, jūs būtībā vēlaties iekļaut visas izdošanas darba rindas, kas jums ir.
- **Displeja līmenis** - atlasiet _Atvērtās rindas_, jo vēlaties skatīt informāciju pa rindām, nevis darba virsrakstā.

Tālāk redzamajā attēlā ir parādīts iegūtās diagrammas piemērs.

![Zona pret darba statusa vizualizāciju](media/work-viz-chart.png "Zona pret darba statusa vizualizāciju")

Šajā diagrammā tiek rādītas divas zonas ar nosaukumu **GRĪDA** un **LIELAPJOMA**, kā arī zona ar nosaukumu **Tukšs**. **Tukšajā** zonā attēlotas visas darba rindas, kas nav nevienas zonas dalībnieki. Diagramma vienmēr parāda visus nesaistītos filtrētos datus kā **Tukšus**, lai nodrošinātu pēc iespējas lielāku redzamību. **GRĪDAS** zonā diagramma rāda trīs slēgtas rindas un četras atvērtās rindas. **LIELAPJOMA** zonā diagramma rāda četras slēgtas rindas, vienu atvērtu rindu un 24 atceltās rindas. Visbeidzot diagramma rāda astoņas slēgtas rindas, kas nav daļa no nevienas zonas, tāpēc ir uzskaitītas kā **Tukšas**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]