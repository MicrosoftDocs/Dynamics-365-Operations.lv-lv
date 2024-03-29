---
title: Klastera izdošanas iestatīšana
description: Šajā rakstā ir aprakstīts, kā iestatīt klastera izdošanu un kā lietot krājuma apstiprinājumu klastera izdošanai.
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
ms.openlocfilehash: 0ec3de073def2ff63af3c04b5696cbcec4f09948
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/15/2022
ms.locfileid: "9014768"
---
# <a name="set-up-cluster-picking"></a>Klastera izdošanas iestatīšana

[!include[banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā iespējot darbiniekus izmantot savas mobilās ierīces izdošanas darbu grupēšanai klasteros, lai viņi var izdot krājumus no vienas atrašanās vietas vairākiem darba pasūtījumiem vienlaicīgi. To dēvē par *klastera izdošanu*.

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

1. Pārejiet uz **sadaļu Noliktavas** > **pārvaldības iestatījuma** > **mobilās ierīces** > **mobilās ierīces izvēlnes vienumi**.
1. Saraksta rūtī atlasiet izvēlnes elementu, kuru vēlaties iestatīt.
1. Darbību rūtī atlasiet Darba **apstiprinājuma iestatījumi**.
1. Veiciet vienu no tālāk šīm darbībām:
    - Ja darba tipam, kuru vēlaties iestatīt **, jau** pastāv rinda, atlasiet to un pēc tam **darbību** rūtī atlasiet Rediģēt.
    - Ja atbilstoša rinda nepastāv, atlasiet Jauns darbību **rūtī** un pēc tam iestatiet darba **veidu** kā atbilstošu veidu.
1. Atzīmējiet **izvēles rūtiņu Preces** apstiprināšana jaunajai vai atlasītajai rindai. Tādējādi darbinieki varēs pārbaudīt katru krājuma vienību, izmantojot mobilo ierīci.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]