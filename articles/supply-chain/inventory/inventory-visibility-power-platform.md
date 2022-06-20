---
title: Krājumu redzamības programma
description: Šajā rakstā ir aprakstīts, kā izmantot krājumu redzamības programmu.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: db158e3b6ae76f69149db04096f99d3dc4251146
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895762"
---
# <a name="use-the-inventory-visibility-app"></a>Inventory Visibility programmas lietošana

[!include [banner](../includes/banner.md)]


Šajā rakstā ir aprakstīts, kā izmantot krājumu redzamības programmu.

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

Izmantojiet cilni **Rezervācijas grāmatošana**, lai grāmatotu rezervēšanas pieprasījumu. Pirms rezervēšanas pieprasījuma grāmatošanas ir jāslēdz funkcija *OnHandReservation*. Papildinformāciju skatiet [Krājumu uztveramības pievienojumprogrammas rezervācijas](inventory-visibility-reservations.md).

Lai grāmatotu rezervēšanas pieprasījumu, pieprasījuma pamattekstā ir jāievada vērtība. Izmantojiet modeli, kas ir aprakstīts sadaļā [Izveidot vienu rezervācijas notikumu](inventory-visibility-api.md#create-one-reservation-event). Pēc tam atlasiet **Grāmatot**. Lai skatītu pieprasījuma atbildes informāciju, atlasiet **Rādīt informāciju**. Atbildes informācijā varat arī iegūt `reservationId` vērtību.

## <a name="inventory-summary"></a><a name="inventory-summary"></a>Krājumu kopsavilkums

**Krājuma kopsavilkums** ir pielāgots skats uz *Inventory OnHand Sum* entitīju. Tajā sniegts krājumu kopsavilkums precēm kopā ar visām dimensijām. Krājumu kopsavilkuma dati periodiski tiek sinhronizēti no krājumu redzamības ik pēc 15 minūtēm. Lai skatītu datus cilnē **Krājumu kopsavilkums**, *cilnē Līdzekļu pārvaldība ir jāiestata funkcija OnHandMostSpecificBackgroundService* **un** jāatlasa **Atjaunināt konfigurāciju**.

> [!NOTE]
> Funkcija *OnHandMostSpecificBackgroundService* izseko tikai rīcībā esošo preču izmaiņas, kas notikušas pēc funkcijas ieslēgtšanas. To preču dati, kuras nav mainītas kopš ieslēgts līdzeklis, netiks sinhronizēti no krājumu pakalpojuma kešatmiņas vidē Dataverse. **Ja** jūsu Krājumu kopsavilkuma lapā nav parādīta visa pieejamā informācija, ko plānojat, **pārejiet uz sadaļu Krājumu pārvaldība > Periodiskie uzdevumi >** Krājumu redzamības integrācija, atspējojiet pakešuzdevumu un ataktivizējiet to. Tas veiks sākotnējo virzību, un visi dati nākamo *15 minūšu laikā tiks sinhronizēti* ar elementu Krājumu rīcībā summa. Ja vēlaties izmantot šo funkciju, **ieteicams to ieslēgt pirms jebkādu rīcībā esošo izmaiņu veikšanas un iespējot pakešuzdevumu Krājumu** redzamība integrācija.

Lietojiet Dataverse sniegto **Detalizēto filtru**, varat izveidot personalizētu skatu, kurā rādītas jums svarīgākās rindas. Papildu filtra opcijas ļauj izveidot plašu skatījumu klāstu no vienkāršiem uz kompleksiem. Tie arī ļauj pievienot filtriem grupētus un ligzdotus nosacījumus. Lai uzzinātu vairāk par **Papildu filtra** lietošanu, skatiet rakstu [Rediģēt vai izveidot personalizētus skatus, izmantojot detalizētā režģa filtrus](/powerapps/user/grid-filters-advanced).

Pielāgotā skata augšpusē redzami trīs lauki: **Noklusējuma dimensija**, **Pielāgotā dimensija** un **Mērījums**. Šos laukus varat izmantot, lai kontrolētu, kuras kolonnas ir redzamas.

Var atlasīt kolonnas virsrakstu, lai filtrētu vai kārtotu pašreizējo rezultātu.

Pielāgotā skata apakšā ir redzama informācija, piemēram, "50 ieraksti (atlasīti 29)" vai "50 ieraksti." Šī informācija attiecas uz ierakstiem, kas pašlaik ielādēti no **Detalizētā filtra** rezultāta. Teksts "atlasīts 29" attiecas uz ierakstu skaitu, kas ir atlasīti, ielādētajiem ierakstiem izmantojot kolonnas virsraksta filtru.

Skatījuma apakšdaļā ir poga **Ielādēt vairāk**, ko varat izmantot, lai ielādētu vairāk Dataverse ierakstu. Noklusējuma ielādēto ierakstu skaits ir 50. Ja atlasāt **Ielādēt vairāk**, nākamajā skatā tiek ielādēti nākamie 1000 pieejamie ieraksti. Skaits pogā **Ielādēt vēl** norāda pašlaik ielādētos ierakstus un kopējo ierakstu skaitu **Detalizētā filtra** rezultātā.

![Krājumu kopsavilkums](media/inventory-visibility-onhand-list.png "Krājumu kopsavilkums")
