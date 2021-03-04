---
title: Ražošanas parametri ražošanas izpildes procesā
description: Šajā tēmā ir sniegta informācija par ražošanas parametru iestatīšanu modulī Ražošanas izpilde.
author: johanhoffmann
manager: tfehr
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e4d459fb516cca3825c0a1871797f83df4c1a7c6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432699"
---
# <a name="production-parameters-in-manufacturing-execution"></a>Ražošanas parametri ražošanas izpildes procesā

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegta informācija par ražošanas parametru iestatīšanu modulī Ražošanas izpilde.

Moduli **Ražošanas izpilde** galvenokārt ir paredzēts izmantot ražošanas uzņēmumos. To var izmantot, lai reģistrētu ražošanas darbu vai projektu laiku un krājumu patēriņu. Pirms moduli Ražošanas izpilde izmantot darbu reģistrācijai, ir jāiestata dažādi ražošanas parametri, kas nosaka, kā un kad reģistrācijas tiek grāmatotas ražošanas procesa laikā. Ražošanas parametru iestatījumi ietekmē krājumu pārvaldību, ražošanas pārvaldību un izmaksu aprēķinu.

Pirms darbinieki sāk reģistrācijas ražošanas darbos, nopietni apsveriet visus iestatījumus lapā **Ražošanas parametri**. Noklikšķiniet uz vienuma **Ražošanas kontrole** &gt; **Uzstādīt** &gt; **Ražošanas izpilde** &gt; **Ražošanas pasūtījuma noklusējuma vērtības**. Ja jūsu uzņēmums izmanto vairākvietu funkcijas, iespējams, vēlaties katrai vietai iestatīt atšķirīgas ražošanas parametrus. Parametri integrācijai modulī **Ražošana** tiek iestatīti tālāk norādītajās lapas **Ražošanas parametri** cilnēs.

- **Vispārīgi** — vispārīgi parametru iestatījumi ražošanas darbiem modulī Ražošanas izpilde.
- **Sākums** — parametri, kas izmantoti, kad ražošanas operācijas ir sāktas.
- **Operācijas** — parametri, kas tiek lietoti ražošanas operācijām un atsauksmēm par operācijām ražošanas procesa laikā.
- **Ziņot kā pabeigtu** — parametri, kas izmantoti, kad krājumi ražošanas pasūtījuma pēdējā operācijā ir pabeigti.
- **Daudzuma pārbaude** — parametri, kas tiek izmantot, lai pārbaudītu sākuma un atsauksmju daudzumus ražošanas pasūtījumos.

## <a name="types-of-production-jobs"></a>Ražošanas darbu tipi
Cilnē **Operācijas** varat atlasīt ražošanas darbu tipus, kuriem ir jāreģistrējas lapā **Darba reģistrācija**.

Parasti darbinieki reģistrējas iestatīšanas darbiem un procesa darbiem. Taču, ja tiek izmantota darbu plānošana, varat atlasīt citus darbu veidus, kam darbiniekiem ir jāreģistrējas, apstrādājot ražošanas pasūtījumus. Piemēram, varat pieprasīt transportēšanas darbu reģistrāciju.

> [!IMPORTANT]
> Noteikti atlasiet visus atbilstošos darbu veidus. Pretējā gadījumā darbi var nebūt pieejami reģistrācijai lapā **Darba reģistrācija**. Atlasei ir jāatbilst atlasēm lapas **Maršrutu grupas** cilnes **Iestatījumi** kolonnā **Darbu vadība** (**Ražošanas kontrole** &gt; **Iestatījumi** &gt; **Maršruti** &gt; **Maršrutu grupas**).

Ja opcija **Darbu vadība** joprojām ir atlasīta maršruta grupā, šis darba veids ražošanas pasūtījumā tiks ziņots kā pabeigts, kad darba pabeigšana ir ziņota modulī Ražošanas izpilde. Kad visi operācijas darbu veidi, kam ir atlasīta opcija **Darbu vadība**, ir reģistrēti kā pabeigti, arī modulī Ražošanas izpilde operācija tiek ziņota kā pabeigta.

> [!NOTE]
> Par dažiem darbu veidiem iespējams ziņot manuāli, izmantojot ražošanas žurnālus. Šādā gadījumā atlasiet darba veidam opciju **Darbu vadība**, taču neatlasiet darba veidu reģistrācijai moduļa Ražošanas izpilde lapas **Ražošanas parametri** cilnē **Operācijas**.

## <a name="bom-consumption-and-picking-list-journals"></a>MK patēriņš un izdošanas sarakstu žurnāli
Konsekventa materiālu komplekta (MK) patēriņa iestatīšana ir svarīga, jo tas palīdz garantēt efektīvu krājumu vadību. Piemēram, ja MK patēriņa parametri nav pareizi iestatīti modulī Ražošanas izpilde, materiāli var tikt atvilkti no krājuma divreiz vai vispār netikt atvilkti.

