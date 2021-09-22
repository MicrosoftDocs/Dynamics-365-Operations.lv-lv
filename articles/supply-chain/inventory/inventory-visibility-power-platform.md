---
title: Krājumu redzamības programma
description: Šajā tēmā ir aprakstīts, kā izmantot Krājumu redzamības līdzekļus.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a60fc00642a77d3dc595a6222727637f0d7cd588
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475064"
---
# <a name="use-the-inventory-visibility-app"></a>Inventory Visibility lietojumprogrammas lietošana

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Šajā tēmā ir aprakstīts, kā izmantot Krājumu redzamības līdzekļus.

Krājumu redzamība nodrošina modeļa vadītas programmas vizualizēšanu. Programmā ir trīs lapas: **Konfigurācija**, **Operāciju redzamība** un **Krājumu kopsavilkums**. Tam ir tālāk minētās vērtības:

- Tā nodrošina lietotāja interfeisu (UI) rīcībā esošo konfigurāciju un vieglās rezervēšanas konfigurāciju.
- Tas atbalsta reāllaika rīcībā esošo krājumu vaicājumus par dažādām dimensiju kombinācijām.
- Tas sniedz UI rezervāciju pieprasījumu grāmatošanai.
- Tā sniedz pielāgotu skatu uz rīcībā esošo krājumu precēm ar visām dimensijām.

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms sākat darbu, uzinstalējiet un iestatiet Inventory Visibility pievienojumprogrammu, kā aprakstīts rakstā [Inventory Visibility instalēšana un iestatīšana](inventory-visibility-setup.md).

## <a name="open-the-inventory-visibility-app"></a>Atveriet Inventory Visibility lietojumprogrammu

Lai atvērtu Inventory Visibility lietojumprogrammu, pierakstieties Power Apps vidē un atveriet **Inventory Visibility**.

## <a name="configuration"></a><a name="configuration"></a>Konfigurācija

Pakalpojuma lapa **Konfigurācijas** Inventory Visibility programmā palīdz iestatīt rīcībā esošo konfigurāciju un vieglās rezervācijas konfigurāciju. Pēc lietojumprogrammas pievienošanas noklusējuma konfigurācija ietver Microsoft Dynamics 365 Supply Chain Management (`fno` datu avots) noklusējuma iestatījumu. Varat pārskatīt noklusēto iestatījumu. Turklāt, pamatojoties uzņēmuma prasībās un ārējās sistēmas krājumu grāmatošanas prasībās, varat pārveidot konfigurāciju, lai standartizētu veidu, kādā var vairākās sistēmās grāmatot, organizēt un vaicātas krājumu izmaiņas.

Visu informāciju par to, kā konfigurēt risinājumu, skatiet sadaļā [Inventory Visibility konfigurēšana](inventory-visibility-configuration.md).

## <a name="operational-visibility"></a>Darbības redzamība

Lapa **Darbības redzamība** sniedz reāllaika rīcībā esošo krājumu vaicājuma rezultātus, kas pamatoti uz dažādām dimensiju kombinācijām. Ja ir ieslēgta funkcija *OnHandReservation*, varat arī grāmatot rezervēšanas pieprasījumus no lapas **Operāciju redzamība**.

### <a name="on-hand-query"></a>Rīcībā esošie vaicājumi

Cilnē **Rīcībā esošie vaicājumi** tiek rādīti reāllaika rīcībā esošo krājumu vaicājuma rezultāti.

Atlasot cilni **Rīcībā esošie vaicājumi**, sistēma pieprasa savus akreditācijas datus, lai varētu iegūt uzrādītāja marķieri, kas ir nepieciešams, lai vaicātu par Krājumu redzamības pakalpojumu. Variet tikai ielīmēt uzrādītāja marķieri laukā **BearerToken** un aizvērt dialoglodziņu. Pēc tam varat iegrāmatot rīcībā esošo vaicājumu pieprasījumu.

Ja uzrādītāja marķieris nav derīgs vai arī tā derīgums ir beidzies, pievienojiet jaunu laukā **BearerToken**. Ievadiet pareizo **Klienta ID**, **Nomnieka ID**, **Klienta slepeno informāciju** un pēc tam atlasiet **Atsvaidzināt**. Sistēma automātiski saņems jaunu, derīgu uzrādītāja marķieri.

