---
title: Kravas rindu svara lauki neatbilst kravas svara laukiem
description: Kravas rindu svara lauki neatbilst kravas svara laukiem
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSShipmentDetails_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f71ac7b2777cb77fccdf1a4c72a47c9b406bbd68b2d20c41ddc96028d2ffc348
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756707"
---
# <a name="the-weight-fields-on-load-lines-dont-match-the-weight-fields-on-the-load"></a>Kravas rindu svara lauki neatbilst kravas svara laukiem

Kļūdas kods: WHSLoadWeightOnLinesDoNotMatchLoadWarning

## <a name="symptoms"></a>Simptomi

Sistēma parāda šādu kļūdas ziņojumu:

> Kravas rindu svara lauki neatbilst kravas svara laukiem %1. Palaidiet noliktavas kravas svara konsekvences pārbaudi, lai pārrēķinātu svara laukus.

## <a name="cause"></a>Iemesls

Lauki **Neto svars** un **Taras svars** kravas rindā ir iestatīti uz *0* (nulli). Tomēr svara lauki nav iestatīti uz *0* preces svara mērījumiem. Ja kravas rindā nav iestatīti svara lauki, visas kravas rindā iestatītā daudzuma korekcijas var radīt nepareizu kravas svara aprēķinu. Šī problēma var rasties, ja pēc kravas rindas izveidošanas preces svars ir mainīts.

## <a name="resolution"></a>Novēršana

Pēc noklusējuma, veidojot kravas rindu, tajā tiek ievadīti preces svara lauki. Ja svars ir nulle, to var pārrēķināt, izmantojot funkcionalitāti *Noliktavas kravas konsekvences pārbaude*.

1. Dodieties uz **Sistēmas administrēšana \> Periodiskie uzdevumi \> Datu bāze \> Konsekvences pārbaude**.
1. Izvēles rūtiņā **Konsekvences pārbaude** iestatiet lauku **Modulis** uz *Noliktavas pārvaldība*.
1. Lauku **Pārbaudīt/Labot** iestatiet uz *Labot kļūdu*.
1. Izvēles rūtiņu sarakstā atzīmējiet izvēles rūtiņu **Noliktavas kravas svara konsekvences pārdaude** un pārliecinieties, vai ir iezīmēta tikai rinda šai izvēles rūtiņai.
1. Izvēles rūtiņas saraksta augšpusē atlasiet daudzpunktes pogu (**...**) un pēc tam izvēlnē atlasiet **Dialogs**.
1. Lai norādītu kritērijus, kuriem jāpalaiž konsekvences pārbaude, dialoglodziņā **Noliktavas kravas svara konsekvences pārbaude** iestatiet šādus laukus:

    - **Kravas ID:** norādiet kravas ID. Atstājiet šo tukšu, lai pārbaudītu visus kravas ID.
    - **Krājuma kods:** norādiet krājuma kodu. Atstājiet šo tukšu, lai pārbaudītu visas kravas.
    - **Vienmēr pārrēķināt kravu svaru:** iestatiet šo opciju kā *Jā*.
    - **Atļaut pārrakstīt svaru kravas rindās:** iestatiet šo opciju kā *Jā*.

1. Atlasiet **Labi**, lai aizvērtu dialoglodziņu **Noliktavas noslodzes svara konsekvences pārbaude**.
1. Atlasiet daudzpunktes pogu un pēc tam izvēlnē atlasiet **Izpildīt**.

Svars tiek pārrēķināts, ņemot vērā norādītos kritērijus. Atlasiet saiti **Ziņojuma detaļas**, lai skatītu konsekvences pārbaudes rezultātus.
