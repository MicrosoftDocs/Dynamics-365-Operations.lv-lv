---
title: "Papildināšana"
description: "Šajā tēmā ir aprakstītas papildināšanas stratēģijas, kas ir pieejamas noliktavām, kuras izmanto noliktavas vadībā pieejamo funkcionalitāti."
author: Mirzaab
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSReplenishmentTemplates
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 90043
ms.assetid: 49fa97eb-8e10-49a5-9261-1e393159f178
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 67e361aedf77166e01d9e7a5b9dcb19d08ea26bd
ms.openlocfilehash: 872fbe41ed8137c1e7bec24656d4f132e170ae7f
ms.contentlocale: lv-lv
ms.lasthandoff: 10/05/2017

---

# <a name="replenishment"></a>Papildināšana

[!include[banner](../includes/banner.md)]

Šajā tēmā ir aprakstītas papildināšanas stratēģijas, kas ir pieejamas noliktavām, kuras izmanto noliktavas vadībā pieejamo funkcionalitāti. Informācija šajā tēmā neattiecas uz noliktavu risinājumu, kas ir pieejams modulī Krājumu vadība.

Ir pieejamas tālāk minētās papildināšanas stratēģijas.

- **Kopuma pieprasījuma papildināšana** — šī stratēģija izveido papildināšanas darbu izejošajiem pasūtījumiem vai kravām, ja krājums nav pieejams, kad kopums izveido darbu. Piemēram, papildināšanas darbu var izveidot, ja kopuma apstrādāšanas laikā pārdošanas pasūtījumā pieprasītais daudzums nav pieejams.
- **Minimālā/maksimālā papildināšana** — šī stratēģija izmanto minimālos un maksimālos dimensiju ierobežojumus, lai noteiktu novietojumu papildināšanas laiku. Krājumu un novietojumu kritērijus nosaka krājumi, kas tiek novērtēti attiecībā uz papildināšanu. Minimālās/maksimālās papildināšanas veidnes ir galvenais mehānisms optimālu līmeņu uzturēšanai izdošanas vietās. Lai palīdzētu garantēt, ka ir kopuma pieprasījumam atbilstošs daudzums izdošanai pieejamo krājumu, papildus minimālās/maksimālās papildināšanas cikliem varat izmantot pieprasījuma papildināšanu.
- **Kravas pieprasījuma papildināšana** — šī stratēģija summē pieprasījumu pēc vairākām kravām un izveido papildināšanas darbu, kas ir nepieciešams, lai būtu pietiekami daudz krājumu attiecīgajās izdošanas vietās. Šī stratēģija palīdz garantēt, ka izveidotās kravas var izdot noliktavā pēc to izlaišanas.
- **Tūlītēja papildināšana** — šī stratēģija krājumus papildina, pirms tiek izpildīts kopums, ja notiek nesekmīgs sadalījums kādai novietojuma direktīvas rindai, kurai ir papildinājuma veidne. 

Visas četras stratēģijas izveido papildināšanas darbu, pamatojoties uz kādu papildināšanas veidni.

## <a name="wave-demand-replenishment"></a>Kopuma pieprasījuma papildināšana
Kopuma pieprasījuma papildināšana izveido papildināšanas darbu, pamatojoties uz pieprasījumu, ja ražošanas pasūtījumiem, Kaban, izejošajiem pasūtījumiem vai kravām nepieciešamais daudzums nav pieejams laikā, kad kopums izveido darbu. Papildināšanas veidne satur informāciju par krājumu kritērijiem, mērvienību, pieprasījuma pieaugumu un novietojumu. 

Novietojuma direktīvās tiek izmantotas, lai noteiktu, kuri novietojumi ir jāpapildina. Šīs novietojuma direktīvas jūs saistāt ar papildināšanas veidni, izmantojot lauku **Direktīvas kods**. Ja lauks **Direktīvas kods** nav iestatīts, tiek izmantoti vaicājumi, lai noteiktu, kura novietojuma direktīva ir jāizmanto. Ņemiet vērā — ja direktīvas kods nav norādīts papildināšanas veidnē, bet novietojuma direktīvai ir direktīvas kods, tad novietojuma direktīva tiks ignorēta, pat ja vaicājums uz šo noliktavas direktīvu ir pareizs. Izdošanas novietojuma direktīvas tiek izmantotas, lai noteiktu, kur iegūt krājumus papildināšanai. 

Papildus veidnes izveidošanai jums kopuma veidnē ir jānorāda arī kādi papildināšanas iestatījumi. Kopuma veidnei ir jāietver kopuma darbība papildināšanai, kas tiek izpildīta tikai tad, ja krājumam nav sekmīgi izpildīts sadalījums. Šajā papildināšanas kopuma darbībā tiek izmantots kopuma darbības kods, lai noteiktu, kura papildināšanas veidne ir jāizmanto. Papildus papildināšanai paredzētajai kopuma darbībai jums ir jānodrošina, lai kopuma veidnes sadaļā **Metodes** būtu atlasīta vērtība **Papildināt**. 

Lapā **Papildināšanas veidne** ir ietverta izvēles rūtiņa **Atļaut kopuma pieprasījumā izmantot nerezervētos daudzumus**. Atzīmējiet šo izvēles rūtiņu, ja pieprasījuma papildināšana ir nepieciešama spēja atskaitīt nerezervētos daudzumus no darba, kas ir ģenerēts no atlasītās papildināšanas veidnes. Lai pieprasījuma papildināšanas veidnēm ļautu lietot šo loģiku, šī izvēles rūtiņa jums ir jāatzīmē katrai esošajai papildināšanas veidnei. Kad noliktavā tiek aktivizēta pieprasījuma papildināšana, tā pieprasījumu atskaita no esoša papildināšanas darba, kuram ir nerezervēts daudzums, ja darbs tiek ģenerēts no papildināšanas veidnēm, kurām ir atzīmēta izvēles rūtiņa **Atļaut kopuma pieprasījumam lietot nerezervēto daudzumu**.