Lapā **Ražošanas parametri** automātisks MK patēriņš tiek iestatīts trīs posmos:

- Ražošanas sākumā. Šis posms jāiestata cilnē **Sākums**.
- Ražošanas procesa laikā pēc operācijas pabeigšanas. Šis posms jāiestata cilnē **Operācijas**.
- Kad tiek ziņots, ka ražošanas pasūtījums ir pabeigts. Šis posms jāiestata cilnē **Ziņot kā pabeigtu**.

Katram posmam laukā **Automātisks MK patēriņš** var atlasīt vienu no trim ražošanas pasūtījuma krājumu izdošanas metodēm.

- **Norakstīšanas princips** — šī opcija tiek izmantota kopā ar opciju, kas noteikta attiecībā uz MK modulī **Ražošana**. Noklikšķiniet uz **Ražošanas kontrole** &gt; **Vispārīgi** &gt; **Ražošanas pasūtījumi** &gt; **Visi ražošanas pasūtījumi**. Lapā **Visi ražošanas pasūtījumi** sarakstā izvēlieties ražošanas pasūtījumu un pēc tam darbību rūti noklikšķiniet uz **MK**. Lapas **MK** cilnes **Iestatījumi** laukā **Norakstīšanas princips** atlasiet vienu no šīm opcijām:

  - **Sākums**;
  - **Beigas**;
  - **Manuāli**;
  - tukšs (nav opcija ir izvēlēta);
  - **Pieejams atrašanās vietā**.

    Ja ražošanas izpildē cilnes **Sākums** laukā **Automātisks MK patēriņš** tika atlasīta metode **Norakstīšanas princips**, visi materiāli, kam iestatīta MK opcija **Sākums** tiek atvilkti no krājuma, kad operācija tiek sākta. Opcija **Pieejams atrašanās vietā** tiek izmantota precēm, kas ir iespējotas papildu noliktavas procesiem. Atlasot norakstīšanas principu, materiāli tiek norakstīti, kad izejmateriālu izdošanas noliktavas darbs ir pabeigts. Materiāli tiek norakstīti arī tad, kad MK rinda, kas izmanto šo norakstīšanas principu, tiek izdota noliktavā un materiāli ir pieejami ražošanas ievades atrašanās vietai.

    > [!NOTE]
    > Ja ražošanas izpildē laukam **Norakstīšanas princips** ir iestatīta opcija **Sākums**, tas pats princips ir jāatlasa cilnē **Operācijas** vai cilnē **Ziņot kā pabeigtu**. Šī prasība palīdz nodrošināt, ka materiāli tiek atskaitīti no tiem MK krājumiem, kuri ražošanas pasūtījumā kā norakstīšanas principu lieto opciju **Beigas**. Ja tas pats norakstīšanas princips nav atlasīts cilnē **Operācijas** vai **Ziņot kā pabeigtu**, materiāli var tikt atvilkti no krājumiem divas reizes.

- **Vienmēr** — atlasot posmam šo opciju, materiāli vienmēr tiek atvilkti no krājumiem šajā posmā. Piemēram, ražošanai nepieciešamie materiāli tiek atvilkti, kad ražošanas pasūtījums tiek sākts. Šis iestatījums nosaka, ka cilnē **Operācijas** un **Ziņot kā pabeigtu** jāatlasa opcija **Nekad**. Šī prasība neļauj vienības atvilkt no krājumiem divas reizes.
- **Nekad** — ja posmam atlasāt šo opciju, šajā posmā nav MK patēriņa. Piemēram, atlasot **Nekad** visas trīs cilnēs (**Sākums**, **Operācijas** un **Ziņot kā pabeigtu**), materiāli ir manuāli jāatvelk no krājumiem.

> [!IMPORTANT]
> Rūpīgi apsveriet ražošanas parametru iestatīšanu, un pārliecinieties, vai parametriem, kas atlasīti dažādās lapas **Ražošanas parametri** cilnēs nav pretrunā viens ar otru.

Tālāk sniegtajos piemēros ir aprakstīti parametru iestatījumi, kas atbalsta dažādus MK patēriņa principus. Ražošanas izpildē parametri tiek iestatīti lapā **Ražošanas parametri**.

### <a name="example-1-backflushing-on-operations"></a>1. piemērs — operāciju norakstīšana

Izmantojiet šos iestatījumus, ja izdošanas saraksta žurnāli ar MK krājuma patēriņu ir jāveido, kad krājumi operācijā ir pabeigti.

