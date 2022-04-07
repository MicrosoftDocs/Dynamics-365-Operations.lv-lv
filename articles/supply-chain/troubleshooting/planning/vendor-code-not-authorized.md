---
title: Piegādātāja kods nav autorizēts noteiktai precei un datumam
description: Mēģinot apstiprināt plānoto pasūtījumu vai pievienot rindu pirkšanas pasūtījumam, tiek parādīts kļūdas ziņojums, kurā norādīts, ka kreditora kods nav autorizēts precei un datumam.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO_ReqTransPoMarkFirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 917526dfcefb36ce6e59af6f1f5bebc23ee6e53f
ms.sourcegitcommit: ab690bc897699ff8a4c489e749251fe0367050ca
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/26/2022
ms.locfileid: "8489061"
---
# <a name="vendor-code-isnt-authorized-for-a-specific-product-and-date"></a>Piegādātāja kods nav autorizēts noteiktai precei un datumam

Kļūdas kods: SYP4881415

## <a name="symptoms"></a>Simptomi

Mēģinot apstiprināt plānoto pasūtījumu vai pievienot rindu pirkšanas pasūtījumam saņemsit šādu kļūdas ziņojumu:

> Kreditora kods %1 nav autorizēts lietošanai vienumā %2 šeit: %3.

## <a name="cause"></a>Iemesls

Kļūda rodas, jo norādītajai precei lauks **Apstiprināts piegādātāja pārbaudes metode** ir iestatīts uz *Tikai brīdinājums* vai *Nav atļauts* un kreditors pašlaik nav autorizēts piegādāt šo preci.

## <a name="resolution"></a>Novēršana

Lai novērstu šo problēmu, deaktivizējiet kreditora pārbaudi atbilstošai precei vai apstipriniet kreditoru.

Lai atspējotu kreditora pārbaudi precei, izpildiet šīs darbības.

1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Atveriet attiecīgo preci.
1. Kopsavilkuma cilnē **Pirkums** iestatiet lauku **Apstiprinātais kreditors** uz vērtību, kas nav *Tikai brīdinājums* vai *Nav atļauts*.

Lai apstiprinātu kreditoru precei, izpildiet šīs darbības.

1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Atveriet attiecīgo krājumu.
1. Darbību rūtī, cilnē **Pirkšana**, grupā **Apstiprinātais piegādātājs** atlasiet **Iestatījumi**.
1. Darbību rūtī atlasiet saraksta lapu **Apstiprinātais piegādātājs**, pievienojiet rindu režģim, un iestatiet tai šādas vērtības:

    - **Kreditors** – izvēlieties kreditoru, ko apstiprināt pašreizējai precei.
    - **Spēkā stāšanās datums** – izvēlieties pirmo datumu, kuram kreditors ir apstiprināts.
    - **Beigu datums** – izvēlieties pēdējo datumu, kuram kreditors ir apstiprināts.

Papildinformāciju skatiet [Kreditoru apstiprināšana noteiktām precēm](../../procurement/tasks/approve-vendors-specific-products.md).
