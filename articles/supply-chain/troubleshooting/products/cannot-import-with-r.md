---
title: Nevar importēt krājumu, izmantojot Izlaistās preces V2 elementu
description: Nevar importēt krājumu, izmantojot Izlaistās preces V2 elementu.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended, DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8182f2f83f6a3e4cf54fe6fa64b25a2f461ff541
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026703"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a>Nevar importēt krājumu, izmantojot Izlaistās preces V2 elementu

KB numurs: 4611825

## <a name="symptoms"></a>Simptomi

Kad mēģināt importēt krājumu, izmantojot *Izlaistās preces V2* elementu, tiek saņemts kļūdas ziņojums, kas līdzīgs šim piemēram:

> Nevar izveidot ierakstu laukā Krājumi — izsekošanas dimensiju grupas (EcoResTrackingDimensionGroupItem). Krājuma numurs: 2040663, Partija. Ieraksts jau pastāv.

## <a name="resolution"></a>Novēršana

Lai importētu jaunas izlaistās preces, *Izlaistās preces V2* entītijas vietā jums jāizmanto *Izlaistās preces izveide V2*.
