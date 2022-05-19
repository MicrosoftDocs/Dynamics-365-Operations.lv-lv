---
title: Iestatījumu stornēšana žurnālos un rindās
description: Šajā tēmā ir aplūkots, kāpēc stornēts ieraksts, kas ievadīts virsgrāmatas žurnālā, var nebūt iekļauts iegrāmatotajā transakcijā.
author: kweekley
ms.date: 04/29/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ff8c0bda8e750e95261039b373cfb96a76034f6f
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2022
ms.locfileid: "8724450"
---
# <a name="reverse-settings-on-journals-and-lines"></a>Iestatījumu stornēšana žurnālos un rindās

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aplūkots, kāpēc stornēts ieraksts, kas ievadīts virsgrāmatas žurnālā, var nebūt iekļauts iegrāmatotajā transakcijā.  

## <a name="symptom"></a>Simptoms

Virsgrāmatas žurnālā ir iekļauts stornēšanas ieraksts un stornēšanas datums žurnālā. Grāmatojot žurnālu, neviens dokuments netiek stornēts. Kādēļ tā notiek?

## <a name="resolution"></a>Novēršana

Grāmatojot žurnālu, stornēšanas process ņem vērā tikai iestatījumus **Stornēšanas ieraksts** un **Stornēšanas datums** dokumenta sadaļā **Rindas**. Šī pieeja ļauj žurnālam iekļaut dažus dokumentus, kas ir atzīmēti stornēšanai, un citus dokumentus, kas nav atzīmēti.

Žurnāla vērtības tiek izmantotas tikai kā noklusējuma vērtības, pievienojot *jaunas* rindas. Vērtību maiņa žurnālā neietekmē esošās rindas. Šajā piemērā vispirms tika ievadītas dokumenta rindas. Ievadot rindas informāciju pirms žurnāla noformēšanas par stornējamu žurnālu, apzīmējums kā stornēšanas ieraksts un datums netiks attiecināts uz esošajām rindām.

Mainot stornēšanas ierakstu vai stornēšanas datumu esošā rindā, attiecīgās izmaiņas tiek izplatītas arī citās tā paša dokumenta rindās. Lai optimizētu veiktspēju, pēc izmaiņu izplatīšanas citās rindās režģis netiek atsvaidzināts. Atjauninātās vērtības var parādīt, atsvaidzinot režģi.


