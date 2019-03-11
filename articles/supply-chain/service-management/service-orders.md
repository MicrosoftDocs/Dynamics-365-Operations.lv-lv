---
title: Pakalpojumu pasūtījumi
description: Pakalpojuma pasūtījums nozīmē servisa tehniķa vizīti debitora atrašanās vietā noteiktā datumā.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4da0b965f3719bc16b5a73538df111ff6df071be
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "366516"
---
# <a name="service-orders"></a>Pakalpojumu pasūtījumi   

[!include [banner](../includes/banner.md)]


Pakalpojuma pasūtījums nozīmē servisa tehniķa vizīti debitora atrašanās vietā noteiktā datumā. Katrs pakalpojumu pasūtījums sastāv no vienas vai vairākām pakalpojumu pasūtījuma rindām. Pakalpojumu pasūtījumu rindas ataino darba stundas, kas pakalpojumu sniegšanas speciālistam ir jānodrošina, kā arī saistītos krājumus, izdevumus un maksas.

Pakalpojuma pasūtījuma rindai varat pievienot uzdevumus un objektus. Pēc tam pakalpojumu pasūtījumu rindas varat grupēt pēc uzdevuma vai pēc objekta. Pakalpojumu pasūtījumu rindām varat pievienot arī elementus, kas ir uzskaitīti krājumos.

## <a name="create-service-orders"></a>Pakalpojumu pasūtījumu izveidošana

Pakalpojumu pasūtījumus varat izveidot, pamatojoties uz pakalpojumu līgumu un šajā līgumā ietvertajām rindām. Taču ar pakalpojumu līgumu saistītus pakalpojumu pasūtījumus varat izveidot tikai tajā periodā, kas ir norādīts attiecīgajā līgumā. Piemēram, ja pakalpojumu līgums ir derīgs 2011. kalendārajam gadam, pakalpojumu pasūtījumus šim līgumam varat izveidot no 2011. gada 1. janvāra līdz 2011. gada 31. decembrim.

Pakalpojumu pasūtījumus varat izveidot arī atsevišķi, tos nesaistot ar kādu līgumu. Šos pakalpojumu pasūtījumus var izmantot, lai apstrādātu neplānotas vai vienreizējas apkopes vizītes. Piemēram, martā jūsu klients vēlas, lai papildus pakalpojumu līgumā norādītajām iekārtām tiktu veikta apkalpošana vēl divām iekārtām. Šim uzdevumam jūs izveidojat pakalpojumu pasūtījumus, bet tos nesaistāt ar līgumu.


> [!NOTE]
> <P>Lai izveidotu pakalpojumu līgumus, kas nav saistīti ar pakalpojumu līgumu, jums ir jāatzīmē izvēles rūtiņa <STRONG>Atļaut bez pakalpojumu līguma</STRONG> formā <STRONG>Pakalpojumu pārvaldības parametri</STRONG>.</P>

**Scenārijs**

Nākamajā scenārijā ir aprakstīta cita situācija, kur var noderēt ar pakalpojumu līgumu nesaistīta pakalpojumu pasūtījuma izveidošana.

Uzņēmuma dispečers saņem zvanu ar ārkārtas labošanas prasību liftam. Nav laika izveidot pakalpojumu līgumu un pakalpojuma projektu. Tādēļ dispečers izveido pakalpojumu pasūtījumu tieši formā **Pakalpojumu pasūtījumi**, šo pakalpojumu pasūtījumu pievieno jau esošam projektam un izveido pakalpojumu pasūtījuma rindas. Dispečers izveido arī uzdevumu vai objektu relāciju jau esošam pakalpojumu pasūtījumam, lai ierakstītu darbu, kas nav saistīts ar pakalpojumu līgumu. Plašāku informāciju skatiet tēmā [Pakalpojumu līgumu izveidošana manuāli](create-service-orders-manually.md) un [Pakalpojumu uzdevumu relāciju izveidošana](create-service-task-relations.md).

## <a name="monitor-the-progress-of-service-orders"></a>Pakalpojumu pasūtījumu norises uzraudzīšana