| Cilne                | Lauks                          | Iestatījums                             |
|--------------------|--------------------------------|-------------------------------------|
| Sākšana              | Labot sākšanu tiešsaistē           | **Statuss** vai **Statuss + daudzums** |
| Sākšana              | Automātisks MK patēriņš      | **Nekad**                           |
| Operations         | Automātisks MK patēriņš      | **Vienmēr**                          |
| Ziņot kā pabeigtu | Automātisks MK patēriņš      | **Nekad**                           |
| Ziņot kā pabeigtu | Labot pabeigtu pārskatu tiešsaistē | **Statuss + daudzums**               |

### <a name="example-2-backflushing-on-production"></a>2. piemērs — ražošanas norakstīšana

Izmantojiet šos iestatījumus, ja izdošanas saraksta žurnāli ar MK krājuma patēriņu ir jāveido, kad krājumi ražošanas pasūtījumā ir pabeigti.

| Cilne                | Lauks                          | Iestatījums                             |
|--------------------|--------------------------------|-------------------------------------|
| Sākšana              | Labot sākšanu tiešsaistē           | **Statuss** vai **Statuss + daudzums** |
| Sākšana              | Automātisks MK patēriņš      | **Nekad**                           |
| Operations         | Automātisks MK patēriņš      | **Nekad**                           |
| Ziņot kā pabeigtu | Automātisks MK patēriņš      | **Vienmēr**                          |
| Ziņot kā pabeigtu | Labot pabeigtu pārskatu tiešsaistē | **Statuss + daudzums**               |

### <a name="example-3-flushing-principle"></a>3. piemērs — norakstīšanas princips

Izmantojiet šos iestatījumus, ja izdošanas saraksta žurnāli ar MK krājuma patēriņu ir jāveido atbilstoši MK krājumu norakstīšanas principa iestatījumam.

| Cilne                | Lauks                          | Iestatījums                |
|--------------------|--------------------------------|------------------------|
| Sākšana              | Labot sākšanu tiešsaistē           | **Statuss + daudzums**  |
| Sākšana              | Automātisks MK patēriņš      | **Norakstīšanas princips** |
| Operations         | Automātisks MK patēriņš      | **Norakstīšanas princips** |
| Ziņot kā pabeigtu | Automātisks MK patēriņš      | **Nekad**              |
| Ziņot kā pabeigtu | Labot pabeigtu pārskatu tiešsaistē | **Statuss + daudzums**  |

### <a name="example-4-deduction-of-materials-during-startup-of-a-production-order"></a>4. piemērs: Materiālu ieturējumi, sākot ražošanas pasūtījumu

Izmantojiet šos iestatījumus, ja izdošanas saraksta žurnāli ar MK krājuma patēriņu ir jāveido, kad tiek sākta ražošana.

| Cilne                | Lauks                          | Iestatījums                             |
|--------------------|--------------------------------|-------------------------------------|
| Sākšana              | Labot sākšanu tiešsaistē           | **Statuss + daudzums**               |
| Sākšana              | Automātisks MK patēriņš      | **Vienmēr**                          |
| Operations         | Automātisks MK patēriņš      | **Nekad**                           |
| Ziņot kā pabeigtu | Automātisks MK patēriņš      | **Nekad**                           |
| Ziņot kā pabeigtu | Labot pabeigtu pārskatu tiešsaistē | **Statuss** vai **Statuss + daudzums** |

Pamatojoties uz atlasēm, kas ir aprakstītas iepriekš šajā sadāļā, izdošanas saraksta žurnāli tiek grāmatoti dažādos ražošanas pasūtījumu procesa posmos.

- Kad operācija tiek sākta
- Kad tiek ziņots par daudzumu operācijā
- Kad ražošanas pasūtījumā krājumi tiek reģistrēti kā pabeigti

### <a name="example-5-manual-bom-consumption"></a>5. piemērs: Manuāls MK patēriņš

Šos iestatījumus var izmantot, ja materiāli vienmēr ir manuāli jāatskaita no noliktavas. Šajā gadījumā izdošanas saraksta žurnāli netiek grāmatoti.


|        Cilne         |             Lauks              |         Iestatījums         |
|--------------------|--------------------------------|-------------------------|
|       Sākšana        |      Labot sākšanu tiešsaistē      | <strong>Statuss</strong> |
|       Sākšana        |   Automātisks MK patēriņš    | <strong>Nekad</strong>  |
|     Operations     |   Automātisks MK patēriņš    | <strong>Nekad</strong>  |
| Ziņot kā pabeigtu |   Automātisks MK patēriņš    | <strong>Nekad</strong>  |
| Ziņot kā pabeigtu | Labot pabeigtu pārskatu tiešsaistē | <strong>Statuss</strong> |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]