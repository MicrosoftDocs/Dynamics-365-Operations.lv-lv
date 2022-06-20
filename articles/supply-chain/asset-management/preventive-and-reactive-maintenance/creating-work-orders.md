---
title: Darba pasūtījumu izveidošana
description: Šajā rakstā skaidrots, kā izveidot darba pasūtījumus Līdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetMaintenancePlan, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePoolsOpen
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: b1b8b3d8d83bdad2efe49bd4e878793cca6c49f4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891210"
---
# <a name="creating-work-orders"></a>Darba pasūtījumu izveidošana

[!include [banner](../../includes/banner.md)]

Kad ir izveidots profilaktisks uzturēšanas darbs, nākamais solis ir darba pasūtījumu izveide darbiem. Šo soli var izpildīt, izmantojot vienu no uzturēšanas grafikiem. Uzturēšanas grafikā ieplānotajiem darbiem var būt dažādi atsauces veidi, kā norādīts nākamajā tabulā.

| Atsauces tips | Apraksts |
|---|---|
| Uzturēšanas plāni | Profilaktiskie uzturēšanas darbi, balstoties uz apkopes plāna veidiem *Laiks* vai *Skaitītājs*. |
| Uzturēšanas cikls | Profilaktiskie uzturēšanas darbi, kas satur vairākus līdzekļus, kam vajadzīga viena veida uzturēšana. |
| Uzturēšanas pieprasījums | Manuāli izveidots pieprasījums par pamatlīdzekļa uzturēšanu vai remontu. Šo pieprasījumu var konvertēt uz darba pasūtījumu. |

## <a name="create-work-orders-based-on-your-maintenance-schedule"></a>Darba pasūtījumu izveide, pamatojoties uz uzturēšanas grafiku

Lai izveidotu darba pasūtījumus, kas ir balstīti uz uzturēšanas grafiku, sekojiet šiem soļiem.

1. Atveriet vienu no šīm lapām atkarībā no tā, kā vēlaties atlasīt grafika krājumus darba pasūtījumiem:

    - Viss uzturēšanas grafiks (**Līdzekļu pārvaldība \> Uzturēšanas grafiks \> Visi uzturēšanas grafiki**)
    - Viss uzturēšanas grafiks (**Līdzekļu pārvaldība \> Uzturēšanas grafiks \> Visi uzturēšanas grafiki**)
    - Viss uzturēšanas grafiks (**Līdzekļu pārvaldība \> Uzturēšanas grafiks \> Visi uzturēšanas grafiki**)

1. Režģī atzīmējiet izvēles rūtiņu katram plānotajam uzturēšanas darbam, kuram vēlaties izveidot darba pasūtījumu. Darbību rūtī atlasiet **Darba pasūtījums**.

    Tiek parādīts dialoglodziņš **Izveidot darba pasūtījumus**. Kopīgais paredzamais stundu skaits atlasītajām rindām tiek parādīts laukā **Uzturēšanas prognozes stundas**.

    ![Darba pasūtījumu dialoglodziņa izveide.](media/18-preventive-maintenance.png)

1. Sadaļā **Parametri** norādiet izveidojamo darba pasūtījumu skaitu. Izvēlieties vienu no šīm opcijām:

    - **Viens darba pasūtījums katrā rindā** – izveidot vienu darba pasūtījumu katrai uzturēšanas grafika rindai.
    - **Viens darba pasūtījums katram** – izveidojiet darba pasūtījumus, kas ir grupēti atbilstoši citu opciju iestatījumiem, kaskļūst pieejami, izvēloties šo opciju.

1. Laukā **Darba pasūtījuma veids** atlasiet darba pasūtījuma veidu, ko izmantot visiem izveidotajiem darba pasūtījumiem.
1. Atlasiet **Labi**, lai izveidotu darba pasūtījumus atbilstoši iestatījumiem.

## <a name="group-work-order-lines-that-are-automatically-created-while-a-maintenance-plan-runs"></a>Grupēt darba pasūtījuma rindas, kas tiek automātiski izveidotas uzturēšanas plāna izpildes laikā

