---
title: Vispārējā plāna parametri nepastāv
description: Mēģinot apstiprināt plānoto pasūtījumu, tiek saņemts kļūdas ziņojums, kurā norādīts, ka vispārējām plānam nav parametru.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d4b64af2e30109b8560d40c4c532504611528bbe
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294130"
---
# <a name="parameters-for-the-master-plan-dont-exist"></a>Vispārējā plāna parametri nepastāv

Kļūdas kods: SYS25368

## <a name="symptoms"></a>Simptomi

Mēģinot apstiprināt plānoto pasūtījumu saņemsit šādu kļūdas ziņojumu:

> Vispārējā plāna %1 parametri nav izveidoti.

## <a name="cause"></a>Iemesls

Konfigurācijas problēmu dēļ sistēma nevar atrast iestatījumus norādītajam plānam.

## <a name="resolution"></a>Novēršana

- Dodieties uz **Vispārējā plānošana \> Iestatīšana \> Plāni \> Vispārējie plāni** un pārliecinieties, vai pastāv plāns ar norādīto nosaukumu.
