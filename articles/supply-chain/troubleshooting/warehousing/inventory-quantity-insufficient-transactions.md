---
title: Krājuma daudzums netiek atjaunināts nepietiekamu darījumu dēļ
description: Krājuma daudzumu -1% nevar atjaunināt jo vienumam %2, kuram ir konkrēts izmērs, nepietiek krājuma transakciju.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 88130a969039dd741c8ea4fbaabe81acf0e6fb6a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476935"
---
# <a name="system-cant-update-inventory-quantity-because-of-insufficient-transactions"></a>Sistema nevar atjaunināt krājuma daudzumu, jo nepietiek transakciju

## <a name="symptoms"></a>Simptomi

Šī problēma var rasties, ja sistēma nevar atjaunināt krājumu daudzumu, jo nav pietiekoši daudz krājumu darbību, kurām ir noteiktas dimensijas. Saņemsit šādu kļūdas ziņojumu:

> Krājumu daudzums -%1 nevarēja atjaunināt %2 krājumu darbību nepietiekamā daudzuma dēļ, kas atbilst dimensijas Lielumam=%3, Krāsai=%4, Papildinājumiem=%5, Vietai=%6, Noliktavai=%7, Novietojumam=%8, Krājuma statusam=pieejams, Numura zīmei=%9, Partijas numuram=%10, Atsauces ID %11, Laidien ID %12.

## <a name="resolution"></a>Novēršana

Pārliecinieties, vai krājumu darbības fiziski nerezervē daudzumu. Piemēram, šīs darbības var atvērt kvalitātes pasūtījumus, krājumu bloķēšanas ierakstus vai izdošanas pasūtījumus.
