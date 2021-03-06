---
title: Klastera izdošanas iestatīšana
description: Šajā tēmā ir aprakstīts, kā iestatīt klastera izdošanu un kā piemērot krājumu apstiprinājumu ar klastera izdošanu.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSClusterProfile, WHSRFAutoConfirm, WHSWorkCluster
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 481db453656097de8eeb93c89306509493cce3c3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831198"
---
# <a name="set-up-cluster-picking"></a>Klastera izdošanas iestatīšana

[!include[banner](../includes/banner.md)]

Šajā tēmā aprakstīts, kā darbiniekiem nodrošināt iespēju izmantot mobilās ierīces izdošanas darbu grupēšanai klasteros, lai krājumus varētu izdot no vienas atrašanās vietas vienlaikus vairākiem darba pasūtījumiem. To dēvē par *klastera izdošanu*.

## <a name="about-cluster-picking"></a>Par klastera izdošanu

Kad darba pasūtījumi ir nodoti nosūtīšanai uz noliktavu, darbinieks var izmantot mobilo ierīci, lai pasūtījumus piešķirtu klasterim. Klasterī darbiniekam tiks organizēts izdošanas darbs. Kad darba pasūtījums ir piešķirts klasterim, darbiniekam jāizmanto klastera izdošana, lai izpildītu pasūtījuma izdošanas darbu. Darbinieks nevar izmantot citas izdošanas metodes. Ja darba pasūtījums tiek piešķirts klasterim kļūdas dēļ, darbiniekam klasteris ir jāsadala un pēc tam tas no jauna jāizveido.

Ja nepieciešams, darbinieks var nodot klasteri citam darbiniekam. Tādējādi klastera statuss tiek mainīts uz Nodots. Kad nodarbinātais izmanto mobilo ierīci, lai norādītu, ka izdošanas un izvietošanas darbs ir pabeigts, sūtījums vai krava ir jāapstiprina klientā.

## <a name="enable-cluster-picking"></a>Klastera izdošanas iespējošana

Lai iespējotu klastera izdošanu, jāveic tālāk norādītie iestatījumi:

- **Klastera profili** – norādiet, vai automātiski ģenerēt klastera ID, izmantojamo pozīciju skaitu, kad klasterus sadalīt, kā izveidot izdošanas darba secību un kā šo darbu pārbaudīt.

- **Darbu veidnes** — definējiet, kā izveidot izdošanas darbu klastera izdošanai.

- **Novietojuma direktīvas** — norādiet, no kurienes saņemt krājumus un kur tos novietot.

- **Mobilās ierīces izvēlnes vienumi** — konfigurējiet mobilās ierīces izvēlnes vienumu, lai izmantotu esošu darbu, ko novirzījusi klastera izdošana. Pēc tam izvēlnes vienums jāpievieno mobilās ierīces izvēlnei, lai tas tiktu parādīts mobilajās ierīcēs.

- **Noliktavas vadības parametri** — norādiet izmantojamo numuru sēriju, ja vēlaties klasteriem ģenerēt identifikatorus.

## <a name="set-up-a-cluster-profile"></a>Klastera profila iestatīšana

Lai iestatītu klastera profilu, veiciet tālāk aprakstītās darbības.

1. Noklikšķiniet uz **Noliktavas vadība** \> **Iestatīšana** \> **Mobilā ierīce** \>  **Klastera profili**.

1. Noklikšķiniet uz **Jauns**, lai izveidotu jaunu profilu.

1. Noklikšķiniet uz **Izveidot klasteri** un sadaļā **Klastera kārtošana** noklikšķiniet uz **Jauns**, lai klasterim iestatītu kārtošanas kritērijus. Kārtošanas kritēriji kontrolē kārtību, kādā darbinieks veiks izdošanas darbu. Varat pievienot tik daudz kritērijus, cik nepieciešams.

1. Laukā **Sērijas numurs** ievadiet numuru, lai definētu kārtību, kādā tiek apstrādāti kārtošanas kritēriji.

1. Laukā **Lauka nosaukums** atlasiet lauku, kas noteiks kārtošanu. Piemēram, atlasot lauku **WMSLocationId**, darbs tiks kārtots pēc atrašanās vietas.

1. Laukā **Kārtošana** atlasiet vienu no tālāk norādītajām opcijām.

| **Opcija**     | **Apraksts**                                                                                                                                                                                                                    |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Pieaugošā secībā**  | Izdošanas darbs tiek kārtots augošā secībā, pamatojoties uz kārtošanas kritērijiem. Piemēram, ja kā kārtošanas kritērijus izmantojat lauku **WMSLocationId** un vietas ID ir 1, 2, 3 un 4, izdošana vispirms notiks no 4. atrašanās vietas. |
| **Dilstošā kārtībā** | Izdošanas darbs tiek kārtots dilstošā secībā, pamatojoties uz kārtošanas kritērijiem. Piemēram, ja kā kārtošanas kritērijus izmantojat lauku **WMSLocationId** un vietas ID ir 1, 2, 3 un 4, izdošana vispirms notiks no 1. atrašanās vietas. |

## <a name="item-confirmation"></a>Krājuma apstiprināšana

Ja tiek lietota klasteru izdošana, ir svarīgi veikt krājumu apstiprināšanu, lai pārbaudītu klasteriem pievienotos krājumus. Varat pārbaudīt klastera izdošanā ietvertos krājumus klastera izdošanas procesa laikā. Iestatīšana tiek veikta, pamatojoties uz preču svītrkodu iestatījumiem.

### <a name="set-up-item-verification-with-cluster-picking"></a>Krājumu pārbaudes klastera izdošanai iestatīšana

1. Mobilās ierīces izvēlnes vienumā atveriet iestatīšanas formu darba apstiprināšanai:  **Noliktavas pārvaldība** \> **Noliktavas pārvaldība** \> **Iestatījumi** \>  **Mobilā ierīce** \> **Mobilās ierīces izvēlnes vienumi**.

1. Mobilās ierīces izvēlnes vienumā atveriet sadaļu **Darba apstiprinājuma iestatīšana**. Opcija **Preces apstiprināšana** jums ļauj skenēšanas laikā mobilajā ierīcē pārbaudīt katru krājumu vienību.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]