Lai grāmatotu rīcībā esošo vaicājumu, ievadiet pieprasījuma pamattekstā. Izmantojiet Modeli, kas aprakstīts [Vaicājumā, izmantojot grāmatošanas metodi](inventory-visibility-api.md#query-with-post-method).

![Rīcībā esošie vaicājumu iestatījumi](media/inventory-visibility-query-settings.png "Rīcībā esošie vaicājumu iestatījumi")

### <a name="reservation-posting"></a>Rezervāciju grāmatošana

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Izmantojiet cilni **Rezervācijas grāmatošana**, lai grāmatotu rezervēšanas pieprasījumu. Pirms rezervēšanas pieprasījuma grāmatošanas ir jāslēdz funkcija *OnHandReservation*. Papildinformāciju skatiet [Krājumu uztveramības pievienojumprogrammas rezervācijas](inventory-visibility-reservations.md).

Lai grāmatotu rezervēšanas pieprasījumu, pieprasījuma pamattekstā ir jāievada vērtība. Izmantojiet modeli, kas ir aprakstīts sadaļā [Izveidot vienu rezervācijas notikumu](inventory-visibility-api.md#create-one-reservation-event). Pēc tam atlasiet **Grāmatot**. Lai skatītu pieprasījuma atbildes informāciju, atlasiet **Rādīt informāciju**. Atbildes informācijā varat arī iegūt `reservationId` vērtību.

## <a name="inventory-summary"></a><a name="inventory-summary"></a>Krājumu kopsavilkums

**Krājuma kopsavilkums** ir pielāgots skats uz *Inventory OnHand Sum* entitīju. Tajā sniegts krājumu kopsavilkums precēm kopā ar visām dimensijām. Krājuma kopsavilkuma dati tiks periodiski sinhronizēti no Inventory Visibility. Pirms varat aplūkot datus cilnē **Krājuma kopsavilkums**, ir **Līdzekļu pārvaldības** cilnē ir jāiespējo līdzeklis *OnHandMostSpecificBackgroundService*.

Lietojiet Dataverse sniegto **Detalizēto filtru**, varat izveidot personalizētu skatu, kurā rādītas jums svarīgākās rindas. Papildu filtra opcijas ļauj izveidot plašu skatījumu klāstu no vienkāršiem uz kompleksiem. Tie arī ļauj pievienot filtriem grupētus un ligzdotus nosacījumus. Lai uzzinātu vairāk par **Papildu filtra** lietošanu, skatiet rakstu [Rediģēt vai izveidot personalizētus skatus, izmantojot detalizētā režģa filtrus](/powerapps/user/grid-filters-advanced).

Pielāgotā skata augšpusē redzami trīs lauki: **Noklusējuma dimensija**, **Pielāgotā dimensija** un **Mērījums**. Šos laukus varat izmantot, lai kontrolētu, kuras kolonnas ir redzamas.

Var atlasīt kolonnas virsrakstu, lai filtrētu vai kārtotu pašreizējo rezultātu.

Pielāgotā skata apakšā ir redzama informācija, piemēram, "50 ieraksti (atlasīti 29)" vai "50 ieraksti." Šī informācija attiecas uz ierakstiem, kas pašlaik ielādēti no **Detalizētā filtra** rezultāta. Teksts "atlasīts 29" attiecas uz ierakstu skaitu, kas ir atlasīti, ielādētajiem ierakstiem izmantojot kolonnas virsraksta filtru.

Skatījuma apakšdaļā ir poga **Ielādēt vairāk**, ko varat izmantot, lai ielādētu vairāk Dataverse ierakstu. Noklusējuma ielādēto ierakstu skaits ir 50. Ja atlasāt **Ielādēt vairāk**, nākamajā skatā tiek ielādēti nākamie 1000 pieejamie ieraksti. Skaits pogā **Ielādēt vēl** norāda pašlaik ielādētos ierakstus un kopējo ierakstu skaitu **Detalizētā filtra** rezultātā.

![Krājumu kopsavilkums](media/inventory-visibility-onhand-list.png "Krājumu kopsavilkums")
