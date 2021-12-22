---
title: Mobilās ierīces lietotāja iestatījumi
description: Šajā tēmā skaidrots, kā pārvaldīt mobilās ierīces lietotāja iestatījumus noliktavas darbiniekiem.
author: Mirzaab
ms.date: 02/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppDeviceBrand,WHSMobileAppUserDisplaySettings
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: mirzaab
ms.search.validFrom: 2021-02-09
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 13c99854224a6d220e73a43636d85ec1951f8149
ms.sourcegitcommit: fd6270dc7f49f93a8155d2b827153b13edb7be8a
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/09/2021
ms.locfileid: "7901876"
---
# <a name="mobile-device-user-settings"></a>Mobilās ierīces lietotāja iestatījumi

[!include [banner](../../includes/banner.md)]

Jaunajā noliktavas pārvaldības mobilajā programmā ir programmai raksturīgo iestatījumu kopa, kas palīdz pielāgot lietotāja pieredzi. Tā kā programmu var lietot dažādu ekrāna izmēru un konfigurāciju (piemēram, planšetdatora, tālruņa vai aizturētas) ierīcēs, varat ērti pārvaldīt šos iestatījumus programmā Microsoft Dynamics 365 Supply Chain Management.

*Mobilās ierīces lietotāja iestatījumu* funkcija ļauj definēt globālos lietotāja iestatījumus, kas tiks izmantoti visās ierīcēs. Varat arī definēt granulētāku lietotāja iestatījumus atsevišķiem ierīces zīmolu, ierīču modeļiem un/vai darbiniekiem. Kad darbinieks pierakstās mobilajā programmā Warehouse Management mobile app, tiek ieneses un tiek lietots viss raksturīgākais iestatījumu profils, kas tiek glabāts Supply Chain Management atbilstošā zīmola, ierīces un/vai lietotāja ID.

Šī funkcija palīdzēs darbiniekiem sākt darbu ātrāk, kad tie sāk izmantot jaunu ierīci. Daži piemēri:

- Administratori var izveidot standarta preferenču kopu, kas darbojas vislabāk ierīcēm no konkrēta ražotāja un/vai noteiktiem ierīču modeļiem. Tāpēc darbinieki var sākt darbu ar jaunu ierīci bez nepieciešamības mainīt iestatījumus.
- Ja jūsu uzņēmumam ir identisku ierīču kopa, kas ir kopīgi starp darbiniekiem, darbinieki redzēs viņu vēlamo iestatījumu katru reizi, kad tas pieteiksies, pat ja tie nekad nav izmantojis noteiktu fizisko ierīci, ko viņi atlasījuši konkrētajā dienā.
- Programmā Supply Chain Management administratori var skatīt un rediģēt visus saglabātos iestatījumus pat atsevišķiem darbiniekiem. Šī iespēja var palīdzēt novērst problēmu vai precīzi iestatīt jaunus līdzekļus.

> [!IMPORTANT]
> *Mobilās ierīces lietotāja iestatījumu* funkcija attiecas tikai uz jauno Warehouse Management mobile programmu. Tas nefunkcionē ar veco noliktavas lietotni.

## <a name="turn-on-the-mobile-device-user-settings-feature"></a>Ieslēgt mobilās ierīces lietotāja iestatījumu līdzekli

Lai varētu izmantot šo līdzekli, tas vispirms ir jāiespējo jūsu sistēmā. Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Noliktavas pārvaldība*
- **Līdzekļa nosaukums:** *Lietotāja iestatījumi, ikonas un darbību nosaukumi jaunajai noliktavas programmai*

## <a name="create-and-manage-user-settings"></a>Izveidot un pārvaldīt lietotāja iestatījumus

Izmantojiet **Mobilās ierīces lietotāja iestatījumu** lapu, lai izveidotu, skatītu un pārvaldītu iestatījumu profilus visos granularitātes līmeņos. Pirmo reizi, kad darbinieks rediģē savus lietotāja iestatījumus jaunā ierīcē, šajā lapā automātiski tiek pievienots jauns profils, ja tas vēl nepastāv. Šis profils pēc tam tiek atjaunināts katru reizi, kad darbinieks veic izmaiņas.

Varat arī definēt granulētāku lietotāja iestatījumus, kas ir piemēroti visiem ierīces zīmolu, ierīču modeļiem un/vai darbiniekiem. Tādā gadījumā varat palielināt granularitāti, atsevišķiem zīmolu, modeļiem un/vai darbiniekiem lietojot precīzākus iestatījumus.

Izpildiet šīs darbības, lai izveidotu un pārvaldītu lietotāju iestatījumus mobilajām ierīcēm.

1. Dodieties uz **Noliktavu pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces lietotāja iestatījumi**.
1. Saraksta rūtī atlasiet esošu lietotāja iestatījumu profilu, lai atvērtu tā ierakstu. Lai izveidotu jaunu profilu, darbību rūtī atlasiet **Jauns**.

    Katrs profils saraksta rūtī ir atzīmēts, lai norādītu zīmolu, modeli un/vai lietotāja ID, uz kuru attiecas profils. Dažiem vai visiem šiem raksturlielumiem vispārīgiem profiliem ir vērtība *Visi*.

