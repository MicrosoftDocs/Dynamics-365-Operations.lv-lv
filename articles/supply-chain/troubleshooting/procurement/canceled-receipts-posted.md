---
title: Darījumus var grāmatot aizturētā grāmatas kontā
description: Ja tiek atcelta preces kvīts, sistēma ļauj darījumus grāmatot aizturētos grāmatu kontos pat, ja galvenie konti ir aizturēti
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 20df0ee4107ad62bec0dd9a683660fe2375a3dd1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477032"
---
# <a name="transactions-can-be-posted-to-a-suspended-ledger-account"></a>Darījumus var grāmatot aizturētā grāmatas kontā

## <a name="symptoms"></a>Simptomi

Ja produktu ieejas plūsma ir atcelta, sistēma ļauj grāmatot darījumus aizturētajos Virsgrāmatas kontos, pat ja galvenie konti ir aizturēti.

## <a name="reproduce-the-issue"></a>Problēmas atveide

Nākamajā procedūrā ir parādīts viens šīs problēmas atveides veids.

1. Lapā **Kreditoru parametri** cilnē **Vispārīgi** pārliecinieties, vai opcija **Grāmatot produktu ieejas plūsmu Virsgrāmatā** ir iestatīta uz *Jā*.
1. Izveidojiet pirkšanas pasūtījumu un pievienojiet pasūtījuma rindu, kurā preces daudzums ir *1 000*.
1. Apstipriniet pirkšanas pasūtījumu.
1. Grāmatojiet produktu ieejas plūsmu un pārbaudiet dokumentus.
1. Aizturiet attiecīgos galvenos kontus, *200140* un *140200*.
1. Atceliet grāmatoto produktu ieejas plūsmu.
1. Ievērojiet, ka darījumus var grāmatot aizturētajos Virsgrāmatas kontos.

## <a name="resolution"></a>Novēršana

Darījumus var grāmatot aizturētajos Virsgrāmatas kontos, kad produktu ieejas plūsmas ir atceltas, jo šī darbība ļauj labot grāmatojumus.
