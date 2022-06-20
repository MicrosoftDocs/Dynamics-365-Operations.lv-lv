---
title: Nomu pārvaldība, izmantojot nomas importēšanas struktūru
description: Šajā rakstā ir izskaidrots, kā izmantot nomas importa struktūru, lai vienlaikus pielāgotu vairākas nomas.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseLeaseImportHeader
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 8cf81ccf61e62ac49e6cb90d13ca5fe50147cc76
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894969"
---
# <a name="manage-leases-through-the-lease-import-framework"></a>Nomu pārvaldība, izmantojot nomas importēšanas struktūru

[!include [banner](../includes/banner.md)]

Šajā rakstā ir izskaidrots, kā izmantot nomas importēšanas struktūru, lai vienā solī koriģētu vairākas nomas. Izmantojot šo iespēju, varat ietaupīt laiku un varat arī nodrošināt precīzākas korekcijas, samazinot cilvēka kļūdas iespējamību. Turklāt šī iespēja var savienot Microsoft Dynamics 365 finanses ar ārējiem datu elementiem, lai efektīvi augšupielādētu datus.

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

Pēc informācijas augšupielādes, izmantojot **Datu pārvaldības** darbvietu, atveriet **Virsraksta importēšanas** lapu (**Līdzekļa noma \> Nomas importēšanas struktūra \> Virsraksta importēšana**). Šajā lapā uzskaitītas visas trīs datu entītijas, kas tika uzskaitītas iepriekš.

Lai skatītu nomas sagatavošanas posmu datus pirms apstrādes palaišanas, atlasiet **Sagatavošanas posmu dati**.

Salīdzināšanas funkcija ļauj salīdzināt ierakstu, ko importējat, ar atbilstošo ierakstu, kas jau ir jūsu sistēmā. Lai salīdzinātu atsevišķu nomas ierakstu, atlasiet nomu un pēc tam atlasiet **Salīdzināt**. Šī darbība jāveic, lai ģenerētu pārskatu **Atšķirības**, pirms migrējat nomas ierakstus. Salīdzināšanas funkcija salīdzina sagatavošanas posmu datos norādītās vērtības ar to nomu vērtībām, kas pašlaik ir sistēmā.

> [!NOTE]
> Salīdzināšanas funkcionalitāte nedarbojas nomām, kurām ir **Pievienot ieraksutu** procesa tips, jo nav nekā, ko salīdzināt ar šo nomu.
>
> Lai vienlaicīgi salīdzinātu vairākas nomas, dodieties uz **Līdzekļu noma \> Nomas importēšanas struktūra \> Periodisks** un atlasiet **Salīdzināt**.

Katram elementam varat apskatīt atšķirības starp to, kas pašlaik ir sistēmā, un to, kas atrodas sagatavošanas posmos. Katram elementam sagatavošanas tabulās atlasiet opciju **Skatīt atšķirības**. Redzamais dialoglodziņš rāda pašreizējo vērtību un piedāvāto sagatavošanas vērtību.

Varat arī atjaunināt sagatavošanas posma vērtību, mainot to kolonnā **Jauna vērtība** un pēc tam atlasot **Atjaunināt sagatavošanas posmu**.

Jūs varat pārbaudīt nomas, lai nodrošinātu, ka ieraksti var tikt ienesti sistēmā, neieviešot kļūdas. Pirms nomas ieraksts tiek migrēts, sistēma izpilda vairākas pārbaudes, lai nodrošinātu, ka ieraksts tiks sekmīgi importēts. Lai apstiprinātu atsevišķu nomu, atlasiet **Pārbaudīt**.

> [!NOTE]
> Lai vienlaicīgi pārbaudītu vairākas nomas, dodieties uz **Līdzekļu noma \> Nomas importēšanas struktūra \> Periodisks** un atlasiet **Pārbaudīt**.

Lai apstrādātu atsevišķu nomu, atlasiet **Migrēt nomas ierakstus** lapā **Virsraksta importēšana**. Kad noma tiek migrēta, sistēma veic darbību, kas norādīta laukā **Procesa tips**.

> [!NOTE]
> Lai vienlaicīgi migrētu vairākas nomas, dodieties uz **Līdzekļu noma \> Nomas importēšanas struktūra \> Periodisks** un atlasiet **Migrēt**.

Pēc tam, kad noma ir salīdzināta, varat palaist pārskatu, lai skatītu atšķirības katrai nomai, kas iekļauta importēšanas ID. Lai palaistu pārskatu vienam nomas līgumam, atlasiet šo nomu sagatavošanas posma datos un pēc tam atlasiet **Salīdzināt un skatīt pārskatu \> Atšķirību pārskats**.

> [!NOTE]
> Lai vienlaicīgi salīdzinātu vairākas nomas, dodieties uz **Līdzekļu noma \> Nomas importēšanas struktūra \> Periodisks** un atlasiet **Salīdzināt**. 

## <a name="set-up-update-fields"></a>Iestatīt atjaunināšanas laukus

Ja izmantojat nomas importēšanas struktūru, lai atjauninātu nomas, un procesa tips ir **Atjaunināšanas ieraksts**, varat atlasīt konkrētus laukus, kas jāatjaunina.

1. Doties uz **Līdzekļu noma \> Nomas importēšanas struktūra \> Iestatīšana \> Atjaunināt lauku atlasi**.
2. Parādītajā lapā atlasiet atjaunināmos laukus un pēc tam atlasiet zaļo bultiņu, lai pārvietotu tos uz sarakstu **Atlasītie lauki**. Tikai lauki sarakstā **Atlasītie lauki** var tikt atjaunināti, izmantojot nomas importēšanas komplektu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
