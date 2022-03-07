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
ms.openlocfilehash: d039b79684f87e7791fb9dae7cbdc6ced220bc092d9a0ab624616c1c345986da
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756779"
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
