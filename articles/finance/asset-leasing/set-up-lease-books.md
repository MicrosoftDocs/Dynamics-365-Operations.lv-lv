---
title: Nomas grāmatu iestatīšana
description: Šī tēma apraksta informāciju, kas tiek uzturēta nomas grāmatās. Nomas grāmatās ir iekļautas uzskaites politikas, kas nosaka, kā sistēmā tiek uzskaitīta noma.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseBookMaster
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: aafb5913d9aff8b0ac2cfbb8126f4b6d8362c96c
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880940"
---
# <a name="set-up-lease-books"></a>Nomas grāmatu iestatīšana

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Nomas grāmatās ir iekļautas uzskaites politikas, kas nosaka, kā sistēmā tiek uzskaitīta noma. Papildus skaidras naudas pamata uzskaitei līdzekļu noma atbalsta tālāk norādītos standartus.

- Vispārpieņemtie uzskaites principi Amerikas Savienotajās valstīs (US GAAP)
- Uzskaites standartu kodifikācijas tēma 842 (ASC 842)
- ASC 840
- Starptautisko finanšu pārskatu standarts 16 (IFRS 16)
- Starptautiskais uzskaites standarts 17 (IAS 17)

Lai izveidotu nomas grāmatu, izpildiet tālāk aprakstītās darbības.

1. Dodieties uz **Līdzekļu noma \> Iestatījumi \> Nomas grāmatas**.
2. Lai pievienotu grāmatu, atlasiet **Jauns**.
3. Iestatiet tālāk minētos laukus.

    | Vārds, uzvārds                                     | Apraksts |
    |------------------------------------------|-------------|
    | Grāmatošanas līmenis                            | Atlasiet izmantojamo grāmatošanas līmeni. Katra grāmata, kas pievienota nomai, ir iestatīta noteiktam grāmatošanas līmenim. Katram grāmatošanas līmenim ir atšķirīgi grāmatošanas mērķi. |
    | Nomas veids                               | Atlasiet, vai noma ir jāklasificē automātiski, vai arī tā ir jādefinē kā finanšu vai operatīvā noma. |
    | Uzskaites struktūra                     | Atlasiet struktūru, kas ir saistīta ar grāmatu. |
    | Nomas termiņa/lietderīgās lietošanas laika iestatīšana          | Sistēma klasificēs nomu kā finanšu nomu, ja nomas veids ir iestatīts uz **Automātisks** un ja nomas termiņš līdzekļa lietderīgās lietošanas laiks ir lielāks vai vienāds ar šajā laukā ievadīto procentuālo vērtību.  |
    | Pašreizējās vērtības/līdzekļa patiesās vērtības iestatīšana   | Ievadiet veselu skaitli, lai definētu slieksni, kas noteiks nomas tipu. Ja nākotnes minimālo nomas maksājumu pašreizējā vērtība ir lielāka par lietotāja definēto vērtību no grāmatas iestatījuma un grāmatas nomas klasifikācija ir iestatīta uz Automātisks, sistēma klasificēs nomu kā finanšu nomu. |
    | Īstermiņa slieksnis                     | Ievadiet mēnešu skaitu, ko izmantot kā slieksni īstermiņa nomām. Ja nomas termiņš ir mazāks par vai vienāds ar šeit ievadīto mēnešu skaitu, sistēma klasificēs nomu kā īstermiņa nomu, un tiks piemērota atliktā nomas maksa. |
    | Nelielas vērtības slieksnis                      | Ievadiet summu, ko izmantot kā nelielas vērtības nomas robežvērtību. Ja līdzekļa patiesā vērtība ir mazāka par vai vienāda ar šeit ievadīto vērtību, sistēma klasificēs nomu kā nelielas vērtības nomu, un tiks piemērota atliktā nomas maksa. |
    | Maksāt kreditoram                            | Iestatiet šo opciju kā **Jā**, lai atļautu grāmatot nomas maksājumus kā rēķinu kreditora kontā, kas norādīts katrā nomā. Kad nomas maksājums būs grāmatots, tiks kreditēts kreditora konts. Ja šī opcija ir iestatīta uz **Nē**, tā vietā tiks kreditēts konts, kas ir norādīts lapas **Nomas grāmatošanas parametri** grāmatošanas tipam **Nomas maksājums**. |
    | Līzinga līgums                       | Atlasiet konvenciju nomas sākuma datumam:<ul><li><b>Neviens</b> – kā sākuma datumu izmantot nomas sākuma datumu.</li><li><b>Pilns mēnesis</b> – kā sākuma datumu izmanto tā mēneša pirmo dienu, kurā iekrīt nomas sākuma datums.</li></ul><p>Ja atlasāt <b>Neviens</b>, pastāv risks, ka saistību norakstīšanas un līdzekļa nolietojuma grafiki uzkrās un iegrāmatos izdevumus mēneša vidū, nevis imēneša beigās. Atlasot <b>Pilns mēnesis</b>, jūs nodrošināt, ka sistēma sāks uzskaitīt nomu mēneša pirmajā datumā un visa mēneša izdevumi tiks uzkrāti un grāmatoti mēneša pēdējā dienā.</p><p><strong>Piezīme.</strong> Nomas līgumu līdzeklis ir jāieslēdz, izmantojot Līdzekļu pārvaldību. <b>Līdzekļu pārvaldības</b> darbvietā atrodiet un atlasiet līdzekli ar nosaukumu <b>Nomas līgums līdzekļa iznomāšanai</b>, un pēc tam atlasiet <b>Iespējot tūlīt</b>.</p> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
