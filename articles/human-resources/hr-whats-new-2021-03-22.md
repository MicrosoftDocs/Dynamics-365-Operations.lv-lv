---
title: Jaunumi un izmaiņas programmā Dynamics 365 Human Resources 2021. gada 22. martā
description: Šajā tēmā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources uz 2021. gada 22. martu.
author: marcelbf
ms.date: 03/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-03-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 609b70fb2dfa3f3b2a1746392984108d7ac195c4
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019278"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-22-2021"></a>Jaunumi un izmaiņas programmā Dynamics 365 Human Resources 2021. gada 22. martā

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā sadaļā ir aprakstīti līdzekļi, kas ir jauni, mainīti vai drīzumā gaidāmi programmā Dynamics 365 Human Resources.

Papildinformāciju par mūsu atjaunināšanas procesu un grafiku skatiet sadaļā [Atjaunināšanas process](hr-admin-setup-update-process.md).

Papildinformāciju par jaunajiem līdzekļiem un to paredzētajiem vispārējās pieejamības datumiem skatiet sadaļā [Pakalpojuma Dynamics 365 Human Resources 2021 laidiena 1. kopuma pārskats](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šajā laidienā

Šajā laidienā ietilpst tālāk minētie jaunie līdzekļi un kļūdu labojumi. Izmaiņas attiecas uz būvējuma numuru 8.1.4049.

### <a name="new-features"></a>Jauni līdzekļi

Zemāk minētie līdzekļi parasti ir pieejami ar šo laidienu.

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
| --- | --- | --- |
| Iespēja uzspiest iestrēgušu pakešuzdevumu atcelšanu un atiestatīšanu (560976) | NA | [Atiestatīt iestrēgušus pakešuzdevumus](./hr-admin-troubleshooting-batch-execution.md) |
| Nelieli UX atjauninājumi jauna priekšrocību plāna izveidei (419941) | NA | [Atvieglojumu plāna izveide](hr-benefits-plans-setup.md) |

### <a name="bug-fixes"></a>Kļūdu labojumi

Šajā laidienā ir iekļauti tālāk minētie kļūdu labojumi.

> [!NOTE]
> Mūsu mērķis ir nodot jums šo informāciju pēc iespējas ātrāk. Mēs varam atjaunināt šo tēmu, lai iekļautu kļūdu labojumus, kas padarīja to par būvējumu pēc šīs tēmas sākotnējās publicēšanas.

| Problēmas numurs | Izsniegt |  Apraksts |
| --- | --- | --- |
| 554239 | Veiktspējas uzlabojumi entītijām, kas saistītas ar **BusinessProcessTaskAssignment** tabulu | Uzlabojiet ar **BusinessProcessTaskAssignment** tabulu saistīto entītiju veiktspēju, pievienojot tabulai ieteiktos indeksus. |
| 566061 | V2 elementa rezerves koda noņemšana no nakts sinhronizācijas | Noņemiet V2 rezerves kodu, lai sinhronizētu Dataverse katru nakti. Rezerves vairs nav nepieciešamas un neļauj filtrētai sinhronizācijai darboties, kā paredzēts. Izmaiņas uzlabo Dataverse datu sinhronizācijas konsekvenci. |
| 538024 | Darbinieku atvieglojumu plāni > Noņemt izrakstīšanās mešanas kļūdu | Novērsta kļūda, noņemot izrakstīšanās atvieglojumu plāna opcijai veidlap Nodarbinātā atvieglojumi. |
| 557965 | **Priekšrocības** darbvieta: saitei **Aktīvie dzīves notikumi** vienmēr jābūt redzamai **Saites** sadaļā | Novērsta problēma, kuras dēļ sadaļā **Saites** bija redzama **Aktīvie dzīves notikumi** saite, bet radās kļūda, mēģinot naviģēt, ja nav iespējots **(Priekšskatījuma) Atvieglojumu pārvaldības darbvietas** līdzeklis. Papildinformāciju par darbvietas iespējošanu skatiet [darbvietā Priekšrocību pārvaldība](hr-benefits-management-workspace.md). |
| 556672 | Nevar apstrādāt pārtrauktā darbinieka uzkrājumus, ja **Racionalizēta darbinieka ievadne** ir iespējots līdzekļu pārvaldībā | Iespēja uzkrāt atvaļinājuma un prombūtnes plānus ir pievienota **Papildu opcijas** sadaļā **Darba vēsture** darbiniekiem, ja līdzekļu pārvaldībā ir iespējots **Racionalizēts darbinieka ieraksts**. |
| 562656 | **SysRecordChangeLogValidTimeState** izvēlnes elements jāiekļauj drošības privilēģijā un drošības pienākuma **SystemExternalBasicMaintain** paplašinājumā | Ārpussistēmas administratora lomām datumu pārvaldnieka veidlapās trūka pogas **Skatīt izmaiņas**. |
| 505989 | Dzīves notikumu apstrāde: Nepareizi apstrādātas piemērotības izmaiņas sakarā ar izmantoto datumu | Fiksēta izejas plūsma, kur izmaiņas atbilstības apstrādē bija atkarīgas no amata sākuma datuma, nevis tikai no pašreizējās pozīcijas. |
| 562286 | Darbinieks, kas pārtrauc darba attiecības, nosūta vairākus atjauninājumus Dataverse | Kad darbinieks pārtrauc darba attiecības, uz Dataverse tiek nosūtītas vairākas atjaunināšanas operācijas, kā rezultātā rodas divi atjaunināšanas paziņojumi par vienām un tām pašām izmaiņām. Tas var izraisīt vairākus trigerus, ja Power Automate plūsma ir konfigurēta, lai izraisītu darbību. |
| 527340 | Kļūda "Nepārstāvams DatumsLaiks" tiek parādīta, atverot atvaļinājuma un kavējumu reģistrācijas | Atlasot atvaļinājuma un kavējumu reģistrāciju, kļūda vairs netiek rādīta. |
| 561663 | Klastera nodrošinājuma gaidīšanas laika intervāla palielināšana | Uzlabot infrastruktūras stabilitāti un nodrošināt konsekvenci ar klasteru nodrošinājuma atjauninājumiem. |
| 486129 | Nevar rediģēt pielāgotus laukus **Pozīcijas > Pārvaldīt izmaiņas** | Novērsta problēma, kuras dēļ pielāgotus laukus nevarēja rediģēt **Pozīciju** cilnē **Izmaiņu pārvaldība**. |

## <a name="in-preview"></a>Priekšskatījumā

Tālāk norādītie jaunie līdzekļi ir priekšskatījumā. Papildinformāciju par līdzekļu ieslēgšanu vai izslēgšanu skatiet sadaļā [Līdzekļu pārvaldība](hr-admin-manage-features.md).

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
| --- | --- | --- |
| Atvieglojumu pārvaldības darbvieta | [Atvieglojumu pārvaldības darbvieta (Priekšskatījums)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Atvieglojumu pārvaldības darbvieta](hr-benefits-management-workspace.md) |
| Ierobežot darbiniekus rediģēt uzņēmuma kontaktinformāciju | [Ierobežot darbiniekus rediģēt uzņēmuma kontaktinformāciju](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [Ierobežot personiskās informācijas rediģēšanu](hr-employee-self-service-restrict-editing.md)|

## <a name="coming-soon"></a>Drīzumā

| Funkcija | Detaļas |
| --- | --- |
| Vadītāja ievadītās prasmes saviem darbiniekiem var automātiski apstiprināt ar darbplūsmu | Drīzumā. |

Pilnīgu sarakstu ar plānotajiem līdzekļiem un to ieplānotajiem laidieniem skatiet sadaļā [Pakalpojuma Dynamics 365 Human Resources 2021 laidiena 1. kopuma pārskats](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Skatiet arī

[Jaunumi un izmaiņas programmā Human Resources](hr-admin-whats-new.md)</br>
[Pārskats par Dynamics 365 Human Resources 2021. gada laidiena 1. kopumu](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Procesa atjaunināšana](hr-admin-setup-update-process.md)</br>
[Līdzekļu pārvaldība](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]