Šī funkcija ļauj definēt noteikumus darba pasūtījumu rindu grupēšanai saskaņā ar vienu darba pasūtījumu, ja sistēma ir iestatīta darba pasūtījumu automātiskai ģenerēšanai, pamatojoties uz uzturēšanas plānu. Iepriekš automātiski izveidotie darba pasūtījumi var ietvert tikai vienu rindu. Tomēr tagad var grupēt darba pasūtījumus pēc, piemēram, pamatlīdzekļa, pamatlīdzekļa tipa vai funkcionālās atrašanās vietas. (Manuāli izveidotos darba pasūtījumus var jau grupēt šādā veidā, kā aprakstīts iepriekšējā šī raksta sadaļā.)

### <a name="enable-grouping-for-automatically-generated-work-orders"></a>Iespējot grupēšanu automātiski ģenerētiem darba pasūtījumiem

Lai varētu izmantot šo līdzekli, tas vispirms ir jāiespējo jūsu sistēmā. Administratori var izmantot [funkciju pārvaldības](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Līdzekļu pārvaldība*
- **Līdzekļa nosaukums:** *Piemērot noteikumus darba pasūtījumu grupēšanai uzturēšanas plāna izpildes laikā*

### <a name="set-up-grouping-for-automatically-generated-work-orders"></a>Iestatīt grupēšanu automātiski ģenerētiem darba pasūtījumiem

Lai iestatītu grupēšanu automātiski ģenerētiem darba pasūtījumiem, rīkojieties šādi.

1. Dodieties uz **Līdzekļu pārvaldība \> Uzstādīšana \> Preventīvā uzturēšana \> Uzturēšanas plāni**.
1. Katram plānam, kur vēlaties izveidot grupētus darba pasūtījumus, rīkojieties šādi:

    1. Sarakstu rūtī atlasiet plānu.
    1. Kopsavilkuma cilnē **Rindas** pārliecinieties, vai katrā rindā ir atzīmēta izvēles rūtiņa **Automātiski izveidot**.

1. Dodieties uz **Līdzekļu pārvaldība \> Periodiskās darbības \> Profilaktiskā uzturēšana \> Ieplānot uzturēšanas plānus**.
1. Dialoglodziņa **Plānot uzturēšanas plānus** sadaļā **Periods** norādiet plāna laika diapazonu (cik tālu uz priekšu meklējiet plānotos uzturēšanas darbus, lai ģenerētu darbu).
1. Iestatiet opciju **Automātiski izveidot darba pasūtījumu no grafika** uz *Jā*.
1. Sadaļā **Apliecinājums** izvēlieties vienu no šīm opcijām:

    - **Viens darba pasūtījums katrā rindā** – izveidot vienu darba pasūtījumu katrai uzturēšanas grafika rindai. (Šī opcija nodrošina to pašu funkcionalitāti, kas ir pieejama, ja ir atspējota funkcija *Piemērot darba pasūtījumu grupēšanas kārtulas, kamēr uzturēšanas plāna līdzeklis*.)
    - **Viens darba pasūtījums katram** – izveidojiet darba pasūtījumus, kas ir grupēti atbilstoši citu opciju iestatījumiem, kaskļūst pieejami, izvēloties šo opciju.

1. Ja vēlaties, lai opcijas tiek lietotas, kad palaižat tikai dažus no jūsu uzturēšanas plāniem, kopsavilkuma cilnē **Iekļaujamie ieraksti** pievienojiet filtrus pēc vajadzības, tāpat kā citiem Microsoft Dynamics 365 Supply Chain Management  pakešuzdevumiem.
1. Kopsavilkuma cilnē **Palaist fonā** iestatiet pakešuzdevumu un plānošanas opcijas pēc vajadzības, tāpat kā citiem Supply Chain Management pakešuzdevumiem.
1. Atlasiet **Labi**, lai palaistu un/vai plānotu atlasītos uzturēšanas plānus.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]