Lai uzraudzītu pārdošanas pasūtījumu norisi dažādās darba grupās un darba procesos, pakalpojumu pasūtījumiem varat iestatīt stadiju sistēmu un iemeslu kodus. Katrai stadijai varat norādīt atļautās darbības. Plašāku informāciju skatiet tēmā [Iemeslu kodu izveidošana](create-reason-codes.md).

**Piemērs**

Dispečers apstiprina pakalpojumu pasūtījumu. Dispečers atjaunina pakalpojumu pasūtījuma stadiju un izvēlas iemesla kodu, kurš norāda, ka pakalpojumu pasūtījums ir nodots pakalpojumu sniegšanas speciālistam. Tehniskais speciālists dodas uz klienta telpām un sniedz pakalpojumu.

## <a name="specify-item-requirements-for-service-orders"></a>Krājumu vajadzību norādīšana pakalpojumu pasūtījumiem

Varat norādīt pakalpojumu pasūtījumiem nepieciešamās krājumu vienības. Taču pakalpojumu pasūtījumam ir jābūt saistītam ar kādu projektu. Krājumu vajadzības pakalpojumu pasūtījumiem tiek apstrādātas ar projektu. 

**Piemērs**

Dispečers apstrādā pakalpojumu pasūtījumus, kas ir izveidoti no pakalpojumu līguma. Pirmajam pakalpojumu pasūtījumam dispečers saprot, ka pakalpojumu sniegšanas speciālistam ir nepieciešama svarīga rezerves daļa, kuras nav rīcībā esošajos krājumos. Tādēļ dispečers izveido krājuma vajadzību rezerves daļai tieši no pakalpojumu pasūtījuma.

## <a name="move-and-post-lines"></a>Rindu pārvietošana un grāmatošana

Pakalpojumu sniegšanas speciālists atgriežas no apkopes vizītes un pēc tam modificē un atjaunina pakalpojumu pasūtījuma rindas. Šīs apkopes vizītes laikā tehniskais speciālists veica kādu apkopes darbu, kura veikšana bija ieplānota nākamās apkopes vizītes laikā. Tādēļ tehniskais speciālists pārvieto rindas no nākamās apkopes veikšanas vizītes uz pašreizējo apkopes vizīti. Pēc tam tehniskais speciālists iegrāmato pakalpojumu pasūtījumu. Plašāku informāciju skatiet tēmā [Pakalpojumu pasūtījumu rindu pārvietošana](move-service-order-lines.md).

## <a name="cancel-service-orders"></a>Pakalpojumu pasūtījumu atcelšana

Viens no pārējiem pakalpojumu pasūtījumiem, kas tika izveidoti janvāra mēnesim, kļūst par novecojušu, jo darbs ir atcelts. Tādēļ pakalpojumu dispečers atceļ šo pakalpojumu pasūtījumu. Plašāku informāciju skatiet tēmā [Pakalpojumu pasūtījumu atcelšana](cancel-service-orders.md).

## <a name="post-from-projects"></a>Grāmatošana no projektiem

Katras nedēļas beigās dispečers vēlas iegrāmatot visus pakalpojumu pasūtījumus, kas ir pievienoti noteiktam projektam. Tādēļ dispečers atrod attiecīgo projektu formā **Projekti** un iegrāmato izpildītos pakalpojumu pasūtījumus. Plašāku informāciju skatiet tēmā [Pakalpojumu pasūtījumu grāmatošana (klases forma)](https://technet.microsoft.com/en-us/library/aa574685\(v=ax.60\)).

## <a name="delete-service-orders"></a>Pakalpojumu pasūtījumu dzēšana

Gada otrajā pusē jūsu klients izlemj, ka apkopes vizītes notiek pārāk reti. Jums ir jāizveido jauna, biežāka apkopes vizīšu sērija pakalpojumu līguma atlikušajam periodam. Tādēļ jums ir jāizdzēš esošie pakalpojumu pasūtījumi un jāizveido jauni pakalpojumu pasūtījumi. Plašāku informāciju skatiet tēmā [Pakalpojumu pasūtījumu dzēšana](delete-service-orders.md).

## <a name="see-also"></a>Skatiet arī

[Pakalpojumu pasūtījumi (forma)](https://technet.microsoft.com/en-us/library/aa554361\(v=ax.60\))

  