Pieprasījuma papildināšana tiek atbalstīta pārdošanas pasūtījumiem, pārsūtīšanas pasūtījumiem, ražošanas pasūtījumiem un Kanban. 

## <a name="minmax-replenishment"></a>Minimālā/maksimālā papildināšana
Minimālajā/maksimālajā papildināšanā krājumi tiek papildināti tā, lai to daudzums būtu starp iestatīto minimālo un maksimālo ierobežojumu. Parasti šis process notiek vienu reizi katru dienu, lai palīdzētu garantēt, ka visi izdošanas novietojumi ir piepildīti līdz maksimālajam līmenim, pirms sākas izdošana. 

Minimālās un maksimālās summas tiek iestatītas papildināšanas veidnē. Daudzi citi iestatījumi šajā veidnē līdzināties iestatījumiem veidnēs, kas tiek izmantotas kopuma pieprasījuma papildināšanai. Šajā veidnē ir jābūt vienai rindai katram krājumam un novietojumam. Kad papildināšanu izpildāt, izmantojot pakešuzdevumu, Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition izvērtē, vai ir nepieciešama papildināšana, izmantojot secību, kādā ir sakārtotas rindas. 

Ņemiet vērā, ka minimālās/maksimālās papildināšanas stratēģija nevar papildināt tukšu novietojumu, izņemot gadījumus, kad šis novietojums ir iestatīts kā krājuma fiksētais novietojums. Ja papildināmais novietojums nav fiksētais novietojums, tad sistēma nevar noteikt, kuri krājumi ir jāpapildina. Tādēļ pirms papildināšanas ir nepieciešams vismaz kaut kāds rīcībā esošais daudzums.

## <a name="load-demand-replenishment"></a>Kravas pieprasījuma papildināšana
Kravas pieprasījuma papildināšana summē pieprasījumu pēc vairākām kravām un izveido papildināšanas darbu, kas ir nepieciešams, lai būtu pietiekami daudz krājumu attiecīgajās izdošanas vietās. Kravas pieprasījuma papildināšana daudzējādi līdzinās kopuma pieprasījuma papildināšanai. Galvenā atšķirība ir veidā un laikā, kad tiek palaista kravas pieprasījuma papildināšana un kopuma pieprasījuma papildināšana. Tāpat kā minimālā/maksimālā papildināšana, arī kravas pieprasījuma papildināšana tiek palaista, izmantojot pakešuzdevumu. Lai iestatītu šo pakešuzdevumu, lapā **Kravas pieprasījuma papildināšana** atlasiet izmantojamo papildināšanas veidni un iestatiet filtra vaicājumu, lai norādītu, kuras kravas tiek izmantotas pieprasījuma noteikšanai. Novietojuma vaicājums definē novietojumus, no kuriem tiks atņemts viss pieejamais daudzums, lai atbilstu apkopotajam kravu pieprasījumam.

## <a name="immediate-replenishment"></a>Tūlītēja papildināšana
Tā vietā, lai pieprasījumu vajadzētu saskaitīt sadalījuma procesa beigās un papildināšanu vajadzētu veikt, pamatojoties uz saskaitīto daudzumu, varat lietot stratēģiju Tūlītēja papildināšana. Kad izmantojat šo stratēģiju, krājumus var papildināt uzreiz pēc tam, kad neizdodas izpildīt novietojuma direktīvas rindu. Tāpēc papildināšanu varat iestatīt tā, lai tā būtu ierobežota ar noteiktām vienībām un lai tā izmantotu daudzumus, kas ir iestatīti konkrētiem novietojumiem.

## <a name="replenishment-prerequisites"></a>Papildināšanas priekšnoteikumi
| Priekšnoteikumi            | Apraksts |
|-------------------------|-------------|
| Krājums                    | Krājumam jābūt iespējotam noliktavas pārvaldības procesiem. |
| Noliktava               | Noliktavai jābūt iespējotai noliktavas pārvaldības procesiem. Lai noliktavu aktivizētu noliktavas vadības procesiem, lapā **Noliktavas** atlasiet šo noliktavu un pēc tam atzīmējiet opciju **Izmantot noliktavas pārvaldības procesus**. |
| Papildināšanas veidnes | Ir jāiestata vismaz viena papildināšanas veidne minimālajai/maksimālajai papildināšanai, kopuma pieprasījuma papildināšanai vai kravas pieprasījuma papildināšanai. |
| Novietojumi               | Novietojumiem ir jābūt izveidotiem un savienotiem ar novietojuma profilu. |
| Atrašanās vietu profili       | Novietojumu profili ir nepieciešami, lai izveidotu novietojumus. |
| Novietojuma direktīvas     | Novietojuma direktīvas ir nepieciešamas, lai vadītu darbu uz novietojumiem, kur ir nepieciešama papildināšana, un uz novietojumiem, no kuriem tiek iegūti krājumi. |
| Darbu veidnes          | Darba veidnes ar tipu **Papildināšana** ir nepieciešamas, lai izveidotu papildināšanas darbu un krājumus varētu pārvietot uz vēlamajiem novietojumiem. |

