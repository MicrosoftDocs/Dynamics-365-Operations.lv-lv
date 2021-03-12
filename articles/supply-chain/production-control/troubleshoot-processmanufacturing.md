---
title: Problēmu novēršana saistībā ar ražošanas procesu
description: Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar ražošanas procesu.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d999c91aa1cc14f29ebfa6be8e456e45ef0d3fa4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966184"
---
# <a name="troubleshoot-process-manufacturing"></a>Problēmu novēršana saistībā ar ražošanas procesu

Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar ražošanas procesu.

## <a name="when-i-use-the-job-card-device-to-report-a-partial-quantity-on-the-last-job-in-a-production-order-all-the-previous-jobs-on-that-order-that-have-a-status-of-in-progress-are-automatically-ended"></a>Kad es izmantoju darba kartes ierīci, lai pārskatā sniegtu daļēju daudzumu, kas ir pēdējais darbs ražošanas pasūtījumā, visi iepriekšēji darbi, kuru statuss ir nepabeigts, tiek automātiski pabeigti.

Tas tiek darīts ar nolūku. Lapā **Ražošanas pasūtījuma noklusējumi** cilnē **Ziņot kā pabeigtus** ir opcija, kas tiek saukta par **Beigu zīmes maršrutu**. Ja šī tēma ir iestatīta uz *Jā*, maršruta kartes žurnāls tiek grāmatots, kad darbinieks izmanto darba kartes ierīci vai darba kartes termināli, lai ziņotu par pēdējo operāciju. Šis žurnāls atzīmē visas operācijas kā pabeigtas un beidz visus ražošanas darbus. Ja **Beigu zīmes maršruta** opcija ir iestatīta uz *Jā*, sistēma neņem vērā darbinieka izvēlēto darba statusu brīdī, kad viņš ziņoja par pēdējo operāciju. Sistēma arī neņem vērā, vai darbinieks ziņo par pilnīgu vai daļēju daudzumu.

## <a name="when-i-attempt-a-stock-closing-i-receive-the-following-warning-message-no-execution-of-backflush-costing-calculation-with-a-date-1-matching-period-end-has-been-registered"></a>Kad es mēģinu veikt krājumu slēgšanu, tiek saņemts šāds brīdinājuma ziņojums: "nav reģistrēta atgriezeniskas izmaksu aprēķināšanas izpilde ar datumu %1, kas atbilst perioda beigām."

Laidienos pirms 10.0.13 izlaiduma, ja neizmantojat taupīgo ražošanas izmaksu plūsmu, krājuma slēgšanas laikā saņemat šādu kļūdainu brīdinājuma ziņojumu:

> Jūs gatavojaties izpildīt Krājumu slēgšanu ar datumu %1. Nav reģistrēta neviena Atgriezeniska izmaksu aprēķināšana ar datumu %1 salīdzināšanas perioda beigas. Lūdzu atceraties veikt Atgriezenisko izmaksu aprēķināšanu ar datumu %1 salīdzināšanas perioda beigas. Krājumu novērtējums, pārdoto preču izmaksas un novirzes Apakšgrāmatās vai Virsgrāmatā var nebūt pareizas, kamēr tās nav izpildītas.

Šī problēma ir novērsta, 10.0.13 laidienā un jaunākos. Papildinformāciju skatiet [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).
