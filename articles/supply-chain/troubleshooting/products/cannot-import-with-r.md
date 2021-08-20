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
ms.openlocfilehash: efd773313f89784d8fca6b37d867e204cb2d06ab29694a19cbec7eed107a8019
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6764696"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a>Nevar importēt krājumu, izmantojot Izlaistās preces V2 elementu

KB numurs: 4611825

## <a name="symptoms"></a>Simptomi

Kad mēģināt importēt krājumu, izmantojot *Izlaistās preces V2* elementu, tiek saņemts kļūdas ziņojums, kas līdzīgs šim piemēram:

> Nevar izveidot ierakstu laukā Krājumi — izsekošanas dimensiju grupas (EcoResTrackingDimensionGroupItem). Krājuma numurs: 2040663, Partija. Ieraksts jau pastāv.

## <a name="resolution"></a>Novēršana

Lai importētu jaunas izlaistās preces, *Izlaistās preces V2* entītijas vietā jums jāizmanto *Izlaistās preces izveide V2*.
