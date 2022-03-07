---
title: Nav iespējams atlasīt krājuma statusa izmaiņas kā darba veidu
description: Nevarat izveidot darba veidnes rindu krājuma statusa izmaiņām, jo darba veidu izmanto tikai sistēmas procesos. Atlasiet citu darba veidu.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ad7f26f3235d15779583f9cdadeb4e6dca16242a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477018"
---
# <a name="cant-select-inventory-status-change-in-the-work-type-column"></a>Nav iespējams atlasīt krājuma statusa izmaiņas darba veida kolonnā

## <a name="symptoms"></a>Simptomi

Konfigurējot Microsoft Dynamics 365 Supply Chain Management, iespējams, saņemsit šādu kļūdas ziņojumu:

> Nevarat izveidot darba veidnes rindu krājuma statusa izmaiņām, jo darba veids nav derīgs. Atlasiet citu darba veidu.

## <a name="resolution"></a>Novēršana

Tas tiek darīts ar nolūku. *Krājumu statusa maiņas* darba veidu izmanto tikai sistēmas procesi. To nevar konfigurēt. Tā kā darba veidu saraksts ir fiksēts kā uzskaitījums, papildu ievades nevar filtrēt no **Darba veida** nolaižamās izvēlnes.
