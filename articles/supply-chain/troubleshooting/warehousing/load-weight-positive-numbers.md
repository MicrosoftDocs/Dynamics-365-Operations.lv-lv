---
title: Kravas svars var saturēt tikai pozitīvus skaitļus
description: Apstrādājot darbu starp atrašanās vietām, iespējams, saņemsit kļūdas ziņojumu par slodzes svaru un to, ka jūsu atjauninājums ir atcelts. Lai atrisinātu šo problēmu, veiciet tālāk norādītās darbības.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8ea1f6679a521e3e8683b8e5f18f509e98044414
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476972"
---
# <a name="load-weight-error-and-update-canceled-when-processing-work-between-locations"></a>Kravas svara kļūda un atjauninājuma atcelšana, apstrādājot darbu starp atrašanās vietām

## <a name="symptoms"></a>Simptomi

Ja apstrādājot darbu no pakošanas vietām uz sagatavošanas vietām, vai no sagatavošanas vietām uz pārkraušanas vietām, ir atvērts darbs, iespējams, saņemsit šādu kļūdas ziņojumu:

> Lauks 'Kravas svars'(=-%1) drīkst saturēt tikai pozitīvus skaitļus. Labojumi ir atcelti.

## <a name="resolution"></a>Novēršana

Lai labotu šo problēmu, dodieties uz **Sistēmas administrēšana \> Periodiskie uzdevumi \> Datu bāzes \> Konsekvences pārbaude** un palaidiet procesu **Noliktavas kravas svara konsekvences pārbaudei**.