1. Jaunā vai atlasītā iestatījumu profila ieraksta virsraksta sadaļā iestatiet šādus laukus:

    - **Ierīces zīmola nosaukums** — atlasiet ierīces zīmola nosaukumu, kas jālieto profilam. Ja profils jālieto visiem zīmolu, atstājiet šo lauku tukšu. Vērtību sarakstā ir ietverti visi jūsu sistēmā definētie zīmoli. Lai iegūtu informāciju par to, kā definēt zīmolu sarakstu, skatiet nākamo sadaļu.
    - **Ierīces modeļa ID** — atlasiet ierīces modeli, kas jālieto profilam. Ja profils jālieto visiem modeļiem, atstājiet šo lauku tukšu. Vērtību sarakstā ir ietverti visi modeļi, kas ir definēti laukā **Ierīces zīmola nosaukums** atlasītajam zīmolam. Lai iegūtu informāciju par to, kā definēt katra zīmola modeļu sarakstu, skatiet nākamo sadaļu.
    - **Lietotāja ID** – atlasiet noliktavas darbinieka lietotāja ID, uz kuru attiecas iestatījuma profils. Ja profils jālieto visiem darbiniekiem, atstājiet šo lauku tukšu.

1. Kopsavilkuma cilnē **Vispārīgi**, iestatiet tālāk minētos laukus:

    - **Pogas pozīcija** – atlasiet, kā pogas jānovieto ierīcē. Elementi programmā tiks pārvietoti tā, lai tie labāk atbilstu darbinieka izvēlei vai gatavībai. Pieejamās opcijas ir *Apakšpusē pa labi (noklusējums)*, *Apakšpusē pa kreisi*, *Augšpusē pa labi* un *Augšpusē pa kreisi*.
    - **Rādīšanas orientācija** — atlasiet parādāmo orientāciju, kas programmā jālieto pēc noklusējuma.
    - **Skenēt ar kameru** — iestatiet šo opciju kā *Jā*, lai lietotu ierīces kameru to ievades lauku skenēšanai, kuros vēlamais ievades režīms ir iestatīts uz *Skenēšana*. Ja jūsu ierīcei ir iebūvēts skeneris, iestatiet šo opciju uz *Nē*, lai skeneri izmantotu.
    - **Rādīt preces fotoattēlu** — atlasiet, vai ir jārāda preces fotoattēli, ja tie ir pieejami izlaistai precei. Papildinformāciju par to, kā pievienot preču attēlus, skatiet sadaļā [Attēla pievienošana precei](../pim/tasks/add-image-product.md).
    - **Displeja krāsas tēma** — atlasiet ierīces krāsu tēmu.
    - **Trokšņu līmenis** — atlasiet drošības līmeni ierīcei. Atlasiet vērtību no 0 (nulle) līdz 10. Vērtība *0* neataino troksni, un vērtība *10* attēlo maksimālo skaņu. Noklusējuma vērtība ir *4*.
    - **Vibrāciju līmenis** — atlasiet ierīces vibrāciju līmenis. Atlasiet vērtību no 0 (nulle) līdz 5. Vērtība *0* neataino troksni, un vērtība *5* attēlo maksimālo vibrāciju līmeni. Noklusējuma vērtība ir *1*.
    - **Teksta skalas procenti** – norādiet teksta lielumu kā standarta lieluma procentus. Ievadiet vērtību no 70 līdz 400. Vērtība *70* attēlo mazāko teksta mērogu, un vērtība *400* attēlo lielāko teksta skalu. Noklusējuma vērtība ir *100*.
    - **Pogas skalas procenti** – norādiet teksta lielumu kā standarta lieluma procentus. Ievadiet vērtību no 50 līdz 200. Vērtība *50* attēlo mazāko pogas mērogu, un vērtība *200* attēlo lielāko pogas skalu. Noklusējuma vērtība ir *100*.

## <a name="create-and-manage-mobile-device-brands"></a>Izveidot un pārvaldīt mobilās ierīces zīmolus

Izmantojiet **Mobilās ierīces zīmolu** lapu, lai skatītu, izveidotu un pārvaldītu ierīces zīmolus un modeļus, ko var izmantot ar iestatījumu profiliem. Mobilā programma automātiski i paņemiet un iesniedz lokālo zīmola nosaukumu un modeļa ID pirmajā reizē, kad darbinieks rediģē savus iestatījumus attiecīgajā ierīcē. Tāpēc lielākā daļa šo ierakstu parasti tiks ģenerēta automātiski. Tomēr varat arī pārvaldīt visus šīs lapas ierakstus. Piemēram, katram zīmolam un modelim varat piešķirt vairāk noderīga apraksta, lai palīdzētu izšķirt līdzīgus vai kriptogrāfiskus modeļu šifrējumus.

Izpildiet šīs darbības, lai izveidotu un pārvaldītu mobilo ierīču zīmolus un modeļus.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces darbības**.
1. Atlasiet mobilās ierīces zīmolu no saraksta kolonnas, lai atvērtu ierakstu. Lai izveidotu jaunu zīmolu, darbību rūtī atlasiet **Jauns**.
1. Jaunā vai atlasītā ierīces zīmola ieraksta virsraksta sadaļā iestatiet šādus laukus:

    - **Ierīces zīmola nosaukums** — ierīces zīmola nosaukums, piemēram, *Microsoft Corporation*.
    - **Apraksts** — varat ievadīt aprakstu, kas palīdzēs atšķirt zīmolu nosaukumus.

1. Kopsavilkuma cilnē **Mobilās ierīces modeļi** ir redzami visi atlasītā ierīces zīmola modeļi. Rīkjoslas pogas var izmantot, lai pievienotu produktus režģim vai noņemtu produktus. Katrai rindai jūs varat iestatīt tālāk norādītos laukus:

    - **Ierīces modeļa ID** — ierīces modeļa ID, piemēram, *Surface Book 2*.
    - **Apraksts** — varat ievadīt aprakstu, kas palīdzēs atšķirt modeļu ID.

## <a name="additional-resources"></a>Papildu resursi

- [Noliktavas pārvaldības mobilās programmas instalēšana un savienošana](install-configure-warehouse-management-app.md)
- [Darbību ikonu un nosaukumu piešķiršana Warehouse Management mobilajai programmai](step-icons-titles.md)