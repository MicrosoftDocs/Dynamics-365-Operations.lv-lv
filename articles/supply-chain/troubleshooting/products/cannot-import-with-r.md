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
ms.openlocfilehash: bf6eb0eb755de3f2842c235946bfd7ccad04ccf7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7474728"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a>Nevar importēt krājumu, izmantojot Izlaistās preces V2 elementu

KB numurs: 4611825

## <a name="symptoms"></a>Simptomi

Kad mēģināt importēt krājumu, izmantojot *Izlaistās preces V2* elementu, tiek saņemts kļūdas ziņojums, kas līdzīgs šim piemēram:

> Nevar izveidot ierakstu laukā Krājumi — izsekošanas dimensiju grupas (EcoResTrackingDimensionGroupItem). Krājuma numurs: 2040663, Partija. Ieraksts jau pastāv.

## <a name="resolution"></a>Novēršana

Lai importētu jaunas izlaistās preces, *Izlaistās preces V2* entītijas vietā jums jāizmanto *Izlaistās preces izveide V2*.
