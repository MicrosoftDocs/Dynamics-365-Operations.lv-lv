---
title: Nomu pārvaldība, izmantojot nomas importēšanas struktūru
description: Šajā tēmā skaidrots, kā izmantot nomas importēšanas struktūru, lai vienlaicīgi koriģētu vairākas nomas.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d7a7d2afd8f352bc167ec8c0a354ee4ac0a9e77b
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4445794"
---
# <a name="manage-leases-through-the-lease-import-framework"></a>Nomu pārvaldība, izmantojot nomas importēšanas struktūru

[!include [banner](../includes/banner.md)]

Šajā tēmā skaidrots, kā izmantot nomas importēšanas struktūru, lai ar vienu darbību koriģētu vairākas nomas. Izmantojot šo iespēju, varat ietaupīt laiku un varat arī nodrošināt precīzākas korekcijas, samazinot cilvēka kļūdas iespējamību. Turklāt šī iespēja var savienot Microsoft Dynamics 365 Finance ar ārējo datu vienībām, lai efektīvi augšupielādētu datus.

Tālāk norādītos datu elementus var izmantot, lai integrētu līdzekļu nomu ar ārējām sistēmām:

- Nomas sagatavošana
- Maksājumu līguma sagatavošana
- Izpildes līguma sagatavošana

Varat izmantot importēšanas procesu, lai koriģētu nomu, atjauninātu nefinanšu informāciju vai pievienotu jaunas nomas. Pirms importēšanas varat apskatīt un rediģēt nomas datus.

Sistēma var izpildīt trīs tālāk minētos procesus, izmantojot nomas importēšanas komplektu.

| Procesa tips  | Apraksts |
|---------------|-------------|
| Pievienot ierakstu    | Migrētās nomas, kurām ir šis procesa tips, veido nomu sistēmā. Maksājumu grafiks ir manuāli jāapstiprina, un sākotnējās atpazīšanas žurnāla ieraksts pēc migrācijas ir manuāli jāiegrāmato. |
| Labot ierakstu | Migrētās nomas, kurām ir šī procesa tipa atjaunināšanas lauka vērtības nomai, kas jau ir sistēmā. Tiek atjaunināti tikai tie lauki, kas ir atlasīti lapā **Atjaunināt lauku atlasi**. Mēs iesakām atlasīt nefinanšu laukus lapā **Atjaunināt lauku atlasi**, jo šis procesa tips nepielāgo nomu. |
| Koriģēt ierakstu | Migrētās nomas, kurām ir šis procesa tips, pielāgo nomu. Šī korekcija izraisa finanšu nomas modifikāciju. Pēc nomas apstrādāšanas sistēma izveido jaunu maksājumu grafiku, izmantojot jaunos datus no nomas importēšanas komplekta. Sistēma neapstiprina maksājuma grafiku u negrāmato korekcijas žurnāla ierakstu. |

Pēc informācijas augšupielādes, izmantojot **Datu pārvaldības** darbvietu, atveriet **Virsraksta importēšanas** lapu ( **Līdzekļa noma \>Nomas importēšanas struktūra \> Virsraksta importēšana**). Šajā lapā uzskaitītas visas trīs datu entītijas, kas tika uzskaitītas iepriekš.

Lai skatītu nomas sagatavošanas posmu datus pirms apstrādes palaišanas, atlasiet **Sagatavošanas posmu dati**.

Salīdzināšanas funkcija ļauj salīdzināt ierakstu, ko importējat, ar atbilstošo ierakstu, kas jau ir jūsu sistēmā. Lai salīdzinātu atsevišķu nomas ierakstu, atlasiet nomu un pēc tam atlasiet **Salīdzināt**. Šī darbība jāveic, lai ģenerētu pārskatu **Atšķirības**, pirms migrējat nomas ierakstus. Salīdzināšanas funkcija salīdzina sagatavošanas posmu datos norādītās vērtības ar to nomu vērtībām, kas pašlaik ir sistēmā.

> [!NOTE]
> Salīdzināšanas funkcionalitāte nedarbojas nomām, kurām ir **pievienošanas ieraksta** procesa tips, jo nav nekā, ko salīdzināt ar šo nomu.
>
> Lai vienlaicīgi salīdzinātu vairākas nomas, dodieties uz **Līdzekļu noma \> Nomas importēšanas struktūra \> Periodisks \> Salīdzināt** un atlasiet **Salīdzināt**.

Katram elementam varat apskatīt atšķirības starp to, kas pašlaik ir sistēmā, un to, kas atrodas sagatavošanas posmos. Katram elementam sagatavošanas tabulās atlasiet opciju **Skatīt atšķirības**. Redzamais dialoglodziņš rāda pašreizējo vērtību un piedāvāto sagatavošanas vērtību.

Varat arī atjaunināt sagatavošanas posma vērtību, mainot to kolonnā **Jauna vērtība** un pēc tam atlasot **Atjaunināt sagatavošanas posmu**.

Jūs varat pārbaudīt nomas, lai nodrošinātu, ka ieraksti var tikt ienesti sistēmā, neieviešot kļūdas. Pirms nomas ieraksts tiek migrēts, sistēma izpilda vairākas pārbaudes, lai nodrošinātu, ka ieraksts tiks sekmīgi importēts. Lai apstiprinātu atsevišķu nomu, atlasiet **Pārbaudīt**.

> [!NOTE]
> Lai vienlaicīgi pārbaudītu vairākas nomas, dodieties uz **Līdzekļu noma \> Nomas importēšanas struktūra \> Periodisks \> Pārbaudīt** un atlasiet **Pārbaudīt**.

Lai apstrādātu atsevišķu nomu, atlasiet **Migrēt nomas ierakstus** lapā **Virsraksta importēšana**. Kad noma tiek migrēta, sistēma veic darbību, kas norādīta laukā **Procesa tips**.

> [!NOTE]
> Lai vienlaicīgi pārbaudītu vairākas nomas, dodieties uz **Līdzekļu noma \> Nomas importēšanas struktūra \> Periodisks \> Pārbaudīt** un atlasiet **Pārbaudīt**.

Pēc tam, kad noma ir salīdzināta, varat palaist pārskatu, lai skatītu atšķirības katrai nomai, kas iekļauta importēšanas ID. Lai palaistu pārskatu vienam nomas līgumam, atlasiet šo nomu sagatavošanas posma datos un pēc tam atlasiet **Salīdzināt un skatīt pārskatu \> Atšķirību pārskats**.

> [!NOTE]
> Lai vienlaicīgi pārbaudītu vairākas nomas, dodieties uz **Līdzekļu noma \> Pieprasījumi un pārskati \> Atšķirību pārskats** un atlasiet **Salīdzināt**.

## <a name="set-up-update-fields"></a>Iestatīt atjaunināšanas laukus

Ja izmantojat nomas importēšanas struktūru, lai atjauninātu nomas, un procesa tips ir **Atjaunināšanas ieraksts**, varat atlasīt konkrētus laukus, kas jāatjaunina.

1. Doties uz **Līdzekļu noma \> Nomas importēšanas struktūra \> Iestatīšana \> Atjaunināt lauku atlasi**.
2. Parādītajā lapā atlasiet atjaunināmos laukus un pēc tam atlasiet zaļo bultiņu, lai pārvietotu tos uz sarakstu **Atlasītie lauki**. Tikai lauki sarakstā **Atlasītie lauki** var tikt atjaunināti, izmantojot nomas importēšanas komplektu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]